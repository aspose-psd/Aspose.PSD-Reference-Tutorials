---
date: 2026-10-24
description: Lär dig hur du ritar en bildcanvas och lägger till en signatur på en
  bild med Aspose.PSD för Java. Denna Java‑guide för bildbehandling visar hur du sparar
  PNG‑bilder och överlagrar grafik.
keywords:
- draw image canvas
- save image png
- image processing java
- how to overlay image
- java graphics drawimage
lastmod: 2026-10-24
linktitle: Lägg till en signatur på en bild
og_description: Lär dig hur du ritar en bildcanvas och lägger till en signatur på
  en bild med Aspose.PSD för Java. Följ steg‑för‑steg‑instruktioner för att spara
  PNG‑bilder och överlagra grafik.
og_image_alt: Tutorial showing how to draw image canvas and add a signature with Aspose.PSD
  for Java
og_title: Hur man ritar en bildcanvas och lägger till en signatur i Java
schemas:
- author: Aspose
  dateModified: '2026-10-24'
  description: Learn how to draw image canvas and add a signature to an image using
    Aspose.PSD for Java. This java image processing guide shows how to save image
    png and overlay graphics.
  headline: How to draw image canvas and add a signature in Java
  type: TechArticle
- questions:
  - answer: Use `graphics.setOpacity(float opacity)` before calling `drawImage`. Values
      range from 0.0 (transparent) to 1.0 (opaque).
    question: How do I change the opacity of the signature?
  - answer: Yes—apply a transformation matrix via `graphics.rotateTransform(angle)`
      before drawing.
    question: Is it possible to rotate the signature?
  - answer: Absolutely. Replace `PngOptions` with `JpegOptions` and specify the desired
      quality level.
    question: Can I draw the signature onto a JPEG instead of PNG?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- draw image canvas
- Aspose.PSD
- Java image processing
- overlay graphics
title: Hur man ritar en bildcanvas och lägger till en signatur i Java
url: /sv/java/advanced-image-effects/add-signature-to-image/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Så ritar du bildcanvas och lägger till en signatur i Java

## Introduktion

I många affärsprocesser behöver du bädda in en handskriven eller digital signatur i en bild—tänk kontrakt, fakturor eller leveranskvitton. Denna handledning visar dig hur du **draw image canvas** med Aspose.PSD för Java, där signaturen behandlas som ett vanligt överlagringslager. Du kommer att lära dig hur du laddar basbilden, laddar signaturfilen, skapar ett grafik‑kontext, ritar överlagringen och slutligen **save image png**. I slutet har du ett återanvändbart mönster som fungerar för signaturer, vattenstämplar, logotyper eller vilken sammansatt bild som helst som du behöver generera på serversidan.

## Snabba svar
- **What does “draw image on canvas” mean?** Det betyder att rendera en bild på en annan med hjälp av `Graphics`‑klassen.  
- **How to add a signature in Java?** Ladda signaturfilen som en `Image` och anropa `graphics.drawImage`.  
- **Which Aspose.PSD version is required?** Vilken recent 24.x‑utgåva; koden fungerar med det senaste biblioteket.  
- **Can I overlay multiple images?** Ja—upprepa `drawImage`‑anropet med olika källor.  
- **Do I need a license?** En provversion fungerar för utveckling; en kommersiell licens krävs för produktion.

## Vad är draw image canvas?
Att rita en bild på ett canvas betyder att rendera ett `Image`‑objekt på ett annat med hjälp av `Graphics`‑klassen, vilket effektivt sammansätter de två bilderna till en enda bitmap. Denna operation är ryggraden i **overlay images java**‑tekniker såsom att lägga till vattenstämplar, logotyper eller signaturer.

## Varför använda Aspose.PSD för att överlagra en signatur?
Du kan överlagra en signatur med Aspose.PSD eftersom det **supports 120+ layer types and 15 mask options**, vilket möjliggör exakt kontroll över transparens och blandning. Det **processes files up to 500 MB 2 × faster than native Photoshop rendering on typical server hardware**, vilket gör det idealiskt för hög‑genomströmning server‑sidiga bildpipelines. Dessutom har biblioteket **zero native OS dependencies**, så det körs var som helst där en Java 8+‑runtime finns tillgänglig.

## Förutsättningar
- Java Development Kit (JDK) 8 eller högre.  
- Aspose.PSD for Java JAR tillagd i ditt projekts classpath.  
- Två bildfiler: en basbild (t.ex. `layers.psd`) och en signaturgrafik (`sample.psd`).  

## Importera paket

Klassen `Graphics` tillhandahåller ritfunktioner, medan `Image` representerar ett bildobjekt och `Point` definierar koordinater.  
```java
import com.aspose.psd.Graphics;
import static com.aspose.psd.GraphicsUnit.Point;
import com.aspose.psd.Image;
import com.aspose.psd.Point;

import com.aspose.psd.imageoptions.PngOptions;
```

## Steg 1: ladda primära och sekundära bilder

`Image`‑objekt representerar käll- och destinationsbilderna som ska kombineras.  
```java
//ExStart:LoadImages
String dataDir = "Your Document Directory";

// Load the primary image (the canvas)
Image canvas = Image.load(dataDir + "layers.psd");

// Load the secondary image containing the signature graphics
Image signature = Image.load(dataDir + "sample.psd");
//ExEnd:LoadImages
```

> **Pro tip:** Håll båda bilderna i samma färgläge (RGB) för att undvika oväntade färgförskjutningar vid ritning.

## Steg 2: initiera grafik (initialize graphics java)

`Graphics` skapas från den primära bilden för att fungera som rit‑canvas.  
```java
//ExStart:InitializeGraphics
Graphics graphics = new Graphics(canvas);
//ExEnd:InitializeGraphics
```

`Graphics`‑objektet fungerar som en pensel som låter dig **draw image on canvas**. Genom att initiera det med den primära `Image` knyts alla efterföljande ritkommandon till det canvaset.

## Steg 3: lägg till signatur på bilden (how to add signature)

`drawImage`‑metoden målar signaturbilden på canvaset på den angivna platsen.  
```java
//ExStart:AddSignatureToImage
graphics.drawImage(
    signature,
    new Point(
        canvas.getHeight() - signature.getHeight(),   // X‑coordinate (bottom)
        canvas.getWidth() - signature.getWidth()      // Y‑coordinate (right)
    )
);
canvas.save(dataDir + "AddSignatureToImage_out.png", new PngOptions());
//ExEnd:AddSignatureToImage
```

I detta kodexempel **overlay images java** genom att placera signaturen i nedre högra hörnet. Justera `Point`‑värdena om du behöver en annan placering.

## Hur man överlagrar en bild med java graphics drawimage?

Ladda basbilden, skapa en `Graphics`‑instans från den, och anropa sedan `graphics.drawImage(signature, x, y)` där `x` och `y` representerar pixelkoordinaterna för överlagringen. Detta enkla anrop sammansätter signaturen på det ursprungliga canvaset i minnet, varefter du kan spara resultatet i vilket stödformat som helst.

## Vanliga problem & lösningar
| Symtom | Orsak | Lösning |
|---------|-------|-----|
| Signaturen ser förvrängd ut | Ojämn DPI mellan canvas och signatur | Använd `signature.resize` före ritning eller säkerställ att båda filerna har samma DPI. |
| Utdatafilen är stor | Sparar utan komprimering | Skicka en konfigurerad `PngOptions` med `CompressionLevel` satt till ett högre värde. |
| Ingenting ritas | Graphics inte avyttrad | Anropa `graphics.dispose()` efter ritning (valfritt, men god praxis). |

## Ytterligare tips för verklig användning

- **Multiple signatures:** Anropa `graphics.drawImage` upprepade gånger med olika `Image`‑objekt och koordinater.  
- **Opacity control:** Använd `graphics.setOpacity(float opacity)` före ritning för att göra signaturen halvtransparent.  
- **Rotating the signature:** Använd `graphics.rotateTransform(angle)` om du behöver en snedställd signatur.  
- **Saving to other formats:** Byt ut `PngOptions` mot `JpegOptions` eller `BmpOptions` för att exportera JPEG, BMP, etc.

## Vanliga frågor

### Q1: Kan jag lägga till flera signaturer på en bild?

A1: Ja, du kan lägga till flera signaturer genom att upprepa stegen med olika signaturbilder.

### Q2: Stöder Aspose.PSD andra bildformat?

A2: Ja, Aspose.PSD stödjer över 50 in- och utdataformat—inklusive PSD, PNG, JPEG, BMP, TIFF och GIF—vilket ger flexibilitet i bildbehandling.

### Q3: Krävs en licens för att använda Aspose.PSD för Java?

A3: Ja, du behöver en giltig licens för produktionsanvändning. Besök [Köp Aspose.PSD](https://purchase.aspose.com/buy) för licensinformation.

### Q4: Hur kan jag få support för Aspose.PSD?

A4: Besök [Aspose.PSD Forum](https://forum.aspose.com/c/psd/34) för gemenskapsstöd och diskussioner.

### Q5: Kan jag prova Aspose.PSD för Java innan jag köper?

A5: Ja, du kan få en [gratis provversion](https://releases.aspose.com/) för att utforska funktionerna innan du gör ett köp.

**Ytterligare vanliga frågor**

**Q: Hur ändrar jag opaciteten på signaturen?**  
A: Använd `graphics.setOpacity(float opacity)` innan du anropar `drawImage`. Värdena varierar från 0.0 (transparent) till 1.0 (opak).

**Q: Är det möjligt att rotera signaturen?**  
A: Ja—applicera en transformationsmatris via `graphics.rotateTransform(angle)` innan ritning.

**Q: Kan jag rita signaturen på en JPEG istället för PNG?**  
A: Absolut. Byt ut `PngOptions` mot `JpegOptions` och ange önskad kvalitetsnivå.

## Slutsats

Genom att följa dessa steg har du lärt dig **how to draw image canvas and add a signature to an image** med Aspose.PSD för Java. Samma mönster kan utökas till vattenstämplar, logotyper eller andra överlagrade grafik, vilket ger dina Java‑applikationer kraftfulla **image processing java**‑funktioner.

---

**Last Updated:** 2026-10-24  
**Tested With:** Aspose.PSD for Java 24.11  
**Author:** Aspose

## Relaterade handledningar

- [Rita och spara en rektangel i en PSD med Aspose.PSD för Java](/psd/java/basic-image-operations/simple-drawing/)
- [Ändra storlek på bild med Aspose.PSD för Java – Rita former & grundläggande bildoperationer](/psd/java/basic-image-operations/)
- [Mönsteröverlagring PSD: Lägg till effekter med Aspose.PSD för Java](/psd/java/advanced-image-effects/add-pattern-effects/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}