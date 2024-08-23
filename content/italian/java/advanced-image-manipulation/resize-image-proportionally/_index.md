---
title: Ridimensiona l'immagine proporzionalmente con Aspose.PSD per Java
linktitle: Ridimensiona l'immagine proporzionalmente
second_title: API Java Aspose.PSD
description: Migliora le tue applicazioni Java con Aspose.PSD. Segui la nostra guida per ridimensionare le immagini proporzionalmente senza sforzo. Potenzia oggi stesso le tue capacità di gestione delle immagini.
type: docs
weight: 17
url: /it/java/advanced-image-manipulation/resize-image-proportionally/
---
## Introduzione

Benvenuti nella nostra guida passo passo sul ridimensionamento proporzionale delle immagini utilizzando Aspose.PSD per Java. Se stai cercando di migliorare le tue applicazioni Java con efficienti funzionalità di ridimensionamento delle immagini, sei nel posto giusto. In questo tutorial ti guideremo attraverso il processo utilizzando passaggi chiari e concisi.

## Prerequisiti

Prima di immergerti nel tutorial, assicurati di disporre dei seguenti prerequisiti:

1. Ambiente Java: assicurati di avere Java installato sul tuo sistema.
2.  Libreria Aspose.PSD: scarica e installa la libreria Aspose.PSD. Puoi trovare le risorse necessarie[Qui](https://releases.aspose.com/psd/java/).

## Importa pacchetti

Una volta ordinati i prerequisiti, importa i pacchetti richiesti nel tuo progetto Java. Assicurati che la libreria Aspose.PSD sia correttamente referenziata nel tuo progetto.

```java
import com.aspose.psd.Image;

import com.aspose.psd.imageoptions.PngOptions;
```

## Passaggio 1: caricare l'immagine

Inizia caricando l'immagine che desideri ridimensionare nella tua applicazione Java.

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

Image image = Image.load(sourceFile);

if (!image.isCached()) {
    image.cacheData();
}
```

## Passaggio 2: specificare larghezza e altezza

Determina la nuova larghezza e altezza per l'immagine ridimensionata. In questo esempio, ridimensioneremo l'immagine alla metà delle sue dimensioni originali.

```java
int newWidth = image.getWidth() / 2;
image.resizeWidthProportionally(newWidth);

int newHeight = image.getHeight() / 2;
image.resizeHeightProportionally(newHeight);
```

## Passaggio 3: salva l'immagine ridimensionata

Salva l'immagine ridimensionata nella posizione desiderata, specificando le opzioni di formato (PNG, in questo caso).

```java
String destName = dataDir + "SimpleResizeImageProportionally_out.png";
image.save(destName, new PngOptions());
```

Ed ecco qua! Hai ridimensionato con successo un'immagine proporzionalmente utilizzando Aspose.PSD per Java.

## Conclusione

In questo tutorial, abbiamo trattato i passaggi essenziali per ridimensionare le immagini proporzionalmente utilizzando la libreria Aspose.PSD per Java. Ora puoi integrare facilmente questa funzionalità nelle tue applicazioni Java per una migliore gestione delle immagini.

## Domande frequenti

### Q1: Aspose.PSD è compatibile con tutti i formati di immagine?

 R1: Aspose.PSD supporta vari formati di immagine, inclusi PSD, PNG, JPEG e altri. Controlla il[documentazione](https://reference.aspose.com/psd/java/) per un elenco completo.

### Q2: Posso utilizzare Aspose.PSD per progetti commerciali?

 A2: Sì, puoi. Visita il[pagina di acquisto](https://purchase.aspose.com/buy) per i dettagli sulla licenza.

### Q3: Sono disponibili licenze temporanee a scopo di test?

 R3: Sì, puoi ottenere una licenza temporanea[Qui](https://purchase.aspose.com/temporary-license/) per la valutazione.

### Q4: Dove posso trovare supporto per Aspose.PSD?

 A4: Visita il[Forum Aspose.PSD](https://forum.aspose.com/c/psd/34) per il sostegno e l'assistenza della comunità.

### Q5: Come posso accedere alla documentazione Aspose.PSD?

 R5: Fare riferimento alla documentazione dettagliata[Qui](https://reference.aspose.com/psd/java/).
`