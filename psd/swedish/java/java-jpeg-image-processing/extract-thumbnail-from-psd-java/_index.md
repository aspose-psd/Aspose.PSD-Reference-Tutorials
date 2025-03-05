---
title: Extrahera miniatyrbild från PSD i Java
linktitle: Extrahera miniatyrbild från PSD i Java
second_title: Aspose.PSD Java API
description: Lär dig hur du extraherar miniatyrer från PSD-filer med Aspose.PSD för Java. Den här steg-för-steg-guiden täcker allt från installation till att spara extraherade bilder.
type: docs
weight: 15
url: /sv/java/java-jpeg-image-processing/extract-thumbnail-from-psd-java/
---
## Introduktion
den här handledningen kommer vi att utforska hur man extraherar miniatyrer från PSD-filer med Aspose.PSD för Java. Miniatyrer kan vara användbara för snabba förhandsgranskningar eller för att skapa mindre versioner av bilder inbäddade i PSD-dokument. Låt oss dyka in i stegen som krävs för att uppnå detta med Aspose.PSD.
## Förutsättningar
Innan vi börjar, se till att du har följande inställning:
- Java Development Kit (JDK) installerat på ditt system.
-  Aspose.PSD för Java-bibliotek. Du kan ladda ner den från[här](https://releases.aspose.com/psd/java/).
- Grundläggande kunskaper i Java-programmering.
## Importera paket
För att komma igång, inkludera det nödvändiga Aspose.PSD-paketet i din Java-klass:
```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.resources.Thumbnail4Resource;
import com.aspose.psd.fileformats.psd.resources.ThumbnailResource;
import com.aspose.psd.imageoptions.JpegOptions;
```
## Steg 1: Ladda PSD-filen
Ladda först PSD-filen som innehåller miniatyrbilden du vill extrahera.
```java
String dataDir = "Your_Document_Directory/";
PsdImage image = (PsdImage)Image.load(dataDir + "your_file.psd");
```
 Ersätta`"Your_Document_Directory/"` med katalogsökvägen där din PSD-fil finns, och`"your_file.psd"` med namnet på din PSD-fil.
## Steg 2: Iterera över bildresurser
Iterera genom bildresurserna för att hitta miniatyrbildsresursen.
```java
for (int i = 0; i < image.getImageResources().length; i++) {
    if (image.getImageResources()[i] instanceof ThumbnailResource) {
        ThumbnailResource thumbnail = (ThumbnailResource) image.getImageResources()[i];
        
        // Extrahera miniatyrbildsdata
        int[] data = thumbnail.getThumbnailArgb32Data();
        
        // Skapa en ny bild med den extraherade miniatyrdatan
        PsdImage extractedThumbnailImage = new PsdImage(thumbnail.getWidth(), thumbnail.getHeight());
        extractedThumbnailImage.saveArgb32Pixels(extractedThumbnailImage.getBounds(), data);
        
        // Spara den extraherade miniatyren som en separat JPEG-fil
        extractedThumbnailImage.save(dataDir + "extracted_thumbnail.jpg", new JpegOptions());
        
        // Utdata framgångsmeddelande
        System.out.println("Thumbnail extracted and saved successfully.");
        
        break; // Gå ur slingan när miniatyren har hittats och bearbetats
    }
}
```
## Steg 3: Spara den extraherade miniatyrbilden
Spara den extraherade miniatyren som en separat bildfil (i det här fallet som en JPEG-fil).
## Steg 4: Hantera olika typer av miniatyrer
 Om din PSD-fil kan innehålla flera typer av miniatyrer, t.ex`Thumbnail4Resource`, kan du utöka logiken för att hantera dessa fall på liknande sätt.

## Slutsats
I den här handledningen undersökte vi hur man extraherar miniatyrer från PSD-filer med Aspose.PSD för Java. Genom att följa stegen som beskrivs ovan kan du effektivt hämta och spara miniatyrer inbäddade i dina PSD-dokument.

## FAQ's
### Vad är Aspose.PSD?
Aspose.PSD är ett Java-bibliotek som låter utvecklare arbeta med PSD och andra bildfilformat programmatiskt.
### Var kan jag hitta mer dokumentation om Aspose.PSD för Java?
 Du kan hänvisa till[dokumentation](https://reference.aspose.com/psd/java/) för detaljerade API-referenser och exempel.
### Kan jag prova Aspose.PSD gratis innan jag köper?
 Ja, du kan ladda ner en[gratis provperiod](https://releases.aspose.com/) för att utvärdera bibliotekets kapacitet.
### Hur kan jag få tillfälliga licenser för Aspose.PSD?
 Tillfälliga licenser kan erhållas från[här](https://purchase.aspose.com/temporary-license/).
### Är Aspose.PSD lämplig för kommersiellt bruk?
Ja, Aspose.PSD kan användas för både personliga och kommersiella projekt under dess licensvillkor.