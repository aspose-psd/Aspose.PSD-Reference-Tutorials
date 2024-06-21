---
title: Implementieren der Gamma-Anpassung in Aspose.PSD für .NET
linktitle: Implementierung der Gamma-Anpassung
second_title: Aspose.PSD .NET-API
description: Entdecken Sie die Leistungsfähigkeit von Aspose.PSD für .NET mit unserer Schritt-für-Schritt-Anleitung zur Implementierung der Gamma-Anpassung. Passen Sie Bildhelligkeit und Kontrast mühelos an.
type: docs
weight: 12
url: /de/net/image-adjustment/gamma-adjustment/
---
## Einführung

Willkommen zu diesem umfassenden Leitfaden zur Implementierung der Gamma-Anpassung in Aspose.PSD für .NET! Die Gamma-Anpassung ist eine wichtige Bildverarbeitungstechnik, mit der Sie die Helligkeit und den Kontrast eines Bildes feinabstimmen können. In diesem Tutorial führen wir Sie durch den Prozess mithilfe der leistungsstarken Aspose.PSD-Bibliothek für .NET.

## Voraussetzungen

Bevor Sie mit der Implementierung beginnen, stellen Sie sicher, dass die folgenden Voraussetzungen erfüllt sind:

-  Aspose.PSD für .NET-Bibliothek: Stellen Sie sicher, dass Sie die Aspose.PSD-Bibliothek für .NET installiert haben. Sie können es herunterladen[Hier](https://releases.aspose.com/psd/net/).

- .NET Framework: In diesem Tutorial wird davon ausgegangen, dass Sie über grundlegende Kenntnisse der .NET-Entwicklung verfügen und das .NET Framework installiert haben.

- Integrierte Entwicklungsumgebung (IDE): Wählen Sie Ihre bevorzugte IDE für die .NET-Entwicklung, z. B. Visual Studio.

## Namespaces importieren

Beginnen Sie in Ihrem .NET-Projekt mit dem Importieren der erforderlichen Namespaces für die Arbeit mit Aspose.PSD:

```csharp
using Aspose.PSD.FileFormats.Tiff.Enums;
using Aspose.PSD.ImageOptions;
```

## Schritt 1: Richten Sie Ihr Projekt ein

Erstellen Sie ein neues .NET-Projekt in der von Ihnen gewählten IDE. Stellen Sie sicher, dass Sie Verweise auf die Aspose.PSD-Bibliothek hinzufügen.

## Schritt 2: Definieren Sie das Dokumentenverzeichnis

```csharp
string dataDir = "Your Document Directory";
```

## Schritt 3: Laden Sie das Bild

```csharp
string sourceFile = dataDir + @"sample.psd";
using (var image = Image.Load(sourceFile))
{
    // Innerhalb dieses using-Blocks werden weitere Schritte ausgeführt.
}
```

## Schritt 4: In RasterImage umwandeln und Daten zwischenspeichern

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

Glückwunsch! Sie haben die Gamma-Anpassung mit Aspose.PSD für .NET erfolgreich implementiert. Diese leistungsstarke Bibliothek bietet robuste Funktionen für die Bildverarbeitung und ist damit ein wertvolles Werkzeug für .NET-Entwickler.

## FAQs

### F1: Wo finde ich die Aspose.PSD-Dokumentation?

 A1: Sie können sich auf die Dokumentation beziehen[Hier](https://reference.aspose.com/psd/net/).

### F2: Wie lade ich Aspose.PSD für .NET herunter?

 A2: Sie können die Bibliothek herunterladen.[Hier](https://releases.aspose.com/psd/net/).

### F3: Gibt es eine kostenlose Testversion?

 A3: Ja, Sie können eine kostenlose Testversion erhalten.[Hier](https://releases.aspose.com/).

### F4: Wo erhalte ich Unterstützung für Aspose.PSD?

 A4: Sie können das Support-Forum besuchen.[Hier](https://forum.aspose.com/c/psd/34).

### F5: Benötige ich eine temporäre Lizenz?

 A5: Bei Bedarf können Sie eine temporäre Lizenz erwerben.[Hier](https://purchase.aspose.com/temporary-license/).