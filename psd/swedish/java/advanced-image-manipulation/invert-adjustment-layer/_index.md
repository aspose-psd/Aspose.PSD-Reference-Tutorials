---
date: 2026-11-04
description: Lär dig hur du använder Aspose.PSD för Java för att applicera ett invert
  adjustment layer, batch process PSD images och skapa negative image PSD files.
keywords:
- how to use aspose
- batch process psd images
- create negative image psd
- image processing java library
- apply multiple adjustment layers
lastmod: 2026-11-04
linktitle: Invert Adjustment Layer
og_description: Så använder du Aspose.PSD för Java för att lägga till ett invert adjustment
  layer, batch process PSD images och skapa en negative image PSD. Följ den steg‑för‑steg‑guiden.
og_image_alt: Screenshot showing Aspose.PSD Java code adding an invert adjustment
  layer
og_title: Så använder du Aspose.PSD för att lägga till ett invert adjustment layer
  i Java
schemas:
- author: Aspose
  dateModified: '2026-11-04'
  description: Learn how to use Aspose.PSD for Java to apply an invert adjustment
    layer, batch process PSD images, and create negative image PSD files.
  headline: How to use Aspose.PSD to add an invert adjustment layer in Java
  type: TechArticle
- questions:
  - answer: Yes, it supports Java 6.0 and later, including Java 8, 11, and 17.
    question: Is Aspose.PSD compatible with all Java versions?
  - answer: Absolutely. After adding the invert layer you can call `addBrightnessAdjustmentLayer()`,
      `addHueSaturationAdjustmentLayer()`, etc., to stack effects.
    question: Can I apply multiple adjustment layers in a single operation?
  - answer: The complete documentation is available [Aspose.PSD Java API reference](https://reference.aspose.com/psd/java/).
    question: Where can I find the full API reference?
  - answer: Yes, you can download a trial version [Aspose.PSD trial download](https://releases.aspose.com/).
    question: Is there a free trial for Aspose.PSD?
  - answer: Request a temporary license [temporary license request page](https://purchase.aspose.com/temporary-license/).
    question: How do I obtain a temporary license for testing?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- aspose psd
- java image processing
- invert adjustment layer
- batch psd processing
title: Så använder du Aspose.PSD för att lägga till ett invert adjustment layer i
  Java
url: /sv/java/advanced-image-manipulation/invert-adjustment-layer/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Hur man använder Aspose.PSD för att lägga till ett inverteringsjusteringslager i Java

## Introduktion

Om du letar efter ett robust **image processing java library**, är Aspose.PSD för Java ett av de mest mångsidiga alternativen på marknaden. I den här handledningen kommer du att se **hur du använder Aspose** för att infoga ett **Invert Adjustment Layer** i en PSD‑fil, stapla det med andra justeringar och till och med köra operationen på dussintals filer. Oavsett om du bygger ett batch‑processeringsverktyg, en server‑sidig bildtjänst eller en enskild bildredigerare, kommer stegen nedan att ta dig från käll‑PSD till en fullt redigerbar negativ bild på några minuter.

## Snabba svar
- **Vad gör Invert Adjustment Layer?** Det vänder varje RGB‑värde i det valda området, vilket gör bilden till ett fotografiskt negativ.  
- **Vilket bibliotek tillhandahåller den här funktionen?** Aspose.PSD, ett ledande **image processing java library**.  
- **Kan jag stapla det med andra justeringar?** Ja – du kan **apply multiple adjustment layers** såsom Brightness/Contrast, Hue/Saturation, och mer.  
- **Behöver jag en licens för utveckling?** En gratis provversion finns tillgänglig; en licens krävs för produktionsanvändning.  
- **Hur lång tid tar implementeringen?** Vanligtvis under 10 minuter för ett grundläggande användningsfall.

## Vad är Invert Adjustment Layer?

Invert Adjustment Layer är en icke‑destruktiv redigering som vänder färgvärdena för varje pixel den påverkar. Eftersom den ligger ovanpå lagerstacken kan du växla dess synlighet eller ändra dess ordning utan att permanent ändra originalbildens data. Detta är det snabbaste sättet att **create negative image PSD**‑filer eller uppnå ett klassiskt film‑negativt utseende.

## Varför använda Aspose.PSD som ditt image processing java library?

Aspose.PSD stöder **200+ PSD features**, kan läsa och skriva Photoshop‑filer utan att kräva Photoshop, och bearbetar dokument med hundratals sidor med mindre än 500 MB heap‑minne. Det körs på vilken Java‑runtime som helst (Java 6+), vilket gör det idealiskt för **batch process psd images** på Windows-, Linux- eller macOS‑servrar.

## Förutsättningar

Innan du börjar, se till att du har:

1. **Aspose.PSD for Java** – ladda ner den senaste JAR‑filen från den officiella sidan [Aspose.PSD for Java download page](https://releases.aspose.com/psd/java/).  
2. **Java Development Kit** – JDK 6.0 eller senare installerad och konfigurerad i din `PATH`.  

Nu är du redo att skriva koden.

## Importera paket

`PsdImage`‑klassen representerar ett helt Photoshop‑dokument i minnet, medan justerings‑lagerklasserna finns i paketet `com.aspose.psd.layers.adjustments`.

`PsdImage`‑klassen är Aspose.PSD:s top‑nivå‑objekt som kapslar in en PSD‑fils struktur och pixeldata. Importera namnutrymmena, så kan du ladda, redigera och spara PSD‑filer.

## Steg 1: konfigurera dokumentkatalog

Definiera mappen som innehåller din käll‑PSD‑fil och där utdata ska sparas. Att använda absoluta sökvägar undviker `NullPointerException` när arbetskatalogen ändras.

## Steg 2: ladda PSD‑fil

Ladda källfilen i ett `PsdImage`‑objekt. Detta objekt håller hela lagerhierarkin i minnet, vilket möjliggör icke‑destruktiva redigeringar.

`PsdImage`‑klassen erbjuder en statisk `load`‑metod som läser filhuvudet, validerar formatet och konstruerar en in‑memory‑representation klar för manipulation.

## Steg 3: lägg till inverteringsjusteringslager

Anropa den inbyggda metoden för att infoga ett Invert Adjustment Layer ovanpå den aktuella lagerstacken. Du kan senare lägga till fler lager (t.ex. Brightness, Hue) för att **apply multiple adjustment layers** i ett enda arbetsflöde.

`addInvertAdjustmentLayer()` lägger till ett Invert Adjustment Layer i PSD:ens lagerkollektion.

## Steg 4: spara utdata

Spara den modifierade PSD‑filen till disk.  

`save()` skriver PSD‑filen, inklusive alla lager och metadata, till den angivna sökvägen.

Sparandet använder samma `save`‑metod som skriver hela dokumentet, inklusive alla justeringslager, masker och metadata, till det angivna formatet.

### Vad hände just nu?

PSD‑filen laddades in i ett `PsdImage`‑objekt, ett `InvertAdjustmentLayer` skapades och lades till som det översta lagret, och dokumentet sparades. Denna sekvens bevarar originalbildens data samtidigt som den lägger till en icke‑destruktiv inverteringseffekt som kan växlas på/av eller omordnas senare.

Du har nu framgångsrikt använt Aspose.PSD, ett **image processing java library**, för att manipulera en PSD‑fil.

## Hur man batch‑processar PSD‑bilder med inverteringsjustering?

Ladda varje fil i en `for`‑loop, tillämpa samma steg och anropa `save` för varje iteration. Eftersom Aspose.PSD bearbetar filer i ett strömningsläge kan du hantera **hundreds of PSDs** samtidigt som minnesanvändningen hålls under 300 MB genom att återanvända samma `PsdImage`‑instans.

## Hur man konverterar en PSD till en negativ bild?

Lägg till Invert Adjustment Layer som det översta objektet och spara dokumentet – den operationen är ekvivalent med **convert PSD to negative**. Du kan senare inaktivera eller ta bort lagret för att återgå till originalutseendet utan att ladda om källfilen.

## Vanliga problem & tips

| Problem | Orsak | Lösning |
|-------|-------|----------|
| **NullPointerException på `Image.load`** | Felaktig filsökväg eller fil saknas | Verifiera `dataDir` och filnamn; använd absoluta sökvägar för testning |
| **Lagerordning inte som förväntat** | Att lägga till lager efter befintliga förändrar staplingen | Infoga invert‑lagret före andra justeringar, eller ändra ordning via `psdImage.getLayers().move()` |
| **Prestandaförsämring på stora PSD‑filer** | Laddar mycket stora filer i minnet | Öka JVM‑heap (`-Xmx2g`) eller bearbeta filer i delar med `psdImage.getPages().get(0).getResources().setMemoryOptimized(true)` |

## Vanliga frågor

**Q: Är Aspose.PSD kompatibel med alla Java‑versioner?**  
A: Ja, den stöder Java 6.0 och senare, inklusive Java 8, 11 och 17.

**Q: Kan jag tillämpa flera justeringslager i en enda operation?**  
A: Absolut. Efter att ha lagt till invert‑lagret kan du anropa `addBrightnessAdjustmentLayer()`, `addHueSaturationAdjustmentLayer()`, etc., för att stapla effekter.

**Q: Var kan jag hitta den fullständiga API‑referensen?**  
A: Den kompletta dokumentationen finns tillgänglig [Aspose.PSD Java API reference](https://reference.aspose.com/psd/java/).

**Q: Finns det en gratis provversion av Aspose.PSD?**  
A: Ja, du kan ladda ner en provversion [Aspose.PSD trial download](https://releases.aspose.com/).

**Q: Hur får jag en tillfällig licens för testning?**  
A: Begär en tillfällig licens [temporary license request page](https://purchase.aspose.com/temporary-license/).

---

**Senast uppdaterad:** 2026-11-04  
**Testad med:** Aspose.PSD 24.12 för Java  
**Författare:** Aspose  









```java
import com.aspose.psd.Image;

import com.aspose.psd.fileformats.psd.PsdImage;
```

```java
String dataDir = "Your Document Directory";
```

```java
String filePath = dataDir + "InvertStripes_before.psd";
String outputPath = dataDir + "InvertStripes_after.psd";

PsdImage im = (PsdImage)Image.load(filePath);
```

```java
im.addInvertAdjustmentLayer();
```

```java
im.save(outputPath);
```

## Relaterade handledningar

- [Lägg till nivåjusteringslager till PSD‑filer med Aspose.PSD för Java](/psd/java/modifying-converting-psd-images/add-level-adjustment-layer-psd/)
- [Hur man lägger till justeringslager – Channel Mixer i PSD (Java)](/psd/java/modifying-converting-psd-images/add-channel-mixer-adjustment-layer-psd/)
- [Hur man redigerar PSD – Lägg till kurvjusteringslager med Java](/psd/java/modifying-converting-psd-images/add-curves-adjustment-layer-psd/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}