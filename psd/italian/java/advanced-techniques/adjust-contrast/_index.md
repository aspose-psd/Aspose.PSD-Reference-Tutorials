---
date: 2025-12-21
description: Scopri come regolare il contrasto delle immagini usando Aspose.PSD per
  Java, una libreria leader per la manipolazione di immagini Java, e convertire i
  file PSD in TIFF in modo efficiente.
linktitle: Adjust Contrast of an Image
second_title: Aspose.PSD Java API
title: Come regolare il contrasto di un'immagine con Aspose.PSD per Java
url: /it/java/advanced-techniques/adjust-contrast/
weight: 22
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Come regolare il contrasto di un'immagine con Aspose.PSD per Java

## Introduzione

Se stai cercando **come regolare il contrasto** nei tuoi progetti Java, sei nel posto giusto. Aspose.PSD per Java è una potente **java image manipulation library** che ti consente di perfezionare le proprietà dell'immagine come contrasto, luminosità e altro. In questo tutorial percorreremo i passaggi esatti per aumentare il contrasto di un file PSD e poi **convertire PSD in TIFF** per i flussi di lavoro successivi.

## Risposte rapide
- **Cosa significa “regolare il contrasto”?** Modifica la differenza tra i pixel più scuri e più chiari, facendo risaltare i dettagli.
- **Quale libreria gestisce questa operazione?** Aspose.PSD per Java – un toolkit di elaborazione immagini completo.
- **È necessaria una licenza?** Una licenza temporanea funziona per i test; è richiesta una licenza completa per la produzione.
- **Posso salvare il risultato come TIFF?** Sì, utilizzeremo `TiffOptions` per esportare l'immagine elaborata.
- **Quanto tempo impiega il codice ad eseguire?** Tipicamente meno di un secondo per file PSD di dimensioni standard.

## Che cos’è la regolazione del contrasto?
La regolazione del contrasto modifica l’intervallo tonale di un'immagine, amplificando la distinzione tra le aree chiare e scure. È particolarmente utile quando le immagini appaiono piatte dopo la scansione o quando si preparano grafiche per la stampa.

## Perché usare Aspose.PSD per Java?
- **Supporto ricco di formati** – apri, modifica e salva PSD, TIFF, PNG, JPEG e molti altri.
- **Alte prestazioni** – caching e ottimizzazioni delle immagini raster riducono il consumo di memoria.
- **API semplice** – chiamate a metodo singolo come `adjustContrast` rendono il codice leggibile.

## Prerequisiti

Prima di iniziare, assicurati di avere:

- Conoscenze di base della programmazione Java.
- La libreria Aspose.PSD per Java installata. Puoi scaricarla [qui](https://releases.aspose.com/psd/java/).

## Importare i pacchetti

Aggiungi gli import necessari alla tua classe Java:

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.psd.fileformats.tiff.enums.TiffPhotometrics;
import com.aspose.psd.imageoptions.TiffOptions;
```

## Passo 1: Caricare l'immagine

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

// Load an existing image into an instance of RasterImage class
Image image = Image.load(sourceFile);
```

Carichiamo il file PSD di origine (`sample.psd`) in un oggetto `Image`, che funge da punto di ingresso per tutte le successive elaborazioni.

## Passo 2: Convertire in RasterImage e memorizzare nella cache i dati

```java
// Cast object of Image to RasterImage
RasterImage rasterImage = (RasterImage)image;

// Check if RasterImage is cached and Cache RasterImage for better performance
if (!rasterImage.isCached()) {
    rasterImage.cacheData();
}
```

Il cast a `RasterImage` ci dà accesso alle operazioni a livello di pixel. Il caching migliora le prestazioni, soprattutto per file di grandi dimensioni.

## Come regolare il contrasto di un'immagine

```java
// Adjust the contrast
rasterImage.adjustContrast(50);
```

Il metodo `adjustContrast` accetta un intero che rappresenta la variazione percentuale. In questo esempio aumentiamo il contrasto del **50 %**.

## Convertire PSD in TIFF usando Aspose.PSD

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

Qui configuriamo `TiffOptions` (bits per sample, interpretazione fotometrica) e scriviamo l'immagine con contrasto migliorato in un file TIFF.

## Problemi comuni e soluzioni
- **Immagine non memorizzata nella cache:** Chiama sempre `cacheData()` per PSD di grandi dimensioni per evitare `OutOfMemoryError`.
- **Spostamento di colore inatteso:** Verifica che `setPhotometric` corrisponda allo spazio colore di destinazione (RGB vs. CMYK).
- **File non trovato:** Assicurati che `dataDir` punti alla cartella corretta e che il nome del file sia scritto correttamente.

## Domande frequenti

### Q1: Aspose.PSD è compatibile con diversi formati immagine?
A1: Sì, Aspose.PSD supporta vari formati immagine, offrendo flessibilità nei tuoi progetti.

### Q2: Come posso ottenere una licenza temporanea per Aspose.PSD?
A2: Puoi ottenere una licenza temporanea [qui](https://purchase.aspose.com/temporary-license/).

### Q3: Dove posso trovare la documentazione di Aspose.PSD?
A3: La documentazione è disponibile [qui](https://reference.aspose.com/psd/java/).

### Q4: Quali opzioni di supporto sono disponibili per Aspose.PSD?
A4: Per supporto, visita il [forum Aspose.PSD](https://forum.aspose.com/c/psd/34).

### Q5: Posso acquistare Aspose.PSD?
A5: Sì, puoi acquistare Aspose.PSD [qui](https://purchase.aspose.com/buy).

## Conclusione

Ora sai **come regolare il contrasto** di un'immagine PSD usando Aspose.PSD per Java e **come convertire PSD in TIFF** per ulteriori elaborazioni. Questi passaggi ti offrono un controllo fine sulla qualità dell'immagine mantenendo il codice pulito e manutenibile. Sentiti libero di sperimentare con altri metodi di regolazione dell'immagine come `adjustBrightness` o `adjustGamma` per soddisfare le tue esigenze specifiche.

---

**Ultimo aggiornamento:** 2025-12-21  
**Testato con:** Aspose.PSD per Java 24.12  
**Autore:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}