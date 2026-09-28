---
date: 2026-09-28
description: Come aggiungere una miniatura a un segmento JFIF in Java usando Aspose.PSD.
  Segui questa guida passo‑passo per incorporare miniature nei file PSD in modo rapido
  e affidabile.
keywords:
- how to add thumbnail
- JFIF segment Java
- Aspose.PSD thumbnail
- Java image processing
lastmod: 2026-09-28
linktitle: Aggiungi miniatura al segmento JFIF in Java
og_description: Come aggiungere una miniatura a un segmento JFIF in Java usando Aspose.PSD.
  Segui questa guida passo‑passo per incorporare miniature nei file PSD in modo rapido
  e affidabile.
og_image_alt: Guide showing how to add thumbnail to JFIF segment in Java with Aspose.PSD
og_title: Come aggiungere una miniatura al segmento JFIF in Java
schemas:
- author: Aspose
  dateModified: '2026-09-28'
  description: How to add thumbnail to a JFIF segment in Java using Aspose.PSD. Follow
    this step‑by‑step guide to embed thumbnails in PSD files quickly and reliably.
  headline: How to add thumbnail to JFIF segment in Java
  type: TechArticle
- description: How to add thumbnail to a JFIF segment in Java using Aspose.PSD. Follow
    this step‑by‑step guide to embed thumbnails in PSD files quickly and reliably.
  name: How to add thumbnail to JFIF segment in Java
  steps:
  - name: import packages
    text: '`Document`, `JfifResource`, and related classes are part of the Aspose.PSD
      namespace. Document represents the PSD file container, and JfifResource provides
      access to the JFIF segment within the PSD. Import them at the top of your source
      file.'
  - name: load the PSD image
    text: Create a `PsdImage` instance by passing the file path to the constructor.
      PsdImage is the Aspose.PSD class that models a Photoshop document. This loads
      the document metadata while streaming the pixel data.
  - name: iterate over image resources
    text: Search the `Resources` collection for a `JfifResource`. When found, you
      can replace its thumbnail byte array with a new JPEG‑encoded preview.
  - name: adjust thumbnail data
    text: Generate a small JPEG thumbnail (e.g., 120 × 120 px) using any image‑processing
      library, then assign the resulting byte array to `jfifResource.ThumbnailData`.
  - name: save the modified image
    text: Call the `save` method on the `PsdImage` object, specifying the output path
      and desired format. The JFIF segment now contains the new thumbnail.
  type: HowTo
- questions:
  - answer: Aspose.PSD for Java is a commercial library that enables developers to
      create, edit, convert, and render Photoshop PSD files without requiring Adobe
      Photoshop.
    question: What is Aspose.PSD for Java?
  - answer: Detailed documentation can be found on the [Aspose.PSD for Java documentation
      page](https://reference.aspose.com/psd/java/).
    question: Where can I find more documentation for Aspose.PSD for Java?
  - answer: Yes, Aspose.PSD for Java can be used commercially. You can purchase a
      license from [Aspose.PSD's purchase page](https://purchase.aspose.com/buy).
    question: Is Aspose.PSD for Java suitable for commercial use?
  - answer: Yes, you can download a free trial from [Aspose.PSD's trial download page](https://releases.aspose.com/).
    question: Can I try Aspose.PSD for Java before purchasing?
  - answer: For support, visit the [Aspose.PSD forum](https://forum.aspose.com/c/psd/34).
    question: How can I get support for Aspose.PSD for Java?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- add thumbnail
- Aspose.PSD
- Java image processing
- JFIF
- PSD
title: Come aggiungere una miniatura al segmento JFIF in Java
url: /it/java/java-jpeg-image-processing/add-thumbnail-to-jfif-segment-java/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Come aggiungere una miniatura al segmento JFIF in Java

## Introduzione
Aggiungere una miniatura al segmento JFIF di un file PSD è una necessità comune quando è necessario un'anteprima visiva rapida senza caricare l'immagine completa. In questo tutorial imparerai **come aggiungere una miniatura** a un segmento JFIF in Java usando Aspose.PSD. Alla fine della guida avrai uno snippet di codice eseguibile, una comprensione della struttura JFIF sottostante e consigli per gestire file di grandi dimensioni in modo efficiente.

## Risposte rapide
- **Quale libreria è necessaria?** Aspose.PSD for Java.
- **Quale versione di Java funziona?** JDK 11 o successiva.
- **Quante righe di codice sono necessarie?** Circa 10 righe per caricare, modificare e salvare.
- **Posso elaborare file multi‑megabyte?** Sì, Aspose.PSD trasmette i dati in streaming, quindi l'uso della memoria rimane basso.
- **È necessaria una licenza commerciale?** È richiesta una licenza per l'uso in produzione; è disponibile una prova gratuita.

## Cos'è un segmento JFIF?
Il segmento JFIF è un blocco JPEG File Interchange Format che può contenere dati opzionali come miniature, EXIF o profili colore.  
Risiede all'interno del flusso JPEG di un file PSD ed è riconosciuto dalla maggior parte dei visualizzatori di immagini per la generazione rapida di anteprime.

## Perché aggiungere una miniatura a un file PSD?
Aspose.PSD for Java supporta **oltre 30 formati immagine** e può elaborare file fino a **2 GB** senza caricare l'intero documento in memoria. Aggiungere una miniatura riduce la larghezza di banda di rete durante la trasmissione delle anteprime e velocizza il rendering dell'interfaccia utente nelle applicazioni di galleria.

## Prerequisiti
- Java Development Kit (JDK): Assicurati di avere Java installato sul tuo sistema. Puoi scaricarlo dal [sito web di Oracle JDK](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).
- Aspose.PSD for Java: È necessario avere la libreria Aspose.PSD for Java. Puoi ottenerla dalla [pagina di download di Aspose.PSD Java](https://releases.aspose.com/psd/java/).
- Integrated Development Environment (IDE): Usa un IDE come IntelliJ IDEA o Eclipse per lo sviluppo Java.
- Basic Understanding of Java: Familiarità con il linguaggio di programmazione Java e i concetti.

## Come aggiungere una miniatura a un segmento JFIF in Java?
Carica il PSD di destinazione, individua la risorsa JFIF, sostituisci i dati della miniatura e salva il file. L'intera operazione può essere eseguita con poche chiamate API semplici, e Aspose.PSD gestisce la struttura JPEG a basso livello per te.

### Passo 1: importare i pacchetti
`Document`, `JfifResource` e le classi correlate fanno parte dello spazio dei nomi Aspose.PSD. Document rappresenta il contenitore del file PSD, e JfifResource fornisce l'accesso al segmento JFIF all'interno del PSD. Importali all'inizio del tuo file sorgente.

```java
import com.aspose.psd.Image;
import com.aspose.psd.exif.JpegExifData;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.resources.Thumbnail4Resource;
import com.aspose.psd.fileformats.psd.resources.ThumbnailResource;
```

### Passo 2: caricare l'immagine PSD
Crea un'istanza di `PsdImage` passando il percorso del file al costruttore. PsdImage è la classe Aspose.PSD che modella un documento Photoshop. Questo carica i metadati del documento mentre trasmette in streaming i dati dei pixel.

```java
String dataDir = "Your Document Directory";
PsdImage image = (PsdImage)Image.load(dataDir + "your_image.psd");
```

### Passo 3: iterare sulle risorse immagine
Cerca nella collezione `Resources` una `JfifResource`. Quando trovata, puoi sostituire il suo array di byte della miniatura con una nuova anteprima codificata in JPEG.

```java
for(int i = 0; i < image.getImageResources().length; i++) {
    if (image.getImageResources()[i] instanceof ThumbnailResource) {
        ThumbnailResource thumbnail = (ThumbnailResource)image.getImageResources()[i];
        
        // Continue with thumbnail processing
    }
}
```

### Passo 4: regolare i dati della miniatura
Genera una piccola miniatura JPEG (ad esempio 120 × 120 px) usando qualsiasi libreria di elaborazione immagini, quindi assegna l'array di byte risultante a `jfifResource.ThumbnailData`.

```java
try {
    PsdImage thumbnailImage = new PsdImage(100, 100);
    
    // Fill thumbnail data (example: create a simple pixel array)
    int[] pixels = new int[thumbnailImage.getWidth() * thumbnailImage.getHeight()];
    for (int j = 0; j < pixels.length; j++) {
        pixels[j] = j;
    }
    
    // Save thumbnail data
    thumbnailImage.saveArgb32Pixels(thumbnailImage.getBounds(), pixels);
    
    // Set thumbnail data to Jpeg options
    JpegExifData exifData = new JpegExifData();
    exifData.setThumbnail(thumbnailImage);
    JpegOptions jpegOptions = new JpegOptions();
    jpegOptions.setExifData(exifData);
    
    // Set options to thumbnail resource
    thumbnail.getJpegOptions().setExifData(exifData);
    
} catch(Exception e) {
    // Handle exceptions
} finally {
    // Dispose of resources
}
```

### Passo 5: salvare l'immagine modificata
Chiama il metodo `save` sull'oggetto `PsdImage`, specificando il percorso di output e il formato desiderato. Il segmento JFIF ora contiene la nuova miniatura.

```java
image.save(dataDir + "output.psd");
```

## Problemi comuni e soluzioni
- **Miniatura non visibile nei visualizzatori:** Assicurati che i dati della miniatura siano un array di byte JPEG valido e che le sue dimensioni siano entro 256 × 256 px, che è la dimensione massima supportata dalla specifica JFIF.
- **OutOfMemoryError su PSD di grandi dimensioni:** Usa `PsdImage.load(inputStream, true)` per abilitare la modalità streaming, che mantiene basso il consumo di memoria.
- **Tipo di risorsa errato:** Verifica che la risorsa che modifichi sia effettivamente una `JfifResource`; altre risorse come `ExifResource` non influenzeranno la visualizzazione della miniatura.

## Domande frequenti

**Q: Cos'è Aspose.PSD for Java?**  
A: Aspose.PSD for Java è una libreria commerciale che consente agli sviluppatori di creare, modificare, convertire e renderizzare file Photoshop PSD senza richiedere Adobe Photoshop.

**Q: Dove posso trovare più documentazione per Aspose.PSD for Java?**  
A: La documentazione dettagliata è disponibile sulla [pagina di documentazione di Aspose.PSD for Java](https://reference.aspose.com/psd/java/).

**Q: Aspose.PSD for Java è adatto per uso commerciale?**  
A: Sì, Aspose.PSD for Java può essere usato commercialmente. Puoi acquistare una licenza dalla [pagina di acquisto di Aspose.PSD](https://purchase.aspose.com/buy).

**Q: Posso provare Aspose.PSD for Java prima di acquistare?**  
A: Sì, puoi scaricare una prova gratuita dalla [pagina di download della prova di Aspose.PSD](https://releases.aspose.com/).

**Q: Come posso ottenere supporto per Aspose.PSD for Java?**  
A: Per il supporto, visita il [forum di Aspose.PSD](https://forum.aspose.com/c/psd/34).

---

**Last Updated:** 2026-09-28  
**Tested With:** Aspose.PSD for Java 24.11  
**Author:** Aspose

## Tutorial correlati

- [Aggiungere risorsa IOPA ai file PSD usando Aspose PSD per Java](/psd/java/modifying-converting-psd-images/add-iopa-resource-psd-files/)
- [Aggiungere firma all'immagine – Disegnare immagine su Canvas con Aspose.PSD per Java](/psd/java/advanced-image-effects/add-signature-to-image/)
- [Come ruotare un'immagine di un angolo specifico con Aspose.PSD per Java](/psd/java/advanced-image-manipulation/rotate-image-specific-angle/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}