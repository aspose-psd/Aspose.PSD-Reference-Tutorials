---
date: 2025-12-21
description: Leer hoe u het contrast van afbeeldingen kunt aanpassen met Aspose.PSD
  voor Java, een toonaangevende Java-afbeeldingsbewerkingsbibliotheek, en converteer
  PSD efficiënt naar TIFF.
linktitle: Adjust Contrast of an Image
second_title: Aspose.PSD Java API
title: Hoe het contrast van een afbeelding aanpassen met Aspose.PSD voor Java
url: /nl/java/advanced-techniques/adjust-contrast/
weight: 22
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Hoe het contrast van een afbeelding aan te passen met Aspose.PSD voor Java

## Introductie

Als je op zoek bent naar **hoe je contrast kunt aanpassen** in je Java‑projecten, ben je hier aan het juiste adres. Aspose.PSD voor Java is een krachtige **java‑afbeeldingsbewerkingsbibliotheek** die je in staat stelt beeld‑eigenschappen zoals contrast, helderheid en meer fijn af te stellen. In deze tutorial lopen we de exacte stappen door om het contrast van een PSD‑bestand te verhogen en vervolgens **PSD naar TIFF te converteren** voor vervolg‑werkstromen.

## Snelle antwoorden
- **Wat betekent “adjust contrast”?** Het verandert het verschil tussen de donkerste en helderste pixels, waardoor details beter zichtbaar worden.
- **Welke bibliotheek regelt dit?** Aspose.PSD voor Java – een volledig uitgeruste toolkit voor beeldverwerking.
- **Heb ik een licentie nodig?** Een tijdelijke licentie werkt voor testen; een volledige licentie is vereist voor productie.
- **Kan ik het resultaat opslaan als TIFF?** Ja, we gebruiken `TiffOptions` om de bewerkte afbeelding te exporteren.
- **Hoe lang duurt het om de code uit te voeren?** Meestal minder dan een seconde voor standaard‑grootte PSD‑bestanden.

## Wat is contrastaanpassing?
Contrastaanpassing wijzigt het tonale bereik van een afbeelding, waardoor het onderscheid tussen lichte en donkere gebieden wordt vergroot. Dit is vooral nuttig wanneer afbeeldingen vlak lijken na het scannen of bij het voorbereiden van graphics voor drukwerk.

## Waarom Aspose.PSD voor Java gebruiken?
- **Rijke formaatondersteuning** – open, bewerk en sla PSD, TIFF, PNG, JPEG en vele andere formaten op.
- **Hoge prestaties** – caching en raster‑beeldoptimalisaties verminderen het geheugenverbruik.
- **Eenvoudige API** – enkele‑methoden‑aanroepen zoals `adjustContrast` maken de code leesbaar.

## Vereisten

Voordat je begint, zorg dat je het volgende hebt:

- Basiskennis van Java‑programmeren.
- Aspose.PSD voor Java‑bibliotheek geïnstalleerd. Je kunt het downloaden [hier](https://releases.aspose.com/psd/java/).

## Import pakketten

Voeg de benodigde imports toe aan je Java‑klasse:

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

// Load an existing image into an instance of RasterImage class
Image image = Image.load(sourceFile);
```

We laden het bron‑PSD‑bestand (`sample.psd`) in een `Image`‑object, dat dient als toegangspunt voor alle verdere verwerking.

## Stap 2: Cast naar RasterImage en cache gegevens

```java
// Cast object of Image to RasterImage
RasterImage rasterImage = (RasterImage)image;

// Check if RasterImage is cached and Cache RasterImage for better performance
if (!rasterImage.isCached()) {
    rasterImage.cacheData();
}
```

Casting naar `RasterImage` geeft ons toegang tot pixel‑niveau bewerkingen. Caching verbetert de prestaties, vooral bij grote bestanden.

## Hoe contrast van een afbeelding aan te passen

```java
// Adjust the contrast
rasterImage.adjustContrast(50);
```

De `adjustContrast`‑methode neemt een geheel getal dat de procentuele wijziging aangeeft. In dit voorbeeld verhogen we het contrast met **50 %**.

## Converteer PSD naar TIFF met Aspose.PSD

```java
// Create an instance of TiffOptions for the resultant image
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
int[] ushort = { 8, 8, 8 };
tiffOptions.setBitsPerSample(ushort);
tiffOptions.setPhotometric(TiffPhotometrics.Rgb);

// Save the resultant image to TIFF format
String destName = dataDir + "AdjustContrast_out.tiff";
rasterImage.save(destName, tiffOptions);
```

Hier configureren we `TiffOptions` (bits per sample, fotometrische interpretatie) en schrijven we de contrast‑verbeterde afbeelding naar een TIFF‑bestand.

## Veelvoorkomende problemen en oplossingen
- **Afbeelding niet gecached:** Roep altijd `cacheData()` aan voor grote PSD‑bestanden om `OutOfMemoryError` te voorkomen.
- **Onverwachte kleurverschuiving:** Controleer of `setPhotometric` overeenkomt met je doel‑kleurenspace (RGB vs. CMYK).
- **Bestand niet gevonden:** Zorg ervoor dat `dataDir` naar de juiste map wijst en dat de bestandsnaam correct gespeld is.

## Veelgestelde vragen

### V1: Is Aspose.PSD compatibel met verschillende afbeeldingsformaten?
A1: Ja, Aspose.PSD ondersteunt verschillende afbeeldingsformaten, wat flexibiliteit biedt in je projecten.

### V2: Hoe kan ik een tijdelijke licentie voor Aspose.PSD verkrijgen?
A2: Je kunt een tijdelijke licentie krijgen [hier](https://purchase.aspose.com/temporary-license/).

### V3: Waar vind ik de Aspose.PSD documentatie?
A3: De documentatie is beschikbaar [hier](https://reference.aspose.com/psd/java/).

### V4: Welke ondersteuningsopties zijn beschikbaar voor Aspose.PSD?
A4: Voor ondersteuning kun je het [Aspose.PSD forum](https://forum.aspose.com/c/psd/34) bezoeken.

### V5: Kan ik Aspose.PSD kopen?
A5: Ja, je kunt Aspose.PSD kopen [hier](https://purchase.aspose.com/buy).

## Conclusie

Je weet nu **hoe je contrast kunt aanpassen** van een PSD‑afbeelding met Aspose.PSD voor Java en **hoe je PSD naar TIFF kunt converteren** voor verdere verwerking. Deze stappen geven je fijne controle over de beeldkwaliteit terwijl de code schoon en onderhoudbaar blijft. Voel je vrij om te experimenteren met andere beeld‑aanpassingsmethoden zoals `adjustBrightness` of `adjustGamma` om aan je specifieke behoeften te voldoen.

---

**Last Updated:** 2025-12-21  
**Tested With:** Aspose.PSD for Java 24.12  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}