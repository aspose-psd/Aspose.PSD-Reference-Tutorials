---
date: 2025-12-21
description: Lär dig hur du utför bildbehandling i Java genom att justera bildens
  gamma med Aspose.PSD. Steg‑för‑steg‑guide för att konvertera PSD till TIFF och applicera
  gamma‑korrektion.
linktitle: Adjust Gamma of an Image
second_title: Aspose.PSD Java API
title: Java bildbehandling – justera gamma med Aspose.PSD
url: /sv/java/advanced-techniques/adjust-gamma/
weight: 23
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Java Bildbehandling – Justera Gamma med Aspose.PSD

## Introduktion

Om du arbetar med **java image processing** är justering av gamma i en bild en grundläggande teknik för att förbättra ljusstyrka och kontrast utan att förlora detaljer. I den här handledningen går vi igenom hur du använder **Aspose.PSD for Java** för att applicera gamma‑korrektion på en PSD‑fil och sedan exportera resultatet som en TIFF‑bild. Du kommer att se varför detta tillvägagångssätt är snabbt, pålitligt och perfekt för server‑sidiga bildpipelines.

## Snabba svar
- **Vad gör gamma‑korrektion?** Den omkartlägger luminansvärden för att göra mörka områden ljusare eller ljusa områden mörkare samtidigt som den bevarar detaljerna.  
- **Vilket bibliotek hanterar bearbetningen?** Aspose.PSD for Java tillhandahåller en dedikerad `adjustGamma`‑metod för rasterbilder.  
- **Kan jag konvertera PSD till TIFF i samma flöde?** Ja – efter gammajustering kan du spara bilden direkt till TIFF med `TiffOptions`.  
- **Behöver jag en licens för utveckling?** En gratis provversion fungerar för testning; en kommersiell licens krävs för produktionsanvändning.  
- **Vilken Java‑version stöds?** Aspose.PSD stödjer Java 8 och senare.

## Vad är java image processing?

Java image processing avser manipulation, analys och transformation av visuella data med hjälp av Java‑bibliotek. Uppgifter inkluderar storleksändring, filtrering, färgkorrigering och formatkonvertering – allt som kan automatiseras i skrivbords‑ eller webbapplikationer.

## Varför använda Aspose.PSD för gamma‑korrektion?

Aspose.PSD erbjuder ett hög‑nivå‑API som abstraherar komplexiteten i PSD‑formatet, så att du kan fokusera på själva bildjusteringarna. Det hanterar cachning, färgprofiler och ger ett enkelt `adjustGamma`‑anrop, vilket gör det idealiskt för **image gamma correction** och **convert psd to tiff** arbetsflöden.

## Förutsättningar

1. **Java Development Environment** – Se till att du har en Java‑utvecklingsmiljö installerad på ditt system.  
2. **Aspose.PSD Library** – Ladda ner och integrera Aspose.PSD‑biblioteket i ditt Java‑projekt. Du hittar de nödvändiga resurserna i [documentation](https://reference.aspose.com/psd/java/).  
3. **Sample Image** – Förbered en exempel‑PSD‑bild som du kommer att använda för att applicera gammajusteringen.

## Importera paket

För att starta processen importerar du de nödvändiga paketen i ditt Java‑projekt. Detta förbereder grunden för att sömlöst använda Aspose.PSD‑funktionaliteten.

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.psd.fileformats.tiff.enums.TiffPhotometrics;
import com.aspose.psd.imageoptions.TiffOptions;
```

## Steg 1: Ladda bilden

Börja med att ladda den exempel‑PSD‑bilden i en instans av klassen `RasterImage`. Detta är grunden för efterföljande gammajusteringar.

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

## Steg 2: Justera Gamma

Justera nu gamma för den laddade bilden med metoden `adjustGamma`. Finjustera gamma‑värdena enligt dina krav.

```java
// Adjust the gamma
rasterImage.adjustGamma(2.2f, 2.2f, 2.2f);
```

## Steg 3: Skapa TiffOptions

Skapa en instans av `TiffOptions` för den resulterande bilden. Ställ in olika egenskaper, såsom bits per sample och fotometriska alternativ, för att anpassa utdata efter dina specifikationer.

```java
// Create an instance of TiffOptions for the resultant image
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
int[] ushort = { 8, 8, 8 };
tiffOptions.setBitsPerSample(ushort);
tiffOptions.setPhotometric(TiffPhotometrics.Rgb);
```

## Steg 4: Spara den resulterande bilden

Spara den manipulerade bilden i TIFF‑format med den tidigare definierade `TiffOptions`.

```java
// Save the resultant image to TIFF format
String destName = dataDir + "AdjustGamma_out.tiff";
rasterImage.save(destName, tiffOptions);
```

## Vanliga problem och lösningar

| Problem | Varför det händer | Hur man åtgärdar |
|---------|-------------------|------------------|
| **Bilden ser urvattnad ut** | Gamma‑värdet är för högt (t.ex. > 2,5) | Sänk gamma‑faktorn till ett värde mellan 1,8 och 2,2. |
| **`rasterImage.isCached()` returnerar false** | Bilden har ännu inte laddats in i minnet | Anropa `rasterImage.cacheData()` innan du justerar gamma. |
| **TIFF‑filstorleken är stor** | Bits per sample är inställda på 16‑bit | Använd ett 8‑bits sample (`{8,8,8}`) som visas i exemplet. |

## Vanliga frågor

**Q: Kan jag applicera olika gamma‑värden på varje färgkanal?**  
A: Ja – `adjustGamma`‑metoden accepterar separata float‑värden för röd, grön och blå kanal.

**Q: Är det möjligt att kedja flera bildjusteringar innan sparning?**  
A: Absolut. Du kan utföra storleksändring, beskärning eller färgkorrigering sekventiellt på samma `RasterImage`‑instans.

**Q: Stöder Aspose.PSD multi‑page PSD‑filer?**  
A: Ja, varje lager kan nås och bearbetas individuellt.

**Q: Vilket format kan jag exportera till förutom TIFF?**  
A: Aspose.PSD stödjer PNG, JPEG, BMP och många andra format via deras respektive options‑klasser.

## Slutsats

Grattis! Du har framgångsrikt utfört **java image processing** genom att justera gamma för en PSD‑fil och exportera den som en TIFF‑bild med Aspose.PSD for Java. Detta arbetsflöde ger dig fin‑granulär kontroll över bildens ljusstyrka och kontrast, vilket gör det idealiskt för automatiserade grafik‑pipelines, webbtjänster eller skrivbordsverktyg.

---

**Senast uppdaterad:** 2025-12-21  
**Testat med:** Aspose.PSD 24.11 for Java  
**Författare:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

## Vanliga frågor

### Q1: Var kan jag hitta Aspose.PSD‑dokumentationen?

A1: Du kan komma åt dokumentationen på [https://reference.aspose.com/psd/java/](https://reference.aspose.com/psd/java/).

### Q2: Hur laddar jag ner Aspose.PSD for Java?

A2: Ladda ner biblioteket från [https://releases.aspose.com/psd/java/](https://releases.aspose.com/psd/java/).

### Q3: Var kan jag köpa Aspose.PSD?

A3: Besök [https://purchase.aspose.com/buy](https://purchase.aspose.com/buy) för att köpa Aspose.PSD.

### Q4: Finns det en gratis provversion?

A4: Ja, du kan utforska en gratis provversion på [https://releases.aspose.com/](https://releases.aspose.com/).

### Q5: Vart kan jag få support för Aspose.PSD?

A5: För support, besök Aspose.PSD‑forumet på [https://forum.aspose.com/c/psd/34](https://forum.aspose.com/c/psd/34).