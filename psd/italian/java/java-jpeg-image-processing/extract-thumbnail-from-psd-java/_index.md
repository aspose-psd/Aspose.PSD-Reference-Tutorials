---
title: Estrai la miniatura da PSD in Java
linktitle: Estrai la miniatura da PSD in Java
second_title: API Java Aspose.PSD
description: Scopri come estrarre le miniature dai file PSD utilizzando Aspose.PSD per Java. Questa guida passo passo copre tutto, dalla configurazione al salvataggio delle immagini estratte.
weight: 15
url: /it/java/java-jpeg-image-processing/extract-thumbnail-from-psd-java/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Estrai la miniatura da PSD in Java

## Introduzione
In questo tutorial esploreremo come estrarre le miniature dai file PSD utilizzando Aspose.PSD per Java. Le miniature possono essere utili per anteprime rapide o per creare versioni più piccole di immagini incorporate nei documenti PSD. Immergiamoci nei passaggi necessari per raggiungere questo obiettivo utilizzando Aspose.PSD.
## Prerequisiti
Prima di iniziare, assicurati di avere la seguente configurazione:
- Java Development Kit (JDK) installato sul tuo sistema.
-  Aspose.PSD per la libreria Java. Puoi scaricarlo da[Qui](https://releases.aspose.com/psd/java/).
- Conoscenza base della programmazione Java.
## Importa pacchetti
Per iniziare, includi il pacchetto Aspose.PSD necessario nella tua classe Java:
```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.resources.Thumbnail4Resource;
import com.aspose.psd.fileformats.psd.resources.ThumbnailResource;
import com.aspose.psd.imageoptions.JpegOptions;
```
## Passaggio 1: carica il file PSD
Innanzitutto, carica il file PSD che contiene la miniatura che desideri estrarre.
```java
String dataDir = "Your_Document_Directory/";
PsdImage image = (PsdImage)Image.load(dataDir + "your_file.psd");
```
 Sostituire`"Your_Document_Directory/"` con il percorso della directory in cui si trova il file PSD e`"your_file.psd"` con il nome del tuo file PSD.
## Passaggio 2: ripetere le risorse immagine
Scorrere le risorse immagine per trovare la risorsa miniatura.
```java
for (int i = 0; i < image.getImageResources().length; i++) {
    if (image.getImageResources()[i] instanceof ThumbnailResource) {
        ThumbnailResource thumbnail = (ThumbnailResource) image.getImageResources()[i];
        
        // Estrai i dati della miniatura
        int[] data = thumbnail.getThumbnailArgb32Data();
        
        // Crea una nuova immagine con i dati della miniatura estratti
        PsdImage extractedThumbnailImage = new PsdImage(thumbnail.getWidth(), thumbnail.getHeight());
        extractedThumbnailImage.saveArgb32Pixels(extractedThumbnailImage.getBounds(), data);
        
        // Salva la miniatura estratta come file JPEG separato
        extractedThumbnailImage.save(dataDir + "extracted_thumbnail.jpg", new JpegOptions());
        
        // Emetti il messaggio di successo
        System.out.println("Thumbnail extracted and saved successfully.");
        
        break; // Esci dal ciclo una volta trovata ed elaborata la miniatura
    }
}
```
## Passaggio 3: salva la miniatura estratta
Salva la miniatura estratta come file immagine separato (in questo caso come file JPEG).
## Passaggio 4: gestione di diversi tipi di miniature
 Se il tuo file PSD può contenere più tipi di miniature, come ad esempio`Thumbnail4Resource`, puoi estendere la logica per gestire questi casi in modo simile.

## Conclusione
In questo tutorial, abbiamo esplorato come estrarre le miniature dai file PSD utilizzando Aspose.PSD per Java. Seguendo i passaggi sopra descritti, puoi recuperare e salvare in modo efficiente le miniature incorporate nei tuoi documenti PSD.

## Domande frequenti
### Cos'è Aspose.PSD?
Aspose.PSD è una libreria Java che consente agli sviluppatori di lavorare con PSD e altri formati di file immagine a livello di codice.
### Dove posso trovare ulteriore documentazione su Aspose.PSD per Java?
 Puoi fare riferimento a[documentazione](https://reference.aspose.com/psd/java/) per riferimenti ed esempi API dettagliati.
### Posso provare Aspose.PSD gratuitamente prima dell'acquisto?
 Sì, puoi scaricare un file[prova gratuita](https://releases.aspose.com/) valutare le capacità della biblioteca.
### Come posso ottenere licenze temporanee per Aspose.PSD?
 È possibile ottenere licenze temporanee da[Qui](https://purchase.aspose.com/temporary-license/).
### Aspose.PSD è adatto per l'uso commerciale?
Sì, Aspose.PSD può essere utilizzato sia per progetti personali che commerciali secondo i termini di licenza.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
