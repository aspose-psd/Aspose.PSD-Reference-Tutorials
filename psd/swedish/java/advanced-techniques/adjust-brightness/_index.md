---
title: Justera ljusstyrkan för en bild med Aspose.PSD för Java
linktitle: Justera ljusstyrkan för en bild
second_title: Aspose.PSD Java API
description: Förbättra bildens ljusstyrka i Java med Aspose.PSD. Steg-för-steg-guide för att justera bildens ljusstyrka programmatiskt.
type: docs
weight: 21
url: /sv/java/advanced-techniques/adjust-brightness/
---
## Introduktion

Att förbättra bilder är ett vanligt krav inom grafisk design och digital fotografering. Aspose.PSD för Java tillhandahåller en kraftfull lösning för att justera bildens ljusstyrka programmatiskt. I den här handledningen kommer vi att utforska hur man använder Aspose.PSD för Java-biblioteket för att justera ljusstyrkan på en bild, steg för steg.

## Förutsättningar

Innan du dyker in i handledningen, se till att du har följande förutsättningar:

-  Aspose.PSD för Java Library: Ladda ner och installera biblioteket från[Aspose.PSD för Java-dokumentation](https://reference.aspose.com/psd/java/).

## Importera paket

För att börja, importera de nödvändiga paketen till ditt Java-projekt. I det här exemplet använder vi följande:

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.psd.fileformats.tiff.enums.TiffPhotometrics;
import com.aspose.psd.imageoptions.TiffOptions;
```

Låt oss nu dela upp processen att justera ljusstyrkan på en bild i enkla steg:

## Steg 1: Ladda bilden

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";
String destName = dataDir + "AdjustBrightness_out.tiff";

// Ladda en befintlig bild i en instans av RasterImage-klassen
Image image = Image.load(sourceFile);
// Kasta bildens objekt till RasterImage
RasterImage rasterImage = (RasterImage) image;

// Kontrollera om RasterImage är cachad och Cache RasterImage för bättre prestanda
if (!rasterImage.isCached()) {
    rasterImage.cacheData();
}
```

 I det här steget laddar vi målbilden och castar den till en`RasterImage` för vidare bearbetning.

## Steg 2: Justera ljusstyrkan

```java
// Justera ljusstyrkan
rasterImage.adjustBrightness(-50);
```

 Här använder vi`adjustBrightness`metod för att ändra bildens ljusstyrka. I det här exemplet minskar vi ljusstyrkan med 50 enheter, men du kan anpassa detta värde baserat på dina krav.

## Steg 3: Ställ in TiffOptions

```java
int[] ushort = {8, 8, 8};
// Skapa en instans av TiffOptions för den resulterande bilden
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
tiffOptions.setBitsPerSample(ushort);
tiffOptions.setPhotometric(TiffPhotometrics.Rgb);
```

 Konfigurera`TiffOptions` för att spara den justerade bilden. Justera`bitsPerSample` och`photometric` egenskaper utifrån dina specifika behov.

## Steg 4: Spara den resulterande bilden

```java
// Spara den resulterande bilden
rasterImage.save(destName, tiffOptions);
```

 Slutligen, spara den modifierade bilden med den angivna`TiffOptions`.

## Slutsats

Att justera ljusstyrkan på en bild programmatiskt görs enkelt med Aspose.PSD för Java. Den här handledningen har gett en omfattande guide om hur du implementerar den här funktionen i dina Java-applikationer.

## FAQ's

### F1: Kan jag justera ljusstyrkan i andra bildformat än PSD?

S1: Ja, Aspose.PSD för Java stöder olika bildformat som JPEG, PNG och TIFF.

### F2: Hur kan jag hantera fel under bildjusteringsprocessen?

S2: Du kan implementera felhantering med hjälp av try-catch-block för att hantera undantag som kan uppstå.

### F3: Finns det en gräns för intervallet för ljusstyrkajustering?

S3: Justeringsintervallet beror på bildinnehållet och formatet, men Aspose.PSD ger flexibilitet vid anpassning.

### F4: Kan jag använda Aspose.PSD för Java i kommersiella projekt?

 S4: Ja, Aspose.PSD för Java är ett kommersiellt bibliotek och du kan få en licens från[här](https://purchase.aspose.com/buy).

### F5: Finns det en gratis testversion tillgänglig för Aspose.PSD för Java?

 S5: Ja, du kan utforska biblioteket med en gratis provperiod från[här](https://releases.aspose.com/).