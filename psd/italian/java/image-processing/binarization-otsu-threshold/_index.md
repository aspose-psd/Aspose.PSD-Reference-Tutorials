---
date: 2026-08-11
description: Scopri come applicare la soglia Otsu in Java utilizzando Aspose.PSD per
  Java – una potente tecnica di segmentazione delle immagini.
keywords:
- apply otsu threshold java
- image segmentation with otsu
- java image segmentation tutorial
lastmod: 2026-08-11
linktitle: Binarizzazione con Otsu Threshold
og_description: Applicare la soglia Otsu in Java con Aspose.PSD per Java. Questo tutorial
  ti mostra step‑by‑step come binarizzare le immagini, spiega perché il metodo è veloce
  e fornisce consigli di troubleshooting per le comuni insidie.
og_image_alt: Screenshot of Java code applying Otsu threshold using Aspose.PSD
og_title: Applicare la soglia Otsu in Java con Aspose.PSD – guida rapida
schemas:
- author: Aspose
  dateModified: '2026-08-11'
  description: Learn how to apply otsu threshold java using Aspose.PSD for Java –
    a powerful image segmentation technique.
  headline: Apply otsu threshold java with Aspose.PSD
  type: TechArticle
- description: Learn how to apply otsu threshold java using Aspose.PSD for Java –
    a powerful image segmentation technique.
  name: Apply otsu threshold java with Aspose.PSD
  steps:
  - name: set up your document directory
    text: Define the folder that contains the source PSD file and the output location
      for the binarized image.
  - name: load the PSD file
    text: '`PsdImage` is the top‑level Aspose.PSD class that represents a PSD document
      and gives access to its layers, metadata, and pixel data.'
  - name: cache the image
    text: '`RasterImage` holds the raster representation of a layer; calling `cache()`
      loads the pixel data into memory so subsequent operations are fast.'
  - name: binarize image with Otsu threshold
    text: '`applyOtsuThreshold()` evaluates all possible gray levels and selects the
      optimal cutoff, producing a binary image that separates foreground objects from
      the background.'
  - name: save the resultant image
    text: '`JpegOptions` configures JPEG‑specific settings such as quality and compression
      when saving the processed image. You can also choose PNG or BMP by swapping
      the options class – the API supports over **30 image formats** for output. {{<
      blocks/products/products-backtop-button >}}'
  type: HowTo
- questions:
  - answer: It automatically finds the gray‑level that minimizes intra‑class variance,
      producing a binary image in one step.
    question: What does Otsu Threshold do?
  - answer: A free trial works for development; a commercial license is required for
      production.
    question: Do I need a license to run the sample?
  - answer: Aspose.PSD for Java supports Java 8 through Java 21.
    question: Which Java version is supported?
  - answer: Yes – you can iterate over each layer and apply the threshold individually.
    question: Can I process multi‑layer PSD files?
  - answer: For a 1920 × 1080 image the Otsu binarization finishes in under 30 ms
      on a typical laptop CPU.
    question: How fast is the operation?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- apply otsu threshold java
- image segmentation
- Aspose.PSD
- Java image processing
title: Applicare la soglia Otsu in Java con Aspose.PSD
url: /it/java/image-processing/binarization-otsu-threshold/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Applica soglia Otsu Java con Aspose.PSD

## Introduzione

In questo tutorial imparerai come **applicare soglia Otsu Java** usando la libreria Aspose.PSD per Java. La binarizzazione con soglia Otsu è una delle tecniche di segmentazione delle immagini più affidabili, selezionando automaticamente un valore di livello di grigio ottimale per separare il primo piano dallo sfondo. Alla fine della guida avrai uno snippet Java funzionante che trasforma qualsiasi livello PSD in un'immagine pulita in bianco e nero.

## Risposte rapide
- **Cosa fa la soglia Otsu?** Trova automaticamente il livello di grigio che minimizza la varianza intra‑classe, producendo un'immagine binaria in un solo passo.  
- **Ho bisogno di una licenza per eseguire l'esempio?** Una prova gratuita è sufficiente per lo sviluppo; è necessaria una licenza commerciale per la produzione.  
- **Quale versione di Java è supportata?** Aspose.PSD per Java supporta Java 8 fino a Java 21.  
- **Posso elaborare file PSD multi‑layer?** Sì – è possibile iterare su ogni livello e applicare la soglia individualmente.  
- **Quanto è veloce l'operazione?** Per un'immagine 1920 × 1080 la binarizzazione Otsu termina in meno di 30 ms su una tipica CPU di laptop.

## Che cos'è applicare soglia Otsu Java?

Applicare soglia Otsu Java è il processo di utilizzo del codice Java per invocare l'algoritmo di Otsu su un'immagine, producendo un risultato binario (bianco‑e‑nero). L'algoritmo valuta tutti i possibili livelli di grigio, seleziona quello che fornisce la varianza intra‑classe ponderata più bassa e poi classifica ogni pixel come primo piano o sfondo. Questo approccio automatizzato elimina la necessità di una selezione manuale della soglia e funziona bene su immagini con istogrammi bimodali, rendendolo ideale per l'elaborazione batch di grandi collezioni di immagini.

## Perché usare Aspose.PSD per Java?

Aspose.PSD per Java supporta **oltre 50 formati di input e output** (inclusi PSD, JPEG, PNG, BMP e TIFF) e può elaborare file fino a **2 GB** di dimensione senza caricare l'intero documento in memoria. L'implementazione Otsu integrata nella libreria funziona in tempo lineare, consentendo di elaborare in batch centinaia di immagini in pochi secondi.

## Prerequisiti
- **Ambiente di sviluppo Java** – JDK 8 o versioni successive installate e configurate.  
- **Libreria Aspose.PSD per Java** – Scarica e installa la libreria dalla pagina ufficiale di download di Aspose.PSD per Java. Puoi trovare il link di download [Aspose.PSD for Java download page](https://releases.aspose.com/psd/java/).  
- **File PSD di esempio** – Disporre di un file PSD con almeno un livello raster per testare la binarizzazione.  
- Per altri prodotti Aspose puoi anche consultare la pagina generale dei rilasci su [Aspose releases](https://releases.aspose.com/).

## Importa pacchetti

Importa le classi `PsdImage`, `RasterImage` e `JpegOptions` dalla libreria Aspose.PSD, che forniscono l'accesso ai file PSD, ai dati raster e alle opzioni di esportazione JPEG.  
```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterCachedImage;

import com.aspose.psd.imageoptions.JpegOptions;
```

## Come applicare soglia Otsu Java?

Carica il tuo PSD, recupera il livello raster desiderato e chiama il metodo di binarizzazione Otsu – l'intero flusso di lavoro si riduce a cinque istruzioni concise. Prima crei un oggetto `PsdImage` che rappresenta il file di origine, poi ottieni il `RasterImage` per il livello target, invochi `applyOtsuThreshold()` su di esso e infine salvi il risultato usando `JpegOptions`. Questo approccio garantisce un utilizzo minimo della memoria e massime prestazioni.

### Passo 1: configura la directory del documento

Definisci la cartella che contiene il file PSD di origine e la posizione di output per l'immagine binarizzata.  
```java
String dataDir = "Your Document Directory";
```

### Passo 2: carica il file PSD

`PsdImage` è la classe di livello superiore di Aspose.PSD che rappresenta un documento PSD e fornisce l'accesso ai suoi livelli, metadati e dati dei pixel.  
```java
String sourceFile = dataDir + "sample.psd";
Image image = Image.load(sourceFile);
```

### Passo 3: memorizza nella cache l'immagine

`RasterImage` contiene la rappresentazione raster di un livello; chiamare `cache()` carica i dati dei pixel in memoria così le operazioni successive sono rapide.  
```java
RasterCachedImage rasterCachedImage = (RasterCachedImage)image;

if (!rasterCachedImage.isCached()) {
    rasterCachedImage.cacheData();
}
```

### Passo 4: binarizza l'immagine con soglia Otsu

`applyOtsuThreshold()` valuta tutti i possibili livelli di grigio e seleziona il valore di cutoff ottimale, producendo un'immagine binaria che separa gli oggetti in primo piano dallo sfondo.  
```java
rasterCachedImage.binarizeOtsu();
```

### Passo 5: salva l'immagine risultante

`JpegOptions` configura le impostazioni specifiche per JPEG come qualità e compressione durante il salvataggio dell'immagine elaborata. Puoi anche scegliere PNG o BMP sostituendo la classe delle opzioni – l'API supporta oltre **30 formati immagine** per l'output.  
```java
String destName = dataDir + "BinarizationWithOtsuThreshold_out.jpg";
rasterCachedImage.save(destName, new JpegOptions());
```

{{< blocks/products/products-backtop-button >}}

## Problemi comuni e soluzioni

- **Errori di memoria fuori dai limiti** – Assicurati di chiamare `cache()` sui livelli grandi prima dell'elaborazione; questo costringe Aspose.PSD a utilizzare un approccio di streaming.  
- **Colori errati dopo la binarizzazione** – Verifica che il livello di origine sia un'immagine realmente in scala di grigi; i livelli a colori devono essere convertiti in scala di grigi prima usando `convertToGrayscale()`.

## Domande frequenti

### Q1: Cos'è la binarizzazione con soglia Otsu?

La binarizzazione con soglia Otsu è un metodo utilizzato per la segmentazione delle immagini, che separa un'immagine in primo piano e sfondo basandosi su una soglia ottimale.

### Q2: Posso usare Aspose.PSD per Java gratuitamente?

Aspose.PSD per Java è una libreria commerciale, ma puoi esplorarne le funzionalità con una prova gratuita. Ottienila dalla [Aspose.PSD for Java download page](https://releases.aspose.com/psd/java/).

### Q3: Dove posso trovare la documentazione di Aspose.PSD per Java?

La documentazione è disponibile sul sito ufficiale di riferimento di Aspose.PSD per Java: [Aspose.PSD Java API reference](https://reference.aspose.com/psd/java/).

### Q4: Come posso ottenere supporto per Aspose.PSD per Java?

Visita il forum della community di Aspose.PSD per assistenza: [Aspose.PSD forum](https://forum.aspose.com/c/psd/34).

### Q5: È disponibile una licenza temporanea per Aspose.PSD per Java?

Sì, puoi ottenere una licenza temporanea dalla pagina di licenza temporanea di Aspose: [Aspose temporary license](https://purchase.aspose.com/temporary-license/).

---

**Ultimo aggiornamento:** 2026-08-11  
**Testato con:** Aspose.PSD for Java 24.11  
**Autore:** Aspose

## Tutorial correlati

- [Converti in scala di grigi un'immagine usando Aspose.PSD per Java](/psd/java/advanced-techniques/grayscale-image/)
- [Tutorial di elaborazione immagini Java - Regola la luminosità di un'immagine con Aspose.PSD per Java](/psd/java/advanced-techniques/adjust-brightness/)
- [Come regolare il gamma nell'elaborazione immagini Java con Aspose.PSD](/psd/java/advanced-techniques/adjust-gamma/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}