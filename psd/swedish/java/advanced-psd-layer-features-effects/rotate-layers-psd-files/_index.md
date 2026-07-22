---
date: 2026-07-22
description: Lär dig hur du sparar PSD som PNG, bevarar PNG‑transparens och roterar
  PSD‑lager i Java med Aspose.PSD. Steg‑för‑steg‑guide, kod‑fri förklaringar och felsökningstips.
keywords:
- save psd as png
- export psd layers png
- convert photoshop file png
- psd to png transparency
lastmod: 2026-07-22
linktitle: Spara PSD som PNG och rotera lager i Java med Aspose.PSD
og_description: Spara PSD som PNG med Aspose.PSD för Java. Bevara transparens, rotera
  lager och exportera PNG på bara några kodrader—perfekt för automatiserade arbetsflöden.
og_image_alt: 'Developer guide: save PSD as PNG and rotate layers using Aspose.PSD
  for Java'
og_title: Spara PSD som PNG och rotera lager i Java med Aspose.PSD
schemas:
- author: Aspose
  dateModified: '2026-07-22'
  description: Learn how to save psd as png, preserve PNG transparency, and rotate
    PSD layers in Java with Aspose.PSD. Step‑by‑step guide, code‑free explanations,
    and troubleshooting tips.
  headline: save psd as png and rotate layers in Java using Aspose.PSD
  type: TechArticle
- description: Learn how to save psd as png, preserve PNG transparency, and rotate
    PSD layers in Java with Aspose.PSD. Step‑by‑step guide, code‑free explanations,
    and troubleshooting tips.
  name: save psd as png and rotate layers in Java using Aspose.PSD
  steps:
  - name: Set Up Your Java Project
    text: Create a new Java project in your IDE and add the Aspose.PSD JAR to the
      project’s build path.
  - name: Import Required Classes
    text: '`PsdImage` is the core class that represents a Photoshop document in memory.
      `PngOptions` controls PNG‑specific settings, and `RotateFlipType` defines rotation
      and flip operations. These imports give you access to image loading, rotation,
      and PNG‑specific options.'
  - name: Define File Paths
    text: Specify where your source PSD lives and where the output files should be
      written. Using absolute paths during testing avoids “file not found” errors.
      > **Pro tip:** Store paths in a configuration file for easier maintenance in
      larger projects.
  - name: Load the PSD File
    text: '`PsdImage` loads the entire Photoshop document, including all layers, masks,
      and effects, into a manipulable object. Now `im` represents the whole PSD, ready
      for transformations.'
  - name: Rotate the Image (How to rotate PSD)
    text: '`RotateFlipType` enumerates all supported rotations and flips. In this
      example we rotate 270° and flip both axes, which swaps width and height while
      mirroring the image. Feel free to experiment with other values such as `Rotate90FlipNone`
      or `Rotate180FlipX`.'
  - name: Save the Rotated Image as PNG (save PSD as PNG)
    text: Configure `PngOptions` to keep transparency (`PngColorType.TruecolorWithAlpha`)
      and then call `save`. The PNG retains layer transparency, ensuring it works
      seamlessly in web or mobile apps. The resulting PNG preserves alpha channels,
      making it suitable for compositing or further processing.
  - name: Save the Modified PSD (optional)
    text: If you also need a new PSD with the rotation applied, you can save the modified
      `PsdImage` back to disk. You now have both a PNG preview and an updated PSD
      file.
  type: HowTo
- questions:
  - answer: Yes, you can call `layer.rotateFlip(RotateFlipType.Rotate90FlipNone)`
      after iterating through `im.getLayers()`.
    question: Can I rotate a specific layer in a PSD file?
  - answer: The library handles most files efficiently, but extremely large PSDs (>500
      MB) may require additional memory or streaming options.
    question: Is there any performance limitation with Aspose.PSD for Java?
  - answer: Aspose offers a free trial, but a paid license is needed for production.
      See the [temporary license](https://purchase.aspose.com/temporary-license/)
      for testing.
    question: Is Aspose.PSD free to use?
  - answer: Comprehensive docs are available at [Aspose.PSD Documentation](https://reference.aspose.com/psd/java/).
    question: Where can I find detailed documentation?
  - answer: Get help via the [Aspose Support Forum](https://forum.aspose.com/c/psd/34).
    question: What if I encounter issues while using Aspose.PSD?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- convert PSD
- Aspose.PSD
- Java image processing
- rotate PSD layers
title: Spara PSD som PNG och rotera lager i Java med Aspose.PSD
url: /sv/java/advanced-psd-layer-features-effects/rotate-layers-psd-files/
weight: 21
---

## Relaterade handledningar

- [Spara PSD som PNG och tillämpa Rendering Drop Shadow i Aspose.PSD för Java](/psd/java/advanced-image-manipulation/rendering-drop-shadow/)
- [Hur man komprimerar PNG-filer med Aspose.PSD för Java](/psd/java/optimizing-png-files/compress-png-files/)
- [Hur man roterar bild i Java med Aspose.PSD](/psd/java/advanced-image-manipulation/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< blocks/products/pf/main-wrap-class >}}

# spara psd som png och rotera lager i Java med Aspose.PSD

## Introduktion
Om du behöver **save PSD as PNG** samtidigt som du roterar lager, är den här guiden för dig. Oavsett om du bygger ett batch‑behandlingsverktyg, en webbtjänst som kräver bildmanipulation i realtid, eller helt enkelt automatiserar ett designflöde, sparar ett programatiskt tillvägagångssätt tid och tar bort beroendet av Adobe Photoshop. I den här handledningen går vi igenom **how to rotate PSD layers** och exporterar resultatet som en PNG med hjälp av Aspose.PSD‑biblioteket för Java. Låt oss kavla upp ärmarna och få ditt designflöde att fungera smidigt!

## Snabba svar
- **Vilket bibliotek kan jag använda?** Aspose.PSD for Java  
- **Kan jag både rotera och spara PSD som PNG i ett steg?** Yes – rotate the PSD then save as PNG  
- **Behöver jag en licens?** A free trial works for testing; a paid license is required for production  
- **Vilken Java‑version stöds?** Java 8 and later  
- **Är PNG‑utdata transparent?** Yes, when you set `PngColorType.TruecolorWithAlpha`

## Vad är “convert PSD to PNG”?
Att konvertera ett Photoshop‑dokument (PSD) till en PNG‑bild extraherar det visuella innehållet—inklusive lager, masker och alfakanaler—till ett brett stödformat som bevarar transparens. Detta gör PNG‑filen idealisk för webb‑grafik, miniatyrbilder och efterföljande bildbehandling. Den resulterande PNG‑filen kan användas direkt i webbsidor, mobilappar eller vidare bearbetas av andra bildbibliotek.

## Varför använda Aspose.PSD för Java för att spara PSD som PNG och rotera PSD‑lager?
Aspose.PSD möjliggör att **save PSD as PNG** och rotera lager utan att installera Photoshop. Det stödjer **50+ input and output formats**, bearbetar hundratals‑sidiga PSD‑filer med mindre än 200 MB RAM, och körs på Windows, Linux och macOS. API‑et kräver bara några metodanrop, levererar högkvalitativa resultat med inbyggd hantering av lagereffekter, masker och alfakanaler.

## Förutsättningar
Innan vi dyker ner i koden, se till att du har följande:

- **Java Development Kit (JDK)** – ladda ner från [Oracle website](https://www.oracle.com/java/technologies/javase-downloads.html).  
- **Integrated Development Environment (IDE)** – IntelliJ IDEA, Eclipse eller NetBeans är alla bra.  
- **Aspose.PSD for Java library** – hämta den senaste JAR‑filen från [release page](https://releases.aspose.com/psd/java/).  
- **Basic Java knowledge** – familiarity with classes, objects, and exception handling.

## Steg‑för‑steg‑guide

### Steg 1: Ställ in ditt Java‑projekt
Skapa ett nytt Java‑projekt i din IDE och lägg till Aspose.PSD‑JAR‑filen i projektets byggsökväg.

### Steg 2: Importera nödvändiga klasser
`PsdImage` är kärnklassen som representerar ett Photoshop‑dokument i minnet. `PngOptions` styr PNG‑specifika inställningar, och `RotateFlipType` definierar rotations‑ och vändningsoperationer.

```java
import com.aspose.psd.Image;
import com.aspose.psd.RotateFlipType;
import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.PngOptions;
```

Dessa importeringar ger dig åtkomst till bildladdning, rotation och PNG‑specifika alternativ.

### Steg 3: Definiera filsökvägar
Ange var din käll‑PSD finns och var utdata‑filerna ska skrivas. Att använda absoluta sökvägar under testning undviker “file not found”-fel.

```java
String dataDir = "Your Document Directory"; // Change this to your actual document directory.
String sourceFile = dataDir + "1.psd"; // Source PSD file
String pngPath = dataDir + "RotateFlipTest2617.png"; // Output PNG file path
String psdPath = dataDir + "RotateFlipTest2617.psd"; // Output PSD file path
```

> **Proffstips:** Store paths in a configuration file for easier maintenance in larger projects.

### Steg 4: Ladda PSD‑filen
`PsdImage` laddar hela Photoshop‑dokumentet, inklusive alla lager, masker och effekter, till ett manipulerbart objekt.

```java
PsdImage im = (PsdImage) Image.load(sourceFile);
```

Nu representerar `im` hela PSD‑filen, redo för transformationer.

### Steg 5: Rotera bilden (Hur man roterar PSD)
`RotateFlipType` enumererar alla stödjade rotationer och vändningar. I detta exempel roterar vi 270° och vänder båda axlar, vilket byter **width** och **height** medan bilden **mirroring**.

```java
int flipType = RotateFlipType.Rotate270FlipXY; // Choose the rotation type
im.rotateFlip(flipType); // Rotate the image
```

Känn dig fri att experimentera med andra värden som `Rotate90FlipNone` eller `Rotate180FlipX`.

### Steg 6: Spara den roterade bilden som PNG (save PSD as PNG)
Konfigurera `PngOptions` för att behålla transparens (`PngColorType.TruecolorWithAlpha`) och anropa sedan `save`. PNG‑filen behåller lager‑transparens, vilket gör att den fungerar sömlöst i webb‑ eller mobilappar.

```java
PngOptions options = new PngOptions();
options.setColorType(PngColorType.TruecolorWithAlpha); // Preserve transparency
im.save(pngPath, options); // Save the rotated image
```

Den resulterande PNG‑filen bevarar alfakanaler, vilket gör den lämplig för sammansättning eller vidare bearbetning.

### Steg 7: Spara den modifierade PSD‑filen (valfritt)
Om du också behöver en ny PSD med rotationen applicerad, kan du spara den modifierade `PsdImage` tillbaka till disk.

```java
im.save(psdPath);
```

Du har nu både en PNG‑förhandsgranskning och en uppdaterad PSD‑fil.

## Vanliga problem och lösningar
- **Fil ej hittad:** Verifiera att `dataDir` slutar med en sökvägsavgränsare (`/` eller `\`).  
- **OutOfMemoryError på stora PSD‑filer:** Öka JVM‑heap‑storlek (`-Xmx2g`).  
- **Transparens förlorad:** Se till att `PngColorType.TruecolorWithAlpha` är satt; annars sparas PNG utan alfa.  
- **Flip PSD‑bild beter sig inte som förväntat:** Dubbelkolla den `RotateFlipType`‑konstant du valt; vissa konstanter kombinerar rotation och flip i ett steg.

## Vanliga frågor

**Q: Kan jag rotera ett specifikt lager i en PSD‑fil?**  
A: Ja, du kan anropa `layer.rotateFlip(RotateFlipType.Rotate90FlipNone)` efter att ha itererat genom `im.getLayers()`.

**Q: Finns det någon prestandabegränsning med Aspose.PSD för Java?**  
A: Biblioteket hanterar de flesta filer effektivt, men extremt stora PSD‑filer (>500 MB) kan kräva extra minne eller streaming‑alternativ.

**Q: Är Aspose.PSD gratis att använda?**  
A: Aspose erbjuder en gratis provperiod, men en betald licens behövs för produktion. Se den [tillfällig licens](https://purchase.aspose.com/temporary-license/) för testning.

**Q: Var kan jag hitta detaljerad dokumentation?**  
A: Omfattande dokumentation finns på [Aspose.PSD-dokumentation](https://reference.aspose.com/psd/java/).

**Q: Vad gör jag om jag stöter på problem när jag använder Aspose.PSD?**  
A: Få hjälp via [Aspose supportforum](https://forum.aspose.com/c/psd/34).

**Q: Bevarar konvertering av PSD till PNG lager‑effekter?**  
A: Ja, när du sparar med `PngColorType.TruecolorWithAlpha` rasteriseras de flesta visuella effekter till PNG.

**Q: Kan jag batch‑processa flera PSD‑filer?**  
A: Absolut. Lägg koden i en loop som itererar över en katalog med PSD‑filer.

**Q: Är det möjligt att ställa in PNG‑komprimeringsnivå?**  
A: `PngOptions` tillhandahåller en `setCompressionLevel(int)`‑metod för finjustering av utskriftsstorlek.

**Q: Måste jag stänga bildobjektet?**  
A: `PsdImage` implementerar `Closeable`; använd try‑with‑resources eller anropa `im.close()` i ett `finally`‑block.

**Q: Kommer den roterade PNG‑filen ha samma dimensioner som originalet?**  
A: Rotering med 90° eller 270° byter bredd och höjd, så PNG‑filen speglar den nya orienteringen automatiskt.

## Slutsats
Genom att utnyttja Aspose.PSD för Java kan du **save PSD as PNG**, **preserve PNG transparency**, och **rotate PSD layers** med bara några rader kod. Detta tillvägagångssätt eliminerar behovet av Photoshop, snabbar upp automatiserade arbetsflöden och ger dig full kontroll över bildutdata. Prova det i dina egna projekt och se hur mycket tid du sparar!

---

**Last Updated:** 2026-07-22  
**Tested With:** Aspose.PSD for Java 24.11  
**Author:** Aspose  

{{< blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/products-backtop-button >}}