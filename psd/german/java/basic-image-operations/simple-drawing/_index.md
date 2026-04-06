---
date: 2025-12-27
description: Erfahren Sie, wie Sie in PSD‑Dateien mit Aspose.PSD für Java rote Rechtecke
  und andere Formen zeichnen. Diese Schritt‑für‑Schritt‑Anleitung behandelt das Erstellen
  von Dokumenten, das Hinzufügen von Ebenen und das Zeichnen mit Codebeispielen.
linktitle: Perform Simple Drawing
second_title: Aspose.PSD Java API
title: Rotes Rechteck mit Aspose.PSD für Java zeichnen
url: /de/java/basic-image-operations/simple-drawing/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Rotes Rechteck mit Aspose.PSD für Java zeichnen

## Einführung

Willkommen zu dieser Schritt‑für‑Schritt‑Anleitung, wie Sie **rotes Rechteck** mit Aspose.PSD für Java zeichnen! In diesem Tutorial führen wir Sie durch das Erstellen eines neuen PSD‑Dokuments, das Hinzufügen einer Ebene und das Zeichnen von Formen mit benutzerdefinierten Farben. Egal, ob Sie Grafik‑Assets automatisieren oder ein Backend für ein Design‑Tool erstellen, dieses Tutorial liefert Ihnen die wesentlichen Bausteine.

## Schnellantworten
- **Was ist die primäre Klasse zum Erstellen einer PSD‑Datei?** `PsdImage`
- **Welche Methode löscht die Hintergrundfarbe einer Ebene?** `Graphics.clear(Color)`
- **Wie zeichnet man ein rotes Rechteck?** `graphic.drawRectangle(new Pen(Color.getRed()), new Rectangle(...))`
- **Benötige ich eine Lizenz für die Entwicklung?** Eine kostenlose Testversion reicht für Tests; für die Produktion ist eine Lizenz erforderlich.
- **Kann ich bestehende PSD‑Dateien mit derselben API manipulieren?** Ja, Aspose.PSD unterstützt die vollständige PSD‑Bearbeitung.

## Was bedeutet das Zeichnen eines roten Rechtecks in einer PSD‑Datei?
Das Zeichnen eines roten Rechtecks bedeutet, dass das `Graphics`‑Objekt verwendet wird, um eine rechteckige Form, gefüllt oder umrandet mit der Farbe Rot, auf einer bestimmten Ebene eines PSD‑Bildes zu rendern. Dieser Vorgang wird häufig zum Hervorheben von Bereichen, Erstellen von Platzhaltern oder Hinzufügen einfacher Grafiken programmgesteuert verwendet.

## Warum Aspose.PSD für Java zur Manipulation von PSD‑Dateien verwenden?
Aspose.PSD bietet eine reine Java‑API, mit der Sie Photoshop‑PSD‑Dateien lesen, bearbeiten und schreiben können, ohne dass Photoshop installiert sein muss. Sie unterstützt Ebenenverwaltung, Farbmanipulation und Vektordrawing, was sie ideal für serverseitige Bildverarbeitung, automatisierte Asset‑Pipelines und benutzerdefinierte Grafikgenerierung macht.

## Voraussetzungen

- Java Development Kit (JDK) auf Ihrem Rechner installiert.  
- Aspose.PSD für Java Bibliothek. Sie können sie von der [Aspose.PSD for Java Documentation](https://reference.aspose.com/psd/java/) herunterladen.

## Pakete importieren

Um zu beginnen, importieren Sie die erforderlichen Klassen in Ihr Java‑Projekt:

```java
import com.aspose.psd.Color;
import com.aspose.psd.Graphics;
import com.aspose.psd.Pen;
import com.aspose.psd.Rectangle;
import com.aspose.psd.brushes.SolidBrush;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.Layer;
```

## Schritt 1: Ein neues Dokument erstellen

Erstellen Sie zunächst ein frisches PSD‑Dokument mit der gewünschten Canvas‑Größe. Dieses Dokument wird die Ebene hosten, auf der wir zeichnen.

```java
//ExStart:CreateDocument
String outputDir = "Your Document Directory";
String outPsdFilePath = outputDir + "output.psd";
int width = 100;
int height = 100;

PsdImage image = new PsdImage(width, height);
//ExEnd:CreateDocument
```

## Schritt 2: Eine Ebene hinzufügen

Fügen Sie als Nächstes eine neue leere Ebene hinzu, die die gesamte Breite und Höhe des Bildes abdeckt. Ebenen sind wichtig, um Zeichenoperationen zu trennen.

```java
//ExStart:AddLayer
Layer layer = new Layer();
layer.setBottom(height);
layer.setRight(width);
image.addLayer(layer);
//ExEnd:AddLayer
```

## Schritt 3: Formen zeichnen

Wir verwenden die Klasse `Graphics`, um die Pixeldaten der Ebene zu manipulieren. Nachfolgend finden Sie drei Beispiele, die das Löschen des Hintergrunds und das Zeichnen von Rechtecken mit unterschiedlichen Farben veranschaulichen.

### Ebene‑Farbe löschen (Hintergrund auf Gelb setzen)

```java
//ExStart:DrawRectangleYellow
Graphics graphic = new Graphics(layer);
graphic.clear(Color.getYellow());
//ExEnd:DrawRectangleYellow
```

### Rotes Rechteck zeichnen (Hauptfokus)

```java
//ExStart:DrawRedRectangle
graphic.drawRectangle(new Pen(Color.getRed()), new Rectangle(30, 10, 40, 80));
//ExEnd:DrawRedRectangle
```

### Blaues Rechteck zeichnen (zusätzliches Beispiel)

```java
//ExStart:DrawBlueRectangle
graphic.drawRectangle(new Pen(new SolidBrush(Color.getBlue())), new Rectangle(10, 30, 80, 40));
//ExEnd:DrawBlueRectangle
```

## Schritt 4: Änderungen speichern

Schreiben Sie schließlich das modifizierte PSD‑Bild auf die Festplatte. Die Datei enthält die neue Ebene und die gezeichneten Formen.

```java
//ExStart:SaveChanges
image.save(outPsdFilePath);
//ExEnd:SaveChanges
```

## Häufige Probleme und Lösungen

- **Ebene nach dem Zeichnen nicht sichtbar:** Stellen Sie sicher, dass die Ebene dem Bild **vor** dem Erzeugen des `Graphics`‑Objekts hinzugefügt wird.
- **Farben erscheinen falsch:** Vergewissern Sie sich, dass Sie `Color.getRed()` (oder andere statische Methoden) verwenden und nicht benutzerdefinierte RGB‑Werte, die außerhalb des zulässigen Bereichs liegen könnten.
- **Datei wird nicht gespeichert:** Prüfen Sie, ob der Pfad `outputDir` existiert und die Anwendung Schreibrechte hat.

## Häufig gestellte Fragen

### Q1: Kann ich Aspose.PSD für Java verwenden, um bestehende PSD‑Dateien zu manipulieren?

A1: Ja, Aspose.PSD für Java bietet umfangreiche Funktionen zum Bearbeiten und Manipulieren vorhandener PSD‑Dateien.

### Q2: Wo finde ich Support für Aspose.PSD für Java?

A2: Sie können das [Aspose.PSD for Java Forum](https://forum.aspose.com/c/psd/34) für supportbezogene Anfragen besuchen.

### Q3: Gibt es eine kostenlose Testversion von Aspose.PSD für Java?

A3: Ja, Sie können die kostenlose Testversion [hier](https://releases.aspose.com/) abrufen.

### Q4: Wie kann ich eine Lizenz für Aspose.PSD für Java erwerben?

A4: Sie können eine Lizenz über die [Aspose.PSD Purchase Page](https://purchase.aspose.com/buy) kaufen.

### Q5: Gibt es temporäre Lizenzen für Aspose.PSD für Java?

A5: Ja, eine temporäre Lizenz erhalten Sie [hier](https://purchase.aspose.com/temporary-license/).

## Weitere häufig gestellte Fragen

**Q: Kann ich neben Rechtecken auch andere Formen zeichnen?**  
A: Ja, die Klasse `Graphics` unterstützt ebenfalls das Zeichnen von Ellipsen, Linien und benutzerdefinierten Pfaden.

**Q: Unterstützt Aspose.PSD Transparenz bei gezeichneten Formen?**  
A: Absolut; Sie können `SolidBrush` mit einer ARGB‑Farbe verwenden, um Alpha‑Transparenz einzubeziehen.

**Q: Ist es möglich, die Opazität einer Ebene zu bearbeiten?**  
A: Ja, jedes `Layer`‑Objekt verfügt über eine `setOpacity`‑Methode, die einen Wert von 0 bis 255 akzeptiert.

**Q: Wie lade ich eine bestehende PSD‑Datei, anstatt eine neue zu erstellen?**  
A: Verwenden Sie `PsdImage image = (PsdImage)Image.load("path/to/file.psd");` bevor Sie Ebenen manipulieren.

## Fazit

Sie haben nun gelernt, wie Sie **rotes Rechteck** und andere Grundformen in einer PSD‑Datei mit Aspose.PSD für Java zeichnen. Durch das Erstellen eines Dokuments, das Hinzufügen einer Ebene, das Löschen des Hintergrunds und das Zeichnen mit der `Graphics`‑API können Sie viele Grafik‑Design‑Aufgaben automatisieren. Experimentieren Sie weiter mit verschiedenen Pinseln, Ebeneneffekten und Dateiformaten.

---

**Zuletzt aktualisiert:** 2025-12-27  
**Getestet mit:** Aspose.PSD für Java 24.12 (zum Zeitpunkt der Erstellung die neueste Version)  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}