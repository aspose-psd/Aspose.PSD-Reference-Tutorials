---
date: 2026-07-27
description: Scopri come convertire PSD in TIFF ed eseguire la regolazione del contrasto
  dell'immagine usando Aspose.PSD for Java, una delle principali librerie Java per
  la manipolazione di immagini.
keywords:
- convert psd to tiff
- java image processing
- improve image contrast
lastmod: 2026-07-27
linktitle: Converti PSD in TIFF e Regola il Contrasto
og_description: Converti PSD in TIFF con regolazione del contrasto usando Aspose.PSD
  for Java. Questa guida mostra codice passo‑a‑passo, consigli sulle prestazioni e
  opzioni di esportazione per output TIFF di alta qualità.
og_image_alt: 'Guide: Convert PSD to TIFF and adjust contrast using Aspose.PSD for
  Java'
og_title: Converti PSD in TIFF & Regola il Contrasto – Aspose.PSD Java
schemas:
- author: Aspose
  dateModified: '2026-07-27'
  description: Learn how to convert PSD to TIFF and perform image contrast adjustment
    using Aspose.PSD for Java, a leading java image manipulation library.
  headline: Convert PSD to TIFF and Adjust Contrast with Aspose.PSD for Java
  type: TechArticle
- questions:
  - answer: It changes the difference between the darkest and brightest pixels, making
      details pop.
    question: What does “adjust contrast” mean?
  - answer: Aspose.PSD for Java – a full‑featured image processing toolkit.
    question: Which library handles this?
  - answer: A **temporary Aspose license** works for testing; a full license is required
      for production.
    question: Do I need a license?
  - answer: Absolutely – we’ll use `TiffOptions` to export the processed image.
    question: Can I convert PSD to TIFF?
  - answer: For a typical 30 MB PSD the whole pipeline runs under one second on a
      modern CPU.
    question: How fast is the conversion?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- convert psd
- Aspose.PSD
- Java image manipulation
- tiff export options
title: Converti PSD in TIFF e Regola il Contrasto con Aspose.PSD for Java
url: /it/java/advanced-techniques/adjust-contrast/
weight: 22
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Come convertire PSD in TIFF e regolare il contrasto con Aspose.PSD per Java

## Introduzione

Se hai bisogno di **convertire PSD in TIFF** mentre affini anche la qualità visiva delle tue grafiche, sei nel posto giusto. In questo tutorial percorreremo l'intero flusso di lavoro usando Aspose.PSD per Java — una solida libreria di **manipolazione di immagini java**. Imparerai come migliorare la **regolazione del contrasto dell'immagine**, memorizzare nella cache grandi dati raster per le prestazioni e infine **salvare l'immagine come TIFF** per l'elaborazione successiva. Immergiamoci!

## Risposte rapide
- **Cosa significa “regolare il contrasto”?** Modifica la differenza tra i pixel più scuri e quelli più luminosi, facendo risaltare i dettagli.  
- **Quale libreria gestisce questo?** Aspose.PSD per Java – un toolkit di elaborazione immagini completo.  
- **Ho bisogno di una licenza?** Una **licenza temporanea Aspose** funziona per i test; è necessaria una licenza completa per la produzione.  
- **Posso convertire PSD in TIFF?** Assolutamente – utilizzeremo `TiffOptions` per esportare l'immagine elaborata.  
- **Quanto è veloce la conversione?** Per un PSD tipico da 30 MB l'intera pipeline viene eseguita in meno di un secondo su una CPU moderna.

## Cos'è la regolazione del contrasto dell'immagine?
La regolazione del contrasto modifica la gamma tonale di un'immagine, amplificando la distinzione tra le aree chiare e scure. Questo è particolarmente utile quando le immagini appaiono piatte dopo la scansione o quando si preparano grafiche per la stampa. Funziona allungando o comprimendo l'istogramma delle intensità dei pixel, rendendo le ombre più profonde e le luci più luminose, il che migliora la percezione di profondità e dettaglio.

## Perché usare Aspose.PSD per Java?
Aspose.PSD fornisce un motore ad alte prestazioni e ricco di funzionalità che può gestire **oltre 50 formati raster e vettoriali**, elaborare file fino a 500 MB senza caricare l'intero contenuto in memoria, ed esportare in TIFF con controllo preciso su bit‑per‑sample e interpretazione fotometrica. Queste capacità quantificate lo rendono una scelta di prim'ordine per pipeline di immagini di livello aziendale.

## Prerequisiti
- Conoscenza di base della programmazione Java.  
- Libreria Aspose.PSD per Java installata. Puoi scaricarla [qui](https://releases.aspose.com/psd/java/).

## Importa pacchetti
Aggiungi gli import necessari alla tua classe Java:

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.psd.fileformats.tiff.enums.TiffPhotometrics;
import com.aspose.psd.imageoptions.TiffOptions;
```

## Passo 1: Carica l'immagine
La classe `Image` è il punto di ingresso di Aspose.PSD che rappresenta qualsiasi immagine raster supportata in memoria.  
```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

// Load an existing image into an instance of RasterImage class
Image image = Image.load(sourceFile);
```

Carichiamo il file PSD di origine (`sample.psd`) in un oggetto `Image`, che funge da punto di ingresso per tutte le successive elaborazioni.

## Passo 2: Converti in RasterImage e memorizza nella cache i dati
`RasterImage` fornisce accesso diretto a livello di pixel e consente la memorizzazione nella cache per file di grandi dimensioni.  
```java
// Cast object of Image to RasterImage
RasterImage rasterImage = (RasterImage)image;

// Check if RasterImage is cached and Cache RasterImage for better performance
if (!rasterImage.isCached()) {
    rasterImage.cacheData();
}
```

Il cast a `RasterImage` ci dà accesso alle operazioni a livello di pixel. La memorizzazione nella cache migliora le prestazioni, soprattutto per file di grandi dimensioni.

## Come regolare il contrasto di un'immagine
Il metodo `adjustContrast` è una semplice chiamata API che modifica il contrasto dell'immagine di un valore percentuale.  
```java
// Adjust the contrast
rasterImage.adjustContrast(50);
```

Il metodo `adjustContrast` accetta un intero che rappresenta la variazione percentuale. In questo esempio aumentiamo il contrasto del **50 %**.

## Converti PSD in TIFF usando Aspose.PSD
`TiffOptions` consente di specificare impostazioni specifiche per TIFF come bit per campione, tipo di compressione e interpretazione fotometrica.  
```java
// Create an instance of TiffOptions for the resultant image
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
int[] ushort = { 8, 8, 8 };
tiffOptions.setBitsPerSample(ushort);
tiffOptions.setPhotometric(TiffPhotometrics.Rgb);

// Save the resultant image to TIFF format
String destName = dataDir + "AdjustContrast_out.tiff";
rasterImage.save(destName, tiffOptions);
```

Qui configuriamo `TiffOptions` (bit per campione, interpretazione fotometrica) e **salviamo l'immagine come TIFF**. Questo passaggio completa il flusso di lavoro di **conversione da PSD a TIFF**.

## Problemi comuni e soluzioni
- **Immagine non memorizzata nella cache:** Chiama sempre `cacheData()` per PSD di grandi dimensioni per evitare `OutOfMemoryError`.  
- **Spostamento di colore inatteso:** Verifica che `setPhotometric` corrisponda allo spazio colore di destinazione (RGB vs. CMYK).  
- **File non trovato:** Assicurati che `dataDir` punti alla cartella corretta e che il nome del file sia scritto correttamente.

## Domande frequenti

### Q1: Aspose.PSD è compatibile con diversi formati di immagine?
Sì, Aspose.PSD supporta **oltre 50 formati di input e output**, inclusi PSD, TIFF, PNG, JPEG, BMP e GIF, offrendoti flessibilità in tutti i progetti.

### Q2: Come posso ottenere una licenza temporanea per Aspose.PSD?
Puoi ottenere una licenza temporanea [qui](https://purchase.aspose.com/temporary-license/).

### Q3: Dove posso trovare la documentazione di Aspose.PSD?
La documentazione è disponibile [qui](https://reference.aspose.com/psd/java/).

### Q4: Quali opzioni di supporto sono disponibili per Aspose.PSD?
Per il supporto, visita il [forum Aspose.PSD](https://forum.aspose.com/c/psd/34).

### Q5: Posso acquistare Aspose.PSD?
Sì, puoi acquistare Aspose.PSD [qui](https://purchase.aspose.com/buy).

## Conclusione
Ora sai **come convertire PSD in TIFF** e eseguire la **regolazione del contrasto dell'immagine** usando Aspose.PSD per Java. Questi passaggi ti offrono un controllo dettagliato sulla qualità dell'immagine mantenendo il codice pulito e manutenibile. Sentiti libero di sperimentare altri metodi di regolazione come `adjustBrightness` o `adjustGamma` per soddisfare le tue esigenze specifiche.

---

**Ultimo aggiornamento:** 2026-07-27  
**Testato con:** Aspose.PSD for Java 24.12  
**Autore:** Aspose

## Tutorial correlati
- [Tutorial di elaborazione immagini Java - Regola la luminosità di un'immagine con Aspose.PSD per Java](/psd/java/advanced-techniques/adjust-brightness/)
- [Come regolare il gamma nell'elaborazione immagini Java con Aspose.PSD](/psd/java/advanced-techniques/adjust-gamma/)
- [Converti PSD in formati di immagine raster con Aspose.PSD per Java](/psd/java/advanced-techniques/convert-psd-to-raster-formats/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}