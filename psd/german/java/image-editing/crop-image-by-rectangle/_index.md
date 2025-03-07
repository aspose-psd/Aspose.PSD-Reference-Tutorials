---
title: Bild per Rechteck in Aspose.PSD für Java zuschneiden
linktitle: Bild rechteckig zuschneiden
second_title: Aspose.PSD Java API
description: Entdecken Sie die nahtlosen Bildzuschneidefunktionen in Java mit Aspose.PSD. Folgen Sie unserer Schritt-für-Schritt-Anleitung, um Bilder mühelos mit Aspose.PSD für Java zuzuschneiden.
weight: 15
url: /de/java/image-editing/crop-image-by-rectangle/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Bild per Rechteck in Aspose.PSD für Java zuschneiden

## Einführung

In der Welt der Java-Entwicklung ist die Bildbearbeitung eine gängige Aufgabe, und Aspose.PSD für Java bietet eine leistungsstarke Lösung für die Bildverarbeitung. In diesem Tutorial führen wir Sie durch den Prozess des Zuschneidens eines Bildes um ein Rechteck mit Aspose.PSD für Java. Befolgen Sie die folgenden Schritte, um dies problemlos zu erreichen.

## Voraussetzungen

Bevor Sie mit dem Lernprogramm beginnen, stellen Sie sicher, dass die folgenden Voraussetzungen erfüllt sind:

- Auf Ihrem Computer ist Java Development Kit (JDK) installiert.
- Aspose.PSD für Java-Bibliothek. Sie können es herunterladen von der[Webseite](https://releases.aspose.com/psd/java/).

## Pakete importieren

Stellen Sie sicher, dass Sie die erforderlichen Pakete in Ihr Java-Projekt einbinden, um die Funktionen von Aspose.PSD für Java nutzen zu können. Fügen Sie am Anfang Ihrer Java-Datei die folgenden Importanweisungen hinzu:

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;
import com.aspose.psd.Rectangle;

import com.aspose.psd.imageoptions.JpegOptions;
```

Lassen Sie uns den Vorgang nun in mehrere Schritte aufteilen, um Sie durch das Zuschneiden eines Bildes um ein Rechteck mit Aspose.PSD für Java zu führen.

## Schritt 1: Richten Sie Ihr Dokumentverzeichnis ein

```java
String dataDir = "Your Document Directory";
```

 Ersetzen`"Your Document Directory"` durch den tatsächlichen Pfad, in dem sich Ihre PSD-Datei befindet.

## Schritt 2: Quell- und Zieldateien angeben

```java
String sourceFile = dataDir + "sample.psd";
String destName = dataDir + "CroppingByRectangle_out.jpg";
```

Definieren Sie die Pfade für Ihre Quell-PSD-Datei und die Ziel-JPEG-Datei.

## Schritt 3: Laden und Zwischenspeichern des Bildes

```java
RasterImage rasterImage = (RasterImage)Image.load(sourceFile);

if (!rasterImage.isCached()) {
    rasterImage.cacheData();
}
```

 Laden Sie das PSD-Bild in ein`RasterImage` Instanz und zwischenspeichern Sie deren Daten.

## Schritt 4: Erstellen und Definieren des Zuschneiderechtecks

```java
Rectangle rectangle = new Rectangle(20, 20, 20, 20);
```

 Erstellen Sie eine Instanz des`Rectangle` Klasse mit der gewünschten Größe zum Zuschneiden.

## Schritt 5: Bild zuschneiden und speichern

```java
rasterImage.crop(rectangle);
rasterImage.save(destName, new JpegOptions());
```

Führen Sie den Zuschneidevorgang mit dem angegebenen Rechteck durch und speichern Sie die Ergebnisse als JPEG-Datei.

Wiederholen Sie diese Schritte nach Bedarf und passen Sie die Parameter entsprechend Ihren spezifischen Anforderungen an.

## Abschluss

In diesem Tutorial haben wir den Prozess des Zuschneidens eines Bildes um ein Rechteck mit Aspose.PSD für Java durchgegangen. Indem Sie diese Schritte befolgen, können Sie problemlos leistungsstarke Bildbearbeitungsfunktionen in Ihre Java-Anwendungen integrieren.

## Häufig gestellte Fragen

### F1: Kann ich Aspose.PSD für Java mit anderen Java-Frameworks verwenden?

A1: Ja, Aspose.PSD für Java kann in verschiedene Java-Frameworks integriert werden und bietet so Flexibilität für Ihre Entwicklungsprojekte.

### F2: Gibt es eine kostenlose Testversion für Aspose.PSD für Java?

 A2: Ja, Sie können auf die kostenlose Testversion zugreifen[Hier](https://releases.aspose.com/).

### F3: Wo finde ich zusätzliche Unterstützung oder Hilfe?

 A3: Besuchen Sie die[Aspose.PSD-Forum](https://forum.aspose.com/c/psd/34) für Community-Unterstützung und Diskussionen.

### F4: Wie erhalte ich eine temporäre Lizenz für Aspose.PSD für Java?

 A4: Sie können eine temporäre Lizenz erwerben[Hier](https://purchase.aspose.com/temporary-license/).

### F5: Welche Bildformate werden zum Zuschneiden in Aspose.PSD für Java unterstützt?

A5: Aspose.PSD für Java unterstützt verschiedene Bildformate, darunter PSD, PNG, JPEG und mehr.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
