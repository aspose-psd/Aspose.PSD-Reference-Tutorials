---
date: 2026-02-04
description: Lär dig hur du ritar en bildcanvas och lägger över en signatur i Java
  med Aspose.PSD. Följ den här steg‑för‑steg Java‑bildbehandlingshandledningen och
  spara resultatet som PNG.
linktitle: Add a Signature to an Image
second_title: Aspose.PSD Java API
title: rita bildcanvas – Lägg till en signatur med Aspose.PSD för Java
url: /sv/java/advanced-image-effects/add-signature-to-image/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Rita bild på canvas – Lägg till en signatur med Aspose.PSD för Java

## Introduktion

Att lägga till en handskriven eller digital signatur på en bild är ett vanligt krav för kontrakt, fakturor eller vilket dokument som helst som behöver bevis på äkthet. Med **Aspose.PSD for Java** kan du **draw image canvas** och behandla signaturen som ett annat överlagringslager. I den här **java image processing tutorial** går vi igenom hela arbetsflödet—from loading the base picture and the signature file, to initializing graphics, drawing the overlay, and finally **save image png java**‑stil.

## Snabba svar
- **What does “draw image canvas” mean?** Det hänvisar till att rendera en bild på en annan med hjälp av `Graphics`-klassen.  
- **How to add a signature in Java?** Läs in signaturfilen som en `Image` och använd `Graphics.drawImage`.  
- **Which Aspose.PSD version is required?** Vilken som helst ny 24.x-utgåva; koden fungerar med det senaste biblioteket.  
- **Can I overlay multiple images?** Ja – upprepa `drawImage`-anropet med olika källor, vilket möjliggör en **multiple image overlay**.  
- **Do I need a license?** En provversion fungerar för utveckling; en kommersiell licens krävs för produktion.

## Vad betyder “Draw Image on Canvas”?
I Aspose.PSD‑terminologi betyder att rita en bild på en duk att måla ett `Image`‑objekt på ett annat med hjälp av en `Graphics`‑kontext. Denna operation är ryggraden i **overlay images java**‑tekniker såsom att lägga till vattenstämplar, logotyper eller signaturer.

## Hur man ritar bild på canvas med Aspose.PSD
Nedan följer steg‑för‑steg‑processen du kommer att följa för att placera en signatur på någon PSD‑ eller rasterbild.

## Varför använda Aspose.PSD för att överlagra en signatur?
- **Full PSD support** – fungerar med lager, masker och transparens.  
- **No native OS dependencies** – ren Java, perfekt för server‑sidig bearbetning.  
- **High‑performance rendering** – optimerad för stora filer och komplexa sammansättningar.  

## Förutsättningar
- Java Development Kit (JDK) 8 eller högre.  
- Aspose.PSD for Java JAR tillagd i ditt projekts classpath.  
- Två bildfiler: en basbild (t.ex. `layers.psd`) och en signaturgrafik (`sample.psd`).  

## Import Packages

```java
import com.aspose.psd.Graphics;
import static com.aspose.psd.GraphicsUnit.Point;
import com.aspose.psd.Image;
import com.aspose.psd.Point;

import com.aspose.psd.imageoptions.PngOptions;
```

## Step 1: Load Primary and Secondary Images

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

## Step 2: Initialize Graphics (initialize graphics java)

```java
//ExStart:InitializeGraphics
Graphics graphics = new Graphics(canvas);
//ExEnd:InitializeGraphics
```

`Graphics`‑objektet fungerar som en pensel som låter dig **draw image canvas**. Genom att initiera det med den primära `Image` kopplas alla efterföljande ritkommandon till den duken.

## Step 3: Add Signature to Image (how to add signature)

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

I detta kodsnutt **overlay images java** vi genom att placera signaturen i nedre högra hörnet. Justera `Point`‑värdena om du behöver en annan placering.

## Common Issues & Solutions
| Symtom | Orsak | Lösning |
|---------|-------|-----|
| Signaturen visas förvrängd | Olika DPI mellan duk och signatur | Använd `signature.resize` innan ritning eller säkerställ att båda filerna har samma DPI. |
| Utdatafilen är stor | Sparar utan kompression | Skicka en konfigurerad `PngOptions` med `CompressionLevel` satt till ett högre värde. |
| Ingenting ritas | Graphics har inte frigjorts | Anropa `graphics.dispose()` efter ritning (valfritt, men god praxis). |

## Utöka tekniken
- **Add watermark java:** Ersätt signaturbilden med ett semi‑transparent vattenmärke och sätt dess opacitet med `graphics.setOpacity(0.5f)`.  
- **Rotate image java:** Anropa `graphics.rotateTransform(angle)` före `drawImage` för att rotera signaturen eller vattenmärket.  
- **Set image opacity:** Justera opaciteten för vilket överlagring som helst med `graphics.setOpacity(float opacity)` där `0.0` är helt transparent och `1.0` är helt ogenomskinlig.  

## Slutsats
Genom att följa dessa steg har du l och sömlöst **add a signature** med Aspyper eller någon **multiple image overlay**, vilket ger dina Java‑applikationer kraftfulla **java image processing**‑ lägga till du ett.

### Q2: Stöder Aspose.PSD andra bildformat?

A2: Ja, Asphandling för Java?

A3: Ja, du behöver en giltig licens för att använda Aspose.PSD. Besök [Purchase Aspose.PSD](https://purchase.aspose.com/buy) för licensinformation.

### Q4: Hur kan jag få support för Aspose.PSD?

A4: Besök [Aspose.PSD Forum](https://forum.aspose.com/c/psd/34) för gemenskapsstöd och diskussioner.

### Q5: Kan jag prova Aspose.PSD för Java innan jag köper?

A5: Ja, du kan få en [free trial](https://releases.as ett köp.

## YQ: Hur ändrar jag opaciteten för signaturen?**  
A: An sig från 0.0 (transparent) till 1.0 (opak).

**Q appliceraning.

 Absolut. ErsättJpegOptions` och ange önskad kvalitetsnivå.

---

**Senast uppdaterad:** 2026-02-04  
**Testad med:** Aspose.PSD for Java 24.11  
**Författare:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}