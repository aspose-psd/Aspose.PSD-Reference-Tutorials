---
title: Stöd Shadow Effect i Aspose.PSD för Java
linktitle: Stöd Shadow Effect
second_title: Aspose.PSD Java API
description: Lär dig hur du lägger till fängslande skuggeffekter till bilder med Aspose.PSD för Java. Lyft din grafiska design med denna steg-för-steg handledning.
type: docs
weight: 13
url: /sv/java/basic-image-operations/support-shadow-effect/
---
## Introduktion

Att förbättra bilder med skuggeffekter är en vanlig praxis inom grafisk design, vilket ger djup och realism. Aspose.PSD för Java ger robust stöd för skuggeffekter, vilket gör att utvecklare enkelt kan integrera dessa effekter i sina Java-applikationer. I den här handledningen kommer vi att undersöka hur du stöder skuggeffekter med Aspose.PSD, steg för steg.

## Förutsättningar

Innan du dyker in i handledningen, se till att du har följande förutsättningar på plats:

- Grundläggande kunskaper i Java-programmering.
-  Aspose.PSD för Java installerat. Du kan ladda ner den[här](https://releases.aspose.com/psd/java/).

## Importera paket

Se till att du har importerat de nödvändiga paketen för att utnyttja Aspose.PSD-funktionerna i din Java-applikation. Använd följande kodavsnitt som vägledning:

```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;


import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.layereffects.DropShadowEffect;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
```

## Steg 1: Ladda PSD-bilden

```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "Shadow.psd";
String psdPathAfterChange = dataDir + "ShadowChanged.psd";

PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);

PsdImage im = (PsdImage)Image.load(sourceFileName, loadOptions);
```

## Steg 2: Hämta skuggeffekt

```java
DropShadowEffect shadowEffect = (DropShadowEffect)(im.getLayers()[1].getBlendingOptions().getEffects()[0]);
```

## Steg 3: Verifiera standardinställningarna

```java
Assert.areEqual(Color.getBlack(), shadowEffect.getColor());
Assert.areEqual(255, shadowEffect.getOpacity());
Assert.areEqual(3, shadowEffect.getDistance());
Assert.areEqual(7, shadowEffect.getSize());
Assert.areEqual(true, shadowEffect.getUseGlobalLight());
Assert.areEqual(90, shadowEffect.getAngle());
Assert.areEqual(0, shadowEffect.getSpread());
Assert.areEqual(0, shadowEffect.getNoise());
```

## Steg 4: Anpassa skuggeffekten

```java
shadowEffect.setColor(Color.getGreen());
shadowEffect.setOpacity((byte)128);
shadowEffect.setDistance(11);
shadowEffect.setUseGlobalLight(false);
shadowEffect.setSize(9);
shadowEffect.setAngle(45);
shadowEffect.setSpread(3);
shadowEffect.setNoise(50);
```

## Steg 5: Spara den ändrade bilden

```java
im.save(psdPathAfterChange);
```

## Slutsats

Med dessa enkla steg kan du enkelt stödja skuggeffekter i Aspose.PSD för Java, vilket förbättrar dina bilders visuella tilltalande.

## FAQ's

### F1: Är Aspose.PSD för Java lämplig för professionella grafiska designprojekt?

A1: Absolut! Aspose.PSD för Java är ett kraftfullt bibliotek designat för professionella grafiska designuppgifter.

### F2: Kan jag använda Aspose.PSD för Java i kommersiella applikationer?

 S2: Ja, Aspose.PSD för Java är en kommersiell produkt. Du kan köpa den[här](https://purchase.aspose.com/buy).

### F3: Finns det en gratis provperiod?

 A3: Ja, du kan utforska en gratis testversion[här](https://releases.aspose.com/).

### F4: Var kan jag hitta detaljerad dokumentation?

 S4: Se den omfattande dokumentationen[här](https://reference.aspose.com/psd/java/).

### F5: Hur kan jag få support för Aspose.PSD för Java?

 S5: Gå med i communityforumet[här](https://forum.aspose.com/c/psd/34) för eventuella supportfrågor.