---
date: 2026-09-28
description: Lär dig hur du exporterar PSD som PNG samtidigt som du ställer in PSD:s
  färgläge till 16‑bit gråskala med Aspose.PSD för Java. Steg‑för‑steg‑guide med kodexempel.
keywords:
- export psd as png
- how to convert psd to png
- 16-bit grayscale java
lastmod: 2026-09-28
linktitle: Exportera PSD som PNG – 16‑bit gråskala – Java
og_description: Exportera PSD som PNG med 16‑bit gråskala med Aspose.PSD för Java.
  Följ den här steg‑för‑steg‑handledningen för att bevara 65 536 grå nyanser.
og_image_alt: Guide showing how to export PSD as PNG with 16-bit grayscale using Aspose.PSD
  Java
og_title: Exportera PSD som PNG med 16‑bit gråskala i Java – Aspose.PSD Guide
schemas:
- author: Aspose
  dateModified: '2026-09-28'
  description: Learn how to export PSD as PNG while setting PSD color mode to 16-bit
    grayscale using Aspose.PSD for Java. Step‑by‑step guide with code examples.
  headline: How to export PSD as PNG with 16‑bit grayscale color mode in Java
  type: TechArticle
- description: Learn how to export PSD as PNG while setting PSD color mode to 16-bit
    grayscale using Aspose.PSD for Java. Step‑by‑step guide with code examples.
  name: How to export PSD as PNG with 16‑bit grayscale color mode in Java
  steps:
  - name: '**Java Development Kit (JDK)** – Install the latest JDK from [Oracle''s
      site](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).'
    text: '**Java Development Kit (JDK)** – Install the latest JDK from [Oracle''s
      site](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).'
  - name: '**Aspose.PSD for Java library** – Download the JAR from the [Aspose download
      page](https://releases.aspose.com/psd/java/).'
    text: '**Aspose.PSD for Java library** – Download the JAR from the [Aspose download
      page](https://releases.aspose.com/psd/java/).'
  - name: '**An IDE** – IntelliJ IDEA, Eclipse, or Visual Studio Code works perfectly.'
    text: '**An IDE** – IntelliJ IDEA, Eclipse, or Visual Studio Code works perfectly.'
  - name: '**Basic Java knowledge** – You should be comfortable creating classes,
      handling exceptions, and working with file paths.'
    text: '**Basic Java knowledge** – You should be comfortable creating classes,
      handling exceptions, and working with file paths.'
  - name: '**A sample PSD file** – Create one in Adobe Photoshop or grab a free sample
      online.'
    text: '**A sample PSD file** – Create one in Adobe Photoshop or grab a free sample
      online.'
  type: HowTo
- questions:
  - answer: It provides 65 536 shades of gray, delivering far more tonal detail than
      the standard 8‑bit (256 shades).
    question: What is 16‑bit grayscale color mode?
  - answer: Absolutely! Aspose.PSD supports RGB, CMYK, Lab, Indexed, and many other
      color modes.
    question: Can I use Aspose.PSD for non‑grayscale images?
  - answer: Yes, you can try a free trial version of Aspose.PSD. Just head to the
      [Aspose download page](https://releases.aspose.com/).
    question: Is there a trial version of Aspose.PSD?
  - answer: Check the official [documentation](https://reference.aspose.com/psd/java/)
      for in‑depth tutorials, API references, and sample projects.
    question: Where can I find more Aspose.PSD examples?
  - answer: You can buy a license by visiting the [Aspose purchase page](https://purchase.aspose.com/buy).
    question: How do I purchase a license for Aspose.PSD?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- convert psd
- Aspose.PSD
- Java image processing
title: Hur man exporterar PSD som PNG med 16‑bit gråskala färgläge i Java
url: /sv/java/advanced-psd-layer-features-effects/support-16-bit-grayscale-color-mode-psd/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Exportera PSD som PNG med 16‑bits gråskala färgläge i Java

## Introduktion
Att exportera PSD som PNG samtidigt som du behåller ett 16‑bits gråskala färgläge ger dig djupet i ett professionellt fotografi och den universella kompatibiliteten hos PNG. I den här guiden lär du dig hur du **ställer in PSD-färgläget till 16‑bits gråskala** och sedan **exporterar PSD som PNG** med Aspose.PSD för Java. Handledningen täcker allt från förutsättningar till felsökning, så att du kan integrera arbetsflödet i någon Java‑baserad bildpipeline.

## Snabba svar
- **Vad innebär “exportera PSD som PNG”?** Ladda en PSD, ändra eventuellt dess färgläge, och spara den som en PNG‑fil.  
- **Vilken Aspose‑klass hanterar konverteringen?** `PsdImage` laddar PSD‑filen och `PngOptions` definierar PNG‑utdatainställningarna.  
- **Behöver jag en licens för produktion?** Ja – en provversion fungerar för testning, men en betald licens krävs för kommersiell användning.  
- **Kan 16‑bits djup bevaras i PNG?** Absolut, genom att använda `PngColorType.GrayscaleWithAlpha`.  
- **Vilka IDE:er stöds?** Alla Java‑IDE:er – IntelliJ IDEA, Eclipse, VS Code eller NetBeans.

## Vad är export av PSD som PNG?
Export PSD som PNG är processen att konvertera ett Adobe Photoshop‑dokument (PSD) till en Portable Network Graphics‑fil (PNG) samtidigt som bildens pixeldata och färgdjup bevaras. Denna konvertering används ofta för att dela högkvalitativa gråskala‑tillgångar på webben utan att förlora tonala detaljer.

## Varför exportera PSD som PNG med 16‑bits gråskala?
Att exportera till PNG samtidigt som du behåller 16‑bits gråskala bevarar 65 536 gråtoner, vilket ger mycket mer tonrikedom än 8‑bits bilder. PNG:s universella stöd säkerställer att filerna kan visas i webbläsare, mobilappar och skrivbordsredigerare utan förlust, medan den förlustfria komprimeringen i Aspose.PSD garanterar att inga artefakter introduceras.

## Förutsättningar
1. **Java Development Kit (JDK)** – Installera den senaste JDK:n från [Oracle's site](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).  
2. **Aspose.PSD för Java‑bibliotek** – Ladda ner JAR‑filen från [Aspose download page](https://releases.aspose.com/psd/java/).  
3. **En IDE** – IntelliJ IDEA, Eclipse eller Visual Studio Code fungerar utmärkt.  
4. **Grundläggande Java‑kunskaper** – Du bör vara bekväm med att skapa klasser, hantera undantag och arbeta med filsökvägar.  
5. **En exempel‑PSD‑fil** – Skapa en i Adobe Photoshop eller hämta ett gratis exempel online.

## Så exporterar du PSD som PNG steg för steg

## Hur ställer du in PSD‑färgläget till 16‑bits gråskala?
`PsdImage` är Aspose.PSD‑klassen som laddar och representerar en PSD‑fil i minnet.  
`ColorMode` är en uppräkning som definierar färgläget för en PSD‑bild.

Ladda PSD‑filen med `PsdImage`, ändra dess färgläge med `ColorMode`‑egenskapen och spara sedan den modifierade filen. Denna operation körs helt i minnet, vilket eliminerar behovet av mellanfiler och säkerställer att konverteringen är snabb och effektiv.

```java
import com.aspose.psd.*;
import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.fileformats.psd.ColorModes;
import com.aspose.psd.fileformats.psd.CompressionMethod;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.PngOptions;
import com.aspose.psd.imageoptions.PsdOptions;
import com.aspose.psd.system.Enum;
```

Dessa importeringar ger dig åtkomst till de funktioner du kommer att använda för att manipulera PSD‑filer, ställa in färgläget och exportera resultatet som PNG.

## Hur definierar du käll- och målmappar?
`File` är en java.io‑klass som representerar en fil‑ eller mapp‑sökväg i filsystemet.

Du måste tala om för programmet var den ursprungliga PSD‑filen ska läsas och var den konverterade PNG‑filen ska skrivas. Att använda absoluta eller relativa sökvägar fungerar, men håll dem konsekventa över miljöer för att undvika fel vid sökvägsupplösning.

```java
String sourceDir = "Your Source Directory"; // Change to your source directory
String outputDir = "Your Document Directory"; // Change to your output directory
```

Ersätt platshållarsträngarna med de faktiska sökvägarna på din maskin.

## Hur kapslar du in konverteringslogiken i en återanvändbar metod?
`convertPsdToPng` är en anpassad metod som kapslar in alla steg som krävs för att konvertera en PSD‑fil till PNG med valfria inställningar.

Att skapa en dedikerad metod låter dig återanvända samma konverteringssteg för flera filer eller olika inställningar. Skicka parametrar som källsökväg, destinationsmapp och valfri komprimeringsnivå, vilket gör arbetsflödet flexibelt och underhållbart.

```java
class LocalScopeExtension {
    void saveToPsdThenLoadAndSaveToPng(
        String file,
        short colorMode,
        short channelBitsCount,
        short channelsCount,
        short compression,
        int layerNumber) {
```

Denna metod låter dig **ställa in PSD‑färgläget** och sedan **exportera PSD som PNG** i ett enda flöde.

## Hur laddar du PSD‑filen och tillämpar 16‑bits gråskala‑läget?
`PsdImage` är Aspose.PSD‑klassen som laddar en PSD‑fil i minnet.  
`ColorMode.GRAYSCALE_16` är ett uppräkningsvärde som ställer in bilden till 16‑bits gråskala.  
`channelBitsCount` är en egenskap som specificerar antalet bitar per kanal.

Inuti konverteringsmetoden bygger du de fullständiga filsökvägarna, instansierar `PsdImage` och ändrar dess `ColorMode` till `ColorMode.GRAYSCALE_16`. `channelBitsCount`‑egenskapen måste sättas till 16 för att behålla den höga bitdjupet, vilket säkerställer att bilden behåller all tonal information.

```java
String filePath = sourceDir + file + ".psd";
String postfix = Enum.getName(ColorModes.class, colorMode) + channelBitsCount + "_" +
                 channelsCount + "_" + Enum.getName(CompressionMethod.class, compression);
String exportPath = outputDir + file + postfix + ".psd";
String pngExportPath = outputDir + file + postfix + ".png";
// Load a predefined 16-bit grayscale PSD
PsdImage image = (PsdImage)Image.load(filePath);
```

`postfix` hjälper dig att hålla reda på de inställningar som används för varje exporterad fil.

## Hur ritar du en subtil kantlinje på bilden (valfritt steg)?
`Graphics` är en klass som ger ritningsmöjligheter på en `PsdImage`‑canvas.

Du kan valfritt rita en grå rektangel runt bilden för att göra utskriften mer synlig under testning. Detta steg visar hur man arbetar med lager och grafikobjekt, och rektangeln beräknas dynamiskt så att den förblir centrerad oavsett bildstorlek.

```java
try {
    RasterCachedImage raster = layerNumber >= 0 ? image.getLayers()[layerNumber] : image;
    // Draw a gray inner border around the perimeter of the layer
    Graphics graphics = new Graphics(raster);
    int width = raster.getWidth();
    int height = raster.getHeight();
    Rectangle rect = new Rectangle(
        width / 3,
        height / 3,
        width - (2 * (width / 3)) - 1,
        height - (2 * (height / 3)) - 1);
    graphics.drawRectangle(new Pen(Color.getDarkGray(), 1), rect);
```

Rektangeln beräknas dynamiskt så att den förblir centrerad oavsett bildstorlek.

## Hur sparar du den modifierade PSD‑filen med det nya färgläget?
`PsdOptions` är en klass som styr hur en PSD‑fil sparas, inklusive färgläge och bitdjupsinställningar.

Efter ritning (eller om du hoppar över det steget) anropar du `save` på `PsdImage`‑instansen och skickar ett `PsdOptions`‑objekt som bevarar 16‑bits gråskala‑konfigurationen. Detta säkerställer att den sparade PSD‑filen behåller det önskade färgläget utan någon dataförlust.

```java
    // Save a copy of PSD with specific characteristics
    PsdOptions psdOptions = new PsdOptions();
    psdOptions.setColorMode(colorMode);
    psdOptions.setChannelBitsCount(channelBitsCount);
    psdOptions.setChannelsCount(channelsCount);
    psdOptions.setCompressionMethod(compression);
    image.save(exportPath, psdOptions);
}
```

## Hur konverterar du PSD till PNG samtidigt som du bevarar 16‑bits djup?
`PngOptions` är en klass som definierar PNG‑utdatainställningar såsom färgtyp och komprimeringsnivå.  
`PngColorType.GrayscaleWithAlpha` är ett uppräkningsvärde som lagrar 16‑bits gråskala‑data med en alfakanal.

Ladda den nyss sparade PSD‑filen, konfigurera `PngOptions` med `PngColorType.GrayscaleWithAlpha` och anropa `save`. Detta behåller 16‑bits gråskala‑data i PNG‑filen, vilket ger en förlustfri, högkvalitativ bild som är lämplig för vidare bearbetning eller distribution.

```java
finally {
    image.dispose();
}
// Load the saved PSD
PsdImage image1 = (PsdImage)Image.load(exportPath);
try {
    // Convert the saved PSD to a grayscale PNG image
    PngOptions pngOptions = new PngOptions();
    pngOptions.setColorType(PngColorType.GrayscaleWithAlpha);
    image1.save(pngExportPath, pngOptions); // here should be no exception
}
finally {
    image1.dispose();
}
```

Nu har du framgångsrikt **exporterat PSD som PNG** samtidigt som du behåller den högkvalitativa 16‑bits gråskala‑datan.

## Vanliga problem och lösningar
| Problem | Varför det händer | Lösning |
|-------|----------------|-----|
| **“Unsupported color type” exception** | Försöker spara en PSD med en ej stödjande kanalkonfiguration. | Se till att `channelBitsCount` matchar den faktiska bitdjupet (16) och att `channelsCount` är korrekt för gråskala (1). |
| **File not found** | Felaktig sökväg till källmappen. | Dubbelkolla `sourceDir`‑strängen och verifiera att PSD‑filen finns på den platsen. |
| **Output PNG appears black** | PNG sparad utan korrekt alfahantering. | Använd `PngColorType.GrayscaleWithAlpha` som visat ovan. |
| **Memory overflow on large PSDs** | Laddar hela filen i minnet. | Aktivera strömningsläge via `PsdImage.load(inputStream, new LoadOptions())` för att bearbeta stora filer effektivt. |

## Vanliga frågor

**Q: Vad är 16‑bits gråskala färgläge?**  
A: Det ger 65 536 gråtoner, vilket levererar mycket mer tonaldetalj än standard‑8‑bits (256 nyanser).

**Q: Kan jag använda Aspose.PSD för icke‑gråskala bilder?**  
A: Absolut! Aspose.PSD stöder RGB, CMYK, Lab, Indexed och många andra färglägen.

**Q: Finns det en provversion av Aspose.PSD?**  
A: Ja, du kan prova en gratis provversion av Aspose.PSD. Gå bara till [Aspose download page](https://releases.aspose.com/).

**Q: Var kan jag hitta fler Aspose.PSD‑exempel?**  
A: Kolla den officiella [documentation](https://reference.aspose.com/psd/java/) för djupgående handledningar, API‑referenser och exempelprojekt.

**Q: Hur köper jag en licens för Aspose.PSD?**  
A: Du kan köpa en licens genom att besöka [Aspose purchase page](https://purchase.aspose.com/buy).

---

**Senast uppdaterad:** 2026-09-28  
**Testad med:** Aspose.PSD för Java 24.12 (senaste vid skrivtillfället)  
**Författare:** Aspose

## Relaterade handledningar

- [Konvertera PSD till PNG med specificerad bitdjup med Aspose.PSD för Java](/psd/java/optimizing-png-files/specify-png-bit-depth/)
- [Exportera PSD till PNG med lagerffekter med Aspose.PSD för Java](/psd/java/psd-image-modification-conversion/apply-layer-effects-psd-files/)
- [Spara PSD som JPEG och stöd RGB‑färg med Aspose.PSD Java](/psd/java/advanced-psd-layer-features-effects/support-rgb-color-psd-files/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}