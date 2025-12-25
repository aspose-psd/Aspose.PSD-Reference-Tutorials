---
date: 2025-12-25
description: Scopri come convertire PSD in PNG usando Aspose.PSD per Java con supporto
  al monitor di interruzione, includendo un esempio di interruzione di thread Java
  e consigli per salvare PSD come PNG.
linktitle: Support for Interrupt Monitor
second_title: Aspose.PSD Java API
title: Come convertire PSD in PNG con supporto per il monitor di interruzione in Aspose.PSD
  per Java
url: /it/java/advanced-techniques/support-interrupt-monitor/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Converti PSD in PNG con Interrupt Monitor in Aspose.PSD per Java

## Introduzione

Se hai bisogno di **convertire PSD in PNG** mantenendo il pieno controllo sulle conversioni di immagini a lungo termine, l'Interrupt Monitor di Aspose.PSD per Java è lo strumento che stavi cercando. In questo tutorial vedremo un esempio reale di **java thread interrupt example** che ti permette di interrompere una conversione a metà processo, offrendoti la flessibilità di gestire le risorse, applicare timeout o rispondere alle cancellazioni dell'utente.

## Risposte rapide
- **Che cosa fa l'Interrupt Monitor?** Consente di segnalare a una conversione di immagine in corso di fermarsi in modo sicuro.  
- **Posso convertire PSD in PNG con esso?** Sì – il monitor funziona con qualsiasi operazione di salvataggio, incluso PNG.  
- **È necessario un thread separato?** Tipicamente esegui la conversione in un thread separato così da poterla interrompere.  
- **Quale versione di Aspose.PSD è necessaria?** Qualsiasi versione recente che includa `com.aspose.psd.multithreading.InterruptMonitor`.  
- **È necessaria una licenza per la produzione?** Sì, è richiesta una licenza valida di Aspose.PSD per l'uso non‑trial.

## Cos'è “convertire PSD in PNG” con un Interrupt Monitor?

Convertire un grande documento Photoshop (PSD/PSB) in un'immagine PNG può richiedere molte risorse CPU. Collegando un **Interrupt Monitor** al worker di conversione, ottieni la possibilità di fermare il processo programmaticamente—perfetto per servizi web, lavori batch o applicazioni UI in cui gli utenti possono annullare le operazioni.

## Perché usare l'Interrupt Monitor?

- **UI reattiva:** Impedisce all'applicazione di bloccarsi mentre viene elaborato un file di grandi dimensioni.  
- **Gestione delle risorse:** Interrompe le conversioni che superano i limiti di tempo o di memoria.  
- **Gestione degli errori:** Pulisce elegantemente i file di output parziali quando si verifica un'interruzione.

## Prerequisiti

- Ambiente di sviluppo Java (JDK 8 o superiore).  
- Libreria Aspose.PSD per Java – scaricala **[qui](https://releases.aspose.com/psd/java/)**.  
- Una cartella che contiene i file PSD/PSB con cui vuoi lavorare.

## Importa pacchetti

Inizia importando le classi necessarie. Questo ti dà accesso alle opzioni immagine, all'interrupt monitor e alle utility di threading.

```java
import com.aspose.psd.ImageOptionsBase;

import static com.aspose.psd.examples.Utils.Utils.getDateTime;
import com.aspose.psd.imageoptions.PngOptions;
import com.aspose.psd.multithreading.InterruptMonitor;
import com.aspose.psd.system.Threading.ThreadStart;
import java.io.File;
```

## Guida passo‑passo

### Passo 1: Imposta la directory dei documenti

Sostituisci `"Your Document Directory"` con il percorso assoluto dove risiedono i tuoi file PSD.

```java
String dataDir = "Your Document Directory";
```

### Passo 2: Definisci le opzioni immagine e il percorso di output

Qui **salviamo PSD come PNG** usando `PngOptions`. Regola i nomi dei file secondo necessità.

```java
ImageOptionsBase saveOptions = new PngOptions();
String source = dataDir + "big2.psb";
String output = dataDir + "big_out.png";
```

### Passo 3: Inizializza Interrupt Monitor e SaveImageWorker

L'istanza `InterruptMonitor` sarà usata più tardi per fermare la conversione. `SaveImageWorker` collega il monitor al compito di conversione.

```java
InterruptMonitor monitor = new InterruptMonitor();
SaveImageWorker worker = new SaveImageWorker(source, output, saveOptions, monitor);
```

### Passo 4: Avvia la conversione immagine in un thread separato

Avviamo la conversione su un thread in background così il thread principale può rimanere reattivo. La chiamata `Thread.sleep(3000)` simula uno scenario di timeout.

```java
Thread thread = new Thread(worker.ThreadProc());
try {
    thread.start();
    // Add a timeout to allow for potential interruption
    Thread.sleep(3000);
```

### Passo 5: Interrompi il processo (Esempio Java Thread Interrupt)

Chiamare `monitor.interrupt()` attiva la logica di **how to interrupt monitor**. Dopo l'interruzione puliamo eventuali file PNG scritti parzialmente.

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

## Problemi comuni e soluzioni

| Problema | Motivo | Soluzione |
|----------|--------|-----------|
| La conversione non si ferma mai | Monitor non collegato al worker | Assicurati che `SaveImageWorker` riceva la stessa istanza di `InterruptMonitor`. |
| Il file di output rimane dopo l'interruzione | Il codice di pulizia non è stato eseguito | Verifica che il blocco `finally` venga eseguito e che il percorso del file sia corretto. |
| `OutOfMemoryError` on large PSB files | Non si stanno usando le opzioni di streaming | Usa `PsdImage` con `LoadOptions` che abilitano il caricamento a basso consumo di memoria. |

## Domande frequenti

### Q1: Cos'è un Interrupt Monitor in Aspose.PSD per Java?

A1: L'Interrupt Monitor consente agli sviluppatori di **gestire e interrompere i processi di conversione delle immagini**, fornendo un controllo dettagliato sui compiti a lungo termine.

### Q2: Come posso ottenere la libreria Aspose.PSD per Java?

A2: Puoi scaricare la libreria Aspose.PSD per Java **[qui](https://releases.aspose.com/psd/java/)**.

### Q3: È disponibile una versione di prova gratuita per Aspose.PSD per Java?

A3: Sì, puoi provare gratuitamente Aspose.PSD **[qui](https://releases.aspose.com/)**.

### Q4: Dove posso trovare supporto per Aspose.PSD per Java?

A4: Visita il forum di supporto di Aspose.PSD per Java **[qui](https://forum.aspose.com/c/psd/34)**.

### Q5: Come posso acquistare una licenza per Aspose.PSD per Java?

A5: Puoi acquistare una licenza per Aspose.PSD per Java **[qui](https://purchase.aspose.com/buy)**.

---

**Ultimo aggiornamento:** 2025-12-25  
**Testato con:** Aspose.PSD 24.11 for Java  
**Autore:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}