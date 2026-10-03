---
date: 2026-10-03
description: Erfahren Sie, wie Sie thumbnail aus PSD in Java mit Aspose.PSD extrahieren.
  Dieser step‑by‑step Leitfaden behandelt setup, code snippets und das Speichern des
  thumbnails als JPEG‑Bild.
keywords:
- extract thumbnail from psd
- java aspose psd
- psd thumbnail extraction
lastmod: 2026-10-03
linktitle: Thumbnail aus PSD in Java extrahieren
og_description: Erfahren Sie, wie Sie thumbnail aus PSD in Java mit Aspose.PSD extrahieren.
  Dieser Leitfaden führt Sie durch setup, loading the file, extracting the thumbnail
  und saving it as a JPEG image.
og_image_alt: Screenshot showing Java code extracting a thumbnail from a PSD file
  using Aspose.PSD
og_title: Thumbnail aus PSD in Java mit Aspose.PSD extrahieren
schemas:
- author: Aspose
  dateModified: '2026-10-03'
  description: Learn how to extract thumbnail from PSD in Java using Aspose.PSD. This
    step‑by‑step guide covers setup, code snippets, and saving the thumbnail as a
    JPEG image.
  headline: Extract thumbnail from PSD in Java
  type: TechArticle
- questions:
  - answer: Aspose.PSD is a Java library that enables programmatic creation, manipulation,
      and conversion of PSD and other raster image formats without requiring Adobe
      Photoshop.
    question: What is Aspose.PSD?
  - answer: You can refer to the [documentation](https://reference.aspose.com/psd/java/)
      for detailed API references and examples.
    question: Where can I find more documentation on Aspose.PSD for Java?
  - answer: Yes, you can download a [free trial](https://releases.aspose.com/) to
      evaluate the library’s capabilities.
    question: Can I try Aspose.PSD for free before purchasing?
  - answer: Temporary licenses are available from the [temporary license](https://purchase.aspose.com/temporary-license/)
      page.
    question: How can I obtain a temporary license for Aspose.PSD?
  - answer: Yes, Aspose.PSD can be used in both personal and commercial projects under
      its licensing terms.
    question: Is Aspose.PSD suitable for commercial use?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- java image processing
- aspose.psd
- thumbnail extraction
title: Thumbnail aus PSD in Java extrahieren
url: /de/java/java-jpeg-image-processing/extract-thumbnail-from-psd-java/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Vorschaubild aus PSD in Java extrahieren

## Einführung
Das Extrahieren eines Vorschaubildes aus einer PSD‑Datei ermöglicht das schnelle Erstellen von Vorschauen, ohne das Bild in voller Auflösung zu laden. In Java macht Aspose.PSD diesen Vorgang unkompliziert und performant. In diesem Tutorial lernen Sie, wie Sie die Bibliothek einrichten, die Vorschaubild‑Ressource finden und sie als JPEG‑Datei speichern – alles mit nur wenigen Codezeilen.

## Schnelle Antworten
- **Welche Bibliothek verarbeitet PSD‑Vorschaubilder?** Aspose.PSD for Java.  
- **Wie viele Codezeilen werden benötigt?** Etwa fünf Zeilen zum Laden, Extrahieren und Speichern.  
- **Kann ich Vorschaubilder aus großen PSD‑Dateien extrahieren?** Ja, Aspose.PSD verarbeitet Dateien bis zu 500 MB, ohne das gesamte Bild in den Speicher zu laden.  
- **Benötige ich eine Lizenz für die Entwicklung?** Eine kostenlose Testversion reicht für die Evaluierung; für die Produktion ist eine Lizenz erforderlich.  
- **Welche Ausgabeformate werden unterstützt?** Das extrahierte Vorschaubild kann als JPEG, PNG oder BMP gespeichert werden.

## Was ist das Extrahieren eines Vorschaubildes aus PSD?
Das Extrahieren eines Vorschaubildes aus PSD ist der Vorgang, das kleine Vorschau‑Bild, das in einem Photoshop‑(PSD‑)Dokument eingebettet ist, auszulesen. Diese Vorschau wird als Ressource gespeichert und kann unabhängig zur Katalogisierung oder Anzeige gespeichert werden. Das Vorschaubild ist typischerweise eine niedrigauflösende Darstellung, die von Anwendungen verwendet wird, um eine schnelle visuelle Zusammenfassung anzuzeigen, ohne das Vollbild zu laden.

## Warum Aspose.PSD für diese Aufgabe verwenden?
Aspose.PSD unterstützt **30+ Bildformate** und kann PSD‑Dateien bis zu **500 MB** verarbeiten, während der Speicherverbrauch gering bleibt, weil Ressourcen bei Bedarf gelesen werden. Die API bietet zudem robuste Fehlerbehandlung, sodass Sie zuverlässig Vorschaubilder selbst aus beschädigten Dateien extrahieren können.

## Voraussetzungen
- Java Development Kit (JDK) installiert.  
- Aspose.PSD for Java‑Bibliothek heruntergeladen von [Aspose.PSD für Java Download](https://releases.aspose.com/psd/java/).  
- Grundlegende Kenntnisse in Java‑Syntax und Projektsetup.

## Wie extrahiert man ein Vorschaubild aus einer PSD‑Datei in Java?
Laden Sie die PSD‑Datei mit `PsdImage`, finden Sie die `ThumbnailResource` und speichern Sie deren Bilddaten als JPEG. Aspose.PSD abstrahiert das Low‑Level‑Parsing, sodass Sie nur `getResources()` aufrufen und anschließend `save()` auf dem extrahierten Bild verwenden müssen. Dieser Ansatz funktioniert für jede PSD, die ein Vorschaubild enthält, unabhängig von der Dateigröße.

## Pakete importieren
`Image` ist die Basisklasse zum Laden von Bildern. `PsdImage` repräsentiert ein PSD‑Dokument. `ThumbnailResource` und `Thumbnail4Resource` repräsentieren Vorschaubild‑Ressourcen. `JpegOptions` gibt JPEG‑Speicheroptionen an.

```text
```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.resources.Thumbnail4Resource;
import com.aspose.psd.fileformats.psd.resources.ThumbnailResource;
import com.aspose.psd.imageoptions.JpegOptions;
```
```

## Schritt 1: PSD‑Datei laden
Zuerst erstellen Sie eine `PsdImage`‑Instanz, die auf Ihre PSD‑Datei verweist. Der Konstruktor liest nur den Header und die benötigten Ressourcen, wodurch der Speicherverbrauch minimal bleibt.

```text
```java
String dataDir = "Your_Document_Directory/";
PsdImage image = (PsdImage)Image.load(dataDir + "your_file.psd");
```
```

Ersetzen Sie `"Your_Document_Directory/"` durch den Verzeichnispfad, in dem sich Ihre PSD‑Datei befindet, und `"your_file.psd"` durch den Namen Ihrer PSD‑Datei.

## Schritt 2: Bildressourcen durchlaufen
Aspose.PSD speichert Vorschaubilder als `ThumbnailResource`‑Objekte innerhalb der Bild‑Ressourcensammlung. Durchlaufen Sie die Sammlung, prüfen Sie den Ressourcentyp und erfassen Sie das erste gefundene Vorschaubild.

```text
```java
for (int i = 0; i < image.getImageResources().length; i++) {
    if (image.getImageResources()[i] instanceof ThumbnailResource) {
        ThumbnailResource thumbnail = (ThumbnailResource) image.getImageResources()[i];
        
        // Extract thumbnail data
        int[] data = thumbnail.getThumbnailArgb32Data();
        
        // Create a new image with the extracted thumbnail data
        PsdImage extractedThumbnailImage = new PsdImage(thumbnail.getWidth(), thumbnail.getHeight());
        extractedThumbnailImage.saveArgb32Pixels(extractedThumbnailImage.getBounds(), data);
        
        // Save the extracted thumbnail as a separate JPEG file
        extractedThumbnailImage.save(dataDir + "extracted_thumbnail.jpg", new JpegOptions());
        
        // Output success message
        System.out.println("Thumbnail extracted and saved successfully.");
        
        break; // Exit the loop once thumbnail is found and processed
    }
}
```
```

## Schritt 3: Extrahiertes Vorschaubild speichern
Sobald Sie das Vorschaubild haben, rufen Sie dessen `save`‑Methode auf, um es auf die Festplatte zu schreiben. Sie können JPEG, PNG oder BMP wählen; JPEG ist am gebräuchlichsten für Web‑Vorschauen.

## Schritt 4: Umgang mit verschiedenen Vorschaubildtypen
Enthält ein PSD mehrere Vorschaubild‑Varianten, wie `Thumbnail4Resource`, erweitern Sie die Iterationslogik, um jeden Typ zu prüfen. Die API stellt separate Klassen für jede Ressource bereit, sodass Sie die gewünschte Auflösung auswählen können.

## Häufige Probleme und Lösungen
- **Kein Vorschaubild gefunden:** Nicht alle PSD‑Dateien enthalten eine Vorschau. Überprüfen Sie die Quelldatei im Photoshop‑„Datei → Dateiinformationen“-Panel.  
- **Fehler: Nicht unterstütztes Format:** Stellen Sie sicher, dass Sie die neueste Aspose.PSD‑Version verwenden; ältere Versionen unterstützen möglicherweise neuere Vorschaubild‑Ressourcentypen nicht.  
- **Speicher‑Out‑of‑Memory bei großen Dateien:** Verwenden Sie `PsdImage.load(..., LoadOptions)` mit `LoadOptions.setLoadResourcesOnly(true)`, um das Laden der gesamten Bilddaten zu vermeiden, wenn Sie nur das Vorschaubild benötigen.

## Häufig gestellte Fragen

**F: Was ist Aspose.PSD?**  
A: Aspose.PSD ist eine Java‑Bibliothek, die die programmgesteuerte Erstellung, Manipulation und Konvertierung von PSD‑ und anderen Rasterbildformaten ermöglicht, ohne dass Adobe Photoshop erforderlich ist.

**F: Wo finde ich weitere Dokumentation zu Aspose.PSD für Java?**  
A: Sie können die [Dokumentation](https://reference.aspose.com/psd/java/) für detaillierte API‑Referenzen und Beispiele konsultieren.

**F: Kann ich Aspose.PSD kostenlos testen, bevor ich kaufe?**  
A: Ja, Sie können eine [kostenlose Testversion](https://releases.aspose.com/) herunterladen, um die Fähigkeiten der Bibliothek zu evaluieren.

**F: Wie kann ich eine temporäre Lizenz für Aspose.PSD erhalten?**  
A: Temporäre Lizenzen sind auf der Seite für [temporäre Lizenz](https://purchase.aspose.com/temporary-license/) verfügbar.

**F: Ist Aspose.PSD für den kommerziellen Einsatz geeignet?**  
A: Ja, Aspose.PSD kann sowohl in privaten als auch in kommerziellen Projekten gemäß den Lizenzbedingungen verwendet werden.

---

**Zuletzt aktualisiert:** 2026-10-03  
**Getestet mit:** Aspose.PSD for Java 24.12  
**Autor:** Aspose

## Verwandte Tutorials

- [Wie man PSD in Rasterbildformate mit Aspose.PSD für Java konvertiert](/psd/java/advanced-techniques/convert-psd-to-raster-formats/)
- [PSD als JPEG speichern und RGB‑Farbe mit Aspose.PSD Java unterstützen](/psd/java/advanced-psd-layer-features-effects/support-rgb-color-psd-files/)
- [Bildgröße ändern mit Aspose.PSD für Java – Formen zeichnen & grundlegende Bildoperationen](/psd/java/basic-image-operations/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}