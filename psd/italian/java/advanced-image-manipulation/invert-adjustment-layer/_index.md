---
date: 2025-12-02
description: Scopri come utilizzare la libreria Java per l'elaborazione delle immagini
  Aspose.PSD per applicare più livelli di regolazione, incluso il Livello di Regolazione
  Inverti, per una manipolazione fluida dei PSD.
linktitle: Invert Adjustment Layer
second_title: Aspose.PSD Java API
title: 'Libreria Java per l''elaborazione delle immagini: Inverti livello con Aspose.PSD'
url: /it/java/advanced-image-manipulation/invert-adjustment-layer/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Livello di Regolazione Inverti in Aspose.PSD per Java

## Introduzione

Se stai cercando una **image processing java library** robusta, Aspose.PSD per Java è una delle opzioni più versatili sul mercato. In questo tutorial vedremo come aggiungere un **Invert Adjustment Layer** a un file PSD, una tecnica che puoi combinare con altri livelli di regolazione per ottenere effetti visivi sofisticati. Che tu stia creando uno strumento di elaborazione batch o un editor di immagini singole, questa guida ti offre un percorso chiaro, passo‑passo, per completare il lavoro rapidamente.

## Risposte Rapide
- **Che cosa fa il Livello di Regolazione Inverti?** Inverte tutti i valori di colore nell'area selezionata, creando un effetto immagine negativa.  
- **Quale libreria fornisce questa funzionalità?** Aspose.PSD, una **image processing java library** leader.  
- **Posso impilarlo con altre regolazioni?** Sì – puoi **apply multiple adjustment layers** come Brightness/Contrast, Hue/Saturation e altro.  
- **Ho bisogno di una licenza per lo sviluppo?** È disponibile una prova gratuita; è necessaria una licenza per l'uso in produzione.  
- **Quanto tempo richiede l'implementazione?** Tipicamente meno di 10 minuti per un caso d'uso base.

## Che cos'è il Livello di Regolazione Inverti?

Il Livello di Regolazione Inverti è una modifica non distruttiva che inverte i valori RGB di ogni pixel interessato. Poiché si trova sopra lo stack dei livelli, puoi attivare/disattivare la sua visibilità o riordinarlo senza alterare permanentemente i dati dell'immagine originale.

## Perché usare Aspose.PSD come tua libreria di Image Processing Java?

- **Supporto completo PSD** – leggi, modifica e scrivi file Photoshop senza avere Photoshop installato.  
- **Cross‑platform** – funziona su qualsiasi runtime Java (Java 6+).  
- **Funzionalità di regolazione avanzate** – include metodi integrati per molte modifiche comuni, rendendo facile **apply multiple adjustment layers** in un unico flusso di lavoro.  
- **Ottimizzato per le prestazioni** – gestisce file di grandi dimensioni in modo efficiente, fondamentale per l'elaborazione batch.

## Prerequisiti

Prima di iniziare, assicurati di avere quanto segue:

1. **Aspose.PSD Library** – scaricala dal sito ufficiale [here](https://releases.aspose.com/psd/java/).  
2. **Java Development Environment** – JDK 6.0 o successivo installato e configurato.  

Ora, immergiamoci nel codice.

## Importa Pacchetti

Inizia importando le classi necessarie. Queste importazioni ti danno accesso alle API di gestione delle immagini di base e alle funzionalità specifiche per PSD.

```java
import com.aspose.psd.Image;

import com.aspose.psd.fileformats.psd.PsdImage;
```

## Passo 1: Configura la Directory del Documento

Definisci la cartella che contiene il tuo file PSD di origine e dove verrà salvato l'output.

```java
String dataDir = "Your Document Directory";
```

## Passo 2: Carica il File PSD

Carica il file di origine in un oggetto `PsdImage`. Questo oggetto rappresenta l'intero documento PSD in memoria.

```java
String filePath = dataDir + "InvertStripes_before.psd";
String outputPath = dataDir + "InvertStripes_after.psd";

PsdImage im = (PsdImage)Image.load(filePath);
```

## Passo 3: Aggiungi il Livello di Regolazione Inverti

Chiama il metodo integrato per inserire un Invert Adjustment Layer sopra lo stack dei livelli corrente. Puoi successivamente aggiungere altri livelli (ad es., Brightness, Hue) per **apply multiple adjustment layers**.

```java
im.addInvertAdjustmentLayer();
```

## Passo 4: Salva l'Output

Salva il PSD modificato su disco. Il file salvato ora contiene il Livello di Regolazione Inverti e può essere aperto in Photoshop o in qualsiasi visualizzatore compatibile con PSD.

```java
im.save(outputPath);
```

### Cosa è successo?

- Il PSD è stato caricato in memoria.  
- È stato aggiunto un Invert Adjustment Layer come livello più alto.  
- L'immagine è stata salvata, preservando la modifica non distruttiva.

Hai ora usato con successo Aspose.PSD, una **image processing java library**, per manipolare un file PSD.

## Problemi Comuni e Suggerimenti

| Problema | Causa | Soluzione |
|----------|-------|-----------|
| **NullPointerException su `Image.load`** | Percorso file errato o file mancante | Verifica `dataDir` e il nome del file; usa percorsi assoluti per i test |
| **Ordine dei livelli non come previsto** | Aggiungere livelli dopo quelli esistenti cambia lo stacking | Usa `im.addInvertAdjustmentLayer()` prima di aggiungere altre regolazioni, o riordina i livelli tramite `im.getLayers()` |
| **Rallentamento delle prestazioni su PSD grandi** | Caricamento di file molto grandi in memoria | Considera di elaborare le pagine a blocchi o aumentare la dimensione dell'heap JVM (`-Xmx2g`) |

## Domande Frequenti

**D: Aspose.PSD è compatibile con tutte le versioni di Java?**  
R: Aspose.PSD supporta Java 6.0 e versioni successive.

**D: Posso applicare più livelli di regolazione in un'unica operazione?**  
R: Sì, puoi impilare diversi livelli di regolazione — come Invert, Brightness e Hue/Saturation — per ottenere effetti complessi.

**D: Dove posso trovare documentazione aggiuntiva per Aspose.PSD?**  
R: Consulta la documentazione [here](https://reference.aspose.com/psd/java/) per guide complete e riferimenti API.

**D: È disponibile una prova gratuita per Aspose.PSD?**  
R: Sì, puoi provare la versione gratuita [here](https://releases.aspose.com/).

**D: Come posso ottenere una licenza temporanea per Aspose.PSD?**  
R: Puoi ottenere una licenza temporanea [here](https://purchase.aspose.com/temporary-license/).

---

**Last Updated:** 2025-12-02  
**Tested With:** Aspose.PSD 24.12 for Java  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}