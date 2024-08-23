---
title: Wenden Sie Median- und Wiener-Filter mit Aspose.PSD für Java an
linktitle: Median- und Wiener-Filter anwenden
second_title: Aspose.PSD Java API
description: Entdecken Sie die Leistungsfähigkeit der Bildverarbeitung in Java mit Aspose.PSD. Erfahren Sie Schritt für Schritt, wie Sie Median- und Wiener-Filter anwenden. Verbessern Sie mühelos die Bildqualität.
type: docs
weight: 12
url: /de/java/image-processing/apply-median-wiener-filters/
---
## Einführung

Im Bereich der Java-Programmierung sticht Aspose.PSD als leistungsstarkes Tool zur Bildbearbeitung und -verarbeitung hervor. Eine der wichtigsten Funktionen ist die Anwendung von Median- und Wiener-Filtern, die eine entscheidende Rolle bei der Verbesserung der Bildqualität und der Rauschreduzierung spielen. Diese Schritt-für-Schritt-Anleitung führt Sie durch den Prozess der Anwendung dieser Filter mit Aspose.PSD für Java.

## Voraussetzungen

Bevor Sie mit dem Lernprogramm beginnen, stellen Sie sicher, dass die folgenden Voraussetzungen erfüllt sind:

1.  Aspose.PSD für Java-Bibliothek: Laden Sie die Bibliothek herunter und installieren Sie sie von[Hier](https://releases.aspose.com/psd/java/).
2. Java-Entwicklungsumgebung: Stellen Sie sicher, dass auf Ihrem System eine Java-Entwicklungsumgebung eingerichtet ist.

## Pakete importieren

Beginnen Sie mit dem Importieren der erforderlichen Pakete, um die Aspose.PSD-Funktionalität in Ihrem Java-Projekt zu nutzen:

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.imagefilters.filteroptions.MedianFilterOptions;
import com.aspose.psd.imageoptions.GifOptions;
```

## Medianfilter anwenden

### Schritt 1: Laden Sie das Bild

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

//Laden Sie das Quellbild
Image image = Image.load(sourceFile);
```

### Schritt 2: Bild in Rasterbild umwandeln

```java
// Konvertieren Sie das Bild in RasterImage
RasterImage rasterImage = (RasterImage)image;
if (rasterImage == null) {
    return;
}
```

### Schritt 3: MedianFilterOptions-Instanz erstellen

```java
// Erstellen Sie eine Instanz der MedianFilterOptions-Klasse und legen Sie die Filtergröße fest
MedianFilterOptions options = new MedianFilterOptions(4);
```

### Schritt 4: Medianfilter anwenden

```java
// MedianFilterOptions-Filter auf RasterImage-Objekt anwenden
rasterImage.filter(image.getBounds(), options);
```

### Schritt 5: Speichern Sie das resultierende Bild

```java
String destName = dataDir + "median_test_denoise_out.gif";
// Speichern Sie das resultierende Bild als GIF
image.save(destName, new GifOptions());
```

Indem Sie diese Schritte befolgen, haben Sie den Medianfilter mit Aspose.PSD für Java erfolgreich auf Ihr Bild angewendet.

## Abschluss

In diesem Tutorial haben wir den Prozess der Anwendung von Median- und Wiener-Filtern mit Aspose.PSD für Java untersucht. Diese Filter sind unverzichtbar, um die Bildqualität zu verbessern und Rauschen in Ihren Java-Anwendungen zu reduzieren. Indem Sie die Leistung von Aspose.PSD nutzen, können Sie diese Filter mühelos in Ihre Bildverarbeitungs-Workflows integrieren.

## Häufig gestellte Fragen

### F1: Kann ich diese Filter auf Bilder beliebigen Formats anwenden?

A1: Ja, Aspose.PSD unterstützt eine Vielzahl von Bildformaten und ist daher für verschiedene Projekte vielseitig einsetzbar.

### F2: Gibt es eine kostenlose Testversion für Aspose.PSD für Java?

 A2: Ja, Sie können eine kostenlose Testversion erhalten[Hier](https://releases.aspose.com/).

### F3: Wie erhalte ich Unterstützung für Aspose.PSD für Java?

 A3: Besuchen Sie die[Aspose.PSD-Forum](https://forum.aspose.com/c/psd/34) für die Unterstützung der Community.

### F4: Wo finde ich die Dokumentation für Aspose.PSD für Java?

 A4: Siehe Dokumentation[Hier](https://reference.aspose.com/psd/java/).

### F5: Wie kann ich Aspose.PSD für Java kaufen?

 A5: Sie können das Produkt kaufen[Hier](https://purchase.aspose.com/buy).