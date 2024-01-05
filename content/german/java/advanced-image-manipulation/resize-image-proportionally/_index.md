---
title: Ändern Sie die Bildgröße proportional mit Aspose.PSD für Java
linktitle: Bildgröße proportional ändern
second_title: Aspose.PSD Java-API
description: Erweitern Sie Ihre Java-Anwendungen mit Aspose.PSD. Befolgen Sie unsere Anleitung, um die Größe von Bildern mühelos proportional zu ändern. Steigern Sie noch heute Ihre Möglichkeiten zur Bildbearbeitung.
type: docs
weight: 17
url: /de/java/advanced-image-manipulation/resize-image-proportionally/
---
## Einführung

Willkommen zu unserer Schritt-für-Schritt-Anleitung zur proportionalen Größenänderung von Bildern mit Aspose.PSD für Java. Wenn Sie Ihre Java-Anwendungen mit effizienten Funktionen zur Größenänderung von Bildern erweitern möchten, sind Sie bei uns genau richtig. In diesem Tutorial führen wir Sie anhand klarer und prägnanter Schritte durch den Prozess.

## Voraussetzungen

Bevor Sie mit dem Tutorial beginnen, stellen Sie sicher, dass die folgenden Voraussetzungen erfüllt sind:

1. Java-Umgebung: Stellen Sie sicher, dass Java auf Ihrem System installiert ist.
2.  Aspose.PSD-Bibliothek: Laden Sie die Aspose.PSD-Bibliothek herunter und installieren Sie sie. Sie können die erforderlichen Ressourcen finden[Hier](https://releases.aspose.com/psd/java/).

## Pakete importieren

Sobald Sie Ihre Voraussetzungen geklärt haben, importieren Sie die erforderlichen Pakete in Ihr Java-Projekt. Stellen Sie sicher, dass die Aspose.PSD-Bibliothek in Ihrem Projekt korrekt referenziert wird.

```java
import com.aspose.psd.Image;

import com.aspose.psd.imageoptions.PngOptions;
```

## Schritt 1: Laden Sie das Bild

Laden Sie zunächst das Bild, dessen Größe Sie ändern möchten, in Ihre Java-Anwendung.

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

Image image = Image.load(sourceFile);

if (!image.isCached()) {
    image.cacheData();
}
```

## Schritt 2: Breite und Höhe angeben

Bestimmen Sie die neue Breite und Höhe für Ihr in der Größe geändertes Bild. In diesem Beispiel ändern wir die Größe des Bildes auf die Hälfte seiner Originalabmessungen.

```java
int newWidth = image.getWidth() / 2;
image.resizeWidthProportionally(newWidth);

int newHeight = image.getHeight() / 2;
image.resizeHeightProportionally(newHeight);
```

## Schritt 3: Speichern Sie das in der Größe geänderte Bild

Speichern Sie das in der Größe geänderte Bild am gewünschten Speicherort und geben Sie dabei die Formatoptionen an (in diesem Fall PNG).

```java
String destName = dataDir + "SimpleResizeImageProportionally_out.png";
image.save(destName, new PngOptions());
```

Und da haben Sie es! Sie haben die Größe eines Bildes mit Aspose.PSD für Java erfolgreich proportional geändert.

## Abschluss

In diesem Tutorial haben wir die wesentlichen Schritte zur proportionalen Größenänderung von Bildern mithilfe der Aspose.PSD-Bibliothek für Java behandelt. Jetzt können Sie diese Funktionalität für eine verbesserte Bildverarbeitung mühelos in Ihre Java-Anwendungen integrieren.

## FAQs

### F1: Ist Aspose.PSD mit allen Bildformaten kompatibel?

 A1: Aspose.PSD unterstützt verschiedene Bildformate, darunter PSD, PNG, JPEG und mehr. Überprüf den[Dokumentation](https://reference.aspose.com/psd/java/) für eine umfassende Liste.

### F2: Kann ich Aspose.PSD für kommerzielle Projekte verwenden?

 A2: Ja, das können Sie. Besuche den[Kaufseite](https://purchase.aspose.com/buy) für Lizenzdetails.

### F3: Sind temporäre Lizenzen für Testzwecke verfügbar?

 A3: Ja, Sie können eine temporäre Lizenz erhalten[Hier](https://purchase.aspose.com/temporary-license/) zur Auswertung.

### F4: Wo finde ich Unterstützung für Aspose.PSD?

 A4: Besuchen Sie die[Aspose.PSD-Forum](https://forum.aspose.com/c/psd/34) für die Unterstützung und Unterstützung der Gemeinschaft.

### F5: Wie kann ich auf die Aspose.PSD-Dokumentation zugreifen?

 A5: Weitere Informationen finden Sie in der ausführlichen Dokumentation[Hier](https://reference.aspose.com/psd/java/).
`