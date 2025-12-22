---
date: 2025-12-19
description: Leer hoe je de helderheid van een afbeelding kunt aanpassen met Aspose.PSD
  voor Java. Deze Java‑afbeeldingsbewerkingshandleiding biedt een stapsgewijze gids.
linktitle: Adjust Brightness of an Image
second_title: Aspose.PSD Java API
title: Hoe de helderheid van een afbeelding aan te passen met Aspose.PSD voor Java
url: /nl/java/advanced-techniques/adjust-brightness/
weight: 21
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Helderheid van een afbeelding aanpassen met Aspose.PSD voor Java

## Inleiding

Als je **leert hoe je de helderheid** van een afbeelding direct vanuit Java-code kunt aanpassen, ben je hier aan het juiste adres. Het aanpassen van de helderheid is een veelvoorkomende taak voor grafisch ontwerpers, fotografen en iedereen die beeldverwerkings‑pijplijnen bouwt. In deze **java image manipulation tutorial** lopen we het volledige werkproces door — het laden van een PSD/TIFF, het toepassen van een helderheidsverschuiving, en het opslaan van het resultaat — met behulp van de Aspose.PSD for Java bibliotheek.

## Snelle antwoorden
- **Welke bibliotheek regelt helderheid?** Aspose.PSD for Java  
- **Welke methode wijzigt de helderheid?** `RasterImage.adjustBrightness()`  
- **Kan ik werken met PSD- en TIFF‑bestanden?** Ja, de API ondersteunt beide formaten.  
- **Heb ik een licentie nodig voor productie?** Een commerciële licentie is vereist voor niet‑evaluatiegebruik.  
- **Hoe lang duurt de implementatie?** Meestal minder dan 10 minuten voor een basisaanpassing.

## Wat is beeldhelderheidsaanpassing?

Beeldhelderheidsaanpassing verandert de algehele lichtheid van elke pixel in een afbeelding. Het verhogen van de helderheid maakt donkere gebieden lichter, terwijl het verlagen ervan de hele afbeelding donkerder maakt. Deze bewerking is nuttig voor het corrigeren van onderbelichte foto’s, het voorbereiden van assets voor druk, of het creëren van visuele effecten in toepassingen.

## Waarom Aspose.PSD voor Java gebruiken?

- **Volledige formaatondersteuning** – PSD, TIFF, JPEG, PNG, en meer.  
- **Geen externe native afhankelijkheden** – pure Java, eenvoudig te integreren.  
- **Hoge‑prestaties caching** – rastergegevens kunnen worden gecached voor snellere herhaalde bewerkingen.  
- **Rijke API** – methoden voor kleurcorrectie, lagen, maskers, en andere geavanceerde bewerkingen.

## Voorvereisten

Voordat je aan de tutorial begint, zorg ervoor dat je de volgende voorvereisten hebt:

- Aspose.PSD for Java Library: Download en installeer de bibliotheek vanaf de [Aspose.PSD for Java documentation](https://reference.aspose.com/psd/java/).

## Importeer pakketten

Om te beginnen, importeer je de benodigde pakketten in je Java‑project. In dit voorbeeld gebruiken we het volgende:

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.psd.fileformats.tiff.enums.TiffPhotometrics;
import com.aspose.psd.imageoptions.TiffOptions;
```

Laten we nu het proces van het aanpassen van de helderheid van een afbeelding in eenvoudige stappen opsplitsen:

## Hoe helderheid aanpassen met Aspose.PSD

### Stap 1: Laad de afbeelding

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";
String destName = dataDir + "AdjustBrightness_out.tiff";

// Load an existing image into an instance of RasterImage class
Image image = Image.load(sourceFile);
// Cast object of Image to RasterImage
RasterImage rasterImage = (RasterImage) image;

// Check if RasterImage is cached and Cache RasterImage for better performance
if (!rasterImage.isCached()) {
    rasterImage.cacheData();
}
```

In deze stap laden we de doelafbeelding en casten we deze naar een `RasterImage` voor verdere verwerking.

### Stap 2: Helderheid aanpassen

```java
// Adjust the brightness
rasterImage.adjustBrightness(-50);
```

Hier gebruiken we de `adjustBrightness`‑methode om de helderheid van de afbeelding te wijzigen. In dit voorbeeld verlagen we de helderheid met 50 eenheden, maar je kunt deze waarde aanpassen op basis van je vereisten.

### Stap 3: Stel TiffOptions in

```java
int[] ushort = {8, 8, 8};
// Create an instance of TiffOptions for the resultant image
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
tiffOptions.setBitsPerSample(ushort);
tiffOptions.setPhotometric(TiffPhotometrics.Rgb);
```

Configureer de `TiffOptions` voor het opslaan van de aangepaste afbeelding. Pas de `bitsPerSample`‑ en `photometric`‑eigenschappen aan op basis van je specifieke behoeften.

### Stap 4: Sla de resulterende afbeelding op

```java
// Save the resultant image
rasterImage.save(destName, tiffOptions);
```

Sla tenslotte de gewijzigde afbeelding op met de opgegeven `TiffOptions`.

## Veelvoorkomende problemen en oplossingen

| Probleem | Reden | Oplossing |
|----------|-------|-----------|
| **`ClassCastException` bij het casten van Image** | Het bestand is geen rasterafbeelding (bijv. een vector‑PSD). | Controleer het bronbestandformaat of gebruik `image instanceof RasterImage` vóór het casten. |
| **Helderheidsverandering heeft geen effect** | De afbeelding was niet gecached vóór de aanpassing. | Roep `rasterImage.cacheData()` aan zoals getoond in Stap 1. |
| **Opgeslagen bestand lijkt corrupt** | Onjuiste `TiffOptions`‑configuratie. | Zorg ervoor dat `bitsPerSample` overeenkomt met de diepte van de bronafbeelding (meestal 8‑bit per kanaal). |

## Veelgestelde vragen

### Q1: Kan ik de helderheid aanpassen in andere afbeeldingsformaten dan PSD?

A1: Ja, Aspose.PSD for Java ondersteunt verschillende afbeeldingsformaten zoals JPEG, PNG en TIFF.

### Q2: Hoe kan ik fouten afhandelen tijdens het afbeelding‑aanpassingsproces?

A2: Je kunt foutafhandeling implementeren met try‑catch‑blokken om eventuele uitzonderingen te beheren.

### Q3: Is er een limiet aan het bereik van helderheidsaanpassing?

A3: Het bereik van de aanpassing hangt af van de inhoud en het formaat van de afbeelding, maar Aspose.PSD biedt flexibiliteit in maatwerk.

### Q4: Kan ik Aspose.PSD for Java gebruiken in commerciële projecten?

A4: Ja, Aspose.PSD for Java is een commerciële bibliotheek, en je kunt een licentie verkrijgen via [here](https://purchase.aspose.com/buy).

### Q5: Is er een gratis proefversie beschikbaar voor Aspose.PSD for Java?

A5: Ja, je kunt de bibliotheek verkennen met een gratis proefversie via [here](https://releases.aspose.com/).

### Q6: Heeft de `adjustBrightness`‑methode invloed op de zichtbaarheid van lagen?

A6: De methode werkt op de gerasterde samengestelde afbeelding, dus de zichtbaarheid van lagen wordt gerespecteerd tijdens rasterisatie.

### Q7: Kan ik meerdere aanpassingen (bijv. contrast, verzadiging) achter elkaar uitvoeren?

A7: Absoluut. Na het aanpassen van de helderheid kun je `adjustContrast`, `adjustSaturation`, enz. aanroepen op dezelfde `RasterImage`‑instantie.

---

**Laatst bijgewerkt:** 2025-12-19  
**Getest met:** Aspose.PSD for Java 24.12 (latest at time of writing)  
**Auteur:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}