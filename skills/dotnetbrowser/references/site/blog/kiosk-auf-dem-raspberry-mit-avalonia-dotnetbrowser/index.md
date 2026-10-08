# Kiosk-App auf dem Raspberry Pi mit Avalonia und DotNetBrowser

Diese Anleitung beschreibt, wie man eine Kiosk-Anwendung für den Raspberry Pi 5
mit Avalonia und DotNetBrowser entwickelt.

Die Anwendung nutzt Avalonia für die native Desktop-Oberfläche unter .NET und
DotNetBrowser, um Webinhalte über eine Chromium-Engine einzubetten und zu
steuern.

Dabei richtest du die Entwicklungsumgebung ein, konfiguriert das Betriebssystem
und stellst eine Kiosk-Anwendung für ein Touchdisplay bereit.

## Was du benötigst

Du benötigst einen **Raspberry Pi 5**, idealerweise mit **8 oder 16 GB RAM**.
Chromium, auf dem DotNetBrowser basiert, braucht zur Laufzeit spürbar
Arbeitsspeicher – zusätzlicher RAM verbessert daher die Reaktionsfähigkeit
der Anwendung.

Die Entwicklung und Bereitstellung beginnen auf deinem normalen Rechner. Du
kannst unter Windows, macOS oder Linux arbeiten, solange das .NET-8-SDK
installiert ist. Verwende dafür eine beliebige moderne IDE deiner Wahl:

* Visual Studio 2022 oder neuer  
* Visual Studio Code  
* JetBrains Rider

## Erstellen der Anwendung

### DotNetBrowser-Vorlagen installieren

Die DotNetBrowser-Vorlagen sind Projektgerüste, mit denen sich eine neue
Avalonia-Anwendung mit DotNetBrowser schnell erstellen lässt.

Öffne in deiner Entwicklungsumgebung die Kommandozeile und installiere die
DotNetBrowser-Vorlagen:

```shell
dotnet new install DotNetBrowser.Templates
```

### Testlizenz anfordern

Bevor du ein neues Projekt erstellen kannst, benötigst du eine
DotNetBrowser-Lizenz. DotNetBrowser ist eine kommerzielle Bibliothek. Für
Testzwecke kannst du eine kostenlose 30-Tage-Testlizenz anfordern.

Für die kostenlose 30-Tage-Testlizenz füllst du das Webformular aus. Der
Lizenzschlüssel wird dir anschließend per E-Mail zugeschickt.



### Anwendung erzeugen

Verwende die Vorlage `dotnetbrowser.avalonia.app`, um ein Avalonia-Startprojekt
mit allen erforderlichen Abhängigkeiten zu erzeugen. Führe dazu folgenden
Befehl aus:

```shell
dotnet new dotnetbrowser.avalonia.app -o RaspberryKiosk -li <your_license_key>
```

Der Befehl legt das Projekt im Ordner RaspberryKiosk an. Standardmäßig wird
net8.0 als Target-Framework verwendet. Über den Parameter `-f` kannst du das
Ziel auf net9.0, net7.0 oder net6.0 ändern:

```shell
dotnet new dotnetbrowser.avalonia.app -o RaspberryKiosk -li <your_license_key> -f net9.0
```

### Anwendungsfenster konfigurieren

Die Projektvorlage erzeugt bereits ein funktionsfähiges Avalonia-Fenster mit
eingebettetem **DotNetBrowser**-Control und übernimmt dessen Initialisierung im
Code-Behind. Für den Kiosk-Einsatz muss dieses Fenster nur noch entsprechend
angepasst werden.

Da die Anwendung im Kioskmodus läuft, muss sie im Vollbild starten, im
Vordergrund bleiben und verhindern, dass der Nutzer sie minimiert oder
schließt. In `MainWindow.axaml` konfigurierst du das Hauptfenster daher ohne
Rahmen, im Vollbild, ohne Fensterdekorationen und ohne Zugriff auf die
Taskleiste. Ergänze dazu in `MainWindow.axaml` folgende Attribute:

```xml {hl_lines=["3-7"]}
<Window
    ... 
    WindowState="FullScreen"
    Topmost="True"
    ExtendClientAreaToDecorationsHint="True"
    ExtendClientAreaChromeHints="NoChrome"
    ShowInTaskbar="False"
>
    <app:BrowserView x:Name="BrowserView"/>
</Window>
```

### Webview konfigurieren

Hier startest du die Chromium-Engine und passt einige Einstellungen an, die das
Verhalten auf dem Raspberry Pi beeinflussen. Zwei davon sind besonders relevant:

* Der Rendering-Modus `HardwareAccelerated` ermöglicht es Chromium, direkt über die GPU in das Fenster zu zeichnen – das ist schneller und entlastet die CPU.  
* Pinch-to-Zoom deaktivieren (`--disable-pinch`) — verhindert, dass Nutzer versehentlich den Seitenzoom verändern.

**MainWindow.xaml.cs**

```java
public partial class MainWindow : Window
{
    private readonly IBrowser browser;
    private readonly IEngine engine;

    public MainWindow()
    {          
        // Chromium-Prozess starten.
        EngineOptions engineOptions = new EngineOptions.Builder
        {
            LicenseKey = "",
            RenderingMode = RenderingMode.HardwareAccelerated,
            ChromiumSwitches =
            {
                "--disable-pinch",
            }
        }.Build();
        engine = EngineFactory.Create(engineOptions);

        // Browser-Instanz erstellen.
        browser = engine.CreateBrowser();

        // Avalonia-Komponente initialisieren.
        InitializeComponent();

        // BrowserView-Control initialisieren.
        BrowserView.InitializeFrom(browser);

        // Kontextmenü deaktivieren.
        browser.ShowContextMenuHandler = null;

        // Zu einer beliebigen Seite navigieren, um die Funktion zu prüfen.
        browser.Navigation.LoadUrl("https://google.com");
     }
 }
```

![A web page opened in the full-screen Avalonia window](https://teamdev.com/dotnetbrowser/blog/kiosk-auf-dem-raspberry-mit-avalonia-dotnetbrowser/web-ui-in-avalonia.webp)
<p class="image-caption">A web page opened in the full-screen Avalonia
window.</p>

### Debug-Schließen-Button hinzufügen

Da der Kiosk im Vollbild ohne Systemsteuerung läuft, gibt es während der
Entwicklung keine einfache Möglichkeit, die Anwendung zu schließen. Um das
Debugging zu erleichtern, kannst du eine kleine Debug-Leiste einbauen, die nur
in Debug-Builds sichtbar ist.

![Eine automatisch eingeblendete Leiste für den Debug-Modus](https://teamdev.com/dotnetbrowser/blog/kiosk-auf-dem-raspberry-mit-avalonia-dotnetbrowser/debug-bar.webp)
<p class="image-caption">Eine automatisch eingeblendete Leiste für den
Debug-Modus.</p>

Verwende die Direktive `#if DEBUG`, um nach dem Laden der Seite ein kleines
JavaScript-Snippet einzufügen. Das Skript erzeugt einen fixierten Button auf
dem Bildschirm, der sichtbar bleibt und die Anwendung beim Anklicken beendet. So
bleibt der Release-Build weiterhin abgesichert, während du im Debug-Modus eine
sichere Möglichkeit zum Beenden hast.

**MainWindow.xaml.cs**

```java
browser.navigation.FrameDocumentLoadFinished += (s, e) => 
{
#if DEBUG
    IFrame frame = e.Frame;

    IJsObject window = args.Frame.ExecuteJavaScript<IJsObject>("window").Result;
    // Funktion zum Beenden der Anwendung hinzufügen.
    window.Properties["closeApplication"] = 
         () => Dispatcher.UIThread.InvokeAsync(Close);

    // Debug-Leiste mit einem Schließen-Link hinzufügen.
    browser.MainFrame.ExecuteJavaScript<>(@" 
        (() => {
          const bar = document.createElement('div');
          Object.assign(bar.style, {
            position: 'fixed',
            top: '0',
            left: '0',
            width: '100%',
            padding: '5px 0 5px 0px',
            background: 'pink',
            textAlign: 'center',
            zIndex: '9999'
          });
          bar.innerHTML = 
             'DEBUG MODE. <a onclick="closeApp()">Close application.</a>';
          document.body.appendChild(bar);
        })();
    ");
#else
#endif
};
```

### Webseite hinzufügen

Es gibt mehrere Möglichkeiten, Webseiten in DotNetBrowser auf dem Raspberry Pi
zu laden – je nachdem, wie der Kiosk auf seine Inhalte zugreifen soll:

* **Eine entfernte URL laden** – die einfachste Option, geeignet für Kiosksysteme mit durchgehender Internetverbindung.  
* **Lokalen Webserver betreiben** – geeignet für Offline-Szenarien, bei denen der Browser die Seiten direkt vom selben Gerät lädt  
* **Lokale HTML-Dateien öffnen** – für einfache Fälle kannst du das `file://` Protokoll verwenden. Da Chromium jedoch den Zugriff auf lokale Ressourcen einschränkt, ist diese Variante für komplexere Anwendungen weniger geeignet.  
* **Seiten aus den App-Ressourcen ausliefern** – mit den [Scheme-Interceptoren][guides-interceptors] von DotNetBrowser kannst du Inhalte direkt aus den Ressourcen deiner Anwendung bereitstellen.

### Laufzeit- und Deployment-Konfiguration

Linux-Systeme haben standardmäßig häufig keine .NET-Laufzeitumgebung
installiert, was das Deployment erschweren kann. Um diese Abhängigkeit zu
vermeiden, kannst du die Anwendung als self-contained build veröffentlichen –
also als Paket, das die .NET-Runtime direkt mitliefert. Dadurch kann der
Raspberry Pi den Kiosk ohne zusätzliche Einrichtung ausführen, was das
Deployment für unbeaufsichtigte Geräte einfacher und zuverlässiger macht.

Füge in der Datei `RaspberryKiosk/RaspberryKiosk.csproj` den Runtime-Identifier
`linux-arm64` hinzu und konfiguriere das Projekt als *self-contained*:

```xml {hl_lines=["5-7"]}
<Project Sdk="Microsoft.NET.Sdk">
  <PropertyGroup>
    <OutputType>WinExe</OutputType>
    <TargetFramework>net8.0</TargetFramework>
    <RuntimeIdentifiers>win-x64;linux-arm64</RuntimeIdentifiers>
    <SelfContained>true</SelfContained>
    <PublishSingleFile>true</PublishSingleFile>
  </PropertyGroup>
</Project>
```

Diese Konfiguration bündelt die vollständige .NET-8-Runtime und
veröffentlicht die Anwendung als ausführbare Einzeldatei.

### Anwendung veröffentlichen

Um die Anwendung für den Raspberry Pi vorzubereiten, veröffentlichst du sie
für die Linux-ARM64-Plattform mit folgendem Befehl:

```shell
dotnet publish RaspberryKiosk/RaspberryKiosk.csproj -c Release -r linux-arm64 --self-contained true -o ./publish/rpi
```

Dabei entsteht eine ausführbare Datei im Verzeichnis `./publish/rpi`, die
direkt auf dem Raspberry Pi 5 eingesetzt werden kann.

## Raspberry Pi konfigurieren

Damit das System effizient und stabil bleibt, läuft der Kiosk auf Raspberry Pi
OS Lite – mit nur den Komponenten, die für die grafische Ausgabe notwendig
sind. Anstelle einer vollständigen Desktop-Umgebung verwendest du einen
X-Server und einen minimalen Window-Manager.

Der X-Server ist der Teil von Linux, der die grafische Ausgabe bereitstellt und
Eingabegeräte wie Tastatur und Maus verarbeitet. Er zeichnet keine Fenster
selbst, sondern verwaltet lediglich die Anzeigefläche. Ein Window-Manager sitzt
darüber und steuert, wie Fenster dargestellt werden – Position, Fokus, Rahmen
und Stapelreihenfolge.

Dieses schlanke Setup verhindert, dass Nutzer die Kiosk-Anwendung verlassen
können, und vermeidet gleichzeitig den zusätzlichen Overhead einer kompletten
Desktop-Umgebung.

### Betriebssystem installieren

Folge der [offiziellen Anleitung][raspberry-guide] und installiere Raspberry Pi
OS Lite (64-bit) auf deinem Gerät. Das Image ist im offiziellen Raspberry Pi
Imager verfügbar:

![Raspberry Pi OS Lite im offiziellen Imager.](https://teamdev.com/dotnetbrowser/blog/kiosk-auf-dem-raspberry-mit-avalonia-dotnetbrowser/pi-imager-screenshot.webp)
<p class="image-caption">Raspberry Pi OS Lite im offiziellen Imager.</p>

### Systemabhängigkeiten installieren

Um Avalonia-Anwendungen mit DotNetBrowser unter Raspberry Pi OS Lite
auszuführen, installierst du den X-Server sowie einen leichtgewichtigen
Window-Manager:

```shell
sudo apt update && sudo apt upgrade -y
sudo apt install --no-install-recommends xserver-xorg xinit openbox gldriver-test
```

> Das Paket `gldriver-test` aktiviert die GPU-Nutzung im X-Server.  

Füge anschließend deinen Raspberry

```shell
sudo useradd -G tty username
```

### Chromium-Abhängigkeiten installieren

DotNetBrowser benötigt mehrere Chromium-Abhängigkeiten. Unter Raspberry Pi OS
Lite installierst du sie mit folgendem Befehl:

```shell
sudo apt install libgtk2.0-0 \
        libgtk-3-0 \
        libgbm1 \
        libnotify4 \
        libnss3 \
        libxss1 \
        libasound2 
```

### Anwendung bereitstellen

Nun kannst du die veröffentlichte Anwendung vom Entwicklungsrechner auf den
Raspberry Pi übertragen. Dazu kannst du einen USB-Stick verwenden oder die
Dateien per SCP kopieren:

```shell
scp -r ./publish/rpi username@<your-host-name>:~/
```

Gib der Datei auf dem Raspberry Pi Ausführungsrechte:

```shell
cd rpi
chmod +x RaspberryKiosk
```

Jetzt kannst du die Anwendung starten. Wechsle in das Verzeichnis `~/rpi` und
führe `startx` aus, um sie in einer X-Server-Session zu starten:

```shell
startx ./RaspberryKiosk
```

### Autostart konfigurieren

Die Kiosk-Anwendung soll nach dem Booten automatisch starten. Lege dafür im
Home-Verzeichnis ein einfaches Skript namens `start-kiosk.sh` an, das die
Anwendung startet:

```shell
#!/bin/bash
cd ~/rpi
startx ./RaspberryKiosk
```

Und mache es ausführbar:

```shell
chmod +x ~/start-kiosk.sh
```

Als Nächstes konfiguriert du das System so, dass dein Skript beim Booten
ausgeführt wird. Füge dazu folgenden Abschnitt in die Datei `~/.bashrc` ein:

```shell
if [ "$(tty)" = "/dev/tty1" ]; then
  ~/start-kiosk.sh
fi
```

Und zum Schluss richtest du die automatische Anmeldung ein. Öffne dazu das Tool
`raspi-config`:

```shell
sudo raspi-config
```

Wähle im Tool **„System Options“** > **„Auto Login“**. Bestätige im
Dialog mit **„Yes“** und drücke Enter, um die Änderung zu speichern.
Anschließend wähle **„Finish“**, um das Tool zu verlassen.



## Launching the kiosk

Now, you can restart the Raspberry Pi and the kiosk application will be
automatically launched on the start.

![The kiosk app made with Avalonia and DotNetBrowser launched on Raspberry Pi 5](https://teamdev.com/dotnetbrowser/blog/kiosk-auf-dem-raspberry-mit-avalonia-dotnetbrowser/avalonia-kiosk-raspberry.webp#medium)
<p class="image-caption">The kiosk app made with Avalonia and DotNetBrowser
launched on Raspberry Pi 5.</p>

## Fazit

Mit Avalonia und DotNetBrowser unter Raspberry Pi OS Lite entsteht ein schlankes
und zuverlässiges Kiosksystem. Du steuerst sowohl Hardware als auch Software,
hältst den Ressourcenbedarf gering und lässt die Anwendung nach dem Boot
automatisch starten. Da UI und Deployment getrennt sind, lassen sich Updates
gezielt und ohne Aufwand ausrollen.

Der Kiosk kann lokale HTML-Dateien oder entfernte Seiten laden, sodass sich die
angezeigten Inhalte zentral verwalten lassen. Das Setup eignet sich für Digital
Signage, Dashboards oder allgemein für Displays, die regelmäßig aktualisierte
Inhalte benötigen, ohne manuelle Pflege.

[guides-interceptors]: https://teamdev.com/dotnetbrowser/docs/guides/gs/engine/#intercept-request-per-uri-scheme
[raspberry-guide]: https://www.raspberrypi.com/documentation/computers/getting-started.html#installing-the-operating-system
