---
date: 2026-03-07
description: Lär dig hur du justerar nivåer genom att lägga till ett nivåjusteringslager
  i PSD-filer med Aspose.PSD för Java. Bemästra tonjusteringar snabbt.
linktitle: Add Level Adjustment Layer in PSD
second_title: Aspose.PSD Java API
title: Hur man justerar nivåer – Lägg till ett nivåjusteringslager i PSD
url: /sv/java/modifying-converting-psd-images/add-level-adjustment-layer-psd/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Lägg till nivåjusteringslager i PSD

## Introduction
Om du vill **hur man justerar nivåer** i dina Photoshop‑dokument är nivåjusteringslagret det perfekta verktyget. Det låter dig finjustera skuggor, mellantoner och högdagrar utan att permanent ändra de ursprungliga pixlarna. I den här handledningen går vi igenom hur du lägger till ett nivåjusteringslager i en PSD‑fil med Aspose.PSD för Java, så att du kan uppnå professionell tonkontroll på bara några steg.

## Quick Answers
- **What does a Level Adjustment Layer do?** Det modifierar bildens tonomfång på ett icke‑destruktivt sätt.  
- **Which library is used?** Aspose.PSD för Java.  
- **Do I need a license?** En gratis provversion fungerar för utveckling; en licens krävs för produktion.  
- **How long does the implementation take?** Ungefär 10‑15 minuter för en grundläggande justering.  
- **Can I adjust multiple channels?** Ja, du kan ställa in in‑/utgångsnivåer för varje färgkanal individuellt.

## What is a Level Adjustment Layer?
Ett nivåjusteringslager låter dig korrigera den tonala balansen i en bild genom att justera in‑skuggor, mellantoner och högdagrar samt utgångsnivåer. Eftersom det finns på ett eget lager kan du slå på/av dess synlighet eller radera det utan att påverka det underliggande konstverket.

## Why add a Level Adjustment Layer with Aspose.PSD?
- **Automation:** Integrera nivåjusteringar i batch‑bearbetningspipelines.  
- **Cross‑platform:** Fungerar på alla OS som stödjer Java.  
- **Precision:** Åtkomst till varje kanals inställningar programatiskt för exakta resultat.  

## Prerequisites
1. Java Development Kit (JDK). Om du inte har det, ladda ner det från [Oracle website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html) eller använd OpenJDK.  
2. Aspose.PSD för Java‑bibliotek – hämta den senaste JAR‑filen från denna [download link](https://releases.aspose.com/psd/java/).  
3. Grundläggande kunskap i Java‑programmering.  
4. En IDE som IntelliJ IDEA, Eclipse eller NetBeans med Aspose.PSD‑JAR‑filen tillagd i projektets classpath.

## Import Packages
Innan vi börjar skriva kod behöver vi importera de nödvändiga paketen från Aspose.PSD‑biblioteket. Så här gör du:
```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.adjustmentlayers.LevelsLayer;
import com.aspose.psd.fileformats.psd.layers.layerresources.LevelChannel;
```
Dessa importeringar ger oss åtkomst till klasser för att ladda PSD‑filer, arbeta med nivåjusteringslager och manipulera individuella kanalinställningar.

## How to Adjust Levels in a PSD File
Nedan följer en steg‑för‑steg‑guide som visar exakt **hur man justerar nivåer** programatiskt.

### Step 1: Set Up Your File Paths
Definiera var käll‑PSD‑filen finns och var den redigerade filen ska sparas.
```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "LevelsAdjustmentLayer.psd";
String psdPathAfterChange = dataDir + "LevelsAdjustmentLayerChanged.psd";
```
Byt ut `"Your Document Directory"` mot den faktiska mappen på din maskin.

### Step 2: Load the PSD File
Skapa en `PsdImage`‑instans från källfilen.
```java
PsdImage im = (PsdImage) Image.load(sourceFileName);
```
Nu har du full åtkomst till alla lager i PSD‑filen.

### Step 3: Iterate Through the Layers
Hitta det nivåjusteringslager du vill modifiera.
```java
for (int i = 0; i < im.getLayers().length; i++) {
    if (im.getLayers()[i] instanceof LevelsLayer) {
        LevelsLayer levelsLayer = (LevelsLayer) im.getLayers()[i];
        // Further manipulation will go here...
    }
}
```
Kontrollen `instanceof LevelsLayer` säkerställer att vi bara arbetar med nivåjusteringslager.

### Step 4: Adjust the Level Channel Settings
Finjustera in‑ och utgångsvärdena för den valda kanalen.
```java
LevelChannel channel = levelsLayer.getChannel(0);
channel.setInputMidtoneLevel(2.0f);
channel.setInputShadowLevel((short) 10);
channel.setInputHighlightLevel((short) 230);
channel.setOutputShadowLevel((short) 20);
channel.setOutputHighlightLevel((short) 200);
```
- **Input Midtone Level:** Förskjuter mellantonsområdet.  
- **Input Shadow Level:** Gör skuggor mörkare eller ljusare.  
- **Input Highlight Level:** Styr de ljusaste delarna.  
- **Output Shadow/Highlight Levels:** Definierar det slutgiltiga utgångsområdet.

Känn dig fri att experimentera med olika värden för att se hur de påverkar bilden.

### Step 5: Save the Modified PSD File
Spara dina ändringar till en ny fil.
```java
im.save(psdPathAfterChange);
```
Den uppdaterade PSD‑filen hittar du på den plats du angav i `psdPathAfterChange`.

## Common Issues and Solutions
- **File not found:** Kontrollera att `dataDir` pekar på rätt mapp och att käll‑PSD‑filen finns.  
- **ClassCastException:** Säkerställ att filen du laddar faktiskt är en PSD; andra format kräver andra klasser.  
- **License errors:** Använd en giltig Aspose.PSD‑licens för produktionsbyggen; provversionen fungerar för utveckling.

## Conclusion
Du vet nu **hur man justerar nivåer** genom att lägga till och konfigurera ett nivåjusteringslager i en PSD‑fil med Aspose.PSD för Java. Denna teknik ger dig exakt kontroll över den tonala balansen samtidigt som ditt arbetsflöde förblir helt automatiserat. Fortsätt experimentera med olika kanalvärden och utforska batch‑bearbetning för att applicera samma justeringar på flera bilder.

## Frequently Asked Questions

**Q: What is a Level Adjustment Layer?**  
A: Det är ett icke‑destruktivt lager som låter dig ändra bildens tonomfång (skuggor, mellantoner, högdagrar).

**Q: Can I use Aspose.PSD without purchasing a license?**  
A: Ja, du kan utvärdera biblioteket med en gratis provversion, men en licens krävs för kommersiell distribution.

**Q: Where can I find documentation for Aspose.PSD?**  
A: Du hittar dokumentationen [here](https://reference.aspose.com/psd/java/).

**Q: Is there community support for Aspose products?**  
A: Absolut! Du kan ställa frågor och få hjälp i [Aspose forum](https://forum.aspose.com/c/psd/34).

**Q: How can I get a temporary license for Aspose.PSD?**  
A: Du kan ansöka om en tillfällig licens [here](https://purchase.aspose.com/temporary-license/).

---

**Last Updated:** 2026-03-07  
**Tested With:** Aspose.PSD latest version (Java)  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}