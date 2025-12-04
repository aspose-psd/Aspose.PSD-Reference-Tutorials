---
date: 2025-12-04
description: Lär dig hur du sparar PSD som PNG och applicerar en renderingsskugga
  med Aspose.PSD för Java. Denna guide täcker hur du lägger till skugga, konverterar
  PSD till PNG och applicerar en drop shadow i Java.
language: sv
linktitle: Apply Rendering Drop Shadow
second_title: Aspose.PSD Java API
title: Spara PSD som PNG och lägg till skuggeffekt med Aspose.PSD Java
url: /java/advanced-image-manipulation/rendering-drop-shadow/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Spara PSD som PNG & Lägg till skugga med Aspose.PSD Java

## Introduktion

Om du arbetar med Photoshop‑filer i Java är **saving PSD as PNG** medan du lägger till en professionellt utseende skugga ett vanligt krav. Aspose.PSD gör denna uppgift enkel, så att du kan **convert PSD to PNG** och **apply drop shadow Java** på bara några rader kod. I den här handledningen går vi igenom hela processen, från att ladda en PSD‑fil till att exportera den slutgiltiga PNG‑filen med en renderad skuggeffekt.

## Snabba svar
- **What does “save PSD as PNG” mean?** Det konverterar en lagerbaserad Photoshop‑fil till en platt PNG‑bild, med bibehållen transparens.  
- **Can I add a drop shadow while converting?** Ja—Aspose.PSD låter dig modifiera lag‑effekter innan export.  
- **Do I need a license to run the code?** En gratis provversion fungerar för utvärdering; en licens krävs för produktion.  
- **Which Java version is supported?** Java 8 eller högre.  
- **Is the drop‑shadow effect customizable?** Absolut—du kan justera färg, opacitet, avstånd, storlek, vinkel och mer.

## Förutsättningar

Innan vi dyker ner, se till att du har:

- **Java Development Environment** – JDK 8 eller nyare installerat.  
- **Aspose.PSD Library** – Ladda ner den senaste JAR‑filen från den officiella webbplatsen [here](https://releases.aspose.com/psd/java/).  
- **A PSD file** – En fil som innehåller minst ett lager du vill förbättra med en skugga.  

## Hur sparar man PSD som PNG med en skugga i Java?

Nedan är en steg‑för‑steg‑guide. Varje steg innehåller en kort förklaring följt av den exakta koden du behöver kopiera.

### Steg 1: Importera de nödvändiga paketen

Vi börjar med att importera klasserna som tillhandahåller bildladdning, effekt‑hantering och PNG‑exportfunktioner.

```java
import com.aspose.psd.Image;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.layereffects.DropShadowEffect;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
import com.aspose.psd.Color;

import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.imageoptions.PngOptions;
```

### Steg 2: Definiera dokumentkatalogen

Ange mappen där din käll‑PSD och den resulterande PNG‑filen kommer att ligga.

```java
String dataDir = "Your Document Directory";
```

### Steg 3: Ange PSD‑ och PNG‑filvägar

Specificera de fullständiga sökvägarna för indata‑PSD och utdata‑PNG.

```java
String sourceFileName = dataDir + "Shadow.psd";
String pngExportPath = dataDir + "Shadowchanged1.png";
```

### Steg 4: Ladda PSD‑filen med effekter aktiverade

Att aktivera **loadEffectsResource** säkerställer att lag‑effekter (som skuggor) är tillgängliga för manipulation.

```java
PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);

PsdImage im = (PsdImage) Image.load(sourceFileName, loadOptions);
```

### Steg 5: Åtkomst till Drop Shadow‑effekten

Här hämtar vi den första effekten som applicerats på det andra lagret (index 1). Detta är där vi kommer att läsa eller modifiera skuggegenskaperna.

```java
DropShadowEffect shadowEffect = (DropShadowEffect) (im.getLayers()[1].getBlendingOptions().getEffects()[0]);
```

### Steg 6: Validera skuggeffektens egenskaper (valfritt men användbart)

Att kontrollera de befintliga egenskaperna hjälper dig att avgöra om du behöver ändra något. Påståendena nedan bekräftar standardvärdena.

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

> **Pro tip:** Om du vill **how to add shadow** med anpassade inställningar, modifiera egenskaperna på `shadowEffect` innan du sparar (t.ex. `shadowEffect.setColor(Color.getRed());`).

### Steg 7: Spara den modifierade bilden som PNG

Slutligen exporterar vi PSD‑filen (med den renderade skuggan) till en PNG‑fil. Alternativet `TruecolorWithAlpha` bevarar transparens.

```java
PngOptions saveOptions = new PngOptions();
saveOptions.setColorType(PngColorType.TruecolorWithAlpha);
im.save(pngExportPath, saveOptions);
```

Och där har du det—ett komplett **convert PSD to PNG** arbetsflöde som också **apply drop shadow java** i ett enda steg.

## Varför använda Aspose.PSD för denna uppgift?

- **No native Photoshop required** – Fungerar på alla plattformar som stödjer Java.  
- **Full PSD fidelity** – All lagerinformation, masker och effekter bevaras.  
- **Fine‑grained control** – Justera varje parameter för drop shadow innan export.  
- **High performance** – Optimerad för stora filer och batch‑bearbetning.

## Vanliga problem & felsökning

| Symptom | Trolig orsak | Åtgärd |
|---------|--------------|--------|
| `NullPointerException` på `shadowEffect` | Mållagret har inga effekter eller index är fel. | Verifiera lagerindex (`im.getLayers()[i]`) och säkerställ att en effekt finns. |
| Exporterad PNG är tom | PNG‑alternativ är inte korrekt inställda eller bilden sparas inte. | Använd `PngColorType.TruecolorWithAlpha` och bekräfta att sökvägen för `im.save()` är skrivbar. |
| Skuggfärgen är inte synlig | Skuggopaciteten är satt till 0 eller färgen matchar bakgrunden. | Sätt `shadowEffect.setOpacity(255);` och välj en kontrasterande färg. |

## Vanliga frågor

**Q: Kan jag applicera skuggor på flera lager samtidigt?**  
A: Ja. Loopa igenom `im.getLayers()` och modifiera varje lagers `DropShadowEffect` efter behov.

**Q: Vad gör parametern ‘Spread’?**  
A: Den styr hur skarpt skuggan övergår från helt opak till transparent. En högre spread ger en hårdare kant.

**Q: Är Aspose.PSD kompatibel med alla Photoshop‑versioner?**  
A: Det stödjer ett brett spektrum av PSD‑versioner, från tidiga releaser upp till de senaste Photoshop CC‑filerna.

**Q: Hur kan jag få hjälp om jag stöter på problem?**  
A: Besök [Aspose.PSD‑forumet](https://forum.aspose.com/c/psd/34) för community‑support och officiell assistans.

**Q: Kan jag prova Aspose.PSD innan jag köper?**  
A: Absolut. Ladda ner en gratis provversion från [Aspose‑webbplatsen](https://releases.aspose.com/).

---

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

**Senast uppdaterad:** 2025-12-04  
**Testad med:** Aspose.PSD 24.12 för Java  
**Författare:** Aspose  

---