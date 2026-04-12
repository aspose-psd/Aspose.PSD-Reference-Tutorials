---
date: 2026-04-12
description: Leer hoe je een afbeelding in Java kunt verkleinen met de Bicubic Resampler
  van Aspose.PSD. Deze tutorial over beeldschaling laat stap voor stap zien hoe je
  superieure resultaten kunt behalen.
keywords:
- resize image java
- image scaling tutorial
- java image library
linktitle: Implementeer bicubische resampler
second_title: Aspose.PSD Java API
title: Afbeelding schalen in Java – Bicubische resampler voor hoogwaardige schaalvergroting
url: /nl/java/advanced-image-manipulation/implement-bicubic-resampler/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Afbeelding Grootte Aanpassen Java – Bicubic Resampler voor Schaalvergroting van Hoge Kwaliteit

## Inleiding

Als je **resize image java** projecten nodig hebt zonder scherpte te verliezen of artefacten te introduceren, ben je hier aan het juiste adres. In deze **image scaling tutorial** lopen we door het gebruik van Aspose.PSD’s Bicubic Resampler—een krachtige **java image library**‑functie die soepele, heldere resultaten levert voor PSD‑bestanden en vele andere formaten. Aan het einde van deze gids kun je hoogwaardige schaalvergroting integreren in elke Java‑applicatie met slechts een paar regels code.

## Snelle Antwoorden
- **Wat doet de Bicubic Resampler?** Het past een geavanceerd interpolatie‑algoritme toe dat details behoudt bij het wijzigen van de grootte van afbeeldingen.  
- **Welke ResizeType‑waarden zijn beschikbaar?** `CubicConvolution` en `Bell` zijn de twee Bicubic‑opties die door Aspose.PSD worden geleverd.  
- **Heb ik een licentie nodig om de code uit te voeren?** Een tijdelijke Aspose‑licentie werkt voor evaluatie; een volledige licentie is vereist voor productie.  
- **Welke Java‑versie is vereist?** Elke Java 8+ runtime is compatibel met de nieuwste Aspose.PSD‑bibliotheek.  
- **Kan ik andere formaten (PNG, JPEG) met dezelfde API schalen?** Ja, Aspose.PSD ondersteunt meerdere beeldtypen, hoewel de voorbeelden zich richten op PSD.

## Wat is Schaalvergroting van Hoge Kwaliteit?

Schaalvergroting van hoge kwaliteit verwijst naar het wijzigen van de grootte van een afbeelding terwijl scherpe randen, vloeiende kleurverlopen en nauwkeurige kleurweergave behouden blijven. De Bicubic Resampler bereikt dit door de waarden van omliggende pixels te overwegen (met cubic convolution of het Bell‑algoritme) om elke nieuwe pixel te berekenen, wat resulteert in een natuurlijker uiterlijk vergeleken met nearest‑neighbor‑ of bilineaire methoden.

## Waarom de Bicubic Resampler gebruiken voor Schaalvergroting van Hoge Kwaliteit?

- **Behoudt Details:** Fijne texturen en lijnwerk blijven duidelijk, zelfs na aanzienlijke grootte‑veranderingen.  
- **Vermindert Artefacten:** Minimaliseert ringing en vervaging die vaak optreden bij eenvoudigere algoritmen.  
- **Eenvoudige Integratie:** Eén‑regelige methode‑aanroep (`image.resize`) stelt je in staat om tussen algoritmen te schakelen zonder code te herschrijven.  

## Vereisten

Voordat je begint, zorg ervoor dat je het volgende hebt:

- **Aspose.PSD for Java** – download de nieuwste JAR van de [Aspose.PSD for Java documentation](https://reference.aspose.com/psd/java/).  
- **Java Development Kit** – JDK 8 of nieuwer geïnstalleerd en geconfigureerd.  
- **Voorbeeld PSD‑bestand** – een testafbeelding (bijv. `sample_bicubic.psd`) geplaatst in een bekende map.  

Deze items vormen samen een solide **java image library** basis voor de tutorial.

## Pakketten Importeren

Voeg de benodigde imports toe aan je Java‑klasse. Deze brengen de kern‑Aspose.PSD‑klassen en de `ResizeType`‑enumeratie binnen.

```java
import com.aspose.psd.Image;
import com.aspose.psd.ResizeType;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.PsdOptions;
```

## Hoe Afbeelding Grootte Aanpassen Java met Bicubic Resampler

### Stap 1: Laad de Afbeelding

Laad eerst het bron‑PSD‑bestand dat je wilt schalen. Vervang `Your Document Directory` door het daadwerkelijke pad op jouw machine.

```java
String dataDir = "Your Document Directory";
String filePath = dataDir + "sample_bicubic.psd";
PsdImage image = (PsdImage)Image.load(filePath);
```

### Stap 2: Schalen met Cubic Convolution (Hoge Kwaliteit)

Pas nu het **Cubic Convolution**‑algoritme toe, een van de twee Bicubic‑opties die hoogwaardige schaalvergroting levert. Het voorbeeld schaalt de afbeelding naar 300 × 300 pixels.

```java
String destNameCubicConvolution = dataDir + "ResamplerCubicConvolutionStripes_after.psd";
image.resize(300, 300, ResizeType.CubicConvolution);
image.save(destNameCubicConvolution, new PsdOptions(image));
```

### Stap 3: Schalen met Bell‑algoritme (Alternatieve Hoge Kwaliteit)

Als je de voorkeur geeft aan het **Bell**‑algoritme, dat een iets ander verzachtend effect biedt, kun je het op dezelfde manier gebruiken. Let op dat we de originele afbeelding opnieuw laden om de vergelijking eerlijk te houden.

```java
String destNameBell = dataDir + "ResamplerBellStripes_after.psd";
PsdImage imageBellStripes = (PsdImage)Image.load(filePath);
imageBellStripes.resize(300, 300, ResizeType.Bell);
imageBellStripes.save(destNameBell, new PsdOptions(imageBellStripes));
```

Voel je vrij om te experimenteren met andere afmetingen of bestandsformaten—pas de parameters gewoon dienovereenkomstig aan.

## Veelvoorkomende Valkuilen & Tips

- **Onjuist Pad:** Zorg ervoor dat `dataDir` eindigt met een bestands‑scheidingsteken (`/` of `\`) dat geschikt is voor jouw OS.  
- **Licentie‑Uitzonderingen:** Het uitvoeren zonder een geldige licentie kan een watermerk aan de uitvoerafbeelding toevoegen. Gebruik een **temporary aspose license** voor testen, schakel daarna over naar een permanente licentie voor productie.  
- **Geheugengebruik:** Grote PSD‑bestanden kunnen veel geheugen verbruiken; overweeg om afbeeldingen te verwijderen (`image.dispose()`) na het opslaan.  

## Veelgestelde Vragen

**Q: Kan ik Aspose.PSD for Java gebruiken met andere beeldformaten?**  
A: Ja, de bibliotheek ondersteunt PSD, PNG, JPEG, TIFF, BMP en nog veel meer.

**Q: Is er een tijdelijke licentie beschikbaar voor Aspose.PSD for Java?**  
A: Ja, je kunt een tijdelijke licentie verkrijgen via [here](https://purchase.aspose.com/temporary-license/).

**Q: Waar kan ik ondersteuning vinden voor Aspose.PSD for Java?**  
A: Bezoek het Aspose.PSD‑forum [here](https://forum.aspose.com/c/psd/34) voor vragen met betrekking tot ondersteuning.

**Q: Kan ik de Aspose.PSD for Java‑bibliotheek downloaden?**  
A: Ja, download de bibliotheek vanaf de releases‑pagina [here](https://releases.aspose.com/psd/java/).

**Q: Hoe koop ik Aspose.PSD for Java?**  
A: Je kunt Aspose.PSD for Java aanschaffen via de aankooppagina [here](https://purchase.aspose.com/buy).

---

**Laatst Bijgewerkt:** 2026-04-12  
**Getest Met:** Aspose.PSD for Java 24.11 (latest at time of writing)  
**Auteur:** Aspose

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}