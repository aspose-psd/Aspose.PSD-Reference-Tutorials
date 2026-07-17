---
date: 2026-07-17
description: Java-Bildverarbeitungs-Tutorial mit Aspose.PSD – Erfahren Sie, wie Sie
  Gaussian- und Wiener-Filter Schritt für Schritt anwenden, um beeindruckende visuelle
  Ergebnisse zu erzielen.
keywords:
- java image processing tutorial
- export png java
- gaussian filter java
- wiener filter java
lastmod: 2026-07-17
linktitle: Gaussian- und Wiener-Filter anwenden
og_description: Java-Bildverarbeitungs-Tutorial demonstriert die Anwendung von Gaussian-
  und Wiener-Filtern mit Aspose.PSD für Java, einschließlich Export nach PNG und anderen
  Formaten.
og_image_alt: 'Developer guide: Apply Gaussian and Wiener filters to images in Java
  using Aspose.PSD'
og_title: Java-Bildverarbeitungs-Tutorial – Gaussian- und Wiener-Filter anwenden
schemas:
- author: Aspose
  dateModified: '2026-07-17'
  description: Java image processing tutorial using Aspose.PSD learn how to apply
    Gaussian and Wiener filters step‑by‑step for stunning visual results.
  headline: Java Image Processing Tutorial – Apply Gaussian & Wiener Filters
  type: TechArticle
- questions:
  - answer: It smooths an image by averaging neighboring pixels, reducing high‑frequency
      noise.
    question: What does the Gaussian filter do?
  - answer: It performs adaptive smoothing, preserving edges while diminishing noise.
    question: What is the Wiener filter?
  - answer: Aspose.PSD for Java provides built‑in support for both filters.
    question: Which library is used?
  - answer: A trial works for testing, but a commercial license is required for production.
    question: Do I need a license?
  - answer: Yes—Aspose.PSD supports PNG, JPEG, BMP, and many more.
    question: Can I output formats other than GIF?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- java image processing
- Aspose.PSD
- gaussian filter
- wiener filter
- export png java
title: Java-Bildverarbeitungs-Tutorial – Gaussian- und Wiener-Filter anwenden
url: /de/java/image-processing/apply-gaussian-wiener-filters/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Java-Bildverarbeitungs‑Tutorial – Gaussian‑ und Wiener‑Filter mit Aspose.PSD anwenden

## Einleitung

Willkommen zu unserem **java image processing tutorial**, das Ihnen zeigt, wie Sie Gaussian‑ und Wiener‑Filter mit Aspose.PSD für Java anwenden. Egal, ob Sie verrauschte Fotos bereinigen oder Grafiken für die Web‑Auslieferung vorbereiten, diese Filter liefern glatte, professionell aussehende Ergebnisse. In den nächsten Minuten sehen Sie den gesamten Arbeitsablauf – vom Laden einer PSD‑Datei bis zum Speichern des gefilterten Ergebnisses als GIF.

## Schnelle Antworten
- **Was bewirkt der Gaussian‑Filter?** Er glättet ein Bild, indem er benachbarte Pixel mittelt und hochfrequentes Rauschen reduziert.  
- **Was ist der Wiener‑Filter?** Er führt adaptive Glättung durch, bewahrt Kanten und reduziert gleichzeitig das Rauschen.  
- **Welche Bibliothek wird verwendet?** Aspose.PSD für Java bietet integrierte Unterstützung für beide Filter.  
- **Benötige ich eine Lizenz?** Eine Testversion funktioniert zum Testen, aber für den Produktionseinsatz ist eine kommerzielle Lizenz erforderlich.  
- **Kann ich andere Ausgabeformate als GIF verwenden?** Ja – Aspose.PSD unterstützt PNG, JPEG, BMP und viele weitere.

## Was ist ein Java‑Bildverarbeitungs‑Tutorial?

Ein Java‑Bildverarbeitungs‑Tutorial führt Entwickler durch die wesentlichen Schritte des Ladens eines Bildes, das Anwenden von Transformationen wie Filtern oder Skalieren und schließlich das Speichern des Ergebnisses in einem gewünschten Format. Durch klare Code‑Beispiele und Erklärungen hilft es Ihnen, Bildbearbeitungs‑Funktionen direkt in Java‑Anwendungen zu integrieren und den Bedarf an externen Tools zu reduzieren.

## Warum Gaussian‑ und Wiener‑Filter verwenden?

Laden Sie Ihr Bild, wenden Sie den kombinierten Gaussian‑Wiener‑Filter an, und Sie werden eine dramatische Reduktion von Körnung sehen, während wichtige Kanten scharf bleiben – ideal für die Vorbereitung von Grafiken für das Web oder für Archivscans. Der Gaussian‑Teil entfernt hochfrequentes Rauschen, und der Wiener‑Teil passt sich der lokalen Varianz an, wobei Details dort erhalten bleiben, wo sie am wichtigsten sind.

## Voraussetzungen

- Eine Java‑Entwicklungsumgebung (JDK 8 oder neuer).  
- Die Aspose.PSD‑Bibliothek für Java. Sie können sie **[hier](https://releases.aspose.com/psd/java/)** herunterladen.  
- Grundlegende Kenntnisse der Java‑Syntax und objektorientierter Konzepte.

## Pakete importieren

Die Import‑Anweisungen bringen die Aspose.PSD‑Klassen in den Gültigkeitsbereich, sodass Sie mit Raster‑Bildern, Filteroptionen und Ausgabeformaten arbeiten können.

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.imagefilters.filteroptions.GaussWienerFilterOptions;
import com.aspose.psd.imageoptions.GifOptions;
```

Diese Importe geben Ihnen Zugriff auf das Laden von Bildern, die Raster‑Manipulation, Filteroptionen und Ausgabeformate.

## Schritt 1: Bild laden

Die Klasse `RasterImage` repräsentiert ein rasterbasiertes Bild, das pixelweise verarbeitet werden kann.

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

Image image = Image.load(sourceFile);
RasterImage rasterImage = (RasterImage)image;
```

Wir laden eine PSD‑Datei aus dem angegebenen Verzeichnis und casten sie zu einem `RasterImage`, damit wir mit den Pixeldaten arbeiten können.

## Schritt 2: RasterImage prüfen

Eine Sicherheitsprüfung bestätigt, dass die geladene Datei rasterbasiert ist; andernfalls beendet die Routine den Vorgang sauber.

```java
if (rasterImage == null) {
    return;
}
```

## Schritt 3: Filteroptionen konfigurieren

Die Klasse `GaussWienerFilterOptions` ermöglicht es Ihnen, sowohl Gaussian‑ als auch Wiener‑Parameter in einem einzigen Objekt fein abzustimmen.

```java
GaussWienerFilterOptions options = new GaussWienerFilterOptions(12, 3);
options.setGrayscale(true);
```

- Das erste Argument (`12`) definiert die Radiusgröße für den Gaussian‑Kernel.  
- Das zweite Argument (`3`) legt den Glättungswert fest, der vom Wiener‑Algorithmus verwendet wird.  
- `setGrayscale(true)` weist den Filter an, in Graustufen zu arbeiten, was häufig zu saubereren Ergebnissen bei der Rauschreduzierung führt.

## Schritt 4: Filter anwenden und speichern

Die Methode `filter` wendet die konfigurierte Gaussian‑Wiener‑Kombination auf das gesamte Bild an. Schließlich speichern wir das verarbeitete Bild als GIF mit `GifOptions`. Sie können `GifOptions` durch `PngOptions`, `JpegOptions` usw. ersetzen, um **PNG‑Java** oder andere Formate zu exportieren.

```java
rasterImage.filter(image.getBounds(), options);
String destName = dataDir + "gauss_wiener_out.gif";
image.save(destName, new GifOptions());
```

## Häufige Probleme & Tipps

- **Null RasterImage:** Stellen Sie sicher, dass die Quelldatei ein PSD oder ein anderes rasterkompatibles Format ist.  
- **Leistung:** Große Bilder können länger dauern; erwägen Sie, den Radius zu reduzieren oder zunächst eine verkleinerte Kopie zu verarbeiten.  
- **Farbe vs. Graustufen:** Wenn Sie Farbe beibehalten müssen, setzen Sie `options.setGrayscale(false)`.

## Häufig gestellte Fragen

**F1: Kann ich diese Filter auf Bilder in anderen Formaten als PSD anwenden?**  
Ja, Aspose.PSD für Java unterstützt verschiedene Bildformate über PSD hinaus, wie PNG, JPEG, BMP und GIF.

**F2: Gibt es Einschränkungen in der Testversion von Aspose.PSD für Java?**  
Die Testversion begrenzt die Ausgabengröße und fügt ein Wasserzeichen hinzu. Um den vollen Funktionsumfang freizuschalten, erhalten Sie eine gültige Lizenz.

**F3: Wie kann ich Support für Aspose.PSD für Java erhalten?**  
Besuchen Sie das **[Aspose.PSD Forum](https://forum.aspose.com/c/psd/34)** für Community‑Unterstützung und offizielle Antworten.

**F4: Gibt es eine temporäre Lizenz für Testzwecke?**  
Ja, Sie können eine temporäre Lizenz **[hier](https://purchase.aspose.com/temporary-license/)** erhalten.

**F5: Wo finde ich detaillierte Dokumentation für Aspose.PSD für Java?**  
Siehe die **[Dokumentation](https://reference.aspose.com/psd/java/)** für ausführliche API‑Referenzen und weitere Beispiele.

## Fazit

Sie haben nun ein vollständiges **java image processing tutorial** abgeschlossen, das zeigt, wie man **Gaussian**‑ und Wiener‑Filter mit Aspose.PSD für Java **anwenden** kann. Experimentieren Sie mit verschiedenen Radius‑ und Glättungswerten, schalten Sie Graustufen ein/aus und probieren Sie andere Ausgabeformate wie PNG, um zu sehen, wie die Filter Ihre Bilder beeinflussen. Viel Spaß beim Programmieren!

---

**Last Updated:** 2026-07-17  
**Tested With:** Aspose.PSD for Java 23.12 (latest at time of writing)  
**Author:** Aspose

## Verwandte Tutorials

- [Schritt‑für‑Schritt‑Filter – Motion‑Wiener‑Filter mit Aspose.PSD für Java anwenden](/psd/java/image-processing/apply-motion-wiener-filters/)
- [Schritt‑für‑Schritt‑Filter – Median‑ & Wiener‑Filter anwenden (Java)](/psd/java/image-processing/apply-median-wiener-filters/)
- [Wie man PNG‑Dateien in Aspose.PSD für Java filtert](/psd/java/optimizing-png-files/apply-filters-png-files/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}