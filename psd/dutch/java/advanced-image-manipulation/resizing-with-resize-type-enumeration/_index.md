---
date: 2026-02-12
description: Leer hoe je een afbeelding kunt verkleinen in Java met Aspose.PSD voor
  Java. Stapsgewijze handleiding met de Resize Type‑enumeratie, plus tips voor het
  converteren van PSD naar JPEG.
linktitle: Resizing with Resize Type Enumeration
second_title: Aspose.PSD Java API
title: Afbeelding schalen Java - Gebruik van Resize Type‑enumeratie in Aspose.PSD
  voor Java
url: /nl/java/advanced-image-manipulation/resizing-with-resize-type-enumeration/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Resize Image Java: Gebruik van Resize Type Enumeration in Aspose.PSD voor Java

## Inleiding

Het wijzigen van de grootte van afbeeldingen is een veelvoorkomende vereiste in Java‑toepassingen, en **resize image java**‑bewerkingen worden moeiteloos met Aspose.PSD. In deze tutorial leer je hoe je **resize image java** kunt gebruiken met de krachtige Resize Type Enumeration, en zie je ook hoe je **convert psd to jpeg** kunt uitvoeren na het wijzigen van de grootte. Of je nu een desktop‑tool of een server‑side service bouwt, deze stappen helpen je om afbeeldingsafmetingen betrouwbaar te beheren en een hoogwaardige afbeelding‑grootte‑aanpassing te bereiken.

## Snelle Antwoorden
- **Welke bibliotheek behandelt resize image java?** Aspose.PSD for Java.  
- **Welke resize type geeft de beste kwaliteit?** `ResizeType.LanczosResample`.  
- **Kan ik PSD naar JPEG converteren na het wijzigen van de grootte?** Ja – sla gewoon op met `JpegOptions`.  
- **Heb ik een licentie nodig voor productie?** Een geldige Aspose.PSD‑licentie is vereist voor productiegebruik.  
- **Is deze aanpak geschikt voor grote batches?** Absoluut; de API is geoptimaliseerd voor prestaties.

## Wat is Resize Image Java?

De term “resize image java” verwijst naar het programmatisch wijzigen van de pixelafmetingen van een afbeelding met Java‑code. Aspose.PSD biedt een beknopte API die de low‑level pixelmanipulatie abstraheert, zodat je je kunt concentreren op de bedrijfslogica in plaats van op details van beeldverwerking.

## Waarom Resize Type Enumeration gebruiken?

De Resize Type Enumeration geeft je fijnmazige controle over het resampling‑algoritme, waardoor je snelheid en kwaliteit kunt balanceren. Voor de meeste toepassingen biedt `LanczosResample` een uitstekende afweging, levert scherpe resultaten zonder een zware prestatie‑penalty. Het kiezen van het juiste resize type is cruciaal om een hoogwaardige afbeelding‑grootte‑aanpassing te bereiken.

## Vereisten

Zorg ervoor dat je de volgende vereisten hebt voordat je aan deze tutorial begint:

1. **Java Development Environment** – een JDK 8+ geïnstalleerd en geconfigureerd.  
2. **Aspose.PSD Library** – download en installeer de Aspose.PSD‑bibliotheek van de [website](https://releases.aspose.com/psd/java/).  
3. **Sample PSD File** – zorg voor een voorbeeld‑PSD‑bestand klaar voor experimenten. Je kunt het [sample.psd](Your Document Directory/sample.psd) bestand voor deze tutorial gebruiken.

## Importeer Pakketten

Om te beginnen, importeer de benodigde pakketten in je Java‑project:

```java
import com.aspose.psd.Image;
import com.aspose.psd.ResizeType;

import com.aspose.psd.imageoptions.JpegOptions;
```

## Stap 1: Laad de afbeelding

Begin met het laden van een bestaande afbeelding in een instantie van de `RasterImage`‑klasse. Gebruik de volgende code‑fragment:

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

// Load an existing image into an instance of RasterImage class
Image image = Image.load(sourceFile);
```

## Stap 2: Wijzig de grootte van de afbeelding

Nu wijzig je de grootte van de geladen afbeelding met behulp van de Resize Type Enumeration. In dit voorbeeld gebruiken we de Lanczos Resample‑methode, die ideaal is wanneer je **how to resize image** met hoge kwaliteit:

```java
image.resize(300, 300, ResizeType.LanczosResample);
```

## Stap 3: Sla de gewijzigde afbeelding op

Na het wijzigen van de grootte, sla je de afbeelding op met de opgegeven afmetingen en het gekozen resize type. Hier demonstreren we ook **convert psd to jpeg** door het resultaat op te slaan als een JPEG‑bestand:

```java
String destName = dataDir + "ResizingwithResizeTypeEnumeration_out.jpg";
image.save(destName, new JpegOptions());
```

Je hebt nu een volledige **resize image java**‑workflow uitgevoerd die een hoogwaardige afbeelding‑grootte‑aanpassing oplevert en een kant‑klaar JPEG‑resultaat.

## Veelvoorkomende problemen en oplossingen

- **Afbeelding lijkt wazig na het wijzigen van de grootte** – Probeer een ander `ResizeType` zoals `Bicubic` of `NearestNeighbour` om te zien welke de beste visuele uitkomst geeft voor jouw specifieke afbeelding.  
- **OutOfMemoryError bij grote PSD‑bestanden** – Verwerk de afbeelding in kleinere delen of vergroot de JVM‑heap‑grootte (`-Xmx`‑vlag).  

## FAQ's

### Q1: Is Aspose.PSD for Java geschikt voor zowel kleine als grootschalige projecten?

A1: Absoluut! Aspose.PSD for Java is ontworpen om projecten van elke omvang te bedienen, met schaalbaarheid en efficiëntie.

### Q2: Kan ik een ander resize type gebruiken dan Lanczos Resample?

A2: Ja, Aspose.PSD for Java biedt verschillende resize types, zoals Nearest Neighbour, Bicubic en meer. Bekijk de documentatie voor een volledige lijst.

### Q3: Waar kan ik extra ondersteuning vinden voor Aspose.PSD for Java?

A3: Voor vragen of hulp, bezoek het [Aspose.PSD forum](https://forum.aspose.com/c/psd/34).

### Q4: Is er een gratis proefversie beschikbaar voor Aspose.PSD for Java?

A4: Ja, je kunt een gratis proefversie krijgen [hier](https://releases.aspose.com/).

### Q5: Hoe kan ik een tijdelijke licentie verkrijgen voor Aspose.PSD for Java?

A5: Om een tijdelijke licentie te verkrijgen, bezoek [deze link](https://purchase.aspose.com/temporary-license/).

## Veelgestelde vragen

**Q: Hoe converteer ik programmatisch een PSD‑bestand naar JPEG zonder de grootte te wijzigen?**  
A: Laad de PSD met `Image.load`, en roep vervolgens `image.save("output.jpg", new JpegOptions());` aan.

**Q: Is het mogelijk om de oorspronkelijke DPI te behouden bij het wijzigen van de grootte?**  
A: Ja, je kunt de `Resolution`‑eigenschap op het `Image`‑object instellen vóór het opslaan.

**Q: Kan ik meerdere resize‑bewerkingen achter elkaar uitvoeren?**  
A: Hoewel je `resize` meerdere keren kunt aanroepen, is het efficiënter om de uiteindelijke afmetingen te berekenen en één keer te wijzigen.

## Aanvullende FAQ

**Q: Heeft de Resize Type Enumeration invloed op de verwerkingssnelheid?**  
A: Ja, eenvoudigere algoritmen zoals `NearestNeighbour` zijn sneller maar kunnen lagere kwaliteit opleveren, terwijl `LanczosResample` hogere kwaliteit biedt tegen een bescheiden prestatie‑kost.

**Q: Kan ik afbeeldingen wijzigen in een multi‑threaded omgeving?**  
A: De Aspose.PSD‑API is thread‑safe voor alleen‑lezen bewerkingen. Voor gelijktijdig wijzigen, maak aparte `Image`‑instanties per thread.

**Q: Hoe ga ik om met afbeeldingen met alfakanalen tijdens het wijzigen van de grootte?**  
A: De bibliotheek behoudt standaard alfa‑transparantie. Als je de afbeelding wilt flatten, stel dan de achtergrondkleur in vóór het opslaan.

---

**Laatst bijgewerkt:** 2026-02-12  
**Getest met:** Aspose.PSD for Java 24.12  
**Auteur:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}