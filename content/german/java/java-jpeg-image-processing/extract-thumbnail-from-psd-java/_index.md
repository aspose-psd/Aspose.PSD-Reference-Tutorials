---
title: Extrahieren Sie ein Miniaturbild aus PSD in Java
linktitle: Extrahieren Sie ein Miniaturbild aus PSD in Java
second_title: Aspose.PSD Java API
description: Erfahren Sie, wie Sie mit Aspose.PSD für Java Miniaturansichten aus PSD-Dateien extrahieren. Diese Schritt-für-Schritt-Anleitung deckt alles ab, von der Einrichtung bis zum Speichern extrahierter Bilder.
type: docs
weight: 15
url: /de/java/java-jpeg-image-processing/extract-thumbnail-from-psd-java/
---
## Einführung
In diesem Tutorial erfahren Sie, wie Sie mit Aspose.PSD für Java Miniaturansichten aus PSD-Dateien extrahieren. Miniaturansichten können für eine schnelle Vorschau oder zum Erstellen kleinerer Versionen von Bildern nützlich sein, die in PSD-Dokumente eingebettet sind. Lassen Sie uns einen Blick auf die Schritte werfen, die erforderlich sind, um dies mit Aspose.PSD zu erreichen.
## Voraussetzungen
Bevor wir beginnen, stellen Sie sicher, dass Sie Folgendes eingerichtet haben:
- Auf Ihrem System ist Java Development Kit (JDK) installiert.
-  Aspose.PSD für Java-Bibliothek. Sie können es herunterladen von[Hier](https://releases.aspose.com/psd/java/).
- Grundkenntnisse der Java-Programmierung.
## Pakete importieren
Um zu beginnen, fügen Sie das erforderliche Aspose.PSD-Paket in Ihre Java-Klasse ein:
```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.resources.Thumbnail4Resource;
import com.aspose.psd.fileformats.psd.resources.ThumbnailResource;
import com.aspose.psd.imageoptions.JpegOptions;
```
## Schritt 1: Laden Sie die PSD-Datei
Laden Sie zunächst die PSD-Datei, die das Miniaturbild enthält, das Sie extrahieren möchten.
```java
String dataDir = "Your_Document_Directory/";
PsdImage image = (PsdImage)Image.load(dataDir + "your_file.psd");
```
 Ersetzen`"Your_Document_Directory/"` mit dem Verzeichnispfad, in dem sich Ihre PSD-Datei befindet, und`"your_file.psd"` durch den Namen Ihrer PSD-Datei.
## Schritt 2: Über Bildressourcen iterieren
Durchsuchen Sie die Bildressourcen, um die Miniaturansichtsressource zu finden.
```java
for (int i = 0; i < image.getImageResources().length; i++) {
    if (image.getImageResources()[i] instanceof ThumbnailResource) {
        ThumbnailResource thumbnail = (ThumbnailResource) image.getImageResources()[i];
        
        // Extrahieren von Miniaturbilddaten
        int[] data = thumbnail.getThumbnailArgb32Data();
        
        // Erstellen Sie ein neues Bild mit den extrahierten Miniaturbilddaten
        PsdImage extractedThumbnailImage = new PsdImage(thumbnail.getWidth(), thumbnail.getHeight());
        extractedThumbnailImage.saveArgb32Pixels(extractedThumbnailImage.getBounds(), data);
        
        // Speichern Sie das extrahierte Miniaturbild als separate JPEG-Datei
        extractedThumbnailImage.save(dataDir + "extracted_thumbnail.jpg", new JpegOptions());
        
        // Erfolgsmeldung ausgeben
        System.out.println("Thumbnail extracted and saved successfully.");
        
        break; // Verlassen Sie die Schleife, sobald das Miniaturbild gefunden und verarbeitet wurde
    }
}
```
## Schritt 3: Extrahiertes Miniaturbild speichern
Speichern Sie das extrahierte Miniaturbild als separate Bilddatei (in diesem Fall als JPEG-Datei).
## Schritt 4: Umgang mit verschiedenen Miniaturbildtypen
 Wenn Ihre PSD-Datei mehrere Arten von Miniaturansichten enthalten kann, wie zum Beispiel`Thumbnail4Resource`können Sie die Logik erweitern, um diese Fälle ähnlich zu behandeln.

## Abschluss
In diesem Tutorial haben wir untersucht, wie Sie mit Aspose.PSD für Java Miniaturansichten aus PSD-Dateien extrahieren. Indem Sie die oben beschriebenen Schritte befolgen, können Sie in Ihren PSD-Dokumenten eingebettete Miniaturansichten effizient abrufen und speichern.

## Häufig gestellte Fragen
### Was ist Aspose.PSD?
Aspose.PSD ist eine Java-Bibliothek, die es Entwicklern ermöglicht, programmgesteuert mit PSD und anderen Bilddateiformaten zu arbeiten.
### Wo finde ich weitere Dokumentation zu Aspose.PSD für Java?
 Weitere Informationen finden Sie im[Dokumentation](https://reference.aspose.com/psd/java/) für detaillierte API-Referenzen und Beispiele.
### Kann ich Aspose.PSD vor dem Kauf kostenlos testen?
 Ja, Sie können ein[Kostenlose Testversion](https://releases.aspose.com/) um die Fähigkeiten der Bibliothek zu bewerten.
### Wie kann ich temporäre Lizenzen für Aspose.PSD erhalten?
 Temporäre Lizenzen erhalten Sie bei[Hier](https://purchase.aspose.com/temporary-license/).
### Ist Aspose.PSD für die kommerzielle Nutzung geeignet?
Ja, Aspose.PSD kann gemäß seinen Lizenzbedingungen sowohl für persönliche als auch für kommerzielle Projekte verwendet werden.