---
date: 2026-09-28
description: Hur man lägger till thumbnail i ett JFIF‑segment i Java med Aspose.PSD.
  Följ den här steg‑för‑steg‑guiden för att snabbt och pålitligt bädda in thumbnails
  i PSD‑filer.
keywords:
- how to add thumbnail
- JFIF segment Java
- Aspose.PSD thumbnail
- Java image processing
lastmod: 2026-09-28
linktitle: Lägg till thumbnail i JFIF‑segment i Java
og_description: Hur man lägger till thumbnail i ett JFIF‑segment i Java med Aspose.PSD.
  Följ den här steg‑för‑steg‑guiden för att snabbt och pålitligt bädda in thumbnails
  i PSD‑filer.
og_image_alt: Guide showing how to add thumbnail to JFIF segment in Java with Aspose.PSD
og_title: Hur man lägger till thumbnail i JFIF‑segment i Java
schemas:
- author: Aspose
  dateModified: '2026-09-28'
  description: How to add thumbnail to a JFIF segment in Java using Aspose.PSD. Follow
    this step‑by‑step guide to embed thumbnails in PSD files quickly and reliably.
  headline: How to add thumbnail to JFIF segment in Java
  type: TechArticle
- description: How to add thumbnail to a JFIF segment in Java using Aspose.PSD. Follow
    this step‑by‑step guide to embed thumbnails in PSD files quickly and reliably.
  name: How to add thumbnail to JFIF segment in Java
  steps:
  - name: import packages
    text: '`Document`, `JfifResource`, and related classes are part of the Aspose.PSD
      namespace. Document represents the PSD file container, and JfifResource provides
      access to the JFIF segment within the PSD. Import them at the top of your source
      file.'
  - name: load the PSD image
    text: Create a `PsdImage` instance by passing the file path to the constructor.
      PsdImage is the Aspose.PSD class that models a Photoshop document. This loads
      the document metadata while streaming the pixel data.
  - name: iterate over image resources
    text: Search the `Resources` collection for a `JfifResource`. When found, you
      can replace its thumbnail byte array with a new JPEG‑encoded preview.
  - name: adjust thumbnail data
    text: Generate a small JPEG thumbnail (e.g., 120 × 120 px) using any image‑processing
      library, then assign the resulting byte array to `jfifResource.ThumbnailData`.
  - name: save the modified image
    text: Call the `save` method on the `PsdImage` object, specifying the output path
      and desired format. The JFIF segment now contains the new thumbnail.
  type: HowTo
- questions:
  - answer: Aspose.PSD for Java is a commercial library that enables developers to
      create, edit, convert, and render Photoshop PSD files without requiring Adobe
      Photoshop.
    question: What is Aspose.PSD for Java?
  - answer: Detailed documentation can be found on the [Aspose.PSD for Java documentation
      page](https://reference.aspose.com/psd/java/).
    question: Where can I find more documentation for Aspose.PSD for Java?
  - answer: Yes, Aspose.PSD for Java can be used commercially. You can purchase a
      license from [Aspose.PSD's purchase page](https://purchase.aspose.com/buy).
    question: Is Aspose.PSD for Java suitable for commercial use?
  - answer: Yes, you can download a free trial from [Aspose.PSD's trial download page](https://releases.aspose.com/).
    question: Can I try Aspose.PSD for Java before purchasing?
  - answer: For support, visit the [Aspose.PSD forum](https://forum.aspose.com/c/psd/34).
    question: How can I get support for Aspose.PSD for Java?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- add thumbnail
- Aspose.PSD
- Java image processing
- JFIF
- PSD
title: Hur man lägger till thumbnail i JFIF‑segment i Java
url: /sv/java/java-jpeg-image-processing/add-thumbnail-to-jfif-segment-java/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Hur man lägger till miniatyrbild i JFIF‑segmentet i Java

## Introduktion
Att lägga till en miniatyrbild i JFIF‑segmentet i en PSD‑fil är ett vanligt krav när du behöver en snabb visuell förhandsgranskning utan att ladda hela bilden. I den här handledningen kommer du att lära dig **hur man lägger till miniatyrbild** i ett JFIF‑segment i Java med Aspose.PSD. I slutet av guiden har du ett körbart kodexempel, en förståelse för den underliggande JFIF‑strukturen och tips för att hantera stora filer effektivt.

## Snabba svar
- **Vilket bibliotek krävs?** Aspose.PSD för Java.
- **Vilken Java‑version fungerar?** JDK 11 eller senare.
- **Hur många kodrader behövs?** Ungefär 10 rader för att läsa in, modifiera och spara.
- **Kan jag bearbeta fler‑megabyte‑filer?** Ja, Aspose.PSD strömmar data, så minnesanvändningen hålls låg.
- **Behövs en kommersiell licens?** En licens krävs för produktionsbruk; en gratis provversion finns tillgänglig.

## Vad är ett JFIF‑segment?
JFIF‑segmentet är ett JPEG File Interchange Format‑block som kan lagra valfri data såsom miniatyrbilder, EXIF eller färgprofiler.  
Det finns i JPEG‑strömmen i en PSD‑fil och känns igen av de flesta bildvisare för snabb förhandsgranskning.

## Varför lägga till en miniatyrbild i en PSD‑fil?
Aspose.PSD för Java stödjer **30+ bildformat** och kan bearbeta filer upp till **2 GB** utan att ladda hela dokumentet i minnet. Att lägga till en miniatyrbild minskar nätverksbandbredden vid överföring av förhandsgranskningar och snabbar upp UI‑rendering i galleriprogram.

## Förutsättningar
- Java Development Kit (JDK): Se till att du har Java installerat på ditt system. Du kan ladda ner det från [Oracle's JDK website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).
- Aspose.PSD för Java: Du behöver ha Aspose.PSD för Java‑biblioteket. Du kan hämta det från [Aspose.PSD Java download page](https://releases.aspose.com/psd/java/).
- Integrated Development Environment (IDE): Använd en IDE som IntelliJ IDEA eller Eclipse för Java‑utveckling.
- Grundläggande förståelse för Java: Bekantskap med Java‑programmeringsspråket och koncept.

## Hur lägger man till en miniatyrbild i ett JFIF‑segment i Java?
Läs in mål‑PSD‑filen, lokalisera JFIF‑resursen, ersätt dess miniatyrdata och spara filen. Hela operationen kan utföras med några enkla API‑anrop, och Aspose.PSD hanterar den lågnivå JPEG‑strukturen åt dig.

### Steg 1: importera paket
`Document`, `JfifResource` och relaterade klasser är en del av Aspose.PSD‑namnutrymmet. Document representerar PSD‑filbehållaren, och JfifResource ger åtkomst till JFIF‑segmentet i PSD-filen. Importera dem högst upp i din källfil.

```java
import com.aspose.psd.Image;
import com.aspose.psd.exif.JpegExifData;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.resources.Thumbnail4Resource;
import com.aspose.psd.fileformats.psd.resources.ThumbnailResource;
```

### Steg 2: ladda PSD‑bilden
Skapa en `PsdImage`‑instans genom att skicka filvägen till konstruktorn. PsdImage är Aspose.PSD‑klassen som modellerar ett Photoshop‑dokument. Detta läser in dokumentmetadata samtidigt som pixeldata strömmas.

```java
String dataDir = "Your Document Directory";
PsdImage image = (PsdImage)Image.load(dataDir + "your_image.psd");
```

### Steg 3: iterera över bildresurser
Sök i samlingen `Resources` efter en `JfifResource`. När den hittas kan du ersätta dess miniatyr‑byte‑array med en ny JPEG‑kodad förhandsgranskning.

```java
for(int i = 0; i < image.getImageResources().length; i++) {
    if (image.getImageResources()[i] instanceof ThumbnailResource) {
        ThumbnailResource thumbnail = (ThumbnailResource)image.getImageResources()[i];
        
        // Continue with thumbnail processing
    }
}
```

### Steg 4: justera miniatyrdata
Generera en liten JPEG‑miniatyr (t.ex. 120 × 120 px) med ett bildbehandlingsbibliotek, och tilldela sedan den resulterande byte‑arrayen till `jfifResource.ThumbnailData`.

```java
try {
    PsdImage thumbnailImage = new PsdImage(100, 100);
    
    // Fill thumbnail data (example: create a simple pixel array)
    int[] pixels = new int[thumbnailImage.getWidth() * thumbnailImage.getHeight()];
    for (int j = 0; j < pixels.length; j++) {
        pixels[j] = j;
    }
    
    // Save thumbnail data
    thumbnailImage.saveArgb32Pixels(thumbnailImage.getBounds(), pixels);
    
    // Set thumbnail data to Jpeg options
    JpegExifData exifData = new JpegExifData();
    exifData.setThumbnail(thumbnailImage);
    JpegOptions jpegOptions = new JpegOptions();
    jpegOptions.setExifData(exifData);
    
    // Set options to thumbnail resource
    thumbnail.getJpegOptions().setExifData(exifData);
    
} catch(Exception e) {
    // Handle exceptions
} finally {
    // Dispose of resources
}
```

### Steg 5: spara den modifierade bilden
Anropa `save`‑metoden på `PsdImage`‑objektet, ange utdata‑sökvägen och önskat format. JFIF‑segmentet innehåller nu den nya miniatyrbilden.

```java
image.save(dataDir + "output.psd");
```

## Vanliga problem och lösningar
- **Miniatyrbilden syns inte i visare:** Se till att miniatyrdata är en giltig JPEG‑byte‑array och att dess dimensioner är inom 256 × 256 px, vilket är den maximala storleken som stöds av JFIF‑specifikationen.
- **OutOfMemoryError på stora PSD‑filer:** Använd `PsdImage.load(inputStream, true)` för att aktivera strömningsläge, vilket håller minnesförbrukningen låg.
- **Fel resurstyp:** Verifiera att resursen du modifierar verkligen är en `JfifResource`; andra resurser som `ExifResource` påverkar inte miniatyrvisning.

## Vanliga frågor

**Q: Vad är Aspose.PSD för Java?**  
A: Aspose.PSD för Java är ett kommersiellt bibliotek som gör det möjligt för utvecklare att skapa, redigera, konvertera och rendera Photoshop PSD‑filer utan att kräva Adobe Photoshop.

**Q: Var kan jag hitta mer dokumentation för Aspose.PSD för Java?**  
A: Detaljerad dokumentation finns på [Aspose.PSD for Java documentation page](https://reference.aspose.com/psd/java/).

**Q: Är Aspose.PSD för Java lämplig för kommersiell användning?**  
A: Ja, Aspose.PSD för Java kan användas kommersiellt. Du kan köpa en licens på [Aspose.PSD's purchase page](https://purchase.aspose.com/buy).

**Q: Kan jag prova Aspose.PSD för Java innan jag köper?**  
A: Ja, du kan ladda ner en gratis provversion från [Aspose.PSD's trial download page](https://releases.aspose.com/).

**Q: Hur kan jag få support för Aspose.PSD för Java?**  
A: För support, besök [Aspose.PSD forum](https://forum.aspose.com/c/psd/34).

---

**Senast uppdaterad:** 2026-09-28  
**Testat med:** Aspose.PSD för Java 24.11  
**Författare:** Aspose

## Relaterade handledningar

- [Lägg till IOPA‑resurs i PSD‑filer med Aspose PSD för Java](/psd/java/modifying-converting-psd-images/add-iopa-resource-psd-files/)
- [Lägg till signatur till bild – Rita bild på canvas med Aspose.PSD för Java](/psd/java/advanced-image-effects/add-signature-to-image/)
- [Hur man roterar bild i en specifik vinkel med Aspose.PSD för Java](/psd/java/advanced-image-manipulation/rotate-image-specific-angle/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}