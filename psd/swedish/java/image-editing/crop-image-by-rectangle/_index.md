---
date: 2026-01-01
description: Utforska hur du beskär en bild i Java med Aspose.PSD för Java. Följ vår
  steg‑för‑steg‑guide för att ladda PSD‑fil, beskära bildrektangeln och konvertera
  PSD till JPEG.
linktitle: Crop Image by Rectangle
second_title: Aspose.PSD Java API
title: 'Beskär bild Java: Beskär bild med rektangel med Aspose.PSD'
url: /sv/java/image-editing/crop-image-by-rectangle/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Beskär bild Java: Beskär bild med rektangel med Aspose.PSD

## Introduktion

Att manipulera grafik är en rutinmässig del av **java image processing**, och Aspose.PSD för Java ger dig ett rent, högpresterande API för att arbeta med PSD‑filer. I den här handledningen kommer du att lära dig **hur man beskär en bild** med en rektangel, ladda en PSD‑fil och slutligen konvertera resultatet till en JPEG—allt med bara några rader Java‑kod.

## Snabba svar
- **Vad betyder “crop image java”?** Det avser att beskära en bild till en definierad rektangel med Java‑kod.  
- **Vilket bibliotek hanterar operationen?** Aspose.PSD för Java tillhandahåller de nödvändiga klasserna.  
- **Behöver jag en licens för testning?** En gratis provversion finns tillgänglig; en licens krävs för produktion.  
- **Kan jag konvertera den beskurna PSD‑filen till JPEG?** Ja—använd `JpegOptions` vid sparning.  
- **Hur lång tid tar implementeringen?** Vanligtvis under 10 minuter för ett grundläggande scenario.

## Vad är beskärning av en bildrektangel i Java?

Att beskära en bildrektangel innebär att välja ett specifikt område (definierat av X, Y, bredd och höjd) och kasta bort allt utanför det området. Denna operation är vanlig när du behöver fokusera på en viss region i ett större PSD‑dokument.

## Varför använda Aspose.PSD för denna uppgift?

- **Inga externa beroenden** – fungerar med ren Java.  
- **Stöder PSD, PNG, JPEG och många andra format** – du kan **konvertera PSD till JPEG** omedelbart.  
- **Högupplöst rendering** – behåller lagerinformation och färgprofiler under beskärningen.  

## Förutsättningar

- Java Development Kit (JDK) installerat.  
- Aspose.PSD för Java‑biblioteket – ladda ner det från [webbplatsen](https://releases.aspose.com/psd/java/).  

## Importera paket

Se till att inkludera de nödvändiga paketen i ditt Java‑projekt för att utnyttja funktionerna i Aspose.PSD för Java. Lägg till följande import‑satser i början av din Java‑fil:

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;
import com.aspose.psd.Rectangle;

import com.aspose.psd.imageoptions.JpegOptions;
```

Låt oss nu dela upp processen i flera steg för att guida dig genom att beskära en bild med en rektangel med hjälp av Aspose.PSD för Java.

## Steg 1: Ställ in din dokumentkatalog

```java
String dataDir = "Your Document Directory";
```

Byt ut `"Your Document Directory"` mot den faktiska sökvägen där din PSD‑fil finns.

## Steg 2: Ange käll- och destinationsfiler

```java
String sourceFile = dataDir + "sample.psd";
String destName = dataDir + "CroppingByRectangle_out.jpg";
```

Definiera sökvägarna för din käll‑PSD‑fil och destinations‑JPEG‑filen.

## Steg 3: Ladda och cacha bilden

```java
RasterImage rasterImage = (RasterImage)Image.load(sourceFile);

if (!rasterImage.isCached()) {
    rasterImage.cacheData();
}
```

Här **laddar vi PSD‑filen** i en `RasterImage`‑instans och cachar dess data för att förbättra prestandan.

## Steg 4: Skapa och definiera beskärningsrektangeln

```java
Rectangle rectangle = new Rectangle(20, 20, 20, 20);
```

Skapa en instans av `Rectangle`‑klassen med önskad storlek för beskärning. Parametrarna representerar **X**, **Y**, **bredd** och **höjd** respektive.

## Steg 5: Beskär och spara bilden

```java
rasterImage.crop(rectangle);
rasterImage.save(destName, new JpegOptions());
```

Utför beskärningsoperationen med den angivna rektangeln och **konvertera PSD till JPEG** genom att spara resultatet med `JpegOptions`.

Upprepa dessa steg vid behov och justera parametrarna enligt dina specifika krav.

## Vanliga problem & tips

- **Rektangel utanför bildens gränser** – säkerställ att rektangelns koordinater ligger inom källbildens dimensioner.  
- **Minnesanvändning** – anropa `rasterImage.dispose()` när du är klar för att frigöra inhemska resurser.  
- **Kvalitetskontroll** – du kan sätta `JpegOptions.setQuality(int)` för att styra komprimeringsnivån på den sparade JPEG‑filen.  

## Slutsats

I den här handledningen gick vi igenom processen för **crop image java** med en rektangel med hjälp av Aspose.PSD för Java. Genom att följa dessa steg kan du enkelt integrera kraftfulla bildmanipuleringsfunktioner—ladda en PSD‑fil, beskära en specifik region och konvertera resultatet till JPEG—i vilken Java‑applikation som helst.

## Vanliga frågor

### Q1: Kan jag använda Aspose.PSD för Java med andra Java‑ramverk?

A1: Ja, Aspose.PSD för Java kan integreras med olika Java‑ramverk, vilket ger flexibilitet i dina utvecklingsprojekt.

### Q2: Finns det en gratis provversion av Aspose.PSD för Java?

A2: Ja, du kan komma åt den gratis provversionen [här](https://releases.aspose.com/).

### Q3: Var kan jag hitta ytterligare support eller hjälp?

A3: Besök [Aspose.PSD‑forumet](https://forum.aspose.com/c/psd/34) för gemenskapsstöd och diskussioner.

### Q4: Hur får jag en tillfällig licens för Aspose.PSD för Java?

A4: Du kan skaffa en tillfällig licens [här](https://purchase.aspose.com/temporary-license/).

### Q5: Vilka bildformat stöds för beskärning i Aspose.PSD för Java?

A5: Aspose.PSD för Java stödjer olika bildformat, inklusive PSD, PNG, JPEG och fler.

---

**Senast uppdaterad:** 2026-01-01  
**Testat med:** Aspose.PSD for Java 24.12  
**Författare:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}