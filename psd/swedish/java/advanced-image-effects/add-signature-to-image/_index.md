---
date: 2025-12-02
description: Lär dig hur du ritar en bild på en canvas och lägger över en signatur
  i Java med Aspose.PSD. Följ den här steg‑för‑steg Java‑bildbehandlingshandledningen
  och spara resultatet som PNG.
linktitle: Add a Signature to an Image
second_title: Aspose.PSD Java API
title: Rita bild på canvas – Lägg till en signatur med Aspose.PSD för Java
url: /sv/java/advanced-image-effects/add-signature-to-image/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Rita bild på canvas – Lägg till en signatur med Aspose.PSD för Java

## Introduktion

Att lägga till en handskriven eller digital signatur på en bild är ett vanligt krav för kontrakt, fakturor eller något dokument som behöver bevis på äkthet. Med **Aspose.PSD for Java** kan du **draw image on canvas** och behandla signaturen som ett annat överlagringslager. I den här **java image processing tutorial** går vi igenom hela arbetsflödet—from loading the base picture and the signature file, to initializing graphics, drawing the overlay, and finally **save image png java**‑stil.

## Snabba svar
- **Vad betyder “draw image on canvas”?** Det avser att rendera en bild på en annan med hjälp av `Graphics`-klassen.  
- **Hur lägger man till en signatur i Java?** Läs in signaturfilen som en `Image` och använd `Graphics.drawImage`.  
- **Vilken version av Aspose.PSD krävs?** Vilken som helst av de senaste 24.x‑utgåvorna; koden fungerar med det senaste biblioteket.  
- **Kan jag överlagra flera bilder?** Ja – upprepa `drawImage`‑anropet med olika källor.  
- **Behöver jag en licens?** En provversion fungerar för utveckling; en kommersiell licens krävs för produktion.

## Vad är “draw image on canvas”?
I Aspose.PSD‑terminologi betyder att rita en bild på en canvas att måla ett `Image`‑objekt på ett annat med hjälp av ett `Graphics`‑sammanhang. Denna operation är ryggraden i **overlay images java**‑tekniker såsom att lägga till vattenstämplar, logotyper eller signaturer.

## Varför använda Aspose.PSD för att överlagra en signatur?
- **Full PSD‑stöd** – fungerar med lager, masker och transparens.  
- **Inga inhemska OS‑beroenden** – ren Java, perfekt för server‑sidig bearbetning.  
- **Högpresterande rendering** – optimerad för stora filer och komplexa sammansättningar.  

## Förutsättningar
- Java Development Kit (JDK) 8 eller högre.  
- Aspose.PSD for Java JAR tillagd i ditt projekts classpath.  
- Två bildfiler: en basbild (t.ex. `layers.psd`) och en signaturgrafik (`sample.psd`).  

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

> **Proffstips:** Håll båda bilderna i samma färgläge (RGB) för att undvika oväntade färgskiftningar vid ritning.

## Steg 2: Initiera grafik (initialize graphics java)

```java
//ExStart:InitializeGraphics
Graphics graphics = new Graphics(canvas);
//ExEnd:InitializeGraphics
```

`Graphics`‑objektet fungerar som en pensel som låter dig **draw image on canvas**. Genom att initiera det med den primära `Image` knyts alla efterföljande ritkommandon till den canvasen.

## Steg 3: Lägg till signatur på bild (how to add signature)

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

I detta kodexempel **overlay images java** vi genom att placera signaturen i nedre högra hörnet. Justera `Point`‑värdena om du behöver en annan placering.

## Vanliga problem & lösningar

| Symptom | Orsak | Lösning |
|---------|-------|-----|
| Signaturen visas förvrängd | Olika DPI mellan canvas och signatur | Använd `signature.resize` före ritning eller säkerställ att båda filerna har samma DPI. |
| Utdatafilen är enorm | Sparar utan kompression | Skicka med en konfigurerad `PngOptions` med `CompressionLevel` satt till ett högre värde. |
| Inget ritas | Graphics inte avyttrat | Anropa `graphics.dispose()` efter ritning (valfritt, men god praxis). |

## Slutsats

Genom att följa dessa steg har du lärt dig **how to draw image on canvas** och sömlöst **add a signature** med Aspose.PSD för Java. Denna teknik kan utökas till vattenstämplar, logotyper eller andra överlagrade grafik, vilket ger dina Java‑applikationer kraftfulla **java image processing**‑möjligheter.

## Vanliga frågor

### Q1: Kan jag lägga till flera signaturer på en bild?

A1: Ja, du kan lägga till flera signaturer genom att upprepa stegen med olika signaturbilder.

### Q2: Stöder Aspose.PSD andra bildformat?

A2: Ja, Aspose.PSD stöder ett brett spektrum av bildformat, vilket säkerställer flexibilitet i bildbehandling.

### Q3: Krävs en licens för att använda Aspose.PSD för Java?

A3: Ja, du behöver en giltig licens för att använda Aspose.PSD. Besök [Purchase Aspose.PSD](https://purchase.aspose.com/buy) för licensinformation.

### Q4: Hur kan jag få support för Aspose.PSD?

A4: Besök [Aspose.PSD Forum](https://forum.aspose.com/c/psd/34) för gemenskapsstöd och diskussioner.

### Q5: Kan jag prova Aspose.PSD för Java innan jag köper?

A5: Ja, du kan få en [free trial](https://releases.aspose.com/) för att utforska funktionerna innan du köper.

## Ytterligare vanliga frågor

**Q: Hur ändrar jag opaciteten på signaturen?**  
A: Använd `graphics.setOpacity(float opacity)` innan du anropar `drawImage`. Värdena sträcker sig från 0.0 (genomskinlig) till 1.0 (opak).

**Q: Är det möjligt att rotera signaturen?**  
A: Ja – tillämpa en transformationsmatris via `graphics.rotateTransform(angle)` innan ritning.

**Q: Kan jag rita signaturen på en JPEG istället för PNG?**  
A: Absolut. Byt ut `PngOptions` mot `JpegOptions` och ange önskad kvalitetsnivå.

---

**Senast uppdaterad:** 2025-12-02  
**Testat med:** Aspose.PSD for Java 24.11  
**Författare:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}