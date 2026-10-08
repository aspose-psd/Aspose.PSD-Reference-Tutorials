---
date: 2026-10-08
description: Erfahren Sie, wie Sie EXIF-Tags in Java mit Aspose.PSD for Java (asp)
  in unserem Schritt‑für‑Schritt‑Tutorial lesen und Ihre Bildverarbeitungsfähigkeiten
  erweitern.
keywords:
- read exif tags java
- java exif tag extraction
- java image metadata extraction
lastmod: 2026-10-08
linktitle: Spezifische EXIF-Tag-Informationen in Java lesen
og_description: Lesen Sie EXIF-Tags – Java‑Entwickler können Bild-Metadaten schnell
  mit Aspose.PSD extrahieren. Diese Anleitung führt Sie durch das Laden einer PSD,
  das Auffinden von Thumbnail‑Ressourcen und das Ausgeben wichtiger EXIF‑Felder wie
  WhiteBalance und ISO speed.
og_image_alt: Guide showing how to read EXIF tags from PSD files in Java using Aspose.PSD
og_title: Wie man EXIF-Tags in Java mit Aspose.PSD liest
schemas:
- author: Aspose
  dateModified: '2026-10-08'
  description: Learn how to read EXIF tags in Java using Aspose.PSD for Java (asp)
    with our step‑by‑step tutorial, and boost your image processing capabilities.
  headline: How to read EXIF tags in Java with Aspose.PSD
  type: TechArticle
- description: Learn how to read EXIF tags in Java using Aspose.PSD for Java (asp)
    with our step‑by‑step tutorial, and boost your image processing capabilities.
  name: How to read EXIF tags in Java with Aspose.PSD
  steps:
  - name: 'Java Development Kit (JDK): Ensure you have JDK installed on your machine.
      You can download it from the [Oracle JDK website](https://www.oracle.com/java/technologies/javase-downloads.html).'
    text: 'Java Development Kit (JDK): Ensure you have JDK installed on your machine.
      You can download it from the [Oracle JDK website](https://www.oracle.com/java/technologies/javase-downloads.html).'
  - name: 'Aspose.PSD for Java: Download the library from the [Aspose.PSD for Java
      download page](https://releases.aspose.com/psd/java/).'
    text: 'Aspose.PSD for Java: Download the library from the [Aspose.PSD for Java
      download page](https://releases.aspose.com/psd/java/).'
  - name: 'Integrated Development Environment (IDE): An IDE like IntelliJ IDEA, Eclipse,
      or NetBeans will make coding more convenient.'
    text: 'Integrated Development Environment (IDE): An IDE like IntelliJ IDEA, Eclipse,
      or NetBeans will make coding more convenient.'
  - name: 'PSD file: A PSD file with EXIF data. You can use the sample provided in
      this tutorial or any other PSD file with EXIF tags.'
    text: 'PSD file: A PSD file with EXIF data. You can use the sample provided in
      this tutorial or any other PSD file with EXIF tags.'
  type: HowTo
- questions:
  - answer: Aspose.PSD (asp)
    question: What library reads EXIF data from PSD in Java?
  - answer: WhiteBalance, PixelXDimension, PixelYDimension, ISOSpeed, FocalLength,
      and more.
    question: Which tags can be extracted?
  - answer: Yes, a commercial license is required; a free trial is available.
    question: Do I need a license for production?
  - answer: The same API supports PNG, JPEG, TIFF via Java image metadata extraction.
    question: Can I use this with other image formats?
  - answer: About 10‑15 minutes for a basic read‑only scenario.
    question: How long does implementation take?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- read exif tags java
- Aspose.PSD
- java image metadata extraction
- EXIF extraction
- PSD processing
title: Wie man EXIF-Tags in Java mit Aspose.PSD liest
url: /de/java/java-jpeg-image-processing/read-specific-exif-tags-info-java/
weight: 19
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Spezifische EXIF-Tag-Informationen in Java mit Aspose (asp)

## Einleitung
Wenn Sie **EXIF-Tags in Java lesen** müssen, bietet Aspose.PSD (asp) eine saubere, reine‑Java‑API, die ohne Photoshop funktioniert. In diesem Tutorial lernen Sie, wie Sie EXIF‑Daten aus einem PSD‑Bild extrahieren, nur die für Sie relevanten Tags auswählen und sie in der Konsole ausgeben. Wir behandeln alles, von der Einrichtung Ihrer Entwicklungsumgebung bis zum Abrufen von Metadaten wie WhiteBalance, ISO‑Geschwindigkeit und Brennweite. Los geht’s!

## Schnelle Antworten
- **Welche Bibliothek liest EXIF‑Daten aus PSD in Java?** Aspose.PSD (asp)  
- **Welche Tags können extrahiert werden?** WhiteBalance, PixelXDimension, PixelYDimension, ISOSpeed, FocalLength und mehr.  
- **Benötige ich eine Lizenz für die Produktion?** Ja, eine kommerzielle Lizenz ist erforderlich; ein kostenloser Testzeitraum ist verfügbar.  
- **Kann ich das mit anderen Bildformaten verwenden?** Die gleiche API unterstützt PNG, JPEG, TIFF über die Java‑Bild‑Metadaten‑Extraktion.  
- **Wie lange dauert die Implementierung?** Etwa 10‑15 Minuten für ein einfaches Nur‑Lese‑Szenario.

## Was ist asp (Aspose.PSD für Java)?
Aspose.PSD für Java ist eine reine‑Java‑Bibliothek, die Entwicklern ermöglicht, mit Adobe‑Photoshop‑Dateien (PSD, PSB) zu arbeiten, ohne Photoshop zu installieren. Sie bietet programmatischen Zugriff auf Ebenen, Ressourcen und Metadaten – einschließlich EXIF‑Tags – und ist damit ideal für **java image metadata extraction**‑Aufgaben.

## Warum Aspose.PSD (asp) für die EXIF‑Extraktion verwenden?
Sie können EXIF‑Tags in Java mit nur zwei Methodenaufrufen extrahieren, und die Bibliothek verarbeitet Dateien bis zu 2 GB, ohne das gesamte Dokument in den Speicher zu laden. Sie unterstützt **30+ image formats** und bewahrt die genauen Kameraeinstellungen, sodass Sie deterministische Ergebnisse unter Windows, Linux und macOS erhalten.

## Voraussetzungen
Bevor wir in den Code eintauchen, gibt es einige Dinge, die Sie bereitstellen müssen:

1. Java Development Kit (JDK): Stellen Sie sicher, dass das JDK auf Ihrem Rechner installiert ist. Sie können es von der [Oracle JDK-Website](https://www.oracle.com/java/technologies/javase-downloads.html) herunterladen.  
2. Aspose.PSD für Java: Laden Sie die Bibliothek von der [Aspose.PSD für Java Download‑Seite](https://releases.aspose.com/psd/java/) herunter.  
3. Integrierte Entwicklungsumgebung (IDE): Eine IDE wie IntelliJ IDEA, Eclipse oder NetBeans erleichtert das Programmieren.  
4. PSD‑Datei: Eine PSD‑Datei mit EXIF‑Daten. Sie können das in diesem Tutorial bereitgestellte Beispiel verwenden oder jede andere PSD‑Datei mit EXIF‑Tags.

## Pakete importieren
Importieren Sie die erforderlichen Aspose.PSD‑Klassen wie Image, PsdImage, ThumbnailResource und JpegExifData, um mit PSD‑Dateien zu arbeiten.  
```java
import com.aspose.psd.Image;
import com.aspose.psd.exif.JpegExifData;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.resources.Thumbnail4Resource;
import com.aspose.psd.fileformats.psd.resources.ThumbnailResource;
```

## Schritt 1: PSD‑Bild laden
`Image.load()` lädt eine Datei und gibt ein Image‑Objekt zurück, das die Bilddaten repräsentiert.  
`PsdImage` ist die Aspose.PSD‑Klasse, die PSD‑spezifische Funktionalität bereitstellt.  
Die Methode `Image.load()` lädt jede unterstützte Bilddatei in den Speicher und gibt ein generisches `Image`‑Objekt zurück, das Sie in einen PSD‑spezifischen Typ umwandeln können.  
```java
String dataDir = "Your Document Directory";
PsdImage image = (PsdImage) Image.load(dataDir + "1280px-Zebras_Serengeti.psd");
```

In diesem Schritt laden wir die PSD‑Datei mit der Methode `Image.load()`. Die Klasse `PsdImage` wird verwendet, um das PSD‑Bild darzustellen, und wir casten das geladene Bild in diese Klasse, um PSD‑spezifische Funktionalitäten zu nutzen.

## Schritt 2: Bildressourcen durchlaufen
`PsdImage.getResources()` gibt eine Sammlung eingebetteter Ressourcen zurück, wie Thumbnails und EXIF‑Daten.  
Der Aufruf `PsdImage.getResources()` liefert eine Sammlung aller eingebetteten Ressourcen. Durch das Durchlaufen dieser Sammlung können Sie Thumbnail‑Ressourcen finden, die EXIF‑Metadaten enthalten.  
```java
for (int i = 0; i < image.getImageResources().length; i++) {
    if (image.getImageResources()[i] instanceof ThumbnailResource || 
        image.getImageResources()[i] instanceof Thumbnail4Resource) {
        // Further processing will be done here
    }
}
```

Wir durchlaufen die Bildressourcen mit einer `for`‑Schleife. Ziel ist es, Ressourcen zu identifizieren, die Instanzen von `ThumbnailResource` oder `Thumbnail4Resource` sind, da diese Typen die EXIF‑Daten enthalten.

## Schritt 3: EXIF‑Daten extrahieren
`ThumbnailResource.getJpegOptions()` bietet Zugriff auf JPEG‑Optionen einschließlich EXIF‑Metadaten.  
`JpegExifData` enthält einzelne EXIF‑Tag‑Werte.  
Die Methode `ThumbnailResource.getJpegOptions()` liefert Zugriff auf ein `JpegExifData`‑Objekt, das einzelne EXIF‑Tags wie WhiteBalance, ISOSpeed und FocalLength enthält.  
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

Wir verwenden eine `if`‑Anweisung, um zu prüfen, ob die Ressource eine Instanz von `ThumbnailResource` ist. Ist dies der Fall, casten wir sie und rufen ihre `JpegOptions` ab, um auf die `ExifData` zuzugreifen. Abschließend geben wir verschiedene EXIF‑Tags wie WhiteBalance, Pixel‑Dimensionen, ISOSpeed und FocalLength aus.

## Häufige Probleme & Tipps
- **Null EXIF-Daten:** Einige PSD‑Dateien enthalten möglicherweise keine Thumbnail‑Ressource mit EXIF‑Informationen. Prüfen Sie immer auf `null`, bevor Sie Tag‑Werte abrufen.  
- **Dateipfad‑Fehler:** Verwenden Sie absolute Pfade oder stellen Sie sicher, dass das Arbeitsverzeichnis auf den Ordner mit Ihrer PSD‑Datei zeigt.  
- **Lizenzbeschränkungen:** Die kostenlose Testversion begrenzt die Anzahl der Seiten, die Sie verarbeiten können; ein Upgrade auf eine Voll‑Lizenz ermöglicht uneingeschränkte Nutzung.

## Häufig gestellte Fragen

### Was sind EXIF‑Daten?
EXIF (Exchangeable Image File Format)‑Daten sind Metadaten, die in Bilddateien eingebettet sind und Informationen wie Kameraeinstellungen, Datum und Uhrzeit sowie Bildabmessungen enthalten.

### Kann ich EXIF‑Daten mit Aspose.PSD bearbeiten?
Ja, Aspose.PSD ermöglicht das Lesen und Ändern von EXIF‑Daten. Sie können Tags aktualisieren und die Änderungen wieder in die Bilddatei speichern.

### Ist Aspose.PSD für Java kostenlos?
Aspose.PSD bietet eine kostenlose Testversion, die Sie von der [Aspose.PSD offiziellen Release‑Seite](https://releases.aspose.com/) herunterladen können. Für den vollen Funktionsumfang müssen Sie eine Lizenz erwerben.

### Welche anderen Formate unterstützt Aspose.PSD?
Aspose.PSD unterstützt verschiedene Adobe‑Photoshop‑Formate, einschließlich PSD, PSB und weitere. Außerdem bietet es Optionen, diese Formate in PNG, JPEG, TIFF usw. zu konvertieren.

### Wie erhalte ich Support für Aspose.PSD?
Sie können Support über das Aspose.PSD‑[Forum](https://forum.aspose.com/c/psd/34) erhalten.

### Wie hilft das bei **java image metadata extraction**?
Durch die Verwendung des `JpegExifData`‑Objekts können Sie programmgesteuert jedes benötigte EXIF‑Tag extrahieren, was eine solide Grundlage für umfassendere Metadaten‑Extraktionsaufgaben über verschiedene Bildformate hinweg bietet.

---

**Zuletzt aktualisiert:** 2026-10-08  
**Getestet mit:** Aspose.PSD für Java 24.11 (aktuell zum Zeitpunkt der Erstellung)  
**Autor:** Aspose

## Verwandte Tutorials

- [JPEG‑EXIF‑Tags in Java lesen und ändern](/psd/java/java-jpeg-image-processing/read-modify-jpeg-exif-tags-java/)
- [Java JPEG‑Bildverarbeitung](/psd/java/java-jpeg-image-processing/)
- [Wie man ein Bild um einen bestimmten Winkel mit Aspose.PSD für Java dreht](/psd/java/advanced-image-manipulation/rotate-image-specific-angle/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}