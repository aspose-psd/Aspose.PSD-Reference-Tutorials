---
date: 2025-12-15
description: Lär dig hur du konverterar PSD till PNG och roterar PSD‑lager i Java
  med Aspose.PSD. Steg‑för‑steg‑guide med kodexempel.
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
Om du behöver **konvertera PSD till PNG** samtidigt som du roterar lager, är den här guiden för dig. Oavsett om du bygger ett batch‑bearbetningsverktyg eller integrerar bildmanipulering i en webbtjänst, sparar ett programatiskt tillvägagångssätt tid och tar bort beroendet av Adobe Photoshop. I den här tutorialen visar vi dig **hur du roterar PSD**‑lager och exporterar resultatet som en PNG med hjälp av Aspose.PSD‑biblioteket för Java. Låt oss kavla upp ärmarna och få ditt design‑arbetsflöde att fungera smidigt!

## Snabba svar
- **Vilket bibliotek kan jag använda?** Aspose.PSD for Java  
- **Kan jag både rotera och konvertera i ett steg?** Ja – rotera PSD‑filen och spara sedan som PNG  
- **Behöver jag en licens?** En gratis provversion fungerar för testning; en betald licens krävs för produktion  
- **Vilken Java-version stöds?** Java 8 och senare  
- **Är PNG-utdata transparent?** Ja, när du sätter `PngColorType.TruecolorWithAlpha`

## Vad betyder “konvertera PSD till PNG”?
Att konvertera ett Photoshop‑dokument (PSD) till en PNG‑bild innebär att extrahera det visuella innehållet – inklusive alla lager, masker och transparens – till ett allmänt stödformat för rasterbilder. PNG bevarar alfa‑kanaler, vilket gör det idealiskt för webb‑grafik, miniatyrer och vidare bildbehandling.

## Varför använda Aspose.PSD för Java för att konvertera PSD till PNG och rotera PSD‑lager?
- **Ingen Photoshop krävs** – fungerar på alla servrar eller CI‑miljöer  
- **Full lagerstöd** – behåller transparens och lager‑effekter intakta  
- **Enkelt API** – rotera, vänd och spara med bara några metodanrop  
- **Plattformsoberoende** – körs på Windows, Linux och macOS  

## Förutsättningar
Innan vi dyker ner i koden, se till att du har följande:

- **Java Development Kit (JDK)** – ladda ner från [Oracle website](https://www.oracle.com/java/technologies/javase-downloads.html).  
- **Integrerad utvecklingsmiljö (IDE)** – IntelliJ IDEA, Eclipse eller NetBeans fungerar alla bra.  
- **Aspose.PSD for Java library** – hämta den senaste JAR‑filen från [release page](https://releases.aspose.com/psd/java/).  
- **Grundläggande Java‑kunskaper** – bekantskap med klasser, objekt och undantagshantering.

## Steg‑för‑steg‑guide

### Steg 1: Skapa ditt Java‑projekt
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

Dessa klasser ger dig åtkomst till bildladdning, rotation och PNG‑specifika alternativ.

### Steg 3: Definiera filsökvägar
Ange var din käll‑PSD‑fil finns och var utdata‑filerna ska skrivas.

```java
String dataDir = "Your Document Directory"; // Change this to your actual document directory.
String sourceFile = dataDir + "1.psd"; // Source PSD file
String pngPath = dataDir + "RotateFlipTest2617.png"; // Output PNG file path
String psdPath = dataDir + "RotateFlipTest2617.psd"; // Output PSD file path
```

> **Pro tip:** Använd en absolut sökväg under testning för att undvika fel som “file not found”.

### Steg 4: Läs in PSD‑filen
Läs in PSD‑filen i ett manipulerbart objekt.

```java
PsdImage im = (PsdImage) Image.load(sourceFile);
```

Nu representerar `im` hela Photoshop‑dokumentet, inklusive alla lager.

### Steg 5: Rotera bilden (Hur man roterar PSD)
Välj en roterings‑typ från `RotateFlipType`. I det här exemplet roterar vi 270° och vänder båda axlarna.

```java
int flipType = RotateFlipType.Rotate270FlipXY; // Choose the rotation type
im.rotateFlip(flipType); // Rotate the image
```

Känn dig fri att experimentera med andra värden såsom `Rotate90FlipNone` eller `Rotate180FlipX`.

### Steg 6: Spara den roterade bilden som PNG (konvertera PSD till PNG)
Konfigurera PNG‑alternativ för att behålla transparens, och spara sedan.

```java
PngOptions options = new PngOptions();
options.setColorType(PngColorType.TruecolorWithAlpha); // Preserve transparency
im.save(pngPath, options); // Save the rotated image
```

Den resulterande PNG‑filen behåller lager‑transparensen, vilket gör den redo för webbbruk.

### Steg 7: Spara den modifierade PSD‑filen (valfritt)
Om du också behöver en ny PSD med rotationen applicerad, spara den tillbaka.

```java
im.save(psdPath);
```

Du har nu både en PNG‑förhandsvisning och en uppdaterad PSD‑fil.

## Vanliga problem och lösningar
- **Fil ej hittad:** Verifiera att `dataDir` slutar med en sökvägsseparator (`/` eller `\`).  
- **OutOfMemoryError vid stora PSD‑filer:** Öka JVM‑heap‑storlek (`-Xmx2g`).  
- **Transparens förlorad:** Se till att `PngColorType.TruecolorWithAlpha` är satt; annars sparas PNG utan alfa.

## Vanliga frågor

### Kan jag rotera ett specifikt lager i en PSD‑fil?
Ja, du kan använda `Layer.rotateFlip()` på enskilda lager efter att ha itererat genom `im.getLayers()`.

### Finns det några prestandabegränsningar med Aspose.PSD för Java?
Biblioteket hanterar de flesta filer effektivt, men extremt stora PSD‑filer (>500 MB) kan kräva extra minne.

### Är Aspose.PSD gratis att använda?
Aspose erbjuder en gratis provversion, men en betald licens behövs för produktion. Se den [temporary license](https://purchase.aspose.com/temporary-license/) för testning.

### Var kan jag hitta detaljerad dokumentation?
Du hittar omfattande dokumentation på [Aspose.PSD Documentation](https://reference.aspose.com/psd/java/).

### Vad gör jag om jag stöter på problem när jag använder Aspose.PSD?
Sök hjälp via [Aspose Support Forum](https://forum.aspose.com/c/psd/34).

## Ytterligare vanliga frågor

**Q: Bevarar konvertering av PSD till PNG lager‑effekter?**  
A: Ja, när du sparar med `PngColorType.TruecolorWithAlpha` rasteriseras de flesta visuella effekter in i PNG‑filen.

**Q: Kan jag batch‑processa flera PSD‑filer?**  
A: Absolut. Lägg in koden i en loop som itererar över en katalog med PSD‑filer.

**Q: Är det möjligt att ställa in PNG‑komprimeringsnivå?**  
A: Klassen `PngOptions` erbjuder en metod `setCompressionLevel(int)` för finjustering.

**Q: Måste jag stänga bild‑objektet?**  
A: `PsdImage` implementerar `Closeable`; anropa `im.close()` i ett `finally`‑block eller använd try‑with‑resources.

**Q: Kommer den roterade PNG‑filen ha samma dimensioner som originalet?**  
A: Rotering med 90° eller 270° byter bredd och höjd. PNG‑filen kommer att spegla den nya orienteringen.

## Slutsats
Genom att utnyttja Aspose.PSD för Java kan du **konvertera PSD till PNG** och **rotera PSD**‑lager med bara några rader kod. Detta tillvägagångssätt eliminerar behovet av Photoshop, snabbar upp automatiserade arbetsflöden och ger dig full kontroll över bildutdata. Prova det i dina egna projekt och se hur mycket tid du sparar!

---

**Last Updated:** 2025-12-15  
**Tested With:** Aspose.PSD for Java 24.11  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}