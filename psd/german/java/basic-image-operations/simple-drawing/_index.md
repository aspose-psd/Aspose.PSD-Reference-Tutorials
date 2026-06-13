---
date: 2026-06-13
description: Erfahren Sie, wie Sie ein Rechteck in PSD‑Dateien mit Aspose.PSD für
  Java zeichnen. Dieser Leitfaden zeigt step‑by‑step code, adding layers, server‑side
  image processing und shape drawing.
keywords:
- how to draw rectangle
- how to create psd
- java graphics draw rectangle
- server side image processing
- add layer to psd
linktitle: Einfaches Zeichnen durchführen
schemas:
- author: Aspose
  dateModified: '2026-06-13'
  description: Learn how to draw rectangle in PSD files using Aspose.PSD for Java.
    This guide shows step‑by‑step code, adding layers, server‑side image processing
    and shape drawing.
  headline: How to Draw Rectangle in PSD with Aspose.PSD for Java
  type: TechArticle
- questions:
  - answer: Yes, the `Graphics` class also supports drawing ellipses, lines, and custom
      paths via the `drawPath` method.
    question: Can I draw other shapes besides rectangles?
  - answer: Absolutely; you can use `SolidBrush` with an ARGB color to include alpha
      transparency, enabling semi‑transparent overlays.
    question: Does Aspose.PSD support transparency in drawn shapes?
  - answer: Yes, each `Layer` object has a `setOpacity` method that accepts a value
      from 0 to 255, allowing fine‑grained control over layer transparency.
    question: Is it possible to edit the opacity of a layer?
  - answer: Use `PsdImage image = (PsdImage)Image.load("path/to/file.psd");` before
      manipulating layers. The loaded image retains all original layers and masks.
    question: How do I load an existing PSD file instead of creating a new one?
  type: FAQPage
second_title: Aspose.PSD Java API
title: Wie man ein Rechteck in PSD mit Aspose.PSD für Java zeichnet
url: /de/java/basic-image-operations/simple-drawing/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Wie man ein Rechteck in PSD mit Aspose.PSD für Java zeichnet

## Einführung

In diesem Tutorial entdecken Sie **wie man ein Rechteck zeichnet** Formen innerhalb einer Photoshop‑PSD‑Datei mithilfe der reinen Java‑Bibliothek Aspose.PSD. Egal, ob Sie eine serverseitige Asset‑Pipeline aufbauen, die Erstellung von Vorschaubildern automatisieren oder dynamische Grafiken zu bestehenden Designs hinzufügen, die nachfolgenden Schritte bieten Ihnen eine vollständige, produktionsreife Lösung. Wir behandeln das Erstellen eines neuen PSD‑Dokuments, das Hinzufügen einer Ebene, das Löschen des Hintergrunds und schließlich das Zeichnen roter und blauer Rechtecke – alles ohne Photoshop zu starten.

## Schnelle Antworten
- **Was ist die primäre Klasse zum Erstellen einer PSD‑Datei?** `PsdImage`
- **Welche Methode löscht die Hintergrundfarbe einer Ebene?** `Graphics.clear(Color)`
- **Wie zeichnet man ein rotes Rechteck?** `graphic.drawRectangle(new Pen(Color.getRed()), new Rectangle(...))`
- **Benötige ich eine Lizenz für die Entwicklung?** Eine kostenlose Testversion funktioniert für Tests; für die Produktion ist eine Lizenz erforderlich.
- **Kann ich vorhandene PSD‑Dateien mit derselben API manipulieren?** Ja, Aspose.PSD unterstützt die vollständige PSD‑Bearbeitung.

## Was bedeutet das Zeichnen eines roten Rechtecks in einer PSD‑Datei?

Ein rotes Rechteck zu zeichnen bedeutet, das `Graphics`‑Objekt zu verwenden, um eine rechteckige Form, gefüllt oder umrandet mit der Farbe Rot, auf einer bestimmten Ebene eines PSD‑Bildes zu rendern. Dieser Vorgang ist üblich, um Bereiche hervorzuheben, Platzhalter zu erstellen oder einfache Grafiken programmgesteuert hinzuzufügen.

## Warum Aspose.PSD für Java zur Manipulation von PSD‑Dateien verwenden?

Aspose.PSD für Java unterstützt **mehr als 50 Eingabe‑ und Ausgabeformate**, kann mehrseitige PSD‑Dateien verarbeiten, ohne die gesamte Datei in den Speicher zu laden, und läuft auf jeder Plattform, die Java 8 oder höher unterstützt. Seine serverseitige Bildverarbeitungs‑Engine eliminiert die Notwendigkeit von Photoshop, senkt Lizenzkosten und ermöglicht automatisierte Workflows, die bis zu **10 GB** Bilddaten pro Stunde auf einer bescheidenen VM verarbeiten.

## Voraussetzungen

- Java Development Kit (JDK) 8 oder höher, auf Ihrem Rechner installiert.  
- Aspose.PSD für Java Bibliothek. Sie können sie von der [Aspose.PSD for Java Documentation](https://reference.aspose.com/psd/java/) herunterladen.

## Pakete importieren

Die `import`‑Anweisungen bringen die erforderlichen Klassen in den Gültigkeitsbereich, damit Sie mit PSD‑Bildern, Ebenen, Farben und Grafiken arbeiten können.

Die Klasse `PsdImage` ist das Top‑Level‑Objekt von Aspose.PSD, das eine einzelne PSD‑Datei im Speicher repräsentiert.  
`Graphics` stellt Zeichenprimitive wie Linien, Rechtecke und Ellipsen bereit.  
`Color` und `Pen` ermöglichen die Angabe von Strichfarben und -stärken.  
Die Klasse `Layer` repräsentiert eine einzelne Bildebene innerhalb eines PSD‑Dokuments.  
Die Klasse `Rectangle` definiert die Position und Größe eines rechteckigen Bereichs, der für Zeichenoperationen verwendet wird.  
Die Klasse `SolidBrush` füllt Formen mit einer Vollfarbe.

## Was ist der erste Schritt zum Erstellen eines PSD‑Dokuments?

Sie instanziieren `PsdImage`, indem Sie die Breite und Höhe der Leinwand in Pixel angeben, wodurch eine leere PSD‑Dateistruktur erstellt wird. Nachdem Sie etwaige Anfangsebenen oder den Hintergrund eingerichtet haben, rufen Sie die `save`‑Methode mit einem Dateipfad auf, um das Dokument auf die Festplatte zu schreiben. Dies bereitet das Bild für nachfolgende Bearbeitungsoperationen vor.

## Schritt 1: Neues Dokument erstellen

Zuerst erstellen Sie ein frisches PSD‑Dokument mit der gewünschten Leinwandgröße. Dieses Dokument wird die Ebene beherbergen, auf der wir zeichnen.

```java
import com.aspose.psd.Color;
import com.aspose.psd.Graphics;
import com.aspose.psd.Pen;
import com.aspose.psd.Rectangle;
import com.aspose.psd.brushes.SolidBrush;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.Layer;
```

## Wie fügt man einer PSD‑Bilddatei eine neue leere Ebene hinzu?

Zuerst erstellen Sie eine neue `Layer`‑Instanz mit derselben Breite und Höhe wie das übergeordnete `PsdImage`. Dann fügen Sie diese Ebene mittels der `add`‑Methode zur `Layers`‑Sammlung des Bildes hinzu. Sobald die Ebene Teil des Bildes ist, rufen Sie ihr `Graphics`‑Objekt ab, um Zeichenoperationen durchzuführen; ohne diesen Schritt erscheinen die Zeichnungen nicht.

## Schritt 2: Ebene hinzufügen

Als Nächstes fügen Sie eine neue leere Ebene hinzu, die die gesamte Breite und Höhe des Bildes abdeckt. Ebenen sind unerlässlich, um Zeichenoperationen zu trennen.

```java
//ExStart:CreateDocument
String outputDir = "Your Document Directory";
String outPsdFilePath = outputDir + "output.psd";
int width = 100;
int height = 100;

PsdImage image = new PsdImage(width, height);
//ExEnd:CreateDocument
```

## Was ist der Zweck des Löschens der Hintergrundfarbe einer Ebene?

Der Aufruf von `Graphics.clear` mit einer bestimmten `Color` füllt die gesamte Ebene mit dieser Farbe und setzt damit alle Pixeldaten zurück. Dadurch wird sichergestellt, dass vorheriger Inhalt entfernt wird und die Ebene von einem bekannten Hintergrund startet, was unerwartete Transparenz oder Farbmischungen verhindert, wenn die PSD später in Photoshop geöffnet oder bearbeitet wird.

## Schritt 3: Formen zeichnen

Wir werden die Klasse `Graphics` verwenden, um die Pixeldaten der Ebene zu manipulieren. Nachfolgend finden Sie drei Beispiele, die das Löschen des Hintergrunds und das Zeichnen von Rechtecken mit unterschiedlichen Farben veranschaulichen.

### Ebenenfarbe löschen (Hintergrund auf Gelb setzen)

```java
//ExStart:AddLayer
Layer layer = new Layer();
layer.setBottom(height);
layer.setRight(width);
image.addLayer(layer);
//ExEnd:AddLayer
```

### Rotes Rechteck zeichnen (Hauptfokus)

```java
//ExStart:DrawRectangleYellow
Graphics graphic = new Graphics(layer);
graphic.clear(Color.getYellow());
//ExEnd:DrawRectangleYellow
```

### Blaues Rechteck zeichnen (zusätzliches Beispiel)

```java
//ExStart:DrawRedRectangle
graphic.drawRectangle(new Pen(Color.getRed()), new Rectangle(30, 10, 40, 80));
//ExEnd:DrawRedRectangle
```

## Wie speichert man die bearbeitete PSD‑Datei auf der Festplatte?

Verwenden Sie die `save`‑Methode des `PsdImage`‑Objekts und übergeben Sie den vollständigen Dateipfad, optional können Sie das gewünschte Bildformat angeben (standardmäßig PSD). Dadurch werden alle Ebenen, Masken und Zeichenbefehle in eine einzige PSD‑Datei geschrieben, die der Photoshop‑Spezifikation entspricht und ohne Warnungen geöffnet werden kann.

## Schritt 4: Änderungen speichern

Abschließend schreiben Sie das modifizierte PSD‑Bild auf die Festplatte. Die Datei enthält die neue Ebene und die gezeichneten Formen.

```java
//ExStart:DrawBlueRectangle
graphic.drawRectangle(new Pen(new SolidBrush(Color.getBlue())), new Rectangle(10, 30, 80, 40));
//ExEnd:DrawBlueRectangle
```

## Häufige Probleme und Lösungen

- **Ebene nach dem Zeichnen nicht sichtbar:** Stellen Sie sicher, dass die Ebene dem Bild **vor** dem Erstellen des `Graphics`‑Objekts hinzugefügt wird. Die Zeichenfläche muss einer gültigen Ebene zugeordnet sein.
- **Farben erscheinen falsch:** Vergewissern Sie sich, dass Sie `Color.getRed()` (oder `Color.getBlue()`) verwenden und nicht einen benutzerdefinierten RGB‑Wert, der den Bereich 0‑255 überschreitet.
- **Datei nicht gespeichert:** Stellen Sie sicher, dass der Pfad `outputDir` existiert und die Anwendung Schreibrechte hat. Unter Linux müssen Sie möglicherweise die Ordnerberechtigungen anpassen oder `Files.createDirectories` verwenden.
- **Leistungsverlust bei großen Dateien:** Verwenden Sie `PsdImage`'s `setLoadOptions`, um nur die benötigten Kanäle zu laden, wodurch der Speicherverbrauch bei PSDs größer als 200 MB reduziert wird.

## Häufig gestellte Fragen

**Q1: Kann ich Aspose.PSD für Java verwenden, um vorhandene PSD‑Dateien zu manipulieren?**  
A1: Ja, Aspose.PSD für Java bietet umfangreiche Funktionen zum Bearbeiten und Manipulieren vorhandener PSD‑Dateien, einschließlich Ebenen‑Neuanordnung, Maskenanpassungen und Vektorgezeichnung.

**Q2: Wo finde ich Support für Aspose.PSD für Java?**  
A2: Sie können das [Aspose.PSD for Java Forum](https://forum.aspose.com/c/psd/34) besuchen, um community‑basierte Unterstützung und offizielle Antworten von Aspose zu erhalten.

**Q3: Gibt es eine kostenlose Testversion für Aspose.PSD für Java?**  
A3: Ja, Sie können die kostenlose Testversion [hier](https://releases.aspose.com/) abrufen. Die Testversion enthält alle Funktionen, fügt jedoch ein Wasserzeichen zu gespeicherten Dateien hinzu.

**Q4: Wie kann ich eine Lizenz für Aspose.PSD für Java erwerben?**  
A4: Sie können eine Lizenz über die [Aspose.PSD Purchase Page](https://purchase.aspose.com/buy) kaufen. Lizenzoptionen umfassen unbefristete, Abonnement‑ und Site‑Lizenzen.

**Q5: Gibt es temporäre Lizenzen für Aspose.PSD für Java?**  
A5: Ja, Sie können eine temporäre Lizenz [hier](https://purchase.aspose.com/temporary-license/) erhalten.

## Weitere häufig gestellte Fragen

**Q: Kann ich neben Rechtecken auch andere Formen zeichnen?**  
A: Ja, die Klasse `Graphics` unterstützt ebenfalls das Zeichnen von Ellipsen, Linien und benutzerdefinierten Pfaden über die Methode `drawPath`.

**Q: Unterstützt Aspose.PSD Transparenz bei gezeichneten Formen?**  
A: Absolut; Sie können `SolidBrush` mit einer ARGB‑Farbe verwenden, um Alpha‑Transparenz einzuschließen und halbtransparente Overlays zu ermöglichen.

**Q: Ist es möglich, die Deckkraft einer Ebene zu bearbeiten?**  
A: Ja, jedes `Layer`‑Objekt verfügt über eine `setOpacity`‑Methode, die einen Wert von 0 bis 255 akzeptiert und eine feine Steuerung der Ebenentransparenz ermöglicht.

**Q: Wie lade ich eine vorhandene PSD‑Datei, anstatt eine neue zu erstellen?**  
A: Verwenden Sie `PsdImage image = (PsdImage)Image.load("path/to/file.psd");` bevor Sie Ebenen manipulieren. Das geladene Bild behält alle ursprünglichen Ebenen und Masken bei.

## Fazit

Sie haben nun **wie man ein Rechteck zeichnet** Formen und Ebenen in einer PSD‑Datei mit Aspose.PSD für Java gemeistert. Durch das Erstellen eines Dokuments, das Hinzufügen einer Ebene, das Löschen des Hintergrunds und das Zeichnen mit der `Graphics`‑API können Sie unzählige Grafikdesign‑Aufgaben serverseitig automatisieren. Experimentieren Sie mit verschiedenen Pens, Brushes und Ebeneneffekten, um diese Grundlage zu einer vollwertigen Bildgenerierungspipeline auszubauen.

```java
//ExStart:SaveChanges
image.save(outPsdFilePath);
//ExEnd:SaveChanges
```

{{< blocks/products/products-backtop-button >}}

## Verwandte Tutorials

- [Wie man Formen in Java zeichnet – Grundlegende Bildoperationen](/psd/java/basic-image-operations/)
- [Einfaches Skalieren mit Aspose.PSD – Java Bildbearbeitungsbibliothek](/psd/java/basic-image-operations/simple-resizing/)
- [Bild zuschneiden nach Rechteck in Aspose.PSD für Java](/psd/java/image-editing/crop-image-by-rectangle/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

---

**Zuletzt aktualisiert:** 2026-06-13  
**Getestet mit:** Aspose.PSD for Java 24.12 (latest at time of writing)  
**Autor:** Aspose