---
date: 2026-07-22
description: Leer hoe je een psd opslaat als png, PNG-transparantie behoudt en PSD-lagen
  roteert in Java met Aspose.PSD. Stapsgewijze gids, uitleg zonder code en tips voor
  probleemoplossing.
keywords:
- save psd as png
- export psd layers png
- convert photoshop file png
- psd to png transparency
lastmod: 2026-07-22
linktitle: psd opslaan als png en lagen roteren in Java met Aspose.PSD
og_description: psd opslaan als png met Aspose.PSD voor Java. Behoud transparantie,
  roteer lagen en exporteer PNG in slechts een paar regels code—ideaal voor geautomatiseerde
  workflows.
og_image_alt: 'Developer guide: save PSD as PNG and rotate layers using Aspose.PSD
  for Java'
og_title: psd opslaan als png en lagen roteren in Java met Aspose.PSD
schemas:
- author: Aspose
  dateModified: '2026-07-22'
  description: Learn how to save psd as png, preserve PNG transparency, and rotate
    PSD layers in Java with Aspose.PSD. Step‑by‑step guide, code‑free explanations,
    and troubleshooting tips.
  headline: save psd as png and rotate layers in Java using Aspose.PSD
  type: TechArticle
- description: Learn how to save psd as png, preserve PNG transparency, and rotate
    PSD layers in Java with Aspose.PSD. Step‑by‑step guide, code‑free explanations,
    and troubleshooting tips.
  name: save psd as png and rotate layers in Java using Aspose.PSD
  steps:
  - name: Set Up Your Java Project
    text: Create a new Java project in your IDE and add the Aspose.PSD JAR to the
      project’s build path.
  - name: Import Required Classes
    text: '`PsdImage` is the core class that represents a Photoshop document in memory.
      `PngOptions` controls PNG‑specific settings, and `RotateFlipType` defines rotation
      and flip operations. These imports give you access to image loading, rotation,
      and PNG‑specific options.'
  - name: Define File Paths
    text: Specify where your source PSD lives and where the output files should be
      written. Using absolute paths during testing avoids “file not found” errors.
      > **Pro tip:** Store paths in a configuration file for easier maintenance in
      larger projects.
  - name: Load the PSD File
    text: '`PsdImage` loads the entire Photoshop document, including all layers, masks,
      and effects, into a manipulable object. Now `im` represents the whole PSD, ready
      for transformations.'
  - name: Rotate the Image (How to rotate PSD)
    text: '`RotateFlipType` enumerates all supported rotations and flips. In this
      example we rotate 270° and flip both axes, which swaps width and height while
      mirroring the image. Feel free to experiment with other values such as `Rotate90FlipNone`
      or `Rotate180FlipX`.'
  - name: Save the Rotated Image as PNG (save PSD as PNG)
    text: Configure `PngOptions` to keep transparency (`PngColorType.TruecolorWithAlpha`)
      and then call `save`. The PNG retains layer transparency, ensuring it works
      seamlessly in web or mobile apps. The resulting PNG preserves alpha channels,
      making it suitable for compositing or further processing.
  - name: Save the Modified PSD (optional)
    text: If you also need a new PSD with the rotation applied, you can save the modified
      `PsdImage` back to disk. You now have both a PNG preview and an updated PSD
      file.
  type: HowTo
- questions:
  - answer: Yes, you can call `layer.rotateFlip(RotateFlipType.Rotate90FlipNone)`
      after iterating through `im.getLayers()`.
    question: Can I rotate a specific layer in a PSD file?
  - answer: The library handles most files efficiently, but extremely large PSDs (>500
      MB) may require additional memory or streaming options.
    question: Is there any performance limitation with Aspose.PSD for Java?
  - answer: Aspose offers a free trial, but a paid license is needed for production.
      See the [temporary license](https://purchase.aspose.com/temporary-license/)
      for testing.
    question: Is Aspose.PSD free to use?
  - answer: Comprehensive docs are available at [Aspose.PSD Documentation](https://reference.aspose.com/psd/java/).
    question: Where can I find detailed documentation?
  - answer: Get help via the [Aspose Support Forum](https://forum.aspose.com/c/psd/34).
    question: What if I encounter issues while using Aspose.PSD?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- convert PSD
- Aspose.PSD
- Java image processing
- rotate PSD layers
title: psd opslaan als png en lagen roteren in Java met Aspose.PSD
url: /nl/java/advanced-psd-layer-features-effects/rotate-layers-psd-files/
weight: 21
---

## Gerelateerde tutorials

- [PSD opslaan als PNG en Rendering Drop Shadow toepassen in Aspose.PSD voor Java](/psd/java/advanced-image-manipulation/rendering-drop-shadow/)
- [Hoe PNG-bestanden comprimeren met Aspose.PSD voor Java](/psd/java/optimizing-png-files/compress-png-files/)
- [Hoe afbeelding roteren in Java met Aspose.PSD](/psd/java/advanced-image-manipulation/)

{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< blocks/products/pf/main-wrap-class >}}

# psd opslaan als png en lagen roteren in Java met Aspose.PSD

## Inleiding
Als je **PSD als PNG wilt opslaan** terwijl je ook lagen roteert, is deze gids voor jou. Of je nu een batch‑verwerkingstool bouwt, een webservice die on‑the‑fly beeldbewerking nodig heeft, of simpelweg een ontwerp‑workflow automatiseert, het programmatisch doen bespaart tijd en verwijdert de afhankelijkheid van Adobe Photoshop. In deze tutorial lopen we stap voor stap door **hoe PSD‑lagen te roteren** en het resultaat als PNG te exporteren met de Aspose.PSD‑bibliotheek voor Java. Laten we de mouwen opstropen en je ontwerp‑workflow soepel laten draaien!

## Snelle antwoorden
- **Welke bibliotheek kan ik gebruiken?** Aspose.PSD for Java  
- **Kan ik zowel roteren als PSD als PNG opslaan in één stap?** Ja – roteer de PSD en sla vervolgens op als PNG  
- **Heb ik een licentie nodig?** Een gratis proefversie werkt voor testen; een betaalde licentie is vereist voor productie  
- **Welke Java‑versie wordt ondersteund?** Java 8 en later  
- **Is de PNG‑output transparant?** Ja, wanneer je `PngColorType.TruecolorWithAlpha` instelt  

## Wat is “converteren van PSD naar PNG”?
Het converteren van een Photoshop‑document (PSD) naar een PNG‑afbeelding haalt de visuele inhoud—incl. lagen, maskers en alfakanalen—uit en plaatst deze in een breed ondersteund rasterformaat dat transparantie behoudt. Hierdoor is PNG ideaal voor web‑graphics, miniaturen en verdere beeldverwerking. De resulterende PNG kan direct worden gebruikt in webpagina’s, mobiele apps of verder worden verwerkt door andere beeldbibliotheken.

## Waarom Aspose.PSD voor Java gebruiken om PSD als PNG op te slaan en PSD‑lagen te roteren?
Aspose.PSD stelt je in staat om **PSD als PNG op te slaan** en lagen te roteren zonder Photoshop te installeren. Het ondersteunt **meer dan 50 invoer‑ en uitvoerformaten**, verwerkt PSD‑bestanden met honderden pagina’s met minder dan 200 MB RAM, en draait op Windows, Linux en macOS. De API vereist slechts enkele methode‑aanroepen en levert resultaten met hoge nauwkeurigheid dankzij ingebouwde afhandeling van laageffecten, maskers en alfakanalen.

## Vereisten
- **Java Development Kit (JDK)** – download van de [Oracle website](https://www.oracle.com/java/technologies/javase-downloads.html).  
- **Integrated Development Environment (IDE)** – IntelliJ IDEA, Eclipse of NetBeans zijn allemaal prima.  
- **Aspose.PSD for Java library** – verkrijg de nieuwste JAR van de [release page](https://releases.aspose.com/psd/java/).  
- **Basic Java knowledge** – bekendheid met klassen, objecten en exception handling.  

## Stapsgewijze handleiding

### Stap 1: Stel je Java‑project in
Maak een nieuw Java‑project aan in je IDE en voeg de Aspose.PSD‑JAR toe aan het build‑pad van het project.

### Stap 2: Importeer vereiste klassen
`PsdImage` is de kernklasse die een Photoshop‑document in het geheugen vertegenwoordigt. `PngOptions` regelt PNG‑specifieke instellingen, en `RotateFlipType` definieert rotatie‑ en spiegelbewerkingen.

```java
import com.aspose.psd.Image;
import com.aspose.psd.RotateFlipType;
import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.PngOptions;
```

Deze imports geven je toegang tot het laden van afbeeldingen, rotatie en PNG‑specifieke opties.

### Stap 3: Definieer bestands‑paden
Geef aan waar je bron‑PSD zich bevindt en waar de uitvoerbestanden moeten worden geschreven. Het gebruik van absolute paden tijdens testen voorkomt “file not found”‑fouten.

```java
String dataDir = "Your Document Directory"; // Change this to your actual document directory.
String sourceFile = dataDir + "1.psd"; // Source PSD file
String pngPath = dataDir + "RotateFlipTest2617.png"; // Output PNG file path
String psdPath = dataDir + "RotateFlipTest2617.psd"; // Output PSD file path
```

> **Pro tip:** Sla paden op in een configuratie‑bestand voor gemakkelijker onderhoud in grotere projecten.

### Stap 4: Laad het PSD‑bestand
`PsdImage` laadt het volledige Photoshop‑document, inclusief alle lagen, maskers en effecten, in een manipuleerbaar object.

```java
PsdImage im = (PsdImage) Image.load(sourceFile);
```

Nu vertegenwoordigt `im` de volledige PSD, klaar voor transformaties.

### Stap 5: Roteer de afbeelding (Hoe PSD roteren)
`RotateFlipType` somt alle ondersteunde rotaties en spiegels op. In dit voorbeeld roteren we 270° en spiegelen we beide assen, waardoor breedte en hoogte worden verwisseld terwijl de afbeelding wordt gespiegeld.

```java
int flipType = RotateFlipType.Rotate270FlipXY; // Choose the rotation type
im.rotateFlip(flipType); // Rotate the image
```

Voel je vrij om te experimenteren met andere waarden zoals `Rotate90FlipNone` of `Rotate180FlipX`.

### Stap 6: Sla de geroteerde afbeelding op als PNG (PSD als PNG opslaan)
Configureer `PngOptions` om transparantie te behouden (`PngColorType.TruecolorWithAlpha`) en roep vervolgens `save` aan. De PNG behoudt de laag‑transparantie, waardoor deze naadloos werkt in web‑ of mobiele apps.

```java
PngOptions options = new PngOptions();
options.setColorType(PngColorType.TruecolorWithAlpha); // Preserve transparency
im.save(pngPath, options); // Save the rotated image
```

De resulterende PNG behoudt alfakanalen, waardoor deze geschikt is voor compositing of verdere verwerking.

### Stap 7: Sla de gewijzigde PSD op (optioneel)
Als je ook een nieuwe PSD nodig hebt met de toegepaste rotatie, kun je de gewijzigde `PsdImage` terug naar schijf opslaan.

```java
im.save(psdPath);
```

Je hebt nu zowel een PNG‑preview als een bijgewerkt PSD‑bestand.

## Veelvoorkomende problemen en oplossingen
- **Bestand niet gevonden:** Controleer of `dataDir` eindigt met een pad‑scheidingsteken (`/` of `\`).  
- **OutOfMemoryError bij grote PSD’s:** Verhoog de JVM‑heap‑grootte (`-Xmx2g`).  
- **Transparantie verloren:** Zorg ervoor dat `PngColorType.TruecolorWithAlpha` is ingesteld; anders wordt de PNG zonder alfa opgeslagen.  
- **Flip PSD‑afbeelding werkt niet zoals verwacht:** Controleer de `RotateFlipType`‑constante die je hebt gekozen; sommige constanten combineren rotatie en flip in één stap.  

## Veelgestelde vragen

**Q: Kan ik een specifieke laag in een PSD‑bestand roteren?**  
A: Ja, je kunt `layer.rotateFlip(RotateFlipType.Rotate90FlipNone)` aanroepen na het itereren door `im.getLayers()`.

**Q: Zijn er prestatiebeperkingen met Aspose.PSD voor Java?**  
A: De bibliotheek verwerkt de meeste bestanden efficiënt, maar extreem grote PSD’s (>500 MB) kunnen extra geheugen of streaming‑opties vereisen.

**Q: Is Aspose.PSD gratis te gebruiken?**  
A: Aspose biedt een gratis proefversie, maar een betaalde licentie is nodig voor productie. Zie de [temporary license](https://purchase.aspose.com/temporary-license/) voor testen.

**Q: Waar kan ik gedetailleerde documentatie vinden?**  
A: Uitgebreide documentatie is beschikbaar op [Aspose.PSD Documentation](https://reference.aspose.com/psd/java/).

**Q: Wat als ik problemen ondervind bij het gebruik van Aspose.PSD?**  
A: Krijg hulp via het [Aspose Support Forum](https://forum.aspose.com/c/psd/34).

**Q: Behoudt het converteren van PSD naar PNG laageffecten?**  
A: Ja, wanneer je opslaat met `PngColorType.TruecolorWithAlpha`, worden de meeste visuele effecten gerasterd in de PNG.

**Q: Kan ik meerdere PSD‑bestanden batch‑verwerken?**  
A: Zeker. Plaats de code in een lus die over een map met PSD‑bestanden itereren.

**Q: Is het mogelijk om het PNG‑compressieniveau in te stellen?**  
A: `PngOptions` biedt een `setCompressionLevel(int)`‑methode voor het fijn afstemmen van de output‑grootte.

**Q: Moet ik het afbeelding‑object sluiten?**  
A: `PsdImage` implementeert `Closeable`; gebruik try‑with‑resources of roep `im.close()` aan in een `finally`‑blok.

**Q: Heeft de geroteerde PNG dezelfde afmetingen als het origineel?**  
A: Rotatie met 90° of 270° verwisselt breedte en hoogte, dus de PNG past zich automatisch aan de nieuwe oriëntatie aan.

## Conclusie
Door gebruik te maken van Aspose.PSD voor Java kun je **PSD als PNG opslaan**, **PNG‑transparantie behouden**, en **PSD‑lagen roteren** met slechts een paar code‑regels. Deze aanpak elimineert de noodzaak voor Photoshop, versnelt geautomatiseerde workflows en geeft je volledige controle over de beeldoutput. Probeer het in je eigen projecten en zie hoeveel tijd je bespaart!

---

**Laatst bijgewerkt:** 2026-07-22  
**Getest met:** Aspose.PSD for Java 24.11  
**Auteur:** Aspose  

{{< blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/products-backtop-button >}}