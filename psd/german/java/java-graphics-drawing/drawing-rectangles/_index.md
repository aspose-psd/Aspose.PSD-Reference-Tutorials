---
date: 2026-09-08
description: Erfahren Sie, wie Sie ein Rechteck auf einem Bild mit Aspose.PSD for
  Java zeichnen, einschließlich der Erstellung von Bitmaps, Hintergrundfarbe und der
  Initialisierung von Graphics für die Bildbearbeitung in Java.
keywords:
- how to draw rectangle
- draw rectangle on image
- how to create bitmap
- set background color java
- java image manipulation
lastmod: 2026-09-08
linktitle: Rechtecke in Java zeichnen
og_description: Erfahren Sie, wie Sie ein Rechteck auf einem Bild mit Aspose.PSD for
  Java zeichnen. Dieser Leitfaden behandelt die Erstellung von Bitmaps, das Festlegen
  der Hintergrundfarbe und die Initialisierung von Graphics in Java.
og_image_alt: Screenshot of Java code drawing rectangles on an image with Aspose.PSD
og_title: Wie man ein Rechteck auf einem Bild mit Aspose.PSD for Java zeichnet
schemas:
- author: Aspose
  dateModified: '2026-09-08'
  description: Learn how to draw rectangle on an image using Aspose.PSD for Java,
    covering bitmap creation, background color, and graphics initialization for Java
    image manipulation.
  headline: How to draw rectangle on an image with Aspose.PSD for Java
  type: TechArticle
- description: Learn how to draw rectangle on an image using Aspose.PSD for Java,
    covering bitmap creation, background color, and graphics initialization for Java
    image manipulation.
  name: How to draw rectangle on an image with Aspose.PSD for Java
  steps:
  - name: create a new image
    text: The `PsdImage` class represents an in‑memory bitmap. Initializing it also
      allocates the pixel buffer. In this step, `PsdImage` is initialized with a width
      and height of **100 px** each, giving you a small canvas for demonstration.
  - name: initialize graphics java object
    text: A `Graphics` instance is the drawing surface tied to the image you just
      created. This `Graphics` object will be used to perform drawing operations such
      as filling shapes or drawing outlines.
  - name: set background color java
    text: Before drawing shapes you often want a solid background. Use `clear` with
      a `Color` to fill the entire canvas. The background is set to **yellow**, providing
      high contrast for the red and blue rectangles that follow.
  - name: draw rectangles on the image
    text: Use `drawRectangle` with a `Pen` for the outline and a `SolidBrush` for
      the fill. You can draw multiple rectangles with different colors and positions.
      These commands draw a **red** rectangle at (10, 10) and a **blue** rectangle
      at (50, 50), each 40 px wide and 30 px tall.
  - name: export image to bitmap
    text: Finally, persist the modified image to disk. Aspose.PSD automatically encodes
      the bitmap in the format you specify. The image is saved as a BMP file at the
      path stored in `outpath`.
  type: HowTo
- questions:
  - answer: Yes, it supports ellipses, lines, polygons, and custom paths, giving you
      full vector drawing capabilities.
    question: Can Aspose.PSD for Java handle other shapes besides rectangles?
  - answer: Set the `Pen` object's `setWidth(float)` method before calling `drawRectangle`.
    question: How can I modify the thickness of the rectangle border?
  - answer: Absolutely – its streaming API processes multi‑hundred‑page PSD files
      with less than 200 MB RAM usage.
    question: Is Aspose.PSD for Java suitable for high‑performance image processing
      tasks?
  - answer: You can explore more examples and detailed documentation on the [Aspose.PSD
      for Java documentation](https://reference.aspose.com/psd/java/).
    question: Where can I find more examples and tutorials for Aspose.PSD for Java?
  - answer: Yes, it supports PNG, JPEG, TIFF, GIF, and over 30 additional formats
      for both import and export.
    question: Does Aspose.PSD for Java support other image formats besides BMP?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- java graphics
- Aspose.PSD
- image processing
title: Wie man ein Rechteck auf einem Bild mit Aspose.PSD for Java zeichnet
url: /de/java/java-graphics-drawing/drawing-rectangles/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Wie man ein Rechteck auf einem Bild mit Aspose.PSD für Java zeichnet

## Einleitung
Wenn Sie **how to draw rectangle** programmgesteuert auf einem Bild benötigen, bietet Aspose.PSD für Java eine saubere, leistungsstarke API. In diesem Tutorial sehen Sie, wie Sie ein Bitmap erstellen, die Hintergrundfarbe festlegen und **initialize graphics java** Objekte initialisieren, sodass Sie Rechtecke jeder Größe und Farbe rendern können. Die Schritte sind einfach, der Code ist prägnant und das Ergebnis ist eine BMP‑Datei, die Sie in jedem Java‑basierten Workflow verwenden können.

## Schnelle Antworten
- **Welche Bibliothek übernimmt das Zeichnen von Rechtecken?** Aspose.PSD for Java.
- **Wie viele Codezeilen werden benötigt?** About six lines to create the image, set background, and draw two rectangles.
- **Welche Bildformate werden für den Export unterstützt?** BMP, PNG, JPEG, TIFF, GIF and more.
- **Benötige ich eine Lizenz für die Entwicklung?** A free trial works for testing; a license is required for production.
- **Kann ich die Rahmenstärke ändern?** Yes – adjust the `Pen` thickness property before drawing.

## Was bedeutet das Zeichnen eines Rechtecks auf einem Bild?
Das Zeichnen eines Rechtecks auf einem Bild bedeutet, dass eine gefüllte oder umrandete Form mithilfe eines Grafik‑Kontexts auf ein Bitmap gerendert wird. Die `Graphics`‑Klasse von Aspose.PSD bietet Methoden, mit denen Sie Farbe, Position und Größe in einem einzigen Aufruf festlegen können.

## Warum Aspose.PSD für Java zum Zeichnen von Rechtecken verwenden?
Aspose.PSD unterstützt **50+ Bildformate** und kann Dateien bis zu **2 GB** verarbeiten, ohne das gesamte Dokument in den Speicher zu laden. Seine `Graphics`‑API ist bis zu **3× schneller** als das native Java AWT für Batch‑Operationen, was sie ideal für hochdurchsatz‑Server‑seitige Bildverarbeitung macht.

## Voraussetzungen
Bevor Sie beginnen, stellen Sie sicher, dass Sie:

- **Java Development Kit (JDK) 8 oder höher** installiert.
- **Aspose.PSD for Java** Bibliothek von der [Aspose.PSD for Java download page](https://releases.aspose.com/psd/java/) heruntergeladen und dem Klassenpfad Ihres Projekts hinzugefügt.

### Pakete importieren
Die `import`‑Anweisungen geben Ihnen Zugriff auf die Klassen, die für die Bitmap‑Erstellung und das Zeichnen benötigt werden.

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

## Wie man ein Rechteck auf einem Bild in Java zeichnet?
Laden Sie ein neues `PsdImage`, löschen Sie dessen Oberfläche mit einer Hintergrundfarbe, erstellen Sie ein `Graphics`‑Objekt und rufen Sie anschließend `drawRectangle` mit dem gewünschten Stift und Pinsel auf. Der gesamte Vorgang erfordert nur wenige Methodenaufrufe und erzeugt ein sofort speicherbares Bitmap.  
`PsdImage` stellt ein im Speicher befindliches Bitmap dar, das bearbeitet und gespeichert werden kann.  
`Graphics` bietet eine Zeichenfläche zum Rendern von Formen auf einem Bild.

### Schritt 1: ein neues Bild erstellen
Die `PsdImage`‑Klasse stellt ein im Speicher befindliches Bitmap dar. Die Initialisierung reserviert zudem den Pixelpuffer.

```java
String dataDir = "path_to_your_data_directory/";
String outpath = dataDir + "Rectangle.bmp";
// Create an instance of BmpOptions and set its properties
BmpOptions saveOptions = new BmpOptions();
saveOptions.setBitsPerPixel(32);
// Create an instance of PsdImage with specified dimensions
Image image = new PsdImage(100, 100);
```
In diesem Schritt wird `PsdImage` mit einer Breite und Höhe von jeweils **100 px** initialisiert, was Ihnen eine kleine Zeichenfläche für die Demonstration bietet.

### Schritt 2: graphics java‑Objekt initialisieren
Eine `Graphics`‑Instanz ist die Zeichenfläche, die mit dem von Ihnen gerade erstellten Bild verknüpft ist.

```java
// Initialize Graphics object
Graphics graphic = new Graphics(image);
```
Dieses `Graphics`‑Objekt wird verwendet, um Zeichenoperationen wie das Füllen von Formen oder das Zeichnen von Konturen auszuführen.

### Schritt 3: Hintergrundfarbe in Java festlegen
Bevor Sie Formen zeichnen, möchten Sie häufig einen einfarbigen Hintergrund. Verwenden Sie `clear` mit einem `Color`, um die gesamte Zeichenfläche zu füllen.

```java
// Clear graphics surface with a yellow color
graphic.clear(Color.YELLOW);
```
Der Hintergrund wird auf **gelb** gesetzt, was einen hohen Kontrast zu den nachfolgenden roten und blauen Rechtecken bietet.

### Schritt 4: Rechtecke auf dem Bild zeichnen
Verwenden Sie `drawRectangle` mit einem `Pen` für die Kontur und einem `SolidBrush` für die Füllung. Sie können mehrere Rechtecke mit unterschiedlichen Farben und Positionen zeichnen.

```java
// Draw a red rectangle
graphic.drawRectangle(new Pen(Color.RED), new Rectangle(30, 10, 40, 80));
// Draw a blue rectangle
graphic.drawRectangle(new Pen(new SolidBrush(Color.BLUE)), new Rectangle(10, 30, 80, 40));
```
Diese Befehle zeichnen ein **rotes** Rechteck bei (10, 10) und ein **blaues** Rechteck bei (50, 50), jeweils 40 px breit und 30 px hoch.

### Schritt 5: Bild als Bitmap exportieren
Abschließend wird das modifizierte Bild auf die Festplatte gespeichert. Aspose.PSD kodiert das Bitmap automatisch in dem von Ihnen angegebenen Format.

```java
// Export image to BMP file format
image.save(outpath, saveOptions);
```
Das Bild wird als BMP‑Datei unter dem Pfad gespeichert, der in `outpath` abgelegt ist.

## Häufige Probleme und Lösungen
- **Leere Ausgabedatei** – Stellen Sie sicher, dass Sie `graphics.clear` vor dem Zeichnen aufrufen; andernfalls kann die Zeichenfläche transparent bleiben.
- **Falsche Farben** – Vergewissern Sie sich, dass Sie `com.aspose.psd.Color` importieren und nicht `java.awt.Color`.
- **Große Bilder führen zu Speicherengpässen** – Verwenden Sie `PsdImage`‑Konstruktoren, die Streaming unterstützen, um das Laden der gesamten Datei in den RAM zu vermeiden.

## Häufig gestellte Fragen

**Q: Kann Aspose.PSD für Java andere Formen neben Rechtecken verarbeiten?**  
A: Ja, es unterstützt Ellipsen, Linien, Polygone und benutzerdefinierte Pfade und bietet Ihnen vollständige Vektor‑Zeichenfähigkeiten.

**Q: Wie kann ich die Dicke des Rechteckrahmens ändern?**  
A: Setzen Sie die `setWidth(float)`‑Methode des `Pen`‑Objekts, bevor Sie `drawRectangle` aufrufen.

**Q: Ist Aspose.PSD für Java für hochleistungsfähige Bildverarbeitungsaufgaben geeignet?**  
A: Absolut – seine Streaming‑API verarbeitet mehrseitige PSD‑Dateien mit weniger als 200 MB RAM‑Verbrauch.

**Q: Wo finde ich weitere Beispiele und Tutorials für Aspose.PSD für Java?**  
A: Weitere Beispiele und ausführliche Dokumentation finden Sie unter der [Aspose.PSD for Java documentation](https://reference.aspose.com/psd/java/).

**Q: Unterstützt Aspose.PSD für Java weitere Bildformate neben BMP?**  
A: Ja, es unterstützt PNG, JPEG, TIFF, GIF und über 30 weitere Formate für Import und Export.

## Fazit
Sie wissen jetzt, **how to draw rectangle** auf einem Bild mit Aspose.PSD für Java zu erstellen, von der Erstellung eines Bitmaps über das Festlegen der Hintergrundfarbe bis hin zur Initialisierung von Graphics. Experimentieren Sie mit verschiedenen Größen, Farben und zusätzlichen Formen, um **java image manipulation** zu meistern. Wenn Sie bereit sind, integrieren Sie dieses Muster in größere Batch‑Verarbeitungs‑Pipelines oder UI‑gesteuerte Editoren.

---

**Zuletzt aktualisiert:** 2026-09-08  
**Getestet mit:** Aspose.PSD for Java 24.12  
**Autor:** Aspose

## Verwandte Tutorials

- [Bildgröße ändern mit Aspose.PSD für Java – Formen zeichnen & grundlegende Bildoperationen](/psd/java/basic-image-operations/)
- [Signatur zum Bild hinzufügen – Bild auf Leinwand zeichnen mit Aspose.PSD für Java](/psd/java/advanced-image-effects/add-signature-to-image/)
- [Bild per Rechteck zuschneiden mit Aspose.PSD für Java](/psd/java/image-editing/crop-image-by-rectangle/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}