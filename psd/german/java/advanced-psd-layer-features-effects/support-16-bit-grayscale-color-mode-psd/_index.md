---
date: 2026-02-20
description: Erfahren Sie, wie Sie PSD in PNG konvertieren und dabei den Farbmodus
  von PSD auf 16‑Bit Graustufen einstellen, mithilfe von Aspose.PSD für Java. Schritt‑für‑Schritt‑Anleitung
  mit Codebeispielen.
linktitle: Convert PSD to PNG – 16-bit Grayscale – Java
second_title: Aspose.PSD Java API
title: Wie man PSD in PNG mit 16‑Bit Graustufen‑Farbmodus in Java konvertiert
url: /de/java/advanced-psd-layer-features-effects/support-16-bit-grayscale-color-mode-psd/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# PSD in PNG mit 16‑Bit Graustufen‑Farbmodus in Java konvertieren

## Einführung
Wenn Sie in die Welt des Grafikdesigns und der Bildbearbeitung eintauchen, ist das Wissen, **wie man PSD in PNG konvertiert**, wie eine Geheimwaffe. Die Verwendung eines 16‑Bit Graustufenmodus fügt unglaubliche Tiefe und tonale Reichhaltigkeit hinzu, sodass Ihre Bilder hervorstechen. In diesem Tutorial zeigen wir, wie man den **PSD‑Farbmodus** auf 16‑Bit Graustufen **setzt** und anschließend **PSD als PNG exportiert** mit Aspose.PSD für Java. Bereit, Ihren Bild‑Workflow zu verbessern? Dann legen wir los.

## Schnelle Antworten
- **Was beinhaltet „PSD in PNG konvertieren“?** Laden einer PSD, optional Ändern des Farbmodus und Speichern als PNG‑Datei.  
- **Welche Aspose‑Klasse übernimmt die Konvertierung?** `PsdImage` zum Laden und `PngOptions` zum Speichern.  
- **Benötige ich eine spezielle Lizenz?** Eine Testversion funktioniert für Tests; für den Produktionseinsatz ist eine kostenpflichtige Lizenz erforderlich.  
- **Kann ich die 16‑Bit‑Tiefe im PNG beibehalten?** Ja, indem Sie `PngColorType.GrayscaleWithAlpha` verwenden.  
- **Welche IDEs werden unterstützt?** Jede Java‑IDE – IntelliJ IDEA, Eclipse, VS Code usw.

## Warum PSD in PNG mit 16‑Bit Graustufen konvertieren?
* **Tonale Details erhalten:** 16‑Bit Graustufen speichern 65 536 Graustufen, deutlich mehr als die 256 Graustufen eines 8‑Bit‑Bildes.  
* **Breite Kompatibilität:** PNG wird von Browsern, mobilen Apps und Desktop‑Tools breit unterstützt und behält gleichzeitig die hochwertigen Daten bei.  
* **Verlustloser Workflow:** Die Konvertierung mit Aspose.PSD sorgt für keine unerwünschten Kompressionsartefakte, ideal für Archivierung oder weitere Verarbeitung.

## Voraussetzungen
Bevor wir beginnen, stellen wir sicher, dass Sie alles eingerichtet haben, um das Beste aus diesem Tutorial herauszuholen. Folgendes benötigen Sie:

1. **Java Development Kit (JDK)** – Stellen Sie sicher, dass die neueste Version installiert ist. Sie können es von der [Oracle‑Seite](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html) herunterladen.  
2. **Aspose.PSD for Java Library** – Dies ist die Engine, die uns die Manipulation von PSD‑Dateien ermöglicht. Laden Sie sie von der [Aspose‑Download‑Seite](https://releases.aspose.com/psd/java/) herunter.  
3. **Eine IDE** – IntelliJ IDEA, Eclipse oder Visual Studio Code funktionieren einwandfrei.  
4. **Grundkenntnisse in Java** – Vertrautheit mit der Java‑Syntax erleichtert die Schritte.  
5. **Eine Beispiel‑PSD‑Datei** – Erstellen Sie eine in Adobe Photoshop oder laden Sie ein kostenloses Beispiel online herunter.

Bereit? Großartig! Lassen Sie uns die erforderlichen Pakete importieren und mit dem Codieren beginnen.

## Pakete importieren
Um loszulegen, fügen Sie die erforderlichen Aspose.PSD‑Imports zu Ihrer Java‑Datei hinzu:

```java
import com.aspose.psd.*;
import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.fileformats.psd.ColorModes;
import com.aspose.psd.fileformats.psd.CompressionMethod;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.PngOptions;
import com.aspose.psd.imageoptions.PsdOptions;
import com.aspose.psd.system.Enum;
```

Diese Imports geben Ihnen Zugriff auf die Funktionen, die Sie zum Manipulieren von PSD‑Dateien, zum Festlegen des Farbmodus und zum Exportieren des Ergebnisses als PNG benötigen.

## Schritt 1: Definieren Sie Ihre Verzeichnisse
Zuerst richten Sie die Quell‑ und Zielordner ein. Dies teilt dem Programm mit, wo die ursprüngliche PSD gelesen und wohin die konvertierten Dateien geschrieben werden.

```java
String sourceDir = "Your Source Directory"; // Change to your source directory
String outputDir = "Your Document Directory"; // Change to your output directory
```

Ersetzen Sie die Platzhalter‑Strings durch die tatsächlichen Pfade auf Ihrem Rechner.

## Schritt 2: Erstellen Sie eine Methode zur Bildverarbeitung
Wir kapseln die Konvertierungslogik in einer wiederverwendbaren Methode ein. Sie erhält alle Parameter, die Sie anpassen möchten, wie Farbmodus, Bit‑Tiefe und Kompression.

```java
class LocalScopeExtension {
    void saveToPsdThenLoadAndSaveToPng(
        String file,
        short colorMode,
        short channelBitsCount,
        short channelsCount,
        short compression,
        int layerNumber) {
```

Diese Methode ermöglicht es Ihnen, den **PSD‑Farbmodus** zu **setzen** und anschließend **PSD als PNG** in einem einzigen Ablauf zu **exportieren**.

## Schritt 3: Definieren Sie Dateipfade und laden Sie die PSD
Innerhalb der Methode bauen Sie die vollständigen Dateipfade zusammen und laden die ursprüngliche 16‑Bit Graustufen‑PSD:

```java
String filePath = sourceDir + file + ".psd";
String postfix = Enum.getName(ColorModes.class, colorMode) + channelBitsCount + "_" +
                 channelsCount + "_" + Enum.getName(CompressionMethod.class, compression);
String exportPath = outputDir + file + postfix + ".psd";
String pngExportPath = outputDir + file + postfix + ".png";
// Load a predefined 16-bit grayscale PSD
PsdImage image = (PsdImage)Image.load(filePath);
```

Der `postfix` hilft Ihnen, die für jede exportierte Datei verwendeten Einstellungen nachzuverfolgen.

## Schritt 4: Verarbeiten Sie die Ebene oder das gesamte Bild
Jetzt zeichnen wir entweder auf einer bestimmten Ebene oder auf dem gesamten Bild. In diesem Beispiel fügen wir einen dezenten grauen Rand hinzu, um das Ergebnis besser sichtbar zu machen.

```java
try {
    RasterCachedImage raster = layerNumber >= 0 ? image.getLayers()[layerNumber] : image;
    // Draw a gray inner border around the perimeter of the layer
    Graphics graphics = new Graphics(raster);
    int width = raster.getWidth();
    int height = raster.getHeight();
    Rectangle rect = new Rectangle(
        width / 3,
        height / 3,
        width - (2 * (width / 3)) - 1,
        height - (2 * (height / 3)) - 1);
    graphics.drawRectangle(new Pen(Color.getDarkGray(), 1), rect);
```

Das Rechteck wird dynamisch berechnet, sodass es unabhängig von der Bildgröße zentriert bleibt.

## Schritt 5: Speichern Sie die modifizierte PSD‑Datei
Nach dem Zeichnen speichern wir die PSD mit dem exakt angegebenen Farbmodus und der Bit‑Tiefe. Dies ist der Kern des **Setzens des PSD‑Farbmodus** vor der Konvertierung.

```java
    // Save a copy of PSD with specific characteristics
    PsdOptions psdOptions = new PsdOptions();
    psdOptions.setColorMode(colorMode);
    psdOptions.setChannelBitsCount(channelBitsCount);
    psdOptions.setChannelsCount(channelsCount);
    psdOptions.setCompressionMethod(compression);
    image.save(exportPath, psdOptions);
}
```

## Schritt 6: Konvertieren Sie die PSD in PNG
Abschließend laden wir die neu gespeicherte PSD und exportieren sie als PNG. Durch die Verwendung von `PngColorType.GrayscaleWithAlpha` bewahren wir die 16‑Bit‑Tiefe in der PNG‑Datei.

```java
finally {
    image.dispose();
}
// Load the saved PSD
PsdImage image1 = (PsdImage)Image.load(exportPath);
try {
    // Convert the saved PSD to a grayscale PNG image
    PngOptions pngOptions = new PngOptions();
    pngOptions.setColorType(PngColorType.GrayscaleWithAlpha);
    image1.save(pngExportPath, pngOptions); // here should be no exception
}
finally {
    image1.dispose();
}
```

Jetzt haben Sie **PSD erfolgreich in PNG konvertiert**, während Sie die hochwertige 16‑Bit Graustufen‑Daten beibehalten.

## Häufige Probleme und Lösungen
| Problem | Warum es passiert | Lösung |
|---------|-------------------|--------|
| **„Unsupported color type“-Ausnahme** | Versuch, eine PSD mit einer nicht unterstützten Kanalkonfiguration zu speichern. | Stellen Sie sicher, dass `channelBitsCount` der tatsächlichen Bit‑Tiefe (16) entspricht und `channelsCount` für Graustufen (1) korrekt ist. |
| **Datei nicht gefunden** | Falscher Quellverzeichnis‑Pfad. | Überprüfen Sie den `sourceDir`‑String und stellen Sie sicher, dass die PSD‑Datei existiert. |
| **Ausgabe‑PNG erscheint schwarz** | PNG wurde ohne Alpha‑Kanal‑Behandlung gespeichert. | Verwenden Sie `PngColorType.GrayscaleWithAlpha` wie oben gezeigt. |

## Häufig gestellte Fragen

**Q: Was ist der 16‑Bit Graustufen‑Farbmodus?**  
A: Er bietet 65 536 Graustufen und liefert damit deutlich mehr tonale Details als der Standard‑8‑Bit‑Modus (256 Graustufen).

**Q: Kann ich Aspose.PSD für nicht‑Graustufen‑Bilder verwenden?**  
A: Auf jeden Fall! Aspose.PSD unterstützt RGB, CMYK, Lab und viele andere Farbmodi.

**Q: Gibt es eine Testversion von Aspose.PSD?**  
A: Ja, Sie können eine kostenlose Testversion von Aspose.PSD ausprobieren. Besuchen Sie einfach die [Aspose‑Download‑Seite](https://releases.aspose.com/).

**Q: Wo finde ich weitere Beispiele zur Verwendung von Aspose.PSD?**  
A: Schauen Sie in die [Dokumentation](https://reference.aspose.com/psd/java/) für weiterführende Beispiele und Tutorials.

**Q: Wie kaufe ich eine Lizenz für Aspose.PSD?**  
A: Sie können eine Lizenz erwerben, indem Sie die [Aspose‑Kaufseite](https://purchase.aspose.com/buy) besuchen.

---

**Zuletzt aktualisiert:** 2026-02-20  
**Getestet mit:** Aspose.PSD for Java 24.12 (latest at time of writing)  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}