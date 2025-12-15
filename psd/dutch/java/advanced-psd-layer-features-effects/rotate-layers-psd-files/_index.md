---
date: 2025-12-15
description: Leer hoe je PSD naar PNG converteert en PSD‑lagen roteert in Java met
  Aspose.PSD. Stapsgewijze handleiding met codevoorbeelden.
linktitle: Convert PSD to PNG and Rotate Layers in PSD Files using Java
second_title: Aspose.PSD Java API
title: Converteer PSD naar PNG en roteer lagen in PSD‑bestanden met Java
url: /nl/java/advanced-psd-layer-features-effects/rotate-layers-psd-files/
weight: 21
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# PSD naar PNG converteren en lagen in PSD‑bestanden roteren met Java

## Introductie
Als je **PSD naar PNG wilt converteren** terwijl je ook lagen roteert, is deze gids voor jou. Of je nu een batch‑verwerkingstool bouwt of beeldbewerking integreert in een webservice, dit programmatic doen bespaart tijd en verwijdert de afhankelijkheid van Adobe Photoshop. In deze tutorial laten we je zien **hoe je PSD‑lagen roteert** en het resultaat exporteert als een PNG met behulp van de Aspose.PSD‑bibliotheek voor Java. Laten we de mouwen opstropen en je ontwerpworkflow soepel laten verlopen!

## Snelle antwoorden
- **Welke bibliotheek kan ik gebruiken?** Aspose.PSD for Java  
- **Kan ik zowel roteren als converteren in één stap?** Ja – roteer de PSD en sla vervolgens op als PNG  
- **Heb ik een licentie nodig?** Een gratis proefversie werkt voor testen; een betaalde licentie is vereist voor productie  
- **Welke Java‑versie wordt ondersteund?** Java 8 en later  
- **Is de PNG‑output transparant?** Ja, wanneer je `PngColorType.TruecolorWithAlpha` instelt  

## Wat is “PSD naar PNG converteren”?
Het converteren van een Photoshop‑document (PSD) naar een PNG‑afbeelding betekent het extraheren van de visuele inhoud—incl. alle lagen, maskers en transparantie—naar een breed ondersteund rasterformaat. PNG behoudt alfakanalen, waardoor het ideaal is voor web‑graphics, miniaturen en verdere beeldverwerking.

## Waarom Aspose.PSD for Java gebruiken om PSD naar PNG te converteren en PSD‑lagen te roteren?
- **Geen Photoshop nodig** – werkt op elke server of CI‑omgeving  
- **Volledige laagondersteuning** – behoudt transparantie en laag‑effecten intact  
- **Eenvoudige API** – roteer, spiegel en sla op met slechts een paar methode‑aanroepen  
- **Cross‑platform** – draait op Windows, Linux en macOS  

## Voorvereisten
Voordat we in de code duiken, zorg ervoor dat je het volgende hebt:

- **Java Development Kit (JDK)** – download van de [Oracle‑website](https://www.oracle.com/java/technologies/javase-downloads.html).  
- **Integrated Development Environment (IDE)** – IntelliJ IDEA, Eclipse of NetBeans zijn allemaal geschikt.  
- **Aspose.PSD for Java library** – verkrijg de nieuwste JAR van de [release‑pagina](https://releases.aspose.com/psd/java/).  
- **Basiskennis van Java** – vertrouwdheid met klassen, objecten en foutafhandeling.  

## Stapsgewijze handleiding

### Stap 1: Stel je Java‑project in
Maak een nieuw Java‑project aan in je IDE en voeg de Aspose.PSD‑JAR toe aan het build‑pad van het project.

### Stap 2: Importeer vereiste klassen
Voeg de volgende imports toe aan de bovenkant van je Java‑bronbestand:

```java
import com.aspose.psd.Image;
import com.aspose.psd.RotateFlipType;
import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.PngOptions;
```

Deze klassen geven je toegang tot het laden van afbeeldingen, rotatie en PNG‑specifieke opties.

### Stap 3: Definieer bestands‑paden
Geef aan waar je bron‑PSD zich bevindt en waar de uitvoerbestanden moeten worden geschreven.

```java
String dataDir = "Your Document Directory"; // Change this to your actual document directory.
String sourceFile = dataDir + "1.psd"; // Source PSD file
String pngPath = dataDir + "RotateFlipTest2617.png"; // Output PNG file path
String psdPath = dataDir + "RotateFlipTest2617.psd"; // Output PSD file path
```

> **Pro tip:** Gebruik een absoluut pad tijdens het testen om “bestand niet gevonden” fouten te voorkomen.

### Stap 4: Laad het PSD‑bestand
Laad de PSD in een manipuleerbaar object.

```java
PsdImage im = (PsdImage) Image.load(sourceFile);
```

Nu vertegenwoordigt `im` het volledige Photoshop‑document, inclusief alle lagen.

### Stap 5: Roteer de afbeelding (Hoe PSD te roteren)
Kies een rotatietype uit `RotateFlipType`. In dit voorbeeld roteren we 270° en spiegelen we beide assen.

```java
int flipType = RotateFlipType.Rotate270FlipXY; // Choose the rotation type
im.rotateFlip(flipType); // Rotate the image
```

Voel je vrij om te experimenteren met andere waarden zoals `Rotate90FlipNone` of `Rotate180FlipX`.

### Stap 6: Sla de geroteerde afbeelding op als PNG (PSD naar PNG converteren)
Configureer PNG‑opties om transparantie te behouden, en sla vervolgens op.

```java
PngOptions options = new PngOptions();
options.setColorType(PngColorType.TruecolorWithAlpha); // Preserve transparency
im.save(pngPath, options); // Save the rotated image
```

De resulterende PNG behoudt laag‑transparantie, waardoor deze klaar is voor webgebruik.

### Stap 7: Sla de gewijzigde PSD op (optioneel)
Als je ook een nieuwe PSD nodig hebt met de toegepaste rotatie, sla deze dan opnieuw op.

```java
im.save(psdPath);
```

Je hebt nu zowel een PNG‑preview als een bijgewerkt PSD‑bestand.

## Veelvoorkomende problemen en oplossingen
- **Bestand niet gevonden:** Controleer of `dataDir` eindigt op een pad‑scheidingsteken (`/` of `\`).  
- **OutOfMemoryError bij grote PSD’s:** Verhoog de JVM‑heap‑grootte (`-Xmx2g`).  
- **Transparantie verloren:** Zorg ervoor dat `PngColorType.TruecolorWithAlpha` is ingesteld; anders wordt de PNG zonder alfa opgeslagen.

## Veelgestelde vragen

### Kan ik een specifieke laag in een PSD‑bestand roteren?
Ja, je kunt `Layer.rotateFlip()` gebruiken op individuele lagen na iteratie over `im.getLayers()`.

### Zijn er prestatiebeperkingen met Aspose.PSD for Java?
De bibliotheek verwerkt de meeste bestanden efficiënt, maar extreem grote PSD’s (>500 MB) kunnen extra geheugen vereisen.

### Is Aspose.PSD gratis te gebruiken?
Aspose biedt een gratis proefversie, maar een betaalde licentie is nodig voor productie. Bekijk de [tijdelijke licentie](https://purchase.aspose.com/temporary-license/) voor testen.

### Waar kan ik gedetailleerde documentatie vinden?
Je kunt uitgebreide documentatie vinden op [Aspose.PSD Documentation](https://reference.aspose.com/psd/java/).

### Wat als ik problemen ondervind bij het gebruik van Aspose.PSD?
Vraag hulp via het [Aspose Support Forum](https://forum.aspose.com/c/psd/34).

## Aanvullende veelgestelde vragen

**Q: Behoudt het converteren van PSD naar PNG laag‑effecten?**  
**A: Ja, wanneer je opslaat met `PngColorType.TruecolorWithAlpha`, worden de meeste visuele effecten gerasterd in de PNG.**

**Q: Kan ik meerdere PSD‑bestanden batch‑verwerken?**  
**A: Zeker. Plaats de code in een lus die over een map met PSD‑bestanden iterereert.**

**Q: Is het mogelijk om het PNG‑compressieniveau in te stellen?**  
**A: De `PngOptions`‑klasse biedt een `setCompressionLevel(int)`‑methode voor fijne afstemming.**

**Q: Moet ik het afbeelding‑object sluiten?**  
**A: `PsdImage` implementeert `Closeable`; roep `im.close()` aan in een `finally`‑blok of gebruik try‑with‑resources.**

**Q: Heeft de geroteerde PNG dezelfde afmetingen als het origineel?**  
**A: Rotatie met 90° of 270° verwisselt breedte en hoogte. De PNG zal de nieuwe oriëntatie weergeven.**

## Conclusie
Door gebruik te maken van Aspose.PSD for Java kun je **PSD naar PNG converteren** en **PSD‑lagen roteren** met slechts een paar regels code. Deze aanpak elimineert de noodzaak van Photoshop, versnelt geautomatiseerde workflows en geeft je volledige controle over de beeldoutput. Probeer het in je eigen projecten en zie hoeveel tijd je bespaart!

---

**Last Updated:** 2025-12-15  
**Tested With:** Aspose.PSD for Java 24.11  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}