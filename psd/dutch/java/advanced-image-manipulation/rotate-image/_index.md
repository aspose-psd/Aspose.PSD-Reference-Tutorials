---
date: 2025-12-06
description: Leer hoe u een afbeelding 270 graden draait met Aspose.PSD voor Java.
  Deze gids laat zien hoe u PSD‑bestanden draait, afbeeldingen spiegelt en PSD naar
  JPEG converteert.
linktitle: Rotate Image 270 Degrees
second_title: Aspose.PSD Java API
title: Hoe een afbeelding 270 graden te roteren met Aspose.PSD voor Java
url: /nl/java/advanced-image-manipulation/rotate-image/
weight: 19
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Afbeelding 270 graden roteren met Aspose.PSD voor Java

## Inleiding

In deze **java image processing tutorial**, ontdek je hoe je **een afbeelding 270 graden draait** snel en betrouwbaar met Aspose.PSD voor Java. Of je nu een foto‑bewerkingshulpmiddel bouwt, batchconversies automatiseert, of gewoon een PSD‑laag opnieuw moet oriënteren, de bibliotheek maakt de taak moeiteloos. We zullen ook ingaan op het spiegelen van afbeeldingen en het converteren van de geroteerde PSD naar een JPEG, zodat je een volledige end‑to‑end workflow krijgt.

## Snelle antwoorden
- **Welke bibliotheek handelt de rotatie af?** Aspose.PSD for Java  
- **Welke rotatiehoek gebruikt het voorbeeld?** 270 degrees  
- **Kan ik de afbeelding ook spiegelen?** Ja – gebruik `RotateFlipType` opties zoals `Rotate90FlipX`  
- **Hoe sla ik het resultaat op?** In het voorbeeld slaan we op als JPEG met `JpegOptions`  
- **Heb ik een licentie nodig voor productie?** Een geldige Aspose.PSD‑licentie is vereist voor commercieel gebruik  

## Wat betekent “rotate image 270 degrees”?
Een afbeelding 270 graden draaien betekent dat je de foto drie kwart van een volledige cirkel met de klok mee draait (of 90 graden tegen de klok in). In veel grafische‑bewerkingsscenario's komt deze oriëntatie overeen met de oorspronkelijke portretlay-out na een reeks transformaties.

## Waarom Aspose.PSD gebruiken voor deze taak?
- **Volledige PSD‑ondersteuning** – werkt met lagen, maskers en aanpassingsobjecten.  
- **Geen native Photoshop vereist** – werkt op elke Java‑runtime.  
- **Eenvoudige API** – één enkele methodeaanroep (`rotateFlip`) behandelt rotatie en spiegelen.  
- **Eenvoudige formaatconversie** – exporteer direct naar JPEG, PNG of andere gangbare formaten.

## Vereisten

Before you start, make sure you have:

- **Aspose.PSD for Java** bibliotheek geïnstalleerd. Je kunt het downloaden en de volledige API‑referentie bekijken [hier](https://reference.aspose.com/psd/java/).  
- Een Java‑ontwikkelomgeving (JDK 8 of hoger).  
- Een voorbeeld‑PSD‑bestand dat je wilt draaien. Werk de variabele `sourceFile` in de code bij met het juiste pad naar je bestand.

## Pakketten importeren

Start by importing the necessary classes from the Aspose.PSD package:

```java
import com.aspose.psd.Image;
import com.aspose.psd.RotateFlipType;

import com.aspose.psd.imageoptions.JpegOptions;
```

## Hoe PSD te roteren – Stap 1: Laad de afbeelding

Create an `Image` instance that points to your source PSD file:

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";
Image image = Image.load(sourceFile);
```

## Hoe PSD te roteren – Stap 2: Draai de afbeelding 270 graden

Use the `rotateFlip` method with `RotateFlipType.Rotate270FlipNone` to achieve a 270‑degree rotation without any flipping:

```java
image.rotateFlip(RotateFlipType.Rotate270FlipNone);
```

> **Pro tip:** Als je de afbeelding ook horizontaal of verticaal wilt spiegelen, kies dan een andere `RotateFlipType` zoals `Rotate90FlipX` of `Rotate180FlipY`.

## Hoe PSD te roteren – Stap 3: Converteer PSD naar JPEG en sla op

After rotating, you can **convert PSD to JPEG** (or any other supported format) using the appropriate options class:

```java
String destName = dataDir + "RotatedImage_out.jpg";
image.save(destName, new JpegOptions());
```

Het bestand `RotatedImage_out.jpg` bevat nu de oorspronkelijke PSD‑inhoud die 270 graden is gedraaid en opgeslagen als een JPEG.

## Veelvoorkomende problemen en oplossingen

| Probleem | Oplossing |
|----------|-----------|
| **Afbeelding verschijnt ondersteboven** | Controleer of je `Rotate270FlipNone` hebt gebruikt. Voor een 90‑graden rotatie met de klok mee gebruik `Rotate90FlipNone`. |
| **Uitvoerbestand is beschadigd** | Zorg ervoor dat de doelmap bestaat en dat je schrijfrechten hebt. |
| **Licentie‑exception** | Installeer een tijdelijke of permanente Aspose.PSD‑licentie voordat je de afbeelding in productie laadt. |

## Veelgestelde vragen

**Q: Is Aspose.PSD compatibel met verschillende afbeeldingsformaten?**  
A: Ja, Aspose.PSD ondersteunt PSD, JPEG, PNG, BMP, GIF en vele andere rasterformaten.

**Q: Kan ik aangepaste rotaties toepassen, niet alleen vooraf gedefinieerde flips?**  
A: Absoluut! Terwijl `RotateFlipType` veelvoorkomende hoeken biedt, kun je meerdere aanroepen combineren of transformatie‑matrices gebruiken voor willekeurige hoeken.

**Q: Hoe converteer ik de gedraaide PSD naar een ander formaat, zoals PNG?**  
A: Vervang `JpegOptions` door `PngOptions` (of de juiste opties‑klasse) in de `save`‑methode.

**Q: Waar kan ik extra ondersteuning of hulp vinden?**  
A: Voor community‑hulp, bezoek het [Aspose.PSD Forum](https://forum.aspose.com/c/psd/34).

**Q: Is er een gratis proefversie beschikbaar?**  
A: Ja, je kunt Aspose.PSD verkennen met een [gratis proefversie](https://releases.aspose.com/).

**Q: Hoe verkrijg ik een tijdelijke licentie?**  
A: Als je een tijdelijke licentie nodig hebt, kun je er een krijgen [hier](https://purchase.aspose.com/temporary-license/).

## Conclusie

Je hebt nu geleerd hoe je **een afbeelding 270 graden draait** met Aspose.PSD voor Java, afbeeldingen spiegelt wanneer nodig, en het resultaat exporteert naar JPEG. Deze eenvoudige workflow kan worden geïntegreerd in grotere Java‑gebaseerde beeldverwerkings‑pijplijnen, waardoor je volledige controle krijgt over PSD‑manipulatie zonder Photoshop te gebruiken.

---

**Laatst bijgewerkt:** 2025-12-06  
**Getest met:** Aspose.PSD for Java 24.12  
**Auteur:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}