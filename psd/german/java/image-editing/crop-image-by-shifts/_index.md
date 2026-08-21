---
date: 2026-07-03
description: Erfahren Sie, wie Sie Bilder in Java mit Aspose.PSD für Java zuschneiden.
  Dieses Schritt‑für‑Schritt‑Tutorial zum Bildzuschnitt behandelt das Laden von PSD‑Dateien,
  das Festlegen von Verschiebungswerten und das Speichern des Ergebnisses.
keywords:
- crop image java
- how to crop image
- load psd file
- java image processing
- crop image left right
linktitle: Bild nach Verschiebungen zuschneiden
schemas:
- author: Aspose
  dateModified: '2026-07-03'
  description: Learn how to crop image java using Aspose.PSD for Java. This step‑by‑step
    image cropping tutorial covers loading PSD files, setting shift values, and saving
    the result.
  headline: Crop Image Java by Shifts with Aspose.PSD
  type: TechArticle
- description: Learn how to crop image java using Aspose.PSD for Java. This step‑by‑step
    image cropping tutorial covers loading PSD files, setting shift values, and saving
    the result.
  name: Crop Image Java by Shifts with Aspose.PSD
  steps:
  - name: Load the Image
    text: '`Image` is the base class for all image types in Aspose.PSD. `RasterImage`
      represents a raster image and provides cropping capabilities.'
  - name: Cache Image Data
    text: '`cacheData()` loads the image data into memory for faster processing.'
  - name: Define Shift Values
    text: Specify the shift values for all four sides of the image (left, top, right,
      bottom) in pixels.
  - name: Apply Cropping
    text: '`crop(left, right, top, bottom)` trims the image by the specified pixel
      shifts on each side.'
  - name: Save the Results
    text: '`JpegOptions` defines JPEG encoding settings such as quality and color
      profile. Congratulations! You''ve successfully cropped an image using Aspose.PSD
      for Java.'
  type: HowTo
- questions:
  - answer: Yes, Aspose.PSD supports over 30 raster formats, including PSD, JPEG,
      PNG, BMP, TIFF, and GIF, ensuring broad compatibility.
    question: Is Aspose.PSD compatible with all image formats?
  - answer: Absolutely. After each `crop` call you receive a new image object, which
      you can crop again as needed.
    question: Can I apply multiple cropping operations to the same image?
  - answer: Yes, you can find support and engage with the community at [Aspose.PSD
      Forum](https://forum.aspose.com/c/psd/34).
    question: Is there a community forum for Aspose.PSD support?
  - answer: Visit [here](https://purchase.aspose.com/temporary-license/) to obtain
      a temporary license.
    question: How can I obtain a temporary license for Aspose.PSD?
  - answer: Explore the documentation and examples at [Aspose.PSD Java Documentation](https://reference.aspose.com/psd/java/).
    question: Are there sample projects showcasing Aspose.PSD functionalities?
  type: FAQPage
second_title: Aspose.PSD Java API
title: Bild in Java nach Verschiebungen zuschneiden mit Aspose.PSD
url: /de/java/image-editing/crop-image-by-shifts/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Bild zuschneiden in Java nach Verschiebungen mit Aspose.PSD

## Einführung

In der Java-Bildverarbeitung ist **crop image java** ein häufiges Bedürfnis, um Grafiken, Thumbnails oder UI‑Assets vorzubereiten. Aspose.PSD für Java macht diese Aufgabe einfach, indem es eine unkomplizierte `crop`‑Methode bereitstellt, die mit jedem unterstützten Rasterformat funktioniert. In diesem Tutorial lernen Sie, wie Sie eine PSD‑Datei laden, Links‑Rechts‑Oben‑Unten‑Verschiebungswerte definieren, das Zuschneiden anwenden und das Ergebnis speichern – ganz ohne eigenen Pixel‑Manipulationscode.

## Schnelle Antworten
- **Welche Bibliothek übernimmt das Zuschneiden?** Aspose.PSD für Java bietet eine eingebaute `crop`‑Methode.  
- **Benötige ich eine Lizenz?** Eine temporäre Lizenz reicht für die Evaluierung; für den Produktionseinsatz ist eine Voll‑Lizenz erforderlich.  
- **Unterstützte Formate?** Über 30 Rasterformate, darunter PSD, JPEG, PNG, BMP und TIFF.  
- **Maximale Dateigröße?** Verarbeitet Dateien bis zu 2 GB, ohne das gesamte Bild in den Speicher zu laden.  
- **Wie viele Code‑Zeilen?** Nur fünf logische Schritte – Laden, Zwischenspeichern, Verschiebungen festlegen, Zuschneiden und Speichern.

## Was ist crop image java?
`crop image java` bezeichnet den Vorgang, ein Bitmap in einer Java‑Anwendung zu beschneiden. Mit Aspose.PSD wird die Operation durch die `crop`‑Methode ausgeführt, die Verschiebungswerte für jede Bildseite akzeptiert und eine neue Bildinstanz zurückgibt.

## Warum Aspose.PSD für das Zuschneiden von Bildern verwenden?
Aspose.PSD unterstützt **30+** Bildformate und kann mehrseitige PSD‑Dateien mit mehreren hundert Seiten verarbeiten, wobei weniger als 150 MB RAM verbraucht werden, dank seiner Lazy‑Loading‑Architektur. Die Bibliothek garantiert zudem pixelgenaue Ergebnisse, bewahrt Ebenen, Masken und Farbprofile – etwas, das viele generische Bildbibliotheken nicht sicherstellen können.

## Voraussetzungen

### Java Development Kit (JDK)

Stellen Sie sicher, dass die neueste Version des JDK auf Ihrem System installiert ist. Sie können es von [hier](https://www.oracle.com/java/technologies/javase-downloads.html) herunterladen.

### Aspose.PSD für Java Bibliothek

Um zu beginnen, benötigen Sie die Aspose.PSD für Java Bibliothek. Besuchen Sie die [Download‑Seite](https://releases.aspose.com/psd/java/) und holen Sie sich die aktuelle Version.

### Integrierte Entwicklungsumgebung (IDE)

Wählen Sie Ihre bevorzugte Java‑IDE, z. B. Eclipse oder IntelliJ, für ein reibungsloses Entwicklungserlebnis.

## Wie man crop image java verwendet?

Laden Sie Ihre Quelldatei, definieren Sie die Pixel‑Verschiebungen für jede Seite und rufen Sie die `crop`‑Methode auf – dieser gesamte Workflow lässt sich in fünf knappen Code‑Zeilen schreiben. Der `crop`‑Vorgang erzeugt ein neues Bild, das nur den von Ihnen angegebenen Bereich enthält, während die Originaldatei unverändert bleibt.

### Schritt 1: Bild laden

`Image` ist die Basisklasse für alle Bildtypen in Aspose.PSD.  
`RasterImage` repräsentiert ein Rasterbild und bietet Zuschneide‑Funktionen.  
```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.imageoptions.JpegOptions;
```

### Schritt 2: Bilddaten zwischenspeichern

`cacheData()` lädt die Bilddaten in den Speicher für schnellere Verarbeitung.  
```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

// Load an existing image into an instance of RasterImage class
RasterImage rasterImage = (RasterImage)Image.load(sourceFile);
```

### Schritt 3: Verschiebungswerte festlegen

Geben Sie die Verschiebungswerte für alle vier Bildseiten (links, oben, rechts, unten) in Pixeln an.  
```java
if (!rasterImage.isCached()) {
  rasterImage.cacheData();
}
```

### Schritt 4: Zuschneiden anwenden

`crop(left, right, top, bottom)` schneidet das Bild um die angegebenen Pixel‑Verschiebungen an jeder Seite zu.  
```java
int leftShift = 10;
int rightShift = 10;
int topShift = 10;
int bottomShift = 10;
```

### Schritt 5: Ergebnisse speichern

`JpegOptions` definiert JPEG‑Kodierungseinstellungen wie Qualität und Farbprofil.  
```java
rasterImage.crop(leftShift, rightShift, topShift, bottomShift);
```

Herzlichen Glückwunsch! Sie haben ein Bild erfolgreich mit Aspose.PSD für Java zugeschnitten.

## Häufige Probleme und Lösungen

- **Bild erscheint unverändert:** Stellen Sie sicher, dass die Verschiebungswerte positiv sind und die Originalabmessungen nicht überschreiten.  
- **OutOfMemoryError bei großen Dateien:** Aktivieren Sie das Caching wie in Schritt 2 gezeigt; dadurch verwendet Aspose.PSD eine temporäre Datei anstelle des gesamten Bildes im RAM.  
- **Farbverschiebung nach dem Zuschneiden:** Bewahren Sie das Farbprofil, indem Sie `image.save(..., new JpegOptions { ColorProfile = image.ColorProfile })` aufrufen, falls Sie eine exakte Farbtreue benötigen.

## Häufig gestellte Fragen

**Q: Ist Aspose.PSD mit allen Bildformaten kompatibel?**  
A: Ja, Aspose.PSD unterstützt über 30 Rasterformate, darunter PSD, JPEG, PNG, BMP, TIFF und GIF, und bietet damit breite Kompatibilität.

**Q: Kann ich mehrere Zuschneide‑Operationen auf dasselbe Bild anwenden?**  
A: Absolut. Nach jedem `crop`‑Aufruf erhalten Sie ein neues Bildobjekt, das Sie bei Bedarf erneut zuschneiden können.

**Q: Gibt es ein Community‑Forum für den Aspose.PSD‑Support?**  
A: Ja, Sie finden Unterstützung und können sich mit der Community austauschen unter [Aspose.PSD Forum](https://forum.aspose.com/c/psd/34).

**Q: Wie erhalte ich eine temporäre Lizenz für Aspose.PSD?**  
A: Besuchen Sie [hier](https://purchase.aspose.com/temporary-license/), um eine temporäre Lizenz zu erhalten.

**Q: Gibt es Beispielprojekte, die Aspose.PSD‑Funktionalitäten demonstrieren?**  
A: Erkunden Sie die Dokumentation und Beispiele unter [Aspose.PSD Java Documentation](https://reference.aspose.com/psd/java/).

---

**Zuletzt aktualisiert:** 2026-07-03  
**Getestet mit:** Aspose.PSD 24.11 für Java  
**Autor:** Aspose  

{{< blocks/products/products-backtop-button >}}

```java
String destName = dataDir + "CroppingByShifts_out.jpg";
rasterImage.save(destName, new JpegOptions());
```

## Verwandte Tutorials

- [Crop Image by Rectangle in Aspose.PSD for Java](/psd/java/image-editing/crop-image-by-rectangle/)
- [Crop Image Java - Expand and Crop Images with Aspose.PSD for Java](/psd/java/image-editing/expand-and-crop-images/)
- [Resize Image Java - Using Resize Type Enumeration in Aspose.PSD for Java](/psd/java/advanced-image-manipulation/resizing-with-resize-type-enumeration/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}