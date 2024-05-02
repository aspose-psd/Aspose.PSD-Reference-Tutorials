---
title: Unschärfe eines Bildes in Aspose.PSD für .NET
linktitle: Ein Bild verwischen
second_title: Aspose.PSD .NET-API
description: Erfahren Sie, wie Sie mit Aspose.PSD für .NET Bilder mühelos verwischen. Eine Schritt-für-Schritt-Anleitung für die nahtlose Bildbearbeitung in Ihren C#-Projekten.
type: docs
weight: 13
url: /de/net/image-adjustment/blur-image/
---
## Einführung

Im Bereich der .NET-Entwicklung erweist sich Aspose.PSD als leistungsstarker Verbündeter für die Bildbearbeitung. Dieses Tutorial konzentriert sich auf eine bestimmte Aufgabe: das Verwischen eines Bildes mit Aspose.PSD für .NET. Wenn Sie Ihre Bildverarbeitungsfähigkeiten verbessern möchten oder einfach nach einer effizienten Möglichkeit suchen, Bilder programmgesteuert zu verwischen, sind Sie hier richtig.

## Voraussetzungen

Bevor Sie mit dem Tutorial beginnen, stellen Sie sicher, dass die folgenden Voraussetzungen erfüllt sind:

-  Aspose.PSD für .NET: Stellen Sie sicher, dass die Aspose.PSD-Bibliothek installiert ist. Sie können es herunterladen unter[Hier](https://releases.aspose.com/psd/net/).

- Entwicklungsumgebung: Richten Sie eine .NET-Entwicklungsumgebung ein und verfügen Sie über grundlegende Kenntnisse von C#.

- Beispielbild: Bereiten Sie ein Beispielbild im PSD-Format vor. Sie können Ihr eigenes verwenden oder eines zum Testen herunterladen.

## Namespaces importieren

Beginnen Sie mit dem Importieren der erforderlichen Namespaces in Ihren C#-Code:

```csharp
using Aspose.PSD.ImageFilters.FilterOptions;
using Aspose.PSD.ImageOptions;
```

## Schritt 1: Definieren Sie Ihr Dokumentenverzeichnis

```csharp
// Der Pfad zum Dokumentenverzeichnis.
string dataDir = "Your Document Directory";
```

## Schritt 2: Laden Sie das Bild

```csharp
//ExStart:BluranImage

string sourceFile = dataDir + @"sample.psd";

// Laden Sie ein vorhandenes Bild in eine Instanz der RasterImage-Klasse
using (var image = Image.Load(sourceFile))
{
    // Fahren Sie mit den nächsten Schritten in diesem Verwendungsblock fort
}
```

## Schritt 3: Konvertieren Sie das Bild in RasterImage

```csharp
RasterImage rasterImage = (RasterImage)image;
```

## Schritt 4: Gaußschen Unschärfefilter anwenden

```csharp
rasterImage.Filter(rasterImage.Bounds, new GaussianBlurFilterOptions(15, 15));
```

 Hier das`GaussianBlurFilterOptions` Die Klasse wird mit einem angegebenen Radius von 15 sowohl für die horizontale als auch für die vertikale Unschärfe verwendet.

## Schritt 5: Speichern Sie das unscharfe Bild

```csharp
string destName = dataDir + @"BlurAnImage_out.gif";
rasterImage.Save(destName, new GifOptions());
```

## Abschluss

Glückwunsch! Sie haben ein Bild mit Aspose.PSD für .NET erfolgreich unscharf gemacht. Dieses Tutorial bietet einen Einblick in die Funktionen von Aspose.PSD und öffnet die Tür zu einer Vielzahl von Möglichkeiten zur Bildbearbeitung in Ihren .NET-Anwendungen.

## FAQs

### F1: Kann ich unterschiedliche Unschärfeintensitäten auf verschiedene Teile eines Bildes anwenden?

A1: Ja, Aspose.PSD ermöglicht Ihnen die Anwendung von Filtern mit unterschiedlichen Parametern auf bestimmte Bereiche eines Bildes und bietet so eine detaillierte Kontrolle über den Unschärfeprozess.

### F2: Ist Aspose.PSD mit allen Bildformaten kompatibel?

A2: Obwohl Aspose.PSD eine Vielzahl von Bildformaten unterstützt, empfiehlt es sich, die Dokumentation auf die vollständige Liste und etwaige formatspezifische Überlegungen zu prüfen.

### F3: Wie kann ich eine temporäre Lizenz für Aspose.PSD erhalten?

 A3: Sie können eine temporäre Lizenz erwerben bei[Hier](https://purchase.aspose.com/temporary-license/) zu Test- und Evaluierungszwecken.

### F4: Gibt es in Aspose.PSD weitere Bildbearbeitungsfunktionen?

A4: Auf jeden Fall! Aspose.PSD bietet einen umfassenden Satz an Funktionen, einschließlich Größenänderung, Zuschneiden und Farbanpassungen. Eine vollständige Liste finden Sie in der Dokumentation.

### F5: Wo kann ich Hilfe suchen oder mich mit der Aspose.PSD-Community verbinden?

 A5: Bei Fragen oder Diskussionen gehen Sie zu[Aspose.PSD-Forum](https://forum.aspose.com/c/psd/34).