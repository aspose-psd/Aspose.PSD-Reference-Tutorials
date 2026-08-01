---
date: 2026-08-01
description: Erfahren Sie, wie Sie Gamma in der Java-Bildverarbeitung mit Aspose.PSD
  anpassen, PSD in TIFF konvertieren und ausgewaschene Bilder in einem kurzen Tutorial
  beheben.
keywords:
- how to adjust gamma
- fix washed out image
- java image processing
- convert psd to tiff
- server side image processing
lastmod: 2026-08-01
linktitle: Gamma eines Bildes anpassen
og_description: Erfahren Sie, wie Sie Gamma in der Java-Bildverarbeitung mit Aspose.PSD
  anpassen – eine schnelle serverseitige Bibliothek, die ausgewaschene Bilder korrigiert
  und PSD in TIFF in nur wenigen Codezeilen konvertiert.
og_image_alt: 'Guide: Adjust gamma in Java images with Aspose.PSD, convert PSD to
  TIFF'
og_title: wie man Gamma anpasst – Java-Verarbeitung mit Aspose.PSD
schemas:
- author: Aspose
  dateModified: '2026-08-01'
  description: Learn how to adjust gamma in Java image processing with Aspose.PSD,
    convert PSD to TIFF, and fix washed‑out images in a concise tutorial.
  headline: How to Adjust Gamma in Java Image Processing with Aspose.PSD
  type: TechArticle
- description: Learn how to adjust gamma in Java image processing with Aspose.PSD,
    convert PSD to TIFF, and fix washed‑out images in a concise tutorial.
  name: How to Adjust Gamma in Java Image Processing with Aspose.PSD
  steps:
  - name: '**Java Development Environment** – Java 8 or later installed.'
    text: '**Java Development Environment** – Java 8 or later installed.'
  - name: '**Aspose.PSD Library** – Download and add the JAR to your project. See
      the official [documentation](https://reference.aspose.com/psd/java/).'
    text: '**Aspose.PSD Library** – Download and add the JAR to your project. See
      the official [documentation](https://reference.aspose.com/psd/java/).'
  - name: '**Sample Image** – A PSD file you want to process (e.g., `sample.psd`).'
    text: '**Sample Image** – A PSD file you want to process (e.g., `sample.psd`).'
  type: HowTo
- questions:
  - answer: Yes – the `adjustGamma` method accepts separate float values for red,
      green, and blue channels.
    question: Can I apply different gamma values to each colour channel?
  - answer: Absolutely. You can perform resizing, cropping, or colour corrections
      sequentially on the same `RasterImage` instance.
    question: Is it possible to chain multiple image adjustments before saving?
  - answer: Yes, each layer can be accessed and processed individually.
    question: Does Aspose.PSD support multi‑page PSD files?
  - answer: Aspose.PSD supports PNG, JPEG, BMP, and many other formats via their respective
      options classes.
    question: What format can I export to besides TIFF?
  - answer: Start with a moderate gamma (around 2.0) and preview the result; adjust
      downwards if the image looks too bright.
    question: How do I avoid a washed‑out image after gamma correction?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- adjust gamma
- Aspose.PSD
- Java image processing
- PSD to TIFF
- server side processing
title: Wie man Gamma in der Java-Bildverarbeitung mit Aspose.PSD anpasst
url: /de/java/advanced-techniques/adjust-gamma/
weight: 23
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Wie man Gamma in der Java-Bildverarbeitung mit Aspose.PSD anpasst

## Einführung

Wenn Sie an **java image processing** arbeiten, ist das Erlernen **wie man Gamma anpasst** eine grundlegende Technik, um Helligkeit und Kontrast zu verbessern, ohne Details zu verlieren. In diesem Tutorial zeigen wir, wie Sie **Aspose.PSD for Java** verwenden, um eine Gamma‑Korrektur auf eine PSD‑Datei anzuwenden, **PSD zu TIFF konvertieren** und ein **ausgewaschenes Bild** zu vermeiden. Sie werden sehen, warum dieser Ansatz schnell, zuverlässig und perfekt für **serverseitige Bildverarbeitung**‑Pipelines ist.

## Schnelle Antworten
- **Was bewirkt die Gamma‑Korrektur?** Sie ordnet Luminanzwerte neu zu, um dunkle Bereiche heller oder helle Bereiche dunkler zu machen, wobei die Gesamtdetails erhalten bleiben.  
- **Welche Bibliothek übernimmt die Verarbeitung?** Aspose.PSD for Java bietet eine dedizierte `adjustGamma`‑Methode für Rasterbilder.  
- **Kann ich PSD im selben Ablauf zu TIFF konvertieren?** Ja – nach der Gamma‑Anpassung können Sie das Bild direkt mit `TiffOptions` als TIFF speichern.  
- **Benötige ich eine Lizenz für die Entwicklung?** Eine kostenlose Testversion funktioniert zum Testen; für den Produktionseinsatz ist eine kommerzielle Lizenz erforderlich.  
- **Welche Java‑Version wird unterstützt?** Aspose.PSD unterstützt Java 8 und höher.

## Was ist Java Gamma‑Korrektur?

Gamma‑Korrektur ändert die nichtlineare Beziehung zwischen den codierten Pixelwerten und der angezeigten Helligkeit. Durch Anpassen der Gamma‑Kurve können Sie **ausgewaschenes Bild**‑Probleme beheben oder Details in Schatten verbessern, ohne Highlights zu überbelichten. Sie funktioniert, indem sie auf jedes Pixel eine Potenzfunktion anwendet, die dunkle Töne aufhellt und Highlights komprimiert, was zu einem natürlicheren visuellen Erscheinungsbild führt.

## Warum Aspose.PSD für Gamma‑Korrektur verwenden?

Aspose.PSD ist eine **java image processing library**, die die Komplexität des PSD‑Formats abstrahiert. Sie unterstützt die Verarbeitung von Dateien bis zu 2 GB, kann über 50 verschiedene Bildformate handhaben und bietet einen einfachen `adjustGamma`‑Aufruf, wodurch sie ideal für **java gamma correction** und **convert PSD to TIFF**‑Workflows ist.

## Voraussetzungen

1. **Java-Entwicklungsumgebung** – Java 8 oder höher installiert.  
2. **Aspose.PSD Bibliothek** – Herunterladen und das JAR zu Ihrem Projekt hinzufügen. Siehe die offizielle [documentation](https://reference.aspose.com/psd/java/).  
3. **Beispielbild** – Eine PSD‑Datei, die Sie verarbeiten möchten (z. B. `sample.psd`).  

## Pakete importieren

Bevor Sie beginnen, importieren Sie die wesentlichen Namespaces, die Ihnen Zugriff auf Rasterverarbeitung und Dateiformat‑Optionen geben.

## Schritt 1: Bild laden

Die Klasse `RasterImage` repräsentiert die rasterisierten Pixeldaten einer PSD‑Ebene im Speicher. Das einmalige Laden des Bildes und das Zwischenspeichern reduziert den Speicherverbrauch für nachfolgende Anpassungen.

## Schritt 2: Gamma anpassen

Laden Sie Ihre PSD mit `new RasterImage("sample.psd")` und rufen Sie `rasterImage.adjustGamma(2.0f)` auf – diese eine Zeile wendet ein Gamma von 2.0 auf alle Farbkanäle an, hellt Schatten auf und lässt Highlights unverändert. Sie können separate Werte für Rot, Grün und Blau übergeben, falls kanalspezifische Anpassungen erforderlich sind.

## Schritt 3: TiffOptions erstellen

`TiffOptions` ermöglicht die Steuerung von Kompression, Bits pro Sample und anderen TIFF‑spezifischen Einstellungen. Das Festlegen eines 8‑Bit‑Samples (`{8,8,8}`) hält die TIFF‑Dateigröße angemessen, während die Farbtreue erhalten bleibt.

## Schritt 4: Ergebnisbild speichern

Rufen Sie `rasterImage.save("output.tif", tiffOptions)` auf, um das verarbeitete Bild auf die Festplatte zu schreiben. Nach dem Speichern können Sie das TIFF in nachgelagerte Systeme wie Druckdienste oder Web‑APIs einspeisen.

## Häufige Anwendungsfälle

- **Automatisierte Grafik‑Pipelines** – Gamma on‑the‑fly anpassen, bevor Thumbnails erzeugt werden.  
- **Batch‑Konvertierungstools** – Große PSD‑Archive zu TIFF konvertieren und dabei die Helligkeit normalisieren.  
- **Web‑Dienste** – Einen Endpunkt bereitstellen, der ein PSD empfängt, Gamma‑Korrektur anwendet und ein TIFF für den Client zurückgibt.

## Häufige Probleme und Lösungen

| Issue | Why it Happens | How to Fix |
|-------|----------------|------------|
| **Bild erscheint ausgewaschen** | Gamma‑Wert zu hoch (z. B. > 2.5) | Gamma‑Faktor auf einen Wert zwischen 1.8 und 2.2 senken. |
| **`rasterImage.isCached()` returns false** | Bild noch nicht in den Speicher geladen | `rasterImage.cacheData()` vor der Gamma‑Anpassung aufrufen. |
| **TIFF‑Dateigröße ist groß** | Bits pro Sample auf 16‑Bit gesetzt | Ein 8‑Bit‑Sample (`{8,8,8}`) wie im Beispiel verwenden. |

## Häufig gestellte Fragen

**F: Kann ich verschiedene Gamma‑Werte auf jeden Farbkanal anwenden?**  
A: Ja – die `adjustGamma`‑Methode akzeptiert separate Float‑Werte für Rot-, Grün- und Blau‑Kanäle.

**F: Ist es möglich, mehrere Bildanpassungen vor dem Speichern zu verketten?**  
A: Absolut. Sie können Größenänderungen, Zuschneiden oder Farbkorrekturen nacheinander am selben `RasterImage`‑Objekt durchführen.

**F: Unterstützt Aspose.PSD mehrseitige PSD‑Dateien?**  
A: Ja, jede Ebene kann einzeln zugegriffen und verarbeitet werden.

**F: In welches Format kann ich außer TIFF exportieren?**  
A: Aspose.PSD unterstützt PNG, JPEG, BMP und viele andere Formate über die jeweiligen Options‑Klassen.

**F: Wie vermeide ich ein ausgewaschenes Bild nach der Gamma‑Korrektur?**  
A: Beginnen Sie mit einem moderaten Gamma (etwa 2.0) und prüfen Sie das Ergebnis; reduzieren Sie den Wert, wenn das Bild zu hell wirkt.

## Fazit

Herzlichen Glückwunsch! Sie haben erfolgreich **how to adjust gamma** in einem **java image processing**‑Workflow gelernt, ein PSD zu TIFF konvertiert und gängige Fallstricke wie ein **washed‑out image** vermieden. Dieses Muster gibt Ihnen eine feinkörnige Kontrolle über Helligkeit und Kontrast und ist ideal für automatisierte Grafik‑Pipelines, Web‑Dienste oder Desktop‑Utilities.

---

**Zuletzt aktualisiert:** 2026-08-01  
**Getestet mit:** Aspose.PSD 24.11 for Java  
**Autor:** Aspose  

{{< blocks/products/products-backtop-button >}}

## Verwandte Tutorials

- [Java-Bildverarbeitungs‑Tutorial – Helligkeit eines Bildes mit Aspose.PSD für Java anpassen](/psd/java/advanced-techniques/adjust-brightness/)
- [Wie man PSD zu TIFF konvertiert und den Kontrast mit Aspose.PSD für Java anpasst](/psd/java/advanced-techniques/adjust-contrast/)
- [PSD in Java zu Bild konvertieren – Anpassungsebenen mit Aspose.PSD anwenden](/psd/java/advanced-psd-layer-features-effects/apply-adjustment-layers-psd-files/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.psd.fileformats.tiff.enums.TiffPhotometrics;
import com.aspose.psd.imageoptions.TiffOptions;
```

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

// Load an existing image into an instance of RasterImage class
Image image = Image.load(sourceFile);

// Cast object of Image to RasterImage
RasterImage rasterImage = (RasterImage)image;

// Check if RasterImage is cached for better performance
if (!rasterImage.isCached()) {
    rasterImage.cacheData();
}
```

```java
// Adjust the gamma
rasterImage.adjustGamma(2.2f, 2.2f, 2.2f);
```

```java
// Create an instance of TiffOptions for the resultant image
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
int[] ushort = { 8, 8, 8 };
tiffOptions.setBitsPerSample(ushort);
tiffOptions.setPhotometric(TiffPhotometrics.Rgb);
```

```java
// Save the resultant image to TIFF format
String destName = dataDir + "AdjustGamma_out.tiff";
rasterImage.save(destName, tiffOptions);
```