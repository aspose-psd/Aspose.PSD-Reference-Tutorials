---
date: 2026-08-01
description: Scopri come regolare il gamma nell'elaborazione di immagini Java con
  Aspose.PSD, convertire PSD in TIFF e correggere le immagini sbiadite in un tutorial
  conciso.
keywords:
- how to adjust gamma
- fix washed out image
- java image processing
- convert psd to tiff
- server side image processing
lastmod: 2026-08-01
linktitle: Regola il gamma di un'immagine
og_description: Scopri come regolare il gamma nell'elaborazione di immagini Java usando
  Aspose.PSD – una libreria veloce, server‑side, che corregge le immagini sbiadite
  e converte PSD in TIFF in poche righe di codice.
og_image_alt: 'Guide: Adjust gamma in Java images with Aspose.PSD, convert PSD to
  TIFF'
og_title: come regolare il gamma – elaborazione Java con Aspose.PSD
schemas:
- author: Aspose
  dateModified: '2026-08-01'
  description: Learn how to adjust gamma in Java image processing with Aspose.PSD,
    convert PSD to TIFF, and fix washed‑out images in a concise tutorial.
  headline: How to Adjust Gamma in Java Image Processing with Aspose.PSD
  type: TechArticle
- description: Learn how to adjust gamma in Java image processing with Aspose.PSD,
    convert PSD to TIFF, and fix washed‑out images in a concise tutorial.
  name: How to Adjust Gamma in Java Image Processing with Aspose.PSD
  steps:
  - name: '**Java Development Environment** – Java 8 or later installed.'
    text: '**Java Development Environment** – Java 8 or later installed.'
  - name: '**Aspose.PSD Library** – Download and add the JAR to your project. See
      the official [documentation](https://reference.aspose.com/psd/java/).'
    text: '**Aspose.PSD Library** – Download and add the JAR to your project. See
      the official [documentation](https://reference.aspose.com/psd/java/).'
  - name: '**Sample Image** – A PSD file you want to process (e.g., `sample.psd`).'
    text: '**Sample Image** – A PSD file you want to process (e.g., `sample.psd`).'
  type: HowTo
- questions:
  - answer: Yes – the `adjustGamma` method accepts separate float values for red,
      green, and blue channels.
    question: Can I apply different gamma values to each colour channel?
  - answer: Absolutely. You can perform resizing, cropping, or colour corrections
      sequentially on the same `RasterImage` instance.
    question: Is it possible to chain multiple image adjustments before saving?
  - answer: Yes, each layer can be accessed and processed individually.
    question: Does Aspose.PSD support multi‑page PSD files?
  - answer: Aspose.PSD supports PNG, JPEG, BMP, and many other formats via their respective
      options classes.
    question: What format can I export to besides TIFF?
  - answer: Start with a moderate gamma (around 2.0) and preview the result; adjust
      downwards if the image looks too bright.
    question: How do I avoid a washed‑out image after gamma correction?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- adjust gamma
- Aspose.PSD
- Java image processing
- PSD to TIFF
- server side processing
title: Come regolare il gamma nell'elaborazione di immagini Java con Aspose.PSD
url: /it/java/advanced-techniques/adjust-gamma/
weight: 23
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Come regolare il gamma nella elaborazione di immagini Java con Aspose.PSD

## Introduzione

Se stai lavorando su **java image processing**, imparare **come regolare il gamma** è una tecnica fondamentale per migliorare luminosità e contrasto senza perdere dettagli. In questo tutorial vedremo come utilizzare **Aspose.PSD for Java** per applicare la correzione gamma a un file PSD, **convertire PSD in TIFF**, ed evitare un **washed‑out image**. Scoprirai perché questo approccio è veloce, affidabile e perfetto per **server‑side image processing** pipelines.

## Risposte rapide
- **What does gamma correction do?** Rimappa i valori di luminanza per rendere le aree scure più luminose o le aree luminose più scure mantenendo i dettagli complessivi.  
- **Which library handles the processing?** Aspose.PSD for Java fornisce un metodo dedicato `adjustGamma` per le immagini raster.  
- **Can I convert PSD to TIFF in the same flow?** Sì – dopo la regolazione del gamma è possibile salvare l'immagine direttamente in TIFF usando `TiffOptions`.  
- **Do I need a license for development?** Una versione di prova gratuita è sufficiente per i test; è necessaria una licenza commerciale per l'uso in produzione.  
- **What Java version is supported?** Aspose.PSD supporta Java 8 e versioni successive.

## Cos'è la correzione gamma in Java

La correzione gamma modifica la relazione non lineare tra i valori dei pixel codificati e la luminosità visualizzata. Regolando la curva gamma è possibile **fix washed out image** problemi o migliorare i dettagli nelle ombre senza sovra‑esporre le alte luci. Funziona applicando una funzione di legge di potenza a ciascun pixel, che schiarisce le tonalità scure e comprime le alte luci, risultando in un aspetto visivo più naturale.

## Perché usare Aspose.PSD per la correzione gamma?

Aspose.PSD è una **java image processing library** che astrae le complessità del formato PSD. Supporta l'elaborazione di file fino a 2 GB, gestisce oltre 50 formati di immagine diversi e fornisce una semplice chiamata `adjustGamma`, rendendola ideale per **java gamma correction** e flussi di lavoro **convert PSD to TIFF**.

## Prerequisiti

1. **Java Development Environment** – Java 8 o successivo installato.  
2. **Aspose.PSD Library** – Download and add the JAR to your project. See the official [documentazione](https://reference.aspose.com/psd/java/).  
3. **Sample Image** – A PSD file you want to process (e.g., `sample.psd`).  

## Importa i pacchetti

Prima di iniziare, importa gli spazi dei nomi essenziali che ti danno accesso alla gestione raster e alle opzioni di formato file.

## Passo 1: Carica l'immagine

La classe `RasterImage` rappresenta i dati pixel rasterizzati di un livello PSD in memoria. Caricare l'immagine una volta e memorizzarla nella cache riduce il consumo di memoria per le regolazioni successive.

## Passo 2: Regola il gamma

Carica il tuo PSD con `new RasterImage("sample.psd")` e chiama `rasterImage.adjustGamma(2.0f)` — quella singola riga applica un gamma di 2.0 a tutti i canali colore, schiarendo le ombre mantenendo intatte le alte luci. È possibile passare valori separati per rosso, verde e blu se sono necessarie regolazioni specifiche per canale.

## Passo 3: Crea TiffOptions

`TiffOptions` ti consente di controllare la compressione, i bit per campione e altre impostazioni specifiche del TIFF. Impostare un campione a 8 bit (`{8,8,8}`) mantiene la dimensione del file TIFF ragionevole preservando la fedeltà del colore.

## Passo 4: Salva l'immagine risultante

Chiama `rasterImage.save("output.tif", tiffOptions)` per scrivere l'immagine elaborata su disco. Dopo il salvataggio, puoi inviare il TIFF a sistemi a valle come servizi di stampa o API web.

## Casi d'uso comuni

- **Automated graphics pipelines** – Regola il gamma al volo prima di generare le miniature.  
- **Batch conversion tools** – Converti grandi archivi PSD in TIFF normalizzando la luminosità.  
- **Web services** – Espone un endpoint che riceve un PSD, applica la correzione gamma e restituisce un TIFF per il consumo del client.

## Problemi comuni e soluzioni

| Issue | Why it Happens | How to Fix |
|-------|----------------|------------|
| **L'immagine appare washed out** | Valore gamma troppo alto (es., > 2.5) | Riduci il fattore gamma a un valore compreso tra 1.8 e 2.2. |
| **`rasterImage.isCached()` restituisce false** | Immagine non ancora caricata in memoria | Chiama `rasterImage.cacheData()` prima di regolare il gamma. |
| **La dimensione del file TIFF è grande** | Bit per campione impostati a 16‑bit | Usa un campione a 8‑bit (`{8,8,8}`) come mostrato nell'esempio. |

## Domande frequenti

**Q: Posso applicare valori gamma diversi a ciascun canale colore?**  
A: Sì – il metodo `adjustGamma` accetta valori float separati per i canali rosso, verde e blu.

**Q: È possibile concatenare più regolazioni dell'immagine prima del salvataggio?**  
A: Assolutamente. È possibile eseguire ridimensionamento, ritaglio o correzioni colore in sequenza sulla stessa istanza `RasterImage`.

**Q: Aspose.PSD supporta file PSD multi‑pagina?**  
A: Sì, ogni livello può essere accesso e processato individualmente.

**Q: In quale formato posso esportare oltre a TIFF?**  
A: Aspose.PSD supporta PNG, JPEG, BMP e molti altri formati tramite le rispettive classi di opzioni.

**Q: Come evito un'immagine washed‑out dopo la correzione gamma?**  
A: Inizia con un gamma moderato (intorno a 2.0) e visualizza l'anteprima; riduci il valore se l'immagine appare troppo luminosa.

## Conclusione

Congratulazioni! Hai appreso con successo **how to adjust gamma** in un flusso di lavoro **java image processing**, convertito un PSD in TIFF e evitato le insidie comuni come una **washed‑out image**. Questo modello ti offre un controllo preciso su luminosità e contrasto, rendendolo ideale per pipeline grafiche automatizzate, servizi web o utility desktop.

---

**Ultimo aggiornamento:** 2026-08-01  
**Testato con:** Aspose.PSD 24.11 for Java  
**Autore:** Aspose  

{{< blocks/products/products-backtop-button >}}

## Tutorial correlati

- [Tutorial di elaborazione immagini Java - Regola la luminosità di un'immagine con Aspose.PSD for Java](/psd/java/advanced-techniques/adjust-brightness/)
- [Come convertire PSD in TIFF e regolare il contrasto con Aspose.PSD for Java](/psd/java/advanced-techniques/adjust-contrast/)
- [Converti PSD in immagine in Java – Applica i livelli di regolazione con Aspose.PSD](/psd/java/advanced-psd-layer-features-effects/apply-adjustment-layers-psd-files/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.psd.fileformats.tiff.enums.TiffPhotometrics;
import com.aspose.psd.imageoptions.TiffOptions;
```

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

// Load an existing image into an instance of RasterImage class
Image image = Image.load(sourceFile);

// Cast object of Image to RasterImage
RasterImage rasterImage = (RasterImage)image;

// Check if RasterImage is cached for better performance
if (!rasterImage.isCached()) {
    rasterImage.cacheData();
}
```

```java
// Adjust the gamma
rasterImage.adjustGamma(2.2f, 2.2f, 2.2f);
```

```java
// Create an instance of TiffOptions for the resultant image
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
int[] ushort = { 8, 8, 8 };
tiffOptions.setBitsPerSample(ushort);
tiffOptions.setPhotometric(TiffPhotometrics.Rgb);
```

```java
// Save the resultant image to TIFF format
String destName = dataDir + "AdjustGamma_out.tiff";
rasterImage.save(destName, tiffOptions);
```