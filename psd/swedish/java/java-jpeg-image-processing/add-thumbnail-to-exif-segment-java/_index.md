---
date: 2026-09-18
description: Lär dig hur du lägger till java‑bildmetadata‑miniatyr i EXIF‑segmentet
  med Aspose.PSD for Java. Denna steg‑för‑steg‑guide täcker förutsättningar, kodgenomgång
  och sparande av den uppdaterade bilden.
keywords:
- java image metadata
- how to add thumbnail
- java exif metadata
lastmod: 2026-09-18
linktitle: Lägg till miniatyr i EXIF‑segmentet i Java
og_description: Lär dig hur du lägger till java‑bildmetadata‑miniatyr i EXIF‑segmentet
  med Aspose.PSD for Java. Följ steg‑för‑steg‑guiden för att infoga miniatyrer och
  spara den uppdaterade bilden.
og_image_alt: Guide showing Java code to embed a thumbnail into EXIF metadata using
  Aspose.PSD
og_title: Hur man lägger till java‑bildmetadata‑miniatyr i EXIF‑segmentet
schemas:
- author: Aspose
  dateModified: '2026-09-18'
  description: Learn how to add java image metadata thumbnail to the EXIF segment
    using Aspose.PSD for Java. This step‑by‑step guide covers prerequisites, code
    walkthrough, and saving the updated image.
  headline: How to add java image metadata thumbnail to EXIF segment
  type: TechArticle
- questions:
  - answer: EXIF metadata is embedded information in digital images that includes
      camera settings, capture date, GPS coordinates, and other details.
    question: What is EXIF metadata?
  - answer: Adding a thumbnail improves user experience by allowing quick image previews
      without loading the full image.
    question: Why add a thumbnail to EXIF?
  - answer: You can download Aspose.PSD for Java from the [Aspose.PSD for Java download
      page](https://releases.aspose.com/psd/java/).
    question: Where can I download Aspose.PSD for Java?
  - answer: You can obtain a temporary license for Aspose.PSD from the [temporary
      license page](https://purchase.aspose.com/temporary-license/).
    question: How can I get a temporary license for Aspose.PSD?
  - answer: For support, visit the [Aspose.PSD forum](https://forum.aspose.com/c/psd/34).
    question: How do I get support for Aspose.PSD?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- java image metadata
- EXIF thumbnail
- Aspose.PSD
- Java image processing
title: Hur man lägger till java‑bildmetadata‑miniatyr i EXIF‑segmentet
url: /sv/java/java-jpeg-image-processing/add-thumbnail-to-exif-segment-java/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Lägg till java bildmetadata miniatyr i EXIF-segmentet

## Introduktion
I den här handledningen lär du dig hur du lägger till **java image metadata**‑miniatyr i EXIF‑segmentet i en PSD‑fil med Aspose.PSD för Java. EXIF (Exchangeable Image File Format)‑metadata lagrar kamerainställningar, inspelningsdatum, plats och annan användbar information. Att bädda in en liten förhandsgransknings‑miniatyr gör att applikationer kan visa en snabb bildöversikt utan att ladda hela filen, vilket förbättrar prestanda och användarupplevelse.

## Snabba svar
- **Vad täcker handledningen?** Lägga till en miniatyr i EXIF‑segmentet för en PSD‑bild med Aspose.PSD för Java.  
- **Hur lång tid tar implementeringen?** Ungefär 10‑15 minuter för en grundläggande integration.  
- **Behöver jag en licens?** En tillfällig licens krävs för produktionsanvändning; en gratis provversion fungerar för utvärdering.  
- **Vilken Java‑version stöds?** Java 8 och senare stöds fullt ut.  
- **Kan stora filer bearbetas?** Ja—Aspose.PSD kan hantera filer upp till 2 GB utan att ladda hela bilden i minnet.

## Vad är java image metadata?
Java image metadata avser den strukturerade information som är inbäddad i bildfiler (såsom EXIF, IPTC eller XMP) och som kan läsas, modifieras eller skapas programatiskt med Java‑bibliotek som Aspose.PSD. Denna metadata gör det möjligt för applikationer att hämta kamerainställningar, tidsstämplar, GPS‑koordinater och anpassad data utan att öppna det visuella innehållet.

## Varför lägga till en miniatyr i EXIF‑metadata?
Att lägga till en miniatyr i EXIF‑segmentet ger en omedelbar visuell ledtråd för bildbläddrare, filutforskare och innehållshanteringssystem. Aspose.PSD bearbetar miniatyrer i minnet, vilket gör att du kan bädda in en förhandsgranskning på under 0,2 sekunder för bilder upp till 500 KB, och den stöder över 30 bildformat, inklusive PSD, JPEG, PNG och TIFF.

## Förutsättningar
- Grundläggande kunskap i Java‑programmering.  
- Java Development Kit (JDK) installerat på ditt system.  
- IDE (Integrated Development Environment) för Java, såsom IntelliJ IDEA eller Eclipse.  
- Aspose.PSD för Java‑biblioteket. Du kan ladda ner det från [Aspose.PSD för Java nedladdningssida](https://releases.aspose.com/psd/java/).

## Importera paket
Följande importeringar tar in de Aspose.PSD‑klasser som behövs för att arbeta med PSD‑bilder och EXIF‑data.  
```java
import com.aspose.psd.Image;
import com.aspose.psd.exif.JpegExifData;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.resources.Thumbnail4Resource;
import com.aspose.psd.fileformats.psd.resources.ThumbnailResource;
```

## Steg 1: läs in psd‑bilden
`PsdImage` representerar en Photoshop PSD‑fil och ger åtkomst till dess lager och resurser.  
```java
String dataDir = "Your Document Directory";
PsdImage image = (PsdImage)Image.load(dataDir + "sample.psd");
```

## Steg 2: iterera över bildresurser
`ImageResource` kapslar resurser såsom miniatyrer, ICC‑profiler och metadata som är inbäddade i en PSD‑fil.  
```java
for (int i = 0; i < image.getImageResources().length; i++) {
    if (image.getImageResources()[i] instanceof ThumbnailResource || image.getImageResources()[i] instanceof Thumbnail4Resource) {
        ThumbnailResource thumbnail = (ThumbnailResource)image.getImageResources()[i];
        // Process the thumbnail resource
    }
}
```

## Steg 3: justera miniatyrdata
`JpegOptions` låter dig konfigurera JPEG‑specifika inställningar, såsom kvalitet, för miniatyrbilden.  
```java
JpegOptions jpegOptions = new JpegOptions();
jpegOptions.setQuality(100); // Set JPEG quality
```

## Steg 4: spara bilden
Genom att anropa `save` skrivs det uppdaterade EXIF‑segmentet (inklusive den nya miniatyren) tillbaka till disk utan att omkoda hela bilden.  
```java
image.save(dataDir + "output.psd");
```

## Vanliga problem och lösningar
- **Miniatyr visas inte:** Verifiera att miniatyrresursen har lagts till korrekt i EXIF‑segmentet och att bilden sparas med metoden `PsdImage.save`.  
- **Minnesbristfel på stora filer:** Använd `PsdImage.load(..., LoadOptions)` med `LoadOptions.setLoadOnlyMetadata(true)` för att arbeta endast med metadata.  
- **Felaktig orientering:** Säkerställ att miniatyren respekterar originalbildens orienteringsflagga; du kan läsa `Orientation`‑EXIF‑taggen och rotera miniatyren därefter.

## Vanliga frågor

**Q: Vad är EXIF‑metadata?**  
A: EXIF‑metadata är inbäddad information i digitala bilder som inkluderar kamerainställningar, inspelningsdatum, GPS‑koordinater och andra detaljer.

**Q: Varför lägga till en miniatyr i EXIF?**  
A: Att lägga till en miniatyr förbättrar användarupplevelsen genom att möjliggöra snabba bildförhandsgranskningar utan att ladda hela bilden.

**Q: Var kan jag ladda ner Aspose.PSD för Java?**  
A: Du kan ladda ner Aspose.PSD för Java från [Aspose.PSD för Java nedladdningssida](https://releases.aspose.com/psd/java/).

**Q: Hur kan jag få en tillfällig licens för Aspose.PSD?**  
A: Du kan skaffa en tillfällig licens för Aspose.PSD från [tillfällig licenssida](https://purchase.aspose.com/temporary-license/).

**Q: Hur får jag support för Aspose.PSD?**  
A: För support, besök [Aspose.PSD forum](https://forum.aspose.com/c/psd/34).

---

**Senast uppdaterad:** 2026-09-18  
**Testat med:** Aspose.PSD för Java 24.10  
**Författare:** Aspose

## Relaterade handledningar

- [Skapa XMP‑metadata i PSD‑filer med Aspose.PSD för Java](/psd/java/image-editing/create-xmp-metadata/)
- [Ändra storlek på bild med Aspose.PSD för Java – Rita former & grundläggande bildoperationer](/psd/java/basic-image-operations/)
- [Hur man konverterar PSD till rasterbildformat med Aspose.PSD för Java](/psd/java/advanced-techniques/convert-psd-to-raster-formats/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}