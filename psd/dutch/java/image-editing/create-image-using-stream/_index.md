---
date: 2026-01-01
description: Leer hoe je een bitmap in Java maakt met een stream in Aspose.PSD, een
  afbeeldingsbestand in Java opslaat en efficiënt bits per pixel instelt.
linktitle: Create Image using Stream
second_title: Aspose.PSD Java API
title: Maak bitmap in Java met Stream in Aspose.PSD
url: /nl/java/image-editing/create-image-using-stream/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Maak bitmap java met Stream in Aspose.PSD

## Inleiding

Als je **bitmap java**‑afbeeldingen on‑the‑fly moet maken, biedt Aspose.PSD voor Java een schone, stream‑gebaseerde aanpak die zowel snel als geheugen‑efficiënt is. In deze tutorial lopen we stap voor stap door het genereren van een bitmap‑afbeelding vanuit een stream, het configureren van het aantal bits per pixel, en uiteindelijk **save image file java** naar schijf. Aan het einde begrijp je waarom deze methode ideaal is voor server‑side beeldverwerking, batch‑taken of elke situatie waarin je tijdelijke bestanden wilt vermijden.

## Snelle antwoorden
- **Wat betekent “create bitmap java”?** Het verwijst naar het programmatisch genereren van een BMP‑afbeelding met Java‑code.  
- **Welke bibliotheek behandelt de stream?** Aspose.PSD’s `StreamSource` en `FileCreateSource`‑klassen.  
- **Kan ik de kleurdiepte instellen?** Ja – gebruik `BmpOptions.setBitsPerPixel(int)` (bijv. 24 bpp).  
- **Hoe sla ik het resultaat op?** Roep `image.save(outputPath)` aan om **save image file java** op te slaan.  
- **Is een licentie vereist voor productie?** Een geldige Aspose.PSD‑licentie is nodig voor commercieel gebruik.

## Vereisten voor het maken van bitmap java

Voordat je begint, zorg dat je het volgende hebt:

- **Java Development Kit (JDK)** – elke recente versie (8 of hoger).  
- **Aspose.PSD for Java** – download de nieuwste JAR van de [documentatie](https://reference.aspose.com/psd/java/).  
- **IDE** – Eclipse, IntelliJ IDEA, of een andere Java‑compatibele editor naar keuze.

## Importpakketten voor bitmap‑generatie

Begin met het importeren van de benodigde namespaces. Deze geven je toegang tot beeldcreatie, BMP‑opties en stream‑verwerking.

```java
import com.aspose.psd.Image;

import com.aspose.psd.imageoptions.BmpOptions;
import com.aspose.psd.sources.FileCreateSource;
import com.aspose.psd.sources.StreamSource;
import com.aspose.psd.system.io.FileMode;
import com.aspose.psd.system.io.FileStream;
import com.aspose.psd.system.io.Stream;
import java.io.FileInputStream;
```

## Stap 1: Documentmap instellen

```java
String dataDir = "Your Document Directory";
```

Vervang `"Your Document Directory"` door het absolute pad waar je bron‑ en uitvoerbestanden zich bevinden.

## Stap 2: De bestandsnaam voor de uitvoer definiëren

```java
String desName = dataDir + "CreatingImageUsingStream_out.bmp";
```

Dit is het pad waar de **save image file java**‑operatie de bitmap zal schrijven.

## Stap 3: BmpOptions configureren (bits per pixel instellen)

```java
BmpOptions imageOptions = new BmpOptions();
imageOptions.setBitsPerPixel(24);
```

Hier **stellen we bits per pixel** in op 24 bpp, wat een true‑color bitmap oplevert. Pas de waarde aan als je een andere kleurdiepte nodig hebt.

## Stap 4: Een FileCreateSource maken (stream‑bron)

```java
FileCreateSource stream = new FileCreateSource(dataDir + "sample_out.bmp");
imageOptions.setSource(stream);
```

`FileCreateSource` omsluit een bestandsstream zodat Aspose.PSD direct naar de bestemming kan schrijven zonder tussenliggende buffers.

## Stap 5: De bitmap‑afbeelding genereren

```java
Image image = Image.create(imageOptions, 500, 500);
```

Deze regel **genereert een bitmap java**‑afbeelding van 500 × 500 pixels met de opties die we eerder hebben gedefinieerd.

## Stap 6: Beeldverwerking uitvoeren en opslaan

```java
// Perform desired image processing operations here
// For example, you could draw shapes, apply filters, etc.

// Save the processed bitmap to disk
image.save(desName);
```

Na eventuele optionele manipulatie slaat de aanroep van `image.save` de **save image file java** op naar de locatie die is opgegeven in `desName`.

## Conclusie

Je hebt nu geleerd hoe je **bitmap java**‑afbeeldingen kunt **create bitmap java** met streams in Aspose.PSD, de kleurdiepte kunt regelen met **set bits per pixel**, en **save image file java** efficiënt kunt opslaan. Experimenteer met verschillende afmetingen, pixelformaten of extra verwerkingsstappen om aan de behoeften van je project te voldoen.

## Veelgestelde vragen

### Q1: Kan ik Aspose.PSD gebruiken met andere Java‑bibliotheken?

A1: Ja, Aspose.PSD is ontworpen om naadloos te integreren met andere Java‑bibliotheken, waardoor je project veelzijdig blijft.

### Q2: Waar vind ik ondersteuning voor vragen over Aspose.PSD?

A2: Bezoek het [Aspose.PSD‑forum](https://forum.aspose.com/c/psd/34) voor community‑ondersteuning en discussies.

### Q3: Is er een gratis proefversie beschikbaar voor Aspose.PSD?

A3: Ja, je kunt een gratis proefversie krijgen [hier](https://releases.aspose.com/).

### Q4: Hoe verkrijg ik een tijdelijke licentie voor Aspose.PSD?

A4: Verkrijg een tijdelijke licentie [hier](https://purchase.aspose.com/temporary-license/).

### Q5: Wat zijn de systeemvereisten voor Aspose.PSD?

A5: Raadpleeg de [documentatie](https://reference.aspose.com/psd/java/) voor gedetailleerde systeemvereisten.

---

**Laatst bijgewerkt:** 2026-01-01  
**Getest met:** Aspose.PSD Java nieuwste release  
**Auteur:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}