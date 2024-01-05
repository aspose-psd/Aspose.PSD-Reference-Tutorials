---
title: Führen Sie einfaches Zeichnen mit Aspose.PSD für Java durch
linktitle: Führen Sie ein einfaches Zeichnen durch
second_title: Aspose.PSD Java-API
description: Erfahren Sie, wie Sie mit Aspose.PSD für Java Formen in PSD-Dateien zeichnen. Diese Schritt-für-Schritt-Anleitung behandelt das Erstellen, Hinzufügen von Ebenen und Zeichnen anhand von Codebeispielen.
type: docs
weight: 10
url: /de/java/basic-image-operations/simple-drawing/
---
## Einführung

Willkommen bei dieser Schritt-für-Schritt-Anleitung zum Durchführen einfacher Zeichnungen mit Aspose.PSD für Java! In diesem Tutorial erkunden wir die Grundlagen zum Erstellen eines neuen PSD-Dokuments, zum Hinzufügen von Ebenen und zum Zeichnen von Formen mit verschiedenen Farben. Aspose.PSD für Java ist eine leistungsstarke Bibliothek, die Ihnen die programmgesteuerte Bearbeitung von PSD-Dateien ermöglicht und umfangreiche Funktionen für Grafikdesignaufgaben bietet.

## Voraussetzungen

Bevor Sie mit dem Tutorial beginnen, stellen Sie sicher, dass die folgenden Voraussetzungen erfüllt sind:

- Java Development Kit (JDK) ist auf Ihrem Computer installiert.
-  Aspose.PSD für Java-Bibliothek. Sie können es hier herunterladen[Aspose.PSD für Java-Dokumentation](https://reference.aspose.com/psd/java/).

## Pakete importieren

Importieren Sie zunächst die erforderlichen Pakete in Ihr Java-Projekt. Fügen Sie den folgenden Code am Anfang Ihrer Java-Datei ein:

```java
import com.aspose.psd.Color;
import com.aspose.psd.Graphics;
import com.aspose.psd.Pen;
import com.aspose.psd.Rectangle;
import com.aspose.psd.brushes.SolidBrush;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.Layer;
```

## Schritt 1: Erstellen Sie ein neues Dokument

Beginnen wir mit der Erstellung eines neuen PSD-Dokuments mit einer angegebenen Breite und Höhe:

```java
//ExStart:CreateDocument
String outputDir = "Your Document Directory";
String outPsdFilePath = outputDir + "output.psd";
int width = 100;
int height = 100;

PsdImage image = new PsdImage(width, height);
//ExEnd:CreateDocument
```

## Schritt 2: Fügen Sie eine Ebene hinzu

Fügen wir nun mit dem Konstruktor ohne Argumente eine Ebene zum Dokument hinzu:

```java
//ExStart:AddLayer
Layer layer = new Layer();
layer.setBottom(height);
layer.setRight(width);
image.addLayer(layer);
//ExEnd:AddLayer
```

## Schritt 3: Formen zeichnen

In diesem Schritt verwenden wir die Graphics-Klasse, um Formen auf der erstellten Ebene zu zeichnen:

### Zeichnen Sie ein Rechteck mit einer gelben Farbe

```java
//ExStart:DrawRectangleYellow
Graphics graphic = new Graphics(layer);
graphic.clear(Color.getYellow());
//ExEnd:DrawRectangleYellow
```

### Zeichnen Sie ein rotes Rechteck

```java
//ExStart:DrawRedRectangle
graphic.drawRectangle(new Pen(Color.getRed()), new Rectangle(30, 10, 40, 80));
//ExEnd:DrawRedRectangle
```

### Zeichnen Sie ein blaues Rechteck

```java
//ExStart:DrawBlueRectangle
graphic.drawRectangle(new Pen(new SolidBrush(Color.getBlue())), new Rectangle(10, 30, 80, 40));
//ExEnd:DrawBlueRectangle
```

## Schritt 4: Speichern Sie die Änderungen

Speichern Sie abschließend eine Kopie der geladenen PSD-Datei einschließlich der Änderungen:

```java
//ExStart:SaveChanges
image.save(outPsdFilePath);
//ExEnd:SaveChanges
```

## Abschluss

Glückwunsch! Sie haben erfolgreich ein einfaches Zeichnen mit Aspose.PSD für Java durchgeführt. In diesem Tutorial wurde das Erstellen eines neuen Dokuments, das Hinzufügen von Ebenen und das Zeichnen von Rechtecken mit verschiedenen Farben behandelt. Entdecken Sie die erweiterten Funktionen der Bibliothek für Ihre Grafikdesign-Anforderungen.

## FAQs

### F1: Kann ich Aspose.PSD für Java verwenden, um vorhandene PSD-Dateien zu bearbeiten?

A1: Ja, Aspose.PSD für Java bietet umfangreiche Funktionen zum Bearbeiten und Bearbeiten bestehender PSD-Dateien.

### F2: Wo finde ich Unterstützung für Aspose.PSD für Java?

 A2: Sie können die besuchen[Aspose.PSD für Java-Forum](https://forum.aspose.com/c/psd/34) für alle Supportanfragen.

### F3: Gibt es eine kostenlose Testversion für Aspose.PSD für Java?

 A3: Ja, Sie können auf die kostenlose Testversion zugreifen[Hier](https://releases.aspose.com/).

### F4: Wie kann ich eine Lizenz für Aspose.PSD für Java erwerben?

 A4: Sie können eine Lizenz bei kaufen[Aspose.PSD-Kaufseite](https://purchase.aspose.com/buy).

### F5: Sind temporäre Lizenzen für Aspose.PSD für Java verfügbar?

 A5: Ja, Sie können eine temporäre Lizenz erhalten von[Hier](https://purchase.aspose.com/temporary-license/).