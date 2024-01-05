---
title: Erweitern und Zuschneiden von Bildern in Aspose.PSD für .NET
linktitle: Bilder erweitern und zuschneiden
second_title: Aspose.PSD .NET-API
description: Erfahren Sie, wie Sie Bilder mit Aspose.PSD für .NET dynamisch erweitern und zuschneiden. Befolgen Sie unsere Schritt-für-Schritt-Anleitung für eine nahtlose Bildbearbeitung.
type: docs
weight: 13
url: /de/net/image-manipulation/expand-crop-images/
---
## Einführung

Aspose.PSD für .NET ist eine umfassende Bildbibliothek, die es Entwicklern ermöglicht, in ihren .NET-Anwendungen mit verschiedenen Bildformaten zu arbeiten. Eine seiner herausragenden Funktionen ist die Möglichkeit, Bilder problemlos zu bearbeiten. In diesem Tutorial konzentrieren wir uns auf das Erweitern und Zuschneiden von Bildern und bieten Ihnen eine praktische Anleitung zum Ausführen dieser Aufgaben mit Aspose.PSD.

## Voraussetzungen

Bevor Sie mit dem Tutorial beginnen, stellen Sie sicher, dass die folgenden Voraussetzungen erfüllt sind:

-  Aspose.PSD für .NET-Bibliothek: Stellen Sie sicher, dass Sie die Aspose.PSD für .NET-Bibliothek installiert haben. Sie können es hier herunterladen[Aspose.PSD für .NET-Dokumentation](https://reference.aspose.com/psd/net/).

- Beispielbild: Bereiten Sie eine Beispielbilddatei (z. B. „example1.psd“) vor, die Sie für das Tutorial verwenden.

Beginnen wir nun mit der Schritt-für-Schritt-Anleitung.

## Namespaces importieren

Beginnen Sie mit dem Importieren der erforderlichen Namespaces, um die von Aspose.PSD für .NET bereitgestellten Funktionen zu nutzen. Fügen Sie Ihrem Code die folgenden Namespaces hinzu:

```csharp
using Aspose.PSD.ImageOptions;
```

## Schritt 1: Richten Sie das Projekt ein

 Stellen Sie sicher, dass Sie ein Projekt mit integriertem Aspose.PSD für .NET eingerichtet haben. Wenn nicht, befolgen Sie die Anweisungen[Dokumentation](https://reference.aspose.com/psd/net/) zur Führung.

## Schritt 2: Laden Sie das Bild

Laden Sie das Beispielbild mit dem folgenden Code:

```csharp
string dataDir = RunExamples.GetDataDir_DrawingAndFormattingImages();
string sourceFile = dataDir + @"example1.psd";

// Laden Sie das Bild
using (RasterImage rasterImage = (RasterImage)Image.Load(sourceFile))
{
    // Zusätzlicher Code für die Bildverarbeitung wird hier eingefügt
}
```

## Schritt 3: Bilddaten zwischenspeichern

Zwischenspeichern Sie die Bilddaten, um die Leistung zu optimieren:

```csharp
rasterImage.CacheData();
```

## Schritt 4: Zielrechteck definieren

Erstellen Sie eine Instanz der Klasse „Rechteck“ und definieren Sie X, Y, Breite und Höhe des Rechtecks. Dies ist der Bereich, auf den das Bild erweitert oder zugeschnitten wird.

```csharp
Rectangle destRect = new Rectangle { X = -200, Y = -200, Width = 300, Height = 300 };
```

## Schritt 5: Speichern Sie das Ausgabebild

Speichern Sie das Ausgabebild mit den angegebenen Optionen und dem Zielrechteck:

```csharp
string destName = dataDir + @"jpeg_out.jpg";
rasterImage.Save(destName, new JpegOptions(), destRect);
```

## Abschluss

Glückwunsch! Sie haben erfolgreich gelernt, wie Sie Bilder mit Aspose.PSD für .NET erweitern und zuschneiden. Diese leistungsstarke Bibliothek eröffnet eine Welt voller Möglichkeiten zur Bildbearbeitung in Ihren .NET-Anwendungen.

## FAQs

### F1: Kann Aspose.PSD neben PSD auch andere Bildformate verarbeiten?

A1: Ja, Aspose.PSD unterstützt eine Vielzahl von Bildformaten, darunter JPEG, PNG, GIF und mehr.

### F2: Wo finde ich Unterstützung für Aspose.PSD?

 A2: Sie können Unterstützung finden und sich mit der Community austauschen unter[Aspose.PSD-Forum](https://forum.aspose.com/c/psd/34).

### F3 Gibt es eine kostenlose Testversion für Aspose.PSD für .NET?

 A3: Ja, Sie können die Funktionen mit einer kostenlosen Testversion erkunden, die unter verfügbar ist[Kostenlose Testversion von Aspose.PSD](https://releases.aspose.com/).

### F4: Wie erhalte ich eine temporäre Lizenz für Aspose.PSD?

 A4: Sie können eine temporäre Lizenz erhalten von[Temporäre Aspose.PSD-Lizenz](https://purchase.aspose.com/temporary-license/).

### F5: Wo kann ich Aspose.PSD für .NET kaufen?

 A5: Sie können die Bibliothek im kaufen[Aspose.PSD-Kaufseite](https://purchase.aspose.com/buy).