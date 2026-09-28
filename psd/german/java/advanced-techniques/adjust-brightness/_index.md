---
date: 2026-09-28
description: Java-Bildverarbeitungs‑Tutorial zeigt, wie man die Helligkeit eines Bildes
  mit Aspose.PSD für Java anpasst. Folgen Sie dem step‑by‑step‑Code, um PSD‑ oder
  TIFF‑Dateien zu laden, zu ändern und zu speichern.
keywords:
- java image processing
- aspose psd java
- java image manipulation
- adjust brightness java
lastmod: 2026-09-28
linktitle: Helligkeit eines Bildes anpassen
og_description: Java-Bildverarbeitungs‑Tutorial zeigt, wie man die Helligkeit eines
  Bildes mit Aspose.PSD für Java anpasst. Folgen Sie dem step‑by‑step‑Code, um PSD‑
  oder TIFF‑Dateien zu laden, zu ändern und zu speichern.
og_image_alt: Guide to adjusting image brightness in Java using Aspose.PSD
og_title: 'Java-Bildverarbeitung: Helligkeit anpassen mit Aspose.PSD'
schemas:
- author: Aspose
  dateModified: '2026-09-28'
  description: Java image processing tutorial shows how to adjust brightness of an
    image using Aspose.PSD for Java. Follow step‑by‑step code to load, modify, and
    save PSD or TIFF files.
  headline: 'Java image processing: adjust brightness with Aspose.PSD'
  type: TechArticle
- description: Java image processing tutorial shows how to adjust brightness of an
    image using Aspose.PSD for Java. Follow step‑by‑step code to load, modify, and
    save PSD or TIFF files.
  name: 'Java image processing: adjust brightness with Aspose.PSD'
  steps:
  - name: Load the image
    text: The `RasterImage` class represents a rasterized version of a PSD or TIFF
      file in memory. It provides direct pixel access for color‑correction operations.
      In this step, we load the target image and cast it to a `RasterImage` for further
      processing.
  - name: Adjust brightness
    text: '`adjustBrightness(int value)` changes the lightness of every pixel by the
      specified integer value. Positive numbers brighten the image; negative numbers
      darken it. The method processes the image in‑place, so no additional object
      creation is required. Here, we use the `adjustBrightness` method to mod'
  - name: Set TiffOptions
    text: '`TiffOptions` specifies the encoding parameters for TIFF output, such as
      bits per sample and photometric interpretation. It lets you control how the
      resulting file is encoded. Configure the `TiffOptions` for saving the adjusted
      image. Adjust the `bitsPerSample` and `photometric` properties based on '
  - name: Save the resultant image
    text: Calling `save` writes the processed raster data to a file using the previously
      defined options. The operation is atomic and guarantees that the output file
      is a valid TIFF image. Finally, save the modified image using the specified
      `TiffOptions`.
  type: HowTo
- questions:
  - answer: Yes, Aspose.PSD for Java supports JPEG, PNG, BMP, GIF, and many other
      raster formats in addition to PSD and TIFF.
    question: Can I adjust brightness in other image formats besides PSD?
  - answer: Wrap the processing code in a try‑catch block and catch `IOException`
      or `ImageProcessingException` to manage file‑access and raster‑operation errors.
    question: How can I handle errors during the image adjustment process?
  - answer: The method accepts integer values from –255 to +255; values outside this
      range are clamped to the nearest limit.
    question: Is there a limit to the range of brightness adjustment?
  - answer: Yes, a commercial license is required for production use. Purchase a license
      [here](https://purchase.aspose.com/buy).
    question: Can I use Aspose.PSD for Java in commercial projects?
  - answer: Yes, you can explore the library with a free trial from [here](https://releases.aspose.com/).
    question: Is there a free trial available?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- java image processing
- aspose psd
- java image manipulation
title: 'Java-Bildverarbeitung: Helligkeit anpassen mit Aspose.PSD'
url: /de/java/advanced-techniques/adjust-brightness/
weight: 21
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Helligkeit eines Bildes mit Aspose.PSD für Java anpassen

## Einleitung

In diesem **java image processing** Tutorial lernen Sie, wie Sie die Helligkeit eines Bildes direkt aus Java‑Code heraus anpassen. Das Anpassen der Helligkeit ist eine häufige Aufgabe für Grafikdesigner, Fotografen und alle, die Bild‑Verarbeitungspipelines erstellen. In diesem **java image manipulation** Leitfaden gehen wir den kompletten Workflow durch – Laden einer PSD/TIFF, Anwenden eines Helligkeits‑Offsets und Speichern des Ergebnisses – unter Verwendung der Aspose.PSD für Java Bibliothek.

## Schnelle Antworten
- **Welche Bibliothek verarbeitet die Helligkeit?** Aspose.PSD for Java.  
- **Welche Methode ändert die Helligkeit?** `RasterImage.adjustBrightness()`.  
- **Kann ich mit PSD- und TIFF-Dateien arbeiten?** Yes, the API supports both formats and 10+ additional image types.  
- **Benötige ich eine Lizenz für die Produktion?** A commercial license is required for non‑evaluation use.  
- **Wie lange dauert die Implementierung?** Typically under 10 minutes for a basic adjustment.

## Was ist java image processing?

`Java image processing` bezieht sich auf die Menge von Techniken, die es ermöglichen, Bilddaten programmgesteuert mit Java zu lesen, zu transformieren und zu schreiben. Das Anpassen der Helligkeit ist einer der Kernoperationen, die die Gesamthelligkeit jedes Pixels ändern, dunkle Bereiche aufhellen oder helle Bereiche abdunkeln.

## Warum Aspose.PSD für Java verwenden?

Aspose.PSD für Java bietet eine umfassende, reine‑Java‑Lösung, die eine breite Palette von Raster‑ und Vektorformaten unterstützt, native Abhängigkeiten eliminiert und ein Hochleistungs‑Caching für große Dateien bereitstellt. Seine umfangreiche API ermöglicht es Entwicklern, komplexe Farbkorrektur‑ und schichtbasierte Bearbeitungen mit minimalem Code durchzuführen, wodurch sie sowohl für einfache Anpassungen als auch für fortgeschrittene Bild‑Verarbeitungspipelines ideal ist.

- **Unterstützt 10+ Raster‑ und Vektorformate** – PSD, TIFF, JPEG, PNG, BMP, GIF und mehr.  
- **Reine‑Java‑Implementierung** – keine nativen DLLs oder externen Abhängigkeiten, sodass sie auf jeder JVM funktioniert.  
- **Hochleistungs‑Caching** – Rasterdaten können zwischengespeichert werden, was bis zu 2× schnellere wiederholte Bearbeitungen großer Dateien ermöglicht.  
- **Umfangreiche API** – über 150 Methoden für Farbkorrektur, Ebenenverwaltung, Masken und Kompositing.

## Voraussetzungen

Bevor Sie in das Tutorial eintauchen, stellen Sie sicher, dass Sie die folgenden Voraussetzungen erfüllen:

- Aspose.PSD for Java Library: Laden Sie die Bibliothek von der [Aspose.PSD for Java documentation](https://reference.aspose.com/psd/java/) herunter und installieren Sie sie.  
- Java Development Kit (JDK) 8 oder höher, das auf Ihrem Rechner installiert ist.  
- Eine Entwicklungsumgebung (IDE) wie IntelliJ IDEA, Eclipse oder VS Code.

## Pakete importieren

Um zu beginnen, importieren Sie die notwendigen Pakete in Ihr Java‑Projekt. In diesem Beispiel verwenden wir das Folgende:

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.psd.fileformats.tiff.enums.TiffPhotometrics;
import com.aspose.psd.imageoptions.TiffOptions;
```

Nun zerlegen wir den Prozess des Anpassen der Helligkeit eines Bildes in einfache Schritte:

## Wie man die Helligkeit mit Aspose.PSD anpasst?

Laden Sie Ihr Quellbild, wenden Sie einen Helligkeits‑Offset an, konfigurieren Sie die Speicheroptionen und schreiben Sie das Ergebnis auf die Festplatte – alles in vier prägnanten Schritten. Die folgenden Abschnitte bieten eine klare, schritt‑für‑schritt Anleitung, die Sie in Ihr eigenes Projekt übernehmen können. Dieser Ansatz stellt sicher, dass jede Operation effizient ausgeführt wird und das endgültige Bild die ursprüngliche Qualität beibehält, während es die gewünschte Helligkeitsänderung widerspiegelt.

### Schritt 1: Bild laden

Die Klasse `RasterImage` repräsentiert eine rasterisierte Version einer PSD‑ oder TIFF‑Datei im Speicher. Sie bietet direkten Pixelzugriff für Farbkorrekturoperationen.

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";
String destName = dataDir + "AdjustBrightness_out.tiff";

// Load an existing image into an instance of RasterImage class
Image image = Image.load(sourceFile);
// Cast object of Image to RasterImage
RasterImage rasterImage = (RasterImage) image;

// Check if RasterImage is cached and Cache RasterImage for better performance
if (!rasterImage.isCached()) {
    rasterImage.cacheData();
}
```

In diesem Schritt laden wir das Zielbild und casten es zu einem `RasterImage` für die weitere Verarbeitung.

### Schritt 2: Helligkeit anpassen

`adjustBrightness(int value)` ändert die Helligkeit jedes Pixels um den angegebenen ganzzahligen Wert. Positive Zahlen hellen das Bild auf; negative Zahlen verdunkeln es. Die Methode verarbeitet das Bild inplace, sodass keine zusätzliche Objekterstellung erforderlich ist.

```java
// Adjust the brightness
rasterImage.adjustBrightness(-50);
```

Hier verwenden wir die Methode `adjustBrightness`, um die Helligkeit des Bildes zu ändern. In diesem Beispiel verringern wir die Helligkeit um 50 Einheiten, Sie können diesen Wert jedoch nach Ihren Anforderungen anpassen.

### Schritt 3: TiffOptions festlegen

`TiffOptions` gibt die Kodierungsparameter für die TIFF‑Ausgabe an, wie Bits pro Sample und photometrische Interpretation. Damit können Sie steuern, wie die resultierende Datei kodiert wird.

```java
int[] ushort = {8, 8, 8};
// Create an instance of TiffOptions for the resultant image
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
tiffOptions.setBitsPerSample(ushort);
tiffOptions.setPhotometric(TiffPhotometrics.Rgb);
```

Konfigurieren Sie die `TiffOptions` zum Speichern des angepassten Bildes. Passen Sie die Eigenschaften `bitsPerSample` und `photometric` nach Ihren spezifischen Bedürfnissen an.

### Schritt 4: Ergebnisbild speichern

Der Aufruf von `save` schreibt die verarbeiteten Rasterdaten mithilfe der zuvor definierten Optionen in eine Datei. Der Vorgang ist atomar und garantiert, dass die Ausgabedatei ein gültiges TIFF‑Bild ist.

```java
// Save the resultant image
rasterImage.save(destName, tiffOptions);
```

## Häufige Probleme und Lösungen

| Problem | Grund | Lösung |
|-------|--------|----------|
| **`ClassCastException` beim Casten von Image** | Die Datei ist kein Rasterbild (z. B. ein Vektor‑PSD). | Überprüfen Sie das Quelldateiformat oder verwenden Sie `image instanceof RasterImage` vor dem Casten. |
| **Helligkeitsänderung hat keine Wirkung** | Das Bild wurde vor der Anpassung nicht zwischengespeichert. | Rufen Sie `rasterImage.cacheData()` wie in Schritt 1 gezeigt auf. |
| **Gespeicherte Datei erscheint beschädigt** | Falsche `TiffOptions`‑Konfiguration. | Stellen Sie sicher, dass `bitsPerSample` der Tiefe des Quellbildes entspricht (in der Regel 8‑Bit pro Kanal). |

## Häufig gestellte Fragen

**Q: Kann ich die Helligkeit in anderen Bildformaten außer PSD anpassen?**  
A: Ja, Aspose.PSD für Java unterstützt JPEG, PNG, BMP, GIF und viele andere Rasterformate zusätzlich zu PSD und TIFF.

**Q: Wie kann ich Fehler während des Bildanpassungsprozesses behandeln?**  
A: Wickeln Sie den Verarbeitungscode in einen try‑catch‑Block und fangen Sie `IOException` oder `ImageProcessingException`, um Datei‑Zugriffs‑ und Raster‑Operationsfehler zu verwalten.

**Q: Gibt es eine Begrenzung für den Bereich der Helligkeitsanpassung?**  
A: Die Methode akzeptiert ganzzahlige Werte von –255 bis +255; Werte außerhalb dieses Bereichs werden auf das nächste Limit begrenzt.

**Q: Kann ich Aspose.PSD für Java in kommerziellen Projekten verwenden?**  
A: Ja, für den Produktionseinsatz ist eine kommerzielle Lizenz erforderlich. Kaufen Sie eine Lizenz [hier](https://purchase.aspose.com/buy).

**Q: Gibt es eine kostenlose Testversion?**  
A: Ja, Sie können die Bibliothek mit einer kostenlosen Testversion von [hier](https://releases.aspose.com/) erkunden.

**Q: Beeinflusst die Methode `adjustBrightness` die Ebenen‑Sichtbarkeit?**  
A: Die Methode arbeitet am rasterisierten Composite‑Bild, sodass versteckte Ebenen während der Rasterisierung ignoriert werden und das beabsichtigte visuelle Ergebnis erhalten bleibt.

**Q: Kann ich mehrere Anpassungen (z. B. Kontrast, Sättigung) hintereinander ausführen?**  
A: Absolut. Nach dem Anpassen der Helligkeit können Sie `adjustContrast`, `adjustSaturation` oder andere Farbkorrektur‑Methoden auf derselben `RasterImage`‑Instanz aufrufen.

---

**Zuletzt aktualisiert:** 2026-09-28  
**Getestet mit:** Aspose.PSD for Java 24.12 (aktuell zum Zeitpunkt des Schreibens)  
**Autor:** Aspose

## Verwandte Tutorials

- [Java-Bibliothek für Bildverarbeitung: Ebene invertieren mit Aspose.PSD](/psd/java/advanced-image-manipulation/invert-adjustment-layer/)
- [Bild in Graustufen konvertieren mit Aspose.PSD für Java](/psd/java/advanced-techniques/grayscale-image/)
- [Wie man ein Bild um einen bestimmten Winkel mit Aspose.PSD für Java dreht](/psd/java/advanced-image-manipulation/rotate-image-specific-angle/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}