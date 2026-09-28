---
date: 2026-09-28
description: Il tutorial di elaborazione immagini Java mostra come regolare la luminosità
  di un'immagine usando Aspose.PSD per Java. Segui il codice passo‑a‑passo per caricare,
  modificare e salvare file PSD o TIFF.
keywords:
- java image processing
- aspose psd java
- java image manipulation
- adjust brightness java
lastmod: 2026-09-28
linktitle: Regola la luminosità di un'immagine
og_description: Il tutorial di elaborazione immagini Java mostra come regolare la
  luminosità di un'immagine usando Aspose.PSD per Java. Segui il codice passo‑a‑passo
  per caricare, modificare e salvare file PSD o TIFF.
og_image_alt: Guide to adjusting image brightness in Java using Aspose.PSD
og_title: 'Elaborazione immagini Java: regola la luminosità con Aspose.PSD'
schemas:
- author: Aspose
  dateModified: '2026-09-28'
  description: Java image processing tutorial shows how to adjust brightness of an
    image using Aspose.PSD for Java. Follow step‑by‑step code to load, modify, and
    save PSD or TIFF files.
  headline: 'Java image processing: adjust brightness with Aspose.PSD'
  type: TechArticle
- description: Java image processing tutorial shows how to adjust brightness of an
    image using Aspose.PSD for Java. Follow step‑by‑step code to load, modify, and
    save PSD or TIFF files.
  name: 'Java image processing: adjust brightness with Aspose.PSD'
  steps:
  - name: Load the image
    text: The `RasterImage` class represents a rasterized version of a PSD or TIFF
      file in memory. It provides direct pixel access for color‑correction operations.
      In this step, we load the target image and cast it to a `RasterImage` for further
      processing.
  - name: Adjust brightness
    text: '`adjustBrightness(int value)` changes the lightness of every pixel by the
      specified integer value. Positive numbers brighten the image; negative numbers
      darken it. The method processes the image in‑place, so no additional object
      creation is required. Here, we use the `adjustBrightness` method to mod'
  - name: Set TiffOptions
    text: '`TiffOptions` specifies the encoding parameters for TIFF output, such as
      bits per sample and photometric interpretation. It lets you control how the
      resulting file is encoded. Configure the `TiffOptions` for saving the adjusted
      image. Adjust the `bitsPerSample` and `photometric` properties based on '
  - name: Save the resultant image
    text: Calling `save` writes the processed raster data to a file using the previously
      defined options. The operation is atomic and guarantees that the output file
      is a valid TIFF image. Finally, save the modified image using the specified
      `TiffOptions`.
  type: HowTo
- questions:
  - answer: Yes, Aspose.PSD for Java supports JPEG, PNG, BMP, GIF, and many other
      raster formats in addition to PSD and TIFF.
    question: Can I adjust brightness in other image formats besides PSD?
  - answer: Wrap the processing code in a try‑catch block and catch `IOException`
      or `ImageProcessingException` to manage file‑access and raster‑operation errors.
    question: How can I handle errors during the image adjustment process?
  - answer: The method accepts integer values from –255 to +255; values outside this
      range are clamped to the nearest limit.
    question: Is there a limit to the range of brightness adjustment?
  - answer: Yes, a commercial license is required for production use. Purchase a license
      [here](https://purchase.aspose.com/buy).
    question: Can I use Aspose.PSD for Java in commercial projects?
  - answer: Yes, you can explore the library with a free trial from [here](https://releases.aspose.com/).
    question: Is there a free trial available?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- java image processing
- aspose psd
- java image manipulation
title: 'Elaborazione immagini Java: regola la luminosità con Aspose.PSD'
url: /it/java/advanced-techniques/adjust-brightness/
weight: 21
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Regola la luminosità di un'immagine con Aspose.PSD per Java

## Introduzione

In questo tutorial di **java image processing** imparerai come regolare la luminosità di un'immagine direttamente dal codice Java. La regolazione della luminosità è un compito frequente per grafici, fotografi e chiunque costruisca pipeline di elaborazione immagini. In questa guida di **java image manipulation** percorreremo l'intero flusso di lavoro—caricamento di un PSD/TIFF, applicazione di un offset di luminosità e salvataggio del risultato—utilizzando la libreria Aspose.PSD per Java.

## Risposte rapide
- **Quale libreria gestisce la luminosità?** Aspose.PSD for Java.  
- **Quale metodo modifica la luminosità?** `RasterImage.adjustBrightness()`.  
- **Posso lavorare con file PSD e TIFF?** Sì, l'API supporta entrambi i formati e oltre 10 tipi di immagine aggiuntivi.  
- **È necessaria una licenza per la produzione?** È richiesta una licenza commerciale per l'uso non‑valutativo.  
- **Quanto tempo richiede l'implementazione?** Tipicamente meno di 10 minuti per una regolazione di base.

## Che cos'è java image processing?
`Java image processing` si riferisce all'insieme di tecniche che consentono di leggere, trasformare e scrivere dati immagine programmaticamente usando Java. Regolare la luminosità è una delle operazioni fondamentali che modifica la chiarezza complessiva di ogni pixel, rendendo le aree scure più chiare o le aree luminose più scure.

## Perché usare Aspose.PSD per Java?
Aspose.PSD per Java fornisce una soluzione completa, pure‑Java, che supporta un'ampia gamma di formati raster e vettoriali, elimina le dipendenze native e offre una cache ad alte prestazioni per file di grandi dimensioni. La sua API estesa consente agli sviluppatori di eseguire correzioni di colore complesse e modifiche basate su livelli con poco codice, rendendola ideale sia per semplici aggiustamenti sia per pipeline di elaborazione immagini avanzate.

- **Supporta più di 10 formati raster e vettoriali** – PSD, TIFF, JPEG, PNG, BMP, GIF e altri.  
- **Implementazione Pure‑Java** – nessun DLL nativo o dipendenze esterne, quindi funziona su qualsiasi JVM.  
- **Cache ad alte prestazioni** – i dati raster possono essere memorizzati nella cache, consentendo modifiche ripetute fino a 2× più veloci su file di grandi dimensioni.  
- **Ampia superficie API** – oltre 150 metodi per correzione del colore, gestione dei livelli, maschere e compositing.

## Prerequisiti

Prima di immergerti nel tutorial, assicurati di avere i seguenti prerequisiti:

- Libreria Aspose.PSD per Java: scarica e installa la libreria dalla [documentazione Aspose.PSD for Java](https://reference.aspose.com/psd/java/).  
- Java Development Kit (JDK) 8 o superiore installato sul tuo computer.  
- Un ambiente di sviluppo (IDE) come IntelliJ IDEA, Eclipse o VS Code.

## Importa i pacchetti

Per iniziare, importa i pacchetti necessari nel tuo progetto Java. In questo esempio, utilizzeremo i seguenti:

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.psd.fileformats.tiff.enums.TiffPhotometrics;
import com.aspose.psd.imageoptions.TiffOptions;
```

Ora, suddividiamo il processo di regolazione della luminosità di un'immagine in passaggi semplici:

## Come regolare la luminosità usando Aspose.PSD?

Carica l'immagine sorgente, applica un offset di luminosità, configura le opzioni di salvataggio e scrivi il risultato su disco—tutto in quattro passaggi concisi. Le sezioni seguenti forniscono una guida chiara, passo‑per‑passo, che puoi copiare nel tuo progetto. Questo approccio garantisce che ogni operazione sia eseguita in modo efficiente e che l'immagine finale mantenga la qualità originale riflettendo la modifica di luminosità desiderata.

### Passo 1: Carica l'immagine

La classe `RasterImage` rappresenta una versione rasterizzata di un file PSD o TIFF in memoria. Fornisce accesso diretto ai pixel per operazioni di correzione colore.

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";
String destName = dataDir + "AdjustBrightness_out.tiff";

// Load an existing image into an instance of RasterImage class
Image image = Image.load(sourceFile);
// Cast object of Image to RasterImage
RasterImage rasterImage = (RasterImage) image;

// Check if RasterImage is cached and Cache RasterImage for better performance
if (!rasterImage.isCached()) {
    rasterImage.cacheData();
}
```

In questo passaggio, carichiamo l'immagine di destinazione e la convertiamo in un `RasterImage` per ulteriori elaborazioni.

### Passo 2: Regola la luminosità

`adjustBrightness(int value)` cambia la chiarezza di ogni pixel del valore intero specificato. I numeri positivi schiariscono l'immagine; i numeri negativi la scuriscono. Il metodo elabora l'immagine in‑place, quindi non è necessaria la creazione di oggetti aggiuntivi.

```java
// Adjust the brightness
rasterImage.adjustBrightness(-50);
```

Qui utilizziamo il metodo `adjustBrightness` per modificare la luminosità dell'immagine. In questo esempio diminuiamo la luminosità di 50 unità, ma puoi personalizzare il valore in base alle tue esigenze.

### Passo 3: Imposta TiffOptions

`TiffOptions` specifica i parametri di codifica per l'output TIFF, come i bit per campione e l'interpretazione fotometrica. Ti consente di controllare come viene codificato il file risultante.

```java
int[] ushort = {8, 8, 8};
// Create an instance of TiffOptions for the resultant image
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
tiffOptions.setBitsPerSample(ushort);
tiffOptions.setPhotometric(TiffPhotometrics.Rgb);
```

Configura le `TiffOptions` per salvare l'immagine regolata. Regola le proprietà `bitsPerSample` e `photometric` in base alle tue necessità specifiche.

### Passo 4: Salva l'immagine risultante

Chiamare `save` scrive i dati raster elaborati su un file utilizzando le opzioni precedentemente definite. L'operazione è atomica e garantisce che il file di output sia un TIFF valido.

```java
// Save the resultant image
rasterImage.save(destName, tiffOptions);
```

Infine, salva l'immagine modificata usando le `TiffOptions` specificate.

## Problemi comuni e soluzioni

| Problema | Motivo | Soluzione |
|----------|--------|-----------|
| **`ClassCastException` durante il cast di Image** | Il file non è un'immagine raster (ad es., un PSD vettoriale). | Verifica il formato del file sorgente o usa `image instanceof RasterImage` prima del cast. |
| **La modifica della luminosità non ha effetto** | L'immagine non è stata memorizzata nella cache prima della regolazione. | Chiama `rasterImage.cacheData()` come mostrato nel Passo 1. |
| **Il file salvato appare corrotto** | Configurazione errata di `TiffOptions`. | Assicurati che `bitsPerSample` corrisponda alla profondità dell'immagine sorgente (solitamente 8‑bit per canale). |

## Domande frequenti

**D: Posso regolare la luminosità in altri formati immagine oltre a PSD?**  
R: Sì, Aspose.PSD per Java supporta JPEG, PNG, BMP, GIF e molti altri formati raster oltre a PSD e TIFF.

**D: Come posso gestire gli errori durante il processo di regolazione dell'immagine?**  
R: Avvolgi il codice di elaborazione in un blocco try‑catch e cattura `IOException` o `ImageProcessingException` per gestire errori di accesso al file e operazioni raster.

**D: Esiste un limite all'intervallo di regolazione della luminosità?**  
R: Il metodo accetta valori interi da –255 a +255; valori al di fuori di questo intervallo vengono limitati al valore più vicino.

**D: Posso usare Aspose.PSD per Java in progetti commerciali?**  
R: Sì, è necessaria una licenza commerciale per l'uso in produzione. Acquista una licenza [qui](https://purchase.aspose.com/buy).

**D: È disponibile una versione di prova gratuita?**  
R: Sì, puoi esplorare la libreria con una prova gratuita [qui](https://releases.aspose.com/).

**D: Il metodo `adjustBrightness` influisce sulla visibilità dei livelli?**  
R: Il metodo opera sull'immagine rasterizzata composita, quindi i livelli nascosti vengono ignorati durante la rasterizzazione, preservando il risultato visivo previsto.

**D: Posso concatenare più regolazioni (ad es., contrasto, saturazione) insieme?**  
R: Assolutamente. Dopo aver regolato la luminosità, puoi chiamare `adjustContrast`, `adjustSaturation` o altri metodi di correzione colore sulla stessa istanza di `RasterImage`.

**Ultimo aggiornamento:** 2026-09-28  
**Testato con:** Aspose.PSD for Java 24.12 (latest at time of writing)  
**Autore:** Aspose

## Tutorial correlati

- [Libreria di elaborazione immagini Java: Inverti livello usando Aspose.PSD](/psd/java/advanced-image-manipulation/invert-adjustment-layer/)
- [Converti immagine in scala di grigi usando Aspose.PSD per Java](/psd/java/advanced-techniques/grayscale-image/)
- [Come ruotare un'immagine di un angolo specifico con Aspose.PSD per Java](/psd/java/advanced-image-manipulation/rotate-image-specific-angle/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}