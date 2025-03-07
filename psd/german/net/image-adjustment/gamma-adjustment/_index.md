---
title: Implementieren der Gammaanpassung in Aspose.PSD für .NET
linktitle: Implementieren der Gamma-Anpassung
second_title: Aspose.PSD .NET API
description: Entdecken Sie die Leistungsfähigkeit von Aspose.PSD für .NET mit unserer Schritt-für-Schritt-Anleitung zur Implementierung der Gamma-Anpassung. Optimieren Sie Bildhelligkeit und -kontrast mühelos.
weight: 12
url: /de/net/image-adjustment/gamma-adjustment/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Implementieren der Gammaanpassung in Aspose.PSD für .NET

## Einführung

Willkommen zu diesem umfassenden Leitfaden zur Implementierung der Gamma-Anpassung in Aspose.PSD für .NET! Die Gamma-Anpassung ist eine wichtige Bildverarbeitungstechnik, mit der Sie die Helligkeit und den Kontrast eines Bildes feinabstimmen können. In diesem Tutorial führen wir Sie mithilfe der leistungsstarken Aspose.PSD-Bibliothek für .NET durch den Prozess.

## Voraussetzungen

Stellen Sie vor dem Eintauchen in die Implementierung sicher, dass die folgenden Voraussetzungen erfüllt sind:

-  Aspose.PSD für .NET-Bibliothek: Stellen Sie sicher, dass Sie die Aspose.PSD-Bibliothek für .NET installiert haben. Sie können sie herunterladen[Hier](https://releases.aspose.com/psd/net/).

- .NET Framework: Dieses Tutorial setzt voraus, dass Sie über grundlegende Kenntnisse der .NET-Entwicklung verfügen und das .NET Framework installiert haben.

- Integrierte Entwicklungsumgebung (IDE): Wählen Sie Ihre bevorzugte IDE für die .NET-Entwicklung, beispielsweise Visual Studio.

## Namespaces importieren

Importieren Sie in Ihrem .NET-Projekt zunächst die erforderlichen Namespaces für die Arbeit mit Aspose.PSD:

```csharp
using Aspose.PSD.FileFormats.Tiff.Enums;
using Aspose.PSD.ImageOptions;
```

## Schritt 1: Richten Sie Ihr Projekt ein

Erstellen Sie ein neues .NET-Projekt in der von Ihnen gewählten IDE. Achten Sie darauf, Verweise auf die Aspose.PSD-Bibliothek hinzuzufügen.

## Schritt 2: Definieren Sie das Dokumentverzeichnis

```csharp
string dataDir = "Your Document Directory";
```

## Schritt 3: Laden Sie das Bild

```csharp
string sourceFile = dataDir + @"sample.psd";
using (var image = Image.Load(sourceFile))
{
    // Innerhalb dieses Using-Blocks werden zusätzliche Schritte ausgeführt.
}
```

## Schritt 4: In Rasterbild umwandeln und Daten zwischenspeichern

```csharp
RasterImage rasterImage = (RasterImage)image;
if (!rasterImage.IsCached)
{
    rasterImage.CacheData();
}
```

## Schritt 5: Gamma anpassen

```csharp
rasterImage.AdjustGamma(2.2f, 2.2f, 2.2f);
```

## Schritt 6: TiffOptions erstellen und speichern

```csharp
string destName = dataDir + @"AdjustGamma_out.tiff";
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
tiffOptions.BitsPerSample = new ushort[] { 8, 8, 8 };
tiffOptions.Photometric = TiffPhotometrics.Rgb;
rasterImage.Save(destName, tiffOptions);
```

## Abschluss

Herzlichen Glückwunsch! Sie haben die Gammaanpassung mit Aspose.PSD für .NET erfolgreich implementiert. Diese leistungsstarke Bibliothek bietet robuste Funktionen für die Bildverarbeitung und ist damit ein wertvolles Werkzeug für .NET-Entwickler.

## Häufig gestellte Fragen

### F1: Wo finde ich die Aspose.PSD-Dokumentation?

 A1: Sie können die Dokumentation zu Rate ziehen[Hier](https://reference.aspose.com/psd/net/).

### F2: Wie lade ich Aspose.PSD für .NET herunter?

 A2: Sie können die Bibliothek herunterladen[Hier](https://releases.aspose.com/psd/net/).

### F3: Gibt es eine kostenlose Testversion?

 A3: Ja, Sie können eine kostenlose Testversion erhalten[Hier](https://releases.aspose.com/).

### F4: Wo erhalte ich Support für Aspose.PSD?

 A4: Sie können das Support-Forum besuchen[Hier](https://forum.aspose.com/c/psd/34).

### F5: Benötige ich eine vorübergehende Lizenz?

 A5: Bei Bedarf können Sie eine temporäre Lizenz erwerben[Hier](https://purchase.aspose.com/temporary-license/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
