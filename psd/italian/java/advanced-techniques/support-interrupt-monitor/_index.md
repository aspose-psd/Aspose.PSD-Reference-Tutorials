---
date: 2026-06-08
description: Scopri come salvare PSD come PNG utilizzando Aspose.PSD for Java e interrompere
  la conversione quando necessario. Gestisci il flusso di lavoro delle immagini in
  modo efficiente.
keywords:
- save psd as png
- how to interrupt conversion
- psd to png conversion
- manage image workflow
linktitle: Supporto per Interrupt Monitor
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
title: Come salvare PSD come PNG con Interrupt Monitor in Aspose.PSD for Java
url: /it/java/advanced-techniques/support-interrupt-monitor/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Salva PSD come PNG con Interrupt Monitor in Aspose.PSD per Java

## Introduzione

Se hai bisogno di **salvare PSD come PNG** mantenendo il pieno controllo sulle conversioni a lunga durata, l'Interrupt Monitor di Aspose.PSD per Java ti offre esattamente questo. In questo tutorial vedremo come configurare il monitor, convertire un file PSD in PNG e interrompere in modo sicuro l'operazione quando necessario. Vedrai anche come questo si inserisce in un tipico flusso di lavoro di elaborazione immagini e perché è indispensabile per applicazioni robuste.

## Risposte Rapide
- **Posso interrompere una conversione da PSD a PNG?** Sì, usa `InterruptMonitor` per fermare il processo su richiesta.  
- **Quale metodo salva un PSD come PNG?** Chiama `save(outputPath, new PngOptions())`.  
- **È necessaria una licenza per la produzione?** È richiesta una licenza commerciale; è disponibile una prova gratuita.  
- **Quale versione di Java è supportata?** Java 8 e successive sono pienamente supportate.  
- **La libreria è thread‑safe?** Le conversioni possono essere eseguite in thread separati; il monitor gestisce le interruzioni in modo sicuro.

## Prerequisiti

Prima di immergerti nelle complessità dell'uso dell'Interrupt Monitor, assicurati di avere i seguenti prerequisiti in ordine:

- **Ambiente di sviluppo Java:** Configura un ambiente di sviluppo Java sul tuo sistema.  
- **Libreria Aspose.PSD:** Ottieni la libreria Aspose.PSD per Java. Puoi scaricarla [qui](https://releases.aspose.com/psd/java/). Puoi anche visitare il sito principale di Aspose [qui](https://releases.aspose.com/).  
- **Directory dei documenti:** Disporre di una directory designata per i tuoi documenti PSD.

## Importa Pacchetti

Inizia importando i pacchetti necessari nel tuo progetto Java. Questo garantisce l'accesso alle funzionalità di Aspose.PSD.

```java
import com.aspose.psd.ImageOptionsBase;

import static com.aspose.psd.examples.Utils.Utils.getDateTime;
import com.aspose.psd.imageoptions.PngOptions;
import com.aspose.psd.multithreading.InterruptMonitor;
import com.aspose.psd.system.Threading.ThreadStart;
import java.io.File;
```

Ora, analizziamo il codice di esempio in una guida passo‑passo per incorporare l'Interrupt Monitor nel tuo progetto Aspose.PSD per Java.

## Come salvare PSD come PNG usando l'Interrupt Monitor?

`PsdImage` rappresenta un documento PSD caricato in memoria.  
`SaveImageWorker` esegue la conversione dell'immagine in un thread separato.  

Carica il tuo file PSD con `new PsdImage("source.psd")`, collega un `InterruptMonitor` al `SaveImageWorker` e chiama `save("output.png", new PngOptions())`. Il monitor osserva le richieste di cancellazione e interrompe la conversione in modo pulito, restituendo il controllo alla tua applicazione entro pochi millisecondi.

### Passo 1: Imposta la tua directory dei documenti

```java
String dataDir = "Your Document Directory";
```

Assicurati di sostituire “Your Document Directory” con il percorso reale in cui sono archiviati i tuoi documenti PSD.

### Passo 2: Definisci le opzioni immagine e il percorso di output

```java
ImageOptionsBase saveOptions = new PngOptions();
String source = dataDir + "big2.psb";
String output = dataDir + "big_out.png";
```

Specifica le opzioni immagine, il file PSD di origine e il percorso di output desiderato per l'immagine convertita.

### Passo 3: Inizializza Interrupt Monitor e SaveImageWorker

La classe `InterruptMonitor` osserva una conversione in corso e può interromperla quando viene chiamato `requestInterrupt()`.

```java
InterruptMonitor monitor = new InterruptMonitor();
SaveImageWorker worker = new SaveImageWorker(source, output, saveOptions, monitor);
```

### Passo 4: Avvia il thread di conversione immagine

```java
Thread thread = new Thread(worker.ThreadProc());
try {
    thread.start();
    // Add a timeout to allow for potential interruption
    Thread.sleep(3000);
```

Avvia un nuovo thread per il processo di conversione dell'immagine e introduce un periodo di timeout per anticipare l'interruzione.

### Passo 5: Interrompi il processo

Chiamare `monitor.requestInterrupt()` segnala al monitor di abortire la conversione in corso.

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

Interrompi il processo di conversione dell'immagine usando l'`InterruptMonitor` e attendi che l'interruzione sia completata. Infine, pulisci eliminando il file di output.

## Perché usare l'Interrupt Monitor per la conversione da PSD a PNG?

Aspose.PSD supporta **oltre 30 formati di output**, tra cui PNG, JPEG, BMP e TIFF, e può elaborare file fino a **500 MB** senza caricare l'intero documento in memoria. Aggiungendo un interrupt monitor riduci lo spreco di CPU e migliori la reattività nei flussi di lavoro batch, soprattutto quando una conversione supera i limiti di tempo previsti.

## Problemi comuni e soluzioni

- **La conversione si blocca indefinitamente:** Assicurati che il monitor sia collegato **prima** di chiamare `save`.  
- **Il file di output è corrotto dopo l'interruzione:** Il monitor abortisce in modo pulito; tuttavia, verifica sempre se il file esiste prima di usarlo.  
- **Problemi di thread‑safety:** Esegui ogni conversione nel proprio thread; il monitor influisce solo sul worker a cui è associato.

## Domande frequenti

**Q1: Cos'è un Interrupt Monitor in Aspose.PSD per Java?**  
A: L'Interrupt Monitor consente agli sviluppatori di mettere in pausa o annullare conversioni di immagini a lunga durata, fornendo un controllo in tempo reale sull'uso delle risorse.

**Q2: Come posso ottenere la libreria Aspose.PSD per Java?**  
A: Puoi scaricare la libreria Aspose.PSD per Java [qui](https://releases.aspose.com/psd/java/).

**Q3: È disponibile una prova gratuita per Aspose.PSD per Java?**  
A: Sì, puoi provare una versione di prova gratuita di Aspose.PSD [qui](https://releases.aspose.com/).

**Q4: Dove posso trovare supporto per Aspose.PSD per Java?**  
A: Visita il forum di supporto di Aspose.PSD per Java [qui](https://forum.aspose.com/c/psd/34).

**Q5: Come posso acquistare una licenza per Aspose.PSD per Java?**  
A: Puoi acquistare una licenza per Aspose.PSD per Java [qui](https://purchase.aspose.com/buy).

**Q6: Posso convertire più file PSD in PNG in parallelo?**  
A: Sì, avvia un thread separato per ogni file e collega un `InterruptMonitor` individuale a ciascun worker di conversione.

**Q7: La libreria gestisce i profili colore durante la conversione da PSD a PNG?**  
A: Assolutamente; Aspose.PSD preserva i profili ICC incorporati e li applica automaticamente al PNG di output.

---

**Ultimo aggiornamento:** 2026-06-08  
**Testato con:** Aspose.PSD 23.12 for Java  
**Autore:** Aspose  

{{< blocks/products/products-backtop-button >}}

## Tutorial correlati

- [Salva PSD come PNG e applica Rendering Drop Shadow in Aspose.PSD per Java](/psd/java/advanced-image-manipulation/rendering-drop-shadow/)
- [Esporta PSD in PNG e aggiungi un nuovo livello regolare usando Aspose.PSD per Java](/psd/java/advanced-image-effects/add-new-regular-layer/)
- [Supporto per Interrupt Monitor nei file PSD - Java](/psd/java/psd-layer-management-effects/support-interrupt-monitor-psd-files/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}