---
date: 2025-12-19
description: Erfahren Sie, wie Sie die Helligkeit eines Bildes mit Aspose.PSD für
  Java anpassen. Dieses Java‑Bildbearbeitungs‑Tutorial bietet eine Schritt‑für‑Schritt‑Anleitung.
linktitle: Adjust Brightness of an Image
second_title: Aspose.PSD Java API
title: Wie man die Helligkeit eines Bildes mit Aspose.PSD für Java anpasst
url: /de/java/advanced-techniques/adjust-brightness/
weight: 21
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Helligkeit eines Bildes mit Aspose.PSD für Java anpassen

## Einführung

Wenn Sie **lernen möchten, wie man die Helligkeit** eines Bildes direkt aus Java‑Code anpasst, sind Sie hier genau richtig. Das Anpassen der Helligkeit ist eine häufige Aufgabe für Grafikdesigner, Fotografen und alle, die Bildverarbeitungspipelines erstellen. In diesem **Java‑Bildbearbeitungs‑Tutorial** gehen wir den kompletten Workflow durch – Laden einer PSD/TIFF, Anwenden eines Helligkeits‑Offsets und Speichern des Ergebnisses – mithilfe der Aspose.PSD für Java‑Bibliothek.

## Schnellantworten
- **Welche Bibliothek behandelt die Helligkeit?** Aspose.PSD für Java  
- **Welche Methode ändert die Helligkeit?** `RasterImage.adjustBrightness()`  
- **Kann ich mit PSD‑ und TIFF‑Dateien arbeiten?** Ja, die API unterstützt beide Formate.  
- **Benötige ich eine Lizenz für die Produktion?** Für den nicht‑evaluativen Einsatz ist eine kommerzielle Lizenz erforderlich.  
- **Wie lange dauert die Implementierung?** In der Regel unter 10 Minuten für eine einfache Anpassung.

## Was ist die Bild‑Helligkeitsanpassung?

Die Bild‑Helligkeitsanpassung ändert die Gesamthelligkeit jedes Pixels in einem Bild. Eine Erhöhung der Helligkeit macht dunkle Bereiche heller, während eine Verringerung das gesamte Bild abdunkelt. Dieser Vorgang ist nützlich, um unterbelichtete Fotos zu korrigieren, Assets für den Druck vorzubereiten oder visuelle Effekte in Anwendungen zu erzeugen.

## Warum Aspose.PSD für Java verwenden?

- **Vollständige Formatunterstützung** – PSD, TIFF, JPEG, PNG und mehr.  
- **Keine externen nativen Abhängigkeiten** – reines Java, einfach zu integrieren.  
- **Leistungsstarkes Caching** – Rasterdaten können für schnellere wiederholte Vorgänge zwischengespeichert werden.  
- **Umfangreiche API** – Methoden für Farbkorrektur, Ebenen, Masken und andere fortgeschrittene Bearbeitungen.

## Voraussetzungen

Bevor Sie mit dem Tutorial beginnen, stellen Sie sicher, dass Sie die folgenden Voraussetzungen erfüllen:

- Aspose.PSD für Java Bibliothek: Laden Sie die Bibliothek von der [Aspose.PSD für Java Dokumentation](https://reference.aspose.com/psd/java/) herunter und installieren Sie sie.

## Pakete importieren

Um zu beginnen, importieren Sie die notwendigen Pakete in Ihr Java‑Projekt. In diesem Beispiel verwenden wir die folgenden:

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.psd.fileformats.tiff.enums.TiffPhotometrics;
import com.aspose.psd.imageoptions.TiffOptions;
```

Nun zerlegen wir den Prozess zur Anpassung der Helligkeit eines Bildes in einfache Schritte:

## Wie man die Helligkeit mit Aspose.PSD anpasst

### Schritt 1: Bild laden

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

### Schritt 2: Helligkeit anpassen

```java
// Adjust the brightness
rasterImage.adjustBrightness(-50);
```

Hier verwenden wir die Methode `adjustBrightness`, um die Helligkeit des Bildes zu ändern. In diesem Beispiel verringern wir die Helligkeit um 50 Einheiten, Sie können diesen Wert jedoch nach Ihren Anforderungen anpassen.

### Schritt 3: TiffOptions festlegen

```java
int[] ushort = {8, 8, 8};
// Create an instance of TiffOptions for the resultant image
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
tiffOptions.setBitsPerSample(ushort);
tiffOptions.setPhotometric(TiffPhotometrics.Rgb);
```

Konfigurieren Sie die `TiffOptions` zum Speichern des angepassten Bildes. Passen Sie die Eigenschaften `bitsPerSample` und `photometric` je nach Ihren spezifischen Bedürfnissen an.

### Schritt 4: Ergebnisbild speichern

```java
// Save the resultant image
rasterImage.save(destName, tiffOptions);
```

Speichern Sie schließlich das modifizierte Bild mit den angegebenen `TiffOptions`.

## Häufige Probleme und Lösungen

| Problem | Grund | Lösung |
|---------|-------|--------|
| **`ClassCastException` beim Casten von Image** | Die Datei ist kein Rasterbild (z. B. ein vektorbasierter PSD). | Überprüfen Sie das Quellformat oder verwenden Sie `image instanceof RasterImage` vor dem Casten. |
| **Helligkeitsänderung hat keine Wirkung** | Das Bild wurde vor der Anpassung nicht zwischengespeichert. | Rufen Sie `rasterImage.cacheData()` wie in Schritt 1 gezeigt auf. |
| **Gespeicherte Datei erscheint beschädigt** | Falsche `TiffOptions`‑Konfiguration. | Stellen Sie sicher, dass `bitsPerSample` der Tiefe des Quellbildes entspricht (gewöhnlich 8‑Bit pro Kanal). |

## Häufig gestellte Fragen

### Q1: Kann ich die Helligkeit in anderen Bildformaten außer PSD anpassen?

A1: Ja, Aspose.PSD für Java unterstützt verschiedene Bildformate wie JPEG, PNG und TIFF.

### Q2: Wie kann ich Fehler während des Bildanpassungsprozesses behandeln?

A2: Sie können Fehlerbehandlung mit try‑catch‑Blöcken implementieren, um auftretende Ausnahmen zu verwalten.

### Q3: Gibt es eine Grenze für den Bereich der Helligkeitsanpassung?

A3: Der Anpassungsbereich hängt vom Bildinhalt und -format ab, aber Aspose.PSD bietet Flexibilität bei der Anpassung.

### Q4: Kann ich Aspose.PSD für Java in kommerziellen Projekten verwenden?

A4: Ja, Aspose.PSD für Java ist eine kommerzielle Bibliothek, und Sie können eine Lizenz [hier](https://purchase.aspose.com/buy) erwerben.

### Q5: Gibt es eine kostenlose Testversion von Aspose.PSD für Java?

A5: Ja, Sie können die Bibliothek mit einer kostenlosen Testversion [hier](https://releases.aspose.com/) ausprobieren.

### Q6: Beeinflusst die Methode `adjustBrightness` die Sichtbarkeit von Ebenen?

A6: Die Methode arbeitet am rasterisierten Composite‑Bild, sodass die Ebenensichtbarkeit während der Rasterisierung berücksichtigt wird.

### Q7: Kann ich mehrere Anpassungen (z. B. Kontrast, Sättigung) hintereinander ausführen?

A7: Absolut. Nach der Helligkeitsanpassung können Sie `adjustContrast`, `adjustSaturation` usw. auf derselben `RasterImage`‑Instanz aufrufen.

---

**Zuletzt aktualisiert:** 2025-12-19  
**Getestet mit:** Aspose.PSD für Java 24.12 (zum Zeitpunkt der Erstellung)  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}