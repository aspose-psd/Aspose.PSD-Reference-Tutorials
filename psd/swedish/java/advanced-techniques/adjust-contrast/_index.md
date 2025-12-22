---
date: 2025-12-21
description: Lär dig hur du justerar kontrasten på bilder med Aspose.PSD för Java,
  ett ledande Java‑bildmanipuleringsbibliotek, och konverterar PSD till TIFF effektivt.
linktitle: Adjust Contrast of an Image
second_title: Aspose.PSD Java API
title: Hur man justerar kontrasten på en bild med Aspose.PSD för Java
url: /sv/java/advanced-techniques/adjust-contrast/
weight: 22
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Hur man justerar kontrast på en bild med Aspose.PSD för Java

## Introduktion

Om du letar efter **hur man justerar kontrast** i dina Java‑projekt, har du kommit till rätt ställe. Aspose.PSD för Java är ett kraftfullt **java‑bildmanipuleringsbibliotek** som låter dig finjustera bildegenskaper såsom kontrast, ljusstyrka och mer. I den här handledningen går vi igenom de exakta stegen för att öka kontrasten i en PSD‑fil och sedan **konvertera PSD till TIFF** för efterföljande arbetsflöden.

## Snabba svar
- **Vad betyder “adjust contrast”?** Det ändrar skillnaden mellan de mörkaste och ljusaste pixlarna, vilket får detaljer att framträda.
- **Vilket bibliotek hanterar detta?** Aspose.PSD för Java – ett fullständigt bildbehandlingsverktyg.
- **Behöver jag en licens?** En tillfällig licens fungerar för testning; en full licens krävs för produktion.
- **Kan jag spara resultatet som TIFF?** Ja, vi kommer att använda `TiffOptions` för att exportera den bearbetade bilden.
- **Hur lång tid tar koden att köra?** Vanligtvis under en sekund för standard‑storlek PSD‑filer.

## Vad är kontrastjustering?
Kontrastjustering förändrar bildens tonomfång och förstärker skillnaden mellan ljusa och mörka områden. Detta är särskilt användbart när bilder ser platta ut efter skanning eller när grafik förbereds för tryck.

## Varför använda Aspose.PSD för Java?
- **Rikt formatstöd** – öppna, redigera och spara PSD, TIFF, PNG, JPEG och många fler.
- **Hög prestanda** – cachning och raster‑bildoptimeringar minskar minnesanvändningen.
- **Enkel API** – enkla metodanrop som `adjustContrast` gör koden läsbar.

## Förutsättningar

Innan du dyker ner, se till att du har:

- Grundläggande kunskaper i Java‑programmering.
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

## Steg 2: Kasta till RasterImage och cacha data

```java
// Cast object of Image to RasterImage
RasterImage rasterImage = (RasterImage)image;

// Check if RasterImage is cached and Cache RasterImage for better performance
if (!rasterImage.isCached()) {
    rasterImage.cacheData();
}
```

Att kasta till `RasterImage` ger oss åtkomst till pixel‑nivå operationer. Cachning förbättrar prestanda, särskilt för stora filer.

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

Här konfigurerar vi `TiffOptions` (bitar per prov, fotometrisk tolkning) och skriver den kontrastförbättrade bilden till en TIFF‑fil.

## Vanliga problem och lösningar
- **Bild inte cachad:** Anropa alltid `cacheData()` för stora PSD‑filer för att undvika `OutOfMemoryError`.
- **Oväntad färgförskjutning:** Verifiera att `setPhotometric` matchar ditt mål‑färgrymd (RGB vs. CMYK).
- **Fil ej hittad:** Säkerställ att `dataDir` pekar på rätt mapp och att filnamnet är stavat korrekt.

## Vanliga frågor

### Q1: Är Aspose.PSD kompatibel med olika bildformat?
A1: Ja, Aspose.PSD stödjer olika bildformat, vilket ger flexibilitet i dina projekt.

### Q2: Hur kan jag få en tillfällig licens för Aspose.PSD?
A2: Du kan få en tillfällig licens [here](https://purchase.aspose.com/temporary-license/).

### Q3: Var kan jag hitta Aspose.PSD-dokumentation?
A3: Dokumentationen finns tillgänglig [here](https://reference.aspose.com/psd/java/).

### Q4: Vilka supportalternativ finns för Aspose.PSD?
A4: För support, besök [Aspose.PSD forum](https://forum.aspose.com/c/psd/34).

### Q5: Kan jag köpa Aspose.PSD?
A5: Ja, du kan köpa Aspose.PSD [here](https://purchase.aspose.com/buy).

## Slutsats

Du vet nu **hur man justerar kontrast** på en PSD‑bild med Aspose.PSD för Java och hur man **konverterar PSD till TIFF** för vidare bearbetning. Dessa steg ger dig fin‑granulär kontroll över bildkvaliteten samtidigt som koden hålls ren och underhållbar. Känn dig fri att experimentera med andra bildjusteringsmetoder som `adjustBrightness` eller `adjustGamma` för att passa dina specifika behov.

---

**Senast uppdaterad:** 2025-12-21  
**Testad med:** Aspose.PSD for Java 24.12  
**Författare:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}