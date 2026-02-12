---
date: 2026-02-12
description: Lär dig hur du roterar en bild i en specifik vinkel i Java med Aspose.PSD.
  Den här guiden visar hur du roterar en bild, roterar en bild i grader och hanterar
  bakgrundsfärger.
linktitle: How to Rotate Image on a Specific Angle
second_title: Aspose.PSD Java API
title: Hur man roterar en bild på en specifik vinkel med Aspose.PSD för Java
url: /sv/java/advanced-image-manipulation/rotate-image-specific-angle/
weight: 20
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Hur man roterar en bild i en specifik vinkel med Aspose.PSD för Java

## Introduction

Om du behöver **hur man roterar en bild** programatiskt i en Java‑applikation, erbjuder Aspose.PSD för Java ett rent, högpresterande API som tar hand om det tunga lyftet. Oavsett om du bygger en foto‑editor, genererar miniatyrbilder eller förbereder resurser för en webbtjänst, är rotation av en bild med exakt gradtal ett vanligt krav. I den här handledningen går vi igenom hela processen—från att ladda en PSD‑fil till att spara det roterade resultatet—och lyfter fram bästa praxis såsom cachning och bakgrundshantering.

## Quick Answers
- **Vilket bibliotek är bäst för att rotera bilder i Java?** Aspose.PSD for Java.  
- **Kan jag rotera med vilken grad som helst?** Ja, `rotate`‑metoden accepterar en `float`‑vinkel (positiv eller negativ).  
- **Behöver jag en licens för utveckling?** En gratis provversion fungerar för testning; en licens krävs för produktion.  
- **Vilka bildformat stöds?** PSD, JPEG, PNG, TIFF, GIF, BMP och många fler.  
- **Hur sätter jag en bakgrundsfärg för tomt utrymme?** Skicka en `Color`‑instans till `rotate`‑metoden.

## What is Image Rotation in Java?

Bildrotation innebär att vrida pixelmatrisen runt en pivot‑punkt (vanligtvis centrum) med en given vinkel. I Java kan du uppnå detta manuellt med `Graphics2D`, men Aspose.PSD abstraherar matematiken, hanterar olika färgdjup och bevarar lagerinformation när du arbetar med PSD‑filer.

## Why Use Aspose.PSD for Rotating Images?

- **Precision:** Rotera med vilken bråkdel av en grad som helst utan kvalitetsförlust.  
- **Prestanda:** Inbyggd cachning (`image.cacheData()`) snabbar upp stora filer.  
- **Bakgrundskontroll:** Ange en bakgrundsfärg för att fylla de tomrum som rotationen skapar.  
- **Formatflexibilitet:** Ladda PSD, exportera JPEG, PNG eller något annat stödd format.

## Prerequisites

Innan vi börjar, se till att du har följande:

1. **Java Development Kit (JDK 8 eller senare)** – en fungerande Java‑IDE eller kommandoradsuppsättning.  
2. **Aspose.PSD for Java** – ladda ner den senaste JAR‑filen från den [Aspose.PSD Java‑sidan](https://reference.aspose.com/psd/java/).  
3. **Exempel‑PSD‑fil** – t.ex. `sample.psd` placerad i en mapp som du kan referera till från din kod.

## Import Packages

First, import the classes we’ll need. These imports stay the same regardless of the rotation angle you choose.

```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.imageoptions.JpegOptions;
```

## Step‑by‑Step Guide

### Step 1: Define Your Document Directory

Set the folder that holds the source PSD and where the output will be written.

```java
String dataDir = "Your Document Directory";
```

> **Pro tip:** Use an absolute path or `System.getProperty("user.dir")` to avoid relative‑path surprises.

### Step 2: Specify Source and Destination File Paths

```java
String sourceFile = dataDir + "sample.psd";
String destName = dataDir + "RotatingImageOnSpecificAngle_out.jpg";
```

Du kan ändra `destName` till vilken stödd filändelse som helst (`.png`, `.tiff`, etc.) beroende på dina utskriftsbehov.

### Step 3: Load the Image

```java
RasterImage image = (RasterImage)Image.load(sourceFile);
```

`Image.load` upptäcker automatiskt filformatet och returnerar ett konkret `RasterImage` för raster‑baserade operationer.

### Step 4: Cache Image Data (Optional but Recommended)

```java
if (!image.isCached())
{
    image.cacheData();
}
```

Cachning lagrar bildens pixlar i minnet, vilket snabbar upp efterföljande transformationer—särskilt användbart för stora PSD‑filer.

### Step 5: Rotate the Image

```java
image.rotate(20f, true, Color.getRed());
```

- **20f** – rotationsvinkeln i grader (float). Ändra detta värde för att rotera med vilken vinkel som helst, t.ex. `-45f` för moturs.  
- **true** – behåll originalförhållandet medan duken expanderas för att rymma den roterade bilden.  
- **Color.getRed()** – bakgrundsfärg som fyller de tomma hörnen som rotationen skapar. Byt ut mot `Color.getWhite()` eller någon annan färg vid behov.

#### Rotate Image by Degrees in Java

`rotate`‑metoden accepterar vilket flyttal som helst, så du kan **rotate image by degrees** såsom `30f`, `90f` eller `-15f`. Positiva värden roterar medurs, medan negativa värden roterar moturs.

#### Rotate Image Specific Angle Using Aspose.PSD

Eftersom metoden arbetar med en `float` kan du ange en **rotate image specific angle** som `22.5f` för exakt kontroll i grafisk‑designarbetsflöden.

#### Rotate Image Java Example Summary

Alla stegen ovan demonstrerar ett komplett **rotate image java**‑arbetsflöde—from loading the file to saving the rotated output.

### Step 6: Save the Result

```java
image.save(destName, new JpegOptions());
```

`JpegOptions` låter dig kontrollera kvalitet, komprimering och andra JPEG‑specifika inställningar. För förlustfri utskrift, byt ut mot `PngOptions`.

## Common Issues and Solutions

| Issue | Cause | Fix |
|-------|-------|-----|
| **Tomma hörn efter rotation** | Ingen bakgrundsfärg angiven | Skicka en `Color` (t.ex. `Color.getWhite()`) till `rotate`. |
| **Minnesbristfel på stora PSD‑filer** | Bild inte cachad | Anropa `image.cacheData()` innan bearbetning. |
| **Fel rotationsriktning** | Förvirring mellan negativ och positiv vinkel | Använd negativa värden för medurs rotation (eller tvärtom beroende på ditt koordinatsystem). |
| **Osparade ändringar** | Glömt att anropa `save` | Säkerställ att `image.save(...)` körs efter rotation. |

## Frequently Asked Questions

**Q: Kan jag rotera bilder med transparens med Aspose.PSD för Java?**  
A: Ja. Biblioteket bevarar alfakanaler; undvik bara att ange en ogenomskinlig bakgrundsfärg om du vill ha transparenta hörn.

**Q: Finns det några begränsningar för vilka bildfilformat som stöds för rotation?**  
A: Nej. Aspose.PSD stöder PSD, JPEG, PNG, TIFF, GIF, BMP, JPEG2000, WMF, EMF och många fler.

**Q: Kan jag rotera bilder med en negativ vinkel?**  
A: Absolut. Skicka ett negativt flyttal till `rotate` (t.ex. `-30f`) för att rotera medurs.

**Q: Ger Aspose.PSD real‑tids‑förhandsgranskning av bilden under rotation?**  
A: API‑et är enbart server‑sida. För live‑förhandsgranskning, integrera den roterade bitmapen i ett UI‑ramverk (Swing, JavaFX) och uppdatera vyn.

**Q: Finns det ett community‑forum för Aspose.PSD där jag kan få hjälp?**  
A: Ja, besök [Aspose.PSD‑forumet](https://forum.aspose.com/c/psd/34) för att ställa frågor och dela erfarenheter.

## Conclusion

Du vet nu **hur man roterar en bild** på en specifik vinkel med Aspose.PSD för Java. Genom att utnyttja cachning, bakgrundsfärgs‑kontroll och flexibla utskriftsalternativ kan du integrera exakt rotationsfunktionalitet i vilket Java‑baserat bildarbetsflöde som helst.

---

**Last Updated:** 2026-02-12  
**Tested With:** Aspose.PSD for Java 24.11 (latest at time of writing)  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}