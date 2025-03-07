---
title: Justera gamma för en bild med Aspose.PSD för Java
linktitle: Justera gamma för en bild
second_title: Aspose.PSD Java API
description: Lär dig att justera bildgamma utan ansträngning med Aspose.PSD för Java. Följ vår steg-för-steg-guide för optimala resultat.
weight: 23
url: /sv/java/advanced-techniques/adjust-gamma/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Justera gamma för en bild med Aspose.PSD för Java

## Introduktion

Inom bildbehandlingsområdet är justering av gamma för en bild ett avgörande steg för att förbättra dess visuella tilltalande. Aspose.PSD för Java erbjuder en kraftfull lösning för Java-utvecklare för att enkelt manipulera bildgamma. I den här handledningen kommer vi att undersöka hur man justerar gamma med Aspose.PSD, och bryta ner varje steg för att säkerställa en sömlös implementering.

## Förutsättningar

Innan du dyker in i handledningen, se till att du har följande förutsättningar inställda:

1. Java-utvecklingsmiljö: Se till att du har en Java-utvecklingsmiljö installerad på ditt system.
2.  Aspose.PSD-bibliotek: Ladda ner och integrera Aspose.PSD-biblioteket i ditt Java-projekt. Du kan hitta de nödvändiga resurserna i[dokumentation](https://reference.aspose.com/psd/java/).
3. Exempelbild: Förbered en PSD-exempelbild som du ska använda för att tillämpa gammajusteringen.

## Importera paket

För att starta processen, importera de nödvändiga paketen i ditt Java-projekt. Detta skapar förutsättningar för att använda Aspose.PSD-funktioner sömlöst.

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.psd.fileformats.tiff.enums.TiffPhotometrics;
import com.aspose.psd.imageoptions.TiffOptions;
```

## Steg 1: Ladda bilden

 Börja med att ladda PSD-exemplet i en instans av`RasterImage` klass. Detta är grunden för efterföljande gammajusteringar.

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

// Ladda en befintlig bild i en instans av RasterImage-klassen
Image image = Image.load(sourceFile);

// Kasta bildens objekt till RasterImage
RasterImage rasterImage = (RasterImage)image;

// Kontrollera om RasterImage är cachad för bättre prestanda
if (!rasterImage.isCached()) {
    rasterImage.cacheData();
}
```

## Steg 2: Justera gamma

 Justera nu gamma för den laddade bilden med hjälp av`adjustGamma` metod. Finjustera gammavärdena enligt dina krav.

```java
// Justera gamma
rasterImage.adjustGamma(2.2f, 2.2f, 2.2f);
```

## Steg 3: Skapa TiffOptions

 Skapa en instans av`TiffOptions` för den resulterande bilden. Ställ in olika egenskaper, såsom bitar per prov och fotometriska alternativ, för att skräddarsy utdata efter dina specifikationer.

```java
// Skapa en instans av TiffOptions för den resulterande bilden
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
int[] ushort = { 8, 8, 8 };
tiffOptions.setBitsPerSample(ushort);
tiffOptions.setPhotometric(TiffPhotometrics.Rgb);
```

## Steg 4: Spara den resulterande bilden

 Spara den manipulerade bilden i TIFF-format med det tidigare definierade`TiffOptions`.

```java
// Spara den resulterande bilden i TIFF-format
String destName = dataDir + "AdjustGamma_out.tiff";
rasterImage.save(destName, tiffOptions);
```

## Slutsats

Grattis! Du har framgångsrikt justerat gamma för en bild med Aspose.PSD för Java. Denna process ger utvecklare möjlighet att förbättra bildkvaliteten utan ansträngning, vilket bidrar till en visuellt tilltalande användarupplevelse.

## FAQ's

### F1: Var kan jag hitta Aspose.PSD-dokumentationen?

 S1: Du kan komma åt dokumentationen på[https://reference.aspose.com/psd/java/](https://reference.aspose.com/psd/java/).

### F2: Hur laddar jag ner Aspose.PSD för Java?

 A2: Ladda ner biblioteket från[https://releases.aspose.com/psd/java/](https://releases.aspose.com/psd/java/).

### F3: Var kan jag köpa Aspose.PSD?

 A3: Besök[https://purchase.aspose.com/buy](https://purchase.aspose.com/buy) att köpa Aspose.PSD.

### F4: Finns det en gratis provperiod?

 A4: Ja, du kan utforska en gratis provperiod på[https://releases.aspose.com/](https://releases.aspose.com/).

### F5: Var kan jag söka support för Aspose.PSD?

 S5: För support, besök Aspose.PSD-forumet på[https://forum.aspose.com/c/psd/34](https://forum.aspose.com/c/psd/34).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
