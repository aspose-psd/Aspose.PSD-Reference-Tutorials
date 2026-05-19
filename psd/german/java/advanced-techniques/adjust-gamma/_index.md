---
date: 2026-02-27
description: Erfahren Sie, wie Sie Gamma in der Java‑Bildverarbeitung mit Aspose.PSD
  anpassen, PSD in TIFF konvertieren und ausgewaschene Bilder in einem kurzen Tutorial
  beheben.
linktitle: Adjust Gamma of an Image
second_title: Aspose.PSD Java API
title: Wie man Gamma in der Java‑Bildverarbeitung mit Aspose.PSD anpasst
url: /de/java/advanced-techniques/adjust-gamma/
weight: 23
---

" line.

Let's craft.

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Wie man Gamma in der Java-Bildverarbeitung mit Aspose.PSD anpasst

## Einführung

Wenn Sie an **java image processing** arbeiten, ist das **Anpassen von Gamma** eine grundlegende Technik, um Helligkeit und Kontrast zu verbessern, ohne Details zu verlieren. In diesem Tutorial zeigen wir, wie Sie **Aspose.PSD für Java** verwenden, um eine Gamma‑Korrektur auf eine PSD‑Datei anzuwenden, **PSD in TIFF zu konvertieren** und ein **ausgewaschenes Bild** zu vermeiden. Sie sehen, warum dieser Ansatz schnell, zuverlässig und perfekt für serverseitige Bild‑Pipelines ist.

## Schnellantworten
- **Was bewirkt die Gamma‑Korrektur?** Sie ordnet Luminanzwerte neu, um dunkle Bereiche heller oder helle Bereiche dunkler zu machen, während die Gesamtdetails erhalten bleiben.  
- **Welche Bibliothek übernimmt die Verarbeitung?** Aspose.PSD für Java stellt eine dedizierte `adjustGamma`‑Methode für Rasterbilder bereit.  
- **Kann ich PSD im gleichen Ablauf in TIFF konvertieren?** Ja – nach der Gamma‑Anpassung können Sie das Bild direkt mit `TiffOptions` als TIFF speichern.  
- **Benötige ich eine Lizenz für die Entwicklung?** Eine kostenlose Testversion reicht für Tests; für den Produktionseinsatz ist eine kommerzielle Lizenz erforderlich.  
- **Welche Java‑Version wird unterstützt?** Aspose.PSD unterstützt Java 8 und höher.

## Wie man Gamma in der Java-Bildverarbeitung anpasst
Das Anpassen von Gamma ist ein Kernbestandteil jedes **java image processing tutorial**, das sich mit Helligkeit oder Kontrast beschäftigt. Im Folgenden zerlegen wir die Schritte, erklären, warum jede Zeile wichtig ist, und zeigen, wie Sie den Prozess in Ihren bestehenden Code integrieren.

## Was ist Java Gamma‑Korrektur?
Gamma‑Korrektur ändert die nichtlineare Beziehung zwischen den codierten Pixelwerten und der angezeigten Helligkeit. Durch das Anpassen der Gamma‑Kurve können Sie **ausgewaschene Bild**‑Probleme beheben oder Details in Schatten verbessern, ohne Highlights zu überbelichten.

## Warum Aspose.PSD für Gamma‑Korrektur verwenden?
Aspose.PSD fungiert als leistungsstarke **java image processing library**, die die Komplexität des PSD‑Formats abstrahiert. Es verarbeitet Farbprofile, Caching und bietet einen einfachen Aufruf `adjustGamma`, was es ideal für **java gamma correction** und **convert PSD to TIFF** Workflows macht.

## Voraussetzungen

1. **Java‑Entwicklungsumgebung** – Java 8 oder höher installiert.  
2. **Aspose.PSD‑Bibliothek** – Laden Sie die JAR herunter und fügen Sie sie Ihrem Projekt hinzu. Siehe die offizielle [documentation](https://reference.aspose.com/psd/java/).  
3. **Beispielbild** – Eine PSD‑Datei, die Sie verarbeiten möchten (z. B. `sample.psd`).  

## Pakete importieren

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.psd.fileformats.tiff.enums.TiffPhotometrics;
import com.aspose.psd.imageoptions.TiffOptions;
```

## Schritt 1: Bild laden

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

**Profi‑Tipp:** Das Cachen der Rasterdaten reduziert den Speicherverbrauch, wenn Sie mehrere Anpassungen hintereinander durchführen.

## Schritt 2: Gamma anpassen

```java
// Adjust the gamma
rasterImage.adjustGamma(2.2f, 2.2f, 2.2f);
```

Sie können unterschiedliche Werte für die Rot-, Grün‑ und Blau‑Kanäle übergeben, wenn Sie kanalspezifische Anpassungen benötigen.

## Schritt 3: TiffOptions erstellen

```java
// Create an instance of TiffOptions for the resultant image
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
int[] ushort = { 8, 8, 8 };
tiffOptions.setBitsPerSample(ushort);
tiffOptions.setPhotometric(TiffPhotometrics.Rgb);
```

Das Setzen einer 8‑Bit‑Probe (`{8,8,8}`) hält die TIFF‑Dateigröße angemessen, während die Farbtreue erhalten bleibt.

## Schritt 4: Ergebnisbild speichern

```java
// Save the resultant image to TIFF format
String destName = dataDir + "AdjustGamma_out.tiff";
rasterImage.save(destName, tiffOptions);
```

Nach dem Speichern können Sie das TIFF in nachgelagerte Systeme wie Druckdienste oder Web‑APIs einspeisen.

## Häufige Anwendungsfälle

- **Automatisierte Grafik‑Pipelines** – Gamma on‑the‑fly anpassen, bevor Thumbnails erzeugt werden.  
- **Batch‑Konvertierungstools** – Große PSD‑Archive in TIFF konvertieren und gleichzeitig die Helligkeit normalisieren.  
- **Web‑Dienste** – Einen Endpunkt bereitstellen, der ein PSD empfängt, Gamma‑Korrektur anwendet und ein TIFF für den Client zurückgibt.

## Häufige Probleme und Lösungen

| Problem | Warum es passiert | Lösung |
|-------|----------------|------------|
| **Bild erscheint ausgewaschen** | Gamma‑Wert zu hoch (z. B. > 2,5) | Gamma‑Faktor auf einen Wert zwischen 1,8 und 2,2 senken. |
| **`rasterImage.isCached()` gibt false zurück** | Bild noch nicht in den Speicher geladen | `rasterImage.cacheData()` vor der Gamma‑Anpassung aufrufen. |
| **TIFF‑Dateigröße ist groß** | Bits‑pro‑Sample auf 16‑Bit gesetzt | Wie im Beispiel ein 8‑Bit‑Sample (`{8,8,8}`) verwenden. |

## Häufig gestellte Fragen

**F: Kann ich unterschiedliche Gamma‑Werte für jeden Farbkanal anwenden?**  
A: Ja – die `adjustGamma`‑Methode akzeptiert separate Float‑Werte für Rot-, Grün‑ und Blau‑Kanäle.

**F: Ist es möglich, mehrere Bildanpassungen vor dem Speichern zu verketten?**  
A: Absolut. Sie können Größenänderungen, Zuschnitte oder Farbkorrekturen sequenziell auf derselben `RasterImage`‑Instanz durchführen.

**F: Unterstützt Aspose.PSD mehrseitige PSD‑Dateien?**  
A: Ja, jede Ebene kann einzeln zugegriffen und verarbeitet werden.

**F: In welche Formate kann ich außer TIFF exportieren?**  
A: Aspose.PSD unterstützt PNG, JPEG, BMP und viele weitere Formate über die jeweiligen Options‑Klassen.

**F: Wie vermeide ich ein ausgewaschenes Bild nach der Gamma‑Korrektur?**  
A: Beginnen Sie mit einem moderaten Gamma (etwa 2,0) und prüfen Sie das Ergebnis; bei zu heller Darstellung den Wert nach unten anpassen.

## Fazit

Herzlichen Glückwunsch! Sie haben erfolgreich **wie man Gamma anpasst** in einem **java image processing**‑Workflow gelernt, ein PSD in TIFF konvertiert und gängige Fallstricke wie ein **ausgewaschenes Bild** vermieden. Dieses Muster gibt Ihnen feinkörnige Kontrolle über Helligkeit und Kontrast und ist ideal für automatisierte Grafik‑Pipelines, Web‑Dienste oder Desktop‑Utilities.

---

**Zuletzt aktualisiert:** 2026-02-27  
**Getestet mit:** Aspose.PSD 24.11 für Java  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}