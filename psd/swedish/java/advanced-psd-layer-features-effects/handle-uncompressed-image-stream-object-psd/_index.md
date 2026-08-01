---
date: 2026-08-01
description: Lär dig hur du exporterar PSD till PNG och hanterar okrypterade bildströmmar
  med Aspose.PSD for Java.
keywords:
- export psd to png
- save psd as png
- java image manipulation
lastmod: 2026-08-01
linktitle: Hantera okrypterat bildströmsobjekt i PSD – Java
og_description: exportera psd till png med Aspose.PSD for Java. Lär dig att hantera
  okrypterade bildströmmar, skapa grafikobjekt och spara högkvalitativa PNG‑filer.
og_image_alt: 'Developer guide: Export PSD to PNG with uncompressed stream using Aspose.PSD
  Java'
og_title: exportera psd till png – Java‑guide för okrypterade PSD‑strömmar
schemas:
- author: Aspose
  dateModified: '2026-08-01'
  description: Learn how to export PSD to PNG and handle uncompressed image streams
    with Aspose.PSD for Java.
  headline: Export PSD to PNG – Create PSD Graphics Object – Uncompressed Stream in
    Java
  type: TechArticle
- questions:
  - answer: Yes. After loading the PSD, retrieve the desired layer via `psdImage.getLayers().get_Item(index)`
      and pass that layer to the `Graphics` constructor.
    question: Can I use the graphics object to edit only one specific layer?
  - answer: Raw stores pixel data without any compression, so the resulting file is
      larger than a compressed PSD, but it guarantees 100 % pixel fidelity.
    question: Does the Raw compression method affect file size?
  - answer: Absolutely. After editing, call `psdImage.save("output.png", new PngOptions())`—this
      is the standard way to **export PSD to PNG** with lossless quality.
    question: Is it possible to export the edited PSD to another format (e.g., PNG)?
  - answer: Aspose.PSD for Java supports JDK 8 and later, including all LTS releases
      up to JDK 21.
    question: What Java version is required?
  - answer: Invoke `psdImage.dispose()` and close any streams (e.g., `ms.close()`)
      to free native memory and avoid leaks.
    question: How do I release resources after processing?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- export psd
- Aspose.PSD
- Java image processing
- uncompressed stream
- PSD graphics
title: Exportera PSD till PNG – Skapa PSD-grafikobjekt – Okrypterad ström i Java
url: /sv/java/advanced-psd-layer-features-effects/handle-uncompressed-image-stream-object-psd/
weight: 26
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Exportera PSD till PNG – Skapa PSD Graphics-objekt – Okrypterad ström i Java

## Introduktion
I den här steg‑för‑steg‑guiden kommer du **exportera PSD till PNG** medan du arbetar med en okrypterad bildström med Aspose.PSD för Java. Oavsett om du automatiserar en designpipeline eller bygger en anpassad redigerare är förmågan att rendera en Photoshop‑fil utan kvalitetsförlust avgörande. Vi börjar med den nödvändiga konfigurationen, går igenom hur du skapar ett `Graphics`‑objekt och avslutar med en förlustfri PNG‑export. När du är klar förstår du varför Aspose.PSD hanterar råa strömmar effektivt och hur du integrerar det i vilket Java‑projekt som helst.

## Snabba svar
- **Vad betyder “skapa PSD graphics‑objekt”?** Det betyder att instansiera ett `Graphics`‑sammanhang som låter dig rita på eller modifiera en PSD‑bild programatiskt.  
- **Vilket bibliotek hanterar okrypterade strömmar?** Aspose.PSD för Java erbjuder fullt stöd för rå (okrypterad) bilddata.  
- **Kan jag exportera PSD till PNG efter redigering?** Ja — när du har ett `Graphics`‑objekt kan du rendera PSD:n och spara den som PNG i ett enda anrop.  
- **Behöver jag en licens för utveckling?** En gratis provversion fungerar för testning; en kommersiell licens krävs för produktionsmiljöer.  
- **Är exporten förlustfri?** Export till PNG bevarar den ursprungliga pixeldata, vilket ger förlustfri kvalitet med en mindre filstorlek än den råa PSD‑filen.

## Vad är export av psd till png?
Att exportera PSD till PNG omvandlar ett lagerbaserat Photoshop‑dokument till en enkellager‑, förlustfri rasterbild som kan visas i vilken webbläsare eller bildvisare som helst. Processen behåller transparens, färgdjup och lager‑effekter samtidigt som Photoshop‑specifik metadata tas bort. Den bevarar också den ursprungliga färgprofilen för exakt färgåtergivning.

## Varför använda Aspose.PSD för Java för bildmanipulation?
Aspose.PSD stödjer **50+** in‑ och utdataformat — inklusive PSD, PNG, JPEG, BMP och TIFF—och kan bearbeta filer med **200+ lager** utan att ladda hela dokumentet i minnet. Dess `Raw`‑komprimeringsalternativ lagrar pixeldata okrypterat, vilket garanterar pixel‑perfekt trohet för efterföljande redigering eller arkivering.

## Förutsättningar
Innan vi dyker ner i koden, verifiera att du har följande:

- **Java Development Kit (JDK)** – JDK 8 eller senare installerat.  
- **Aspose.PSD för Java** – Ladda ner den senaste JAR‑filen från den officiella releasesidan: [Aspose.PSD Java nedladdning](https://releases.aspose.com/psd/java/). Du kan också nå den via [denna länk](https://releases.aspose.com/psd/java/) eller [releasesidan](https://releases.aspose.com/psd/java/). För andra Aspose‑produkter, klicka [här](https://releases.aspose.com/).  
- **IDE** – IntelliJ IDEA, Eclipse eller någon annan Java‑kompatibel editor.  
- **Grundläggande Java‑kunskaper** – Bekantskap med klasser, metoder och undantagshantering.

Med dessa på plats är du redo att börja koda.

## Importera paket
`Graphics`‑klassen är Aspose.PSD:s rityta som låter dig rendera eller redigera pixeldata direkt. `PsdImage`‑klassen representerar en PSD‑fil i minnet, medan `PsdOptions` styr hur bilden sparas.

```java
import com.aspose.psd.Graphics;
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.CompressionMethod;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.PsdOptions;
import java.io.ByteArrayInputStream;
import java.io.ByteArrayOutputStream;
```

Låt oss nu dela upp koden i hanterbara steg så att du enkelt kan följa med. Vi kommer att konfigurera miljön, läsa in en PSD‑fil, manipulera den och slutligen spara resultatet.

## Steg 1: Definiera din dokumentkatalog
Innan några filoperationer måste du tala om för programmet var dina PSD‑tillgångar finns. Denna katalogsökväg används genom hela handledningen.

```java
String dataDir = "Your Document Directory";
```

Ersätt `"Your Document Directory"` med den absoluta sökvägen som innehåller `layers.psd`. Att hålla sökvägen konfigurerbar gör koden återanvändbar i olika projekt.

## Steg 2: Skapa en ByteArrayOutputStream
En `ByteArrayOutputStream` är en Java‑ström som lagrar data i minnet som en byte‑array. Den fungerar som en intern buffert för den modifierade bilden, så att du kan fånga de råa bytena innan du skriver dem till disk eller skickar dem över ett nätverk.

```java
ByteArrayOutputStream ms = new ByteArrayOutputStream();
```

Variabeln `ms` kommer att innehålla den okrypterade bilddatan efter `save`‑operationen.

## Steg 3: Läs in PSD‑filen
`PsdImage`‑klassen läser in en PSD‑fil i minnet för manipulation. Att läsa in filen konverterar PSD‑filen på disken till ett `PsdImage`‑objekt som du kan arbeta med. Detta steg är där Aspose.PSD läser filhuvudet, lager och resurser.

```java
PsdImage psdImage = (PsdImage) Image.load(dataDir + "layers.psd");
```

Om sökvägen är felaktig kastar Aspose.PSD ett `FileNotFoundException`, vilket du bör fånga i produktionskod.

## Steg 4: Ställ in PsdOptions för sparande
`PsdOptions` specificerar sparparametrar för PSD‑filer. Att sätta komprimeringsmetoden till `Raw` indikerar att pixeldata ska lagras utan komprimering, vilket bevarar varje pixel exakt som den visas i minnet.

```java
PsdOptions saveOptions = new PsdOptions();
saveOptions.setCompressionMethod(CompressionMethod.Raw);
```

Alternativet `CompressionMethod.Raw` lagrar pixeldata utan någon komprimering, vilket är idealiskt när du planerar att göra ytterligare redigeringar senare.

## Steg 5: Spara bilden till utströmmen
Nu persisterar du PSD:n (med eventuella ändringar) i den tidigare skapade `ByteArrayOutputStream`. `save`‑metoden respekterar de `PsdOptions` du konfigurerat.

```java
psdImage.save(ms, saveOptions);
```

På den här punkten innehåller `ms` den fullständiga binära representationen av den okrypterade PSD‑filen.

## Steg 6: Återställ utströmmen
Efter skrivning sitter strömmens interna pekare i slutet. Att återställa den spolar tillbaka strömmen så att du kan läsa från början.

```java
ms.reset();
```

Tänk på det som att flytta bandhuvudet tillbaka till start innan uppspelning.

## Steg 7: Läs in den nyss skapade bilden
Du kan nu skapa en ny `PsdImage`‑instans direkt från byte‑arrayen. Detta steg verifierar att den sparade datan kan laddas om utan korruption.

```java
PsdImage img = (PsdImage) Image.load(new ByteArrayInputStream(ms.toByteArray()));
```

Om bilden laddas framgångsrikt vet du att den okrypterade strömmen skrevs korrekt.

## Steg 8: Skapa Graphics‑objekt
`Graphics`‑klassen är Aspose.PSD:s ritcanvas. Den erbjuder metoder för att rita former, text och applicera filter direkt på pixelmatrisen i ett `PsdImage`.

```java
Graphics graphics = new Graphics(psdImage);
```

Med detta `Graphics`‑objekt kan du måla nytt innehåll, radera delar eller komponera ytterligare lager.

## Hur exporterar jag PSD till PNG med Aspose.PSD för Java?
Läs in PSD:n med `new PsdImage(dataDir + "layers.psd")`, skapa ett `Graphics`‑objekt, utför önskad ritning och anropa sedan `psdImage.save("output.png", new PngOptions())`. Denna sekvens renderar den redigerade PSD:n och skriver en förlustfri PNG i ett enda steg, med hjälp av Aspose.PSD:s inbyggda konverteringsmotor.

## Manipulera PSD‑lager med Graphics‑objekt
Att ha ett `Graphics`‑instans ger dig pixel‑nivå kontroll över varje lager. Du kan rita geometriska former, rendera text eller applicera egna filter. Eftersom grafik‑kontexten arbetar på den rasteriserade vyn av lagret, blir förändringarna omedelbart synliga när du sparar bilden.

## Vanliga problem och lösningar
- **NullPointerException vid inläsning av filen** – dubbelkolla `dataDir`‑sökvägen och säkerställ att filnamnet stämmer exakt, inklusive skiftlägeskänslighet.  
- **Komprimerad output trots att Raw används** – verifiera att `saveOptions.setCompressionMethod(CompressionMethod.Raw);` anropas **innan** `save`.  
- **Graphics‑objektet är tomt** – se till att du ritar på rätt `PsdImage`‑instans (den du laddade, inte en ny tom bild).  
- **OutOfMemoryError på stora filer** – använd `PsdImage.load(dataDir, LoadOptions)` med `loadOptions.setLoadMode(LoadMode.Memory)` för att strömma stora filer utan att ladda hela dokumentet i RAM.

## Vanliga frågor

### Vad är Aspose.PSD?
Aspose.PSD är ett Java‑bibliotek som gör det möjligt för utvecklare att skapa, redigera och konvertera Photoshop‑PSD‑filer programatiskt utan att behöva Adobe Photoshop. Det stödjer läsning och skrivning av PSD‑filer, hantering av lager, masker, kanaler och diverse bildresurser, samt erbjuder API:er för raster‑ och vektoroperationer, vilket gör det lämpligt för server‑sidig bildbehandling och automatisering.

### Hur kan jag ladda ner Aspose.PSD för Java?
Du kan ladda ner det från den officiella releasesidan: [Aspose.PSD Java nedladdning](https://releases.aspose.com/psd/java/).

### Finns det en gratis provversion för Aspose.PSD?
Ja, en fullt funktionell provversion finns på samma nedladdningssida. Den fungerar för utveckling och utvärdering.

### Kan jag få support för Aspose.PSD?
Absolut! Aspose‑supportforumet ger svar från produktteamet och communityn: [Aspose supportforum](https://forum.aspose.com/c/psd/34).

### Hur kan jag få en tillfällig licens för Aspose.PSD?
Du kan begära en tillfällig licens direkt via Asposes licensportal, som ger en tidsbegränsad nyckel giltig i 30 dagar. Detta låter dig utvärdera hela funktionaliteten i Aspose.PSD utan att köpa en kommersiell licens. Efter provperioden måste du ersätta den tillfälliga nyckeln med en permanent licens för att fortsätta använda biblioteket i produktion. Besök den tillfälliga licensportalen för att generera en tidsbegränsad nyckel: [tillfällig licenssida](https://purchase.aspose.com/temporary-license/).

## Vanliga frågor

**Q: Kan jag använda graphics‑objektet för att redigera bara ett specifikt lager?**  
A: Ja. Efter att ha laddat PSD:n, hämta önskat lager via `psdImage.getLayers().get_Item(index)` och skicka det lagret till `Graphics`‑konstruktorn.

**Q: Påverkar Raw‑komprimeringsmetoden filstorleken?**  
A: Raw lagrar pixeldata utan någon komprimering, så den resulterande filen blir större än en komprimerad PSD, men den garanterar 100 % pixel‑fidelitet.

**Q: Är det möjligt att exportera den redigerade PSD:n till ett annat format (t.ex. PNG)?**  
A: Absolut. Efter redigering, anropa `psdImage.save("output.png", new PngOptions())` — detta är standardmetoden för att **exportera PSD till PNG** med förlustfri kvalitet.

**Q: Vilken Java‑version krävs?**  
A: Aspose.PSD för Java stödjer JDK 8 och senare, inklusive alla LTS‑utgåvor upp till JDK 21.

**Q: Hur frigör jag resurser efter bearbetning?**  
A: Anropa `psdImage.dispose()` och stäng eventuella strömmar (t.ex. `ms.close()`) för att frigöra native‑minne och undvika läckor.

---

**Senast uppdaterad:** 2026-08-01  
**Testat med:** Aspose.PSD för Java (senaste release)  
**Författare:** Aspose  

{{< blocks/products/products-backtop-button >}}

## Relaterade handledningar

- [Spara bilder till ström med Aspose.PSD för Java](/psd/java/advanced-techniques/save-images-to-stream/)
- [Exportera PSD‑lagergrupp till bild med Java](/psd/java/working-with-psd-files/export-psd-layer-group-to-image/)
- [Skapa bild med ström i Aspose.PSD för Java](/psd/java/image-editing/create-image-using-stream/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}