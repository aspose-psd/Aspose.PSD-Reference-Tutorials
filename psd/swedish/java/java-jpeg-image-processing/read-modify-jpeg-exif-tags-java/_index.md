---
date: 2026-10-03
description: Lär dig hur du java läser bildmetadata och ändrar JPEG EXIF-taggar med
  Aspose.PSD for Java i den här steg‑för‑steg‑guiden, perfekt för utvecklare som hanterar
  bildmetadata effektivt.
keywords:
- java read image metadata
- read EXIF tags Java
- modify JPEG metadata Java
- Aspose.PSD Java
lastmod: 2026-10-03
linktitle: Läs och modifiera JPEG EXIF-taggar i Java
og_description: Lär dig hur du java läser bildmetadata och ändrar JPEG EXIF-taggar
  med Aspose.PSD for Java. Denna guide visar steg‑för‑steg‑kod för att extrahera och
  uppdatera EXIF‑information.
og_image_alt: Guide showing how to java read image metadata and edit JPEG EXIF tags
  using Aspose.PSD for Java
og_title: Hur man java läser bildmetadata och modifierar JPEG EXIF-taggar
schemas:
- author: Aspose
  dateModified: '2026-10-03'
  description: Learn how to java read image metadata and modify JPEG EXIF tags with
    Aspose.PSD for Java in this step‑by‑step guide, perfect for developers handling
    image metadata efficiently.
  headline: How to java read image metadata and modify JPEG EXIF tags
  type: TechArticle
- description: Learn how to java read image metadata and modify JPEG EXIF tags with
    Aspose.PSD for Java in this step‑by‑step guide, perfect for developers handling
    image metadata efficiently.
  name: How to java read image metadata and modify JPEG EXIF tags
  steps:
  - name: '**Java Development Kit (JDK)** – make sure you have JDK 11 or newer. You
      can download it from the [Oracle website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).'
    text: '**Java Development Kit (JDK)** – make sure you have JDK 11 or newer. You
      can download it from the [Oracle website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).'
  - name: '**Aspose.PSD for Java library** – obtain the latest JAR from the [Aspose
      releases page](https://releases.aspose.com/psd/java/).'
    text: '**Aspose.PSD for Java library** – obtain the latest JAR from the [Aspose
      releases page](https://releases.aspose.com/psd/java/).'
  - name: '**IDE** – IntelliJ IDEA, Eclipse, or any editor you prefer.'
    text: '**IDE** – IntelliJ IDEA, Eclipse, or any editor you prefer.'
  - name: '**Basic Java knowledge** – you should be comfortable with creating projects
      and adding external JARs.'
    text: '**Basic Java knowledge** – you should be comfortable with creating projects
      and adding external JARs.'
  type: HowTo
- questions:
  - answer: EXIF (Exchangeable Image File Format) metadata stores camera settings,
      timestamps, GPS coordinates, and other information embedded in JPEG and other
      image files.
    question: What is EXIF data?
  - answer: You can get a free trial from the [Aspose releases page](https://releases.aspose.com/).
    question: Can I use Aspose.PSD for Java for free?
  - answer: Aspose.PSD for Java supports Java SE 7 and above.
    question: Is Aspose.PSD for Java compatible with all versions of Java?
  - answer: Check out the [documentation](https://reference.aspose.com/psd/java/)
      for more details.
    question: Where can I find more documentation on Aspose.PSD for Java?
  - answer: You can get support from the [Aspose PSD support forum](https://forum.aspose.com/c/psd/34/).
    question: How do I get support for Aspose.PSD for Java?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- java image metadata
- exif tags
- aspose psd
- jpeg metadata
- java tutorial
title: Hur man java läser bildmetadata och modifierar JPEG EXIF-taggar
url: /sv/java/java-jpeg-image-processing/read-modify-jpeg-exif-tags-java/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Läs och ändra JPEG EXIF-taggar i Java

## Introduktion
Om du behöver **java read image metadata** från JPEG‑filer och ändra dem programatiskt, har du hamnat på rätt ställe. I den här handledningen går vi igenom hur du extraherar och uppdaterar EXIF‑taggar med Aspose.PSD för Java. När du är klar kan du hämta kameradetaljer, orientering och anpassade fält, och sedan skriva tillbaka dem till filen – helt utan en grafisk editor.

## Snabba svar
- **Vilket bibliotek hanterar JPEG EXIF i Java?** Aspose.PSD för Java.  
- **Hur många rader kod behövs för att läsa EXIF?** Ungefär tre rader efter att bilden har laddats.  
- **Kan du ändra EXIF‑taggar?** Ja, du kan ändra vilken standard‑ eller anpassad tagg som helst och spara resultatet.  
- **Vilka bildformat stöds?** Över 150 format, inklusive PSD, JPEG, PNG, TIFF och BMP.  
- **Minsta Java‑version?** Java 7 eller högre.

## Varför använda Aspose.PSD för Java?
Aspose.PSD stödjer **150+ bildformat** och kan bearbeta filer upp till **2 GB** utan att ladda hela dokumentet i minnet, vilket ger snabba, minneslätta metadata‑operationer på stora fotokollektioner. Det erbjuder också ett enkelt API för att läsa och skriva EXIF, IPTC och XMP‑data, vilket gör batch‑bearbetning av tusentals bilder effektiv och pålitlig.

## Förutsättningar
1. **Java Development Kit (JDK)** – se till att du har JDK 11 eller nyare. Du kan ladda ner det från [Oracle website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).  
2. **Aspose.PSD för Java‑bibliotek** – hämta den senaste JAR‑filen från [Aspose releases page](https://releases.aspose.com/psd/java/).  
3. **IDE** – IntelliJ IDEA, Eclipse eller någon annan editor du föredrar.  
4. **Grundläggande kunskaper i Java** – du bör vara bekväm med att skapa projekt och lägga till externa JAR‑filer.

## Vad innebär att läsa bildmetadata i Java?
Java read image metadata avser processen att programatiskt komma åt inbäddad information såsom EXIF, IPTC och XMP som lagras i bildfiler med Java‑kod. Denna metadata kan inkludera kamerainställningar, tidsstämplar, GPS‑koordinater, upphovsrättsmeddelanden och användarkommentarer, vilket möjliggör att applikationer kan organisera, söka och manipulera bilder baserat på deras beskrivande data.

## Importera paket
Först, lägg till Aspose.PSD‑JAR‑filen i ditt projekts classpath och importera de nödvändiga klasserna.

`com.aspose.psd`‑paketet tillhandahåller kärn‑API‑et för att ladda bilder och komma åt deras resurser.

```java
import com.aspose.psd.Image;
import com.aspose.psd.exif.JpegExifData;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.resources.Thumbnail4Resource;
import com.aspose.psd.fileformats.psd.resources.ThumbnailResource;
```

## Hur läser man bildmetadata från JPEG‑filer i Java?
Ladda JPEG‑filen med `PsdImage.load("image.jpg")`, lokalisera thumbnail‑resursen som innehåller EXIF‑data och anropa sedan `ExifData.read()` för att få ett fyllt `ExifData`‑objekt. Detta en‑steg‑förfarande ger dig full åtkomst till alla standard‑EXIF‑fält och eventuella anpassade taggar du har lagt till.

## Steg 1: Ladda PSD‑bilden
PsdImage är Aspose.PSD‑klassen som representerar en PSD‑fil och erbjuder metoder för att komma åt dess resurser och metadata.  
I detta steg laddar vi PSD‑bilden som vi vill läsa EXIF‑data från. Se till att bilden finns i rätt katalog.

```java
String dataDir = "Your Document Directory";
PsdImage image = null;
try {
    image = (PsdImage) Image.load(dataDir + "1280px-Zebras_Serengeti.psd");
} catch (IOException e) {
    e.printStackTrace();
}
```

## Steg 2: Iterera över bildresurser
ThumbnailResource representerar en miniatyrbild som lagras i en PSD‑fil, ofta med inbäddad EXIF‑data.  
När bilden är laddad är nästa steg att iterera över dess resurser för att hitta thumbnail‑resursen, som vanligtvis innehåller EXIF‑data.

```java
for (int i = 0; i < image.getImageResources().length; i++) {
    if (image.getImageResources()[i] instanceof ThumbnailResource) {
        ThumbnailResource thumbnail = (ThumbnailResource) image.getImageResources()[i];
        // Proceed to next step
    }
}
```

## Steg 3: Extrahera EXIF‑data
JpegExifData är klassen som innehåller EXIF‑information extraherad från en JPEG‑bild, vilket låter dig läsa och ändra enskilda taggar.  
Nu när vi har thumbnail‑resursen kan vi extrahera EXIF‑data från den. EXIF‑data inkluderar värdefull information som kamerans ägares namn, bländarvärde, orientering och mer.

```java
JpegExifData exifData = thumbnail.getJpegOptions().getExifData();
if (exifData != null) {
    System.out.println("Camera Owner Name: " + exifData.getCameraOwnerName());
    System.out.println("Aperture Value: " + exifData.getApertureValue());
    System.out.println("Orientation: " + exifData.getOrientation());
    System.out.println("Focal Length: " + exifData.getFocalLength());
    System.out.println("Compression: " + exifData.getCompression());
}
```

## Steg 4: Ändra EXIF‑data
Efter att ha läst EXIF‑data kanske du vill ändra några av dess fält. Så här gör du:

```java
if (exifData != null) {
    exifData.setCameraOwnerName("New Camera Owner");
    exifData.setApertureValue(3.5);
    exifData.setOrientation(1);
    exifData.setFocalLength(35.0);
    exifData.setCompression(6);
    thumbnail.getJpegOptions().setExifData(exifData);
}
```

## Steg 5: Spara ändringarna
Till sist, efter att ha ändrat EXIF‑data, sparar du förändringarna till en ny PSD‑fil.

```java
try {
    image.save(dataDir + "Modified_Zebras_Serengeti.psd");
} catch (IOException e) {
    e.printStackTrace();
}
```

## Vanliga problem och lösningar
- **Saknad thumbnail‑resurs** – Vissa JPEG‑filer lagrar EXIF direkt i huvud‑bildhuvudet. Om thumbnail‑resursen saknas, använd `image.getExifData()` istället.  
- **Stora filer ger OutOfMemoryError** – Se till att köra JVM med tillräckligt heap‑utrymme (`-Xmx2g`) eller bearbeta bilden i streaming‑läge med `PsdImage.load(inputStream, loadOptions)`.  
- **Ej stödda taggtyper** – Aspose.PSD stödjer alla standard‑EXIF‑taggar; anpassade taggar kan kräva manuell byte‑nivå‑hantering.

## Vanliga frågor

**Q: Vad är EXIF‑data?**  
A: EXIF (Exchangeable Image File Format) metadata lagrar kamerainställningar, tidsstämplar, GPS‑koordinater och annan information som är inbäddad i JPEG‑ och andra bildfiler.

**Q: Kan jag använda Aspose.PSD för Java gratis?**  
A: Du kan få en gratis provversion från [Aspose releases page](https://releases.aspose.com/).

**Q: Är Aspose.PSD för Java kompatibel med alla Java‑versioner?**  
A: Aspose.PSD för Java stödjer Java SE 7 och senare.

**Q: Var kan jag hitta mer dokumentation om Aspose.PSD för Java?**  
A: Se [documentation](https://reference.aspose.com/psd/java/) för fler detaljer.

**Q: Hur får jag support för Aspose.PSD för Java?**  
A: Du kan få support via [Aspose PSD support forum](https://forum.aspose.com/c/psd/34/).

## Slutsats
Genom att följa dessa steg kan du **java read image metadata** från vilken JPEG‑fil som helst, justera de EXIF‑fält du behöver och skriva tillbaka den uppdaterade datan till filen – allt med några få rader ren Java‑kod. Aspose.PSD:s rika API gör metadata‑hantering pålitlig och presterande, så att du kan integrera det i batch‑processer, fotohanteringsverktyg eller vilken applikation som helst som behöver arbeta med bildinformation.

---

**Senast uppdaterad:** 2026-10-03  
**Testat med:** Aspose.PSD för Java 24.5  
**Författare:** Aspose

## Relaterade handledningar

- [Läs specifik EXIF‑tagginformation i Java med Aspose (asp)](/psd/java/java-jpeg-image-processing/read-specific-exif-tags-info-java/)
- [Skapa XMP‑metadata i PSD‑filer med Aspose.PSD för Java](/psd/java/image-editing/create-xmp-metadata/)
- [Ändra storlek på bild med Aspose.PSD för Java – Rita former och grundläggande bildoperationer](/psd/java/basic-image-operations/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}