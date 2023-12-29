---
title: Implementieren der Kontrastanpassung in Aspose.PSD für .NET
linktitle: Implementierung der Kontrastanpassung
second_title: Aspose.PSD .NET-API
description: Erfahren Sie in dieser Schritt-für-Schritt-Anleitung, wie Sie die Kontrastanpassung in Aspose.PSD für .NET implementieren.
type: docs
weight: 11
url: /de/net/image-adjustment/contrast-adjustment/
---
## Einführung

Willkommen zu dieser umfassenden Anleitung zur Implementierung der Kontrastanpassung in Aspose.PSD für .NET! In diesem Tutorial untersuchen wir den Prozess der Verbesserung des Kontrasts eines Bildes mithilfe von Aspose.PSD, einer leistungsstarken .NET-Bildbibliothek. Am Ende dieser Anleitung verfügen Sie über ein solides Verständnis dafür, wie Sie Kontrastanpassungen nahtlos an Ihren Bildern vornehmen können.

## Voraussetzungen

Bevor wir in den schrittweisen Prozess eintauchen, stellen Sie sicher, dass die folgenden Voraussetzungen erfüllt sind:

1.  Aspose.PSD für .NET-Bibliothek: Laden Sie die Aspose.PSD für .NET-Bibliothek herunter und installieren Sie sie. Den Download-Link finden Sie hier[Hier](https://releases.aspose.com/psd/net/).

2. Dokumentverzeichnis: Richten Sie ein Verzeichnis ein, in dem Ihre Quell- und Zieldateien gespeichert werden. Ersetzen Sie „Ihr Dokumentverzeichnis“ im bereitgestellten Code durch den Pfad zu diesem Verzeichnis.

Nachdem wir nun alle Voraussetzungen erfüllt haben, fahren wir mit der Implementierung fort.

## Namespaces importieren

In diesem Schritt importieren wir die erforderlichen Namespaces, um auf die von der Aspose.PSD-Bibliothek bereitgestellten Funktionen zuzugreifen.

```csharp
using Aspose.PSD.FileFormats.Tiff.Enums;
using Aspose.PSD.ImageOptions;
```

## Schritt 1: Laden Sie das Bild

 Laden Sie das Quellbild in eine Instanz von`RasterImage` Klasse.

```csharp
//ExStart:LoadImage
string sourceFile = dataDir + @"sample.psd";
using (var image = Image.Load(sourceFile))
{
    RasterImage rasterImage = (RasterImage)image;
    if (!rasterImage.IsCached)
    {
        rasterImage.CacheData();
    }
    // Fahren Sie mit dem nächsten Schritt fort...
}
//ExEnd:LoadImage
```

## Schritt 2: Kontrast anpassen

In diesem Schritt passen wir den Kontrast des geladenen Bildes an.

```csharp
//ExStart:Kontrast anpassen
rasterImage.AdjustContrast(50); // Passen Sie den Kontrast um 50 % an.
// Fahren Sie mit dem nächsten Schritt fort...
//ExEnd:AdjustContrast
```

## Schritt 3: TIFF-Optionen erstellen

 Erstellen Sie eine Instanz von`TiffOptions` Legen Sie für das resultierende Bild verschiedene Eigenschaften fest und speichern Sie das Bild im TIFF-Format.

```csharp
//ExStart:CreateTiffOptions
string destName = dataDir + @"AdjustContrast_out.tiff";
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
tiffOptions.BitsPerSample = new ushort[] { 8, 8, 8 };
tiffOptions.Photometric = TiffPhotometrics.Rgb;
rasterImage.Save(destName, tiffOptions);
//ExEnd:CreateTiffOptions
```

Glückwunsch! Sie haben die Kontrastanpassung mit Aspose.PSD für .NET erfolgreich implementiert.

## Abschluss

In diesem Tutorial haben wir den Prozess der Verbesserung des Bildkontrasts mit Aspose.PSD für .NET untersucht. Die Bibliothek bietet eine unkomplizierte Möglichkeit, Bildeigenschaften zu manipulieren, sodass Entwickler mühelos optisch ansprechende Bilder erstellen können.

## FAQs

### F1: Ist Aspose.PSD für .NET für Anfänger geeignet?

A1: Aspose.PSD für .NET ist entwicklerfreundlich konzipiert und eignet sich daher sowohl für Anfänger als auch für erfahrene Entwickler.

### F2: Kann ich Aspose.PSD für kommerzielle Projekte verwenden?

 A2: Ja, Aspose.PSD für .NET kann in kommerziellen Projekten verwendet werden. Einzelheiten zur Lizenzierung finden Sie unter[Hier](https://purchase.aspose.com/buy).

### F3: Gibt es eine kostenlose Testversion?

 A3: Ja, Sie können eine kostenlose Testversion von Aspose.PSD für .NET ausprobieren[Hier](https://releases.aspose.com/).

### F4: Wo finde ich Unterstützung für Aspose.PSD für .NET?

 A4: Besuchen Sie das Aspose.PSD für .NET-Supportforum[Hier](https://forum.aspose.com/c/psd/34) zur Hilfe.

### F5: Wie kann ich eine temporäre Lizenz erhalten?

 A5: Bei Bedarf können Sie eine temporäre Lizenz erhalten[Hier](https://purchase.aspose.com/temporary-license/).