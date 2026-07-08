---
date: 2026-07-08
description: 'Tutorial della libreria Java per l''editing di immagini: impara come
  ritagliare un''immagine in Java usando Aspose.PSD per Java, ridimensionare, espandere
  la tela e convertire PSD in JPEG.'
keywords:
- java image editing library
- java image processing tutorial
- how to crop image java
lastmod: 2026-07-08
linktitle: Espandi e ritaglia le immagini
og_description: Il tutorial della libreria Java per l'editing di immagini mostra come
  ritagliare, espandere la tela e convertire PSD in JPEG usando Aspose.PSD per Java
  in pochi minuti.
og_image_alt: 'Guide: Crop and expand images in Java with Aspose.PSD'
og_title: Libreria Java per l'editing di immagini – Ritaglia immagine con Aspose.PSD
schemas:
- author: Aspose
  dateModified: '2026-07-08'
  description: 'Java image editing library tutorial: learn how to crop image java
    using Aspose.PSD for Java, resize, expand canvas, and convert PSD to JPEG.'
  headline: Java Image Editing Library – Crop Image with Aspose.PSD
  type: TechArticle
- questions:
  - answer: Aspose.PSD for Java.
    question: What library handles crop image java?
  - answer: A free trial works for testing; a commercial license is required for production.
    question: Do I need a license for development?
  - answer: Yes, using `JpegOptions` together with a cropping rectangle.
    question: Can I convert PSD to JPEG while cropping?
  - answer: Aspose.PSD supports Java 8 and newer versions.
    question: Is Java 8 supported?
  - answer: Typically under 10 minutes for a basic crop operation.
    question: How long does the implementation take?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- java image editing
- Aspose.PSD
- image cropping
- PSD to JPEG
title: Libreria Java per l'editing di immagini – Ritaglia immagine con Aspose.PSD
url: /it/java/image-editing/expand-and-crop-images/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Libreria Java per l'editing di immagini: Ritagliare immagini Java con Aspose.PSD

## Introduzione

In questo tutorial imparerai a usare una **java image editing library**—specificamente Aspose.PSD per Java—per ritagliare, espandere e convertire file PSD in JPEG. Che tu stia preparando risorse per un portale web o automatizzando la generazione di miniature, i passaggi seguenti ti offrono un flusso di lavoro ripetibile e pronto per la produzione che puoi integrare in qualsiasi progetto Java 8+.

## Risposte rapide
- **Quale libreria gestisce il crop image java?** Aspose.PSD for Java.  
- **È necessaria una licenza per lo sviluppo?** Una versione di prova gratuita funziona per i test; è richiesta una licenza commerciale per la produzione.  
- **Posso convertire PSD in JPEG durante il ritaglio?** Sì, usando `JpegOptions` insieme a un rettangolo di ritaglio.  
- **Java 8 è supportato?** Aspose.PSD supporta Java 8 e versioni successive.  
- **Quanto tempo richiede l'implementazione?** Tipicamente meno di 10 minuti per un'operazione di ritaglio di base.

## Cos'è “crop image java”?

Crop image java significa selezionare una regione rettangolare dell'immagine di origine e scartare tutto ciò che si trova al di fuori di quella regione. Con Aspose.PSD, crei un `Rectangle` che definisce l'area, lo applichi a un `RasterImage` e poi salvi il risultato in qualsiasi formato supportato, come JPEG.

## Perché usare Aspose.PSD per il ritaglio di immagini Java?

Aspose.PSD fornisce una **java image editing library** che gestisce i file PSD in modo nativo, supporta oltre 100 funzionalità di livello e può elaborare immagini fino a 10 000 × 10 000 pixel mantenendo l'uso della memoria al di sotto di 500 MB. Offre inoltre la conversione integrata in JPEG, PNG, BMP e altri formati, tutto senza necessità di strumenti esterni. Questo rende le pipeline di elaborazione in batch rapide, affidabili e facili da mantenere.

## Prerequisiti

1. **Java Development Kit (JDK)** – Java 8 o versioni successive installate.  
2. **Aspose.PSD for Java** – scarica la libreria dal sito ufficiale **[qui](https://releases.aspose.com/psd/java/)**.  

> **Consiglio professionale:** aggiungi il JAR di Aspose.PSD al classpath del tuo progetto o alle dipendenze Maven/Gradle per evitare `ClassNotFoundException`.

## Importare i pacchetti

Aggiungi le importazioni necessarie al tuo file sorgente Java. Queste classi ti danno accesso al caricamento delle immagini, alla manipolazione raster, alla definizione del rettangolo e alle opzioni di esportazione JPEG.

## Come ritagliare immagini Java usando Aspose.PSD?

Carica il PSD di origine con `RasterImage`, definisci un `Rectangle` che descrive l'area di ritaglio (coordinate negative possono espandere la tela) e infine salva il risultato con `JpegOptions`. Questo flusso a tre passaggi gestisce sia il ritaglio sia la conversione del formato in un'unica operazione, eliminando la necessità di file intermedi.

## Passo 1: Imposta la directory del documento

Specifica la cartella che contiene il file PSD di origine. Sostituisci il segnaposto con il percorso reale sul tuo computer.

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;
import com.aspose.psd.Rectangle;

import com.aspose.psd.imageoptions.JpegOptions;
```

## Passo 2: Specifica i percorsi di origine e destinazione

Definisci da dove leggere il PSD e dove scrivere il JPEG ritagliato.

```java
String dataDir = "Your Document Directory";
```

## Passo 3: Carica e memorizza nella cache l'immagine

`RasterImage` rappresenta una versione rasterizzata di un file PSD in memoria.  
Carica il PSD in un oggetto `RasterImage`. La memorizzazione nella cache migliora le prestazioni per operazioni successive come il ritaglio.

```java
String sourceFile = dataDir + "example1.psd";
String destName = dataDir + "jpeg_out.jpg";
```

## Passo 4: Crea un rettangolo per il ritaglio

`Rectangle` definisce le coordinate X, Y e la larghezza/altezza della regione di ritaglio.  
Crea un `Rectangle` che descrive la regione che desideri mantenere. Le coordinate possono essere negative per **espandere** la tela prima del ritaglio, il che è utile per aggiungere un bordo attorno all'immagine originale.

```java
RasterImage rasterImage = (RasterImage)Image.load(sourceFile);
rasterImage.cacheData();
```

> **Perché usare coordinate negative?**  
> I valori X/Y negativi spostano l'area di ritaglio a sinistra/alto, aggiungendo effettivamente spazio vuoto (espansione) attorno al contenuto originale prima del ritaglio finale.

## Passo 5: Salva l'immagine ritagliata

`JpegOptions` specifica le impostazioni per l'output JPEG, come qualità e compressione.  
Infine, salva l'immagine risultante usando `JpegOptions`. Questo passo dimostra anche **convert psd jpeg** applicando il rettangolo di ritaglio.

```java
Rectangle destRect = new Rectangle(-200, -200, 300, 300);
```

> **Risultato:** `jpeg_out.jpg` ora contiene un'immagine di 300 × 300 pixel che è stata espansa di 200 px su ogni lato e poi ritagliata al rettangolo definito.

Congratulazioni! Hai eseguito con successo **java image cropping**, espanso la tela e convertito un file PSD in JPEG—tutto in poche righe di codice concise.

## Casi d'uso comuni

- **Preparare risorse per il web** – ritaglia e ridimensiona screenshot o design prima del caricamento.  
- **Generare miniature** – estrai una regione specifica da un grande PSD per scopi di anteprima.  
- **Elaborazione batch automatizzata** – attraversa una cartella di file PSD, applicando lo stesso rettangolo di ritaglio a ciascuno.

## Risoluzione dei problemi e consigli

| Problema | Correzione suggerita |
|----------|----------------------|
| `OutOfMemoryError` durante il caricamento di grandi PSD | Chiama `rasterImage.cacheData()` subito e considera di aumentare la dimensione dell'heap JVM (`-Xmx`). |
| L'area ritagliata è fuori centro | Verifica gli offset X/Y del rettangolo; ricorda che i valori negativi espandono la tela. |
| Il JPEG di output appare sfocato | Regola l'impostazione di qualità di `JpegOptions` (ad esempio, `new JpegOptions { Quality = 90 }`). |

## Domande frequenti

### Q1: Aspose.PSD è compatibile con diverse versioni di Java?

A1: Sì, Aspose.PSD supporta Java 8, 11, 17 e versioni più recenti, garantendo ampia compatibilità con gli ambienti di sviluppo.

### Q2: Posso usare Aspose.PSD per progetti commerciali?

A2: Assolutamente, Aspose.PSD fornisce licenze commerciali per gli sviluppatori, consentendo il suo utilizzo sia in applicazioni personali che commerciali.

### Q3: Ci sono limitazioni sui formati di file immagine supportati?

A3: Aspose.PSD supporta oltre 30 formati di immagine, inclusi PSD, JPEG, PNG, BMP, TIFF e altri. Consulta la [documentazione](https://reference.aspose.com/psd/java/) per l'elenco completo.

### Q4: Come posso ottenere supporto per le domande relative ad Aspose.PSD?

A4: Visita il [forum Aspose.PSD](https://forum.aspose.com/c/psd/34) per chiedere assistenza alla community o al team di supporto Aspose.

### Q5: È disponibile una versione di prova gratuita?

A5: Sì, puoi provare Aspose.PSD con una versione di prova gratuita. Scaricala [qui](https://releases.aspose.com/).

**Ultimo aggiornamento:** 2026-07-08  
**Testato con:** Aspose.PSD for Java 24.12  
**Autore:** Aspose  

{{< blocks/products/products-backtop-button >}}

```java
rasterImage.save(destName, new JpegOptions(), destRect);
```

## Tutorial correlati

- [Ridimensionamento semplice con Aspose.PSD – Libreria Java per la manipolazione di immagini](/psd/java/basic-image-operations/simple-resizing/)
- [Come ruotare l'immagine di 270 gradi con Aspose.PSD per Java](/psd/java/advanced-image-manipulation/rotate-image/)
- [Come regolare il gamma nella elaborazione di immagini Java con Aspose.PSD](/psd/java/advanced-techniques/adjust-gamma/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}