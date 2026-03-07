---
date: 2026-03-07
description: Leer hoe je tekst aan PSD‑bestanden kunt toevoegen tijdens runtime met
  Java en Aspose.PSD. Volg deze stapsgewijze handleiding om snel een tekstlaag in
  een PSD te maken.
linktitle: Add Text Layer on Runtime in PSD Files using Java
second_title: Aspose.PSD Java API
title: Tekst toevoegen aan PSD‑bestanden tijdens runtime met Java
url: /nl/java/modifying-converting-psd-images/add-text-layer-runtime-psd-files/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Tekst toevoegen aan PSD‑bestanden tijdens runtime met Java

## Inleiding
Als je ooit handmatig een Photoshop‑document hebt bewerkt, weet je hoe krachtig lagen kunnen zijn. Wat als je **tekst aan PSD‑bestanden** automatisch kunt toevoegen vanuit je Java‑applicatie? Met de Aspose.PSD for Java‑bibliotheek kun je tijdens runtime een tekstlaag in een PSD maken, waardoor batch‑verwerking, dynamische grafiekgeneratie en geautomatiseerde branding‑workflows mogelijk worden. In deze tutorial lopen we het volledige proces door, van het opzetten van het project tot het opslaan van het bijgewerkte bestand.

## Snelle antwoorden
- **Welke bibliotheek heb ik nodig?** Aspose.PSD for Java.  
- **Kan ik tekst toevoegen aan een bestaande PSD?** Ja – laad simpelweg het bestand, voeg een `TextLayer` toe en sla op.  
- **Heb ik een licentie nodig voor productie?** Een commerciële licentie is vereist voor niet‑evaluatiegebruik.  
- **Welke Java‑versie wordt ondersteund?** JDK 8 of hoger (we raden de nieuwste LTS aan).  
- **Is dit geschikt voor web‑back‑ends?** Absoluut – de API werkt in elke Java‑gebaseerde serveromgeving.

## Wat betekent “tekst toevoegen aan PSD”?
Tekst toevoegen aan een PSD betekent programmatiche een nieuwe tekstlaag aanmaken binnen een Photoshop‑document. De laag gedraagt zich als elke andere Photoshop‑tekstlaag: je kunt hem verplaatsen, de inhoud bewerken en styling toepassen – alles zonder Photoshop te openen.

## Waarom een tekstlaag in een PSD maken met Java?
- **Automatisering** – Genereer marketing‑assets, watermerken of productlabels in bulk.  
- **Consistentie** – Zorg voor dezelfde lettertype, grootte en positionering in duizenden bestanden.  
- **Integratie** – Combineer met andere Java‑services (e‑commerce, rapportage, CI‑pipelines) om grafieken on‑the‑fly te leveren.

## Vereisten
Voordat je code schrijft, zorg dat je het volgende hebt:

1. **Java Development Kit (JDK)** – Installeer JDK 8 of nieuwer. Je kunt [het hier downloaden](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).  
2. **Aspose.PSD for Java** – Haal de nieuwste JAR van de [Aspose releases‑pagina](https://releases.aspose.com/psd/java/).  
3. **IDE (optioneel maar handig)** – IntelliJ IDEA, Eclipse of een andere editor naar keuze.  
4. **Basiskennis van Java** – Je moet vertrouwd zijn met klassen, objecten en bestands‑I/O.  
5. **Een voorbeeld‑PSD** – Voor deze gids gebruiken we `OneLayer.psd` geplaatst in een map naar keuze.

## Pakketten importeren
Importeer eerst de klassen die je nodig hebt om met PSD‑bestanden en tekstlagen te werken.

```java
import com.aspose.psd.Image;
import com.aspose.psd.Rectangle;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.TextLayer;
```

Deze imports geven je toegang tot de kernfunctionaliteit van Aspose.PSD.

## Stapsgewijze handleiding

### Stap 1: Stel je documentmap in
Definieer de map die je bron‑PSD bevat en waar de uitvoer wordt opgeslagen.

```java
String dataDir = "Your Document Directory"; 
```

Vervang `"Your Document Directory"` door het absolute of relatieve pad naar je bestanden.

### Stap 2: Laad je bron‑PSD‑bestand
Breng de bestaande PSD in het geheugen met `Image.load()`.

```java
String sourceFileName = dataDir + "OneLayer.psd"; 
Image img = Image.load(sourceFileName);
```

Als het pad correct is, vertegenwoordigt `img` nu het geladen Photoshop‑document.

### Stap 3: Cast naar `PsdImage`
Aangezien we Photoshop‑specifieke functies gebruiken, casten we de generieke `Image` naar `PsdImage`.

```java
PsdImage im = (PsdImage)img;
```

De cast maakt methoden zoals `addTextLayer()` beschikbaar.

### Stap 4: Definieer de rechthoek voor de tekstlaag
Geef aan waar de nieuwe tekst moet verschijnen. De rechthoek bepaalt positie (x, y) en grootte (breedte, hoogte).

```java
Rectangle rect = new Rectangle(
    (int)(im.getWidth() * 0.25),
    (int)(im.getHeight() * 0.25),
    (int)(im.getWidth() * 0.5),
    (int)(im.getHeight() * 0.5)
);
```

Pas de berekeningen gerust aan om aan je lay‑outbehoeften te voldoen.

### Stap 5: Voeg de tekstlaag toe
Maak de daadwerkelijke tekstlaag binnen de gedefinieerde rechthoek.

```java
TextLayer layer = im.addTextLayer("Added text", rect);
```

Vervang `"Added text"` door elke string die je in de PSD wilt laten verschijnen. Dit is waar we **tekstlaag PSD** programmatiche creëren.

### Stap 6: Sla je bijgewerkte PSD‑bestand op
Schrijf het gewijzigde document naar een nieuw bestand zodat je het origineel niet overschrijft.

```java
String psdPath = dataDir + "ImageWithTextLayer.psd";
im.save(psdPath);
```

Na uitvoering vind je `ImageWithTextLayer.psd` in de doelmap, nu met de nieuwe tekstlaag.

## Veelvoorkomende problemen & oplossingen
| Probleem | Reden | Oplossing |
|----------|-------|-----------|
| **`NullPointerException` op `im.addTextLayer`** | PSD niet correct geladen (verkeerd pad). | Controleer of `sourceFileName` naar een bestaand PSD‑bestand wijst. |
| **Tekst niet zichtbaar** | Rechthoek buiten het canvas geplaatst of laag verborgen. | Pas de coördinaten van de rechthoek aan of controleer de zichtbaarheid met `layer.setVisible(true)`. |
| **LicenseException** | Bibliotheek wordt zonder geldige licentie in productie gebruikt. | Schaf een commerciële licentie aan en stel deze in via `License license = new License(); license.setLicense("Aspose.PSD.lic");`. |

## Veelgestelde vragen

**V: Kan ik meerdere tekstlagen toevoegen?**  
A: Ja – herhaal simpelweg Stappen 4 en 5 voor elke tekst die je wilt invoegen.

**V: Hoe style ik de tekst (lettertype, grootte, kleur)?**  
A: De `TextLayer`‑klasse biedt een `getTextData()`‑methode waarmee je `Font`, `FontSize`, `Color` en andere stijl‑eigenschappen kunt aanpassen. Raadpleeg de Aspose.PSD API‑documentatie voor volledige details.

**V: Wat als mijn PSD al veel lagen heeft?**  
A: Aspose.PSD werkt met complexe laagstructuren. Je kunt specifieke groepen targeten of de nieuwe tekstlaag op een gewenste index invoegen met overloads van `addTextLayer`.

**V: Is deze aanpak geschikt voor webapplicaties?**  
A: Absoluut. Zolang je server Java draait, kun je PSD‑bestanden on‑the‑fly genereren of aanpassen en aan cliënten leveren.

**V: Waar kan ik hulp krijgen als ik problemen ondervind?**  
A: Bezoek de [Aspose support forums](https://forum.aspose.com/c/psd/34) waar zowel de community als Aspose‑engineers je kunnen assisteren.

## Conclusie
Je hebt nu gezien hoe eenvoudig het is om **tekst aan PSD‑bestanden** toe te voegen tijdens runtime met Java en Aspose.PSD. Deze techniek stelt je in staat grafiekcreatie te automatiseren, assets te personaliseren en Photoshop‑niveau bewerkingen te integreren in elke Java‑gebaseerde oplossing. Verken de rest van de Aspose.PSD API om vormen, rasterlagen of zelfs filters toe te voegen voor nog rijkere automatisering.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Laatst bijgewerkt:** 2026-03-07  
**Getest met:** Aspose.PSD for Java 24.12 (latest at time of writing)  
**Auteur:** Aspose  

---