---
date: 2026-05-19
description: Leer hoe u PSD naar JPEG kunt converteren en een afbeelding 270 graden
  kunt roteren met Aspose.PSD voor Java. Deze gids laat zien hoe u PSD‑bestanden roteert,
  afbeeldingen draait en PSD naar JPEG converteert.
keywords:
- convert psd to jpeg
- how to rotate psd
- flip image java
- rotate psd layer
- rotate image without photoshop
linktitle: Afbeelding 270 graden roteren
schemas:
- author: Aspose
  dateModified: '2026-05-19'
  description: Learn how to convert PSD to JPEG and rotate image 270 degrees using
    Aspose.PSD for Java. This guide shows how to rotate PSD files, flip images, and
    convert PSD to JPEG.
  headline: Convert PSD to JPEG & Rotate 270° with Aspose.PSD for Java
  type: TechArticle
- description: Learn how to convert PSD to JPEG and rotate image 270 degrees using
    Aspose.PSD for Java. This guide shows how to rotate PSD files, flip images, and
    convert PSD to JPEG.
  name: Convert PSD to JPEG & Rotate 270° with Aspose.PSD for Java
  steps:
  - name: Load the PSD File
    text: '`Image` is Aspose.PSD''s core class that represents a single PSD document
      in memory. Instantiating it reads only the header information, keeping memory
      usage low.'
  - name: Rotate the Image 270 Degrees
    text: '`rotateFlip` performs the specified rotation and optional flip on the image.
      `RotateFlipType.Rotate270FlipNone` rotates the canvas 270 degrees clockwise
      while leaving the image orientation unchanged. > **Pro tip:** If you also need
      to flip the image horizontally or vertically, choose a different `Ro'
  - name: Convert PSD to JPEG and Save
    text: '`JpegOptions` defines JPEG‑specific parameters such as compression quality.
      The `save` method writes the transformed image to disk in the desired format.
      The file `RotatedImage_out.jpg` now contains the original PSD content rotated
      270 degrees and saved as a JPEG.'
  type: HowTo
- questions:
  - answer: Yes, Aspose.PSD supports PSD, JPEG, PNG, BMP, GIF, TIFF, and many other
      raster formats.
    question: Is Aspose.PSD compatible with different image formats?
  - answer: Absolutely! While `RotateFlipType` provides common angles, you can chain
      multiple calls or use transformation matrices for arbitrary angles.
    question: Can I apply custom rotations, not just predefined flips?
  - answer: Replace `JpegOptions` with `PngOptions` (or the appropriate options class)
      in the `save` method.
    question: How do I convert the rotated PSD to another format, such as PNG?
  - answer: For community help, visit the [Aspose.PSD Forum](https://forum.aspose.com/c/psd/34).
    question: Where can I find additional support or assistance?
  - answer: Yes, you can explore Aspose.PSD with a [free trial](https://releases.aspose.com/).
    question: Is there a free trial available?
  type: FAQPage
second_title: Aspose.PSD Java API
title: Converteer PSD naar JPEG & roteer 270° met Aspose.PSD voor Java
url: /nl/java/advanced-image-manipulation/rotate-image/
weight: 19
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Converteer PSD naar JPEG & roteer afbeelding 270 graden met Aspose.PSD voor Java

## Introductie

In deze **Java image‑processing tutorial** leer je hoe je **PSD naar JPEG** kunt converteren terwijl je de afbeelding 270 degrees roteert met Aspose.PSD voor Java. Of je nu een batch‑verwerkingspipeline, een web‑gebaseerde editor of een desktop‑hulpmiddel bouwt, de bibliotheek stelt je in staat PSD‑lagen te manipuleren zonder Photoshop. We behandelen ook optioneel spiegelen en tonen de volledige end‑to‑end stroom van het laden van een PSD‑bestand tot het opslaan van een JPEG.

## Snelle antwoorden
- **Welke bibliotheek behandelt de rotatie?** Aspose.PSD for Java  
- **Welke rotatiehoek gebruikt het voorbeeld?** 270 graden  
- **Kan ik de afbeelding ook spiegelen?** Ja – gebruik `RotateFlipType`‑opties zoals `Rotate90FlipX`  
- **Hoe sla ik het resultaat op?** In het voorbeeld slaan we op als JPEG met `JpegOptions`  
- **Heb ik een licentie nodig voor productie?** Een geldige Aspose.PSD‑licentie is vereist voor commercieel gebruik  

## Wat betekent “afbeelding 270 graden roteren”?
Een afbeelding 270 graden roteren betekent dat je de foto drie‑kwart van een volledige cirkel met de klok mee draait (of 90 graden tegen de klok in). Deze oriëntatie herstelt vaak de oorspronkelijke portretindeling na eerdere transformaties, en wordt vaak gebruikt wanneer afbeeldingen in landschapsmodus zijn gemaakt maar in portret moeten worden weergegeven. Het resultaat is een correct georiënteerde weergave zonder kwaliteitsverlies.

## Waarom Aspose.PSD voor deze taak gebruiken?
Aspose.PSD ondersteunt **meer dan 50 invoer‑ en uitvoerformaten**—inclusief PSD, JPEG, PNG, BMP, GIF en TIFF—en kan bestanden tot **2 GB** verwerken zonder het volledige document in het geheugen te laden. De API werkt op elke Java‑runtime (JDK 8+), vereist geen native Photoshop‑installatie, en biedt een enkele `rotateFlip`‑aanroep die zowel rotatie als spiegelen in één stap afhandelt.

## Vereisten

Voordat je begint, zorg dat je het volgende hebt:

- **Aspose.PSD for Java** bibliotheek geïnstalleerd. Je kunt deze downloaden en de volledige API‑referentie bekijken [hier](https://reference.aspose.com/psd/java/).  
- Een Java‑ontwikkelomgeving (JDK 8 of hoger).  
- Een voorbeeld‑PSD‑bestand dat je wilt roteren. Werk de `sourceFile`‑variabele in de code bij met het juiste pad naar je bestand.

## Pakketten importeren

De klassen `Image`, `RotateFlipType` en `JpegOptions` zijn vereist voor het laden, transformeren en opslaan van het bestand.  
`Image` is de kernklasse die een PSD‑document in het geheugen vertegenwoordigt.  
`RotateFlipType` somt de ondersteunde rotatie‑ en spiegelbewerkingen op.  
`JpegOptions` configureert JPEG‑uitvoersettings zoals kwaliteit.  

```java
import com.aspose.psd.Image;
import com.aspose.psd.RotateFlipType;

import com.aspose.psd.imageoptions.JpegOptions;
```

## Hoe PSD naar JPEG converteren na rotatie?

Laad de bron‑PSD, pas een rotatie van 270 graden toe, en sla deze direct op als JPEG. Deze drie‑stappen‑stroom duurt minder dan een seconde voor typische 10‑MP‑afbeeldingen op een moderne CPU, waardoor het ideaal is voor high‑throughput batch‑taken. Door alleen de benodigde beeldgegevens te verwerken blijft het geheugenverbruik laag, en behoudt de resulterende JPEG visuele getrouwheid terwijl de bestandsgrootte wordt verkleind.

### Stap 1: Laad het PSD‑bestand

`Image` is de kernklasse van Aspose.PSD die een enkel PSD‑document in het geheugen vertegenwoordigt. Bij het instantieren wordt alleen de header‑informatie gelezen, waardoor het geheugenverbruik laag blijft.

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";
Image image = Image.load(sourceFile);
```

### Stap 2: Roteer de afbeelding 270 graden

`rotateFlip` voert de opgegeven rotatie en optioneel spiegelen uit op de afbeelding. `RotateFlipType.Rotate270FlipNone` roteert het canvas 270 graden met de klok mee terwijl de afbeelding oriëntering ongewijzigd blijft.

```java
image.rotateFlip(RotateFlipType.Rotate270FlipNone);
```

> **Pro tip:** Als je de afbeelding ook horizontaal of verticaal wilt spiegelen, kies dan een andere `RotateFlipType` zoals `Rotate90FlipX` of `Rotate180FlipY`.

### Stap 3: Converteer PSD naar JPEG en sla op

`JpegOptions` definieert JPEG‑specifieke parameters zoals compressiekwaliteit. De `save`‑methode schrijft de getransformeerde afbeelding naar schijf in het gewenste formaat.

```java
String destName = dataDir + "RotatedImage_out.jpg";
image.save(destName, new JpegOptions());
```

Het bestand `RotatedImage_out.jpg` bevat nu de oorspronkelijke PSD‑inhoud, geroteerd 270 graden en opgeslagen als een JPEG.

## Veelvoorkomende problemen en oplossingen

| Probleem | Oplossing |
|-------|----------|
| **Afbeelding verschijnt ondersteboven** | Controleer of je `Rotate270FlipNone` hebt gebruikt. Voor een rotatie van 90 graden met de klok mee gebruik je `Rotate90FlipNone`. |
| **Uitvoerbestand is corrupt** | Zorg ervoor dat de doelmap bestaat en dat je schrijfrechten hebt. |
| **Licentie‑exception** | Installeer een tijdelijke of permanente Aspose.PSD‑licentie voordat je de afbeelding in productie laadt. |

## Veelgestelde vragen

**Q: Is Aspose.PSD compatibel met verschillende afbeeldingsformaten?**  
A: Ja, Aspose.PSD ondersteunt PSD, JPEG, PNG, BMP, GIF, TIFF en vele andere rasterformaten.

**Q: Kan ik aangepaste rotaties toepassen, niet alleen vooraf gedefinieerde flips?**  
A: Absoluut! Hoewel `RotateFlipType` veelvoorkomende hoeken biedt, kun je meerdere aanroepen combineren of transformatie‑matrices gebruiken voor willekeurige hoeken.

**Q: Hoe converteer ik de geroteerde PSD naar een ander formaat, zoals PNG?**  
A: Vervang `JpegOptions` door `PngOptions` (of de juiste opties‑klasse) in de `save`‑methode.

**Q: Waar kan ik extra ondersteuning of hulp vinden?**  
A: Voor community‑hulp kun je het [Aspose.PSD Forum](https://forum.aspose.com/c/psd/34) bezoeken.

**Q: Is er een gratis proefversie beschikbaar?**  
A: Ja, je kunt Aspose.PSD verkennen met een [gratis proefversie](https://releases.aspose.com/).

**Q: Hoe verkrijg ik een tijdelijke licentie?**  
A: Als je een tijdelijke licentie nodig hebt, kun je er een verkrijgen [hier](https://purchase.aspose.com/temporary-license/).

---

**Laatst bijgewerkt:** 2026-05-19  
**Getest met:** Aspose.PSD for Java 24.12  
**Auteur:** Aspose  

{{< blocks/products/products-backtop-button >}}

## Gerelateerde tutorials

- [Converteer PSD naar rasterafbeeldingsformaten met Aspose.PSD voor Java](/psd/java/advanced-techniques/convert-psd-to-raster-formats/)
- [Converteer PSD naar PNG en roteer lagen in PSD‑bestanden met Java](/psd/java/advanced-psd-layer-features-effects/rotate-layers-psd-files/)
- [Hoe afbeelding roteren in Java met Aspose.PSD](/psd/java/advanced-image-manipulation/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}