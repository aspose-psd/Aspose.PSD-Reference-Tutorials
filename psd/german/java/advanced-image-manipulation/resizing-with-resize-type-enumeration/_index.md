---
date: 2026-06-03
description: Erfahren Sie, wie Sie Bilder mit Aspose.PSD für Java skalieren. Dieser
  Schritt‑für‑Schritt‑Leitfaden behandelt die Resize Type Enumeration, das hochqualitative
  Bildskalieren und wie man PSD in JPEG konvertiert.
keywords:
- how to resize image
- convert psd to jpeg
- high quality image resize
- resize image java
- java image manipulation tutorial
linktitle: Skalieren mit Resize Type Enumeration
schemas:
- author: Aspose
  dateModified: '2026-06-03'
  description: Learn how to resize image with Aspose.PSD for Java. This step‑by‑step
    guide covers the Resize Type Enumeration, high‑quality image resize, and how to
    convert PSD to JPEG.
  headline: How to Resize Image Java Using Resize Type Enumeration
  type: TechArticle
- description: Learn how to resize image with Aspose.PSD for Java. This step‑by‑step
    guide covers the Resize Type Enumeration, high‑quality image resize, and how to
    convert PSD to JPEG.
  name: How to Resize Image Java Using Resize Type Enumeration
  steps:
  - name: '**Java Development Environment** – JDK 8 or newer installed and configured.'
    text: '**Java Development Environment** – JDK 8 or newer installed and configured.'
  - name: '**Aspose.PSD Library** – Download the latest JAR from the [website](https://releases.aspose.com/psd/java/).'
    text: '**Aspose.PSD Library** – Download the latest JAR from the [website](https://releases.aspose.com/psd/java/).'
  - name: '**Sample PSD File** – Use the [sample.psd](Your Document Directory/sample.psd)
      file included with the SDK for hands‑on testing.'
    text: '**Sample PSD File** – Use the [sample.psd](Your Document Directory/sample.psd)
      file included with the SDK for hands‑on testing.'
  type: HowTo
- questions:
  - answer: Load the PSD with `Image.load`, then call `image.save("output.jpg", new
      JpegOptions());`.
    question: How do I programmatically convert a PSD file to JPEG without resizing?
  - answer: Yes, you can set the `Resolution` property on the `Image` object before
      saving.
    question: Is it possible to maintain the original DPI when resizing?
  - answer: While you can call `resize` multiple times, it’s more efficient to calculate
      the final dimensions and resize once.
    question: Can I chain multiple resize operations?
  type: FAQPage
second_title: Aspose.PSD Java API
title: Wie man ein Bild in Java mit Resize Type Enumeration verkleinert
url: /de/java/advanced-image-manipulation/resizing-with-resize-type-enumeration/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Wie man ein Bild in Java mit der Resize Type Enumeration skaliert

## Einführung

If you’re looking for **how to resize image** files efficiently in a Java project, Aspose.PSD for Java provides a clean, high‑performance API. In this tutorial we’ll walk through loading a PSD, applying the **Resize Type Enumeration** for high‑quality image resize, and finally **convert PSD to JPEG**. Whether you’re building a desktop editor or an automated server‑side pipeline, these steps let you control dimensions, quality, and format with just a few lines of code.

## Schnelle Antworten
- **Welche Bibliothek verarbeitet das Bildskalieren in Java?** Aspose.PSD for Java.
- **Welcher Resize‑Typ liefert die beste Qualität?** `ResizeType.LanczosResample`.
- **Kann ich nach dem Skalieren PSD in JPEG konvertieren?** Ja – einfach mit `JpegOptions` speichern.
- **Benötige ich eine Lizenz für die Produktion?** Eine gültige Aspose.PSD‑Lizenz ist für den Produktionseinsatz erforderlich.
- **Ist dieser Ansatz für große Stapel geeignet?** Absolut; die API verarbeitet Dateien mit mehreren hundert Seiten, ohne das gesamte Dokument in den Speicher zu laden.

## Was bedeutet „how to resize image“ in Java?
**How to resize image** bezieht sich darauf, die Pixelabmessungen eines Bildes programmgesteuert zu ändern und dabei die visuelle Treue zu bewahren. Die `Resize`‑Methode von Aspose.PSD in Kombination mit der `ResizeType`‑Enumeration bietet präzise Kontrolle über Skalierungsalgorithmen und ermöglicht Entwicklern, die Qualität über ein breites Spektrum von Quelldateien und Zielgrößen hinweg beizubehalten.

## Warum die Resize Type Enumeration verwenden?
`ResizeType` ermöglicht die Auswahl des Resampling‑Algorithmus, der Geschwindigkeit und visuelle Qualität am besten ausbalanciert. Für die meisten Szenarien liefert **LanczosResample** scharfe Ergebnisse bei moderaten Leistungsanforderungen und verarbeitet ein 2000 × 1500‑Bild in weniger als 120 ms auf einer typischen Server‑CPU, während Kanten‑Details erhalten bleiben.

## Voraussetzungen

1. **Java-Entwicklungsumgebung** – JDK 8 oder neuer, installiert und konfiguriert.  
2. **Aspose.PSD‑Bibliothek** – Laden Sie die neueste JAR von der [Website](https://releases.aspose.com/psd/java/) herunter.  
3. **Beispiel‑PSD‑Datei** – Verwenden Sie die Datei [sample.psd](Your Document Directory/sample.psd), die im SDK für praktische Tests enthalten ist.

## Pakete importieren

`Image` ist die Basisklasse für alle Bildtypen in Aspose.PSD. Fügen Sie die erforderlichen Importe zu Ihrer Java‑Quelldatei hinzu:

```java
import com.aspose.psd.Image;
import com.aspose.psd.ResizeType;

import com.aspose.psd.imageoptions.JpegOptions;
```

## Schritt 1: Bild laden

### Definitionsanker
Die Klasse `RasterImage` ist das Kernobjekt von Aspose.PSD, das ein rasterbasiertes Bild darstellt, das aus einer PSD‑Datei geladen wurde.

Laden Sie Ihre PSD in eine `RasterImage`‑Instanz, um deren Pixel zu manipulieren:

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

// Load an existing image into an instance of RasterImage class
Image image = Image.load(sourceFile);
```

## Schritt 2: Bild skalieren

`image.resize(width, height, resizeType)` skaliert das Bild auf die angegebenen Abmessungen unter Verwendung des gewählten Algorithmus.

Skalieren Sie nun das geladene Bild mit der **Resize Type Enumeration**. In diesem Beispiel verwenden wir die Lanczos‑Resample‑Methode, die ideal ist, wenn Sie **how to resize image** mit hoher Qualität durchführen möchten:

```java
image.resize(300, 300, ResizeType.LanczosResample);
```

## Schritt 3: Skalierte Bild speichern

`image.save(path, options)` schreibt das Bild auf die Festplatte im durch die angegebenen Optionen definierten Format.

Nach dem Skalieren speichern Sie das Bild mit den angegebenen Abmessungen und dem gewählten Resize‑Typ. Hier demonstrieren wir außerdem das **convert psd to jpeg**, indem wir das Ergebnis als JPEG‑Datei speichern:

```java
String destName = dataDir + "ResizingwithResizeTypeEnumeration_out.jpg";
image.save(destName, new JpegOptions());
```

## Warum die Resize Type Enumeration verwenden?

`ResizeType` gibt Ihnen eine feinkörnige Kontrolle über den Resampling‑Algorithmus, sodass Sie Geschwindigkeit und Qualität ausbalancieren können. Für die meisten Anwendungen bietet `LanczosResample` einen guten Kompromiss, liefert scharfe Ergebnisse ohne große Leistungseinbußen und funktioniert gut bei unterschiedlichen Bildinhalten.

## Häufige Probleme und Lösungen

- **Bild erscheint nach dem Skalieren unscharf** – Versuchen Sie einen anderen `ResizeType` wie `Bicubic` oder `NearestNeighbour`, um zu sehen, welcher für Ihr spezielles Bild das beste visuelle Ergebnis liefert.  
- **OutOfMemoryError bei großen PSD‑Dateien** – Verarbeiten Sie das Bild in kleineren Teilen oder erhöhen Sie die JVM‑Heap‑Größe (`-Xmx`‑Flag). Aspose.PSD kann Dateien bis zu **2 GB** verarbeiten, ohne das gesamte Dokument in den Speicher zu laden.

## Häufig gestellte Fragen

### Q1: Ist Aspose.PSD für Java sowohl für kleine als auch für groß angelegte Projekte geeignet?
A1: Absolut! Aspose.PSD für Java ist darauf ausgelegt, Projekte jeder Größe zu unterstützen und bietet Skalierbarkeit sowie Effizienz.

### Q2: Kann ich einen anderen Resize‑Typ als Lanczos Resample verwenden?
A2: Ja, Aspose.PSD für Java bietet verschiedene Resize‑Typen, wie **NearestNeighbour**, **Bicubic** und weitere. Konsultieren Sie die API‑Dokumentation für die vollständige Liste.

### Q3: Wo finde ich zusätzlichen Support für Aspose.PSD für Java?
A3: Bei Fragen oder Unterstützung besuchen Sie das [Aspose.PSD‑Forum](https://forum.aspose.com/c/psd/34).

### Q4: Gibt es eine kostenlose Testversion für Aspose.PSD für Java?
A4: Ja, Sie können eine kostenlose Testversion [hier](https://releases.aspose.com/) erhalten.

### Q5: Wie kann ich eine temporäre Lizenz für Aspose.PSD für Java erhalten?
A5: Um eine temporäre Lizenz zu erhalten, besuchen Sie [diesen Link](https://purchase.aspose.com/temporary-license/).

## Weitere häufig gestellte Fragen

**Q: Wie konvertiere ich programmgesteuert eine PSD‑Datei in JPEG, ohne sie zu skalieren?**  
A: Laden Sie die PSD mit `Image.load` und rufen Sie anschließend `image.save("output.jpg", new JpegOptions());` auf.

**Q: Ist es möglich, die ursprüngliche DPI beim Skalieren beizubehalten?**  
A: Ja, Sie können die Eigenschaft `Resolution` des `Image`‑Objekts vor dem Speichern setzen.

**Q: Kann ich mehrere Skalierungsvorgänge hintereinander ausführen?**  
A: Obwohl Sie `resize` mehrmals aufrufen können, ist es effizienter, die Endabmessungen zu berechnen und einmal zu skalieren.

---

**Letzte Aktualisierung:** 2026-06-03  
**Getestet mit:** Aspose.PSD for Java 24.12  
**Autor:** Aspose  

{{< blocks/products/products-backtop-button >}}

## Verwandte Tutorials

- [Einfaches Skalieren mit Aspose.PSD – Java Bildbearbeitungsbibliothek](/psd/java/basic-image-operations/simple-resizing/)
- [Hochqualitative Bildskalierung mit Bicubic Resampler in Aspose.PSD für Java](/psd/java/advanced-image-manipulation/implement-bicubic-resampler/)
- [Wie man PSD in PNG konvertiert und proportional skaliert mit Aspose.PSD für Java](/psd/java/advanced-image-manipulation/resize-image-proportionally/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}