---
date: 2026-04-12
description: Lär dig hur du ändrar storlek på en bild i Java med Aspose.PSD:s bikubiska
  omprovare. Denna handledning om bildskalning visar steg för steg hur du uppnår överlägsna
  resultat.
keywords:
- resize image java
- image scaling tutorial
- java image library
linktitle: Implementera bikubisk resampler
second_title: Aspose.PSD Java API
title: Ändra storlek på bild i Java – Bikubisk resampler för högkvalitativ skalning
url: /sv/java/advanced-image-manipulation/implement-bicubic-resampler/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Ändra storlek på bild Java – Bicubic Resampler för högkvalitativ skalning

## Introduktion

Om du behöver **resize image java** projekt utan att förlora skärpa eller introducera artefakter, har du kommit till rätt ställe. I den här **image scaling tutorial** går vi igenom hur du använder Aspose.PSD:s Bicubic Resampler – en kraftfull **java image library**-funktion som levererar mjuka, skarpa resultat för PSD‑filer och många andra format. I slutet av den här guiden kommer du att kunna integrera högkvalitativ skalning i vilken Java‑applikation som helst med bara några rader kod.

## Snabba svar
- **What does the Bicubic Resampler do?** Den tillämpar en sofistikerad interpolationsalgoritm som bevarar detaljer vid storleksändring av bilder.  
- **Which ResizeType values are available?** `CubicConvolution` och `Bell` är de två Bicubic‑alternativen som tillhandahålls av Aspose.PSD.  
- **Do I need a license to run the code?** En temporär aspose‑licens fungerar för utvärdering; en full licens krävs för produktion.  
- **What Java version is required?** Alla Java 8+‑runtime är kompatibla med det senaste Aspose.PSD‑biblioteket.  
- **Can I resize other formats (PNG, JPEG) with the same API?** Ja, Aspose.PSD stödjer flera bildtyper, även om exemplen fokuserar på PSD.

## Vad är högkvalitativ bildskalning?

Högkvalitativ bildskalning avser att ändra storlek på en bild samtidigt som skarpa kanter, mjuka gradienter och korrekt färgåtergivning bevaras. Bicubic Resampler uppnår detta genom att beakta värdena hos omgivande pixlar (med cubic convolution eller Bell‑algoritmen) för att beräkna varje ny pixel, vilket ger ett mer naturligt utseende jämfört med nearest‑neighbor‑ eller bilinear‑metoder.

## Varför använda Bicubic Resampler för högkvalitativ bildskalning?

- **Preserves Detail:** Fina texturer och linjearbete förblir tydliga även efter betydande storleksändringar.  
- **Reduces Artifacts:** Minimerar ringing och oskärpa som ofta uppstår med enklare algoritmer.  
- **Easy Integration:** En‑radig metodanrop (`image.resize`) låter dig byta mellan algoritmer utan att skriva om kod.  

## Förutsättningar

Innan du börjar, se till att du har:

- **Aspose.PSD for Java** – ladda ner den senaste JAR‑filen från [Aspose.PSD for Java documentation](https://reference.aspose.com/psd/java/).  
- **Java Development Kit** – JDK 8 eller nyare installerad och konfigurerad.  
- **Sample PSD file** – en testbild (t.ex. `sample_bicubic.psd`) placerad i en känd katalog.  

Dessa objekt tillsammans bildar en solid **java image library**‑grund för handledningen.

## Importera paket

Lägg till de nödvändiga importerna i din Java‑klass. Dessa importerar de centrala Aspose.PSD‑klasserna och `ResizeType`‑enumerationen.

```java
import com.aspose.psd.Image;
import com.aspose.psd.ResizeType;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.PsdOptions;
```

## Hur man ändrar storlek på bild Java med Bicubic Resampler

### Steg 1: Ladda bilden

Först, ladda käll‑PSD‑filen som du vill ändra storlek på. Ersätt `Your Document Directory` med den faktiska sökvägen på din maskin.

```java
String dataDir = "Your Document Directory";
String filePath = dataDir + "sample_bicubic.psd";
PsdImage image = (PsdImage)Image.load(filePath);
```

### Steg 2: Ändra storlek med Cubic Convolution (hög kvalitet)

Applicera nu **Cubic Convolution**‑algoritmen, ett av de två Bicubic‑alternativen som levererar högkvalitativ bildskalning. Exemplet ändrar bildens storlek till 300 × 300 pixlar.

```java
String destNameCubicConvolution = dataDir + "ResamplerCubicConvolutionStripes_after.psd";
image.resize(300, 300, ResizeType.CubicConvolution);
image.save(destNameCubicConvolution, new PsdOptions(image));
```

### Steg 3: Ändra storlek med Bell‑algoritmen (alternativ hög kvalitet)

Om du föredrar **Bell**‑algoritmen, som ger en något annorlunda mjukningseffekt, kan du använda den på samma sätt. Observera att vi laddar om originalbilden för att hålla jämförelsen rättvis.

```java
String destNameBell = dataDir + "ResamplerBellStripes_after.psd";
PsdImage imageBellStripes = (PsdImage)Image.load(filePath);
imageBellStripes.resize(300, 300, ResizeType.Bell);
imageBellStripes.save(destNameBell, new PsdOptions(imageBellStripes));
```

Känn dig fri att experimentera med andra dimensioner eller filformat – justera bara parametrarna därefter.

## Vanliga fallgropar & tips

- **Incorrect Path:** Se till att `dataDir` slutar med en filseparator (`/` eller `\`) som passar ditt OS.  
- **License Exceptions:** Att köra utan en giltig licens kan lägga till ett vattenmärke på utdata‑bilden. Använd en **temporary aspose license** för testning, byt sedan till en permanent för produktion.  
- **Memory Usage:** Stora PSD‑filer kan förbruka mycket minne; överväg att avyttra bilder (`image.dispose()`) efter sparning.  

## Vanliga frågor

**Q: Can I use Aspose.PSD for Java with other image formats?**  
A: Ja, biblioteket stödjer PSD, PNG, JPEG, TIFF, BMP och många fler.

**Q: Is a temporary license available for Aspose.PSD for Java?**  
A: Ja, du kan få en temporär licens från [here](https://purchase.aspose.com/temporary-license/).

**Q: Where can I find support for Aspose.PSD for Java?**  
A: Besök Aspose.PSD‑forumet [here](https://forum.aspose.com/c/psd/34) för supportrelaterade frågor.

**Q: Can I download the Aspose.PSD for Java library?**  
A: Ja, ladda ner biblioteket från releases‑sidan [here](https://releases.aspose.com/psd/java/).

**Q: How do I purchase Aspose.PSD for Java?**  
A: Du kan köpa Aspose.PSD for Java från köpsidan [here](https://purchase.aspose.com/buy).

---

**Senast uppdaterad:** 2026-04-12  
**Testad med:** Aspose.PSD for Java 24.11 (senaste vid skrivande)  
**Författare:** Aspose

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}