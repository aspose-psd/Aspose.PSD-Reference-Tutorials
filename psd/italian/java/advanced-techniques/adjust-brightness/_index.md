---
title: Regola la luminosità di un'immagine con Aspose.PSD per Java
linktitle: Regola la luminosità di un'immagine
second_title: API Java Aspose.PSD
description: Migliora la luminosità dell'immagine in Java con Aspose.PSD. Guida passo passo per regolare la luminosità dell'immagine a livello di codice.
weight: 21
url: /it/java/advanced-techniques/adjust-brightness/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Regola la luminosità di un'immagine con Aspose.PSD per Java

## Introduzione

Il miglioramento delle immagini è un requisito comune nella progettazione grafica e nella fotografia digitale. Aspose.PSD per Java fornisce una potente soluzione per regolare la luminosità dell'immagine a livello di codice. In questo tutorial esploreremo come utilizzare la libreria Aspose.PSD per Java per regolare la luminosità di un'immagine, passo dopo passo.

## Prerequisiti

Prima di immergerti nel tutorial, assicurati di possedere i seguenti prerequisiti:

-  Aspose.PSD per Java Library: scarica e installa la libreria da[Aspose.PSD per la documentazione Java](https://reference.aspose.com/psd/java/).

## Importa pacchetti

Per iniziare, importa i pacchetti necessari nel tuo progetto Java. In questo esempio, utilizzeremo quanto segue:

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.psd.fileformats.tiff.enums.TiffPhotometrics;
import com.aspose.psd.imageoptions.TiffOptions;
```

Ora suddividiamo il processo di regolazione della luminosità di un'immagine in semplici passaggi:

## Passaggio 1: caricare l'immagine

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";
String destName = dataDir + "AdjustBrightness_out.tiff";

// Carica un'immagine esistente in un'istanza della classe RasterImage
Image image = Image.load(sourceFile);
// Trasmetti l'oggetto Image a RasterImage
RasterImage rasterImage = (RasterImage) image;

// Controlla se RasterImage è memorizzato nella cache e memorizza nella cache RasterImage per prestazioni migliori
if (!rasterImage.isCached()) {
    rasterImage.cacheData();
}
```

 In questo passaggio, carichiamo l'immagine di destinazione e la trasmettiamo su a`RasterImage` per ulteriore elaborazione.

## Passaggio 2: regola la luminosità

```java
// Regola la luminosità
rasterImage.adjustBrightness(-50);
```

 Qui usiamo il`adjustBrightness`metodo per modificare la luminosità dell'immagine. In questo esempio riduciamo la luminosità di 50 unità, ma puoi personalizzare questo valore in base alle tue esigenze.

## Passaggio 3: imposta le opzioni Tiff

```java
int[] ushort = {8, 8, 8};
// Crea un'istanza di TiffOptions per l'immagine risultante
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
tiffOptions.setBitsPerSample(ushort);
tiffOptions.setPhotometric(TiffPhotometrics.Rgb);
```

 Configura il`TiffOptions` per salvare l'immagine regolata. Regola il`bitsPerSample` E`photometric` immobili in base alle vostre specifiche esigenze.

## Passaggio 4: salva l'immagine risultante

```java
// Salva l'immagine risultante
rasterImage.save(destName, tiffOptions);
```

 Infine, salva l'immagine modificata utilizzando il file specificato`TiffOptions`.

## Conclusione

La regolazione della luminosità di un'immagine a livello di codice è semplificata con Aspose.PSD per Java. Questo tutorial ha fornito una guida completa sull'implementazione di questa funzionalità nelle tue applicazioni Java.

## Domande frequenti

### Q1: Posso regolare la luminosità in altri formati di immagine oltre a PSD?

A1: Sì, Aspose.PSD per Java supporta vari formati di immagine come JPEG, PNG e TIFF.

### Q2: Come posso gestire gli errori durante il processo di regolazione dell'immagine?

A2: È possibile implementare la gestione degli errori utilizzando i blocchi try-catch per gestire le eccezioni che potrebbero verificarsi.

### Q3: Esiste un limite alla gamma di regolazione della luminosità?

A3: L'intervallo di regolazione dipende dal contenuto e dal formato dell'immagine, ma Aspose.PSD offre flessibilità nella personalizzazione.

### Q4: posso utilizzare Aspose.PSD per Java in progetti commerciali?

 A4: Sì, Aspose.PSD per Java è una libreria commerciale ed è possibile ottenere una licenza da[Qui](https://purchase.aspose.com/buy).

### Q5: È disponibile una prova gratuita per Aspose.PSD per Java?

 R5: Sì, puoi esplorare la libreria con una prova gratuita da[Qui](https://releases.aspose.com/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
