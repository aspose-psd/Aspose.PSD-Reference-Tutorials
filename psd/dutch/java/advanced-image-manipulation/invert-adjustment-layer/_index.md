---
date: 2026-11-04
description: Leer hoe u Aspose.PSD for Java kunt gebruiken om een invert adjustment
  layer toe te passen, PSD-afbeeldingen in batch te verwerken en negatieve PSD‑bestanden
  te maken.
keywords:
- how to use aspose
- batch process psd images
- create negative image psd
- image processing java library
- apply multiple adjustment layers
lastmod: 2026-11-04
linktitle: Invert Adjustment Layer
og_description: Hoe u Aspose.PSD for Java kunt gebruiken om een invert adjustment
  layer toe te voegen, PSD-afbeeldingen in batch te verwerken en een negatieve PSD
  te maken. Volg de stapsgewijze handleiding.
og_image_alt: Screenshot showing Aspose.PSD Java code adding an invert adjustment
  layer
og_title: Hoe Aspose.PSD te gebruiken om een invert adjustment layer toe te voegen
  in Java
schemas:
- author: Aspose
  dateModified: '2026-11-04'
  description: Learn how to use Aspose.PSD for Java to apply an invert adjustment
    layer, batch process PSD images, and create negative image PSD files.
  headline: How to use Aspose.PSD to add an invert adjustment layer in Java
  type: TechArticle
- questions:
  - answer: Yes, it supports Java 6.0 and later, including Java 8, 11, and 17.
    question: Is Aspose.PSD compatible with all Java versions?
  - answer: Absolutely. After adding the invert layer you can call `addBrightnessAdjustmentLayer()`,
      `addHueSaturationAdjustmentLayer()`, etc., to stack effects.
    question: Can I apply multiple adjustment layers in a single operation?
  - answer: The complete documentation is available [Aspose.PSD Java API reference](https://reference.aspose.com/psd/java/).
    question: Where can I find the full API reference?
  - answer: Yes, you can download a trial version [Aspose.PSD trial download](https://releases.aspose.com/).
    question: Is there a free trial for Aspose.PSD?
  - answer: Request a temporary license [temporary license request page](https://purchase.aspose.com/temporary-license/).
    question: How do I obtain a temporary license for testing?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- aspose psd
- java image processing
- invert adjustment layer
- batch psd processing
title: Hoe Aspose.PSD te gebruiken om een invert adjustment layer toe te voegen in
  Java
url: /nl/java/advanced-image-manipulation/invert-adjustment-layer/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Hoe gebruik je Aspose.PSD om een invert‑aanpassingslaag toe te voegen in Java

## Introductie

Als je op zoek bent naar een robuuste **image processing java library**, is Aspose.PSD for Java een van de meest veelzijdige opties op de markt. In deze tutorial zie je **hoe je Aspose** kunt gebruiken om een **Invert Adjustment Layer** in een PSD‑bestand in te voegen, deze te stapelen met andere aanpassingen, en zelfs de bewerking uit te voeren op tientallen bestanden. Of je nu een batch‑verwerkingstool, een server‑side image service, of een enkele‑beeldeditor bouwt, de onderstaande stappen brengen je van bron‑PSD naar een volledig bewerkbare negatieve afbeelding in enkele minuten.

## Snelle antwoorden
- **Wat doet de Invert Adjustment Layer?** Het keert elke RGB‑waarde in het geselecteerde gebied om, waardoor de afbeelding een fotografisch negatief wordt.  
- **Welke library biedt deze functie?** Aspose.PSD, een toonaangevende **image processing java library**.  
- **Kan ik het stapelen met andere aanpassingen?** Ja – je kunt **meerdere aanpassingslagen toepassen** zoals Brightness/Contrast, Hue/Saturation, en meer.  
- **Heb ik een licentie nodig voor ontwikkeling?** Een gratis proefversie is beschikbaar; een licentie is vereist voor productiegebruik.  
- **Hoe lang duurt de implementatie?** Meestal minder dan 10 minuten voor een basisgeval.

## Wat is de Invert‑aanpassingslaag?

De Invert Adjustment Layer is een niet‑destructieve bewerking die de kleurwaarden van elke pixel die het beïnvloedt omkeert. Omdat het bovenop de laagstapel zit, kun je de zichtbaarheid in- of uitschakelen of de volgorde wijzigen zonder de oorspronkelijke afbeeldingsgegevens permanent te wijzigen. Dit is de snelste manier om **negative image PSD** bestanden te maken of een klassieke film‑negatief look te bereiken.

## Waarom Aspose.PSD gebruiken als je image processing java library?

Aspose.PSD ondersteunt **200+ PSD‑functies**, kan Photoshop‑bestanden lezen en schrijven zonder Photoshop te vereisen, en verwerkt documenten met honderden pagina's met minder dan 500 MB heap‑geheugen. Het draait op elke Java‑runtime (Java 6+), waardoor het ideaal is voor **batch process psd images** op Windows-, Linux- of macOS-servers.

## Vereisten

Voordat je begint, zorg ervoor dat je het volgende hebt:

1. **Aspose.PSD for Java** – download de nieuwste JAR van de officiële site [Aspose.PSD voor Java downloadpagina](https://releases.aspose.com/psd/java/).  
2. **Java Development Kit** – JDK 6.0 of later geïnstalleerd en geconfigureerd in je `PATH`.  

Nu ben je klaar om de code te schrijven.

## Import pakketten

De `PsdImage`‑klasse vertegenwoordigt een volledig Photoshop‑document in het geheugen, terwijl de aanpassings‑laagklassen zich bevinden in het `com.aspose.psd.layers.adjustments`‑pakket.

De `PsdImage`‑klasse is het top‑level object van Aspose.PSD dat de structuur en pixelgegevens van een PSD‑bestand omsluit. Importeer de namespaces, waarna je PSD‑bestanden kunt laden, bewerken en opslaan.

## Stap 1: stel documentmap in

Definieer de map die je bron‑PSD‑bestand bevat en waar de output wordt opgeslagen. Het gebruik van absolute paden voorkomt `NullPointerException` wanneer de werkmap verandert.

## Stap 2: laad PSD‑bestand

Laad het bronbestand in een `PsdImage`‑object. Dit object bevat de volledige laaghiërarchie in het geheugen, waardoor niet‑destructieve bewerkingen mogelijk zijn.

De `PsdImage`‑klasse biedt een statische `load`‑methode die de bestandsheader leest, het formaat valideert en een in‑memory representatie maakt die klaar is voor manipulatie.

## Stap 3: voeg invert‑aanpassingslaag toe

Roep de ingebouwde methode aan om een Invert Adjustment Layer in te voegen bovenop de huidige laagstapel. Je kunt later meer lagen toevoegen (bijv. Brightness, Hue) om **multiple adjustment layers** in één workflow **toepassen**.

`addInvertAdjustmentLayer()` voegt een Invert Adjustment Layer toe aan de laagcollectie van de PSD.

## Stap 4: sla de output op

Sla de gewijzigde PSD op schijf op.  

`save()` schrijft het PSD‑bestand, inclusief alle lagen en metadata, naar het opgegeven pad.

Opslaan gebruikt dezelfde `save`‑methode die het volledige document schrijft, inclusief alle aanpassingslagen, maskers en metadata, naar het opgegeven formaat.

### Wat is er net gebeurd?

Het PSD‑bestand werd geladen in een `PsdImage`‑object, er werd een `InvertAdjustmentLayer` aangemaakt en als bovenste laag toegevoegd, en het document werd opgeslagen. Deze volgorde behoudt de oorspronkelijke afbeeldingsgegevens terwijl een niet‑destructief invert‑effect wordt toegevoegd dat later kan worden in- of uitgeschakeld of opnieuw geordend.

Je hebt nu met succes Aspose.PSD, een **image processing java library**, gebruikt om een PSD‑bestand te manipuleren.

## Hoe batchverwerking van PSD‑afbeeldingen met invert‑aanpassing?

Laad elk bestand binnen een `for`‑lus, voer dezelfde stappen uit en roep `save` aan voor elke iteratie. Omdat Aspose.PSD bestanden in een streaming‑modus verwerkt, kun je **hundreds of PSDs** afhandelen terwijl je het geheugenverbruik onder 300 MB houdt door dezelfde `PsdImage`‑instantie opnieuw te gebruiken.

## Hoe converteer je een PSD naar een negatief beeld?

Voeg de Invert Adjustment Layer toe als bovenste item en sla het document op – die bewerking is gelijk aan **convert PSD to negative**. Je kunt later de laag uitschakelen of verwijderen om terug te keren naar het oorspronkelijke uiterlijk zonder het bronbestand opnieuw te laden.

## Veelvoorkomende problemen & tips

| Probleem | Oorzaak | Oplossing |
|----------|---------|-----------|
| **NullPointerException on `Image.load`** | Onjuist bestandspad of ontbrekend bestand | Controleer `dataDir` en bestandsnaam; gebruik absolute paden voor testen |
| **Layer order not as expected** | Lagen toevoegen na bestaande lagen wijzigt de stapeling | Voeg de invert‑laag toe vóór andere aanpassingen, of wijzig de volgorde via `psdImage.getLayers().move()` |
| **Performance slowdown on large PSDs** | Zeer grote bestanden in het geheugen laden | Vergroot de JVM‑heap (`-Xmx2g`) of verwerk bestanden in stukken met `psdImage.getPages().get(0).getResources().setMemoryOptimized(true)` |

## Veelgestelde vragen

**Q: Is Aspose.PSD compatibel met alle Java‑versies?**  
A: Ja, het ondersteunt Java 6.0 en later, inclusief Java 8, 11 en 17.

**Q: Kan ik meerdere aanpassingslagen in één bewerking toepassen?**  
A: Absoluut. Na het toevoegen van de invert‑laag kun je `addBrightnessAdjustmentLayer()`, `addHueSaturationAdjustmentLayer()`, enz. aanroepen om effecten te stapelen.

**Q: Waar kan ik de volledige API‑referentie vinden?**  
A: De volledige documentatie is beschikbaar [Aspose.PSD Java API-referentie](https://reference.aspose.com/psd/java/).

**Q: Is er een gratis proefversie voor Aspose.PSD?**  
A: Ja, je kunt een proefversie downloaden [Aspose.PSD proefdownload](https://releases.aspose.com/).

**Q: Hoe verkrijg ik een tijdelijke licentie voor testen?**  
A: Vraag een tijdelijke licentie aan [pagina voor tijdelijke licentieaanvraag](https://purchase.aspose.com/temporary-license/).

---

**Laatst bijgewerkt:** 2026-11-04  
**Getest met:** Aspose.PSD 24.12 for Java  
**Auteur:** Aspose  









```java
import com.aspose.psd.Image;

import com.aspose.psd.fileformats.psd.PsdImage;
```

```java
String dataDir = "Your Document Directory";
```

```java
String filePath = dataDir + "InvertStripes_before.psd";
String outputPath = dataDir + "InvertStripes_after.psd";

PsdImage im = (PsdImage)Image.load(filePath);
```

```java
im.addInvertAdjustmentLayer();
```

```java
im.save(outputPath);
```

## Gerelateerde tutorials

- [Niveau‑aanpassingslaag toevoegen aan PSD‑bestanden met Aspose.PSD voor Java](/psd/java/modifying-converting-psd-images/add-level-adjustment-layer-psd/)
- [Hoe een aanpassingslaag – Channel Mixer toevoegen in PSD (Java)](/psd/java/modifying-converting-psd-images/add-channel-mixer-adjustment-layer-psd/)
- [Hoe PSD bewerken – Curves‑aanpassingslaag toevoegen met Java](/psd/java/modifying-converting-psd-images/add-curves-adjustment-layer-psd/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}