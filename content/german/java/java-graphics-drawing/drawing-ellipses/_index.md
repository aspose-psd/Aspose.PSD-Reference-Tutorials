---
title: Zeichnen von Ellipsen in Java
linktitle: Zeichnen von Ellipsen in Java
second_title: Aspose.PSD Java-API
description: Erfahren Sie, wie Sie mit Aspose.PSD Ellipsen in Java zeichnen, um präzises Grafikdesign und Bildbearbeitung zu ermöglichen. Meistern Sie Schritt-für-Schritt-Anleitungen.
type: docs
weight: 15
url: /de/java/java-graphics-drawing/drawing-ellipses/
---
## Einführung
In diesem Tutorial erfahren Sie, wie Sie mit Aspose.PSD für Java Ellipsen zeichnen. Aspose.PSD ist eine leistungsstarke Bibliothek, die es Java-Entwicklern ermöglicht, problemlos mit PSD-Dateien zu arbeiten und Bilder zu bearbeiten. Das Zeichnen von Formen wie Ellipsen ist eine grundlegende Aufgabe in der Bildverarbeitung und im Grafikdesign. Wenn Sie dieser Anleitung folgen, sammeln Sie praktische Erfahrungen beim programmgesteuerten Erstellen von Ellipsen mit Aspose.PSD.
## Voraussetzungen
Bevor Sie beginnen, stellen Sie sicher, dass Sie über Folgendes verfügen:
- Grundkenntnisse der Java-Programmierung.
- JDK (Java Development Kit) auf Ihrem System installiert.
- Integrierte Entwicklungsumgebung (IDE) wie IntelliJ IDEA oder Eclipse.
-  Aspose.PSD für Java-Bibliothek. Sie können es herunterladen unter[Hier](https://releases.aspose.com/psd/java/).
## Pakete importieren
Zuerst müssen Sie die erforderlichen Pakete aus Aspose.PSD importieren:
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
## Schritt 1: Richten Sie Ihr Java-Projekt ein
Bevor Sie mit dem Codieren beginnen, stellen Sie sicher, dass Ihr Java-Projekt korrekt eingerichtet ist und Aspose.PSD als Abhängigkeit enthalten ist.
## Schritt 2: Erstellen Sie eine Instanz von PsdImage
Initialisieren Sie eine neue Instanz von PsdImage mit der gewünschten Breite und Höhe.
```java
Image image = new PsdImage(100, 100);
```
## Schritt 3: Grafikobjekt initialisieren
Erstellen und initialisieren Sie eine Instanz von Graphics, um mit dem Bild zu arbeiten.
```java
Graphics graphics = new Graphics(image);
```
## Schritt 4: Reinigen Sie die Grafikoberfläche
Reinigen Sie die Grafikoberfläche vor dem Zeichnen mit einer bestimmten Farbe (optional).
```java
graphics.clear(Color.getYellow());
```
## Schritt 5: Zeichnen Sie eine gepunktete Ellipse.
Verwenden Sie ein Pen-Objekt mit roter Farbe und zeichnen Sie eine gepunktete Ellipse innerhalb eines angegebenen Rechtecks.
```java
graphics.drawEllipse(new Pen(Color.getRed()), new Rectangle(30, 10, 40, 80));
```
## Schritt 6: Zeichnen Sie eine durchgehende Ellipse
Erstellen Sie ein Stiftobjekt mit einem durchgehenden blauen Pinsel und zeichnen Sie eine durchgehende Ellipse innerhalb eines anderen Rechtecks.
```java
graphics.drawEllipse(new Pen(new SolidBrush(Color.getBlue())), new Rectangle(10, 30, 80, 40));
```
## Schritt 7: Speichern Sie das Bild
Speichern Sie abschließend das generierte Bild im BMP-Format unter einem angegebenen Pfad.
```java
String outputPath = "Your Document Directory/Ellipse.bmp";
BmpOptions saveOptions = new BmpOptions();
saveOptions.setBitsPerPixel(32);
image.save(outputPath, saveOptions);
```

## Abschluss
Glückwunsch! Sie haben erfolgreich gelernt, wie Sie mit Aspose.PSD für Java programmgesteuert Ellipsen zeichnen. In diesem Tutorial wurde das Einrichten Ihres Projekts, das Initialisieren von Grafiken, das Zeichnen gepunkteter und kontinuierlicher Ellipsen sowie das Speichern des resultierenden Bildes behandelt. Jetzt können Sie diese Techniken für verschiedene Grafikdesign- und Bildbearbeitungsaufgaben in Ihre Java-Anwendungen integrieren.
## FAQs
### Kann ich Aspose.PSD kostenlos nutzen?
Aspose.PSD bietet eine kostenlose Testversion, mit der Sie die Funktionen vor dem Kauf testen können.
### Wo finde ich weitere Beispiele und Dokumentation?
 Besuchen[Aspose.PSD-Dokumentation](https://reference.aspose.com/psd/java/) Ausführliche Anleitungen und Beispiele finden Sie hier.
### Wie kann ich temporäre Lizenzen für Aspose.PSD erhalten?
 Temporäre Lizenzen sind erhältlich bei[Temporäre Aspose.PSD-Lizenz](https://purchase.aspose.com/temporary-license/).
### In welchen Formaten kann Aspose.PSD Bilder speichern?
Aspose.PSD unterstützt das Speichern von Bildern in verschiedenen Formaten, einschließlich BMP, PNG, JPEG und PSD.
### Ist Aspose.PSD für den Unternehmenseinsatz geeignet?
Ja, Aspose.PSD ist für Bildverarbeitungsaufgaben auf professioneller und Unternehmensebene konzipiert.