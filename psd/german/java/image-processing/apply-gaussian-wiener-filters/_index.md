---
title: Wenden Sie Gauß- und Wiener-Filter in Aspose.PSD für Java an
linktitle: Anwenden von Gauß- und Wiener-Filtern
second_title: Aspose.PSD Java API
description: Verbessern Sie Ihre Java-Bildverarbeitung mit Aspose.PSD. Erfahren Sie Schritt für Schritt, wie Sie Gauß- und Wiener-Filter anwenden, um beeindruckende visuelle Ergebnisse zu erzielen.
weight: 10
url: /de/java/image-processing/apply-gaussian-wiener-filters/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Wenden Sie Gauß- und Wiener-Filter in Aspose.PSD für Java an

## Einführung

Willkommen zu unserem umfassenden Tutorial zur Anwendung von Gauß- und Wiener-Filtern in Aspose.PSD für Java! In dieser Anleitung führen wir Sie durch den Prozess der Bildverbesserung mit diesen leistungsstarken Filtern. Aspose.PSD für Java bietet einen robusten Satz von Funktionen zur Bildverarbeitung und mit der Anwendung von Gauß- und Wiener-Filtern können Sie glattere und verfeinerte Bilder erzielen.

## Voraussetzungen

Bevor wir mit dem Tutorial beginnen, stellen Sie sicher, dass die folgenden Voraussetzungen erfüllt sind:

- Java-Entwicklungsumgebung: Stellen Sie sicher, dass auf Ihrem Computer eine Java-Entwicklungsumgebung eingerichtet ist.

- Aspose.PSD für Java-Bibliothek: Laden Sie die Aspose.PSD für Java-Bibliothek herunter und installieren Sie sie. Den Download-Link finden Sie[Hier](https://releases.aspose.com/psd/java/).

## Pakete importieren

Importieren Sie in Ihr Java-Projekt die erforderlichen Pakete für Aspose.PSD. Hier ist eine Beispiel-Importanweisung, um Ihnen den Einstieg zu erleichtern:

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.imagefilters.filteroptions.GaussWienerFilterOptions;
import com.aspose.psd.imageoptions.GifOptions;
```

Lassen Sie uns das Beispiel nun in mehrere Schritte aufteilen, um Gauß- und Wiener-Filter anzuwenden.

## Schritt 1: Bild laden

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

Image image = Image.load(sourceFile);
RasterImage rasterImage = (RasterImage)image;
```

In diesem Schritt laden wir die PSD-Bilddatei aus dem angegebenen Verzeichnis.

## Schritt 2: RasterImage prüfen

```java
if (rasterImage == null) {
    return;
}
```

Stellen Sie sicher, dass es sich bei dem geladenen Bild um ein gültiges Rasterbild handelt. Andernfalls wird der Vorgang abgebrochen.

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

Wenden Sie abschließend die konfigurierten Gauß- und Wiener-Filter auf das Rasterbild an und speichern Sie das resultierende Bild im GIF-Format.

## Abschluss

Herzlichen Glückwunsch! Sie haben erfolgreich gelernt, wie Sie mit Aspose.PSD für Java Gauß- und Wiener-Filter anwenden. Experimentieren Sie mit verschiedenen Parametern, um die gewünschten Bildverbesserungen zu erzielen.

## Häufig gestellte Fragen

### F1: Kann ich diese Filter auf Bilder in anderen Formaten als PSD anwenden?

A1: Ja, Aspose.PSD für Java unterstützt neben PSD verschiedene Bildformate.

### F2: Gibt es irgendwelche Einschränkungen in der Testversion von Aspose.PSD für Java?

A2: Die Testversion weist Einschränkungen auf und Sie können den vollen Funktionsumfang erkunden, indem Sie eine gültige Lizenz erwerben.

### F3: Wie kann ich Support für Aspose.PSD für Java erhalten?

 A3: Besuchen Sie die[Aspose.PSD Forum](https://forum.aspose.com/c/psd/34) für Community-Unterstützung und Diskussionen.

### F4: Gibt es eine temporäre Lizenz zu Testzwecken?

 A4: Ja, Sie können eine vorübergehende Lizenz erhalten[Hier](https://purchase.aspose.com/temporary-license/).

### F5: Wo finde ich eine ausführliche Dokumentation für Aspose.PSD für Java?

 A5: Siehe[Dokumentation](https://reference.aspose.com/psd/java/) für ausführlichere Informationen.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
