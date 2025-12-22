---
date: 2025-12-19
description: Scopri come regolare la luminosità di un'immagine usando Aspose.PSD per
  Java. Questo tutorial di manipolazione delle immagini in Java fornisce una guida
  passo‑passo.
linktitle: Adjust Brightness of an Image
second_title: Aspose.PSD Java API
title: Come regolare la luminosità di un'immagine con Aspose.PSD per Java
url: /it/java/advanced-techniques/adjust-brightness/
weight: 21
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Regola la luminosità di un'immagine con Aspose.PSD per Java

## Introduzione

Se hai bisogno di **imparare come regolare la luminosità** di un'immagine direttamente dal codice Java, sei nel posto giusto. La regolazione della luminosità è un'operazione frequente per grafici, fotografi e chiunque costruisca pipeline di elaborazione immagini. In questo **tutorial di manipolazione immagini in Java** vedremo l'intero flusso di lavoro—caricamento di un PSD/TIFF, applicazione di un offset di luminosità e salvataggio del risultato—utilizzando la libreria Aspose.PSD per Java.

## Risposte rapide
- **Quale libreria gestisce la luminosità?** Aspose.PSD per Java  
- **Quale metodo cambia la luminosità?** `RasterImage.adjustBrightness()`  
- **Posso lavorare con file PSD e TIFF?** Sì, l'API supporta entrambi i formati.  
- **È necessaria una licenza per la produzione?** È richiesta una licenza commerciale per l'uso non‑valutativo.  
- **Quanto tempo richiede l'implementazione?** Tipicamente meno di 10 minuti per una regolazione di base.

## Che cos'è la regolazione della luminosità dell'immagine?

La regolazione della luminosità dell'immagine modifica la chiarezza complessiva di ogni pixel. Aumentare la luminosità rende le aree scure più chiare, mentre diminuirla scurisce l'intera immagine. Questa operazione è utile per correggere foto sottoesposte, preparare asset per la stampa o creare effetti visivi nelle applicazioni.

## Perché usare Aspose.PSD per Java?

- **Supporto completo dei formati** – PSD, TIFF, JPEG, PNG e molti altri.  
- **Nessuna dipendenza nativa esterna** – puro Java, facile da integrare.  
- **Caching ad alte prestazioni** – i dati raster possono essere memorizzati nella cache per operazioni ripetute più veloci.  
- **API ricca** – metodi per correzione colore, livelli, maschere e altre modifiche avanzate.

## Prerequisiti

Prima di immergerti nel tutorial, assicurati di avere i seguenti prerequisiti:

- Libreria Aspose.PSD per Java: scarica e installa la libreria dalla [documentazione di Aspose.PSD per Java](https://reference.aspose.com/psd/java/).

## Importare i pacchetti

Per iniziare, importa i pacchetti necessari nel tuo progetto Java. In questo esempio utilizzeremo i seguenti:

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.psd.fileformats.tiff.enums.TiffPhotometrics;
import com.aspose.psd.imageoptions.TiffOptions;
```

Ora, analizziamo il processo di regolazione della luminosità di un'immagine in semplici passaggi:

## Come regolare la luminosità usando Aspose.PSD

### Passo 1: Carica l'immagine

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";
String destName = dataDir + "AdjustBrightness_out.tiff";

// Load an existing image into an instance of RasterImage class
Image image = Image.load(sourceFile);
// Cast object of Image to RasterImage
RasterImage rasterImage = (RasterImage) image;

// Check if RasterImage is cached and Cache RasterImage for better performance
if (!rasterImage.isCached()) {
    rasterImage.cacheData();
}
```

In questo passaggio, carichiamo l'immagine di destinazione e la convertiamo in un `RasterImage` per ulteriori elaborazioni.

### Passo 2: Regola la luminosità

```java
// Adjust the brightness
rasterImage.adjustBrightness(-50);
```

Qui utilizziamo il metodo `adjustBrightness` per modificare la luminosità dell'immagine. In questo esempio diminuiamo la luminosità di 50 unità, ma puoi personalizzare questo valore in base alle tue esigenze.

### Passo 3: Imposta TiffOptions

```java
int[] ushort = {8, 8, 8};
// Create an instance of TiffOptions for the resultant image
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
tiffOptions.setBitsPerSample(ushort);
tiffOptions.setPhotometric(TiffPhotometrics.Rgb);
```

Configura le `TiffOptions` per salvare l'immagine regolata. Regola le proprietà `bitsPerSample` e `photometric` in base alle tue necessità specifiche.

### Passo 4: Salva l'immagine risultante

```java
// Save the resultant image
rasterImage.save(destName, tiffOptions);
```

Infine, salva l'immagine modificata utilizzando le `TiffOptions` specificate.

## Problemi comuni e soluzioni

| Problema | Motivo | Soluzione |
|----------|--------|-----------|
| **`ClassCastException` durante il cast di Image** | Il file non è un'immagine raster (ad es., un PSD vettoriale). | Verifica il formato del file sorgente o usa `image instanceof RasterImage` prima del cast. |
| **La modifica della luminosità non ha effetto** | L'immagine non è stata memorizzata nella cache prima della regolazione. | Chiama `rasterImage.cacheData()` come mostrato nel Passo 1. |
| **Il file salvato appare corrotto** | Configurazione errata di `TiffOptions`. | Assicurati che `bitsPerSample` corrisponda alla profondità dell'immagine sorgente (solitamente 8 bit per canale). |

## Domande frequenti

### Q1: Posso regolare la luminosità in altri formati immagine oltre al PSD?

A1: Sì, Aspose.PSD per Java supporta vari formati immagine come JPEG, PNG e TIFF.

### Q2: Come posso gestire gli errori durante il processo di regolazione dell'immagine?

A2: Puoi implementare la gestione degli errori usando blocchi try‑catch per gestire le eccezioni che possono verificarsi.

### Q3: Esiste un limite all'intervallo di regolazione della luminosità?

A3: L'intervallo di regolazione dipende dal contenuto e dal formato dell'immagine, ma Aspose.PSD offre flessibilità nella personalizzazione.

### Q4: Posso usare Aspose.PSD per Java in progetti commerciali?

A4: Sì, Aspose.PSD per Java è una libreria commerciale e puoi ottenere una licenza da [qui](https://purchase.aspose.com/buy).

### Q5: È disponibile una versione di prova gratuita per Aspose.PSD per Java?

A5: Sì, puoi esplorare la libreria con una prova gratuita da [qui](https://releases.aspose.com/).

### Q6: Il metodo `adjustBrightness` influisce sulla visibilità dei livelli?

A6: Il metodo opera sull'immagine composita rasterizzata, quindi la visibilità dei livelli è rispettata durante la rasterizzazione.

### Q7: Posso concatenare più regolazioni (ad es., contrasto, saturazione) insieme?

A7: Assolutamente. Dopo aver regolato la luminosità, puoi chiamare `adjustContrast`, `adjustSaturation`, ecc., sulla stessa istanza di `RasterImage`.

---

**Ultimo aggiornamento:** 2025-12-19  
**Testato con:** Aspose.PSD per Java 24.12 (ultima versione al momento della stesura)  
**Autore:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}