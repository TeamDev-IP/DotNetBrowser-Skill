# DotNetBrowser oder WebView2: Ein Vergleich für Entwickler

Wenn es um eingebettete Browser geht, bietet die Branche die unterschiedlichsten
Lösungen: frei und kommerziell, Open Source und proprietär. Sie unterscheiden
sich darin, was sie können, wie sie genutzt werden und welche zusätzlichen
Services dazugehören. In diesem Artikel helfen wir Ihnen bei der Auswahl der
richtigen Lösung.

Im Artikel [DotNetBrowser oder CefSharp][dotnetbrowser-vs-cefsharp-article]
haben wir das Open-Source-Projekt CefSharp mit DotNetBrowser verglichen und
erläutert, wie man sich entscheiden kann.

Heute nehmen wir den proprietären WebView2 unter die Lupe und argumentieren,
dass DotNetBrowser für den kommerziellen Einsatz besser geeignet ist. Wir
beginnen mit organisatorischen und rechtlichen Aspekten. Danach gehen wir auf
die funktionalen Unterschiede ein.

Die Migration zu DotNetBrowser ist unkompliziert. Sie finden alle Details
im [Migration Guide][migration-guide], der Sie durch den Prozess führt und die
wichtigsten Punkte erklärt.

## In a nutshell


<div class="table-wrapper comparison-table">

|                              | <img class="product-logo" src="/dotnetbrowser/blog/dotnetbrowser-or-webview2/edge-logo.svg" alt="CEF logo" width="22" height="22"/> WebView2 | <img class="product-logo" src="/images/product-logos/dotnetbrowser.svg" alt="DotNetBrowser logo" width="22" height="22"/> DotNetBrowser |
|:-----------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------|
| Lizenz                       | Proprietär                                                                                                                                   | Kommerziell                                                                                                                             |
| Unterstützte Betriebssysteme | Nur Windows                                                                                                                                  | Windows, macOS, Linux                                                                                                                   |
| Unterstützte UI-Toolkits     | WinForms, WPF, Win UI 3, MAUI                                                                                                                | WinForms, WPF, Avalonia, Win UI 3                                                                                                       |
| [Datensammlung][privacy]     | Ja                                                                                                                                           | Nein                                                                                                                                    |
| Headless Mode                | Nein                                                                                                                                         | Ja, läuft in Konsole oder als Service                                                                                                   |
| [Support][support]           | Nein                                                                                                                                         | Ja, vertraulich, mit SLA                                                                                                                |

</div>

DotNetBrowser und WebView2 sind ausgereifte Lösungen von kommerziellen
Unternehmen mit umfangreicher Erfahrung in diesem Bereich. Damit erhalten Sie
eine Softwarelösung, die funktioniert und nicht von einer Open-Source-Community
abhängt.

Wählen Sie WebView2, wenn:

* Sie ausschließlich freie Software einsetzen dürfen.
* Sie die Vorteile der Evergreen-Distribution nutzen möchten.
* Es für Sie in Ordnung ist, dass Microsoft Daten der Endanwender sammelt.

Wählen Sie DotNetBrowser, wenn:

* Sie ein individuelles Feature benötigen.
* Sie Unterstützung bei der Nutzung des Produkts wünschen.
* Sie Bugs vertraulich melden und beheben lassen möchten.
* Sie Kontrolle über die Datensammlung bei Endanwendern haben möchten.
* Sie eine Anwendung ohne UI ausführen müssen.
* Sie Linux und macOS unterstützen möchten.
* Sie programmgesteuertes Drucken benötigen.

## Unterschiedliche Ansätze

WebView2 ist ein Control von Microsoft. Es ist kostenlos, aber – wie man es von
Microsoft erwartet – auch proprietär. Es ersetzt das alte, auf Trident
basierende WebView und setzt stattdessen auf Edge.

WebView2 ist ein Control: ein Eintrag in der Visual-Studio-Toolbox, Klassen aus
`Microsoft.Web.WebView2.Core.dll`. Es ist jedoch kein Microsoft-Produkt wie 
Office oder PowerBI. Daher gibt es keine Kundenbetreuung, keinen Support 
und keine Hilfestellung.

DotNetBrowser ist ein Produkt von TeamDev, einem Unternehmen, das sich auf
Browser-Embedding spezialisiert hat. Angefangen haben wir 2004 mit Internet
Explorer, später mit Safari und WebKit – bis wir uns 2013 auf Chromium
festgelegt haben.

2015 haben wir DotNetBrowser eingeführt. Es ist ein kommerzielles Produkt, das
für den kommerziellen Einsatz entwickelt wurde. Neben der Software und der
Dokumentation umfasst das Angebot einen dedizierten Kundenbetreuer, technischen
[Support][getting-help] 
und [Premium-Services][premium-services].

## Unterschiede für Unternehmen

### Fixes, Features und Support

Wie bekommen Sie Hilfe, wenn Sie einen Bug finden oder ein Feature benötigen?
Werfen wir einen Blick darauf, was WebView2 und DotNetBrowser bieten.

WebView2 sammelt Feedback von der Öffentlichkeit in einem speziellen
GitHub-Repository. Wenn Sie etwas melden möchten, erstellen Sie dort ein Issue.
Wenn Microsoft-Entwickler Ihren Report für wichtig halten, übertragen sie ihn in
ihr internes System. Das erkennen Sie am Label „tracked“.

Die Entwickler von Microsoft reagieren schnell auf neue Meldungen, aber die
Bearbeitung dauert deutlich länger. Zum Zeitpunkt des Schreibens blieben fast
80 % der „tracked“-Issues länger als 6 Monate ungelöst.

DotNetBrowser verfügt über ein privates Helpdesk-System, in dem Meldungen von
Kunden vertraulich bleiben. Die garantierte erste Reaktionszeit (SLA) beträgt
einen Geschäftstag.

Der technische Support umfasst: Hilfe bei der Nutzung des Produkts,
Unterstützung beim Troubleshooting, Bugfixes und die Berücksichtigung von
Feature-Requests. Alle Ihre Support-Anfragen werden direkt von
DotNetBrowser-Entwicklern bearbeitet.

### Privacy der Endanwender

> Dieser Artikel wurde im Oktober 2022 verfasst und beschreibt die EULA-Version zu diesem Zeitpunkt.

Wenn ein Endanwender WebView2 in seiner Umgebung installiert, zeigt der
Installer die EULA an. Zwei Punkte könnten für Sie relevant sein:

1. Microsoft darf Informationen über Ihre Endanwender sammeln.
2. Sie sind verpflichtet, die Anwender darüber zu informieren.

Abschnitt 3.a der EULA besagt, dass WebView2 Informationen über Sie und die
Nutzung durch den Endanwender erfassen darf. Diese Informationen können
anschließend an Microsoft gesendet werden.

Die Tatsache, dass Microsoft Informationen der Endanwender sammelt, verpflichtet
Sie dazu, die entsprechende Mitteilung anzuzeigen und deren Zustimmung
einzuholen (Abschnitt 9 der EULA).

DotNetBrowser sammelt keine Informationen über Sie oder Ihre Endanwender.
Außerdem verhindert es die Datensammlung durch Google. Mehr dazu, wie
DotNetBrowser mit Daten umgeht und Ihnen Kontrolle über die Privatsphäre gibt,
finden Sie in
den [Privacy Practices][privacy-practices].

## Technische Unterschiede

Aus technischer Sicht unterscheiden sich DotNetBrowser und WebView2 nicht
grundlegend. Beide haben eine ähnliche Architektur, bei der Chromium in einem
separaten Prozess läuft. Beide haben Hunderte Features, von denen sich viele
überschneiden.

Die Unterschiede existieren jedoch – und sie können entscheidend sein, wenn Sie
die passende Lösung auswählen müssen. Werfen wir also einen genaueren Blick
darauf.

### Distribution und Deployment

Sie können WebView2 Runtime zusammen mit Ihrer Anwendung ausliefern oder die
Version nutzen, die beim Endanwender bereits installiert ist. Diese Modi heißen
Fixed-Version und Evergreen.

Im Fixed-Version-Mode kontrollieren Sie die Version von WebView2 in Ihrer
Anwendung – gut für Stabilität. Im Evergreen-Mode überlassen Sie Microsoft die
Logistik und Updates und reduzieren die Größe Ihrer Software.

DotNetBrowser muss mit Ihrer Anwendung ausgeliefert werden. Das ist der einzige
Distribution-Mode, den es out of the box gibt.

### Chrome extensions

Sowohl DotNetBrowser als auch WebView2 unterstützen Extensions. Während WebView2
nur sehr grundlegende Funktionen bereitstellt, gibt DotNetBrowser Entwicklern
mehr Optionen und volle Kontrolle über den Lebenszyklus und die Aktivitäten von
Extensions.

In WebView2 kann ein Entwickler eine Extension aus einer entpackten CRX-Datei
installieren, die Extension aktivieren/deaktivieren und wieder deinstallieren.

In DotNetBrowser kann ein Entwickler eine Extension direkt aus der CRX-Datei
installieren, programmatisch auf das Extension-Icon „klicken“, mit einem Popup
interagieren und neue „Tabs“ handhaben, die eine Extension öffnet.

Darüber hinaus können Sie Endanwendern erlauben, direkt mit Extensions zu
arbeiten:

* Nutzung über den Chrome Web Store.
* Anzeige des Extension-Icons mit Badges und Labels.
* Darstellung von Popups und Tabs, die durch die Extension geöffnet werden.

Lesen Sie mehr im [Guide zu Extensions][extensions-guide]
und [probieren Sie es praktisch aus][extensions-article].

### Betrieb ohne UI

Für Use Cases wie Automatisierung oder PDF-Generierung ist keine
Benutzeroberfläche erforderlich. Hier ist ein Headless Mode einfacher und
effizienter.

WebView2 unterstützt den Betrieb ohne UI nicht, da ein Anwendungsfenster
erforderlich ist.

In DotNetBrowser funktioniert das out of the box. Sie können es in einer
Konsolenanwendung, in einem Webserver oder sogar als Windows-Service nutzen. Zum
Beispiel so:

```cs
using (IEngine engine = EngineFactory.Create())
{
    using (IBrowser browser = engine.CreateBrowser())
    {
        browser.Navigation.LoadUrl("https://teamdev.com/dotnetbrowser").Wait();
    }
}
```

### Linux und macOS

Im Jahr 2024 hat Microsoft den Plan offiziell verworfen, WebView2 für macOS und
Linux zu unterstützen.

DotNetBrowser ist eine plattformübergreifende Bibliothek, die auf Windows, macOS
und Linux läuft. Nutzen Sie es mit 
[Avalonia UI][avalonia] 
oder in [Server-Anwendungen][console].

### WPF und überlappende Controls

In WPF ist es unmöglich, ein beliebiges Control über ein WebView2-Control zu
legen. Das liegt an den nativen Einschränkungen von WPF und daran, wie WebView2
funktioniert.

WPF unterstützt kein Overlapping zwischen Bereichen, die in unterschiedlichen
Fenstern gerendert werden, und WebView2 bettet genau ein solches Fremd-Fenster
in ein WPF-Control ein.

Für DotNetBrowser ist das kein Problem. Neben der Nutzung eines nativen Fensters
wie WebView2 kann es auch direkt im WPF-Fenster rendern.

Das nennt sich Off-Screen Rendering Mode. In diesem Modus werden die gerenderten
Pixel in den Speicherprozess von .NET kopiert und in einem regulären WPF-Widget
angezeigt.

### JavaScript aus .NET aufrufen

In beiden Lösungen können Sie JavaScript direkt aus .NET-Code ausführen. Der
Unterschied liegt darin, was passiert, wenn das Ergebnis von Chromium zurück in
die .NET-Welt übertragen wird.

WebView2 konvertiert das Ergebnis zu JSON:

```cs
string result = await coreWebView2.ExecuteScriptAsync(@"'example'");
Debug.Assert(result == "\"example\"");
```

DotNetBrowser konvertiert automatisch 
[einfache Typen][javascript]. Komplexe Typen 
werden durch Proxies für die tatsächlichen V8-Objekte ersetzt:

```cs
string title = await browser.MainFrame.ExecuteJavaScript<string>("document.title");
IJsObject window = await browser.MainFrame.ExecuteJavaScript<IJsObject>("window");

// Or just use dynamic types.
dynamic document = browser.MainFrame.ExecuteJavaScript("document").Result;
document.write("Hello world!");
```

### .NET aus JavaScript aufrufen

Beide Lösungen erlauben es, .NET-Objekte in JavaScript verfügbar zu machen – mit
einem Haken.

In WebView2 muss ein injected Object COM-visible sein und IDispatch
implementieren. Diese Anforderung schränkt ein, was Sie injizieren können, und
erzeugt viel Boilerplate Code.

In DotNetBrowser können Sie [beliebige Objekte injecten][js-to-net]: 
Standard-.NET-Objekte, Collections und sogar WPF-Controls. In JavaScript haben 
Sie Zugriff auf die öffentlichen Member und indizierten Properties 
des injecteten Objekts.

### Netzwerk-Intercepting

WebView2 hat keine API zum Abfangen, Filtern oder Modifizieren von
HTTP-Requests.

DotNetBrowser hingegen bietet umfangreiche Funktionen für den Umgang mit
HTTP-Traffic. Damit können Sie u. a. Folgendes implementieren:

* [HTTP-Requests filtern][navigation-filtering].
* [HTTP-Requests umleiten][before-url-request].
* [HTTP-Request-][before-start-transaction]
  und [Response-Header][receive-headers] überschreiben.
* [Upload-Daten überschreiben][before-upload].
* [Cookies filtern][suppress-cookies].

Weitere Beispiele für Networking mit DotNetBrowser finden Sie in unserem
[GitHub][examples-network].

### Printing API

WebView2 verfügt über eine eingeschränkte Printing API. Sie kann in PDF drucken
und erlaubt die Manipulation weniger Einstellungen. Leider ist sie ziemlich
limitiert:

* Sie können keinen spezifischen Systemdrucker auswählen.
* Sie können keine Seitenbereiche festlegen.
* Sie können die Druckdialoge, die dem Anwender angezeigt werden, nicht 
  kontrollieren.

DotNetBrowser bietet vollständige Kontrolle über den Druckprozess. Sie können:

* Einen Drucker auswählen.
* Druck, der durch JavaScript oder .NET-Code initiiert wird, behandeln.
* Die Fähigkeiten eines Druckers einsehen, um die Nutzung nicht unterstützter 
  Features zu vermeiden.
* Druckeinstellungen konfigurieren, inkl. Seitenbereiche, Papiergröße, Ränder, 
  Kopf- und Fußzeilen usw.

## Kostenlos ausprobieren

Holen Sie sich Ihre kostenlose Lizenz und wählen Sie einen unserer Quickstarts. 



Es dauert 5 Minuten, um mit DotNetBrowser zu starten:

* [DotNetBrowser in WPF][wpf]
* [DotNetBrowser in Avalonia][avalonia]
* [DotNetBrowser in WinForms][winforms]
* [DotNetBrowser in the console][console] — nützlich für Windows-Services 
  und Server-Anwendungen.

[extensions-article]: https://teamdev.com/dotnetbrowser/blog/chrome-extensions-in-dotnetbrowser/
[extensions-guide]: https://teamdev.com/dotnetbrowser/docs/guides/gs/extensions/
[dotnetbrowser-vs-cefsharp-article]: https://teamdev.com/dotnetbrowser/blog/dotnetbrowser-or-cefsharp/
[privacy]: https://teamdev.com/dotnetbrowser/blog/dotnetbrowser-or-webview2/#privacy-of-end-users
[support]: https://teamdev.com/dotnetbrowser/blog/dotnetbrowser-or-webview2/#fixes-features-and-assistance
[migration-guide]: https://teamdev.com/dotnetbrowser/blog/from-webview2-to-dotnetbrowser-part-1/
[getting-help]: https://teamdev.com/dotnetbrowser/#getting-help
[premium-services]: https://teamdev.com/dotnetbrowser/#getting-help
[privacy-practices]: https://teamdev.com/dotnetbrowser/docs/guides/privacy/
[javascript]: https://teamdev.com/dotnetbrowser/docs/guides/gs/javascript/
[navigation-filtering]: https://teamdev.com/dotnetbrowser/docs/guides/gs/navigation/#filtering-resources
[before-url-request]: https://teamdev.com/dotnetbrowser/docs/guides/gs/network/#before-url-request
[before-start-transaction]: https://teamdev.com/dotnetbrowser/docs/guides/gs/network/#before-start-transaction
[receive-headers]: https://teamdev.com/dotnetbrowser/docs/guides/gs/network/#receive-headers
[before-upload]: https://teamdev.com/dotnetbrowser/docs/guides/gs/network/#before-send-upload-data
[suppress-cookies]: https://teamdev.com/dotnetbrowser/docs/guides/gs/cookies/#suppressing-cookies
[examples-network]: https://github.com/TeamDev-IP/DotNetBrowser-Examples#network
[wpf]: https://teamdev.com/dotnetbrowser/docs/quickstart/wpf/
[avalonia]: https://teamdev.com/dotnetbrowser/docs/quickstart/avalonia/
[winforms]: https://teamdev.com/dotnetbrowser/docs/quickstart/winforms/
[console]: https://teamdev.com/dotnetbrowser/docs/quickstart/console/
[js-to-net]: https://teamdev.com/dotnetbrowser/docs/guides/gs/javascript/#javascript-to-net
