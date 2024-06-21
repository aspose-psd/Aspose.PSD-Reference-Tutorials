---
title: Drehen Sie ein Bild in Aspose.PSD für Java
linktitle: Drehen Sie ein Bild
second_title: Aspose.PSD Java-API
description: Entdecken Sie mühelos die Bildrotation in Java mit Aspose.PSD. Drehen, spiegeln und speichern Sie PSD-Dateien ganz einfach.
type: docs
weight: 19
url: /de/java/advanced-image-manipulation/rotate-image/
---
## Einführung

Aspose.PSD für Java bietet leistungsstarke Funktionen für die Arbeit mit Bildern und ermöglicht Entwicklern die effiziente Bearbeitung und Verarbeitung von PSD-Dateien. In diesem Tutorial konzentrieren wir uns auf eine bestimmte Aufgabe: das Drehen eines Bildes. Egal, ob Sie eine Fotobearbeitungsanwendung erstellen oder einfach nur die Ausrichtung eines Bildes anpassen müssen, Aspose.PSD macht den Vorgang unkompliziert.

## Voraussetzungen

Bevor Sie mit dem Tutorial beginnen, stellen Sie sicher, dass die folgenden Voraussetzungen erfüllt sind:

-  Aspose.PSD für Java-Bibliothek: Stellen Sie sicher, dass Sie die Aspose.PSD für Java-Bibliothek heruntergeladen und installiert haben. Hier finden Sie die Bibliothek und eine ausführliche Dokumentation[Hier](https://reference.aspose.com/psd/java/).

- Java-Entwicklungsumgebung: Stellen Sie sicher, dass auf Ihrem Computer eine Java-Entwicklungsumgebung eingerichtet ist.

-  Beispiel-PSD-Datei: Bereiten Sie eine Beispiel-PSD-Datei vor, die Sie drehen möchten. Verstelle die`sourceFile` Variable im Beispielcode mit dem Pfad zu Ihrer PSD-Datei.

## Pakete importieren

Beginnen Sie mit dem Importieren der erforderlichen Pakete, um die Funktionen von Aspose.PSD zu nutzen:

```java
import com.aspose.psd.Image;
import com.aspose.psd.RotateFlipType;

import com.aspose.psd.imageoptions.JpegOptions;
```

## Schritt 1: Laden Sie das Bild

 Laden Sie das vorhandene Bild in eine Instanz von`Image` Klasse:

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";
Image image = Image.load(sourceFile);
```

## Schritt 2: Drehen Sie das Bild

 Drehen Sie das Bild mit`rotateFlip` Methode. In diesem Beispiel drehen wir das Bild um 270 Grad:

```java
image.rotateFlip(RotateFlipType.Rotate270FlipNone);
```

## Schritt 3: Speichern Sie das gedrehte Bild

 Speichern Sie das gedrehte Bild mit`save` -Methode und Angabe des Ausgabeformats (in diesem Fall JPEG):

```java
String destName = dataDir + "RotatedImage_out.jpg";
image.save(destName, new JpegOptions());
```

## Abschluss

Glückwunsch! Sie haben ein Bild mit Aspose.PSD für Java erfolgreich gedreht. Diese einfache, aber leistungsstarke Bibliothek eröffnet eine Welt voller Möglichkeiten zur Bildbearbeitung in Ihren Java-Anwendungen.

## FAQs

### F1: Ist Aspose.PSD mit verschiedenen Bildformaten kompatibel?

A1: Ja, Aspose.PSD unterstützt verschiedene Bildformate, darunter PSD, JPEG, PNG und mehr.

### F2: Kann ich benutzerdefinierte Drehungen anwenden, nicht nur vordefinierte Drehungen?

A2: Auf jeden Fall! Aspose.PSD bietet Flexibilität für die Anwendung benutzerdefinierter Rotationen, um Ihre spezifischen Anforderungen zu erfüllen.

### F3: Wo finde ich zusätzliche Unterstützung oder Unterstützung?

 A3: Bei Fragen oder Problemen besuchen Sie die[Aspose.PSD-Forum](https://forum.aspose.com/c/psd/34) für die Unterstützung der Gemeinschaft.

### F4: Gibt es eine kostenlose Testversion?

 A4: Ja, Sie können Aspose.PSD mit a erkunden[Kostenlose Testphase](https://releases.aspose.com/).

### F5: Wie erhalte ich eine temporäre Lizenz?

 A5: Wenn Sie eine temporäre Lizenz benötigen, können Sie eine erhalten.[Hier](https://purchase.aspose.com/temporary-license/).