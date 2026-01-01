---
date: 2026-01-01
description: Erfahren Sie, wie Sie XMP‑Metadaten erstellen, XMP zu PSD‑Dateien hinzufügen
  und Bildmetadaten mit Aspose.PSD für Java aktualisieren. Folgen Sie jetzt dieser
  Schritt‑für‑Schritt‑Anleitung.
linktitle: Create XMP Metadata
second_title: Aspose.PSD Java API
title: XMP-Metadaten mit Aspose.PSD für Java erstellen
url: /de/java/image-editing/create-xmp-metadata/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# XMP-Metadaten mit Aspose.PSD für Java erstellen

## Einführung

Die Verwaltung von Bildmetadaten ist ein häufiges Anliegen für Java‑Entwickler, die mit Photoshop‑Dateien (PSD) arbeiten. In diesem Tutorial lernen Sie **wie Sie XMP‑Metadaten** mit der Aspose.PSD‑Bibliothek erstellen, XMP zu einem PSD‑Bild hinzufügen und Bildmetadaten programmgesteuert aktualisieren. Wir gehen jeden Schritt durch, erklären, warum jeder Teil wichtig ist, und geben Ihnen praktische Tipps, die Sie in realen Projekten anwenden können.

## Schnellantworten
- **Was sind XMP‑Metadaten?** Ein standardisiertes Format zum Einbetten beschreibender Informationen (Autor, Schlüsselwörter usw.) in Bilddateien.  
- **Warum Aspose.PSD verwenden?** Es bietet eine reine Java‑API zum Erstellen, Lesen und Bearbeiten von PSD‑Dateien ohne Photoshop.  
- **Kann ich XMP zu einer bestehenden PSD hinzufügen?** Ja – Sie können Bildmetadaten on‑the‑fly mit `setXmpData` aktualisieren.  
- **Was sind die Hauptschritte?** Bildgröße festlegen, Header/Trailer erstellen, XMP‑Pakete zusammenbauen, anhängen und speichern.  
- **Benötige ich eine Lizenz?** Eine kostenlose Testversion reicht für die Entwicklung; für die Produktion ist eine kommerzielle Lizenz erforderlich.

## Was bedeutet „XMP‑Metadaten erstellen“ in Java?

XMP‑Metadaten zu erstellen bedeutet, ein XMP‑Paket (Header, Body, Trailer) zu bauen, das das Bild beschreibt, und dieses Paket dann in eine PSD‑Datei einzubetten. Die Aspose.PSD‑Bibliothek abstrahiert die Low‑Level‑Details, sodass Sie sich auf den Inhalt konzentrieren können, den Sie speichern möchten.

## Warum XMP zu PSD‑Dateien hinzufügen?

- **Durchsuchbarkeit:** Ermöglicht leistungsstarke Asset‑Management‑Suchen basierend auf Autor, Titel oder benutzerdefinierten Tags.  
- **Interoperabilität:** XMP wird von Adobe‑Produkten, Lightroom und vielen DAM‑Systemen erkannt.  
- **Versionskontrolle:** Speichern Sie Verarbeitungsverläufe (z. B. Stadt, Farbmodus) direkt in der Datei.

## Voraussetzungen

- **Java‑Entwicklungsumgebung:** JDK 8 oder höher installiert und Grundkenntnisse in Java.  
- **Aspose.PSD‑Bibliothek:** Laden Sie die Aspose.PSD für Java‑Bibliothek herunter und richten Sie sie ein. Die Bibliothek und die ausführliche Dokumentation finden Sie [hier](https://reference.aspose.com/psd/java/).  
- **Ihr Dokumentenverzeichnis:** Legen Sie fest, wo Sie PSD‑Dateien auf Ihrem System lesen/schreiben möchten.

## Pakete importieren

Importieren Sie in Ihrem Java‑Projekt die notwendigen Pakete, um die Funktionen von Aspose.PSD zu nutzen:

```java
import com.aspose.psd.Rectangle;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.system.io.MemoryStream;
import com.aspose.psd.xmp.XmpHeaderPi;
import com.aspose.psd.xmp.XmpMeta;
import com.aspose.psd.xmp.XmpPacketWrapper;
import com.aspose.psd.xmp.XmpTrailerPi;
import com.aspose.psd.xmp.schemas.dublincore.DublinCorePackage;
import com.aspose.psd.xmp.schemas.photoshop.ColorMode;
import com.aspose.psd.xmp.schemas.photoshop.PhotoshopPackage;
```

## Schritt 1: Bildgröße festlegen

Definieren Sie zunächst die Canvas‑Abmessungen für das neue PSD‑Bild.

```java
// Specify the size of the image by defining a Rectangle
Rectangle rect = new Rectangle(0, 0, 100, 200);
```

## Schritt 2: Neues Bild erstellen

Erzeugen Sie ein leeres PSD‑Bild, das wir später mit XMP‑Metadaten anreichern.

```java
// Create a brand new image for sample purposes
PsdImage image = new PsdImage(rect.getWidth(), rect.getHeight());
```

## Schritt 3: XMP‑Header erstellen

Der Header enthält die öffnende XML‑Verarbeitungsanweisung und eine GUID, die das Dokument identifiziert.

```java
// Create an instance of XMP-Header
XmpHeaderPi xmpHeader = new XmpHeaderPi();
xmpHeader.setGuid("Your Document Directory");
```

## Schritt 4: XMP‑Trailer erstellen

Der Trailer markiert das Ende des XMP‑Pakets. Das Setzen des `true`‑Flags schreibt die schließende Verarbeitungsanweisung.

```java
// Create an instance of Xmp-TrailerPi 
XmpTrailerPi xmpTrailer = new XmpTrailerPi(true);
```

## Schritt 5: XMP‑Metadaten erstellen

Fügen Sie generische Attribute wie Autor und Beschreibung zum Kern‑XMP‑Metadaten‑Objekt hinzu.

```java
// Create an instance of XMPmeta class to set different attributes
XmpMeta xmpMeta = new XmpMeta();
xmpMeta.addAttribute("Author", "Mr Smith");
xmpMeta.addAttribute("Description", "The fake metadata value");
```

## Schritt 6: XMP‑Paket‑Wrapper erstellen

Packen Sie Header, Trailer und Kern‑Metadaten in ein einzelnes Paket, das dem Bild angehängt werden kann.

```java
// Create an instance of XmpPacketWrapper that contains all metadata
XmpPacketWrapper xmpData = new XmpPacketWrapper(xmpHeader, xmpTrailer, xmpMeta);
```

## Schritt 7: Photoshop‑Attribute setzen

Füllen Sie Photoshop‑spezifische Felder (Stadt, Land, Farbmodus) aus, die viele Adobe‑Tools erwarten.

```java
// Create an instance of Photoshop package and set Photoshop attributes
PhotoshopPackage photoshopPackage = new PhotoshopPackage();
photoshopPackage.setCity("London");
photoshopPackage.setCountry("England");
photoshopPackage.setColorMode(ColorMode.Rgb);
```

## Schritt 8: Photoshop‑Paket zu XMP‑Metadaten hinzufügen

Hängen Sie das Photoshop‑Paket an das XMP‑Paket an.

```java
// Add Photoshop package into XMP metadata
xmpData.addPackage(photoshopPackage);
```

## Schritt 9: Dublin‑Core‑Attribute setzen

Fügen Sie Dublin‑Core‑Metadaten wie Autor, Titel und ein benutzerdefiniertes „movie“‑Tag hinzu.

```java
// Create an instance of DublinCore package and set DublinCore attributes
DublinCorePackage dublinCorePackage = new DublinCorePackage();
dublinCorePackage.setAuthor("Charles Bukowski");
dublinCorePackage.setTitle("Confessions of a Man Insane Enough to Live With the Beasts");
dublinCorePackage.addValue("dc:movie", "Barfly");
```

## Schritt 10: Dublin‑Core‑Paket zu XMP‑Metadaten hinzufügen

Kombinieren Sie das Dublin‑Core‑Paket mit dem bereits bestehenden XMP‑Paket.

```java
// Add DublinCore Package into XMP metadata
xmpData.addPackage(dublinCorePackage);
```

## Schritt 11: XMP‑Metadaten im Bild aktualisieren

Betten Sie nun das vollständige XMP‑Paket in das PSD‑Bild ein.

```java
// Update XMP metadata into the image
image.setXmpData(xmpData);
```

## Schritt 12: Bild speichern

Schreiben Sie schließlich die PSD‑Datei auf die Festplatte (oder in einen Speicher‑Stream), damit die Metadaten persistiert werden.

```java
// Save the image on the disk or in a memory stream
image.save("Your Document Directory" + "create_XMP_Metadata.psd");
```

## Häufige Probleme und Lösungen

| Problem | Warum es passiert | Lösung |
|---------|-------------------|--------|
| **`NullPointerException` bei `setXmpData`** | Das XMP‑Paket war nicht vollständig gebaut (Header/Trailer fehlten). | Stellen Sie sicher, dass Sie `XmpHeaderPi`, `XmpTrailerPi` erstellen und alle Pakete hinzufügen, bevor Sie `setXmpData` aufrufen. |
| **Metadaten in Photoshop nicht sichtbar** | Photoshop erwartet, dass das XMP‑Paket korrekt umschlossen ist. | Prüfen Sie, dass `XmpTrailerPi(true)` verwendet wird und das Paket mit dem Bild gespeichert wird. |
| **Dateipfad‑Fehler** | Verwendung eines relativen Pfads ohne passende Berechtigungen. | Nutzen Sie einen absoluten Pfad oder stellen Sie sicher, dass die Anwendung Schreibzugriff auf das Zielverzeichnis hat. |

## Häufig gestellte Fragen

**F: Ist Aspose.PSD mit verschiedenen Bildformaten kompatibel?**  
A: Ja, Aspose.PSD unterstützt PSD, PSB, BMP, GIF, JPEG, PNG, TIFF und mehr, sodass Sie flexibel über Formate hinweg arbeiten können.

**F: Kann ich vorhandene Metadaten mit Aspose.PSD manipulieren?**  
A: Absolut. Sie können ein bestehendes PSD laden, dessen XMP‑Daten mit `getXmpData()` abrufen, das Paket ändern und wieder speichern.

**F: Gibt es Beschränkungen bezüglich der Bildgröße, die Aspose.PSD verarbeiten kann?**  
A: Aspose.PSD ist für sehr große Bilder (bis zu mehreren Gigapixel) ausgelegt, begrenzt nur durch den verfügbaren Arbeitsspeicher.

**F: Gibt es eine Testversion von Aspose.PSD?**  
A: Ja, Sie können die Funktionen von Aspose.PSD mit einer kostenlosen Testversion [hier](https://releases.aspose.com/) ausprobieren.

**F: Wo finde ich Support für Fragen zu Aspose.PSD?**  
A: Für Unterstützung oder Fragen besuchen Sie das [Aspose.PSD‑Forum](https://forum.aspose.com/c/psd/34).

## Fazit

Sie haben nun **gelernt, wie Sie XMP‑Metadaten erstellen**, XMP zu einer PSD hinzufügen und Bildmetadaten mit Aspose.PSD für Java aktualisieren. Diese Schritte geben Ihnen die volle Kontrolle über die beschreibenden Informationen, die in Ihren Bildern eingebettet sind, machen sie durchsuchbar und bereit für nachgelagerte Workflows. Experimentieren Sie gern mit zusätzlichen XMP‑Schemas oder integrieren Sie diesen Code in größere Bildverarbeitungspipelines.

---

**Zuletzt aktualisiert:** 2026-01-01  
**Getestet mit:** Aspose.PSD für Java 24.12  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}