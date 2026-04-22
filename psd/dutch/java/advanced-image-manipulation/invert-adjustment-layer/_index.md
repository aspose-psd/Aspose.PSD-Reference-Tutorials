---
date: 2026-02-07
description: Leer hoe u de Java-afbeeldingsverwerkingsbibliotheek Aspose.PSD kunt
  gebruiken om meerdere aanpassingslagen, waaronder de Invert‑aanpassingslaag, toe
  te passen voor naadloze PSD‑manipulatie.
linktitle: Invert Adjustment Layer
second_title: Aspose.PSD Java API
title: 'Afbeeldingsverwerking Java‑bibliotheek: Laag inverteren met Aspose.PSD'
url: /nl/java/advanced-image-manipulation/invert-adjustment-layer/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Invert Adjustment Layer in Aspose.PSD voor Java

## Introductie

Als je op zoek bent naar een robuuste **image processing java library**, is Aspose.PSD for Java een van de meest veelzijdige opties op de markt. In deze tutorial laten we zien hoe je een **Invert Adjustment Layer** toevoegt aan een PSD‑bestand, een techniek die je kunt combineren met andere aanpassingslagen om verfijnde visuele effecten te bereiken. Of je nu een batch‑verwerkingstool of een enkele‑afbeeldingseditor bouwt, deze gids biedt je een duidelijke, stapsgewijze route om het werk snel te voltooien.

## Snelle antwoorden
- **Wat doet de Invert Adjustment Layer?** Het keert alle kleurwaarden in het geselecteerde gebied om, waardoor een negatief‑beeld effect ontstaat.  
- **Welke bibliotheek biedt deze functie?** Aspose.PSD, een toonaangevende image processing java library.  
- **Kan ik het stapelen met andere aanpassingen?** Ja – je kunt **apply multiple adjustment layers** toepassen, zoals Brightness/Contrast, Hue/Saturation, en meer.  
- **Heb ik een licentie nodig voor ontwikkeling?** Er is een gratis proefversie beschikbaar; een licentie is vereist voor productiegebruik.  
- **Hoe lang duurt de implementatie?** Meestal minder dan 10 minuten voor een basisgeval.

## Wat is de Invert Adjustment Layer?

De Invert Adjustment Layer is een niet‑destructieve bewerking die de RGB-waarden van elke pixel die het beïnvloedt omdraait. Omdat het bovenop de lagenstapel zit, kun je de zichtbaarheid togglen of de volgorde wijzigen zonder de oorspronkelijke afbeeldingsgegevens permanent te wijzigen.

## Hoe een laag omkeren met Aspose.PSD

Hieronder zie je precies hoe je **een laag omkeert** in een PSD‑bestand. De stappen zijn opzettelijk eenvoudig zodat je je kunt concentreren op het concept in plaats van op boilerplate‑code.

## Waarom Aspose.PSD gebruiken als jouw Image Processing Java Library?

- **Full PSD support** – lees, bewerk en schrijf Photoshop‑bestanden zonder Photoshop geïnstalleerd te hebben.  
- **Cross‑platform** – werkt op elke Java‑runtime (Java 6+).  
- **Rich adjustment features** – bevat ingebouwde methoden voor veel voorkomende bewerkingen, waardoor het eenvoudig is om **multiple adjustment layers** toe te passen in een enkele workflow.  
- **Performance‑optimized** – verwerkt grote bestanden efficiënt, wat essentieel is voor batchverwerking.

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

Definieer de map die je bron‑PSD‑bestand bevat en waar de output wordt opgeslagen.

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

Roep de ingebouwde methode aan om een Invert Adjustment Layer toe te voegen bovenop de huidige lagenstapel. Je kunt later meer lagen toevoegen (bijv. Brightness, Hue) om **multiple adjustment layers** toe te passen.

```java
im.addInvertAdjustmentLayer();
```

## Stap 4: Output opslaan

Sla de gewijzigde PSD op schijf op. Het opgeslagen bestand bevat nu de Invert Adjustment Layer en kan worden geopend in Photoshop of elke PSD‑compatibele viewer.

```java
im.save(outputPath);
```

### Wat is er net gebeurd?

- De PSD is in het geheugen geladen.  
- Een Invert Adjustment Layer is toegevoegd als bovenste laag.  
- De afbeelding is opgeslagen, waarbij de niet‑destructieve bewerking behouden blijft.

Je hebt nu met succes Aspose.PSD, een **image processing java library**, gebruikt om een PSD‑bestand te manipuleren.

## Veelvoorkomende problemen & tips

| Probleem | Oorzaak | Oplossing |
|-------|-------|----------|
| **NullPointerException on `Image.load`** | Incorrect file path or missing file | Verify `dataDir` and file name; use absolute paths for testing |
| **Layer order not as expected** | Adding layers after existing ones changes stacking | Use `im.addInvertAdjustmentLayer()` before adding other adjustments, or reorder layers via `im.getLayers()` |
| **Performance slowdown on large PSDs** | Loading very large files into memory | Consider processing pages in chunks or increasing JVM heap size (`-Xmx2g`) |

## Veelgestelde vragen

**Q: Is Aspose.PSD compatibel met alle Java‑versies?**  
A: Aspose.PSD ondersteunt Java 6.0 en latere versies.

**Q: Kan ik meerdere aanpassingslagen in één bewerking toepassen?**  
A: Ja, je kunt verschillende aanpassingslagen stapelen — zoals Invert, Brightness en Hue/Saturation — om complexe effecten te bereiken.

**Q: Waar kan ik extra documentatie voor Aspose.PSD vinden?**  
A: Raadpleeg de documentatie [here](https://reference.aspose.com/psd/java/) voor uitgebreide handleidingen en API‑referenties.

**Q: Is er een gratis proefversie beschikbaar voor Aspose.PSD?**  
A: Ja, je kunt de gratis proefversie verkennen [here](https://releases.aspose.com/).

**Q: Hoe kan ik een tijdelijke licentie voor Aspose.PSD verkrijgen?**  
A: Je kunt een tijdelijke licentie verkrijgen [here](https://purchase.aspose.com/temporary-license/).

---

**Laatst bijgewerkt:** 2026-02-07  
**Getest met:** Aspose.PSD 24.12 for Java  
**Auteur:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}