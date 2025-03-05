---
title: Führen Sie einfache Zeichnungen mit Aspose.PSD für Java durch
linktitle: Einfaches Zeichnen durchführen
second_title: Aspose.PSD Java API
description: Erfahren Sie, wie Sie mit Aspose.PSD für Java Formen in PSD-Dateien zeichnen. Diese Schritt-für-Schritt-Anleitung behandelt das Erstellen, Hinzufügen von Ebenen und Zeichnen mit Codebeispielen.
type: docs
weight: 10
url: /de/java/basic-image-operations/simple-drawing/
---
## Einführung

Willkommen zu dieser Schritt-für-Schritt-Anleitung zum Erstellen einfacher Zeichnungen mit Aspose.PSD für Java! In diesem Tutorial lernen wir die Grundlagen zum Erstellen eines neuen PSD-Dokuments, zum Hinzufügen von Ebenen und zum Zeichnen von Formen mit unterschiedlichen Farben kennen. Aspose.PSD für Java ist eine leistungsstarke Bibliothek, mit der Sie PSD-Dateien programmgesteuert bearbeiten können und die umfangreiche Funktionen für Grafikdesignaufgaben bietet.

## Voraussetzungen

Bevor Sie mit dem Lernprogramm beginnen, stellen Sie sicher, dass die folgenden Voraussetzungen erfüllt sind:

- Auf Ihrem Computer ist Java Development Kit (JDK) installiert.
- Aspose.PSD für Java-Bibliothek. Sie können es herunterladen von der[Aspose.PSD für Java-Dokumentation](https://reference.aspose.com/psd/java/).

## Pakete importieren

Importieren Sie zunächst die erforderlichen Pakete in Ihr Java-Projekt. Fügen Sie am Anfang Ihrer Java-Datei den folgenden Code ein:

```java
import com.aspose.psd.Color;
import com.aspose.psd.Graphics;
import com.aspose.psd.Pen;
import com.aspose.psd.Rectangle;
import com.aspose.psd.brushes.SolidBrush;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.Layer;
```

## Schritt 1: Neues Dokument erstellen

Beginnen wir mit der Erstellung eines neuen PSD-Dokuments mit einer bestimmten Breite und Höhe:

```java
//ExStart:DokumentErstellen
String outputDir = "Your Document Directory";
String outPsdFilePath = outputDir + "output.psd";
int width = 100;
int height = 100;

PsdImage image = new PsdImage(width, height);
//ExEnd:CreateDocument
```

## Schritt 2: Eine Ebene hinzufügen

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

### Zeichnen Sie ein Rechteck mit gelber Farbe

```java
//ExStart:RechteckZeichnenGelb
Graphics graphic = new Graphics(layer);
graphic.clear(Color.getYellow());
//ExEnd:RechteckZeichnenGelb
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

## Schritt 4: Änderungen speichern

Speichern Sie abschließend eine Kopie der geladenen PSD-Datei inklusive der Änderungen:

```java
//ExStart:Änderungen speichern
image.save(outPsdFilePath);
//ExEnd:Änderungen speichern
```

## Abschluss

Herzlichen Glückwunsch! Sie haben erfolgreich eine einfache Zeichnung mit Aspose.PSD für Java erstellt. In diesem Tutorial wurde das Erstellen eines neuen Dokuments, das Hinzufügen von Ebenen und das Zeichnen von Rechtecken mit unterschiedlichen Farben behandelt. Erkunden Sie gerne die erweiterten Funktionen der Bibliothek für Ihre Grafikdesignanforderungen.

## Häufig gestellte Fragen

### F1: Kann ich Aspose.PSD für Java verwenden, um vorhandene PSD-Dateien zu bearbeiten?

A1: Ja, Aspose.PSD für Java bietet umfangreiche Funktionen zum Bearbeiten und Manipulieren vorhandener PSD-Dateien.

### F2: Wo finde ich Unterstützung für Aspose.PSD für Java?

 A2: Sie können die[Aspose.PSD für Java-Forum](https://forum.aspose.com/c/psd/34) für Supportanfragen.

### F3: Gibt es eine kostenlose Testversion von Aspose.PSD für Java?

 A3: Ja, Sie können auf die kostenlose Testversion zugreifen[Hier](https://releases.aspose.com/).

### F4: Wie kann ich eine Lizenz für Aspose.PSD für Java erwerben?

 A4: Sie können eine Lizenz erwerben bei der[Aspose.PSD-Kaufseite](https://purchase.aspose.com/buy).

### F5: Sind temporäre Lizenzen für Aspose.PSD für Java verfügbar?

 A5: Ja, Sie können eine temporäre Lizenz erhalten von[Hier](https://purchase.aspose.com/temporary-license/).