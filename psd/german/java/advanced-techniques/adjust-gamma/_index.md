---
date: 2025-12-21
description: Erfahren Sie, wie Sie die Bildverarbeitung in Java durchführen, indem
  Sie die Bild‑Gamma mit Aspose.PSD anpassen. Schritt‑für‑Schritt‑Anleitung zum Konvertieren
  von PSD in TIFF und Anwenden der Gamma‑Korrektur.
linktitle: Adjust Gamma of an Image
second_title: Aspose.PSD Java API
title: Java-Bildverarbeitung – Gamma anpassen mit Aspose.PSD
url: /de/java/advanced-techniques/adjust-gamma/
weight: 23
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Java-Bildverarbeitung – Gamma anpassen mit Aspose.PSD

## Einleitung

Wenn Sie an **java image processing** arbeiten, ist das Anpassen des Gammawertes eines Bildes eine grundlegende Technik, um Helligkeit und Kontrast zu verbessern, ohne Details zu verlieren. In diesem Tutorial zeigen wir, wie Sie **Aspose.PSD for Java** verwenden, um eine Gammakorrektur auf eine PSD‑Datei anzuwenden und das Ergebnis anschließend als TIFF‑Bild zu exportieren. Sie sehen, warum dieser Ansatz schnell, zuverlässig und ideal für serverseitige Bild‑Pipelines ist.

## Schnelle Antworten
- **Was bewirkt die Gammakorrektur?** Sie ordnet Luminanzwerte neu zu, um dunkle Bereiche heller oder helle Bereiche dunkler zu machen, während die Gesamtdetails erhalten bleiben.  
- **Welche Bibliothek übernimmt die Verarbeitung?** Aspose.PSD for Java stellt eine dedizierte `adjustGamma`‑Methode für Rasterbilder bereit.  
- **Kann ich PSD im selben Ablauf in TIFF konvertieren?** Ja – nach der Gamma‑Anpassung können Sie das Bild direkt mit `TiffOptions` als TIFF speichern.  
- **Benötige ich eine Lizenz für die Entwicklung?** Eine kostenlose Testversion reicht für Tests; für den Produktionseinsatz ist eine kommerzielle Lizenz erforderlich.  
- **Welche Java-Version wird unterstützt?** Aspose.PSD unterstützt Java 8 und höher.

## Was ist Java-Bildverarbeitung?

Java-Bildverarbeitung bezeichnet die Manipulation, Analyse und Transformation visueller Daten mithilfe von Java‑Bibliotheken. Aufgaben umfassen Größenänderung, Filterung, Farbkorrektur und Formatkonvertierung – alles kann in Desktop‑ oder Web‑Anwendungen automatisiert werden.

## Warum Aspose.PSD für die Gammakorrektur verwenden?

Aspose.PSD bietet eine hochrangige API, die die Komplexität des PSD‑Formats abstrahiert, sodass Sie sich auf die eigentlichen Bildanpassungen konzentrieren können. Es übernimmt Caching, Farbprofile und stellt einen einfachen Aufruf `adjustGamma` bereit, was es ideal für **image gamma correction** und **convert psd to tiff** Workflows macht.

## Voraussetzungen

Bevor Sie mit dem Tutorial beginnen, stellen Sie sicher, dass Sie die folgenden Voraussetzungen erfüllt haben:

1. **Java-Entwicklungsumgebung** – Vergewissern Sie sich, dass eine Java‑Entwicklungsumgebung auf Ihrem System installiert ist.  
2. **Aspose.PSD-Bibliothek** – Laden Sie die Aspose.PSD‑Bibliothek herunter und integrieren Sie sie in Ihr Java‑Projekt. Die notwendigen Ressourcen finden Sie in der [documentation](https://reference.aspose.com/psd/java/).  
3. **Beispielbild** – Bereiten Sie ein Beispiel‑PSD‑Bild vor, das Sie für die Gamma‑Anpassung verwenden.

## Pakete importieren

Um den Prozess zu starten, importieren Sie die erforderlichen Pakete in Ihrem Java‑Projekt. Dies legt die Grundlage für die nahtlose Nutzung der Aspose.PSD‑Funktionen.

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.psd.fileformats.tiff.enums.TiffPhotometrics;
import com.aspose.psd.imageoptions.TiffOptions;
```

## Schritt 1: Bild laden

Laden Sie das Beispiel‑PSD‑Bild in eine Instanz der Klasse `RasterImage`. Dies ist die Basis für die nachfolgenden Gamma‑Anpassungen.

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

## Schritt 2: Gamma anpassen

Passen Sie nun das Gamma des geladenen Bildes mit der Methode `adjustGamma` an. Stimmen Sie die Gamma‑Werte nach Ihren Anforderungen ab.

```java
// Adjust the gamma
rasterImage.adjustGamma(2.2f, 2.2f, 2.2f);
```

## Schritt 3: TiffOptions erstellen

Erzeugen Sie eine Instanz von `TiffOptions` für das resultierende Bild. Setzen Sie verschiedene Eigenschaften, wie Bits pro Sample und photometric‑Optionen, um die Ausgabe Ihren Vorgaben anzupassen.

```java
// Create an instance of TiffOptions for the resultant image
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
int[] ushort = { 8, 8, 8 };
tiffOptions.setBitsPerSample(ushort);
tiffOptions.setPhotometric(TiffPhotometrics.Rgb);
```

## Schritt 4: Ergebnisbild speichern

Speichern Sie das bearbeitete Bild im TIFF‑Format mithilfe der zuvor definierten `TiffOptions`.

```java
// Save the resultant image to TIFF format
String destName = dataDir + "AdjustGamma_out.tiff";
rasterImage.save(destName, tiffOptions);
```

## Häufige Probleme und Lösungen

| Problem | Warum es passiert | Wie zu beheben |
|---------|-------------------|----------------|
| **Bild wirkt ausgewaschen** | Gamma‑Wert zu hoch (z. B. > 2,5) | Reduzieren Sie den Gamma‑Faktor auf einen Wert zwischen 1,8 und 2,2. |
| **`rasterImage.isCached()` returns false** | Bild noch nicht in den Speicher geladen | Rufen Sie `rasterImage.cacheData()` auf, bevor Sie das Gamma anpassen. |
| **TIFF‑Dateigröße ist groß** | Bits pro Sample auf 16‑Bit gesetzt | Verwenden Sie ein 8‑Bit‑Sample (`{8,8,8}`) wie im Beispiel gezeigt. |

## Häufig gestellte Fragen

**Q: Kann ich unterschiedliche Gamma‑Werte für jeden Farbkanal anwenden?**  
A: Ja – die `adjustGamma`‑Methode akzeptiert separate float‑Werte für Rot-, Grün‑ und Blau‑Kanäle.

**Q: Ist es möglich, mehrere Bildanpassungen zu verketten, bevor ich speichere?**  
A: Absolut. Sie können Größenänderungen, Zuschnitte oder Farbkorrekturen nacheinander auf derselben `RasterImage`‑Instanz ausführen.

**Q: Unterstützt Aspose.PSD mehrseitige PSD‑Dateien?**  
A: Ja, jede Ebene kann einzeln zugegriffen und verarbeitet werden.

**Q: In welches Format kann ich neben TIFF exportieren?**  
A: Aspose.PSD unterstützt PNG, JPEG, BMP und viele weitere Formate über die jeweiligen Options‑Klassen.

## Fazit

Herzlichen Glückwunsch! Sie haben erfolgreich **java image processing** durchgeführt, indem Sie das Gamma einer PSD‑Datei angepasst und das Ergebnis als TIFF‑Bild mit Aspose.PSD for Java exportiert haben. Dieser Workflow gibt Ihnen eine feinkörnige Kontrolle über Helligkeit und Kontrast, was ihn ideal für automatisierte Grafik‑Pipelines, Web‑Services oder Desktop‑Utilities macht.

---

**Last Updated:** 2025-12-21  
**Tested With:** Aspose.PSD 24.11 for Java  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

## FAQ

### Q1: Wo finde ich die Aspose.PSD‑Dokumentation?

A1: Sie können die Dokumentation unter [https://reference.aspose.com/psd/java/](https://reference.aspose.com/psd/java/) abrufen.

### Q2: Wie lade ich Aspose.PSD für Java herunter?

A2: Laden Sie die Bibliothek von [https://releases.aspose.com/psd/java/](https://releases.aspose.com/psd/java/) herunter.

### Q3: Wo kann ich Aspose.PSD kaufen?

A3: Besuchen Sie [https://purchase.aspose.com/buy](https://purchase.aspose.com/buy), um Aspose.PSD zu erwerben.

### Q4: Gibt es eine kostenlose Testversion?

A4: Ja, Sie können eine kostenlose Testversion unter [https://releases.aspose.com/](https://releases.aspose.com/) ausprobieren.

### Q5: Wo finde ich Support für Aspose.PSD?

A5: Für Support besuchen Sie das Aspose.PSD‑Forum unter [https://forum.aspose.com/c/psd/34](https://forum.aspose.com/c/psd/34).