---
title: Ritaglio di file PSD durante la conversione in PNG in Aspose.PSD per .NET
linktitle: Ritaglio di file PSD durante la conversione in PNG
second_title: API Aspose.PSD .NET
description: Scopri come ritagliare i file PSD senza sforzo utilizzando Aspose.PSD per .NET. Segui la nostra guida passo passo per una conversione senza problemi in PNG.
type: docs
weight: 18
url: /it/net/psd-file-manipulation/crop-psd-conversion-png/
---
## introduzione
Nell'ambito dello sviluppo .NET, la manipolazione e la conversione delle immagini è un compito comune. Aspose.PSD per .NET fornisce un potente set di strumenti per semplificare questo processo. Un requisito frequente è ritagliare i file PSD prima di convertirli in PNG. In questo tutorial passo passo, approfondiremo il processo utilizzando Aspose.PSD per .NET.
## Prerequisiti
Prima di intraprendere questo viaggio, assicurati di avere quanto segue:
-  Aspose.PSD per .NET Library: scarica e installa la libreria da[Aspose.PSD per la documentazione .NET](https://reference.aspose.com/psd/net/).
- File PSD di esempio: tieni un file PSD pronto per la sperimentazione. Se non ne hai uno, puoi utilizzare l'esempio fornito nel tutorial.
- Ambiente .NET: assicurati di avere configurato un ambiente di sviluppo .NET funzionante.
- Directory dei documenti: specificare il percorso della directory dei documenti nel codice.
## Importa spazi dei nomi
Nel tuo progetto .NET, includi gli spazi dei nomi necessari per Aspose.PSD per .NET:
```csharp
using Aspose.PSD.ImageOptions;
```
## Passaggio 1: carica l'immagine PSD
```csharp
// Il percorso della directory dei documenti.
string dataDir = "Your Document Directory";
string srcPath = dataDir + @"sample.psd";
// Carica un'immagine PSD esistente
using (RasterImage image = (RasterImage)Image.Load(srcPath))
{
    // Il tuo codice per i passaggi successivi verrà inserito qui
}
```
## Passaggio 2: Definire il rettangolo di ritaglio
```csharp
// Crea un'istanza della classe Rectangle passando x, y, larghezza e altezza
Rectangle cropRectangle = new Rectangle(0, 0, 350, 450);
```
## Passaggio 3: ritaglia l'immagine
```csharp
//Chiama il metodo crop della classe Image e passa l'istanza della classe rettangolo
image.Crop(cropRectangle);
```
## Passaggio 4: specificare le opzioni PNG
```csharp
// Crea un'istanza della classe PngOptions
PngOptions pngOptions = new PngOptions();
```
## Passaggio 5: salva l'immagine ritagliata come PNG
```csharp
// Chiama il metodo di salvataggio, fornisci il percorso di output e PngOptions per convertire il file PSD in PNG e salvare l'output
string destName = dataDir + @"export.png";
image.Save(destName, pngOptions);
```
## Conclusione

Congratulazioni! Hai imparato con successo come ritagliare i file PSD durante la conversione in PNG utilizzando Aspose.PSD per .NET. Questa funzionalità può essere preziosa in vari scenari di elaborazione delle immagini.

## Domande frequenti

### Q1: Posso utilizzare questa libreria in un progetto commerciale?

 A1: Sì, Aspose.PSD per .NET è disponibile per uso commerciale. Fare riferimento a[Licenza Aspose.PSD](https://purchase.aspose.com/buy) per dettagli.

### Q2: È disponibile una prova gratuita?

 A2: Assolutamente! Puoi esplorare una versione di prova gratuita[Qui](https://releases.aspose.com/).

### Q3: Dove posso trovare supporto per Aspose.PSD per .NET?

 A3: Visita il[Aspose.PSD Forum](https://forum.aspose.com/c/psd/34) per qualsiasi assistenza o domanda.

### Q4: Come posso ottenere una licenza temporanea?

 R4: Se hai bisogno di una licenza temporanea, puoi ottenerne una[Qui](https://purchase.aspose.com/temporary-license/).

### Q5: Sono presenti esempi o tutorial disponibili nella documentazione?

 R5: Sì, è possibile trovare documentazione ed esempi completi[Qui](https://reference.aspose.com/psd/net/).