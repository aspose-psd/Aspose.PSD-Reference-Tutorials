---
date: 2026-02-12
description: Leer hoe je een afbeelding onder een specifieke hoek kunt roteren in
  Java met Aspose.PSD. Deze gids laat zien hoe je een afbeelding roteert, een afbeelding
  roteert met graden, en hoe je achtergrondkleuren afhandelt.
linktitle: How to Rotate Image on a Specific Angle
second_title: Aspose.PSD Java API
title: Hoe een afbeelding te roteren op een specifieke hoek met Aspose.PSD voor Java
url: /nl/java/advanced-image-manipulation/rotate-image-specific-angle/
weight: 20
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Hoe een afbeelding op een specifieke hoek te roteren met Aspose.PSD voor Java

## Introductie

Als je **hoe een afbeelding te roteren** programmatically in een Java‑applicatie moet doen, biedt Aspose.PSD voor Java een nette, high‑performance API die het zware werk uit handen neemt. Of je nu een foto‑editor bouwt, thumbnails genereert, of assets voorbereidt voor een webservice, een afbeelding met een exacte graad roteren is een veelvoorkomende eis. In deze tutorial lopen we het volledige proces door — van het laden van een PSD‑bestand tot het opslaan van het geroteerde resultaat—en belichten we best practices zoals caching en achtergrondafhandeling.

## Snelle antwoorden
- **Welke bibliotheek is het beste voor het roteren van afbeeldingen in Java?** Aspose.PSD voor Java.  
- **Kan ik roteren met elke graad?** Ja, de `rotate`‑methode accepteert een `float`‑hoek (positief of negatief).  
- **Heb ik een licentie nodig voor ontwikkeling?** Een gratis proefversie werkt voor testen; een licentie is vereist voor productie.  
- **Welke afbeeldingsformaten worden ondersteund?** PSD, JPEG, PNG, TIFF, GIF, BMP en nog veel meer.  
- **Hoe stel ik een achtergrondkleur in voor lege ruimte?** Geef een `Color`‑instantie door aan de `rotate`‑methode.

## Wat is afbeeldingsrotatie in Java?

Afbeeldingsrotatie betekent het draaien van de pixelmatrix rond een draaipunt (meestal het centrum) met een opgegeven hoek. In Java kun je dit handmatig doen met `Graphics2D`, maar Aspose.PSD abstraheert de wiskunde, behandelt verschillende kleurdieptes en behoudt laaginformatie bij het werken met PSD‑bestanden.

## Waarom Aspose.PSD gebruiken voor het roteren van afbeeldingen?

- **Precisie:** Roteer met elke fractiegraad zonder kwaliteitsverlies.  
- **Prestaties:** Ingebouwde caching (`image.cacheData()`) versnelt grote bestanden.  
- **Achtergrondcontrole:** Specificeer een achtergrondkleur om de gaten die door rotatie ontstaan op te vullen.  
- **Formaatflexibiliteit:** Laad PSD, exporteer JPEG, PNG of elk ondersteund formaat.

## Voorvereisten

Zorg ervoor dat je het volgende hebt:

1. **Java Development Kit (JDK 8 of later)** – een werkende Java‑IDE of command‑line‑setup.  
2. **Aspose.PSD voor Java** – download de nieuwste JAR van de [Aspose.PSD Java‑pagina](https://reference.aspose.com/psd/java/).  
3. **Voorbeeld‑PSD‑bestand** – bijv. `sample.psd` geplaatst in een map die je vanuit je code kunt refereren.

## Importpakketten

Eerst importeren we de klassen die we nodig hebben. Deze imports blijven hetzelfde, ongeacht de rotatiehoek die je kiest.

```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.imageoptions.JpegOptions;
```

## Stapsgewijze handleiding

### Stap 1: Definieer je documentdirectory

Stel de map in die de bron‑PSD bevat en waar de output wordt weggeschreven.

```java
String dataDir = "Your Document Directory";
```

> **Pro tip:** Gebruik een absoluut pad of `System.getProperty("user.dir")` om verrassingen met relatieve paden te voorkomen.

### Stap 2: Specificeer bron‑ en bestemmings‑bestandspaden

```java
String sourceFile = dataDir + "sample.psd";
String destName = dataDir + "RotatingImageOnSpecificAngle_out.jpg";
```

Je kunt `destName` wijzigen naar elke ondersteunde extensie (`.png`, `.tiff`, enz.) afhankelijk van je outputbehoeften.

### Stap 3: Laad de afbeelding

```java
RasterImage image = (RasterImage)Image.load(sourceFile);
```

`Image.load` detecteert automatisch het bestandsformaat en retourneert een concrete `RasterImage` voor raster‑gebaseerde bewerkingen.

### Stap 4: Cache afbeeldingsgegevens (optioneel maar aanbevolen)

```java
if (!image.isCached())
{
    image.cacheData();
}
```

Caching slaat de afbeeldingspixels in het geheugen op, waardoor latere transformaties sneller verlopen — vooral nuttig bij grote PSD‑bestanden.

### Stap 5: Roteer de afbeelding

```java
image.rotate(20f, true, Color.getRed());
```

- **20f** – de rotatiehoek in graden (float). Wijzig deze waarde om met elke hoek te roteren, bijv. `-45f` voor tegen de klok in.  
- **true** – behoudt de oorspronkelijke beeldverhouding terwijl het canvas wordt uitgebreid om de geroteerde afbeelding te passen.  
- **Color.getRed()** – achtergrondkleur die de lege hoeken vult die door de rotatie ontstaan. Vervang door `Color.getWhite()` of een andere aangepaste kleur indien nodig.

#### Afbeelding roteren met graden in Java

De `rotate`‑methode accepteert elke floating‑point‑waarde, zodat je **afbeelding roteren met graden** kunt, zoals `30f`, `90f` of `-15f`. Positieve waarden roteren met de klok mee, negatieve waarden roteren tegen de klok in.

#### Specifieke rotatiehoek gebruiken met Aspose.PSD

Omdat de methode werkt met een `float`, kun je een **rotatiehoek specifiek instellen** zoals `22.5f` voor precieze controle in grafisch‑ontwerpprocessen.

#### Samenvatting voorbeeld Java‑rotatie

Alle bovenstaande stappen demonstreren een volledige **rotate image java** workflow — van het laden van het bestand tot het opslaan van de geroteerde output.

### Stap 6: Sla het resultaat op

```java
image.save(destName, new JpegOptions());
```

`JpegOptions` stelt je in staat de kwaliteit, compressie en andere JPEG‑specifieke instellingen te regelen. Voor lossless output, verwissel met `PngOptions`.

## Veelvoorkomende problemen en oplossingen

| Probleem | Oorzaak | Oplossing |
|----------|---------|-----------|
| **Lege hoeken na rotatie** | Geen achtergrondkleur opgegeven | Geef een `Color` (bijv. `Color.getWhite()`) door aan `rotate`. |
| **Out‑of‑memory‑fout bij grote PSD’s** | Afbeelding niet gecached | Roep `image.cacheData()` aan vóór verwerking. |
| **Onjuiste draairichting** | Verwarring tussen negatieve en positieve hoek | Gebruik negatieve waarden voor rotatie met de klok mee (of omgekeerd, afhankelijk van je coördinatensysteem). |
| **Niet‑opgeslagen wijzigingen** | Vergeten `save` aan te roepen | Zorg dat `image.save(...)` wordt uitgevoerd na rotatie. |

## Veelgestelde vragen

**Q: Kan ik afbeeldingen met transparantie roteren met Aspose.PSD voor Java?**  
A: Ja. De bibliotheek behoudt alfakanalen; vermijd het specificeren van een ondoorzichtige achtergrondkleur als je transparante hoeken wilt.

**Q: Zijn er beperkingen qua ondersteunde afbeeldingsformaten voor rotatie?**  
A: Nee. Aspose.PSD ondersteunt PSD, JPEG, PNG, TIFF, GIF, BMP, JPEG2000, WMF, EMF en nog veel meer.

**Q: Kan ik afbeeldingen roteren met een negatieve hoek?**  
A: Absoluut. Geef een negatieve float door aan `rotate` (bijv. `-30f`) om met de klok mee te roteren.

**Q: Biedt Aspose.PSD realtime‑voorbeeld van de afbeelding tijdens rotatie?**  
A: De API werkt alleen server‑side. Voor live‑voorbeelden kun je de geroteerde bitmap integreren in een UI‑framework (Swing, JavaFX) en de weergave verversen.

**Q: Is er een community‑forum voor Aspose.PSD waar ik hulp kan zoeken?**  
A: Ja, bezoek het [Aspose.PSD‑forum](https://forum.aspose.com/c/psd/34) om vragen te stellen en ervaringen te delen.

## Conclusie

Je weet nu **hoe een afbeelding te roteren** op een specifieke hoek met Aspose.PSD voor Java. Door gebruik te maken van caching, achtergrondkleurcontrole en flexibele outputopties kun je precieze rotatiefuncties integreren in elke Java‑gebaseerde afbeeldingsworkflow.

---

**Laatst bijgewerkt:** 2026-02-12  
**Getest met:** Aspose.PSD voor Java 24.11 (latest at time of writing)  
**Auteur:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}