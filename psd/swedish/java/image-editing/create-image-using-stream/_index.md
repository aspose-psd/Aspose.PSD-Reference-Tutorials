---
date: 2026-01-01
description: Lär dig hur du skapar bitmap i Java med ström i Aspose.PSD, sparar bildfil
  i Java och ställer in bitar per pixel effektivt.
linktitle: Create Image using Stream
second_title: Aspose.PSD Java API
title: Skapa bitmap i Java med Stream i Aspose.PSD
url: /sv/java/image-editing/create-image-using-stream/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Skapa bitmap java med Stream i Aspose.PSD

## Introduktion

Om du behöver **create bitmap java** bilder i realtid, ger Aspose.PSD för Java dig ett rent, ström‑baserat tillvägagångssätt som är både snabbt och minnes‑effektivt. I den här handledningen går vi igenom hur du genererar en bitmap‑bild från en ström, konfigurerar bitar per pixel och slutligen **save image file java** till disk. I slutet förstår du varför denna metod är idealisk för server‑sidig bildbehandling, batch‑jobb eller någon situation där du vill undvika temporära filer.

## Snabba svar
- **Vad betyder “create bitmap java”?** Det avser att programatiskt generera en BMP‑bild med Java‑kod.  
- **Vilket bibliotek hanterar strömmen?** Aspose.PSD:s `StreamSource`‑ och `FileCreateSource`‑klasser.  
- **Kan jag ställa in färgdjupet?** Ja – använd `BmpOptions.setBitsPerPixel(int)` (t.ex. 24 bpp).  
- **Hur sparar jag resultatet?** Anropa `image.save(outputPath)` för att **save image file java**.  
- **Krävs en licens för produktion?** En giltig Aspose.PSD‑licens behövs för kommersiell användning.

## Förutsättningar för att skapa bitmap java

Innan du börjar, se till att du har:

- **Java Development Kit (JDK)** – någon aktuell version (8 eller högre).  
- **Aspose.PSD for Java** – ladda ner den senaste JAR‑filen från [documentation](https://reference.aspose.com/psd/java/).  
- **IDE** – Eclipse, IntelliJ IDEA eller någon Java‑kompatibel editor du föredrar.

## Importera paket för bitmap‑generering

Börja med att importera de nödvändiga namnutrymmena. Dessa ger dig åtkomst till bildskapande, BMP‑alternativ och strömhantering.

```java
import com.aspose.psd.Image;

import com.aspose.psd.imageoptions.BmpOptions;
import com.aspose.psd.sources.FileCreateSource;
import com.aspose.psd.sources.StreamSource;
import com.aspose.psd.system.io.FileMode;
import com.aspose.psd.system.io.FileStream;
import com.aspose.psd.system.io.Stream;
import java.io.FileInputStream;
```

## Steg 1: Ställ in dokumentkatalogen

Byt ut `"Your Document Directory"` mot den absoluta sökvägen där du lagrar dina käll‑ och utdatafiler.

```java
String dataDir = "Your Document Directory";
```

## Steg 2: Definiera utdatafilens namn

Detta är sökvägen där **save image file java**‑operationen kommer att skriva bitmap‑filen.

```java
String desName = dataDir + "CreatingImageUsingStream_out.bmp";
```

## Steg 3: Konfigurera BmpOptions (ställ in bitar per pixel)

Här **set bits per pixel** till 24 bpp, vilket ger en true‑color bitmap. Justera värdet om du behöver ett annat färgdjup.

```java
BmpOptions imageOptions = new BmpOptions();
imageOptions.setBitsPerPixel(24);
```

## Steg 4: Skapa en FileCreateSource (strömkälla)

`FileCreateSource` omsluter en filström så att Aspose.PSD kan skriva direkt till destinationen utan mellanstegsbuffertar.

```java
FileCreateSource stream = new FileCreateSource(dataDir + "sample_out.bmp");
imageOptions.setSource(stream);
```

## Steg 5: Generera bitmap‑bilden

Denna rad **generates a bitmap java** bild på 500 × 500 pixlar med de alternativ vi definierade tidigare.

```java
Image image = Image.create(imageOptions, 500, 500);
```

## Steg 6: Utför bildbehandling och spara

Efter eventuell valfri manipulation, anropet till `image.save` **saves the image file java** till den plats som anges i `desName`.

```java
// Perform desired image processing operations here
// For example, you could draw shapes, apply filters, etc.

// Save the processed bitmap to disk
image.save(desName);
```

## Slutsats

Du har nu lärt dig hur du **create bitmap java** bilder med strömmar i Aspose.PSD, styr färgdjupet med **set bits per pixel** och **save image file java** effektivt. Experimentera med olika dimensioner, pixelformater eller ytterligare bearbetningssteg för att passa ditt projekts behov.

## Vanliga frågor

### Q1: Kan jag använda Aspose.PSD med andra Java‑bibliotek?

A1: Ja, Aspose.PSD är designat för att sömlöst integreras med andra Java‑bibliotek, vilket ger mångsidighet i dina projekt.

### Q2: Var kan jag hitta support för frågor relaterade till Aspose.PSD?

A2: Besök [Aspose.PSD forum](https://forum.aspose.com/c/psd/34) för community‑support och diskussioner.

### Q3: Finns det en gratis provversion av Aspose.PSD?

A3: Ja, du kan få åtkomst till en gratis provversion [här](https://releases.aspose.com/).

### Q4: Hur får jag en tillfällig licens för Aspose.PSD?

A4: Skaffa en tillfällig licens [här](https://purchase.aspose.com/temporary-license/).

### Q5: Vad är systemkraven för Aspose.PSD?

A5: Se [documentation](https://reference.aspose.com/psd/java/) för detaljerade systemkrav.

---

**Last Updated:** 2026-01-01  
**Tested With:** Aspose.PSD Java latest release  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}