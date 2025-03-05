---
title: Implementieren der Kontrastanpassung in Aspose.PSD für .NET
linktitle: Implementieren der Kontrastanpassung
second_title: Aspose.PSD .NET API
description: Erfahren Sie in dieser Schritt-für-Schritt-Anleitung, wie Sie die Kontrastanpassung in Aspose.PSD für .NET implementieren.
type: docs
weight: 11
url: /de/net/image-adjustment/contrast-adjustment/
---
## Einführung

Willkommen zu diesem umfassenden Leitfaden zur Implementierung der Kontrastanpassung in Aspose.PSD für .NET! In diesem Tutorial erkunden wir den Prozess der Kontrastverbesserung eines Bildes mit Aspose.PSD, einer leistungsstarken .NET-Bildbibliothek. Am Ende dieses Leitfadens verfügen Sie über ein solides Verständnis dafür, wie Sie Kontrastanpassungen nahtlos auf Ihre Bilder anwenden können.

## Voraussetzungen

Bevor wir uns in den schrittweisen Prozess stürzen, stellen Sie sicher, dass die folgenden Voraussetzungen erfüllt sind:

1.  Aspose.PSD für .NET-Bibliothek: Laden Sie die Aspose.PSD für .NET-Bibliothek herunter und installieren Sie sie. Den Download-Link finden Sie[Hier](https://releases.aspose.com/psd/net/).

2. Dokumentverzeichnis: Richten Sie ein Verzeichnis ein, in dem Ihre Quell- und Zieldateien gespeichert werden. Ersetzen Sie „Ihr Dokumentverzeichnis“ im bereitgestellten Code durch den Pfad zu diesem Verzeichnis.

Nachdem wir nun unsere Voraussetzungen erfüllt haben, können wir mit der Implementierung fortfahren.

## Namespaces importieren

In diesem Schritt importieren wir die erforderlichen Namespaces, um auf die von der Aspose.PSD-Bibliothek bereitgestellten Funktionen zuzugreifen.

```csharp
using Aspose.PSD.FileFormats.Tiff.Enums;
using Aspose.PSD.ImageOptions;
```

## Schritt 1: Laden Sie das Bild

Laden Sie das Quellbild in eine Instanz des`RasterImage` Klasse.

```csharp
//ExStart:Bild laden
string sourceFile = dataDir + @"sample.psd";
using (var image = Image.Load(sourceFile))
{
    RasterImage rasterImage = (RasterImage)image;
    if (!rasterImage.IsCached)
    {
        rasterImage.CacheData();
    }
    // Fahren Sie mit dem nächsten Schritt fort ...
}
//ExEnd:LoadImage
```

## Schritt 2: Kontrast anpassen

In diesem Schritt passen wir den Kontrast des geladenen Bildes an.

```csharp
//ExStart:Kontrast anpassen
rasterImage.AdjustContrast(50); // Passen Sie den Kontrast um 50 % an
// Fahren Sie mit dem nächsten Schritt fort ...
//ExEnd:Kontrast anpassen
```

## Schritt 3: TIFF-Optionen erstellen

 Erstellen Sie eine Instanz von`TiffOptions` Legen Sie für das resultierende Bild verschiedene Eigenschaften fest und speichern Sie das Bild im TIFF-Format.

```csharp
//ExStart:ErstellenTiffOptions
string destName = dataDir + @"AdjustContrast_out.tiff";
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
tiffOptions.BitsPerSample = new ushort[] { 8, 8, 8 };
tiffOptions.Photometric = TiffPhotometrics.Rgb;
rasterImage.Save(destName, tiffOptions);
//ExEnd:CreateTiffOptions
```

Herzlichen Glückwunsch! Sie haben die Kontrastanpassung mit Aspose.PSD für .NET erfolgreich implementiert.

## Abschluss

In diesem Tutorial haben wir den Prozess der Bildkontrastverbesserung mit Aspose.PSD für .NET untersucht. Die Bibliothek bietet eine unkomplizierte Möglichkeit, Bildeigenschaften zu bearbeiten, sodass Entwickler mühelos optisch ansprechende Bilder erstellen können.

## Häufig gestellte Fragen

### F1: Ist Aspose.PSD für .NET für Anfänger geeignet?

A1: Aspose.PSD für .NET ist entwicklerfreundlich konzipiert und daher sowohl für Anfänger als auch für erfahrene Entwickler geeignet.

### F2: Kann ich Aspose.PSD für kommerzielle Projekte verwenden?

 A2: Ja, Aspose.PSD für .NET kann in kommerziellen Projekten verwendet werden. Lizenzdetails finden Sie unter[Hier](https://purchase.aspose.com/buy).

### F3: Gibt es eine kostenlose Testversion?

 A3: Ja, Sie können eine kostenlose Testversion von Aspose.PSD für .NET ausprobieren.[Hier](https://releases.aspose.com/).

### F4: Wo finde ich Unterstützung für Aspose.PSD für .NET?

 A4: Besuchen Sie das Aspose.PSD für .NET-Supportforum[Hier](https://forum.aspose.com/c/psd/34) um Hilfe.

### F5: Wie kann ich eine vorübergehende Lizenz erhalten?

 A5: Bei Bedarf können Sie eine temporäre Lizenz erwerben[Hier](https://purchase.aspose.com/temporary-license/).