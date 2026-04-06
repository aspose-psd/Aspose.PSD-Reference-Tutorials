---
date: 2026-01-07
description: Scopri come ritagliare immagini in Java usando Aspose.PSD per Java. Guida
  passo‑passo per il ritaglio, il ridimensionamento e la conversione da PSD a JPEG.
linktitle: Expand and Crop Images
second_title: Aspose.PSD Java API
title: 'Ritaglia immagine Java - espandi e ritaglia immagini con Aspose.PSD per Java'
url: /it/java/image-editing/expand-and-crop-images/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Crop Image Java: Espandi e Ritaglia Immagini con Aspose.PSD per Java

## Introduzione

In questo tutorial scoprirai come **crop image java** con la libreria Aspose.PSD. Che tu debba espandere una tela, ritagliare bordi indesiderati o convertire un file PSD in JPEG, i passaggi seguenti ti guideranno attraverso un processo pulito e ripetibile. Tratteremo i prerequisiti, le istruzioni di importazione e ogni passaggio di codifica con spiegazioni chiare, così potrai applicare la tecnica a progetti reali.

## Risposte Rapide
- **Quale libreria gestisce crop image java?** Aspose.PSD per Java.  
- **È necessaria una licenza per lo sviluppo?** Una versione di prova gratuita è sufficiente per i test; è richiesta una licenza commerciale per la produzione.  
- **Posso convertire PSD in JPEG durante il ritaglio?** Sì, usando `JpegOptions` insieme a un rettangolo di ritaglio.  
- **Java 8 è supportato?** Aspose.PSD supporta Java 8 e versioni successive.  
- **Quanto tempo richiede l'implementazione?** Tipicamente meno di 10 minuti per un'operazione di ritaglio di base.

## Cos'è “crop image java”?

Ritagliare un'immagine in Java significa selezionare una regione rettangolare dell'immagine di origine e scartare il resto. Con Aspose.PSD è possibile definire questa regione usando un oggetto `Rectangle`, quindi salvare il risultato in un formato diverso, ad esempio JPEG.

## Perché usare Aspose.PSD per il ritaglio di immagini Java?

- **Supporto completo PSD** – lavora direttamente con file PSD a più livelli senza doverli convertire prima.  
- **Gestione raster ad alte prestazioni** – utilizzo efficiente della memoria per immagini di grandi dimensioni.  
- **Conversione integrata** – esporta facilmente in JPEG, PNG, BMP, ecc., applicando il ritaglio o l'espansione della tela.  
- **Cross‑platform** – funziona su qualsiasi sistema che esegue Java.

## Prerequisiti

Prima di iniziare, assicurati di avere:

1. **Java Development Kit (JDK)** – Java 8 o versioni successive installate.  
2. **Aspose.PSD per Java** – scarica la libreria dal sito ufficiale **[qui](https://releases.aspose.com/psd/java/)**.  

> **Suggerimento:** aggiungi il JAR di Aspose.PSD al classpath del tuo progetto o alle dipendenze Maven/Gradle per evitare `ClassNotFoundException`.

## Importa i Pacchetti

Aggiungi gli import necessari al tuo file sorgente Java. Queste classi ti consentono di caricare immagini, manipolare raster, definire rettangoli e impostare le opzioni di esportazione JPEG.

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;
import com.aspose.psd.Rectangle;

import com.aspose.psd.imageoptions.JpegOptions;
```

## Passo 1: Imposta la Directory del Documento

Specifica la cartella che contiene il file PSD di origine. Sostituisci il segnaposto con il percorso reale sul tuo computer.

```java
String dataDir = "Your Document Directory";
```

## Passo 2: Specifica i Percorsi di Origine e Destinazione

Definisci dove leggere il PSD e dove scrivere il JPEG ritagliato.

```java
String sourceFile = dataDir + "example1.psd";
String destName = dataDir + "jpeg_out.jpg";
```

## Passo 3: Carica e Cache l'Immagine

Carica il PSD in un oggetto `RasterImage`. Il caching migliora le prestazioni per le operazioni successive, come il ritaglio.

```java
RasterImage rasterImage = (RasterImage)Image.load(sourceFile);
rasterImage.cacheData();
```

## Passo 4: Crea il Rettangolo per il Ritaglio

Crea un `Rectangle` che descrive la regione da conservare. Le coordinate possono essere negative per **espandere** la tela prima del ritaglio, utile per aggiungere un bordo attorno all'immagine originale.

```java
Rectangle destRect = new Rectangle(-200, -200, 300, 300);
```

> **Perché usare coordinate negative?**  
> Valori X/Y negativi spostano l'area di ritaglio verso sinistra/alto, aggiungendo spazio vuoto (espansione) attorno al contenuto originale prima del ritaglio finale.

## Passo 5: Salva l'Immagine Ritagliata

Infine, salva l'immagine risultante usando `JpegOptions`. Questo passaggio dimostra anche **convert psd jpeg** applicando il rettangolo di ritaglio.

```java
rasterImage.save(destName, new JpegOptions(), destRect);
```

> **Risultato:** `jpeg_out.jpg` contiene ora un'immagine di 300 × 300 pixel che è stata espansa di 200 px su ciascun lato e poi ritagliata secondo il rettangolo definito.

Congratulazioni! Hai eseguito con successo **java image cropping**, espanso la tela e convertito un file PSD in JPEG—tutto in poche righe di codice.

## Casi d'Uso Comuni

- **Preparazione di asset per il web** – ritaglia e ridimensiona screenshot o design prima del caricamento.  
- **Generazione di miniature** – estrai una regione specifica da un PSD di grandi dimensioni per anteprime.  
- **Elaborazione batch automatizzata** – itera su una cartella di file PSD, applicando lo stesso rettangolo di ritaglio a ciascuno.

## Risoluzione dei Problemi e Suggerimenti

| Problema | Soluzione Consigliata |
|----------|-----------------------|
| `OutOfMemoryError` durante il caricamento di PSD di grandi dimensioni | Chiama `rasterImage.cacheData()` subito e considera di aumentare la dimensione dell'heap JVM (`-Xmx`). |
| L'area ritagliata è fuori centro | Verifica gli offset X/Y del rettangolo; ricorda che i valori negativi espandono la tela. |
| Il JPEG di output appare sfocato | Regola l'impostazione di qualità di `JpegOptions` (ad es., `new JpegOptions { Quality = 90 }`). |

## Domande Frequenti

### Q1: Aspose.PSD è compatibile con diverse versioni di Java?

A1: Sì, Aspose.PSD supporta varie versioni di Java, garantendo compatibilità con un'ampia gamma di ambienti di sviluppo.

### Q2: Posso usare Aspose.PSD per progetti commerciali?

A2: Assolutamente sì, Aspose.PSD offre licenze commerciali per gli sviluppatori, consentendone l'uso sia in progetti personali che commerciali.

### Q3: Ci sono limitazioni sui formati di file immagine supportati?

A3: Aspose.PSD supporta diversi formati di immagine, tra cui PSD, JPEG, PNG e altri. Consulta la [documentazione](https://reference.aspose.com/psd/java/) per l'elenco completo.

### Q4: Come posso ottenere supporto per domande relative ad Aspose.PSD?

A4: Visita il [forum Aspose.PSD](https://forum.aspose.com/c/psd/34) per chiedere assistenza alla community o al team di supporto Aspose.

### Q5: È disponibile una versione di prova gratuita?

A5: Sì, puoi provare Aspose.PSD con una versione di prova gratuita. Scaricala [qui](https://releases.aspose.com/).

---

**Ultimo aggiornamento:** 2026-01-07  
**Testato con:** Aspose.PSD per Java 24.12  
**Autore:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}