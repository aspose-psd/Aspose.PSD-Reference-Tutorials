---
title: Ritaglio di immagini per turni in Aspose.PSD per .NET
linktitle: Ritaglio delle immagini per turni
second_title: API Aspose.PSD .NET
description: Impara a ritagliare le immagini senza sforzo utilizzando Aspose.PSD per .NET. Segui la nostra guida passo passo per regolazioni precise dell'immagine.
type: docs
weight: 12
url: /it/net/image-manipulation/crop-image-shifts/
---
## Introduzione

Nel regno dello sviluppo .NET, Aspose.PSD si distingue come un potente toolkit per attività di elaborazione delle immagini. Una delle sue caratteristiche degne di nota è la capacità di ritagliare le immagini con precisione, grazie alla funzionalità "Ritaglio per turni". In questa guida passo passo, ti guideremo attraverso il processo di ritaglio delle immagini senza problemi utilizzando Aspose.PSD per .NET.

## Prerequisiti

Prima di approfondire il tutorial, assicurati di disporre dei seguenti prerequisiti:

-  Aspose.PSD per .NET Library: assicurati di avere la libreria installata. In caso contrario, puoi scaricarlo da[pagina di rilascio](https://releases.aspose.com/psd/net/).

- Ambiente .NET: assicurati di avere un ambiente di sviluppo .NET configurato sul tuo computer.

- Immagine di esempio: prepara un'immagine di esempio in formato PSD con cui desideri lavorare.

## Importa spazi dei nomi

Inizia importando gli spazi dei nomi necessari nel tuo progetto .NET. Questi spazi dei nomi forniscono l'accesso alle classi Aspose.PSD e ai metodi richiesti per il ritaglio delle immagini.

```csharp
using Aspose.PSD.ImageOptions;
```

## Passaggio 1: definire la directory dei documenti

Imposta il percorso della directory dei documenti in cui verranno posizionati i file di origine e di destinazione.

```csharp
string dataDir = "Your Document Directory";
```

## Passaggio 2: carica l'immagine sorgente

Carica l'immagine PSD che desideri ritagliare. Assicurati di sostituire "sample.psd" con il nome del file sorgente.

```csharp
string sourceFile = dataDir + @"sample.psd";
string destName = dataDir + @"CroppingByShifts_out.jpg";
```

## Passaggio 3: memorizzare nella cache i dati dell'immagine per prestazioni migliori

Prima di ritagliare, è consigliabile memorizzare nella cache i dati dell'immagine per migliorare le prestazioni.

```csharp
using (RasterImage rasterImage = (RasterImage)Image.Load(sourceFile))
{
    if (!rasterImage.IsCached)
    {
        rasterImage.CacheData();
    }
```

## Passaggio 4: definire i valori di spostamento per il ritaglio

Specificare i valori di spostamento per i lati sinistro, destro, superiore e inferiore dell'immagine. Regola questi valori in base alle tue esigenze di ritaglio.

```csharp
int leftShift = 10;
int rightShift = 10;
int topShift = 10;
int bottomShift = 10;
```

## Passaggio 5: applica il ritaglio e salva i risultati

 Utilizza il`Crop` metodo per applicare gli spostamenti specificati e salvare l'immagine ritagliata nel file di destinazione.

```csharp
rasterImage.Crop(leftShift, rightShift, topShift, bottomShift);
rasterImage.Save(destName, new JpegOptions());
}
```

## Conclusione

Congratulazioni! Hai imparato con successo come ritagliare le immagini per turni utilizzando Aspose.PSD per .NET. Questa potente funzionalità fornisce la precisione e il controllo necessari per varie attività di elaborazione delle immagini.

## Domande frequenti

### Q1: Posso ritagliare immagini di formati diversi, non solo PSD?

R1: Sì, Aspose.PSD supporta vari formati di immagine, consentendoti di ritagliare immagini in formati come JPEG, PNG e altri.

### Q2: È disponibile una versione di prova prima di acquistare Aspose.PSD per .NET?

 A2: Certamente! Puoi esplorare il toolkit con una prova gratuita disponibile[Qui](https://releases.aspose.com/).

### Q3: Come posso ottenere una licenza temporanea per Aspose.PSD per .NET?

 R3: È possibile acquisire una licenza temporanea a scopo di test[Qui](https://purchase.aspose.com/temporary-license/).

### Q4: Dove posso trovare ulteriore supporto e discussioni relative ad Aspose.PSD?

 A4: Visita il[Aspose.PSD Forum](https://forum.aspose.com/c/psd/34) per supporto e discussioni coinvolgenti.

### Q5: Posso acquistare Aspose.PSD per .NET direttamente dal sito web?

 R5: Sì, puoi acquistare la libreria in modo sicuro da[pagina di acquisto](https://purchase.aspose.com/buy).
