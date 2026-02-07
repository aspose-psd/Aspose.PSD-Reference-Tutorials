---
date: 2026-02-07
description: Lär dig hur du sparar PSD som PNG, exporterar PNG med alfa och lägger
  till ett skugglager med Aspose.PSD för Java – en komplett steg‑för‑steg‑guide.
linktitle: Apply Rendering Drop Shadow
second_title: Aspose.PSD Java API
title: Spara PSD som PNG och tillämpa renderingsskugga i Aspose.PSD för Java
url: /sv/java/advanced-image-manipulation/rendering-drop-shadow/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Spara PSD som PNG och applicera renderingsskugga i Aspose.PSD för Java

## Introduktion

Om du arbetar med Photoshop‑filer i Java är **saving PSD as PNG** en av de vanligaste uppgifterna du kommer att stöta på. Med Aspose.PSD kan du inte bara **convert PSD to PNG** utan också förbättra bilden genom att **adding a drop shadow layer**. I den här handledningen går vi igenom hela processen – att ladda en PSD, applicera en rendering drop shadow och slutligen **saving the PSD as a PNG**‑fil – så att du kan integrera arbetsflödet i dina egna projekt med självförtroende.

## Snabba svar
- **Vilket bibliotek hanterar PSD till PNG-konvertering?** Aspose.PSD for Java.  
- **Hur lång tid tar implementeringen av drop‑shadow?** Ungefär 10‑15 minuter för ett grundexempel.  
- **Behöver jag en licens för att köra koden?** En gratis provversion fungerar för utvärdering; en licens krävs för produktion.  
- **Kan jag applicera skuggan på flera lager?** Ja—loopa bara igenom önskade lager.  
- **Vilken Java‑version krävs?** Java 8 eller högre.

## Vad är “save PSD as PNG” och varför är det viktigt?

Att spara en PSD som PNG skapar en brett stödjande, förlustfri bild som behåller transparens. Detta är avgörande när du behöver visa Photoshop‑tillgångar på webben, i mobilappar eller som en del av en större bild‑behandlingspipeline. Att samtidigt lägga till en drop shadow låter dig producera en polerad visuell effekt utan att öppna Photoshop.

## Varför använda Aspose.PSD för detta arbetsflöde?

* **Full kontroll från kod** – Ingen behov av att starta Photoshop eller förlita sig på externa verktyg.  
* **Bevarar lagereffekter** – Drop shadows, glows och andra effekter renderas exakt som de visas i originalfilen.  
* **Exportera PNG med alfa** – PNG‑utdata behåller den transparenta bakgrunden, vilket gör den klar för webb eller UI‑användning.  
* **Plattformsoberoende** – Fungerar på alla OS som stödjer Java 8+.

## Förutsättningar

Innan vi dyker ner, se till att du har:

- **Java‑utvecklingsmiljö** – JDK 8 eller nyare installerat.  
- **Aspose.PSD for Java** – Ladda ner den senaste JAR‑filen från [Aspose.PSD download page](https://releases.aspose.com/psd/java/).  
- **En PSD‑fil** – Filen bör innehålla minst ett lager du vill förbättra med en drop shadow (t.ex. *Shadow.psd*).  

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
Ange både inmatnings‑PSD och utdata‑PNG som kommer att innehålla den renderade drop‑shadow.

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

### Steg 5: Validera skuggeffektens egenskaper  
Se till att effektens egenskaper matchar vad du förväntar dig innan du sparar. Du kan också justera dessa värden för att uppnå ett annat utseende.

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

Vid detta tillfälle har du framgångsrikt **konverterat PSD till PNG**, **exporterat PNG med alfa**, och applicerat en renderings‑drop‑shadow i ett enda arbetsflöde.

## Exportera PNG med alfa‑transparens

När du behöver att PNG‑utdata behåller sin transparenta bakgrund—särskilt för UI‑överlägg eller webb‑grafik—se till att du använder `PngColorType.TruecolorWithAlpha` som visas i sparsteget ovan. Detta garanterar att drop‑shadow ligger på en transparent canvas snarare än en solid bakgrund.

## Lägg till Drop Shadow‑lager med Java

Om din PSD innehåller flera lager som kräver skuggor, upprepa helt enkelt **Steg 4** och **Steg 5** inom en loop som itererar över `im.getLayers()`. Varje iteration kan skapa eller modifiera en `DropShadowEffect`‑instans, vilket ger dig fin‑granulerad kontroll över opacitet, avstånd, storlek och vinkel per lager.

## Java Convert Photoshop PNG – Vanliga användningsfall

* **Webb‑tillgångspipelines** – Konvertera designer‑tillhandahållna PSD‑filer till webbklara PNG‑filer med inbyggda skuggor.  
* **Mobila app‑resurser** – Generera transparenta PNG‑ikoner i farten, undvik manuell export.  
* **Batch‑behandling** – Automatisera konvertering av hundratals PSD‑filer i ett server‑sidigt jobb.

## Vanliga problem och lösningar

| Problem | Trolig orsak | Lösning |
|-------|--------------|-----|
| **Skugga syns inte** | `Opacity` är satt till 0 eller lagret är dolt | Verifiera att `shadowEffect.getOpacity()` > 0 och att lagret är synligt. |
| **PNG ser platt ut (ingen transparens)** | Fel `PngColorType` använd | Använd `PngColorType.TruecolorWithAlpha` som visat. |
| **Undantag vid laddning** | Effekter inte laddade | Säkerställ att `loadOptions.setLoadEffectsResource(true)` anropas. |
| **Fel lagerindex** | PSD‑strukturen skiljer sig | Inspektera `im.getLayers()` och välj rätt index. |

## Vanliga frågor

**Q: Kan jag applicera skuggor på flera lager samtidigt?**  
A: Ja. Loopa igenom `im.getLayers()` och lägg till eller modifiera en `DropShadowEffect` för varje mål‑lager.

**Q: Vad styr parametern ‘Spread’?**  
A: `Spread` bestämmer hur abrupt skuggan övergår från full opacitet till transparent. Ett högre värde skapar en hårdare kant.

**Q: Är Aspose.PSD kompatibel med alla Photoshop‑versioner?**  
A: Aspose.PSD stödjer PSD‑filer från Photoshop 3.0 upp till den senaste versionen och hanterar de flesta lagertyper och effekter.

**Q: Hur kan jag testa koden innan jag köper en licens?**  
A: Ladda ner den gratis provversionen från [Aspose.PSD download page](https://releases.aspose.com/psd/java/) och kör exemplet utan en licensnyckel.

**Q: Var kan jag få hjälp om jag stöter på problem?**  
A: Ställ din fråga på [Aspose.PSD forum](https://forum.aspose.com/c/psd/34) där communityn och Aspose‑ingenjörer kan hjälpa till.

## Slutsats

Du vet nu hur du **save PSD as PNG**, **export PNG with alpha**, **convert Photoshop PNG**‑filer och **apply a drop shadow layer** med Aspose.PSD för Java. Denna kombination låter dig automatisera högkvalitativ bildförberedelse för webb, mobil eller skrivbordsapplikationer—utan att någonsin öppna Photoshop.

---

**Last Updated:** 2026-02-07  
**Tested With:** Aspose.PSD 24.11 for Java  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}