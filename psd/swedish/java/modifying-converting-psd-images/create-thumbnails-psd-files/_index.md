---
title: Skapa miniatyrer från PSD-filer med Java
linktitle: Skapa miniatyrer från PSD-filer med Java
second_title: Aspose.PSD Java API
description: Lär dig hur du enkelt skapar miniatyrer från PSD-filer med Java och Aspose.PSD. Följ vår steg-för-steg-guide för sömlös bildbehandling.
weight: 24
url: /sv/java/modifying-converting-psd-images/create-thumbnails-psd-files/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Skapa miniatyrer från PSD-filer med Java

## Introduktion
en värld av grafisk design är det vanligt att arbeta med PSD-filer (Photoshop Document). Oavsett om du är en erfaren utvecklare, en grafisk designer eller bara någon som vill dyka in i bildbehandling, kan du spara tid och effektivisera ditt arbetsflöde genom att skapa miniatyrer från PSD-filer. Denna handledning guidar dig genom hela processen med Aspose.PSD för Java. Aspose.PSD är inte bara ett robust bibliotek för att hantera Photoshop-filer, utan det gör också uppgiften intuitiv och hanterbar. Är du redo att lära dig hur du skapar miniatyrer från PSD-filer effektivt?
## Förutsättningar
Innan vi dyker in i det finurliga med att skapa miniatyrer, låt oss ta upp vad du behöver för att komma igång.
### Java utvecklingsmiljö
-  Java JDK: Se till att du har Java Development Kit (JDK) installerat på din dator. Du kan ladda ner den[här](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).
- IDE: En integrerad utvecklingsmiljö (IDE) som IntelliJ IDEA, Eclipse eller NetBeans kommer att göra kodningen enklare.
### Aspose.PSD-bibliotek
- Du måste inkludera Aspose.PSD-biblioteket i ditt projekt. Du kan[ladda ner den senaste versionen här](https://releases.aspose.com/psd/java/).
### Grundläggande kunskaper i Java
- Bekantskap med Java-grunderna hjälper dig att navigera genom exempelkoden mer effektivt. Begrepp som klasser, objekt och loopar kommer att användas ofta.
## Importera paket
Börja med att importera de nödvändiga klasserna från Aspose.PSD-biblioteket. Detta steg är avgörande eftersom det gör att du kan utnyttja bibliotekets funktioner i din kod.
```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.resources.ThumbnailFormat;
import com.aspose.psd.fileformats.psd.resources.ThumbnailResource;
```
Med förutsättningarna ur vägen, låt oss hoppa in i huvudevenemanget! Att skapa miniatyrer från PSD-filer innebär några enkla steg, och jag ska dela upp det åt dig.
## Steg 1: Ställ in din miljö
Så här startar du ditt projekt och förbereder dig för generering av miniatyrbilder.
1. Skapa ett Java-projekt:
   - Öppna din IDE och skapa ett nytt Java-projekt.
   - Namnge det något i stil med "PsdThumbnailGenerator".
2. Inkludera Aspose.PSD-bibliotek:
   -  Lägg till Aspose.PSD JAR-filen till ditt projekts byggväg. Om du använder Maven, inkludera det i din`pom.xml`:
     ```xml
     <dependency>
         <groupId>com.aspose</groupId>
         <artifactId>aspose-psd</artifactId>
         <version>your_version_here</version>
     </dependency>
     ```
## Steg 2: Ladda PSD-filen
Därefter måste vi ladda PSD-filen från vilken vi vill skapa miniatyrer. 
1. Ange din dokumentkatalog:
   Definiera katalogen där din PSD-fil finns.
   ```java
   String dataDir = "Your Document Directory"; // Ersätt med din väg
   ```
2. Ladda PSD-filen:
    Använd`PsdImage` klass för att ladda din PSD-fil.
   ```java
   PsdImage image = (PsdImage) Image.load(dataDir + "sample.psd");
   ```
 Här,`sample.psd` är namnet på din PSD-fil. Justera detta efter ditt filnamn.
## Steg 3: Iterera över PSD-resurser
Nu när vi har laddat vår PSD-bild är nästa steg att undersöka dess resurser.
1. Få resursräkning:
   Vi går igenom alla resurser i PSD-filen.
   ```java
   for (int i = 0; i < image.getImageResources().length; i++) {
       // Bearbetningsresurser
   }
   ```
   
2. Identifiera miniatyrresurser:
   Inuti slingan, kontrollera om en resurs är en miniatyrbild.
   ```java
   if (image.getImageResources()[i] instanceof ThumbnailResource) {
       // Bearbeta miniatyren
   }
   ```
## Steg 4: Bearbeta miniatyrbilden
När vi har identifierat en miniatyrbildsresurs måste vi hantera den därefter.
1. Hämta och kontrollera miniatyrformat:
   Om resursen verkligen är en miniatyr, hämta den och kontrollera dess format.
   ```java
   ThumbnailResource thumbnail = (ThumbnailResource) image.getImageResources()[i];
   if (thumbnail.getFormat() == ThumbnailFormat.KJpegRgb) {
       // Skapa och spara miniatyren
   }
   ```
## Steg 5: Skapa och spara miniatyrbilden
Det är här magin händer! Vi kommer att skapa en ny bild från miniatyrdata och spara den.
1. Skapa en ny bild:
   Vi kommer att använda bredden och höjden på miniatyrresursen för att skapa en ny bitmappsbild.
   ```java
   PsdImage thumbnailImage = new PsdImage(thumbnail.getWidth(), thumbnail.getHeight());
   ```
2. Lagra pixlar i den nya bilden:
   Överför miniatyrdata till den nyskapade bilden.
   ```java
   thumbnailImage.savePixels(thumbnailImage.getBounds(), thumbnail.getThumbnailData());
   ```
3. Spara miniatyrbilden:
   Slutligen sparar du miniatyrbilden i din dokumentkatalog med ett unikt namn.
   ```java
   thumbnailImage.save(dataDir + "CreateThumbnailsFromPSDFiles_out_" + i + ".bmp");
   ```

## Slutsats
Att skapa miniatyrer från PSD-filer med Java och Aspose.PSD kan vara en enkel uppgift när du väl delar upp det i hanterbara steg. Med denna handledning har du nu möjlighet att extrahera miniatyrer från dina PSD-filer med lätthet, vilket ger dig ett snyggt verktyg för att förbättra ditt arbetsflöde. Så vad hindrar dig? Lägg vantarna på några PSD-filer och prova!
## FAQ's
### Vad är Aspose.PSD?
Aspose.PSD är ett Java-bibliotek som låter utvecklare arbeta med Photoshop-filer, vilket gör det lättare att manipulera och hantera PSD-filer programmatiskt.
### Kan jag använda Aspose.PSD gratis?
Ja, Aspose erbjuder en gratis provperiod som du kan använda för att testa biblioteket innan du köper en licens.
### Vilka format kan jag spara miniatyrerna i?
I det här exemplet sparade vi miniatyrerna i BMP-format, men Aspose.PSD stöder också olika andra format.
### Behöver jag Photoshop installerat för att använda Aspose.PSD?
Nej, Aspose.PSD fungerar oberoende av Photoshop.
### Var kan jag hitta mer information om Aspose.PSD?
 Du kan kolla in[Aspose.PSD-dokumentation](https://reference.aspose.com/psd/java/) för mer information, handledning och resurser.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
