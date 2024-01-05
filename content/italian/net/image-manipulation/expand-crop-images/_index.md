---
title: Espansione e ritaglio di immagini in Aspose.PSD per .NET
linktitle: Espansione e ritaglio delle immagini
second_title: API Aspose.PSD .NET
description: Scopri come espandere e ritagliare dinamicamente le immagini utilizzando Aspose.PSD per .NET. Segui la nostra guida passo passo per una manipolazione perfetta delle immagini.
type: docs
weight: 13
url: /it/net/image-manipulation/expand-crop-images/
---
## introduzione

Aspose.PSD per .NET è una libreria di immagini completa che consente agli sviluppatori di lavorare con vari formati di immagine nelle loro applicazioni .NET. Una delle sue caratteristiche più straordinarie è la capacità di manipolare le immagini con facilità. In questo tutorial, ci concentreremo sull'espansione e sul ritaglio delle immagini, fornendoti una guida pratica per realizzare queste attività utilizzando Aspose.PSD.

## Prerequisiti

Prima di immergerti nel tutorial, assicurati di avere i seguenti prerequisiti:

-  Aspose.PSD per .NET Library: assicurati di avere installato la libreria Aspose.PSD per .NET. Puoi scaricarlo da[Aspose.PSD per la documentazione .NET](https://reference.aspose.com/psd/net/).

- Immagine di esempio: prepara un file di immagine di esempio (ad esempio, "example1.psd") che utilizzerai per il tutorial.

Ora iniziamo con la guida passo passo.

## Importa spazi dei nomi

Inizia importando gli spazi dei nomi necessari per sfruttare le funzionalità fornite da Aspose.PSD per .NET. Aggiungi i seguenti spazi dei nomi al tuo codice:

```csharp
using Aspose.PSD.ImageOptions;
```

## Passaggio 1: impostare il progetto

 Assicurati di avere un progetto impostato con Aspose.PSD per .NET integrato. In caso contrario, seguire il[documentazione](https://reference.aspose.com/psd/net/) per l'orientamento.

## Passaggio 2: caricare l'immagine

Carica l'immagine di esempio utilizzando il seguente codice:

```csharp
string dataDir = RunExamples.GetDataDir_DrawingAndFormattingImages();
string sourceFile = dataDir + @"example1.psd";

// Carica l'immagine
using (RasterImage rasterImage = (RasterImage)Image.Load(sourceFile))
{
    // Il codice aggiuntivo per l'elaborazione delle immagini verrà inserito qui
}
```

## Passaggio 3: memorizzare nella cache i dati dell'immagine

Memorizza nella cache i dati dell'immagine per ottimizzare le prestazioni:

```csharp
rasterImage.CacheData();
```

## Passaggio 4: definire il rettangolo di destinazione

Crea un'istanza della classe Rectangle e definisci X, Y, Larghezza e Altezza del rettangolo. Questa sarà l'area in cui l'immagine verrà espansa o ritagliata.

```csharp
Rectangle destRect = new Rectangle { X = -200, Y = -200, Width = 300, Height = 300 };
```

## Passaggio 5: salva l'immagine di output

Salva l'immagine di output con le opzioni specificate e il rettangolo di destinazione:

```csharp
string destName = dataDir + @"jpeg_out.jpg";
rasterImage.Save(destName, new JpegOptions(), destRect);
```

## Conclusione

Congratulazioni! Hai imparato con successo come espandere e ritagliare le immagini utilizzando Aspose.PSD per .NET. Questa potente libreria apre un mondo di possibilità per la manipolazione delle immagini all'interno delle tue applicazioni .NET.

## Domande frequenti

### Q1: Aspose.PSD può gestire altri formati di immagine oltre a PSD?

R1: Sì, Aspose.PSD supporta un'ampia gamma di formati di immagine, inclusi JPEG, PNG, GIF e altri.

### Q2: Dove posso trovare supporto per Aspose.PSD?

 A2: Puoi trovare supporto e interagire con la comunità su[Aspose.PSD Forum](https://forum.aspose.com/c/psd/34).

### Q3 È disponibile una prova gratuita per Aspose.PSD per .NET?

 R3: Sì, puoi esplorare le funzionalità con una prova gratuita disponibile su[Prova gratuita di Aspose.PSD](https://releases.aspose.com/).

### Q4: Come posso ottenere una licenza temporanea per Aspose.PSD?

 A4: Puoi ottenere una licenza temporanea da[Licenza temporanea Aspose.PSD](https://purchase.aspose.com/temporary-license/).

### Q5: Dove posso acquistare Aspose.PSD per .NET?

 A5: Puoi acquistare la libreria presso[Pagina di acquisto Aspose.PSD](https://purchase.aspose.com/buy).