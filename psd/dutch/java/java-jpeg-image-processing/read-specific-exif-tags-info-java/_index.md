---
date: 2026-10-08
description: Leer hoe u EXIF-tags kunt lezen in Java met Aspose.PSD for Java (asp)
  met onze stapsgewijze tutorial, en verbeter uw mogelijkheden voor beeldverwerking.
keywords:
- read exif tags java
- java exif tag extraction
- java image metadata extraction
lastmod: 2026-10-08
linktitle: Specifieke EXIF-taginformatie lezen in Java
og_description: Lees EXIF-tags Java-ontwikkelaars kunnen snel afbeeldingsmetadata
  extraheren met Aspose.PSD. Deze gids leidt u door het laden van een PSD, het vinden
  van miniatuurbronnen en het afdrukken van belangrijke EXIF-velden zoals WhiteBalance
  en ISO speed.
og_image_alt: Guide showing how to read EXIF tags from PSD files in Java using Aspose.PSD
og_title: Hoe EXIF-tags lezen in Java met Aspose.PSD
schemas:
- author: Aspose
  dateModified: '2026-10-08'
  description: Learn how to read EXIF tags in Java using Aspose.PSD for Java (asp)
    with our step‑by‑step tutorial, and boost your image processing capabilities.
  headline: How to read EXIF tags in Java with Aspose.PSD
  type: TechArticle
- description: Learn how to read EXIF tags in Java using Aspose.PSD for Java (asp)
    with our step‑by‑step tutorial, and boost your image processing capabilities.
  name: How to read EXIF tags in Java with Aspose.PSD
  steps:
  - name: 'Java Development Kit (JDK): Ensure you have JDK installed on your machine.
      You can download it from the [Oracle JDK website](https://www.oracle.com/java/technologies/javase-downloads.html).'
    text: 'Java Development Kit (JDK): Ensure you have JDK installed on your machine.
      You can download it from the [Oracle JDK website](https://www.oracle.com/java/technologies/javase-downloads.html).'
  - name: 'Aspose.PSD for Java: Download the library from the [Aspose.PSD for Java
      download page](https://releases.aspose.com/psd/java/).'
    text: 'Aspose.PSD for Java: Download the library from the [Aspose.PSD for Java
      download page](https://releases.aspose.com/psd/java/).'
  - name: 'Integrated Development Environment (IDE): An IDE like IntelliJ IDEA, Eclipse,
      or NetBeans will make coding more convenient.'
    text: 'Integrated Development Environment (IDE): An IDE like IntelliJ IDEA, Eclipse,
      or NetBeans will make coding more convenient.'
  - name: 'PSD file: A PSD file with EXIF data. You can use the sample provided in
      this tutorial or any other PSD file with EXIF tags.'
    text: 'PSD file: A PSD file with EXIF data. You can use the sample provided in
      this tutorial or any other PSD file with EXIF tags.'
  type: HowTo
- questions:
  - answer: Aspose.PSD (asp)
    question: What library reads EXIF data from PSD in Java?
  - answer: WhiteBalance, PixelXDimension, PixelYDimension, ISOSpeed, FocalLength,
      and more.
    question: Which tags can be extracted?
  - answer: Yes, a commercial license is required; a free trial is available.
    question: Do I need a license for production?
  - answer: The same API supports PNG, JPEG, TIFF via Java image metadata extraction.
    question: Can I use this with other image formats?
  - answer: About 10‑15 minutes for a basic read‑only scenario.
    question: How long does implementation take?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- read exif tags java
- Aspose.PSD
- java image metadata extraction
- EXIF extraction
- PSD processing
title: Hoe EXIF-tags lezen in Java met Aspose.PSD
url: /nl/java/java-jpeg-image-processing/read-specific-exif-tags-info-java/
weight: 19
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Specifieke EXIF-taginformatie lezen in Java met Aspose (asp)

## Introductie
Als je **EXIF-tags in Java** wilt lezen, biedt Aspose.PSD (asp) een nette, pure‑Java API die werkt zonder Photoshop. In deze tutorial leer je hoe je EXIF-gegevens uit een PSD‑afbeelding kunt extraheren, alleen de tags selecteert die je nodig hebt, en ze naar de console afdrukt. We behandelen alles, van het opzetten van je ontwikkelomgeving tot het ophalen van metadata zoals WhiteBalance, ISO‑snelheid en brandpuntsafstand. Laten we beginnen!

## Snelle antwoorden
- **Welke bibliotheek leest EXIF-gegevens van PSD in Java?** Aspose.PSD (asp)  
- **Welke tags kunnen worden geëxtraheerd?** WhiteBalance, PixelXDimension, PixelYDimension, ISOSpeed, FocalLength en meer.  
- **Heb ik een licentie nodig voor productie?** Ja, een commerciële licentie is vereist; een gratis proefversie is beschikbaar.  
- **Kan ik dit gebruiken met andere afbeeldingsformaten?** Dezelfde API ondersteunt PNG, JPEG, TIFF via Java‑afbeeldingsmetadata‑extractie.  
- **Hoe lang duurt de implementatie?** Ongeveer 10‑15 minuten voor een basis‑alleen‑lezen‑scenario.

## Wat is asp (Aspose.PSD voor Java)?
Aspose.PSD voor Java is een pure‑Java bibliotheek die ontwikkelaars in staat stelt te werken met Adobe Photoshop‑bestanden (PSD, PSB) zonder Photoshop te installeren. Het biedt programmatische toegang tot lagen, resources en metadata — inclusief EXIF‑tags — wat het ideaal maakt voor **java image metadata extraction**‑taken.

## Waarom Aspose.PSD (asp) gebruiken voor EXIF-extractie?
Je kunt EXIF‑tags in Java extraheren met slechts twee methode‑aanroepen, en de bibliotheek verwerkt bestanden tot 2 GB zonder het volledige document in het geheugen te laden. Ze ondersteunt **30+ afbeeldingsformaten** en behoudt exacte camera‑instellingen, waardoor je deterministische resultaten krijgt op Windows, Linux en macOS omgevingen.

## Vereisten
Voordat we in de code duiken, zijn er een paar zaken die je moet hebben:

1. **Java Development Kit (JDK):** Zorg ervoor dat je JDK op je machine geïnstalleerd hebt. Je kunt het downloaden van de [Oracle JDK-website](https://www.oracle.com/java/technologies/javase-downloads.html).  
2. **Aspose.PSD voor Java:** Download de bibliotheek van de [Aspose.PSD voor Java downloadpagina](https://releases.aspose.com/psd/java/).  
3. **Integrated Development Environment (IDE):** Een IDE zoals IntelliJ IDEA, Eclipse of NetBeans maakt coderen handiger.  
4. **PSD‑bestand:** Een PSD‑bestand met EXIF‑gegevens. Je kunt het voorbeeld gebruiken dat in deze tutorial wordt geleverd of elk ander PSD‑bestand met EXIF‑tags.

## Pakketten importeren
Importeer de benodigde Aspose.PSD‑klassen zoals Image, PsdImage, ThumbnailResource en JpegExifData om met PSD‑bestanden te werken.  
```java
import com.aspose.psd.Image;
import com.aspose.psd.exif.JpegExifData;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.resources.Thumbnail4Resource;
import com.aspose.psd.fileformats.psd.resources.ThumbnailResource;
```

## Stap 1: laad de PSD-afbeelding
`Image.load()` laadt een bestand en retourneert een Image‑object dat de afbeeldingsgegevens vertegenwoordigt.  
`PsdImage` is de Aspose.PSD‑klasse die PSD‑specifieke functionaliteit biedt.  
De `Image.load()`‑methode laadt elk ondersteund afbeeldingsbestand in het geheugen en geeft een generiek `Image`‑object terug dat je kunt casten naar een PSD‑specifiek type.  
```java
String dataDir = "Your Document Directory";
PsdImage image = (PsdImage) Image.load(dataDir + "1280px-Zebras_Serengeti.psd");
```

In deze stap laden we het PSD‑bestand met de `Image.load()`‑methode. De `PsdImage`‑klasse wordt gebruikt om de PSD‑afbeelding te vertegenwoordigen, en we casten de geladen afbeelding naar deze klasse om PSD‑specifieke functionaliteiten te benaderen.

## Stap 2: doorloop de afbeeldingsbronnen
`PsdImage.getResources()` retourneert een collectie van ingebedde resources zoals thumbnails en EXIF‑gegevens.  
De `PsdImage.getResources()`‑aanroep geeft een collectie van alle ingebedde resources terug. Door deze collectie te itereren kun je thumbnail‑resources vinden die EXIF‑metadata bevatten.  
```java
for (int i = 0; i < image.getImageResources().length; i++) {
    if (image.getImageResources()[i] instanceof ThumbnailResource || 
        image.getImageResources()[i] instanceof Thumbnail4Resource) {
        // Further processing will be done here
    }
}
```

We lopen door de afbeeldingsresources met een `for`‑lus. Het doel is om resources te identificeren die instanties zijn van `ThumbnailResource` of `Thumbnail4Resource`, aangezien deze de EXIF‑gegevens bevatten.

## Stap 3: EXIF-gegevens extraheren
`ThumbnailResource.getJpegOptions()` biedt toegang tot JPEG‑opties inclusief EXIF‑metadata.  
`JpegExifData` bevat individuele EXIF‑tagwaarden.  
De `ThumbnailResource.getJpegOptions()`‑methode biedt toegang tot een `JpegExifData`‑object, dat individuele EXIF‑tags bevat zoals WhiteBalance, ISOSpeed en FocalLength.  
```java
if (image.getImageResources()[i] instanceof ThumbnailResource) {
    JpegExifData exif = ((ThumbnailResource) image.getImageResources()[i]).getJpegOptions().getExifData();
    if (exif != null) {
        System.out.println("Exif WhiteBalance: " + exif.getWhiteBalance());
        System.out.println("Exif PixelXDimension: " + exif.getPixelXDimension());
        System.out.println("Exif PixelYDimension: " + exif.getPixelYDimension());
        System.out.println("Exif ISOSpeed: " + exif.getISOSpeed());
        System.out.println("Exif FocalLength: " + exif.getFocalLength());
    }
}
```

We gebruiken een `if`‑statement om te controleren of de resource een instantie is van `ThumbnailResource`. Als dat zo is, casten we deze en halen we de `JpegOptions` op om toegang te krijgen tot de `ExifData`. Ten slotte drukken we verschillende EXIF‑tags af, zoals WhiteBalance, Pixel‑dimensies, ISOSpeed en FocalLength.

## Veelvoorkomende problemen & tips
- **Null EXIF‑gegevens:** Sommige PSD‑bestanden bevatten mogelijk geen thumbnail‑resource met EXIF‑informatie. Controleer altijd op `null` voordat je tag‑waarden benadert.  
- **Bestandspad‑fouten:** Gebruik absolute paden of zorg ervoor dat de werkdirectory wijst naar de map met je PSD‑bestand.  
- **Licentiebeperkingen:** De gratis proefversie beperkt het aantal pagina's dat je kunt verwerken; upgrade naar een volledige licentie voor onbeperkt gebruik.

## Veelgestelde vragen
### Wat zijn EXIF-gegevens?
EXIF (Exchangeable Image File Format)‑gegevens zijn metadata die in beeldbestanden zijn ingebed en informatie bevatten zoals camera‑instellingen, datum en tijd, en afbeeldingsdimensies.

### Kan ik EXIF-gegevens bewerken met Aspose.PSD?
Ja, Aspose.PSD stelt je in staat EXIF‑gegevens te lezen en te wijzigen. Je kunt tags bijwerken en de wijzigingen terug opslaan in het beeldbestand.

### Is Aspose.PSD voor Java gratis?
Aspose.PSD biedt een gratis proefversie die je kunt downloaden van de [Aspose.PSD officiële releases‑pagina](https://releases.aspose.com/). Voor volledige functionaliteit moet je een licentie aanschaffen.

### Welke andere formaten ondersteunt Aspose.PSD?
Aspose.PSD ondersteunt diverse Adobe Photoshop‑formaten, waaronder PSD, PSB en meer. Het biedt ook opties om deze formaten te converteren naar PNG, JPEG, TIFF, enzovoort.

### Hoe krijg ik ondersteuning voor Aspose.PSD?
Je kunt ondersteuning krijgen via het Aspose.PSD [forum](https://forum.aspose.com/c/psd/34).

### Hoe helpt dit bij **java image metadata extraction**?
Door het `JpegExifData`‑object te gebruiken, kun je programmatisch elke EXIF‑tag ophalen die je nodig hebt, waardoor het een solide basis vormt voor bredere metadata‑extractietaken over verschillende beeldformaten.

**Laatst bijgewerkt:** 2026-10-08  
**Getest met:** Aspose.PSD voor Java 24.11 (latest at time of writing)  
**Auteur:** Aspose

## Gerelateerde tutorials

- [Lees en wijzig JPEG Exif-tags Java](/psd/java/java-jpeg-image-processing/read-modify-jpeg-exif-tags-java/)
- [Java JPEG-afbeeldingsverwerking](/psd/java/java-jpeg-image-processing/)
- [Hoe een afbeelding roteren onder een specifieke hoek met Aspose.PSD voor Java](/psd/java/advanced-image-manipulation/rotate-image-specific-angle/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}