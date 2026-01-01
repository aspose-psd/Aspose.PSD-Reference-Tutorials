---
date: 2026-01-01
description: Leer hoe u XMP‑metadata maakt, XMP toevoegt aan PSD‑bestanden en afbeeldingsmetadata
  bijwerkt met Aspose.PSD voor Java. Volg nu deze stapsgewijze handleiding.
linktitle: Create XMP Metadata
second_title: Aspose.PSD Java API
title: Maak XMP-metadata met Aspose.PSD voor Java
url: /nl/java/image-editing/create-xmp-metadata/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Maak XMP-metadata met Aspose.PSD voor Java

## Introductie

Het beheren van afbeeldingsmetadata is een veelvoorkomende vereiste voor Java‑ontwikkelaars die met Photoshop (PSD)-bestanden werken. In deze tutorial leer je **hoe je XMP-metadata maakt** met behulp van de Aspose.PSD‑bibliotheek, XMP toevoegt aan een PSD‑afbeelding, en afbeeldingsmetadata programmatisch bijwerkt. We lopen elke stap door, leggen uit waarom elk onderdeel belangrijk is, en geven praktische tips die je in echte projecten kunt toepassen.

## Snelle antwoorden
- **Wat is XMP-metadata?** Een gestandaardiseerd formaat voor het insluiten van beschrijvende informatie (auteur, trefwoorden, enz.) in afbeeldingsbestanden.  
- **Waarom Aspose.PSD gebruiken?** Het biedt een pure‑Java API voor het maken, lezen en bewerken van PSD‑bestanden zonder Photoshop.  
- **Kan ik XMP toevoegen aan een bestaande PSD?** Ja – je kunt afbeeldingsmetadata direct bijwerken met `setXmpData`.  
- **Wat zijn de belangrijkste stappen?** Stel de afbeeldingsgrootte in, maak header/trailer, bouw XMP‑pakketten, voeg ze toe, en sla op.  
- **Heb ik een licentie nodig?** Een gratis proefversie werkt voor ontwikkeling; een commerciële licentie is vereist voor productie.

## Wat betekent “XMP-metadata maken” in Java?

XMP-metadata maken betekent het bouwen van een XMP‑pakket (header, body, trailer) dat de afbeelding beschrijft en vervolgens dat pakket in een PSD‑bestand insluiten. De Aspose.PSD‑bibliotheek abstraheert de low‑level details, zodat je je kunt concentreren op de inhoud die je wilt opslaan.

## Waarom XMP toevoegen aan PSD‑bestanden?

- **Zoekbaarheid:** Maakt krachtige asset‑management zoekopdrachten mogelijk op basis van auteur, titel of aangepaste tags.  
- **Interoperabiliteit:** XMP wordt herkend door Adobe‑producten, Lightroom en vele DAM‑systemen.  
- **Versiebeheer:** Sla verwerkingsgeschiedenis (bijv. stad, kleurmodus) direct in het bestand op.

## Voorvereisten

- **Java‑ontwikkelomgeving:** JDK 8 of hoger geïnstalleerd en een basisbegrip van Java.  
- **Aspose.PSD‑bibliotheek:** Download en installeer de Aspose.PSD voor Java bibliotheek. Je kunt de bibliotheek en gedetailleerde documentatie vinden [hier](https://reference.aspose.com/psd/java/).  
- **Je documentmap:** Bepaal waar je PSD‑bestanden op je systeem leest/schrijft.

## Importeer pakketten

Importeer in je Java‑project de benodigde pakketten om de functionaliteit van Aspose.PSD te benutten:

```java
import com.aspose.psd.Rectangle;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.system.io.MemoryStream;
import com.aspose.psd.xmp.XmpHeaderPi;
import com.aspose.psd.xmp.XmpMeta;
import com.aspose.psd.xmp.XmpPacketWrapper;
import com.aspose.psd.xmp.XmpTrailerPi;
import com.aspose.psd.xmp.schemas.dublincore.DublinCorePackage;
import com.aspose.psd.xmp.schemas.photoshop.ColorMode;
import com.aspose.psd.xmp.schemas.photoshop.PhotoshopPackage;
```

## Stap 1: Afbeeldingsgrootte opgeven

Definieer eerst de canvasafmetingen voor de nieuwe PSD‑afbeelding.

```java
// Specify the size of the image by defining a Rectangle
Rectangle rect = new Rectangle(0, 0, 100, 200);
```

## Stap 2: Maak een nieuwe afbeelding

Maak een lege PSD‑afbeelding die we later verrijken met XMP‑metadata.

```java
// Create a brand new image for sample purposes
PsdImage image = new PsdImage(rect.getWidth(), rect.getHeight());
```

## Stap 3: Maak XMP‑header

De header bevat de opening XML processing instruction en een GUID die het document identificeert.

```java
// Create an instance of XMP-Header
XmpHeaderPi xmpHeader = new XmpHeaderPi();
xmpHeader.setGuid("Your Document Directory");
```

## Stap 4: Maak XMP‑trailer

De trailer markeert het einde van het XMP‑pakket. Het instellen van de `true`‑vlag schrijft de afsluitende processing instruction.

```java
// Create an instance of Xmp-TrailerPi 
XmpTrailerPi xmpTrailer = new XmpTrailerPi(true);
```

## Stap 5: Maak XMP‑metadata

Voeg algemene attributen zoals auteur en beschrijving toe aan het kern‑XMP‑metadata‑object.

```java
// Create an instance of XMPmeta class to set different attributes
XmpMeta xmpMeta = new XmpMeta();
xmpMeta.addAttribute("Author", "Mr Smith");
xmpMeta.addAttribute("Description", "The fake metadata value");
```

## Stap 6: Maak XMP‑pakketwrapper

Verpak de header, trailer en kern‑metadata in één pakket dat aan de afbeelding kan worden toegevoegd.

```java
// Create an instance of XmpPacketWrapper that contains all metadata
XmpPacketWrapper xmpData = new XmpPacketWrapper(xmpHeader, xmpTrailer, xmpMeta);
```

## Stap 7: Stel Photoshop‑attributen in

Vul Photoshop‑specifieke velden (stad, land, kleurmodus) in die veel Adobe‑tools verwachten.

```java
// Create an instance of Photoshop package and set Photoshop attributes
PhotoshopPackage photoshopPackage = new PhotoshopPackage();
photoshopPackage.setCity("London");
photoshopPackage.setCountry("England");
photoshopPackage.setColorMode(ColorMode.Rgb);
```

## Stap 8: Voeg Photoshop‑pakket toe aan XMP‑metadata

Voeg het Photoshop‑pakket toe aan het XMP‑pakket.

```java
// Add Photoshop package into XMP metadata
xmpData.addPackage(photoshopPackage);
```

## Stap 9: Stel DublinCore‑attributen in

Voeg Dublin Core‑metadata toe zoals auteur, titel en een aangepast movie‑tag.

```java
// Create an instance of DublinCore package and set DublinCore attributes
DublinCorePackage dublinCorePackage = new DublinCorePackage();
dublinCorePackage.setAuthor("Charles Bukowski");
dublinCorePackage.setTitle("Confessions of a Man Insane Enough to Live With the Beasts");
dublinCorePackage.addValue("dc:movie", "Barfly");
```

## Stap 10: Voeg DublinCore‑pakket toe aan XMP‑metadata

Combineer het Dublin Core‑pakket met het bestaande XMP‑pakket.

```java
// Add DublinCore Package into XMP metadata
xmpData.addPackage(dublinCorePackage);
```

## Stap 11: Werk XMP‑metadata bij in afbeelding

Sluit nu het volledige XMP‑pakket in de PSD‑afbeelding in.

```java
// Update XMP metadata into the image
image.setXmpData(xmpData);
```

## Stap 12: Sla afbeelding op

Schrijf tenslotte het PSD‑bestand naar schijf (of een geheugen‑stream) zodat de metadata wordt bewaard.

```java
// Save the image on the disk or in a memory stream
image.save("Your Document Directory" + "create_XMP_Metadata.psd");
```

## Veelvoorkomende problemen en oplossingen

| Probleem | Waarom het gebeurt | Oplossing |
|----------|--------------------|-----------|
| **`NullPointerException` bij `setXmpData`** | Het XMP‑pakket was niet volledig opgebouwd (header/trailer ontbreekt). | Zorg ervoor dat je `XmpHeaderPi`, `XmpTrailerPi` maakt en alle pakketten toevoegt voordat je `setXmpData` aanroept. |
| **Metadata niet zichtbaar in Photoshop** | Photoshop verwacht dat het XMP‑pakket correct wordt verpakt. | Controleer of `XmpTrailerPi(true)` wordt gebruikt en dat het pakket met de afbeelding wordt opgeslagen. |
| **Bestandspad‑fouten** | Een relatief pad gebruiken zonder de juiste permissies. | Gebruik een absoluut pad of zorg dat de applicatie schrijfrechten heeft voor de doelmap. |

## Veelgestelde vragen

**V: Is Aspose.PSD compatibel met verschillende afbeeldingsformaten?**  
A: Ja, Aspose.PSD ondersteunt PSD, PSB, BMP, GIF, JPEG, PNG, TIFF en meer, waardoor je flexibiliteit hebt over formaten.

**V: Kan ik bestaande metadata manipuleren met Aspose.PSD?**  
A: Absoluut. Je kunt een bestaande PSD laden, de XMP‑data ophalen met `getXmpData()`, het pakket aanpassen en het opnieuw opslaan.

**V: Zijn er beperkingen aan de afbeeldingsgrootte die Aspose.PSD kan verwerken?**  
A: Aspose.PSD is ontworpen om met grote afbeeldingen te werken (tot enkele gigapixels), alleen beperkt door beschikbaar geheugen.

**V: Is er een proefversie beschikbaar voor Aspose.PSD?**  
A: Ja, je kunt de mogelijkheden van Aspose.PSD verkennen door een gratis proefversie te verkrijgen [hier](https://releases.aspose.com/).

**V: Waar kan ik ondersteuning vinden voor vragen over Aspose.PSD?**  
A: Voor hulp of vragen kun je het [Aspose.PSD‑forum](https://forum.aspose.com/c/psd/34) bezoeken.

## Conclusie

Je hebt nu geleerd **hoe je XMP‑metadata maakt**, XMP toevoegt aan een PSD, en afbeeldingsmetadata bijwerkt met Aspose.PSD voor Java. Deze stappen geven je volledige controle over de beschrijvende informatie die in je afbeeldingen is ingebed, waardoor ze doorzoekbaar zijn en klaar voor downstream‑workflows. Voel je vrij om te experimenteren met extra XMP‑schema's of deze code te integreren in grotere beeld‑verwerkingspijplijnen.

---

**Laatst bijgewerkt:** 2026-01-01  
**Getest met:** Aspose.PSD for Java 24.12  
**Auteur:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}