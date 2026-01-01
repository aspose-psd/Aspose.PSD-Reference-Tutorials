---
date: 2026-01-01
description: Scopri come ritagliare un'immagine in Java usando Aspose.PSD per Java.
  Segui la nostra guida passo‑passo per caricare un file PSD, ritagliare un rettangolo
  dell'immagine e convertire il PSD in JPEG.
linktitle: Crop Image by Rectangle
second_title: Aspose.PSD Java API
title: 'Ritaglia immagine Java: Ritaglia immagine per rettangolo con Aspose.PSD'
url: /it/java/image-editing/crop-image-by-rectangle/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Ritaglia immagine Java: Ritaglia immagine per rettangolo con Aspose.PSD

## Introduzione

Manipolare la grafica è una parte di routine del **java image processing**, e Aspose.PSD per Java ti offre un'API pulita e ad alte prestazioni per lavorare con file PSD. In questo tutorial imparerai **come ritagliare un'immagine** usando un rettangolo, caricare un file PSD e infine convertire il risultato in JPEG—tutto con poche righe di codice Java.

## Risposte rapide
- **Che cosa significa “crop image java”?** Si riferisce al ritaglio di un'immagine a un rettangolo definito usando codice Java.  
- **Quale libreria gestisce l'operazione?** Aspose.PSD per Java fornisce le classi necessarie.  
- **È necessaria una licenza per i test?** È disponibile una versione di prova gratuita; è richiesta una licenza per la produzione.  
- **Posso convertire il PSD ritagliato in JPEG?** Sì—usa `JpegOptions` durante il salvataggio.  
- **Quanto tempo richiede l'implementazione?** Di solito meno di 10 minuti per uno scenario base.

## Che cos'è il ritaglio di un rettangolo di immagine in Java?

Il ritaglio di un rettangolo di immagine significa selezionare un'area specifica (definita da X, Y, larghezza e altezza) e scartare tutto ciò che si trova al di fuori di quell'area. Questa operazione è comune quando è necessario concentrarsi su una regione particolare di un documento PSD più grande.

## Perché usare Aspose.PSD per questo compito?

- **Nessuna dipendenza esterna** – funziona con Java puro.  
- **Supporta PSD, PNG, JPEG e molti altri formati** – puoi **convertire PSD in JPEG** istantaneamente.  
- **Rendering ad alta fedeltà** – mantiene le informazioni dei livelli e i profili colore durante il ritaglio.  

## Prerequisiti

- Java Development Kit (JDK) installato.  
- Aspose.PSD for Java library – scaricala dal [sito web](https://releases.aspose.com/psd/java/).  

## Importa pacchetti

Assicurati di includere i pacchetti necessari nel tuo progetto Java per sfruttare le capacità di Aspose.PSD per Java. Aggiungi le seguenti istruzioni di importazione all'inizio del tuo file Java:

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;
import com.aspose.psd.Rectangle;

import com.aspose.psd.imageoptions.JpegOptions;
```

Ora, suddividiamo il processo in più passaggi per guidarti nel ritaglio di un'immagine per rettangolo usando Aspose.PSD per Java.

## Passo 1: Configura la directory del documento

```java
String dataDir = "Your Document Directory";
```

Sostituisci `"Your Document Directory"` con il percorso reale in cui si trova il tuo file PSD.

## Passo 2: Specifica i file di origine e destinazione

```java
String sourceFile = dataDir + "sample.psd";
String destName = dataDir + "CroppingByRectangle_out.jpg";
```

Definisci i percorsi per il tuo file PSD di origine e il file JPEG di destinazione.

## Passo 3: Carica e memorizza nella cache l'immagine

```java
RasterImage rasterImage = (RasterImage)Image.load(sourceFile);

if (!rasterImage.isCached()) {
    rasterImage.cacheData();
}
```

Qui **carichiamo il file PSD** in un'istanza `RasterImage` e memorizziamo nella cache i suoi dati per migliorare le prestazioni.

## Passo 4: Crea e definisci il rettangolo di ritaglio

```java
Rectangle rectangle = new Rectangle(20, 20, 20, 20);
```

Crea un'istanza della classe `Rectangle` con le dimensioni desiderate per il ritaglio. I parametri rappresentano rispettivamente **X**, **Y**, **larghezza** e **altezza**.

## Passo 5: Ritaglia e salva l'immagine

```java
rasterImage.crop(rectangle);
rasterImage.save(destName, new JpegOptions());
```

Esegui l'operazione di ritaglio usando il rettangolo specificato e **converti PSD in JPEG** salvando il risultato con `JpegOptions`.

Ripeti questi passaggi secondo necessità, regolando i parametri in base alle tue esigenze specifiche.

## Problemi comuni e suggerimenti

- **Rettangolo fuori dai limiti dell'immagine** – assicurati che le coordinate del rettangolo siano entro le dimensioni dell'immagine di origine.  
- **Consumo di memoria** – chiama `rasterImage.dispose()` al termine per liberare le risorse native.  
- **Controllo della qualità** – puoi impostare `JpegOptions.setQuality(int)` per controllare il livello di compressione del JPEG di output.  

## Conclusione

In questo tutorial abbiamo illustrato il processo di **crop image java** per rettangolo usando Aspose.PSD per Java. Seguendo questi passaggi puoi integrare facilmente potenti capacità di manipolazione delle immagini—caricamento di un file PSD, ritaglio di una regione specifica e conversione del risultato in JPEG—in qualsiasi applicazione Java.

## FAQ

### Q1: Posso usare Aspose.PSD per Java con altri framework Java?

R1: Sì, Aspose.PSD per Java può essere integrato con vari framework Java, offrendo flessibilità nei tuoi progetti di sviluppo.

### Q2: È disponibile una versione di prova gratuita per Aspose.PSD per Java?

R2: Sì, puoi accedere alla versione di prova gratuita [qui](https://releases.aspose.com/).

### Q3: Dove posso trovare supporto o assistenza aggiuntivi?

R3: Visita il [forum di Aspose.PSD](https://forum.aspose.com/c/psd/34) per supporto della community e discussioni.

### Q4: Come posso ottenere una licenza temporanea per Aspose.PSD per Java?

R4: Puoi ottenere una licenza temporanea [qui](https://purchase.aspose.com/temporary-license/).

### Q5: Quali sono i formati immagine supportati per il ritaglio in Aspose.PSD per Java?

R5: Aspose.PSD per Java supporta vari formati immagine, inclusi PSD, PNG, JPEG e altri.

---

**Ultimo aggiornamento:** 2026-01-01  
**Testato con:** Aspose.PSD for Java 24.12  
**Autore:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}