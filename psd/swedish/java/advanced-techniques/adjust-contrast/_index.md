---
date: 2026-02-25
description: Lär dig hur du konverterar PSD till TIFF och justerar bildkontrast med
  Aspose.PSD för Java, ett ledande Java-bildmanipuleringsbibliotek.
linktitle: Convert PSD to TIFF and Adjust Contrast
second_title: Aspose.PSD Java API
title: Hur man konverterar PSD till TIFF och justerar kontrast med Aspose.PSD för
  Java
url: /sv/java/advanced-techniques/adjust-contrast/
weight: 22
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Så konverterar du PSD till TIFF och justerar kontrast med Aspose.PSD för Java

## Introduktion

Om du behöver **konvertera PSD till TIFF** samtidigt som du finjusterar den visuella kvaliteten på dina grafikbilder, är du på rätt plats. I den här handledningen går vi igenom hela arbetsflödet med Aspose.PSD för Java – ett robust **java image manipulation**‑bibliotek. Du kommer att lära dig hur du förbättrar **image contrast adjustment**, cachar stora rasterdata för bättre prestanda och slutligen **save image as TIFF** för vidare bearbetning. Låt oss dyka in!

## Snabba svar
- **Vad betyder “adjust contrast”?** Det ändrar skillnaden mellan de mörkaste och ljusaste pixlarna, vilket får detaljer att framträda.  
- **Vilket bibliotek hanterar detta?** Aspose.PSD för Java – ett full‑featured image processing‑verktyg.  
- **Behöver jag en licens?** En **temporary aspose license** fungerar för testning; en full licens krävs för produktion.  
- **Kan jag **convert PSD to TIFF**?** Absolut – vi kommer att använda `TiffOptions` för att exportera den bearbetade bilden.  
- **Hur lång tid tar det för koden att köras?** Vanligtvis under en sekund för standard‑storlek PSD‑filer på modern hårdvara.

## Vad är Image Contrast Adjustment?
Contrast adjustment modifierar tonalområdet i en bild och förstärker skillnaden mellan ljusa och mörka områden. Detta är särskilt användbart när bilder ser platta ut efter skanning eller när grafik förbereds för tryck.

## Varför använda Aspose.PSD för Java?
- **Rich format support** – öppna, redigera och **save image as TIFF**, PNG, JPEG och många fler.  
- **High performance** – caching och raster‑image optimeringar minskar minnesanvändning, vilket är avgörande för stora PSD‑filer.  
- **Straight‑forward API** – enkla metodanrop som `adjustContrast` gör koden läsbar och underhållbar.  
- **Comprehensive java image manipulation** funktioner som passar både enkla skript och företagsapplikationer.

## Förutsättningar

Innan du börjar, se till att du har:

- Grundläggande kunskap i Java‑programmering.  
- Aspose.PSD för Java‑biblioteket installerat. Du kan ladda ner det [here](https://releases.aspose.com/psd/java/).

## Importera paket

Lägg till de nödvändiga importerna i din Java‑klass:

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
```

Vi laddar käll‑PSD‑filen (`sample.psd`) i ett `Image`‑objekt, som fungerar som startpunkt för all vidare bearbetning.

## Steg 2: Casta till RasterImage och cacha data

```java
// Cast object of Image to RasterImage
RasterImage rasterImage = (RasterImage)image;

// Check if RasterImage is cached and Cache RasterImage for better performance
if (!rasterImage.isCached()) {
    rasterImage.cacheData();
}
```

Att casta till `RasterImage` ger oss tillgång till pixel‑nivå operationer. Caching förbättrar prestanda, särskilt för stora filer.

## Hur man justerar kontrast på en bild

```java
// Adjust the contrast
rasterImage.adjustContrast(50);
```

`adjustContrast`‑metoden tar ett heltal som representerar procentuell förändring. I detta exempel ökar vi kontrasten med **50 %**.

## Konvertera PSD till TIFF med Aspose.PSD

```java
// Create an instance of TiffOptions for the resultant image
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
int[] ushort = { 8, 8, 8 };
tiffOptions.setBitsPerSample(ushort);
tiffOptions.setPhotometric(TiffPhotometrics.Rgb);

// Save the resultant image to TIFF format
String destName = dataDir + "AdjustContrast_out.tiff";
rasterImage.save(destName, tiffOptions);
```

Här konfigurerar vi `TiffOptions` (bits per sample, fotometrisk tolkning) och **save image as TIFF**. Detta steg slutför arbetsflödet för **convert PSD to TIFF**.

## Vanliga problem och lösningar
- **Image not cached:** Anropa alltid `cacheData()` för stora PSD‑filer för att undvika `OutOfMemoryError`.  
- **Unexpected color shift:** Verifiera att `setPhotometric` matchar ditt mål‑färgrymd (RGB vs. CMYK).  
- **File not found:** Säkerställ att `dataDir` pekar på rätt mapp och att filnamnet är korrekt stavat.

## Vanliga frågor

### Q1: Är Aspose.PSD kompatibel med olika bildformat?

A1: Ja, Aspose.PSD stödjer olika bildformat, vilket ger flexibilitet i dina projekt.

### Q2: Hur kan jag få en temporär licens för Aspose.PSD?

A2: Du kan få en temporär licens [here](https://purchase.aspose.com/temporary-license/).

### Q3: Var kan jag hitta Aspose.PSD‑dokumentationen?

A3: Dokumentationen finns [here](https://reference.aspose.com/psd/java/).

### Q4: Vilka supportalternativ finns för Aspose.PSD?

A4: För support, besök [Aspose.PSD forum](https://forum.aspose.com/c/psd/34).

### Q5: Kan jag köpa Aspose.PSD?

A5: Ja, du kan köpa Aspose.PSD [here](https://purchase.aspose.com/buy).

## Slutsats

Du vet nu **hur du konverterar PSD till TIFF** och utför **image contrast adjustment** med Aspose.PSD för Java. Dessa steg ger dig fin kontroll över bildkvaliteten samtidigt som koden förblir ren och underhållbar. Känn dig fri att experimentera med andra justeringsmetoder som `adjustBrightness` eller `adjustGamma` för att passa dina specifika behov.

---

**Senast uppdaterad:** 2026-02-25  
**Testat med:** Aspose.PSD för Java 24.12  
**Författare:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}