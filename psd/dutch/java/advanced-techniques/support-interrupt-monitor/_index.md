---
date: 2026-06-08
description: Leer hoe u PSD kunt opslaan als PNG met behulp van Aspose.PSD voor Java
  en de conversie kunt onderbreken wanneer nodig. Beheer de afbeeldingsworkflow efficiënt.
keywords:
- save psd as png
- how to interrupt conversion
- psd to png conversion
- manage image workflow
linktitle: Ondersteuning voor Interrupt Monitor
schemas:
- author: Aspose
  dateModified: '2026-06-08'
  description: Learn how to save PSD as PNG using Aspose.PSD for Java and interrupt
    conversion when needed. Manage image workflow efficiently.
  headline: How to Save PSD as PNG with Interrupt Monitor in Aspose.PSD for Java
  type: TechArticle
- description: Learn how to save PSD as PNG using Aspose.PSD for Java and interrupt
    conversion when needed. Manage image workflow efficiently.
  name: How to Save PSD as PNG with Interrupt Monitor in Aspose.PSD for Java
  steps:
  - name: Set Your Document Directory
    text: Ensure to replace “Your Document Directory” with the actual path where your
      PSD documents are stored.
  - name: Define Image Options and Output Path
    text: Specify the image options, source PSD file, and the desired output path
      for the converted image.
  - name: Initialize Interrupt Monitor and SaveImageWorker
    text: The `InterruptMonitor` class watches a running conversion and can interrupt
      it when `requestInterrupt()` is called. Create instances of `InterruptMonitor`
      and `SaveImageWorker`, linking the monitor to the image conversion worker.
  - name: Start Image Conversion Thread
    text: Initiate a new thread for the image conversion process and introduce a timeout
      period to anticipate interruption.
  - name: Interrupt the Process
    text: Calling `monitor.requestInterrupt()` signals the monitor to abort the ongoing
      conversion. Interrupt the image conversion process using the `InterruptMonitor`
      and wait for the interruption to complete. Finally, clean up by deleting the
      output file.
  type: HowTo
- questions:
  - answer: Yes, use `InterruptMonitor` to stop the process on demand.
    question: Can I interrupt a PSD‑to‑PNG conversion?
  - answer: Call `save(outputPath, new PngOptions())`.
    question: Which method saves a PSD as PNG?
  - answer: A commercial license is required; a free trial is available.
    question: Do I need a license for production?
  - answer: Java 8 and later are fully supported.
    question: What Java version is supported?
  - answer: Conversions can run in separate threads; the monitor handles interruptions
      safely.
    question: Is the library thread‑safe?
  type: FAQPage
second_title: Aspose.PSD Java API
title: Hoe PSD opslaan als PNG met Interrupt Monitor in Aspose.PSD voor Java
url: /nl/java/advanced-techniques/support-interrupt-monitor/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# PSD opslaan als PNG met Interrupt Monitor in Aspose.PSD voor Java

## Introductie

Als je **PSD als PNG wilt opslaan** terwijl je volledige controle behoudt over langdurige conversies, biedt de Interrupt Monitor van Aspose.PSD voor Java precies dat. In deze tutorial lopen we door het instellen van de monitor, het converteren van een PSD‑bestand naar PNG, en het veilig afbreken van de bewerking wanneer dat nodig is. Je ziet ook hoe dit past in een typische beeldverwerkingsworkflow en waarom het een onmisbare functie is voor robuuste applicaties.

## Snelle antwoorden
- **Kan ik een PSD‑naar‑PNG conversie onderbreken?** Ja, gebruik `InterruptMonitor` om het proces op verzoek te stoppen.  
- **Welke methode slaat een PSD op als PNG?** Roep `save(outputPath, new PngOptions())` aan.  
- **Heb ik een licentie nodig voor productie?** Een commerciële licentie is vereist; een gratis proefversie is beschikbaar.  
- **Welke Java‑versie wordt ondersteund?** Java 8 en hoger worden volledig ondersteund.  
- **Is de bibliotheek thread‑safe?** Conversies kunnen in afzonderlijke threads draaien; de monitor behandelt onderbrekingen veilig.

## Vereisten

Voordat je de details van het gebruik van Interrupt Monitor induikt, zorg ervoor dat je de volgende vereisten hebt:

- **Java‑ontwikkelomgeving:** Richt een Java‑ontwikkelomgeving op je systeem in.  
- **Aspose.PSD‑bibliotheek:** Verkrijg de Aspose.PSD voor Java bibliotheek. Je kunt deze downloaden [hier](https://releases.aspose.com/psd/java/). Je kunt ook de hoofd‑Aspose‑site bezoeken [hier](https://releases.aspose.com/).  
- **Documentmap:** Zorg voor een aangewezen map voor je PSD‑documenten.

## Pakketten importeren

Begin met het importeren van de benodigde pakketten in je Java‑project. Dit zorgt ervoor dat je toegang hebt tot de functionaliteiten van Aspose.PSD.

```java
import com.aspose.psd.ImageOptionsBase;

import static com.aspose.psd.examples.Utils.Utils.getDateTime;
import com.aspose.psd.imageoptions.PngOptions;
import com.aspose.psd.multithreading.InterruptMonitor;
import com.aspose.psd.system.Threading.ThreadStart;
import java.io.File;
```

Laten we nu de voorbeeldcode stap voor stap ontleden voor het integreren van Interrupt Monitor in je Aspose.PSD voor Java‑project.

## Hoe PSD opslaan als PNG met behulp van de Interrupt Monitor?

`PsdImage` vertegenwoordigt een PSD‑document dat in het geheugen is geladen.  
`SaveImageWorker` voert de beeldconversie uit in een aparte thread.  

Laad je PSD‑bestand met `new PsdImage("source.psd")`, koppel een `InterruptMonitor` aan de `SaveImageWorker`, en roep `save("output.png", new PngOptions())` aan. De monitor houdt een annuleringsverzoek in de gaten en stopt de conversie netjes, waardoor de controle binnen enkele milliseconden terugkeert naar je applicatie.

### Stap 1: Stel je documentmap in

```java
String dataDir = "Your Document Directory";
```

Zorg ervoor dat je “Your Document Directory” vervangt door het daadwerkelijke pad waar je PSD‑documenten zijn opgeslagen.

### Stap 2: Definieer afbeeldingsopties en uitvoerpad

```java
ImageOptionsBase saveOptions = new PngOptions();
String source = dataDir + "big2.psb";
String output = dataDir + "big_out.png";
```

Specificeer de afbeeldingsopties, het bron‑PSD‑bestand en het gewenste uitvoerpad voor de geconverteerde afbeelding.

### Stap 3: Initialiseer Interrupt Monitor en SaveImageWorker

De `InterruptMonitor`‑klasse houdt een lopende conversie in de gaten en kan deze onderbreken wanneer `requestInterrupt()` wordt aangeroepen.  

```java
InterruptMonitor monitor = new InterruptMonitor();
SaveImageWorker worker = new SaveImageWorker(source, output, saveOptions, monitor);
```

Maak instanties van `InterruptMonitor` en `SaveImageWorker` aan, en koppel de monitor aan de afbeelding‑conversiewerker.

### Stap 4: Start afbeeldingsconversie‑thread

```java
Thread thread = new Thread(worker.ThreadProc());
try {
    thread.start();
    // Add a timeout to allow for potential interruption
    Thread.sleep(3000);
```

Start een nieuwe thread voor het afbeeldingsconversieproces en introduceer een timeout‑periode om een onderbreking te anticiperen.

### Stap 5: Onderbreek het proces

Het aanroepen van `monitor.requestInterrupt()` signaleert de monitor om de lopende conversie af te breken.  

```java
    // Interrupt the process
    monitor.interrupt();
    System.out.println("Interrupting the save thread #" + thread.getId() + " at " + getDateTime().toString());

    // Wait for interruption...
    thread.join();
} finally {
    // Delete the output file if it exists
    File f = new File(output);
    if (f.exists()) {
        f.delete();
    }
}
```

Onderbreek het afbeeldingsconversieproces met behulp van de `InterruptMonitor` en wacht tot de onderbreking is voltooid. Verwijder ten slotte het uitvoerbestand.

## Waarom de Interrupt Monitor gebruiken voor PSD‑naar‑PNG conversie?

Aspose.PSD ondersteunt **30+ uitvoerformaten**, waaronder PNG, JPEG, BMP en TIFF, en kan bestanden tot **500 MB** verwerken zonder het volledige document in het geheugen te laden. Door een interrupt monitor toe te voegen, verminder je CPU‑verspilling en verbeter je de responsiviteit in batch‑verwerkingspijplijnen, vooral wanneer een conversie de verwachte tijdslimieten overschrijdt.

## Veelvoorkomende problemen en oplossingen

- **Conversie blijft oneindig hangen:** Zorg ervoor dat de monitor is gekoppeld **voordat** `save` wordt aangeroepen.  
- **Uitvoerbestand is corrupt na onderbreking:** De monitor stopt netjes; controleer echter altijd of het bestand bestaat voordat je het gebruikt.  
- **Thread‑safety zorgen:** Voer elke conversie uit in een eigen thread; de monitor beïnvloedt alleen de bijbehorende worker.

## Veelgestelde vragen

**Q1: Wat is een Interrupt Monitor in Aspose.PSD voor Java?**  
A: De Interrupt Monitor stelt ontwikkelaars in staat om langdurige beeldconversies te pauzeren of te annuleren, waardoor ze realtime controle over het resourcegebruik krijgen.

**Q2: Hoe kan ik de Aspose.PSD‑bibliotheek voor Java verkrijgen?**  
A: Je kunt de Aspose.PSD voor Java‑bibliotheek downloaden [hier](https://releases.aspose.com/psd/java/).

**Q3: Is er een gratis proefversie beschikbaar voor Aspose.PSD voor Java?**  
A: Ja, je kunt een gratis proefversie van Aspose.PSD verkennen [hier](https://releases.aspose.com/).

**Q4: Waar kan ik ondersteuning vinden voor Aspose.PSD voor Java?**  
A: Bezoek het Aspose.PSD voor Java‑ondersteuningsforum [hier](https://forum.aspose.com/c/psd/34).

**Q5: Hoe kan ik een licentie kopen voor Aspose.PSD voor Java?**  
A: Je kunt een licentie voor Aspose.PSD voor Java kopen [hier](https://purchase.aspose.com/buy).

**Q6: Kan ik meerdere PSD‑bestanden parallel naar PNG converteren?**  
A: Ja, spawn een aparte thread voor elk bestand en koppel een individuele `InterruptMonitor` aan elke conversiewerker.

**Q7: Handelt de bibliotheek kleurprofielen af tijdens PSD‑naar‑PNG conversie?**  
A: Absoluut; Aspose.PSD behoudt ingesloten ICC‑profielen en past ze automatisch toe op de uitvoer‑PNG.

---

**Laatst bijgewerkt:** 2026-06-08  
**Getest met:** Aspose.PSD 23.12 voor Java  
**Auteur:** Aspose  

{{< blocks/products/products-backtop-button >}}

## Gerelateerde tutorials

- [PSD opslaan als PNG en Rendering Drop Shadow toepassen in Aspose.PSD voor Java](/psd/java/advanced-image-manipulation/rendering-drop-shadow/)
- [Export PSD naar PNG & Voeg een nieuwe reguliere laag toe met Aspose.PSD voor Java](/psd/java/advanced-image-effects/add-new-regular-layer/)
- [Ondersteuning voor Interrupt Monitor in PSD‑bestanden - Java](/psd/java/psd-layer-management-effects/support-interrupt-monitor-psd-files/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}