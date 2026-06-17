---
date: 2026-02-25
description: Scopri come convertire PSD in TIFF ed eseguire la regolazione del contrasto
  dell'immagine utilizzando Aspose.PSD per Java, una delle principali librerie Java
  per la manipolazione delle immagini.
linktitle: Convert PSD to TIFF and Adjust Contrast
second_title: Aspose.PSD Java API
title: Come convertire PSD in TIFF e regolare il contrasto con Aspose.PSD per Java
url: /it/java/advanced-techniques/adjust-contrast/
weight: 22
---

Tested With:" translate.

- "Author:" translate.

- The shortcodes at bottom remain.

Make sure to keep code block placeholders unchanged.

Now produce final content.{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Come convertire PSD in TIFF e regolare il contrasto con Aspose.PSD per Java

## Introduzione

Se hai bisogno di **convertire PSD in TIFF** e allo stesso tempo perfezionare la qualità visiva dei tuoi grafici, sei nel posto giusto. In questo tutorial percorreremo l’intero flusso di lavoro usando Aspose.PSD per Java, una solida libreria di **java image manipulation**. Imparerai come migliorare la **regolazione del contrasto dell’immagine**, memorizzare nella cache grandi dati raster per le prestazioni e, infine, **salvare l’immagine come TIFF** per l’elaborazione successiva. Immergiamoci!

## Risposte rapide
- **Cosa significa “regolare il contrasto”?** Cambia la differenza tra i pixel più scuri e più chiari, facendo risaltare i dettagli.  
- **Quale libreria gestisce questo?** Aspose.PSD per Java – un toolkit completo per l’elaborazione delle immagini.  
- **Ho bisogno di una licenza?** Una **licenza temporanea di Aspose** funziona per i test; è necessaria una licenza completa per la produzione.  
- **Posso **convertire PSD in TIFF**?** Assolutamente – useremo `TiffOptions` per esportare l’immagine elaborata.  
- **Quanto tempo impiega il codice ad eseguire?** Tipicamente meno di un secondo per file PSD di dimensioni standard su hardware moderno.

## Cos'è la regolazione del contrasto dell'immagine?
La regolazione del contrasto modifica l’intervallo tonale di un’immagine, amplificando la distinzione tra le aree chiare e scure. È particolarmente utile quando le immagini appaiono piatte dopo la scansione o quando si preparano grafiche per la stampa.

## Perché usare Aspose.PSD per Java?
- **Supporto ricco di formati** – apri, modifica e **salva l’immagine come TIFF**, PNG, JPEG e molti altri.  
- **Alte prestazioni** – la memorizzazione nella cache e le ottimizzazioni delle immagini raster riducono l’overhead di memoria, fondamentale per file PSD di grandi dimensioni.  
- **API semplice** – chiamate a metodo singolo come `adjustContrast` rendono il codice leggibile e manutenibile.  
- **Capacità complete di java image manipulation** che si adattano sia a script semplici sia a applicazioni di livello enterprise.

## Prerequisiti

Prima di iniziare, assicurati di avere:

- Conoscenze di base della programmazione Java.  
- Libreria Aspose.PSD per Java installata. Puoi scaricarla [qui](https://releases.aspose.com/psd/java/).

## Importare i pacchetti

Aggiungi le importazioni necessarie alla tua classe Java:

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

Convertire in `RasterImage` ci dà accesso alle operazioni a livello di pixel. La memorizzazione nella cache migliora le prestazioni, soprattutto per file di grandi dimensioni.

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

Qui configuriamo `TiffOptions` (bit per campione, interpretazione fotometrica) e **salviamo l’immagine come TIFF**. Questo passaggio completa il flusso di lavoro **convertire PSD in TIFF**.

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

A4: Per il supporto, visita il [forum Aspose.PSD](https://forum.aspose.com/c/psd/34).

### Q5: Posso acquistare Aspose.PSD?

A5: Sì, puoi acquistare Aspose.PSD [qui](https://purchase.aspose.com/buy).

## Conclusione

Ora sai **come convertire PSD in TIFF** e eseguire la **regolazione del contrasto dell’immagine** usando Aspose.PSD per Java. Questi passaggi ti offrono un controllo granulare sulla qualità dell’immagine mantenendo il codice pulito e manutenibile. Sentiti libero di sperimentare con altri metodi di regolazione come `adjustBrightness` o `adjustGamma` per soddisfare le tue esigenze specifiche.

---

**Ultimo aggiornamento:** 2026-02-25  
**Testato con:** Aspose.PSD per Java 24.12  
**Autore:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}