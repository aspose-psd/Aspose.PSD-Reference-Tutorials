---
date: 2025-12-17
description: Leer hoe u PSD naar PNG kunt converteren terwijl u de kleurmodus van
  PSD instelt op 16‑bit grijswaarden met Aspose.PSD voor Java. Stapsgewijze gids met
  codevoorbeelden.
linktitle: Convert PSD to PNG – 16-bit Grayscale – Java
second_title: Aspose.PSD Java API
title: Hoe PSD naar PNG te converteren met 16‑bit grijswaardenkleurmodus in Java
url: /nl/java/advanced-psd-layer-features-effects/support-16-bit-grayscale-color-mode-psd/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Convert PSD to PNG with 16-bit Grayscale Color Mode in Java

## Introduction
Wanneer je je onderdompelt in de wereld van grafisch ontwerp en beeldbewerking, is het begrijpen hoe je **convert PSD to PNG** is als een geheim wapen. In het bijzonder geeft het gebruik van een 16‑bit grijswaardenmodus je afbeeldingen een verbluffende diepte en detail die ze echt laten opvallen. In deze tutorial lopen we stap voor stap door hoe je **set PSD color mode** naar 16‑bit grijswaarden en vervolgens **export PSD as PNG** met Aspose.PSD voor Java. Klaar om je beeldworkflow naar een hoger niveau te tillen? Laten we beginnen.

## Quick Answers
- **Wat houdt “convert PSD to PNG” in?** Een PSD laden, eventueel de kleurmodus wijzigen, en opslaan als PNG‑bestand.  
- **Welke Aspose‑klasse behandelt de conversie?** `PsdImage` voor het laden en `PngOptions` voor het opslaan.  
- **Heb ik een speciale licentie nodig?** Een proefversie werkt voor testen; een betaalde licentie is vereist voor productie.  
- **Kan ik de 16‑bit diepte behouden in PNG?** Ja, door `PngColorType.GrayscaleWithAlpha` te gebruiken.  
- **Welke IDE's worden ondersteund?** Elke Java‑IDE – IntelliJ IDEA, Eclipse, VS Code, enz.

## Prerequisites
Voordat we beginnen, laten we ervoor zorgen dat je alles hebt ingesteld om het meeste uit deze tutorial te halen. Dit is wat je nodig hebt:

1. **Java Development Kit (JDK)** – Zorg ervoor dat je de nieuwste versie geïnstalleerd hebt. Je kunt het downloaden van [Oracle's site](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).  
2. **Aspose.PSD for Java Library** – Dit is de engine die ons in staat stelt PSD‑bestanden te manipuleren. Haal het van de [Aspose download page](https://releases.aspose.com/psd/java/).  
3. **Een IDE** – IntelliJ IDEA, Eclipse of Visual Studio Code werkt prima.  
4. **Basiskennis van Java** – Vertrouwdheid met Java‑syntaxis maakt de stappen soepeler.  
5. **Een voorbeeld‑PSD‑bestand** – Maak er een in Adobe Photoshop of download een gratis voorbeeld online.

Klaar? Geweldig! Laten we de benodigde pakketten importeren en beginnen met coderen.

## Import Packages
Om te beginnen, voeg de vereiste Aspose.PSD‑imports toe aan je Java‑bestand:

```java
import com.aspose.psd.*;
import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.fileformats.psd.ColorModes;
import com.aspose.psd.fileformats.psd.CompressionMethod;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.PngOptions;
import com.aspose.psd.imageoptions.PsdOptions;
import com.aspose.psd.system.Enum;
```

## Step 1: Define Your Directories
Eerst stel je de bron- en uitvoermappen in. Dit vertelt het programma waar het de oorspronkelijke PSD moet lezen en waar het de geconverteerde bestanden moet schrijven.

```java
String sourceDir = "Your Source Directory"; // Change to your source directory
String outputDir = "Your Document Directory"; // Change to your output directory
```

## Step 2: Create a Method to Handle Image Processing
We zullen de conversielogica in een herbruikbare methode onderbrengen. Deze ontvangt alle parameters die je eventueel wilt aanpassen, zoals kleurmodus, bitdiepte en compressie.

```java
class LocalScopeExtension {
    void saveToPsdThenLoadAndSaveToPng(
        String file,
        short colorMode,
        short channelBitsCount,
        short channelsCount,
        short compression,
        int layerNumber) {
```

## Step 3: Define File Paths and Load the PSD
Binnen de methode bouw je de volledige bestands‑paden op en laad je de oorspronkelijke 16‑bit grijswaarden‑PSD:

```java
String filePath = sourceDir + file + ".psd";
String postfix = Enum.getName(ColorModes.class, colorMode) + channelBitsCount + "_" +
                 channelsCount + "_" + Enum.getName(CompressionMethod.class, compression);
String exportPath = outputDir + file + postfix + ".psd";
String pngExportPath = outputDir + file + postfix + ".png";
// Load a predefined 16-bit grayscale PSD
PsdImage image = (PsdImage)Image.load(filePath);
```

De `postfix` helpt je bij te houden welke instellingen voor elk geëxporteerd bestand zijn gebruikt.

## Step 4: Process the Layer or Full Image
Nu tekenen we ofwel op een specifieke laag of op de volledige afbeelding. In dit voorbeeld voegen we een subtiele grijze rand toe om het resultaat beter zichtbaar te maken.

```java
try {
    RasterCachedImage raster = layerNumber >= 0 ? image.getLayers()[layerNumber] : image;
    // Draw a gray inner border around the perimeter of the layer
    Graphics graphics = new Graphics(raster);
    int width = raster.getWidth();
    int height = raster.getHeight();
    Rectangle rect = new Rectangle(
        width / 3,
        height / 3,
        width - (2 * (width / 3)) - 1,
        height - (2 * (height / 3)) - 1);
    graphics.drawRectangle(new Pen(Color.getDarkGray(), 1), rect);
```

De rechthoek wordt dynamisch berekend zodat deze gecentreerd blijft, ongeacht de afbeeldingsgrootte.

## Step 5: Save the Modified PSD File
Na het tekenen slaan we de PSD op met precies de kleurmodus en bitdiepte die je hebt opgegeven. Dit is de kern van **setting PSD color mode** vóór conversie.

```java
    // Save a copy of PSD with specific characteristics
    PsdOptions psdOptions = new PsdOptions();
    psdOptions.setColorMode(colorMode);
    psdOptions.setChannelBitsCount(channelBitsCount);
    psdOptions.setChannelsCount(channelsCount);
    psdOptions.setCompressionMethod(compression);
    image.save(exportPath, psdOptions);
}
```

## Step 6: Convert the PSD to PNG
Tot slot laden we de nieuw opgeslagen PSD en exporteren we deze als PNG. Door `PngColorType.GrayscaleWithAlpha` te gebruiken behouden we de 16‑bit diepte in het PNG‑bestand.

```java
finally {
    image.dispose();
}
// Load the saved PSD
PsdImage image1 = (PsdImage)Image.load(exportPath);
try {
    // Convert the saved PSD to a grayscale PNG image
    PngOptions pngOptions = new PngOptions();
    pngOptions.setColorType(PngColorType.GrayscaleWithAlpha);
    image1.save(pngExportPath, pngOptions); // here should be no exception
}
finally {
    image1.dispose();
}
```

Nu heb je met succes **converted PSD to PNG** uitgevoerd terwijl je de hoogwaardige 16‑bit grijswaarden‑data behoudt.

## Common Issues and Solutions
| Probleem | Waarom het gebeurt | Oplossing |
|----------|--------------------|-----------|
| **“Unsupported color type” exception** | Proberen een PSD op te slaan met een niet‑ondersteunde kanaalconfiguratie. | Zorg ervoor dat `channelBitsCount` overeenkomt met de werkelijke bitdiepte (16) en `channelsCount` correct is voor grijswaarden (1). |
| **File not found** | Onjuist pad naar bronmap. | Controleer de `sourceDir`‑string en verifieer dat het PSD‑bestand bestaat. |
| **Output PNG appears black** | PNG opgeslagen zonder alpha‑kanaalafhandeling. | Gebruik `PngColorType.GrayscaleWithAlpha` zoals hierboven getoond. |

## Frequently Asked Questions

**Q: Wat is 16-bit grijswaarden‑kleurmodus?**  
A: Het biedt 65 536 grijstinten, wat veel meer tonale detail levert dan de standaard 8‑bit (256 tinten).

**Q: Kan ik Aspose.PSD gebruiken voor niet‑grijswaarden‑afbeeldingen?**  
A: Zeker! Aspose.PSD ondersteunt RGB, CMYK, Lab en vele andere kleurmodi.

**Q: Is er een proefversie van Aspose.PSD?**  
A: Ja, je kunt een gratis proefversie van Aspose.PSD uitproberen. Ga gewoon naar de [Aspose download page](https://releases.aspose.com/).

**Q: Waar kan ik meer voorbeelden vinden van het gebruik van Aspose.PSD?**  
A: Je kunt de [documentation](https://reference.aspose.com/psd/java/) raadplegen voor meer diepgaande voorbeelden en tutorials.

**Q: Hoe koop ik een licentie voor Aspose.PSD?**  
A: Je kunt een licentie kopen door de [Aspose purchase page](https://purchase.aspose.com/buy) te bezoeken.

---

**Laatst bijgewerkt:** 2025-12-17  
**Getest met:** Aspose.PSD for Java 24.12 (latest at time of writing)  
**Auteur:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}