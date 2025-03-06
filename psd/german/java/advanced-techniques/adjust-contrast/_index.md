---
title: Passen Sie den Kontrast eines Bildes mit Aspose.PSD für Java an
linktitle: Kontrast eines Bildes anpassen
second_title: Aspose.PSD Java API
description: Entdecken Sie die Welt der Bildkontrastanpassung in Java mit Aspose.PSD. Folgen Sie unserer Schritt-für-Schritt-Anleitung zur nahtlosen Bildbearbeitung.
weight: 22
url: /de/java/advanced-techniques/adjust-contrast/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Passen Sie den Kontrast eines Bildes mit Aspose.PSD für Java an

## Einführung

Im Bereich der Bildbearbeitung mit Java ist Aspose.PSD ein leistungsstarkes Tool. Zu den unzähligen Funktionen gehört die Anpassung des Bildkontrasts. Dieses Tutorial führt Sie durch den Prozess der Anpassung des Bildkontrasts mit Aspose.PSD für Java. Egal, ob Sie ein erfahrener Entwickler sind oder gerade erst anfangen, diese Anleitung hilft Ihnen, diesen wesentlichen Aspekt der Bildbearbeitung zu meistern.

## Voraussetzungen

Bevor Sie mit dem Lernprogramm beginnen, stellen Sie sicher, dass die folgenden Voraussetzungen erfüllt sind:

- Grundlegende Kenntnisse der Java-Programmierung.
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

 In diesem Schritt laden wir das Beispielbild ("sample.psd") mit dem`Image.load` Verfahren.

## Schritt 2: In Rasterbild umwandeln und Daten zwischenspeichern

```java
// Konvertieren Sie das Objekt von Image in RasterImage
RasterImage rasterImage = (RasterImage)image;

// Überprüfen Sie, ob RasterImage zwischengespeichert ist, und cachen Sie RasterImage für eine bessere Leistung
if (!rasterImage.isCached()) {
    rasterImage.cacheData();
}
```

 Hier werfen wir das generische`Image` Einspruch gegen eine`RasterImage` für bestimmte Verarbeitungen. Das Zwischenspeichern der Bilddaten verbessert die Leistung.

## Schritt 3: Kontrast anpassen

```java
// Kontrast anpassen
rasterImage.adjustContrast(50);
```

 Der`adjustContrast`Die Methode wird verwendet, um den Kontrast des Bildes zu ändern. In diesem Beispiel wird der Kontrast um 50 % erhöht.

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

 Hier richten wir`TiffOptions` für das Ausgabebild, wobei das Format und andere Eigenschaften angegeben werden. Das endgültige Bild wird dann in einer TIFF-Datei gespeichert.

## Abschluss

Herzlichen Glückwunsch! Sie haben den Kontrast eines Bildes mit Aspose.PSD für Java erfolgreich angepasst. Dieses Tutorial behandelte die wesentlichen Schritte, vom Importieren von Paketen bis zum Speichern des verarbeiteten Bildes.

## Häufig gestellte Fragen

### F1: Ist Aspose.PSD mit verschiedenen Bildformaten kompatibel?

A1: Ja, Aspose.PSD unterstützt verschiedene Bildformate und bietet Flexibilität für Ihre Projekte.

### F2: Wie kann ich eine temporäre Lizenz für Aspose.PSD erhalten?

 A2: Sie können eine vorübergehende Lizenz erhalten[Hier](https://purchase.aspose.com/temporary-license/).

### F3: Wo finde ich die Aspose.PSD-Dokumentation?

A3: Die Dokumentation ist verfügbar[Hier](https://reference.aspose.com/psd/java/).

### F4: Welche Supportoptionen sind für Aspose.PSD verfügbar?

 A4: Für Support besuchen Sie die[Aspose.PSD-Forum](https://forum.aspose.com/c/psd/34).

### F5: Kann ich Aspose.PSD kaufen?

 A5: Ja, Sie können Aspose.PSD kaufen[Hier](https://purchase.aspose.com/buy).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
