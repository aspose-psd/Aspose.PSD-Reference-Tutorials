---
date: 2026-03-28
description: Leer hoe u een nieuwe PSD‑laag maakt en de aanmaakdatum en -tijd beheert
  met Aspose.PSD voor Java. Deze stap‑voor‑stap gids behandelt het laden, lezen, valideren
  en toevoegen van lagen.
linktitle: Create New PSD Layer and Manage Creation DateTime in Java
second_title: Aspose.PSD Java API
title: Maak een nieuwe PSD‑laag en beheer de creatiedatum‑ en -tijd in Java
url: /nl/java/psd-image-modification-conversion/manage-layer-creation-datetime-psd/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Maak een nieuwe PSD-laag en beheer de aanmaakdatum/tijd in Java

## Introductie
Wanneer je programmatisch met Photoshop (PSD)-bestanden werkt, is het kunnen **create new PSD layer** objecten en het bijhouden van hun aanmaak‑timestamps een echte game‑changer. Of je nu een versiebeheersysteem voor ontwerp‑assets bouwt, batch‑bewerkingen automatiseert, of gewoon een audit‑trail nodig hebt voor samenwerkingsprojecten, weten hoe je de aanmaakdatum van een laag kunt lezen en instellen, stelt je in staat de volledige herkomst van elke wijziging te behouden. In deze tutorial lopen we het volledige proces door met Aspose.PSD for Java — van het laden van een PSD, het ophalen van de aanmaakdatum van een laag, het valideren ervan, tot het uiteindelijk toevoegen van een splinternieuwe aanpassingslaag.

## Snelle antwoorden
- **Wat is de bibliotheek die PSD‑bestanden in Java verwerkt?** Aspose.PSD for Java  
- **Kan ik de aanmaakdatum van een laag lezen?** Ja, met `layer.getLayerCreationDateTime()`  
- **Is het mogelijk om een nieuwe aanpassingslaag toe te voegen?** Absoluut – `im.addLevelsAdjustmentLayer()` maakt er één  
- **Heb ik een licentie nodig voor productiegebruik?** Een commerciële licentie is vereist voor niet‑trial implementaties  
- **Welke Java‑versie wordt ondersteund?** JDK 8 of later  

## Wat betekent “create new PSD layer”?
Een nieuwe PSD‑laag maken betekent programmatisch een vers frisse laag‑object—zoals een aanpassings‑, tekst‑ of pixel‑laag—in een bestaand PSD‑document invoegen. Deze bewerking stelt je in staat de afbeelding uit te breiden of te wijzigen zonder handmatig Photoshop te openen.

## Waarom de aanmaakdatum/tijd van een laag beheren?
Het bijhouden van de aanmaak‑DateTime van elke laag helpt je:
- **Revisies auditen** – precies weten wanneer een laag is toegevoegd.  
- **Assets synchroniseren** tussen teams door timestamps te vergelijken.  
- **Workflows automatiseren** die afhankelijk zijn van tijd‑gebaseerde regels (bijv. lagen ouder dan een maand verbergen).  

## Voorvereisten
Voordat je begint, zorg dat je het volgende klaar hebt staan:

1. **Java Development Kit (JDK)** – versie 8 of later.  
2. **IDE** – IntelliJ IDEA, Eclipse, NetBeans, of elke editor die je verkiest.  
3. **Aspose.PSD for Java** – je kunt het [hier downloaden](https://releases.aspose.com/psd/java/) voor installatie.  
4. **Basiskennis van Java** – als je nieuw bent met Java, geen zorgen; de code is volledig gecommentarieerd.

Alles klaar? Geweldig! Laten we naar het leuke deel van coderen springen.

## Pakketten importeren
Eerst importeer je de Aspose.PSD‑klassen en Java‑hulpmiddelen die je nodig hebt. Deze imports geven je toegang tot beeldverwerking, laagmanipulatie en datumopmaak.

```java
import com.aspose.psd.Image;
import com.aspose.psd.examples.Utils.Assert;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.Layer;
import java.text.DateFormat;
import java.text.SimpleDateFormat;
import java.util.Date;
```

## Stap 1: Stel uw documentmap in
Geef de map op die de PSD bevat waarmee je wilt werken. Vervang de placeholder door het absolute pad op jouw machine.

```java
String dataDir = "Your Document Directory";
```

## Stap 2: Laad het PSD‑bestand
Maak een `PsdImage`‑instantie door het doelbestand te laden. Dit object is het startpunt voor alle laag‑operaties.

```java
String sourceName = dataDir + "OneLayer.psd";
PsdImage im = (PsdImage) Image.load(sourceName);
```

## Stap 3: Toegang tot de laag en de aanmaakdatum
Pak de eerste laag (index 0) en haal de aanmaak‑timestamp op. Dit is de datum die je later kunt vergelijken of loggen.

```java
Layer layer = im.getLayers()[0];
Date creationDateTime = layer.getLayerCreationDateTime();
```

## Stap 4: Formatteer de aanmaakdatum
Converteer het ruwe `Date`‑object naar een mens‑leesbare string. Pas het patroon aan als je een ander formaat wilt.

```java
DateFormat dateFormat = new SimpleDateFormat("yyyy/MM/dd HH:mm:ss");
```

## Stap 5: Valideer de aanmaakdatum
Voor demonstratie vergelijken we de opgehaalde datum met een verwachte waarde. In echte projecten kun je vergelijken met een database‑record of een configuratie‑bestand.

```java
Date expectedDateTime = new Date("2018/7/17 8:57:24");
Assert.areEqual(expectedDateTime, creationDateTime);
```

## Stap 6: Maak een nieuwe laag
Nu maken we daadwerkelijk **create new PSD layer** objecten. Hier voegen we een Levels‑aanpassingslaag toe, waarmee je toonbereiken kunt bijstellen zonder de originele pixels te wijzigen.

```java
Date now = new Date();
Layer createdLayer = im.addLevelsAdjustmentLayer();
```

> **Pro tip:** De variabele `now` legt het moment vast waarop je de laag toevoegt, die je later als metadata kunt opslaan als je een aangepaste tijdstempel nodig hebt.

## Veelvoorkomende problemen en oplossingen
| Probleem | Waarom het gebeurt | Oplossing |
|----------|--------------------|-----------|
| `NullPointerException` op `layer.getLayerCreationDateTime()` | De PSD heeft geen lagen of de laagindex ligt buiten het bereik. | Controleer `im.getLayers().length > 0` voordat je toegang krijgt. |
| Datumafwijking bij validatie | `Date`‑constructor parseert strings op een locale‑afhankelijke manier. | Gebruik `SimpleDateFormat.parse("2018/07/17 08:57:24")` voor betrouwbare parsing. |
| Nieuwe laag niet zichtbaar in Photoshop | Aanpassingslaag kan standaard verborgen zijn. | Roep `createdLayer.setVisible(true);` aan na creatie. |

## Conclusie
Je weet nu hoe je **create new PSD layer** objecten kunt maken, hun aanmaak‑timestamps kunt lezen, die timestamps kunt valideren en aanpassingslagen kunt toevoegen — alles met Aspose.PSD for Java. Deze mogelijkheid opent de deur naar geavanceerde automatisering, audit‑trails en samenwerkings‑workflows in elke Java‑gebaseerde beeldverwerkings‑pipeline.

Als je van deze tutorial hebt genoten, verken dan andere Aspose.PSD‑functies zoals lagen samenvoegen, filters toepassen of exporteren naar verschillende formaten. De mogelijkheden zijn eindeloos!

## Veelgestelde vragen
### Wat is Aspose.PSD?  
Aspose.PSD is een krachtige bibliotheek voor het programmatisch werken met Photoshop (PSD)-bestanden.

### Kan ik Aspose.PSD gratis gebruiken?  
Ja! Je kunt beginnen met een gratis proefversie die [hier](https://releases.aspose.com/) beschikbaar is.

### Moet ik een licentie aanschaffen voor langdurig gebruik?  
Ja, je kunt een licentie [hier](https://purchase.aspose.com/buy) verkrijgen zodra je klaar bent.

### Waar kan ik meer informatie vinden over Aspose.PSD?  
Je kunt de [documentatie](https://reference.aspose.com/psd/java/) raadplegen voor gedetailleerde handleidingen en API‑referenties.

### Hoe kan ik ondersteuning krijgen als ik problemen ondervind met Aspose.PSD?  
Bezoek gerust het [support forum](https://forum.aspose.com/c/psd/34) voor community‑ondersteuning.

---

**Laatst bijgewerkt:** 2026-03-28  
**Getest met:** Aspose.PSD for Java 24.10  
**Auteur:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}