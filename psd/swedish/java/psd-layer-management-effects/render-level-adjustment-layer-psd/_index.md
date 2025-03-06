---
title: Render nivåjusteringslager i PSD-filer - Java
linktitle: Render nivåjusteringslager i PSD-filer - Java
second_title: Aspose.PSD Java API
description: Lär dig hur du enkelt förbättrar bildens kontrast och livlighet med Aspose.PSD för Java. Master Levels Adjustment Layers med denna steg-för-steg-guide.
weight: 17
url: /sv/java/psd-layer-management-effects/render-level-adjustment-layer-psd/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Render nivåjusteringslager i PSD-filer - Java

## Introduktion

Har du någonsin öppnat en PSD-fil bara för att hitta bilden saknar kontrast eller livfullhet? Frukta inte, bildredigeringskrigare! Aspose.PSD för Java kommer till undsättning med dess kraftfulla nivåjusteringslagermanipuleringsmöjligheter. Den här guiden kommer att utrusta dig med kunskapen för att finjustera dina bilder med hjälp av nivåer i en bris. 

## Förutsättningar

- Java Development Kit (JDK): Se till att du har en senaste version av JDK installerad på ditt system. Du kan ladda ner den från Oracles webbplats ([https://www.oracle.com/java/technologies/javase-downloads.html](https://www.oracle.com/java/technologies/javase-downloads.html)).
- Aspose.PSD for Java Library: Ladda ner Aspose.PSD for Java-biblioteket från nedladdningssidan ([https://releases.aspose.com/psd/java/](https://releases.aspose.com/psd/java/)). Du behöver en giltig licens för att använda alla funktioner, men en gratis provperiod är tillgänglig för att komma igång ([https://releases.aspose.com/](https://releases.aspose.com/)).

## Importera paket

Innan vi dyker in i koden måste vi importera de nödvändiga Aspose.PSD-klasserna för att interagera med PSD-filer. Här är vad du behöver:

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.adjustmentlayers.LevelsLayer;
import com.aspose.psd.fileformats.psd.layers.layerresources.LevelChannel;
import com.aspose.psd.imageoptions.PngOptions;
```

 De`com.aspose.psd` paketet ger tillgång till PSD-manipuleringsfunktioner, medan`com.aspose.psd.imaging.PngOptions` tillåter oss att definiera alternativ när du sparar bilden som en PNG.

Låt oss nu ge oss ut på vårt nivåjusteringsäventyr:

## Steg 1: Konfigurera filsökvägar:

- Definiera variabler för din dokumentkatalog (`dataDir`), käll-PSD-filnamn (`sourceFileName`), mål-PSD-filnamn efter ändring (`psdPathAfterChange`), och den sista PNG-exportsökvägen (`pngExportPath`). Överväg att använda beskrivande namn för att förbättra kodläsbarheten.

```java
String dataDir = "Your Document Directory";

String sourceFileName = dataDir + "LevelsAdjustmentLayer.psd";
String psdPathAfterChange = dataDir + "LevelsAdjustmentLayerChanged.psd";
String pngExportPath = dataDir + "LevelsAdjustmentLayerChanged.png";
```

## Steg 2: Ladda PSD-bilden:

-  Använd`Image.load` metod för att öppna käll-PSD-filen och lagra den i en`PsdImage`objekt (`im`). Aspose.PSD känner automatiskt av filformatet.

```java
PsdImage im = (PsdImage)Image.load(sourceFileName);
```

## Steg 3: Iterera genom lager:

- Vi måste hitta nivåjusteringslagret i din PSD. Aspose ger ett bekvämt sätt att iterera genom alla lager med hjälp av en slinga.

```java
for (int i = 0; i < im.getLayers().length; i++) {
   // ... (kod för att kontrollera Levels Layer kommer att läggas till här)
}
```

## Steg 4: Identifiera nivåskiktet:

- Inuti slingan, kontrollera om det aktuella lagret (`im.getLayers()[i]` ) är en instans av`LevelsLayer` klass med hjälp av`instanceof` operatör. 
-  Om det är det, gjuta lagret till a`LevelsLayer` föremål för ytterligare manipulation.

```java
for (int i = 0; i < im.getLayers().length; i++) {
   if (im.getLayers()[i] instanceof LevelsLayer) {
	   LevelsLayer levelsLayer = (LevelsLayer) im.getLayers()[i];
	   // ... (kod för att justera nivåer kommer att läggas till här)
   }
}
```
## Steg 5: Finjustering av nivåer (fortsättning):

-  Justera utgångsnivåerna med`setOutputShadowLevel` och`setOutputHighlightLevel` för att kontrollera mörkret och ljusheten i den resulterande bilden. Dessa värden bestämmer intervallet av ingångsnivåer som kommer att mappas till utgångsområdet.

```java
for (int i = 0; i < im.getLayers().length; i++) {
   if (im.getLayers()[i] instanceof LevelsLayer) {
	   LevelsLayer levelsLayer = (LevelsLayer) im.getLayers()[i];
	   LevelChannel channel = levelsLayer.getChannel(0);

	   // Justera ingångsnivåer (0-255):
	   channel.setInputShadowLevel((short) 10); // Gör skuggorna något mörkare
	   channel.setInputMidtoneLevel(2.0f);     // Öka mellantoner
	   channel.setInputHighlightLevel((short) 230); // Minska höjdpunkter

	   // Justera utnivåer (0-255):
	   channel.setOutputShadowLevel((short) 20); // Mörka skuggorna ytterligare
	   channel.setOutputHighlightLevel((short) 200); //Ljusna upp höjdpunkter
   }
}
```

## Steg 6: Spara den modifierade PSD:en:

-  Använd`save` metod för`PsdImage` objekt för att spara den ändrade bilden till den angivna sökvägen (`psdPathAfterChange`).

```java
im.save(psdPathAfterChange);
```

## Steg 7: Exportera som PNG (valfritt):

-  Om du behöver en PNG-version av den justerade bilden, skapa en`PngOptions` objekt och ställ in färgtypen till`TruecolorWithAlpha` . Använd sedan`save` metod igen med PNG-exportsökvägen och alternativen.

```java
PngOptions saveOptions = new PngOptions();
saveOptions.setColorType(PngColorType.TruecolorWithAlpha);
im.save(pngExportPath, saveOptions);
```

Och där har du det! Du har framgångsrikt justerat nivåjusteringslagret i din PSD-fil med Aspose.PSD för Java. Genom att förstå dessa steg och experimentera med olika värden kan du förbättra kontrasten och det övergripande utseendet på dina bilder.

## Slutsats

Aspose.PSD för Java ger dig möjlighet att ta kontroll över din bildredigeringsprocess. Genom att behärska nivåjusteringslagret kan du blåsa nytt liv i dina foton och mönster. Kom ihåg att övning ger färdighet, så tveka inte att experimentera och utforska den fulla potentialen hos detta kraftfulla verktyg.
 
## FAQ's

### Kan jag justera individuella färgkanaler (RGB) separat? 
Ja, du kan komma åt varje färgkanal med hjälp av`getChannel` metod för`LevelsLayer` objekt och modifiera dess nivåer oberoende.

### Hur hanterar jag flera nivåjusteringslager i en PSD?
Koden itererar genom alla lager, så den kommer automatiskt att bearbeta eventuella ytterligare nivålager som finns i bilden.

### Finns det andra sätt att justera bildkontrasten förutom nivåer?
Absolut! Aspose.PSD erbjuder olika bildjusteringsverktyg som kurvor, ljusstyrka/kontrast och mer.

### Kan jag automatisera den här processen för flera bilder? 
Ja, du kan infoga den här koden i ett loop- eller batchbearbetningsskript för att effektivt bearbeta flera PSD-filer.

### Var kan jag hitta mer information och support?
Aspose tillhandahåller omfattande dokumentation ([https://reference.aspose.com/psd/java/](https://reference.aspose.com/psd/java/)) och ett supportforum ([https://forum.aspose.com/c/psd/34](https://forum.aspose.com/c/psd/34)) för alla frågor eller problem du kan stöta på.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
