---
date: 2026-10-08
description: Scopri come leggere i tag EXIF in Java utilizzando Aspose.PSD per Java
  (asp) con il nostro tutorial passo‑passo e potenzia le tue capacità di elaborazione
  delle immagini.
keywords:
- read exif tags java
- java exif tag extraction
- java image metadata extraction
lastmod: 2026-10-08
linktitle: Leggi le informazioni dei tag EXIF specifici in Java
og_description: 'Leggi i tag EXIF: gli sviluppatori Java possono estrarre rapidamente
  i metadati delle immagini usando Aspose.PSD. Questa guida ti accompagna nel caricamento
  di un PSD, nella localizzazione delle risorse thumbnail e nella stampa dei campi
  EXIF chiave come WhiteBalance e ISO speed.'
og_image_alt: Guide showing how to read EXIF tags from PSD files in Java using Aspose.PSD
og_title: Come leggere i tag EXIF in Java con Aspose.PSD
schemas:
- author: Aspose
  dateModified: '2026-10-08'
  description: Learn how to read EXIF tags in Java using Aspose.PSD for Java (asp)
    with our step‑by‑step tutorial, and boost your image processing capabilities.
  headline: How to read EXIF tags in Java with Aspose.PSD
  type: TechArticle
- description: Learn how to read EXIF tags in Java using Aspose.PSD for Java (asp)
    with our step‑by‑step tutorial, and boost your image processing capabilities.
  name: How to read EXIF tags in Java with Aspose.PSD
  steps:
  - name: 'Java Development Kit (JDK): Ensure you have JDK installed on your machine.
      You can download it from the [Oracle JDK website](https://www.oracle.com/java/technologies/javase-downloads.html).'
    text: 'Java Development Kit (JDK): Ensure you have JDK installed on your machine.
      You can download it from the [Oracle JDK website](https://www.oracle.com/java/technologies/javase-downloads.html).'
  - name: 'Aspose.PSD for Java: Download the library from the [Aspose.PSD for Java
      download page](https://releases.aspose.com/psd/java/).'
    text: 'Aspose.PSD for Java: Download the library from the [Aspose.PSD for Java
      download page](https://releases.aspose.com/psd/java/).'
  - name: 'Integrated Development Environment (IDE): An IDE like IntelliJ IDEA, Eclipse,
      or NetBeans will make coding more convenient.'
    text: 'Integrated Development Environment (IDE): An IDE like IntelliJ IDEA, Eclipse,
      or NetBeans will make coding more convenient.'
  - name: 'PSD file: A PSD file with EXIF data. You can use the sample provided in
      this tutorial or any other PSD file with EXIF tags.'
    text: 'PSD file: A PSD file with EXIF data. You can use the sample provided in
      this tutorial or any other PSD file with EXIF tags.'
  type: HowTo
- questions:
  - answer: Aspose.PSD (asp)
    question: What library reads EXIF data from PSD in Java?
  - answer: WhiteBalance, PixelXDimension, PixelYDimension, ISOSpeed, FocalLength,
      and more.
    question: Which tags can be extracted?
  - answer: Yes, a commercial license is required; a free trial is available.
    question: Do I need a license for production?
  - answer: The same API supports PNG, JPEG, TIFF via Java image metadata extraction.
    question: Can I use this with other image formats?
  - answer: About 10‑15 minutes for a basic read‑only scenario.
    question: How long does implementation take?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- read exif tags java
- Aspose.PSD
- java image metadata extraction
- EXIF extraction
- PSD processing
title: Come leggere i tag EXIF in Java con Aspose.PSD
url: /it/java/java-jpeg-image-processing/read-specific-exif-tags-info-java/
weight: 19
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Leggi informazioni specifiche sui tag EXIF in Java con Aspose (asp)

## Introduzione
Se hai bisogno di **leggere i tag EXIF in Java**, Aspose.PSD (asp) offre un'API pulita, pure‑Java che funziona senza Photoshop. In questo tutorial imparerai come estrarre i dati EXIF da un'immagine PSD, selezionare solo i tag di tuo interesse e stamparli sulla console. Copriremo tutto, dall'impostazione dell'ambiente di sviluppo all'estrazione dei metadati come WhiteBalance, velocità ISO e lunghezza focale. Iniziamo!

## Risposte rapide
- **Quale libreria legge i dati EXIF da PSD in Java?** Aspose.PSD (asp)  
- **Quali tag possono essere estratti?** WhiteBalance, PixelXDimension, PixelYDimension, ISOSpeed, FocalLength e altri.  
- **Ho bisogno di una licenza per la produzione?** Sì, è necessaria una licenza commerciale; è disponibile una versione di prova gratuita.  
- **Posso usarlo con altri formati immagine?** La stessa API supporta PNG, JPEG, TIFF tramite l'estrazione di metadati immagine Java.  
- **Quanto tempo richiede l'implementazione?** Circa 10‑15 minuti per uno scenario di sola lettura di base.

## Cos'è asp (Aspose.PSD per Java)?
Aspose.PSD per Java è una libreria pure‑Java che consente agli sviluppatori di lavorare con file Adobe Photoshop (PSD, PSB) senza installare Photoshop. Fornisce accesso programmatico a livelli, risorse e metadati—including i tag EXIF—rendendola ideale per attività di **estrazione di metadati immagine java**.

## Perché usare Aspose.PSD (asp) per l'estrazione EXIF?
Puoi estrarre i tag EXIF in Java con sole due chiamate di metodo, e la libreria elabora file fino a 2 GB senza caricare l'intero documento in memoria. Supporta **oltre 30 formati immagine** e preserva le impostazioni esatte della fotocamera, fornendo risultati deterministici su ambienti Windows, Linux e macOS.

## Prerequisiti
Prima di immergerci nel codice, ci sono alcune cose di cui avrai bisogno:

1. Java Development Kit (JDK): Assicurati di avere il JDK installato sulla tua macchina. Puoi scaricarlo dal [Oracle JDK website](https://www.oracle.com/java/technologies/javase-downloads.html).  
2. Aspose.PSD per Java: Scarica la libreria dalla [Aspose.PSD for Java download page](https://releases.aspose.com/psd/java/).  
3. Integrated Development Environment (IDE): Un IDE come IntelliJ IDEA, Eclipse o NetBeans renderà la programmazione più comoda.  
4. File PSD: Un file PSD con dati EXIF. Puoi usare il campione fornito in questo tutorial o qualsiasi altro file PSD con tag EXIF.

## Importa i pacchetti
Importa le classi Aspose.PSD necessarie come Image, PsdImage, ThumbnailResource e JpegExifData per lavorare con i file PSD.  
```java
import com.aspose.psd.Image;
import com.aspose.psd.exif.JpegExifData;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.resources.Thumbnail4Resource;
import com.aspose.psd.fileformats.psd.resources.ThumbnailResource;
```

## Passo 1: carica l'immagine PSD
`Image.load()` carica un file e restituisce un oggetto Image che rappresenta i dati dell'immagine.  
`PsdImage` è la classe Aspose.PSD che fornisce funzionalità specifiche per PSD.  
Il metodo `Image.load()` carica qualsiasi file immagine supportato in memoria, restituendo un oggetto generico `Image` che puoi castare al tipo specifico PSD.  
```java
String dataDir = "Your Document Directory";
PsdImage image = (PsdImage) Image.load(dataDir + "1280px-Zebras_Serengeti.psd");
```

In questo passo, carichiamo il file PSD usando il metodo `Image.load()`. La classe `PsdImage` è usata per rappresentare l'immagine PSD, e castiamo l'immagine caricata a questa classe per accedere alle funzionalità specifiche di PSD.

## Passo 2: itera sulle risorse dell'immagine
`PsdImage.getResources()` restituisce una collezione di risorse incorporate come miniature e dati EXIF.  
La chiamata `PsdImage.getResources()` restituisce una collezione di tutte le risorse incorporate. Iterando su questa collezione puoi individuare le risorse thumbnail che contengono metadati EXIF.  
```java
for (int i = 0; i < image.getImageResources().length; i++) {
    if (image.getImageResources()[i] instanceof ThumbnailResource || 
        image.getImageResources()[i] instanceof Thumbnail4Resource) {
        // Further processing will be done here
    }
}
```

Scorriamo le risorse dell'immagine usando un ciclo `for`. L'obiettivo è identificare le risorse che sono istanze di `ThumbnailResource` o `Thumbnail4Resource`, poiché questi sono i tipi che contengono i dati EXIF.

## Passo 3: estrai i dati EXIF
`ThumbnailResource.getJpegOptions()` fornisce accesso alle opzioni JPEG includendo i metadati EXIF.  
`JpegExifData` contiene i valori individuali dei tag EXIF.  
Il metodo `ThumbnailResource.getJpegOptions()` fornisce accesso a un oggetto `JpegExifData`, che contiene i singoli tag EXIF come WhiteBalance, ISOSpeed e FocalLength.  
```java
if (image.getImageResources()[i] instanceof ThumbnailResource) {
    JpegExifData exif = ((ThumbnailResource) image.getImageResources()[i]).getJpegOptions().getExifData();
    if (exif != null) {
        System.out.println("Exif WhiteBalance: " + exif.getWhiteBalance());
        System.out.println("Exif PixelXDimension: " + exif.getPixelXDimension());
        System.out.println("Exif PixelYDimension: " + exif.getPixelYDimension());
        System.out.println("Exif ISOSpeed: " + exif.getISOSpeed());
        System.out.println("Exif FocalLength: " + exif.getFocalLength());
    }
}
```

Usiamo una dichiarazione `if` per verificare se la risorsa è un'istanza di `ThumbnailResource`. Se lo è, la castiamo e recuperiamo le sue `JpegOptions` per accedere all'`ExifData`. Infine, stampiamo vari tag EXIF come WhiteBalance, Dimensioni Pixel, ISOSpeed e FocalLength.

## Problemi comuni e consigli
- **Dati EXIF null:** Alcuni file PSD potrebbero non contenere una risorsa thumbnail con informazioni EXIF. Controlla sempre `null` prima di accedere ai valori dei tag.  
- **Errori di percorso file:** Usa percorsi assoluti o assicurati che la directory di lavoro punti alla cartella contenente il tuo file PSD.  
- **Restrizioni di licenza:** La versione di prova gratuita limita il numero di pagine che puoi elaborare; passa a una licenza completa per utilizzo illimitato.

## Domande frequenti
### Cos'è il dato EXIF?
EXIF (Exchangeable Image File Format) è un insieme di metadati incorporati nei file immagine, contenente informazioni come impostazioni della fotocamera, data e ora, e dimensioni dell'immagine.

### Posso modificare i dati EXIF usando Aspose.PSD?
Sì, Aspose.PSD consente di leggere e modificare i dati EXIF. Puoi aggiornare i tag e salvare le modifiche nel file immagine.

### Aspose.PSD per Java è gratuito?
Aspose.PSD offre una versione di prova gratuita che puoi scaricare dalla [Aspose.PSD official releases page](https://releases.aspose.com/). Per tutte le funzionalità, è necessario acquistare una licenza.

### Quali altri formati supporta Aspose.PSD?
Aspose.PSD supporta vari formati Adobe Photoshop, inclusi PSD, PSB e altri. Fornisce anche opzioni per convertire questi formati in PNG, JPEG, TIFF, ecc.

### Come posso ottenere supporto per Aspose.PSD?
Puoi ottenere supporto tramite il [forum Aspose.PSD](https://forum.aspose.com/c/psd/34).

### Come questo aiuta con **estrazione di metadati immagine java**?
Utilizzando l'oggetto `JpegExifData`, puoi estrarre programmaticamente qualsiasi tag EXIF di cui hai bisogno, creando una solida base per attività più ampie di estrazione di metadati su diversi formati immagine.

---

**Ultimo aggiornamento:** 2026-10-08  
**Testato con:** Aspose.PSD per Java 24.11 (ultima versione al momento della scrittura)  
**Autore:** Aspose

## Tutorial correlati

- [Leggi Modifica Tag Jpeg Exif Java](/psd/java/java-jpeg-image-processing/read-modify-jpeg-exif-tags-java/)
- [Elaborazione Immagine Jpeg Java](/psd/java/java-jpeg-image-processing/)
- [Come ruotare l'immagine di un angolo specifico con Aspose.PSD per Java](/psd/java/advanced-image-manipulation/rotate-image-specific-angle/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}