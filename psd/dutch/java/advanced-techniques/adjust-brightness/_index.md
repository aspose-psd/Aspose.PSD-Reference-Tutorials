---
date: 2026-09-28
description: Java-afbeeldingsverwerkingstutorial laat zien hoe je de helderheid van
  een afbeelding aanpast met Aspose.PSD voor Java. Volg stap‑voor‑stap code om PSD-
  of TIFF‑bestanden te laden, te wijzigen en op te slaan.
keywords:
- java image processing
- aspose psd java
- java image manipulation
- adjust brightness java
lastmod: 2026-09-28
linktitle: Helderheid van een afbeelding aanpassen
og_description: Java-afbeeldingsverwerkingstutorial laat zien hoe je de helderheid
  van een afbeelding aanpast met Aspose.PSD voor Java. Volg stap‑voor‑stap code om
  PSD- of TIFF‑bestanden te laden, te wijzigen en op te slaan.
og_image_alt: Guide to adjusting image brightness in Java using Aspose.PSD
og_title: 'Java-afbeeldingsverwerking: helderheid aanpassen met Aspose.PSD'
schemas:
- author: Aspose
  dateModified: '2026-09-28'
  description: Java image processing tutorial shows how to adjust brightness of an
    image using Aspose.PSD for Java. Follow step‑by‑step code to load, modify, and
    save PSD or TIFF files.
  headline: 'Java image processing: adjust brightness with Aspose.PSD'
  type: TechArticle
- description: Java image processing tutorial shows how to adjust brightness of an
    image using Aspose.PSD for Java. Follow step‑by‑step code to load, modify, and
    save PSD or TIFF files.
  name: 'Java image processing: adjust brightness with Aspose.PSD'
  steps:
  - name: Load the image
    text: The `RasterImage` class represents a rasterized version of a PSD or TIFF
      file in memory. It provides direct pixel access for color‑correction operations.
      In this step, we load the target image and cast it to a `RasterImage` for further
      processing.
  - name: Adjust brightness
    text: '`adjustBrightness(int value)` changes the lightness of every pixel by the
      specified integer value. Positive numbers brighten the image; negative numbers
      darken it. The method processes the image in‑place, so no additional object
      creation is required. Here, we use the `adjustBrightness` method to mod'
  - name: Set TiffOptions
    text: '`TiffOptions` specifies the encoding parameters for TIFF output, such as
      bits per sample and photometric interpretation. It lets you control how the
      resulting file is encoded. Configure the `TiffOptions` for saving the adjusted
      image. Adjust the `bitsPerSample` and `photometric` properties based on '
  - name: Save the resultant image
    text: Calling `save` writes the processed raster data to a file using the previously
      defined options. The operation is atomic and guarantees that the output file
      is a valid TIFF image. Finally, save the modified image using the specified
      `TiffOptions`.
  type: HowTo
- questions:
  - answer: Yes, Aspose.PSD for Java supports JPEG, PNG, BMP, GIF, and many other
      raster formats in addition to PSD and TIFF.
    question: Can I adjust brightness in other image formats besides PSD?
  - answer: Wrap the processing code in a try‑catch block and catch `IOException`
      or `ImageProcessingException` to manage file‑access and raster‑operation errors.
    question: How can I handle errors during the image adjustment process?
  - answer: The method accepts integer values from –255 to +255; values outside this
      range are clamped to the nearest limit.
    question: Is there a limit to the range of brightness adjustment?
  - answer: Yes, a commercial license is required for production use. Purchase a license
      [here](https://purchase.aspose.com/buy).
    question: Can I use Aspose.PSD for Java in commercial projects?
  - answer: Yes, you can explore the library with a free trial from [here](https://releases.aspose.com/).
    question: Is there a free trial available?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- java image processing
- aspose psd
- java image manipulation
title: 'Java-afbeeldingsverwerking: helderheid aanpassen met Aspose.PSD'
url: /nl/java/advanced-techniques/adjust-brightness/
weight: 21
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Helderheid van een afbeelding aanpassen met Aspose.PSD voor Java

## Introductie

In deze **java image processing** tutorial leer je hoe je de helderheid van een afbeelding direct vanuit Java-code kunt aanpassen. Het aanpassen van de helderheid is een veelvoorkomende taak voor grafisch ontwerpers, fotografen en iedereen die beeldverwerkings‑pijplijnen bouwt. In deze **java image manipulation** gids lopen we het volledige werkproces door — het laden van een PSD/TIFF, het toepassen van een helderheidsverschuiving, en het opslaan van het resultaat — met behulp van de Aspose.PSD for Java bibliotheek.

## Snelle antwoorden
- **Welke bibliotheek regelt helderheid?** Aspose.PSD for Java.  
- **Welke methode wijzigt de helderheid?** `RasterImage.adjustBrightness()`.  
- **Kan ik werken met PSD- en TIFF‑bestanden?** Ja, de API ondersteunt beide formaten en meer dan 10 extra afbeeldingsformaten.  
- **Heb ik een licentie nodig voor productie?** Een commerciële licentie is vereist voor niet‑evaluatiegebruik.  
- **Hoe lang duurt de implementatie?** Meestal minder dan 10 minuten voor een eenvoudige aanpassing.

## Wat is java image processing?

`Java image processing` verwijst naar de reeks technieken waarmee je programmatisch beeldgegevens kunt lezen, transformeren en schrijven met Java. Het aanpassen van de helderheid is een van de kernbewerkingen die de algehele lichtheid van elke pixel verandert, waardoor donkere gebieden lichter of heldere gebieden donkerder worden.

## Waarom Aspose.PSD voor Java gebruiken?

Aspose.PSD for Java biedt een uitgebreide, pure‑Java oplossing die een breed scala aan raster‑ en vectorformaten ondersteunt, native afhankelijkheden elimineert en high‑performance caching biedt voor grote bestanden. De uitgebreide API stelt ontwikkelaars in staat complexe kleuraanpassingen en laag‑gebaseerde bewerkingen uit te voeren met minimale code, waardoor het ideaal is voor zowel eenvoudige aanpassingen als geavanceerde beeldverwerkings‑pijplijnen.

- **Ondersteunt meer dan 10 raster‑ en vectorformaten** – PSD, TIFF, JPEG, PNG, BMP, GIF, en meer.  
- **Pure‑Java implementatie** – geen native DLL's of externe afhankelijkheden, dus werkt op elke JVM.  
- **High‑performance caching** – rastergegevens kunnen worden gecached, waardoor herhaalde bewerkingen op grote bestanden tot 2× sneller kunnen zijn.  
- **Rijke API** – meer dan 150 methoden voor kleuraanpassing, laagbeheer, maskers en compositie.

## Vereisten

Voordat je aan de tutorial begint, zorg ervoor dat je de volgende vereisten hebt:

- Aspose.PSD for Java Bibliotheek: Download en installeer de bibliotheek vanaf de [Aspose.PSD for Java documentatie](https://reference.aspose.com/psd/java/).  
- Java Development Kit (JDK) 8 of hoger geïnstalleerd op je machine.  
- Een ontwikkelomgeving (IDE) zoals IntelliJ IDEA, Eclipse, of VS Code.

## Pakketten importeren

Om te beginnen, importeer je de benodigde pakketten in je Java‑project. In dit voorbeeld gebruiken we het volgende:

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.psd.fileformats.tiff.enums.TiffPhotometrics;
import com.aspose.psd.imageoptions.TiffOptions;
```

Laten we nu het proces van het aanpassen van de helderheid van een afbeelding in eenvoudige stappen opsplitsen:

## Hoe helderheid aanpassen met Aspose.PSD?

Laad je bronafbeelding, pas een helderheidsverschuiving toe, configureer de opslaan‑opties, en schrijf het resultaat naar schijf — alles in vier beknopte stappen. De volgende secties bieden een duidelijke, stap‑voor‑stap walkthrough die je kunt kopiëren naar je eigen project. Deze aanpak zorgt ervoor dat elke bewerking efficiënt wordt uitgevoerd en dat de uiteindelijke afbeelding de oorspronkelijke kwaliteit behoudt terwijl de gewenste helderheidsverandering wordt weergegeven.

### Stap 1: Afbeelding laden

De `RasterImage`‑klasse vertegenwoordigt een gerasterde versie van een PSD‑ of TIFF‑bestand in het geheugen. Het biedt directe pixeltoegang voor kleuraanpassingsbewerkingen.

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

### Stap 2: Helderheid aanpassen

`adjustBrightness(int value)` verandert de lichtheid van elke pixel met de opgegeven gehele waarde. Positieve getallen maken de afbeelding lichter; negatieve getallen maken deze donkerder. De methode verwerkt de afbeelding in‑place, dus er is geen extra objectcreatie nodig.

```java
// Adjust the brightness
rasterImage.adjustBrightness(-50);
```

Hier gebruiken we de `adjustBrightness`‑methode om de helderheid van de afbeelding te wijzigen. In dit voorbeeld verlagen we de helderheid met 50 eenheden, maar je kunt deze waarde aanpassen op basis van je vereisten.

### Stap 3: TiffOptions instellen

`TiffOptions` specificeert de coderingsparameters voor TIFF‑output, zoals bits per sample en fotometrische interpretatie. Het stelt je in staat te bepalen hoe het resulterende bestand wordt gecodeerd.

```java
int[] ushort = {8, 8, 8};
// Create an instance of TiffOptions for the resultant image
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
tiffOptions.setBitsPerSample(ushort);
tiffOptions.setPhotometric(TiffPhotometrics.Rgb);
```

Configureer de `TiffOptions` voor het opslaan van de aangepaste afbeelding. Pas de `bitsPerSample`‑ en `photometric`‑eigenschappen aan op basis van je specifieke behoeften.

### Stap 4: Het resulterende beeld opslaan

Het aanroepen van `save` schrijft de verwerkte rastergegevens naar een bestand met behulp van de eerder gedefinieerde opties. De bewerking is atomair en garandeert dat het uitvoerbestand een geldige TIFF‑afbeelding is.

```java
// Save the resultant image
rasterImage.save(destName, tiffOptions);
```

Sla tenslotte de gewijzigde afbeelding op met de opgegeven `TiffOptions`.

## Veelvoorkomende problemen en oplossingen

| Probleem | Reden | Oplossing |
|----------|-------|-----------|
| **`ClassCastException` bij casten van Image** | Het bestand is geen rasterafbeelding (bijv. een vector‑PSD). | Controleer het bronbestandformaat of gebruik `image instanceof RasterImage` vóór het casten. |
| **Helderheidsverandering heeft geen effect** | De afbeelding was niet gecached vóór aanpassing. | Roep `rasterImage.cacheData()` aan zoals getoond in Stap 1. |
| **Opgeslagen bestand lijkt beschadigd** | Onjuiste `TiffOptions`‑configuratie. | Zorg ervoor dat `bitsPerSample` overeenkomt met de diepte van de bronafbeelding (meestal 8‑bit per kanaal). |

## Veelgestelde vragen

**Q: Kan ik de helderheid aanpassen in andere afbeeldingsformaten dan PSD?**  
A: Ja, Aspose.PSD for Java ondersteunt JPEG, PNG, BMP, GIF en vele andere rasterformaten naast PSD en TIFF.

**Q: Hoe kan ik fouten afhandelen tijdens het aanpassen van de afbeelding?**  
A: Plaats de verwerkingscode in een try‑catch‑blok en vang `IOException` of `ImageProcessingException` om fouten bij bestands‑toegang en raster‑bewerkingen te beheren.

**Q: Is er een limiet aan het bereik van de helderheidsaanpassing?**  
A: De methode accepteert gehele waarden van –255 tot +255; waarden buiten dit bereik worden begrensd tot de dichtstbijzijnde limiet.

**Q: Kan ik Aspose.PSD for Java gebruiken in commerciële projecten?**  
A: Ja, een commerciële licentie is vereist voor productiegebruik. Koop een licentie [hier](https://purchase.aspose.com/buy).

**Q: Is er een gratis proefversie beschikbaar?**  
A: Ja, je kunt de bibliotheek verkennen met een gratis proefversie via [hier](https://releases.aspose.com/).

**Q: Heeft de `adjustBrightness`‑methode invloed op de zichtbaarheid van lagen?**  
A: De methode werkt op de gerasterde samengestelde afbeelding, dus verborgen lagen worden genegeerd tijdens rasterisatie, waardoor het beoogde visuele resultaat behouden blijft.

**Q: Kan ik meerdere aanpassingen (bijv. contrast, verzadiging) achter elkaar uitvoeren?**  
A: Zeker. Na het aanpassen van de helderheid kun je `adjustContrast`, `adjustSaturation` of andere kleuraanpassingsmethoden aanroepen op dezelfde `RasterImage`‑instantie.

---

**Laatst bijgewerkt:** 2026-09-28  
**Getest met:** Aspose.PSD for Java 24.12 (latest op het moment van schrijven)  
**Auteur:** Aspose

## Gerelateerde tutorials

- [Afbeeldingsverwerking Java Bibliotheek: Laag inverteren met Aspose.PSD](/psd/java/advanced-image-manipulation/invert-adjustment-layer/)
- [Afbeelding converteren naar grijswaarden met Aspose.PSD voor Java](/psd/java/advanced-techniques/grayscale-image/)
- [Hoe een afbeelding draaien op een specifieke hoek met Aspose.PSD voor Java](/psd/java/advanced-image-manipulation/rotate-image-specific-angle/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}