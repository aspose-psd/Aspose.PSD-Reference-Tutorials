---
title: Passen Sie den Kontrast eines Bildes mit Aspose.PSD für Java an
linktitle: Passen Sie den Kontrast eines Bildes an
second_title: Aspose.PSD Java-API
description: Entdecken Sie die Welt der Bildkontrastanpassung in Java mit Aspose.PSD. Befolgen Sie unsere Schritt-für-Schritt-Anleitung für eine nahtlose Bildbearbeitung.
type: docs
weight: 22
url: /de/java/advanced-techniques/adjust-contrast/
---
## Einführung

Im Bereich der Bildverarbeitung mit Java sticht Aspose.PSD als leistungsstarkes Tool hervor. Unter den unzähligen Funktionen ist die Anpassung des Bildkontrasts eine häufige Anforderung. Dieses Tutorial führt Sie durch den Prozess der Anpassung des Bildkontrasts mit Aspose.PSD für Java. Ganz gleich, ob Sie ein erfahrener Entwickler sind oder gerade erst anfangen: Dieser Leitfaden hilft Ihnen dabei, diesen wesentlichen Aspekt der Bildbearbeitung zu meistern.

## Voraussetzungen

Bevor Sie mit dem Tutorial beginnen, stellen Sie sicher, dass die folgenden Voraussetzungen erfüllt sind:

- Grundlegendes Verständnis der Java-Programmierung.
-  Aspose.PSD für Java-Bibliothek installiert. Sie können es herunterladen[Hier](https://releases.aspose.com/psd/java/).

## Pakete importieren

Um zu beginnen, müssen Sie die erforderlichen Pakete in Ihr Java-Projekt importieren. Fügen Sie Ihrem Code die folgenden Zeilen hinzu:

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.psd.fileformats.tiff.enums.TiffPhotometrics;
import com.aspose.psd.imageoptions.TiffOptions;
```

## Schritt 1: Laden Sie das Bild

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

// Laden Sie ein vorhandenes Bild in eine Instanz der RasterImage-Klasse
Image image = Image.load(sourceFile);
```

 In diesem Schritt laden wir das Beispielbild („sample.psd“) mithilfe von`Image.load` Methode.

## Schritt 2: In RasterImage umwandeln und Daten zwischenspeichern

```java
// Bildobjekt in RasterImage umwandeln
RasterImage rasterImage = (RasterImage)image;

// Überprüfen Sie, ob RasterImage zwischengespeichert ist, und speichern Sie RasterImage zwischen, um eine bessere Leistung zu erzielen
if (!rasterImage.isCached()) {
    rasterImage.cacheData();
}
```

 Hier werfen wir das Generikum um`Image` Einspruch gegen a`RasterImage` für eine konkrete Bearbeitung. Das Zwischenspeichern der Bilddaten verbessert die Leistung.

## Schritt 3: Kontrast anpassen

```java
// Passen Sie den Kontrast an
rasterImage.adjustContrast(50);
```

 Der`adjustContrast`Mit dieser Methode wird der Kontrast des Bildes verändert. In diesem Beispiel wird der Kontrast um 50 % erhöht.

## Schritt 4: TiffOptions erstellen und speichern

```java
// Erstellen Sie eine Instanz von TiffOptions für das resultierende Bild
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
int[] ushort = { 8, 8, 8 };
tiffOptions.setBitsPerSample(ushort);
tiffOptions.setPhotometric(TiffPhotometrics.Rgb);

// Speichern Sie das resultierende Bild im TIFF-Format
String destName = dataDir + "AdjustContrast_out.tiff";
rasterImage.save(destName, tiffOptions);
```

 Hier haben wir uns eingerichtet`TiffOptions` für das Ausgabebild unter Angabe des Formats und anderer Eigenschaften. Das endgültige Bild wird dann in einer TIFF-Datei gespeichert.

## Abschluss

Glückwunsch! Sie haben den Kontrast eines Bildes mit Aspose.PSD für Java erfolgreich angepasst. In diesem Tutorial wurden die wesentlichen Schritte behandelt, vom Importieren von Paketen bis zum Speichern des verarbeiteten Bildes.

## FAQs

### F1: Ist Aspose.PSD mit verschiedenen Bildformaten kompatibel?

A1: Ja, Aspose.PSD unterstützt verschiedene Bildformate und bietet so Flexibilität bei Ihren Projekten.

### F2: Wie kann ich eine temporäre Lizenz für Aspose.PSD erhalten?

 A2: Sie können eine temporäre Lizenz erhalten[Hier](https://purchase.aspose.com/temporary-license/).

### F3: Wo finde ich die Aspose.PSD-Dokumentation?

A3: Die Dokumentation ist verfügbar[Hier](https://reference.aspose.com/psd/java/).

### F4: Welche Supportoptionen stehen für Aspose.PSD zur Verfügung?

 A4: Für Unterstützung besuchen Sie die[Aspose.PSD-Forum](https://forum.aspose.com/c/psd/34).

### F5: Kann ich Aspose.PSD kaufen?

 A5: Ja, Sie können Aspose.PSD kaufen[Hier](https://purchase.aspose.com/buy).