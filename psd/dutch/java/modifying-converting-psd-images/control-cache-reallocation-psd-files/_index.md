---
date: 2026-03-13
description: Leer hoe je PSD-afbeeldingsprojecten in Java maakt terwijl je cacheherallocatie
  beheert met Aspose.PSD voor Java. Optimaliseer geheugen- en schijfgebruik efficiënt.
linktitle: Create PSD Image Java – Control Cache Reallocation
second_title: Aspose.PSD Java API
title: Maak PSD‑afbeelding Java – Beheer cacheherallocatie
url: /nl/java/modifying-converting-psd-images/control-cache-reallocation-psd-files/
weight: 22
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Cacheherallocatie beheren in PSD-bestanden

## Introductie
Als je efficiënt **create PSD image java** projecten wilt maken, is het beheersen van cacheherallocatie essentieel. Bij het programmatisch werken met afbeeldingen en Photoshop‑bestanden is efficiëntie een cruciale factor. Aspose.PSD for Java biedt robuuste functies om PSD‑bestanden naadloos te beheren en te manipuleren. Een van de fundamentele aspecten van prestatie‑optimalisatie is het beheersen van cacheherallocatie. Cache‑beheer helpt de balans tussen geheugen‑ en schijfgebruik te behouden, waardoor je applicatie soepel draait, zonder onverwachte crashes of vertragingen.

## Snelle antwoorden
- **Wat doet cacheherallocatie?** Het balanceert geheugen‑ en schijfgebruik tijdens het verwerken van grote PSD‑bestanden.  
- **Welk cachetype is het beste voor grote afbeeldingen?** `CacheOnDiskOnly` houdt het geheugen vrij door de cache op de schijf op te slaan.  
- **Hoeveel schijfruimte kan ik toewijzen?** Tot 1 GB (of elke grootte die je instelt met `setMaxDiskSpaceForCache`).  
- **Heb ik een licentie nodig om deze functies te gebruiken?** Een licentie verwijdert de proefbeperkingen; zie de Aspose‑aankooppagina.  
- **Kan ik het cachegebruik tijdens runtime monitoren?** Ja, gebruik `Cache.getAllocatedDiskBytesCount()` en `Cache.getAllocatedMemoryBytesCount()`.

## Waarom cacheherallocatie beheren?
Het beheren van cache is cruciaal wanneer je **create PSD image java** applicaties maakt die hoge resolutie‑ of multi‑layer‑bestanden verwerken. Juiste cache‑instellingen voorkomen out‑of‑memory‑fouten, verminderen GC‑pauzes en geven je voorspelbare prestaties op servers of desktop‑apps.

## Voorvereisten
Voordat we naar het code‑gedeelte gaan, zijn er een paar zaken die je moet controleren zodat alles soepel verloopt:
1. Java Development Kit (JDK): Zorg ervoor dat je JDK op je machine hebt geïnstalleerd. Je kunt het downloaden van [Oracle's website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).
2. Aspose.PSD for Java: Je moet de Aspose.PSD‑bibliotheek downloaden. Je kunt de nieuwste release vinden [hier](https://releases.aspose.com/psd/java/).
3. IDE‑configuratie: Een Integrated Development Environment (IDE) zoals IntelliJ IDEA of Eclipse maakt het makkelijker om je code te beheren.
4. Basiskennis van Java: Vertrouwdheid met Java‑programmeren helpt je de concepten en code‑fragmenten beter te begrijpen.
5. Aspose‑licentie (optioneel): Als je watermerken wilt verwijderen en volledige functionaliteit wilt, overweeg dan een licentie aan te schaffen [hier](https://purchase.aspose.com/buy) of de gratis proefversie te proberen [hier](https://releases.aspose.com/).

## Pakketten importeren
Voordat we beginnen met het schrijven van de code, laten we ervoor zorgen dat we de benodigde pakketten hebben geïmporteerd. Hieronder staat een korte lijst van wat je aan het begin van je Java‑bestand moet opnemen:
```java
import com.aspose.psd.Cache;
import com.aspose.psd.CacheType;
import com.aspose.psd.Color;
import com.aspose.psd.ColorPalette;
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;
import com.aspose.psd.imageoptions.GifOptions;
import com.aspose.psd.imageoptions.PsdOptions;
import com.aspose.psd.sources.StreamSource;
import com.aspose.psd.system.io.MemoryStream;
```

## Hoe PSD Image Java maken met cache‑beheer
Hieronder vind je een stapsgewijze walkthrough die cache‑configuratie direct koppelt aan het proces van het maken van een PSD‑afbeelding in Java.

### Stap 1: Instellen van je gegevensmap
Allereerst moet je een map instellen waar je cache‑bestanden worden opgeslagen. Dit is essentieel voor effectief cache‑beheer.
```java
String dataDir = "Your Document Directory";
Cache.setCacheFolder(dataDir);
```

- `String dataDir`: Definieer de map voor je documentcache.  
- `Cache.setCacheFolder(dataDir)`: Deze methode stelt de cache‑map in op de opgegeven map. Alle cache die door Aspose wordt aangemaakt, wordt nu hier opgeslagen in plaats van in de standaard tijdelijke map.

### Stap 2: Cache naar schijf configureren
Vervolgens geven we aan dat we onze cache alleen op de schijf willen opslaan. Dit is vooral nuttig als je applicatie grote bestanden gebruikt en je wilt dat het geheugen vrij blijft.
```java
Cache.setCacheType(CacheType.CacheOnDiskOnly);
```

- `Cache.setCacheType(CacheType.CacheOnDiskOnly)`: Deze optie zorgt ervoor dat de cache niet in het geheugen wordt gehouden, wat voordelig is bij het verwerken van grote PSD‑bestanden zonder te veel RAM te verbruiken.

### Stap 3: Maximale schijf‑ en geheugen‑cachesize instellen
Nu beperken we onze cachesizes. Dit is cruciaal omdat onbeperkte cache kan leiden tot prestatieproblemen.
```java
Cache.setMaxDiskSpaceForCache(1073741824); // 1 gigabyte
Cache.setMaxMemoryForCache(1073741824); // 1 gigabyte
```

- `Cache.setMaxDiskSpaceForCache(1073741824)`: Stelt een limiet van 1 GB in voor de cache op de schijf. Je kunt deze grootte aanpassen aan je behoeften.  
- `Cache.setMaxMemoryForCache(1073741824)`: Beperkt op dezelfde manier de cache in het geheugen, zodat je applicatie geen overmatig geheugen gebruikt.

### Stap 4: Cache‑herallocatiestrategie beheren
Het beheren van hoe cache wordt heralloceerd is essentieel voor het behouden van prestaties. Zo stel je het in.
```java
Cache.setExactReallocateOnly(false);
```

- `Cache.setExactReallocateOnly(false)`: Wanneer ingesteld op `false`, laat dit Aspose toe de cache‑herallocatie flexibeler te beheren, wat kan leiden tot betere prestaties.

### Stap 5: Toegewezen cache‑grootte controleren
Deze stap gaat over het monitoren hoeveel bytes momenteel zijn toegewezen voor de cache in het geheugen of op de schijf. Laten we dat implementeren:
```java
long l1 = Cache.getAllocatedDiskBytesCount();
long l2 = Cache.getAllocatedMemoryBytesCount();
```

- `long l1`: Slaat het aantal bytes op dat op de schijf is toegewezen.  
- `long l2`: Slaat het aantal bytes op dat in het geheugen is toegewezen.  
Je kunt deze waarden op elk moment controleren om er zeker van te zijn dat je applicatie geheugen‑ en schijfgebruik naar verwachting beheert.

### Stap 6: Een PSD‑afbeelding maken
Nu we onze cache‑configuraties hebben ingesteld, laten we een eenvoudige PSD‑afbeelding maken.
```java
PsdOptions options = new PsdOptions();
Color[] color = { Color.getRed(), Color.getBlue(), Color.getBlack(), Color.getWhite() };
options.setPalette(new ColorPalette(color));
options.setSource(new StreamSource(new ByteArrayInputStream(new byte[0])));
RasterImage image = (RasterImage) Image.create(options, 100, 100);
```

- `PsdOptions options`: Dit object stelt je in staat opties op te geven bij het maken van een Photoshop‑afbeelding.  
- `Color[] color`: Een array met de kleuren die in het afbeeldingspalet worden gebruikt.

### Stap 7: Pixelgegevens opslaan in de afbeelding
Laten we nu onze afbeelding vullen met pixelgegevens en opslaan.
```java
Color[] pixels = new Color[10000];
for (int i = 0; i < pixels.length; i++) {
    pixels[i] = Color.getWhite();
}
image.savePixels(image.getBounds(), pixels);
```

- `Color[] pixels`: Dit is een array van kleurobjecten. Hier vullen we deze met witte pixels.  
- `image.savePixels(image.getBounds(), pixels)`: Deze methode slaat de pixelgegevens op in de afbeelding. Het werkt de afbeelding bij met de kleuren die we hebben gedefinieerd.

### Stap 8: Toegewezen cache monitoren na het maken van de afbeelding
Na het maken van de afbeelding is het een goede gewoonte om opnieuw te controleren hoeveel bytes er voor de cache zijn toegewezen.
```java
long diskBytes = Cache.getAllocatedDiskBytesCount();
long memoryBytes = Cache.getAllocatedMemoryBytesCount();
```

- `long diskBytes`: Legt de huidige toewijzing op de schijf vast na het maken van de afbeelding.  
- `long memoryBytes`: Legt de huidige toewijzing in het geheugen vast.  
Deze stap helpt je bepalen hoeveel cache er na je bewerkingen wordt verbruikt.

### Stap 9: Controleren op correcte opruiming
Tot slot is het cruciaal om te zorgen dat alle Aspose.PSD‑objecten correct zijn opgeruimd om geheugenlekken te voorkomen.
```java
l1 = Cache.getAllocatedDiskBytesCount();
l2 = Cache.getAllocatedMemoryBytesCount();
```

- `l1` en `l2`: Deze variabelen helpen je de uiteindelijke toewijzing te controleren. Als ze niet nul zijn, duidt dit op objecten die niet correct zijn opgeruimd.

## Veelvoorkomende problemen en oplossingen
- **Cache‑map niet aangemaakt** – Controleer of de applicatie schrijfrechten heeft voor het pad dat je hebt doorgegeven aan `Cache.setCacheFolder`.  
- **Out‑of‑memory‑fouten** – Controleer nogmaals dat `Cache.setCacheType(CacheType.CacheOnDiskOnly)` is toegepast vóór het laden van grote PSD‑bestanden.  
- **Onverwachte cache‑grootte** – Gebruik de `Cache.getAllocated*BytesCount()`‑methoden na elke belangrijke bewerking om de groei bij te houden.

## Veelgestelde vragen

**Q: Wat is Aspose.PSD?**  
A: Aspose.PSD is een bibliotheek voor .NET‑ en Java‑ontwikkelaars om Photoshop (PSD)‑bestanden programmatisch te maken, manipuleren en converteren.

**Q: Hoe controleer ik de toegewezen cache‑grootte?**  
A: Gebruik methoden zoals `Cache.getAllocatedDiskBytesCount()` en `Cache.getAllocatedMemoryBytesCount()` om het huidige cachegebruik te monitoren.

**Q: Kan ik een aangepaste map voor cache instellen?**  
A: Ja, je kunt een andere map opgeven door `Cache.setCacheFolder("Your Directory Path")` te gebruiken.

**Q: Is Aspose.PSD gratis te gebruiken?**  
A: Aspose.PSD is een betaalde bibliotheek, maar je kunt beginnen met een gratis proefversie die beschikbaar is op hun [website](https://releases.aspose.com/).

**Q: Wat gebeurt er als ik objecten niet opruim?**  
A: Het niet opruimen van objecten kan leiden tot geheugenlekken, waardoor je applicatie meer bronnen gebruikt dan nodig is.

## Conclusie
Het beheersen van cacheherallocatie terwijl je **create PSD image java** applicaties ontwikkelt, kan een aanzienlijk verschil maken in prestaties. Door de bovenstaande stappen te volgen, beheer je de cache efficiënt, minimaliseer je het geheugenverbruik en genereer je hoogwaardige PSD‑bestanden met Aspose.PSD for Java. Pas deze technieken toe, en je projecten zullen soepeler draaien en beter schalen.

---

**Last Updated:** 2026-03-13  
**Tested With:** Aspose.PSD for Java (latest release)  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}