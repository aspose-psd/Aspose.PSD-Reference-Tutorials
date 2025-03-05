---
title: Passen Sie die Helligkeit eines Bildes mit Aspose.PSD für Java an
linktitle: Helligkeit eines Bildes anpassen
second_title: Aspose.PSD Java API
description: Verbessern Sie die Bildhelligkeit in Java mit Aspose.PSD. Schritt-für-Schritt-Anleitung zum programmgesteuerten Anpassen der Bildhelligkeit.
type: docs
weight: 21
url: /de/java/advanced-techniques/adjust-brightness/
---
## Einführung

Die Verbesserung von Bildern ist eine häufige Anforderung im Grafikdesign und in der Digitalfotografie. Aspose.PSD für Java bietet eine leistungsstarke Lösung zum programmgesteuerten Anpassen der Bildhelligkeit. In diesem Tutorial erfahren Sie Schritt für Schritt, wie Sie die Helligkeit eines Bildes mithilfe der Bibliothek Aspose.PSD für Java anpassen können.

## Voraussetzungen

Bevor Sie mit dem Lernprogramm beginnen, stellen Sie sicher, dass Sie die folgenden Voraussetzungen erfüllen:

-  Aspose.PSD für Java-Bibliothek: Laden Sie die Bibliothek herunter und installieren Sie sie von der[Aspose.PSD für Java-Dokumentation](https://reference.aspose.com/psd/java/).

## Pakete importieren

Importieren Sie zunächst die erforderlichen Pakete in Ihr Java-Projekt. In diesem Beispiel verwenden wir Folgendes:

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.psd.fileformats.tiff.enums.TiffPhotometrics;
import com.aspose.psd.imageoptions.TiffOptions;
```

Lassen Sie uns nun den Vorgang zum Anpassen der Helligkeit eines Bildes in einfache Schritte aufschlüsseln:

## Schritt 1: Laden Sie das Bild

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";
String destName = dataDir + "AdjustBrightness_out.tiff";

// Laden Sie ein vorhandenes Bild in eine Instanz der RasterImage-Klasse
Image image = Image.load(sourceFile);
// Konvertieren Sie das Objekt von Image in RasterImage
RasterImage rasterImage = (RasterImage) image;

// Überprüfen Sie, ob RasterImage zwischengespeichert ist, und cachen Sie RasterImage für eine bessere Leistung
if (!rasterImage.isCached()) {
    rasterImage.cacheData();
}
```

 In diesem Schritt laden wir das Zielbild und konvertieren es in ein`RasterImage` zur weiteren Verarbeitung.

## Schritt 2: Helligkeit anpassen

```java
// Passen Sie die Helligkeit an
rasterImage.adjustBrightness(-50);
```

 Hier verwenden wir die`adjustBrightness`Methode zum Ändern der Helligkeit des Bildes. In diesem Beispiel verringern wir die Helligkeit um 50 Einheiten, aber Sie können diesen Wert Ihren Anforderungen entsprechend anpassen.

## Schritt 3: TiffOptions festlegen

```java
int[] ushort = {8, 8, 8};
// Erstellen Sie eine Instanz von TiffOptions für das resultierende Bild
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
tiffOptions.setBitsPerSample(ushort);
tiffOptions.setPhotometric(TiffPhotometrics.Rgb);
```

 Konfigurieren Sie die`TiffOptions` zum Speichern des angepassten Bildes. Passen Sie die`bitsPerSample` Und`photometric` Eigenschaften basierend auf Ihren spezifischen Anforderungen.

## Schritt 4: Speichern Sie das resultierende Bild

```java
// Speichern Sie das resultierende Bild
rasterImage.save(destName, tiffOptions);
```

 Speichern Sie das geänderte Bild abschließend unter dem angegebenen`TiffOptions`.

## Abschluss

Mit Aspose.PSD für Java können Sie die Helligkeit eines Bildes ganz einfach programmgesteuert anpassen. Dieses Tutorial bietet eine umfassende Anleitung zur Implementierung dieser Funktion in Ihren Java-Anwendungen.

## Häufig gestellte Fragen

### F1: Kann ich die Helligkeit auch in anderen Bildformaten als PSD anpassen?

A1: Ja, Aspose.PSD für Java unterstützt verschiedene Bildformate wie JPEG, PNG und TIFF.

### F2: Wie kann ich mit Fehlern während des Bildanpassungsprozesses umgehen?

A2: Sie können die Fehlerbehandlung mithilfe von Try-Catch-Blöcken implementieren, um eventuell auftretende Ausnahmen zu verwalten.

### F3: Gibt es eine Grenze für den Bereich der Helligkeitseinstellung?

A3: Der Anpassungsumfang hängt vom Bildinhalt und -format ab, aber Aspose.PSD bietet Flexibilität bei der Anpassung.

### F4: Kann ich Aspose.PSD für Java in kommerziellen Projekten verwenden?

 A4: Ja, Aspose.PSD für Java ist eine kommerzielle Bibliothek und Sie können eine Lizenz erhalten von[Hier](https://purchase.aspose.com/buy).

### F5: Gibt es eine kostenlose Testversion von Aspose.PSD für Java?

 A5: Ja, Sie können die Bibliothek mit einer kostenlosen Testversion erkunden von[Hier](https://releases.aspose.com/).