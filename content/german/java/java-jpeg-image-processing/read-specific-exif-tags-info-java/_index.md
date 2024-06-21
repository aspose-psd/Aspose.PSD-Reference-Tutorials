---
title: Lesen Sie spezifische EXIF-Tags-Informationen in Java
linktitle: Lesen Sie spezifische EXIF-Tags-Informationen in Java
second_title: Aspose.PSD Java-API
description: Erfahren Sie in unserem Schritt-für-Schritt-Tutorial, wie Sie mit Aspose.PSD für Java bestimmte EXIF-Tags aus PSD-Bildern lesen. Verbessern Sie Ihre Bildverarbeitungsfähigkeiten.
type: docs
weight: 19
url: /de/java/java-jpeg-image-processing/read-specific-exif-tags-info-java/
---
## Einführung
Möchten Sie in die Welt der PSD-Dateibearbeitung mit Java eintauchen? Wenn Sie verstehen möchten, wie man bestimmte EXIF-Tags aus PSD-Bildern liest, sind Sie hier richtig. Dieses Tutorial führt Sie durch den gesamten Prozess mit Aspose.PSD für Java, von der Einrichtung Ihrer Umgebung bis zum Extrahieren detaillierter EXIF-Daten. Lass uns anfangen!
## Voraussetzungen
Bevor wir uns mit dem Code befassen, müssen Sie einige Dinge bereithalten:
1.  Java Development Kit (JDK): Stellen Sie sicher, dass JDK auf Ihrem Computer installiert ist. Sie können es hier herunterladen[Oracle JDK-Website](https://www.oracle.com/java/technologies/javase-downloads.html).
2.  Aspose.PSD für Java: Laden Sie die Bibliothek herunter von[Hier](https://releases.aspose.com/psd/java/).
3. Integrierte Entwicklungsumgebung (IDE): Eine IDE wie IntelliJ IDEA, Eclipse oder NetBeans erleichtert das Codieren.
4. PSD-Datei: Eine PSD-Datei mit EXIF-Daten. Sie können das in diesem Tutorial bereitgestellte Beispiel oder jede andere PSD-Datei mit EXIF-Tags verwenden.
## Pakete importieren
Zunächst müssen Sie die erforderlichen Aspose.PSD-Pakete in Ihr Java-Projekt importieren. So richten Sie es ein.
```java
import com.aspose.psd.Image;
import com.aspose.psd.examples.Utils.Utils;
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
 In diesem Schritt laden wir die PSD-Datei mit`Image.load()` Methode. Der`PsdImage` Die Klasse wird verwendet, um das PSD-Bild darzustellen, und wir wandeln das geladene Bild in diese Klasse um, um auf PSD-spezifische Funktionen zuzugreifen.
## Schritt 2: Durchlaufen Sie Bildressourcen
Jetzt müssen wir die Bildressourcen durchlaufen, um die Miniaturbildressource zu finden, die normalerweise EXIF-Daten enthält.
```java
for (int i = 0; i < image.getImageResources().length; i++) {
    if (image.getImageResources()[i] instanceof ThumbnailResource || 
        image.getImageResources()[i] instanceof Thumbnail4Resource) {
        // Die weitere Bearbeitung erfolgt hier
    }
}
```
 Wir durchlaufen die Bildressourcen mithilfe von a`for` Schleife. Das Ziel besteht darin, Ressourcen zu identifizieren, die Instanzen von sind`ThumbnailResource` oder`Thumbnail4Resource`, da dies die Typen sind, die die EXIF-Daten enthalten.
## Schritt 3: EXIF-Daten extrahieren
Sobald wir die Miniaturbildressource identifiziert haben, extrahieren wir die EXIF-Daten und drucken sie auf der Konsole aus.
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
 Wir verwenden ein`if` Anweisung, um zu überprüfen, ob die Ressource eine Instanz von ist`ThumbnailResource` . Wenn ja, werfen wir es um und rufen es ab`JpegOptions` um auf die zuzugreifen`ExifData`Abschließend drucken wir verschiedene EXIF-Tags wie WhiteBalance, Pixel Dimensions, ISOSpeed und FocalLength aus.

## Abschluss
Durch Befolgen dieser Schritte haben Sie gelernt, wie Sie mit Aspose.PSD für Java bestimmte EXIF-Tags aus einem PSD-Bild lesen. Dieser Prozess umfasst das Laden des Bildes, das Durchlaufen seiner Ressourcen, das Identifizieren der Miniaturbildressource und das Extrahieren der EXIF-Daten. Mit diesem Wissen können Sie nun EXIF-Daten in Ihren PSD-Dateien untersuchen und bearbeiten und so anspruchsvollere Bildverarbeitungsaufgaben ermöglichen.
## FAQs
### Was sind EXIF-Daten?
EXIF-Daten (Exchangeable Image File Format) sind in Bilddateien eingebettete Metadaten, die Informationen wie Kameraeinstellungen, Datum und Uhrzeit sowie Bildabmessungen enthalten.
### Kann ich EXIF-Daten mit Aspose.PSD bearbeiten?
Ja, mit Aspose.PSD können Sie EXIF-Daten lesen und ändern. Sie können Tags aktualisieren und Änderungen wieder in der Bilddatei speichern.
### Ist Aspose.PSD für Java kostenlos?
 Aspose.PSD bietet eine kostenlose Testversion, die Sie herunterladen können[Hier](https://releases.aspose.com/). Für alle Funktionen müssen Sie eine Lizenz erwerben.
### Welche anderen Formate unterstützt Aspose.PSD?
Aspose.PSD unterstützt verschiedene Adobe Photoshop-Formate, darunter PSD, PSB und mehr. Es bietet auch Optionen zum Konvertieren dieser Formate in andere wie PNG, JPEG, TIFF usw.
### Wie erhalte ich Unterstützung für Aspose.PSD?
 Unterstützung erhalten Sie über Aspose.PSD[Forum](https://forum.aspose.com/c/psd/34).