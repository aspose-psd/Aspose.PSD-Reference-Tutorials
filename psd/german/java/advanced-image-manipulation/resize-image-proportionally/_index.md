---
title: Passen Sie die Bildgröße proportional mit Aspose.PSD für Java an
linktitle: Bildgröße proportional anpassen
second_title: Aspose.PSD Java API
description: Verbessern Sie Ihre Java-Anwendungen mit Aspose.PSD. Folgen Sie unserer Anleitung, um Bilder mühelos proportional zu skalieren. Verbessern Sie noch heute Ihre Bildbearbeitungsfunktionen.
weight: 17
url: /de/java/advanced-image-manipulation/resize-image-proportionally/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Passen Sie die Bildgröße proportional mit Aspose.PSD für Java an

## Einführung

Willkommen zu unserer Schritt-für-Schritt-Anleitung zum proportionalen Ändern der Bildgröße mit Aspose.PSD für Java. Wenn Sie Ihre Java-Anwendungen mit effizienten Funktionen zur Bildgrößenänderung verbessern möchten, sind Sie hier richtig. In diesem Tutorial führen wir Sie in klaren und prägnanten Schritten durch den Prozess.

## Voraussetzungen

Bevor Sie mit dem Lernprogramm beginnen, stellen Sie sicher, dass die folgenden Voraussetzungen erfüllt sind:

1. Java-Umgebung: Stellen Sie sicher, dass Java auf Ihrem System installiert ist.
2.  Aspose.PSD-Bibliothek: Laden Sie die Aspose.PSD-Bibliothek herunter und installieren Sie sie. Sie finden die erforderlichen Ressourcen[Hier](https://releases.aspose.com/psd/java/).

## Pakete importieren

Sobald Sie Ihre Voraussetzungen erfüllt haben, importieren Sie die erforderlichen Pakete in Ihr Java-Projekt. Stellen Sie sicher, dass in Ihrem Projekt korrekt auf die Aspose.PSD-Bibliothek verwiesen wird.

```java
import com.aspose.psd.Image;

import com.aspose.psd.imageoptions.PngOptions;
```

## Schritt 1: Laden Sie das Bild

Beginnen Sie, indem Sie das Bild, dessen Größe Sie ändern möchten, in Ihre Java-Anwendung laden.

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

Image image = Image.load(sourceFile);

if (!image.isCached()) {
    image.cacheData();
}
```

## Schritt 2: Breite und Höhe festlegen

Bestimmen Sie die neue Breite und Höhe für Ihr skaliertes Bild. In diesem Beispiel skalieren wir das Bild auf die Hälfte seiner Originalmaße.

```java
int newWidth = image.getWidth() / 2;
image.resizeWidthProportionally(newWidth);

int newHeight = image.getHeight() / 2;
image.resizeHeightProportionally(newHeight);
```

## Schritt 3: Speichern Sie das skalierte Bild

Speichern Sie das skalierte Bild am gewünschten Speicherort und geben Sie die Formatoptionen an (in diesem Fall PNG).

```java
String destName = dataDir + "SimpleResizeImageProportionally_out.png";
image.save(destName, new PngOptions());
```

Und da haben Sie es! Sie haben die Größe eines Bildes mit Aspose.PSD für Java erfolgreich proportional geändert.

## Abschluss

In diesem Tutorial haben wir die wesentlichen Schritte zum proportionalen Ändern der Bildgröße mithilfe der Aspose.PSD-Bibliothek für Java erläutert. Jetzt können Sie diese Funktion mühelos in Ihre Java-Anwendungen integrieren, um die Bildverarbeitung zu verbessern.

## Häufig gestellte Fragen

### F1: Ist Aspose.PSD mit allen Bildformaten kompatibel?

 A1: Aspose.PSD unterstützt verschiedene Bildformate, darunter PSD, PNG, JPEG und mehr. Überprüfen Sie die[Dokumentation](https://reference.aspose.com/psd/java/) für eine umfassende Liste.

### F2: Kann ich Aspose.PSD für kommerzielle Projekte verwenden?

 A2: Ja, das können Sie. Besuchen Sie die[Kaufseite](https://purchase.aspose.com/buy) für Lizenzdetails.

### F3: Sind temporäre Lizenzen zu Testzwecken verfügbar?

 A3: Ja, Sie können eine vorübergehende Lizenz erhalten[Hier](https://purchase.aspose.com/temporary-license/) zur Auswertung.

### F4: Wo finde ich Unterstützung für Aspose.PSD?

 A4: Besuchen Sie die[Aspose.PSD-Forum](https://forum.aspose.com/c/psd/34) für die Unterstützung und Hilfe der Community.

### F5: Wie kann ich auf die Aspose.PSD-Dokumentation zugreifen?

 A5: Lesen Sie die ausführliche Dokumentation[Hier](https://reference.aspose.com/psd/java/).
`
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
