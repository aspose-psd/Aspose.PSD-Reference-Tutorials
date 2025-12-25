---
date: 2025-12-25
description: Leer hoe je PSD naar PNG kunt converteren met Aspose.PSD voor Java met
  ondersteuning voor interruptmonitor, inclusief een voorbeeld van een Java-threadinterrupt
  en tips voor het opslaan van PSD als PNG.
linktitle: Support for Interrupt Monitor
second_title: Aspose.PSD Java API
title: Hoe PSD naar PNG converteren met ondersteuning voor Interrupt Monitor in Aspose.PSD
  voor Java
url: /nl/java/advanced-techniques/support-interrupt-monitor/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# PSD naar PNG converteren met Interrupt Monitor in Aspose.PSD voor Java

## Inleiding

Als je **PSD naar PNG** wilt **converteren** terwijl je volledige controle behoudt over langdurige afbeeldingsconversies, is de Interrupt Monitor van Aspose.PSD voor Java het gereedschap dat je zoekt. In deze tutorial lopen we een praktijkvoorbeeld van een **java thread interrupt example** door dat je in staat stelt een conversie halverwege te stoppen, waardoor je de flexibiliteit krijgt om resources te beheren, time‑outs af te dwingen of te reageren op gebruikersannuleringen.

## Snelle antwoorden
- **What does the Interrupt Monitor do?** Het stelt je in staat een lopende afbeeldingsconversie veilig te signaleren om te stoppen.  
- **Can I convert PSD to PNG with it?** Ja – de monitor werkt met elke opslaan‑operatie, inclusief PNG.  
- **Is a separate thread required?** Meestal voer je de conversie uit in een aparte thread zodat je deze kunt onderbreken.  
- **Which Aspose.PSD version is needed?** Elke recente versie die `com.aspose.psd.multithreading.InterruptMonitor` bevat.  
- **Do I need a license for production?** Ja, een geldige Aspose.PSD‑licentie is vereist voor niet‑trial gebruik.

## Wat is “PSD naar PNG converteren” met een Interrupt Monitor?

Het converteren van een groot Photoshop‑document (PSD/PSB) naar een PNG‑afbeelding kan CPU‑intensief zijn. Door een **Interrupt Monitor** aan de conversiewerker te koppelen, krijg je de mogelijkheid om het proces programmatisch te stoppen — perfect voor webservices, batch‑taken of UI‑applicaties waarbij gebruikers operaties kunnen annuleren.

## Waarom de Interrupt Monitor gebruiken?

- **Responsieve UI:** Voorkom dat je applicatie vastloopt terwijl een groot bestand wordt verwerkt.  
- **Resource‑beheer:** Stop conversies die de tijd‑ of geheugenlimieten overschrijden.  
- **Foutafhandeling:** Ruim gedeeltelijke uitvoerbestanden netjes op wanneer een onderbreking optreedt.

## Vereisten

- Java‑ontwikkelomgeving (JDK 8 of nieuwer).  
- Aspose.PSD voor Java‑bibliotheek – download deze **[here](https://releases.aspose.com/psd/java/)**.  
- Een map die de PSD/PSB‑bestanden bevat waarmee je wilt werken.

## Importeer pakketten

Begin met het importeren van de benodigde klassen. Hiermee krijg je toegang tot afbeeldingsopties, de interrupt monitor en threading‑hulpmiddelen.

```java
import com.aspose.psd.ImageOptionsBase;

import static com.aspose.psd.examples.Utils.Utils.getDateTime;
import com.aspose.psd.imageoptions.PngOptions;
import com.aspose.psd.multithreading.InterruptMonitor;
import com.aspose.psd.system.Threading.ThreadStart;
import java.io.File;
```

## Stapsgewijze handleiding

### Stap 1: Stel uw documentmap in

```java
String dataDir = "Your Document Directory";
```

Vervang `"Your Document Directory"` door het absolute pad waar je PSD‑bestanden zich bevinden.

### Stap 2: Definieer afbeeldingsopties en uitvoerpad

```java
ImageOptionsBase saveOptions = new PngOptions();
String source = dataDir + "big2.psb";
String output = dataDir + "big_out.png";
```

Hier **saven we PSD als PNG** met behulp van `PngOptions`. Pas de bestandsnamen aan indien nodig.

### Stap 3: Initialiseer Interrupt Monitor en SaveImageWorker

```java
InterruptMonitor monitor = new InterruptMonitor();
SaveImageWorker worker = new SaveImageWorker(source, output, saveOptions, monitor);
```

De `InterruptMonitor`‑instantie wordt later gebruikt om de conversie te stoppen. `SaveImageWorker` koppelt de monitor aan de conversietaak.

### Stap 4: Start afbeeldingsconversie in een aparte thread

```java
Thread thread = new Thread(worker.ThreadProc());
try {
    thread.start();
    // Add a timeout to allow for potential interruption
    Thread.sleep(3000);
```

We starten de conversie op een achtergrond‑thread zodat de hoofdthread responsief blijft. De aanroep `Thread.sleep(3000)` simuleert een timeout‑scenario.

### Stap 5: Onderbreek het proces (Java Thread Interrupt Example)

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

Het aanroepen van `monitor.interrupt()` activeert de **how to interrupt monitor**‑logica. Na de onderbreking ruimen we eventueel gedeeltelijk geschreven PNG‑bestanden op.

## Veelvoorkomende problemen en oplossingen

| Probleem | Reden | Oplossing |
|----------|-------|-----------|
| Conversie stopt nooit | Monitor niet gekoppeld aan worker | Zorg ervoor dat `SaveImageWorker` dezelfde `InterruptMonitor`‑instantie ontvangt. |
| Uitvoerbestand blijft bestaan na onderbreking | Opruimcode niet uitgevoerd | Controleer of het `finally`‑blok wordt uitgevoerd en of het bestandspad correct is. |
| `OutOfMemoryError` bij grote PSB‑bestanden | Geen streaming‑opties gebruikt | Gebruik `PsdImage` met `LoadOptions` die geheugen‑efficiënt laden mogelijk maken. |

## Veelgestelde vragen

### Q1: Wat is een Interrupt Monitor in Aspose.PSD voor Java?

A1: De Interrupt Monitor stelt ontwikkelaars in staat **beeldconversieprocessen te beheren en te onderbreken**, waardoor je fijne controle hebt over langdurige taken.

### Q2: Hoe kan ik de Aspose.PSD bibliotheek voor Java verkrijgen?

A2: Je kunt de Aspose.PSD voor Java‑bibliotheek downloaden **[here](https://releases.aspose.com/psd/java/)**.

### Q3: Is er een gratis proefversie beschikbaar voor Aspose.PSD voor Java?

A3: Ja, je kunt een gratis proefversie van Aspose.PSD verkennen **[here](https://releases.aspose.com/)**.

### Q4: Waar kan ik ondersteuning vinden voor Aspose.PSD voor Java?

A4: Bezoek het Aspose.PSD voor Java‑ondersteuningsforum **[here](https://forum.aspose.com/c/psd/34)**.

### Q5: Hoe kan ik een licentie kopen voor Aspose.PSD voor Java?

A5: Je kunt een licentie voor Aspose.PSD voor Java aanschaffen **[here](https://purchase.aspose.com/buy)**.

**Laatst bijgewerkt:** 2025-12-25  
**Getest met:** Aspose.PSD 24.11 for Java  
**Auteur:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}