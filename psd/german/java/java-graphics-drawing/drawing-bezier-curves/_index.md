---
date: 2026-01-17
description: Erfahren Sie, wie Sie ein Bezier‑Kurven‑Bild in Java mit Aspose.PSD erstellen.
  Diese Schritt‑für‑Schritt‑Anleitung behandelt das Zeichnen von Bezier‑Kurven in
  Java, die Einstellung der Stiftbreite und das Exportieren des Ergebnisses.
linktitle: How to Create Bezier Curve Image in Java
second_title: Aspose.PSD Java API
title: Wie man ein Bézierkurven‑Bild in Java erstellt
url: /de/java/java-graphics-drawing/drawing-bezier-curves/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Wie man ein Bezier‑Kurvenbild in Java erstellt

## Einführung
Wenn Sie ein **Bezier‑Kurvenbild** für eine Java‑Desktop‑ oder Server‑Anwendung benötigen, macht Aspose.PSD für Java die Aufgabe mühelos. In diesem Tutorial führen wir Sie durch das Zeichnen einer glatten Bezier‑Kurve, das Anpassen der Stiftbreite und das Speichern des Ergebnisses als Bitmap. Am Ende sind Sie mit der Methode `drawBezier()` vertraut und bereit, vektorartige Grafiken in jedes Java‑Projekt zu integrieren.

## Schnelle Antworten
- **Welche Bibliothek ist am besten zum Zeichnen von Kurven in Java?** Aspose.PSD für Java bietet eine voll ausgestattete Grafik‑API.  
- **Wie lange dauert es, ein einfaches Bezier‑Kurvenbild zu erstellen?** In der Regel weniger als 10 Minuten, sobald das SDK eingerichtet ist.  
- **Welche Bildformate werden für den Export unterstützt?** BMP, PNG, JPEG, TIFF und weitere.  
- **Kann ich die Stiftbreite der Kurve ändern?** Ja – der `Pen`‑Konstruktor ermöglicht es, jede gewünschte Breite anzugeben.  
- **Benötige ich eine Lizenz für den Produktionseinsatz?** Für den Einsatz außerhalb der Evaluierung ist eine kommerzielle Lizenz erforderlich.

## Was bedeutet „create bezier curve image“?
Ein Bezier‑Kurvenbild zu erstellen bedeutet, ein Rasterbild zu erzeugen, das eine mathematisch definierte Kurve enthält. Die Kurve wird durch einen Startpunkt, zwei Kontrollpunkte und einen Endpunkt definiert, sodass Sie glatte, skalierbare Formen erzeugen können, die in jeder Größe gut aussehen.

## Warum Aspose.PSD für Java verwenden?
- **Umfangreiche Grafik‑Primitive** – Linien, Formen und Kurven zeichnen, ohne sich mit Pixel‑Manipulation auf niedriger Ebene befassen zu müssen.  
- **Plattformübergreifend** – funktioniert auf jedem Betriebssystem, das Java unterstützt.  
- **Unterstützung hoher Auflösung** – große Leinwände verarbeiten, ohne übermäßigen Speicherverbrauch.  
- **Einfacher Export** – mit einer einzigen Codezeile zwischen BMP, PNG, JPEG, TIFF wechseln.

## Voraussetzungen
Bevor Sie beginnen, stellen Sie sicher, dass Sie Folgendes haben:

1. **Java Development Kit (JDK)** – jede aktuelle Version (8 oder neuer).  
2. **Aspose.PSD for Java JAR** – laden Sie es von [here](https://releases.aspose.com/psd/java/) herunter und fügen Sie es dem Klassenpfad Ihres Projekts hinzu.  
3. **IDE** – Eclipse, IntelliJ IDEA oder ein beliebiger Editor Ihrer Wahl, konfiguriert mit dem JDK.

## Pakete importieren
Bevor Sie mit der Implementierung beginnen, importieren Sie die erforderlichen Aspose.PSD‑Klassen:

```java
import com.aspose.psd.Color;
import com.aspose.psd.Graphics;
import com.aspose.psd.Image;
import com.aspose.psd.Pen;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.BmpOptions;
```

## Schritt‑für‑Schritt‑Anleitung

### Schritt 1: Bildinstanz erstellen
Zuerst müssen Sie eine Instanz der Klasse `PsdImage` erstellen, die ein PSD‑Bild im Speicher repräsentiert.

```java
String dataDir = "Your Document Directory";
Image image = new PsdImage(100, 100);
```

*Erklärung*: `PsdImage` wird mit einer Breite und Höhe von **100 × 100 Pixel** instanziiert – Sie können diese Werte für eine höher aufgelöste Ausgabe erhöhen.

### Schritt 2: Grafik‑Kontext initialisieren
Als Nächstes initialisieren Sie eine Instanz der Klasse `Graphics`, um Zeichenoperationen auf dem Bild auszuführen.

```java
Graphics graphics = new Graphics(image);
```

*Erklärung*: Das `Graphics`‑Objekt verbindet die Zeichenbefehle mit dem `image`, das wir gerade erstellt haben.

### Schritt 3: Grafikfläche löschen
Löschen Sie die Grafikfläche mit einer bestimmten Hintergrundfarbe, hier `Color.getYellow()`.

```java
graphics.clear(Color.getYellow());
```

*Erklärung*: Dies setzt einen leuchtend gelben Hintergrund, sodass die schwarze Bezier‑Kurve hervorsticht.

### Schritt 4: Stift zum Zeichnen initialisieren
Richten Sie ein `Pen`‑Objekt mit Eigenschaften wie Farbe und Breite ein, um zu definieren, wie die Kurve gezeichnet wird.

```java
Pen blackPen = new Pen(Color.getBlack(), 3);
```

*Erklärung*: Der Stift ist schwarz und **3 Pixel breit** – Sie können die Breite anpassen, um die Kurve dicker oder dünner zu machen (`java graphics pen width`).

### Schritt 5: Bezier‑Kurvenparameter festlegen
Geben Sie die Kontrollpunkte und Endpunkte für die Bezier‑Kurve an.

```java
float startX = 10, startY = 25;
float controlX1 = 20, controlY1 = 5;
float controlX2 = 55, controlY2 = 10;
float endX = 90, endY = 25;
```

*Erklärung*:  
- `startX`, `startY` – Startpunkt der Kurve.  
- `controlX1`, `controlY1` – erster Kontrollpunkt.  
- `controlX2`, `controlY2` – zweiter Kontrollpunkt.  
- `endX`, `endY` – Endpunkt.

### Schritt 6: Bezier‑Kurve zeichnen
Verwenden Sie die Methode `drawBezier()`, um die Bezier‑Kurve auf das Bild zu zeichnen, wobei Sie den zuvor definierten `Pen` und die Kontrollpunkte nutzen.

```java
graphics.drawBezier(blackPen, startX, startY, controlX1, controlY1, controlX2, controlY2, endX, endY);
```

*Erklärung*: Dieser einzelne Aufruf rendert eine glatte **draw bezier curve java**‑Linie, die den von Ihnen angegebenen Kontrollpunkten folgt.

### Schritt 7: Bild speichern
Speichern Sie das gezeichnete Bild im BMP‑Dateiformat.

```java
String outpath = dataDir + "Bezier.bmp";
BmpOptions saveOptions = new BmpOptions();
image.save(outpath, saveOptions);
```

*Erklärung*: Das `BmpOptions`‑Objekt weist Aspose.PSD an, die Datei als BMP zu schreiben. Tauschen Sie es gegen `PngOptions`, `JpegOptions` usw. aus, wenn Sie ein anderes Format benötigen.

## Häufige Probleme & Lösungen
- **Kurve erscheint flach** – Überprüfen Sie die Koordinaten der Kontrollpunkte; sie dürfen nicht kollinear mit den Start‑/Endpunkten sein.  
- **Bild ist leer** – Stellen Sie sicher, dass `graphics.clear()` vor dem Zeichnen aufgerufen wird und dass die `Pen`‑Farbe einen Kontrast zum Hintergrund bildet.  
- **OutOfMemoryError bei großen Leinwänden** – Erhöhen Sie die JVM‑Heap‑Größe (`-Xmx`) oder arbeiten Sie mit geteilten Bildern.

## FAQ

### Kann ich mehrere Bezier‑Kurven im selben Bild zeichnen?
Ja, Sie können mehrere Kurven zeichnen, indem Sie den Vorgang in einer Schleife wiederholen und dabei die Kontrollpunkte und Endpunkte nach Bedarf ändern.

### Wie kann ich die Farbe der Bezier‑Kurve ändern?
Ändern Sie die Farbeigenschaft des `Pen`‑Objekts (`Color.getBlack()` im Beispiel) bevor Sie `drawBezier()` aufrufen.

### Ist Aspose.PSD für Java für hochauflösende Bilder geeignet?
Ja, Aspose.PSD für Java unterstützt hochauflösende Bilder mit effizientem Speicher‑Management.

### Kann ich das Bild in andere Formate als BMP exportieren?
Ja, Aspose.PSD für Java unterstützt den Export in verschiedene Formate wie PNG, JPEG, TIFF usw.

### Wo finde ich weitere Beispiele und Dokumentation?
Besuchen Sie die [Aspose.PSD for Java documentation](https://reference.aspose.com/psd/java/) für umfassende Anleitungen und Code‑Beispiele.

## Fazit
Wenn Sie diesem **bezier curve tutorial java** folgen, wissen Sie jetzt, wie Sie mit Aspose.PSD für Java ein **Bezier‑Kurvenbild** erstellen. Experimentieren Sie mit verschiedenen Kontrollpunkten, Stiftfarben und Linienbreiten, um eine Vielzahl künstlerischer Effekte in Ihren Java‑Anwendungen zu erzeugen.

---

**Zuletzt aktualisiert:** 2026-01-17  
**Getestet mit:** Aspose.PSD for Java 24.12 (latest at time of writing)  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}