---
title: Verwischen eines Bildes in Aspose.PSD für .NET
linktitle: Ein Bild verwischen
second_title: Aspose.PSD .NET API
description: Erfahren Sie, wie Sie mit Aspose.PSD für .NET Bilder mühelos verwischen. Eine Schritt-für-Schritt-Anleitung zur nahtlosen Bildbearbeitung in Ihren C#-Projekten.
type: docs
weight: 13
url: /de/net/image-adjustment/blur-image/
---
## Einführung

Im Bereich der .NET-Entwicklung erweist sich Aspose.PSD als leistungsstarker Verbündeter für die Bildbearbeitung. Dieses Tutorial konzentriert sich auf eine bestimmte Aufgabe: das Weichzeichnen eines Bilds mit Aspose.PSD für .NET. Wenn Sie Ihre Bildverarbeitungskenntnisse verbessern möchten oder einfach nach einer effizienten Möglichkeit suchen, Bilder programmgesteuert weichzuzeichnen, sind Sie hier richtig.

## Voraussetzungen

Bevor Sie mit dem Lernprogramm beginnen, stellen Sie sicher, dass die folgenden Voraussetzungen erfüllt sind:

-  Aspose.PSD für .NET: Stellen Sie sicher, dass Sie die Aspose.PSD-Bibliothek installiert haben. Sie können sie hier herunterladen:[Hier](https://releases.aspose.com/psd/net/).

- Entwicklungsumgebung: Richten Sie eine .NET-Entwicklungsumgebung ein und verfügen Sie über grundlegende Kenntnisse in C#.

- Beispielbild: Bereiten Sie ein Beispielbild im PSD-Format vor. Sie können Ihr eigenes verwenden oder eines zum Testen herunterladen.

## Namespaces importieren

Beginnen Sie mit dem Importieren der erforderlichen Namespaces in Ihren C#-Code:

```csharp
using Aspose.PSD.ImageFilters.FilterOptions;
using Aspose.PSD.ImageOptions;
```

## Schritt 1: Definieren Sie Ihr Dokumentverzeichnis

```csharp
// Der Pfad zum Dokumentverzeichnis.
string dataDir = "Your Document Directory";
```

## Schritt 2: Laden Sie das Bild

```csharp
//ExStart:BluranImage

string sourceFile = dataDir + @"sample.psd";

// Laden Sie ein vorhandenes Bild in eine Instanz der RasterImage-Klasse
using (var image = Image.Load(sourceFile))
{
    // Fahren Sie mit den nächsten Schritten innerhalb dieses Using-Blocks fort.
}
```

## Schritt 3: Konvertieren Sie das Bild in ein Rasterbild

```csharp
RasterImage rasterImage = (RasterImage)image;
```

## Schritt 4: Gaußschen Weichzeichnerfilter anwenden

```csharp
rasterImage.Filter(rasterImage.Bounds, new GaussianBlurFilterOptions(15, 15));
```

 Hier die`GaussianBlurFilterOptions` Klasse wird mit einem angegebenen Radius von 15 für horizontale und vertikale Unschärfe verwendet.

## Schritt 5: Das unscharfe Bild speichern

```csharp
string destName = dataDir + @"BlurAnImage_out.gif";
rasterImage.Save(destName, new GifOptions());
```

## Abschluss

Herzlichen Glückwunsch! Sie haben ein Bild erfolgreich mit Aspose.PSD für .NET verwischt. Dieses Tutorial bietet einen Einblick in die Funktionen von Aspose.PSD und öffnet die Tür zu unzähligen Möglichkeiten zur Bildbearbeitung in Ihren .NET-Anwendungen.

## Häufig gestellte Fragen

### F1: Kann ich auf unterschiedliche Teile eines Bildes unterschiedliche Unschärfeintensitäten anwenden?

A1: Ja, Aspose.PSD ermöglicht Ihnen, Filter mit unterschiedlichen Parametern auf bestimmte Bereiche eines Bildes anzuwenden und so eine detaillierte Kontrolle über den Unschärfeprozess zu erhalten.

### F2: Ist Aspose.PSD mit allen Bildformaten kompatibel?

A2: Obwohl Aspose.PSD eine Vielzahl von Bildformaten unterstützt, ist es ratsam, die Dokumentation auf die vollständige Liste und formatspezifische Überlegungen zu prüfen.

### F3: Wie kann ich eine temporäre Lizenz für Aspose.PSD erhalten?

 A3: Eine temporäre Lizenz erhalten Sie bei[Hier](https://purchase.aspose.com/temporary-license/) zu Test- und Evaluierungszwecken.

### F4: Gibt es in Aspose.PSD andere Bildbearbeitungsfunktionen?

A4: Absolut! Aspose.PSD bietet einen umfassenden Funktionsumfang, darunter Größenänderung, Zuschneiden und Farbanpassungen. Eine vollständige Liste finden Sie in der Dokumentation.

### F5: Wo kann ich Hilfe suchen oder mich mit der Aspose.PSD-Community verbinden?

 A5: Bei Fragen oder Diskussionen wenden Sie sich bitte an die[Aspose.PSD Forum](https://forum.aspose.com/c/psd/34).