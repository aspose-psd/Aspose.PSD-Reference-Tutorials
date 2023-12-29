---
title: Einfache Größenänderung von Bildern in Aspose.PSD für .NET
linktitle: Einfache Größenänderung von Bildern
second_title: Aspose.PSD .NET-API
description: Größenänderung des Masterbilds mit Aspose.PSD für .NET. Effizient, nahtlos und leistungsstark. Verbessern Sie Ihre .NET-Projekte mühelos.
type: docs
weight: 17
url: /de/net/image-manipulation/simple-resizing/
---
## Einführung

Im dynamischen Bereich der .NET-Entwicklung ist die Bearbeitung von Bildern eine häufige Notwendigkeit. Aspose.PSD für .NET kommt mit seinen leistungsstarken Funktionen zur Rettung und bietet ein nahtloses Erlebnis bei der Größenänderung von Bildern. In diesem Tutorial befassen wir uns mit dem einfachen, aber wichtigen Prozess der Größenänderung von Bildern mithilfe von Aspose.PSD für .NET. Schnall dich an, wenn wir uns auf die Reise begeben, um deine Bildverarbeitungsfähigkeiten zu verbessern.

## Voraussetzungen

Bevor wir uns mit dem Tutorial befassen, stellen wir sicher, dass Sie alles für ein reibungsloses Erlebnis eingerichtet haben:

## Namespaces importieren

Stellen Sie sicher, dass Sie die erforderlichen Namespaces importiert haben, um auf die Funktionen von Aspose.PSD für .NET zuzugreifen:

```csharp
using Aspose.PSD.ImageOptions;
```

Lassen Sie uns nun den Prozess der Größenänderung von Bildern in mehrere Schritte unterteilen:

## Schritt 1: Legen Sie Ihr Dokumentenverzeichnis fest

Legen Sie zunächst den Pfad zu Ihrem Dokumentenverzeichnis fest:

```csharp
string dataDir = "Your Document Directory";
```

## Schritt 2: Laden Sie das Bild

Laden Sie ein vorhandenes Bild in eine Instanz der RasterImage-Klasse:

```csharp
string sourceFile = dataDir + @"sample.psd";
using (Image image = Image.Load(sourceFile))
{
    // Ihr Code hier
}
```

## Schritt 3: Ändern Sie die Größe des Bildes

 Die Größenänderung eines Bildes ist so einfach wie das Aufrufen von`Resize` Methode für das Bildobjekt:

```csharp
image.Resize(300, 300);
```

## Schritt 4: Speichern Sie das geänderte Bild

Speichern Sie das verkleinerte Bild mit Ihrem bevorzugten Format und Ihren bevorzugten Optionen. In diesem Beispiel speichern wir es als JPEG:

```csharp
string destName = dataDir + @"SimpleResizing_out.jpg";
image.Save(destName, new JpegOptions());
```

Und das ist es! Sie haben die Größe eines Bildes mit Aspose.PSD für .NET erfolgreich geändert.

## Abschluss

Das Beherrschen der Größenänderung von Bildern ist eine grundlegende Fähigkeit im Toolkit eines jeden .NET-Entwicklers. Mit Aspose.PSD für .NET wird der Prozess nicht nur effizient, sondern auch unterhaltsam. Mit diesem Wissen können Sie nun Ihre Bildbearbeitungsfähigkeiten in Ihren .NET-Projekten verbessern.

## FAQs

### F1: Kann ich mit Aspose.PSD für .NET die Größe von Bildern auf ein bestimmtes Seitenverhältnis ändern?

A1: Ja, Sie können ein bestimmtes Seitenverhältnis beibehalten, während Sie die Größe von Bildern ändern, indem Sie entweder die Breite oder Höhe entsprechend anpassen.

### F2: Unterstützt Aspose.PSD für .NET neben JPEG auch andere Bildformate?

A2: Auf jeden Fall! Aspose.PSD für .NET unterstützt eine Vielzahl von Bildformaten, darunter PNG, GIF, BMP und mehr.

### F3: Ist eine temporäre Lizenz für Aspose.PSD für .NET verfügbar?

A3: Ja, Sie können eine temporäre Lizenz für Aspose.PSD für .NET erwerben, um dessen Funktionen vor dem Kauf zu testen.

### F4: Wo finde ich eine umfassende Dokumentation für Aspose.PSD für .NET?

 A4: Entdecken Sie die ausführliche Dokumentation unter[Aspose.PSD für .NET-Dokumentation](https://reference.aspose.com/psd/net/).

### F5: Wie kann ich Unterstützung für Aspose.PSD für .NET erhalten oder mich mit der Community verbinden?

 A5: Besuchen Sie die[Aspose.PSD für .NET Forum](https://forum.aspose.com/c/psd/34) für Community-Unterstützung und Diskussionen.