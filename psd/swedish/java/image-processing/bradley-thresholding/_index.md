---
date: 2026-01-09
description: Lär dig hur du konverterar PSD till PNG med Bradley-tröskling i Aspose.PSD
  för Java. Denna guide visar hur du väljer optimal tröskel och binäriserar PSD-bilden
  effektivt.
linktitle: Bradley Thresholding
second_title: Aspose.PSD Java API
title: Konvertera PSD till PNG med Bradley-tröskling (Aspose.PSD Java)
url: /sv/java/image-processing/bradley-thresholding/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Konvertera PSD till PNG med Bradley Thresholding (Aspose.PSD Java)

Välkommen till den här omfattande guiden om **konvertera PSD till PNG** med hjälp av Bradley Thresholding i Aspose.PSD för Java. Under de kommande minuterna kommer du att se varför denna teknik är perfekt för att skapa högkontrastiga, binäriserade PNG‑filer från Photoshop‑dokument, och du får en praktisk steg‑för‑steg‑genomgång.

## Snabba svar
- **Kan jag konvertera PSD till PNG med Aspose.PSD?** Ja – ladda PSD‑filen, applicera `binarizeBradley`, och spara sedan som PNG.  
- **Vad betyder “choose optimal threshold”?** Det är känslighetsvärdet (0‑1) som bestämmer hur mörka/licha pixlar klassificeras.  
- **Behöver jag en licens för produktionsbruk?** En kommersiell licens krävs; en gratis provversion fungerar för utvärdering.  
- **Vilka bildformat stöds för sparande?** PNG, JPEG, BMP och många andra via `ImageOptions`‑klasserna.  
- **Är koden kompatibel med Java 8 och senare?** Absolut – Aspose.PSD Java API stöder Java 8+.

## Vad är Bradley Thresholding?
Bradley Thresholding är en adaptiv binäriseringsalgoritm som beräknar ett lokalt medelvärde för varje pixel och jämför pixelns intensitet med det medelvärdet multiplicerat med ett användardefinierat tröskelvärde. Resultatet blir en ren svart‑vit bild som behåller viktiga detaljer.

## Varför konvertera PSD till PNG med Bradley Thresholding?
- **Bevara skarpa kanter** – Idealiskt för OCR, streckkoddetektering eller vilket arbetsflöde som helst som kräver tydlig separation mellan förgrund och bakgrund.  
- **Minska filstorlek** – PNG är förlustfri men ofta mindre efter binärisering.  
- **Plattformsoberoende kompatibilitet** – PNG fungerar överallt, medan PSD är Photoshop‑specifikt.  

## Förutsättningar
Innan vi dyker ner, se till att du har:

1. **Java Development Environment** – JDK 8 eller nyare installerat.  
2. **Aspose.PSD Library** – Ladda ner den senaste JAR‑filen från [here](https://releases.aspose.com/psd/java/).  
3. **Sample PSD Image** – Vilken PSD‑fil du vill konvertera; du kan också använda provfilen som medföljer i Aspose‑exemplen.

## Importera paket
Börja med att importera de nödvändiga klasserna i ditt Java‑projekt:

```java
import com.aspose.psd.Image;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.PngOptions;
```

## Så konverterar du PSD till PNG med Bradley Thresholding
Nedan är hela arbetsflödet uppdelat i tydliga, numrerade steg. Varje steg innehåller en kort förklaring följt av den exakta koden du behöver kopiera‑klistra in.

### Steg 1: Ladda PSD‑bilden
Först, peka på din källfil och ladda den med Aspose.PSD.

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";
String destName = dataDir + "binarized_out.png";

// Load an image
PsdImage image = (PsdImage)Image.load(sourceFile);
```

### Steg 2: Välj optimal tröskel
Tröskelvärdet (intervall 0 – 1) styr hur aggressiv binäriseringen är. En vanlig startpunkt är **0.15**, men du kan justera det för att passa din bild.

```java
// Define threshold value
double threshold = 0.15;
```

### Steg 3: Binärisera PSD‑bilden
Applicera nu Bradley‑algoritmen. Detta steg **binäriserar PSD‑bilden** baserat på den tröskel du valt.

```java
// Call BinarizeBradley method and pass the threshold value as a parameter
image.binarizeBradley(threshold);
```

### Steg 4: Spara resultatet som PNG
Slutligen, skriv den bearbetade bilden till disk i PNG‑format.

```java
// Save the output image
image.save(destName, new PngOptions());
```

Upprepa dessa steg för valfritt antal PSD‑filer du behöver bearbeta, justera tröskeln vid behov för att uppnå bästa visuella resultat.

## Vanliga problem & tips
- **Tröskel för låg/hög:** Om resultatet ser för brusigt eller urtvättat ut, justera `threshold`‑värdet stegvis (t.ex. 0.10 – 0.20).  
- **Minnesanvändning:** Stora PSD‑filer kan vara minnesintensiva. Överväg att bearbeta dem en i taget eller öka JVM‑heap‑storleken (`-Xmx`).  
- **Förhandsgranska innan sparning:** Använd `image.save("preview.bmp", new BmpOptions());` för att inspektera det binäriserade resultatet innan slutlig PNG‑export.

## Vanliga frågor

**Q: Vad är skillnaden mellan `binarizeBradley` och andra tröskelmetoder?**  
A: `binarizeBradley` beräknar ett lokalt medelvärde för varje pixel, vilket gör den mer robust för bilder med ojämn belysning jämfört med global tröskling.

**Q: Kan jag applicera Bradley Thresholding på JPEG‑ eller BMP‑filer?**  
A: Ja. Ladda vilket stödformat som helst med `Image.load(...)`, och anropa sedan `binarizeBradley` innan du sparar.

**Q: Finns det ett sätt att förhandsgranska den binäriserade bilden innan sparning?**  
A: Absolut. Använd någon av Aspose.PSD:s bild‑sparalternativ (t.ex. BMP) för att skriva en temporär förhandsgranskningsfil.

**Q: Var kan jag hitta mer support och resurser?**  
A: Besök [Aspose.PSD forum](https://forum.aspose.com/c/psd/34) för gemenskapsstöd och utforska den fullständiga [dokumentationen](https://reference.aspose.com/psd/java/) för avancerade scenarier.

## Slutsats
Du har nu lärt dig hur du **konverterar PSD till PNG** effektivt genom att **välja en optimal tröskel** och **binärisera PSD‑bilden** med Bradley Thresholding. Denna metod är perfekt för arbetsflöden som kräver rena, högkontrastiga PNG‑utdata från komplexa Photoshop‑filer.

---

**Last Updated:** 2026-01-09  
**Tested With:** Aspose.PSD Java 23.12 (latest at time of writing)  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}