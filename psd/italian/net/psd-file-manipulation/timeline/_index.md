---
title: Lavorare con Timeline in Aspose.PSD per .NET
linktitle: Lavorare con la sequenza temporale
second_title: API Aspose.PSD .NET
description: Migliora la manipolazione delle immagini PSD con Aspose.PSD per la classe Timeline .NET. Controlla le proprietà dei fotogrammi, gli stati dei livelli e libera le possibilità creative senza sforzo.
type: docs
weight: 16
url: /it/net/psd-file-manipulation/timeline/
---
## Introduzione
Nel dinamico mondo della progettazione grafica e della manipolazione delle immagini, la capacità di controllare e manipolare la sequenza temporale delle immagini è fondamentale. Aspose.PSD per .NET fornisce una potente soluzione con la sua classe Timeline. Questa funzionalità di alto livello consente agli utenti di apportare modifiche alla sequenza temporale di PsdImage, come alterare il ritardo dei fotogrammi, modificare gli stati dei livelli su fotogrammi specifici e altro ancora.
## Prerequisiti
Prima di immergerti nelle entusiasmanti possibilità offerte dalla classe Timeline, assicurati di possedere i seguenti prerequisiti:
-  Aspose.PSD per .NET Library: assicurati di avere installato la libreria Aspose.PSD per .NET. Puoi scaricarlo da[Aspose.PSD per la documentazione .NET](https://reference.aspose.com/psd/net/).
-  Directory di documenti e output: definisci i percorsi per le directory di documenti e output nel codice. Regola il`baseDir` E`outputDir` variabili in base alla struttura del progetto.
Ora esploriamo come utilizzare la classe Timeline passo dopo passo.
## Importa spazi dei nomi
Per iniziare a lavorare con la classe Timeline, importa gli spazi dei nomi necessari nel tuo codice:
```csharp
using System;
using System.Collections.Generic;
using System.IO;
using Aspose.PSD.FileFormats.Core.Blending;
using Aspose.PSD.FileFormats.Psd;
using Aspose.PSD.FileFormats.Psd.Layers.Animation;
```
## Passaggio 1: carica l'immagine PSD
Inizia caricando l'immagine PSD dal file sorgente specificato. Assicurati che il percorso del file di origine sia impostato correttamente:
```csharp
string sourceFile = Path.Combine(baseDir, "image1219.psd");
using (PsdImage psdImage = (PsdImage)Image.Load(sourceFile))
{
    //Il tuo codice per ulteriori operazioni va qui
}
```
## Passaggio 2: accedi alla sequenza temporale
Una volta caricata l'immagine PSD, accedi alla Timeline utilizzando il seguente codice:
```csharp
Timeline timeline = psdImage.Timeline;
```
## Passaggio 3: modificare il metodo di smaltimento
Manipolare il metodo di smaltimento di un frame specifico. In questo esempio, modifichiamo il metodo di smaltimento del frame 1:
```csharp
timeline.Frames[0].DisposalMethod = FrameDisposalMethod.DoNotDispose;
```
## Passaggio 4: regola il ritardo del frame
Modificare il ritardo di un particolare frame. Qui, modifichiamo il ritardo del frame 2 in 15:
```csharp
timeline.Frames[1].Delay = 15;
```
## Passaggio 5: modifica lo stato del livello
Cambia l'opacità del "Livello 1" su un fotogramma specifico. In questo caso, impostiamo l'opacità su 50 sul fotogramma 2:
```csharp
LayerState layerState11 = timeline.Frames[1].LayerStates[1];
layerState11.Opacity = 50;
```
## Passaggio 6: sposta il livello
Sposta il "Livello 1" nell'angolo in basso a sinistra su un fotogramma specifico (fotogramma 3 in questo esempio):
```csharp
LayerState layerState21 = timeline.Frames[2].LayerStates[1];
layerState21.PositionOffset = new Point(-50, 230);
```
## Passaggio 7: aggiungi una nuova cornice
Aggiungi un nuovo fotogramma alla timeline:
```csharp
List<Frame> frames = new List<Frame>(timeline.Frames);
frames.Add(new Frame());
timeline.Frames = frames.ToArray();
```
## Passaggio 8: modifica la modalità di fusione
Modifica la modalità di fusione di "Livello 1" su un fotogramma specifico (fotogramma 4 in questo caso):
```csharp
LayerState layerState31 = timeline.Frames[3].LayerStates[1];
layerState31.BlendMode = BlendMode.Dissolve;
```
## Passaggio 9: salva le modifiche
Applica nuovamente le modifiche all'istanza PsdImage e salva l'immagine PSD modificata:
```csharp
psdImage.Save(outputPsd);
```
## Passaggio 10: pulizia
Infine, ripulisci eliminando il file di output temporaneo:
```csharp
File.Delete(outputPsd);
```
## Conclusione

In conclusione, la classe Timeline in Aspose.PSD per .NET consente agli sviluppatori di avere un controllo granulare sulla sequenza temporale delle immagini PSD. Attraverso una serie di semplici passaggi, puoi manipolare le proprietà dei fotogrammi, gli stati dei livelli e altro ancora, aprendo un regno di possibilità creative.

## Domande frequenti

### Q1: Aspose.PSD per .NET è adatto ai principianti?

R1: Assolutamente! Aspose.PSD per .NET fornisce un'interfaccia intuitiva e una documentazione completa, rendendola accessibile sia ai principianti che agli sviluppatori esperti.

### Q2: Posso applicare modifiche alla timeline alle immagini GIF?

A2: La classe Timeline è progettata specificamente per le immagini PSD. Per la manipolazione delle GIF, fare riferimento ad Aspose.GIF per .NET.

### Q3: Dove posso trovare ulteriore supporto o discutere i problemi?

 A3: Visita il[Forum Aspose.PSD](https://forum.aspose.com/c/psd/34) per il supporto della comunità e le discussioni sui problemi.

### Q4: Come posso ottenere una licenza temporanea per Aspose.PSD per .NET?

 A4: acquisire una licenza temporanea[Qui](https://purchase.aspose.com/temporary-license/).

### Q5: Quali sono i principali vantaggi dell'utilizzo di Aspose.PSD per .NET?

A5: Aspose.PSD per .NET offre funzionalità avanzate di elaborazione delle immagini, manipolazione di file PSD e rendering ad alte prestazioni.