---
title: Regola la gamma di un'immagine con Aspose.PSD per Java
linktitle: Regola la gamma di un'immagine
second_title: API Java Aspose.PSD
description: Impara a regolare la gamma dell'immagine senza sforzo utilizzando Aspose.PSD per Java. Segui la nostra guida passo passo per ottenere risultati ottimali.
weight: 23
url: /it/java/advanced-techniques/adjust-gamma/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Regola la gamma di un'immagine con Aspose.PSD per Java

## Introduzione

Nel campo dell'elaborazione delle immagini, la regolazione della gamma di un'immagine è un passaggio cruciale per migliorarne l'attrattiva visiva. Aspose.PSD per Java offre una potente soluzione per gli sviluppatori Java per manipolare senza sforzo la gamma delle immagini. In questo tutorial esploreremo come regolare la gamma utilizzando Aspose.PSD, analizzando ogni passaggio per garantire un'implementazione senza problemi.

## Prerequisiti

Prima di immergerti nel tutorial, assicurati di aver impostato i seguenti prerequisiti:

1. Ambiente di sviluppo Java: assicurati di avere un ambiente di sviluppo Java installato sul tuo sistema.
2.  Libreria Aspose.PSD: scarica e integra la libreria Aspose.PSD nel tuo progetto Java. Puoi trovare le risorse necessarie in[documentazione](https://reference.aspose.com/psd/java/).
3. Immagine campione: prepara un'immagine PSD campione che utilizzerai per applicare la regolazione della gamma.

## Importa pacchetti

Per avviare il processo, importa i pacchetti richiesti nel tuo progetto Java. Ciò pone le basi per l'utilizzo delle funzionalità Aspose.PSD senza problemi.

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.psd.fileformats.tiff.enums.TiffPhotometrics;
import com.aspose.psd.imageoptions.TiffOptions;
```

## Passaggio 1: caricare l'immagine

 Inizia caricando l'immagine PSD di esempio in un'istanza del file`RasterImage` classe. Questa è la base per le successive regolazioni della gamma.

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

// Carica un'immagine esistente in un'istanza della classe RasterImage
Image image = Image.load(sourceFile);

// Trasmetti l'oggetto Image a RasterImage
RasterImage rasterImage = (RasterImage)image;

// Controlla se RasterImage è memorizzato nella cache per prestazioni migliori
if (!rasterImage.isCached()) {
    rasterImage.cacheData();
}
```

## Passaggio 2: regola la gamma

 Ora regola la gamma dell'immagine caricata utilizzando`adjustGamma` metodo. Ottimizza i valori gamma in base alle tue esigenze.

```java
// Regola la gamma
rasterImage.adjustGamma(2.2f, 2.2f, 2.2f);
```

## Passaggio 3: crea TiffOptions

 Crea un'istanza di`TiffOptions` per l'immagine risultante. Imposta varie proprietà, come bit per campione e opzioni fotometriche, per personalizzare l'output in base alle tue specifiche.

```java
// Crea un'istanza di TiffOptions per l'immagine risultante
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
int[] ushort = { 8, 8, 8 };
tiffOptions.setBitsPerSample(ushort);
tiffOptions.setPhotometric(TiffPhotometrics.Rgb);
```

## Passaggio 4: salva l'immagine risultante

 Salvare l'immagine manipolata in formato TIFF utilizzando quello precedentemente definito`TiffOptions`.

```java
// Salva l'immagine risultante in formato TIFF
String destName = dataDir + "AdjustGamma_out.tiff";
rasterImage.save(destName, tiffOptions);
```

## Conclusione

Congratulazioni! Hai regolato con successo la gamma di un'immagine utilizzando Aspose.PSD per Java. Questo processo consente agli sviluppatori di migliorare facilmente la qualità dell'immagine, contribuendo a creare un'esperienza utente visivamente accattivante.

## Domande frequenti

### Q1: dove posso trovare la documentazione Aspose.PSD?

 R1: È possibile accedere alla documentazione all'indirizzo[https://reference.aspose.com/psd/java/](https://reference.aspose.com/psd/java/).

### Q2: Come posso scaricare Aspose.PSD per Java?

 A2: Scarica la libreria da[https://releases.aspose.com/psd/java/](https://releases.aspose.com/psd/java/).

### Q3: Dove posso acquistare Aspose.PSD?

 A3: Visita[https://purchase.aspose.com/buy](https://purchase.aspose.com/buy) per acquistare Aspose.PSD.

### Q4: È disponibile una prova gratuita?

 R4: Sì, puoi esplorare una prova gratuita su[https://releases.aspose.com/](https://releases.aspose.com/).

### Q5: Dove posso cercare supporto per Aspose.PSD?

 R5: Per supporto, visitare il forum Aspose.PSD all'indirizzo[https://forum.aspose.com/c/psd/34](https://forum.aspose.com/c/psd/34).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
