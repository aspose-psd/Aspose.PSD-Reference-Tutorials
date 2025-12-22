---
date: 2025-12-19
description: Lär dig hur du justerar bildens ljusstyrka med Aspose.PSD för Java. Denna
  Java‑tutorial för bildmanipulation ger en steg‑för‑steg‑guide.
linktitle: Adjust Brightness of an Image
second_title: Aspose.PSD Java API
title: Hur man justerar bildens ljusstyrka med Aspose.PSD för Java
url: /sv/java/advanced-techniques/adjust-brightness/
weight: 21
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Justera ljusstyrka på en bild med Aspose.PSD för Java

## Introduction

Om du behöver **lära dig hur du justerar ljusstyrka** på en bild direkt från Java‑kod, är du på rätt plats. Ljusstyrkejustering är en vanlig uppgift för grafiska formgivare, fotografer och alla som bygger bild‑behandlings‑pipelines. I den här **java image manipulation tutorial** går vi igenom hela arbetsflödet—laddar en PSD/TIFF, applicerar ett ljusstyrke‑offset och sparar resultatet—med Aspose.PSD för Java‑biblioteket.

## Quick Answers
- **Vilket bibliotek hanterar ljusstyrka?** Aspose.PSD for Java  
- **Vilken metod ändrar ljusstyrka?** `RasterImage.adjustBrightness()`  
- **Kan jag arbeta med PSD‑ och TIFF‑filer?** Ja, API‑et stöder båda formaten.  
- **Behöver jag en licens för produktion?** En kommersiell licens krävs för icke‑utvärderingsbruk.  
- **Hur lång tid tar implementeringen?** Vanligtvis under 10 minuter för en grundläggande justering.

## What is Image Brightness Adjustment?

Bildens ljusstyrkejustering förändrar den övergripande ljusheten för varje pixel i en bild. Att öka ljusstyrkan gör mörka områden ljusare, medan en minskning mörknar hela bilden. Denna operation är användbar för att korrigera underexponerade foton, förbereda material för tryck eller skapa visuella effekter i applikationer.

## Why Use Aspose.PSD for Java?

- **Fullt formatstöd** – PSD, TIFF, JPEG, PNG och mer.  
- **Inga externa inhemska beroenden** – ren Java, enkel att integrera.  
- **Högpresterande cachning** – rasterdata kan cachas för snabbare upprepade operationer.  
- **Rik API** – metoder för färgkorrigering, lager, masker och andra avancerade redigeringar.

## Prerequisites

Innan du dyker ner i handledningen, se till att du har följande förutsättningar:

- Aspose.PSD for Java Library: Ladda ner och installera biblioteket från [Aspose.PSD for Java documentation](https://reference.aspose.com/psd/java/).

## Import Packages

För att börja, importera de nödvändiga paketen i ditt Java‑projekt. I detta exempel använder vi följande:

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.psd.fileformats.tiff.enums.TiffPhotometrics;
import com.aspose.psd.imageoptions.TiffOptions;
```

Nu ska vi bryta ner processen för att justera ljusstyrkan på en bild i enkla steg:

## How to Adjust Brightness Using Aspose.PSD

### Step 1: Load the Image

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";
String destName = dataDir + "AdjustBrightness_out.tiff";

// Load an existing image into an instance of RasterImage class
Image image = Image.load(sourceFile);
// Cast object of Image to RasterImage
RasterImage rasterImage = (RasterImage) image;

// Check if RasterImage is cached and Cache RasterImage for better performance
if (!rasterImage.isCached()) {
    rasterImage.cacheData();
}
```

I detta steg laddar vi målbilden och kastar den till en `RasterImage` för vidare bearbetning.

### Step 2: Adjust Brightness

```java
// Adjust the brightness
rasterImage.adjustBrightness(-50);
```

Här använder vi `adjustBrightness`‑metoden för att ändra bildens ljusstyrka. I detta exempel minskar vi ljusstyrkan med 50 enheter, men du kan anpassa värdet efter dina behov.

### Step 3: Set TiffOptions

```java
int[] ushort = {8, 8, 8};
// Create an instance of TiffOptions for the resultant image
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
tiffOptions.setBitsPerSample(ushort);
tiffOptions.setPhotometric(TiffPhotometrics.Rgb);
```

Konfigurera `TiffOptions` för att spara den justerade bilden. Justera egenskaperna `bitsPerSample` och `photometric` efter dina specifika krav.

### Step 4: Save the Resultant Image

```java
// Save the resultant image
rasterImage.save(destName, tiffOptions);
```

Spara slutligen den modifierade bilden med de angivna `TiffOptions`.

## Common Issues and Solutions

| Problem | Orsak | Lösning |
|---------|-------|----------|
| **`ClassCastException` vid typkonvertering av Image** | Filen är inte en rasterbild (t.ex. en vektor‑PSD). | Verifiera källfilens format eller använd `image instanceof RasterImage` innan typkonvertering. |
| **Ljusstyrkeändring har ingen effekt** | Bilden cacheades inte innan justering. | Anropa `rasterImage.cacheData()` som visas i Steg 1. |
| **Sparad fil verkar korrupt** | Felaktig `TiffOptions`‑konfiguration. | Säkerställ att `bitsPerSample` matchar källbildens djup (vanligtvis 8‑bit per kanal). |

## Frequently Asked Questions

### Q1: Kan jag justera ljusstyrka i andra bildformat än PSD?

A1: Ja, Aspose.PSD for Java stöder olika bildformat som JPEG, PNG och TIFF.

### Q2: Hur kan jag hantera fel under bildjusteringsprocessen?

A2: Du kan implementera felhantering med try‑catch‑block för att hantera eventuella undantag som kan uppstå.

### Q3: Finns det någon gräns för intervallet av ljusstyrkejustering?

A3: Intervallet beror på bildens innehåll och format, men Aspose.PSD ger flexibilitet för anpassning.

### Q4: Kan jag använda Aspose.PSD for Java i kommersiella projekt?

A4: Ja, Aspose.PSD for Java är ett kommersiellt bibliotek, och du kan skaffa en licens från [here](https://purchase.aspose.com/buy).

### Q5: Finns det en gratis provperiod för Aspose.PSD for Java?

A5: Ja, du kan utforska biblioteket med en gratis provperiod från [here](https://releases.aspose.com/).

### Q6: Påverkar `adjustBrightness`‑metoden lagersynlighet?

A6: Metoden arbetar på den rasteriserade sammansatta bilden, så lagersynlighet respekteras under rasteriseringen.

### Q7: Kan jag kedja flera justeringar (t.ex. kontrast, mättnad) tillsammans?

A7: Absolut. Efter att ha justerat ljusstyrkan kan du anropa `adjustContrast`, `adjustSaturation` osv. på samma `RasterImage`‑instans.

---

**Last Updated:** 2025-12-19  
**Tested With:** Aspose.PSD for Java 24.12 (latest at time of writing)  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}