---
date: 2026-10-03
description: Scopri come estrarre la miniatura da PSD in Java usando Aspose.PSD. Questa
  guida passo‑passo copre la configurazione, gli snippet di codice e il salvataggio
  della miniatura come immagine JPEG.
keywords:
- extract thumbnail from psd
- java aspose psd
- psd thumbnail extraction
lastmod: 2026-10-03
linktitle: Estrai la miniatura da PSD in Java
og_description: Scopri come estrarre la miniatura da PSD in Java con Aspose.PSD. Questa
  guida ti accompagna nella configurazione, nel caricamento del file, nell'estrazione
  della miniatura e nel salvataggio come immagine JPEG.
og_image_alt: Screenshot showing Java code extracting a thumbnail from a PSD file
  using Aspose.PSD
og_title: Estrai la miniatura da PSD in Java usando Aspose.PSD
schemas:
- author: Aspose
  dateModified: '2026-10-03'
  description: Learn how to extract thumbnail from PSD in Java using Aspose.PSD. This
    step‑by‑step guide covers setup, code snippets, and saving the thumbnail as a
    JPEG image.
  headline: Extract thumbnail from PSD in Java
  type: TechArticle
- questions:
  - answer: Aspose.PSD is a Java library that enables programmatic creation, manipulation,
      and conversion of PSD and other raster image formats without requiring Adobe
      Photoshop.
    question: What is Aspose.PSD?
  - answer: You can refer to the [documentation](https://reference.aspose.com/psd/java/)
      for detailed API references and examples.
    question: Where can I find more documentation on Aspose.PSD for Java?
  - answer: Yes, you can download a [free trial](https://releases.aspose.com/) to
      evaluate the library’s capabilities.
    question: Can I try Aspose.PSD for free before purchasing?
  - answer: Temporary licenses are available from the [temporary license](https://purchase.aspose.com/temporary-license/)
      page.
    question: How can I obtain a temporary license for Aspose.PSD?
  - answer: Yes, Aspose.PSD can be used in both personal and commercial projects under
      its licensing terms.
    question: Is Aspose.PSD suitable for commercial use?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- java image processing
- aspose.psd
- thumbnail extraction
title: Estrai la miniatura da PSD in Java
url: /it/java/java-jpeg-image-processing/extract-thumbnail-from-psd-java/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Estrai miniatura da PSD in Java

## Introduzione
Estrai una miniatura da un file PSD ti consente di generare anteprime rapide senza caricare l'immagine a piena risoluzione. In Java, Aspose.PSD rende questo processo semplice e performante. In questo tutorial imparerai come configurare la libreria, individuare la risorsa della miniatura e salvarla come file JPEG — il tutto con poche righe di codice.

## Risposte rapide
- **Quale libreria gestisce le miniature PSD?** Aspose.PSD for Java.
- **Quante righe di codice sono necessarie?** Circa cinque righe per caricare, estrarre e salvare.
- **Posso estrarre miniature da file PSD di grandi dimensioni?** Sì, Aspose.PSD elabora file fino a 500 MB senza caricare l'intera memoria.
- **È necessaria una licenza per lo sviluppo?** Una versione di prova gratuita è sufficiente per la valutazione; è richiesta una licenza per la produzione.
- **Quali formati di output sono supportati?** La miniatura estratta può essere salvata come JPEG, PNG o BMP.

## Cos'è l'estrazione della miniatura da PSD?
L'estrazione della miniatura da PSD è il processo di lettura della piccola immagine di anteprima incorporata all'interno di un documento Photoshop (PSD). Questa anteprima è memorizzata come risorsa e può essere salvata indipendentemente per scopi di catalogazione o visualizzazione. La miniatura è tipicamente una rappresentazione a bassa risoluzione utilizzata dalle applicazioni per mostrare un rapido riepilogo visivo senza caricare l'immagine a dimensione intera.

## Perché utilizzare Aspose.PSD per questo compito?
Aspose.PSD supporta **oltre 30 formati di immagine** e può gestire file PSD fino a **500 MB** mantenendo basso l'uso di memoria perché legge le risorse su richiesta. L'API fornisce anche una solida gestione degli errori, così puoi estrarre miniature in modo affidabile anche da file corrotti.

## Prerequisiti
- Java Development Kit (JDK) installato.
- Libreria Aspose.PSD for Java scaricata da [Aspose.PSD for Java download](https://releases.aspose.com/psd/java/).
- Familiarità di base con la sintassi Java e la configurazione del progetto.

## Come estrarre una miniatura da un file PSD in Java?
Carica il file PSD con `PsdImage`, individua il `ThumbnailResource` e salva i dati dell'immagine come JPEG. Aspose.PSD astrae il parsing a basso livello, quindi devi solo chiamare `getResources()` e poi `save()` sull'immagine estratta. Questo approccio funziona per qualsiasi PSD che contenga una miniatura, indipendentemente dalla dimensione del file.

## Importa pacchetti
`Image` è la classe base per il caricamento delle immagini. `PsdImage` rappresenta un documento PSD. `ThumbnailResource` e `Thumbnail4Resource` rappresentano le risorse delle miniature. `JpegOptions` specifica le opzioni di salvataggio JPEG.

```text
```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.resources.Thumbnail4Resource;
import com.aspose.psd.fileformats.psd.resources.ThumbnailResource;
import com.aspose.psd.imageoptions.JpegOptions;
```
```

## Passo 1: carica il file PSD
Per prima cosa, crea un'istanza `PsdImage` che punti al tuo file PSD. Il costruttore legge solo l'intestazione e le risorse necessarie, mantenendo l'uso di memoria minimo.

```text
```java
String dataDir = "Your_Document_Directory/";
PsdImage image = (PsdImage)Image.load(dataDir + "your_file.psd");
```
```

Sostituisci `"Your_Document_Directory/"` con il percorso della directory in cui si trova il tuo file PSD, e `"your_file.psd"` con il nome del tuo file PSD.

## Passo 2: iterare le risorse dell'immagine
Aspose.PSD memorizza le miniature come oggetti `ThumbnailResource` all'interno della collezione di risorse dell'immagine. Scorri la collezione, verifica il tipo di risorsa e cattura la prima miniatura che incontri.

```text
```java
for (int i = 0; i < image.getImageResources().length; i++) {
    if (image.getImageResources()[i] instanceof ThumbnailResource) {
        ThumbnailResource thumbnail = (ThumbnailResource) image.getImageResources()[i];
        
        // Extract thumbnail data
        int[] data = thumbnail.getThumbnailArgb32Data();
        
        // Create a new image with the extracted thumbnail data
        PsdImage extractedThumbnailImage = new PsdImage(thumbnail.getWidth(), thumbnail.getHeight());
        extractedThumbnailImage.saveArgb32Pixels(extractedThumbnailImage.getBounds(), data);
        
        // Save the extracted thumbnail as a separate JPEG file
        extractedThumbnailImage.save(dataDir + "extracted_thumbnail.jpg", new JpegOptions());
        
        // Output success message
        System.out.println("Thumbnail extracted and saved successfully.");
        
        break; // Exit the loop once thumbnail is found and processed
    }
}
```
```

## Passo 3: salva la miniatura estratta
Una volta ottenuta l'immagine della miniatura, chiama il suo metodo `save` per scriverla su disco. Puoi scegliere JPEG, PNG o BMP; JPEG è il più comune per le anteprime web.

## Passo 4: gestione di diversi tipi di miniatura
Se un PSD contiene più varianti di miniatura, come `Thumbnail4Resource`, estendi la logica di iterazione per verificare ciascun tipo. L'API fornisce classi separate per ogni risorsa, consentendoti di selezionare la risoluzione di cui hai bisogno.

## Problemi comuni e soluzioni
- **Nessuna miniatura trovata:** Non tutti i file PSD incorporano un'anteprima. Verifica il file sorgente nel pannello “File → Informazioni file” di Photoshop.
- **Errore di formato non supportato:** Assicurati di utilizzare l'ultima versione di Aspose.PSD; le versioni più vecchie potrebbero non riconoscere i nuovi tipi di risorsa miniatura.
- **Out‑of‑memory su file di grandi dimensioni:** Usa `PsdImage.load(..., LoadOptions)` con `LoadOptions.setLoadResourcesOnly(true)` per evitare di caricare i dati completi dell'immagine quando ti serve solo la miniatura.

## Domande frequenti

**Q: Cos'è Aspose.PSD?**  
A: Aspose.PSD è una libreria Java che consente la creazione, manipolazione e conversione programmatica di file PSD e altri formati di immagine raster senza richiedere Adobe Photoshop.

**Q: Dove posso trovare ulteriore documentazione su Aspose.PSD per Java?**  
A: Puoi consultare la [documentazione](https://reference.aspose.com/psd/java/) per riferimenti API dettagliati ed esempi.

**Q: Posso provare Aspose.PSD gratuitamente prima di acquistare?**  
A: Sì, puoi scaricare una [versione di prova gratuita](https://releases.aspose.com/) per valutare le capacità della libreria.

**Q: Come posso ottenere una licenza temporanea per Aspose.PSD?**  
A: Le licenze temporanee sono disponibili nella pagina della [licenza temporanea](https://purchase.aspose.com/temporary-license/).

**Q: Aspose.PSD è adatto per uso commerciale?**  
A: Sì, Aspose.PSD può essere utilizzato sia in progetti personali che commerciali secondo i termini di licenza.

---

**Ultimo aggiornamento:** 2026-10-03  
**Testato con:** Aspose.PSD for Java 24.12  
**Autore:** Aspose

## Tutorial correlati

- [Come convertire PSD in formati di immagine raster con Aspose.PSD per Java](/psd/java/advanced-techniques/convert-psd-to-raster-formats/)
- [Salva PSD come JPEG e supporta il colore RGB con Aspose.PSD Java](/psd/java/advanced-psd-layer-features-effects/support-rgb-color-psd-files/)
- [Ridimensiona immagine con Aspose.PSD per Java – Disegna forme e operazioni di base sull'immagine](/psd/java/basic-image-operations/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}