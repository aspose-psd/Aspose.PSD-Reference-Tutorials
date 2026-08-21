---
date: 2026-06-18
description: Impara come modificare il colore dell'ombra in Java e personalizzare
  gli effetti ombra usando Aspose.PSD per Java. Segui questo tutorial passo‑passo
  sugli effetti ombra.
keywords:
- change shadow color java
- Aspose.PSD shadow effect
- Java PSD manipulation
linktitle: Supporto effetto ombra
schemas:
- author: Aspose
  dateModified: '2026-06-18'
  description: Learn how to change shadow color java and customize shadow effects
    using Asprose.PSD for Java. Follow this step‑by‑step shadow effect tutorial.
  headline: Change Shadow Color Java with Aspose.PSD for Java
  type: TechArticle
- description: Learn how to change shadow color java and customize shadow effects
    using Asprose.PSD for Java. Follow this step‑by‑step shadow effect tutorial.
  name: Change Shadow Color Java with Aspose.PSD for Java
  steps:
  - name: Load the PSD Image
    text: 'First, load the source PSD while enabling the loading of effect resources:'
  - name: Retrieve the Existing Drop Shadow Effect
    text: 'Locate the shadow effect on the desired layer (in this example, the second
      layer):'
  - name: Verify the Default Settings (Optional)
    text: 'Running these assertions helps you understand the original values before
      you modify them:'
  - name: '**Change Shadow Color** and Customize Other Properties'
    text: Now we actually **change shadow color** to green, adjust opacity, distance,
      size, and other attributes. This demonstrates the **customize shadow effect**
      capabilities of Aspose.PSD. The `setOpacity(byte)` method sets the shadow's
      opacity level (0‑255).
  - name: Save the Modified Image
    text: 'Finally, write the updated PSD back to disk using the `save` method of
      `PsdImage`:'
  type: HowTo
- questions:
  - answer: Absolutely! Aspose.PSD for Java is a powerful library designed for professional
      graphic design tasks.
    question: Is Aspose.PSD for Java suitable for professional graphic design projects?
  - answer: Yes, Aspose.PSD for Java is a commercial product. You can purchase it
      [here](https://purchase.aspose.com/buy).
    question: Can I use Aspose.PSD for Java in commercial applications?
  - answer: Yes, you can explore a free trial version [here](https://releases.aspose.com/).
    question: Is there a free trial available?
  - answer: Refer to the comprehensive documentation [here](https://reference.aspose.com/psd/java/).
    question: Where can I find detailed documentation?
  - answer: Join the community forum [here](https://forum.aspose.com/c/psd/34) for
      any support queries.
    question: How can I get support for Aspose.PSD for Java?
  type: FAQPage
second_title: Aspose.PSD Java API
title: Modifica il colore dell'ombra in Java con Aspose.PSD per Java
url: /it/java/basic-image-operations/support-shadow-effect/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Cambia il colore dell'ombra Java con Aspose.PSD per Java

## Introduzione

Aggiungere profondità alle tue grafiche spesso significa **changing shadow color** per adattarsi all'umore del design. Con Aspose.PSD per Java puoi facilmente aggiungere o modificare effetti di ombra proiettata, controllare l'opacità e perfezionare altri parametri — tutto dal codice Java. In questo **shadow effect tutorial** vedremo come caricare un PSD, leggere l'ombra esistente, personalizzare il suo colore, opacità, distanza e infine salvare il file aggiornato. Questa guida mostra esattamente come **change shadow color java** in modo riproducibile.

## Risposte rapide
- **What does “change shadow color” mean?** Aggiorna la proprietà colore di un DropShadowEffect applicato a un livello PSD.  
- **Which library supports this?** Aspose.PSD per Java fornisce pieno supporto per gli effetti di ombra.  
- **Do I need a license?** Una versione di prova funziona per lo sviluppo; è necessaria una licenza commerciale per la produzione.  
- **Can I set shadow opacity?** Sì – usa `setOpacity(byte)` per definire la trasparenza (0‑255).  
- **Is the code compatible with Java 8+?** Assolutamente, l'API è destinata a Java 8 e versioni successive.

## Cos'è “change shadow color” nei file PSD?

Modificare il colore dell'ombra cambia la tonalità visiva dell'ombra proiettata che appare dietro a un livello. Questa regolazione consente ai designer di simulare diverse condizioni di illuminazione, allineare le ombre con le palette di colori del brand e aggiungere un tocco artistico alle composizioni. Alterando la tonalità, è possibile far apparire le ombre più calde, più fredde o farle corrispondere esattamente a uno schema di colori specifico, migliorando l'impatto visivo complessivo.

## Perché usare Aspose.PSD per Java per personalizzare gli effetti di ombra?

Aspose.PSD per Java conserva **100+ formati immagine** e può elaborare file PSD fino a **2 GB** senza caricare l'intero documento in memoria, offrendo prestazioni di livello enterprise. La libreria ti dà il pieno controllo su ogni attributo dell'ombra — colore, opacità, distanza, angolo, diffusione e rumore — senza la necessità di avere Photoshop installato. Funziona su JVM Windows, Linux e macOS, rendendola la scelta più affidabile per pipeline grafiche automatizzate.

## Prerequisiti

- Conoscenza di base della programmazione Java.  
- Aspose.PSD per Java installato. Puoi scaricarlo [qui](https://releases.aspose.com/psd/java/).  

## Importa i pacchetti

Prima di iniziare, importa le classi richieste così da poter lavorare con immagini ed effetti di ombra:

La classe `Color` rappresenta un valore di colore utilizzato in tutta l'API.  
La classe `Image` è il tipo base per tutti gli oggetti immagine.  
La classe `PsdImage` fornisce funzionalità specifiche per i file PSD.  
La classe `PsdLoadOptions` consente di specificare opzioni per il caricamento dei file PSD, come l'abilitazione delle risorse degli effetti.  
La classe `DropShadowEffect` rappresenta un filtro di ombra proiettata applicato a un livello PSD e ti dà accesso a tutte le sue proprietà regolabili.

```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;


import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.layereffects.DropShadowEffect;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
```

## Guida passo‑passo

### Passo 1: Carica l'immagine PSD

Prima, carica il PSD di origine abilitando il caricamento delle risorse degli effetti:

```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "Shadow.psd";
String psdPathAfterChange = dataDir + "ShadowChanged.psd";

PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);

PsdImage im = (PsdImage)Image.load(sourceFileName, loadOptions);
```

### Passo 2: Recupera l'effetto di ombra proiettata esistente

Individua l'effetto di ombra sul livello desiderato (in questo esempio, il secondo livello):

```java
DropShadowEffect shadowEffect = (DropShadowEffect)(im.getLayers()[1].getBlendingOptions().getEffects()[0]);
```

### Passo 3: Verifica le impostazioni predefinite (Opzionale)

Eseguire queste asserzioni ti aiuta a comprendere i valori originali prima di modificarli:

```java
Assert.areEqual(Color.getBlack(), shadowEffect.getColor());
Assert.areEqual(255, shadowEffect.getOpacity());
Assert.areEqual(3, shadowEffect.getDistance());
Assert.areEqual(7, shadowEffect.getSize());
Assert.areEqual(true, shadowEffect.getUseGlobalLight());
Assert.areEqual(90, shadowEffect.getAngle());
Assert.areEqual(0, shadowEffect.getSpread());
Assert.areEqual(0, shadowEffect.getNoise());
```

### Passo 4: **Change Shadow Color** e personalizza altre proprietà

Adesso effettuiamo realmente **change shadow color** a verde, regolare l'opacità, la distanza, la dimensione e altre proprietà. Questo dimostra le capacità di **customize shadow effect** di Aspose.PSD. Il metodo `setOpacity(byte)` imposta il livello di opacità dell'ombra (0‑255).  

```java
shadowEffect.setColor(Color.getGreen());          // change shadow color
shadowEffect.setOpacity((byte)128);               // set shadow opacity (50% transparent)
shadowEffect.setDistance(11);                     // move shadow farther from the object
shadowEffect.setUseGlobalLight(false);            // use local lighting
shadowEffect.setSize(9);                          // adjust blur radius
shadowEffect.setAngle(45);                        // rotate light source
shadowEffect.setSpread(3);                        // increase spread
shadowEffect.setNoise(50);                        // add texture noise
```

### Passo 5: Salva l'immagine modificata

Infine, scrivi il PSD aggiornato su disco usando il metodo `save` di `PsdImage`:

```java
im.save(psdPathAfterChange);
```

## Problemi comuni e consigli

- **NullPointerException when retrieving effects** – assicurati che `setLoadEffectsResource(true)` sia chiamato; altrimenti gli effetti non vengono caricati.  
- **Color not changing** – verifica di modificare l'indice di livello corretto (`im.getLayers()[1]` in questo esempio).  
- **Opacity looks unchanged** – ricorda che l'opacità è un byte (0‑255). È necessario il cast a `(byte)`.

## Conclusione

Seguendo questi passaggi puoi **change shadow color**, **set shadow opacity** e personalizzare completamente i parametri di **customize shadow effect** in qualsiasi file PSD usando Aspose.PSD per Java. Questo ti consente di creare grafiche più ricche programmaticamente senza lavoro manuale su Photoshop, perfetto per pipeline di design automatizzate e elaborazioni batch.

## Domande frequenti

**Q: Aspose.PSD per Java è adatto per progetti professionali di design grafico?**  
A: Assolutamente! Aspose.PSD per Java è una libreria potente progettata per compiti di design grafico professionale.

**Q: Posso usare Aspose.PSD per Java in applicazioni commerciali?**  
A: Sì, Aspose.PSD per Java è un prodotto commerciale. Puoi acquistarlo [qui](https://purchase.aspose.com/buy).

**Q: È disponibile una versione di prova gratuita?**  
A: Sì, puoi provare una versione di prova gratuita [qui](https://releases.aspose.com/).

**Q: Dove posso trovare la documentazione dettagliata?**  
A: Consulta la documentazione completa [qui](https://reference.aspose.com/psd/java/).

**Q: Come posso ottenere supporto per Aspose.PSD per Java?**  
A: Unisciti al forum della community [qui](https://forum.aspose.com/c/psd/34) per qualsiasi domanda di supporto.

---

**Ultimo aggiornamento:** 2026-06-18  
**Testato con:** Aspose.PSD per Java 24.10  
**Autore:** Aspose  

{{< blocks/products/products-backtop-button >}}

## Tutorial correlati

- [Manipolazione immagini Java - Aggiungi effetti a runtime con Aspose.PSD per Java](/psd/java/advanced-techniques/add-effects-runtime/)
- [Salva PSD come PNG e applica Rendering Drop Shadow in Aspose.PSD per Java](/psd/java/advanced-image-manipulation/rendering-drop-shadow/)
- [Sfoca immagine Java con Aspose.PSD – Aggiungi effetto blur](/psd/java/advanced-techniques/blur-image/)

{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}