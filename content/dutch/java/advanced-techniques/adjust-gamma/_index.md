---
title: Pas het gamma van een afbeelding aan met Aspose.PSD voor Java
linktitle: Pas de gamma van een afbeelding aan
second_title: Aspose.PSD Java-API
description: Leer moeiteloos het beeldgamma aanpassen met Aspose.PSD voor Java. Volg onze stap-voor-stap handleiding voor een optimaal resultaat.
type: docs
weight: 23
url: /nl/java/advanced-techniques/adjust-gamma/
---
## Invoering

Op het gebied van beeldverwerking is het aanpassen van het gamma van een afbeelding een cruciale stap om de visuele aantrekkingskracht ervan te vergroten. Aspose.PSD voor Java biedt een krachtige oplossing voor Java-ontwikkelaars om moeiteloos beeldgamma te manipuleren. In deze zelfstudie onderzoeken we hoe u gamma kunt aanpassen met Aspose.PSD, waarbij we elke stap opsplitsen om een naadloze implementatie te garanderen.

## Vereisten

Voordat u in de zelfstudie duikt, moet u ervoor zorgen dat u aan de volgende vereisten voldoet:

1. Java-ontwikkelomgeving: Zorg ervoor dat er een Java-ontwikkelomgeving op uw systeem is geïnstalleerd.
2.  Aspose.PSD-bibliotheek: Download en integreer de Aspose.PSD-bibliotheek in uw Java-project. De benodigde hulpmiddelen vindt u in de[documentatie](https://reference.aspose.com/psd/java/).
3. Voorbeeldafbeelding: bereid een voorbeeld-PSD-afbeelding voor die u gaat gebruiken om de gamma-aanpassing toe te passen.

## Pakketten importeren

Om het proces te starten, importeert u de vereiste pakketten in uw Java-project. Dit vormt de basis voor een naadloos gebruik van Aspose.PSD-functionaliteiten.

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.psd.fileformats.tiff.enums.TiffPhotometrics;
import com.aspose.psd.imageoptions.TiffOptions;
```

## Stap 1: Laad de afbeelding

 Begin met het laden van de voorbeeld-PSD-afbeelding in een exemplaar van de`RasterImage` klas. Dit is de basis voor daaropvolgende gamma-aanpassingen.

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

// Laad een bestaande afbeelding in een exemplaar van de RasterImage-klasse
Image image = Image.load(sourceFile);

// Object van afbeelding naar RasterImage casten
RasterImage rasterImage = (RasterImage)image;

// Controleer of RasterImage in de cache is opgeslagen voor betere prestaties
if (!rasterImage.isCached()) {
    rasterImage.cacheData();
}
```

## Stap 2: Gamma aanpassen

 Pas nu het gamma van de geladen afbeelding aan met behulp van de`adjustGamma` methode. Verfijn de gammawaarden volgens uw vereisten.

```java
// Pas het gamma aan
rasterImage.adjustGamma(2.2f, 2.2f, 2.2f);
```

## Stap 3: Maak TiffOptions

 Maak een exemplaar van`TiffOptions` voor het resulterende beeld. Stel verschillende eigenschappen in, zoals bits per monster en fotometrische opties, om de uitvoer aan uw specificaties aan te passen.

```java
// Maak een exemplaar van TiffOptions voor de resulterende afbeelding
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
int[] ushort = { 8, 8, 8 };
tiffOptions.setBitsPerSample(ushort);
tiffOptions.setPhotometric(TiffPhotometrics.Rgb);
```

## Stap 4: Sla de resulterende afbeelding op

 Sla de gemanipuleerde afbeelding op in TIFF-formaat met behulp van het eerder gedefinieerde`TiffOptions`.

```java
// Sla de resulterende afbeelding op in TIFF-formaat
String destName = dataDir + "AdjustGamma_out.tiff";
rasterImage.save(destName, tiffOptions);
```

## Conclusie

Gefeliciteerd! U hebt het gamma van een afbeelding met succes aangepast met Aspose.PSD voor Java. Dit proces stelt ontwikkelaars in staat de beeldkwaliteit moeiteloos te verbeteren, wat bijdraagt aan een visueel aantrekkelijke gebruikerservaring.

## Veelgestelde vragen

### V1: Waar kan ik de Aspose.PSD-documentatie vinden?

 A1: U kunt de documentatie raadplegen op[https://reference.aspose.com/psd/java/](https://reference.aspose.com/psd/java/).

### Vraag 2: Hoe download ik Aspose.PSD voor Java?

 A2: Download de bibliotheek van[https://releases.aspose.com/psd/java/](https://releases.aspose.com/psd/java/).

### Vraag 3: Waar kan ik Aspose.PSD kopen?

 A3: Bezoek[https://purchase.aspose.com/buy](https://purchase.aspose.com/buy) om Aspose.PSD te kopen.

### Vraag 4: Is er een gratis proefversie beschikbaar?

 A4: Ja, u kunt een gratis proefperiode uitproberen op[https://releases.aspose.com/](https://releases.aspose.com/).

### V5: Waar kan ik ondersteuning zoeken voor Aspose.PSD?

 A5: Bezoek voor ondersteuning het Aspose.PSD-forum op[https://forum.aspose.com/c/psd/34](https://forum.aspose.com/c/psd/34).