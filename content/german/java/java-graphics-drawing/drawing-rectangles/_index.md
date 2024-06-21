---
title: Zeichnen von Rechtecken in Java
linktitle: Zeichnen von Rechtecken in Java
second_title: Aspose.PSD Java-API
description: Erfahren Sie, wie Sie mit Aspose.PSD für Java Rechtecke auf Bildern zeichnen. Dieses Tutorial führt Java-Entwickler Schritt für Schritt an. Perfekt für Bildbearbeitungsaufgaben.
type: docs
weight: 17
url: /de/java/java-graphics-drawing/drawing-rectangles/
---
## Einführung
In der Welt der Java-Entwicklung ist die programmgesteuerte Bearbeitung und Generierung von Bildern eine allgemeine Anforderung für verschiedene Anwendungen. Eine solche häufig anzutreffende Aufgabe ist das Zeichnen von Formen wie Rechtecken auf Bildern. Aspose.PSD für Java bietet einen robusten Satz an Tools und Funktionen, um dies effizient zu erreichen. Dieses Tutorial führt Sie Schritt für Schritt durch den Prozess des Zeichnens von Rechtecken auf einem Bild mit Aspose.PSD für Java.
## Voraussetzungen
Bevor Sie mit dem Tutorial beginnen, stellen Sie sicher, dass die folgenden Voraussetzungen erfüllt sind:
### Java-Entwicklungsumgebung
Stellen Sie sicher, dass auf Ihrem System ein Java Development Kit (JDK) installiert ist, vorzugsweise JDK 8 oder höher.
### Aspose.PSD für Java
 Sie benötigen die Aspose.PSD für Java-Bibliothek. Sie können es hier herunterladen[Aspose.PSD für Java-Downloadseite](https://releases.aspose.com/psd/java/) und befolgen Sie die Installationsanweisungen in der Dokumentation.
## Pakete importieren
Importieren Sie zunächst die erforderlichen Aspose.PSD für Java-Pakete in Ihre Java-Datei:
```java
import com.aspose.psd.Color;
import com.aspose.psd.Graphics;
import com.aspose.psd.Image;
import com.aspose.psd.Pen;
import com.aspose.psd.Rectangle;
import com.aspose.psd.brushes.SolidBrush;
import com.aspose.psd.examples.Utils.Utils;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.BmpOptions;
```
Diese Importe ermöglichen Ihnen den Zugriff auf die Klassen und Methoden, die zum Zeichnen von Rechtecken auf Bildern erforderlich sind.
## Schritt 1: Erstellen Sie ein neues Bild
 Erstellen Sie zunächst eine neue Instanz von`PsdImage` Klasse mit einer bestimmten Breite und Höhe.
```java
String dataDir = "path_to_your_data_directory/";
String outpath = dataDir + "Rectangle.bmp";
// Erstellen Sie eine Instanz von BmpOptions und legen Sie deren Eigenschaften fest
BmpOptions saveOptions = new BmpOptions();
saveOptions.setBitsPerPixel(32);
// Erstellen Sie eine Instanz von PsdImage mit den angegebenen Abmessungen
Image image = new PsdImage(100, 100);
```
 In diesem Schritt`PsdImage` wird mit einer Breite und Höhe von jeweils 100 Pixeln initialisiert.
## Schritt 2: Grafikobjekt initialisieren
 Als nächstes initialisieren Sie a`Graphics` Objekt mit der`image` im vorherigen Schritt erstellt.
```java
// Grafikobjekt initialisieren
Graphics graphic = new Graphics(image);
```
 Das`Graphics`Das Objekt wird verwendet, um Zeichenvorgänge am Bild auszuführen.
## Schritt 3: Grafikoberfläche reinigen
Löschen Sie die Grafikoberfläche des Bildes mit einer bestimmten Farbe.
```java
// Klare Grafikoberfläche mit gelber Farbe
graphic.clear(Color.YELLOW);
```
Dadurch wird der Hintergrund des Bildes auf Gelb gesetzt.
## Schritt 4: Zeichnen Sie Rechtecke
Zeichnen Sie nun Rechtecke mit unterschiedlichen Farben und Abmessungen auf das Bild.
```java
// Zeichnen Sie ein rotes Rechteck
graphic.drawRectangle(new Pen(Color.RED), new Rectangle(30, 10, 40, 80));
// Zeichnen Sie ein blaues Rechteck
graphic.drawRectangle(new Pen(new SolidBrush(Color.BLUE)), new Rectangle(10, 30, 80, 40));
```
Diese Befehle zeichnen Rechtecke mit bestimmten Farben (Rot und Blau) und Positionen auf dem Bild.
## Schritt 5: Bild exportieren
Speichern Sie abschließend das geänderte Bild im BMP-Dateiformat.
```java
// Bild in das BMP-Dateiformat exportieren
image.save(outpath, saveOptions);
```
 Dadurch wird das Bild mit den gezeichneten Rechtecken in einer von angegebenen BMP-Datei gespeichert`outpath`.

## Abschluss
Das programmgesteuerte Zeichnen von Rechtecken auf Bildern in Java mit Aspose.PSD für Java ist mit den richtigen Tools und Bibliotheken unkompliziert. Durch Befolgen dieses Tutorials haben Sie gelernt, wie Sie ein Bild initialisieren, Grafikobjekte manipulieren, Formen zeichnen und das geänderte Bild in einer Datei speichern. Das Experimentieren mit verschiedenen Formen, Farben und Abmessungen wird Ihr Verständnis der Bildmanipulation in Java weiter verbessern.
## FAQs
### Kann Aspose.PSD für Java neben Rechtecken auch andere Formen verarbeiten?
Aspose.PSD für Java unterstützt neben Rechtecken auch das Zeichnen verschiedener Formen wie Ellipsen, Linien und Polygone.
### Wie kann ich die Dicke des Rechteckrandes ändern?
 Sie können die Dicke des Rechteckrandes anpassen, indem Sie festlegen`Pen` Dickeneigenschaft.
### Ist Aspose.PSD für Java für Hochleistungsbildverarbeitungsaufgaben geeignet?
Ja, Aspose.PSD für Java ist für eine leistungsstarke Bildverarbeitung mit umfangreichen Funktionen für einfache und komplexe Vorgänge konzipiert.
### Wo finde ich weitere Beispiele und Tutorials für Aspose.PSD für Java?
 Weitere Beispiele und eine ausführliche Dokumentation finden Sie unter[Aspose.PSD für Java-Dokumentation](https://reference.aspose.com/psd/java/).
### Unterstützt Aspose.PSD für Java neben BMP auch andere Bildformate?
Ja, Aspose.PSD für Java unterstützt eine Vielzahl von Bildformaten, darunter PNG, JPEG, TIFF und GIF.