---
date: 2026-09-13
description: Lär dig hur du ritar en ellips och andra former i Java med Aspose.PSD.
  Denna steg‑för‑steg Java‑grafikhandledning visar gradientfyllningar, polygonfyllningar
  och bildexport.
keywords:
- how to draw ellipse
- draw shapes java
- how to create gradient
- java graphics tutorial
- fill polygon java
lastmod: 2026-09-13
linktitle: Rita med grafik i Java
og_description: Lär dig hur du ritar en ellips i Java med Aspose.PSD. Denna Java‑grafikhandledning
  täcker formritning, gradientfyllningar, polygonfyllning och export av bilder.
og_image_alt: Screenshot of Java code drawing an ellipse with Aspose.PSD
og_title: Hur man ritar en ellips med grafik i Java med Aspose.PSD
schemas:
- author: Aspose
  dateModified: '2026-09-13'
  description: Learn how to draw an ellipse and other shapes in Java with Aspose.PSD.
    This step‑by‑step Java graphics tutorial shows gradient fills, polygon fills,
    and image export.
  headline: How to draw ellipse using graphics in Java with Aspose.PSD
  type: TechArticle
- questions:
  - answer: Yes, it supports layer merging, channel adjustments, text rendering, and
      advanced masking in addition to shape drawing.
    question: Can Aspose.PSD handle complex image manipulations?
  - answer: Absolutely; the library is optimized for speed and can process a 10 MP
      image in under 2 seconds on a typical server.
    question: Is Aspose.PSD suitable for high‑performance applications?
  - answer: Visit the [Aspose.PSD Java documentation](https://reference.aspose.com/psd/java/)
      for comprehensive guides and API references.
    question: Where can I find more examples and documentation?
  - answer: Yes, you can export to BMP, PNG, JPEG, TIFF, GIF, and PSD among others.
    question: Does Aspose.PSD support multiple image formats for export?
  - answer: Reach out to the Aspose.PSD community on the [support forum](https://forum.aspose.com/c/psd/34)
      or consider a [temporary license](https://purchase.aspose.com/temporary-license/)
      for priority assistance.
    question: How can I get support or assistance if I encounter issues?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- java graphics
- Aspose.PSD
- drawing shapes java
- gradient fill java
- initialize graphics java
title: Hur man ritar en ellips med grafik i Java med Aspose.PSD
url: /sv/java/java-graphics-drawing/drawing-using-graphics/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Hur man ritar ellips med grafik i Java med Aspose.PSD

## Introduktion
I den här Java‑grafikhandledningen kommer du att upptäcka **hur man ritar ellips** objekt och andra former programatiskt med Aspose.PSD för Java. Oavsett om du behöver generera dynamiska miniatyrbilder, skapa anpassade UI‑element eller automatisera designarbetsflöden, ger behärskning av ellipsteckning och gradientfyllningar dig exakt visuell kontroll. Stegen nedan guidar dig genom att initiera grafik, konfigurera pennor och borstar samt exportera resultatet i vanliga bildformat.

## Snabba svar
- **Vilket bibliotek krävs?** Aspose.PSD för Java (ladda ner från den officiella webbplatsen).  
- **Vilken form fokuserar handledningen på?** Att rita en ellips och fylla en polygon.  
- **Kan jag exportera till andra format än BMP?** Ja – PNG, JPEG, TIFF och fler stöds.  
- **Behöver jag en licens för utveckling?** En gratis tillfällig licens fungerar för testning; en full licens krävs för produktion.  
- **Är API:et lämpligt för stora bilder?** Aspose.PSD bearbetar filer upp till 500 MB utan att ladda hela bitmapen i minnet.

## Hur ritar man ellips i Java?
Läs in en `PsdImage` med önskad bredd och höjd, skapa ett `Graphics`‑objekt, sätt en `Pen` och anropa `drawEllipse` med en omslutande rektangel. Hela operationen kräver bara några metodanrop och körs på under en sekund för typiska 800×600‑bilder på modern hårdvara.

## Vad är Aspose.PSD för Java?
Aspose.PSD för Java är ett **pure‑Java‑bibliotek som erbjuder 50+ bildformatkonverteringar och fullständiga PSD‑redigeringsfunktioner** utan att behöva Adobe Photoshop. Det kan rendera, modifiera och exportera flerskiktsfiler samtidigt som minnesanvändningen hålls låg, vilket gör det idealiskt för server‑sidig grafikgenerering.

## Varför använda Aspose.PSD för att rita former?
Aspose.PSD erbjuder hög prestanda, omfattande formatstöd och exakt rendering, vilket gör det idealiskt för server‑sidig grafikgenerering och komplex formritning.

- **Prestanda:** Hanterar bilder upp till 500 MB med mindre än 150 MB heap‑användning (≈30 % lägre än konkurrerande bibliotek).  
- **Formatstöd:** 50+ in‑ och utdataformat, inklusive BMP, PNG, JPEG, TIFF och PSD.  
- **Precision:** Sub‑pixelrendering säkerställer skarpa ellipser och mjuka gradienter på hög‑DPI‑skärmar.

## Förutsättningar
- Grundläggande kunskap i Java‑programmering.  
- Java Development Kit (JDK) installerat.  
- En IDE som IntelliJ IDEA eller Eclipse.  
- Aspose.PSD för Java‑biblioteket. Du kan ladda ner det från [Aspose.PSD Java nedladdning](https://releases.aspose.com/psd/java/).

## Importera paket
För att börja, importera de nödvändiga Aspose.PSD‑klasserna och standard‑Java‑verktygen. Följande klasser tillhandahåller ritningsprimitiver och färghantering:
```java
import com.aspose.psd.Color;
import com.aspose.psd.Graphics;
import com.aspose.psd.Pen;
import com.aspose.psd.Point;
import com.aspose.psd.Rectangle;
import com.aspose.psd.brushes.LinearGradientBrush;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.BmpOptions;
```

## Steg 1: skapa ett bildobjekt
`PsdImage` representerar en raster‑canvas i minnet som kan ritas på och sparas i olika format.
```java
String dataDir = "Your Document Directory";
PsdImage image = new PsdImage(500, 500);
```

## Steg 2: initiera grafikobjekt
`Graphics` är ritningsytan som är kopplad till en `PsdImage`, vilket möjliggör vektoroperationer såsom att rita former.
```java
Graphics graphics = new Graphics(image);
```

## Steg 3: rensa bildytan
`clear` fyller hela canvasen med en enda bakgrundsfärg.
```java
graphics.clear(Color.getWhite());
```

## Steg 4: skapa och konfigurera pen‑objekt
`Pen` definierar linjefärgen, bredden och stilen som används när konturer ritas.
```java
Pen pen = new Pen(Color.getBlue());
```

## Steg 5: rita former
`drawEllipse` renderar en ellips som passar inom den angivna rektangeln med den aktuella pennan.
```java
graphics.drawEllipse(pen, new Rectangle(10, 10, 150, 100));
```

## Steg 6: använd borstar för fyllning
`LinearGradientBrush` skapar en gradientfyllning som övergår mellan två färger över ett definierat område.
```java
LinearGradientBrush linearGradientBrush = new LinearGradientBrush(image.getBounds(), Color.getRed(), Color.getWhite(), 45f);
Point[] points = { new Point(200, 200), new Point(400, 200), new Point(250, 350) };
graphics.fillPolygon(linearGradientBrush, points);
```

## Steg 7: spara den modifierade bilden
`save` skriver `PsdImage` till disk i det valda formatet, såsom BMP eller PNG.
```java
image.save(dataDir + "DrawingUsingGraphics_output.bmp", new BmpOptions());
```

## Vanliga fallgropar och felsökning
- **NullPointerException på grafik:** Se till att `PsdImage` är helt instansierad innan du skapar `Graphics`‑objektet.  
- **Felaktiga färger:** Använd `Color.fromArgb` för att ange exakta ARGB‑värden när standardpaletten inte matchar förväntningarna.  
- **Prestandafördröjning på stora bilder:** Aktivera `PsdImageOptions` med `compression = CompressionType.Rle` för att minska minnesbelastningen.

## Vanliga frågor

**Q: Kan Aspose.PSD hantera komplexa bildmanipulationer?**  
A: Ja, det stöder lager‑sammanfogning, kanaljusteringar, textrendering och avancerad maskning utöver formritning.

**Q: Är Aspose.PSD lämpligt för högpresterande applikationer?**  
A: Absolut; biblioteket är optimerat för hastighet och kan bearbeta en 10 MP‑bild på under 2 sekunder på en vanlig server.

**Q: Var kan jag hitta fler exempel och dokumentation?**  
A: Besök [Aspose.PSD Java-dokumentation](https://reference.aspose.com/psd/java/) för omfattande guider och API‑referenser.

**Q: Stöder Aspose.PSD flera bildformat för export?**  
A: Ja, du kan exportera till BMP, PNG, JPEG, TIFF, GIF och PSD bland annat.

**Q: Hur kan jag få support eller hjälp om jag stöter på problem?**  
A: Kontakta Aspose.PSD‑gemenskapen på [supportforum](https://forum.aspose.com/c/psd/34) eller överväg en [tillfällig licens](https://purchase.aspose.com/temporary-license/) för prioriterad assistans.

---

**Last updated:** 2026-09-13  
**Tested with:** Aspose.PSD for Java 24.10  
**Author:** Aspose

## Relaterade handledningar

- [Ändra storlek på bild med Aspose.PSD för Java – Rita former & grundläggande bildoperationer](/psd/java/basic-image-operations/)
- [Rita och spara en rektangel i en PSD med Aspose.PSD för Java](/psd/java/basic-image-operations/simple-drawing/)
- [Lägg till signatur till bild – Rita bild på canvas med Aspose.PSD för Java](/psd/java/advanced-image-effects/add-signature-to-image/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}