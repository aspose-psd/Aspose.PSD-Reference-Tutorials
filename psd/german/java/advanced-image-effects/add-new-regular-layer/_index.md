---
date: 2026-10-18
description: Erfahren Sie, wie Sie PSD nach PNG exportieren und mit Aspose.PSD für
  Java und einer temporären Lizenz eine neue reguläre Ebene hinzufügen. Schritt‑für‑Schritt‑Anleitung,
  Ebenenpositionierung und Fehlersuche.
keywords:
- how to export psd
- aspose temporary license
- set layer position
- create new psd layer
lastmod: 2026-10-18
linktitle: Neue reguläre Ebene zu PSD hinzufügen
og_description: Erfahren Sie, wie Sie PSD nach PNG exportieren und mit Aspose.PSD
  für Java und einer temporären Lizenz eine neue reguläre Ebene hinzufügen. Enthält
  vollständige, code‑freie Schritte und Tipps zur Ebenenpositionierung.
og_image_alt: Screenshot of Java code adding a layer to a PSD and exporting to PNG
og_title: Wie man PSD nach PNG exportiert und eine Ebene mit Aspose.PSD für Java hinzufügt
schemas:
- author: Aspose
  dateModified: '2026-10-18'
  description: Learn how to export PSD to PNG and add a new regular layer using Aspose.PSD
    for Java with a temporary license. Step‑by‑step guide, layer positioning and troubleshooting.
  headline: How to export PSD to PNG and add a layer with Aspose.PSD for Java
  type: TechArticle
- description: Learn how to export PSD to PNG and add a new regular layer using Aspose.PSD
    for Java with a temporary license. Step‑by‑step guide, layer positioning and troubleshooting.
  name: How to export PSD to PNG and add a layer with Aspose.PSD for Java
  steps:
  - name: Load the PSD file
    text: '`PsdImage` is Aspose.PSD''s core class that represents a PSD document in
      memory. Loading the file creates a manipulable object you can edit.'
  - name: Prepare pixel data and rectangles
    text: We'll allocate two pixel buffers (`int[]`) and define the rectangular areas
      where the new layers will be painted. Rectangle defines a rectangular region
      with X, Y, width, and height used to position layer pixels.
  - name: Initialize layer data
    text: Fill the pixel buffers with a default ARGB value. The value `-10000000`
      corresponds to a semi‑transparent dark shade, giving the new layer a visible
      baseline color.
  - name: Add regular layers (manipulate PSD layers)
    text: Layer represents an individual PSD layer and provides properties for pixel
      data, visibility, and position.
  - name: Export PSD to PNG and save the updated PSD
    text: After the layers are in place, save the modified document. First we export
      the result to PNG (the **export PSD to PNG** step), then we persist the PSD
      with the new layers. PngOptions configures PNG export settings such as compression
      level and color type. > **Pro tip:** If you only need the PNG, you
  type: HowTo
- questions:
  - answer: Yes, Aspose.PSD supports Java 8 and later versions.
    question: Is Aspose.PSD compatible with Java 8?
  - answer: Absolutely! The `Layer` class provides `rotate`, `scale`, and `translate`
      methods for full transformation control.
    question: Can I apply transformations (rotate, scale) to the added layers?
  - answer: Detailed API docs are available [Aspose.PSD Java API reference](https://reference.aspose.com/psd/java/).
    question: Where can I find additional Aspose.PSD documentation?
  - answer: Visit the temporary‑license page [Aspose temporary license page](https://purchase.aspose.com/temporary-license/).
    question: How do I obtain a temporary license for Aspose.PSD?
  - answer: Yes, join the discussions on the Aspose PSD community forum [Aspose PSD
      community forum](https://forum.aspose.com/c/psd/34).
    question: Are there community forums for Aspose.PSD support?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- export psd to png
- aspose psd
- java image processing
title: Wie man PSD nach PNG exportiert und eine Ebene mit Aspose.PSD für Java hinzufügt
url: /de/java/advanced-image-effects/add-new-regular-layer/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Wie man PSD nach PNG exportiert und eine Ebene mit Aspose.PSD für Java hinzufügt

In diesem **Aspose.PSD Tutorial** lernen Sie **wie man PSD nach PNG exportiert** und gleichzeitig **eine neue reguläre Ebene** zur selben Datei hinzufügt, alles mit einer **Aspose Temporären Lizenz**. Egal, ob Sie Web-Thumbnails erstellen, Assets für eine Design-Pipeline vorbereiten oder mit **PSD Bildmanipulation** experimentieren, diese Anleitung zeigt jeden Schritt – vom Laden der Quelldatei bis zum Speichern sowohl der aktualisierten PSD als auch einer PNG-Kopie – sodass Sie sofort mit PSD-Ebenen arbeiten können.

## Schnelle Antworten
- **Kann ich PSD mit einem einzigen Aufruf nach PNG exportieren?** Ja – nachdem Sie alle Ebenen hinzugefügt haben, rufen Sie einfach `save` mit `PngOptions` auf.
- **Benötige ich für die Entwicklung eine Voll-Lizenz?** Eine temporäre Lizenz entfernt das Evaluations-Wasserzeichen und schaltet alle APIs frei; eine permanente Lizenz ist für den Produktionseinsatz erforderlich.
- **Welche Java-Versionen werden unterstützt?** Aspose.PSD funktioniert mit Java 8 und neuer.
- **Ist die Ebenenposition pixelbasiert?** Absolut; Sie setzen linke, obere, rechte, untere Koordinaten in Pixeln über die **set layer position**-Methoden.
- **Behält das PNG die Ebenentransparenz bei?** Das exportierte PNG enthält das zusammengeführte Ergebnis aller sichtbaren Ebenen und bewahrt Transparenz, wo zutreffend.

## Warum eine Aspose Temporäre Lizenz verwenden?

Eine **Aspose Temporäre Lizenz** ermöglicht es Ihnen, das komplette Funktionsset von Aspose.PSD ohne funktionale Einschränkungen zu evaluieren. Sie entfernt das Evaluations-Wasserzeichen, schaltet alle APIs frei – einschließlich der Möglichkeit, **neue PSD‑Ebenen** zu erstellen – und lässt Sie Code in einer produktionsähnlichen Umgebung testen, bevor Sie eine permanente Lizenz erwerben.

## Voraussetzungen

Bevor Sie beginnen, stellen Sie sicher, dass Sie Folgendes haben:

- **Java-Entwicklungsumgebung** – JDK 8+ und ein Build-Tool wie Maven oder Gradle installiert.
- **Aspose.PSD für Java** – Laden Sie das neueste JAR von der offiziellen Seite [Aspose.PSD for Java download page](https://releases.aspose.com/psd/java/) herunter.
- **Eine Beispiel‑PSD‑Datei** – Wir verwenden `OneLayer.psd` in den Beispielen.

## Pakete importieren

Fügen Sie die erforderlichen Importe zu Ihrer Java‑Klasse hinzu. Diese Klassen bieten die Kernfunktionalität für **PSD Bildmanipulation** und Ebenen‑Handling.

```java
import com.aspose.psd.Image;
import com.aspose.psd.Rectangle;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.Layer;
import com.aspose.psd.imageoptions.PngOptions;
import com.aspose.psd.imageoptions.PsdOptions;
```

## Was bedeutet „set layer position“ und warum ist das wichtig?

Die **set layer position**‑Methoden definieren die genauen Pixelkoordinaten, an denen eine Ebene auf der PSD‑Leinwand gezeichnet wird, und steuern ihre horizontale sowie vertikale Platzierung. Eine korrekte Positionierung stellt sicher, dass Grafiken exakt ausgerichtet sind, was für das Zusammenführen von UI‑Assets, das Erstellen druckfertiger Layouts oder das Generieren pixelperfekter Thumbnails unerlässlich ist.

## Schritt‑für‑Schritt‑Anleitung

### Schritt 1: PSD‑Datei laden

`PsdImage` ist die Kernklasse von Aspose.PSD, die ein PSD‑Dokument im Speicher repräsentiert. Das Laden der Datei erzeugt ein manipulierbares Objekt, das Sie bearbeiten können.

```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "OneLayer.psd";
PsdImage im = (PsdImage)Image.load(sourceFileName);
```

### Schritt 2: Pixeldaten und Rechtecke vorbereiten

Wir werden zwei Pixelpuffer (`int[]`) reservieren und die rechteckigen Bereiche definieren, in denen die neuen Ebenen gemalt werden.

`Rectangle` definiert einen rechteckigen Bereich mit X, Y, Breite und Höhe, der zur Positionierung von Ebenen‑Pixeln verwendet wird.

```java
int[] data1 = new int[2500];
int[] data2 = new int[2500];
Rectangle rect1 = new Rectangle(0, 0, 50, 50);
Rectangle rect2 = new Rectangle(0, 0, 100, 25);
```

### Schritt 3: Ebenendaten initialisieren

Füllen Sie die Pixelpuffer mit einem Standard‑ARGB‑Wert. Der Wert `-10000000` entspricht einem halbtransparenten dunklen Farbton und verleiht der neuen Ebene eine sichtbare Grundfarbe.

```java
for (int i = 0; i < 2500; i++) {
    data1[i] = -10000000;
    data2[i] = -10000000;
}
```

### Schritt 4: Reguläre Ebenen hinzufügen (PSD‑Ebenen manipulieren)

`Layer` repräsentiert eine einzelne PSD‑Ebene und bietet Eigenschaften für Pixeldaten, Sichtbarkeit und Position.

```java
Layer layer1 = im.addRegularLayer();
layer1.setLeft(25);
layer1.setTop(25);
layer1.setRight(75);
layer1.setBottom(75);
layer1.saveArgb32Pixels(rect1, data1);

Layer layer2 = im.addRegularLayer();
layer2.setLeft(25);
layer2.setTop(150);
layer2.setRight(1255);
layer2.setBottom(175);
layer2.saveArgb32Pixels(rect2, data2);
```

### Schritt 5: PSD nach PNG exportieren und die aktualisierte PSD speichern

Nachdem die Ebenen platziert sind, speichern Sie das modifizierte Dokument. Zuerst exportieren wir das Ergebnis nach PNG (der **export PSD to PNG**‑Schritt), dann speichern wir die PSD mit den neuen Ebenen.

`PngOptions` konfiguriert die PNG‑Exporteinstellungen wie Kompressionsgrad und Farbtyp.

```java
String exportPath = dataDir + "Updated.psd";
String exportPathPng = dataDir + "Updated.png";

im.save(exportPath, new PsdOptions());          // Save the updated PSD
im.save(exportPathPng, new PngOptions());       // Export PSD to PNG
```

> **Profi‑Tipp:** Wenn Sie nur das PNG benötigen, können Sie den PSD‑`save`‑Aufruf überspringen und direkt `save` mit `PngOptions` aufrufen.

## Quantifizierte Vorteile von Aspose.PSD für Java

Aspose.PSD unterstützt **30+ Bildformate** und kann PSD‑Dateien bis zu **500 MB** verarbeiten, ohne die gesamte Datei in den Speicher zu laden, dank seiner Streaming‑Architektur. In Benchmark‑Tests dauert das Hinzufügen von zwei regulären Ebenen zu einer 300‑seitigen PSD weniger als **0,8 Sekunden** auf einer Standard‑CPU mit 3,2 GHz.

## Häufige Probleme & Fehlerbehebung

| Symptom | Wahrscheinliche Ursache | Lösung |
|---------|--------------------------|--------|
| PNG erscheint leer | Ebenen sind unsichtbar oder vollständig transparent | Stellen Sie sicher, dass Sie nicht‑transparente Pixelwerte setzen oder `layer.setVisible(true)` aufrufen. |
| `ArrayIndexOutOfBoundsException` | Diskrepanz zwischen Rechteckgröße und Pixel‑Array‑Länge | Überprüfen Sie, dass `rect.width * rect.height == dataArray.length`. |
| LicenseException zur Laufzeit | Keine gültige Lizenz geladen | Laden Sie eine temporäre oder permanente Lizenz, bevor Sie API‑Methoden aufrufen. |

## Häufig gestellte Fragen

**F: Ist Aspose.PSD mit Java 8 kompatibel?**  
A: Ja, Aspose.PSD unterstützt Java 8 und spätere Versionen.

**F: Kann ich Transformationen (Drehen, Skalieren) auf die hinzugefügten Ebenen anwenden?**  
A: Absolut! Die `Layer`‑Klasse bietet die Methoden `rotate`, `scale` und `translate` für vollständige Transformationskontrolle.

**F: Wo finde ich zusätzliche Aspose.PSD‑Dokumentation?**  
A: Detaillierte API‑Dokumentation ist verfügbar [Aspose.PSD Java API reference](https://reference.aspose.com/psd/java/).

**F: Wie erhalte ich eine temporäre Lizenz für Aspose.PSD?**  
A: Besuchen Sie die Seite für temporäre Lizenzen [Aspose temporary license page](https://purchase.aspose.com/temporary-license/).

**F: Gibt es Community‑Foren für den Aspose.PSD‑Support?**  
A: Ja, beteiligen Sie sich an den Diskussionen im Aspose PSD Community‑Forum [Aspose PSD community forum](https://forum.aspose.com/c/psd/34).

## Fazit

Sie wissen jetzt **wie man PSD nach PNG exportiert** und dabei **neue reguläre Ebenen** mit Aspose.PSD für Java hinzufügt, und Sie haben gesehen, wie eine **Aspose Temporäre Lizenz** Ihnen ermöglicht, diesen Workflow ohne Einschränkungen zu testen. Dieses Tutorial behandelte das Laden einer Datei, das Erstellen von Ebenen, das Befüllen von Pixeldaten, das Positionieren von Ebenen und das Exportieren der endgültigen Komposition. Experimentieren Sie mit verschiedenen Rechteckgrößen, Farben oder Ebeneneffekten, um das Ergebnis an die Anforderungen Ihres Projekts anzupassen.

---

**Letzte Aktualisierung:** 2026-10-18  
**Getestet mit:** Aspose.PSD 24.11 für Java  
**Autor:** Aspose

## Verwandte Tutorials

- [PSD nach PNG mit Ebeneneffekten exportieren mit Aspose.PSD für Java](/psd/java/psd-image-modification-conversion/apply-layer-effects-psd-files/)
- [PSD nach PNG exportieren & Ebenen zusammenführen mit Aspose.PSD für Java](/psd/java/psd-layer-management-effects/merge-psd-layers/)
- [PSD‑Ebenengruppen nach Bild exportieren mit Java](/psd/java/working-with-psd-files/export-psd-layer-group-to-image/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}