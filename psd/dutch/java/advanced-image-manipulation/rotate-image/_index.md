---
date: 2026-02-12
description: Leer hoe je een afbeelding draait en hoe je een afbeelding 270 graden
  draait met Aspose.PSD voor Java. Deze gids behandelt het roteren van PSD‑bestanden,
  het spiegelen van afbeeldingen en het converteren van PSD naar JPEG zonder Photoshop.
linktitle: Rotate Image 270 Degrees
second_title: Aspose.PSD Java API
title: Hoe een afbeelding 270 graden te roteren met Aspose.PSD voor Java
url: /nl/java/advanced-image-manipulation/rotate-image/
weight: 19
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Afbeelding 270 graden draaien met Aspose.PSD voor Java

## Introductie

In deze **java image processing tutorial**, ontdek je **hoe je een afbeelding draait** 270 graden snel en betrouwbaar met Aspose.PSD voor Java. Of je nu een foto‑bewerkings‑tool bouwt, batch‑conversies automatiseert, of gewoon een PSD‑laag opnieuw moet oriënteren, de bibliotheek maakt de taak moeiteloos. We zullen ook ingaan op **flip image java** technieken en het converteren van de gedraaide PSD naar een JPEG, zodat je een volledige end‑to‑end workflow krijgt zonder Photoshop.

## Snelle antwoorden
- **Welke bibliotheek behandelt de rotatie?** Aspose.PSD for Java  
- **Welke rotatiehoek gebruikt het voorbeeld?** 270 degrees  
- **Kan ik de afbeelding ook spiegelen?** Yes – use `RotateFlipType` options like `Rotate90FlipX`  
- **Hoe sla ik het resultaat op?** In the example we save as JPEG using `JpegOptions`  
- **Heb ik een licentie nodig voor productie?** A valid Aspose.PSD license is required for commercial use  

## Wat is “rotate image 270 degrees”?
Roteren van een afbeelding 270 graden betekent dat je de foto drie‑kwart van een volledige cirkel met de klok mee draait (of 90 graden tegen de klok in). In veel grafische‑bewerkingsscenario's komt deze oriëntatie overeen met de oorspronkelijke portretlay-out na een reeks transformaties.

## Waarom Aspose.PSD gebruiken voor deze taak?
- **Volledige PSD‑ondersteuning** – werkt met lagen, maskers en aanpassingsobjecten.  
- **Geen native Photoshop vereist** – werkt op elke Java‑runtime.  
- **Eenvoudige API** – een enkele methodeaanroep (`rotateFlip`) verwerkt rotatie en spiegelen.  
- **Eenvoudige formaatconversie** – exporteer direct naar JPEG, PNG of andere gangbare formaten.

## Hoe een afbeelding draaien met Aspose.PSD voor Java
Hieronder vind je een stap‑voor‑stap‑gids die je begeleidt bij het laden van een PSD, het toepassen van een 270°‑rotatie, eventueel het spiegelen van de afbeelding, en uiteindelijk het opslaan van het resultaat als JPEG.

### Voorvereisten

Voordat je begint, zorg dat je het volgende hebt:

- **Aspose.PSD for Java** library geïnstalleerd. Je kunt het downloaden en de volledige API‑referentie bekijken [hier](https://reference.aspose.com/psd/java/).  
- Een Java‑ontwikkelomgeving (JDK 8 of hoger).  
- Een voorbeeld‑PSD‑bestand dat je wilt draaien. Werk de variabele `sourceFile` in de code bij met het juiste pad naar jouw bestand.

### Importeer pakketten

Begin met het importeren van de benodigde klassen uit het Aspose.PSD‑pakket:

```java
import com.aspose.psd.Image;
import com.aspose.psd.RotateFlipType;

import com.aspose.psd.imageoptions.JpegOptions;
```

### Stap 1: Laad de afbeelding

Maak een `Image`‑instantie die naar je bron‑PSD‑bestand wijst:

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";
Image image = Image.load(sourceFile);
```

### Stap 2: Draai de afbeelding 270 graden

Gebruik de `rotateFlip`‑methode met `RotateFlipType.Rotate270FlipNone` om een rotatie van 270 graden te bereiken zonder enige spiegeling:

```java
image.rotateFlip(RotateFlipType.Rotate270FlipNone);
```

> **Pro tip:** Als je de afbeelding ook horizontaal of verticaal wilt spiegelen, kies dan een andere `RotateFlipType` zoals `Rotate90FlipX` of `Rotate180FlipY`. Dit is de meest voorkomende manier om **flip image java** bewerkingen uit te voeren.

### Stap 3: Converteer PSD naar JPEG en sla op

Na het draaien kun je **convert PSD to JPEG** (of elk ander ondersteund formaat) gebruiken met de juiste opties‑klasse:

```java
String destName = dataDir + "RotatedImage_out.jpg";
image.save(destName, new JpegOptions());
```

Het bestand `RotatedImage_out.jpg` bevat nu de oorspronkelijke PSD‑inhoud gedraaid 270 graden en opgeslagen als een JPEG.

## Waarom dit belangrijk is – Praktische toepassingen
- **Batchverwerking van productcatalogi** – draai tientallen PSD‑assets naar een uniforme oriëntatie vóór publicatie.  
- **Geautomatiseerde thumbnail‑generatie** – maak correct georiënteerde previews voor webgalerijen zonder Photoshop te openen.  
- **Mobiele app‑back‑ends** – heroriënteer door gebruikers geüploade PSD‑bestanden aan de serverzijde met pure Java.

## Veelvoorkomende valkuilen & probleemoplossing

| Probleem | Oplossing |
|----------|-----------|
| **Image appears upside‑down** | Verify you used `Rotate270FlipNone`. For a 90‑degree clockwise rotation use `Rotate90FlipNone`. |
| **Output file is corrupted** | Ensure the destination folder exists and you have write permissions. |
| **License exception** | Install a temporary or permanent Aspose.PSD license before loading the image in production. |
| **Need to rotate image without Photoshop** | This API performs the rotation entirely in code, removing the Photoshop dependency. |
| **Want to flip image as part of the same operation** | Use other `RotateFlipType` values such as `Rotate90FlipX` (covers **how to flip image**). |

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
A: Ja, je kunt Aspose.PSD verkennen met een [free trial](https://releases.aspose.com/).

**Q: Hoe verkrijg ik een tijdelijke licentie?**  
A: Als je een tijdelijke licentie nodig hebt, kun je er een verkrijgen [hier](https://purchase.aspose.com/temporary-license/).

**Q: Werkt deze aanpak op headless servers?**  
A: Ja, Aspose.PSD for Java draait in elke standaard JVM‑omgeving, waardoor het ideaal is voor CI/CD‑pijplijnen of cloud‑functies.

## Conclusie

Je hebt nu geleerd **hoe je een afbeelding draait** 270 graden met Aspose.PSD voor Java, hoe je **flip image** toepast wanneer nodig, en hoe je het resultaat exporteert naar JPEG. Deze eenvoudige workflow kan worden geïntegreerd in grotere Java‑gebaseerde beeldverwerkings‑pijplijnen, waardoor je volledige controle krijgt over PSD‑manipulatie zonder afhankelijk te zijn van Photoshop.

---

**Last Updated:** 2026-02-12  
**Tested With:** Aspose.PSD for Java 24.12  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}