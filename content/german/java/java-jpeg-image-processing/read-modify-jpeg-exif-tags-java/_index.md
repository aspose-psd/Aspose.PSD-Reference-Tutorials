---
title: Lesen und ändern Sie JPEG-EXIF-Tags in Java
linktitle: Lesen und ändern Sie JPEG-EXIF-Tags in Java
second_title: Aspose.PSD Java-API
description: Erfahren Sie in dieser Schritt-für-Schritt-Anleitung, wie Sie JPEG-EXIF-Tags mit Aspose.PSD für Java lesen und ändern. Perfekt für Entwickler, die Bildmetadaten mühelos verarbeiten möchten.
type: docs
weight: 18
url: /de/java/java-jpeg-image-processing/read-modify-jpeg-exif-tags-java/
---
## Einführung
Hallo! Haben Sie sich jemals gefragt, wie Sie JPEG-EXIF-Tags mit Java lesen und ändern können? Dann sind Sie hier genau richtig! Dieses Tutorial führt Sie Schritt für Schritt durch den Prozess mit Aspose.PSD für Java. Unabhängig davon, ob Sie ein erfahrener Entwickler oder ein Neuling sind, werden Sie am Ende dieses Handbuchs in der Lage sein, mit JPEG-EXIF-Tags wie ein Profi umzugehen. Also, lasst uns eintauchen!
## Voraussetzungen
Bevor wir beginnen, stellen Sie sicher, dass Sie über Folgendes verfügen:
1.  Java Development Kit (JDK): Stellen Sie sicher, dass JDK auf Ihrem System installiert ist. Sie können es hier herunterladen[Oracle-Website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).
2.  Aspose.PSD für Java-Bibliothek: Sie müssen die Aspose.PSD für Java-Bibliothek herunterladen. Holen Sie es sich von der[Aspose-Veröffentlichungsseite](https://releases.aspose.com/psd/java/).
3. Integrierte Entwicklungsumgebung (IDE): Eine IDE wie IntelliJ IDEA oder Eclipse sorgt für ein reibungsloseres Programmiererlebnis.
4. Grundlegende Java-Kenntnisse: Um diesem Tutorial folgen zu können, sind grundlegende Java-Kenntnisse erforderlich.
## Pakete importieren
Das Wichtigste zuerst: Importieren wir die notwendigen Pakete. Öffnen Sie Ihre Java-IDE und erstellen Sie ein neues Java-Projekt. Fügen Sie dann die Aspose.PSD für Java-Bibliothek in Ihre Projektabhängigkeiten ein.
```java
import com.aspose.psd.Image;
import com.aspose.psd.examples.Utils.Utils;
import com.aspose.psd.exif.JpegExifData;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.resources.Thumbnail4Resource;
import com.aspose.psd.fileformats.psd.resources.ThumbnailResource;
```
## Schritt 1: Laden Sie das PSD-Bild
In diesem Schritt laden wir das PSD-Bild, aus dem wir die EXIF-Daten lesen möchten. Stellen Sie sicher, dass sich Ihr Bild im richtigen Verzeichnis befindet.
```java
String dataDir = "Your Document Directory";
PsdImage image = null;
try {
    image = (PsdImage) Image.load(dataDir + "1280px-Zebras_Serengeti.psd");
} catch (IOException e) {
    e.printStackTrace();
}
```
## Schritt 2: Durchlaufen Sie Bildressourcen
Sobald das Bild geladen ist, besteht der nächste Schritt darin, seine Ressourcen zu durchlaufen, um die Miniaturbildressource zu finden, die normalerweise die EXIF-Daten enthält.
```java
for (int i = 0; i < image.getImageResources().length; i++) {
    if (image.getImageResources()[i] instanceof ThumbnailResource) {
        ThumbnailResource thumbnail = (ThumbnailResource) image.getImageResources()[i];
        // Fahren Sie mit dem nächsten Schritt fort
    }
}
```
## Schritt 3: EXIF-Daten extrahieren
Da wir nun über die Miniaturansichtsressource verfügen, können wir die EXIF-Daten daraus extrahieren. EXIF-Daten enthalten wertvolle Informationen wie den Namen des Kamerabesitzers, den Blendenwert, die Ausrichtung und mehr.
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
Nachdem Sie die EXIF-Daten gelesen haben, möchten Sie möglicherweise einige ihrer Felder ändern. So können Sie es machen:
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
## Schritt 5: Speichern Sie die Änderungen
Speichern Sie abschließend nach der Änderung der EXIF-Daten die Änderungen in einer neuen PSD-Datei.
```java
try {
    image.save(dataDir + "Modified_Zebras_Serengeti.psd");
} catch (IOException e) {
    e.printStackTrace();
}
```

## Abschluss
Und da haben Sie es! Wenn Sie diese Schritte befolgen, können Sie JPEG-EXIF-Tags mit Aspose.PSD für Java problemlos lesen und ändern. Diese leistungsstarke Bibliothek macht den Umgang mit Bildmetadaten zum Kinderspiel. Probieren Sie es also bei Ihren eigenen Projekten aus. Viel Spaß beim Codieren!
## FAQs
### Was sind EXIF-Daten?
EXIF-Daten (Exchangeable Image File Format) enthalten Metadaten zu einem Bild, wie z. B. Kameraeinstellungen und Ausrichtung.
### Kann ich Aspose.PSD für Java kostenlos nutzen?
 Sie können eine kostenlose Testversion von erhalten[Aspose-Veröffentlichungsseite](https://releases.aspose.com/).
### Ist Aspose.PSD für Java mit allen Java-Versionen kompatibel?
Aspose.PSD für Java unterstützt Java SE 7 und höher.
### Wo finde ich weitere Dokumentation zu Aspose.PSD für Java?
 Besuche die[Dokumentation](https://reference.aspose.com/psd/java/) für mehr Details.
### Wie erhalte ich Unterstützung für Aspose.PSD für Java?
 Unterstützung erhalten Sie von der[Aspose PSD-Supportforum](https://forum.aspose.com/c/psd/34).