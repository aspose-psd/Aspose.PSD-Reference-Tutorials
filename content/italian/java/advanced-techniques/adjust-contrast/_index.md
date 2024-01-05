---
title: Regola il contrasto di un'immagine con Aspose.PSD per Java
linktitle: Regola il contrasto di un'immagine
second_title: API Java Aspose.PSD
description: Esplora il mondo della regolazione del contrasto delle immagini in Java con Aspose.PSD. Segui la nostra guida passo passo per una manipolazione perfetta delle immagini.
type: docs
weight: 22
url: /it/java/advanced-techniques/adjust-contrast/
---
## introduzione

Nel campo dell'elaborazione delle immagini con Java, Aspose.PSD si distingue come uno strumento potente. Tra le sue innumerevoli funzionalità, la regolazione del contrasto dell'immagine è un requisito comune. Questo tutorial ti guiderà attraverso il processo di regolazione del contrasto dell'immagine utilizzando Aspose.PSD per Java. Che tu sia uno sviluppatore esperto o che tu abbia appena iniziato, questa guida ti aiuterà a padroneggiare questo aspetto essenziale della manipolazione delle immagini.

## Prerequisiti

Prima di immergerti nel tutorial, assicurati di disporre dei seguenti prerequisiti:

- Conoscenza di base della programmazione Java.
-  Aspose.PSD per la libreria Java installata. Puoi scaricarlo[Qui](https://releases.aspose.com/psd/java/).

## Importa pacchetti

Per iniziare, devi importare i pacchetti necessari nel tuo progetto Java. Aggiungi le seguenti righe al tuo codice:

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.psd.fileformats.tiff.enums.TiffPhotometrics;
import com.aspose.psd.imageoptions.TiffOptions;
```

## Passaggio 1: caricare l'immagine

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

// Carica un'immagine esistente in un'istanza della classe RasterImage
Image image = Image.load(sourceFile);
```

 In questo passaggio, carichiamo l'immagine di esempio ("sample.psd") utilizzando il file`Image.load` metodo.

## Passaggio 2: trasmettere a RasterImage e memorizzare nella cache i dati

```java
// Trasmetti l'oggetto Image a RasterImage
RasterImage rasterImage = (RasterImage)image;

// Controlla se RasterImage è memorizzato nella cache e memorizza nella cache RasterImage per prestazioni migliori
if (!rasterImage.isCached()) {
    rasterImage.cacheData();
}
```

 Qui, lanciamo il generico`Image` opporsi ad a`RasterImage` per lavorazioni specifiche. La memorizzazione nella cache dei dati dell'immagine migliora le prestazioni.

## Passaggio 3: regola il contrasto

```java
// Regola il contrasto
rasterImage.adjustContrast(50);
```

 IL`adjustContrast`Il metodo viene utilizzato per modificare il contrasto dell'immagine. In questo esempio, il contrasto è aumentato del 50%.

## Passaggio 4: crea TiffOptions e salva

```java
// Crea un'istanza di TiffOptions per l'immagine risultante
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
int[] ushort = { 8, 8, 8 };
tiffOptions.setBitsPerSample(ushort);
tiffOptions.setPhotometric(TiffPhotometrics.Rgb);

// Salva l'immagine risultante in formato TIFF
String destName = dataDir + "AdjustContrast_out.tiff";
rasterImage.save(destName, tiffOptions);
```

 Ecco, ci siamo sistemati`TiffOptions` per l'immagine di output, specificando il formato e altre proprietà. L'immagine finale viene quindi salvata in un file TIFF.

## Conclusione

Congratulazioni! Hai regolato con successo il contrasto di un'immagine utilizzando Aspose.PSD per Java. Questo tutorial ha coperto i passaggi essenziali, dall'importazione dei pacchetti al salvataggio dell'immagine elaborata.

## Domande frequenti

### Q1: Aspose.PSD è compatibile con diversi formati di immagine?

A1: Sì, Aspose.PSD supporta vari formati di immagine, offrendo flessibilità nei tuoi progetti.

### Q2: Come posso ottenere una licenza temporanea per Aspose.PSD?

 A2: Puoi ottenere una licenza temporanea[Qui](https://purchase.aspose.com/temporary-license/).

### Q3: Dove posso trovare la documentazione Aspose.PSD?

A3: La documentazione è disponibile[Qui](https://reference.aspose.com/psd/java/).

### Q4: Quali opzioni di supporto sono disponibili per Aspose.PSD?

 R4: Per supporto, visitare il[Forum Aspose.PSD](https://forum.aspose.com/c/psd/34).

### Q5: Posso acquistare Aspose.PSD?

 A5: Sì, puoi acquistare Aspose.PSD[Qui](https://purchase.aspose.com/buy).