---
title: Rechtecke in Java zeichnen
linktitle: Rechtecke in Java zeichnen
second_title: Aspose.PSD Java API
description: Lernen Sie, mit Aspose.PSD für Java Rechtecke auf Bildern zu zeichnen. Dieses Tutorial führt Java-Entwickler Schritt für Schritt durch. Perfekt für Bildbearbeitungsaufgaben.
weight: 17
url: /de/java/java-graphics-drawing/drawing-rectangles/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Rechtecke in Java zeichnen

## Einführung
In der Welt der Java-Entwicklung ist das programmgesteuerte Bearbeiten und Generieren von Bildern eine häufige Anforderung in verschiedenen Anwendungen. Eine solche häufig anzutreffende Aufgabe ist das Zeichnen von Formen wie Rechtecken auf Bildern. Aspose.PSD für Java bietet einen robusten Satz von Tools und Funktionen, um dies effizient zu erreichen. Dieses Tutorial führt Sie Schritt für Schritt durch den Prozess des Zeichnens von Rechtecken auf einem Bild mit Aspose.PSD für Java.
## Voraussetzungen
Bevor Sie mit dem Lernprogramm beginnen, stellen Sie sicher, dass die folgenden Voraussetzungen erfüllt sind:
### Java-Entwicklungsumgebung
Stellen Sie sicher, dass auf Ihrem System ein Java Development Kit (JDK) installiert ist, vorzugsweise JDK 8 oder höher.
### Aspose.PSD für Java
 Sie benötigen die Aspose.PSD-Bibliothek für Java. Sie können sie herunterladen von[Aspose.PSD für Java-Downloadseite](https://releases.aspose.com/psd/java/) und befolgen Sie die Installationsanweisungen in der Dokumentation.
## Pakete importieren
Importieren Sie zunächst die erforderlichen Aspose.PSD-Pakete für Java in Ihre Java-Datei:
```java
import com.aspose.psd.Color;
import com.aspose.psd.Graphics;
import com.aspose.psd.Image;
import com.aspose.psd.Pen;
import com.aspose.psd.Rectangle;
import com.aspose.psd.brushes.SolidBrush;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.BmpOptions;
```
Diese Importe ermöglichen Ihnen den Zugriff auf die Klassen und Methoden, die zum Zeichnen von Rechtecken auf Bildern erforderlich sind.
## Schritt 1: Neues Image erstellen
 Erstellen Sie zunächst eine neue Instanz des`PsdImage` Klasse mit einer bestimmten Breite und Höhe.
```java
String dataDir = "path_to_your_data_directory/";
String outpath = dataDir + "Rectangle.bmp";
// Erstellen Sie eine Instanz von BmpOptions und legen Sie deren Eigenschaften fest
BmpOptions saveOptions = new BmpOptions();
saveOptions.setBitsPerPixel(32);
// Erstellen Sie eine Instanz von PsdImage mit angegebenen Abmessungen
Image image = new PsdImage(100, 100);
```
 In diesem Schritt`PsdImage` wird mit einer Breite und Höhe von jeweils 100 Pixeln initialisiert.
## Schritt 2: Grafikobjekt initialisieren
 Als nächstes initialisieren Sie`Graphics` Objekt mit dem`image` im vorherigen Schritt erstellt.
```java
// Grafikobjekt initialisieren
Graphics graphic = new Graphics(image);
```
 Das`Graphics`Das Objekt wird verwendet, um Zeichenvorgänge auf dem Bild durchzuführen.
## Schritt 3: Grafikoberfläche löschen
Löschen Sie die Grafikoberfläche des Bildes mithilfe einer bestimmten Farbe.
```java
// Klare Grafikoberfläche mit gelber Farbe
graphic.clear(Color.YELLOW);
```
Dadurch wird der Bildhintergrund gelb.
## Schritt 4: Rechtecke zeichnen
Zeichnen Sie nun Rechtecke mit unterschiedlichen Farben und Abmessungen auf das Bild.
```java
// Zeichnen Sie ein rotes Rechteck
graphic.drawRectangle(new Pen(Color.RED), new Rectangle(30, 10, 40, 80));
// Zeichnen Sie ein blaues Rechteck
graphic.drawRectangle(new Pen(new SolidBrush(Color.BLUE)), new Rectangle(10, 30, 80, 40));
```
Diese Befehle zeichnen Rechtecke mit angegebenen Farben (rot und blau) und Positionen auf dem Bild.
## Schritt 5: Bild exportieren
Speichern Sie das geänderte Bild abschließend im BMP-Dateiformat.
```java
// Bild in das BMP-Dateiformat exportieren
image.save(outpath, saveOptions);
```
 Dadurch wird das Bild mit den gezeichneten Rechtecken in eine BMP-Datei gespeichert, die angegeben wird durch`outpath`.

## Abschluss
Mit den richtigen Tools und Bibliotheken ist das programmgesteuerte Zeichnen von Rechtecken auf Bildern in Java mit Aspose.PSD für Java ganz einfach. In diesem Tutorial haben Sie gelernt, wie Sie ein Bild initialisieren, Grafikobjekte bearbeiten, Formen zeichnen und das geänderte Bild in einer Datei speichern. Durch das Experimentieren mit verschiedenen Formen, Farben und Abmessungen werden Sie Ihr Verständnis der Bildbearbeitung in Java noch weiter verbessern.
## Häufig gestellte Fragen
### Kann Aspose.PSD für Java andere Formen als Rechtecke verarbeiten?
Aspose.PSD für Java unterstützt das Zeichnen verschiedener Formen wie Ellipsen, Linien und Polygone zusätzlich zu Rechtecken.
### Wie kann ich die Dicke des Rechteckrahmens ändern?
 Sie können die Dicke des Rechteckrahmens anpassen, indem Sie die`Pen` Dickeneigenschaft.
### Ist Aspose.PSD für Java für leistungsstarke Bildverarbeitungsaufgaben geeignet?
Ja, Aspose.PSD für Java ist für die leistungsstarke Bildverarbeitung mit umfangreichen Funktionen für einfache und komplexe Vorgänge konzipiert.
### Wo finde ich weitere Beispiele und Tutorials für Aspose.PSD für Java?
 Weitere Beispiele und eine ausführlichere Dokumentation finden Sie auf der[Aspose.PSD für Java-Dokumentation](https://reference.aspose.com/psd/java/).
### Unterstützt Aspose.PSD für Java andere Bildformate außer BMP?
Ja, Aspose.PSD für Java unterstützt eine Vielzahl von Bildformaten, darunter PNG, JPEG, TIFF und GIF.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
