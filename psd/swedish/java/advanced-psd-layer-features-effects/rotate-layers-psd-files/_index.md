---
date: 2026-02-17
description: Lär dig hur du konverterar PSD till PNG, bevarar PNG‑transparens och
  roterar PSD‑lager i Java med Aspose.PSD. Steg‑för‑steg‑guide med kodexempel.
linktitle: Convert PSD to PNG and Rotate Layers in PSD Files using Java
second_title: Aspose.PSD Java API
title: Konvertera PSD till PNG och rotera lager i PSD‑filer med Java
url: /sv/java/advanced-psd-layer-features-effects/rotate-layers-psd-files/
weight: 21
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Konvertera PSD till PNG och rotera lager i PSD-filer med Java

## Introduktion
Om du behöver **konvertera PSD till PNG** samtidigt som du roterar lager, är den här guiden för dig. Oavsett om du bygger ett batch‑bearbetningsverktyg, en webbtjänst som kräver bildmanipulation i realtid, eller helt enkelt automatiserar ett designarbetsflöde, sparar ett programatiskt tillvägagångssätt tid och tar bort beroendet av Adobe Photoshop. I den här tutorialen går vi igenom **hur man roterar PSD**‑lager och exporterar resultatet som en PNG med hjälp av Aspose.PSD‑biblioteket för Java. Låt oss kavla upp ärmarna och få ditt designarbetsflöde att fungera smidigt!

## Snabba svar
- **Vilket bibliotek kan jag använda?** Aspose.PSD for Java  
- **Kan jag både rotera och konvertera i ett steg?** Ja – rotera PSD-filen och spara sedan som PNG  
- **Behöver jag en licens?** En gratis provversion fungerar för testning; en betald licens krävs för produktion  
- **Vilken Java‑version stöds?** Java 8 och senare  
- **Är PNG‑utdata transparent?** Ja, när du sätter `PngColorType.TruecolorWithAlpha`

## Vad betyder “konvertera PSD till PNG”?
Att konvertera ett Photoshop‑dokument (PSD) till en PNG‑bild innebär att extrahera det visuella innehållet—inklusive alla lager, masker och transparens—till ett allmänt stödjande rasterformat. PNG bevarar alfakanaler, vilket gör det idealiskt för webb‑grafik, miniatyrbilder och vidare bildbehandling.

## Varför använda Aspose.PSD för Java för att konvertera PSD till PNG och rotera PSD‑lager?
- **Ingen Photoshop krävs** – fungerar på vilken server eller CI‑miljö som helst  
- **Fullt lagerstöd** – behåller transparens och lager‑effekter intakta  
- **Enkelt API** – rotera, vänd och spara med bara några metodanrop  
- **Plattformsoberoende** – körs på Windows, Linux och macOS  
- **Java‑bildkonvertering** görs enkelt med ett enda bibliotek  

## Förutsättningar
Innan vi dyker ner i koden, se till att du har följande:

- **Java Development Kit (JDK)** – ladda ner från [Oracle‑webbplatsen](https://www.oracle.com/java/technologies/javase-downloads.html).  
- **Integrerad utvecklingsmiljö (IDE)** – IntelliJ IDEA, Eclipse eller NetBeans fungerar alla bra.  
- **Aspose.PSD för Java‑bibliotek** – hämta den senaste JAR‑filen från [release‑sidan](https://releases.aspose.com/psd/java/).  
- **Grundläggande Java‑kunskaper** – bekantskap med klasser, objekt och undantagshantering.

## Steg‑för‑steg‑guide

### Steg 1: Ställ in ditt Java‑projekt
Skapa ett nytt Java‑projekt i din IDE och lägg till Aspose.PSD‑JAR‑filen i projektets byggsökväg.

### Steg 2: Importera nödvändiga klasser
Lägg till följande import‑satser högst upp i din Java‑källfil:

```java
import com.aspose.psd.Image;
import com.aspose.psd.RotateFlipType;
import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.PngOptions;
```

### Steg 3: Definiera filsökvägar
Ange var din käll‑PSD finns och var utdata‑filerna ska skrivas.

```java
String dataDir = "Your Document Directory"; // Change this to your actual document directory.
String sourceFile = dataDir + "1.psd"; // Source PSD file
String pngPath = dataDir + "RotateFlipTest2617.png"; // Output PNG file path
String psdPath = dataDir + "RotateFlipTest2617.psd"; // Output PSD file path
```

> **Proffstips:** Använd en absolut sökväg under testning för att undvika felmeddelandet “file not found”.

### Steg 4: Läs in PSD‑filen
Läs in PSD‑filen i ett manipulerbart objekt.

```java
PsdImage im = (PsdImage) Image.load(sourceFile);
```

Nu representerar `im` hela Photoshop‑dokumentet, inklusive alla lager.

### Steg 5: Rotera bilden (Hur man roterar PSD)
Välj en roterings‑typ från `RotateFlipType`. I detta exempel roterar vi 270° och vänder båda axlarna.

```java
int flipType = RotateFlipType.Rotate270FlipXY; // Choose the rotation type
im.rotateFlip(flipType); // Rotate the image
```

Känn dig fri att experimentera med andra värden såsom `Rotate90FlipNone` eller `Rotate180FlipX`. Detta är delen **hur man roterar PSD** i tutorialen.

### Steg 6: Spara den roterade bilden som PNG (konvertera PSD till PNG)
Konfigurera PNG‑alternativ för att behålla transparens och spara sedan.

```java
PngOptions options = new PngOptions();
options.setColorType(PngColorType.TruecolorWithAlpha); // Preserve transparency
im.save(pngPath, options); // Save the rotated image
```

Den resulterande PNG‑filen behåller lager‑transparensen, vilket säkerställer **bevara PNG‑transparens** för vidare användning.

### Steg 7: Spara den modifierade PSD‑filen (valfritt)
Om du också behöver en ny PSD med rotationen applicerad, spara den tillbaka.

```java
im.save(psdPath);
```

Du har nu både en PNG‑förhandsvisning och en uppdaterad PSD‑fil.

## Vanliga problem och lösningar
- **Fil ej hittad:** Verifiera att `dataDir` slutar med en sökvägsseparator (`/` eller `\`).  
- **OutOfMemoryError på stora PSD‑filer:** Öka JVM‑heap‑storleken (`-Xmx2g`).  
- **Transparens förlorad:** Säkerställ att `PngColorType.TruecolorWithAlpha` är satt; annars sparas PNG utan alfa.  
- **Vändning av PSD‑bild beter sig inte som förväntat:** Dubbelkolla den `RotateFlipType`‑konstant du valt; vissa konstanter kombinerar rotation och vändning i ett steg.

## Vanliga frågor

**Q: Kan jag rotera ett specifikt lager i en PSD‑fil?**  
A: Ja, du kan använda `Layer.rotateFlip()` på enskilda lager efter att ha itererat genom `im.getLayers()`.

**Q: Finns det några prestandabegränsningar med Aspose.PSD för Java?**  
A: Biblioteket hanterar de flesta filer effektivt, men extremt stora PSD‑filer (>500 MB) kan kräva extra minne.

**Q: Är Aspose.PSD gratis att använda?**  
A: Aspose erbjuder en gratis provversion, men en betald licens behövs för produktion. Se den [tillfälliga licensen](https://purchase.aspose.com/temporary-license/) för testning.

**Q: Var kan jag hitta detaljerad dokumentation?**  
A: Du hittar omfattande dokumentation på [Aspose.PSD Documentation](https://reference.aspose.com/psd/java/).

**Q: Vad gör jag om jag stöter på problem när jag använder Aspose.PSD?**  
A: Sök hjälp via [Aspose Support Forum](https://forum.aspose.com/c/psd/34).

**Q: Bevarar konvertering av PSD till PNG lager‑effekter?**  
A: Ja, när du sparar med `PngColorType.TruecolorWithAlpha` rasteriseras de flesta visuella effekter in i PNG‑filen.

**Q: Kan jag batch‑processa flera PSD‑filer?**  
A: Absolut. Lägg koden i en loop som itererar över en katalog med PSD‑filer.

**Q: Är det möjligt att ställa in PNG‑komprimeringsnivå?**  
A: Klassen `PngOptions` erbjuder en `setCompressionLevel(int)`‑metod för finjustering.

**Q: Måste jag stänga bild‑objektet?**  
A: `PsdImage` implementerar `Closeable`; anropa `im.close()` i ett `finally`‑block eller använd try‑with‑resources.

**Q: Kommer den roterade PNG‑filen ha samma dimensioner som originalet?**  
A: Rotering med 90° eller 270° byter bredd och höjd. PNG‑filen kommer att spegla den nya orienteringen.

## Slutsats
Genom att utnyttja Aspose.PSD för Java kan du **konvertera PSD till PNG**, **bevara PNG‑transparens** och **rotera PSD**‑lager med bara några rader kod. Detta tillvägagångssätt eliminerar behovet av Photoshop, snabbar upp automatiserade arbetsflöden och ger dig full kontroll över bildutdata. Prova det i dina egna projekt och se hur mycket tid du sparar!

---

**Last Updated:** 2026-02-17  
**Tested With:** Aspose.PSD for Java 24.11  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}