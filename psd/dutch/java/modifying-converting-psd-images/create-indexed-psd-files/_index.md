---
date: 2026-03-15
description: Leer hoe u PSD‑bestanden maakt, een PSD‑kleurenpalet genereert en de
  PSD‑kleurmodus instelt met Aspose.PSD voor Java in deze stapsgewijze handleiding.
linktitle: Create Indexed PSD Files using Aspose.PSD for Java
second_title: Aspose.PSD Java API
title: Hoe PSD-bestanden maken met Aspose.PSD voor Java
url: /nl/java/modifying-converting-psd-images/create-indexed-psd-files/
weight: 23
---

 exactly.

Now produce final content.{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Hoe PSD‑bestanden te maken met Aspose.PSD voor Java

## Introductie
Als je je ooit hebt afgevraagd **hoe je PSD**‑bestanden programmatisch kunt maken, ben je hier op de juiste plek. Aspose.PSD voor Java geeft je volledige controle over Photoshop‑documenten, zodat je PSD‑bestanden kunt genereren, bewerken en opslaan zonder ooit Photoshop te openen. In deze tutorial lopen we stap voor stap door het maken van een **geïndexeerde PSD**‑bestand, het instellen van de PSD‑kleurmodus en het genereren van een aangepast kleurenpalet — allemaal met duidelijke Java‑code. Of je nu een grafische pijplijn bouwt, asset‑creatie automatiseert of gewoon experimenteert, de concepten hier helpen je je visuele ideeën tot leven te brengen.

## Snelle antwoorden
- **Welke bibliotheek heb ik nodig?** Aspose.PSD voor Java  
- **Kan ik een geïndexeerde PSD maken?** Ja, door de kleurmodus in te stellen op `Indexed`  
- **Heb ik Photoshop geïnstalleerd nodig?** Nee, Aspose.PSD werkt onafhankelijk  
- **Welke Java‑versie is vereist?** JDK 8 of hoger  
- **Hoe groot kan het canvas zijn?** Elke grootte; dit voorbeeld gebruikt 500 × 500 px  

## Wat is een geïndexeerd PSD‑bestand?
Een geïndexeerde PSD slaat kleuren op in een palet in plaats van volledige kleurwaarden voor elke pixel. Dit verkleint de bestandsgrootte en is ideaal voor graphics met een beperkt aantal kleuren, zoals iconen of UI‑assets. Door een aangepast palet te genereren bepaal je precies welke kleuren in de uiteindelijke afbeelding verschijnen.

## Waarom een PSD‑kleurpalet genereren?
Het maken van een **PSD‑kleurpalet** stelt je in staat om:
- Bestandsgroottes klein te houden voor web‑ of mobiel gebruik  
- Consistente branding te waarborgen door kleuren te beperken tot je bedrijfs‑palet  
- De weergave te versnellen in toepassingen die geïndexeerde afbeeldingen ondersteunen  

## Vereisten
Voordat we in de code duiken, zorg dat je het volgende hebt:

1. **Basiskennis van Java** – je moet vertrouwd zijn met klassen, methoden en objectcreatie.  
2. **Java Development Kit (JDK) 8+** – geïnstalleerd en geconfigureerd in je IDE.  
3. **IDE (IntelliJ IDEA, Eclipse, enz.)** – optioneel maar sterk aanbevolen voor gemakkelijker debuggen.  
4. **Aspose.PSD for Java Library** – download het **[hier](https://releases.aspose.com/psd/java/)** en voeg de JAR toe aan de classpath van je project.  
5. **Fundamentele concepten van grafisch ontwerp** – begrip van kleurmodi, paletten en basisvormen helpt je de tutorial te volgen.  

## Importeer pakketten
Voordat we verder gaan met de code, laten we ervoor zorgen dat alle benodigde pakketten zijn geïmporteerd in je Java‑applicatie. Dit is wat je nodig hebt:

```java
import com.aspose.psd.Color;
import com.aspose.psd.Graphics;
import com.aspose.psd.Image;
import com.aspose.psd.Pen;
import com.aspose.psd.Rectangle;
import com.aspose.psd.fileformats.psd.ColorModes;
import com.aspose.psd.fileformats.psd.CompressionMethod;
import com.aspose.psd.fileformats.psd.PsdColorPalette;
import com.aspose.psd.imageoptions.PsdOptions;
import com.aspose.psd.sources.FileCreateSource;
```

Deze imports stellen je in staat om met PSD‑opties, kleuren en grafische manipulatie te werken via Aspose.PSD.

Laten we nu de code stap voor stap ontleden om **hoe je PSD**‑bestanden maakt met een geïndexeerde kleurmodus.

## Stap 1: Stel uw documentmap in
Definieer eerst waar de gegenereerde PSD wordt opgeslagen.

```java
String dataDir = "Your Document Directory";
```

Vervang `"Your Document Directory"` door een absoluut of relatief pad, bijv. `"/Users/YourName/Documents/"`.

## Stap 2: Maak een instantie van PsdOptions
`PsdOptions` bevat alle instellingen voor het bestand dat je gaat genereren.

```java
PsdOptions createOptions = new PsdOptions();
```

## Stap 3: Stel kerninstellingen van PsdOptions in
Hier specificeren we de uitvoerlokatie, de **set psd color mode** naar `Indexed`, en de PSD‑versie.

```java
createOptions.setSource(new FileCreateSource(dataDir + "Newsample_out.psd", false));
createOptions.setColorMode(ColorModes.Indexed);
createOptions.setVersion(5);
```

- **Bron** – het volledige pad van het nieuwe bestand.  
- **Kleurmodus** – `Indexed` vertelt Aspose.PSD om een palet‑gebaseerde afbeelding te gebruiken.  
- **Versie** – PSD‑formaatversie (5 werkt voor de meeste moderne Photoshop‑versies).  

## Stap 4: Maak een kleurpalet (Genereer PSD‑kleurpalet)
Definieer de kleuren die beschikbaar zullen zijn in de geïndexeerde afbeelding.

```java
Color[] palette = { Color.getRed(), Color.getGreen(), Color.getBlue(), Color.getYellow() };
createOptions.setPalette(new PsdColorPalette(palette));
createOptions.setCompressionMethod(CompressionMethod.RLE);
```

- De `palette`‑array bevat maximaal 256 `Color`‑objecten.  
- `CompressionMethod.RLE` biedt efficiënte verliesloze compressie voor geïndexeerde afbeeldingen.

## Stap 5: Maak het PSD‑beeldcanvas
Nu maken we een lege PSD met de gewenste afmetingen.

```java
Image psd = Image.create(createOptions, 500, 500);
```

Dit creëert een canvas van 500 × 500 pixel dat het eerder gedefinieerde palet gebruikt.

## Stap 6: Teken graphics op de PSD
Voeg visuele inhoud toe — hier tekenen we een eenvoudige rode ellips op een witte achtergrond.

```java
Graphics graphics = new Graphics(psd);
graphics.clear(Color.getWhite());
graphics.drawEllipse(new Pen(Color.getRed(), 6), new Rectangle(0, 0, 400, 400));
```

- `clear(Color.getWhite())` vult de achtergrond met wit.  
- `drawEllipse` tekent een rode ellips met een 6‑pixel lijn.

## Stap 7: Sla het PSD‑bestand op
Sla tenslotte de afbeelding op schijf op.

```java
psd.save();
```

Het bestand `Newsample_out.psd` verschijnt in de map die je eerder hebt opgegeven.

## Algemene problemen & tips
- **Paletgrootte** – Als je meer dan 4 kleuren nodig hebt, voeg ze dan eenvoudig toe aan de `palette`‑array (maximaal 256).  
- **Bestandsrechten** – Zorg ervoor dat het Java‑proces schrijfrechten heeft op `dataDir`.  
- **Onjuiste kleurmodus** – Het vergeten van `createOptions.setColorMode(ColorModes.Indexed)` resulteert in een RGB‑PSD in plaats van een geïndexeerde.  

## Veelgestelde vragen

**Q: Wat is Aspose.PSD voor Java?**  
A: Aspose.PSD voor Java is een bibliotheek die programmatische manipulatie van PSD (Photoshop)‑bestanden mogelijk maakt met Java.

**Q: Kan ik Aspose.PSD gratis gebruiken?**  
A: Ja, je kunt een gratis proefversie van Aspose.PSD **[hier](https://releases.aspose.com/)** downloaden.

**Q: Heb ik Photoshop geïnstalleerd nodig om met Aspose.PSD te werken?**  
A: Nee, je kunt PSD‑bestanden maken en manipuleren zonder Photoshop, omdat Aspose.PSD alle bewerkingen onafhankelijk afhandelt.

**Q: Hoe verkrijg ik een tijdelijke licentie voor Aspose.PSD?**  
A: Je kunt een tijdelijke licentie aanvragen **[hier](https://purchase.aspose.com/temporary-license/)**.

**Q: Waar kan ik ondersteuning krijgen voor Aspose.PSD?**  
A: Je kunt ondersteuning krijgen via het Aspose‑forum **[hier](https://forum.aspose.com/c/psd/34)**.

## Conclusie
Je hebt zojuist geleerd **hoe je PSD**‑bestanden maakt met een geïndexeerde kleurmodus, een aangepast palet genereert en eenvoudige graphics toevoegt — allemaal met Aspose.PSD voor Java. Met deze bouwblokken kun je uitbreiden naar complexere tekeningen, lagenbeheer en batchverwerking. Voor een diepere verkenning, bekijk de officiële API‑referentie **[hier](https://reference.aspose.com/psd/java/)** en blijf experimenteren met verschillende paletten en teken‑primitieven.

---

**Last Updated:** 2026-03-15  
**Tested With:** Aspose.PSD for Java 24.12 (latest)  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}