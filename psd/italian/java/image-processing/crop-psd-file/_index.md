---
date: 2026-08-17
description: Scopri come ritagliare file psd in Java con Aspose.PSD per Java – un
  modo rapido e preciso per tagliare documenti Photoshop nelle tue applicazioni Java.
keywords:
- crop psd file java
- aspose.psd java
- java image cropping
lastmod: 2026-08-17
linktitle: Ritaglia file PSD
og_description: Ritaglia file psd in Java usando Aspose.PSD per Java. Questa guida
  ti mostra passo passo come tagliare i file Photoshop in modo efficiente, con spiegazioni
  senza codice e consigli sulle migliori pratiche.
og_image_alt: Guide showing how to crop a PSD file in Java using Aspose.PSD
og_title: Ritaglia file psd in Java con Aspose.PSD – ritaglio rapido di immagini
schemas:
- author: Aspose
  dateModified: '2026-08-17'
  description: Learn how to crop psd file java with Aspose.PSD for Java – a fast,
    precise way to trim Photoshop documents in your Java applications.
  headline: Crop psd file java using Aspose.PSD
  type: TechArticle
- description: Learn how to crop psd file java with Aspose.PSD for Java – a fast,
    precise way to trim Photoshop documents in your Java applications.
  name: Crop psd file java using Aspose.PSD
  steps:
  - name: set document directory
    text: Replace “Your Document Directory” with the absolute or relative path that
      contains the PSD you want to process.
  - name: load PSD file
    text: The `RasterImage` class is Aspose.PSD’s entry point for raster‑based operations
      on a PSD file. Loading the file creates an in‑memory representation that you
      can manipulate.
  - name: define crop area
    text: '`Rectangle` defines the X and Y coordinates together with width and height
      of the region to keep. This class is part of the standard Java AWT package and
      is used by Aspose.PSD to specify cropping bounds.'
  - name: save cropped PSD
    text: After applying the crop, you can persist the result back to PSD format.
      The library writes only the cropped pixels, keeping the original color mode
      and bit depth.
  - name: save cropped image as PNG
    text: If you need a web‑friendly version, export the cropped raster to PNG. Aspose.PSD
      provides PNG save options that let you control compression level and interlacing.
  type: HowTo
- questions:
  - answer: Aspose.PSD for Java.
    question: What library handles PSD cropping in Java?
  - answer: Two API calls after loading the image.
    question: How many lines of code are required for a basic crop?
  - answer: Yes, using the built‑in PNG save options.
    question: Can I export the cropped area as PNG?
  - answer: A commercial license is needed beyond the trial period.
    question: Is a license required for production use?
  - answer: Java 8 and later, including Java 11, 17, and 21.
    question: What Java versions are supported?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- crop psd
- aspose.psd
- java image processing
title: Ritaglia file psd in Java con Aspose.PSD
url: /it/java/image-processing/crop-psd-file/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Ritagliare file PSD Java usando Aspose.PSD

## Introduzione

Se hai bisogno di ritagliare i documenti Photoshop in modo programmatico, **crop psd file java** è un compito comune per gli sviluppatori Java che lavorano con pipeline grafiche, pipeline di asset o flussi di lavoro di design automatizzati. Aspose.PSD per Java fornisce un'API dedicata che ti consente di definire un rettangolo ed estrarre la regione di cui hai bisogno in poche righe di codice. In questo tutorial imparerai perché la libreria è progettata per un ritaglio ad alte prestazioni, come configurare l'ambiente e i passaggi esatti per produrre sia risultati PSD che PNG.

## Risposte rapide
- **Quale libreria gestisce il ritaglio PSD in Java?** Aspose.PSD for Java.
- **Quante righe di codice sono necessarie per un ritaglio di base?** Due chiamate API dopo il caricamento dell'immagine.
- **Posso esportare l'area ritagliata come PNG?** Sì, usando le opzioni di salvataggio PNG integrate.
- **È necessaria una licenza per l'uso in produzione?** È necessaria una licenza commerciale oltre il periodo di prova.
- **Quali versioni di Java sono supportate?** Java 8 e successive, incluse Java 11, 17 e 21.

## Cos'è crop psd file java?

Crop psd file java si riferisce al processo di tagliare programmaticamente una regione rettangolare da un documento Photoshop (.psd) usando codice Java. Con Aspose.PSD è possibile eseguire questa operazione senza avviare Photoshop, rendendola ideale per pipeline di immagini lato server.

## Perché usare Aspose.PSD per Java?

Aspose.PSD supporta **oltre 30 formati di input e output** e può elaborare file PSD fino a **500 MB** senza caricare l'intero documento in memoria, grazie alla sua architettura di streaming. La libreria preserva livelli, maschere e profili colore, fornendo un risultato ritagliato che corrisponde all'output nativo di Photoshop. Questa performance quantificata ti consente di gestire lavori batch su hardware di consumo con un utilizzo di memoria prevedibile.

## Prerequisiti

- **Ambiente di sviluppo Java** – JDK 8 o versioni successive installate e configurate.
- **Aspose.PSD per Java** – scarica l'ultimo JAR e la documentazione [Documentazione di Aspose.PSD per Java](https://reference.aspose.com/psd/java/).
- **File PSD di esempio** – posiziona un file .psd nella directory del tuo progetto in modo che il codice possa individuarlo.

## Come ritagliare un file PSD in Java?

Carica il file sorgente, definisci il rettangolo da conservare, applica il ritaglio e infine salva il risultato nei formati desiderati. L'intero flusso di lavoro richiede solo cinque passaggi semplici, ognuno illustrato con un segnaposto dove inserirai il tuo codice.

### Passo 1: impostare la directory del documento

Sostituisci “Your Document Directory” con il percorso assoluto o relativo che contiene il PSD che desideri elaborare.

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;
import com.aspose.psd.Rectangle;

import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.imageoptions.PngOptions;
import com.aspose.psd.imageoptions.PsdOptions;
import com.aspose.psd.xmp.types.complex.colorant.ColorType;
```

### Passo 2: caricare il file PSD

La classe `RasterImage` è il punto di ingresso di Aspose.PSD per operazioni basate su raster su un file PSD. Il caricamento del file crea una rappresentazione in memoria che puoi manipolare.

```java
String dataDir = "Your Document Directory";
```

### Passo 3: definire l'area di ritaglio

`Rectangle` definisce le coordinate X e Y insieme a larghezza e altezza della regione da conservare. Questa classe fa parte del pacchetto Java AWT standard ed è usata da Aspose.PSD per specificare i limiti del ritaglio.

```java
String sourceFileName = dataDir + "1.psd";
RasterImage image = (RasterImage)Image.load(sourceFileName);
```

### Passo 4: salvare il PSD ritagliato

Dopo aver applicato il ritaglio, puoi persistere il risultato nuovamente in formato PSD. La libreria scrive solo i pixel ritagliati, mantenendo la modalità colore e la profondità di bit originali.

```java
image.crop(new Rectangle(10, 30, 100, 100));
```

### Passo 5: salvare l'immagine ritagliata come PNG

Se ti serve una versione web‑friendly, esporta il raster ritagliato in PNG. Aspose.PSD fornisce opzioni di salvataggio PNG che ti permettono di controllare il livello di compressione e l'interlacciamento.

```java
String exportPathPsd = dataDir + "CropTest.psd";
image.save(exportPathPsd, new PsdOptions());
```

## Problemi comuni e soluzioni

- **Coordinate del rettangolo errate** – Assicurati che i valori X/Y partano da 0 per l'angolo in alto a sinistra; valori negativi genereranno un `ArgumentException`.
- **Picchi di memoria su file di grandi dimensioni** – Usa l'opzione `loadOptions.setLoadOnlyVisibleLayers(true)` per ridurre la memoria quando non sono necessari i livelli nascosti.
- **Perdita del profilo colore** – Conserva il profilo ICC originale chiamando `image.getColorProfile()` prima del ritaglio e riassegnandolo dopo l'operazione.

## Domande frequenti

### Q1: posso usare Aspose.PSD per Java per ritagliare immagini in altri formati?

A1: Aspose.PSD è principalmente orientato ai file PSD, ma supporta anche BMP, GIF, JPEG, PNG, TIFF e diversi altri formati raster sia per l'input che per l'output.

### Q2: Aspose.PSD per Java è adatto per l'elaborazione di immagini su larga scala?

A2: Sì. L'architettura di streaming della libreria elabora file PSD di centinaia di pagine con un consumo di memoria inferiore a 100 MB, rendendola ideale per lavori batch.

### Q3: ci sono considerazioni di licenza per l'uso di Aspose.PSD per Java?

A3: È necessaria una licenza commerciale per le distribuzioni in produzione. I dettagli sono disponibili sulla [pagina di acquisto di Aspose.PSD per Java](https://purchase.aspose.com/buy).

### Q4: come posso ottenere supporto per problemi relativi ad Aspose.PSD per Java?

A4: Visita il [forum di Aspose.PSD per Java](https://forum.aspose.com/c/psd/34) per porre domande, condividere snippet di codice e ricevere aiuto dalla community e dagli ingegneri del prodotto.

### Q5: posso provare Aspose.PSD per Java prima di acquistarlo?

A5: Sì, è possibile scaricare una prova gratuita completamente funzionale [download della prova gratuita di Aspose.PSD](https://releases.aspose.com/).

{{< blocks/products/products-backtop-button >}}

```java
String exportPathPng = dataDir + "CropTest.png";
PngOptions options = new PngOptions();
options.setColorType(PngColorType.TruecolorWithAlpha);
image.save(exportPathPng, options);
```

## Tutorial correlati

- [Ritagliare immagine per rettangolo in Aspose.PSD per Java](/psd/java/image-editing/crop-image-by-rectangle/)
- [Ritagliare immagine per spostamenti in Aspose.PSD per Java](/psd/java/image-editing/crop-image-by-shifts/)
- [Come ruotare un'immagine in Java con Aspose.PSD](/psd/java/advanced-image-manipulation/rotate-image/)

{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}