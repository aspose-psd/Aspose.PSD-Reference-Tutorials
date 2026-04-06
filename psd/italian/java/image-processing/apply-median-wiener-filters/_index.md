---
date: 2026-01-07
description: Impara passo dopo passo le tecniche di filtraggio per applicare i filtri
  Mediano e Wiener usando Aspose.PSD per Java e converti i file PSD in GIF in modo
  efficiente.
linktitle: Apply Median and Wiener Filters
second_title: Aspose.PSD Java API
title: 'Filtro passo passo - applica i filtri mediano e Wiener (Java)'
url: /it/java/image-processing/apply-median-wiener-filters/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Filtro passo‑passo: applicare filtri mediano e Wiener (Java)

## Introduzione

Se stai cercando un **flusso di lavoro filtro passo‑passo** per pulire le immagini rumorose in Java, sei nel posto giusto. Aspose.PSD per Java rende semplice applicare sia il filtro Mediano sia il filtro Wiener, e ti permette anche di **convertire PSD in GIF** dopo l’elaborazione. In questo tutorial percorreremo tutto ciò di cui hai bisogno—dalla configurazione della libreria al salvataggio del risultato filtrato—così potrai integrare una denoising di alta qualità nelle tue applicazioni con sicurezza.

## Risposte rapide
- **Cosa fa il filtro Mediano?** Riduce il rumore sale‑e‑pepe preservando i bordi.  
- **Quando devo usare il filtro Wiener?** Per una riduzione adattiva del rumore che considera la varianza locale dell’immagine.  
- **È necessaria una licenza per eseguire il codice?** Una versione di prova gratuita è sufficiente per lo sviluppo; è richiesta una licenza commerciale per la produzione.  
- **Posso salvare l’output come GIF?** Sì—Aspose.PSD ti consente di **convertire PSD in GIF** in un unico passaggio.  
- **Quanto tempo richiede l’implementazione?** Tipicamente meno di 10 minuti per una configurazione di base.

## Che cos’è un filtro passo‑passo?

Un approccio *filtro passo‑passo* suddivide l’elaborazione delle immagini in fasi chiare e gestibili—caricamento dell’immagine, configurazione delle opzioni del filtro, applicazione del filtro e, infine, salvataggio del risultato. Questo flusso metodico ti aiuta a fare il debug di ogni parte, riutilizzare il codice e adattare il processo a diversi formati di immagine.

## Perché usare Aspose.PSD per Java?

- **Ampio supporto di formati** – Gestisce PSD, PNG, JPEG, GIF e molto altro.  
- **Nessuna dipendenza esterna** – Pure Java, facile da incorporare in qualsiasi progetto.  
- **Opzioni filtro integrate** – Mediano, Wiener e altri filtri avanzati sono pronti all’uso.  
- **Conversione con un click** – Esporta direttamente in GIF, PNG o JPEG dopo l’elaborazione.

## Prerequisiti

Prima di iniziare, assicurati di avere:

1. **Libreria Aspose.PSD per Java** – Scarica e installa la libreria da [qui](https://releases.aspose.com/psd/java/).  
2. **Ambiente di sviluppo Java** – JDK 8+ e un IDE o uno strumento di build (Maven/Gradle) configurati sulla tua macchina.

## Importare i pacchetti

Inizia importando le classi necessarie che ti danno accesso alla gestione delle immagini e alle opzioni filtro.

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.imagefilters.filteroptions.MedianFilterOptions;
import com.aspose.psd.imageoptions.GifOptions;
```

## Filtro passo‑passo: come applicare il filtro Mediano

### Passo 1: caricare l’immagine

Per prima cosa, indica all’API il file PSD che desideri pulire.

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

// Load the source image
Image image = Image.load(sourceFile);
```

### Passo 2: convertire l’immagine in RasterImage

Il filtro opera sui dati raster, quindi convertiamo l’`Image` generica in una `RasterImage`.

```java
// Cast the image into RasterImage
RasterImage rasterImage = (RasterImage)image;
if (rasterImage == null) {
    return;
}
```

### Passo 3: creare un’istanza di MedianFilterOptions

Configura la dimensione del kernel mediano. Una dimensione di **4** funziona bene per rumore moderato.

```java
// Create an instance of MedianFilterOptions class and set the filter size
MedianFilterOptions options = new MedianFilterOptions(4);
```

### Passo 4: applicare il filtro Mediano

Ora applica il filtro a tutti i limiti dell’immagine.

```java
// Apply MedianFilterOptions filter to RasterImage object
rasterImage.filter(image.getBounds(), options);
```

### Passo 5: salvare l’immagine risultante (convertire PSD in GIF)

Dopo il filtraggio, salveremo l’output come GIF—dimostrando la capacità di **convertire PSD in GIF**.

```java
String destName = dataDir + "median_test_denoise_out.gif";
// Save the resultant image as a GIF
image.save(destName, new GifOptions());
```

Seguendo questi passaggi hai applicato con successo un filtro Mediano e hai esportato l’immagine pulita come GIF.

## Applicare il filtro Wiener (estensione opzionale)

Se il tuo progetto richiede una riduzione adattiva del rumore, puoi sostituire il filtro Mediano con il filtro Wiener. La struttura del codice è identica; devi solo importare `WienerFilterOptions` e istanziarlo con il raggio desiderato.

> **Suggerimento professionale:** sperimenta diverse dimensioni del kernel per entrambi i filtri per trovare il giusto equilibrio tra rimozione del rumore e conservazione dei dettagli.

## Problemi comuni e risoluzione

| Sintomo | Probabile causa | Soluzione |
|---------|----------------|-----------|
| `ClassCastException` durante il cast a `RasterImage` | Il file di input non è un PSD compatibile con raster | Verifica che il PSD contenga livelli raster o converti i livelli in raster prima |
| GIF di output è vuota | Il percorso di destinazione è errato o la cartella non ha permessi di scrittura | Assicurati che `dataDir` punti a una directory esistente e scrivibile |
| Il filtro sembra non avere effetto | La dimensione del kernel è troppo piccola per il livello di rumore | Aumenta la dimensione del filtro (es. `new MedianFilterOptions(6)`) |

## Domande frequenti

**D1: Posso applicare questi filtri a immagini di qualsiasi formato?**  
R1: Sì, Aspose.PSD supporta un’ampia gamma di formati immagine, rendendolo versatile per vari progetti.

**D2: È disponibile una versione di prova gratuita per Aspose.PSD per Java?**  
R2: Sì, puoi ottenere una prova gratuita [qui](https://releases.aspose.com/).

**D3: Come posso ottenere supporto per Aspose.PSD per Java?**  
R3: Visita il [forum Aspose.PSD](https://forum.aspose.com/c/psd/34) per il supporto della community.

**D4: Dove posso trovare la documentazione per Aspose.PSD per Java?**  
R4: Consulta la documentazione [qui](https://reference.aspose.com/psd/java/).

**D5: Come posso acquistare Aspose.PSD per Java?**  
R5: Puoi comprare il prodotto [qui](https://purchase.aspose.com/buy).

## Conclusione

In questa guida abbiamo mostrato un processo **filtro passo‑passo** per applicare i filtri Mediano (e opzionalmente Wiener) usando Aspose.PSD per Java, e abbiamo illustrato come **convertire PSD in GIF** dopo la denoising. Con questi blocchi costitutivi puoi integrare pipeline di elaborazione immagini robuste in qualsiasi applicazione Java—sia che tu stia pulendo foto, preparando risorse per il web o automatizzando conversioni batch.

---

**Ultimo aggiornamento:** 2026-01-07  
**Testato con:** Aspose.PSD per Java 24.12 (ultima versione al momento della stesura)  
**Autore:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}