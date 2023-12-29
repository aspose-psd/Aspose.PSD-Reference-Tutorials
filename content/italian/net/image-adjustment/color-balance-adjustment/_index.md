---
title: Applicazione della regolazione del bilanciamento del colore in Aspose.PSD per .NET
linktitle: Applicazione della regolazione del bilanciamento del colore
second_title: API Aspose.PSD .NET
description: Migliora i colori delle immagini PSD senza sforzo con Aspose.PSD per la funzione di regolazione del bilanciamento del colore di .NET. Segui la nostra guida passo passo per risultati sorprendenti.
type: docs
weight: 14
url: /it/net/image-adjustment/color-balance-adjustment/
---
## introduzione

Benvenuti in questa guida completa sull'applicazione della regolazione del bilanciamento del colore in Aspose.PSD per .NET! Aspose.PSD è una potente libreria .NET che consente agli sviluppatori di lavorare in modo efficiente con i file PSD. In questo tutorial, ci concentreremo sulla funzione di regolazione del bilanciamento del colore, che ti consente di migliorare facilmente il bilanciamento del colore delle tue immagini PSD.

## Prerequisiti

Prima di immergerci nel tutorial, assicurati di disporre dei seguenti prerequisiti:

-  Aspose.PSD per .NET Library: scarica e installa la libreria da[Sito web Aspose.PSD](https://releases.aspose.com/psd/net/).
- Ambiente di sviluppo: assicurati di avere un ambiente di sviluppo .NET funzionante configurato sul tuo computer.
- File PSD: tieni pronto un file PSD a cui desideri applicare la regolazione del bilanciamento del colore.

## Importa spazi dei nomi

Nel tuo progetto .NET, includi gli spazi dei nomi necessari per utilizzare le funzionalità Aspose.PSD. Aggiungi le seguenti righe al tuo codice:

```csharp
using Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers;
```

Ora suddividiamo il processo di regolazione del bilanciamento del colore in più passaggi:

## Passaggio 1: carica il file PSD

```csharp
string dataDir = "Your Document Directory";
var filePath = dataDir + "ColorBalance.psd";
var outputPath = dataDir + "ColorBalance_out.psd";

using (var im = (FileFormats.Psd.PsdImage)Image.Load(filePath))
{
    // Il codice per la regolazione del bilanciamento del colore verrà aggiunto nei passaggi seguenti.
}
```

## Passaggio 2: accedi e regola il bilanciamento del colore

```csharp
foreach (var layer in im.Layers)
{
    var cbLayer = layer as ColorBalanceAdjustmentLayer;
    if (cbLayer != null)
    {
        cbLayer.ShadowsCyanRedBalance = 30;
        cbLayer.ShadowsMagentaGreenBalance = -15;
        cbLayer.ShadowsYellowBlueBalance = 40;
        cbLayer.MidtonesCyanRedBalance = -90;
        cbLayer.MidtonesMagentaGreenBalance = -25;
        cbLayer.MidtonesYellowBlueBalance = 20;
        cbLayer.HighlightsCyanRedBalance = -30;
        cbLayer.HighlightsMagentaGreenBalance = 67;
        cbLayer.HighlightsYellowBlueBalance = -95;
        cbLayer.PreserveLuminosity = true;
    }
}
```

## Passaggio 3: salvare l'immagine modificata

```csharp
im.Save(outputPath);
```

Ora hai applicato con successo la regolazione del bilanciamento del colore al tuo file PSD utilizzando Aspose.PSD per .NET!

## Conclusione

Congratulazioni! Hai imparato come migliorare il bilanciamento del colore delle tue immagini PSD con Aspose.PSD per .NET. Sperimenta diversi valori di equilibrio per ottenere gli effetti visivi desiderati.

## Domande frequenti

### Q1: Posso applicare la regolazione del bilanciamento del colore a più livelli?

R1: Sì, puoi scorrere tutti i livelli del tuo file PSD e regolare il bilanciamento del colore secondo necessità.

### Q2: Aspose.PSD per .NET è adatto per l'elaborazione batch di file PSD?

A2: Assolutamente! Aspose.PSD fornisce efficienti funzionalità di elaborazione batch per i file PSD.

### Q3: Come posso ottenere una licenza temporanea per Aspose.PSD per .NET?

 A3: Visita[Licenza temporanea Aspose.PSD](https://purchase.aspose.com/temporary-license/) per una licenza temporanea.

### Q4: Dove posso trovare altri esempi e documentazione?

 A4: Esplora il[Documentazione Aspose.PSD](https://reference.aspose.com/psd/net/) per esempi e guide dettagliate.

### Q5: quali opzioni di supporto sono disponibili per Aspose.PSD per .NET?

 A5: Visita il[Forum Aspose.PSD](https://forum.aspose.com/c/psd/34) per il supporto e le discussioni della comunità.
