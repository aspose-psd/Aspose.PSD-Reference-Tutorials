---
title: Arbeiten mit der Zeitleiste in Aspose.PSD für .NET
linktitle: Arbeiten mit Timeline
second_title: Aspose.PSD .NET-API
description: Verbessern Sie die PSD-Bildbearbeitung mit der Aspose.PSD für die .NET-Timeline-Klasse. Steuern Sie Rahmeneigenschaften und Ebenenzustände und setzen Sie mühelos kreative Möglichkeiten frei.
type: docs
weight: 16
url: /de/net/psd-file-manipulation/timeline/
---
## Einführung
In der dynamischen Welt des Grafikdesigns und der Bildbearbeitung ist die Fähigkeit, die Zeitachse von Bildern zu steuern und zu manipulieren, von entscheidender Bedeutung. Aspose.PSD für .NET bietet mit seiner Timeline-Klasse eine leistungsstarke Lösung. Mit dieser High-Level-Funktion können Benutzer Änderungen an der Zeitleiste von PsdImage vornehmen, z. B. die Frame-Verzögerung ändern, den Ebenenstatus für bestimmte Frames bearbeiten und vieles mehr.
## Voraussetzungen
Bevor Sie in die aufregenden Möglichkeiten eintauchen, die der Timeline-Kurs bietet, stellen Sie sicher, dass die folgenden Voraussetzungen erfüllt sind:
-  Aspose.PSD für .NET-Bibliothek: Stellen Sie sicher, dass Sie die Aspose.PSD für .NET-Bibliothek installiert haben. Sie können es hier herunterladen[Aspose.PSD für .NET-Dokumentation](https://reference.aspose.com/psd/net/).
-  Dokument- und Ausgabeverzeichnisse: Definieren Sie die Pfade für Ihre Dokument- und Ausgabeverzeichnisse im Code. Verstelle die`baseDir` Und`outputDir` Variablen entsprechend Ihrer Projektstruktur.
Lassen Sie uns nun Schritt für Schritt untersuchen, wie Sie die Timeline-Klasse verwenden.
## Namespaces importieren
Um mit der Timeline-Klasse zu arbeiten, importieren Sie die erforderlichen Namespaces in Ihren Code:
```csharp
using System;
using System.Collections.Generic;
using System.IO;
using Aspose.PSD.FileFormats.Core.Blending;
using Aspose.PSD.FileFormats.Psd;
using Aspose.PSD.FileFormats.Psd.Layers.Animation;
```
## Schritt 1: PSD-Bild laden
Laden Sie zunächst das PSD-Bild aus der angegebenen Quelldatei. Stellen Sie sicher, dass der Quelldateipfad korrekt eingestellt ist:
```csharp
string sourceFile = Path.Combine(baseDir, "image1219.psd");
using (PsdImage psdImage = (PsdImage)Image.Load(sourceFile))
{
    //Hier finden Sie Ihren Code für weitere Vorgänge
}
```
## Schritt 2: Greifen Sie auf die Zeitleiste zu
Sobald das PSD-Bild geladen ist, greifen Sie mit dem folgenden Code auf die Timeline zu:
```csharp
Timeline timeline = psdImage.Timeline;
```
## Schritt 3: Entsorgungsmethode ändern
Manipulieren Sie die Entsorgungsmethode eines bestimmten Frames. In diesem Beispiel ändern wir die Dispose-Methode von Frame 1:
```csharp
timeline.Frames[0].DisposalMethod = FrameDisposalMethod.DoNotDispose;
```
## Schritt 4: Passen Sie die Bildverzögerung an
Ändern Sie die Verzögerung eines bestimmten Frames. Hier ändern wir die Verzögerung von Frame 2 auf 15:
```csharp
timeline.Frames[1].Delay = 15;
```
## Schritt 5: Ebenenstatus bearbeiten
Ändern Sie die Deckkraft von „Ebene 1“ für einen bestimmten Rahmen. In diesem Fall stellen wir die Deckkraft für Frame 2 auf 50 ein:
```csharp
LayerState layerState11 = timeline.Frames[1].LayerStates[1];
layerState11.Opacity = 50;
```
## Schritt 6: Ebene verschieben
Verschieben Sie „Ebene 1“ in die linke untere Ecke eines bestimmten Frames (Frame 3 in diesem Beispiel):
```csharp
LayerState layerState21 = timeline.Frames[2].LayerStates[1];
layerState21.PositionOffset = new Point(-50, 230);
```
## Schritt 7: Neuen Rahmen hinzufügen
Fügen Sie der Timeline einen neuen Frame hinzu:
```csharp
List<Frame> frames = new List<Frame>(timeline.Frames);
frames.Add(new Frame());
timeline.Frames = frames.ToArray();
```
## Schritt 8: Mischmodus ändern
Ändern Sie den Mischmodus von „Ebene 1“ in einem bestimmten Frame (in diesem Fall Frame 4):
```csharp
LayerState layerState31 = timeline.Frames[3].LayerStates[1];
layerState31.BlendMode = BlendMode.Dissolve;
```
## Schritt 9: Änderungen speichern
Wenden Sie die Änderungen wieder auf die PsdImage-Instanz an und speichern Sie das geänderte PSD-Bild:
```csharp
psdImage.Save(outputPsd);
```
## Schritt 10: Aufräumen
Bereinigen Sie abschließend, indem Sie die temporäre Ausgabedatei löschen:
```csharp
File.Delete(outputPsd);
```
## Abschluss

Zusammenfassend lässt sich sagen, dass die Timeline-Klasse in Aspose.PSD für .NET Entwicklern eine detaillierte Kontrolle über die Zeitleiste von PSD-Bildern ermöglicht. Durch eine Reihe einfacher Schritte können Sie Rahmeneigenschaften, Ebenenzustände und mehr manipulieren und so eine Fülle kreativer Möglichkeiten eröffnen.

## FAQs

### F1: Ist Aspose.PSD für .NET für Anfänger geeignet?

A1: Auf jeden Fall! Aspose.PSD für .NET bietet eine benutzerfreundliche Oberfläche und eine umfassende Dokumentation, sodass es sowohl für Anfänger als auch für erfahrene Entwickler zugänglich ist.

### F2: Kann ich Timeline-Änderungen auf GIF-Bilder anwenden?

A2: Die Timeline-Klasse ist speziell für PSD-Bilder konzipiert. Informationen zur GIF-Manipulation finden Sie unter Aspose.GIF für .NET.

### F3: Wo kann ich zusätzliche Unterstützung finden oder Probleme besprechen?

 A3: Besuchen Sie die[Aspose.PSD-Forum](https://forum.aspose.com/c/psd/34) für Community-Unterstützung und Problemdiskussionen.

### F4: Wie kann ich eine temporäre Lizenz für Aspose.PSD für .NET erhalten?

 A4: Erwerben Sie eine temporäre Lizenz[Hier](https://purchase.aspose.com/temporary-license/).

### F5: Was sind die Hauptvorteile der Verwendung von Aspose.PSD für .NET?

A5: Aspose.PSD für .NET bietet erweiterte Bildverarbeitungsfunktionen, PSD-Dateibearbeitung und leistungsstarkes Rendering.