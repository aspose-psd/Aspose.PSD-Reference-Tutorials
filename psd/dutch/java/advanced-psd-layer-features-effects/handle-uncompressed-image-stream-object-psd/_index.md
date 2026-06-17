---
date: 2026-02-17
description: Leer hoe u PSD naar PNG kunt exporteren en ongecomprimeerde afbeeldingsstromen
  kunt verwerken met Aspose.PSD voor Java.
linktitle: Handle Uncompressed Image Stream Object in PSD - Java
second_title: Aspose.PSD Java API
title: Exporteer PSD naar PNG – Maak PSD Graphics-object – Niet‑gecomprimeerde stream
  in Java
url: /nl/java/advanced-psd-layer-features-effects/handle-uncompressed-image-stream-object-psd/
weight: 26
---

 "Tested With", "Author". Keep values.

Then closing shortcodes.

Also there is a backtop button shortcode after main container.

We must keep all shortcodes unchanged.

Now produce final content.

Let's craft translation.

Be careful to keep markdown formatting exactly.

Let's write.{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Export PSD naar PNG – Maak PSD Graphics Object – Niet-gecomprimeerde Stream in Java

## Introduction
Welkom in de wereld van beeldmanipulatie in Java! In deze tutorial zul je **een PSD graphics object maken**, ongecomprimeerde beeldstreamobjecten verwerken, en leren hoe je **PSD naar PNG exporteert** met Aspose.PSD for Java. Of je nu een grafisch ontwerper bent die zijn workflow wil automatiseren of een softwareontwikkelaar die krachtige beeldverwerkingsmogelijkheden in zijn applicaties wil integreren, deze gids is speciaal voor jou. We lopen alles door, van de vereisten tot de uiteindelijke export, zodat je een goed begrip hebt van het volledige proces.

## Quick Answers
- **Wat betekent “create PSD graphics object”?** Het verwijst naar het instantiëren van een graphics‑context voor een PSD‑bestand zodat je de inhoud kunt tekenen of bewerken.  
- **Welke bibliotheek verwerkt ongecomprimeerde streams?** Aspose.PSD for Java biedt volledige ondersteuning voor ruwe (ongecomprimeerde) beeldgegevens.  
- **Kan ik PSD naar PNG exporteren na bewerken?** Ja—zodra je een `Graphics`‑object hebt, kun je de PSD renderen en opslaan als PNG.  
- **Heb ik een licentie nodig voor ontwikkeling?** Een gratis proefversie werkt voor testen; een commerciële licentie is vereist voor productie.  
- **Is de export verliesloos?** Exporteren naar PNG behoudt de beeldkwaliteit, terwijl de bestandsgrootte groter is dan bij JPEG maar kleiner dan een ongecomprimeerde PSD.  

## How to export PSD to PNG using Aspose.PSD for Java
Wanneer je **PSD naar PNG moet exporteren**, is de typische workflow:

1. Laad het PSD‑bestand (of maak er een).  
2. Voer teken- of laagmanipulaties uit met een `Graphics`‑object.  
3. Sla de resulterende afbeelding op met `PngOptions` (dezelfde `Graphics`‑instantie kan opnieuw worden gebruikt).  

Hoewel deze tutorial zich richt op het verwerken van ongecomprimeerde streams, kan hetzelfde `Graphics`‑object dat je maakt later in je pipeline worden hergebruikt om de PSD in een PNG‑bestand te renderen.

## Prerequisites
Voordat we in de code duiken, zorgen we ervoor dat je alles hebt wat je nodig hebt om aan dit avontuur te beginnen. Hier zijn de vereisten:

### Java Development Kit (JDK)
Zorg ervoor dat je JDK op je machine hebt geïnstalleerd. Je kunt het downloaden van de website van Oracle of OpenJDK gebruiken.

### Aspose.PSD for Java
Je moet de Aspose.PSD‑bibliotheek downloaden en installeren. Deze krachtige bibliotheek stelt je in staat PSD‑bestanden eenvoudig te manipuleren. Je kunt de nieuwste versie krijgen via [this link](https://releases.aspose.com/psd/java/).

### Integrated Development Environment (IDE)
Het is een goed idee om een IDE te gebruiken om je Java‑code te schrijven en te testen. Je kunt IntelliJ IDEA, Eclipse of een andere IDE gebruiken die je voorkeur heeft.

### Basic Understanding of Java
Een basiskennis van Java‑programmeren maakt dit proces soepeler. Zorg dat je de basisprincipes kent, zoals klassen, methoden en exception‑handling.

Met alles klaar, laten we de mouwen opstropen en naar het spannende deel gaan – coderen!

## Import Packages
Om te beginnen moeten we de benodigde pakketten importeren om met Aspose.PSD te werken. Hieronder vind je de imports die je doorgaans nodig hebt voor het verwerken van PSD‑bestanden.

```java
import com.aspose.psd.Graphics;
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.CompressionMethod;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.PsdOptions;
import java.io.ByteArrayInputStream;
import java.io.ByteArrayOutputStream;
```

Laten we nu de code in hapklare stappen opsplitsen zodat je gemakkelijk kunt volgen. We zullen opzetten, een PSD‑bestand laden, het manipuleren en de output opslaan.

## Step 1: Define Your Document Directory
Voordat je begint met coderen, wil je definiëren waar je PSD‑bestand zich bevindt. Dit is in feite het voorbereiden van de basis voor je project.

```java
String dataDir = "Your Document Directory";
```

Vervang `"Your Document Directory"` door het daadwerkelijke pad waar je PSD‑bestand (bijv. layers.psd) zich bevindt. Dit helpt je om je bestanden zonder gedoe te vinden.

## Step 2: Create a Byte Array Output Stream
Je hebt een plek nodig om de gewijzigde afbeelding op te slaan voordat je er iets mee doet. Een `ByteArrayOutputStream` helpt je de beelddata eenvoudig vast te leggen.

```java
ByteArrayOutputStream ms = new ByteArrayOutputStream();
```

Deze regel initialiseert een nieuw `ByteArrayOutputStream`‑object met de naam `ms`. Je zult dit object gebruiken om je ongecomprimeerde afbeelding op te slaan.

## Step 3: Load the PSD File
Nu is het tijd om het daadwerkelijke PSD‑bestand te laden. Hier begint de magie!

```java
PsdImage psdImage = (PsdImage) Image.load(dataDir + "layers.psd");
```

Deze regel laadt je PSD‑bestand in een `PsdImage`‑object. Zorg dat je het juiste pad hebt; anders verschijnt er een foutmelding als een onverwachte pop‑quiz.

## Step 4: Set Up the PsdOptions for Saving
Je moet aangeven hoe je de afbeelding wilt opslaan — uiteraard ongecomprimeerd!

```java
PsdOptions saveOptions = new PsdOptions();
saveOptions.setCompressionMethod(CompressionMethod.Raw);
```

Hier maak je een `PsdOptions`‑object aan en stel je de compressiemethode in op `Raw`. Deze methode zorgt ervoor dat de afbeelding haar volledige kwaliteit behoudt en zonder enige compressie wordt opgeslagen.

## Step 5: Save the Image to the Output Stream
```java
psdImage.save(ms, saveOptions);
```

Deze regel slaat je gewijzigde afbeelding op in de `ByteArrayOutputStream` die je in Stap 2 hebt aangemaakt, met behulp van de opties die in Stap 4 zijn gedefinieerd. De `save`‑methode zorgt voor de juiste codering van de afbeelding op basis van jouw instellingen.

## Step 6: Reset the Output Stream
Na het opslaan staat je output‑stream aan het einde. Je moet deze resetten zodat je vanaf het begin kunt lezen.

```java
ms.reset();
```

Deze `reset`‑methode maakt je `ByteArrayOutputStream` klaar om opnieuw vanaf het begin te lezen. Zie het als het terugspoelen van een band voordat je je favoriete nummer beluistert!

## Step 7: Load the Newly Created Image
```java
PsdImage img = (PsdImage) Image.load(new ByteArrayInputStream(ms.toByteArray()));
```

Hier laden we de afbeelding terug vanuit de `ByteArrayOutputStream` in een nieuw `PsdImage`‑object. Dit is het moment om de resultaten van je eerdere werk te controleren.

## Step 8: Create Graphics Object
Om de afbeelding verder te wijzigen of te renderen, moet je een graphics‑object maken.

```java
Graphics graphics = new Graphics(psdImage);
```

Deze regel initialiseert een `Graphics`‑object met behulp van je `psdImage`. Je kunt dit graphics‑object nu gebruiken om de afbeelding te tekenen of te manipuleren zoals nodig. Het is net alsof je een penseel in je hand hebt!

## Manipulate PSD Layers with Graphics Object
Nu je een **Graphics**‑instantie hebt, kun je **PSD‑lagen manipuleren** — bijvoorbeeld vormen tekenen, tekst toevoegen of filters toepassen op een specifieke laag. De graphics‑context werkt direct op de onderliggende pixeldata, waardoor je fijnmazige controle hebt over het uiterlijk van elke laag.

## Common Issues and Solutions
- **NullPointerException bij het laden van het bestand** – controleer het `dataDir`‑pad en zorg dat de bestandsnaam correct is.  
- **Gecomprimeerde output ondanks gebruik van Raw** – controleer of `saveOptions.setCompressionMethod(CompressionMethod.Raw);` wordt aangeroepen vóór de `save`‑methode.  
- **Graphics‑object lijkt leeg** – zorg dat je tekent op de juiste `PsdImage`‑instantie (gebruik de geladen, niet de nieuw aangemaakte tenzij bedoeld).

## FAQ's
### What is Aspose.PSD?
Aspose.PSD is een .NET‑bibliotheek die ontwikkelaars in staat stelt Photoshop PSD‑bestanden en gerelateerde beeldformaten programmatisch te maken, bewerken en manipuleren.

### How can I download Aspose.PSD for Java?
Je kunt het downloaden van de [release page](https://releases.aspose.com/psd/java/).

### Is there a free trial for Aspose.PSD?
Ja, je kunt een gratis proefversie verkrijgen via [here](https://releases.aspose.com/).

### Can I get support for Aspose.PSD?
Absoluut! Je kunt hulp zoeken op het [Aspose support forum](https://forum.aspose.com/c/psd/34).

### How can I obtain a temporary license for Aspose.PSD?
Bezoek gewoon de [temporary license page](https://purchase.aspose.com/temporary-license/) om te beginnen.

## Frequently Asked Questions

**Q: Kan ik het graphics‑object gebruiken om slechts één specifieke laag te bewerken?**  
A: Ja. Nadat je de PSD hebt geladen, selecteer je de gewenste laag via `psdImage.getLayers().get_Item(index)` en geef je deze door aan de `Graphics`‑constructor.

**Q: Heeft de Raw‑compressiemethode invloed op de bestandsgrootte?**  
A: Raw slaat pixeldata op zonder compressie, dus de bestandsgrootte zal groter zijn dan bij gecomprimeerde PSD‑bestanden, maar de beeldkwaliteit blijft onaangetast.

**Q: Is het mogelijk om de bewerkte PSD naar een ander formaat te exporteren (bijv. PNG)?**  
A: Absoluut. Gebruik de juiste `Image.save`‑overload met `PngOptions` na het bewerken — dit is de standaard manier om **PSD naar PNG te exporteren**.

**Q: Welke Java‑versie is vereist?**  
A: Aspose.PSD for Java ondersteunt JDK 8 en hoger.

**Q: Hoe kan ik bronnen vrijgeven na verwerking?**  
A: Roep `psdImage.dispose()` aan en sluit eventuele streams om native bronnen vrij te maken.

---

**Last Updated:** 2026-02-17  
**Tested With:** Aspose.PSD for Java (latest release)  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}