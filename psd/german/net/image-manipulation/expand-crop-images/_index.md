---
title: Erweitern und Zuschneiden von Bildern in Aspose.PSD für .NET
linktitle: Bilder vergrößern und zuschneiden
second_title: Aspose.PSD .NET API
description: Erfahren Sie, wie Sie Bilder mit Aspose.PSD für .NET dynamisch erweitern und zuschneiden. Folgen Sie unserer Schritt-für-Schritt-Anleitung zur nahtlosen Bildbearbeitung.
type: docs
weight: 13
url: /de/net/image-manipulation/expand-crop-images/
---
## Einführung

Aspose.PSD für .NET ist eine umfassende Bildbibliothek, die es Entwicklern ermöglicht, in ihren .NET-Anwendungen mit verschiedenen Bildformaten zu arbeiten. Eines ihrer herausragenden Merkmale ist die Möglichkeit, Bilder mühelos zu bearbeiten. In diesem Tutorial konzentrieren wir uns auf das Erweitern und Zuschneiden von Bildern und bieten Ihnen eine praktische Anleitung zum Erledigen dieser Aufgaben mit Aspose.PSD.

## Voraussetzungen

Bevor Sie mit dem Lernprogramm beginnen, stellen Sie sicher, dass die folgenden Voraussetzungen erfüllt sind:

-  Aspose.PSD für .NET-Bibliothek: Stellen Sie sicher, dass Sie die Aspose.PSD für .NET-Bibliothek installiert haben. Sie können sie von der[Aspose.PSD für .NET-Dokumentation](https://reference.aspose.com/psd/net/).

- Beispielbild: Bereiten Sie eine Beispielbilddatei vor (z. B. „example1.psd“), die Sie für das Tutorial verwenden werden.

Beginnen wir nun mit der Schritt-für-Schritt-Anleitung.

## Namespaces importieren

Beginnen Sie mit dem Importieren der erforderlichen Namespaces, um die von Aspose.PSD für .NET bereitgestellten Funktionen zu nutzen. Fügen Sie Ihrem Code die folgenden Namespaces hinzu:

```csharp
using Aspose.PSD.ImageOptions;
```

## Schritt 1: Einrichten des Projekts

 Stellen Sie sicher, dass Sie ein Projekt mit integriertem Aspose.PSD für .NET eingerichtet haben. Wenn nicht, folgen Sie den[Dokumentation](https://reference.aspose.com/psd/net/) zur Orientierung.

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

Erstellen Sie eine Instanz der Rectangle-Klasse und definieren Sie die X-, Y-, Breiten- und Höhenwerte des Rechtecks. Dies ist der Bereich, auf den das Bild erweitert oder zugeschnitten wird.

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

Herzlichen Glückwunsch! Sie haben erfolgreich gelernt, wie Sie Bilder mit Aspose.PSD für .NET vergrößern und zuschneiden. Diese leistungsstarke Bibliothek eröffnet Ihnen eine Welt voller Möglichkeiten zur Bildbearbeitung in Ihren .NET-Anwendungen.

## Häufig gestellte Fragen

### F1: Kann Aspose.PSD außer PSD auch andere Bildformate verarbeiten?

A1: Ja, Aspose.PSD unterstützt eine Vielzahl von Bildformaten, darunter JPEG, PNG, GIF und mehr.

### F2: Wo finde ich Unterstützung für Aspose.PSD?

 A2: Sie können Unterstützung finden und sich in der Community engagieren unter[Aspose.PSD Forum](https://forum.aspose.com/c/psd/34).

### F3: Gibt es eine kostenlose Testversion für Aspose.PSD für .NET?

 A3: Ja, Sie können die Funktionen mit einer kostenlosen Testversion erkunden, die verfügbar ist unter[Kostenlose Testversion von Aspose.PSD](https://releases.aspose.com/).

### F4: Wie erhalte ich eine temporäre Lizenz für Aspose.PSD?

 A4: Eine vorläufige Lizenz erhalten Sie bei[Aspose.PSD Temporäre Lizenz](https://purchase.aspose.com/temporary-license/).

### F5: Wo kann ich Aspose.PSD für .NET kaufen?

 A5: Die Bibliothek gibt es im[Aspose.PSD-Kaufseite](https://purchase.aspose.com/buy).