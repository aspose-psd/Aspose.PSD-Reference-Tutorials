---
title: Wenden Sie Gaußsche und Wiener-Filter in Aspose.PSD für Java an
linktitle: Wenden Sie Gaußsche und Wiener-Filter an
second_title: Aspose.PSD Java-API
description: Verbessern Sie Ihre Java-Bildverarbeitung mit Aspose.PSD. Erfahren Sie Schritt für Schritt, wie Sie Gaußsche und Wiener-Filter anwenden, um beeindruckende visuelle Ergebnisse zu erzielen.
type: docs
weight: 10
url: /de/java/image-processing/apply-gaussian-wiener-filters/
---
## Einführung

Willkommen zu unserem umfassenden Tutorial zum Anwenden von Gaußschen und Wiener-Filtern in Aspose.PSD für Java! In diesem Leitfaden führen wir Sie durch den Prozess der Verbesserung Ihrer Bilder mithilfe dieser leistungsstarken Filter. Aspose.PSD für Java bietet eine Reihe robuster Funktionen für die Bildverarbeitung und mit der Anwendung von Gauß- und Wiener-Filtern können Sie glattere und verfeinerte Bilder erzielen.

## Voraussetzungen

Bevor wir uns mit dem Tutorial befassen, stellen Sie sicher, dass die folgenden Voraussetzungen erfüllt sind:

- Java-Entwicklungsumgebung: Stellen Sie sicher, dass auf Ihrem Computer eine Java-Entwicklungsumgebung eingerichtet ist.

- Aspose.PSD für Java-Bibliothek: Laden Sie die Aspose.PSD für Java-Bibliothek herunter und installieren Sie sie. Den Download-Link finden Sie hier[Hier](https://releases.aspose.com/psd/java/).

## Pakete importieren

Importieren Sie in Ihrem Java-Projekt die erforderlichen Pakete für Aspose.PSD. Hier ist eine Beispiel-Importanweisung, um Ihnen den Einstieg zu erleichtern:

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.imagefilters.filteroptions.GaussWienerFilterOptions;
import com.aspose.psd.imageoptions.GifOptions;
```

Lassen Sie uns das Beispiel nun in mehrere Schritte unterteilen, um Gauß- und Wiener-Filter anzuwenden.

## Schritt 1: Bild laden

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

Image image = Image.load(sourceFile);
RasterImage rasterImage = (RasterImage)image;
```

In diesem Schritt laden wir die PSD-Bilddatei aus dem angegebenen Verzeichnis.

## Schritt 2: Überprüfen Sie RasterImage

```java
if (rasterImage == null) {
    return;
}
```

Stellen Sie sicher, dass das geladene Bild ein gültiges RasterImage ist. andernfalls wird der Prozess beendet.

## Schritt 3: Filteroptionen konfigurieren

```java
GaussWienerFilterOptions options = new GaussWienerFilterOptions(12, 3);
options.setGrayscale(true);
```

Erstellen Sie eine Instanz von GaussWienerFilterOptions, legen Sie die Radiusgröße und den Glättungswert fest und geben Sie an, ob Sie den Filter in Graustufen anwenden möchten.

## Schritt 4: Filter anwenden und speichern

```java
rasterImage.filter(image.getBounds(), options);
String destName = dataDir + "gauss_wiener_out.gif";
image.save(destName, new GifOptions());
```

Wenden Sie abschließend die konfigurierten Gauß- und Wiener-Filter auf das RasterImage an und speichern Sie das resultierende Bild im GIF-Format.

## Abschluss

Glückwunsch! Sie haben erfolgreich gelernt, wie Sie Gaußsche und Wiener-Filter mit Aspose.PSD für Java anwenden. Experimentieren Sie mit verschiedenen Parametern, um die gewünschte Bildverbesserung zu erzielen.

## FAQs

### F1: Kann ich diese Filter auf Bilder in anderen Formaten als PSD anwenden?

A1: Ja, Aspose.PSD für Java unterstützt verschiedene Bildformate über PSD hinaus.

### F2: Gibt es Einschränkungen in der Testversion von Aspose.PSD für Java?

A2: Die Testversion unterliegt Einschränkungen und Sie können alle Funktionen erkunden, indem Sie eine gültige Lizenz erwerben.

### F3: Wie erhalte ich Unterstützung für Aspose.PSD für Java?

 A3: Besuchen Sie die[Aspose.PSD-Forum](https://forum.aspose.com/c/psd/34) für Community-Unterstützung und Diskussionen.

### F4: Gibt es eine temporäre Lizenz für Testzwecke?

 A4: Ja, Sie können eine temporäre Lizenz erhalten.[Hier](https://purchase.aspose.com/temporary-license/).

### F5: Wo finde ich eine ausführliche Dokumentation für Aspose.PSD für Java?

 A5: Siehe[Dokumentation](https://reference.aspose.com/psd/java/) für ausführliche Informationen.