---
title: Arbeiten mit der Zeitleiste in Aspose.PSD für .NET
linktitle: Arbeiten mit der Zeitleiste
second_title: Aspose.PSD .NET API
description: Verbessern Sie die PSD-Bildbearbeitung mit der Aspose.PSD für die .NET Timeline-Klasse. Steuern Sie Rahmeneigenschaften und Ebenenzustände und entfesseln Sie mühelos kreative Möglichkeiten.
weight: 16
url: /de/net/psd-file-manipulation/timeline/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Arbeiten mit der Zeitleiste in Aspose.PSD für .NET

## Einführung
In der dynamischen Welt des Grafikdesigns und der Bildbearbeitung ist die Fähigkeit, die Zeitleiste von Bildern zu steuern und zu bearbeiten, von entscheidender Bedeutung. Aspose.PSD für .NET bietet mit seiner Timeline-Klasse eine leistungsstarke Lösung. Mit dieser hochrangigen Funktion können Benutzer Änderungen an der Zeitleiste von PsdImage vornehmen, z. B. die Frame-Verzögerung ändern, Ebenenzustände in bestimmten Frames bearbeiten und vieles mehr.
## Voraussetzungen
Bevor Sie in die spannenden Möglichkeiten eintauchen, die die Timeline-Klasse bietet, stellen Sie sicher, dass die folgenden Voraussetzungen erfüllt sind:
-  Aspose.PSD für .NET-Bibliothek: Stellen Sie sicher, dass Sie die Aspose.PSD für .NET-Bibliothek installiert haben. Sie können sie von der[Aspose.PSD für .NET-Dokumentation](https://reference.aspose.com/psd/net/).
-  Dokument- und Ausgabeverzeichnisse: Definieren Sie die Pfade für Ihre Dokument- und Ausgabeverzeichnisse im Code. Passen Sie die`baseDir` Und`outputDir` Variablen entsprechend Ihrer Projektstruktur.
Lassen Sie uns nun Schritt für Schritt untersuchen, wie die Timeline-Klasse genutzt wird.
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
Beginnen Sie mit dem Laden des PSD-Bilds aus der angegebenen Quelldatei. Stellen Sie sicher, dass der Quelldateipfad richtig eingestellt ist:
```csharp
string sourceFile = Path.Combine(baseDir, "image1219.psd");
using (PsdImage psdImage = (PsdImage)Image.Load(sourceFile))
{
    //Hier kommt Ihr Code für weitere Operationen hin
}
```
## Schritt 2: Zugriff auf die Timeline
Sobald das PSD-Bild geladen ist, greifen Sie mit dem folgenden Code auf die Zeitleiste zu:
```csharp
Timeline timeline = psdImage.Timeline;
```
## Schritt 3: Entsorgungsmethode ändern
Manipulieren Sie die Dispose-Methode eines bestimmten Frames. In diesem Beispiel ändern wir die Dispose-Methode von Frame 1:
```csharp
timeline.Frames[0].DisposalMethod = FrameDisposalMethod.DoNotDispose;
```
## Schritt 4: Frame-Verzögerung anpassen
Ändern Sie die Verzögerung eines bestimmten Frames. Hier ändern wir die Verzögerung von Frame 2 auf 15:
```csharp
timeline.Frames[1].Delay = 15;
```
## Schritt 5: Layerstatus bearbeiten
Ändern Sie die Deckkraft von „Ebene 1“ in einem bestimmten Frame. In diesem Fall setzen wir die Deckkraft in Frame 2 auf 50:
```csharp
LayerState layerState11 = timeline.Frames[1].LayerStates[1];
layerState11.Opacity = 50;
```
## Schritt 6: Ebene verschieben
Verschieben Sie „Ebene 1“ in die linke untere Ecke eines bestimmten Frames (in diesem Beispiel Frame 3):
```csharp
LayerState layerState21 = timeline.Frames[2].LayerStates[1];
layerState21.PositionOffset = new Point(-50, 230);
```
## Schritt 7: Neuen Rahmen hinzufügen
Fügen Sie der Zeitleiste ein neues Bild hinzu:
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
Zum Schluss führen Sie eine Bereinigung durch, indem Sie die temporäre Ausgabedatei löschen:
```csharp
File.Delete(outputPsd);
```
## Abschluss

Zusammenfassend lässt sich sagen, dass die Timeline-Klasse in Aspose.PSD für .NET Entwicklern eine detaillierte Kontrolle über die Zeitleiste von PSD-Bildern ermöglicht. Mit einer Reihe einfacher Schritte können Sie Rahmeneigenschaften, Ebenenzustände und mehr bearbeiten und so eine Fülle kreativer Möglichkeiten eröffnen.

## Häufig gestellte Fragen

### F1: Ist Aspose.PSD für .NET für Anfänger geeignet?

A1: Auf jeden Fall! Aspose.PSD für .NET bietet eine benutzerfreundliche Oberfläche und umfassende Dokumentation und ist damit sowohl für Anfänger als auch für erfahrene Entwickler zugänglich.

### F2: Kann ich Zeitleistenänderungen auf GIF-Bilder anwenden?

A2: Die Timeline-Klasse ist speziell für PSD-Bilder konzipiert. Informationen zur GIF-Manipulation finden Sie unter Aspose.GIF für .NET.

### F3: Wo kann ich weitere Unterstützung finden oder Probleme besprechen?

 A3: Besuchen Sie die[Aspose.PSD-Forum](https://forum.aspose.com/c/psd/34) für Community-Support und Problemdiskussionen.

### F4: Wie kann ich eine temporäre Lizenz für Aspose.PSD für .NET erhalten?

 A4: Erwerben Sie eine temporäre Lizenz[Hier](https://purchase.aspose.com/temporary-license/).

### F5: Was sind die wichtigsten Vorteile der Verwendung von Aspose.PSD für .NET?

A5: Aspose.PSD für .NET bietet erweiterte Bildverarbeitungsfunktionen, PSD-Dateibearbeitung und Hochleistungs-Rendering.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
