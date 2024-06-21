---
title: Automatische Korrektur der JPEG-Bildausrichtung in Java
linktitle: Automatische Korrektur der JPEG-Bildausrichtung in Java
second_title: Aspose.PSD Java-API
description: Erfahren Sie, wie Sie die Ausrichtung von JPEG-Bildern in Java mithilfe von Aspose.PSD automatisch korrigieren. Verbessern Sie mühelos Ihre Bildverarbeitungsfähigkeiten.
type: docs
weight: 12
url: /de/java/java-jpeg-image-processing/auto-correct-jpeg-image-orientation-java/
---
## Einführung
Im heutigen digitalen Zeitalter ist die programmgesteuerte Bearbeitung und Optimierung von Bildern zu einer entscheidenden Aufgabe für Entwickler in verschiedenen Bereichen geworden. Aspose.PSD für Java stellt Entwicklern robuste Tools zur effizienten Verarbeitung von PSD-, JPEG- und anderen Bildformaten zur Verfügung. Dieses Tutorial befasst sich mit einer bestimmten Aufgabe: der automatischen Korrektur der JPEG-Bildausrichtung mithilfe von Aspose.PSD für Java. Ganz gleich, ob Sie eine Fotobearbeitungs-App erstellen, Bildressourcen in einem Content-Management-System verwalten oder Bildverarbeitungs-Workflows automatisieren, dieser Leitfaden vermittelt Ihnen das nötige Wissen, um diese Funktionalität nahtlos in Ihre Java-Anwendungen zu integrieren.
## Voraussetzungen
Bevor Sie mit diesem Tutorial beginnen, stellen Sie sicher, dass die folgenden Voraussetzungen erfüllt sind:
- Java-Entwicklungsumgebung: Stellen Sie sicher, dass auf Ihrem System das Java Development Kit (JDK) installiert ist.
-  Aspose.PSD für Java JAR: Laden Sie die Aspose.PSD für Java-Bibliothek von herunter[Hier](https://releases.aspose.com/psd/java/).
- Integrierte Entwicklungsumgebung (IDE): Verwenden Sie IntelliJ IDEA, Eclipse oder eine beliebige IDE Ihrer Wahl für die Java-Entwicklung.
- Grundlegendes Verständnis von Java und Bildverarbeitung: Vertrautheit mit der Java-Programmierung und grundlegenden Konzepten der Bildverarbeitung ist von Vorteil.

## Pakete importieren
Bevor Sie mit dem Beispiel beginnen, stellen Sie sicher, dass Sie die erforderlichen Pakete aus Aspose.PSD für Java importieren:
```java
import com.aspose.psd.Image;
import com.aspose.psd.examples.Utils.Utils;
import com.aspose.psd.exif.JpegExifData;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.resources.Thumbnail4Resource;
import com.aspose.psd.fileformats.psd.resources.ThumbnailResource;
```
## Schritt 1: Laden Sie das PSD-Bild
Laden Sie zunächst das PSD-Bild, das die JPEG-Miniaturansicht enthält, deren Ausrichtung korrigiert werden muss:
```java
String dataDir = "Your Document Directory";
PsdImage image = (PsdImage)Image.load(dataDir + "1280px-Zebras_Serengeti.psd");
```
 Ersetzen`"Your Document Directory"` mit dem tatsächlichen Verzeichnispfad, in dem sich Ihre PSD-Datei befindet.
## Schritt 2: Durchlaufen Sie Bildressourcen
Durchlaufen Sie als Nächstes die Bildressourcen, um die JPEG-Miniaturansichtsressource zu finden:
```java
for (int i = 0; i < image.getImageResources().length; i++) {
    // Miniaturansicht-Ressource finden. Normalerweise liegen sie im JPEG-Dateiformat vor.
    if (image.getImageResources()[i] instanceof ThumbnailResource || image.getImageResources()[i] instanceof Thumbnail4Resource) {
        // Miniaturbilddaten anpassen.
        ThumbnailResource thumbnail = (ThumbnailResource) image.getImageResources()[i];
        JpegExifData exifData = thumbnail.getJpegOptions().getExifData();
        if (exifData != null && exifData.getThumbnail() != null) {
            // Wenn ein Miniaturbild gespeichert ist, drehen Sie es automatisch.
            PsdImage jpegImage = (PsdImage) exifData.getThumbnail();
            if (jpegImage != null) {
                jpegImage.autoRotate();
            }
        }
    }
}
```
## Schritt 3: Speichern Sie das Bild
Speichern Sie abschließend das korrigierte Bild, nachdem Sie die automatische Drehung angewendet haben:
```java
image.save();
```
Dieser Schritt stellt sicher, dass die am Bild vorgenommenen Änderungen beibehalten werden.

## Abschluss
Zusammenfassend lässt sich sagen, dass die Verwendung von Aspose.PSD für Java eine leistungsstarke Lösung zur automatischen Korrektur von JPEG-Bildausrichtungen in PSD-Dateien bietet. Durch Befolgen der in diesem Tutorial beschriebenen Schritte können Entwickler ihre Bildverarbeitungsabläufe verbessern und sicherstellen, dass Bilder auf verschiedenen Plattformen und Geräten korrekt angezeigt werden.
## FAQs
### Was ist Aspose.PSD für Java?
Aspose.PSD für Java ist eine leistungsstarke Bibliothek, die es Java-Entwicklern ermöglicht, programmgesteuert mit PSD, JPEG und anderen Bildformaten zu arbeiten.
### Wie kann ich Aspose.PSD für Java herunterladen?
 Sie können die Bibliothek herunterladen unter[Hier](https://releases.aspose.com/psd/java/).
### Unterstützt Aspose.PSD für Java die Bildmanipulation?
Ja, es unterstützt verschiedene Bildbearbeitungsaufgaben wie Größenänderung, Zuschneiden und Anpassen der Ausrichtung.
### Wo finde ich Dokumentation für Aspose.PSD für Java?
 Eine umfassende Dokumentation ist vorhanden[Hier](https://reference.aspose.com/psd/java/).
### Kann ich Aspose.PSD für Java kostenlos testen?
 Ja, Sie können eine kostenlose Testversion von erhalten[Hier](https://releases.aspose.com/).