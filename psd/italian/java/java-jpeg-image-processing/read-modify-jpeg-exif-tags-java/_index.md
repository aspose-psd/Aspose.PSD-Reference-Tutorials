---
date: 2026-10-03
description: Scopri come leggere i metadati delle immagini in Java e modificare i
  tag EXIF JPEG con Aspose.PSD for Java in questa guida passo-passo, perfetta per
  gli sviluppatori che gestiscono i metadati delle immagini in modo efficiente.
keywords:
- java read image metadata
- read EXIF tags Java
- modify JPEG metadata Java
- Aspose.PSD Java
lastmod: 2026-10-03
linktitle: Leggi e modifica i tag EXIF JPEG in Java
og_description: Scopri come leggere i metadati delle immagini in Java e modificare
  i tag EXIF JPEG con Aspose.PSD for Java. Questa guida mostra codice passo-passo
  per estrarre e aggiornare le informazioni EXIF.
og_image_alt: Guide showing how to java read image metadata and edit JPEG EXIF tags
  using Aspose.PSD for Java
og_title: Come leggere i metadati delle immagini in Java e modificare i tag EXIF JPEG
schemas:
- author: Aspose
  dateModified: '2026-10-03'
  description: Learn how to java read image metadata and modify JPEG EXIF tags with
    Aspose.PSD for Java in this step‑by‑step guide, perfect for developers handling
    image metadata efficiently.
  headline: How to java read image metadata and modify JPEG EXIF tags
  type: TechArticle
- description: Learn how to java read image metadata and modify JPEG EXIF tags with
    Aspose.PSD for Java in this step‑by‑step guide, perfect for developers handling
    image metadata efficiently.
  name: How to java read image metadata and modify JPEG EXIF tags
  steps:
  - name: '**Java Development Kit (JDK)** – make sure you have JDK 11 or newer. You
      can download it from the [Oracle website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).'
    text: '**Java Development Kit (JDK)** – make sure you have JDK 11 or newer. You
      can download it from the [Oracle website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).'
  - name: '**Aspose.PSD for Java library** – obtain the latest JAR from the [Aspose
      releases page](https://releases.aspose.com/psd/java/).'
    text: '**Aspose.PSD for Java library** – obtain the latest JAR from the [Aspose
      releases page](https://releases.aspose.com/psd/java/).'
  - name: '**IDE** – IntelliJ IDEA, Eclipse, or any editor you prefer.'
    text: '**IDE** – IntelliJ IDEA, Eclipse, or any editor you prefer.'
  - name: '**Basic Java knowledge** – you should be comfortable with creating projects
      and adding external JARs.'
    text: '**Basic Java knowledge** – you should be comfortable with creating projects
      and adding external JARs.'
  type: HowTo
- questions:
  - answer: EXIF (Exchangeable Image File Format) metadata stores camera settings,
      timestamps, GPS coordinates, and other information embedded in JPEG and other
      image files.
    question: What is EXIF data?
  - answer: You can get a free trial from the [Aspose releases page](https://releases.aspose.com/).
    question: Can I use Aspose.PSD for Java for free?
  - answer: Aspose.PSD for Java supports Java SE 7 and above.
    question: Is Aspose.PSD for Java compatible with all versions of Java?
  - answer: Check out the [documentation](https://reference.aspose.com/psd/java/)
      for more details.
    question: Where can I find more documentation on Aspose.PSD for Java?
  - answer: You can get support from the [Aspose PSD support forum](https://forum.aspose.com/c/psd/34/).
    question: How do I get support for Aspose.PSD for Java?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- java image metadata
- exif tags
- aspose psd
- jpeg metadata
- java tutorial
title: Come leggere i metadati delle immagini in Java e modificare i tag EXIF JPEG
url: /it/java/java-jpeg-image-processing/read-modify-jpeg-exif-tags-java/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Leggi e modifica i tag EXIF JPEG in Java

## Introduzione
Se hai bisogno di **java read image metadata** da file JPEG e cambiarlo programmaticamente, sei nel posto giusto. In questo tutorial vedremo come estrarre e aggiornare i tag EXIF usando Aspose.PSD per Java. Alla fine sarai in grado di recuperare i dettagli della fotocamera, l'orientamento e i campi personalizzati, quindi scriverli nuovamente nel file—tutto senza un editor grafico.

## Risposte rapide
- **Quale libreria gestisce JPEG EXIF in Java?** Aspose.PSD for Java.
- **Quante righe di codice servono per leggere EXIF?** Circa tre righe dopo il caricamento dell'immagine.
- **È possibile modificare i tag EXIF?** Sì, è possibile cambiare qualsiasi tag standard o personalizzato e salvare il risultato.
- **Formati immagine supportati?** Oltre 150 formati, inclusi PSD, JPEG, PNG, TIFF e BMP.
- **Versione minima di Java?** Java 7 o superiore.

## Perché usare Aspose.PSD per Java?
Aspose.PSD supporta **150+ formati immagine** e può elaborare file fino a **2 GB** senza caricare l'intero documento in memoria, offrendoti operazioni di metadati rapide e a basso consumo di memoria su grandi collezioni fotografiche. Fornisce inoltre una semplice API per leggere e scrivere dati EXIF, IPTC e XMP, rendendo l'elaborazione batch di migliaia di immagini efficiente e affidabile.

## Prerequisiti
1. **Java Development Kit (JDK)** – assicurati di avere JDK 11 o più recente. Puoi scaricarlo dal [Oracle website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).  
2. **Aspose.PSD for Java library** – ottieni l'ultimo JAR dalla [Aspose releases page](https://releases.aspose.com/psd/java/).  
3. **IDE** – IntelliJ IDEA, Eclipse o qualsiasi editor tu preferisca.  
4. **Basic Java knowledge** – dovresti sentirti a tuo agio nel creare progetti e aggiungere JAR esterni.

## Cos'è Java read image metadata?
Java read image metadata si riferisce al processo di accesso programmatico alle informazioni incorporate come EXIF, IPTC e XMP memorizzate all'interno dei file immagine usando codice Java. Questi metadati possono includere impostazioni della fotocamera, timestamp, coordinate GPS, avvisi di copyright e commenti degli utenti, consentendo alle applicazioni di organizzare, cercare e manipolare le immagini in base ai loro dati descrittivi.

## Importa pacchetti
Prima, aggiungi il JAR di Aspose.PSD al classpath del tuo progetto e importa le classi necessarie.

Il pacchetto `com.aspose.psd` fornisce l'API principale per caricare immagini e accedere alle loro risorse.

```java
import com.aspose.psd.Image;
import com.aspose.psd.exif.JpegExifData;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.resources.Thumbnail4Resource;
import com.aspose.psd.fileformats.psd.resources.ThumbnailResource;
```

## Come leggere i metadati immagine da file JPEG in Java?
Carica il JPEG con `PsdImage.load("image.jpg")`, individua la risorsa thumbnail che contiene i dati EXIF, e poi chiama `ExifData.read()` per ottenere un oggetto `ExifData` popolato. Questo approccio a singolo passaggio ti dà pieno accesso a tutti i campi EXIF standard e a eventuali tag personalizzati che potresti aver aggiunto.

## Passo 1: Carica l'immagine PSD
PsdImage è la classe Aspose.PSD che rappresenta un file PSD e fornisce metodi per accedere alle sue risorse e metadati.  
In questo passo, caricheremo l'immagine PSD da cui vogliamo leggere i dati EXIF. Assicurati che la tua immagine sia nella directory corretta.

```java
String dataDir = "Your Document Directory";
PsdImage image = null;
try {
    image = (PsdImage) Image.load(dataDir + "1280px-Zebras_Serengeti.psd");
} catch (IOException e) {
    e.printStackTrace();
}
```

## Passo 2: Itera sulle risorse dell'immagine
ThumbnailResource rappresenta un'immagine thumbnail memorizzata in un file PSD, spesso contenente dati EXIF incorporati.  
Una volta caricata l'immagine, il passo successivo è iterare sulle sue risorse per trovare la risorsa thumbnail, che tipicamente contiene i dati EXIF.

```java
for (int i = 0; i < image.getImageResources().length; i++) {
    if (image.getImageResources()[i] instanceof ThumbnailResource) {
        ThumbnailResource thumbnail = (ThumbnailResource) image.getImageResources()[i];
        // Proceed to next step
    }
}
```

## Passo 3: Estrai i dati EXIF
JpegExifData è la classe che contiene le informazioni EXIF estratte da un'immagine JPEG, permettendoti di leggere e modificare i singoli tag.  
Ora che abbiamo la risorsa thumbnail, possiamo estrarre i dati EXIF da essa. I dati EXIF includono informazioni preziose come il nome del proprietario della fotocamera, il valore di apertura, l'orientamento e altro.

```java
JpegExifData exifData = thumbnail.getJpegOptions().getExifData();
if (exifData != null) {
    System.out.println("Camera Owner Name: " + exifData.getCameraOwnerName());
    System.out.println("Aperture Value: " + exifData.getApertureValue());
    System.out.println("Orientation: " + exifData.getOrientation());
    System.out.println("Focal Length: " + exifData.getFocalLength());
    System.out.println("Compression: " + exifData.getCompression());
}
```

## Passo 4: Modifica i dati EXIF
Dopo aver letto i dati EXIF, potresti voler modificare alcuni dei suoi campi. Ecco come puoi farlo:

```java
if (exifData != null) {
    exifData.setCameraOwnerName("New Camera Owner");
    exifData.setApertureValue(3.5);
    exifData.setOrientation(1);
    exifData.setFocalLength(35.0);
    exifData.setCompression(6);
    thumbnail.getJpegOptions().setExifData(exifData);
}
```

## Passo 5: Salva le modifiche
Infine, dopo aver modificato i dati EXIF, salva le modifiche in un nuovo file PSD.

```java
try {
    image.save(dataDir + "Modified_Zebras_Serengeti.psd");
} catch (IOException e) {
    e.printStackTrace();
}
```

## Problemi comuni e soluzioni
- **Risorsa thumbnail mancante** – Alcuni JPEG memorizzano EXIF direttamente nell'intestazione dell'immagine principale. Se la risorsa thumbnail è assente, usa `image.getExifData()` invece.  
- **File di grandi dimensioni causano OutOfMemoryError** – Assicurati di eseguire la JVM con abbastanza heap (`-Xmx2g`) o elabora l'immagine in modalità streaming usando `PsdImage.load(inputStream, loadOptions)`.  
- **Tipi di tag non supportati** – Aspose.PSD supporta tutti i tag EXIF standard; i tag personalizzati potrebbero richiedere una gestione manuale a livello di byte.

## Domande frequenti

**Q: Cos'è il dato EXIF?**  
A: I metadati EXIF (Exchangeable Image File Format) memorizzano le impostazioni della fotocamera, i timestamp, le coordinate GPS e altre informazioni incorporate nei file JPEG e in altri file immagine.

**Q: Posso usare Aspose.PSD per Java gratuitamente?**  
A: Puoi ottenere una prova gratuita dalla [Aspose releases page](https://releases.aspose.com/).

**Q: Aspose.PSD per Java è compatibile con tutte le versioni di Java?**  
A: Aspose.PSD per Java supporta Java SE 7 e versioni successive.

**Q: Dove posso trovare ulteriore documentazione su Aspose.PSD per Java?**  
A: Consulta la [documentation](https://reference.aspose.com/psd/java/) per maggiori dettagli.

**Q: Come posso ottenere supporto per Aspose.PSD per Java?**  
A: Puoi ottenere supporto dal [Aspose PSD support forum](https://forum.aspose.com/c/psd/34/).

## Conclusione
Seguendo questi passaggi puoi **java read image metadata** da qualsiasi JPEG, regolare i campi EXIF di cui hai bisogno e scrivere i dati aggiornati nel file—tutto con poche righe di codice Java pulito. L'API ricca di Aspose.PSD rende la gestione dei metadati affidabile e performante, così da poterla integrare in pipeline di elaborazione batch, strumenti di gestione foto o qualsiasi applicazione che necessiti di lavorare con le informazioni delle immagini.

---

**Ultimo aggiornamento:** 2026-10-03  
**Testato con:** Aspose.PSD for Java 24.5  
**Autore:** Aspose

## Tutorial correlati

- [Leggi informazioni su tag EXIF specifici in Java con Aspose (asp)](/psd/java/java-jpeg-image-processing/read-specific-exif-tags-info-java/)
- [Crea metadati XMP nei file PSD usando Aspose.PSD per Java](/psd/java/image-editing/create-xmp-metadata/)
- [Ridimensiona immagine con Aspose.PSD per Java – Disegna forme e operazioni base su immagini](/psd/java/basic-image-operations/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}