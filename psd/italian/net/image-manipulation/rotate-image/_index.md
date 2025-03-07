---
title: Rotazione di un'immagine in Aspose.PSD per .NET
linktitle: Rotazione di un'immagine
second_title: API Aspose.PSD .NET
description: Impara a ruotare le immagini senza sforzo in .NET con Aspose.PSD. Segui il nostro tutorial passo dopo passo.
weight: 15
url: /it/net/image-manipulation/rotate-image/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Rotazione di un'immagine in Aspose.PSD per .NET

## Introduzione

Se ti stai immergendo nel mondo della manipolazione delle immagini utilizzando .NET, Aspose.PSD è il tuo strumento di riferimento per un'elaborazione delle immagini fluida ed efficiente. In questo tutorial, ci concentreremo su un'attività fondamentale: ruotare un'immagine utilizzando Aspose.PSD per .NET. Seguici mentre suddividiamo il processo in passaggi semplici e attuabili.

## Prerequisiti

Prima di iniziare, assicurati di disporre dei seguenti prerequisiti:

-  Aspose.PSD per .NET Library: scarica e installa la libreria da[Documentazione Aspose.PSD .NET](https://reference.aspose.com/psd/net/).

- La tua directory dei documenti: imposta una directory in cui sono archiviate le tue immagini. Sostituisci "La tua directory dei documenti" nello snippet di codice con il percorso di questa directory.

## Importa spazi dei nomi

Assicurati di includere gli spazi dei nomi necessari per accedere alla funzionalità Aspose.PSD. Aggiungi le seguenti righe all'inizio del tuo progetto .NET:

```csharp
using Aspose.PSD.ImageOptions;
```

## Passaggio 1: caricare l'immagine

```csharp
string sourceFile = dataDir + @"sample.psd";

// Carica un'immagine esistente in un'istanza della classe RasterImage
using (Image image = Image.Load(sourceFile))
{
```

## Passaggio 2: ruotare l'immagine

```csharp
    // Ruota l'immagine di 270 gradi in senso orario
    image.RotateFlip(RotateFlipType.Rotate270FlipNone);
```

## Passaggio 3: salva l'immagine ruotata

```csharp
    // Salva l'immagine ruotata come file JPEG
    string destName = dataDir + @"RotatingAnImage_out.jpg";
    image.Save(destName, new JpegOptions());
}
```

Questo è tutto! Con solo poche righe di codice, hai ruotato con successo un'immagine utilizzando Aspose.PSD per .NET.

## Conclusione

In questo tutorial, abbiamo esplorato le basi della rotazione delle immagini utilizzando Aspose.PSD per .NET. Aspose.PSD fornisce un robusto set di strumenti per la manipolazione delle immagini, rendendolo una libreria essenziale per gli sviluppatori .NET. Sperimenta diverse rotazioni ed esplora ulteriori funzionalità per migliorare i flussi di lavoro di elaborazione delle immagini.

## Domande frequenti

### Q1: Posso ruotare le immagini con un angolo personalizzato utilizzando Aspose.PSD?

 Sì, Aspose.PSD ti consente di specificare un angolo personalizzato per la rotazione. Sostituisci semplicemente il`RotateFlipType.Rotate270FlipNone` linea con l'angolo di rotazione desiderato.

### Q2: Aspose.PSD è compatibile con vari formati di immagine?

 Assolutamente. Aspose.PSD supporta un'ampia gamma di formati di immagine, inclusi PSD, JPEG, PNG e altri. Controlla il[documentazione](https://reference.aspose.com/psd/net/) per l'elenco completo.

### Q3: Come posso ottenere una licenza temporanea per Aspose.PSD?

 Visita il[pagina della licenza temporanea](https://purchase.aspose.com/temporary-license/) sul sito Aspose per ottenere una licenza temporanea a scopo di valutazione.

### Q4: Dove posso trovare supporto per Aspose.PSD?

 Per qualsiasi domanda o assistenza, visitare il[Forum Aspose.PSD](https://forum.aspose.com/c/psd/34) e connettersi con la comunità.

### Q5: Posso acquistare Aspose.PSD per uso commerciale?

 Certamente. Esplora il[pagina di acquisto](https://purchase.aspose.com/buy) per acquisire una licenza su misura per le tue esigenze.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
