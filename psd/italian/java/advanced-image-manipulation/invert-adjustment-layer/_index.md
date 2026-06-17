---
date: 2026-04-22
description: Scopri come utilizzare la libreria Java di elaborazione immagini Aspose.PSD
  per applicare più livelli di regolazione, incluso il livello di regolazione Inverti,
  per una manipolazione fluida dei PSD.
keywords:
- image processing java library
- how to add invert
- invert colors psd
- batch process psd images
- apply multiple adjustment layers
linktitle: Livello di regolazione Inverti
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

Se stai cercando una robusta **image processing java library**, Aspose.PSD per Java è una delle opzioni più versatili sul mercato. In questo tutorial ti mostreremo come aggiungere un **Invert Adjustment Layer** a un file PSD, una tecnica che puoi combinare con altri livelli di regolazione per ottenere effetti visivi sofisticati. Che tu stia creando uno strumento di elaborazione batch, un servizio di immagini lato server o un editor di immagini singole, questa guida ti offre un percorso chiaro, passo‑per‑passo, per completare il lavoro rapidamente e in modo affidabile.

## Risposte Rapide
- **Che cosa fa il Livello di Regolazione Inverti?** Inverte tutti i valori di colore nell'area selezionata, creando un effetto immagine negativa (cioè **converte PSD in negativo**).  
- **Quale libreria fornisce questa funzionalità?** Aspose.PSD, una delle principali **image processing java library**.  
- **Posso combinarlo con altre regolazioni?** Sì – puoi **applicare più livelli di regolazione** come Luminosità/Contrasto, Tinta/Saturazione e altro.  
- **Ho bisogno di una licenza per lo sviluppo?** È disponibile una versione di prova gratuita; è necessaria una licenza per l'uso in produzione.  
- **Quanto tempo richiede l'implementazione?** Tipicamente meno di 10 minuti per un caso d'uso base.

## Cos'è il Livello di Regolazione Inverti?

Il Livello di Regolazione Inverti è una modifica non distruttiva che inverte i valori RGB di ogni pixel interessato. Poiché si trova sopra lo stack dei livelli, puoi attivare o disattivare la sua visibilità o riordinarlo senza alterare permanentemente i dati originali dell'immagine. Questo è il modo più semplice per **invert colors PSD** file o creare un negativo fotografico.

## Perché usare Aspose.PSD come la tua Image Processing Java Library?

- **Full PSD support** – leggi, modifica e scrivi file Photoshop senza avere Photoshop installato.  
- **Cross‑platform** – funziona su qualsiasi runtime Java (Java 6+).  
- **Rich adjustment features** – include metodi integrati per molte modifiche comuni, rendendo facile **applicare più livelli di regolazione** in un unico flusso di lavoro.  
- **Performance‑optimized** – gestisce file di grandi dimensioni in modo efficiente, il che è essenziale per **batch process psd images**.  

## Prerequisiti

Prima di iniziare, assicurati di avere quanto segue:

1. **Aspose.PSD Library** – scaricala dal sito ufficiale [qui](https://releases.aspose.com/psd/java/).  
2. **Java Development Environment** – JDK 6.0 o successivo installato e configurato.  

Ora, immergiamoci nel codice.

## Importa Pacchetti

Inizia importando le classi necessarie. Questi import ti danno accesso alle API core di gestione delle immagini e alle funzionalità specifiche di PSD.

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

Chiama il metodo integrato per inserire un Livello di Regolazione Inverti sopra lo stack dei livelli corrente. Puoi successivamente aggiungere altri livelli (ad esempio, Luminosità, Tinta) per **applicare più livelli di regolazione**.

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
- È stato aggiunto un Livello di Regolazione Inverti come livello più alto.  
- L'immagine è stata salvata, preservando la modifica non distruttiva.

Hai ora usato con successo Aspose.PSD, una **image processing java library**, per manipolare un file PSD.

## Elaborazione batch di immagini PSD con regolazione inverti

Se devi applicare lo stesso effetto inverti a decine o centinaia di file, puoi inserire il codice sopra all'interno di un semplice ciclo che itera su una directory di PSD. Poiché la libreria è **performance‑optimized**, l'elaborazione di grandi batch rimane veloce, e puoi combinare il passo di inversione con altre regolazioni (ad esempio, luminosità, tinta) nello stesso ciclo.

## Convertire un PSD in un'immagine negativa

Il Livello di Regolazione Inverti è essenzialmente l'operazione **convert PSD to negative**. Aggiungendo questo livello come elemento più alto, ottieni un effetto completamente negativo senza alterare permanentemente i dati pixel originali. Puoi successivamente rimuovere o disabilitare il livello per tornare all'aspetto originale.

## Problemi Comuni e Suggerimenti

| Issue | Cause | Solution |
|-------|-------|----------|
| **NullPointerException su `Image.load`** | Percorso file errato o file mancante | Verifica `dataDir` e il nome del file; usa percorsi assoluti per i test |
| **Ordine dei livelli non come previsto** | Aggiungere livelli dopo quelli esistenti cambia lo stacking | Usa `im.addInvertAdjustmentLayer()` prima di aggiungere altre regolazioni, o riordina i livelli tramite `im.getLayers()` |
| **Rallentamento delle prestazioni su PSD grandi** | Caricamento di file molto grandi in memoria | Considera di elaborare le pagine a blocchi o aumentare la dimensione dell'heap JVM (`-Xmx2g`) |

## Domande Frequenti

**Q: Aspose.PSD è compatibile con tutte le versioni Java?**  
A: Aspose.PSD supporta Java 6.0 e versioni successive.

**Q: Posso applicare più livelli di regolazione in un'unica operazione?**  
A: Sì, puoi impilare diversi livelli di regolazione — come Invert, Brightness e Hue/Saturation — per ottenere effetti complessi.

**Q: Dove posso trovare documentazione aggiuntiva per Aspose.PSD?**  
A: Consulta la documentazione [qui](https://reference.aspose.com/psd/java/) per guide complete e riferimenti API.

**Q: È disponibile una versione di prova gratuita per Aspose.PSD?**  
A: Sì, puoi esplorare la versione di prova gratuita [qui](https://releases.aspose.com/).

**Q: Come posso ottenere una licenza temporanea per Aspose.PSD?**  
A: Puoi ottenere una licenza temporanea [qui](https://purchase.aspose.com/temporary-license/).

---

**Ultimo Aggiornamento:** 2026-04-22  
**Testato Con:** Aspose.PSD 24.12 for Java  
**Autore:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}