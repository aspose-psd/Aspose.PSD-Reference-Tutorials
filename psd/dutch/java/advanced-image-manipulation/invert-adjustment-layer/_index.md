---
date: 2026-04-22
description: Leer hoe je de Java‑bibliotheek voor beeldverwerking Aspose.PSD kunt
  gebruiken om meerdere aanpassingslagen toe te passen, waaronder de Invert‑aanpassingslaag,
  voor naadloze PSD‑manipulatie.
keywords:
- image processing java library
- how to add invert
- invert colors psd
- batch process psd images
- apply multiple adjustment layers
linktitle: Aanpassingslaag Inverteren
second_title: Aspose.PSD Java API
title: 'Afbeeldingsverwerking Java‑bibliotheek: Laag inverteren met Aspose.PSD'
url: /nl/java/advanced-image-manipulation/invert-adjustment-layer/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Invert Adjustment Layer in Aspose.PSD voor Java

## Inleiding

Als je op zoek bent naar een robuuste **image processing java library**, is Aspose.PSD for Java een van de meest veelzijdige opties op de markt. In deze tutorial laten we zien hoe je een **Invert Adjustment Layer** aan een PSD‑bestand kunt toevoegen, een techniek die je kunt combineren met andere aanpassingslagen om verfijnde visuele effecten te bereiken. Of je nu een batch‑verwerkingstool, een server‑side image service, of een enkele‑afbeeldingseditor bouwt, deze gids biedt je een duidelijke, stap‑voor‑stap route om het werk snel en betrouwbaar te voltooien.

## Snelle antwoorden
- **Wat doet de Invert Adjustment Layer?** Het keert alle kleurwaarden in het geselecteerde gebied om, waardoor een negatief‑beeld effect ontstaat (d.w.z. het **convert PSD to negative**).  
- **Welke bibliotheek biedt deze functie?** Aspose.PSD, een toonaangevende **image processing java library**.  
- **Kan ik het stapelen met andere aanpassingen?** Ja – je kunt **apply multiple adjustment layers** zoals Brightness/Contrast, Hue/Saturation, en meer.  
- **Heb ik een licentie nodig voor ontwikkeling?** Een gratis proefversie is beschikbaar; een licentie is vereist voor productiegebruik.  
- **Hoe lang duurt de implementatie?** Meestal minder dan 10 minuten voor een basisgeval.

## Wat is de Invert Adjustment Layer?

De Invert Adjustment Layer is een niet‑destructieve bewerking die de RGB‑waarden van elke pixel die het beïnvloedt omdraait. Omdat het bovenop de laagstapel zit, kun je de zichtbaarheid ervan in- of uitschakelen of de volgorde wijzigen zonder de oorspronkelijke afbeeldingsgegevens permanent te wijzigen. Dit is de gemakkelijkste manier om **invert colors PSD** bestanden te inverteren of een fotografisch negatief te creëren.

## Waarom Aspose.PSD gebruiken als uw Image Processing Java Library?

- **Full PSD support** – lees, bewerk en schrijf Photoshop‑bestanden zonder Photoshop geïnstalleerd te hebben.  
- **Cross‑platform** – werkt op elke Java‑runtime (Java 6+).  
- **Rich adjustment features** – bevat ingebouwde methoden voor veelvoorkomende bewerkingen, waardoor het eenvoudig is om **apply multiple adjustment layers** in één workflow toe te passen.  
- **Performance‑optimized** – verwerkt grote bestanden efficiënt, wat essentieel is voor **batch process psd images**.  

## Vereisten

Voordat je begint, zorg ervoor dat je het volgende hebt:

1. **Aspose.PSD Library** – download deze van de officiële site [here](https://releases.aspose.com/psd/java/).  
2. **Java Development Environment** – JDK 6.0 of later geïnstalleerd en geconfigureerd.  

Laten we nu in de code duiken.

## Pakketten importeren

Begin met het importeren van de benodigde klassen. Deze imports geven je toegang tot de kern‑image‑handling API's en de PSD‑specifieke functionaliteit.

```java
import com.aspose.psd.Image;

import com.aspose.psd.fileformats.psd.PsdImage;
```

## Stap 1: Documentmap instellen

Definieer de map die je bron‑PSD‑bestand bevat en waar de uitvoer wordt opgeslagen.

```java
String dataDir = "Your Document Directory";
```

## Stap 2: PSD‑bestand laden

Laad het bronbestand in een `PsdImage`‑object. Dit object vertegenwoordigt het volledige PSD‑document in het geheugen.

```java
String filePath = dataDir + "InvertStripes_before.psd";
String outputPath = dataDir + "InvertStripes_after.psd";

PsdImage im = (PsdImage)Image.load(filePath);
```

## Stap 3: Invert Adjustment Layer toevoegen

Roep de ingebouwde methode aan om een Invert Adjustment Layer bovenop de huidige laagstapel in te voegen. Je kunt later meer lagen toevoegen (bijv. Brightness, Hue) om **apply multiple adjustment layers**.

```java
im.addInvertAdjustmentLayer();
```

## Stap 4: Uitvoer opslaan

Sla de gewijzigde PSD op schijf op. Het opgeslagen bestand bevat nu de Invert Adjustment Layer en kan geopend worden in Photoshop of elke PSD‑compatibele viewer.

```java
im.save(outputPath);
```

### Wat is er net gebeurd?

- De PSD is in het geheugen geladen.  
- Er is een Invert Adjustment Layer toegevoegd als bovenste laag.  
- De afbeelding is opgeslagen, waarbij de niet‑destructieve bewerking behouden blijft.

Je hebt nu met succes Aspose.PSD, een **image processing java library**, gebruikt om een PSD‑bestand te manipuleren.

## Batchverwerking van PSD‑afbeeldingen met invert‑aanpassing

Als je hetzelfde invert‑effect op tientallen of honderden bestanden wilt toepassen, kun je de bovenstaande code in een eenvoudige lus plaatsen die over een map met PSD‑bestanden itereren. Omdat de bibliotheek **performance‑optimized** is, blijft het verwerken van grote batches snel, en kun je de invert‑stap combineren met andere aanpassingen (bijv. brightness, hue) in dezelfde lus.

## Een PSD converteren naar een negatief beeld

De Invert Adjustment Layer is in wezen de **convert PSD to negative** bewerking. Door deze laag als bovenste item toe te voegen, bereik je een volledig negatief effect zonder de oorspronkelijke pixelgegevens permanent te wijzigen. Je kunt later de laag verwijderen of uitschakelen om terug te keren naar het oorspronkelijke uiterlijk.

## Veelvoorkomende problemen & tips

| Probleem | Oorzaak | Oplossing |
|----------|---------|-----------|
| **NullPointerException op `Image.load`** | Onjuist bestandspad of ontbrekend bestand | Controleer `dataDir` en bestandsnaam; gebruik absolute paden voor testen |
| **Laagvolgorde niet zoals verwacht** | Lagen toevoegen na bestaande verandert de stapeling | Gebruik `im.addInvertAdjustmentLayer()` voordat je andere aanpassingen toevoegt, of herschik lagen via `im.getLayers()` |
| **Prestatievertraging bij grote PSD's** | Zeer grote bestanden in het geheugen laden | Overweeg pagina's in delen te verwerken of vergroot de JVM-heapgrootte (`-Xmx2g`) |

## Veelgestelde vragen

**V: Is Aspose.PSD compatibel met alle Java‑versies?**  
A: Aspose.PSD ondersteunt Java 6.0 en latere versies.

**V: Kan ik meerdere aanpassingslagen in één bewerking toepassen?**  
A: Ja, je kunt meerdere aanpassingslagen stapelen — zoals Invert, Brightness en Hue/Saturation — om complexe effecten te bereiken.

**V: Waar kan ik extra documentatie voor Aspose.PSD vinden?**  
A: Verwijs naar de documentatie [here](https://reference.aspose.com/psd/java/) voor uitgebreide handleidingen en API‑referenties.

**V: Is er een gratis proefversie beschikbaar voor Aspose.PSD?**  
A: Ja, je kunt de gratis proefversie [here](https://releases.aspose.com/) verkennen.

**V: Hoe kan ik een tijdelijke licentie voor Aspose.PSD verkrijgen?**  
A: Je kunt een tijdelijke licentie [here](https://purchase.aspose.com/temporary-license/) verkrijgen.

---

**Laatst bijgewerkt:** 2026-04-22  
**Getest met:** Aspose.PSD 24.12 for Java  
**Auteur:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}