---
date: 2026-08-01
description: Leer hoe je gamma kunt aanpassen in Java-afbeeldingsverwerking met Aspose.PSD,
  PSD naar TIFF kunt converteren en wasachtige afbeeldingen kunt herstellen in een
  beknopte tutorial.
keywords:
- how to adjust gamma
- fix washed out image
- java image processing
- convert psd to tiff
- server side image processing
lastmod: 2026-08-01
linktitle: Gamma van een afbeelding aanpassen
og_description: Leer hoe je gamma kunt aanpassen in Java-afbeeldingsverwerking met
  Aspose.PSD – een snelle, server‑side bibliotheek die wasachtige afbeeldingen corrigeert
  en PSD naar TIFF converteert in slechts een paar regels code.
og_image_alt: 'Guide: Adjust gamma in Java images with Aspose.PSD, convert PSD to
  TIFF'
og_title: hoe gamma aan te passen – Java-verwerking met Aspose.PSD
schemas:
- author: Aspose
  dateModified: '2026-08-01'
  description: Learn how to adjust gamma in Java image processing with Aspose.PSD,
    convert PSD to TIFF, and fix washed‑out images in a concise tutorial.
  headline: How to Adjust Gamma in Java Image Processing with Aspose.PSD
  type: TechArticle
- description: Learn how to adjust gamma in Java image processing with Aspose.PSD,
    convert PSD to TIFF, and fix washed‑out images in a concise tutorial.
  name: How to Adjust Gamma in Java Image Processing with Aspose.PSD
  steps:
  - name: '**Java Development Environment** – Java 8 or later installed.'
    text: '**Java Development Environment** – Java 8 or later installed.'
  - name: '**Aspose.PSD Library** – Download and add the JAR to your project. See
      the official [documentation](https://reference.aspose.com/psd/java/).'
    text: '**Aspose.PSD Library** – Download and add the JAR to your project. See
      the official [documentation](https://reference.aspose.com/psd/java/).'
  - name: '**Sample Image** – A PSD file you want to process (e.g., `sample.psd`).'
    text: '**Sample Image** – A PSD file you want to process (e.g., `sample.psd`).'
  type: HowTo
- questions:
  - answer: Yes – the `adjustGamma` method accepts separate float values for red,
      green, and blue channels.
    question: Can I apply different gamma values to each colour channel?
  - answer: Absolutely. You can perform resizing, cropping, or colour corrections
      sequentially on the same `RasterImage` instance.
    question: Is it possible to chain multiple image adjustments before saving?
  - answer: Yes, each layer can be accessed and processed individually.
    question: Does Aspose.PSD support multi‑page PSD files?
  - answer: Aspose.PSD supports PNG, JPEG, BMP, and many other formats via their respective
      options classes.
    question: What format can I export to besides TIFF?
  - answer: Start with a moderate gamma (around 2.0) and preview the result; adjust
      downwards if the image looks too bright.
    question: How do I avoid a washed‑out image after gamma correction?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- adjust gamma
- Aspose.PSD
- Java image processing
- PSD to TIFF
- server side processing
title: Hoe gamma aan te passen in Java-afbeeldingsverwerking met Aspose.PSD
url: /nl/java/advanced-techniques/adjust-gamma/
weight: 23
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Hoe gamma aan te passen in Java-afbeeldingsverwerking met Aspose.PSD

## Introductie

Als je werkt aan **java image processing**, is het leren **hoe gamma aan te passen** een fundamentele techniek om helderheid en contrast te verbeteren zonder details te verliezen. In deze tutorial lopen we stap voor stap door hoe je **Aspose.PSD for Java** kunt gebruiken om gamma‑correctie toe te passen op een PSD‑bestand, **PSD naar TIFF te converteren**, en een **wasachtig beeld** te vermijden. Je zult zien waarom deze aanpak snel, betrouwbaar en perfect is voor **server‑side image processing**‑pijplijnen.

## Snelle antwoorden
- **Wat doet gamma‑correctie?** Het herschikt luminantiewaarden om donkere gebieden lichter te maken of lichte gebieden donkerder, terwijl de algehele details behouden blijven.  
- **Welke bibliotheek verwerkt de bewerking?** Aspose.PSD for Java biedt een speciale `adjustGamma`‑methode voor rasterafbeeldingen.  
- **Kan ik PSD naar TIFF converteren in dezelfde workflow?** Ja – na gamma‑aanpassing kun je de afbeelding direct opslaan als TIFF met `TiffOptions`.  
- **Heb ik een licentie nodig voor ontwikkeling?** Een gratis proefversie werkt voor testen; een commerciële licentie is vereist voor productiegebruik.  
- **Welke Java‑versie wordt ondersteund?** Aspose.PSD ondersteunt Java 8 en hoger.

## Wat is Java Gamma-correctie?

Gamma‑correctie verandert de niet‑lineaire relatie tussen de gecodeerde pixelwaarden en de weergegeven helderheid. Door de gamma‑curve aan te passen kun je **wasachtig beeld**‑problemen oplossen of details in schaduwen verbeteren zonder highlights overbelichten. Het werkt door een machtswet‑functie toe te passen op elke pixel, die donkere tonen opheldert en highlights comprimeert, wat resulteert in een meer natuurlijke visuele weergave.

## Waarom Aspose.PSD gebruiken voor gamma‑correctie?

Aspose.PSD is een **java image processing library** die de complexiteit van het PSD‑formaat abstraheert. Het ondersteunt het verwerken van bestanden tot 2 GB, behandelt meer dan 50 verschillende afbeeldingsformaten, en biedt een eenvoudige `adjustGamma`‑aanroep, waardoor het ideaal is voor **java gamma correction** en **convert PSD to TIFF**‑workflows.

## Vereisten

1. **Java Development Environment** – Java 8 of later geïnstalleerd.  
2. **Aspose.PSD Library** – Download en voeg de JAR toe aan je project. Zie de officiële [documentation](https://reference.aspose.com/psd/java/).  
3. **Sample Image** – Een PSD‑bestand dat je wilt verwerken (bijv. `sample.psd`).  

## Pakketten importeren

Voordat je begint, importeer je de essentiële namespaces die je toegang geven tot rasterverwerking en bestandsformaatopties.

## Stap 1: Laad de afbeelding

De `RasterImage`‑klasse vertegenwoordigt de gerasterde pixelgegevens van een PSD‑laag in het geheugen. Het één keer laden en cachen van de afbeelding vermindert geheugenbelasting voor daaropvolgende aanpassingen.

## Stap 2: Gamma aanpassen

Laad je PSD met `new RasterImage("sample.psd")` en roep `rasterImage.adjustGamma(2.0f)` aan — die ene regel past een gamma van 2.0 toe op alle kleurkanalen, waardoor schaduwen worden opgehelderd terwijl highlights intact blijven. Je kunt afzonderlijke waarden voor rood, groen en blauw doorgeven als kanaalspecifieke aanpassingen nodig zijn.

## Stap 3: TiffOptions maken

`TiffOptions` stelt je in staat compressie, bits per sample en andere TIFF‑specifieke instellingen te regelen. Het instellen van een 8‑bit sample (`{8,8,8}`) houdt de TIFF‑bestandsgrootte redelijk terwijl de kleurnauwkeurigheid behouden blijft.

## Stap 4: Sla de resulterende afbeelding op

Roep `rasterImage.save("output.tif", tiffOptions)` aan om de verwerkte afbeelding naar schijf te schrijven. Na het opslaan kun je de TIFF invoeren in downstream‑systemen zoals printservices of web‑API's.

## Veelvoorkomende gebruikssituaties

- **Automated graphics pipelines** – Pas gamma on‑the‑fly aan voordat miniaturen worden gegenereerd.  
- **Batch conversion tools** – Converteer grote PSD‑archieven naar TIFF terwijl de helderheid genormaliseerd wordt.  
- **Web services** – Maak een endpoint beschikbaar dat een PSD ontvangt, gamma‑correctie toepast en een TIFF teruggeeft voor gebruik door de client.

## Veelvoorkomende problemen en oplossingen

| Probleem | Waarom het gebeurt | Hoe op te lossen |
|----------|--------------------|------------------|
| **Afbeelding ziet er wasachtig uit** | Gamma‑waarde te hoog (bijv. > 2.5) | Verlaag de gamma‑factor naar een waarde tussen 1.8 en 2.2. |
| **`rasterImage.isCached()` geeft false terug** | Afbeelding nog niet in het geheugen geladen | Roep `rasterImage.cacheData()` aan vóór het aanpassen van gamma. |
| **TIFF‑bestandsgrootte is groot** | Bits per sample ingesteld op 16‑bit | Gebruik een 8‑bit sample (`{8,8,8}`) zoals in het voorbeeld. |

## Veelgestelde vragen

**Q: Kan ik verschillende gamma‑waarden toepassen op elk kleurkanaal?**  
A: Ja – de `adjustGamma`‑methode accepteert afzonderlijke float‑waarden voor rode, groene en blauwe kanalen.

**Q: Is het mogelijk meerdere afbeeldingsaanpassingen te ketenen vóór het opslaan?**  
A: Absoluut. Je kunt resizing, cropping of kleurcorrecties opeenvolgend uitvoeren op dezelfde `RasterImage`‑instantie.

**Q: Ondersteunt Aspose.PSD multi‑page PSD‑bestanden?**  
A: Ja, elke laag kan afzonderlijk worden benaderd en verwerkt.

**Q: Naar welk formaat kan ik exporteren naast TIFF?**  
A: Aspose.PSD ondersteunt PNG, JPEG, BMP en vele andere formaten via hun respectieve options‑klassen.

**Q: Hoe voorkom ik een wasachtig beeld na gamma‑correctie?**  
A: Begin met een gematigde gamma (rond 2.0) en bekijk het resultaat; verlaag de gamma indien de afbeelding te helder lijkt.

## Conclusie

Gefeliciteerd! Je hebt met succes **hoe gamma aan te passen** geleerd in een **java image processing**‑workflow, een PSD naar TIFF geconverteerd, en veelvoorkomende valkuilen zoals een **wasachtig beeld** vermeden. Dit patroon geeft je fijnmazige controle over helderheid en contrast, waardoor het ideaal is voor geautomatiseerde grafische pijplijnen, webservices of desktop‑hulpmiddelen.

---

**Last Updated:** 2026-08-01  
**Tested With:** Aspose.PSD 24.11 for Java  
**Author:** Aspose  

{{< blocks/products/products-backtop-button >}}

## Gerelateerde tutorials

- [Java Image Processing Tutorial - Helderheid van een afbeelding aanpassen met Aspose.PSD for Java](/psd/java/advanced-techniques/adjust-brightness/)
- [Hoe PSD naar TIFF te converteren en contrast aan te passen met Aspose.PSD for Java](/psd/java/advanced-techniques/adjust-contrast/)
- [PSD naar afbeelding converteren in Java – Aanpassingslagen toepassen met Aspose.PSD](/psd/java/advanced-psd-layer-features-effects/apply-adjustment-layers-psd-files/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.psd.fileformats.tiff.enums.TiffPhotometrics;
import com.aspose.psd.imageoptions.TiffOptions;
```

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

// Load an existing image into an instance of RasterImage class
Image image = Image.load(sourceFile);

// Cast object of Image to RasterImage
RasterImage rasterImage = (RasterImage)image;

// Check if RasterImage is cached for better performance
if (!rasterImage.isCached()) {
    rasterImage.cacheData();
}
```

```java
// Adjust the gamma
rasterImage.adjustGamma(2.2f, 2.2f, 2.2f);
```

```java
// Create an instance of TiffOptions for the resultant image
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
int[] ushort = { 8, 8, 8 };
tiffOptions.setBitsPerSample(ushort);
tiffOptions.setPhotometric(TiffPhotometrics.Rgb);
```

```java
// Save the resultant image to TIFF format
String destName = dataDir + "AdjustGamma_out.tiff";
rasterImage.save(destName, tiffOptions);
```