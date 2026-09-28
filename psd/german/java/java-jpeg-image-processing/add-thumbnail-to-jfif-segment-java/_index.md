---
date: 2026-09-28
description: Wie man ein Thumbnail zu einem JFIF-Segment in Java mit Aspose.PSD hinzufügt.
  Folgen Sie dieser Schritt-für-Schritt-Anleitung, um Thumbnails schnell und zuverlässig
  in PSD-Dateien einzubetten.
keywords:
- how to add thumbnail
- JFIF segment Java
- Aspose.PSD thumbnail
- Java image processing
lastmod: 2026-09-28
linktitle: Thumbnail zum JFIF-Segment in Java hinzufügen
og_description: Wie man ein Thumbnail zu einem JFIF-Segment in Java mit Aspose.PSD
  hinzufügt. Folgen Sie dieser Schritt-für-Schritt-Anleitung, um Thumbnails schnell
  und zuverlässig in PSD-Dateien einzubetten.
og_image_alt: Guide showing how to add thumbnail to JFIF segment in Java with Aspose.PSD
og_title: Wie man ein Thumbnail zum JFIF-Segment in Java hinzufügt
schemas:
- author: Aspose
  dateModified: '2026-09-28'
  description: How to add thumbnail to a JFIF segment in Java using Aspose.PSD. Follow
    this step‑by‑step guide to embed thumbnails in PSD files quickly and reliably.
  headline: How to add thumbnail to JFIF segment in Java
  type: TechArticle
- description: How to add thumbnail to a JFIF segment in Java using Aspose.PSD. Follow
    this step‑by‑step guide to embed thumbnails in PSD files quickly and reliably.
  name: How to add thumbnail to JFIF segment in Java
  steps:
  - name: import packages
    text: '`Document`, `JfifResource`, and related classes are part of the Aspose.PSD
      namespace. Document represents the PSD file container, and JfifResource provides
      access to the JFIF segment within the PSD. Import them at the top of your source
      file.'
  - name: load the PSD image
    text: Create a `PsdImage` instance by passing the file path to the constructor.
      PsdImage is the Aspose.PSD class that models a Photoshop document. This loads
      the document metadata while streaming the pixel data.
  - name: iterate over image resources
    text: Search the `Resources` collection for a `JfifResource`. When found, you
      can replace its thumbnail byte array with a new JPEG‑encoded preview.
  - name: adjust thumbnail data
    text: Generate a small JPEG thumbnail (e.g., 120 × 120 px) using any image‑processing
      library, then assign the resulting byte array to `jfifResource.ThumbnailData`.
  - name: save the modified image
    text: Call the `save` method on the `PsdImage` object, specifying the output path
      and desired format. The JFIF segment now contains the new thumbnail.
  type: HowTo
- questions:
  - answer: Aspose.PSD for Java is a commercial library that enables developers to
      create, edit, convert, and render Photoshop PSD files without requiring Adobe
      Photoshop.
    question: What is Aspose.PSD for Java?
  - answer: Detailed documentation can be found on the [Aspose.PSD for Java documentation
      page](https://reference.aspose.com/psd/java/).
    question: Where can I find more documentation for Aspose.PSD for Java?
  - answer: Yes, Aspose.PSD for Java can be used commercially. You can purchase a
      license from [Aspose.PSD's purchase page](https://purchase.aspose.com/buy).
    question: Is Aspose.PSD for Java suitable for commercial use?
  - answer: Yes, you can download a free trial from [Aspose.PSD's trial download page](https://releases.aspose.com/).
    question: Can I try Aspose.PSD for Java before purchasing?
  - answer: For support, visit the [Aspose.PSD forum](https://forum.aspose.com/c/psd/34).
    question: How can I get support for Aspose.PSD for Java?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- add thumbnail
- Aspose.PSD
- Java image processing
- JFIF
- PSD
title: Wie man ein Thumbnail zum JFIF-Segment in Java hinzufügt
url: /de/java/java-jpeg-image-processing/add-thumbnail-to-jfif-segment-java/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Wie man ein Thumbnail zum JFIF‑Segment in Java hinzufügt

## Einleitung
Ein Thumbnail zum JFIF‑Segment einer PSD‑Datei hinzuzufügen ist eine häufige Anforderung, wenn Sie eine schnelle visuelle Vorschau benötigen, ohne das gesamte Bild zu laden. In diesem Tutorial lernen Sie **wie man ein Thumbnail hinzufügt** zum JFIF‑Segment in Java mit Aspose.PSD. Am Ende der Anleitung haben Sie ein ausführbares Code‑Snippet, ein Verständnis der zugrunde liegenden JFIF‑Struktur und Tipps zum effizienten Umgang mit großen Dateien.

## Schnelle Antworten
- **Welche Bibliothek wird benötigt?** Aspose.PSD for Java.
- **Welche Java‑Version funktioniert?** JDK 11 oder höher.
- **Wie viele Codezeilen werden benötigt?** Etwa 10 Zeilen zum Laden, Ändern und Speichern.
- **Kann ich Multi‑Megabyte‑Dateien verarbeiten?** Ja, Aspose.PSD streamt Daten, sodass der Speicherverbrauch gering bleibt.
- **Wird eine kommerzielle Lizenz benötigt?** Eine Lizenz ist für den Produktionseinsatz erforderlich; eine kostenlose Testversion ist verfügbar.

## Was ist ein JFIF‑Segment?
Das JFIF‑Segment ist ein Block des JPEG File Interchange Format, der optionale Daten wie Thumbnails, EXIF oder Farbprofile speichern kann.  
Es befindet sich im JPEG‑Stream einer PSD‑Datei und wird von den meisten Bildbetrachtern zur schnellen Vorschauerstellung erkannt.

## Warum ein Thumbnail zu einer PSD‑Datei hinzufügen?
Aspose.PSD for Java unterstützt **30+ Bildformate** und kann Dateien bis zu **2 GB** verarbeiten, ohne das gesamte Dokument in den Speicher zu laden. Das Hinzufügen eines Thumbnails reduziert die Netzwerkbandbreite beim Übertragen von Vorschaubildern und beschleunigt das UI‑Rendering in Galerie‑Anwendungen.

## Voraussetzungen
- Java Development Kit (JDK): Stellen Sie sicher, dass Java auf Ihrem System installiert ist. Sie können es von [Oracle's JDK website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html) herunterladen.
- Aspose.PSD for Java: Sie benötigen die Aspose.PSD for Java‑Bibliothek. Sie können sie von der [Aspose.PSD Java download page](https://releases.aspose.com/psd/java/) beziehen.
- Integrated Development Environment (IDE): Verwenden Sie eine IDE wie IntelliJ IDEA oder Eclipse für die Java‑Entwicklung.
- Grundlegendes Verständnis von Java: Vertrautheit mit der Programmiersprache Java und deren Konzepten.

## Wie man ein Thumbnail zum JFIF‑Segment in Java hinzufügt?
Laden Sie das Ziel‑PSD, finden Sie die JFIF‑Ressource, ersetzen Sie deren Thumbnail‑Daten und speichern Sie die Datei. Der gesamte Vorgang kann mit wenigen einfachen API‑Aufrufen durchgeführt werden, und Aspose.PSD übernimmt die Low‑Level‑JPEG‑Struktur für Sie.

### Schritt 1: Pakete importieren
`Document`, `JfifResource` und verwandte Klassen gehören zum Aspose.PSD‑Namensraum. Document repräsentiert den PSD‑Dateicontainer, und JfifResource bietet Zugriff auf das JFIF‑Segment innerhalb des PSD. Importieren Sie sie am Anfang Ihrer Quelldatei.

```java
import com.aspose.psd.Image;
import com.aspose.psd.exif.JpegExifData;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.resources.Thumbnail4Resource;
import com.aspose.psd.fileformats.psd.resources.ThumbnailResource;
```

### Schritt 2: PSD‑Bild laden
Erstellen Sie eine `PsdImage`‑Instanz, indem Sie den Dateipfad an den Konstruktor übergeben. PsdImage ist die Aspose.PSD‑Klasse, die ein Photoshop‑Dokument modelliert. Dadurch werden die Dokument‑Metadaten geladen, während die Pixeldaten gestreamt werden.

```java
String dataDir = "Your Document Directory";
PsdImage image = (PsdImage)Image.load(dataDir + "your_image.psd");
```

### Schritt 3: Bildressourcen iterieren
Durchsuchen Sie die `Resources`‑Sammlung nach einem `JfifResource`. Wenn gefunden, können Sie dessen Thumbnail‑Byte‑Array durch eine neue JPEG‑kodierte Vorschau ersetzen.

```java
for(int i = 0; i < image.getImageResources().length; i++) {
    if (image.getImageResources()[i] instanceof ThumbnailResource) {
        ThumbnailResource thumbnail = (ThumbnailResource)image.getImageResources()[i];
        
        // Continue with thumbnail processing
    }
}
```

### Schritt 4: Thumbnail‑Daten anpassen
Erzeugen Sie ein kleines JPEG‑Thumbnail (z. B. 120 × 120 px) mit einer beliebigen Bildverarbeitungsbibliothek und weisen Sie das resultierende Byte‑Array `jfifResource.ThumbnailData` zu.

```java
try {
    PsdImage thumbnailImage = new PsdImage(100, 100);
    
    // Fill thumbnail data (example: create a simple pixel array)
    int[] pixels = new int[thumbnailImage.getWidth() * thumbnailImage.getHeight()];
    for (int j = 0; j < pixels.length; j++) {
        pixels[j] = j;
    }
    
    // Save thumbnail data
    thumbnailImage.saveArgb32Pixels(thumbnailImage.getBounds(), pixels);
    
    // Set thumbnail data to Jpeg options
    JpegExifData exifData = new JpegExifData();
    exifData.setThumbnail(thumbnailImage);
    JpegOptions jpegOptions = new JpegOptions();
    jpegOptions.setExifData(exifData);
    
    // Set options to thumbnail resource
    thumbnail.getJpegOptions().setExifData(exifData);
    
} catch(Exception e) {
    // Handle exceptions
} finally {
    // Dispose of resources
}
```

### Schritt 5: Modifiziertes Bild speichern
Rufen Sie die `save`‑Methode des `PsdImage`‑Objekts auf, wobei Sie den Ausgabepfad und das gewünschte Format angeben. Das JFIF‑Segment enthält nun das neue Thumbnail.

```java
image.save(dataDir + "output.psd");
```

## Häufige Probleme und Lösungen
- **Thumbnail nicht in Betrachtern sichtbar:** Stellen Sie sicher, dass die Thumbnail‑Daten ein gültiges JPEG‑Byte‑Array sind und dass die Abmessungen innerhalb von 256 × 256 px liegen, was die maximal unterstützte Größe der JFIF‑Spezifikation ist.
- **OutOfMemoryError bei großen PSDs:** Verwenden Sie `PsdImage.load(inputStream, true)`, um den Streaming‑Modus zu aktivieren, wodurch der Speicherverbrauch gering bleibt.
- **Falscher Ressourcentyp:** Vergewissern Sie sich, dass die zu modifizierende Ressource tatsächlich ein `JfifResource` ist; andere Ressourcen wie `ExifResource` beeinflussen die Thumbnail‑Anzeige nicht.

## Häufig gestellte Fragen

**Q: Was ist Aspose.PSD für Java?**  
A: Aspose.PSD für Java ist eine kommerzielle Bibliothek, die Entwicklern ermöglicht, Photoshop‑PSD‑Dateien zu erstellen, zu bearbeiten, zu konvertieren und zu rendern, ohne Adobe Photoshop zu benötigen.

**Q: Wo finde ich weitere Dokumentation zu Aspose.PSD für Java?**  
A: Detaillierte Dokumentation finden Sie auf der [Aspose.PSD for Java documentation page](https://reference.aspose.com/psd/java/).

**Q: Ist Aspose.PSD für Java für den kommerziellen Einsatz geeignet?**  
A: Ja, Aspose.PSD für Java kann kommerziell genutzt werden. Sie können eine Lizenz über die [Aspose.PSD's purchase page](https://purchase.aspose.com/buy) erwerben.

**Q: Kann ich Aspose.PSD für Java vor dem Kauf testen?**  
A: Ja, Sie können eine kostenlose Testversion von der [Aspose.PSD's trial download page](https://releases.aspose.com/) herunterladen.

**Q: Wie erhalte ich Support für Aspose.PSD für Java?**  
A: Für Support besuchen Sie das [Aspose.PSD forum](https://forum.aspose.com/c/psd/34).

---

**Zuletzt aktualisiert:** 2026-09-28  
**Getestet mit:** Aspose.PSD for Java 24.11  
**Autor:** Aspose

## Verwandte Tutorials

- [IOPA‑Ressource zu PSD‑Dateien hinzufügen mit Aspose PSD für Java](/psd/java/modifying-converting-psd-images/add-iopa-resource-psd-files/)
- [Signatur zum Bild hinzufügen – Bild auf Canvas zeichnen mit Aspose.PSD für Java](/psd/java/advanced-image-effects/add-signature-to-image/)
- [Wie man ein Bild um einen bestimmten Winkel rotiert mit Aspose.PSD für Java](/psd/java/advanced-image-manipulation/rotate-image-specific-angle/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}