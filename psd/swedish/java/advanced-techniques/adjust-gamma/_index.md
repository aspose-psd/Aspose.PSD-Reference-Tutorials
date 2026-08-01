---
date: 2026-08-01
description: Lär dig hur du justerar gamma i Java image processing med Aspose.PSD,
  konverterar PSD till TIFF och åtgärdar urvattnade bilder i en kortfattad handledning.
keywords:
- how to adjust gamma
- fix washed out image
- java image processing
- convert psd to tiff
- server side image processing
lastmod: 2026-08-01
linktitle: Justera gamma för en bild
og_description: Lär dig hur du justerar gamma i Java image processing med Aspose.PSD
  – ett snabbt server‑side bibliotek som korrigerar urvattnade bilder och konverterar
  PSD till TIFF på bara några kodrader.
og_image_alt: 'Guide: Adjust gamma in Java images with Aspose.PSD, convert PSD to
  TIFF'
og_title: hur man justerar gamma – Java image processing med Aspose.PSD
schemas:
- author: Aspose
  dateModified: '2026-08-01'
  description: Learn how to adjust gamma in Java image processing with Aspose.PSD,
    convert PSD to TIFF, and fix washed‑out images in a concise tutorial.
  headline: How to Adjust Gamma in Java Image Processing with Aspose.PSD
  type: TechArticle
- description: Learn how to adjust gamma in Java image processing with Aspose.PSD,
    convert PSD to TIFF, and fix washed‑out images in a concise tutorial.
  name: How to Adjust Gamma in Java Image Processing with Aspose.PSD
  steps:
  - name: '**Java Development Environment** – Java 8 or later installed.'
    text: '**Java Development Environment** – Java 8 or later installed.'
  - name: '**Aspose.PSD Library** – Download and add the JAR to your project. See
      the official [documentation](https://reference.aspose.com/psd/java/).'
    text: '**Aspose.PSD Library** – Download and add the JAR to your project. See
      the official [documentation](https://reference.aspose.com/psd/java/).'
  - name: '**Sample Image** – A PSD file you want to process (e.g., `sample.psd`).'
    text: '**Sample Image** – A PSD file you want to process (e.g., `sample.psd`).'
  type: HowTo
- questions:
  - answer: Yes – the `adjustGamma` method accepts separate float values for red,
      green, and blue channels.
    question: Can I apply different gamma values to each colour channel?
  - answer: Absolutely. You can perform resizing, cropping, or colour corrections
      sequentially on the same `RasterImage` instance.
    question: Is it possible to chain multiple image adjustments before saving?
  - answer: Yes, each layer can be accessed and processed individually.
    question: Does Aspose.PSD support multi‑page PSD files?
  - answer: Aspose.PSD supports PNG, JPEG, BMP, and many other formats via their respective
      options classes.
    question: What format can I export to besides TIFF?
  - answer: Start with a moderate gamma (around 2.0) and preview the result; adjust
      downwards if the image looks too bright.
    question: How do I avoid a washed‑out image after gamma correction?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- adjust gamma
- Aspose.PSD
- Java image processing
- PSD to TIFF
- server side processing
title: Hur man justerar gamma i Java image processing med Aspose.PSD
url: /sv/java/advanced-techniques/adjust-gamma/
weight: 23
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Hur man justerar gamma i Java-bildbehandling med Aspose.PSD

## Introduktion

Om du arbetar med **java image processing** är det en grundläggande teknik att lära sig **how to adjust gamma** för att förbättra ljusstyrka och kontrast utan att förlora detaljer. I den här handledningen går vi igenom hur du använder **Aspose.PSD for Java** för att tillämpa gamma‑korrektion på en PSD‑fil, **convert PSD to TIFF**, och undvika en **washed‑out image**. Du kommer att se varför detta tillvägagångssätt är snabbt, pålitligt och perfekt för **server‑side image processing**‑pipelines.

## Snabba svar
- **Vad gör gamma‑korrektion?** Den omkartlägger luminansvärden för att göra mörka områden ljusare eller ljusa områden mörkare samtidigt som den bevarar den övergripande detaljen.  
- **Vilket bibliotek hanterar bearbetningen?** Aspose.PSD for Java provides a dedicated `adjustGamma` method for raster images.  
- **Kan jag konvertera PSD till TIFF i samma flöde?** Ja – efter gammajustering kan du spara bilden direkt till TIFF med `TiffOptions`.  
- **Behöver jag en licens för utveckling?** En gratis provversion fungerar för testning; en kommersiell licens krävs för produktionsanvändning.  
- **Vilken Java‑version stöds?** Aspose.PSD stöder Java 8 och senare.

## Vad är Java Gamma‑korrektion?

Gamma‑korrektion förändrar det icke‑linjära förhållandet mellan de kodade pixelvärdena och den visade ljusstyrkan. Genom att justera gamma‑kurvan kan du **fix washed out image**‑problem eller förbättra detaljer i skuggor utan att överexponera högdagrar. Det fungerar genom att applicera en potenslagfunktion på varje pixel, vilket ljusar upp mörka toner och komprimerar högdagrar, vilket resulterar i ett mer naturligt visuellt utseende.

## Varför använda Aspose.PSD för gamma‑korrektion?

Aspose.PSD är ett **java image processing library** som abstraherar bort komplexiteten i PSD‑formatet. Det stöder bearbetning av filer upp till 2 GB, hanterar över 50 olika bildformat och erbjuder ett enkelt `adjustGamma`‑anrop, vilket gör det idealiskt för **java gamma correction** och **convert PSD to TIFF**‑arbetsflöden.

## Förutsättningar

1. **Java Development Environment** – Java 8 eller senare installerat.  
2. **Aspose.PSD Library** – Ladda ner och lägg till JAR‑filen i ditt projekt. Se den officiella [documentation](https://reference.aspose.com/psd/java/).  
3. **Sample Image** – En PSD‑fil du vill bearbeta (t.ex. `sample.psd`).  

## Importera paket

Innan du börjar, importera de nödvändiga namnutrymmena som ger dig åtkomst till rasterhantering och fil‑formatalternativ.

## Steg 1: Ladda bilden

Klassen `RasterImage` representerar de rasteriserade pixeldata från ett PSD‑lager i minnet. Att ladda bilden en gång och cachea den minskar minnesanvändningen för efterföljande justeringar.

## Steg 2: Justera gamma

Ladda din PSD med `new RasterImage("sample.psd")` och anropa `rasterImage.adjustGamma(2.0f)` — den enda raden tillämpar en gamma på 2.0 över alla färgkanaler, ljusar upp skuggor samtidigt som högdagrar behålls intakta. Du kan skicka separata värden för röd, grön och blå om kanal‑specifika justeringar krävs.

## Steg 3: Skapa TiffOptions

`TiffOptions` låter dig kontrollera kompression, bitar per prov och andra TIFF‑specifika inställningar. Att sätta ett 8‑bitars prov (`{8,8,8}`) håller TIFF‑filens storlek rimlig samtidigt som färgprecision bevaras.

## Steg 4: Spara den resulterande bilden

Anropa `rasterImage.save("output.tif", tiffOptions)` för att skriva den bearbetade bilden till disk. Efter sparandet kan du skicka TIFF‑filen till efterföljande system såsom utskriftstjänster eller webb‑API:er.

## Vanliga användningsfall

- **Automated graphics pipelines** – Justera gamma i realtid innan du genererar miniatyrbilder.  
- **Batch conversion tools** – Konvertera stora PSD‑arkiv till TIFF samtidigt som du normaliserar ljusstyrkan.  
- **Web services** – Exponera en endpoint som tar emot en PSD, tillämpar gamma‑korrektion och returnerar en TIFF för klientanvändning.

## Vanliga problem och lösningar

| Problem | Varför det händer | Hur man åtgärdar |
|-------|----------------|------------|
| **Bilden ser urvattnad ut** | Gamma‑värdet är för högt (t.ex. > 2.5) | Sänk gamma‑faktorn till ett värde mellan 1.8 och 2.2. |
| **`rasterImage.isCached()` returns false** | Bilden är ännu inte inläst i minnet | Anropa `rasterImage.cacheData()` innan du justerar gamma. |
| **TIFF‑filens storlek är stor** | Bitar per prov är inställda på 16‑bit | Använd ett 8‑bitars prov (`{8,8,8}`) som i exemplet. |

## Vanliga frågor

**Q: Kan jag tillämpa olika gamma‑värden på varje färgkanal?**  
A: Ja – `adjustGamma`‑metoden accepterar separata float‑värden för röd, grön och blå kanaler.

**Q: Är det möjligt att kedja flera bildjusteringar innan sparning?**  
A: Absolut. Du kan utföra storleksändring, beskärning eller färgkorrigeringar sekventiellt på samma `RasterImage`‑instans.

**Q: Stöder Aspose.PSD flersidiga PSD‑filer?**  
A: Ja, varje lager kan nås och bearbetas individuellt.

**Q: Vilket format kan jag exportera till förutom TIFF?**  
A: Aspose.PSD stöder PNG, JPEG, BMP och många andra format via deras respektive options‑klasser.

**Q: Hur undviker jag en urvattnad bild efter gamma‑korrektion?**  
A: Börja med en måttlig gamma (ungefär 2.0) och förhandsgranska resultatet; sänk den om bilden ser för ljus ut.

## Slutsats

Grattis! Du har framgångsrikt lärt dig **how to adjust gamma** i ett **java image processing**‑arbetsflöde, konverterat en PSD till TIFF och undvikit vanliga fallgropar såsom en **washed‑out image**. Detta mönster ger dig fin‑granulär kontroll över ljusstyrka och kontrast, vilket gör det idealiskt för automatiserade grafik‑pipelines, webb‑tjänster eller skrivbordsverktyg.

---

**Last Updated:** 2026-08-01  
**Tested With:** Aspose.PSD 24.11 for Java  
**Author:** Aspose  

{{< blocks/products/products-backtop-button >}}

## Relaterade handledningar

- [Java-bildbehandlingshandledning – justera bildens ljusstyrka med Aspose.PSD för Java](/psd/java/advanced-techniques/adjust-brightness/)
- [Hur man konverterar PSD till TIFF och justerar kontrast med Aspose.PSD för Java](/psd/java/advanced-techniques/adjust-contrast/)
- [Konvertera PSD till bild i Java – tillämpa justeringslager med Aspose.PSD](/psd/java/advanced-psd-layer-features-effects/apply-adjustment-layers-psd-files/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.psd.fileformats.tiff.enums.TiffPhotometrics;
import com.aspose.psd.imageoptions.TiffOptions;
```

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

// Load an existing image into an instance of RasterImage class
Image image = Image.load(sourceFile);

// Cast object of Image to RasterImage
RasterImage rasterImage = (RasterImage)image;

// Check if RasterImage is cached for better performance
if (!rasterImage.isCached()) {
    rasterImage.cacheData();
}
```

```java
// Adjust the gamma
rasterImage.adjustGamma(2.2f, 2.2f, 2.2f);
```

```java
// Create an instance of TiffOptions for the resultant image
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
int[] ushort = { 8, 8, 8 };
tiffOptions.setBitsPerSample(ushort);
tiffOptions.setPhotometric(TiffPhotometrics.Rgb);
```

```java
// Save the resultant image to TIFF format
String destName = dataDir + "AdjustGamma_out.tiff";
rasterImage.save(destName, tiffOptions);
```