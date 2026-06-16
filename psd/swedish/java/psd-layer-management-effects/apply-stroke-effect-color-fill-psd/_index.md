---
date: 2026-04-03
description: Lär dig hur du sparar PSD som PNG med en kontureffekt och färgfyllning
  med Aspose.PSD för Java. Denna steg‑för‑steg‑guide visar hur du snabbt exporterar
  PSD till PNG.
keywords:
- save psd as png
- export psd to png
- set stroke color
- apply layer effects
- customize stroke width
linktitle: Spara PSD som PNG med kontureffekt – Java
second_title: Aspose.PSD Java API
title: Spara PSD som PNG med kontureffekt – Java
url: /sv/java/psd-layer-management-effects/apply-stroke-effect-color-fill-psd/
weight: 21
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Spara PSD som PNG med kontureffekt och färgfyllning – Java

## Introduktion

I den här guiden kommer du att lära dig hur du **sparar PSD som PNG** samtidigt som du applicerar en kontureffekt med en färgfyllning med Aspose.PSD för Java. Oavsett om du är en erfaren utvecklare eller precis har börjat, kommer denna steg‑för‑steg‑handledning att göra det enkelt att slutföra uppgiften. Vi täcker allt från att konfigurera din miljö till att exportera den färdiga bilden, så att du snabbt kan **exportera PSD till PNG** i dina egna projekt.

## Snabba svar
- **What does this tutorial achieve?** Det visar hur du sparar en PSD‑fil som PNG efter att ha applicerat en anpassningsbar kontureffekt.  
- **Which library is used?** Aspose.PSD för Java.  
- **Do I need a license?** En gratis provversion fungerar för testning; en licens krävs för produktion.  
- **Can I change the stroke color?** Ja – du kan ange vilken färg som helst via `ColorFillSettings`.  
- **Is batch processing possible?** Absolut – omslut koden i en loop för att bearbeta flera PSD‑filer.

## Vad betyder “spara PSD som PNG”?

Att spara en PSD som PNG innebär att konvertera Photoshops inhemska lagerfil till ett platt, webbvänligt bildformat samtidigt som den visuella kvaliteten bevaras. Detta är användbart när du behöver visa PSD‑innehåll på webbplatser, mobilappar eller någon plattform som inte direkt stöder PSD‑filer.

## Varför applicera en kontureffekt med färgfyllning?

En kontur lägger till en skarp kant runt lagerinnehållet, vilket får grafik att sticka ut mot komplexa bakgrunder. Att kombinera den med en anpassad fyllningsfärg låter dig märka bilder, markera UI‑element eller skapa iögonfallande miniatyrer utan att lämna Photoshop.

## Förutsättningar

1. **Java Development Kit (JDK) 8+** – se till att `java` finns i din PATH.  
2. **Aspose.PSD for Java** – ladda ner från [webbplats](https://releases.aspose.com/psd/java/).  
3. **IDE** – IntelliJ IDEA, Eclipse eller någon editor du föredrar.  
4. **Sample PSD** – en fil som redan innehåller en kontureffekt (eller lägg till en i Photoshop).  
5. **Basic Java knowledge** – du kommer att skriva några rader kod, men inget avancerat.

När du har dessa redo kan vi börja koda.

## Importera paket

```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.fillsettings.ColorFillSettings;
import com.aspose.psd.fileformats.psd.layers.layereffects.StrokeEffect;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
import com.aspose.psd.imageoptions.PngOptions;
import com.aspose.psd.imageoptions.PsdOptions;
```

Dessa importeringar tar in alla klasser som behövs för att läsa in en PSD, modifiera dess kontur och spara både PSD‑ och PNG‑utdata.

## Hur man sparar PSD som PNG med kontureffekt

### Steg 1: Läs in PSD‑filen

Först, peka på mappen som innehåller din käll‑PSD.

```java
String dataDir = "Your Document Directory";
```

Byt ut `"Your Document Directory"` mot den faktiska sökvägen på din maskin.

Läs nu in filen samtidigt som du bevarar eventuella befintliga effektresurser:

```java
String sourceFileName = dataDir + "StrokeComplex.psd";

PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);

PsdImage im = (PsdImage) Image.load(sourceFileName, loadOptions);
```

### Steg 2: Ställ in konturfärg (och eventuellt anpassa bredd)

Loopen nedan går igenom varje lager, hämtar den första `StrokeEffect` och ändrar dess fyllningsfärg. Du kan också justera `setWidth` eller `setPosition` på `StrokeEffect`‑objektet om du behöver **anpassa konturbredd**.

```java
for (int i = 0; i < im.getLayers().length; i++) {
    StrokeEffect effect = (StrokeEffect) im.getLayers()[i].getBlendingOptions().getEffects()[0];
    ColorFillSettings settings = (ColorFillSettings) effect.getFillSettings();
    // Set the stroke color – change to any Color you like
    settings.setColor(Color.getDeepPink());
}
```

> **Pro tip:** `Color.getDeepPink()` är bara ett exempel. Använd `new Color(r, g, b)` för anpassade RGB‑värden.

### Steg 3: Spara den modifierade PSD (valfritt)

Om du vill behålla en PSD‑version med den uppdaterade konturen, spara den så här:

```java
String exportPath = dataDir + "StrokeComplexRendering.psd";
im.save(exportPath, new PsdOptions());
```

### Steg 4: Exportera bilden som PNG (det centrala “spara PSD som PNG”-steget)

Slutligen, konvertera den redigerade PSD‑filen till en PNG‑fil som är klar för webbbruk:

```java
String exportPathPng = dataDir + "StrokeComplexRendering.png";
PngOptions option = new PngOptions();
option.setColorType(PngColorType.TruecolorWithAlpha);

im.save(exportPathPng, option);
```

PNG‑filen behåller den djuprosa konturen du satte tidigare, och alternativet `TruecolorWithAlpha` säkerställer att transparensen bevaras.

## Vanliga problem & lösningar

| Problem | Orsak | Lösning |
|-------|--------|-----|
| **`ArrayIndexOutOfBoundsException`** | Lagret har inga effekter eller den första effekten är inte en `StrokeEffect`. | Verifiera att lagret faktiskt innehåller en kontur eller iterera genom `getEffects()` för att hitta rätt typ. |
| **Färgen ändras inte** | Du kanske redigerar en kopia av inställningarna istället för originalet. | Se till att du castar till `ColorFillSettings` direkt från `effect.getFillSettings()`. |
| **PNG visas tom** | PSD‑filen laddades utan att rasterisera lagret. | Anropa `im.save(..., new PngOptions())` efter alla modifieringar; undvik att spara den ursprungliga `im` innan ändringarna. |

## Vanliga frågor

**Q: Kan jag applicera flera effekter på ett enda lager med Aspose.PSD för Java?**  
A: Ja, du kan komma åt lagrets blandningsalternativ och lägga till så många effekter som behövs, inklusive skuggor, glöd och konturer.

**Q: Är det möjligt att automatisera processen för en batch av PSD‑filer?**  
A: Absolut. Omslut laddnings‑, effekt‑applikations‑ och sparlogiken i en `for‑each`‑loop som itererar över filer i en katalog.

**Q: Hur kan jag återställa ändringar som gjorts i en PSD‑fil?**  
A: Läs in originalfilen igen innan du sparar några modifieringar; Aspose.PSD erbjuder ingen ångra‑funktion.

**Q: Kan jag anpassa konturens bredd och position?**  
A: Ja. Använd `effect.setWidth(float)` och `effect.setPosition(StrokeEffect.Position)` för att kontrollera tjocklek och placering (inuti, utanför eller centrerad).

**Q: Är Aspose.PSD för Java‑biblioteket gratis att använda?**  
A: En gratis provversion finns tillgänglig för utvärdering. Full funktionalitet kräver en köpt licens. Se [köpalternativ](https://purchase.aspose.com/buy) för detaljer.

---

**Senast uppdaterad:** 2026-04-03  
**Testad med:** Aspose.PSD 24.12 för Java  
**Författare:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}