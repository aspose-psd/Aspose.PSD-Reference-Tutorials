---
date: 2026-06-03
description: Scopri come ridimensionare le immagini con Aspose.PSD for Java. Questa
  guida passo‑passo copre Resize Type Enumeration, il ridimensionamento di immagini
  ad alta qualità e come convertire PSD in JPEG.
keywords:
- how to resize image
- convert psd to jpeg
- high quality image resize
- resize image java
- java image manipulation tutorial
linktitle: Ridimensionamento con Resize Type Enumeration
schemas:
- author: Aspose
  dateModified: '2026-06-03'
  description: Learn how to resize image with Aspose.PSD for Java. This step‑by‑step
    guide covers the Resize Type Enumeration, high‑quality image resize, and how to
    convert PSD to JPEG.
  headline: How to Resize Image Java Using Resize Type Enumeration
  type: TechArticle
- description: Learn how to resize image with Aspose.PSD for Java. This step‑by‑step
    guide covers the Resize Type Enumeration, high‑quality image resize, and how to
    convert PSD to JPEG.
  name: How to Resize Image Java Using Resize Type Enumeration
  steps:
  - name: '**Java Development Environment** – JDK 8 or newer installed and configured.'
    text: '**Java Development Environment** – JDK 8 or newer installed and configured.'
  - name: '**Aspose.PSD Library** – Download the latest JAR from the [website](https://releases.aspose.com/psd/java/).'
    text: '**Aspose.PSD Library** – Download the latest JAR from the [website](https://releases.aspose.com/psd/java/).'
  - name: '**Sample PSD File** – Use the [sample.psd](Your Document Directory/sample.psd)
      file included with the SDK for hands‑on testing.'
    text: '**Sample PSD File** – Use the [sample.psd](Your Document Directory/sample.psd)
      file included with the SDK for hands‑on testing.'
  type: HowTo
- questions:
  - answer: Load the PSD with `Image.load`, then call `image.save("output.jpg", new
      JpegOptions());`.
    question: How do I programmatically convert a PSD file to JPEG without resizing?
  - answer: Yes, you can set the `Resolution` property on the `Image` object before
      saving.
    question: Is it possible to maintain the original DPI when resizing?
  - answer: While you can call `resize` multiple times, it’s more efficient to calculate
      the final dimensions and resize once.
    question: Can I chain multiple resize operations?
  type: FAQPage
second_title: Aspose.PSD Java API
title: Come ridimensionare un'immagine Java usando Resize Type Enumeration
url: /it/java/advanced-image-manipulation/resizing-with-resize-type-enumeration/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Come ridimensionare un'immagine Java usando l'enumerazione Resize Type

## Introduzione

Se stai cercando **come ridimensionare un'immagine** in modo efficiente in un progetto Java, Aspose.PSD for Java offre un'API pulita e ad alte prestazioni. In questo tutorial vedremo come caricare un PSD, applicare la **Resize Type Enumeration** per un ridimensionamento di alta qualità e infine **convert PSD to JPEG**. Che tu stia costruendo un editor desktop o una pipeline automatizzata lato server, questi passaggi ti consentono di controllare dimensioni, qualità e formato con poche righe di codice.

## Risposte rapide
- **Quale libreria gestisce il ridimensionamento delle immagini Java?** Aspose.PSD for Java.
- **Quale tipo di ridimensionamento offre la migliore qualità?** `ResizeType.LanczosResample`.
- **Posso convertire PSD in JPEG dopo il ridimensionamento?** Sì – basta salvare con `JpegOptions`.
- **È necessaria una licenza per la produzione?** È necessaria una licenza valida di Aspose.PSD per l'uso in produzione.
- **Questo approccio è adatto a grandi batch?** Assolutamente; l'API elabora file con centinaia di pagine senza caricare l'intero documento in memoria.

## Cos'è "come ridimensionare un'immagine" in Java?

**Come ridimensionare un'immagine** si riferisce al cambiare programmaticamente le dimensioni in pixel di un'immagine mantenendo la fedeltà visiva. Il metodo `Resize` di Aspose.PSD combinato con l'enumerazione `ResizeType` offre un controllo preciso sugli algoritmi di scaling, consentendo agli sviluppatori di mantenere la qualità su un'ampia gamma di file sorgente e dimensioni di destinazione.

## Perché usare l'enumerazione Resize Type?

`ResizeType` ti consente di selezionare l'algoritmo di ricampionamento che meglio bilancia velocità e qualità visiva. Nella maggior parte degli scenari, **LanczosResample** fornisce risultati nitidi con un modesto costo di prestazioni, elaborando un'immagine 2000 × 1500 in meno di 120 ms su una tipica CPU da server mantenendo intatti i dettagli dei bordi.

## Prerequisiti

Prima di iniziare, assicurati di avere:

1. **Ambiente di sviluppo Java** – JDK 8 o versioni successive installate e configurate.  
2. **Libreria Aspose.PSD** – Scarica l'ultimo JAR dal [sito web](https://releases.aspose.com/psd/java/).  
3. **File PSD di esempio** – Usa il file [sample.psd](Your Document Directory/sample.psd) incluso con l'SDK per test pratici.

## Importare i pacchetti

`Image` è la classe base per tutti i tipi di immagine in Aspose.PSD. Aggiungi gli import necessari al tuo file sorgente Java:

```java
import com.aspose.psd.Image;
import com.aspose.psd.ResizeType;

import com.aspose.psd.imageoptions.JpegOptions;
```

## Passo 1: Caricare l'immagine

### Anchor di definizione
La classe `RasterImage` è l'oggetto principale di Aspose.PSD che rappresenta un'immagine raster caricata da un file PSD.

Carica il tuo PSD in un'istanza `RasterImage` così da poter manipolare i suoi pixel:

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

// Load an existing image into an instance of RasterImage class
Image image = Image.load(sourceFile);
```

## Passo 2: Ridimensionare l'immagine

`image.resize(width, height, resizeType)` ridimensiona l'immagine alle dimensioni specificate usando l'algoritmo scelto.

Ora ridimensiona l'immagine caricata usando la **Resize Type Enumeration**. In questo esempio utilizziamo il metodo Lanczos Resample, ideale quando **come ridimensionare un'immagine** con alta qualità:

```java
image.resize(300, 300, ResizeType.LanczosResample);
```

## Passo 3: Salvare l'immagine ridimensionata

`image.save(path, options)` scrive l'immagine su disco nel formato definito dalle opzioni fornite.

Dopo il ridimensionamento, salva l'immagine con le dimensioni specificate e il tipo di ridimensionamento scelto. Qui, dimostriamo anche **convert psd to jpeg** salvando il risultato come file JPEG:

```java
String destName = dataDir + "ResizingwithResizeTypeEnumeration_out.jpg";
image.save(destName, new JpegOptions());
```

## Perché usare l'enumerazione Resize Type?

`ResizeType` ti offre un controllo dettagliato sull'algoritmo di ricampionamento, permettendoti di bilanciare velocità e qualità. Nella maggior parte delle applicazioni, `LanczosResample` offre un ottimo compromesso, fornendo risultati nitidi senza un pesante impatto sulle prestazioni, e funziona bene su una varietà di contenuti immagine.

## Problemi comuni e soluzioni

- **L'immagine appare sfocata dopo il ridimensionamento** – Prova un `ResizeType` diverso come `Bicubic` o `NearestNeighbour` per vedere quale fornisce il miglior risultato visivo per la tua immagine specifica.  
- **OutOfMemoryError su file PSD di grandi dimensioni** – Elabora l'immagine in blocchi più piccoli o aumenta la dimensione dell'heap JVM (flag `-Xmx`). Aspose.PSD può gestire file fino a **2 GB** senza caricare l'intero documento in memoria.

## FAQ

### Q1: Aspose.PSD per Java è adatto sia a progetti piccoli che su larga scala?

A1: Assolutamente! Aspose.PSD per Java è progettato per soddisfare progetti di tutte le dimensioni, offrendo scalabilità ed efficienza.

### Q2: Posso usare un tipo di ridimensionamento diverso da Lanczos Resample?

A2: Sì, Aspose.PSD per Java offre vari tipi di ridimensionamento, come **NearestNeighbour**, **Bicubic** e altri. Consulta la documentazione API per l'elenco completo.

### Q3: Dove posso trovare supporto aggiuntivo per Aspose.PSD per Java?

A3: Per qualsiasi domanda o assistenza, visita il [forum Aspose.PSD](https://forum.aspose.com/c/psd/34).

### Q4: È disponibile una versione di prova gratuita per Aspose.PSD per Java?

A4: Sì, puoi accedere a una versione di prova gratuita [qui](https://releases.aspose.com/).

### Q5: Come posso ottenere una licenza temporanea per Aspose.PSD per Java?

A5: Per ottenere una licenza temporanea, visita [questo link](https://purchase.aspose.com/temporary-license/).

## Domande frequenti

**D: Come posso convertire programmaticamente un file PSD in JPEG senza ridimensionare?**  
R: Carica il PSD con `Image.load`, poi chiama `image.save("output.jpg", new JpegOptions());`.

**D: È possibile mantenere il DPI originale durante il ridimensionamento?**  
R: Sì, puoi impostare la proprietà `Resolution` sull'oggetto `Image` prima di salvare.

**D: Posso concatenare più operazioni di ridimensionamento?**  
R: Sebbene tu possa chiamare `resize` più volte, è più efficiente calcolare le dimensioni finali e ridimensionare una sola volta.

---

**Ultimo aggiornamento:** 2026-06-03  
**Testato con:** Aspose.PSD for Java 24.12  
**Autore:** Aspose  

{{< blocks/products/products-backtop-button >}}

## Tutorial correlati

- [Ridimensionamento semplice con Aspose.PSD – Libreria di manipolazione immagini Java](/psd/java/basic-image-operations/simple-resizing/)
- [Scaling di immagini ad alta qualità con Bicubic Resampler in Aspose.PSD per Java](/psd/java/advanced-image-manipulation/implement-bicubic-resampler/)
- [Come convertire PSD in PNG e ridimensionare proporzionalmente con Aspose.PSD per Java](/psd/java/advanced-image-manipulation/resize-image-proportionally/)

{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}