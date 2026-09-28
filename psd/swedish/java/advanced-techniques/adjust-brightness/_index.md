---
date: 2026-09-28
description: Java bildbehandlingshandledning visar hur man justerar ljusstyrkan på
  en bild med Aspose.PSD för Java. Följ steg‑för‑steg‑kod för att ladda, ändra och
  spara PSD‑ eller TIFF‑filer.
keywords:
- java image processing
- aspose psd java
- java image manipulation
- adjust brightness java
lastmod: 2026-09-28
linktitle: Justera ljusstyrka på en bild
og_description: Java bildbehandlingshandledning visar hur man justerar ljusstyrkan
  på en bild med Aspose.PSD för Java. Följ steg‑för‑steg‑kod för att ladda, ändra
  och spara PSD‑ eller TIFF‑filer.
og_image_alt: Guide to adjusting image brightness in Java using Aspose.PSD
og_title: 'Java bildbehandling: justera ljusstyrka med Aspose.PSD'
schemas:
- author: Aspose
  dateModified: '2026-09-28'
  description: Java image processing tutorial shows how to adjust brightness of an
    image using Aspose.PSD for Java. Follow step‑by‑step code to load, modify, and
    save PSD or TIFF files.
  headline: 'Java image processing: adjust brightness with Aspose.PSD'
  type: TechArticle
- description: Java image processing tutorial shows how to adjust brightness of an
    image using Aspose.PSD for Java. Follow step‑by‑step code to load, modify, and
    save PSD or TIFF files.
  name: 'Java image processing: adjust brightness with Aspose.PSD'
  steps:
  - name: Load the image
    text: The `RasterImage` class represents a rasterized version of a PSD or TIFF
      file in memory. It provides direct pixel access for color‑correction operations.
      In this step, we load the target image and cast it to a `RasterImage` for further
      processing.
  - name: Adjust brightness
    text: '`adjustBrightness(int value)` changes the lightness of every pixel by the
      specified integer value. Positive numbers brighten the image; negative numbers
      darken it. The method processes the image in‑place, so no additional object
      creation is required. Here, we use the `adjustBrightness` method to mod'
  - name: Set TiffOptions
    text: '`TiffOptions` specifies the encoding parameters for TIFF output, such as
      bits per sample and photometric interpretation. It lets you control how the
      resulting file is encoded. Configure the `TiffOptions` for saving the adjusted
      image. Adjust the `bitsPerSample` and `photometric` properties based on '
  - name: Save the resultant image
    text: Calling `save` writes the processed raster data to a file using the previously
      defined options. The operation is atomic and guarantees that the output file
      is a valid TIFF image. Finally, save the modified image using the specified
      `TiffOptions`.
  type: HowTo
- questions:
  - answer: Yes, Aspose.PSD for Java supports JPEG, PNG, BMP, GIF, and many other
      raster formats in addition to PSD and TIFF.
    question: Can I adjust brightness in other image formats besides PSD?
  - answer: Wrap the processing code in a try‑catch block and catch `IOException`
      or `ImageProcessingException` to manage file‑access and raster‑operation errors.
    question: How can I handle errors during the image adjustment process?
  - answer: The method accepts integer values from –255 to +255; values outside this
      range are clamped to the nearest limit.
    question: Is there a limit to the range of brightness adjustment?
  - answer: Yes, a commercial license is required for production use. Purchase a license
      [here](https://purchase.aspose.com/buy).
    question: Can I use Aspose.PSD for Java in commercial projects?
  - answer: Yes, you can explore the library with a free trial from [here](https://releases.aspose.com/).
    question: Is there a free trial available?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- java image processing
- aspose psd
- java image manipulation
title: 'Java bildbehandling: justera ljusstyrka med Aspose.PSD'
url: /sv/java/advanced-techniques/adjust-brightness/
weight: 21
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Justera ljusstyrkan på en bild med Aspose.PSD för Java

## Introduktion

I den här **java image processing**‑handledningen kommer du att lära dig hur du justerar ljusstyrkan på en bild direkt från Java‑kod. Att finjustera ljusstyrka är en vanlig uppgift för grafiska formgivare, fotografer och alla som bygger bildbehandlings‑pipelines. I den här **java image manipulation**‑guiden går vi igenom hela arbetsflödet — laddar en PSD/TIFF, applicerar ett ljusstyrke‑offset och sparar resultatet — med hjälp av Aspose.PSD för Java‑biblioteket.

## Snabba svar
- **Vilket bibliotek hanterar ljusstyrka?** Aspose.PSD for Java.  
- **Vilken metod ändrar ljusstyrka?** `RasterImage.adjustBrightness()`.  
- **Kan jag arbeta med PSD‑ och TIFF‑filer?** Ja, API‑et stödjer båda formaten och 10+ ytterligare bildtyper.  
- **Behöver jag en licens för produktion?** En kommersiell licens krävs för icke‑utvärderingsbruk.  
- **Hur lång tid tar implementeringen?** Vanligtvis under 10 minuter för en grundläggande justering.

## Vad är java image processing?
`Java image processing` avser den uppsättning tekniker som låter dig programatiskt läsa, transformera och skriva bilddata med Java. Att justera ljusstyrka är en av de grundläggande operationerna som ändrar den övergripande ljusheten för varje pixel, vilket gör mörka områden ljusare eller ljusa områden mörkare.

## Varför använda Aspose.PSD för Java?
Aspose.PSD för Java erbjuder en omfattande, ren‑Java‑lösning som stödjer ett brett spektrum av raster‑ och vektorformat, eliminerar inhemska beroenden och erbjuder högpresterande cachning för stora filer. Dess omfattande API låter utvecklare utföra komplex färgkorrigering och lagerbaserade redigeringar med minimal kod, vilket gör det idealiskt för både enkla justeringar och avancerade bildbehandlings‑pipelines.

- **Stöder 10+ raster‑ och vektorformat** – PSD, TIFF, JPEG, PNG, BMP, GIF och mer.  
- **Ren‑Java‑implementation** – inga inhemska DLL‑filer eller externa beroenden, så det fungerar på vilken JVM som helst.  
- **Högpresterande cachning** – rasterdata kan cachas, vilket möjliggör upp till 2× snabbare upprepade redigeringar på stora filer.  
- **Rich API surface** – over 150 methods for color correction, layer handling, masks, and compositing.

## Förutsättningar

Innan du dyker ner i handledningen, se till att du har följande förutsättningar:

- Aspose.PSD för Java Library: Download and install the library from the [Aspose.PSD for Java documentation](https://reference.aspose.com/psd/java/).  
- Java Development Kit (JDK) 8 eller högre installerat på din maskin.  
- En utvecklingsmiljö (IDE) såsom IntelliJ IDEA, Eclipse eller VS Code.

## Importera paket

För att börja, importera de nödvändiga paketen till ditt Java‑project. I detta exempel kommer vi att använda följande:

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.psd.fileformats.tiff.enums.TiffPhotometrics;
import com.aspose.psd.imageoptions.TiffOptions;
```

Nu ska vi bryta ner processen för att justera ljusstyrkan på en bild i enkla steg:

## Hur justerar man ljusstyrka med Aspose.PSD?

Ladda ditt källbild, applicera ett ljusstyrke‑offset, konfigurera sparalternativ och skriv resultatet till disk — allt i fyra koncisa steg. Följande avsnitt ger en tydlig steg‑för‑steg‑genomgång som du kan kopiera in i ditt eget projekt. Detta tillvägagångssätt säkerställer att varje operation utförs effektivt och att den slutliga bilden behåller originalkvaliteten samtidigt som den återspeglar den önskade ljusstyrkeändringen.

### Steg 1: Ladda bilden

`RasterImage`‑klassen representerar en rasteriserad version av en PSD‑ eller TIFF‑fil i minnet. Den ger direkt pixelåtkomst för färgkorrigeringsoperationer.

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";
String destName = dataDir + "AdjustBrightness_out.tiff";

// Load an existing image into an instance of RasterImage class
Image image = Image.load(sourceFile);
// Cast object of Image to RasterImage
RasterImage rasterImage = (RasterImage) image;

// Check if RasterImage is cached and Cache RasterImage for better performance
if (!rasterImage.isCached()) {
    rasterImage.cacheData();
}
```

I detta steg laddar vi målbilden och kastar den till en `RasterImage` för vidare bearbetning.

### Steg 2: Justera ljusstyrka

`adjustBrightness(int value)` ändrar ljusheten för varje pixel med det angivna heltalsvärdet. Positiva tal ljusar upp bilden; negativa tal mörkar den. Metoden bearbetar bilden på plats, så ingen extra objekt‑skapande krävs.

```java
// Adjust the brightness
rasterImage.adjustBrightness(-50);
```

Här använder vi `adjustBrightness`‑metoden för att ändra bildens ljusstyrka. I detta exempel minskar vi ljusstyrkan med 50 enheter, men du kan anpassa detta värde efter dina behov.

### Steg 3: Ställ in TiffOptions

`TiffOptions` specificerar kodningsparametrarna för TIFF‑utdata, såsom bits per sample och fotometrisk tolkning. Det låter dig kontrollera hur den resulterande filen kodas.

```java
int[] ushort = {8, 8, 8};
// Create an instance of TiffOptions for the resultant image
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
tiffOptions.setBitsPerSample(ushort);
tiffOptions.setPhotometric(TiffPhotometrics.Rgb);
```

Konfigurera `TiffOptions` för att spara den justerade bilden. Justera egenskaperna `bitsPerSample` och `photometric` efter dina specifika behov.

### Steg 4: Spara den resulterande bilden

Anropet `save` skriver den bearbetade rasterdatan till en fil med de tidigare definierade alternativen. Operationen är atomisk och garanterar att utdatafilen är en giltig TIFF‑bild.

```java
// Save the resultant image
rasterImage.save(destName, tiffOptions);
```

Till sist sparar du den modifierade bilden med de specificerade `TiffOptions`.

## Vanliga problem och lösningar

| Problem | Orsak | Lösning |
|-------|--------|----------|
| **`ClassCastException` när du kastar Image** | Filen är inte en rasterbild (t.ex. en vektor‑PSD). | Verifiera källfilens format eller använd `image instanceof RasterImage` innan du kastar. |
| **Ljusstyrkeändring har ingen effekt** | Bilden cacheades inte innan justeringen. | Anropa `rasterImage.cacheData()` som visas i Steg 1. |
| **Sparad fil verkar korrupt** | Felaktig `TiffOptions`‑konfiguration. | Säkerställ att `bitsPerSample` matchar källbildens djup (vanligtvis 8‑bit per kanal). |

## Vanliga frågor

**Q: Kan jag justera ljusstyrka i andra bildformat än PSD?**  
A: Ja, Aspose.PSD för Java stödjer JPEG, PNG, BMP, GIF och många andra rasterformat utöver PSD och TIFF.

**Q: Hur kan jag hantera fel under bildjusteringsprocessen?**  
A: Omge bearbetningskoden med ett try‑catch‑block och fånga `IOException` eller `ImageProcessingException` för att hantera filåtkomst‑ och raster‑operationsfel.

**Q: Finns det någon gräns för intervallet av ljusstyrkejustering?**  
A: Metoden accepterar heltalsvärden från –255 till +255; värden utanför detta intervall kläms till närmaste gräns.

**Q: Kan jag använda Aspose.PSD för Java i kommersiella projekt?**  
A: Ja, en kommersiell licens krävs för produktionsbruk. Köp en licens [här](https://purchase.aspose.com/buy).

**Q: Är en gratis provversion tillgänglig?**  
A: Ja, du kan utforska biblioteket med en gratis provversion från [här](https://releases.aspose.com/).

**Q: Påverkar `adjustBrightness`‑metoden lagersynlighet?**  
A: Metoden arbetar på den rasteriserade sammansatta bilden, så dolda lager ignoreras under rasteriseringen, vilket bevarar det avsedda visuella resultatet.

**Q: Kan jag kedja flera justeringar (t.ex. kontrast, mättnad) tillsammans?**  
A: Absolut. Efter att ha justerat ljusstyrkan kan du anropa `adjustContrast`, `adjustSaturation` eller andra färgkorrigeringsmetoder på samma `RasterImage`‑instans.

---

**Senast uppdaterad:** 2026-09-28  
**Testat med:** Aspose.PSD for Java 24.12 (senaste vid skrivande tidpunkt)  
**Författare:** Aspose

## Relaterade handledningar

- [Java‑bibliotek för bildbehandling: Invertera lager med Aspose.PSD](/psd/java/advanced-image-manipulation/invert-adjustment-layer/)
- [Konvertera bild till gråskala med Aspose.PSD för Java](/psd/java/advanced-techniques/grayscale-image/)
- [Hur man roterar en bild i en specifik vinkel med Aspose.PSD för Java](/psd/java/advanced-image-manipulation/rotate-image-specific-angle/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}