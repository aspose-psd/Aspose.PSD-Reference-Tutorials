---
date: 2026-01-25
description: Lär dig hur du extraherar miniatyrbilder från PSD‑filer med Aspose.PSD
  för Java. Följ den här steg‑för‑steg‑guiden för att snabbt ladda, extrahera och
  spara miniatyrbilder.
linktitle: Extract Thumbnail from PSD in Java
second_title: Aspose.PSD Java API
title: Extrahera miniatyrbild från PSD i Java
url: /sv/java/java-jpeg-image-processing/extract-thumbnail-from-psd-java/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Extrahera miniatyrbild från PSD i Java

## Introduktion
I den här handledningen kommer du att lära dig **hur man extraherar miniatyrbild från PSD**‑filer med hjälp av Aspose.PSD‑biblioteket för Java. Miniatyrbilder är små förhandsgranskningsbilder som är inbäddade i PSD‑dokument, och att extrahera dem kan hjälpa dig att snabbt skapa förhandsvisningar, bygga bildgallerier eller minska lagringsutrymme när du bara behöver en liten representation av originalkonstverket. Vi går igenom allt från projektuppsättning till att spara den extraherade miniatyrbilden som en vanlig bildfil.

## Snabba svar
- **Vad täcker den här handledningen?** Extrahera och spara en miniatyrbild från en PSD‑fil med Aspose.PSD för Java.  
- **Vilket bibliotek krävs?** Aspose.PSD för Java (nedladdningsbar från den officiella Aspose‑webbplatsen).  
- **Behöver jag en licens?** En till krävs för produktionsanvändning; en gratis provperiod finns tillgänglig.  
- **Vilket utdataformat används?** Exemplet sparar miniatyrbilden som en JPEG‑fil, men vilket som helst av de stödjade formaten kan väljas.  
- **Hur lång tid tar implementeringen?** Omkring ahera miniatyrbild från PSD”?
Att extrahera en miniatyrbild från en PSD innebär att läsa den lilla förhandsgranskningsbild som Photoshop lagrar i filens resurser‑sektion. Denna förhandsvisning är vanligtvis en lågupplöst version av hela arbetsytan, vilket gör den idealisk för snabb laddning i filbläddrare eller webb‑gallerier.

## Varför extrahera miniatyrbilder med Aspose.PSD?
- **Hastighet:** Ingen behov av att öppna hela PSD‑filen i en grafikredigerare; miniatyrbilden är redan inbäddad.  
- **Automation:** Perfekt för batch‑behandling av stora bildbibliotek.  
- **Plattformsoberoende:** Fungerar på alla OS som stödjer Java, utan att kräva Photoshop.  
- **Formatflexibilitet:** Konvertera miniatyrbilden till JPEG, PNG eller något annat format som stöds av Aspose.PSD.

## Förutsättningar
Innan vi börjar, se till att du har följande på plats:
- Java Development Kit (JDK) installerat på ditt system.  
- Aspose.PSD för Java‑biblioteket. Du kan ladda ner det [här](https://releases.aspose.com/psd/java/).  
- Grundläggande kunskaper i Java‑programmering.

## Importera paket
För att komma igång, inkludera det nödvändiga Aspose.PSD‑paketet i din Java‑klass:
```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.resources.Thumbnail4Resource;
import com.aspose.psd.fileformats.psd.resources.ThumbnailResource;
import com.aspose.psd.imageoptions.JpegOptions;
```

## Hur man extraherar miniatyrbild från PSD med Aspose.PSD för Java
Nedan följer en steg‑för‑steg‑guide. Varje steg innehåller en kort förklaring följt av exakt kod som du kan kopiera.

### Steg 1: Läs in PSD‑filen
Först läser du in PSD‑filen som innehåller den miniatyrbild du vill extrahera.
```java
String dataDir = "Your_Document_Directory/";
PsdImage image = (PsdImage)Image.load(dataDir + "your_file.psd");
```
Byt ut `"Your_Document_Directory/"` mot sökvägen till den katalog där din PSD‑fil ligger, och `"your_file.psd"` mot namnet på din PSD‑fil.

### Steg 2: Iterera över bildresurser
Iterera genom bildresurserna för att hitta miniatyr‑resursen.
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

### Steg 3: Spara den extraherade miniatyrbilden
Koden i föregående steg sparar redan miniatyrbilden som en JPEG‑fil med namnet `extracted_thumbnail.jpg` i samma katalog. Du kan ändra filnamnet eller formatet genom att justera parametrarna i `save`‑metoden.

### Steg 4: Hantera olika miniatyrtyper
Om din PSD‑fil kan innehålla flera typer av miniatyrer, såsom `Thumbnail4Resource`, kan du utöka logiken för att hantera dessa fall på liknande sätt. Lägg bara till en `instanceof Thumbnail4Resource`‑kontroll i loopen och behandla den med samma mönster.

## Vanliga problem och lösningar
- **Ingen miniatyr hittades:** Alla PSD‑filer innehåller inte en miniatyrresurs. Verifiera källfilen i Photoshop (File → Export → Thumbnail) eller använd en annan PSD som inkluderar en förhandsvisning.  
- **Fel: ej stödd bildformat:** Säkerställ att du använder en aktuell version av Aspose.PSD som stödjer det önskade formatet.  
- **Behörighetsfel vid sparning:** Kontrollera att applikationen har skrivbehörighet till mål‑katalogen.

## Vanliga frågor

**Q: Vad är Aspose.PSD?**  
A: Aspose.PSD är ett Java‑bibliotek som låter utvecklare arbeta med PSD‑ och andra bildfilformat programatiskt.

**Q: Var kan jag hitta mer dokumentation om Aspose.PSD för Java?**  
A: Du kan hänvisa till [dokumentationen](https://reference.aspose.com/psd/java/) för detaljerade API‑referenser och exempel.

**Q: Kan jag prova Aspose.PSD gratis innan jag köper?**  
A: Ja, du kan ladda ner en [gratis provperiod](https://releases.aspose.com/) för att utvärdera bibliotekets funktioner.

**Q: Hur får jag tillfälliga licenser för Aspose.PSD?**  
A: Tillfälliga licenser kan erhållas [här](https://purchase.aspose.com/temporary-license/).

**Q: Är Aspose.PSD lämpligt för kommersiell användning?**  
A: Ja, Aspose.PSD kan användas både i personliga och kommersiella projekt under dess licensvillkor.

## Slutsats
I den här handledningen har vi gått igenom hur man **extraherar miniatyrbild från PSD**‑filer med Aspose.PSD för Java. Genom att följa stegen ovan kan du effektivt hämta och spara miniatyrbilder som är inbäddade i dina PSD‑dokument, vilket möjliggör snabbare förhandsvisningar och förenklade bildarbetsflöden.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Senast uppdaterad:** 2026-01-25  
**Testad med:** Aspose.PSD för Java (senaste version)  
**Författare:** Aspose