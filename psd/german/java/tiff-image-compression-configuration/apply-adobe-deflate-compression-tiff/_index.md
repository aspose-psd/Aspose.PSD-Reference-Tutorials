---
title: Adobe Deflate-Komprimierung auf TIFF anwenden – Java
linktitle: Adobe Deflate-Komprimierung auf TIFF anwenden – Java
second_title: Aspose.PSD Java API
description: Erfahren Sie, wie Sie mit Aspose.PSD für Java die Adobe Deflate-Komprimierung auf TIFF-Bilder anwenden. Schritt-für-Schritt-Anleitung für eine effiziente Bildverarbeitung.
type: docs
weight: 12
url: /de/java/tiff-image-compression-configuration/apply-adobe-deflate-compression-tiff/
---
## Einführung

Haben Sie sich schon einmal gefragt, wie Sie Ihre TIFF-Bilder effizient komprimieren können, ohne Kompromisse bei der Qualität einzugehen? Wenn Sie mit großen Bilddateien arbeiten, kennen Sie wahrscheinlich die Probleme mit langen Ladezeiten und Speicherproblemen. Hier kommt die Adobe Deflate-Komprimierung ins Spiel, und mit Aspose.PSD für Java können Sie sie ganz einfach in Ihre Projekte implementieren. Dieses Tutorial führt Sie Schritt für Schritt durch die Anwendung der Adobe Deflate-Komprimierung auf ein TIFF-Bild. Bereit, loszulegen? Dann legen wir los!

## Voraussetzungen

Bevor wir uns in den eigentlichen Code stürzen, stellen wir sicher, dass Sie alles eingerichtet haben. Folgendes benötigen Sie:

1. Java Development Kit (JDK): Stellen Sie sicher, dass auf Ihrem Computer die neueste Version von JDK installiert ist.
2.  Aspose.PSD für Java: Laden Sie die Bibliothek Aspose.PSD für Java herunter und integrieren Sie sie in Ihr Projekt. Sie erhalten sie von[Hier](https://releases.aspose.com/psd/java/).
3. Entwicklungsumgebung: Eine IDE wie IntelliJ IDEA, Eclipse oder NetBeans.
4.  Temporäre Lizenz (optional): Wenn Sie noch nicht zum Kauf bereit sind, können Sie eine[vorläufige Lizenz](https://purchase.aspose.com/temporary-license/) um die Funktionen auszuprobieren.

## Pakete importieren

Beginnen wir mit dem Importieren der erforderlichen Pakete in Ihr Java-Projekt. Diese Importe sind wichtig, da Sie damit mit der Aspose.PSD-Bibliothek und Java-Dienstprogrammen arbeiten können.

```java
import com.aspose.psd.Color;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.tiff.TiffRational;
import com.aspose.psd.fileformats.tiff.enums.TiffCompressions;
import com.aspose.psd.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.psd.fileformats.tiff.enums.TiffPhotometrics;
import com.aspose.psd.fileformats.tiff.enums.TiffPlanarConfigs;
import com.aspose.psd.fileformats.tiff.enums.TiffResolutionUnits;
import com.aspose.psd.imageoptions.TiffOptions;
```

Nachdem wir nun die Grundlagen behandelt haben, unterteilen wir den Prozess in leicht verständliche Schritte.

## Schritt 1: Einrichten der TIFF-Optionen

 Als erstes müssen Sie eine Instanz von`TiffOptions` und konfigurieren Sie es entsprechend Ihren Anforderungen. Diese Optionen definieren, wie die TIFF-Datei verarbeitet wird, einschließlich Auflösung, Farbschema und Komprimierung.

```java
TiffOptions options = new TiffOptions(TiffExpectedFormat.Default);
```

Hier erstellen wir ein`TiffOptions` Objekt mit dem Standardformat. Aber das ist erst der Anfang! 

## Schritt 2: Bildeigenschaften konfigurieren

 Als nächstes müssen Sie verschiedene Eigenschaften des TIFF-Bildes festlegen, wie`BitsPerSample`, `Photometric`, `Resolution` , Und`PlanarConfiguration`. Diese Einstellungen legen fest, wie die Bilddaten gespeichert und angezeigt werden.

```java
int[] ushort = { 8, 8, 8 };
options.setBitsPerSample(ushort);
options.setPhotometric(TiffPhotometrics.Rgb);
options.setXresolution(new TiffRational(72));
options.setYresolution(new TiffRational(72));
options.setResolutionUnit(TiffResolutionUnits.Inch);
options.setPlanarConfiguration(TiffPlanarConfigs.Contiguous);
```

Die einzelnen Eigenschaften haben folgende Funktion:
- BitsPerSample: Legt die Anzahl der Bits pro Sample für jeden Farbkanal fest.
- Photometrisch: Definiert das Farbmodell (in diesem Fall RGB).
- Auflösung: Gibt die horizontale und vertikale Auflösung des Bildes an.
- PlanarConfiguration: Bestimmt, wie Pixeldaten gespeichert werden.

## Schritt 3: Adobe Deflate-Komprimierung anwenden

Jetzt kommt der Zauber! Sie wenden die Adobe Deflate-Komprimierung auf Ihr TIFF-Bild an, wodurch die Dateigröße ohne Qualitätsverlust reduziert wird.

```java
options.setCompression(TiffCompressions.AdobeDeflate);
```

Adobe Deflate ist eine verlustfreie Komprimierungsmethode, die sich perfekt für Bilder eignet, bei denen eine hohe Qualität beibehalten und gleichzeitig die Dateigröße reduziert werden muss.

## Schritt 4: Erstellen und Bearbeiten des TIFF-Bildes

Nachdem die Optionen festgelegt wurden, ist es an der Zeit, ein neues TIFF-Bild zu erstellen und zu bearbeiten. In diesem Schritt erstellen wir ein einfaches 100 x 100-Bild und füllen es mit roten Pixeln.

```java
PsdImage tiffImage = new PsdImage(100, 100);

for (int j = 0; j < tiffImage.getHeight(); j++) {
    for (int i = 0; i < tiffImage.getWidth(); i++) {
        tiffImage.setPixel(i, j, Color.getRed());
    }
}
```

Hier durchlaufen wir jeden Pixel des Bildes und setzen seine Farbe auf Rot. Natürlich können Sie diesen Teil anpassen, um komplexere Bilder zu erstellen.

## Schritt 5: Speichern Sie das komprimierte TIFF-Bild

Nachdem Sie das Image konfiguriert und erstellt haben, müssen Sie es im letzten Schritt mit der angewendeten Komprimierung speichern. Achten Sie dabei auf die Angabe des richtigen Verzeichnispfads.

```java
String dataDir = "Your Document Directory";
tiffImage.save(dataDir + "TIFFwithAdobeDeflateCompression_output.tif");
```

Das ist es! Sie haben die Adobe Deflate-Komprimierung erfolgreich auf ein TIFF-Bild mit Aspose.PSD für Java angewendet.

## Abschluss

Und da haben Sie es! Das Anwenden der Adobe Deflate-Komprimierung auf TIFF-Bilder ist mit Aspose.PSD für Java ein unkomplizierter Vorgang. Egal, ob Sie mit großen Bildern für Ihre Website, digitale Medien oder ein anderes Projekt arbeiten, diese Methode stellt sicher, dass Ihre Dateien eine hohe Qualität aufweisen und gleichzeitig eine handlichere Größe haben. Die Stärke von Aspose.PSD für Java liegt in seiner Einfachheit und Effizienz, was es zu einem unverzichtbaren Tool für Entwickler macht, die mit komplexen Bildformaten arbeiten.

## Häufig gestellte Fragen

### Was ist Adobe Deflate-Komprimierung?
Adobe Deflate ist eine verlustfreie Komprimierungsmethode, mit der die Größe von TIFF-Bildern ohne Qualitätsverlust reduziert wird.

### Kann ich mit Aspose.PSD für Java andere Komprimierungsmethoden verwenden?
Ja, Aspose.PSD unterstützt verschiedene Komprimierungsmethoden wie LZW, CCITT und JPEG.

### Ist die Aspose.PSD-Bibliothek kostenlos?
 Aspose.PSD bietet eine kostenlose Testversion an, für die volle Funktionalität ist jedoch eine Lizenz erforderlich. Sie erhalten eine[vorläufige Lizenz](https://purchase.aspose.com/temporary-license/) um es auszuprobieren.

### Welchen Einfluss hat die Auflösungseinstellung auf das TIFF-Bild?
Die Auflösung bestimmt die Klarheit des Bildes beim Drucken oder Anzeigen. Höhere Auflösungen bieten eine bessere Qualität, führen jedoch zu größeren Dateien.

### Kann ich mit Aspose.PSD für Java andere Bildformate bearbeiten?
Absolut! Aspose.PSD unterstützt verschiedene Formate wie PSD, PNG, JPEG und mehr.