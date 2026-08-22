---
date: 2026-07-22
description: Scopri come estrarre i livelli PSD e convertire i livelli PSD in PNG
  usando Aspose.PSD per Java. Ideale per gli sviluppatori che necessitano di una manipolazione
  grafica robusta.
keywords:
- extract psd layers
- how to extract psd
- convert psd to png
lastmod: 2026-07-22
linktitle: Estrai i livelli PSD e aggiungi il supporto ai livelli per i file PSD con
  Aspose.PSD Java
og_description: Estrai i livelli PSD e convertili in PNG con Aspose.PSD per Java.
  Segui questa guida passo‑a‑passo per automatizzare l'estrazione dei livelli e la
  conversione delle immagini.
og_image_alt: Developer guide showing Java code to extract PSD layers and save as
  PNG using Aspose.PSD
og_title: Estrai i livelli PSD – Aggiungi il supporto ai livelli per i file PSD con
  Aspose.PSD Java
schemas:
- author: Aspose
  dateModified: '2026-07-22'
  description: Learn how to extract PSD layers and convert PSD layers to PNG using
    Aspose.PSD for Java. Ideal for developers needing robust graphics manipulation.
  headline: Extract PSD Layers and Add Layer Support for PSD Files using Aspose.PSD
    Java
  type: TechArticle
- description: Learn how to extract PSD layers and convert PSD layers to PNG using
    Aspose.PSD for Java. Ideal for developers needing robust graphics manipulation.
  name: Extract PSD Layers and Add Layer Support for PSD Files using Aspose.PSD Java
  steps:
  - name: '**Java Development Environment** – JDK installed. You can download it from
      the [Oracle website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).'
    text: '**Java Development Environment** – JDK installed. You can download it from
      the [Oracle website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).'
  - name: '**Aspose.PSD for Java** – Grab the latest library from the official download
      page [here](https://releases.aspose.com/psd/java/).'
    text: '**Aspose.PSD for Java** – Grab the latest library from the official download
      page [here](https://releases.aspose.com/psd/java/).'
  - name: '**Basic Java knowledge** – Familiarity with compiling and running Java
      programs.'
    text: '**Basic Java knowledge** – Familiarity with compiling and running Java
      programs.'
  - name: '**IDE** – IntelliJ IDEA, Eclipse, or any editor you prefer.'
    text: '**IDE** – IntelliJ IDEA, Eclipse, or any editor you prefer.'
  - name: '**A PSD file** – Use any PSD you have, or download a sample PSD for testing.'
    text: '**A PSD file** – Use any PSD you have, or download a sample PSD for testing.'
  type: HowTo
- questions:
  - answer: Aspose.PSD for Java is a library that allows you to manipulate PSD files
      without having Photoshop installed.
    question: What is Aspose.PSD for Java?
  - answer: Yes! While primarily for PSD files, Aspose offers libraries for a wide
      range of formats, including AI, PDF, and SVG.
    question: Can I use Aspose.PSD for other file formats?
  - answer: Absolutely! You can download a free trial version [here](https://releases.aspose.com/).
    question: Is a trial version available?
  - answer: Access the Aspose forum for PSD‑related questions [here](https://forum.aspose.com/c/psd/34).
    question: Where can I get support if I run into problems?
  - answer: Iterate over `image.getLayers()`, create a new `Bitmap` for each layer,
      and save it with its own `PngOptions`. This yields individual PNG files per
      layer.
    question: Can I convert each layer to a separate PNG?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- extract psd
- Aspose.PSD
- Java image processing
title: Estrai i livelli PSD e aggiungi il supporto ai livelli per i file PSD con Aspose.PSD
  Java
url: /it/java/advanced-psd-layer-features-effects/add-layer-support-psd-files/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Estrai i livelli PSD e aggiungi il supporto ai livelli per file PSD usando Aspose.PSD Java

## Introduzione
Lavorare con i file Photoshop Document (PSD) è una realtà quotidiana per designer grafici e sviluppatori, e **estrarre i livelli PSD** è spesso il primo passo per riutilizzare le risorse o automatizzare le pipeline di immagini. In questo tutorial imparerai a estrarre i singoli livelli da un PSD, abilitare il supporto completo ai livelli e **convertire i livelli PSD in PNG** usando Aspose.PSD per Java. Copriremo tutto, dall’impostazione dell’ambiente ai consigli di best‑practice, così potrai integrare questo flusso di lavoro in qualsiasi applicazione Java in pochi minuti.

## Risposte rapide
- **Cosa significa “estrarre i livelli PSD”?** Significa caricare un file PSD e accedere a ciascun livello individuale per manipolarlo o esportarlo.  
- **Quale libreria gestisce questo in Java?** Aspose.PSD per Java fornisce una gestione completa dei PSD senza la necessità di Photoshop.  
- **Posso convertire i livelli PSD in PNG in un unico passaggio?** Sì—bastano le opzioni corrette di caricamento e salvataggio PNG che preservano la trasparenza.  
- **È necessaria una licenza per l’uso in produzione?** È richiesta una licenza commerciale per la produzione; è disponibile una versione di prova gratuita per la valutazione.  
- **Quale versione di Java è richiesta?** JDK 8 o superiore (il tutorial usa JDK 11 come esempio).

## Come estrarre i livelli PSD usando Aspose.PSD per Java?
Carica il PSD, abilita gli effetti dei livelli e salva il risultato come PNG in poche righe di codice Java. Questo approccio diretto elimina la necessità di Photoshop sul server e funziona su qualsiasi piattaforma che supporti Java 8+.  
Inizi creando un oggetto `PsdLoadOptions` con `setLoadEffectsResource(true)` e `setUseDiskForLoadEffectsResource(true)`, quindi carichi il file con `PsdImage.load(path, options)`. Dopo il caricamento, puoi unire i livelli usando `image.save(outputPath, new PngOptions())` oppure iterare su `image.getLayers()` per esportare ogni livello singolarmente, garantendo che tutti gli effetti siano mantenuti riducendo al contempo l’utilizzo di memoria.

## Perché estrarre i livelli PSD e convertirli in PNG?
L’estrazione dei livelli consente di **riutilizzare le risorse**, **automatizzare la generazione di miniature** e **preservare la trasparenza** per grafiche pronte per il web. Aspose.PSD supporta **oltre 50 formati di input e output** e può elaborare file PSD di centinaia di pagine senza caricare l’intero file in memoria, grazie alla gestione delle risorse basata su disco.

## Prerequisiti
Prima di iniziare, assicurati di avere quanto segue:

1. **Ambiente di sviluppo Java** – JDK installato. Puoi scaricarlo dal [sito Oracle](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).  
2. **Aspose.PSD per Java** – Scarica l’ultima libreria dalla pagina ufficiale di download [qui](https://releases.aspose.com/psd/java/).  
3. **Conoscenze di base di Java** – Familiarità con la compilazione ed esecuzione di programmi Java.  
4. **IDE** – IntelliJ IDEA, Eclipse o qualsiasi editor tu preferisca.  
5. **Un file PSD** – Usa qualsiasi PSD a tua disposizione, o scarica un PSD di esempio per i test.

Una volta pronti questi elementi, sei pronto per iniziare a estrarre i livelli PSD.

## Importa i pacchetti
Le classi `PsdImage`, `PsdLoadOptions` e `PngOptions` sono il cuore del flusso di lavoro.  

`PsdImage` è l’oggetto di livello superiore di Aspose.PSD che rappresenta un singolo file PSD in memoria.  

`PsdLoadOptions` ti permette di controllare come vengono caricati le risorse, come gli effetti dei livelli.  

`PngOptions` definisce il formato di output e la gestione della trasparenza per il file PNG.

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
import com.aspose.psd.imageoptions.PngOptions;
```

## Passo 1: Definisci le tue directory
Imposta i percorsi per il PSD di origine e per il PNG di output. Regola `dataDir` in modo che punti alla cartella dove risiedono i tuoi file.

```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "layers.psd";
String output = dataDir + "layers.png";
```

- `dataDir` – Sostituisci `"Your Document Directory"` con il percorso reale della tua cartella.  
- `sourceFileName` – Percorso completo del PSD da elaborare.  
- `output` – Percorso di destinazione per il PNG che conterrà i livelli estratti.

## Passo 2: Configura le opzioni di caricamento
Configurare `PsdLoadOptions` garantisce che tutti gli effetti e le risorse dei livelli vengano caricati correttamente, fondamentale quando **estrai i livelli PSD**.

```java
PsdLoadOptions imageLoadOptions = new PsdLoadOptions();
imageLoadOptions.setLoadEffectsResource(true);
imageLoadOptions.setUseDiskForLoadEffectsResource(true);
```

- `setLoadEffectsResource(true)` – Carica effetti aggiuntivi (come le ombre) associati ai livelli.  
- `setUseDiskForLoadEffectsResource(true)` – Sposta le risorse pesanti su disco, riducendo la pressione sulla memoria.

## Passo 3: Carica il file PSD
Ora carichiamo il PSD in un oggetto `PsdImage` usando le opzioni definite sopra.

```java
PsdImage image = (PsdImage) Image.load(sourceFileName, imageLoadOptions);
```

A questo punto, `image` contiene tutti i livelli, le maschere e gli effetti, pronto per l’estrazione.

## Passo 4: Configura le opzioni di salvataggio
Imposta come verrà salvato il PNG. L’utilizzo di `TruecolorWithAlpha` preserva la trasparenza dei livelli originali.

```java
PngOptions saveOptions = new PngOptions();
saveOptions.setColorType(PngColorType.TruecolorWithAlpha);
```

## Passo 5: Salva l'immagine (Converti i livelli PSD in PNG)
Esporta il PSD caricato (con tutti i suoi livelli) in un unico file PNG. Questo passaggio **converte i livelli PSD in PNG** in un’unica operazione.

```java
image.save(output, saveOptions);
```

Se ti serve ogni livello come PNG separato, puoi iterare su `image.getLayers()`—ma per molti casi d’uso un PNG unificato è sufficiente.

## Passo 6: Concludi
Aggiungi un messaggio di console amichevole così saprai che il processo è terminato con successo.

```java
System.out.println("PSD Layers have been successfully converted to PNG!");
```

## Problemi comuni e consigli
- **Errori Out‑of‑Memory:** Se elabori PSD molto grandi, mantieni abilitato `setUseDiskForLoadEffectsResource(true)` per spostare i dati temporanei su disco.  
- **Effetti mancanti:** Assicurati che `setLoadEffectsResource(true)` sia impostato; altrimenti alcuni effetti dei livelli potrebbero essere ignorati.  
- **Problemi di percorso:** Usa `Paths.get(...)` da `java.nio.file` per gestire i percorsi in modo indipendente dalla piattaforma.

## Domande frequenti

**D: Cos’è Aspose.PSD per Java?**  
R: Aspose.PSD per Java è una libreria che consente di manipolare file PSD senza avere Photoshop installato.

**D: Posso usare Aspose.PSD per altri formati di file?**  
R: Sì! Sebbene sia principalmente per i file PSD, Aspose offre librerie per una vasta gamma di formati, tra cui AI, PDF e SVG.

**D: È disponibile una versione di prova?**  
R: Assolutamente! Puoi scaricare una versione di prova gratuita [qui](https://releases.aspose.com/).

**D: Dove posso ottenere supporto se incontro problemi?**  
R: Accedi al forum Aspose per domande relative ai PSD [qui](https://forum.aspose.com/c/psd/34).

**D: Posso convertire ogni livello in un PNG separato?**  
R: Itera su `image.getLayers()`, crea un nuovo `Bitmap` per ciascun livello e salvalo con le proprie `PngOptions`. Otterrai file PNG individuali per ogni livello.

## Conclusione
Ora sai come **estrarre i livelli PSD**, abilitare il supporto completo ai livelli e **convertire i livelli PSD in PNG** usando Aspose.PSD per Java. Che tu stia costruendo una pipeline automatizzata di asset o aggiungendo capacità grafiche a un’app desktop, questo approccio ti offre un controllo dettagliato sui file Photoshop senza la necessità di Photoshop stesso. Esplora ulteriormente applicando filtri, unendo i livelli programmaticamente o esportando ogni livello singolarmente per adattarlo al tuo flusso di lavoro.

---

**Ultimo aggiornamento:** 2026-07-22  
**Testato con:** Aspose.PSD per Java 24.11 (ultima versione al momento della stesura)  
**Autore:** Aspose

## Tutorial correlati

- [Export PSD to PNG & Add a New Regular Layer using Aspose.PSD for Java](/psd/java/advanced-image-effects/add-new-regular-layer/)
- [Export PSD to PNG with Layer Mask Support in Java](/psd/java/advanced-psd-layer-features-effects/support-layer-mask-psd-files/)
- [Convert PSD to Image in Java – Apply Adjustment Layers with Aspose.PSD](/psd/java/advanced-psd-layer-features-effects/apply-adjustment-layers-psd-files/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< blocks/products/products-backtop-button >}}
{{< /blocks/products/pf/main-wrap-class >}}