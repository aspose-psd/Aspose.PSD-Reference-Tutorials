---
date: 2026-05-19
description: Erfahren Sie, wie Sie PSD in JPEG konvertieren und das Bild um 270 Grad
  mit Aspose.PSD für Java drehen. Dieser Leitfaden zeigt, wie man PSD-Dateien dreht,
  Bilder spiegelt und PSD in JPEG konvertiert.
keywords:
- convert psd to jpeg
- how to rotate psd
- flip image java
- rotate psd layer
- rotate image without photoshop
linktitle: Bild um 270 Grad drehen
schemas:
- author: Aspose
  dateModified: '2026-05-19'
  description: Learn how to convert PSD to JPEG and rotate image 270 degrees using
    Aspose.PSD for Java. This guide shows how to rotate PSD files, flip images, and
    convert PSD to JPEG.
  headline: Convert PSD to JPEG & Rotate 270° with Aspose.PSD for Java
  type: TechArticle
- description: Learn how to convert PSD to JPEG and rotate image 270 degrees using
    Aspose.PSD for Java. This guide shows how to rotate PSD files, flip images, and
    convert PSD to JPEG.
  name: Convert PSD to JPEG & Rotate 270° with Aspose.PSD for Java
  steps:
  - name: Load the PSD File
    text: '`Image` is Aspose.PSD''s core class that represents a single PSD document
      in memory. Instantiating it reads only the header information, keeping memory
      usage low.'
  - name: Rotate the Image 270 Degrees
    text: '`rotateFlip` performs the specified rotation and optional flip on the image.
      `RotateFlipType.Rotate270FlipNone` rotates the canvas 270 degrees clockwise
      while leaving the image orientation unchanged. > **Pro tip:** If you also need
      to flip the image horizontally or vertically, choose a different `Ro'
  - name: Convert PSD to JPEG and Save
    text: '`JpegOptions` defines JPEG‑specific parameters such as compression quality.
      The `save` method writes the transformed image to disk in the desired format.
      The file `RotatedImage_out.jpg` now contains the original PSD content rotated
      270 degrees and saved as a JPEG.'
  type: HowTo
- questions:
  - answer: Yes, Aspose.PSD supports PSD, JPEG, PNG, BMP, GIF, TIFF, and many other
      raster formats.
    question: Is Aspose.PSD compatible with different image formats?
  - answer: Absolutely! While `RotateFlipType` provides common angles, you can chain
      multiple calls or use transformation matrices for arbitrary angles.
    question: Can I apply custom rotations, not just predefined flips?
  - answer: Replace `JpegOptions` with `PngOptions` (or the appropriate options class)
      in the `save` method.
    question: How do I convert the rotated PSD to another format, such as PNG?
  - answer: For community help, visit the [Aspose.PSD Forum](https://forum.aspose.com/c/psd/34).
    question: Where can I find additional support or assistance?
  - answer: Yes, you can explore Aspose.PSD with a [free trial](https://releases.aspose.com/).
    question: Is there a free trial available?
  type: FAQPage
second_title: Aspose.PSD Java API
title: PSD in JPEG konvertieren & 270° drehen mit Aspose.PSD für Java
url: /de/java/advanced-image-manipulation/rotate-image/
weight: 19
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# PSD in JPEG konvertieren & Bild um 270 Grad drehen mit Aspose.PSD für Java

## Einleitung

In diesem **Java-Bildverarbeitungs‑Tutorial** lernen Sie, wie Sie **PSD in JPEG** konvertieren und dabei das Bild 270 Grad mit Aspose.PSD für Java drehen. Egal, ob Sie eine Batch‑Verarbeitungspipeline, einen webbasierten Editor oder ein Desktop‑Dienstprogramm erstellen, ermöglicht die Bibliothek das Manipulieren von PSD‑Ebenen ohne Photoshop. Wir behandeln außerdem optionales Spiegeln und zeigen den vollständigen End‑zu‑End‑Ablauf vom Laden einer PSD‑Datei bis zum Speichern als JPEG.

## Schnelle Antworten
- **Welche Bibliothek führt die Drehung aus?** Aspose.PSD for Java  
- **Welchen Drehwinkel verwendet das Beispiel?** 270 Grad  
- **Kann ich das Bild auch spiegeln?** Ja – verwenden Sie `RotateFlipType`‑Optionen wie `Rotate90FlipX`  
- **Wie speichere ich das Ergebnis?** Im Beispiel speichern wir als JPEG mit `JpegOptions`  
- **Benötige ich eine Lizenz für die Produktion?** Eine gültige Aspose.PSD‑Lizenz ist für die kommerzielle Nutzung erforderlich  

## Was bedeutet „Bild um 270 Grad drehen“?

Ein Bild um 270 Grad zu drehen bedeutet, das Bild um drei Viertel einer vollen Umdrehung im Uhrzeigersinn (oder 90 Grad gegen den Uhrzeigersinn) zu drehen. Diese Ausrichtung stellt häufig das ursprüngliche Hochformat nach vorherigen Transformationen wieder her und wird häufig verwendet, wenn Bilder im Querformat aufgenommen wurden, aber im Hochformat angezeigt werden sollen. Das Ergebnis ist ein korrekt ausgerichtetes Bild ohne Qualitätsverlust.

## Warum Aspose.PSD für diese Aufgabe verwenden?

Aspose.PSD unterstützt **mehr als 50 Eingabe‑ und Ausgabeformate** – darunter PSD, JPEG, PNG, BMP, GIF und TIFF – und kann Dateien bis zu **2 GB** verarbeiten, ohne das gesamte Dokument in den Speicher zu laden. Die API funktioniert auf jeder Java‑Runtime (JDK 8+), erfordert keine native Photoshop‑Installation und bietet einen einzigen `rotateFlip`‑Aufruf, der sowohl Drehung als auch Spiegeln in einem Schritt ausführt.

## Voraussetzungen

Bevor Sie beginnen, stellen Sie sicher, dass Sie:

- **Aspose.PSD for Java**‑Bibliothek installiert haben. Sie können sie herunterladen und die vollständige API‑Referenz [hier](https://reference.aspose.com/psd/java/) einsehen.  
- Eine Java‑Entwicklungsumgebung (JDK 8 oder höher).  
- Eine Beispiel‑PSD‑Datei, die Sie drehen möchten. Aktualisieren Sie die Variable `sourceFile` im Code mit dem korrekten Pfad zu Ihrer Datei.

## Pakete importieren

Die Klassen `Image`, `RotateFlipType` und `JpegOptions` werden zum Laden, Transformieren und Speichern der Datei benötigt.  
`Image` ist die Kernklasse, die ein PSD‑Dokument im Speicher repräsentiert.  
`RotateFlipType` enumeriert die unterstützten Dreh‑ und Spiegel‑Operationen.  
`JpegOptions` konfiguriert JPEG‑Ausgabe‑Einstellungen wie die Qualität.

```java
import com.aspose.psd.Image;
import com.aspose.psd.RotateFlipType;

import com.aspose.psd.imageoptions.JpegOptions;
```

## Wie konvertiere ich PSD nach dem Drehen in JPEG?

Laden Sie das Quell‑PSD, wenden Sie eine 270‑Grad‑Drehung an und speichern Sie es sofort als JPEG. Dieser dreistufige Ablauf dauert bei typischen 10‑MP‑Bildern auf einer modernen CPU weniger als eine Sekunde, was ihn ideal für Hochdurchsatz‑Batch‑Jobs macht. Durch die Verarbeitung nur der notwendigen Bilddaten bleibt der Speicherverbrauch gering, und das resultierende JPEG behält die visuelle Treue bei, während die Dateigröße reduziert wird.

### Schritt 1: PSD‑Datei laden

`Image` ist die Kernklasse von Aspose.PSD, die ein einzelnes PSD‑Dokument im Speicher repräsentiert. Beim Instanziieren werden nur die Header‑Informationen gelesen, wodurch der Speicherverbrauch gering bleibt.

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";
Image image = Image.load(sourceFile);
```

### Schritt 2: Bild um 270 Grad drehen

`rotateFlip` führt die angegebene Drehung und optionales Spiegeln des Bildes aus. `RotateFlipType.Rotate270FlipNone` dreht die Leinwand um 270 Grad im Uhrzeigersinn, während die Bildorientierung unverändert bleibt.

```java
image.rotateFlip(RotateFlipType.Rotate270FlipNone);
```

> **Pro Tipp:** Wenn Sie das Bild zusätzlich horizontal oder vertikal spiegeln müssen, wählen Sie einen anderen `RotateFlipType` wie `Rotate90FlipX` oder `Rotate180FlipY`.

### Schritt 3: PSD in JPEG konvertieren und speichern

`JpegOptions` definiert JPEG‑spezifische Parameter wie die Kompressionsqualität. Die Methode `save` schreibt das transformierte Bild im gewünschten Format auf die Festplatte.

```java
String destName = dataDir + "RotatedImage_out.jpg";
image.save(destName, new JpegOptions());
```

Die Datei `RotatedImage_out.jpg` enthält nun den ursprünglichen PSD‑Inhalt, um 270 Grad gedreht und als JPEG gespeichert.

## Häufige Probleme und Lösungen

| Problem | Lösung |
|-------|----------|
| **Bild erscheint verkehrt herum** | Stellen Sie sicher, dass Sie `Rotate270FlipNone` verwendet haben. Für eine 90‑Grad‑Drehung im Uhrzeigersinn verwenden Sie `Rotate90FlipNone`. |
| **Ausgabedatei ist beschädigt** | Stellen Sie sicher, dass das Zielverzeichnis existiert und Sie Schreibrechte haben. |
| **Lizenzausnahme** | Installieren Sie eine temporäre oder permanente Aspose.PSD‑Lizenz, bevor Sie das Bild in der Produktion laden. |

## Häufig gestellte Fragen

**Q: Ist Aspose.PSD mit verschiedenen Bildformaten kompatibel?**  
A: Ja, Aspose.PSD unterstützt PSD, JPEG, PNG, BMP, GIF, TIFF und viele andere Rasterformate.

**Q: Kann ich benutzerdefinierte Drehungen anwenden, nicht nur vordefinierte Spiegelungen?**  
A: Absolut! Während `RotateFlipType` gängige Winkel bereitstellt, können Sie mehrere Aufrufe verketten oder Transformationsmatrizen für beliebige Winkel verwenden.

**Q: Wie konvertiere ich das gedrehte PSD in ein anderes Format, z. B. PNG?**  
A: Ersetzen Sie `JpegOptions` durch `PngOptions` (oder die entsprechende Options‑Klasse) in der `save`‑Methode.

**Q: Wo finde ich zusätzliche Unterstützung oder Hilfe?**  
A: Für Community‑Hilfe besuchen Sie das [Aspose.PSD Forum](https://forum.aspose.com/c/psd/34).

**Q: Gibt es eine kostenlose Testversion?**  
A: Ja, Sie können Aspose.PSD mit einer [kostenlosen Testversion](https://releases.aspose.com/) ausprobieren.

**Q: Wie erhalte ich eine temporäre Lizenz?**  
A: Wenn Sie eine temporäre Lizenz benötigen, können Sie eine [hier](https://purchase.aspose.com/temporary-license/) erhalten.

---

**Zuletzt aktualisiert:** 2026-05-19  
**Getestet mit:** Aspose.PSD for Java 24.12  
**Autor:** Aspose  

{{< blocks/products/products-backtop-button >}}

## Verwandte Tutorials

- [PSD in Raster‑Bildformate konvertieren mit Aspose.PSD für Java](/psd/java/advanced-techniques/convert-psd-to-raster-formats/)
- [PSD in PNG konvertieren und Ebenen in PSD‑Dateien mit Java drehen](/psd/java/advanced-psd-layer-features-effects/rotate-layers-psd-files/)
- [Wie man ein Bild in Java mit Aspose.PSD dreht](/psd/java/advanced-image-manipulation/)

{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}