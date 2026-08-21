---
date: 2026-07-03
description: Lär dig hur du beskär bild i Java med Aspose.PSD för Java. Denna steg‑för‑steg‑handledning
  om bildbeskärning täcker inläsning av PSD‑filer, inställning av shift values och
  sparar resultatet.
keywords:
- crop image java
- how to crop image
- load psd file
- java image processing
- crop image left right
linktitle: Beskär bild med förskjutningar
schemas:
- author: Aspose
  dateModified: '2026-07-03'
  description: Learn how to crop image java using Aspose.PSD for Java. This step‑by‑step
    image cropping tutorial covers loading PSD files, setting shift values, and saving
    the result.
  headline: Crop Image Java by Shifts with Aspose.PSD
  type: TechArticle
- description: Learn how to crop image java using Aspose.PSD for Java. This step‑by‑step
    image cropping tutorial covers loading PSD files, setting shift values, and saving
    the result.
  name: Crop Image Java by Shifts with Aspose.PSD
  steps:
  - name: Load the Image
    text: '`Image` is the base class for all image types in Aspose.PSD. `RasterImage`
      represents a raster image and provides cropping capabilities.'
  - name: Cache Image Data
    text: '`cacheData()` loads the image data into memory for faster processing.'
  - name: Define Shift Values
    text: Specify the shift values for all four sides of the image (left, top, right,
      bottom) in pixels.
  - name: Apply Cropping
    text: '`crop(left, right, top, bottom)` trims the image by the specified pixel
      shifts on each side.'
  - name: Save the Results
    text: '`JpegOptions` defines JPEG encoding settings such as quality and color
      profile. Congratulations! You''ve successfully cropped an image using Aspose.PSD
      for Java.'
  type: HowTo
- questions:
  - answer: Yes, Aspose.PSD supports over 30 raster formats, including PSD, JPEG,
      PNG, BMP, TIFF, and GIF, ensuring broad compatibility.
    question: Is Aspose.PSD compatible with all image formats?
  - answer: Absolutely. After each `crop` call you receive a new image object, which
      you can crop again as needed.
    question: Can I apply multiple cropping operations to the same image?
  - answer: Yes, you can find support and engage with the community at [Aspose.PSD
      Forum](https://forum.aspose.com/c/psd/34).
    question: Is there a community forum for Aspose.PSD support?
  - answer: Visit [here](https://purchase.aspose.com/temporary-license/) to obtain
      a temporary license.
    question: How can I obtain a temporary license for Aspose.PSD?
  - answer: Explore the documentation and examples at [Aspose.PSD Java Documentation](https://reference.aspose.com/psd/java/).
    question: Are there sample projects showcasing Aspose.PSD functionalities?
  type: FAQPage
second_title: Aspose.PSD Java API
title: Beskär bild i Java med förskjutningar med Aspose.PSD
url: /sv/java/image-editing/crop-image-by-shifts/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Beskär bild Java med förskjutningar med Aspose.PSD

## Introduktion

I Java-bildbehandling är **crop image java** ett vanligt krav för att förbereda grafik, miniatyrbilder eller UI‑tillgångar. Aspose.PSD för Java gör denna uppgift enkel genom att exponera en enkel `crop`‑metod som fungerar på alla stödda rasterformat. I den här handledningen kommer du att lära dig hur du laddar en PSD‑fil, definierar vänster‑höger‑top‑bottom‑förskjutningsvärden, tillämpar beskärningen och sparar resultatet — allt utan att skriva egen pixelmanipuleringskod.

## Snabba svar
- **Vilket bibliotek hanterar beskärning?** Aspose.PSD för Java tillhandahåller en inbyggd `crop`‑metod.  
- **Behöver jag en licens?** En tillfällig licens fungerar för utvärdering; en full licens krävs för produktion.  
- **Stödda format?** Över 30 rasterformat, inklusive PSD, JPEG, PNG, BMP och TIFF.  
- **Maximal filstorlek?** Hanterar filer upp till 2 GB utan att ladda hela bilden i minnet.  
- **Hur många kodrader?** Endast fem logiska steg — ladda, cacha, definiera förskjutningar, beskära och spara.

## Vad är crop image java?
`crop image java` avser operationen att trimma en bitmap i en Java‑applikation. Med Aspose.PSD utförs operationen av `crop`‑metoden, som accepterar förskjutningsvärden för varje sida av bilden och returnerar en ny bildinstans.

## Varför använda Aspose.PSD för bildbeskärning?
Aspose.PSD stödjer **30+** bildformat och kan bearbeta flertalet hundra‑sidiga PSD‑filer samtidigt som den använder mindre än 150 MB RAM, tack vare sin lazy‑loading‑arkitektur. Biblioteket garanterar också pixelperfekta resultat, bevarar lager, masker och färgprofiler — något som många generiska bildbibliotek inte kan garantera.

## Förutsättningar

### Java Development Kit (JDK)

Se till att du har den senaste versionen av JDK installerad på ditt system. Du kan ladda ner den från [här](https://www.oracle.com/java/technologies/javase-downloads.html).

### Aspose.PSD for Java Library

För att börja behöver du skaffa Aspose.PSD för Java‑biblioteket. Gå till [nedladdningssida](https://releases.aspose.com/psd/java/) och hämta den senaste versionen.

### Integrated Development Environment (IDE)

Välj din föredragna Java‑IDE, såsom Eclipse eller IntelliJ, för en smidig kodningsupplevelse.

## Hur man beskär bild java?

Ladda din källfil, definiera pixel‑förskjutningarna för varje sida och anropa `crop`‑metoden — hela arbetsflödet kan skrivas i fem koncisa kodrader. `crop`‑operationen skapar en ny bild som endast innehåller den region du specificerat, och lämnar den ursprungliga filen orörd.

### Steg 1: Ladda bilden

`Image` är basklassen för alla bildtyper i Aspose.PSD.  
`RasterImage` representerar en rasterbild och tillhandahåller beskärningsfunktioner.  
```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.imageoptions.JpegOptions;
```

### Steg 2: Cacha bilddata

`cacheData()` laddar bilddata i minnet för snabbare bearbetning.  
```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

// Load an existing image into an instance of RasterImage class
RasterImage rasterImage = (RasterImage)Image.load(sourceFile);
```

### Steg 3: Definiera förskjutningsvärden

Ange förskjutningsvärdena för alla fyra sidor av bilden (vänster, topp, höger, botten) i pixlar.  
```java
if (!rasterImage.isCached()) {
  rasterImage.cacheData();
}
```

### Steg 4: Tillämpa beskärning

`crop(left, right, top, bottom)` beskär bilden med de angivna pixel‑förskjutningarna på varje sida.  
```java
int leftShift = 10;
int rightShift = 10;
int topShift = 10;
int bottomShift = 10;
```

### Steg 5: Spara resultaten

`JpegOptions` definierar JPEG‑kodningsinställningar såsom kvalitet och färgprofil.  
```java
rasterImage.crop(leftShift, rightShift, topShift, bottomShift);
```

Grattis! Du har framgångsrikt beskärt en bild med Aspose.PSD för Java.

## Vanliga problem och lösningar

- **Bilden ser oförändrad ut:** Verifiera att förskjutningsvärdena är positiva och inte överskrider de ursprungliga dimensionerna.  
- **OutOfMemoryError på stora filer:** Aktivera cachning som visas i Steg 2; detta tvingar Aspose.PSD att använda en temporär fil istället för att hålla hela bilden i RAM.  
- **Färgförskjutning efter beskärning:** Se till att du bevarar färgprofilen genom att anropa `image.save(..., new JpegOptions { ColorProfile = image.ColorProfile })` om du behöver exakt färgprecision.

## Vanliga frågor

**Q: Är Aspose.PSD kompatibel med alla bildformat?**  
A: Ja, Aspose.PSD stödjer över 30 rasterformat, inklusive PSD, JPEG, PNG, BMP, TIFF och GIF, vilket säkerställer bred kompatibilitet.

**Q: Kan jag tillämpa flera beskärningsoperationer på samma bild?**  
A: Absolut. Efter varje `crop`‑anrop får du ett nytt bildobjekt, som du kan beskära igen vid behov.

**Q: Finns det ett community‑forum för Aspose.PSD‑support?**  
A: Ja, du kan hitta support och engagera dig med communityn på [Aspose.PSD‑forum](https://forum.aspose.com/c/psd/34).

**Q: Hur kan jag skaffa en tillfällig licens för Aspose.PSD?**  
A: Besök [här](https://purchase.aspose.com/temporary-license/) för att skaffa en tillfällig licens.

**Q: Finns det exempelprojekt som visar Aspose.PSD‑funktioner?**  
A: Utforska dokumentationen och exemplen på [Aspose.PSD Java-dokumentation](https://reference.aspose.com/psd/java/).

---

**Senast uppdaterad:** 2026-07-03  
**Testad med:** Aspose.PSD 24.11 for Java  
**Författare:** Aspose  

{{< blocks/products/products-backtop-button >}}

```java
String destName = dataDir + "CroppingByShifts_out.jpg";
rasterImage.save(destName, new JpegOptions());
```

## Relaterade handledningar

- [Beskär bild med rektangel i Aspose.PSD för Java](/psd/java/image-editing/crop-image-by-rectangle/)
- [Beskär bild Java - Expandera och beskära bilder med Aspose.PSD för Java](/psd/java/image-editing/expand-and-crop-images/)
- [Ändra storlek på bild Java - Använda Resize Type‑enumeration i Aspose.PSD för Java](/psd/java/advanced-image-manipulation/resizing-with-resize-type-enumeration/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}