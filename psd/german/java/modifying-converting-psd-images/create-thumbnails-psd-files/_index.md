---
title: Erstellen Sie Miniaturansichten aus PSD-Dateien mit Java
linktitle: Erstellen Sie Miniaturansichten aus PSD-Dateien mit Java
second_title: Aspose.PSD Java API
description: Erfahren Sie, wie Sie mit Java und Aspose.PSD mühelos Miniaturansichten aus PSD-Dateien erstellen. Folgen Sie unserer Schritt-für-Schritt-Anleitung zur nahtlosen Bildverarbeitung.
weight: 24
url: /de/java/modifying-converting-psd-images/create-thumbnails-psd-files/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Erstellen Sie Miniaturansichten aus PSD-Dateien mit Java

## Einführung
In der Welt des Grafikdesigns ist die Arbeit mit PSD-Dateien (Photoshop Document) alltäglich. Egal, ob Sie ein erfahrener Entwickler, Grafikdesigner oder einfach jemand sind, der in die Bildverarbeitung einsteigen möchte, das Erstellen von Miniaturansichten aus PSD-Dateien kann Ihnen Zeit sparen und Ihren Arbeitsablauf optimieren. Dieses Tutorial führt Sie durch den gesamten Prozess mit Aspose.PSD für Java. Aspose.PSD ist nicht nur eine robuste Bibliothek zum Verwalten von Photoshop-Dateien, sondern macht die anstehende Aufgabe auch intuitiv und überschaubar. Sind Sie bereit zu lernen, wie Sie effizient Miniaturansichten aus PSD-Dateien erstellen?
## Voraussetzungen
Bevor wir uns in die Einzelheiten der Miniaturbild-Erstellung vertiefen, besprechen wir, was Sie für den Anfang benötigen.
### Java-Entwicklungsumgebung
-  Java JDK: Stellen Sie sicher, dass das Java Development Kit (JDK) auf Ihrem Computer installiert ist. Sie können es herunterladen[Hier](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).
- IDE: Eine integrierte Entwicklungsumgebung (IDE) wie IntelliJ IDEA, Eclipse oder NetBeans erleichtert die Codierung.
### Aspose.PSD-Bibliothek
- Sie müssen die Aspose.PSD-Bibliothek in Ihr Projekt einbinden. Sie können[Laden Sie hier die neueste Version herunter](https://releases.aspose.com/psd/java/).
### Grundkenntnisse in Java
- Wenn Sie mit den Java-Grundlagen vertraut sind, können Sie den Beispielcode besser durchgehen. Konzepte wie Klassen, Objekte und Schleifen werden häufig verwendet.
## Pakete importieren
Beginnen Sie mit dem Importieren der erforderlichen Klassen aus der Aspose.PSD-Bibliothek. Dieser Schritt ist entscheidend, da Sie dadurch die Funktionen der Bibliothek in Ihrem Code nutzen können.
```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.resources.ThumbnailFormat;
import com.aspose.psd.fileformats.psd.resources.ThumbnailResource;
```
Nachdem wir die Voraussetzungen geklärt haben, können wir uns nun auf das Wesentliche konzentrieren! Das Erstellen von Miniaturansichten aus PSD-Dateien umfasst ein paar einfache Schritte, und ich werde es Ihnen erklären.
## Schritt 1: Richten Sie Ihre Umgebung ein
So starten Sie Ihr Projekt und bereiten die Miniaturbildgenerierung vor.
1. Erstellen Sie ein Java-Projekt:
   - Öffnen Sie Ihre IDE und erstellen Sie ein neues Java-Projekt.
   - Geben Sie ihm einen Namen wie „PsdThumbnailGenerator“.
2. Aspose.PSD-Bibliothek einbinden:
   -  Fügen Sie die JAR-Datei Aspose.PSD zum Build-Pfad Ihres Projekts hinzu. Wenn Sie Maven verwenden, fügen Sie sie in Ihren`pom.xml`:
     ```xml
     <dependency>
         <groupId>com.aspose</groupId>
         <artifactId>aspose-psd</artifactId>
         <version>your_version_here</version>
     </dependency>
     ```
## Schritt 2: Laden Sie die PSD-Datei
Als nächstes müssen wir die PSD-Datei laden, aus der wir Miniaturansichten erstellen möchten. 
1. Geben Sie Ihr Dokumentverzeichnis an:
   Definieren Sie das Verzeichnis, in dem sich Ihre PSD-Datei befindet.
   ```java
   String dataDir = "Your Document Directory"; // Ersetzen Sie es durch Ihren Pfad.
   ```
2. Laden Sie die PSD-Datei:
    Verwenden Sie die`PsdImage` Klasse, um Ihre PSD-Datei zu laden.
   ```java
   PsdImage image = (PsdImage) Image.load(dataDir + "sample.psd");
   ```
 Hier,`sample.psd` ist der Name Ihrer PSD-Datei. Passen Sie dies entsprechend dem Namen Ihrer Datei an.
## Schritt 3: Über PSD-Ressourcen iterieren
Nachdem wir unser PSD-Bild geladen haben, besteht der nächste Schritt darin, seine Ressourcen zu untersuchen.
1. Ressourcenanzahl abrufen:
   Wir durchlaufen alle Ressourcen in der PSD-Datei.
   ```java
   for (int i = 0; i < image.getImageResources().length; i++) {
       // Verarbeitungsressourcen
   }
   ```
   
2. Miniaturbildressourcen identifizieren:
   Überprüfen Sie innerhalb der Schleife, ob es sich bei einer Ressource um eine Miniaturansicht handelt.
   ```java
   if (image.getImageResources()[i] instanceof ThumbnailResource) {
       // Verarbeiten Sie das Miniaturbild
   }
   ```
## Schritt 4: Bearbeiten Sie das Miniaturbild
Sobald wir eine Miniaturbildressource identifiziert haben, müssen wir sie entsprechend behandeln.
1. Miniaturbildformat abrufen und prüfen:
   Wenn es sich bei der Ressource tatsächlich um eine Miniaturansicht handelt, rufen Sie sie ab und überprüfen Sie ihr Format.
   ```java
   ThumbnailResource thumbnail = (ThumbnailResource) image.getImageResources()[i];
   if (thumbnail.getFormat() == ThumbnailFormat.KJpegRgb) {
       // Erstellen und Speichern des Miniaturbilds
   }
   ```
## Schritt 5: Erstellen und Speichern des Miniaturbilds
Hier geschieht die Magie! Wir erstellen ein neues Bild aus den Miniaturbilddaten und speichern es.
1. Erstellen Sie ein neues Bild:
   Wir verwenden die Breite und Höhe der Miniaturansichtsressource, um ein neues Bitmap-Bild zu erstellen.
   ```java
   PsdImage thumbnailImage = new PsdImage(thumbnail.getWidth(), thumbnail.getHeight());
   ```
2. Pixel im neuen Bild speichern:
   Übertragen Sie die Miniaturbilddaten auf das neu erstellte Bild.
   ```java
   thumbnailImage.savePixels(thumbnailImage.getBounds(), thumbnail.getThumbnailData());
   ```
3. Miniaturbild speichern:
   Speichern Sie abschließend das Miniaturbild unter einem eindeutigen Namen in Ihrem Dokumentverzeichnis.
   ```java
   thumbnailImage.save(dataDir + "CreateThumbnailsFromPSDFiles_out_" + i + ".bmp");
   ```

## Abschluss
Das Erstellen von Miniaturansichten aus PSD-Dateien mit Java und Aspose.PSD kann eine einfache Aufgabe sein, wenn Sie sie in überschaubare Schritte aufteilen. Mit diesem Tutorial können Sie jetzt ganz einfach Miniaturansichten aus Ihren PSD-Dateien extrahieren und erhalten so ein praktisches Tool zur Verbesserung Ihres Workflows. Also, was hält Sie davon ab? Besorgen Sie sich ein paar PSD-Dateien und probieren Sie es aus!
## Häufig gestellte Fragen
### Was ist Aspose.PSD?
Aspose.PSD ist eine Java-Bibliothek, die Entwicklern die Arbeit mit Photoshop-Dateien ermöglicht und die programmgesteuerte Bearbeitung und Verwaltung von PSD-Dateien erleichtert.
### Kann ich Aspose.PSD kostenlos nutzen?
Ja, Aspose bietet eine kostenlose Testversion an, mit der Sie die Bibliothek testen können, bevor Sie eine Lizenz erwerben.
### In welchen Formaten kann ich die Miniaturansichten speichern?
In diesem Beispiel haben wir die Miniaturansichten im BMP-Format gespeichert, aber Aspose.PSD unterstützt auch verschiedene andere Formate.
### Muss Photoshop installiert sein, um Aspose.PSD zu verwenden?
Nein, Aspose.PSD funktioniert unabhängig von Photoshop.
### Wo finde ich weitere Informationen zu Aspose.PSD?
 Sie können sich die[Aspose.PSD-Dokumentation](https://reference.aspose.com/psd/java/) für weitere Details, Tutorials und Ressourcen.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
