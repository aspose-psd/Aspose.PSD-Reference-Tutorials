---
date: 2026-09-03
description: Lär dig hur du konverterar PSD till BMP i Java med Aspose.PSD, och upptäck
  grundläggande ritfunktioner som att applicera gradienter och skapa rektanglar.
keywords:
- convert PSD to BMP
- how to draw PSD
- apply gradient PSD
- create rectangle PSD
lastmod: 2026-09-03
linktitle: Hur man konverterar PSD till BMP och ritar med Java
og_description: Konvertera PSD till BMP i Java med Aspose.PSD. Denna guide visar steg‑för‑steg
  hur du laddar PSD‑filer, manipulerar pixlar, applicerar gradienter, skapar rektanglar
  och sparar som BMP på ett effektivt sätt.
og_image_alt: 'Tutorial: converting PSD to BMP and drawing shapes in Java using Aspose.PSD'
og_title: Konvertera PSD till BMP i Java – Grundläggande ritguide
schemas:
- author: Aspose
  dateModified: '2026-09-03'
  description: Learn how to convert PSD to BMP in Java using Aspose.PSD, and discover
    core drawing features like applying gradients and creating rectangles.
  headline: How to convert PSD to BMP and draw with Java
  type: TechArticle
- questions:
  - answer: Yes, the library fully supports layered PSD files, including transparency,
      blending modes, and layer effects.
    question: Can Aspose.PSD for Java handle layers and transparency in PSD files?
  - answer: Absolutely. You can automate batch jobs by iterating over a folder, loading
      each PSD, applying the same drawing logic, and saving as BMP or any other supported
      format.
    question: Is Aspose.PSD for Java suitable for batch processing of PSD files?
  - answer: Besides PSD, the API handles BMP, PNG, JPEG, TIFF, GIF, and over 20 additional
      raster formats for both input and output.
    question: Does Aspose.PSD for Java support multiple image formats other than PSD?
  - answer: Visit the [Aspose.PSD temporary license](https://purchase.aspose.com/temporary-license/)
      page for obtaining a temporary license.
    question: How can I obtain a temporary license for Aspose.PSD for Java?
  - answer: Explore the [Aspose.PSD forum](https://forum.aspose.com/c/psd/34) for
      community support, tips, and additional resources.
    question: Where can I find more help and resources for Aspose.PSD for Java?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- convert PSD
- Aspose.PSD
- Java image processing
title: Hur man konverterar PSD till BMP och ritar med Java
url: /sv/java/java-graphics-drawing/core-drawing-features/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Hur man konverterar PSD till BMP och ritar med Java

## Introduktion
Aspose.PSD for Java är ett Java‑bibliotek som möjliggör programmatisk skapande, redigering och konvertering av Adobe Photoshop PSD‑filer. I den här handledningen kommer du att lära dig hur du **konverterar PSD till BMP** och utforskar de grundläggande ritfunktionerna som låter dig **rita PSD‑lager, applicera gradienter och skapa rektanglar** direkt från Java‑kod. Att behärska dessa möjligheter låter dig automatisera komplexa bildbehandlings‑pipelines utan att behöva ha Photoshop installerat.

## Snabba svar
- **Kan jag konvertera PSD till BMP med en enda rad kod?** Ja – ladda PSD‑filen med `PsdImage` och anropa `save("output.bmp", SaveFormat.Bmp)`.  
- **Vilken version av Aspose.PSD krävs?** Den senaste 24.x‑utgåvan stödjer alla grundläggande rit‑API:er.  
- **Behöver jag en licens för utveckling?** En gratis tillfällig licens fungerar för testning; en full licens krävs för produktion.  
- **Vilka Java‑versioner stöds?** Java 8 till Java 21 är fullt kompatibla.  
- **Kan jag batch‑processa många PSD‑filer?** Absolut – loopa över en katalog och återanvänd samma konverteringslogik.

## Hur man konverterar PSD till BMP i Java?
Läs in käll‑PSD‑filen, modifiera eventuellt dess pixlar eller ritlager, och spara sedan som en BMP‑fil. Konverteringen sker i minnet, så du undviker mellanfiler och kan bearbeta tusentals bilder effektivt. Aspose.PSD strömmar data, vilket innebär att även filer med flera hundra sidor hanteras utan att heap‑minnet tar slut.

### Vilka är de grundläggande ritfunktionerna i Aspose.PSD för Java?
Biblioteket erbjuder en komplett uppsättning rit‑primitiver som låter dig **rita PSD‑former**, **applicera gradientfyllningar** och **skapa rektangel‑lager** programatiskt. Dessa API:er arbetar på samma pixel‑nivå‑motor som Photoshop använder, vilket garanterar visuell trohet över format.

## Förutsättningar
Innan du börjar, se till att följande är klara:

### Java‑utvecklingsmiljö
Installera Java Development Kit (JDK) från [Oracles webbplats](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html). Handledningen testades med JDK 11, men vilken JDK 8+ som helst fungerar.

### Aspose.PSD för Java‑installation
1. **Ladda ner Aspose.PSD för Java** – gå till [nedladdningssidan](https://releases.aspose.com/psd/java/) och hämta det senaste ZIP‑arkivet.  
2. **Lägg till JAR‑filerna i ditt projekt** – kopiera `aspose-psd.jar` och dess beroenden till din classpath, eller referera dem via Maven/Gradle enligt produktdokumentationen.

Nu har du allt du behöver för att börja koda.

## Importera paket
För att arbeta med Aspose.PSD måste du importera de grundläggande namnutrymmena. Dessa importeringar ger dig åtkomst till bildladdning, pixelmanipulation och ritverktyg.  
```java
import com.aspose.psd.Rectangle;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.BmpOptions;
```

## Steg 1: läs in en PSD‑bild
Det första steget är att skapa en `PsdImage`‑instans som representerar källfilen i minnet. Detta objekt ger dig läs‑/skriv‑åtkomst till lager, kanaler och enskilda pixlar.  
```java
String dataDir = "Your Document Directory";
String loadpath = dataDir + "sample.psd";
// Load the PSD image
PsdImage image = new PsdImage(loadpath);
```

## Steg 2: manipulera pixlar
När PSD‑filen är inläst kan du ändra dess pixeldata, rita nya former eller applicera gradientfyllningar. Rit‑API:et speglar Photoshops egna verktyg, vilket låter dig **rita PSD‑rektanglar** eller **applicera gradient‑PSD‑effekter** med bara några metodanrop.  
```java
// Load pixels of a specific region (e.g., a 100x10 rectangle starting from top-left corner)
int[] pixels = image.loadArgb32Pixels(new Rectangle(0, 0, 100, 10));
// Modify the pixels (e.g., apply a gradient effect)
for (int i = 0; i < pixels.length; i++) {
    pixels[i] = i;  // Apply your desired manipulation logic here
}
```

## Steg 3: spara den modifierade bilden
När du är klar med redigeringen, anropa `save`‑metoden och specificera `SaveFormat.Bmp`. Biblioteket skriver en BMP‑fil som bevarar de visuella förändringarna du gjort, vilket slutför arbetsflödet för **konvertera PSD till BMP**.  
```java
String outpath = dataDir + "CoreDrawingFeatures.bmp";
// Save modified pixels back to the image
image.saveArgb32Pixels(new Rectangle(0, 0, 100, 10), pixels);
// Save the image to BMP format
image.save(outpath, new BmpOptions());
```

## Vanliga problem och felsökning
- **Out‑of‑memory‑fel** – Aspose.PSD strömmar data; dock kan extremt stora PSD‑filer (>2 GB) fortfarande behöva extra JVM‑heap (`-Xmx4g`).  
- **Färgsprofils‑mismatchar** – Om den sparade BMP‑filen ser urtvättad ut, se till att käll‑PSD:ens ICC‑profil bevaras genom att anropa `psdImage.getColorProfile()` före sparning.  
- **Saknade lager efter konvertering** – Verifiera att dolda lager inte kastas bort genom att kontrollera `layer.isVisible()` före sparning.

## Vanliga frågor

**Q: Kan Aspose.PSD för Java hantera lager och transparens i PSD‑filer?**  
A: Ja, biblioteket stödjer fullt ut lager‑PSD‑filer, inklusive transparens, blandningslägen och lagereffekter.

**Q: Är Aspose.PSD för Java lämplig för batch‑bearbetning av PSD‑filer?**  
A: Absolut. Du kan automatisera batch‑jobb genom att iterera över en mapp, läsa in varje PSD, applicera samma ritlogik och spara som BMP eller något annat stödformat.

**Q: Stöder Aspose.PSD för Java flera bildformat förutom PSD?**  
A: Förutom PSD hanterar API:et BMP, PNG, JPEG, TIFF, GIF och över 20 ytterligare rasterformat för både in- och utdata.

**Q: Hur kan jag få en tillfällig licens för Aspose.PSD för Java?**  
A: Besök sidan [Aspose.PSD tillfälliga licens](https://purchase.aspose.com/temporary-license/) för att få en tillfällig licens.

**Q: Var kan jag hitta mer hjälp och resurser för Aspose.PSD för Java?**  
A: Utforska [Aspose.PSD‑forum](https://forum.aspose.com/c/psd/34) för community‑support, tips och ytterligare resurser.

---

**Senast uppdaterad:** 2026-09-03  
**Testad med:** Aspose.PSD 24.12 for Java  
**Författare:** Aspose

## Relaterade handledningar

- [Hur man skapar radiella gradienteffekter i Aspose.PSD för Java](/psd/java/advanced-image-effects/add-gradient-effects/)
- [Rita och spara en rektangel i en PSD med Aspose.PSD för Java](/psd/java/basic-image-operations/simple-drawing/)
- [Hur man konverterar PSD till rasterbildformat med Aspose.PSD för Java](/psd/java/advanced-techniques/convert-psd-to-raster-formats/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}
{{< blocks/products/products-backtop-button >}}