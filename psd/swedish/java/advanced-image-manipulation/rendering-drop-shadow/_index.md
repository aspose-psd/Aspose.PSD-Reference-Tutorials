---
date: 2026-04-22
description: Lär dig hur du sparar PSD som PNG, exporterar PNG med alfa och lägger
  till ett lager med skuggeffekt med Aspose.PSD för Java – en komplett steg‑för‑steg‑guide.
keywords:
- save psd as png
- convert psd to png
- export png with alpha
- batch psd to png
- preserve png transparency
linktitle: Tillämpa renderingsskugga
second_title: Aspose.PSD Java API
title: Spara PSD som PNG och applicera renderad skugga i Aspose.PSD för Java
url: /sv/java/advanced-image-manipulation/rendering-drop-shadow/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Spara PSD som PNG och tillämpa renderingsskugga i Aspose.PSD för Java

## Introduktion

Om du arbetar med Photoshop‑filer i Java är **saving PSD as PNG** en av de vanligaste uppgifterna du stöter på. I många projekt behöver du **save psd as png** för att leverera resurser till webben eller mobilappar, samtidigt som du bevarar transparens och visuella effekter. Med Aspose.PSD kan du inte bara **convert PSD to PNG** utan också förbättra bilden genom att **adding a drop shadow layer**. I den här handledningen går vi igenom hela processen – laddar en PSD, tillämpar en renderingsskugga och slutligen **saving the PSD as a PNG**‑fil – så att du kan integrera arbetsflödet i dina egna projekt med förtroende.

## Snabba svar
- **Vilket bibliotek hanterar PSD till PNG‑konvertering?** Aspose.PSD for Java.  
- **Hur lång tid tar implementeringen av drop‑shadow?** About 10‑15 minutes for a basic example.  
- **Behöver jag en licens för att köra koden?** A free trial works for evaluation; a license is required for production.  
- **Kan jag tillämpa skuggan på flera lager?** Yes—just loop through the desired layers, which also lets you perform a batch psd to png conversion.  
- **Vilken Java‑version krävs?** Java 8 or higher.

## Vad är “save PSD as PNG” och varför är det viktigt?

**Saving a PSD as PNG** skapar en brett stödjande, förlustfri bild som behåller transparens. Detta är avgörande när du behöver visa Photoshop‑resurser på webben, i mobilappar eller som en del av en större bildbehandlingspipeline. Att lägga till en drop shadow samtidigt låter dig skapa en polerad visuell effekt utan att öppna Photoshop.

## Varför använda Aspose.PSD för detta arbetsflöde?

* **Full control from code** – Ingen behov av att starta Photoshop eller förlita sig på externa verktyg.  
* **Preserves layer effects** – Drop shadows, glows och andra effekter renderas exakt som de visas i originalfilen.  
* **Export PNG with alpha** – PNG‑utdata behåller den transparenta bakgrunden, vilket säkerställer att du **preserve PNG transparency** för UI‑ eller webbbruk.  
* **Cross‑platform** – Fungerar på alla OS som stödjer Java 8+.  

## Förutsättningar

- **Java Development Environment** – JDK 8 eller nyare installerat.  
- **Aspose.PSD for Java** – Ladda ner den senaste JAR‑filen från [Aspose.PSD download page](https://releases.aspose.com/psd/java/).  
- **A PSD file** – Filen bör innehålla minst ett lager du vill förbättra med en drop shadow (t.ex. *Shadow.psd*).  

## Importera paket

Först importerar vi de klasser vi behöver. Detta ger oss åtkomst till bildladdning, lagereffekter och PNG‑exportalternativ.

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

### Steg 1: Definiera dokumentkatalog  
Berätta för programmet var din käll‑PSD finns.

```java
String dataDir = "Your Document Directory";
```

### Steg 2: Ange PSD‑ och PNG‑filvägar  
Ange både inmatnings‑PSD och utdata‑PNG som kommer att innehålla den renderade drop shadow.

```java
String sourceFileName = dataDir + "Shadow.psd";
String pngExportPath = dataDir + "Shadowchanged1.png";
```

### Steg 3: Ladda PSD‑fil med effekter  
Aktivera laddning av effektresurser så att vi kan manipulera drop‑shadow‑effekten.

```java
PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);

PsdImage im = (PsdImage) Image.load(sourceFileName, loadOptions);
```

### Steg 4: Åtkomst till Drop Shadow‑effekt  
Hämta den första drop‑shadow‑effekten från det andra lagret (index 1). Här verifierar eller modifierar vi parametrarna.

```java
DropShadowEffect shadowEffect = (DropShadowEffect) (im.getLayers()[1].getBlendingOptions().getEffects()[0]);
```

### Steg 5: Validera egenskaper för skuggeffekten  
Se till att effektens egenskaper matchar dina förväntningar innan du sparar. Du kan också justera dessa värden för att uppnå ett annat utseende.

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

> **Proffstips:** Justera `setSpread()` eller `setNoise()` för att skapa mjukare eller mer strukturerade skuggor.

### Steg 6: Spara som PNG – “save PSD as PNG”-steget  
Exportera den modifierade bilden till PNG, bevara alfakanalen så att skuggan blandas korrekt.

```java
PngOptions saveOptions = new PngOptions();
saveOptions.setColorType(PngColorType.TruecolorWithAlpha);
im.save(pngExportPath, saveOptions);
```

Vid detta tillfälle har du framgångsrikt **converted PSD to PNG**, **exported PNG with alpha**, och tillämpat en renderingsdrop shadow i ett enda arbetsflöde.

## Exportera PNG med alfa‑transparens

När du behöver att PNG‑utdata behåller sin transparenta bakgrund – särskilt för UI‑överlägg eller webb‑grafik – se till att du använder `PngColorType.TruecolorWithAlpha` som visas i sparsteget ovan. Detta garanterar att drop shadow ligger på en transparent canvas snarare än en solid bakgrund, vilket hjälper dig att **preserve PNG transparency**.

## Lägg till Drop Shadow‑lager med Java

Om din PSD innehåller flera lager som kräver skuggor, upprepa helt enkelt **Step 4** och **Step 5** i en loop som itererar över `im.getLayers()`. Varje iteration kan skapa eller modifiera en `DropShadowEffect`‑instans, vilket ger dig fin‑granulär kontroll över opacitet, avstånd, storlek och vinkel per lager. Detta tillvägagångssätt möjliggör också en **batch psd to png**‑konvertering där varje fil får samma skuggbehandling.

## Vanliga användningsfall för att spara PSD som PNG

* **Web asset pipelines** – Konvertera designer‑tillhandahållna PSD‑filer till webbklara PNG‑filer med inbyggda skuggor.  
* **Mobile app resources** – Generera transparenta PNG‑ikoner i farten, utan manuell export.  
* **Batch processing** – Automatisera konvertering av hundratals PSD‑filer i ett server‑side‑jobb, så att varje PNG behåller sin alfakanal och visuella effekter.  

## Vanliga problem och lösningar

| Problem | Trolig orsak | Lösning |
|-------|--------------|-----|
| **Shadow not visible** | `Opacity` set to 0 or layer is hidden | Verify `shadowEffect.getOpacity()` > 0 and layer visibility. |
| **PNG appears flat (no transparency)** | Wrong `PngColorType` used | Use `PngColorType.TruecolorWithAlpha` as shown. |
| **Exception on loading** | Effects not loaded | Ensure `loadOptions.setLoadEffectsResource(true)` is called. |
| **Incorrect layer index** | PSD structure differs | Inspect `im.getLayers()` and pick the correct index. |

## Vanliga frågor

**Q: Kan jag tillämpa drop shadows på flera lager samtidigt?**  
A: Ja. Loop through `im.getLayers()` and add or modify a `DropShadowEffect` for each target layer, which also lets you perform a batch psd to png conversion.

**Q: Vad styr ‘Spread’-parametern?**  
A: `Spread` determines how abruptly the shadow transitions from full opacity to transparent. A higher value creates a harder edge.

**Q: Är Aspose.PSD kompatibel med alla Photoshop‑versioner?**  
A: Aspose.PSD supports PSD files from Photoshop 3.0 up to the latest version, handling most layer types and effects.

**Q: Hur kan jag testa koden innan jag köper en licens?**  
A: Download the free trial from the [Aspose.PSD download page](https://releases.aspose.com/psd/java/) and run the sample without a license key.

**Q: Var kan jag få hjälp om jag stöter på problem?**  
A: Post your question on the [Aspose.PSD forum](https://forum.aspose.com/c/psd/34) where the community and Aspose engineers can assist.

## Slutsats

Du vet nu hur du **save psd as png**, **export PNG with alpha**, **convert PSD to PNG**, och **apply a drop shadow layer** med Aspose.PSD för Java. Denna kombination låter dig automatisera högkvalitativ bildförberedelse för webb, mobil eller skrivbordsapplikationer – utan att någonsin öppna Photoshop.

---

**Senast uppdaterad:** 2026-04-22  
**Testad med:** Aspose.PSD 24.11 for Java  
**Författare:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}