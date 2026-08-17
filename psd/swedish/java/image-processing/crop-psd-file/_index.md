---
date: 2026-08-17
description: Lär dig hur du beskär PSD‑fil i Java med Aspose.PSD för Java – ett snabbt,
  exakt sätt att trimma Photoshop‑dokument i dina Java‑applikationer.
keywords:
- crop psd file java
- aspose.psd java
- java image cropping
lastmod: 2026-08-17
linktitle: Beskär PSD‑fil
og_description: Beskär PSD‑fil i Java med Aspose.PSD för Java. Denna guide visar dig
  steg för steg hur du trimma Photoshop‑filer effektivt, med kodfria förklaringar
  och bästa‑praxis‑tips.
og_image_alt: Guide showing how to crop a PSD file in Java using Aspose.PSD
og_title: Beskär PSD‑fil i Java med Aspose.PSD – snabb bildbeskärning
schemas:
- author: Aspose
  dateModified: '2026-08-17'
  description: Learn how to crop psd file java with Aspose.PSD for Java – a fast,
    precise way to trim Photoshop documents in your Java applications.
  headline: Crop psd file java using Aspose.PSD
  type: TechArticle
- description: Learn how to crop psd file java with Aspose.PSD for Java – a fast,
    precise way to trim Photoshop documents in your Java applications.
  name: Crop psd file java using Aspose.PSD
  steps:
  - name: set document directory
    text: Replace “Your Document Directory” with the absolute or relative path that
      contains the PSD you want to process.
  - name: load PSD file
    text: The `RasterImage` class is Aspose.PSD’s entry point for raster‑based operations
      on a PSD file. Loading the file creates an in‑memory representation that you
      can manipulate.
  - name: define crop area
    text: '`Rectangle` defines the X and Y coordinates together with width and height
      of the region to keep. This class is part of the standard Java AWT package and
      is used by Aspose.PSD to specify cropping bounds.'
  - name: save cropped PSD
    text: After applying the crop, you can persist the result back to PSD format.
      The library writes only the cropped pixels, keeping the original color mode
      and bit depth.
  - name: save cropped image as PNG
    text: If you need a web‑friendly version, export the cropped raster to PNG. Aspose.PSD
      provides PNG save options that let you control compression level and interlacing.
  type: HowTo
- questions:
  - answer: Aspose.PSD for Java.
    question: What library handles PSD cropping in Java?
  - answer: Two API calls after loading the image.
    question: How many lines of code are required for a basic crop?
  - answer: Yes, using the built‑in PNG save options.
    question: Can I export the cropped area as PNG?
  - answer: A commercial license is needed beyond the trial period.
    question: Is a license required for production use?
  - answer: Java 8 and later, including Java 11, 17, and 21.
    question: What Java versions are supported?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- crop psd
- aspose.psd
- java image processing
title: Beskär PSD‑fil i Java med Aspose.PSD
url: /sv/java/image-processing/crop-psd-file/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Beskär psd-fil java med Aspose.PSD

## Introduktion

Om du behöver trimma Photoshop-dokument programatiskt, **crop psd file java** är en vanlig uppgift för Java‑utvecklare som arbetar med grafik‑pipelines, asset‑pipelines eller automatiserade designarbetsflöden. Aspose.PSD för Java tillhandahåller ett dedikerat API som låter dig definiera en rektangel och extrahera den region du behöver på bara några rader kod. I den här handledningen lär du dig varför biblioteket är byggt för högpresterande beskärning, hur du sätter upp din miljö och de exakta stegen för att producera både PSD‑ och PNG‑resultat.

## Snabba svar
- **Vilket bibliotek hanterar PSD-beskärning i Java?** Aspose.PSD för Java.
- **Hur många kodrader krävs för en grundläggande beskärning?** Två API‑anrop efter att bilden har laddats.
- **Kan jag exportera det beskurna området som PNG?** Ja, med de inbyggda PNG‑spara‑alternativen.
- **Krävs en licens för produktionsanvändning?** En kommersiell licens behövs efter provperioden.
- **Vilka Java‑versioner stöds?** Java 8 och senare, inklusive Java 11, 17 och 21.

## Vad är crop psd file java?

Crop psd file java avser processen att programatiskt skära ut en rektangulär region ur ett Photoshop‑dokument (.psd) med Java‑kod. Med Aspose.PSD kan du utföra denna operation utan att starta Photoshop, vilket gör den idealisk för server‑sida bild‑pipelines.

## Varför använda Aspose.PSD för Java?

Aspose.PSD stöder **30+ in‑ och utdataformat** och kan bearbeta PSD‑filer upp till **500 MB** utan att ladda hela dokumentet i minnet, tack vare sin streaming‑arkitektur. Biblioteket bevarar lager, masker och färgprofiler och levererar ett beskuret resultat som matchar Photoshop‑s inbyggda utdata. Denna kvantifierade prestanda låter dig hantera batch‑jobb på vanlig hårdvara med förutsägbar minnesanvändning.

## Förutsättningar

- **Java‑utvecklingsmiljö** – JDK 8 eller nyare installerad och konfigurerad.
- **Aspose.PSD för Java** – ladda ner den senaste JAR‑filen och dokumentationen [Aspose.PSD for Java documentation](https://reference.aspose.com/psd/java/).
- **Exempel PSD‑fil** – placera en .psd‑fil i din projektkatalog så att koden kan hitta den.

## Hur man beskär en PSD‑fil i Java?

Läs in källfilen, definiera den rektangel du vill behålla, applicera beskärningen och spara slutresultatet i önskade format. Hela arbetsflödet kräver bara fem enkla steg, var och en illustrerad med en platshållare där du ska infoga din egen kod.

### Steg 1: ange dokumentkatalog

Byt ut “Your Document Directory” mot den absoluta eller relativa sökvägen som innehåller PSD‑filen du vill bearbeta.

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;
import com.aspose.psd.Rectangle;

import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.imageoptions.PngOptions;
import com.aspose.psd.imageoptions.PsdOptions;
import com.aspose.psd.xmp.types.complex.colorant.ColorType;
```

### Steg 2: ladda PSD‑fil

Klassen `RasterImage` är Aspose.PSD:s ingångspunkt för raster‑baserade operationer på en PSD‑fil. När filen laddas skapas en minnesrepresentation som du kan manipulera.

```java
String dataDir = "Your Document Directory";
```

### Steg 3: definiera beskärningsområde

`Rectangle` definierar X‑ och Y‑koordinaterna samt bredd och höjd på den region som ska behållas. Denna klass är en del av standard‑paketet Java AWT och används av Aspose.PSD för att specificera beskärningsgränser.

```java
String sourceFileName = dataDir + "1.psd";
RasterImage image = (RasterImage)Image.load(sourceFileName);
```

### Steg 4: spara beskuren PSD

Efter att beskärningen har applicerats kan du skriva tillbaka resultatet i PSD‑format. Biblioteket sparar endast de beskurna pixlarna och behåller originalets färgläge och bitdjup.

```java
image.crop(new Rectangle(10, 30, 100, 100));
```

### Steg 5: spara beskuren bild som PNG

Om du behöver en webbvänlig version, exportera den beskurna raster‑bilden till PNG. Aspose.PSD erbjuder PNG‑spara‑alternativ som låter dig styra komprimeringsnivå och interlacing.

```java
String exportPathPsd = dataDir + "CropTest.psd";
image.save(exportPathPsd, new PsdOptions());
```

## Vanliga problem och lösningar

- **Felaktiga rektangelkoordinater** – Se till att X/Y‑värdena startar på 0 för det övre vänstra hörnet; negativa värden kastar ett `ArgumentException`.
- **Minnesökningar vid stora filer** – Använd alternativet `loadOptions.setLoadOnlyVisibleLayers(true)` för att minska minnet när du inte behöver dolda lager.
- **Förlust av färgprofil** – Bevara den ursprungliga ICC‑profilen genom att anropa `image.getColorProfile()` före beskärning och återtilldela den efter operationen.

## Vanliga frågor

### Q1: kan jag använda Aspose.PSD för Java för att beskära bilder i andra format?

A1: Aspose.PSD fokuserar främst på PSD‑filer, men stöder även BMP, GIF, JPEG, PNG, TIFF och flera andra rasterformat för både in‑ och utdata.

### Q2: är Aspose.PSD för Java lämplig för storskalig bildbehandling?

A2: Ja. Bibliotekets streaming‑arkitektur bearbetar hundratals‑sidiga PSD‑filer med ett minnesavtryck under 100 MB, vilket gör det idealiskt för batch‑jobb.

### Q3: finns det licensfrågor att beakta vid användning av Aspose.PSD för Java?

A3: En kommersiell licens krävs för produktionsdistributioner. Detaljer finns på [Aspose.PSD for Java purchase page](https://purchase.aspose.com/buy).

### Q4: hur kan jag få support för Aspose.PSD för Java‑relaterade problem?

A4: Besök [Aspose.PSD for Java forum](https://forum.aspose.com/c/psd/34) för att ställa frågor, dela kodsnuttar och få hjälp från communityn och produktingenjörer.

### Q5: kan jag prova Aspose.PSD för Java innan jag köper?

A5: Ja, en fullt funktionell gratis provversion kan laddas ner [Aspose.PSD free trial download](https://releases.aspose.com/).

{{< blocks/products/products-backtop-button >}}

```java
String exportPathPng = dataDir + "CropTest.png";
PngOptions options = new PngOptions();
options.setColorType(PngColorType.TruecolorWithAlpha);
image.save(exportPathPng, options);
```

## Relaterade handledningar

- [Beskär bild med rektangel i Aspose.PSD för Java](/psd/java/image-editing/crop-image-by-rectangle/)
- [Beskär bild med förskjutningar i Aspose.PSD för Java](/psd/java/image-editing/crop-image-by-shifts/)
- [Hur man roterar bild i Java med Aspose.PSD](/psd/java/advanced-image-manipulation/rotate-image/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}