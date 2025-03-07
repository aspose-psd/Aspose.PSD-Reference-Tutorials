---
title: Zuschneiden von Bildern per Rechteck in Aspose.PSD für .NET
linktitle: Bilder rechteckig zuschneiden
second_title: Aspose.PSD .NET API
description: Verbessern Sie Ihre .NET-Bildbearbeitungsfähigkeiten mit Aspose.PSD. Erfahren Sie Schritt für Schritt, wie Sie Bilder mit Rechtecken präzise zuschneiden.
weight: 11
url: /de/net/image-manipulation/crop-image-rectangle/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Zuschneiden von Bildern per Rechteck in Aspose.PSD für .NET

## Einführung

Im Bereich der .NET-Programmierung ist das Bearbeiten und Verbessern von Bildern eine gängige Aufgabe, und Aspose.PSD für .NET ist eine leistungsstarke Bibliothek, die diesen Prozess vereinfacht. Dieses Tutorial konzentriert sich auf eine grundlegende, aber entscheidende Bildbearbeitungstechnik – das Zuschneiden von Bildern mit einem Rechteck. Am Ende dieses Handbuchs verfügen Sie über ein solides Verständnis dafür, wie Sie Bilder mit Aspose.PSD für .NET präzise zuschneiden können.

## Voraussetzungen

Bevor Sie mit dem Lernprogramm beginnen, stellen Sie sicher, dass die folgenden Voraussetzungen erfüllt sind:

-  Aspose.PSD für .NET: Stellen Sie sicher, dass Sie die Bibliothek installiert haben. Wenn nicht, können Sie sie herunterladen[Hier](https://releases.aspose.com/psd/net/).

- Ihr Dokumentverzeichnis: Richten Sie ein Verzeichnis ein, in dem Ihre Bilddateien gespeichert werden.

- Integrierte Entwicklungsumgebung (IDE): Nutzen Sie eine .NET-kompatible IDE wie Visual Studio für nahtlose Codierung.

## Namespaces importieren

Um zu beginnen, schließen Sie die erforderlichen Namespaces in Ihr Projekt ein:

```csharp
using Aspose.PSD.ImageOptions;
```

## Schritt 1: Dokumentverzeichnis festlegen

Geben Sie zunächst den Pfad zu Ihrem Dokumentverzeichnis an:

```csharp
string dataDir = "Your Document Directory";
```

## Schritt 2: Laden und Zwischenspeichern des Bildes

Laden Sie das Bild aus der Quelldatei und speichern Sie seine Daten im Cache:

```csharp
//ExStart:ZuschneidendurchRechteck
string sourceFile = dataDir + @"sample.psd";

// Laden Sie ein vorhandenes Bild in eine Instanz der RasterImage-Klasse
using (RasterImage rasterImage = (RasterImage)Image.Load(sourceFile))
{
    if (!rasterImage.IsCached)
    {
        rasterImage.CacheData();
    }
    // Ihr Code für die nachfolgenden Schritte kommt hier hin
}
//ExEnd:ZuschneidendurchRechteck
```

## Schritt 3: Definieren Sie das Zuschneiderechteck

 Erstellen Sie eine Instanz des`Rectangle` Klasse mit der gewünschten Größe zum Zuschneiden:

```csharp
// Erstellen Sie eine Instanz der Rectangle-Klasse mit der gewünschten Größe
Rectangle rectangle = new Rectangle(20, 20, 20, 20);
```

## Schritt 4: Den Zuschneidevorgang durchführen

 Führen Sie den Zuschneidevorgang auf dem`RasterImage` Objekt mithilfe des definierten Rechtecks:

```csharp
rasterImage.Crop(rectangle);
```

## Schritt 5: Ergebnisse speichern

Speichern Sie das zugeschnittene Bild im angegebenen Format (in diesem Fall JPEG) auf der Festplatte:

```csharp
string destName = dataDir + @"CroppingByRectangle_out.jpg";
rasterImage.Save(destName, new JpegOptions());
```

Wiederholen Sie diese Schritte nach Bedarf und passen Sie die Rechteckparameter für verschiedene Zuschneideszenarien an.

## Abschluss

Zusammenfassend lässt sich sagen, dass das Beherrschen der Kunst des rechteckigen Zuschneidens von Bildern mit Aspose.PSD für .NET eine Welt voller Möglichkeiten zur Bildbearbeitung eröffnet. Dieses Tutorial hat Sie mit den wesentlichen Schritten ausgestattet, um diese Funktion nahtlos in Ihre .NET-Anwendungen zu integrieren.

## Häufig gestellte Fragen

### F1: Ist Aspose.PSD für .NET mit allen Bildformaten kompatibel?

A1: Ja, Aspose.PSD für .NET unterstützt eine Vielzahl von Formaten, darunter JPEG, PNG, SVG, TIFF, BMP, GIF, PSD und Jpeg2000.

### F2: Kann ich mehrere Zuschneidevorgänge auf dasselbe Bild anwenden?

A2: Auf jeden Fall! Sie können mehrere Zuschneidevorgänge nacheinander durchführen, um das gewünschte Ergebnis zu erzielen.

### F3: Gibt es Größenbeschränkungen für Bilder, die mit Aspose.PSD für .NET verarbeitet werden?

A3: Aspose.PSD für .NET ist für die Verarbeitung von Bildern verschiedener Größen konzipiert. Berücksichtigen Sie jedoch die Systemressourcen und den Speicher, wenn Sie mit außergewöhnlich großen Bildern arbeiten.

### F4: Gibt es eine Testversion für Aspose.PSD für .NET?

 A4: Ja, Sie können die Funktionen der Bibliothek erkunden, indem Sie eine kostenlose Testversion erwerben[Hier](https://releases.aspose.com/).

### F5: Wo finde ich zusätzliche Unterstützung oder Hilfe?

 A5: Besuchen Sie die[Aspose.PSD-Forum](https://forum.aspose.com/c/psd/34)um Kontakt mit der Community aufzunehmen und Unterstützung zu suchen.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
