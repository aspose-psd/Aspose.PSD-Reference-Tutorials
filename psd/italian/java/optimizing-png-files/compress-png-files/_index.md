---
date: 2026-03-15
description: Scopri come comprimere i file PNG usando Aspose.PSD per Java, una guida
  passo‑passo su come comprimere PNG, ottimizzare le dimensioni dei PNG e convertire
  PSD in PNG in modo efficiente.
linktitle: Compress PNG Files using Aspose.PSD for Java
second_title: Aspose.PSD Java API
title: Come comprimere i file PNG usando Aspose.PSD per Java
url: /it/java/optimizing-png-files/compress-png-files/
weight: 12
---

 with bold formatting: keep **.

Also keep code placeholders.

Now produce final answer.{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Come comprimere file PNG usando Aspose.PSD per Java

## Introduzione

Quando si tratta di gestire le immagini nello sviluppo software, imparare **come comprimere PNG** in modo efficiente può migliorare drasticamente i tempi di caricamento delle pagine e ridurre l'uso della larghezza di banda. Aspose.PSD per Java è una libreria potente che consente di lavorare con file Photoshop (PSD) ed esportarli in una varietà di formati, incluso PNG. Che tu abbia bisogno di **ottimizzare le dimensioni PNG**, convertire PSD in PNG per una galleria web, o perfezionare **i livelli di compressione PNG**, questo tutorial ti guida attraverso un esempio completo, pronto per la produzione.

## Risposte Rapide
- **Cosa significa “come comprimere PNG”?** Si riferisce alla riduzione della dimensione di un'immagine PNG mantenendo la qualità visiva, tipicamente regolando i parametri di compressione.  
- **Quale libreria è la migliore per la compressione PNG in Java?** Aspose.PSD per Java offre opzioni PNG integrate e supporta un'intera gamma di livelli di compressione (0‑9).  
- **È necessaria una licenza?** Una prova gratuita funziona per la valutazione; è richiesta una licenza commerciale per l'uso in produzione.  
- **Posso automatizzare più livelli di compressione?** Sì—ciclare attraverso la proprietà `setCompressionLevel` ti permette di generare PNG a ogni livello.  
- **Questo approccio è adatto a file PSD di grandi dimensioni?** Assolutamente; Aspose.PSD trasmette i dati in modo efficiente, rendendolo sicuro per risorse ad alta risoluzione.

## Cos'è la compressione PNG?

PNG utilizza una compressione senza perdita, il che significa che la qualità dell'immagine rimane intatta mentre la dimensione del file viene ridotta. Regolando il **livello di compressione PNG** (0 = nessuna compressione, 9 = compressione massima) controlli quanto aggressivamente i dati vengono impacchettati. Livelli più alti richiedono un po' più di tempo di elaborazione ma producono file più piccoli—perfetti per l'ottimizzazione web.

## Perché usare Aspose.PSD per Java per comprimere PNG?

- **Supporto completo PSD** – Apri, modifica ed esporta i livelli PSD senza perdere informazioni.  
- **Controllo granulare** – Imposta esattamente i livelli di compressione PNG, il tipo di colore e la profondità di bit.  
- **Cross‑platform** – Funziona su qualsiasi ambiente compatibile con Java, da applicazioni desktop a servizi cloud.  
- **Prestazioni** – Codice nativo ottimizzato garantisce una rapida elaborazione anche per immagini di grandi dimensioni.  

## Prerequisiti

Prima di immergerci nel codice, verifica di avere quanto segue:

1. **Java JDK** – Scarica l'ultima JDK dal [sito web di Oracle](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).  
2. **Libreria Aspose.PSD per Java** – Ottieni il JAR più recente dalla pagina ufficiale di download [qui](https://releases.aspose.com/psd/java/).  
3. **IDE o editor di codice** – IntelliJ IDEA, Eclipse o VS Code funzioneranno perfettamente.  
4. **Conoscenze di base di Java** – Familiarità con la gestione delle eccezioni e I/O di file accelera la curva di apprendimento.  
5. **File PSD di esempio** – Posiziona un file PSD (ad es., `sample.psd`) in una cartella che utilizzerai come directory del documento.

Avere questi elementi pronti ti permetterà di concentrarti sui passaggi di **ottimizzazione immagini java** anziché sui problemi di configurazione.

## Importa Pacchetti

Le seguenti istruzioni `import` ti danno accesso alle classi core di Aspose.PSD e alle opzioni PNG:

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.PngOptions;
```

Queste classi ti consentono di caricare un PSD, configurare le impostazioni PNG e salvare il risultato.

## Passo 1: Configura il tuo progetto

Crea un nuovo progetto Java (ad es., `PsdImageCompressor`) e aggiungi il JAR di Aspose.PSD al percorso di compilazione. Questo garantisce che il compilatore possa trovare le classi referenziate sopra.

## Passo 2: Definisci la directory del documento

Indica al programma dove trovare il file PSD di origine e dove scrivere i PNG compressi:

```java
String dataDir = "Your Document Directory"; // Replace with actual path
```

Sostituisci `"Your Document Directory"` con il percorso assoluto o relativo che contiene `sample.psd`. Mantenere il percorso configurabile rende più semplice **convertire PSD in PNG** in ambienti diversi.

## Passo 3: Carica l'immagine PSD

Carica il file PSD in memoria. Questo passaggio è analogo all'aprire un libro prima di iniziare a leggerlo:

```java
PsdImage psdImage = (PsdImage)Image.load(dataDir + "sample.psd");
```

Se il file non viene trovato, Aspose.PSD lancerà un'eccezione informativa—controlla nuovamente il nome del file e il percorso.

## Passo 4: Cicla attraverso i livelli di compressione

Per esplorare ogni possibile **livello di compressione png**, utilizziamo un semplice ciclo `for`. Questo crea automaticamente nove PNG aggiuntivi, ciascuno con una diversa impostazione di compressione:

```java
for (int i = 0; i <= 9; i++) {
    // Create a new instance of PngOptions
    PngOptions options = new PngOptions();
    options.setCompressionLevel(i); // Set the compression level
```

Il ciclo parte da 0 (nessuna compressione) fino a 9 (compressione massima), offrendoti una chiara visione del compromesso tra dimensione del file e tempo di elaborazione.

## Passo 5: Salva i file PNG compressi

All'interno del ciclo, salva ogni PNG usando un nome file che rifletta il livello di compressione. Questo rende il confronto immediato:

```java
    psdImage.save(dataDir + i + "_out.png", options);
}
```

Al termine del ciclo, avrai file denominati `0_out.png`, `1_out.png`, … `9_out.png` nella tua directory.

## Problemi comuni e soluzioni

| Problema | Perché accade | Soluzione |
|----------|----------------|-----------|
| **FileNotFoundException** | Percorso `dataDir` errato o `sample.psd` mancante. | Verifica la stringa del percorso e assicurati che il file PSD esista. |
| **OutOfMemoryError** su PSD di grandi dimensioni | Caricamento di un PSD enorme senza sufficiente spazio heap. | Aumenta l'heap JVM (`-Xmx2g`) o elabora l'immagine a blocchi. |
| **Il PNG compresso appare invariato** | Uso di un livello di compressione basso (0‑2). | Aumenta il livello a 5‑9 per una riduzione di dimensione evidente. |
| **LicenseException** | Esecuzione senza una licenza valida di Aspose.PSD. | Applica una licenza di prova o acquista una licenza completa. |

## Domande frequenti

**Q: Cos'è Aspose.PSD per Java?**  
A: Aspose.PSD per Java è una libreria che consente agli sviluppatori di manipolare file Photoshop programmaticamente, includendo lettura, modifica ed esportazione in formati come PNG, JPEG e TIFF.

**Q: Posso comprimere altri formati di immagine oltre a PNG?**  
A: Questo tutorial si concentra su PNG, ma Aspose.PSD supporta PSD, TIFF, JPEG, BMP e altri. Puoi cambiare la classe delle opzioni di output per puntare a un formato diverso.

**Q: È necessaria una licenza per usare Aspose.PSD?**  
A: Sebbene tu possa valutare la libreria con una prova gratuita, è richiesta una licenza completa per le distribuzioni in produzione. Puoi ottenerla [qui](https://purchase.aspose.com/buy).

**Q: Cosa devo fare se incontro un errore durante l'esecuzione del codice?**  
A: Controlla nuovamente i percorsi dei file, assicurati che tutte le istruzioni `import` siano presenti e verifica di utilizzare una versione compatibile del JAR Aspose.PSD.

**Q: Dove posso trovare ulteriore documentazione su Aspose.PSD per Java?**  
A: Riferimenti API dettagliati ed esempi aggiuntivi sono disponibili al [riferimento Aspose.PSD](https://reference.aspose.com/psd/java/).

---

**Ultimo aggiornamento:** 2026-03-15  
**Testato con:** Aspose.PSD per Java 24.12 (ultima versione al momento della stesura)  
**Autore:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}