---
date: 2026-07-03
description: Scopri come ritagliare un'immagine Java usando Aspose.PSD per Java. Questo
  tutorial passo‑passo sul ritaglio delle immagini copre il caricamento di file PSD,
  l'impostazione dei valori di spostamento e il salvataggio del risultato.
keywords:
- crop image java
- how to crop image
- load psd file
- java image processing
- crop image left right
linktitle: Ritaglia immagine per spostamenti
schemas:
- author: Aspose
  dateModified: '2026-07-03'
  description: Learn how to crop image java using Aspose.PSD for Java. This step‑by‑step
    image cropping tutorial covers loading PSD files, setting shift values, and saving
    the result.
  headline: Crop Image Java by Shifts with Aspose.PSD
  type: TechArticle
- description: Learn how to crop image java using Aspose.PSD for Java. This step‑by‑step
    image cropping tutorial covers loading PSD files, setting shift values, and saving
    the result.
  name: Crop Image Java by Shifts with Aspose.PSD
  steps:
  - name: Load the Image
    text: '`Image` is the base class for all image types in Aspose.PSD. `RasterImage`
      represents a raster image and provides cropping capabilities.'
  - name: Cache Image Data
    text: '`cacheData()` loads the image data into memory for faster processing.'
  - name: Define Shift Values
    text: Specify the shift values for all four sides of the image (left, top, right,
      bottom) in pixels.
  - name: Apply Cropping
    text: '`crop(left, right, top, bottom)` trims the image by the specified pixel
      shifts on each side.'
  - name: Save the Results
    text: '`JpegOptions` defines JPEG encoding settings such as quality and color
      profile. Congratulations! You''ve successfully cropped an image using Aspose.PSD
      for Java.'
  type: HowTo
- questions:
  - answer: Yes, Aspose.PSD supports over 30 raster formats, including PSD, JPEG,
      PNG, BMP, TIFF, and GIF, ensuring broad compatibility.
    question: Is Aspose.PSD compatible with all image formats?
  - answer: Absolutely. After each `crop` call you receive a new image object, which
      you can crop again as needed.
    question: Can I apply multiple cropping operations to the same image?
  - answer: Yes, you can find support and engage with the community at [Aspose.PSD
      Forum](https://forum.aspose.com/c/psd/34).
    question: Is there a community forum for Aspose.PSD support?
  - answer: Visit [here](https://purchase.aspose.com/temporary-license/) to obtain
      a temporary license.
    question: How can I obtain a temporary license for Aspose.PSD?
  - answer: Explore the documentation and examples at [Aspose.PSD Java Documentation](https://reference.aspose.com/psd/java/).
    question: Are there sample projects showcasing Aspose.PSD functionalities?
  type: FAQPage
second_title: Aspose.PSD Java API
title: Ritaglia immagine Java per spostamenti con Aspose.PSD
url: /it/java/image-editing/crop-image-by-shifts/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Ritaglia Immagine Java con Spostamenti con Aspose.PSD

## Introduzione

Nell'elaborazione delle immagini in Java, **crop image java** è una necessità comune per preparare grafiche, miniature o risorse UI. Aspose.PSD per Java rende questo compito semplice esponendo un metodo `crop` che funziona su qualsiasi formato raster supportato. In questo tutorial imparerai a caricare un file PSD, definire i valori di spostamento sinistra‑destra‑alto‑basso, applicare il ritaglio e salvare il risultato—tutto senza scrivere codice personalizzato di manipolazione dei pixel.

## Risposte Rapide
- **Quale libreria gestisce il ritaglio?** Aspose.PSD per Java fornisce un metodo `crop` integrato.  
- **Ho bisogno di una licenza?** Una licenza temporanea è sufficiente per la valutazione; è necessaria una licenza completa per la produzione.  
- **Formati supportati?** Oltre 30 formati raster, inclusi PSD, JPEG, PNG, BMP e TIFF.  
- **Dimensione massima del file?** Gestisce file fino a 2 GB senza caricare l'intera immagine in memoria.  
- **Quante righe di codice?** Solo cinque passaggi logici—carica, cache, definisci spostamenti, ritaglia e salva.

## Cos'è crop image java?
`crop image java` si riferisce all'operazione di ritaglio di una bitmap in un'applicazione Java. Con Aspose.PSD, l'operazione è eseguita dal metodo `crop`, che accetta valori di spostamento per ciascun lato dell'immagine e restituisce una nuova istanza di immagine.

## Perché usare Aspose.PSD per il ritaglio delle immagini?
Aspose.PSD supporta **30+** formati immagine e può elaborare file PSD con centinaia di pagine utilizzando meno di 150 MB di RAM, grazie alla sua architettura lazy‑loading. La libreria garantisce inoltre risultati pixel‑perfect, preservando livelli, maschere e profili colore—qualcosa che molte librerie generiche non possono assicurare.

## Prerequisiti

### Java Development Kit (JDK)

Assicurati di avere l'ultima versione del JDK installata sul tuo sistema. Puoi scaricarla da [here](https://www.oracle.com/java/technologies/javase-downloads.html).

### Aspose.PSD for Java Library

Per iniziare, devi ottenere la libreria Aspose.PSD for Java. Vai alla [download page](https://releases.aspose.com/psd/java/) e scarica l'ultima versione.

### Integrated Development Environment (IDE)

Scegli il tuo IDE Java preferito, come Eclipse o IntelliJ, per un'esperienza di codifica fluida.

## Come ritagliare image java?

Carica il file sorgente, definisci gli spostamenti in pixel per ciascun lato e chiama il metodo `crop`—l'intero flusso di lavoro può essere scritto in cinque righe concise di codice. L'operazione `crop` crea una nuova immagine che contiene solo la regione specificata, lasciando intatto il file originale.

### Passo 1: Carica l'Immagine

`Image` è la classe base per tutti i tipi di immagine in Aspose.PSD.  
`RasterImage` rappresenta un'immagine raster e fornisce le capacità di ritaglio.  
```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.imageoptions.JpegOptions;
```

### Passo 2: Metti in Cache i Dati dell'Immagine

`cacheData()` carica i dati dell'immagine in memoria per una elaborazione più veloce.  
```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

// Load an existing image into an instance of RasterImage class
RasterImage rasterImage = (RasterImage)Image.load(sourceFile);
```

### Passo 3: Definisci i Valori di Spostamento

Specifica i valori di spostamento per tutti e quattro i lati dell'immagine (sinistra, alto, destra, basso) in pixel.  
```java
if (!rasterImage.isCached()) {
  rasterImage.cacheData();
}
```

### Passo 4: Applica il Ritaglio

`crop(left, right, top, bottom)` ritaglia l'immagine secondo gli spostamenti di pixel specificati per ciascun lato.  
```java
int leftShift = 10;
int rightShift = 10;
int topShift = 10;
int bottomShift = 10;
```

### Passo 5: Salva i Risultati

`JpegOptions` definisce le impostazioni di codifica JPEG come qualità e profilo colore.  
```java
rasterImage.crop(leftShift, rightShift, topShift, bottomShift);
```

Congratulazioni! Hai ritagliato con successo un'immagine usando Aspose.PSD per Java.

## Problemi Comuni e Soluzioni

- **L'immagine sembra invariata:** Verifica che i valori di spostamento siano positivi e non superino le dimensioni originali.  
- **OutOfMemoryError su file grandi:** Abilita il caching come mostrato al Passo 2; questo costringe Aspose.PSD a usare un file temporaneo invece di mantenere l'intera immagine in RAM.  
- **Spostamento di colore dopo il ritaglio:** Assicurati di preservare il profilo colore chiamando `image.save(..., new JpegOptions { ColorProfile = image.ColorProfile })` se hai bisogno di fedeltà cromatica esatta.

## Domande Frequenti

**Q: Aspose.PSD è compatibile con tutti i formati immagine?**  
A: Sì, Aspose.PSD supporta oltre 30 formati raster, inclusi PSD, JPEG, PNG, BMP, TIFF e GIF, garantendo ampia compatibilità.

**Q: Posso applicare più operazioni di ritaglio alla stessa immagine?**  
A: Assolutamente. Dopo ogni chiamata a `crop` ricevi un nuovo oggetto immagine, che puoi ritagliare nuovamente secondo necessità.

**Q: Esiste un forum della community per il supporto di Aspose.PSD?**  
A: Sì, puoi trovare supporto e interagire con la community su [Aspose.PSD Forum](https://forum.aspose.com/c/psd/34).

**Q: Come posso ottenere una licenza temporanea per Aspose.PSD?**  
A: Visita [here](https://purchase.aspose.com/temporary-license/) per ottenere una licenza temporanea.

**Q: Ci sono progetti di esempio che mostrano le funzionalità di Aspose.PSD?**  
A: Esplora la documentazione e gli esempi su [Aspose.PSD Java Documentation](https://reference.aspose.com/psd/java/).

---

**Ultimo Aggiornamento:** 2026-07-03  
**Testato Con:** Aspose.PSD 24.11 per Java  
**Autore:** Aspose  

{{< blocks/products/products-backtop-button >}}

```java
String destName = dataDir + "CroppingByShifts_out.jpg";
rasterImage.save(destName, new JpegOptions());
```

## Tutorial Correlati

- [Ritaglia Immagine per Rettangolo in Aspose.PSD per Java](/psd/java/image-editing/crop-image-by-rectangle/)
- [Ritaglia Immagine Java - Espandi e Ritaglia Immagini con Aspose.PSD per Java](/psd/java/image-editing/expand-and-crop-images/)
- [Ridimensiona Immagine Java - Uso dell'Enumerazione Resize Type in Aspose.PSD per Java](/psd/java/advanced-image-manipulation/resizing-with-resize-type-enumeration/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}