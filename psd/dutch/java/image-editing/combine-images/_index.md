---
date: 2025-12-30
description: Leer hoe je een PSD‑bestand in Java maakt door twee afbeeldingen te combineren
  met Aspose.PSD. Volg onze stapsgewijze handleiding om afbeeldingen snel samen te
  voegen tot een PSD‑bestand.
linktitle: Combine Images
second_title: Aspose.PSD Java API
title: Hoe een PSD‑bestand te maken in Java – Afbeeldingen combineren met Aspose.PSD
url: /nl/java/image-editing/combine-images/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# PSD-bestand maken in Java – Afbeeldingen combineren met Aspose.PSD

## Inleiding

Als je een **PSD-bestand in Java** moet maken door meerdere afbeeldingen te combineren, maakt Aspose.PSD het werk eenvoudig. In deze tutorial lopen we stap voor stap door het combineren van twee afbeeldingen tot één PSD-canvas, leggen we uit waarom deze aanpak nuttig is, en geven we kant‑klaar code. Aan het einde kun je **twee afbeeldingen combineren in Java** stijl en een professioneel uitziend gelaagd bestand genereren.

## Snelle antwoorden
- **Welke bibliotheek is het beste voor het combineren van afbeeldingen in een PSD?** Aspose.PSD for Java.
- **Hoe lang duurt de implementatie?** Ongeveer 10‑15 minuten voor een eenvoudige combinatie.
- **Heb ik een licentie nodig?** Een gratis proefversie werkt voor testen; een commerciële licentie is vereist voor productie.
- **Kan ik meer dan twee afbeeldingen toevoegen?** Ja – herhaal de `drawImage`‑aanroepen voor elke extra laag.
- **Welke Java‑versie wordt ondersteund?** Java 8 en nieuwer.

## Vereisten

Zorg er voordat je begint voor dat je het volgende hebt:

1. **Aspose.PSD Library** – download deze van [here](https://releases.aspose.com/psd/java/).  
2. **Java Development Kit (JDK)** – Java 8+ wordt aanbevolen.  
3. **Document Directory** – een map op je computer waar de bronafbeeldingen en de resulterende PSD worden opgeslagen.

## Importeer pakketten

Begin met het importeren van de benodigde Aspose.PSD‑klassen in je project:

```java
import com.aspose.psd.Color;
import com.aspose.psd.Graphics;
import com.aspose.psd.Image;

import com.aspose.psd.imageoptions.PsdOptions;
import com.aspose.psd.sources.FileCreateSource;
```

## Stapsgewijze handleiding

### Stap 1: PSD‑opties maken (het bestand voorbereiden)

We maken eerst een `PsdOptions`‑instantie die de uitvoerinstellingen bevat.

```java
PsdOptions imageOptions = new PsdOptions();
```

### Stap 2: FileCreateSource instellen (definieer waar de PSD wordt opgeslagen)

Wijs een `FileCreateSource` toe aan de opties, wijzend naar het gewenste resultaatbestand.

```java
imageOptions.setSource(new FileCreateSource(dataDir + "Two_images_result_out.psd", false));
```

### Stap 3: Image‑instantie maken (canvasgrootte initialiseren)

Maak een `Image`‑object met de opties en specificeer een canvas van 600 × 600 pixels.

```java
Image image = Image.create(imageOptions, 600, 600);
```

### Stap 4: Graphics initialiseren en de eerste afbeelding tekenen

Een `Graphics`‑object stelt ons in staat om op het canvas te tekenen. We maken de achtergrond wit en tekenen de eerste bronafbeelding op de linkerde helft.

```java
Graphics graphics = new Graphics(image);
graphics.clear(Color.getWhite());
graphics.drawImage(Image.load(dataDir + "example1.psd"), 0, 0, 300, 600);
```

### Stap 5: De tweede afbeelding tekenen (de combinatie voltooien)

Nu plaatsen we de tweede afbeelding op de rechterhelft van hetzelfde canvas.

```java
graphics.drawImage(Image.load(dataDir + "example2.psd"), 300, 0, 300, 600);
```

### Stap 6: Het resulterende PSD‑bestand opslaan

Sla tenslotte het gecombineerde canvas op schijf op.

```java
image.save();
```

Gefeliciteerd! Je hebt met succes **afbeeldingen samengevoegd in PSD** en een PSD‑bestand in Java gemaakt.

## Waarom afbeeldingen combineren met Aspose.PSD?

- **Laag‑bewust** – elke `drawImage`‑aanroep voegt een aparte laag toe die later bewerkt kan worden.  
- **Formaatflexibiliteit** – ondersteunt PSD, PNG, JPEG, BMP en meer.  
- **Geen native afhankelijkheden** – pure Java, werkt op elk OS dat de JDK draait.

## Veelvoorkomende problemen en oplossingen

| Probleem | Oorzaak | Oplossing |
|----------|---------|-----------|
| `File not found`‑fout bij het laden van bronafbeeldingen | Onjuist `dataDir`‑pad | Controleer of `dataDir` wijst naar de map die `example1.psd` en `example2.psd` bevat. |
| Uitvoer‑PSD is leeg | `graphics.clear` aangeroepen na het tekenen | Zorg ervoor dat `graphics.clear(Color.getWhite())` **voor** alle `drawImage`‑aanroepen wordt uitgevoerd. |
| Licentie‑exception tijdens runtime | Ontbrekende of verlopen Aspose.PSD‑licentie | Pas een geldige licentie toe met `License license = new License(); license.setLicense("Aspose.PSD.lic");` vóór elke API‑aanroep. |

## Veelgestelde vragen

### Q1: Is Aspose.PSD compatibel met alle afbeeldingsformaten?
**A1:** Aspose.PSD richt zich voornamelijk op het PSD‑bestandformaat. Het ondersteunt echter verschillende andere formaten voor invoer en uitvoer.

### Q2: Kan ik extra bewerkingen uitvoeren op de gecombineerde afbeelding?
**A2:** Zeker! Na het combineren van afbeeldingen kun je de resulterende PSD verder bewerken met de uitgebreide functies van Aspose.PSD.

### Q3: Zijn er licentie‑vereisten voor het gebruik van Aspose.PSD?
**A3:** Ja, een geldige licentie is vereist voor commercieel gebruik. Verkrijg deze via [here](https://purchase.aspose.com/buy).

### Q4: Is er een gratis proefversie beschikbaar voor Aspose.PSD?
**A4:** Ja, je kunt Aspose.PSD verkennen met een gratis proefversie [here](https://releases.aspose.com/).

### Q5: Waar kan ik ondersteuning vinden voor vragen over Aspose.PSD?
**A5:** Bezoek het [Aspose.PSD forum](https://forum.aspose.com/c/psd/34) voor community‑ondersteuning en discussies.

---

**Laatst bijgewerkt:** 2025-12-30  
**Getest met:** Aspose.PSD 24.11 for Java  
**Auteur:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}