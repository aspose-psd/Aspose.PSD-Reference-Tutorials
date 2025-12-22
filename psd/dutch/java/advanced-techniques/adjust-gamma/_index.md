---
date: 2025-12-21
description: Leer hoe je Java-beeldverwerking uitvoert door de gamma van een afbeelding
  aan te passen met Aspose.PSD. Stapsgewijze handleiding om PSD naar TIFF te converteren
  en gamma‑correctie toe te passen.
linktitle: Adjust Gamma of an Image
second_title: Aspose.PSD Java API
title: Java-afbeeldingsverwerking – Gamma aanpassen met Aspose.PSD
url: /nl/java/advanced-techniques/adjust-gamma/
weight: 23
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Java-afbeeldingsverwerking – Gamma aanpassen met Aspose.PSD

## Inleiding

Als je werkt aan **java image processing**, is het aanpassen van de gamma van een afbeelding een fundamentele techniek om helderheid en contrast te verbeteren zonder details te verliezen. In deze tutorial laten we zien hoe je **Aspose.PSD for Java** kunt gebruiken om gamma‑correctie toe te passen op een PSD‑bestand en vervolgens het resultaat te exporteren als een TIFF‑afbeelding. Je zult zien waarom deze aanpak snel, betrouwbaar en perfect is voor server‑side‑beeldpijplijnen.

## Snelle antwoorden
- **Wat doet gamma‑correctie?** Het herschikt luminantiewaarden om donkere gebieden helderder te maken of heldere gebieden donkerder, terwijl de algehele details behouden blijven.  
- **Welke bibliotheek verwerkt de bewerking?** Aspose.PSD for Java biedt een speciale `adjustGamma`‑methode voor rasterafbeeldingen.  
- **Kan ik PSD naar TIFF converteren in dezelfde workflow?** Ja – na gamma‑aanpassing kun je de afbeelding direct opslaan als TIFF met `TiffOptions`.  
- **Heb ik een licentie nodig voor ontwikkeling?** Een gratis proefversie werkt voor testen; een commerciële licentie is vereist voor productie.  
- **Welke Java‑versie wordt ondersteund?** Aspose.PSD ondersteunt Java 8 en hoger.

## Wat is java image processing?

Java image processing verwijst naar het manipuleren, analyseren en transformeren van visuele gegevens met behulp van Java‑bibliotheken. Taken omvatten schalen, filteren, kleuraanpassing en formaatconversie — alles wat geautomatiseerd kan worden in desktop‑ of webapplicaties.

## Waarom Aspose.PSD gebruiken voor gamma‑correctie?

Aspose.PSD biedt een high‑level API die de complexiteit van het PSD‑formaat abstraheert, zodat je je kunt concentreren op de daadwerkelijke beeldaanpassingen. Het behandelt caching, kleurprofielen en biedt een eenvoudige `adjustGamma`‑aanroep, waardoor het ideaal is voor **image gamma correction** en **convert psd to tiff** workflows.

## Vereisten

1. **Java‑ontwikkelomgeving** – Zorg ervoor dat je een Java‑ontwikkelomgeving op je systeem hebt geïnstalleerd.  
2. **Aspose.PSD‑bibliotheek** – Download en integreer de Aspose.PSD‑bibliotheek in je Java‑project. De benodigde bronnen vind je in de [documentation](https://reference.aspose.com/psd/java/).  
3. **Voorbeeldafbeelding** – Bereid een voorbeeld‑PSD‑afbeelding voor die je zult gebruiken om de gamma‑aanpassing toe te passen.

## Pakketten importeren

Om het proces te starten, importeer je de benodigde pakketten in je Java‑project. Dit legt de basis voor het naadloos gebruiken van Aspose.PSD‑functionaliteiten.

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.psd.fileformats.tiff.enums.TiffPhotometrics;
import com.aspose.psd.imageoptions.TiffOptions;
```

## Stap 1: Laad de afbeelding

Begin met het laden van de voorbeeld‑PSD‑afbeelding in een instantie van de `RasterImage`‑klasse. Dit vormt de basis voor de daaropvolgende gamma‑aanpassingen.

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

## Stap 2: Gamma aanpassen

Pas nu de gamma van de geladen afbeelding aan met de `adjustGamma`‑methode. Stel de gamma‑waarden nauwkeurig af volgens je vereisten.

```java
// Adjust the gamma
rasterImage.adjustGamma(2.2f, 2.2f, 2.2f);
```

## Stap 3: TiffOptions maken

Maak een instantie van `TiffOptions` voor de resulterende afbeelding. Stel verschillende eigenschappen in, zoals bits per sample en fotometrische opties, om de output aan te passen aan je specificaties.

```java
// Create an instance of TiffOptions for the resultant image
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
int[] ushort = { 8, 8, 8 };
tiffOptions.setBitsPerSample(ushort);
tiffOptions.setPhotometric(TiffPhotometrics.Rgb);
```

## Stap 4: Sla de resulterende afbeelding op

Sla de bewerkte afbeelding op in TIFF‑formaat met behulp van de eerder gedefinieerde `TiffOptions`.

```java
// Save the resultant image to TIFF format
String destName = dataDir + "AdjustGamma_out.tiff";
rasterImage.save(destName, tiffOptions);
```

## Veelvoorkomende problemen en oplossingen

| Probleem | Waarom het gebeurt | Hoe op te lossen |
|----------|--------------------|------------------|
| **Afbeelding ziet er vervaagd uit** | Gamma‑waarde te hoog (bijv. > 2.5) | Verlaag de gamma‑factor naar een waarde tussen 1.8 en 2.2. |
| **`rasterImage.isCached()` retourneert false** | Afbeelding nog niet in het geheugen geladen | Roep `rasterImage.cacheData()` aan vóór het aanpassen van gamma. |
| **TIFF‑bestandsgrootte is groot** | Bits per sample ingesteld op 16‑bit | Gebruik een 8‑bit sample (`{8,8,8}`) zoals in het voorbeeld. |

## Veelgestelde vragen

**V: Kan ik verschillende gamma‑waarden toepassen op elk kleurkanaal?**  
A: Ja – de `adjustGamma`‑methode accepteert afzonderlijke float‑waarden voor rood, groen en blauw.

**V: Is het mogelijk meerdere beeldaanpassingen te ketenen vóór het opslaan?**  
A: Absoluut. Je kunt schalen, bijsnijden of kleuraanpassingen opeenvolgend uitvoeren op dezelfde `RasterImage`‑instantie.

**V: Ondersteunt Aspose.PSD multi‑page PSD‑bestanden?**  
A: Ja, elke laag kan afzonderlijk worden benaderd en verwerkt.

**V: Naar welk formaat kan ik exporteren naast TIFF?**  
A: Aspose.PSD ondersteunt PNG, JPEG, BMP en vele andere formaten via hun respectieve opties‑klassen.

## Conclusie

Gefeliciteerd! Je hebt met succes **java image processing** uitgevoerd door de gamma van een PSD‑bestand aan te passen en deze te exporteren als een TIFF‑afbeelding met Aspose.PSD for Java. Deze workflow geeft je fijnmazige controle over helderheid en contrast van afbeeldingen, waardoor het ideaal is voor geautomatiseerde grafische pijplijnen, webservices of desktop‑hulpmiddelen.

---

**Laatst bijgewerkt:** 2025-12-21  
**Getest met:** Aspose.PSD 24.11 for Java  
**Auteur:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
