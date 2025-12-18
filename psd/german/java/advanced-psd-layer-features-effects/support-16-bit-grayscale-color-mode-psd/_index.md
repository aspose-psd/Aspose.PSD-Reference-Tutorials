---
date: 2025-12-17
description: Erfahren Sie, wie Sie PSD in PNG konvertieren und dabei den Farbmodus
  von PSD auf 16‑Bit‑Graustufen einstellen, mithilfe von Aspose.PSD für Java. Schritt‑für‑Schritt‑Anleitung
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

# PSD in PNG konvertieren mit 16‑Bit Graustufen‑Farbmodus in Java

## Einführung
Wenn Sie in die Welt des Grafikdesigns und der Bildbearbeitung eintauchen, ist das Verständnis, **PSD in PNG zu konvertieren**, wie eine Geheimwaffe. Insbesondere liefert ein 16‑Bit‑Graustufen‑Modus Ihren Bildern eine beeindruckende Tiefe und Detailtreue, die sie wirklich hervorstechen lässt. In diesem Tutorial zeigen wir Ihnen, wie Sie **den PSD‑Farbmodus** auf 16‑Bit‑Graustufen setzen und anschließend **PSD als PNG exportieren** mit Aspose.PSD für Java. Bereit, Ihren Bild‑Workflow zu verbessern? Dann legen wir los.

## Schnellantworten
- **Was beinhaltet „PSD in PNG konvertieren“?** Laden einer PSD, optionales Ändern des Farbmodus und Speichern als PNG‑Datei.  
- **Welche Aspose‑Klasse übernimmt die Konvertierung?** `PsdImage` zum Laden und `PngOptions` zum Speichern.  
- **Benötige ich eine spezielle Lizenz?** Eine Testversion reicht für Tests; für die Produktion ist eine kostenpflichtige Lizenz erforderlich.  
- **Kann ich die 16‑Bit‑Tiefe im PNG beibehalten?** Ja, indem Sie `PngColorType.GrayscaleWithAlpha` verwenden.  
- **Welche IDEs werden unterstützt?** Jede Java‑IDE – IntelliJ IDEA, Eclipse, VS Code usw.

## Voraussetzungen
Bevor wir beginnen, stellen wir sicher, dass Sie alles eingerichtet haben, um das Beste aus diesem Tutorial herauszuholen. Sie benötigen:

1. **Java Development Kit (JDK)** – Stellen Sie sicher, dass die neueste Version installiert ist. Sie können es von der [Oracle‑Seite](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html) herunterladen.  
2. **Aspose.PSD für Java Bibliothek** – Das ist die Engine, die uns die Manipulation von PSD‑Dateien ermöglicht. Laden Sie sie von der [Aspose‑Download‑Seite](https://releases.aspose.com/psd/java/) herunter.  
3. **Eine IDE** – IntelliJ IDEA, Eclipse oder Visual Studio Code funktionieren einwandfrei.  
4. **Grundkenntnisse in Java** – Vertrautheit mit der Java‑Syntax erleichtert die Schritte.  
5. **Eine Beispiel‑PSD‑Datei** – Erstellen Sie eine in Adobe Photoshop oder laden Sie ein kostenloses Beispiel online herunter.

Bereit? Großartig! Importieren wir die notwendigen Pakete und beginnen mit dem Coden.

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

Diese Imports geben Ihnen Zugriff auf die Funktionalitäten, die Sie zur Manipulation von PSD‑Dateien, zum Setzen des Farbmodus und zum Exportieren des Ergebnisses als PNG benötigen.

## Schritt 1: Verzeichnisse definieren
Zuerst richten Sie die Quell‑ und Zielordner ein. Damit weiß das Programm, wo es die ursprüngliche PSD lesen und wo es die konvertierten Dateien schreiben soll.

```java
String sourceDir = "Your Source Directory"; // Change to your source directory
String outputDir = "Your Document Directory"; // Change to your output directory
```

Ersetzen Sie die Platzhalter‑Strings durch die tatsächlichen Pfade auf Ihrem Rechner.

## Schritt 2: Methode zur Bildverarbeitung erstellen
Wir kapseln die Konvertierungslogik in einer wiederverwendbaren Methode. Sie erhält alle Parameter, die Sie anpassen möchten, wie Farbmodus, Bit‑Tiefe und Kompression.

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

Diese Methode ermöglicht es Ihnen, **den PSD‑Farbmodus** zu setzen und anschließend **PSD als PNG zu exportieren** in einem einzigen Ablauf.

## Schritt 3: Dateipfade festlegen und PSD laden
Innerhalb der Methode bauen Sie die vollständigen Dateipfade zusammen und laden die ursprüngliche 16‑Bit‑Graustufen‑PSD:

```java
String filePath = sourceDir + file + ".psd";
String postfix = Enum.getName(ColorModes.class, colorMode) + channelBitsCount + "_" +
                 channelsCount + "_" + Enum.getName(CompressionMethod.class, compression);
String exportPath = outputDir + file + postfix + ".psd";
String pngExportPath = outputDir + file + postfix + ".png";
// Load a predefined 16-bit grayscale PSD
PsdImage image = (PsdImage)Image.load(filePath);
```

Der `postfix` hilft Ihnen, die für jede exportierte Datei verwendeten Einstellungen nachzuvollziehen.

## Schritt 4: Ebene oder gesamtes Bild verarbeiten
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

## Schritt 5: Modifizierte PSD‑Datei speichern
Nach dem Zeichnen speichern wir die PSD mit exakt dem von Ihnen angegebenen Farbmodus und der Bit‑Tiefe. Das ist der Kern von **PSD‑Farbmodus setzen** vor der Konvertierung.

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

## Schritt 6: PSD in PNG konvertieren
Abschließend laden wir die neu gespeicherte PSD und exportieren sie als PNG. Durch die Verwendung von `PngColorType.GrayscaleWithAlpha` erhalten wir die 16‑Bit‑Tiefe im PNG‑Dateiformat.

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

Damit haben Sie **PSD erfolgreich in PNG konvertiert**, während Sie die hochwertige 16‑Bit‑Graustufen‑Daten beibehalten haben.

## Häufige Probleme und Lösungen
| Problem | Warum es passiert | Lösung |
|---------|-------------------|--------|
| **„Unsupported color type“‑Ausnahme** | Versuch, eine PSD mit einer nicht unterstützten Kanalkonfiguration zu speichern. | Stellen Sie sicher, dass `channelBitsCount` der tatsächlichen Bit‑Tiefe (16) entspricht und `channelsCount` für Graustufen (1) korrekt ist. |
| **Datei nicht gefunden** | Falscher Quellverzeichnis‑Pfad. | Überprüfen Sie den String `sourceDir` und vergewissern Sie sich, dass die PSD‑Datei existiert. |
| **Ausgabe‑PNG erscheint schwarz** | PNG wurde ohne Alpha‑Kanal‑Behandlung gespeichert. | Verwenden Sie `PngColorType.GrayscaleWithAlpha` wie oben gezeigt. |

## Häufig gestellte Fragen

**F: Was ist der 16‑Bit‑Graustufen‑Farbmodus?**  
A: Er bietet 65 536 Graustufen und liefert deutlich mehr tonale Details als der Standard‑8‑Bit‑Modus (256 Graustufen).

**F: Kann ich Aspose.PSD für nicht‑Graustufen‑Bilder verwenden?**  
A: Absolut! Aspose.PSD unterstützt RGB, CMYK, Lab und viele weitere Farbmodi.

**F: Gibt es eine Testversion von Aspose.PSD?**  
A: Ja, Sie können eine kostenlose Testversion von Aspose.PSD ausprobieren. Besuchen Sie einfach die [Aspose‑Download‑Seite](https://releases.aspose.com/).

**F: Wo finde ich weitere Beispiele zur Verwendung von Aspose.PSD?**  
A: Schauen Sie in die [Dokumentation](https://reference.aspose.com/psd/java/) für weiterführende Beispiele und Tutorials.

**F: Wie kaufe ich eine Lizenz für Aspose.PSD?**  
A: Sie können eine Lizenz erwerben, indem Sie die [Aspose‑Kaufseite](https://purchase.aspose.com/buy) besuchen.

---

**Zuletzt aktualisiert:** 2025-12-17  
**Getestet mit:** Aspose.PSD für Java 24.12 (zum Zeitpunkt der Erstellung)  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}