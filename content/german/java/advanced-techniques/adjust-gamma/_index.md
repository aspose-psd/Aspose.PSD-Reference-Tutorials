---
title: Passen Sie den Gammawert eines Bildes mit Aspose.PSD für Java an
linktitle: Gamma eines Bildes anpassen
second_title: Aspose.PSD Java-API
description: Erfahren Sie, wie Sie mit Aspose.PSD für Java mühelos den Gammawert von Bildern anpassen. Befolgen Sie unsere Schritt-für-Schritt-Anleitung für optimale Ergebnisse.
type: docs
weight: 23
url: /de/java/advanced-techniques/adjust-gamma/
---
## Einführung

Im Bereich der Bildverarbeitung ist die Anpassung des Gammawerts eines Bildes ein entscheidender Schritt, um dessen visuelle Attraktivität zu verbessern. Aspose.PSD für Java bietet Java-Entwicklern eine leistungsstarke Lösung zur mühelosen Manipulation des Bildgammas. In diesem Tutorial erfahren Sie, wie Sie den Gammawert mithilfe von Aspose.PSD anpassen. Dabei werden die einzelnen Schritte aufgeschlüsselt, um eine nahtlose Implementierung sicherzustellen.

## Voraussetzungen

Bevor Sie mit dem Tutorial beginnen, stellen Sie sicher, dass die folgenden Voraussetzungen erfüllt sind:

1. Java-Entwicklungsumgebung: Stellen Sie sicher, dass auf Ihrem System eine Java-Entwicklungsumgebung installiert ist.
2.  Aspose.PSD-Bibliothek: Laden Sie die Aspose.PSD-Bibliothek herunter und integrieren Sie sie in Ihr Java-Projekt. Die notwendigen Ressourcen finden Sie im[Dokumentation](https://reference.aspose.com/psd/java/).
3. Beispielbild: Bereiten Sie ein PSD-Beispielbild vor, das Sie zum Anwenden der Gammaanpassung verwenden.

## Pakete importieren

Um den Prozess zu starten, importieren Sie die erforderlichen Pakete in Ihr Java-Projekt. Dies schafft die Voraussetzungen für die nahtlose Nutzung der Aspose.PSD-Funktionalitäten.

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.psd.fileformats.tiff.enums.TiffPhotometrics;
import com.aspose.psd.imageoptions.TiffOptions;
```

## Schritt 1: Laden Sie das Bild

 Laden Sie zunächst das Beispiel-PSD-Bild in eine Instanz von`RasterImage` Klasse. Dies ist die Grundlage für spätere Gamma-Anpassungen.

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

// Laden Sie ein vorhandenes Bild in eine Instanz der RasterImage-Klasse
Image image = Image.load(sourceFile);

// Bildobjekt in RasterImage umwandeln
RasterImage rasterImage = (RasterImage)image;

// Überprüfen Sie, ob RasterImage für eine bessere Leistung zwischengespeichert ist
if (!rasterImage.isCached()) {
    rasterImage.cacheData();
}
```

## Schritt 2: Gamma anpassen

 Passen Sie nun den Gammawert des geladenen Bildes mit an`adjustGamma` Methode. Passen Sie die Gammawerte entsprechend Ihren Anforderungen an.

```java
// Passen Sie den Gammawert an
rasterImage.adjustGamma(2.2f, 2.2f, 2.2f);
```

## Schritt 3: TiffOptions erstellen

 Erstellen Sie eine Instanz von`TiffOptions` für das resultierende Bild. Legen Sie verschiedene Eigenschaften fest, z. B. Bits pro Probe und photometrische Optionen, um die Ausgabe an Ihre Spezifikationen anzupassen.

```java
// Erstellen Sie eine Instanz von TiffOptions für das resultierende Bild
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
int[] ushort = { 8, 8, 8 };
tiffOptions.setBitsPerSample(ushort);
tiffOptions.setPhotometric(TiffPhotometrics.Rgb);
```

## Schritt 4: Speichern Sie das resultierende Bild

 Speichern Sie das manipulierte Bild unter Verwendung des zuvor definierten Formats im TIFF-Format`TiffOptions`.

```java
// Speichern Sie das resultierende Bild im TIFF-Format
String destName = dataDir + "AdjustGamma_out.tiff";
rasterImage.save(destName, tiffOptions);
```

## Abschluss

Glückwunsch! Sie haben den Gammawert eines Bildes mit Aspose.PSD für Java erfolgreich angepasst. Dieser Prozess ermöglicht es Entwicklern, die Bildqualität mühelos zu verbessern und so zu einem optisch ansprechenden Benutzererlebnis beizutragen.

## FAQs

### F1: Wo finde ich die Aspose.PSD-Dokumentation?

 A1: Sie können auf die Dokumentation zugreifen unter[https://reference.aspose.com/psd/java/](https://reference.aspose.com/psd/java/).

### F2: Wie lade ich Aspose.PSD für Java herunter?

 A2: Laden Sie die Bibliothek herunter von[https://releases.aspose.com/psd/java/](https://releases.aspose.com/psd/java/).

### F3: Wo kann ich Aspose.PSD kaufen?

 A3: Besuchen[https://purchase.aspose.com/buy](https://purchase.aspose.com/buy) um Aspose.PSD zu kaufen.

### F4: Gibt es eine kostenlose Testversion?

 A4: Ja, Sie können eine kostenlose Testversion unter erkunden[https://releases.aspose.com/](https://releases.aspose.com/).

### F5: Wo kann ich Unterstützung für Aspose.PSD suchen?

 A5: Für Unterstützung besuchen Sie das Aspose.PSD-Forum unter[https://forum.aspose.com/c/psd/34](https://forum.aspose.com/c/psd/34).