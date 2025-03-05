---
title: Beheer cacheherschikking in PSD-bestanden
linktitle: Beheer cacheherschikking in PSD-bestanden
second_title: Aspose.PSD Java-API
description: Beheer de cacheherschikking in PSD-bestanden met Aspose.PSD voor Java. Leer hoe u het geheugen en de bestandsverwerking efficiënt kunt optimaliseren, ideaal voor ontwikkelaars.
type: docs
weight: 22
url: /nl/java/modifying-converting-psd-images/control-cache-reallocation-psd-files/
---
## Invoering
Bij het programmatisch werken met afbeeldingen en Photoshop-bestanden is efficiëntie een sleutelfactor. Aspose.PSD voor Java biedt robuuste functies voor het naadloos beheren en manipuleren van PSD-bestanden. Een van de fundamentele aspecten van het optimaliseren van de prestaties is het beheersen van de cacheherschikking. Cachebeheer helpt bij het behouden van de balans tussen geheugen- en schijfgebruik, waardoor uw applicatie soepel draait, zonder onverwachte crashes of vertragingen. 
## Vereisten
Voordat we ingaan op het codeergedeelte, zijn er een paar dingen die je moet doen om ervoor te zorgen dat alles soepel verloopt:
1. Java Development Kit (JDK): Zorg ervoor dat JDK op uw computer is geïnstalleerd. Je kunt het downloaden van[De website van Oracle](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).
2. Aspose.PSD voor Java: u moet de Aspose.PSD-bibliotheek downloaden. U kunt de nieuwste versie vinden[hier](https://releases.aspose.com/psd/java/).
3. IDE-installatie: Een Integrated Development Environment (IDE) zoals IntelliJ IDEA of Eclipse maakt het gemakkelijker voor u om uw code te beheren.
4. Basiskennis van Java: Bekendheid met programmeren in Java zal u helpen de concepten en codefragmenten beter te begrijpen.
5.  Aspose-licentie (optioneel): Als u watermerken wilt verwijderen en volledige functionaliteit wilt verkrijgen, kunt u overwegen een licentie aan te schaffen[hier](https://purchase.aspose.com/buy) of probeer de gratis proefperiode[hier](https://releases.aspose.com/).
## Pakketten importeren
Voordat we beginnen met het schrijven van de code, zorgen we ervoor dat we de benodigde pakketten hebben geïmporteerd. Hieronder vindt u een korte lijst van wat u aan het begin van uw Java-bestand moet opnemen:
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
## Stap 1: Uw gegevensdirectory instellen
Allereerst moet u een map instellen waarin u uw cachebestanden wilt opslaan. Dit is essentieel voor een effectief beheer van de cache.
```java
String dataDir = "Your Document Directory";
Cache.setCacheFolder(dataDir);
```

- String dataDir: Definieer de map voor uw documentcache.
- Cache.setCacheFolder(dataDir): Met deze methode wordt de cachemap ingesteld op de opgegeven map. Elke door Aspose gemaakte cache wordt nu hier opgeslagen in plaats van de standaard tijdelijke map.
## Stap 2: Cache naar schijf configureren
Vervolgens geven we aan dat we willen dat onze cache alleen op schijf wordt opgeslagen. Dit is vooral handig als uw toepassing grote bestanden gebruikt en u ervoor wilt zorgen dat er geheugen vrij blijft.
```java
Cache.setCacheType(CacheType.CacheOnDiskOnly);
```

- Cache.setCacheType(CacheType.CacheOnDiskOnly): Deze optie zorgt ervoor dat de cache niet in het geheugen wordt bewaard, wat gunstig is voor het verwerken van grote PSD-bestanden zonder al te veel RAM te verbruiken.
## Stap 3: Maximale schijf- en geheugencachegrootte instellen
Laten we nu onze cachegroottes beperken. Dit is cruciaal omdat onbeperkte cache tot prestatieproblemen kan leiden.
```java
Cache.setMaxDiskSpaceForCache(1073741824); // 1 gigabyte
Cache.setMaxMemoryForCache(1073741824); // 1 gigabyte
```

- Cache.setMaxDiskSpaceForCache(1073741824): Hiermee wordt een limiet van 1 GB ingesteld voor de cache op schijf. U kunt deze maat aanpassen aan uw behoeften.
- Cache.setMaxMemoryForCache(1073741824): Op dezelfde manier beperkt dit de cache in het geheugen, zodat uw toepassing geen overmatig geheugen gebruikt.
## Stap 4: Beheer de strategie voor cacheherlocatie
Het beheren van de manier waarop de cache opnieuw wordt toegewezen, is essentieel voor het behoud van de prestaties. Hier leest u hoe u het kunt instellen.
```java
Cache.setExactReallocateOnly(false);
```

- Cache.setExactReallocateOnly(false): Als dit is ingesteld op false, kan Aspose de herverdeling van de cache flexibeler beheren, wat tot betere prestaties kan leiden.
## Stap 5: Controleer de toegewezen cachegrootte
Deze stap gaat over het monitoren van het aantal bytes dat momenteel is toegewezen voor de cache in het geheugen of op schijf. Laten we dat implementeren:
```java
long l1 = Cache.getAllocatedDiskBytesCount();
long l2 = Cache.getAllocatedMemoryBytesCount();
```

- long l1: Slaat het aantal bytes op dat op de schijf is toegewezen.
- long l2: Slaat het aantal bytes op dat in het geheugen is toegewezen. 
U kunt deze waarden op elk gewenst moment controleren om er zeker van te zijn dat uw toepassing het geheugen- en schijfgebruik zoals verwacht beheert.
## Stap 6: Een PSD-afbeelding maken
Nu we onze cacheconfiguraties hebben ingesteld, gaan we een eenvoudige PSD-afbeelding maken.
```java
PsdOptions options = new PsdOptions();
Color[] color = { Color.getRed(), Color.getBlue(), Color.getBlack(), Color.getWhite() };
options.setPalette(new ColorPalette(color));
options.setSource(new StreamSource(new ByteArrayInputStream(new byte[0])));
RasterImage image = (RasterImage) Image.create(options, 100, 100);
```

- PsdOptions-opties: Met dit object kunt u opties opgeven bij het maken van een Photoshop-afbeelding.
- Kleur[] kleur: een array met de kleuren die in het afbeeldingspalet worden gebruikt.
## Stap 7: Pixelgegevens op de afbeelding opslaan
Laten we nu onze afbeelding vullen met pixelgegevens en deze opslaan.
```java
Color[] pixels = new Color[10000];
for (int i = 0; i < pixels.length; i++) {
    pixels[i] = Color.getWhite();
}
image.savePixels(image.getBounds(), pixels);
```

- Kleur[] pixels: dit is een reeks kleurobjecten. Hier vullen we het met witte pixels.
- image.savePixels(image.getBounds(), pixels): Met deze methode worden de pixelgegevens in de afbeelding opgeslagen. Het werkt de afbeelding bij met de kleuren die we hebben gedefinieerd.
## Stap 8: Toegewezen cache controleren na het maken van afbeeldingen
Nadat u de afbeelding hebt gemaakt, is het een goede gewoonte om nogmaals te controleren hoeveel bytes er voor de cache zijn toegewezen.
```java
long diskBytes = Cache.getAllocatedDiskBytesCount();
long memoryBytes = Cache.getAllocatedMemoryBytesCount();
```

- long diskBytes: Legt de huidige toewijzing op de schijf vast na het maken van de afbeelding.
- long memoryBytes: Legt de huidige toewijzing in het geheugen vast. 
Met deze stap kunt u bepalen hoeveel cache er na uw bewerkingen wordt verbruikt.
## Stap 9: Controleer op juiste verwijdering
Ten slotte is het van cruciaal belang om ervoor te zorgen dat alle Aspose.PSD-objecten op de juiste manier worden verwijderd om geheugenlekken te voorkomen.
```java
l1 = Cache.getAllocatedDiskBytesCount();
l2 = Cache.getAllocatedMemoryBytesCount();
```

- l1 en l2: Deze variabelen helpen u de definitieve toewijzing te controleren. Als ze niet nul zijn, betekent dit dat sommige voorwerpen niet op de juiste manier zijn verwijderd.
## Conclusie
Het beheren van de cacheherschikking in Aspose.PSD voor Java kan een aanzienlijk verschil maken in de prestaties van uw toepassing. Door de hierboven beschreven stappen te volgen, kunt u de cache effectief beheren, het geheugengebruik minimaliseren en op efficiënte wijze prachtige PSD-bestanden maken. Omarm deze technieken en zie hoe uw applicaties floreren met optimale prestaties!
## Veelgestelde vragen
### Wat is Aspose.PSD?
Aspose.PSD is een bibliotheek waarmee .NET- en Java-ontwikkelaars Photoshop-bestanden (PSD) programmatisch kunnen maken, manipuleren en converteren.
### Hoe controleer ik de toegewezen cachegrootte?
 Gebruik methoden zoals`Cache.getAllocatedDiskBytesCount()` En`Cache.getAllocatedMemoryBytesCount()` om het huidige cachegebruik te controleren.
### Kan ik een aangepaste directory voor cache instellen?
 Ja, u kunt een andere map opgeven met behulp van`Cache.setCacheFolder("Your Directory Path")`.
### Is Aspose.PSD gratis te gebruiken?
Aspose.PSD is een betaalde bibliotheek, maar u kunt beginnen met een gratis proefversie die beschikbaar is op hun[website](https://releases.aspose.com/).
### Wat gebeurt er als ik voorwerpen niet weggooi?
Het niet weggooien van objecten kan leiden tot geheugenlekken, waardoor uw toepassing meer bronnen gebruikt dan nodig is.