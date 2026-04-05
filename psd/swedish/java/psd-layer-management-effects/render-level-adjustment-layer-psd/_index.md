---
date: 2026-04-05
description: Lär dig hur du exporterar PSD till PNG och enkelt förbättrar bildkontrasten
  med Aspose.PSD för Java. Bemästra nivåjusteringslager med den här steg‑för‑steg‑guiden.
keywords:
- export psd to png
- how to adjust levels
- batch process psd files
linktitle: Exportera PSD till PNG och rendera nivåjusteringslager i Java
second_title: Aspose.PSD Java API
title: Exportera PSD till PNG och rendera nivåjusteringslager i Java
url: /sv/java/psd-layer-management-effects/render-level-adjustment-layer-psd/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Exportera PSD till PNG och rendera nivåjusteringslager i Java

## Introduktion

Har du någonsin öppnat en PSD‑fil och märkt att färgerna ser platta ut eller att kontrasten är fel? Du kan snabbt **export PSD to PNG** samtidigt som du fin‑justerar bilden med ett Levels Adjustment Layer med hjälp av Aspose.PSD för Java. I den här handledningen går vi igenom hela processen — från att ladda en PSD, justera dess nivåer, till att spara resultatet som en PNG — så att du kan öka färgstyrkan och förbereda webbklara resurser på några minuter.

## Snabba svar
- **Vad betyder “export PSD to PNG”?** Den konverterar ett Photoshop‑dokument till en förlustfri PNG‑bild samtidigt som transparensen bevaras.  
- **Kan jag justera nivåer innan export?** Ja, Aspose.PSD låter dig modifiera in‑ och utdata‑nivåer programatiskt.  
- **Behöver jag en licens?** En gratis provversion fungerar för utveckling; en kommersiell licens krävs för produktion.  
- **Är batch‑behandling möjlig?** Absolut — du kan placera koden i en loop för att hantera flera PSD‑filer.  
- **Vilken Java‑version krävs?** Java 8 eller nyare rekommenderas.

## Vad är “export PSD to PNG”?
Att exportera en PSD till PNG innebär att ta den lagerbaserade Photoshop‑filen och platta till den till en Portable Network Graphics‑bild. PNG stöder förlustfri kompression och en alfakanal, vilket gör den idealisk för webb‑grafik och UI‑resurser.

## Varför justera nivåer innan export?
Att justera nivåer låter dig kontrollera skuggor, mellantoner och högdagrar, vilket förbättrar den övergripande kontrasten och färgbalansen. Detta steg säkerställer att den slutliga PNG‑filen ser polerad ut utan behov av manuell redigering i Photoshop.

## Förutsättningar

- **Java Development Kit (JDK)** – ladda ner den senaste versionen från Oracles webbplats ([https://www.oracle.com/java/technologies/javase-downloads.html](https://www.oracle.com/java/technologies/javase-downloads.html)).  
- **Aspose.PSD for Java Library** – hämta den från den officiella nedladdningssidan ([https://releases.aspose.com/psd/java/](https://releases.aspose.com/psd/java/)). En gratis provversion finns ([https://releases.aspose.com/](https://releases.aspose.com/)).  

## Importera paket

Innan du dyker ner i koden, importera klasserna som ger oss åtkomst till PSD‑manipulation och PNG‑export:

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.adjustmentlayers.LevelsLayer;
import com.aspose.psd.fileformats.psd.layers.layerresources.LevelChannel;
import com.aspose.psd.imageoptions.PngOptions;
```

## Steg‑för‑steg‑guide

### Steg 1: Definiera filsökvägar (Hur man automatiserar PSD‑behandling)

Ange tydliga, beskrivande variabler för käll‑PSD, den modifierade PSD‑filen och den slutliga PNG‑exportplatsen.

```java
String dataDir = "Your Document Directory";

String sourceFileName = dataDir + "LevelsAdjustmentLayer.psd";
String psdPathAfterChange = dataDir + "LevelsAdjustmentLayerChanged.psd";
String pngExportPath = dataDir + "LevelsAdjustmentLayerChanged.png";
```

### Steg 2: Ladda PSD‑bilden

Använd `Image.load` för att läsa PSD‑filen till ett `PsdImage`‑objekt. Aspose.PSD upptäcker automatiskt formatet.

```java
PsdImage im = (PsdImage)Image.load(sourceFileName);
```

### Steg 3: Iterera genom lager (Hur man justerar nivåer)

Loopa igenom varje lager för att hitta Levels Adjustment Layer.

```java
for (int i = 0; i < im.getLayers().length; i++) {
   // ... (code to check for Levels Layer will be added here)
}
```

### Steg 4: Identifiera nivålagret

Kontrollera varje lager med `instanceof LevelsLayer`. När det hittas, kasta det så att vi kan ändra dess egenskaper.

```java
for (int i = 0; i < im.getLayers().length; i++) {
   if (im.getLayers()[i] instanceof LevelsLayer) {
	   LevelsLayer levelsLayer = (LevelsLayer) im.getLayers()[i];
	   // ... (code to adjust levels will be added here)
   }
}
```

### Steg 5: Finjustera nivåer (Hur man justerar nivåer)

Justera både in‑ och utdata‑nivåer för den första kanalen (vanligtvis den sammansatta kanalen). Dessa värden är exempel; känn dig fri att experimentera.

```java
for (int i = 0; i < im.getLayers().length; i++) {
   if (im.getLayers()[i] instanceof LevelsLayer) {
	   LevelsLayer levelsLayer = (LevelsLayer) im.getLayers()[i];
	   LevelChannel channel = levelsLayer.getChannel(0);

	   // Adjust Input Levels (0‑255):
	   channel.setInputShadowLevel((short) 10); // Darken shadows slightly
	   channel.setInputMidtoneLevel(2.0f);     // Increase midtones
	   channel.setInputHighlightLevel((short) 230); // Reduce highlights

	   // Adjust Output Levels (0‑255):
	   channel.setOutputShadowLevel((short) 20); // Darken shadows further
	   channel.setOutputHighlightLevel((short) 200); // Brighten highlights
   }
}
```

### Steg 6: Spara den modifierade PSD‑filen (Hur man automatiserar PSD)

Spara ändringarna till en ny PSD‑fil.

```java
im.save(psdPathAfterChange);
```

### Steg 7: Exportera som PNG (Export PSD to PNG)

Om du behöver en PNG‑version, konfigurera `PngOptions` och spara bilden.

```java
PngOptions saveOptions = new PngOptions();
saveOptions.setColorType(PngColorType.TruecolorWithAlpha);
im.save(pngExportPath, saveOptions);
```

## Vanliga användningsfall

- **Förberedelse av webbresurser:** Konvertera designer‑levererade PSD‑mockups till PNG‑filer som är klara för webbläsare.  
- **Batch‑behandling:** Automatisera konverteringen av dussintals PSD‑filer i en CI‑pipeline.  
- **Dynamisk bildgenerering:** Justera nivåer i realtid baserat på användarinmatning innan export.

## Felsökning & tips

- **Null‑pekare vid åtkomst av lager:** Säkerställ att PSD‑filen faktiskt innehåller ett Levels Adjustment Layer; annars lägg till en null‑kontroll.  
- **Oväntade färger efter export:** Verifiera att PNG‑färgt typen är inställd på `TruecolorWithAlpha` för att behålla transparensen.  
- **Prestanda med många filer:** Återanvänd samma `PsdImage`‑instans när du bearbetar en batch för att minska minnesanvändning.

## Vanliga frågor

**Q: Kan jag justera enskilda färgkanaler (RGB) separat?**  
A: Ja. Använd `levelsLayer.getChannel(index)` där `index` = 0 (Röd), 1 (Grön), 2 (Blå) för att justera varje kanal oberoende.

**Q: Hur hanterar jag flera Levels Adjustment Layers i en PSD?**  
A: Loopen bearbetar varje lager; varje `LevelsLayer` som hittas kommer att justeras enligt koden i `if`‑blocket.

**Q: Finns det andra sätt att förbättra kontrasten än Levels?**  
A: Aspose.PSD erbjuder även Curves, Brightness/Contrast och Histogram Equalization‑justeringar.

**Q: Kan jag automatisera detta för en mapp med PSD‑filer?**  
A: Inneslut hela arbetsflödet i en `File[] files = new File(dataDir).listFiles((d, name) -> name.endsWith(".psd"));`‑loop och bearbeta varje fil sekventiellt.

**Q: Var kan jag hitta mer dokumentation och support?**  
A: Besök den officiella referensen ([https://reference.aspose.com/psd/java/](https://reference.aspose.com/psd/java/)) och community‑forumet ([https://forum.aspose.com/c/psd/34](https://forum.aspose.com/c/psd/34)).

## Slutsats

Genom att behärska **export PSD to PNG**‑arbetsflödet och lära dig **how to adjust levels** programatiskt får du full kontroll över bildkvaliteten utan att lämna din Java‑miljö. Oavsett om du förbereder resurser för webben, automatiserar en design‑pipeline eller bygger en batch‑processor, gör Aspose.PSD för Java jobbet enkelt och pålitligt.

---

**Last Updated:** 2026-04-05  
**Tested With:** Aspose.PSD 24.11 for Java  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}