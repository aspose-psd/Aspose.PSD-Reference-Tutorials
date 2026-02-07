---
date: 2026-02-07
description: Scopri come utilizzare la libreria Java per l'elaborazione delle immagini
  Aspose.PSD per applicare più livelli di regolazione, incluso il livello di regolazione
  Inverti, per una manipolazione PSD senza interruzioni.
linktitle: Invert Adjustment Layer
second_title: Aspose.PSD Java API
title: 'Libreria Java per l''elaborazione delle immagini: Inverti il livello con Aspose.PSD'
url: /it/java/advanced-image-manipulation/invert-adjustment-layer/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Livello di Regolazione Invert in Aspose.PSD per Java

## Introduzione

Se stai cercando una **libreria di elaborazione immagini java** robusta, Aspose.PSD per Java è una delle opzioni più versatili sul mercato. In questo tutorial vedremo come aggiungere un **Livello di Regolazione Invert** a un file PSD, una tecnica che puoi combinare con altri livelli di regolazione per ottenere effetti visivi sofisticati. Che tu stia costruendo uno strumento di elaborazione batch o un editor di immagini singole, questa guida ti offre un percorso chiaro, passo‑per‑passo, per completare il lavoro rapidamente.

## Risposte Rapide
- **Cosa fa il Livello di Regolazione Invert?** Inverte tutti i valori di colore nell'area selezionata, creando un effetto immagine negativa.  
- **Quale libreria fornisce questa funzionalità?** Aspose.PSD, una libreria leader di elaborazione immagini java.  
- **Posso combinarlo con altre regolazioni?** Sì – puoi **applicare più livelli di regolazione** come Luminosità/Contrasto, Tinta/Saturazione e altro ancora.  
- **È necessaria una licenza per lo sviluppo?** È disponibile una versione di prova gratuita; è richiesta una licenza per l'uso in produzione.  
- **Quanto tempo richiede l'implementazione?** Tipicamente meno di 10 minuti per un caso d'uso di base.

## Cos'è il Livello di Regolazione Invert?

Il Livello di Regolazione Invert è una modifica non distruttiva che capovolge i valori RGB di ogni pixel a cui si applica. Poiché si trova sopra lo stack dei livelli, puoi attivare/disattivare la sua visibilità o riordinarlo senza alterare permanentemente i dati originali dell'immagine.

## Come invertire un livello usando Aspose.PSD

Di seguito vedrai esattamente **come invertire un livello** in un file PSD. I passaggi sono deliberatamente semplici così da poterti concentrare sul concetto piuttosto che sul codice boilerplate.

## Perché usare Aspose.PSD come tua libreria di elaborazione immagini Java?

- **Supporto completo PSD** – leggi, modifica e scrivi file Photoshop senza avere Photoshop installato.  
- **Cross‑platform** – funziona su qualsiasi runtime Java (Java 6+).  
- **Ricche funzionalità di regolazione** – include metodi integrati per molte modifiche comuni, facilitando **l'applicazione di più livelli di regolazione** in un unico flusso di lavoro.  
- **Ottimizzato per le prestazioni** – gestisce file di grandi dimensioni in modo efficiente, fondamentale per l'elaborazione batch.

## Prerequisiti

Prima di iniziare, assicurati di avere quanto segue:

1. **Libreria Aspose.PSD** – scaricala dal sito ufficiale [qui](https://releases.aspose.com/psd/java/).  
2. **Ambiente di sviluppo Java** – JDK 6.0 o successivo installato e configurato.  

Ora, immergiamoci nel codice.

## Importare i pacchetti

Inizia importando le classi necessarie. Queste importazioni ti danno accesso alle API di gestione delle immagini e alle funzionalità specifiche di PSD.

```java
import com.aspose.psd.Image;

import com.aspose.psd.fileformats.psd.PsdImage;
```

## Passo 1: Configurare la directory del documento

Definisci la cartella che contiene il tuo file PSD di origine e dove verrà salvato l'output.

```java
String dataDir = "Your Document Directory";
```

## Passo 2: Caricare il file PSD

Carica il file di origine in un oggetto `PsdImage`. Questo oggetto rappresenta l'intero documento PSD in memoria.

```java
String filePath = dataDir + "InvertStripes_before.psd";
String outputPath = dataDir + "InvertStripes_after.psd";

PsdImage im = (PsdImage)Image.load(filePath);
```

## Passo 3: Aggiungere il Livello di Regolazione Invert

Chiama il metodo integrato per inserire un Livello di Regolazione Invert sopra lo stack dei livelli corrente. Potrai successivamente aggiungere altri livelli (ad es., Luminosità, Tinta) per **applicare più livelli di regolazione**.

```java
im.addInvertAdjustmentLayer();
```

## Passo 4: Salvare l'output

Persisti il PSD modificato su disco. Il file salvato ora contiene il Livello di Regolazione Invert e può essere aperto in Photoshop o in qualsiasi visualizzatore compatibile con PSD.

```java
im.save(outputPath);
```

### Cosa è appena successo?

- Il PSD è stato caricato in memoria.  
- È stato aggiunto un Livello di Regolazione Invert come livello più in alto.  
- L'immagine è stata salvata, preservando la modifica non distruttiva.

Hai ora usato con successo Aspose.PSD, una **libreria di elaborazione immagini java**, per manipolare un file PSD.

## Problemi comuni e consigli

| Problema | Causa | Soluzione |
|----------|-------|-----------|
| **NullPointerException su `Image.load`** | Percorso file errato o file mancante | Verifica `dataDir` e il nome del file; usa percorsi assoluti per i test |
| **Ordine dei livelli non come previsto** | L'aggiunta di livelli dopo quelli esistenti modifica lo stacking | Usa `im.addInvertAdjustmentLayer()` prima di aggiungere altre regolazioni, o riordina i livelli tramite `im.getLayers()` |
| **Rallentamento delle prestazioni su PSD grandi** | Caricamento di file molto grandi in memoria | Considera l'elaborazione delle pagine a blocchi o aumenta la dimensione dell'heap JVM (`-Xmx2g`) |

## Domande frequenti

**D: Aspose.PSD è compatibile con tutte le versioni di Java?**  
R: Aspose.PSD supporta Java 6.0 e versioni successive.

**D: Posso applicare più livelli di regolazione in un'unica operazione?**  
R: Sì, puoi impilare diversi livelli di regolazione — come Invert, Luminosità e Tinta/Saturazione — per ottenere effetti complessi.

**D: Dove posso trovare ulteriore documentazione per Aspose.PSD?**  
R: Consulta la documentazione [qui](https://reference.aspose.com/psd/java/) per guide complete e riferimenti API.

**D: È disponibile una versione di prova gratuita per Aspose.PSD?**  
R: Sì, puoi esplorare la versione di prova [qui](https://releases.aspose.com/).

**D: Come posso ottenere una licenza temporanea per Aspose.PSD?**  
R: Puoi ottenere una licenza temporanea [qui](https://purchase.aspose.com/temporary-license/).

---

**Ultimo aggiornamento:** 2026-02-07  
**Testato con:** Aspose.PSD 24.12 per Java  
**Autore:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}