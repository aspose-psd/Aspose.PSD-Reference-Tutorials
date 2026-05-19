---
date: 2026-02-27
description: Lär dig hur du justerar gamma i Java‑bildbehandling med Aspose.PSD, konverterar
  PSD till TIFF och åtgärdar urtvättade bilder i en kortfattad handledning.
linktitle: Adjust Gamma of an Image
second_title: Aspose.PSD Java API
title: Hur man justerar gamma i Java‑bildbehandling med Aspose.PSD
url: /sv/java/advanced-techniques/adjust-gamma/
weight: 23
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Hur man justerar gamma i Java-bildbehandling med Aspose.PSD

## Introduktion

Om du arbetar med **java image processing**, är det en grundläggande teknik att lära sig **how to adjust gamma** för att förbättra ljusstyrka och kontrast utan att förlora detaljer. I den här handledningen går vi igenom hur du använder **Aspose.PSD for Java** för att applicera gamma‑korrektion på en PSD‑fil, **convert PSD to TIFF**, och undvika en **washed‑out image**. Du får se varför detta tillvägagångssätt är snabbt, pålitligt och perfekt för server‑side image pipelines.

## Snabba svar
- **What does gamma correction do?** Vad gör gamma‑korrektion? Det omkartlägger luminansvärden för att göra mörka områden ljusare eller ljusa områden mörkare samtidigt som den totala detaljen bevaras.  
- **Which library handles the processing?** Vilket bibliotek hanterar bearbetningen? Aspose.PSD for Java tillhandahåller en dedikerad `adjustGamma`‑metod för rasterbilder.  
- **Can I convert PSD to TIFF in the same flow?** Kan jag konvertera PSD till TIFF i samma flöde? Ja – efter gamma‑justering kan du spara bilden direkt till TIFF med `TiffOptions`.  
- **Do I need a license for development?** Behöver jag en licens för utveckling? En gratis provversion fungerar för testning; en kommersiell licens krävs för produktionsanvändning.  
- **What Java version is supported?** Vilken Java‑version stöds? Aspose.PSD stöder Java 8 och senare.

## Hur man justerar gamma i Java-bildbehandling
Att justera gamma är en kärnkomponent i alla **java image processing tutorial** som hanterar ljusstyrka eller kontrast. Nedan bryter vi ner stegen, förklarar varför varje rad är viktig och visar hur du integrerar processen i din befintliga kodbas.

## Vad är Java gamma‑korrektion?
Gamma‑korrektion förändrar det icke‑linjära förhållandet mellan de kodade pixelvärdena och den visade ljusstyrkan. Genom att justera gamma‑kurvan kan du **fix washed out image**‑problem eller förbättra detaljer i skuggor utan att överexponera högdagrar.

## Varför använda Aspose.PSD för gamma‑korrektion?
Aspose.PSD fungerar som ett kraftfullt **java image processing library** som abstraherar bort komplexiteten i PSD‑formatet. Det hanterar färgprofiler, cachning och erbjuder ett enkelt `adjustGamma`‑anrop, vilket gör det idealiskt för **java gamma correction** och **convert PSD to TIFF**‑arbetsflöden.

## Förutsättningar

1. **Java Development Environment** – Java 8 eller senare installerat.  
2. **Aspose.PSD Library** – Ladda ner och lägg till JAR‑filen i ditt projekt. Se den officiella [documentation](https://reference.aspose.com/psd/java/).  
3. **Sample Image** – En PSD‑fil du vill bearbeta (t.ex. `sample.psd`).  

## Importera paket

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.psd.fileformats.tiff.enums.TiffPhotometrics;
import com.aspose.psd.imageoptions.TiffOptions;
```

## Steg 1: Ladda bilden

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

**Proffstips:** Att cacha rasterdata en gång minskar minnesanvändning när du applicerar flera justeringar i rad.

## Steg 2: Justera gamma

```java
// Adjust the gamma
rasterImage.adjustGamma(2.2f, 2.2f, 2.2f);
```

Du kan skicka olika värden för de röda, gröna och blå kanalerna om du behöver kanal‑specifika justeringar.

## Steg 3: Skapa TiffOptions

```java
// Create an instance of TiffOptions for the resultant image
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
int[] ushort = { 8, 8, 8 };
tiffOptions.setBitsPerSample(ushort);
tiffOptions.setPhotometric(TiffPhotometrics.Rgb);
```

Att sätta ett 8‑bit‑sample (`{8,8,8}`) håller TIFF‑filens storlek rimlig samtidigt som färgprecisionen bevaras.

## Steg 4: Spara den resulterande bilden

```java
// Save the resultant image to TIFF format
String destName = dataDir + "AdjustGamma_out.tiff";
rasterImage.save(destName, tiffOptions);
```

Efter sparandet kan du skicka TIFF‑filen till efterföljande system som trycktjänster eller webb‑API:er.

## Vanliga användningsområden

- **Automated graphics pipelines** – Justera gamma i realtid innan miniatyrbilder genereras.  
- **Batch conversion tools** – Konvertera stora PSD‑arkiv till TIFF samtidigt som ljusstyrkan normaliseras.  
- **Web services** – Exponera en endpoint som tar emot en PSD, applicerar gamma‑korrektion och returnerar en TIFF för klientanvändning.

## Vanliga problem och lösningar

| Problem | Varför det händer | Hur man åtgärdar |
|-------|----------------|------------|
| **Image appears washed out** | Gamma‑värdet för högt (t.ex. > 2.5) | Sänk gamma‑faktorn till ett värde mellan 1.8 och 2.2. |
| **`rasterImage.isCached()` returns false** | Bilden har ännu inte laddats in i minnet | Anropa `rasterImage.cacheData()` innan du justerar gamma. |
| **TIFF file size is large** | Bits per sample är inställt på 16‑bit | Använd ett 8‑bit‑sample (`{8,8,8}`) som visas i exemplet. |

## Vanliga frågor

**Q: Kan jag applicera olika gamma‑värden på varje färgkanal?**  
A: Ja – `adjustGamma`‑metoden accepterar separata float‑värden för röd, grön och blå kanal.

**Q: Är det möjligt att kedja flera bildjusteringar innan sparning?**  
A: Absolut. Du kan utföra storleksändring, beskärning eller färgkorrigering sekventiellt på samma `RasterImage`‑instans.

**Q: Stöder Aspose.PSD multi‑page PSD‑filer?**  
A: Ja, varje lager kan nås och bearbetas individuellt.

**Q: Vilket format kan jag exportera till förutom TIFF?**  
A: Aspose.PSD stöder PNG, JPEG, BMP och många andra format via deras respektive options‑klasser.

**Q: Hur undviker jag en washed‑out image efter gamma‑korrektion?**  
A: Börja med en måttlig gamma (runt 2.0) och förhandsgranska resultatet; sänk värdet om bilden blir för ljus.

## Slutsats

Grattis! Du har nu lärt dig **how to adjust gamma** i ett **java image processing**‑arbetsflöde, konverterat en PSD till TIFF och undvikit vanliga fallgropar som en **washed‑out image**. Detta mönster ger dig fin‑granulär kontroll över ljusstyrka och kontrast, vilket gör det idealiskt för automatiserade grafik‑pipeline‑ar, webbtjänster eller skrivbordsverktyg.

---

**Last Updated:** 2026-02-27  
**Tested With:** Aspose.PSD 24.11 for Java  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}