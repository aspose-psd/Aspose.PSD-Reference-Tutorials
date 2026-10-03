---
date: 2026-10-03
description: Erfahren Sie, wie man in Java Bild-Metadaten liest und JPEG EXIF-Tags
  mit Aspose.PSD for Java in diesem Schritt-für-Schritt-Leitfaden ändert, ideal für
  Entwickler, die Bild-Metadaten effizient verarbeiten.
keywords:
- java read image metadata
- read EXIF tags Java
- modify JPEG metadata Java
- Aspose.PSD Java
lastmod: 2026-10-03
linktitle: JPEG EXIF-Tags in Java lesen und ändern
og_description: Erfahren Sie, wie man in Java Bild-Metadaten liest und JPEG EXIF-Tags
  mit Aspose.PSD for Java. Dieser Leitfaden zeigt Schritt-für-Schritt-Code zum Extrahieren
  und Aktualisieren von EXIF-Informationen.
og_image_alt: Guide showing how to java read image metadata and edit JPEG EXIF tags
  using Aspose.PSD for Java
og_title: Wie man in Java Bild-Metadaten liest und JPEG EXIF-Tags ändert
schemas:
- author: Aspose
  dateModified: '2026-10-03'
  description: Learn how to java read image metadata and modify JPEG EXIF tags with
    Aspose.PSD for Java in this step‑by‑step guide, perfect for developers handling
    image metadata efficiently.
  headline: How to java read image metadata and modify JPEG EXIF tags
  type: TechArticle
- description: Learn how to java read image metadata and modify JPEG EXIF tags with
    Aspose.PSD for Java in this step‑by‑step guide, perfect for developers handling
    image metadata efficiently.
  name: How to java read image metadata and modify JPEG EXIF tags
  steps:
  - name: '**Java Development Kit (JDK)** – make sure you have JDK 11 or newer. You
      can download it from the [Oracle website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).'
    text: '**Java Development Kit (JDK)** – make sure you have JDK 11 or newer. You
      can download it from the [Oracle website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).'
  - name: '**Aspose.PSD for Java library** – obtain the latest JAR from the [Aspose
      releases page](https://releases.aspose.com/psd/java/).'
    text: '**Aspose.PSD for Java library** – obtain the latest JAR from the [Aspose
      releases page](https://releases.aspose.com/psd/java/).'
  - name: '**IDE** – IntelliJ IDEA, Eclipse, or any editor you prefer.'
    text: '**IDE** – IntelliJ IDEA, Eclipse, or any editor you prefer.'
  - name: '**Basic Java knowledge** – you should be comfortable with creating projects
      and adding external JARs.'
    text: '**Basic Java knowledge** – you should be comfortable with creating projects
      and adding external JARs.'
  type: HowTo
- questions:
  - answer: EXIF (Exchangeable Image File Format) metadata stores camera settings,
      timestamps, GPS coordinates, and other information embedded in JPEG and other
      image files.
    question: What is EXIF data?
  - answer: You can get a free trial from the [Aspose releases page](https://releases.aspose.com/).
    question: Can I use Aspose.PSD for Java for free?
  - answer: Aspose.PSD for Java supports Java SE 7 and above.
    question: Is Aspose.PSD for Java compatible with all versions of Java?
  - answer: Check out the [documentation](https://reference.aspose.com/psd/java/)
      for more details.
    question: Where can I find more documentation on Aspose.PSD for Java?
  - answer: You can get support from the [Aspose PSD support forum](https://forum.aspose.com/c/psd/34/).
    question: How do I get support for Aspose.PSD for Java?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- java image metadata
- exif tags
- aspose psd
- jpeg metadata
- java tutorial
title: Wie man in Java Bild-Metadaten liest und JPEG EXIF-Tags ändert
url: /de/java/java-jpeg-image-processing/read-modify-jpeg-exif-tags-java/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# JPEG EXIF-Tags in Java lesen und ändern

## Einleitung
Wenn Sie **java read image metadata** aus JPEG-Dateien lesen und programmgesteuert ändern müssen, sind Sie hier genau richtig. In diesem Tutorial führen wir Sie durch das Extrahieren und Aktualisieren von EXIF-Tags mit Aspose.PSD für Java. Am Ende können Sie Kameradetails, Orientierung und benutzerdefinierte Felder auslesen und zurück in die Datei schreiben – ganz ohne grafischen Editor.

## Schnelle Antworten
- **Welche Bibliothek verarbeitet JPEG EXIF in Java?** Aspose.PSD für Java.  
- **Wie viele Codezeilen werden zum Lesen von EXIF benötigt?** Etwa drei Zeilen nach dem Laden des Bildes.  
- **Können Sie EXIF-Tags ändern?** Ja, Sie können jedes Standard‑ oder benutzerdefinierte Tag ändern und das Ergebnis speichern.  
- **Unterstützte Bildformate?** Über 150 Formate, darunter PSD, JPEG, PNG, TIFF und BMP.  
- **Mindest-Java-Version?** Java 7 oder höher.

## Warum Aspose.PSD für Java verwenden?
Aspose.PSD unterstützt **150+ Bildformate** und kann Dateien bis zu **2 GB** verarbeiten, ohne das gesamte Dokument in den Speicher zu laden. Das ermöglicht schnelle, speichereffiziente Metadaten‑Operationen bei großen Fotosammlungen. Außerdem bietet es eine einfache API zum Lesen und Schreiben von EXIF, IPTC und XMP, sodass die Batch‑Verarbeitung von Tausenden Bildern effizient und zuverlässig ist.

## Voraussetzungen
1. **Java Development Kit (JDK)** – stellen Sie sicher, dass Sie JDK 11 oder neuer haben. Sie können es von der [Oracle-Website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html) herunterladen.  
2. **Aspose.PSD für Java‑Bibliothek** – holen Sie sich die neueste JAR von der [Aspose‑Releases‑Seite](https://releases.aspose.com/psd/java/).  
3. **IDE** – IntelliJ IDEA, Eclipse oder ein beliebiger Editor Ihrer Wahl.  
4. **Grundlegende Java‑Kenntnisse** – Sie sollten mit dem Erstellen von Projekten und dem Hinzufügen externer JARs vertraut sein.

## Was ist Java read image metadata?
Java read image metadata bezeichnet den Vorgang, programmgesteuert auf eingebettete Informationen wie EXIF, IPTC und XMP zuzugreifen, die in Bilddateien gespeichert sind. Diese Metadaten können Kameraeinstellungen, Zeitstempel, GPS‑Koordinaten, Urheberrechtshinweise und Benutzerkommentare umfassen und ermöglichen Anwendungen, Bilder anhand ihrer beschreibenden Daten zu organisieren, zu suchen und zu manipulieren.

## Pakete importieren
Fügen Sie zunächst die Aspose.PSD‑JAR zu Ihrem Klassenpfad hinzu und importieren Sie die benötigten Klassen.

Das `com.aspose.psd`‑Paket stellt die Kern‑API zum Laden von Bildern und zum Zugriff auf deren Ressourcen bereit.

```java
import com.aspose.psd.Image;
import com.aspose.psd.exif.JpegExifData;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.resources.Thumbnail4Resource;
import com.aspose.psd.fileformats.psd.resources.ThumbnailResource;
```

## Wie liest man Bildmetadaten aus JPEG-Dateien in Java?
Laden Sie das JPEG mit `PsdImage.load("image.jpg")`, finden Sie die Thumbnail‑Ressource, die EXIF‑Daten enthält, und rufen Sie dann `ExifData.read()` auf, um ein befülltes `ExifData`‑Objekt zu erhalten. Dieser Ein‑Schritt‑Ansatz gibt Ihnen vollen Zugriff auf alle Standard‑EXIF‑Felder und beliebige benutzerdefinierte Tags.

## Schritt 1: PSD‑Bild laden
`PsdImage` ist die Aspose.PSD‑Klasse, die eine PSD‑Datei repräsentiert und Methoden zum Zugriff auf Ressourcen und Metadaten bereitstellt.  
In diesem Schritt laden wir das PSD‑Bild, aus dem wir die EXIF‑Daten auslesen wollen. Stellen Sie sicher, dass Ihr Bild im richtigen Verzeichnis liegt.

```java
String dataDir = "Your Document Directory";
PsdImage image = null;
try {
    image = (PsdImage) Image.load(dataDir + "1280px-Zebras_Serengeti.psd");
} catch (IOException e) {
    e.printStackTrace();
}
```

## Schritt 2: Über Bildressourcen iterieren
`ThumbnailResource` repräsentiert ein Miniaturbild, das in einer PSD‑Datei gespeichert ist und häufig eingebettete EXIF‑Daten enthält.  
Nachdem das Bild geladen ist, iterieren wir über seine Ressourcen, um die Thumbnail‑Ressource zu finden, die typischerweise die EXIF‑Daten enthält.

```java
for (int i = 0; i < image.getImageResources().length; i++) {
    if (image.getImageResources()[i] instanceof ThumbnailResource) {
        ThumbnailResource thumbnail = (ThumbnailResource) image.getImageResources()[i];
        // Proceed to next step
    }
}
```

## Schritt 3: EXIF-Daten extrahieren
`JpegExifData` ist die Klasse, die EXIF‑Informationen aus einem JPEG‑Bild hält und das Lesen sowie Ändern einzelner Tags ermöglicht.  
Jetzt, wo wir die Thumbnail‑Ressource haben, können wir die EXIF‑Daten daraus extrahieren. EXIF‑Daten enthalten wertvolle Informationen wie den Namen des Kamerabesitzers, den Blendenwert, die Orientierung und mehr.

```java
JpegExifData exifData = thumbnail.getJpegOptions().getExifData();
if (exifData != null) {
    System.out.println("Camera Owner Name: " + exifData.getCameraOwnerName());
    System.out.println("Aperture Value: " + exifData.getApertureValue());
    System.out.println("Orientation: " + exifData.getOrientation());
    System.out.println("Focal Length: " + exifData.getFocalLength());
    System.out.println("Compression: " + exifData.getCompression());
}
```

## Schritt 4: EXIF-Daten ändern
Nachdem Sie die EXIF‑Daten gelesen haben, möchten Sie möglicherweise einige Felder anpassen. So geht's:

```java
if (exifData != null) {
    exifData.setCameraOwnerName("New Camera Owner");
    exifData.setApertureValue(3.5);
    exifData.setOrientation(1);
    exifData.setFocalLength(35.0);
    exifData.setCompression(6);
    thumbnail.getJpegOptions().setExifData(exifData);
}
```

## Schritt 5: Änderungen speichern
Abschließend speichern Sie nach dem Ändern der EXIF‑Daten die Änderungen in einer neuen PSD‑Datei.

```java
try {
    image.save(dataDir + "Modified_Zebras_Serengeti.psd");
} catch (IOException e) {
    e.printStackTrace();
}
```

## Häufige Probleme und Lösungen
- **Fehlende Thumbnail-Ressource** – Einige JPEGs speichern EXIF direkt im Hauptbild‑Header. Wenn die Thumbnail‑Ressource fehlt, verwenden Sie stattdessen `image.getExifData()`.  
- **Große Dateien verursachen OutOfMemoryError** – Stellen Sie sicher, dass die JVM mit ausreichend Heap (`-Xmx2g`) läuft oder verarbeiten Sie das Bild im Streaming‑Modus mit `PsdImage.load(inputStream, loadOptions)`.  
- **Nicht unterstützte Tag-Typen** – Aspose.PSD unterstützt alle Standard‑EXIF‑Tags; benutzerdefinierte Tags können eine manuelle Byte‑Ebene‑Verarbeitung erfordern.

## Häufig gestellte Fragen

**Q: Was sind EXIF-Daten?**  
A: EXIF (Exchangeable Image File Format) Metadaten speichern Kameraeinstellungen, Zeitstempel, GPS‑Koordinaten und andere Informationen, die in JPEG‑ und anderen Bilddateien eingebettet sind.

**Q: Kann ich Aspose.PSD für Java kostenlos nutzen?**  
A: Sie können eine kostenlose Testversion von der [Aspose‑Releases‑Seite](https://releases.aspose.com/) erhalten.

**Q: Ist Aspose.PSD für Java mit allen Java‑Versionen kompatibel?**  
A: Aspose.PSD für Java unterstützt Java SE 7 und höher.

**Q: Wo finde ich weitere Dokumentation zu Aspose.PSD für Java?**  
A: Weitere Details finden Sie in der [Dokumentation](https://reference.aspose.com/psd/java/).

**Q: Wie erhalte ich Support für Aspose.PSD für Java?**  
A: Support erhalten Sie im [Aspose PSD‑Support‑Forum](https://forum.aspose.com/c/psd/34/).

## Fazit
Durch Befolgen dieser Schritte können Sie **java read image metadata** aus jedem JPEG auslesen, die benötigten EXIF‑Felder anpassen und die aktualisierten Daten zurück in die Datei schreiben – alles mit wenigen Zeilen sauberem Java‑Code. Die umfangreiche API von Aspose.PSD macht die Metadaten‑Verarbeitung zuverlässig und performant, sodass Sie sie in Batch‑Verarbeitungspipelines, Foto‑Management‑Tools oder jede Anwendung integrieren können, die mit Bildinformationen arbeiten muss.

---

**Zuletzt aktualisiert:** 2026-10-03  
**Getestet mit:** Aspose.PSD für Java 24.5  
**Autor:** Aspose

## Verwandte Tutorials

- [Spezifische EXIF‑Tag‑Informationen in Java mit Aspose lesen (asp)](/psd/java/java-jpeg-image-processing/read-specific-exif-tags-info-java/)
- [XMP‑Metadaten in PSD‑Dateien mit Aspose.PSD für Java erstellen](/psd/java/image-editing/create-xmp-metadata/)
- [Bildgröße mit Aspose.PSD für Java ändern – Formen zeichnen & grundlegende Bildoperationen](/psd/java/basic-image-operations/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}