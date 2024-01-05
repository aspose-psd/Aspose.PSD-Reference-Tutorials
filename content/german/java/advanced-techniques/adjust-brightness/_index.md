---
title: Passen Sie die Helligkeit eines Bildes mit Aspose.PSD für Java an
linktitle: Passen Sie die Helligkeit eines Bildes an
second_title: Aspose.PSD Java-API
description: Verbessern Sie die Bildhelligkeit in Java mit Aspose.PSD. Schritt-für-Schritt-Anleitung zum programmgesteuerten Anpassen der Bildhelligkeit.
type: docs
weight: 21
url: /de/java/advanced-techniques/adjust-brightness/
---
## Einführung

Die Verbesserung von Bildern ist eine häufige Anforderung im Grafikdesign und in der digitalen Fotografie. Aspose.PSD für Java bietet eine leistungsstarke Lösung zum programmgesteuerten Anpassen der Bildhelligkeit. In diesem Tutorial erfahren Sie Schritt für Schritt, wie Sie die Aspose.PSD für Java-Bibliothek verwenden, um die Helligkeit eines Bildes anzupassen.

## Voraussetzungen

Bevor Sie mit dem Tutorial beginnen, stellen Sie sicher, dass Sie die folgenden Voraussetzungen erfüllen:

-  Aspose.PSD für Java-Bibliothek: Laden Sie die Bibliothek von herunter und installieren Sie sie[Aspose.PSD für Java-Dokumentation](https://reference.aspose.com/psd/java/).

## Pakete importieren

Importieren Sie zunächst die erforderlichen Pakete in Ihr Java-Projekt. In diesem Beispiel verwenden wir Folgendes:

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.psd.fileformats.tiff.enums.TiffPhotometrics;
import com.aspose.psd.imageoptions.TiffOptions;
```

Lassen Sie uns nun den Vorgang zum Anpassen der Helligkeit eines Bildes in einfache Schritte unterteilen:

## Schritt 1: Laden Sie das Bild

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";
String destName = dataDir + "AdjustBrightness_out.tiff";

// Laden Sie ein vorhandenes Bild in eine Instanz der RasterImage-Klasse
Image image = Image.load(sourceFile);
// Bildobjekt in RasterImage umwandeln
RasterImage rasterImage = (RasterImage) image;

// Überprüfen Sie, ob RasterImage zwischengespeichert ist, und speichern Sie RasterImage zwischen, um eine bessere Leistung zu erzielen
if (!rasterImage.isCached()) {
    rasterImage.cacheData();
}
```

 In diesem Schritt laden wir das Zielbild und wandeln es in ein um`RasterImage` zur Weiterverarbeitung.

## Schritt 2: Helligkeit anpassen

```java
// Passen Sie die Helligkeit an
rasterImage.adjustBrightness(-50);
```

 Hier verwenden wir die`adjustBrightness`Methode zum Ändern der Helligkeit des Bildes. In diesem Beispiel verringern wir die Helligkeit um 50 Einheiten, Sie können diesen Wert jedoch entsprechend Ihren Anforderungen anpassen.

## Schritt 3: TiffOptions festlegen

```java
int[] ushort = {8, 8, 8};
// Erstellen Sie eine Instanz von TiffOptions für das resultierende Bild
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
tiffOptions.setBitsPerSample(ushort);
tiffOptions.setPhotometric(TiffPhotometrics.Rgb);
```

 Konfigurieren Sie die`TiffOptions` zum Speichern des angepassten Bildes. Verstelle die`bitsPerSample` Und`photometric` Immobilien basierend auf Ihren spezifischen Bedürfnissen.

## Schritt 4: Speichern Sie das resultierende Bild

```java
// Speichern Sie das resultierende Bild
rasterImage.save(destName, tiffOptions);
```

 Speichern Sie abschließend das geänderte Bild mit dem angegebenen`TiffOptions`.

## Abschluss

Das programmgesteuerte Anpassen der Helligkeit eines Bildes ist mit Aspose.PSD für Java ganz einfach. Dieses Tutorial bietet eine umfassende Anleitung zur Implementierung dieser Funktionalität in Ihren Java-Anwendungen.

## FAQs

### F1: Kann ich die Helligkeit in anderen Bildformaten außer PSD anpassen?

A1: Ja, Aspose.PSD für Java unterstützt verschiedene Bildformate wie JPEG, PNG und TIFF.

### F2: Wie kann ich mit Fehlern während des Bildanpassungsprozesses umgehen?

A2: Sie können die Fehlerbehandlung mithilfe von Try-Catch-Blöcken implementieren, um möglicherweise auftretende Ausnahmen zu verwalten.

### F3: Gibt es eine Grenze für den Bereich der Helligkeitsanpassung?

A3: Der Anpassungsbereich hängt vom Bildinhalt und -format ab, aber Aspose.PSD bietet Flexibilität bei der Anpassung.

### F4: Kann ich Aspose.PSD für Java in kommerziellen Projekten verwenden?

 A4: Ja, Aspose.PSD für Java ist eine kommerzielle Bibliothek und Sie können eine Lizenz von erhalten[Hier](https://purchase.aspose.com/buy).

### F5: Gibt es eine kostenlose Testversion für Aspose.PSD für Java?

 A5: Ja, Sie können die Bibliothek mit einer kostenlosen Testversion erkunden[Hier](https://releases.aspose.com/).