---
title: Lesen bestimmter EXIF-Tag-Informationen in Java
linktitle: Lesen bestimmter EXIF-Tag-Informationen in Java
second_title: Aspose.PSD Java API
description: Erfahren Sie in unserem Schritt-für-Schritt-Tutorial, wie Sie mit Aspose.PSD für Java bestimmte EXIF-Tags aus PSD-Bildern lesen. Verbessern Sie Ihre Bildverarbeitungsfähigkeiten.
type: docs
weight: 19
url: /de/java/java-jpeg-image-processing/read-specific-exif-tags-info-java/
---
## Einführung
Möchten Sie in die Welt der PSD-Dateibearbeitung mit Java eintauchen? Wenn Sie wissen möchten, wie Sie bestimmte EXIF-Tags aus PSD-Bildern lesen, sind Sie hier richtig. Dieses Tutorial führt Sie durch den gesamten Prozess mit Aspose.PSD für Java, vom Einrichten Ihrer Umgebung bis zum Extrahieren detaillierter EXIF-Daten. Lassen Sie uns anfangen!
## Voraussetzungen
Bevor wir uns in den Code vertiefen, müssen Sie einige Dinge vorbereitet haben:
1.  Java Development Kit (JDK): Stellen Sie sicher, dass JDK auf Ihrem Computer installiert ist. Sie können es von der[Oracle JDK-Website](https://www.oracle.com/java/technologies/javase-downloads.html).
2.  Aspose.PSD für Java: Laden Sie die Bibliothek herunter von[Hier](https://releases.aspose.com/psd/java/).
3. Integrierte Entwicklungsumgebung (IDE): Eine IDE wie IntelliJ IDEA, Eclipse oder NetBeans erleichtert das Codieren.
4. PSD-Datei: Eine PSD-Datei mit EXIF-Daten. Sie können das in diesem Tutorial bereitgestellte Beispiel oder jede andere PSD-Datei mit EXIF-Tags verwenden.
## Pakete importieren
Zuerst müssen Sie die erforderlichen Aspose.PSD-Pakete in Ihr Java-Projekt importieren. So richten Sie es ein.
```java
import com.aspose.psd.Image;
import com.aspose.psd.exif.JpegExifData;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.resources.Thumbnail4Resource;
import com.aspose.psd.fileformats.psd.resources.ThumbnailResource;
```
## Schritt 1: Laden Sie das PSD-Bild
Zunächst müssen Sie Ihre PSD-Datei in die Anwendung laden. Stellen Sie sicher, dass Ihr Dateipfad korrekt angegeben ist.
```java
String dataDir = "Your Document Directory";
PsdImage image = (PsdImage) Image.load(dataDir + "1280px-Zebras_Serengeti.psd");
```
 In diesem Schritt laden wir die PSD-Datei mit dem`Image.load()` Methode. Die`PsdImage` Die Klasse wird verwendet, um das PSD-Bild darzustellen, und wir konvertieren das geladene Bild in diese Klasse, um auf PSD-spezifische Funktionen zuzugreifen.
## Schritt 2: Über Bildressourcen iterieren
Jetzt müssen wir die Bildressourcen durchlaufen, um die Miniaturansichtsressource zu finden, die normalerweise EXIF-Daten enthält.
```java
for (int i = 0; i < image.getImageResources().length; i++) {
    if (image.getImageResources()[i] instanceof ThumbnailResource || 
        image.getImageResources()[i] instanceof Thumbnail4Resource) {
        // Die weitere Bearbeitung erfolgt hier
    }
}
```
 Wir durchlaufen die Bildressourcen mit einem`for` Schleife. Ziel ist es, Ressourcen zu identifizieren, die Instanzen von`ThumbnailResource` oder`Thumbnail4Resource`, da diese Typen die EXIF-Daten enthalten.
## Schritt 3: EXIF-Daten extrahieren
Sobald wir die Miniaturbildressource identifiziert haben, extrahieren wir die EXIF-Daten und drucken sie auf der Konsole.
```java
if (image.getImageResources()[i] instanceof ThumbnailResource) {
    JpegExifData exif = ((ThumbnailResource) image.getImageResources()[i]).getJpegOptions().getExifData();
    if (exif != null) {
        System.out.println("Exif WhiteBalance: " + exif.getWhiteBalance());
        System.out.println("Exif PixelXDimension: " + exif.getPixelXDimension());
        System.out.println("Exif PixelYDimension: " + exif.getPixelYDimension());
        System.out.println("Exif ISOSpeed: " + exif.getISOSpeed());
        System.out.println("Exif FocalLength: " + exif.getFocalLength());
    }
}
```
 Wir verwenden ein`if` Anweisung, um zu prüfen, ob die Ressource eine Instanz von`ThumbnailResource` . Wenn ja, dann werfen wir es und holen seine`JpegOptions` für den Zugriff auf die`ExifData`Zum Schluss drucken wir verschiedene EXIF-Tags aus, wie etwa Weißabgleich, Pixelmaße, ISO-Geschwindigkeit und Brennweite.

## Abschluss
Indem Sie diese Schritte befolgen, haben Sie gelernt, wie Sie mit Aspose.PSD für Java bestimmte EXIF-Tags aus einem PSD-Bild lesen. Dieser Prozess umfasst das Laden des Bilds, das Durchlaufen seiner Ressourcen, das Identifizieren der Miniaturansicht-Ressource und das Extrahieren der EXIF-Daten. Mit diesem Wissen können Sie nun EXIF-Daten in Ihren PSD-Dateien untersuchen und bearbeiten und so anspruchsvollere Bildverarbeitungsaufgaben durchführen.
## Häufig gestellte Fragen
### Was sind EXIF-Daten?
EXIF-Daten (Exchangeable Image File Format) sind in Bilddateien eingebettete Metadaten, die Informationen wie Kameraeinstellungen, Datum und Uhrzeit sowie Bildabmessungen enthalten.
### Kann ich EXIF-Daten mit Aspose.PSD bearbeiten?
Ja, mit Aspose.PSD können Sie EXIF-Daten lesen und ändern. Sie können Tags aktualisieren und Änderungen wieder in der Bilddatei speichern.
### Ist Aspose.PSD für Java kostenlos?
 Aspose.PSD bietet eine kostenlose Testversion an, die Sie herunterladen können[Hier](https://releases.aspose.com/). Für den vollen Funktionsumfang müssen Sie eine Lizenz erwerben.
### Welche anderen Formate unterstützt Aspose.PSD?
Aspose.PSD unterstützt verschiedene Adobe Photoshop-Formate, darunter PSD, PSB und mehr. Es bietet auch Optionen zum Konvertieren dieser Formate in andere wie PNG, JPEG, TIFF usw.
### Wie erhalte ich Unterstützung für Aspose.PSD?
 Sie können Unterstützung über Aspose.PSD erhalten.[Forum](https://forum.aspose.com/c/psd/34).