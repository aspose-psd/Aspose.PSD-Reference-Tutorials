---
date: 2026-10-08
description: Lär dig hur du läser EXIF-taggar i Java med Aspose.PSD för Java (asp)
  i vår steg‑för‑steg‑handledning, och förbättra dina bildbehandlingsmöjligheter.
keywords:
- read exif tags java
- java exif tag extraction
- java image metadata extraction
lastmod: 2026-10-08
linktitle: Läs specifik EXIF‑tagginformation i Java
og_description: Läs EXIF-taggar Java‑utvecklare kan snabbt extrahera bildmetadata
  med Aspose.PSD. Denna guide visar hur du laddar en PSD, hittar miniatyrresurser
  och skriver ut viktiga EXIF‑fält såsom WhiteBalance och ISO speed.
og_image_alt: Guide showing how to read EXIF tags from PSD files in Java using Aspose.PSD
og_title: Hur man läser EXIF-taggar i Java med Aspose.PSD
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
title: Hur man läser EXIF-taggar i Java med Aspose.PSD
url: /sv/java/java-jpeg-image-processing/read-specific-exif-tags-info-java/
weight: 19
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Läs specifik EXIF‑tagginformation i Java med Aspose (asp)

## Introduktion
Om du behöver **läsa EXIF‑taggar i Java**, erbjuder Aspose.PSD (asp) ett rent, ren‑Java‑API som fungerar utan Photoshop. I den här handledningen kommer du att lära dig hur du extraherar EXIF‑data från en PSD‑bild, väljer endast de taggar du är intresserad av och skriver ut dem i konsolen. Vi täcker allt från att konfigurera din utvecklingsmiljö till att hämta metadata såsom WhiteBalance, ISO‑hastighet och brännvidd. Låt oss komma igång!

## Snabba svar
- **Vilket bibliotek läser EXIF‑data från PSD i Java?** Aspose.PSD (asp)  
- **Vilka taggar kan extraheras?** WhiteBalance, PixelXDimension, PixelYDimension, ISOSpeed, FocalLength, and more.  
- **Behöver jag en licens för produktion?** Yes, a commercial license is required; a free trial is available.  
- **Kan jag använda detta med andra bildformat?** The same API supports PNG, JPEG, TIFF via Java image metadata extraction.  
- **Hur lång tid tar implementeringen?** About 10‑15 minutes for a basic read‑only scenario.

## Vad är asp (Aspose.PSD för Java)?
Aspose.PSD för Java är ett rent Java‑bibliotek som gör det möjligt för utvecklare att arbeta med Adobe Photoshop‑filer (PSD, PSB) utan att installera Photoshop. Det ger programmatisk åtkomst till lager, resurser och metadata — inklusive EXIF‑taggar — vilket gör det idealiskt för **java image metadata extraction**‑uppgifter.

## Varför använda Aspose.PSD (asp) för EXIF‑extraktion?
Du kan extrahera EXIF‑taggar i Java med bara två metodanrop, och biblioteket behandlar filer upp till 2 GB utan att ladda hela dokumentet i minnet. Det stödjer **30+ bildformat** och bevarar exakta kamerainställningar, vilket ger dig deterministiska resultat på Windows, Linux och macOS‑miljöer.

## Förutsättningar
Innan vi dyker ner i koden finns det några saker du behöver ha på plats:

1. Java Development Kit (JDK): Se till att du har JDK installerat på din maskin. Du kan ladda ner det från den [Oracle JDK‑webbplatsen](https://www.oracle.com/java/technologies/javase-downloads.html).  
2. Aspose.PSD för Java: Ladda ner biblioteket från [Aspose.PSD för Java‑nedladdningssidan](https://releases.aspose.com/psd/java/).  
3. Integrerad utvecklingsmiljö (IDE): En IDE som IntelliJ IDEA, Eclipse eller NetBeans gör kodning mer bekväm.  
4. PSD‑fil: En PSD‑fil med EXIF‑data. Du kan använda provfilen som medföljer i den här handledningen eller någon annan PSD‑fil med EXIF‑taggar.

## Importera paket
Importera de nödvändiga Aspose.PSD‑klasserna såsom Image, PsdImage, ThumbnailResource och JpegExifData för att arbeta med PSD‑filer.  
```java
import com.aspose.psd.Image;
import com.aspose.psd.exif.JpegExifData;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.resources.Thumbnail4Resource;
import com.aspose.psd.fileformats.psd.resources.ThumbnailResource;
```

## Steg 1: ladda PSD‑bilden
`Image.load()` laddar en fil och returnerar ett Image‑objekt som representerar bilddata.  
`PsdImage` är Aspose.PSD‑klassen som tillhandahåller PSD‑specifik funktionalitet.  
Metoden `Image.load()` laddar någon stödjande bildfil i minnet och returnerar ett generiskt `Image`‑objekt som du kan kasta till en PSD‑specifik typ.  
```java
String dataDir = "Your Document Directory";
PsdImage image = (PsdImage) Image.load(dataDir + "1280px-Zebras_Serengeti.psd");
```

I detta steg laddar vi PSD‑filen med metoden `Image.load()`. Klassen `PsdImage` används för att representera PSD‑bilden, och vi kastar den laddade bilden till denna klass för att få åtkomst till PSD‑specifika funktioner.

## Steg 2: iterera över bildresurser
`PsdImage.getResources()` returnerar en samling inbäddade resurser såsom miniatyrbilder och EXIF‑data.  
Anropet `PsdImage.getResources()` returnerar en samling av alla inbäddade resurser. Genom att iterera över denna samling kan du hitta miniatyrresurser som innehåller EXIF‑metadata.  
```java
for (int i = 0; i < image.getImageResources().length; i++) {
    if (image.getImageResources()[i] instanceof ThumbnailResource || 
        image.getImageResources()[i] instanceof Thumbnail4Resource) {
        // Further processing will be done here
    }
}
```

Vi loopar igenom bildresurserna med en `for`‑loop. Målet är att identifiera resurser som är instanser av `ThumbnailResource` eller `Thumbnail4Resource`, eftersom dessa typer innehåller EXIF‑data.

## Steg 3: extrahera EXIF‑data
`ThumbnailResource.getJpegOptions()` ger åtkomst till JPEG‑alternativ inklusive EXIF‑metadata.  
`JpegExifData` innehåller enskilda EXIF‑taggvärden.  
Metoden `ThumbnailResource.getJpegOptions()` ger åtkomst till ett `JpegExifData`‑objekt som innehåller enskilda EXIF‑taggar såsom WhiteBalance, ISOSpeed och FocalLength.  
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

Vi använder ett `if`‑statement för att kontrollera om resursen är en instans av `ThumbnailResource`. Om den är det kastar vi den och hämtar dess `JpegOptions` för att komma åt `ExifData`. Slutligen skriver vi ut olika EXIF‑taggar såsom WhiteBalance, Pixel Dimensions, ISOSpeed och FocalLength.

## Vanliga problem & tips
- **Null EXIF‑data:** Vissa PSD‑filer kanske inte innehåller en miniatyrresurs med EXIF‑information. Kontrollera alltid `null` innan du åtkommer till taggvärden.  
- **Fel i filsökväg:** Använd absoluta sökvägar eller se till att arbetskatalogen pekar på mappen som innehåller din PSD‑fil.  
- **Licensrestriktioner:** Gratisprovversionen begränsar antalet sidor du kan bearbeta; uppgradera till en full licens för obegränsad användning.

## Vanliga frågor

### Vad är EXIF‑data?
EXIF (Exchangeable Image File Format)‑data är metadata inbäddad i bildfiler, som innehåller information såsom kamerainställningar, datum och tid samt bilddimensioner.

### Kan jag redigera EXIF‑data med Aspose.PSD?
Ja, Aspose.PSD låter dig läsa och modifiera EXIF‑data. Du kan uppdatera taggar och spara ändringarna tillbaka till bildfilen.

### Är Aspose.PSD för Java gratis?
Aspose.PSD erbjuder en gratis provversion som du kan ladda ner från [Aspose.PSD officiella releases‑sida](https://releases.aspose.com/). För full funktionalitet måste du köpa en licens.

### Vilka andra format stödjer Aspose.PSD?
Aspose.PSD stödjer olika Adobe Photoshop‑format, inklusive PSD, PSB och fler. Det erbjuder också möjligheter att konvertera dessa format till PNG, JPEG, TIFF osv.

### Hur får jag support för Aspose.PSD?
Du kan få support via Aspose.PSD‑[forumet](https://forum.aspose.com/c/psd/34).

### Hur hjälper detta med **java image metadata extraction**?
Genom att använda `JpegExifData`‑objektet kan du programatiskt hämta vilken EXIF‑tagg du behöver, vilket gör det till en solid grund för bredare metadata‑extraktionsuppgifter över bildformat.

---

**Last Updated:** 2026-10-08  
**Tested with:** Aspose.PSD for Java 24.11 (latest at time of writing)  
**Author:** Aspose

## Relaterade handledningar

- [Läs och ändra JPEG‑Exif‑taggar Java](/psd/java/java-jpeg-image-processing/read-modify-jpeg-exif-tags-java/)
- [Java JPEG‑bildbehandling](/psd/java/java-jpeg-image-processing/)
- [Hur man roterar bild på en specifik vinkel med Aspose.PSD för Java](/psd/java/advanced-image-manipulation/rotate-image-specific-angle/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}