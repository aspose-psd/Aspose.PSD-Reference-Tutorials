---
title: Einfache Größenänderung von Bildern in Aspose.PSD für .NET
linktitle: Einfache Größenanpassung von Bildern
second_title: Aspose.PSD .NET API
description: Beherrschen Sie die Bildgrößenanpassung mit Aspose.PSD für .NET. Effizient, nahtlos und leistungsstark. Verbessern Sie Ihre .NET-Projekte mühelos.
type: docs
weight: 17
url: /de/net/image-manipulation/simple-resizing/
---
## Einführung

Im dynamischen Bereich der .NET-Entwicklung ist die Bildbearbeitung eine häufige Notwendigkeit. Aspose.PSD für .NET kommt mit seinen leistungsstarken Funktionen zur Rettung und ermöglicht eine nahtlose Bildgrößenänderung. In diesem Tutorial werden wir uns mit dem einfachen, aber entscheidenden Prozess der Bildgrößenänderung mit Aspose.PSD für .NET befassen. Schnall dich an, denn wir begeben uns auf eine Reise, um deine Bildverarbeitungsfähigkeiten zu verbessern.

## Voraussetzungen

Bevor wir uns in das Tutorial stürzen, stellen wir sicher, dass Sie alles für ein reibungsloses Erlebnis eingerichtet haben:

## Namespaces importieren

Stellen Sie sicher, dass Sie die erforderlichen Namespaces importiert haben, um auf die Funktionen von Aspose.PSD für .NET zuzugreifen:

```csharp
using Aspose.PSD.ImageOptions;
```

Lassen Sie uns nun den Vorgang der Größenänderung von Bildern in mehrere Schritte aufteilen:

## Schritt 1: Legen Sie Ihr Dokumentverzeichnis fest

Legen Sie zunächst den Pfad zu Ihrem Dokumentverzeichnis fest:

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

## Schritt 3: Bildgröße ändern

 Die Größenänderung eines Bildes ist so einfach wie das Aufrufen der`Resize` Methode für das Bildobjekt:

```csharp
image.Resize(300, 300);
```

## Schritt 4: Speichern Sie das skalierte Bild

Speichern Sie das skalierte Bild in Ihrem bevorzugten Format und mit den gewünschten Optionen. In diesem Beispiel speichern wir es als JPEG:

```csharp
string destName = dataDir + @"SimpleResizing_out.jpg";
image.Save(destName, new JpegOptions());
```

Und das war’s! Sie haben die Größe eines Bildes mit Aspose.PSD für .NET erfolgreich geändert.

## Abschluss

Die Beherrschung der Bildgrößenanpassung ist eine grundlegende Fähigkeit im Toolkit jedes .NET-Entwicklers. Mit Aspose.PSD für .NET wird der Prozess nicht nur effizient, sondern auch unterhaltsam. Mit diesem Wissen ausgestattet, können Sie nun Ihre Bildbearbeitungsfähigkeiten in Ihren .NET-Projekten verbessern.

## Häufig gestellte Fragen

### F1: Kann ich die Größe von Bildern mit Aspose.PSD für .NET auf ein bestimmtes Seitenverhältnis ändern?

A1: Ja, Sie können beim Ändern der Bildgröße ein bestimmtes Seitenverhältnis beibehalten, indem Sie die Breite oder Höhe entsprechend anpassen.

### F2: Unterstützt Aspose.PSD für .NET andere Bildformate außer JPEG?

A2: Auf jeden Fall! Aspose.PSD für .NET unterstützt eine Vielzahl von Bildformaten, darunter PNG, GIF, BMP und mehr.

### F3: Ist eine temporäre Lizenz für Aspose.PSD für .NET verfügbar?

A3: Ja, Sie können eine temporäre Lizenz für Aspose.PSD für .NET erwerben, um die Funktionen vor dem Kauf zu testen.

### F4: Wo finde ich umfassende Dokumentation für Aspose.PSD für .NET?

 A4: Erkunden Sie die ausführliche Dokumentation unter[Aspose.PSD für .NET-Dokumentation](https://reference.aspose.com/psd/net/).

### F5: Wie kann ich Support erhalten oder mich mit der Community für Aspose.PSD für .NET verbinden?

 A5: Besuchen Sie die[Aspose.PSD für .NET Forum](https://forum.aspose.com/c/psd/34) für Community-Unterstützung und Diskussionen.