---
date: 2026-05-19
description: Lär dig hur du konverterar PSD till JPEG och roterar bilden 270 grader
  med Aspose.PSD for Java. Denna guide visar hur du roterar PSD-filer, vänder bilder
  och konverterar PSD till JPEG.
keywords:
- convert psd to jpeg
- how to rotate psd
- flip image java
- rotate psd layer
- rotate image without photoshop
linktitle: Rotera bild 270 grader
schemas:
- author: Aspose
  dateModified: '2026-05-19'
  description: Learn how to convert PSD to JPEG and rotate image 270 degrees using
    Aspose.PSD for Java. This guide shows how to rotate PSD files, flip images, and
    convert PSD to JPEG.
  headline: Convert PSD to JPEG & Rotate 270° with Aspose.PSD for Java
  type: TechArticle
- description: Learn how to convert PSD to JPEG and rotate image 270 degrees using
    Aspose.PSD for Java. This guide shows how to rotate PSD files, flip images, and
    convert PSD to JPEG.
  name: Convert PSD to JPEG & Rotate 270° with Aspose.PSD for Java
  steps:
  - name: Load the PSD File
    text: '`Image` is Aspose.PSD''s core class that represents a single PSD document
      in memory. Instantiating it reads only the header information, keeping memory
      usage low.'
  - name: Rotate the Image 270 Degrees
    text: '`rotateFlip` performs the specified rotation and optional flip on the image.
      `RotateFlipType.Rotate270FlipNone` rotates the canvas 270 degrees clockwise
      while leaving the image orientation unchanged. > **Pro tip:** If you also need
      to flip the image horizontally or vertically, choose a different `Ro'
  - name: Convert PSD to JPEG and Save
    text: '`JpegOptions` defines JPEG‑specific parameters such as compression quality.
      The `save` method writes the transformed image to disk in the desired format.
      The file `RotatedImage_out.jpg` now contains the original PSD content rotated
      270 degrees and saved as a JPEG.'
  type: HowTo
- questions:
  - answer: Yes, Aspose.PSD supports PSD, JPEG, PNG, BMP, GIF, TIFF, and many other
      raster formats.
    question: Is Aspose.PSD compatible with different image formats?
  - answer: Absolutely! While `RotateFlipType` provides common angles, you can chain
      multiple calls or use transformation matrices for arbitrary angles.
    question: Can I apply custom rotations, not just predefined flips?
  - answer: Replace `JpegOptions` with `PngOptions` (or the appropriate options class)
      in the `save` method.
    question: How do I convert the rotated PSD to another format, such as PNG?
  - answer: For community help, visit the [Aspose.PSD Forum](https://forum.aspose.com/c/psd/34).
    question: Where can I find additional support or assistance?
  - answer: Yes, you can explore Aspose.PSD with a [free trial](https://releases.aspose.com/).
    question: Is there a free trial available?
  type: FAQPage
second_title: Aspose.PSD Java API
title: Konvertera PSD till JPEG & Rotera 270° med Aspose.PSD for Java
url: /sv/java/advanced-image-manipulation/rotate-image/
weight: 19
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Konvertera PSD till JPEG & rotera bild 270 grader med Aspose.PSD för Java

## Introduktion

I den här **Java bildbehandlingshandledningen** kommer du att lära dig hur du **konverterar PSD till JPEG** samtidigt som du roterar bilden 270 grader med Aspose.PSD för Java. Oavsett om du bygger en batch‑behandlingspipeline, en webbaserad redigerare eller ett skrivbordsverktyg, låter biblioteket dig manipulera PSD‑lager utan Photoshop. Vi kommer också att gå igenom valfri spegling och visa hela end‑to‑end‑flödet från att ladda en PSD‑fil till att spara en JPEG.

## Snabba svar
- **Vilket bibliotek hanterar rotationen?** Aspose.PSD for Java  
- **Vilken rotationsvinkel använder exemplet?** 270 grader  
- **Kan jag också spegla bilden?** Ja – använd `RotateFlipType`‑alternativ som `Rotate90FlipX`  
- **Hur sparar jag resultatet?** I exemplet sparar vi som JPEG med `JpegOptions`  
- **Behöver jag en licens för produktion?** En giltig Aspose.PSD‑licens krävs för kommersiell användning  

## Vad betyder “rotera bild 270 grader”?
Att rotera en bild 270 grader betyder att vrida bilden tre fjärdedelar av en hel cirkel medurs (eller 90 grader moturs). Denna orientering återställer ofta den ursprungliga porträttlayouten efter tidigare transformationer, och den används ofta när bilder har tagits i landskapsläge men ska visas i porträtt. Resultatet blir en korrekt orienterad bild utan kvalitetsförlust.

## Varför använda Aspose.PSD för denna uppgift?
Aspose.PSD stödjer **50+ in- och utdataformat**—inklusive PSD, JPEG, PNG, BMP, GIF och TIFF—och kan bearbeta filer upp till **2 GB** utan att ladda hela dokumentet i minnet. API:et fungerar på alla Java‑runtime (JDK 8+), kräver ingen inbyggd Photoshop‑installation och erbjuder ett enda `rotateFlip`‑anrop som hanterar både rotation och spegling i ett steg.

## Förutsättningar

Innan du börjar, se till att du har:

- **Aspose.PSD for Java**‑biblioteket installerat. Du kan ladda ner det och se den fullständiga API‑referensen [här](https://reference.aspose.com/psd/java/).  
- En Java‑utvecklingsmiljö (JDK 8 eller högre).  
- En exempel‑PSD‑fil som du vill rotera. Uppdatera variabeln `sourceFile` i koden med rätt sökväg till din fil.

## Importera paket

Klasserna `Image`, `RotateFlipType` och `JpegOptions` krävs för att ladda, transformera och spara filen.  
`Image` är kärnklassen som representerar ett PSD‑dokument i minnet.  
`RotateFlipType` enumererar de stödjade rotations‑ och speglingsoperationerna.  
`JpegOptions` konfigurerar JPEG‑utdatainställningar såsom kvalitet.  

```java
import com.aspose.psd.Image;
import com.aspose.psd.RotateFlipType;

import com.aspose.psd.imageoptions.JpegOptions;
```

## Hur konverterar man PSD till JPEG efter rotation?

Läs in käll‑PSD‑filen, applicera en 270‑graders rotation och spara den omedelbart som en JPEG. Detta trestegsförlopp körs på under en sekund för typiska 10‑MP‑bilder på en modern CPU, vilket gör det idealiskt för höggenomströmmande batch‑jobb. Genom att bearbeta endast den nödvändiga bilddatan hålls minnesförbrukningen låg, och den resulterande JPEG‑filen behåller den visuella kvaliteten samtidigt som filstorleken minskar.

### Steg 1: Läs in PSD‑filen

`Image` är Aspose.PSD:s kärnklass som representerar ett enskilt PSD‑dokument i minnet. Vid instansiering läses endast header‑informationen, vilket håller minnesanvändningen låg.

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";
Image image = Image.load(sourceFile);
```

### Steg 2: Rotera bilden 270 grader

`rotateFlip` utför den angivna rotationen och valfri spegling på bilden. `RotateFlipType.Rotate270FlipNone` roterar duken 270 grader medurs samtidigt som bildens orientering förblir oförändrad.

```java
image.rotateFlip(RotateFlipType.Rotate270FlipNone);
```

> **Proffstips:** Om du också behöver spegla bilden horisontellt eller vertikalt, välj en annan `RotateFlipType` såsom `Rotate90FlipX` eller `Rotate180FlipY`.

### Steg 3: Konvertera PSD till JPEG och spara

`JpegOptions` definierar JPEG‑specifika parametrar såsom komprimeringskvalitet. `save`‑metoden skriver den transformerade bilden till disk i önskat format.

```java
String destName = dataDir + "RotatedImage_out.jpg";
image.save(destName, new JpegOptions());
```

Filen `RotatedImage_out.jpg` innehåller nu det ursprungliga PSD‑innehållet roterat 270 grader och sparat som en JPEG.

## Vanliga problem och lösningar

| Problem | Lösning |
|-------|----------|
| **Bilden visas upp och ner** | Verifiera att du använde `Rotate270FlipNone`. För en 90‑graders rotation medurs, använd `Rotate90FlipNone`. |
| **Utdatfilen är korrupt** | Se till att destinationsmappen finns och att du har skrivrättigheter. |
| **Licensundantag** | Installera en tillfällig eller permanent Aspose.PSD‑licens innan du laddar bilden i produktion. |

## Vanliga frågor

**Q: Är Aspose.PSD kompatibel med olika bildformat?**  
A: Ja, Aspose.PSD stödjer PSD, JPEG, PNG, BMP, GIF, TIFF och många andra rasterformat.

**Q: Kan jag applicera anpassade rotationer, inte bara fördefinierade speglingar?**  
A: Absolut! Även om `RotateFlipType` erbjuder vanliga vinklar kan du kedja flera anrop eller använda transformationsmatriser för godtyckliga vinklar.

**Q: Hur konverterar jag den roterade PSD‑filen till ett annat format, till exempel PNG?**  
A: Ersätt `JpegOptions` med `PngOptions` (eller motsvarande options‑klass) i `save`‑metoden.

**Q: Var kan jag hitta ytterligare support eller hjälp?**  
A: För gemenskapsstöd, besök [Aspose.PSD Forum](https://forum.aspose.com/c/psd/34).

**Q: Finns det en gratis provperiod tillgänglig?**  
A: Ja, du kan utforska Aspose.PSD med en [gratis provperiod](https://releases.aspose.com/).

**Q: Hur får jag en tillfällig licens?**  
A: Om du behöver en tillfällig licens kan du skaffa en [här](https://purchase.aspose.com/temporary-license/).

---

**Senast uppdaterad:** 2026-05-19  
**Testad med:** Aspose.PSD for Java 24.12  
**Författare:** Aspose  

{{< blocks/products/products-backtop-button >}}

## Relaterade handledningar

- [Konvertera PSD till rasterbildformat med Aspose.PSD för Java](/psd/java/advanced-techniques/convert-psd-to-raster-formats/)
- [Konvertera PSD till PNG och rotera lager i PSD‑filer med Java](/psd/java/advanced-psd-layer-features-effects/rotate-layers-psd-files/)
- [Hur rotera bild i Java med Aspose.PSD](/psd/java/advanced-image-manipulation/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}