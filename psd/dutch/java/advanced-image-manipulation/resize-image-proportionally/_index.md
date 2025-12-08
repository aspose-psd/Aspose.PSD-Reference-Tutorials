---
date: 2025-12-08
description: Leer hoe je PSD naar PNG kunt converteren en afbeeldingen proportioneel
  kunt schalen in Java met Aspose.PSD. Deze stapsgewijze tutorial behandelt het cachen
  van afbeeldingen, het schalen en het opslaan als PNG.
language: nl
linktitle: Convert PSD to PNG & Resize Proportionally
second_title: Aspose.PSD Java API
title: Hoe PSD naar PNG converteren en proportioneel schalen met Aspose.PSD voor Java
url: /java/advanced-image-manipulation/resize-image-proportionally/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Hoe PSD naar PNG te converteren en proportioneel te schalen met Aspose.PSD voor Java

## Introduction

Als u **PSD naar PNG moet converteren** terwijl u de oorspronkelijke beeldverhouding behoudt, bent u hier aan het juiste adres. In deze tutorial lopen we een volledige **Aspose.PSD tutorial** door die laat zien **hoe u afbeelding** bestanden proportioneel kunt schalen in Java, de afbeelding kunt cachen voor optimale prestaties, en uiteindelijk het resultaat opslaat als PNG. Aan het einde kunt u deze workflow integreren in elke Java‑gebaseerde beeldverwerkingspipeline.

## Quick Answers
- **Kan Aspose.PSD PSD naar PNG converteren?** Ja – laad eenvoudig de PSD en sla deze op met `PngOptions`.
- **Ondersteunt de bibliotheek proportioneel schalen?** Absoluut; gebruik `resizeWidthProportionally` en `resizeHeightProportionally`.
- **Moet ik de afbeelding eerst cachen?** Caching (`image.cacheData()`) verbetert de prestaties voor grote PSD‑bestanden.
- **Welke Java‑versie is vereist?** Java 8 of nieuwer wordt volledig ondersteund.
- **Is een licentie vereist voor productie?** Ja, een commerciële licentie verwijdert evaluatiewatermerken.

## What is “convert PSD to PNG” and why does it matter?

Het converteren van een Photoshop‑document (PSD) naar een portable network graphics (PNG) bestand stelt u in staat gelaagde ontwerpen te delen als een lichtgewicht, web‑vriendelijk formaat. PNG behoudt transparantie en verliesvrije kwaliteit, waardoor het ideaal is voor UI‑assets, thumbnails, of elke situatie waarin beeldkwaliteit belangrijk is.

## Why resize image proportionally in Java?

Het **hoe afbeelding te schalen** zonder de beeldverhouding te vervormen zorgt ervoor dat graphics er natuurlijk uitzien op verschillende schermen. De `Aspose.PSD` API biedt speciale methoden voor proportionele schaalvergroting, die automatisch de bijpassende hoogte of breedte berekenen, waardoor u handmatige rekenfouten voorkomt.

## Prerequisites

Voordat we in de code duiken, zorg ervoor dat u het volgende heeft:

1. **Java Development Kit (JDK)** – Java 8 of later geïnstalleerd.
2. **Aspose.PSD for Java** – download de nieuwste JAR van de officiële site [here](https://releases.aspose.com/psd/java/).
3. Een voorbeeld‑PSD‑bestand (`sample.psd`) geplaatst in een map die u vanuit uw project kunt refereren.

## Import Packages

Voeg de benodigde imports toe aan uw Java‑klasse. Deze klassen geven u toegang tot het laden van afbeeldingen, cachen, schalen en PNG‑uitvoeropties.

```java
import com.aspose.psd.Image;
import com.aspose.psd.imageoptions.PngOptions;
```

## Step 1: Load the PSD Image

Eerst laadt u het bron‑PSD‑bestand. Als het bestand groot is, vermindert cachen van de afbeeldingsgegevens het geheugenverbruik wanneer u later bewerkingen uitvoert.

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

Image image = Image.load(sourceFile);

if (!image.isCached()) {
    // Image caching java – improves performance for large files
    image.cacheData();
}
```

## Step 2: Resize Image Proportionally (Java)

Bepaal nu de nieuwe afmetingen. In dit voorbeeld verkleinen we de afbeelding tot **de helft** van de oorspronkelijke grootte terwijl we de beeldverhouding behouden. U kunt de doelbreedte of -hoogte naar wens aanpassen.

```java
int newWidth = image.getWidth() / 2;
image.resizeWidthProportionally(newWidth);

int newHeight = image.getHeight() / 2;
image.resizeHeightProportionally(newHeight);
```

> **Pro tip:** Gebruik `resizeWidthProportionally` *of* `resizeHeightProportionally` — de bibliotheek berekent automatisch de andere dimensie om de afbeelding proportioneel te houden.

## Step 3: Save the Resized Image as PNG

Exporteer tenslotte de geschaalde afbeelding naar PNG‑formaat. Deze stap voltooit de **convert PSD to PNG** workflow.

```java
String destName = dataDir + "SimpleResizeImageProportionally_out.png";
image.save(destName, new PngOptions());
```

Wanneer de code wordt uitgevoerd, vindt u een PNG‑bestand dat de helft van de grootte van de oorspronkelijke PSD heeft, met dezelfde visuele kwaliteit en zonder vervorming.

## Common Issues & Solutions

| Probleem | Oorzaak | Oplossing |
|----------|----------|-----------|
| **OutOfMemoryError** | Grote PSD niet gecached | Roep `image.cacheData()` aan vóór het schalen |
| **Lege PNG‑output** | Onjuist bestandspad | Controleer `dataDir` en schrijfrechten |
| **Beeldverhouding lijkt verkeerd** | Zowel breedte als hoogte handmatig gebruikt | Gebruik de proportionele methoden die Aspose.PSD biedt |

## Frequently Asked Questions

**Q: Is Aspose.PSD compatible with all image formats?**  
A: Aspose.PSD ondersteunt PSD, PNG, JPEG, BMP, GIF en nog veel meer. Zie de volledige lijst in de [documentatie](https://reference.aspose.com/psd/java/).

**Q: Kan ik Aspose.PSD gebruiken voor commerciële projecten?**  
A: Ja. Koop een commerciële licentie in de [Aspose store](https://purchase.aspose.com/buy).

**Q: Zijn tijdelijke licenties beschikbaar voor testen?**  
A: Absoluut – vraag een tijdelijke licentie [hier](https://purchase.aspose.com/temporary-license/) aan voor evaluatiedoeleinden.

**Q: Waar kan ik community‑ondersteuning vinden?**  
A: Het [Aspose.PSD‑forum](https://forum.aspose.com/c/psd/34) is een uitstekende plek om vragen te stellen en oplossingen te delen.

**Q: Hoe krijg ik toegang tot de volledige API‑referentie?**  
A: Gedetailleerde API‑documentatie is beschikbaar [hier](https://reference.aspose.com/psd/java/).

## Conclusion

U weet nu hoe u **PSD naar PNG kunt converteren**, de afbeelding proportioneel kunt schalen en efficiënt kunt cachen met Aspose.PSD voor Java. Integreer deze stappen in uw eigen applicaties om snelle, hoogwaardige beeldverwerking te leveren zonder afhankelijk te zijn van native Photoshop‑installaties.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Last Updated:** 2025-12-08  
**Tested With:** Aspose.PSD 24.12 for Java  
**Author:** Aspose