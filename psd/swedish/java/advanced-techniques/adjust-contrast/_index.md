---
title: Justera kontrasten för en bild med Aspose.PSD för Java
linktitle: Justera kontrasten för en bild
second_title: Aspose.PSD Java API
description: Utforska världen av bildkontrastjustering i Java med Aspose.PSD. Följ vår steg-för-steg-guide för sömlös bildmanipulation.
weight: 22
url: /sv/java/advanced-techniques/adjust-contrast/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Justera kontrasten för en bild med Aspose.PSD för Java

## Introduktion

Inom bildbehandlingsområdet med Java framstår Aspose.PSD som ett kraftfullt verktyg. Bland dess otaliga funktioner är justering av bildkontrasten ett vanligt krav. Denna handledning kommer att leda dig genom processen att justera bildkontrasten med Aspose.PSD för Java. Oavsett om du är en erfaren utvecklare eller precis har börjat, hjälper den här guiden dig att bemästra denna viktiga aspekt av bildmanipulation.

## Förutsättningar

Innan du dyker in i handledningen, se till att du har följande förutsättningar på plats:

- Grundläggande förståelse för Java-programmering.
-  Aspose.PSD för Java-biblioteket installerat. Du kan ladda ner den[här](https://releases.aspose.com/psd/java/).

## Importera paket

För att komma igång måste du importera de nödvändiga paketen till ditt Java-projekt. Lägg till följande rader i din kod:

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

// Ladda en befintlig bild i en instans av RasterImage-klassen
Image image = Image.load(sourceFile);
```

 I det här steget laddar vi provbilden ("sample.psd") med hjälp av`Image.load` metod.

## Steg 2: Casta till RasterImage och cachedata

```java
// Kasta bildens objekt till RasterImage
RasterImage rasterImage = (RasterImage)image;

// Kontrollera om RasterImage är cachad och Cache RasterImage för bättre prestanda
if (!rasterImage.isCached()) {
    rasterImage.cacheData();
}
```

 Här gjuter vi det generiska`Image` invända mot en`RasterImage` för specifik bearbetning. Cachelagring av bilddata förbättrar prestandan.

## Steg 3: Justera kontrasten

```java
// Justera kontrasten
rasterImage.adjustContrast(50);
```

 De`adjustContrast`metoden används för att ändra bildens kontrast. I det här exemplet ökas kontrasten med 50 %.

## Steg 4: Skapa TiffOptions och spara

```java
// Skapa en instans av TiffOptions för den resulterande bilden
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
int[] ushort = { 8, 8, 8 };
tiffOptions.setBitsPerSample(ushort);
tiffOptions.setPhotometric(TiffPhotometrics.Rgb);

// Spara den resulterande bilden i TIFF-format
String destName = dataDir + "AdjustContrast_out.tiff";
rasterImage.save(destName, tiffOptions);
```

 Här ställer vi upp`TiffOptions` för utdatabilden, ange format och andra egenskaper. Den slutliga bilden sparas sedan i en TIFF-fil.

## Slutsats

Grattis! Du har framgångsrikt justerat kontrasten i en bild med Aspose.PSD för Java. Denna handledning täckte de väsentliga stegen, från att importera paket till att spara den bearbetade bilden.

## FAQ's

### F1: Är Aspose.PSD kompatibel med olika bildformat?

S1: Ja, Aspose.PSD stöder olika bildformat, vilket ger flexibilitet i dina projekt.

### F2: Hur kan jag få en tillfällig licens för Aspose.PSD?

 A2: Du kan få en tillfällig licens[här](https://purchase.aspose.com/temporary-license/).

### F3: Var kan jag hitta Aspose.PSD-dokumentation?

S3: Dokumentationen finns tillgänglig[här](https://reference.aspose.com/psd/java/).

### F4: Vilka supportalternativ finns tillgängliga för Aspose.PSD?

 S4: För support, besök[Aspose.PSD-forum](https://forum.aspose.com/c/psd/34).

### F5: Kan jag köpa Aspose.PSD?

 S5: Ja, du kan köpa Aspose.PSD[här](https://purchase.aspose.com/buy).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
