---
date: 2026-07-08
description: 'Java image editing library tutorial: leer hoe je een afbeelding bijsnijdt
  met Java met behulp van Aspose.PSD voor Java, formaat wijzigen, canvas uitbreiden
  en PSD naar JPEG converteren.'
keywords:
- java image editing library
- java image processing tutorial
- how to crop image java
lastmod: 2026-07-08
linktitle: Uitbreiden en bijsnijden van afbeeldingen
og_description: Java image editing library tutorial toont hoe je afbeeldingen kunt
  bijsnijden, canvas kunt uitbreiden en PSD naar JPEG kunt converteren met Aspose.PSD
  voor Java in enkele minuten.
og_image_alt: 'Guide: Crop and expand images in Java with Aspose.PSD'
og_title: Java Image Editing Library – Afbeelding bijsnijden met Aspose.PSD
schemas:
- author: Aspose
  dateModified: '2026-07-08'
  description: 'Java image editing library tutorial: learn how to crop image java
    using Aspose.PSD for Java, resize, expand canvas, and convert PSD to JPEG.'
  headline: Java Image Editing Library – Crop Image with Aspose.PSD
  type: TechArticle
- questions:
  - answer: Aspose.PSD for Java.
    question: What library handles crop image java?
  - answer: A free trial works for testing; a commercial license is required for production.
    question: Do I need a license for development?
  - answer: Yes, using `JpegOptions` together with a cropping rectangle.
    question: Can I convert PSD to JPEG while cropping?
  - answer: Aspose.PSD supports Java 8 and newer versions.
    question: Is Java 8 supported?
  - answer: Typically under 10 minutes for a basic crop operation.
    question: How long does the implementation take?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- java image editing
- Aspose.PSD
- image cropping
- PSD to JPEG
title: Java Image Editing Library – Afbeelding bijsnijden met Aspose.PSD
url: /nl/java/image-editing/expand-and-crop-images/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Java-afbeeldingsbewerkingsbibliotheek: Afbeelding bijsnijden Java met Aspose.PSD

## Inleiding

In deze tutorial leer je hoe je een **java image editing library**—specifiek Aspose.PSD for Java—gebruikt om PSD‑bestanden bij te snijden, uit te breiden en te converteren naar JPEG. Of je nu assets voorbereidt voor een webportaal of thumbnails automatisch genereert, de onderstaande stappen bieden een herhaalbare, productie‑klare workflow die je in elk Java 8+ project kunt integreren.

## Snelle antwoorden
- **Welke bibliotheek behandelt crop image java?** Aspose.PSD for Java.  
- **Heb ik een licentie nodig voor ontwikkeling?** Een gratis proefversie werkt voor testen; een commerciële licentie is vereist voor productie.  
- **Kan ik PSD naar JPEG converteren tijdens het bijsnijden?** Ja, door `JpegOptions` te gebruiken samen met een bijsnijdrechthoek.  
- **Wordt Java 8 ondersteund?** Aspose.PSD ondersteunt Java 8 en nieuwere versies.  
- **Hoe lang duurt de implementatie?** Meestal minder dan 10 minuten voor een eenvoudige bijsnijdbewerking.

## Wat is “crop image java”?

Crop image java betekent het selecteren van een rechthoekig gebied van de bronafbeelding en alles buiten dat gebied weggooien. Met Aspose.PSD maak je een `Rectangle` die het gebied definieert, pas je deze toe op een `RasterImage`, en sla je vervolgens het resultaat op in elk ondersteund formaat zoals JPEG.

## Waarom Aspose.PSD gebruiken voor Java-afbeeldingsbijsnijden?

Aspose.PSD biedt een **java image editing library** die PSD‑bestanden native verwerkt, meer dan 100 laagfuncties ondersteunt en afbeeldingen tot 10 000 × 10 000 pixels kan verwerken terwijl het geheugengebruik onder 500 MB blijft. Het biedt ook ingebouwde conversie naar JPEG, PNG, BMP en meer, zonder externe tools nodig te hebben. Dit maakt bulk‑verwerkingspijplijnen snel, betrouwbaar en gemakkelijk te onderhouden.

## Vereisten

1. **Java Development Kit (JDK)** – Java 8 of later geïnstalleerd.  
2. **Aspose.PSD for Java** – download de bibliotheek van de officiële site **[here](https://releases.aspose.com/psd/java/)**.  

> **Pro tip:** Voeg de Aspose.PSD JAR toe aan de classpath van je project of Maven/Gradle‑afhankelijkheden om `ClassNotFoundException` te vermijden.

## Pakketten importeren

Voeg de benodigde imports toe aan je Java‑bronbestand. Deze klassen geven je toegang tot het laden van afbeeldingen, rastermanipulatie, rechthoekdefinitie en JPEG‑exportopties.

## Hoe Crop Image Java gebruiken met Aspose.PSD?

Laad de bron‑PSD met `RasterImage`, definieer een `Rectangle` die het bijsnijdgebied beschrijft (negatieve coördinaten kunnen het canvas uitbreiden), en sla tenslotte het resultaat op met `JpegOptions`. Deze drie‑stappen‑stroom behandelt zowel bijsnijden als formaatconversie in één enkele stap, waardoor tussenbestanden overbodig worden.

## Stap 1: Stel uw documentmap in

Geef de map op die het bron‑PSD‑bestand bevat. Vervang de tijdelijke aanduiding door het daadwerkelijke pad op uw machine.

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;
import com.aspose.psd.Rectangle;

import com.aspose.psd.imageoptions.JpegOptions;
```

## Stap 2: Specificeer bron- en bestemmingspaden

Definieer waar de PSD moet worden gelezen en waar de bijgesneden JPEG moet worden weggeschreven.

```java
String dataDir = "Your Document Directory";
```

## Stap 3: Laad en cache de afbeelding

`RasterImage` vertegenwoordigt een gerasterde versie van een PSD‑bestand in het geheugen.  
Laad de PSD in een `RasterImage`‑object. Caching verbetert de prestaties voor daaropvolgende bewerkingen zoals bijsnijden.

```java
String sourceFile = dataDir + "example1.psd";
String destName = dataDir + "jpeg_out.jpg";
```

## Stap 4: Maak een rechthoek voor bijsnijden

`Rectangle` definieert de X‑, Y‑coördinaten en de breedte/hoogte van het bijsnijdgebied.  
Maak een `Rectangle` die het gebied beschrijft dat je wilt behouden. De coördinaten kunnen negatief zijn om het canvas vóór het bijsnijden te **expanderen**, wat handig is om een rand rond de originele afbeelding toe te voegen.

```java
RasterImage rasterImage = (RasterImage)Image.load(sourceFile);
rasterImage.cacheData();
```

> **Waarom negatieve coördinaten gebruiken?**  
> Negatieve X/Y‑waarden verschuiven het bijsnijdgebied naar links/boven, waardoor effectief lege ruimte (expansie) rond de originele inhoud wordt toegevoegd vóór de uiteindelijke bijsnijding.

## Stap 5: Sla de bijgesneden afbeelding op

`JpegOptions` specificeert instellingen voor JPEG‑output, zoals kwaliteit en compressie.  
Sla tenslotte de resulterende afbeelding op met `JpegOptions`. Deze stap toont ook **convert psd jpeg** terwijl de bijsnijdrechthoek wordt toegepast.

```java
Rectangle destRect = new Rectangle(-200, -200, 300, 300);
```

> **Resultaat:** `jpeg_out.jpg` bevat nu een afbeelding van 300 × 300 pixel die met 200 px aan elke kant is uitgebreid en vervolgens is bijgesneden tot de gedefinieerde rechthoek.

Gefeliciteerd! Je hebt met succes **java image cropping** uitgevoerd, het canvas uitgebreid en een PSD‑bestand naar JPEG geconverteerd — allemaal in een paar beknopte code‑regels.

## Veelvoorkomende gebruikssituaties

- **Assets voorbereiden voor web** – bijsnijden en de grootte van screenshots of ontwerpen aanpassen vóór het uploaden.  
- **Thumbnails genereren** – een specifiek gebied uit een grote PSD extraheren voor voorbeelddoeleinden.  
- **Geautomatiseerde batchverwerking** – doorloop een map met PSD‑bestanden en pas dezelfde bijsnijdrechthoek op elk bestand toe.

## Probleemoplossing & Tips

| Probleem | Aanbevolen oplossing |
|----------|----------------------|
| `OutOfMemoryError` bij het laden van grote PSD's | Roep `rasterImage.cacheData()` vroeg aan en overweeg het vergroten van de JVM‑heap‑grootte (`-Xmx`). |
| Bijsnijdgebied is niet gecentreerd | Controleer de X/Y‑offsets van de rechthoek; onthoud dat negatieve waarden het canvas uitbreiden. |
| Uitvoer‑JPEG ziet er wazig uit | Pas de kwaliteitinstelling van `JpegOptions` aan (bijv. `new JpegOptions { Quality = 90 }`). |

## Veelgestelde vragen

### Q1: Is Aspose.PSD compatibel met verschillende Java‑versies?

A1: Ja, Aspose.PSD ondersteunt Java 8, 11, 17 en nieuwere releases, waardoor brede compatibiliteit met ontwikkelomgevingen wordt gegarandeerd.

### Q2: Kan ik Aspose.PSD gebruiken voor commerciële projecten?

A2: Absoluut, Aspose.PSD biedt commerciële licenties voor ontwikkelaars, waardoor het gebruik in zowel persoonlijke als commerciële toepassingen mogelijk is.

### Q3: Zijn er beperkingen op de ondersteunde afbeeldingsbestandsformaten?

A3: Aspose.PSD ondersteunt meer dan 30 afbeeldingsformaten, waaronder PSD, JPEG, PNG, BMP, TIFF en meer. Raadpleeg de [documentation](https://reference.aspose.com/psd/java/) voor een volledige lijst.

### Q4: Hoe kan ik ondersteuning krijgen voor Aspose.PSD‑gerelateerde vragen?

A4: Bezoek het [Aspose.PSD forum](https://forum.aspose.com/c/psd/34) om hulp te zoeken bij de community of het Aspose‑ondersteuningsteam.

### Q5: Is er een gratis proefversie beschikbaar?

A5: Ja, je kunt Aspose.PSD verkennen met een gratis proefversie. Download deze [here](https://releases.aspose.com/).

---

**Laatst bijgewerkt:** 2026-07-08  
**Getest met:** Aspose.PSD for Java 24.12  
**Auteur:** Aspose  

{{< blocks/products/products-backtop-button >}}

```java
rasterImage.save(destName, new JpegOptions(), destRect);
```

## Gerelateerde tutorials

- [Eenvoudig schalen met Aspose.PSD – Java Image Manipulation Library](/psd/java/basic-image-operations/simple-resizing/)
- [Hoe afbeelding 270 graden roteren met Aspose.PSD for Java](/psd/java/advanced-image-manipulation/rotate-image/)
- [Hoe gamma aanpassen in Java Image Processing met Aspose.PSD](/psd/java/advanced-techniques/adjust-gamma/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}