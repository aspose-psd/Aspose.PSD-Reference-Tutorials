---
date: 2026-07-08
description: 'Java Bildbearbeitungsbibliothek Tutorial: Erfahren Sie, wie Sie ein
  Bild mit Aspose.PSD für Java zuschneiden, die Größe ändern, die Leinwand erweitern
  und PSD in JPEG konvertieren.'
keywords:
- java image editing library
- java image processing tutorial
- how to crop image java
lastmod: 2026-07-08
linktitle: Erweitern und Zuschneiden von Bildern
og_description: Java Bildbearbeitungsbibliothek Tutorial zeigt, wie man Bilder zuschneidet,
  die Leinwand erweitert und PSD in JPEG konvertiert, mit Aspose.PSD für Java, in
  wenigen Minuten.
og_image_alt: 'Guide: Crop and expand images in Java with Aspose.PSD'
og_title: Java Bildbearbeitungsbibliothek – Bild zuschneiden mit Aspose.PSD
schemas:
- author: Aspose
  dateModified: '2026-07-08'
  description: 'Java image editing library tutorial: learn how to crop image java
    using Aspose.PSD for Java, resize, expand canvas, and convert PSD to JPEG.'
  headline: Java Image Editing Library – Crop Image with Aspose.PSD
  type: TechArticle
- questions:
  - answer: Aspose.PSD for Java.
    question: What library handles crop image java?
  - answer: A free trial works for testing; a commercial license is required for production.
    question: Do I need a license for development?
  - answer: Yes, using `JpegOptions` together with a cropping rectangle.
    question: Can I convert PSD to JPEG while cropping?
  - answer: Aspose.PSD supports Java 8 and newer versions.
    question: Is Java 8 supported?
  - answer: Typically under 10 minutes for a basic crop operation.
    question: How long does the implementation take?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- java image editing
- Aspose.PSD
- image cropping
- PSD to JPEG
title: Java Bildbearbeitungsbibliothek – Bild zuschneiden mit Aspose.PSD
url: /de/java/image-editing/expand-and-crop-images/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Java-Bildbearbeitungsbibliothek: Bild zuschneiden in Java mit Aspose.PSD

## Einführung

In diesem Tutorial lernen Sie, wie man eine **java image editing library**—insbesondere Aspose.PSD für Java—verwendet, um PSD-Dateien zuzuschneiden, zu erweitern und in JPEG zu konvertieren. Egal, ob Sie Assets für ein Webportal vorbereiten oder die Thumbnail-Erstellung automatisieren, die nachstehenden Schritte bieten einen wiederholbaren, produktionsbereiten Workflow, den Sie in jedes Java 8+‑Projekt integrieren können.

## Schnelle Antworten
- **Welche Bibliothek verarbeitet das Zuschneiden von Bildern in Java?** Aspose.PSD for Java.  
- **Benötige ich eine Lizenz für die Entwicklung?** Ein kostenloser Testlauf funktioniert für Tests; für die Produktion ist eine kommerzielle Lizenz erforderlich.  
- **Kann ich PSD während des Zuschneidens in JPEG konvertieren?** Ja, mit `JpegOptions` zusammen mit einem Zuschnittrechteck.  
- **Wird Java 8 unterstützt?** Aspose.PSD unterstützt Java 8 und neuere Versionen.  
- **Wie lange dauert die Implementierung?** In der Regel unter 10 Minuten für einen einfachen Zuschnittvorgang.

## Was ist „crop image java“?

Crop image java bedeutet, einen rechteckigen Bereich des Quellbildes auszuwählen und alles außerhalb dieses Bereichs zu verwerfen. Mit Aspose.PSD erstellen Sie ein `Rectangle`, das den Bereich definiert, wenden es auf ein `RasterImage` an und speichern das Ergebnis dann in einem unterstützten Format wie JPEG.

## Warum Aspose.PSD für das Zuschneiden von Bildern in Java verwenden?

Aspose.PSD bietet eine **java image editing library**, die PSD-Dateien nativ verarbeitet, über 100 Layer‑Funktionen unterstützt und Bilder bis zu 10 000 × 10 000 Pixel verarbeiten kann, während der Speicherverbrauch unter 500 MB bleibt. Außerdem bietet es integrierte Konvertierung zu JPEG, PNG, BMP und mehr, alles ohne externe Werkzeuge. Das macht Bulk‑Processing‑Pipelines schnell, zuverlässig und leicht wartbar.

## Voraussetzungen

1. **Java Development Kit (JDK)** – Java 8 oder neuer installiert.  
2. **Aspose.PSD for Java** – laden Sie die Bibliothek von der offiziellen Seite **[hier](https://releases.aspose.com/psd/java/)** herunter.  

> **Pro Tipp:** Fügen Sie die Aspose.PSD JAR zu Ihrem Projekt‑Classpath oder den Maven/Gradle‑Abhängigkeiten hinzu, um `ClassNotFoundException` zu vermeiden.

## Pakete importieren

Fügen Sie die erforderlichen Importe zu Ihrer Java‑Quelldatei hinzu. Diese Klassen geben Ihnen Zugriff auf das Laden von Bildern, Rastermanipulation, Rechteckdefinition und JPEG‑Exportoptionen.

## Wie man Bild in Java mit Aspose.PSD zuschneidet?

Laden Sie das Quell‑PSD mit `RasterImage`, definieren Sie ein `Rectangle`, das den Zuschnittbereich beschreibt (negative Koordinaten können die Leinwand erweitern), und speichern Sie schließlich das Ergebnis mit `JpegOptions`. Dieser dreistufige Ablauf verarbeitet sowohl das Zuschneiden als auch die Formatkonvertierung in einem Durchgang und eliminiert die Notwendigkeit von Zwischendateien.

## Schritt 1: Legen Sie Ihr Dokumentenverzeichnis fest

Geben Sie den Ordner an, der die Quell‑PSD‑Datei enthält. Ersetzen Sie den Platzhalter durch den tatsächlichen Pfad auf Ihrem Rechner.

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;
import com.aspose.psd.Rectangle;

import com.aspose.psd.imageoptions.JpegOptions;
```

## Schritt 2: Quell‑ und Zielpfade angeben

Legen Sie fest, von wo das PSD gelesen und wohin das zugeschnittene JPEG geschrieben werden soll.

```java
String dataDir = "Your Document Directory";
```

## Schritt 3: Bild laden und zwischenspeichern

`RasterImage` stellt eine rasterisierte Version einer PSD‑Datei im Speicher dar.  
Laden Sie das PSD in ein `RasterImage`‑Objekt. Das Zwischenspeichern verbessert die Leistung für nachfolgende Vorgänge wie das Zuschneiden.

```java
String sourceFile = dataDir + "example1.psd";
String destName = dataDir + "jpeg_out.jpg";
```

## Schritt 4: Rechteck für das Zuschneiden erstellen

`Rectangle` definiert die X‑, Y‑Koordinaten sowie Breite/Höhe des Zuschnittbereichs.  
Erstellen Sie ein `Rectangle`, das den Bereich beschreibt, den Sie behalten möchten. Die Koordinaten können negativ sein, um die Leinwand vor dem Zuschneiden zu **erweitern**, was nützlich ist, um einen Rand um das Originalbild hinzuzufügen.

```java
RasterImage rasterImage = (RasterImage)Image.load(sourceFile);
rasterImage.cacheData();
```

> **Warum negative Koordinaten verwenden?**  
> Negative X/Y‑Werte verschieben den Zuschnittbereich nach links/oben und fügen effektiv leeren Raum (Erweiterung) um den Originalinhalt herum hinzu, bevor der endgültige Zuschnitt erfolgt.

## Schritt 5: Das zugeschnittene Bild speichern

`JpegOptions` gibt Einstellungen für die JPEG‑Ausgabe an, wie Qualität und Kompression.  
Speichern Sie schließlich das resultierende Bild mit `JpegOptions`. Dieser Schritt demonstriert zudem **convert psd jpeg**, während das Zuschnittrechteck angewendet wird.

```java
Rectangle destRect = new Rectangle(-200, -200, 300, 300);
```

> **Ergebnis:** `jpeg_out.jpg` enthält nun ein 300 × 300 Pixel‑Bild, das um 200 px auf jeder Seite erweitert und dann auf das definierte Rechteck zugeschnitten wurde.

Herzlichen Glückwunsch! Sie haben erfolgreich **java image cropping** durchgeführt, die Leinwand erweitert und eine PSD‑Datei in JPEG konvertiert – alles in wenigen prägnanten Codezeilen.

## Häufige Anwendungsfälle

- **Assets für das Web vorbereiten** – zuschneiden und die Größe von Screenshots oder Designs vor dem Hochladen anpassen.  
- **Thumbnails generieren** – einen bestimmten Bereich aus einer großen PSD für Vorschauszwecke extrahieren.  
- **Automatisierte Stapelverarbeitung** – durchlaufen Sie einen Ordner mit PSD‑Dateien und wenden Sie dasselbe Zuschnittrechteck auf jede an.

## Fehlerbehebung & Tipps

| Problem | Empfohlene Lösung |
|-------|----------------|
| `OutOfMemoryError` beim Laden großer PSDs | Rufen Sie `rasterImage.cacheData()` frühzeitig auf und erwägen Sie, die JVM‑Heap‑Größe (`-Xmx`) zu erhöhen. |
| Zugeschnittener Bereich ist nicht zentriert | Überprüfen Sie die X/Y‑Offsets des Rechtecks; denken Sie daran, dass negative Werte die Leinwand erweitern. |
| Ausgabe‑JPEG wirkt unscharf | Passen Sie die Qualitäts‑Einstellung von `JpegOptions` an (z. B. `new JpegOptions { Quality = 90 }`). |

## Häufig gestellte Fragen

### Q1: Ist Aspose.PSD mit verschiedenen Java‑Versionen kompatibel?
A1: Ja, Aspose.PSD unterstützt Java 8, 11, 17 und neuere Versionen und gewährleistet damit eine breite Kompatibilität in Entwicklungsumgebungen.

### Q2: Kann ich Aspose.PSD für kommerzielle Projekte verwenden?
A2: Absolut, Aspose.PSD bietet kommerzielle Lizenzen für Entwickler, sodass es sowohl in privaten als auch in kommerziellen Anwendungen verwendet werden kann.

### Q3: Gibt es Einschränkungen bei den unterstützten Bilddateiformaten?
A3: Aspose.PSD unterstützt über 30 Bildformate, darunter PSD, JPEG, PNG, BMP, TIFF und weitere. Siehe die [Dokumentation](https://reference.aspose.com/psd/java/) für eine vollständige Liste.

### Q4: Wie kann ich Unterstützung für Aspose.PSD‑bezogene Anfragen erhalten?
A4: Besuchen Sie das [Aspose.PSD‑Forum](https://forum.aspose.com/c/psd/34), um Hilfe von der Community oder dem Aspose‑Supportteam zu erhalten.

### Q5: Gibt es eine kostenlose Testversion?
A5: Ja, Sie können Aspose.PSD mit einer kostenlosen Testversion ausprobieren. Laden Sie sie [hier](https://releases.aspose.com/) herunter.

---

**Zuletzt aktualisiert:** 2026-07-08  
**Getestet mit:** Aspose.PSD for Java 24.12  
**Autor:** Aspose  

{{< blocks/products/products-backtop-button >}}

```java
rasterImage.save(destName, new JpegOptions(), destRect);
```

## Verwandte Tutorials

- [Einfaches Skalieren mit Aspose.PSD – Java-Bildbearbeitungsbibliothek](/psd/java/basic-image-operations/simple-resizing/)
- [Wie man ein Bild um 270 Grad mit Aspose.PSD für Java dreht](/psd/java/advanced-image-manipulation/rotate-image/)
- [Wie man Gamma in der Java-Bildverarbeitung mit Aspose.PSD anpasst](/psd/java/advanced-techniques/adjust-gamma/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}