---
date: 2025-12-06
description: Scopri come ruotare un'immagine di 270 gradi usando Aspose.PSD per Java.
  Questa guida mostra come ruotare i file PSD, capovolgere le immagini e convertire
  i PSD in JPEG.
linktitle: Rotate Image 270 Degrees
second_title: Aspose.PSD Java API
title: Come ruotare l'immagine di 270 gradi con Aspose.PSD per Java
url: /it/java/advanced-image-manipulation/rotate-image/
weight: 19
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Ruota immagine di 270 gradi con Aspose.PSD per Java

## Introduzione

In questo **java image processing tutorial**, scoprirai come **ruotare un'immagine di 270 gradi** in modo rapido e affidabile usando Aspose.PSD per Java. Che tu stia creando uno strumento di fotoritocco, automatizzando conversioni batch o semplicemente abbia bisogno di riorientare un livello PSD, la libreria rende il compito indolore. Tratteremo anche il ribaltamento delle immagini e la conversione del PSD ruotato in JPEG, così avrai un flusso di lavoro completo end‑to‑end.

## Risposte rapide
- **Quale libreria gestisce la rotazione?** Aspose.PSD per Java  
- **Quale angolo di rotazione usa l'esempio?** 270 gradi  
- **Posso anche ribaltare l'immagine?** Sì – usa le opzioni `RotateFlipType` come `Rotate90FlipX`  
- **Come salvo il risultato?** Nell'esempio salviamo come JPEG usando `JpegOptions`  
- **È necessaria una licenza per la produzione?** È richiesta una licenza valida di Aspose.PSD per uso commerciale  

## Cos'è “ruotare immagine di 270 gradi”?
Ruotare un'immagine di 270 gradi significa girare la foto di tre quarti di cerchio in senso orario (o 90 gradi in senso antiorario). In molti scenari di editing grafico questa orientazione corrisponde al layout originale in modalità ritratto dopo una serie di trasformazioni.

## Perché usare Aspose.PSD per questo compito?
- **Supporto completo PSD** – funziona con livelli, maschere e oggetti di regolazione.  
- **Nessun Photoshop nativo richiesto** – funziona su qualsiasi runtime Java.  
- **API semplice** – una singola chiamata (`rotateFlip`) gestisce rotazione e ribaltamento.  
- **Conversione di formato facile** – esporta direttamente in JPEG, PNG o altri formati comuni.

## Prerequisiti

Prima di iniziare, assicurati di avere:

- La libreria **Aspose.PSD per Java** installata. Puoi scaricarla e consultare la documentazione completa dell'API [qui](https://reference.aspose.com/psd/java/).  
- Un ambiente di sviluppo Java (JDK 8 o superiore).  
- Un file PSD di esempio che desideri ruotare. Aggiorna la variabile `sourceFile` nel codice con il percorso corretto del tuo file.

## Importare i pacchetti

Inizia importando le classi necessarie dal pacchetto Aspose.PSD:

```java
import com.aspose.psd.Image;
import com.aspose.psd.RotateFlipType;

import com.aspose.psd.imageoptions.JpegOptions;
```

## Come ruotare un PSD – Passo 1: Caricare l'immagine

Crea un'istanza `Image` che punti al tuo file PSD di origine:

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";
Image image = Image.load(sourceFile);
```

## Come ruotare un PSD – Passo 2: Ruotare l'immagine di 270 gradi

Usa il metodo `rotateFlip` con `RotateFlipType.Rotate270FlipNone` per ottenere una rotazione di 270 gradi senza alcun ribaltamento:

```java
image.rotateFlip(RotateFlipType.Rotate270FlipNone);
```

> **Suggerimento:** Se devi anche ribaltare l'immagine orizzontalmente o verticalmente, scegli un diverso `RotateFlipType` come `Rotate90FlipX` o `Rotate180FlipY`.

## Come ruotare un PSD – Passo 3: Convertire PSD in JPEG e salvare

Dopo la rotazione, puoi **convertire il PSD in JPEG** (o in qualsiasi altro formato supportato) usando la classe di opzioni appropriata:

```java
String destName = dataDir + "RotatedImage_out.jpg";
image.save(destName, new JpegOptions());
```

Il file `RotatedImage_out.jpg` ora contiene il contenuto originale del PSD ruotato di 270 gradi e salvato come JPEG.

## Problemi comuni e soluzioni

| Problema | Soluzione |
|----------|-----------|
| **L'immagine appare capovolta** | Verifica di aver usato `Rotate270FlipNone`. Per una rotazione di 90 gradi in senso orario usa `Rotate90FlipNone`. |
| **Il file di output è corrotto** | Assicurati che la cartella di destinazione esista e che tu abbia i permessi di scrittura. |
| **Eccezione di licenza** | Installa una licenza temporanea o permanente di Aspose.PSD prima di caricare l'immagine in produzione. |

## Domande frequenti

**D: Aspose.PSD è compatibile con diversi formati immagine?**  
R: Sì, Aspose.PSD supporta PSD, JPEG, PNG, BMP, GIF e molti altri formati raster.

**D: Posso applicare rotazioni personalizzate, non solo i ribaltamenti predefiniti?**  
R: Assolutamente! Sebbene `RotateFlipType` fornisca gli angoli più comuni, puoi combinare più chiamate o usare matrici di trasformazione per angoli arbitrari.

**D: Come converto il PSD ruotato in un altro formato, ad esempio PNG?**  
R: Sostituisci `JpegOptions` con `PngOptions` (o la classe di opzioni appropriata) nel metodo `save`.

**D: Dove posso trovare supporto o assistenza aggiuntiva?**  
R: Per aiuto dalla community, visita il [Forum Aspose.PSD](https://forum.aspose.com/c/psd/34).

**D: È disponibile una versione di prova gratuita?**  
R: Sì, puoi provare Aspose.PSD con una [prova gratuita](https://releases.aspose.com/).

**D: Come ottengo una licenza temporanea?**  
R: Se ti serve una licenza temporanea, puoi ottenerla [qui](https://purchase.aspose.com/temporary-license/).

## Conclusione

Ora sai come **ruotare un'immagine di 270 gradi** usando Aspose.PSD per Java, ribaltare le immagini quando necessario ed esportare il risultato in JPEG. Questo flusso di lavoro semplice può essere integrato in pipeline di elaborazione immagini basate su Java più ampie, offrendoti il pieno controllo sulla manipolazione dei PSD senza dipendere da Photoshop.

---

**Ultimo aggiornamento:** 2025-12-06  
**Testato con:** Aspose.PSD per Java 24.12  
**Autore:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}