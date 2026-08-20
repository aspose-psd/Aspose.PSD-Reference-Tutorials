---
date: 2026-05-19
description: Scopri come convertire PSD in JPEG e ruotare l'immagine di 270 gradi
  usando Aspose.PSD per Java. Questa guida mostra come ruotare i file PSD, capovolgere
  le immagini e convertire PSD in JPEG.
keywords:
- convert psd to jpeg
- how to rotate psd
- flip image java
- rotate psd layer
- rotate image without photoshop
linktitle: Ruota immagine di 270 gradi
schemas:
- author: Aspose
  dateModified: '2026-05-19'
  description: Learn how to convert PSD to JPEG and rotate image 270 degrees using
    Aspose.PSD for Java. This guide shows how to rotate PSD files, flip images, and
    convert PSD to JPEG.
  headline: Convert PSD to JPEG & Rotate 270° with Aspose.PSD for Java
  type: TechArticle
- description: Learn how to convert PSD to JPEG and rotate image 270 degrees using
    Aspose.PSD for Java. This guide shows how to rotate PSD files, flip images, and
    convert PSD to JPEG.
  name: Convert PSD to JPEG & Rotate 270° with Aspose.PSD for Java
  steps:
  - name: Load the PSD File
    text: '`Image` is Aspose.PSD''s core class that represents a single PSD document
      in memory. Instantiating it reads only the header information, keeping memory
      usage low.'
  - name: Rotate the Image 270 Degrees
    text: '`rotateFlip` performs the specified rotation and optional flip on the image.
      `RotateFlipType.Rotate270FlipNone` rotates the canvas 270 degrees clockwise
      while leaving the image orientation unchanged. > **Pro tip:** If you also need
      to flip the image horizontally or vertically, choose a different `Ro'
  - name: Convert PSD to JPEG and Save
    text: '`JpegOptions` defines JPEG‑specific parameters such as compression quality.
      The `save` method writes the transformed image to disk in the desired format.
      The file `RotatedImage_out.jpg` now contains the original PSD content rotated
      270 degrees and saved as a JPEG.'
  type: HowTo
- questions:
  - answer: Yes, Aspose.PSD supports PSD, JPEG, PNG, BMP, GIF, TIFF, and many other
      raster formats.
    question: Is Aspose.PSD compatible with different image formats?
  - answer: Absolutely! While `RotateFlipType` provides common angles, you can chain
      multiple calls or use transformation matrices for arbitrary angles.
    question: Can I apply custom rotations, not just predefined flips?
  - answer: Replace `JpegOptions` with `PngOptions` (or the appropriate options class)
      in the `save` method.
    question: How do I convert the rotated PSD to another format, such as PNG?
  - answer: For community help, visit the [Aspose.PSD Forum](https://forum.aspose.com/c/psd/34).
    question: Where can I find additional support or assistance?
  - answer: Yes, you can explore Aspose.PSD with a [free trial](https://releases.aspose.com/).
    question: Is there a free trial available?
  type: FAQPage
second_title: Aspose.PSD Java API
title: Converti PSD in JPEG e ruota di 270° con Aspose.PSD per Java
url: /it/java/advanced-image-manipulation/rotate-image/
weight: 19
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Converti PSD in JPEG e ruota l'immagine di 270 gradi con Aspose.PSD per Java

## Introduzione

In questo **tutorial di elaborazione immagini Java**, imparerai a **convertire PSD in JPEG** ruotando l'immagine di 270 gradi usando Aspose.PSD per Java. Che tu stia costruendo una pipeline di elaborazione batch, un editor basato sul web o un'utilità desktop, la libreria ti consente di manipolare i livelli PSD senza Photoshop. Tratteremo anche il capovolgimento opzionale e mostreremo l'intero flusso end‑to‑end dal caricamento di un file PSD al salvataggio di un JPEG.

## Risposte rapide
- **Quale libreria gestisce la rotazione?** Aspose.PSD per Java  
- **Quale angolo di rotazione usa l'esempio?** 270 gradi  
- **Posso anche capovolgere l'immagine?** Sì – usa le opzioni `RotateFlipType` come `Rotate90FlipX`  
- **Come salvo il risultato?** Nell'esempio salviamo come JPEG usando `JpegOptions`  
- **È necessaria una licenza per la produzione?** È richiesta una licenza valida di Aspose.PSD per uso commerciale  

## Cos'è “ruotare l'immagine di 270 gradi”?
Ruotare un'immagine di 270 gradi significa girare la foto di tre quarti di giro in senso orario (o 90 gradi in senso antiorario). Questa orientazione ripristina spesso il layout originale in verticale dopo trasformazioni precedenti ed è comunemente usata quando le immagini sono state acquisite in modalità orizzontale ma devono essere visualizzate in verticale. Il risultato è un'immagine correttamente orientata senza perdita di qualità.

## Perché usare Aspose.PSD per questo compito?
Aspose.PSD supporta **oltre 50 formati di input e output**—inclusi PSD, JPEG, PNG, BMP, GIF e TIFF—e può elaborare file fino a **2 GB** senza caricare l'intero documento in memoria. L'API funziona su qualsiasi runtime Java (JDK 8+), non richiede l'installazione di Photoshop e fornisce una singola chiamata `rotateFlip` che gestisce sia rotazione sia capovolgimento in un unico passaggio.

## Prerequisiti

Prima di iniziare, assicurati di avere:

- **Libreria Aspose.PSD per Java** installata. Puoi scaricarla e visualizzare la documentazione completa dell'API [qui](https://reference.aspose.com/psd/java/).  
- Un ambiente di sviluppo Java (JDK 8 o superiore).  
- Un file PSD di esempio che desideri ruotare. Aggiorna la variabile `sourceFile` nel codice con il percorso corretto del tuo file.

## Importa i pacchetti

Le classi `Image`, `RotateFlipType` e `JpegOptions` sono necessarie per caricare, trasformare e salvare il file.  
`Image` è la classe principale che rappresenta un documento PSD in memoria.  
`RotateFlipType` enumera le operazioni di rotazione e capovolgimento supportate.  
`JpegOptions` configura le impostazioni di output JPEG come la qualità.  

```java
import com.aspose.psd.Image;
import com.aspose.psd.RotateFlipType;

import com.aspose.psd.imageoptions.JpegOptions;
```

## Come convertire PSD in JPEG dopo la rotazione?

Carica il PSD di origine, applica una rotazione di 270 gradi e salvalo immediatamente come JPEG. Questo flusso a tre passaggi viene eseguito in meno di un secondo per immagini tipiche da 10 MP su una CPU moderna, rendendolo ideale per lavori batch ad alta velocità. Elaborando solo i dati immagine necessari, il consumo di memoria rimane basso e il JPEG risultante mantiene la fedeltà visiva riducendo le dimensioni del file.

### Passo 1: Carica il file PSD

`Image` è la classe principale di Aspose.PSD che rappresenta un singolo documento PSD in memoria. L'istanza legge solo le informazioni di intestazione, mantenendo basso l'uso di memoria.

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";
Image image = Image.load(sourceFile);
```

### Passo 2: Ruota l'immagine di 270 gradi

`rotateFlip` esegue la rotazione specificata e, opzionalmente, il capovolgimento sull'immagine. `RotateFlipType.Rotate270FlipNone` ruota la tela di 270 gradi in senso orario lasciando invariata l'orientazione dell'immagine.

```java
image.rotateFlip(RotateFlipType.Rotate270FlipNone);
```

> **Suggerimento:** Se hai bisogno di capovolgere anche l'immagine orizzontalmente o verticalmente, scegli un `RotateFlipType` diverso, come `Rotate90FlipX` o `Rotate180FlipY`.

### Passo 3: Converti PSD in JPEG e salva

`JpegOptions` definisce i parametri specifici per JPEG, come la qualità di compressione. Il metodo `save` scrive l'immagine trasformata su disco nel formato desiderato.

```java
String destName = dataDir + "RotatedImage_out.jpg";
image.save(destName, new JpegOptions());
```

Il file `RotatedImage_out.jpg` ora contiene il contenuto originale del PSD ruotato di 270 gradi e salvato come JPEG.

## Problemi comuni e soluzioni

| Problema | Soluzione |
|----------|-----------|
| **L'immagine appare capovolta** | Verifica di aver usato `Rotate270FlipNone`. Per una rotazione di 90 gradi in senso orario usa `Rotate90FlipNone`. |
| **Il file di output è corrotto** | Assicurati che la cartella di destinazione esista e che tu abbia i permessi di scrittura. |
| **Eccezione di licenza** | Installa una licenza temporanea o permanente di Aspose.PSD prima di caricare l'immagine in produzione. |

## Domande frequenti

**D: È Aspose.PSD compatibile con diversi formati immagine?**  
R: Sì, Aspose.PSD supporta PSD, JPEG, PNG, BMP, GIF, TIFF e molti altri formati raster.

**D: Posso applicare rotazioni personalizzate, non solo capovolgimenti predefiniti?**  
R: Assolutamente! Sebbene `RotateFlipType` fornisca gli angoli più comuni, puoi concatenare più chiamate o usare matrici di trasformazione per angoli arbitrari.

**D: Come converto il PSD ruotato in un altro formato, ad esempio PNG?**  
R: Sostituisci `JpegOptions` con `PngOptions` (o la classe di opzioni appropriata) nel metodo `save`.

**D: Dove posso trovare supporto o assistenza aggiuntivi?**  
R: Per aiuto della community, visita il [Forum Aspose.PSD](https://forum.aspose.com/c/psd/34).

**D: È disponibile una versione di prova gratuita?**  
R: Sì, puoi provare Aspose.PSD con una [versione di prova gratuita](https://releases.aspose.com/).

**D: Come ottengo una licenza temporanea?**  
R: Se ti serve una licenza temporanea, puoi ottenerla [qui](https://purchase.aspose.com/temporary-license/).

**Ultimo aggiornamento:** 2026-05-19  
**Testato con:** Aspose.PSD per Java 24.12  
**Autore:** Aspose  

{{< blocks/products/products-backtop-button >}}

## Tutorial correlati

- [Converti PSD in formati immagine raster con Aspose.PSD per Java](/psd/java/advanced-techniques/convert-psd-to-raster-formats/)
- [Converti PSD in PNG e ruota i livelli nei file PSD usando Java](/psd/java/advanced-psd-layer-features-effects/rotate-layers-psd-files/)
- [Come ruotare un'immagine in Java con Aspose.PSD](/psd/java/advanced-image-manipulation/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}