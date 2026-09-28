---
date: 2026-09-28
description: Lär dig hur du ritar ellipse i Java med Aspose.PSD, den ledande Java
  image processing-handledningen för att skapa ellipse och andra former.
keywords:
- how to draw ellipse
- draw shapes java
- java image processing tutorial
- create ellipse image
- draw ellipses java
lastmod: 2026-09-28
linktitle: Rita ellipse i Java
og_description: Lär dig hur du ritar ellipse i Java med Aspose.PSD, den bästa Java
  image processing-handledningen som låter dig skapa ellipse, rita former och generera
  bitmap images effektivt.
og_image_alt: Guide showing how to draw an ellipse in Java with Aspose.PSD
og_title: Hur man ritar ellipse i Java med Aspose.PSD-biblioteket
schemas:
- author: Aspose
  dateModified: '2026-09-28'
  description: Learn how to draw ellipse in Java using Aspose.PSD, the leading Java
    image processing tutorial for creating ellipses and other shapes.
  headline: How to draw ellipse in Java using Aspose.PSD library
  type: TechArticle
- questions:
  - answer: Aspose.PSD offers a fully functional trial that lets you evaluate all
      features before purchasing a license.
    question: Can I use Aspose.PSD for free?
  - answer: Visit [Aspose.PSD Documentation](https://reference.aspose.com/psd/java/)
      for comprehensive guides, API references, and sample projects.
    question: Where can I find more examples and documentation?
  - answer: Temporary licenses are available through the Aspose portal at [Aspose.PSD
      Temporary License](https://purchase.aspose.com/temporary-license/).
    question: How do I obtain a temporary license for testing?
  - answer: It supports BMP, PNG, JPEG, TIFF, GIF, and native PSD among others.
    question: What image formats can Aspose.PSD export to?
  - answer: Yes, the library is designed for high‑throughput server environments and
      includes features such as multi‑threaded processing and memory‑efficient streaming.
    question: Is Aspose.PSD suitable for enterprise‑level workloads?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- draw ellipse
- Aspose.PSD
- Java graphics
- image processing
title: Hur man ritar ellipse i Java med Aspose.PSD-biblioteket
url: /sv/java/java-graphics-drawing/drawing-ellipses/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Hur man ritar en ellips i Java med Aspose.PSD-biblioteket

## Introduktion
I den här handledningen kommer du att lära dig **hur man ritar en ellips** i Java med Aspose.PSD-biblioteket. Aspose.PSD för Java är ett robust API som låter dig skapa, redigera och exportera PSD‑filer utan att behöva Adobe Photoshop. Att rita former som ellipser är en grundläggande färdighet för alla Java‑bildbehandlingsprojekt, och den här guiden leder dig genom varje steg — från projektuppsättning till att spara den slutliga bitmapen.

## Snabba svar
- **Vilket bibliotek är bäst för att rita ellipser i Java?** Aspose.PSD för Java.
- **Hur många kodrader behövs?** Ungefär tio rader plus några konfigurationssatser.
- **Behöver jag en licens för utveckling?** En gratis provversion fungerar för testning; en kommersiell licens krävs för produktion.
- **Kan jag exportera till BMP, PNG eller JPEG?** Ja, Aspose.PSD stödjer BMP, PNG, JPEG och PSD.
- **Är API:et kompatibelt med Java 8 och nyare?** Fullt stöd på Java 8‑21.

## Vad är Aspose.PSD för Java?
Aspose.PSD för Java är ett rent Java‑bibliotek som möjliggör programmatisk skapande, manipulering och konvertering av Photoshop PSD‑filer. Det stödjer över 100 bildformat och kan hantera filer upp till 2 GB utan att ladda hela dokumentet i minnet.

## Varför använda Aspose.PSD för ellipsteckning?
Aspose.PSD levererar hög prestanda, bearbetar flersidiga dokument på sekunder, samtidigt som det stödjer över 100 in‑ och utdataformat som BMP, PNG, JPEG och PSD. Det körs helt i Java, vilket eliminerar behovet av inbyggd Photoshop och gör det idealiskt för CI/CD‑pipelines och molnbaserade tjänster.

## Förutsättningar
Innan du börjar, se till att du har:
- Grundläggande kunskaper i Java‑programmering.
- JDK 8 eller nyare installerat.
- En IDE som IntelliJ IDEA eller Eclipse.
- Aspose.PSD för Java‑biblioteket. Du kan ladda ner det från [Aspose.PSD for Java download page](https://releases.aspose.com/psd/java/).

## Importera paket
Först, importera de klasser du behöver från Aspose.PSD‑namnutrymmet.

## Hur ritar man en ellips i Java?
Läs in Aspose.PSD‑biblioteket, skapa en tom PsdImage‑canvas, hämta ett Graphics‑objekt, rensa eventuellt bakgrunden, och använd sedan Pen‑objekt med önskade färger och stilar för att rita ellipser inom Rectangle‑gränserna. Slutligen, spara bilden i BMP, PNG eller JPEG‑format. Denna process kräver vanligtvis färre än 15 kodrader.

## Steg 1: konfigurera ditt Java‑projekt
Innan du börjar koda, se till att ditt projekt inkluderar Aspose.PSD‑JAR‑filen som en Maven/Gradle‑beroende eller lägger till JAR‑filen i classpath.

## Steg 2: skapa en instans av PsdImage
PsdImage representerar ett Photoshop‑dokument i minnet och tillhandahåller en canvas för ritning.

```java
import com.aspose.psd.Color;
import com.aspose.psd.Graphics;
import com.aspose.psd.Image;
import com.aspose.psd.Pen;
import com.aspose.psd.Rectangle;
import com.aspose.psd.brushes.SolidBrush;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.BmpOptions;
```

## Steg 3: initiera graphics‑objektet
Graphics tillhandahåller ritmetoder för att rendera former på en bildyta.

```java
Image image = new PsdImage(100, 100);
```

## Steg 4: rensa graphics‑ytan
Rensa eventuellt canvasen med en bakgrundsfärg för att säkerställa ett rent ritområde.

```java
Graphics graphics = new Graphics(image);
```

## Steg 5: rita en prickad ellips
Pen definierar färgen och stilen på konturen som används när man ritar former.

```java
graphics.clear(Color.getYellow());
```

## Steg 6: rita en kontinuerlig ellips
Pen med en solid‑blue brush skapar en kontinuerlig kontur för den andra ellipsen.

```java
graphics.drawEllipse(new Pen(Color.getRed()), new Rectangle(30, 10, 40, 80));
```

## Steg 7: spara bilden
BmpOptions specificerar BMP‑formatinställningar för att spara bilden.

```java
graphics.drawEllipse(new Pen(new SolidBrush(Color.getBlue())), new Rectangle(10, 30, 80, 40));
```

```java
String outputPath = "Your Document Directory/Ellipse.bmp";
BmpOptions saveOptions = new BmpOptions();
saveOptions.setBitsPerPixel(32);
image.save(outputPath, saveOptions);
```



## Vanliga problem och lösningar
- **Bilden visas tom:** Se till att du anropade `graphics.clear()` med en synlig färg innan du ritar.
- **Ellipsen ser förvrängd ut:** Verifiera att `Rectangle`‑dimensionerna matchar bildens bildförhållande.
- **Minnesbristfel på stora filer:** Använd `PsdImage`‑s streaming‑API för att bearbeta sektioner av filen istället för att ladda hela dokumentet.

## Vanliga frågor

**Q: Kan jag använda Aspose.PSD gratis?**  
A: Aspose.PSD erbjuder en fullt fungerande provversion som låter dig utvärdera alla funktioner innan du köper en licens.

**Q: Var kan jag hitta fler exempel och dokumentation?**  
A: Besök [Aspose.PSD Documentation](https://reference.aspose.com/psd/java/) för omfattande guider, API‑referenser och exempelprojekt.

**Q: Hur får jag en tillfällig licens för testning?**  
A: Tillfälliga licenser finns tillgängliga via Aspose‑portalen på [Aspose.PSD Temporary License](https://purchase.aspose.com/temporary-license/).

**Q: Vilka bildformat kan Aspose.PSD exportera till?**  
A: Det stödjer BMP, PNG, JPEG, TIFF, GIF och inbyggt PSD bland annat.

**Q: Är Aspose.PSD lämpligt för företagsnivå‑arbetsbelastningar?**  
A: Ja, biblioteket är designat för högkapacitets servermiljöer och inkluderar funktioner som flertrådad bearbetning och minnes‑effektiv streaming.

## Slutsats
Du har nu ett komplett, end‑to‑end‑exempel på **hur man ritar en ellips** i Java med Aspose.PSD. Genom att konfigurera en `PsdImage`, använda `Graphics`‑API:et och konfigurera `Pen`‑objekt kan du rendera både prickade och solida ellipser och spara resultatet i något av de stödjade bitmapformaten. Integrera dessa steg i dina egna applikationer för att generera dynamisk grafik, miniatyrbilder eller anpassade UI‑element utan att förlita dig på externa grafikredigerare.

---

**Last Updated:** 2026-09-28  
**Tested With:** Aspose.PSD for Java 24.12  
**Author:** Aspose

## Relaterade handledningar

- [Rita och spara en rektangel i en PSD med Aspose.PSD för Java](/psd/java/basic-image-operations/simple-drawing/)
- [Ändra storlek på bild med Aspose.PSD för Java – Rita former och grundläggande bildoperationer](/psd/java/basic-image-operations/)
- [Lägg till signatur till bild – Rita bild på canvas med Aspose.PSD för Java](/psd/java/advanced-image-effects/add-signature-to-image/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}