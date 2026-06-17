---
date: 2026-03-13
description: Lär dig hur du skapar PSD‑miniatyrbilder i Java med Aspose.PSD. Följ
  vår steg‑för‑steg‑guide för att snabbt generera miniatyrbilder från PSD‑filer.
linktitle: Create Thumbnails from PSD Files using Java
second_title: Aspose.PSD Java API
title: Skapa PSD‑miniatyrbild Java – Generera miniatyrbilder från PSD
url: /sv/java/modifying-converting-psd-images/create-thumbnails-psd-files/
weight: 24
---

 Aspose  

Now translate Swedish.

Need to keep code block placeholders unchanged.

Let's produce final content.

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Skapa PSD‑thumbnail i Java – Generera miniatyrbilder från PSD

## Introduction
Om du behöver **create PSD thumbnail Java**‑kod som extraherar förhandsbilder från Photoshop‑filer, har du kommit till rätt ställe. Oavsett om du bygger en digital tillgångshanterare, ett webb‑galleri eller en automatiserad batch‑process‑pipeline, kan generering av miniatyrbilder från PSD‑filer dramatiskt förbättra prestanda och användarupplevelse. I den här handledningen går vi igenom hela processen med Aspose.PSD för Java och visar hur du laddar en PSD, hittar dess inbäddade thumbnail‑resurser och sparar dem som separata bildfiler.

## Quick Answers
- **Vilket bibliotek är bäst för PSD‑thumbnail‑extraktion?** Aspose.PSD för Java.  
- **Hur lång tid tar implementeringen?** Ungefär 10‑15 minuter för en grundläggande uppsättning.  
- **Behöver jag ha Photoshop installerat?** Nej, Aspose.PSD fungerar oberoende.  
- **Vilka bildformat kan jag exportera thumbnailen till?** Alla format som stöds av Aspose.PSD (t.ex. BMP, PNG, JPEG).  
- **Krävs en licens för produktion?** Ja, en kommersiell licens behövs för produktionsanvändning.

## What is “create PSD thumbnail Java”?
Att skapa en PSD‑thumbnail i Java betyder att programmässigt läsa den thumbnail‑förhandsgranskning som lagras inuti ett Photoshop‑dokument (PSD) och skriva ut den som en separat bildfil. Detta är användbart för att snabbt generera förhandsvisningar utan att ladda hela, ofta stora, PSD‑innehållet.

## Why use Aspose.PSD for this task?
- **Ingen Photoshop‑beroende:** Fungerar på vilken plattform som helst med en JDK.  
- **Full PSD‑support:** Hanterar alla PSD‑versioner och resurser, inklusive thumbnails.  
- **Enkel API:** Några få rader kod för att extrahera och spara thumbnails.  
- **Prestandaoptimerad:** Effektiv minneshantering för stora filer.

## Prerequisites
Innan vi dyker ner i detaljerna kring thumbnail‑skapande, låt oss gå igenom vad du behöver för att komma igång.

### Java Development Environment
- **Java JDK:** Se till att du har Java Development Kit (JDK) installerat på din dator. Du kan ladda ner det [här](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).  
- **IDE:** En Integrated Development Environment (IDE) som IntelliJ IDEA, Eclipse eller NetBeans gör kodningen enklare.

### Aspose.PSD Library
- Du måste inkludera Aspose.PSD‑biblioteket i ditt projekt. Du kan [ladda ner den senaste versionen här](https://releases.aspose.com/psd/java/).

### Basic Knowledge of Java
- Bekantskap med Java‑grunderna hjälper dig att navigera genom exempel‑koden mer effektivt. Begrepp som klasser, objekt och loopar kommer att användas frekvent.

## Import Packages
Börja med att importera de nödvändiga klasserna från Aspose.PSD‑biblioteket. Detta steg är avgörande eftersom det möjliggör att utnyttja bibliotekets funktioner i din kod.

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.resources.ThumbnailFormat;
import com.aspose.psd.fileformats.psd.resources.ThumbnailResource;
```

Med förutsättningarna på plats, låt oss hoppa in i huvuddelen! Att skapa thumbnails från PSD‑filer innebär några enkla steg, och jag kommer att bryta ner dem åt dig.

## How to create PSD thumbnail Java – Step‑by‑Step Guide

### Step 1: Set Up Your Environment
Här är hur du initierar ditt projekt och förbereder för thumbnail‑generering.

1. **Create a Java Project**  
   - Öppna din IDE och skapa ett nytt Java‑projekt.  
   - Namnge det något i stil med `"PsdThumbnailGenerator"`.

2. **Include Aspose.PSD Library**  
   - Lägg till Aspose.PSD‑JAR‑filen i ditt projekts byggsökväg.  
   - Om du använder Maven, inkludera den i din `pom.xml`:

```xml
<dependency>
    <groupId>com.aspose</groupId>
    <artifactId>aspose-psd</artifactId>
    <version>your_version_here</version>
</dependency>
```

### Step 2: Load the PSD File
Nästa steg är att ladda PSD‑filen som du vill skapa thumbnails från.

1. **Specify Your Document Directory**  
   Definiera katalogen där din PSD‑fil finns.

```java
String dataDir = "Your Document Directory"; // Replace with your path
```

2. **Load the PSD File**  
   Använd `PsdImage`‑klassen för att ladda din PSD‑fil.

```java
PsdImage image = (PsdImage) Image.load(dataDir + "sample.psd");
```

> **Pro tip:** Förvara dina PSD‑filer i en dedikerad mapp (t.ex. `src/main/resources`) för att undvika sökvägsproblem.

### Step 3: Iterate Over PSD Resources
Nu när vi har vår PSD‑bild laddad, är nästa steg att undersöka dess resurser.

1. **Get Resources Count**  
   Vi loopar igenom alla resurser i PSD‑filen.

```java
for (int i = 0; i < image.getImageResources().length; i++) {
    // Processing resources
}
```

2. **Identify Thumbnail Resources**  
   Inuti loopen, kontrollera om en resurs är en thumbnail.

```java
if (image.getImageResources()[i] instanceof ThumbnailResource) {
    // Process the thumbnail
}
```

### Step 4: Process the Thumbnail
När vi identifierat en thumbnail‑resurs måste vi hantera den på rätt sätt.

1. **Retrieve and Check Thumbnail Format**  
   Om resursen faktiskt är en thumbnail, hämta den och kontrollera dess format.

```java
ThumbnailResource thumbnail = (ThumbnailResource) image.getImageResources()[i];
if (thumbnail.getFormat() == ThumbnailFormat.KJpegRgb) {
    // Create and save the thumbnail
}
```

### Step 5: Create and Save the Thumbnail
Det är här magin händer! Vi skapar en ny bild från thumbnail‑data och sparar den.

1. **Create a New Image**  
   Vi använder bredden och höjden på thumbnail‑resursen för att skapa en ny bitmap‑bild.

```java
PsdImage thumbnailImage = new PsdImage(thumbnail.getWidth(), thumbnail.getHeight());
```

2. **Store Pixels in the New Image**  
   Överför thumbnail‑data till den nyskapade bilden.

```java
thumbnailImage.savePixels(thumbnailImage.getBounds(), thumbnail.getThumbnailData());
```

3. **Save the Thumbnail Image**  
   Slutligen sparar du thumbnail‑bilden till din dokumentkatalog med ett unikt namn.

```java
thumbnailImage.save(dataDir + "CreateThumbnailsFromPSDFiles_out_" + i + ".bmp");
```

> **Common pitfall:** Att glömma att stänga `PsdImage`‑objekten kan leda till minnesläckor. Packa in bildhanteringskoden i ett try‑with‑resources‑block om du använder Java 7+.

## Conclusion
Genom att följa dessa steg har du nu en solid, återanvändbar metod för att **create PSD thumbnail Java**‑implementationer som extraherar förhandsbilder från vilken Photoshop‑fil som helst. Denna teknik kan integreras i batch‑processorer, webbtjänster eller skrivbordsverktyg för att snabba upp bildkatalogisering och förbättra UI‑responsen. Prova med din egen PSD‑samling och se hur snabbt du kan generera lätta förhandsvisningar!

## FAQ's
### What is Aspose.PSD?
Aspose.PSD är ett Java‑bibliotek som låter utvecklare arbeta med Photoshop‑filer, vilket gör det enklare att manipulera och hantera PSD‑filer programmässigt.

### Can I use Aspose.PSD for free?
Ja, Aspose erbjuder en gratis provversion som du kan använda för att testa biblioteket innan du köper en licens.

### What formats can I save the thumbnails in?
I detta exempel sparade vi thumbnails i BMP‑format, men Aspose.PSD stöder även flera andra format.

### Do I need Photoshop installed to use Aspose.PSD?
Nej, Aspose.PSD fungerar oberoende av Photoshop.

### Where can I find more information about Aspose.PSD?
Du kan läsa mer i [Aspose.PSD‑dokumentationen](https://reference.aspose.com/psd/java/) för detaljer, handledningar och resurser.

## Frequently Asked Questions

**Q: How do I extract thumbnails from a password‑protected PSD?**  
A: Load the PSD with the appropriate overload of `Image.load` that accepts a password parameter.

**Q: Can I generate thumbnails in PNG instead of BMP?**  
A: Absolutely. Change the file extension in the `save` method and Aspose.PSD will handle the conversion.

**Q: Is there a way to batch‑process multiple PSD files?**  
A: Wrap the code inside a loop that iterates over a directory of PSD files, reusing the same extraction logic for each file.

**Q: What Java version is required?**  
A: Aspose.PSD supports Java 8 and later. Using the latest JDK is recommended for performance and security.

**Q: Does the library handle large PSD files efficiently?**  
A: Yes, Aspose.PSD uses lazy loading and optimized memory management to work with large files without exhausting heap space.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Last Updated:** 2026-03-13  
**Tested With:** Aspose.PSD 24.11 for Java (latest at time of writing)  
**Author:** Aspose