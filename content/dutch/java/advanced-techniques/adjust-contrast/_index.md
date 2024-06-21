---
title: Pas het contrast van een afbeelding aan met Aspose.PSD voor Java
linktitle: Pas het contrast van een afbeelding aan
second_title: Aspose.PSD Java-API
description: Ontdek de wereld van beeldcontrastaanpassing in Java met Aspose.PSD. Volg onze stapsgewijze handleiding voor naadloze beeldmanipulatie.
type: docs
weight: 22
url: /nl/java/advanced-techniques/adjust-contrast/
---
## Invoering

Op het gebied van beeldverwerking met Java onderscheidt Aspose.PSD zich als een krachtig hulpmiddel. Onder de talloze functies is het aanpassen van het beeldcontrast een veel voorkomende vereiste. Deze tutorial begeleidt u bij het aanpassen van het beeldcontrast met Aspose.PSD voor Java. Of u nu een doorgewinterde ontwikkelaar bent of net begint, deze handleiding helpt u dit essentiële aspect van beeldmanipulatie onder de knie te krijgen.

## Vereisten

Voordat u in de zelfstudie duikt, moet u ervoor zorgen dat u aan de volgende vereisten voldoet:

- Basiskennis van Java-programmeren.
-  Aspose.PSD voor Java-bibliotheek geïnstalleerd. Je kunt het downloaden[hier](https://releases.aspose.com/psd/java/).

## Pakketten importeren

Om aan de slag te gaan, moet u de benodigde pakketten in uw Java-project importeren. Voeg de volgende regels toe aan uw code:

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.psd.fileformats.tiff.enums.TiffPhotometrics;
import com.aspose.psd.imageoptions.TiffOptions;
```

## Stap 1: Laad de afbeelding

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

// Laad een bestaande afbeelding in een exemplaar van de RasterImage-klasse
Image image = Image.load(sourceFile);
```

 In deze stap laden we de voorbeeldafbeelding ("sample.psd") met behulp van de`Image.load` methode.

## Stap 2: Casten naar RasterImage en cachegegevens

```java
// Object van afbeelding naar RasterImage casten
RasterImage rasterImage = (RasterImage)image;

// Controleer of RasterImage in de cache is opgeslagen en cache RasterImage voor betere prestaties
if (!rasterImage.isCached()) {
    rasterImage.cacheData();
}
```

 Hier casten we de generieke`Image` bezwaar maken tegen een`RasterImage` voor specifieke verwerking. Het cachen van de afbeeldingsgegevens verbetert de prestaties.

## Stap 3: Pas het contrast aan

```java
// Pas het contrast aan
rasterImage.adjustContrast(50);
```

 De`adjustContrast`Deze methode wordt gebruikt om het contrast van de afbeelding te wijzigen. In dit voorbeeld wordt het contrast met 50% verhoogd.

## Stap 4: Maak TiffOptions en sla op

```java
// Maak een exemplaar van TiffOptions voor de resulterende afbeelding
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
int[] ushort = { 8, 8, 8 };
tiffOptions.setBitsPerSample(ushort);
tiffOptions.setPhotometric(TiffPhotometrics.Rgb);

// Sla de resulterende afbeelding op in TIFF-formaat
String destName = dataDir + "AdjustContrast_out.tiff";
rasterImage.save(destName, tiffOptions);
```

 Hier hebben we ons geïnstalleerd`TiffOptions` voor de uitvoerafbeelding, waarbij het formaat en andere eigenschappen worden gespecificeerd. De uiteindelijke afbeelding wordt vervolgens opgeslagen in een TIFF-bestand.

## Conclusie

Gefeliciteerd! U hebt het contrast van een afbeelding met succes aangepast met Aspose.PSD voor Java. In deze tutorial werden de essentiële stappen behandeld, van het importeren van pakketten tot het opslaan van de verwerkte afbeelding.

## Veelgestelde vragen

### Vraag 1: Is Aspose.PSD compatibel met verschillende afbeeldingsformaten?

A1: Ja, Aspose.PSD ondersteunt verschillende afbeeldingsformaten, wat flexibiliteit in uw projecten biedt.

### Vraag 2: Hoe kan ik een tijdelijke licentie voor Aspose.PSD verkrijgen?

 A2: U kunt een tijdelijke licentie krijgen.[hier](https://purchase.aspose.com/temporary-license/).

### V3: Waar kan ik Aspose.PSD-documentatie vinden?

A3: De documentatie is beschikbaar.[hier](https://reference.aspose.com/psd/java/).

### V4: Welke ondersteuningsopties zijn beschikbaar voor Aspose.PSD?

 A4: Bezoek voor ondersteuning de[Aspose.PSD-forum](https://forum.aspose.com/c/psd/34).

### Vraag 5: Kan ik Aspose.PSD kopen?

 A5: Ja, u kunt Aspose.PSD kopen[hier](https://purchase.aspose.com/buy).