---
title: Aggiunta di effetti tratto ai livelli in Aspose.PSD per .NET
linktitle: Aggiunta di effetti tratto ai livelli
second_title: API Aspose.PSD .NET
description: Migliora l'estetica dell'immagine con Aspose.PSD per .NET. Impara ad aggiungere effetti di tratto passo dopo passo. Scarica, acquista o prova subito la versione di prova gratuita.
weight: 10
url: /it/net/layer-effects/adding-stroke-effects/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aggiunta di effetti tratto ai livelli in Aspose.PSD per .NET

## Introduzione

Benvenuti in questo tutorial passo passo sull'aggiunta di effetti tratto ai livelli in Aspose.PSD per .NET. Migliorare l'attrattiva visiva delle tue immagini è un gioco da ragazzi con l'effetto tratto e Aspose.PSD lo rende perfetto per gli sviluppatori .NET. In questa guida ti guideremo attraverso il processo, fornendo passaggi chiari ed esempi per aiutarti a padroneggiare questa potente funzionalità.

## Prerequisiti

Prima di immergerci nel tutorial, assicurati di disporre dei seguenti prerequisiti:

- Aspose.PSD per .NET: scarica e installa la libreria Aspose.PSD da[sito web](https://releases.aspose.com/psd/net/).

- Directory dei documenti: prepara una directory contenente il documento PSD a cui desideri applicare gli effetti del tratto.

- Directory di output: dispone di una directory separata per archiviare le immagini di output con effetti tratto.

- Visual Studio: assicurati di avere configurato Visual Studio o qualsiasi altro ambiente di sviluppo .NET preferito.

## Importa spazi dei nomi

Nel tuo progetto .NET, includi gli spazi dei nomi necessari per sfruttare la funzionalità Aspose.PSD:

```csharp
using System;
using System.IO;
using Aspose.PSD.FileFormats.Psd;
using Aspose.PSD.FileFormats.Psd.Layers.FillSettings;
using Aspose.PSD.FileFormats.Psd.Layers.LayerEffects;
using Aspose.PSD.ImageLoadOptions;
using Aspose.PSD.ImageOptions;
```

## Passaggio 1: carica il documento PSD

```csharp
string srcFile = Path.Combine(SourceDir, "AddStrokeEffect.psd");
string outputFilePng = Path.Combine(OutputDir, "AddStrokeEffect.png");

using (var psdImage = (PsdImage)Image.Load(srcFile, new PsdLoadOptions() { LoadEffectsResource = true }))
{
    // Il tuo codice per caricare il documento PSD va qui
}
```

## Passaggio 2: aggiungi l'effetto tratto di colore

```csharp
// Aggiunge il riempimento Colore, nella posizione Interno
strokeEffect = psdImage.Layers[1].BlendingOptions.AddStroke(FillType.Color);
strokeEffect.Size = 7;
strokeEffect.Position = StrokePosition.Inside;
colorFillSettings = strokeEffect.FillSettings as IColorFillSettings;
colorFillSettings.Color = Color.Green;
```

## Passaggio 3: posizione esterna

```csharp
// Aggiunge il riempimento colore, nella posizione Esterno
strokeEffect = psdImage.Layers[2].BlendingOptions.AddStroke(FillType.Color);
strokeEffect.Size = 7;
strokeEffect.Position = StrokePosition.Outside;
colorFillSettings = strokeEffect.FillSettings as IColorFillSettings;
colorFillSettings.Color = Color.Green;
```

## Passaggio 4: posizione centrale

```csharp
// Aggiunge il riempimento colore, nella posizione Centro
strokeEffect = psdImage.Layers[3].BlendingOptions.AddStroke(FillType.Color);
strokeEffect.Size = 7;
strokeEffect.Position = StrokePosition.Center;
colorFillSettings = strokeEffect.FillSettings as IColorFillSettings;
colorFillSettings.Color = Color.Green;
```

Ripeti passaggi simili per i riempimenti sfumati e a motivo, regolando le impostazioni di conseguenza.

## Conclusione

Congratulazioni! Hai imparato con successo come aggiungere effetti di tratto ai livelli utilizzando Aspose.PSD per .NET. Sperimenta diverse impostazioni per ottenere l'impatto visivo desiderato nelle tue immagini.

## Domande frequenti

### Q1: Posso applicare effetti tratto solo a livelli specifici?

R1: Sì, puoi scegliere come target livelli specifici modificando l'indice dei livelli nel codice.

### Q2: Aspose.PSD è compatibile con l'ultimo framework .NET?

A2: Assolutamente! Aspose.PSD è progettato per integrarsi perfettamente con gli ultimi framework .NET.

### Q3: Come posso personalizzare il colore del tratto?

 A3: Modifica semplicemente il file`Color` proprietà nel codice per ottenere il colore del tratto desiderato.

### Q4: Aspose.PSD supporta l'elaborazione batch per più file PSD?

R4: Sì, puoi scorrere più file PSD e applicare l'effetto tratto utilizzando un approccio simile.

### Q5: Posso utilizzare la versione di prova prima di acquistare Aspose.PSD?

 A5: Certamente! Prendi il[prova gratuita](https://releases.aspose.com/) per esplorare le capacità di Aspose.PSD prima di effettuare un acquisto.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
