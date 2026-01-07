---
date: 2026-01-07
description: Leer hoe je afbeeldingen bijsnijdt in Java met Aspose.PSD voor Java.
  Stapsgewijze handleiding voor het bijsnijden, schalen en converteren van PSD naar
  JPEG.
linktitle: Expand and Crop Images
second_title: Aspose.PSD Java API
title: 'Afbeelding bijsnijden Java: Uitbreiden en bijsnijden van afbeeldingen met
  Aspose.PSD voor Java'
url: /nl/java/image-editing/expand-and-crop-images/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Crop Image Java: Uitbreiden en bijsnijden van afbeeldingen met Aspose.PSD voor Java

## Inleiding

In deze tutorial ontdek je hoe je **crop image java** kunt gebruiken met de Aspose.PSD bibliotheek. Of je nu een canvas moet uitbreiden, ongewenste randen moet bijsnijden, of een PSD‑bestand naar een JPEG wilt converteren, de onderstaande stappen begeleiden je door een helder, herhaalbaar proces. We behandelen de vereisten, import‑statements en elke code‑stap met duidelijke uitleg zodat je de techniek kunt toepassen in real‑world projecten.

## Snelle antwoorden
- **Welke bibliotheek behandelt crop image java?** Aspose.PSD for Java.
- **Heb ik een licentie nodig voor ontwikkeling?** Een gratis proefversie werkt voor testen; een commerciële licentie is vereist voor productie.
- **Kan ik PSD naar JPEG converteren tijdens het bijsnijden?** Ja, door `JpegOptions` te gebruiken in combinatie met een bijsnijdrechthoek.
- **Wordt Java 8 ondersteund?** Aspose.PSD ondersteunt Java 8 en nieuwere versies.
- **Hoe lang duurt de implementatie?** Meestal minder dan 10 minuten voor een basis‑bijsnijdbewerking.

## Wat is “crop image java”?

Een afbeelding bijsnijden in Java betekent het selecteren van een rechthoekig gebied van de bronafbeelding en de rest negeren. Met Aspose.PSD kun je dit gebied definiëren met een `Rectangle`‑object en vervolgens het resultaat opslaan in een ander formaat, zoals JPEG.

## Waarom Aspose.PSD voor Java‑afbeeldingsbijsnijden gebruiken?

- **Volledige PSD‑ondersteuning** – werk direct met gelaagde PSD‑bestanden zonder ze eerst te converteren.  
- **Hoge‑prestaties rasterverwerking** – efficiënt geheugenverbruik voor grote afbeeldingen.  
- **Ingebouwde conversie** – eenvoudig exporteren naar JPEG, PNG, BMP, enz., terwijl je bijsnijden of canvasuitbreiding toepast.  
- **Cross‑platform** – werkt op elk systeem dat Java draait.

## Vereisten

Voordat we beginnen, zorg ervoor dat je het volgende hebt:

1. **Java Development Kit (JDK)** – Java 8 of later geïnstalleerd.  
2. **Aspose.PSD for Java** – download de bibliotheek van de officiële site **[hier](https://releases.aspose.com/psd/java/)**.  

> **Pro tip:** Voeg de Aspose.PSD‑JAR toe aan de classpath van je project of aan de Maven/Gradle‑afhankelijkheden om `ClassNotFoundException` te voorkomen.

## Import pakketten

Voeg de benodigde imports toe aan je Java‑bronbestand. Deze klassen geven je toegang tot het laden van afbeeldingen, rastermanipulatie, rechthoekdefinitie en JPEG‑exportopties.

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;
import com.aspose.psd.Rectangle;

import com.aspose.psd.imageoptions.JpegOptions;
```

## Stap 1: Stel je documentmap in

Geef de map op die het bron‑PSD‑bestand bevat. Vervang de tijdelijke aanduiding door het daadwerkelijke pad op jouw machine.

```java
String dataDir = "Your Document Directory";
```

## Stap 2: Specificeer bron‑ en bestemmingspaden

Definieer waar de PSD moet worden gelezen en waar de bijgesneden JPEG moet worden weggeschreven.

```java
String sourceFile = dataDir + "example1.psd";
String destName = dataDir + "jpeg_out.jpg";
```

## Stap 3: Laad en cache de afbeelding

Laad de PSD in een `RasterImage`‑object. Caching verbetert de prestaties voor daaropvolgende bewerkingen zoals bijsnijden.

```java
RasterImage rasterImage = (RasterImage)Image.load(sourceFile);
rasterImage.cacheData();
```

## Stap 4: Maak een rechthoek voor bijsnijden

Maak een `Rectangle` die het gebied beschrijft dat je wilt behouden. De coördinaten kunnen negatief zijn om het canvas te **uitbreiden** vóór het bijsnijden, wat handig is om een rand rond de originele afbeelding toe te voegen.

> **Waarom negatieve coördinaten gebruiken?**  
> Negatieve X/Y‑waarden verschuiven het bijsnijgebied naar links/omhoog, waardoor effectief lege ruimte (uitbreiding) rond de originele inhoud wordt toegevoegd vóór het uiteindelijke bijsnijden.

```java
Rectangle destRect = new Rectangle(-200, -200, 300, 300);
```

## Stap 5: Sla de bijgesneden afbeelding op

Sla tenslotte de resulterende afbeelding op met `JpegOptions`. Deze stap toont ook **convert psd jpeg** terwijl de bijsnijdrechthoek wordt toegepast.

```java
rasterImage.save(destName, new JpegOptions(), destRect);
```

> **Resultaat:** `jpeg_out.jpg` bevat nu een afbeelding van 300 × 300 pixel die aan elke kant met 200 px is uitgebreid en vervolgens is bijgesneden tot de gedefinieerde rechthoek.

Gefeliciteerd! Je hebt met succes **java image cropping** uitgevoerd, het canvas uitgebreid en een PSD‑bestand naar JPEG geconverteerd — allemaal in een paar beknopte code‑regels.

## Veelvoorkomende gebruikssituaties

- **Assets voorbereiden voor web** – bijsnijden en formaat wijzigen van screenshots of ontwerpen vóór upload.  
- **Thumbnails genereren** – een specifiek gebied uit een grote PSD extraheren voor preview‑doeleinden.  
- **Geautomatiseerde batchverwerking** – doorloop een map met PSD‑bestanden en pas dezelfde bijsnijdrechthoek op elk bestand toe.

## Probleemoplossing & tips

| Probleem | Aanbevolen oplossing |
|----------|----------------------|
| `OutOfMemoryError` bij het laden van grote PSD's | Roep `rasterImage.cacheData()` vroeg aan en overweeg het verhogen van de JVM-heapgrootte (`-Xmx`). |
| Bijsnijdgebied is niet gecentreerd | Controleer de X/Y‑offsets van de rechthoek; onthoud dat negatieve waarden het canvas uitbreiden. |
| Uitvoer‑JPEG is onscherp | Pas de kwaliteit van `JpegOptions` aan (bijv. `new JpegOptions { Quality = 90 }`). |

## Veelgestelde vragen

### Q1: Is Aspose.PSD compatibel met verschillende Java‑versies?

A1: Ja, Aspose.PSD ondersteunt verschillende Java‑versies, waardoor compatibiliteit met een breed scala aan ontwikkelomgevingen wordt gegarandeerd.

### Q2: Kan ik Aspose.PSD gebruiken voor commerciële projecten?

A2: Absoluut, Aspose.PSD biedt commerciële licenties voor ontwikkelaars, waardoor het zowel in persoonlijke als commerciële projecten kan worden gebruikt.

### Q3: Zijn er beperkingen op de ondersteunde afbeeldingsbestandsformaten?

A3: Aspose.PSD ondersteunt verschillende afbeeldingsbestandsformaten, waaronder PSD, JPEG, PNG en meer. Raadpleeg de [documentatie](https://reference.aspose.com/psd/java/) voor een volledige lijst.

### Q4: Hoe kan ik ondersteuning krijgen voor Aspose.PSD‑gerelateerde vragen?

A4: Bezoek het [Aspose.PSD‑forum](https://forum.aspose.com/c/psd/34) om hulp te zoeken bij de community of het Aspose‑ondersteuningsteam.

### Q5: Is er een gratis proefversie beschikbaar?

A5: Ja, je kunt Aspose.PSD uitproberen met een gratis proefversie. Download deze [hier](https://releases.aspose.com/).

---

**Laatst bijgewerkt:** 2026-01-07  
**Getest met:** Aspose.PSD for Java 24.12  
**Auteur:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}