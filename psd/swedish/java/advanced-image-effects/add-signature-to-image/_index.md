---
date: 2026-04-28
description: Lär dig hur du lägger till en signatur på en bild genom att rita en bild
  på en canvas med Aspose.PSD för Java. Denna Java‑bildbehandlingshandledning visar
  hur du sparar bilden som PNG och överlagrar grafik.
keywords:
- add signature to image
- draw image on canvas
- save image as png
- java image processing
- add watermark java
linktitle: Lägg till en signatur på en bild
second_title: Aspose.PSD Java API
title: Lägg till signatur på bild – Rita bild på canvas med Aspose.PSD för Java
url: /sv/java/advanced-image-effects/add-signature-to-image/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Lägg till signatur till bild – Rita bild på canvas med Aspose.PSD för Java

## Introduktion

Att lägga till en handskriven eller digital **add signature to image** är ett vanligt krav för kontrakt, fakturor eller vilket dokument som helst som behöver bevis på äkthet. I den här handledningen kommer du att se hur Aspose.PSD för Java låter dig **draw image on canvas** och behandla signaturen som ett annat överlagringslager. Vi går igenom att ladda basbilden, ladda signaturfilen, initiera en grafik‑kontext, rita överlägget och slutligen **save image as PNG**. I slutet har du ett återanvändbart mönster för alla **java image processing**‑scenarier, oavsett om det är en signatur, vattenstämpel eller logotyp.

## Snabba svar
- **What does “draw image on canvas” mean?** It refers to rendering one image onto another using the `Graphics` class.  
- **How to add a signature in Java?** Load the signature file as an `Image` and use `Graphics.drawImage`.  
- **Which Aspose.PSD version is required?** Any recent 24.x release; the code works with the latest library.  
- **Can I overlay multiple images?** Yes—repeat the `drawImage` call with different sources.  
- **Do I need a license?** A trial works for development; a commercial license is required for production.

## Vad är “draw image on canvas”?
I Aspose.PSD‑terminologi betyder att rita en bild på en canvas att måla ett `Image`‑objekt på ett annat med hjälp av en `Graphics`‑kontext. Denna operation är ryggraden i **overlay images java**‑tekniker såsom att lägga till vattenstämplar, logotyper eller signaturer.

## Varför använda Aspose.PSD för att överlagra en signatur?
- **Full PSD support** – works with layers, masks, and transparency.  
- **No native OS dependencies** – pure Java, perfect for server‑side processing.  
- **High‑performance rendering** – optimized for large files and complex compositions.  

## Förutsättningar
- Java Development Kit (JDK) 8 or higher.  
- Aspose.PSD for Java JAR added to your project’s classpath.  
- Two image files: a base picture (e.g., `layers.psd`) and a signature graphic (`sample.psd`).  

## Importera paket

```java
import com.aspose.psd.Graphics;
import static com.aspose.psd.GraphicsUnit.Point;
import com.aspose.psd.Image;
import com.aspose.psd.Point;

import com.aspose.psd.imageoptions.PngOptions;
```

## Steg 1: Ladda primära och sekundära bilder

```java
//ExStart:LoadImages
String dataDir = "Your Document Directory";

// Load the primary image (the canvas)
Image canvas = Image.load(dataDir + "layers.psd");

// Load the secondary image containing the signature graphics
Image signature = Image.load(dataDir + "sample.psd");
//ExEnd:LoadImages
```

> **Pro tip:** Håll båda bilderna i samma färgläge (RGB) för att undvika oväntade färgskiftningar vid ritning.

## Steg 2: Initiera grafik (initialize graphics java)

```java
//ExStart:InitializeGraphics
Graphics graphics = new Graphics(canvas);
//ExEnd:InitializeGraphics
```

`Graphics`‑objektet fungerar som en pensel som låter dig **draw image on canvas**. Att initiera det med den primära `Image`‑en binder alla efterföljande ritkommandon till den canvasen.

## Steg 3: Lägg till signatur till bild (how to add signature)

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

I detta kodexempel **overlay images java** genom att placera signaturen i det nedre högra hörnet. Justera `Point`‑värdena om du behöver en annan placering.

## Vanliga problem & lösningar

| Symptom | Orsak | Åtgärd |
|---------|-------|-----|
| Signaturen visas förvrängd | Mismatcherad DPI mellan canvas och signatur | Använd `signature.resize` före ritning eller säkerställ att båda filerna har samma DPI. |
| Utdatafilen är stor | Sparar utan komprimering | Skicka en konfigurerad `PngOptions` med `CompressionLevel` satt till ett högre värde. |
| Ingenting ritas | Graphics inte avyttrad | Anropa `graphics.dispose()` efter ritning (valfritt, men god praxis). |

## Ytterligare tips för verklig användning

- **Multiple signatures:** Call `graphics.drawImage` repeatedly with different `Image` objects and coordinates.  
- **Opacity control:** Use `graphics.setOpacity(float opacity)` before drawing to make the signature semi‑transparent.  
- **Rotating the signature:** Apply `graphics.rotateTransform(angle)` if you need a slanted signature.  
- **Saving to other formats:** Replace `PngOptions` with `JpegOptions` or `BmpOptions` to output JPEG, BMP, etc.

## Vanliga frågor

### Q1: Kan jag lägga till flera signaturer i en bild?

A1: Ja, du kan lägga till flera signaturer genom att upprepa stegen med olika signaturbilder.

### Q2: Stöder Aspose.PSD andra bildformat?

A2: Ja, Aspose.PSD stöder ett brett spektrum av bildformat, vilket säkerställer flexibilitet i bildbehandling.

### Q3: Krävs en licens för att använda Aspose.PSD för Java?

A3: Ja, du behöver en giltig licens för att använda Aspose.PSD. Besök [Purchase Aspose.PSD](https://purchase.aspose.com/buy) för licensinformation.

### Q4: Hur kan jag få support för Aspose.PSD?

A4: Besök [Aspose.PSD Forum](https://forum.aspose.com/c/psd/34) för community‑support och diskussioner.

### Q5: Kan jag prova Aspose.PSD för Java innan jag köper?

A5: Ja, du kan få en [free trial](https://releases.aspose.com/) för att utforska funktionerna innan du gör ett köp.

**Ytterligare vanliga frågor**

**Q: Hur ändrar jag opaciteten på signaturen?**  
A: Använd `graphics.setOpacity(float opacity)` innan du anropar `drawImage`. Värdena sträcker sig från 0.0 (genomskinlig) till 1.0 (opak).

**Q: Är det möjligt att rotera signaturen?**  
A: Ja—tillämpa en transformationsmatris via `graphics.rotateTransform(angle)` innan ritning.

**Q: Kan jag rita signaturen på en JPEG istället för PNG?**  
A: Absolut. Ersätt `PngOptions` med `JpegOptions` och ange önskad kvalitetsnivå.

## Slutsats

Genom att följa dessa steg har du lärt dig **how to add signature to image** genom att **draw an image on canvas** med Aspose.PSD för Java. Samma mönster kan utökas till vattenstämplar, logotyper eller andra överlagrade grafik, vilket ger dina Java‑applikationer kraftfulla **java image processing**‑möjligheter.

---

**Senast uppdaterad:** 2026-04-28  
**Testat med:** Aspose.PSD for Java 24.11  
**Författare:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}