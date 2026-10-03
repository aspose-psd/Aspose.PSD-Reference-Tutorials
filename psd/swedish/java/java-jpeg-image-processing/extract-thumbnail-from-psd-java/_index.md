---
date: 2026-10-03
description: Lär dig hur du extraherar thumbnail från PSD i Java med Aspose.PSD. Denna
  steg‑för‑steg‑guide täcker installation, kodexempel och hur du sparar thumbnail
  som en JPEG‑bild.
keywords:
- extract thumbnail from psd
- java aspose psd
- psd thumbnail extraction
lastmod: 2026-10-03
linktitle: Extrahera thumbnail från PSD i Java
og_description: Lär dig hur du extraherar thumbnail från PSD i Java med Aspose.PSD.
  Denna guide visar dig hur du ställer in, laddar filen, extraherar thumbnail och
  sparar den som en JPEG‑bild.
og_image_alt: Screenshot showing Java code extracting a thumbnail from a PSD file
  using Aspose.PSD
og_title: Extrahera thumbnail från PSD i Java med Aspose.PSD
schemas:
- author: Aspose
  dateModified: '2026-10-03'
  description: Learn how to extract thumbnail from PSD in Java using Aspose.PSD. This
    step‑by‑step guide covers setup, code snippets, and saving the thumbnail as a
    JPEG image.
  headline: Extract thumbnail from PSD in Java
  type: TechArticle
- questions:
  - answer: Aspose.PSD is a Java library that enables programmatic creation, manipulation,
      and conversion of PSD and other raster image formats without requiring Adobe
      Photoshop.
    question: What is Aspose.PSD?
  - answer: You can refer to the [documentation](https://reference.aspose.com/psd/java/)
      for detailed API references and examples.
    question: Where can I find more documentation on Aspose.PSD for Java?
  - answer: Yes, you can download a [free trial](https://releases.aspose.com/) to
      evaluate the library’s capabilities.
    question: Can I try Aspose.PSD for free before purchasing?
  - answer: Temporary licenses are available from the [temporary license](https://purchase.aspose.com/temporary-license/)
      page.
    question: How can I obtain a temporary license for Aspose.PSD?
  - answer: Yes, Aspose.PSD can be used in both personal and commercial projects under
      its licensing terms.
    question: Is Aspose.PSD suitable for commercial use?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- java image processing
- aspose.psd
- thumbnail extraction
title: Extrahera thumbnail från PSD i Java
url: /sv/java/java-jpeg-image-processing/extract-thumbnail-from-psd-java/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Extrahera miniatyrbild från PSD i Java

## Introduktion
Att extrahera en miniatyrbild från en PSD‑fil låter dig skapa snabba förhandsvisningar utan att ladda hela högupplösta bilden. I Java gör Aspose.PSD denna process enkel och presterande. I den här handledningen kommer du att lära dig hur du installerar biblioteket, hittar miniatyrresursen och sparar den som en JPEG‑fil – allt med bara några rader kod.

## Snabba svar
- **Vilket bibliotek hanterar PSD‑miniatyrbilder?** Aspose.PSD for Java.
- **Hur många kodrader krävs?** Ungefär fem rader för att ladda, extrahera och spara.
- **Kan jag extrahera miniatyrbilder från stora PSD‑filer?** Ja, Aspose.PSD bearbetar filer upp till 500 MB utan att ladda hela minnet.
- **Behöver jag en licens för utveckling?** En gratis provversion fungerar för utvärdering; en licens krävs för produktion.
- **Vilka utdataformat stöds?** Den extraherade miniatyrbilden kan sparas som JPEG, PNG eller BMP.

## Vad är att extrahera en miniatyrbild från PSD?
Att extrahera en miniatyrbild från PSD är processen att läsa den lilla förhandsgranskningsbilden som är inbäddad i ett Photoshop‑dokument (PSD). Denna förhandsgranskning lagras som en resurs och kan sparas separat för katalogisering eller visningsändamål. Miniatyrbilden är vanligtvis en lågupplöst representation som används av applikationer för att visa en snabb visuell sammanfattning utan att ladda hela bilden.

## Varför använda Aspose.PSD för denna uppgift?
Aspose.PSD stöder **30+ bildformat** och kan hantera PSD‑filer upp till **500 MB** samtidigt som minnesanvändningen hålls låg eftersom det läser resurser på begäran. API‑et erbjuder också robust felhantering, så du kan på ett pålitligt sätt extrahera miniatyrbilder även från korrupta filer.

## Förutsättningar
- Java Development Kit (JDK) installerat.
- Aspose.PSD för Java‑nedladdning från [Aspose.PSD för Java‑nedladdning](https://releases.aspose.com/psd/java/).
- Grundläggande kunskap om Java‑syntax och projektuppsättning.

## Hur extraherar du en miniatyrbild från en PSD‑fil i Java?
Läs in PSD‑filen med `PsdImage`, lokalisera `ThumbnailResource` och spara dess bilddata som en JPEG. Aspose.PSD abstraherar den lågnivå‑parsing, så du behöver bara anropa `getResources()` och sedan `save()` på den extraherade bilden. Detta tillvägagångssätt fungerar för alla PSD‑filer som innehåller en miniatyrbild, oavsett filstorlek.

## Importera paket
`Image` är basklassen för att ladda bilder. `PsdImage` representerar ett PSD‑dokument. `ThumbnailResource` och `Thumbnail4Resource` representerar miniatyrresurser. `JpegOptions` specificerar JPEG‑sparalternativ.

```text
```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.resources.Thumbnail4Resource;
import com.aspose.psd.fileformats.psd.resources.ThumbnailResource;
import com.aspose.psd.imageoptions.JpegOptions;
```
```

## Steg 1: läs in PSD‑filen
Först, skapa en `PsdImage`‑instans som pekar på din PSD‑fil. Konstruktorn läser endast rubriken och nödvändiga resurser, vilket håller minnesanvändningen minimal.

```text
```java
String dataDir = "Your_Document_Directory/";
PsdImage image = (PsdImage)Image.load(dataDir + "your_file.psd");
```
```

Byt ut `"Your_Document_Directory/"` mot sökvägen till den katalog där din PSD‑fil ligger, och `"your_file.psd"` mot namnet på din PSD‑fil.

## Steg 2: iterera över bildresurser
Aspose.PSD lagrar miniatyrbilder som `ThumbnailResource`‑objekt i bildens resurskollektion. Loopa igenom kollektionen, kontrollera resurstypen och fånga den första miniatyrbild du stöter på.

```text
```java
for (int i = 0; i < image.getImageResources().length; i++) {
    if (image.getImageResources()[i] instanceof ThumbnailResource) {
        ThumbnailResource thumbnail = (ThumbnailResource) image.getImageResources()[i];
        
        // Extract thumbnail data
        int[] data = thumbnail.getThumbnailArgb32Data();
        
        // Create a new image with the extracted thumbnail data
        PsdImage extractedThumbnailImage = new PsdImage(thumbnail.getWidth(), thumbnail.getHeight());
        extractedThumbnailImage.saveArgb32Pixels(extractedThumbnailImage.getBounds(), data);
        
        // Save the extracted thumbnail as a separate JPEG file
        extractedThumbnailImage.save(dataDir + "extracted_thumbnail.jpg", new JpegOptions());
        
        // Output success message
        System.out.println("Thumbnail extracted and saved successfully.");
        
        break; // Exit the loop once thumbnail is found and processed
    }
}
```
```

## Steg 3: spara den extraherade miniatyrbilden
När du har miniatyrbilden, anropa dess `save`‑metod för att skriva den till disk. Du kan välja JPEG, PNG eller BMP; JPEG är vanligast för webbförhandsvisningar.

## Steg 4: hantera olika miniatyrtyper
Om en PSD innehåller flera miniatyrvarianter, såsom `Thumbnail4Resource`, utöka itereringslogiken för att kontrollera varje typ. API‑et tillhandahåller separata klasser för varje resurs, så att du kan välja den upplösning du behöver.

## Vanliga problem och lösningar
- **Ingen miniatyrbild hittades:** Alla PSD‑filer innehåller inte en förhandsgranskning. Verifiera källfilen i Photoshop‑panelens “File → File Info”.
- **Fel: ej stödd format:** Säkerställ att du använder den senaste versionen av Aspose.PSD; äldre versioner kan sakna nya miniatyrresurstyper.
- **Out‑of‑memory på stora filer:** Använd `PsdImage.load(..., LoadOptions)` med `LoadOptions.setLoadResourcesOnly(true)` för att undvika att ladda hela bilddata när du bara behöver miniatyrbilden.

## Vanliga frågor

**Q: Vad är Aspose.PSD?**  
A: Aspose.PSD är ett Java‑bibliotek som möjliggör programmatisk skapande, manipulering och konvertering av PSD‑ och andra rasterbildformat utan att kräva Adobe Photoshop.

**Q: Var kan jag hitta mer dokumentation om Aspose.PSD för Java?**  
A: Du kan hänvisa till [dokumentationen](https://reference.aspose.com/psd/java/) för detaljerade API‑referenser och exempel.

**Q: Kan jag prova Aspose.PSD gratis innan jag köper?**  
A: Ja, du kan ladda ner en [gratis provversion](https://releases.aspose.com/) för att utvärdera bibliotekets funktioner.

**Q: Hur kan jag få en tillfällig licens för Aspose.PSD?**  
A: Tillfälliga licenser finns tillgängliga på sidan för [tillfällig licens](https://purchase.aspose.com/temporary-license/).

**Q: Är Aspose.PSD lämplig för kommersiell användning?**  
A: Ja, Aspose.PSD kan användas i både personliga och kommersiella projekt enligt dess licensvillkor.

---

**Senast uppdaterad:** 2026-10-03  
**Testad med:** Aspose.PSD for Java 24.12  
**Författare:** Aspose

## Relaterade handledningar

- [Hur man konverterar PSD till rasterbildformat med Aspose.PSD för Java](/psd/java/advanced-techniques/convert-psd-to-raster-formats/)
- [Spara PSD som JPEG och stöd RGB‑färg med Aspose.PSD Java](/psd/java/advanced-psd-layer-features-effects/support-rgb-color-psd-files/)
- [Ändra bildstorlek med Aspose.PSD för Java – Rita former & grundläggande bildoperationer](/psd/java/basic-image-operations/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}