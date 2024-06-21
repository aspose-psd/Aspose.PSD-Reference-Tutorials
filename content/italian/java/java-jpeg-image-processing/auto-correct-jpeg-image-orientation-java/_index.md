---
title: Correzione automatica dell'orientamento dell'immagine JPEG in Java
linktitle: Correzione automatica dell'orientamento dell'immagine JPEG in Java
second_title: API Java Aspose.PSD
description: Impara a correggere automaticamente l'orientamento dell'immagine JPEG in Java utilizzando Aspose.PSD. Migliora le tue capacità di elaborazione delle immagini senza sforzo.
type: docs
weight: 12
url: /it/java/java-jpeg-image-processing/auto-correct-jpeg-image-orientation-java/
---
## introduzione
Nell'era digitale di oggi, la manipolazione e l'ottimizzazione delle immagini a livello di programmazione è diventata un compito cruciale per gli sviluppatori di vari domini. Aspose.PSD per Java offre agli sviluppatori strumenti robusti per gestire in modo efficiente PSD, JPEG e altri formati di immagine. Questo tutorial approfondisce un'attività specifica: correggere automaticamente l'orientamento dell'immagine JPEG utilizzando Aspose.PSD per Java. Che tu stia creando un'app di fotoritocco, gestendo risorse di immagini in un sistema di gestione dei contenuti o automatizzando i flussi di lavoro di elaborazione delle immagini, questa guida ti fornirà le conoscenze necessarie per integrare perfettamente questa funzionalità nelle tue applicazioni Java.
## Prerequisiti
Prima di immergerti in questo tutorial, assicurati di aver impostato i seguenti prerequisiti:
- Ambiente di sviluppo Java: assicurati di avere Java Development Kit (JDK) installato sul tuo sistema.
-  Aspose.PSD per Java JAR: scarica la libreria Aspose.PSD per Java da[Qui](https://releases.aspose.com/psd/java/).
- Ambiente di sviluppo integrato (IDE): utilizza IntelliJ IDEA, Eclipse o qualsiasi IDE di tua scelta per lo sviluppo Java.
- Comprensione di base di Java e dell'elaborazione delle immagini: la familiarità con la programmazione Java e i concetti di base dell'elaborazione delle immagini sarà utile.

## Importa pacchetti
Prima di iniziare con l'esempio, assicurati di importare i pacchetti necessari da Aspose.PSD per Java:
```java
import com.aspose.psd.Image;
import com.aspose.psd.examples.Utils.Utils;
import com.aspose.psd.exif.JpegExifData;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.resources.Thumbnail4Resource;
import com.aspose.psd.fileformats.psd.resources.ThumbnailResource;
```
## Passaggio 1: carica l'immagine PSD
Innanzitutto, carica l'immagine PSD che contiene la miniatura JPEG il cui orientamento necessita di correzione:
```java
String dataDir = "Your Document Directory";
PsdImage image = (PsdImage)Image.load(dataDir + "1280px-Zebras_Serengeti.psd");
```
 Sostituire`"Your Document Directory"` con il percorso effettivo della directory in cui si trova il file PSD.
## Passaggio 2: ripetere le risorse immagine
Successivamente, scorri le risorse dell'immagine per trovare la risorsa miniatura JPEG:
```java
for (int i = 0; i < image.getImageResources().length; i++) {
    // Trova risorsa miniatura. In genere sono nel formato file Jpeg.
    if (image.getImageResources()[i] instanceof ThumbnailResource || image.getImageResources()[i] instanceof Thumbnail4Resource) {
        // Regola i dati della miniatura.
        ThumbnailResource thumbnail = (ThumbnailResource) image.getImageResources()[i];
        JpegExifData exifData = thumbnail.getJpegOptions().getExifData();
        if (exifData != null && exifData.getThumbnail() != null) {
            // Se è presente una miniatura memorizzata, ruotala automaticamente.
            PsdImage jpegImage = (PsdImage) exifData.getThumbnail();
            if (jpegImage != null) {
                jpegImage.autoRotate();
            }
        }
    }
}
```
## Passaggio 3: salva l'immagine
Infine, salva l'immagine corretta dopo aver applicato la rotazione automatica:
```java
image.save();
```
Questo passaggio garantisce che le modifiche apportate all'immagine vengano mantenute.

## Conclusione
In conclusione, l'utilizzo di Aspose.PSD per Java fornisce una potente soluzione per correggere automaticamente gli orientamenti delle immagini JPEG all'interno dei file PSD. Seguendo i passaggi descritti in questo tutorial, gli sviluppatori possono migliorare i flussi di lavoro di elaborazione delle immagini, garantendo che le immagini vengano visualizzate correttamente su varie piattaforme e dispositivi.
## Domande frequenti
### Cos'è Aspose.PSD per Java?
Aspose.PSD per Java è una potente libreria che consente agli sviluppatori Java di lavorare con PSD, JPEG e altri formati di immagine a livello di codice.
### Come posso scaricare Aspose.PSD per Java?
 È possibile scaricare la libreria da[Qui](https://releases.aspose.com/psd/java/).
### Aspose.PSD per Java supporta la manipolazione delle immagini?
Sì, supporta varie attività di manipolazione delle immagini come ridimensionamento, ritaglio e regolazione dell'orientamento.
### Dove posso trovare la documentazione per Aspose.PSD per Java?
 È disponibile una documentazione completa[Qui](https://reference.aspose.com/psd/java/).
### Posso provare Aspose.PSD per Java gratuitamente?
 Sì, puoi ottenere una prova gratuita da[Qui](https://releases.aspose.com/).