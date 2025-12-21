---
date: 2025-12-21
description: Erfahren Sie, wie Sie den Kontrast von Bildern mit Aspose.PSD für Java,
  einer führenden Java‑Bildbearbeitungsbibliothek, anpassen und PSD effizient in TIFF
  konvertieren.
linktitle: Adjust Contrast of an Image
second_title: Aspose.PSD Java API
title: Wie man den Kontrast eines Bildes mit Aspose.PSD für Java anpasst
url: /de/java/advanced-techniques/adjust-contrast/
weight: 22
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Wie man den Kontrast eines Bildes mit Aspose.PSD für Java anpasst

## Einführung

Wenn Sie nach **wie man den Kontrast anpasst** in Ihren Java‑Projekten suchen, sind Sie hier genau richtig. Aspose.PSD für Java ist eine leistungsstarke **java image manipulation library**, die es Ihnen ermöglicht, Bildeigenschaften wie Kontrast, Helligkeit und mehr fein abzustimmen. In diesem Tutorial führen wir Sie durch die genauen Schritte, um den Kontrast einer PSD‑Datei zu erhöhen und anschließend **PSD zu TIFF zu konvertieren** für nachgelagerte Workflows.

## Schnelle Antworten
- **Was bedeutet „adjust contrast“?** Es ändert den Unterschied zwischen den dunkelsten und hellsten Pixeln und lässt Details hervortreten.
- **Welche Bibliothek übernimmt das?** Aspose.PSD für Java – ein voll ausgestattetes Image‑Processing‑Toolkit.
- **Brauche ich eine Lizenz?** Eine temporäre Lizenz funktioniert für Tests; für die Produktion ist eine Voll‑Lizenz erforderlich.
- **Kann ich das Ergebnis als TIFF speichern?** Ja, wir verwenden `TiffOptions`, um das verarbeitete Bild zu exportieren.
- **Wie lange dauert die Ausführung des Codes?** In der Regel unter einer Sekunde für PSD‑Dateien Standardgröße.

## Was ist die Kontrastanpassung?
Die Kontrastanpassung verändert den Tonumfang eines Bildes und verstärkt den Unterschied zwischen hellen und dunklen Bereichen. Dies ist besonders nützlich, wenn Bilder nach dem Scannen flach wirken oder wenn Grafiken für den Druck vorbereitet werden.

## Warum Aspose.PSD für Java verwenden?
- **Umfangreiche Formatunterstützung** – öffnen, bearbeiten und speichern Sie PSD, TIFF, PNG, JPEG und viele weitere.
- **Hohe Leistung** – Caching und Raster‑Image‑Optimierungen reduzieren den Speicherverbrauch.
- **Einfach zu nutzende API** – Aufrufe mit einer einzigen Methode wie `adjustContrast` machen den Code lesbar.

## Voraussetzungen

- Grundkenntnisse in der Java‑Programmierung.
- Aspose.PSD für Java Bibliothek installiert. Sie können sie [hier](https://releases.aspose.com/psd/java/) herunterladen.

## Pakete importieren

Fügen Sie die erforderlichen Importe zu Ihrer Java‑Klasse hinzu:

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.psd.fileformats.tiff.enums.TiffPhotometrics;
import com.aspose.psd.imageoptions.TiffOptions;
```

## Schritt 1: Bild laden

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

// Load an existing image into an instance of RasterImage class
Image image = Image.load(sourceFile);
```

Wir laden die Quell‑PSD‑Datei (`sample.psd`) in ein `Image`‑Objekt, das als Einstiegspunkt für alle weiteren Verarbeitungsschritte dient.

## Schritt 2: In RasterImage umwandeln und Daten cachen

```java
// Cast object of Image to RasterImage
RasterImage rasterImage = (RasterImage)image;

// Check if RasterImage is cached and Cache RasterImage for better performance
if (!rasterImage.isCached()) {
    rasterImage.cacheData();
}
```

Das Umwandeln in `RasterImage` gibt uns Zugriff auf Pixel‑Operationen. Caching verbessert die Leistung, insbesondere bei großen Dateien.

## Wie man den Kontrast eines Bildes anpasst

```java
// Adjust the contrast
rasterImage.adjustContrast(50);
```

Die Methode `adjustContrast` nimmt einen Integer entgegen, der die prozentuale Änderung darstellt. In diesem Beispiel erhöhen wir den Kontrast um **50 %**.

## PSD mit Aspose.PSD zu TIFF konvertieren

```java
// Create an instance of TiffOptions for the resultant image
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
int[] ushort = { 8, 8, 8 };
tiffOptions.setBitsPerSample(ushort);
tiffOptions.setPhotometric(TiffPhotometrics.Rgb);

// Save the resultant image to TIFF format
String destName = dataDir + "AdjustContrast_out.tiff";
rasterImage.save(destName, tiffOptions);
```

Hier konfigurieren wir `TiffOptions` (Bits pro Sample, photometrische Interpretation) und schreiben das kontrastverstärkte Bild in eine TIFF‑Datei.

## Häufige Probleme und Lösungen
- **Bild nicht gecached:** Rufen Sie immer `cacheData()` für große PSDs auf, um `OutOfMemoryError` zu vermeiden.
- **Unerwartete Farbverschiebung:** Stellen Sie sicher, dass `setPhotometric` zu Ihrem Ziel‑Farbraum (RGB vs. CMYK) passt.
- **Datei nicht gefunden:** Stellen Sie sicher, dass `dataDir` auf den richtigen Ordner zeigt und der Dateiname korrekt geschrieben ist.

## Häufig gestellte Fragen

### Q1: Ist Aspose.PSD mit verschiedenen Bildformaten kompatibel?

A1: Ja, Aspose.PSD unterstützt verschiedene Bildformate und bietet Flexibilität in Ihren Projekten.

### Q2: Wie kann ich eine temporäre Lizenz für Aspose.PSD erhalten?

A2: Sie können eine temporäre Lizenz [hier](https://purchase.aspose.com/temporary-license/) erhalten.

### Q3: Wo finde ich die Aspose.PSD-Dokumentation?

A3: Die Dokumentation ist [hier](https://reference.aspose.com/psd/java/) verfügbar.

### Q4: Welche Support‑Optionen gibt es für Aspose.PSD?

A4: Für Support besuchen Sie das [Aspose.PSD‑Forum](https://forum.aspose.com/c/psd/34).

### Q5: Kann ich Aspose.PSD kaufen?

A5: Ja, Sie können Aspose.PSD [hier](https://purchase.aspose.com/buy) erwerben.

## Fazit

Sie wissen jetzt, **wie man den Kontrast** eines PSD‑Bildes mit Aspose.PSD für Java anpasst und **wie man PSD zu TIFF** für die weitere Verarbeitung konvertiert. Diese Schritte geben Ihnen eine feinkörnige Kontrolle über die Bildqualität, während der Code sauber und wartbar bleibt. Experimentieren Sie gern mit anderen Bildanpassungsmethoden wie `adjustBrightness` oder `adjustGamma`, um Ihren spezifischen Anforderungen gerecht zu werden.

---

**Last Updated:** 2025-12-21  
**Tested With:** Aspose.PSD for Java 24.12  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}