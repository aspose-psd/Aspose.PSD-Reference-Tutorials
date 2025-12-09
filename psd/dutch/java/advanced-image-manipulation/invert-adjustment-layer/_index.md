---
date: 2025-12-02
description: Leer hoe u de Java‑afbeeldingsverwerkingsbibliotheek Aspose.PSD kunt
  gebruiken om meerdere aanpassingslagen toe te passen, waaronder de Invert‑aanpassingslaag,
  voor naadloze PSD‑manipulatie.
linktitle: Invert Adjustment Layer
second_title: Aspose.PSD Java API
title: 'Afbeeldingsverwerking Java-bibliotheek: Laag inverteren met Aspose.PSD'
url: /nl/java/advanced-image-manipulation/invert-adjustment-layer/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Invert-aanpassingslaag in Aspose.PSD voor Java

## Introduction

Als je op zoek bent naar een robuuste **image processing java library**, is Aspose.PSD voor Java een van de meest veelzijdige opties op de markt. In deze tutorial lopen we stap voor stap door hoe je een **Invert Adjustment Layer** toevoegt aan een PSD‑bestand, een techniek die je kunt combineren met andere aanpassingslagen om verfijnde visuele effecten te bereiken. Of je nu een batch‑verwerkingstool of een enkele‑afbeeldingseditor bouwt, deze gids biedt een duidelijke, stap‑voor‑stap route om het werk snel te voltooien.

## Quick Answers
- **Wat doet de Invert-aanpassingslaag?** Het keert alle kleurwaarden in het geselecteerde gebied om, waardoor een negatief‑beeld effect ontstaat.  
- **Welke bibliotheek biedt deze functie?** Aspose.PSD, een toonaangevende **image processing java library**.  
- **Kan ik het stapelen met andere aanpassingen?** Ja – je kunt **multiple adjustment layers** toepassen zoals Brightness/Contrast, Hue/Saturation, en meer.  
- **Heb ik een licentie nodig voor ontwikkeling?** Een gratis proefversie is beschikbaar; een licentie is vereist voor productiegebruik.  
- **Hoe lang duurt de implementatie?** Meestal minder dan 10 minuten voor een basisgeval.

## What is the Invert Adjustment Layer?

De Invert-aanpassingslaag is een niet‑destructieve bewerking die de RGB‑waarden van elk pixel dat het beïnvloedt omdraait. Omdat het bovenop de laagstapel zit, kun je de zichtbaarheid in- of uitschakelen of de volgorde wijzigen zonder de oorspronkelijke afbeeldingsgegevens permanent te wijzigen.

## Why Use Aspose.PSD as Your Image Processing Java Library?

- **Full PSD support** – lees, bewerk en schrijf Photoshop‑bestanden zonder Photoshop geïnstalleerd.  
- **Cross‑platform** – werkt op elke Java‑runtime (Java 6+).  
- **Rich adjustment features** – bevat ingebouwde methoden voor veelvoorkomende bewerkingen, waardoor het eenvoudig is om **multiple adjustment layers** toe te passen in een enkele workflow.  
- **Performance‑optimized** – verwerkt grote bestanden efficiënt, wat essentieel is voor batch‑verwerking.

## Prerequisites

Zorg ervoor dat je het volgende hebt voordat je begint:

1. **Aspose.PSD Library** – download deze van de officiële site [here](https://releases.aspose.com/psd/java/).  
2. **Java Development Environment** – JDK 6.0 of later geïnstalleerd en geconfigureerd.  

Laten we nu in de code duiken.

## Import Packages

Begin met het importeren van de benodigde klassen. Deze imports geven je toegang tot de kern‑image‑handling API's en de PSD‑specifieke functionaliteit.

```java
import com.aspose.psd.Image;

import com.aspose.psd.fileformats.psd.PsdImage;
```

## Step 1: Set Up Document Directory

Definieer de map die je bron‑PSD‑bestand bevat en waar de output wordt opgeslagen.

```java
String dataDir = "Your Document Directory";
```

## Step 2: Load PSD File

Laad het bronbestand in een `PsdImage`‑object. Dit object vertegenwoordigt het volledige PSD‑document in het geheugen.

```java
String filePath = dataDir + "InvertStripes_before.psd";
String outputPath = dataDir + "InvertStripes_after.psd";

PsdImage im = (PsdImage)Image.load(filePath);
```

## Step 3: Add Invert Adjustment Layer

Roep de ingebouwde methode aan om een Invert‑Adjustment‑Layer toe te voegen bovenop de huidige laagstapel. Je kunt later meer lagen toevoegen (bijv. Brightness, Hue) om **multiple adjustment layers** toe te passen.

```java
im.addInvertAdjustmentLayer();
```

## Step 4: Save the Output

Sla de gewijzigde PSD op schijf op. Het opgeslagen bestand bevat nu de Invert‑Adjustment‑Layer en kan geopend worden in Photoshop of elke PSD‑compatibele viewer.

```java
im.save(outputPath);
```

### What just happened?

- De PSD werd in het geheugen geladen.  
- Er werd een Invert‑Adjustment‑Layer toegevoegd als bovenste laag.  
- De afbeelding werd opgeslagen, waarbij de niet‑destructieve bewerking behouden bleef.

Je hebt nu succesvol Aspose.PSD, een **image processing java library**, gebruikt om een PSD‑bestand te manipuleren.

## Common Issues & Tips

| Probleem | Oorzaak | Oplossing |
|----------|---------|-----------|
| **NullPointerException on `Image.load`** | Onjuist bestandspad of ontbrekend bestand | Controleer `dataDir` en bestandsnaam; gebruik absolute paden voor testen |
| **Layer order not as expected** | Het toevoegen van lagen na bestaande verandert de stapeling | Gebruik `im.addInvertAdjustmentLayer()` vóór het toevoegen van andere aanpassingen, of herschik lagen via `im.getLayers()` |
| **Performance slowdown on large PSDs** | Grote bestanden volledig in het geheugen laden | Overweeg om pagina's in delen te verwerken of vergroot de JVM-heapgrootte (`-Xmx2g`) |

## Frequently Asked Questions

**Q: Is Aspose.PSD compatible with all Java versions?**  
A: Aspose.PSD ondersteunt Java 6.0 en latere versies.

**Q: Can I apply multiple adjustment layers in a single operation?**  
A: Ja, je kunt meerdere aanpassingslagen stapelen — zoals Invert, Brightness en Hue/Saturation — om complexe effecten te bereiken.

**Q: Where can I find additional documentation for Aspose.PSD?**  
A: Raadpleeg de documentatie [here](https://reference.aspose.com/psd/java/) voor uitgebreide handleidingen en API‑referenties.

**Q: Is there a free trial available for Aspose.PSD?**  
A: Ja, je kunt de gratis proefversie verkennen [here](https://releases.aspose.com/).

**Q: How can I obtain a temporary license for Aspose.PSD?**  
A: Je kunt een tijdelijke licentie verkrijgen [here](https://purchase.aspose.com/temporary-license/).

---

**Last Updated:** 2025-12-02  
**Tested With:** Aspose.PSD 24.12 for Java  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}