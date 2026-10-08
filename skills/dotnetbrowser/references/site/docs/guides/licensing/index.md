
# Licensing

**Lead**
This guide focuses on technical aspects of different license types.


For pricing information and details on terms and conditions, see the [Licensing and Pricing](https://teamdev.com/dotnetbrowser#licensing-and-pricing)
section.

**Note**
DotNetBrowser needs a license key which represents a string with combination of letters and digits. Follow the instructions outlined in this [article](https://teamdev.com/dotnetbrowser/docs/guides/installation/license/).


## Commercial licenses

When you purchase a commercial license, we email you with a license key.

You can use this license key both for development purposes and distribution of our library as part of your application.

### Indie license

This license is issued to a person.

It includes a 1 year of [Standard Support](https://teamdev.com/dotnetbrowser/#getting-help) subscription which includes product updates and technical support.

The technical support is provided via allocated account at DotNetBrowser Help Center. We will create one account for the license holder.

Only the license holder has rights to use DotNetBrowser, receive free updates including minor and major versions, and contact technical support during active Standard Support subscription.

[DotNetBrowser Individual License Agreement](https://teamdev.com/dotnetbrowser/individual-license-agreement/)

### Project license

This type of license is issued to a company.

The license is tied to a [namespace](https://learn.microsoft.com/en-us/dotnet/csharp/programming-guide/namespaces/) of your project. When you purchase a Project license, we ask to provide the namespace where you plan to create an `IEngine` instance. You can work with the created `IEngine` instance and make calls to the library's API in other namespaces without any restrictions. The namespace name is expected to be in the `Product.Module` format. See examples below.

Let's assume that the license is tied to `ProductNamespace.MyNamespace`. The license key can then be used in the following way:


**C#**
```csharp
namespace ProductNamespace
{
    namespace MyNamespace
    {
        public class MyClass
        {
            public void InitializeEngine()
            {
                IEngine engine = EngineFactory.Create(new EngineOptions.Builder
                {
                    LicenseKey = "your_project_license_key"
                }.Build());
            }
        }
    }
}
```

**VB**
```vb
Namespace ProductNamespace
    Namespace MyNamespace
        Public Class [MyClass]
            Public Sub InitializeEngine()
                Dim engine As IEngine = EngineFactory.Create(New EngineOptions.Builder With 
                {
                    .LicenseKey = "your_project_license_key"
                }.Build())
            End Sub
        End Class
    End Namespace
End Namespace
```




You can also use this key in the classes located in the inner namespaces, for example:


**C#**
```csharp
namespace ProductNamespace
{
    namespace MyNamespace  
    {
        namespace InnerNamespace  
        {
            public class MyOtherClass
            {
                public void InitializeEngine()
                {
                    IEngine engine = EngineFactory.Create(new EngineOptions.Builder
                    {
                        LicenseKey = "your_project_license_key"
                    }.Build());
                }
            }
        }
    }
}
```

**VB**
```vb
Namespace ProductNamespace
    Namespace MyNamespace
        Namespace InnerNamespace
            Public Class MyOtherClass
                Public Sub InitializeEngine()
                    Dim engine As IEngine = 
                        EngineFactory.Create(New EngineOptions.Builder With
                        {
                            .LicenseKey = "your_project_license_key"
                        }.Build())
                End Sub
            End Class
        End Namespace
    End Namespace
End Namespace
```



If you create the `IEngine` instance in another namespace, the license exception will be thrown. For example, if the license is tied to `ProductNamespace.MyNamespace`, the following code will throw an `InvalidLicenseException`: 


**C#**
```csharp
namespace ProductNamespace
{
    namespace AnotherNamespace
    {
        public class MyClassInAnotherNamespace
        {
            public void InitializeEngine()
            {
                IEngine engine = EngineFactory.Create(new EngineOptions.Builder
                {
                    LicenseKey = "your_project_license_key"
                }.Build()); // <- InvalidLicenseException
            }
        }
    }
}
```

**VB**
```vb
Namespace ProductNamespace
    Namespace AnotherNamespace
        Public Class MyClassInAnotherNamespace
            Public Sub InitializeEngine()
                Dim engine As IEngine = EngineFactory.Create(New EngineOptions.Builder With
                {
                    .LicenseKey = "your_project_license_key"
                }.Build()) ' <- InvalidLicenseException
            End Sub
        End Class
    End Namespace
End Namespace
```



It includes a 1 year of [Standard Support](https://teamdev.com/dotnetbrowser/#getting-help) subscription which includes product updates and technical support.

The technical support is provided via allocated account at DotNetBrowser Help Center. We will create 2 accounts for the license holder.

[DotNetBrowser Project License Agreement](https://teamdev.com/dotnetbrowser/project-license-agreement/)

### Enterprise license

The license is issued to a company.

The library can be used by an unlimited number of developers for any number of projects in your company. 

It includes a 1 year of [Standard Support](https://teamdev.com/dotnetbrowser/#getting-help) subscription which includes product updates and technical support.

The technical support is provided via allocated account at DotNetBrowser Help Center. We will create 4 accounts for the license holder.

## Trial period

You can try DotNetBrowser for free for 30 days.

To start your free trial, please fill in [this form](https://teamdev.com/dotnetbrowser#evaluate). You will receive an email with your personal trial license key and a quick start guide.

### Expiration

When your trial period is over, DotNetBrowser will stop working and throw **"Your trial period has expired."** exception message. If you request another 30-day trial key, it will not work in the environments where you already used the expired one.

Please consider buying a [commercial license](https://teamdev.com/dotnetbrowser#licensing-and-pricing) to continue using DotNetBrowser in this case.

### Extended trial period

There might be cases when your company’s procurement procedures take longer than 30 days. If you need more time to finalize the purchase formalities, please contact our Sales team at [https://teamdev.com/contacts](https://teamdev.com/contacts/) with brief details of your situation.

## Chromium open-source components' licenses

DotNetBrowser is based on [Chromium](https://www.chromium.org/Home) open-source project that includes the source code and libraries written by developers in Chromium community. The project also includes a number of open-source third-party libraries.

**Note**
DotNetBrowser is using Blink, FFmpeg, libsecret, and Wayland Protocols KDE components, supplied under LGPL. Learn more about [DotNetBrowser Compliance with LGPL](https://teamdev.com/dotnetbrowser/lgpl-compliance/).


One of the key questions with an open-source code used in commercial products is the permitted use of the open-source code and possible restrictions on use and distribution of the works based on this open-source code.

We perform a regular review of the licenses associated with the Chromium components used by DotNetBrowser to make sure  there are no terms restricting commercial distribution of DotNetBrowser or customer applications using it. We also make sure that licenses requiring disclosure of the source code (like GPL) do not apply to DotNetBrowser or applications based on it.

Below you can find the links to Chromium components licenses associated with DotNetBrowser releases:

- [Chromium 155.0.8059.40 Licenses](https://docs.google.com/spreadsheets/d/1EBT0xVvO0HAAJ_uK5RpYH5X30262EZ3CWokAQT3Ymwk) (4.3.3 and higher)
- [Chromium 154.0.8037.58 Licenses](https://docs.google.com/spreadsheets/d/1Yw97AFCebZsu4bxayTCOtC5dTO2ItPAR-aAks5C18Aw) (4.3.2)
- [Chromium 153.0.8010.37 Licenses](https://docs.google.com/spreadsheets/d/1C72QstsYU8Lel0JkcunBlE113zgpqAE0XF6OnDT4cHA) (4.3.1)
- [Chromium 152.0.7977.65 Licenses](https://docs.google.com/spreadsheets/d/1qgjrCFMhdILBFjMIeHrbJwbHjKMxTk8Y4bsY5OCorco) (4.3.0)
- [Chromium 151.0.7922.138 Licenses](https://docs.google.com/spreadsheets/d/1zflrdOLrJBAWvS4_rN5qqSfvwByhpHwRnE1cUrN5GC4/) (4.2.3)
- [Chromium 151.0.7922.72 Licenses](https://docs.google.com/spreadsheets/d/1ThZu1cplKOvLgb2MyNdXSt9285LQdk0C6AUMt9zZJ04/) (4.2.2)
- [Chromium 150.0.7871.125 Licenses](https://docs.google.com/spreadsheets/d/1zuyh_ttkrjMdaEtJh5d0m5DmkWqol-g7S59BDYccan0/) (4.2.1)
- [Chromium 150.0.7871.47 Licenses](https://docs.google.com/spreadsheets/d/1fAFIMw40xKYFv96Q0R_bqq-Tdl2FP1xvzAvWc84uLrM/) (4.2.0)
- [Chromium 149.0.7827.103 Licenses](https://docs.google.com/spreadsheets/d/167NnaN6ikpsR-cV4pN5xDaNEiC1Th0qoZUiJjHP_ftY/) (4.1.1)
- [Chromium 148.0.7778.179 Licenses](https://docs.google.com/spreadsheets/d/1pCUn8g4BBOA1ExBwWBqn1ROucPhNIw7ad6-cuevTaxU/) (4.1.0)
- [Chromium 147.0.7727.138 Licenses](https://docs.google.com/spreadsheets/d/1-17NMuvZuAfelwqEaDaeekUzSGEuIxWBI5hmuIJkHRM) (4.0.1)
- [Chromium 147.0.7727.117 Licenses](https://docs.google.com/spreadsheets/d/1P08F9w_Y8uXq2n0j3POQclz6gyqEBJX2nmRhI9HjIHc) (4.0.0)
- [Chromium 146.0.7680.80 Licenses](https://docs.google.com/spreadsheets/d/15Hqy72qYmfJML-KmuIIxd02W5u5m4O12nGK33pZnrMk) (3.5.1)
- [Chromium 145.0.7632.76 Licenses](https://docs.google.com/spreadsheets/d/1jZFGOx1sp-IqUn7jz1L74_KqtxxT9T1v_196YnOtIyo) (3.5.0)
- [Chromium 144.0.7559.60 Licenses](https://docs.google.com/spreadsheets/d/1S3wmSHcNqApYgPDAK4ggfysLj50ktzcRVlsaE76vZyQ) (3.4.0)
- [Chromium 143.0.7499.41 Licenses](https://docs.google.com/spreadsheets/d/1yk1OA3Kgfbn6UMyuYmVxTnjaVSYYV0KJPtOSmGVfSEo) (3.3.7)
- [Chromium 142.0.7444.176 Licenses](https://docs.google.com/spreadsheets/d/1p5txo10GkoKnbvSHC8HWcjrMgzVEZFYYFSa0QJVPFKQ) (2.27.20, 3.3.6)
- [Chromium 142.0.7444.60 Licenses](https://docs.google.com/spreadsheets/d/12vHh6nIxhHoY8e0KNadTimPvXqw7t3mqOcZGF_4qrXI) (2.27.19, 3.3.5)
- [Chromium 141.0.7390.55 Licenses](https://docs.google.com/spreadsheets/d/1bTNdtAmVmELZKdpUAL6tug3Vy7H-efX71a9TIwxKEK4) (2.27.18, 3.3.4)
- [Chromium 140.0.7339.133 Licenses](https://docs.google.com/spreadsheets/d/1ripgrbZy_9I7ndluCtdFt79eyGN1DD9VViGKEoqSBPI) (2.27.17, 3.3.3)
- [Chromium 139.0.7258.67 Licenses](https://docs.google.com/spreadsheets/d/189cc1Pc0d1De40jjlwABTfs0AfBT3iqBZNKhefXbr8o) (2.27.16, 3.3.2)
- [Chromium 138.0.7204.97 Licenses](https://docs.google.com/spreadsheets/d/1eJZavcZP7aOKmdPfczG9_ftgHful77K3BO2WOgo_j-4) (2.27.15, 3.3.1)
- [Chromium 137.0.7151.69 Licenses](https://docs.google.com/spreadsheets/d/1fR9fEcEnJGQjPyG1aB5wPzNmNPswcMoHnpyh7FqnIVY) (2.27.14, 3.3.0)
- [Chromium 136.0.7103.114 Licenses](https://docs.google.com/spreadsheets/d/19_UIdYc7zd8ds6OB5mvSmT4HRJKGY2CyhuEpHWrsM9Q) (2.27.13, 3.2.1)
- [Chromium 135.0.7049.52 Licenses](https://docs.google.com/spreadsheets/d/1AeLbXRQx9zDFdGIyyji-kgmOXJrJh-zvwCgfuhv9cnQ) (2.27.12, 3.2.0)
- [Chromium 134.0.6998.89 Licenses](https://docs.google.com/spreadsheets/d/1HpBxpmkdDP4RMbOn8r26fru7ZgKz4YcRBsDW_iGHZnQ) (2.27.11, 3.1.2)
- [Chromium 133.0.6943.99 Licenses](https://docs.google.com/spreadsheets/d/1y05emvWqW_Nd00Djps-TPAtq2fO0AjHEi5ojI-9Naus) (2.27.10, 3.1.1)
- [Chromium 132.0.6834.84 Licenses](https://docs.google.com/spreadsheets/d/1oNcN40P8PSE4fe0cx4aubySbVt_HaPGBf499U3spDhw) (2.27.8 → 2.27.9, 3.0.1 → 3.1.0)
- [Chromium 131.0.6778.70 Licenses](https://docs.google.com/spreadsheets/d/1n7ZDspZVf0ngjZkfQBg9PvlQyx8Wg5MXb2pJO2kGY3E) (2.27.7, 3.0.0)
- [Chromium 130.0.6723.70 Licenses](https://docs.google.com/spreadsheets/d/1gsjMjngX2Vqk5Ve8jmUHnW3Imj8WxsAsIF4t-fSk8nA) (2.27.6)
- [Chromium 129.0.6668.59 Licenses](https://docs.google.com/spreadsheets/d/1mChXtl6dtGyYttZklKMTbH4L5F0T1wendOYKB8sffiU) (2.27.5)
- [Chromium 128.0.6613.85 Licenses](https://docs.google.com/spreadsheets/d/1DkC9Up0v4zwvx_oSebHWtCjL3g5-OoX-l0e95t-SJZ0) (2.27.4)
- [Chromium 127.0.6533.73 Licenses](https://docs.google.com/spreadsheets/d/1TdQJyq466QyAOhGkEiS7DFHY4C3V9SEl3x7ebJWimO0) (2.27.3)
- [Chromium 126.0.6478.57 Licenses](https://docs.google.com/spreadsheets/d/12Vhv6SQCiQDLUDtgnihQb8AwQ9zgySw3irFenH4CfFs) (2.27.2)
- [Chromium 125.0.6422.77 Licenses](https://docs.google.com/spreadsheets/d/1u1b5qrsjSR4-3G7np6ZbPe7ztz3PCbXkKhfYpxZHSjc) (2.27.1)
- [Chromium 124.0.6367.92 Licenses](https://docs.google.com/spreadsheets/d/1s-p_YZlGAWG3hPIduP2xOTaebOlYlCY0abhAKqFc4L0) (2.27.0)
- [Chromium 123.0.6312.87 Licenses](https://docs.google.com/spreadsheets/d/1INKzOCfYxYzZZidgguTajaShOehYylZIC1tILMCTxWo) (2.26.2)
- [Chromium 122.0.6261.94 Licenses](https://docs.google.com/spreadsheets/d/1SLkbJMJ2JhATaJCpPURNcM6J8KhO-TfCRk2PLmtLcJ8) (2.26.1)
- [Chromium 121.0.6167.184 Licenses](https://docs.google.com/spreadsheets/d/1k1Y3TEUj9LzamMcYcnRxyh_qXeLF006gAdeySLdc_WM) (2.26.0)
- [Chromium 120.0.6099.216 Licenses](https://docs.google.com/spreadsheets/d/17QOxP4ncpcnS5S9EiYmNeVrGoLGrwtWBX-oSantArR0) (2.25.1)
- [Chromium 120.0.6099.109 Licenses](https://docs.google.com/spreadsheets/d/1yY0iroK97hG3JzXrVVLhTqldQVxq2wGbM46PycYf7mY) (2.25.0)
- [Chromium 119.0.6045.105 Licenses](https://docs.google.com/spreadsheets/d/1nAK0xZ0ltOleopL1zcgj1ZfosKXGTnr-z1N09lnyIu8) (2.24.2)
- [Chromium 118.0.5993.70 Licenses](https://docs.google.com/spreadsheets/d/109lGdX7g61huKBDYqJP1l6IxtvQniqEPdgxuDc7e4Yg) (2.24.1)
- [Chromium 117.0.5938.62 Licenses](https://docs.google.com/spreadsheets/d/1_QMLQv6gAo-5IOINAbrcGhE_0Pg8NdO7irfiNZ74PLE) (2.24)
- [Chromium 116.0.5845.140 Licenses](https://docs.google.com/spreadsheets/d/1a_-CEoSBXhqThuaDDfXWrfbQv8Pff5JKOy_po-pY6KM) (2.23.3)
- [Chromium 115.0.5790.99 Licenses](https://docs.google.com/spreadsheets/d/15xKeS5I0ncE5fNgU5YX9V_JYAVnSIbKKmYv54f50oWI) (2.23.2)
- [Chromium 114.0.5735.134 Licenses](https://docs.google.com/spreadsheets/d/1Q7HP5v5zfBiPj7ZxVu_kQyQOVjHQ7P4X720yZ1ujUYg) (2.23.1)
- [Chromium 113.0.5672.63 Licenses](https://docs.google.com/spreadsheets/d/1nn2cF2N-HINh-leXgJleqkLlsGyIKB3DAfdbD0OF7Ls) (2.23)
- [Chromium 112.0.5615.137 Licenses](https://docs.google.com/spreadsheets/d/1peJgW0xtJ7Nof37osoj5eCW48NEh2U7Vz2M51RFCkz0) (2.22.1)
- [Chromium 111.0.5563.65 Licenses](https://docs.google.com/spreadsheets/d/15Z3zpioKdjlyeAUeRxsMbXZzQEKO2l0kGISYgvl90lc) (2.22)
- [Chromium 110.0.5481.77 Licenses](https://docs.google.com/spreadsheets/d/1OEBM6y-vTd1cTz7ySbSgkVWYqXvP5ZZ3oAUhLGAlKik) (2.21)
- [Chromium 108.0.5359.125 Licenses](https://docs.google.com/spreadsheets/d/1xzMWz85h5-mt1dbQ4NJfIH9w-je9tweWqfDirv7hYmA) (2.20 → 2.20.1)
- [Chromium 106.0.5249.168 Licenses](https://docs.google.com/spreadsheets/d/1TpZPbiOeRZVPTpvlKNOVr6b9puaMNg_LNHAgEzVNIN8) (2.18 → 2.19)
- [Chromium 104.0.5112.124 Licenses](https://docs.google.com/spreadsheets/d/10N-xwEkj0RT5-oImMoKqT9wNBseUfVHwUmGCZztNv6k) (2.17)
- [Chromium 102.0.5005.167 Licenses](https://docs.google.com/spreadsheets/d/184rdAlixirpmKjX_9x9BcmaF5WmpdxmBlSFQKlqPncg) (2.15 → 2.16.1)
- [Chromium 100.0.4896.60 Licenses](https://docs.google.com/spreadsheets/d/11j8GUfHntJqYTaZn7TbBCiN93d6H3t1MspdYy5K9WXE) (2.13 → 2.14)
- [Chromium 98.0.4758.102 Licenses](https://docs.google.com/spreadsheets/d/17ziO9Ym3vGJzjrxxE9qBbvae8kX9TAK8nt1H5XI-I-I) (2.12)
- [Chromium 96 Licenses](https://docs.google.com/spreadsheets/d/1lDIleG7Uqo-6VxEImHVLKmlCntzM2-qIAtJ14xY1UBs) (2.11)
- [Chromium 94 Licenses](https://docs.google.com/spreadsheets/d/11_Pp4bjTGaoSKXEupgzcuHpe4QFZ9pfhf-1jW6a40Lk) (2.10)
- [Chromium 92.0.4515.159 Licenses](https://docs.google.com/spreadsheets/d/10FC_7k3Yt-BZD8qmP2yKDT7TF8SYWyL1ZW7sUybFZsU) (2.9)
- [Chromium 91.0.4472.114 Licenses](https://docs.google.com/spreadsheets/d/1-LoeFPvzm0VH9MfDWUwOTUTbmnbHeQ0732Ui4QtKsfM) (2.7 → 2.8)
- [Chromium 90.0.4430.93 Licenses](https://docs.google.com/spreadsheets/d/1tYRgBCwQ3LXUEIRZwddY19EXCOUTRZZDpEfwkgFzEDw) (2.6)
- [Chromium 88.0.4324.150 Licenses](https://docs.google.com/spreadsheets/d/1pISZluqPDGasIc_WfkKuk2oj6SepyPrga8opkOzuW24) (2.5)
- [Chromium 84.0.4147.135 Licenses](https://docs.google.com/spreadsheets/d/1IDKW8duKUEEc3YpU_o5UXlAKRnUo7WuW8kBzEvaO5lc) (2.3 → 2.4)
- [Chromium 79.0.3945.130 Licenses](https://docs.google.com/spreadsheets/d/1sH0bmMbxrzbv3ihq1hwB9-0GyVrb1H0BYpI59nJ3u5A) (2.1 → 2.2)
- [Chromium 69.0.3497.12 Licenses](https://docs.google.com/spreadsheets/d/1HfmIihpLiUinEt_jIJPsLChEuzGZooFcp1G-FwyIGhg) (1.20 → 2.0)
- [Chromium 64.0.3282.24 Licenses](https://docs.google.com/spreadsheets/d/1LR4kGNXkBDvbj8LUKyLbX7mtNpWCSkGfnEXDzqG_Lgk) (1.15 → 1.19.1)
- [Chromium 60.0.3112.113 Licenses](https://docs.google.com/spreadsheets/d/1kvEZE46meUmGgZ4vuBLcjFQuJnzwKAuIQscAm2rDqrg) (1.12 → 1.14.3)
- [Chromium 55.0.2883.87 Licenses](https://docs.google.com/spreadsheets/d/15FO3WN26EwFNnHnzMpIGX-EEAsZTJNn2-fKDBiHT5kk) (1.10 → 1.11.1)
- [Chromium 51.0.2704.106 Licenses](https://docs.google.com/spreadsheets/d/1oRFbR_96Czb2EeXn9DGNXNRK_wtXRADJuC-GYyQ2cY4) (1.8 → 1.9)
- [Chromium 49.0.2623.110 Licenses](https://docs.google.com/spreadsheets/d/10lXhNfC2wJOgHXG9pKtThVGgrZ9OLnTnipMbFhUd4I8) (1.7 → 1.7.1)
- [Chromium 43.0.2357.52 Licenses](https://docs.google.com/spreadsheets/d/115yMnU0h082yEMbXWiQ5Mgx4Y6-U9PDr8fLZ6QH0sC4) (1.4 → 1.6.4)


<br>

<hr>

**Lead**
If you have any questions, email us
at [https://teamdev.com/contacts](https://teamdev.com/contacts/).

