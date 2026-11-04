---
date: 2026-11-04
description: Lär dig hur du sparar PSD som PNG, exporterar PNG med alpha, och lägger
  till ett drop shadow‑lager med Aspose.PSD for Java – en komplett, steg‑för‑steg‑guide.
keywords:
- save psd as png
- convert psd to png
- export png with alpha
- batch psd to png
- java image manipulation
lastmod: 2026-11-04
linktitle: Tillämpa Rendering Drop Shadow
og_description: Spara PSD som PNG med Aspose.PSD for Java, exportera PNG med alpha‑transparens,
  och lägg till ett rendering drop shadow—steg‑för‑steg‑guide för Java‑utvecklare.
og_image_alt: Developer guide showing how to convert PSD to PNG and apply drop shadow
  using Aspose.PSD Java
og_title: Spara PSD som PNG och tillämpa rendering drop shadow i Aspose.PSD for Java
schemas:
- author: Aspose
  dateModified: '2026-11-04'
  description: Learn how to save PSD as PNG, export PNG with alpha, and add a drop
    shadow layer using Aspose.PSD for Java – a complete, step‑by‑step guide.
  headline: Save psd as png and apply rendering drop shadow in Aspose.PSD for Java
  type: TechArticle
- description: Learn how to save PSD as PNG, export PNG with alpha, and add a drop
    shadow layer using Aspose.PSD for Java – a complete, step‑by‑step guide.
  name: Save psd as png and apply rendering drop shadow in Aspose.PSD for Java
  steps:
  - name: define document directory
    text: Define the directory path where your PSD files are stored.
  - name: set psd and png file paths
    text: Specify the full file paths for the source PSD and the target PNG.
  - name: load psd file with effects
    text: '`PsdImage` loads the PSD and gives access to its layers and effects.'
  - name: access drop shadow effect
    text: '`DropShadowEffect` represents a drop‑shadow layer effect that can be read
      or modified.'
  - name: validate shadow effect properties
    text: '`shadowEffect` holds the properties of the drop‑shadow such as opacity,
      distance, and size. > **Pro tip:** Adjust `setSpread()` or `setNoise()` to create
      softer or more textured shadows.'
  - name: save as png – the “save psd as png” step
    text: '`PngOptions` configures PNG export settings, including color type and alpha
      channel handling. At this point you have successfully **converted psd to png**,
      **exported png with alpha**, and applied a rendering drop shadow in a single
      workflow.'
  type: HowTo
- questions:
  - answer: Yes. Loop through `im.getLayers()` and add or modify a `DropShadowEffect`
      for each target layer, which also lets you perform a batch psd to png conversion.
    question: Can I apply drop shadows to multiple layers simultaneously?
  - answer: '`Spread` determines how abruptly the shadow transitions from full opacity
      to transparent. A higher value creates a harder edge.'
    question: What does the ‘Spread’ parameter control?
  - answer: Aspose.PSD supports PSD files from Photoshop 3.0 up to the latest release,
      handling most layer types and effects.
    question: Is Aspose.PSD compatible with all Photoshop versions?
  - answer: Download the free trial from the [Aspose.PSD download page](https://releases.aspose.com/psd/java/)
      and run the sample without a license key.
    question: How can I test the code before purchasing a license?
  - answer: Post your question on the [Aspose.PSD forum](https://forum.aspose.com/c/psd/34)
      where the community and Aspose engineers can assist.
    question: Where can I get help if I run into problems?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- save psd as png
- aspose psd java
- java image manipulation
- png transparency
- rendering drop shadow
title: Spara PSD som PNG och tillämpa rendering drop shadow i Aspose.PSD for Java
url: /sv/java/advanced-image-manipulation/rendering-drop-shadow/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Spara psd som png och applicera renderingsskugga i Aspose.PSD för Java

## Introduktion

Om du arbetar med Photoshop‑filer i Java är **saving psd as png** en av de vanligaste uppgifterna du kommer att stöta på. I många projekt behöver du **save psd as png** för att leverera resurser till webben eller mobilappar, samtidigt som du bevarar transparens och visuella effekter. Med Aspose.PSD kan du inte bara **convert psd to png** utan också förbättra bilden genom att **adding a drop shadow layer**. I den här handledningen går vi igenom hela processen — laddar en PSD, applicerar en renderingsskugga och slutligen **saving the PSD as a PNG**‑fil — så att du kan integrera arbetsflödet i dina egna projekt med förtroende.

## Snabba svar
- **Vilket bibliotek hanterar PSD till PNG-konvertering?** Aspose.PSD for Java.  
- **Hur lång tid tar implementeringen av drop‑shadow?** About 10‑15 minutes for a basic example.  
- **Behöver jag en licens för att köra koden?** A free trial works for evaluation; a license is required for production.  
- **Kan jag applicera skuggan på flera lager?** Yes—just loop through the desired layers, which also lets you perform a batch psd to png conversion.  
- **Vilken Java‑version krävs?** Java 8 or higher.

## Vad är “save psd as png” och varför är det viktigt?

**Saving a PSD as PNG creates a widely‑supported, lossless image that retains transparency.** Detta format är avgörande när du behöver visa Photoshop‑resurser på webben, i mobilappar eller som en del av en större bildbehandlingspipeline. Att lägga till en drop shadow samtidigt låter dig skapa en polerad visuell effekt utan att öppna Photoshop.

## Varför använda Aspose.PSD för detta arbetsflöde?

Renderning av lager‑effekter i laddningstid är inbyggd, så du behöver inte Photoshop. Aspose.PSD stöder över 50 in‑ och utdataformat (PSD, PNG, JPEG, TIFF, BMP) och kan bearbeta stora dokument utan att ladda hela filen i minnet. Det bevarar effekter som drop shadows och glows exakt som de visas, och exporterar automatiskt PNG med alfa‑transparens.

## Förutsättningar

- **Java Development Environment** – JDK 8 eller nyare installerat.  
- **Aspose.PSD for Java** – Ladda ner den senaste JAR‑filen från [Aspose.PSD download page](https://releases.aspose.com/psd/java/).  
- **A PSD file** – Filen bör innehålla minst ett lager du vill förbättra med en drop shadow (t.ex. *Shadow.psd*).  

## Importera paket

Namnutrymmet `com.aspose.psd` tillhandahåller kärnklasserna för att ladda bilder, manipulera lager och exportera PNG‑filer. `PsdImage` är huvudklassen som används för att ladda och manipulera PSD‑filer.  

```java
import com.aspose.psd.Image;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.layereffects.DropShadowEffect;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
import com.aspose.psd.Color;

import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.imageoptions.PngOptions;
```

## Steg‑för‑steg‑guide

### Steg 1: definiera dokumentkatalog
Definiera sökvägen till den katalog där dina PSD‑filer lagras.  

```java
String dataDir = "Your Document Directory";
```

### Steg 2: ange psd‑ och png‑filvägar
Ange de fullständiga filvägarna för käll‑PSD‑filen och mål‑PNG‑filen.  

```java
String sourceFileName = dataDir + "Shadow.psd";
String pngExportPath = dataDir + "Shadowchanged1.png";
```

### Steg 3: ladda psd‑fil med effekter
`PsdImage` laddar PSD‑filen och ger åtkomst till dess lager och effekter.  

```java
PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);

PsdImage im = (PsdImage) Image.load(sourceFileName, loadOptions);
```

### Steg 4: åtkomst till drop shadow‑effekt
`DropShadowEffect` representerar en drop‑shadow‑lagereffekt som kan läsas eller modifieras.  

```java
DropShadowEffect shadowEffect = (DropShadowEffect) (im.getLayers()[1].getBlendingOptions().getEffects()[0]);
```

### Steg 5: validera egenskaper för skuggeffekten
`shadowEffect` innehåller egenskaperna för drop‑shadow‑effekten såsom opacitet, avstånd och storlek.  

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

> **Pro tip:** Justera `setSpread()` eller `setNoise()` för att skapa mjukare eller mer strukturerade skuggor.

### Steg 6: spara som png – “save psd as png”-steget
`PngOptions` konfigurerar PNG‑exportinställningarna, inklusive färgtyp och hantering av alfa‑kanal.  

```java
PngOptions saveOptions = new PngOptions();
saveOptions.setColorType(PngColorType.TruecolorWithAlpha);
im.save(pngExportPath, saveOptions);
```

Vid detta tillfälle har du framgångsrikt **converted psd to png**, **exported png with alpha**, och applicerat en renderings‑drop‑shadow i ett enda arbetsflöde.

## Exportera png med alfa‑transparens

När du behöver att PNG‑utdata behåller sin transparenta bakgrund — särskilt för UI‑överlägg eller webb‑grafik — se till att du använder `PngColorType.TruecolorWithAlpha` som visas i sparsteg ovan. Detta garanterar att drop‑shadow ligger på en transparent canvas istället för en solid bakgrund, vilket hjälper dig att **preserve png transparency**.

## Lägg till drop shadow‑lager med Java

Om din PSD innehåller flera lager som kräver skuggor, upprepa helt enkelt **Step 4** och **Step 5** i en loop som itererar över `im.getLayers()`. Varje iteration kan skapa eller modifiera en `DropShadowEffect`‑instans, vilket ger dig fin‑granulerad kontroll över opacitet, avstånd, storlek och vinkel per lager. Detta tillvägagångssätt möjliggör också en **batch psd to png**‑konvertering där varje fil får samma skuggbehandling.

## Vanliga användningsfall för att spara psd som png

* **Web asset pipelines** – Konvertera designer‑levererade PSD‑filer till webb‑klara PNG‑filer med inbyggda skuggor.  
* **Mobile app resources** – Generera transparenta PNG‑ikoner i farten, utan manuell export.  
* **Batch processing** – Automatisera konvertering av hundratals PSD‑filer i ett server‑sidigt jobb, vilket säkerställer att varje PNG behåller sin alfa‑kanal och visuella effekter.  

## Vanliga problem och lösningar

| Problem | Trolig orsak | Lösning |
|-------|--------------|-----|
| **Shadow not visible** | `Opacity` set to 0 or layer is hidden | Verify `shadowEffect.getOpacity()` > 0 and layer visibility. |
| **PNG appears flat (no transparency)** | Wrong `PngColorType` used | Use `PngColorType.TruecolorWithAlpha` as shown. |
| **Exception on loading** | Effects not loaded | Ensure `loadOptions.setLoadEffectsResource(true)` is called. |
| **Incorrect layer index** | PSD structure differs | Inspect `im.getLayers()` and pick the correct index. |

## Vanliga frågor

**Q: Kan jag applicera drop shadows på flera lager samtidigt?**  
A: Ja. Loopa igenom `im.getLayers()` och lägg till eller modifiera en `DropShadowEffect` för varje mål‑lager, vilket också låter dig utföra en batch psd to png‑konvertering.

**Q: Vad styr ‘Spread’-parametern?**  
A: `Spread` bestämmer hur abrupt skuggan övergår från full opacitet till transparent. Ett högre värde skapar en hårdare kant.

**Q: Är Aspose.PSD kompatibel med alla Photoshop‑versioner?**  
A: Aspose.PSD stöder PSD‑filer från Photoshop 3.0 upp till den senaste versionen, och hanterar de flesta lagertyper och effekter.

**Q: Hur kan jag testa koden innan jag köper en licens?**  
A: Ladda ner gratisprovet från [Aspose.PSD download page](https://releases.aspose.com/psd/java/) och kör exemplet utan licensnyckel.

**Q: Var kan jag få hjälp om jag stöter på problem?**  
A: Ställ din fråga på [Aspose.PSD forum](https://forum.aspose.com/c/psd/34) där communityn och Aspose‑ingenjörer kan hjälpa till.

## Slutsats

Du vet nu hur du **save psd as png**, **export png with alpha**, **convert psd to png**, och **apply a drop shadow layer** med Aspose.PSD för Java. Denna kombination låter dig automatisera högkvalitativ bildförberedelse för webb, mobil eller skrivbordsapplikationer — utan att någonsin öppna Photoshop.

---

**Senast uppdaterad:** 2026-11-04  
**Testad med:** Aspose.PSD 24.11 for Java  
**Författare:** Aspose

## Relaterade handledningar

- [Konvertera PSD till PNG med färgöverlagring – Aspose.PSD för Java](/psd/java/advanced-image-manipulation/rendering-color-effect/)
- [Hur man lägger till skugga i PSD med Java – Avancerade lagereffekter](/psd/java/advanced-psd-layer-features-effects/)
- [Hur man konverterar PSD till rasterbildformat med Aspose.PSD för Java](/psd/java/advanced-techniques/convert-psd-to-raster-forms/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}