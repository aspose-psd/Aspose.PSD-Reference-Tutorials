---
date: 2026-02-27
description: Leer hoe je gamma kunt aanpassen in Java‑beeldverwerking met Aspose.PSD,
  PSD naar TIFF kunt converteren en verbleekte afbeeldingen kunt herstellen in een
  beknopte tutorial.
linktitle: Adjust Gamma of an Image
second_title: Aspose.PSD Java API
title: Hoe gamma aan te passen in Java-beeldverwerking met Aspose.PSD
url: /nl/java/advanced-techniques/adjust-gamma/
weight: 23
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Hoe gamma aan te passen in Java-afbeeldingsverwerking met Aspose.PSD

## Introductie

Als je werkt aan **java image processing**, is het leren **how to adjust gamma** een fundamentele techniek om helderheid en contrast te verbeteren zonder detailverlies. In deze tutorial lopen we door hoe je **Aspose.PSD for Java** gebruikt om gamma-correctie toe te passen op een PSD‑bestand, **convert PSD to TIFF**, en een **washed‑out image** te vermijden. Je ziet waarom deze aanpak snel, betrouwbaar en perfect is voor server‑side image pipelines.

## Snelle antwoorden
- **Wat doet gamma-correctie?** Het herschikt luminantie‑waarden om donkere gebieden lichter te maken of lichte gebieden donkerder, terwijl het algemene detail behouden blijft.  
- **Welke bibliotheek verwerkt de bewerking?** Aspose.PSD for Java biedt een speciale `adjustGamma`‑methode voor raster‑afbeeldingen.  
- **Kan ik PSD naar TIFF converteren in dezelfde workflow?** Ja – na gamma‑aanpassing kun je de afbeelding direct opslaan als TIFF met `TiffOptions`.  
- **Heb ik een licentie nodig voor ontwikkeling?** Een gratis proefversie werkt voor testen; een commerciële licentie is vereist voor productiegebruik.  
- **Welke Java‑versie wordt ondersteund?** Aspose.PSD ondersteunt Java 8 en hoger.

## Hoe gamma aan te passen in Java-afbeeldingsverwerking
Gamma aanpassen is een kernonderdeel van elke **java image processing tutorial** die zich bezighoudt met helderheid of contrast. Hieronder splitsen we de stappen, leggen we uit waarom elke regel belangrijk is, en laten we zien hoe je het proces in je bestaande codebase kunt integreren.

## Wat is Java gamma-correctie?
Gamma‑correctie verandert de niet‑lineaire relatie tussen de gecodeerde pixelwaarden en de weergegeven helderheid. Door de gamma‑curve aan te passen kun je **fix washed out image** problemen oplossen of details in schaduwen verbeteren zonder highlights over‑exponeren.

## Waarom Aspose.PSD gebruiken voor gamma‑correctie?
Aspose.PSD fungeert als een krachtige **java image processing library** die de complexiteit van het PSD‑formaat abstraheert. Het behandelt kleurprofielen, caching, en biedt een eenvoudige `adjustGamma`‑aanroep, waardoor het ideaal is voor **java gamma correction** en **convert PSD to TIFF** workflows.

## Voorvereisten

1. **Java Development Environment** – Java 8 of later geïnstalleerd.  
2. **Aspose.PSD Library** – Download en voeg de JAR toe aan je project. Zie de officiële [documentation](https://reference.aspose.com/psd/java/).  
3. **Sample Image** – Een PSD‑bestand dat je wilt verwerken (bijv. `sample.psd`).  

## Importeer pakketten

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

// Cast object of Image to RasterImage
RasterImage rasterImage = (RasterImage)image;

// Check if RasterImage is cached for better performance
if (!rasterImage.isCached()) {
    rasterImage.cacheData();
}
```

**Pro tip:** Het cachen van de rastergegevens één keer vermindert geheugen‑schommelingen wanneer je meerdere aanpassingen achter elkaar toepast.

## Stap 2: Pas gamma aan

```java
// Adjust the gamma
rasterImage.adjustGamma(2.2f, 2.2f, 2.2f);
```

Je kunt verschillende waarden doorgeven voor de rode, groene en blauwe kanalen als je kanaalspecifieke aanpassingen nodig hebt.

## Stap 3: Maak TiffOptions

```java
// Create an instance of TiffOptions for the resultant image
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
int[] ushort = { 8, 8, 8 };
tiffOptions.setBitsPerSample(ushort);
tiffOptions.setPhotometric(TiffPhotometrics.Rgb);
```

Het instellen van een 8‑bit sample (`{8,8,8}`) houdt de TIFF‑bestandsgrootte redelijk terwijl de kleurnauwkeurigheid behouden blijft.

## Stap 4: Sla de resulterende afbeelding op

```java
// Save the resultant image to TIFF format
String destName = dataDir + "AdjustGamma_out.tiff";
rasterImage.save(destName, tiffOptions);
```

Na het opslaan kun je de TIFF invoeren in downstream‑systemen zoals printservices of web‑API's.

## Veelvoorkomende gebruikssituaties

- **Automated graphics pipelines** – Pas gamma dynamisch aan vóór het genereren van miniaturen.  
- **Batch conversion tools** – Converteer grote PSD‑archieven naar TIFF terwijl je de helderheid normaliseert.  
- **Web services** – Bied een endpoint aan dat een PSD ontvangt, gamma‑correctie toepast en een TIFF terugstuurt voor clientgebruik.

## Veelvoorkomende problemen en oplossingen

| Issue | Why it Happens | How to Fix |
|-------|----------------|------------|
| **Afbeelding lijkt washed out** | Gamma‑waarde te hoog (bijv. > 2.5) | Verlaag de gamma‑factor tot een waarde tussen 1.8 en 2.2. |
| **`rasterImage.isCached()` returns false** | Afbeelding nog niet in het geheugen geladen | Roep `rasterImage.cacheData()` aan vóór het aanpassen van gamma. |
| **TIFF‑bestandsgrootte is groot** | Bits per sample ingesteld op 16‑bit | Gebruik een 8‑bit sample (`{8,8,8}`) zoals in het voorbeeld. |

## Veelgestelde vragen

**Q: Kan ik verschillende gamma‑waarden toepassen op elk kleurkanaal?**  
A: Ja – de `adjustGamma`‑methode accepteert afzonderlijke float‑waarden voor rode, groene en blauwe kanalen.

**Q: Is het mogelijk om meerdere beeldaanpassingen te ketenen vóór het opslaan?**  
A: Absoluut. Je kunt resizing, cropping, of colour corrections opeenvolgend uitvoeren op dezelfde `RasterImage`‑instantie.

**Q: Ondersteunt Aspose.PSD multi‑page PSD‑bestanden?**  
A: Ja, elke laag kan afzonderlijk worden benaderd en verwerkt.

**Q: Naar welk formaat kan ik exporteren naast TIFF?**  
A: Aspose.PSD ondersteunt PNG, JPEG, BMP en vele andere formaten via hun respectieve options‑klassen.

**Q: Hoe voorkom ik een washed‑out image na gamma‑correctie?**  
A: Begin met een gematigde gamma (rond 2.0) en bekijk het resultaat; verlaag de waarde als de afbeelding te helder lijkt.

## Conclusie

Gefeliciteerd! Je hebt met succes **how to adjust gamma** geleerd in een **java image processing** workflow, een PSD naar TIFF geconverteerd, en veelvoorkomende valkuilen zoals een **washed‑out image** vermeden. Dit patroon geeft je fijnmazige controle over helderheid en contrast, waardoor het ideaal is voor geautomatiseerde graphics pipelines, webservices of desktop‑hulpmiddelen.

---

**Laatst bijgewerkt:** 2026-02-27  
**Getest met:** Aspose.PSD 24.11 for Java  
**Auteur:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}