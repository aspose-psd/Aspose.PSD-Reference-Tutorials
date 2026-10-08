---
date: 2026-10-08
description: 'Tutorial di elaborazione immagini Java: impara a manipolare file PSD
  e salvarli come JPEG usando Aspose.PSD. Guida passo‑passo con esempi di codice per
  principianti e professionisti.'
keywords:
- java image processing tutorial
- Aspose.PSD
- 2 bit JPEG
- 7 bit JPEG
lastmod: 2026-10-08
linktitle: Supporto per JPEG a 2 e 7 bit in Java
og_description: 'Tutorial di elaborazione immagini Java: impara a manipolare file
  PSD e salvarli come JPEG usando Aspose.PSD. Passaggi dettagliati, risposte rapide
  e risoluzione dei problemi per gli sviluppatori.'
og_image_alt: Guide to processing 2‑ and 7‑bit JPEG images in Java with Aspose.PSD
og_title: 'Tutorial di elaborazione immagini Java: supporto JPEG a 2‑ e 7‑bit'
schemas:
- author: Aspose
  dateModified: '2026-10-08'
  description: 'Java image processing tutorial: learn how to manipulate PSD files
    and save them as JPEGs using Aspose.PSD. Step‑by‑step guide with code examples
    for beginners and pros.'
  headline: 'Java image processing tutorial: support 2‑ and 7‑bit JPEGs'
  type: TechArticle
- description: 'Java image processing tutorial: learn how to manipulate PSD files
    and save them as JPEGs using Aspose.PSD. Step‑by‑step guide with code examples
    for beginners and pros.'
  name: 'Java image processing tutorial: support 2‑ and 7‑bit JPEGs'
  steps:
  - name: '**Java Development Kit (JDK)** – version 8 or higher.'
    text: '**Java Development Kit (JDK)** – version 8 or higher.'
  - name: '**Aspose.PSD for Java library** – you can [download it here](https://releases.aspose.com/psd/java/).'
    text: '**Aspose.PSD for Java library** – you can [download it here](https://releases.aspose.com/psd/java/).'
  - name: '**IDE** – IntelliJ IDEA, Eclipse, or NetBeans.'
    text: '**IDE** – IntelliJ IDEA, Eclipse, or NetBeans.'
  - name: '**Sample PSD file** – any PSD you wish to convert.'
    text: '**Sample PSD file** – any PSD you wish to convert.'
  - name: '**Basic Java knowledge** – familiarity with classes, objects, and exception
      handling.'
    text: '**Basic Java knowledge** – familiarity with classes, objects, and exception
      handling.'
  type: HowTo
- questions:
  - answer: Aspose.PSD for Java is a commercial library that enables creation, manipulation,
      and conversion of Photoshop PSD files directly from Java applications.
    question: What is Aspose.PSD for Java?
  - answer: You can download the library from the [website](https://releases.aspose.com/psd/java/)
      and add the JAR to your project’s build path or Maven/Gradle dependencies.
    question: How do I install Aspose.PSD for Java?
  - answer: Yes, you can load custom RGB or CMYK ICC profiles and assign them to the
      `JpegOptions` before saving.
    question: Can I use custom color profiles with Aspose.PSD for Java?
  - answer: It supports PSD, JPEG, PNG, BMP, TIFF, GIF, and over 20 additional raster
      formats.
    question: What image formats does Aspose.PSD for Java support?
  - answer: Yes, you can download a [free trial](https://releases.aspose.com/) to
      evaluate the library before purchasing a license.
    question: Is there a free trial available for Aspose.PSD for Java?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- java image processing
- Aspose.PSD
- JPEG conversion
title: 'Tutorial di elaborazione immagini Java: supporto JPEG a 2‑ e 7‑bit'
url: /it/java/java-jpeg-image-processing/support-2-7-bits-jpeg-java/
weight: 20
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Tutorial di elaborazione immagini Java: supporto JPEG a 2‑ e 7‑bit

## Introduzione
In questo **java image processing tutorial**, scoprirai come utilizzare la libreria Aspose.PSD for Java per caricare un file PSD ed esportarlo come JPEG a 2‑ o 7‑bit. Che tu stia creando un servizio di conversione batch o abbia bisogno di un controllo fine sulla qualità dell’immagine, i passaggi seguenti ti guideranno dall’impostazione dell’ambiente al salvataggio del JPEG finale. Iniziamo!

## Risposte rapide
- **Quale libreria gestisce JPEG a 2‑ e 7‑bit?** Aspose.PSD for Java.  
- **Versione minima di Java?** JDK 8 o successiva.  
- **È necessaria una licenza per lo sviluppo?** Una prova gratuita è sufficiente per la valutazione; è richiesta una licenza commerciale per la produzione.  
- **Posso cambiare il modo colore?** Sì – CMYK, YCCK e altri modi sono supportati tramite `JpegCompressionColorMode`.  
- **Quanto riduzione di dimensione file posso aspettarmi?** L’utilizzo di 2‑bit per canale può ridurre il JPEG fino all’80 % rispetto a un output a 8‑bit.

## Cos'è il tutorial di elaborazione immagini Java?
Un tutorial di elaborazione immagini Java è una guida passo‑a‑passo che insegna agli sviluppatori come manipolare programmaticamente i dati delle immagini usando Java. Copre il caricamento di vari formati, l’applicazione di trasformazioni, la regolazione di colore e impostazioni di compressione, e il salvataggio dei risultati, consentendoti di creare flussi di lavoro personalizzati per la gestione delle immagini.

## Perché usare Aspose.PSD per Java?
Aspose.PSD per Java offre un’API completa per lavorare con file Photoshop senza richiedere Photoshop stesso. Supporta oltre 30 formati immagine, gestisce file fino a 2 GB tramite streaming dei dati e offre un controllo fine su livelli, canali e profili colore, rendendola ideale per elaborazioni ad alte prestazioni lato server.

## Prerequisiti
Prima di iniziare, verifica di avere quanto segue:

1. **Java Development Kit (JDK)** – versione 8 o superiore.  
2. **Aspose.PSD for Java library** – è possibile [download it here](https://releases.aspose.com/psd/java/).  
3. **IDE** – IntelliJ IDEA, Eclipse o NetBeans.  
4. **File PSD di esempio** – qualsiasi PSD che desideri convertire.  
5. **Conoscenze di base di Java** – familiarità con classi, oggetti e gestione delle eccezioni.

## Importare i pacchetti
Per prima cosa, aggiungi il JAR di Aspose.PSD al classpath del tuo progetto. Quindi importa gli spazi dei nomi richiesti:

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.jpeg.JpegCompressionColorMode;
import com.aspose.psd.fileformats.jpeg.JpegCompressionMode;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.JpegOptions;
```

## Come caricare un'immagine PSD in Java?
Per caricare un file PSD, chiama il metodo statico `load` della classe `Image` e cast il risultato a `PsdImage`. Questo crea una rappresentazione in memoria del documento Photoshop, dandoti accesso a livelli, canali, maschere e metadati, che puoi poi manipolare o esportare in altri formati.

`PsdImage` è la classe principale di Aspose.PSD che rappresenta un documento Photoshop in memoria, consentendo operazioni di lettura/scrittura sul suo contenuto.

```java
String dataDir = "Your Document Directory";
PsdImage image = (PsdImage) Image.load(dataDir + "PsdImage.psd");
```

## Come configurare le opzioni JPEG per output a 2‑ o 7‑bit?
Crea una nuova istanza di `JpegOptions` e imposta le sue proprietà per corrispondere all’output desiderato. Usa `setColorType` per scegliere il `JpegCompressionColorMode` appropriato (ad es. CMYK o YCCK) e `setCompressionType` per selezionare l’algoritmo di compressione. Infine, assegna il valore `bitsPerChannel` (2 o 7) per controllare la profondità di bit di ciascun canale colore.

```java
JpegOptions options = new JpegOptions();
options.setColorType(JpegCompressionColorMode.Cmyk);
options.setCompressionType(JpegCompressionMode.JpegLs);
```

## Come impostare i bit per canale per JPEG a bassa profondità?
`bitsPerChannel` specifica il numero di bit usati per ciascun canale colore nel JPEG di output. Impostare questa proprietà a 2 riduce ogni canale a due bit, producendo un’immagine altamente compressa con bande visibili, mentre un valore di 7 conserva più dettagli e genera una dimensione file intermedia tra l’estremo a bassa profondità e l’output standard a 8‑bit. Scegli il valore che bilancia qualità e dimensione per il tuo caso d’uso.

```java
byte bpp = 2;
options.setBitsPerChannel(bpp);
```

## Come applicare i profili colore (opzionale)?
`ICCProfile` rappresenta un profilo International Color Consortium che descrive le caratteristiche colore di un dispositivo o spazio di lavoro. Se possiedi un file ICC personalizzato, caricalo con `ICCProfile.getInstance(path)` e assegnalo alla proprietà `iccProfile` dell’oggetto `jpegOptions`. Lasciare la proprietà null fa sì che Aspose.PSD utilizzi il profilo di sistema predefinito, adeguato per la maggior parte degli scenari.

```java
options.setRgbColorProfile(null);
options.setCmykColorProfile(null);
```

## Come salvare l'immagine elaborata come JPEG?
Il metodo `save` scrive l’immagine su file usando le opzioni fornite. Invocalo sull’istanza `PsdImage`, passando il nome file di destinazione (inclusa l’estensione .jpg) e le `JpegOptions` configurate. La libreria gestisce la codifica, applica i bit‑per‑canale e il profilo colore selezionati, e produce un JPEG che corrisponde alle tue specifiche.

```java
image.save(dataDir + "2_7BitsJPEG_output.jpg", options);
```

## Problemi comuni e soluzioni
- **Errore file troppo grande** – Assicurati di utilizzare l’ultima versione di Aspose.PSD, che effettua lo streaming dei dati e evita di caricare l’intero file in RAM.  
- **Colori inattesi** – Verifica che il `JpegCompressionColorMode` selezionato corrisponda allo spazio colore della tua immagine di origine.  
- **Profilo ICC mancante** – Se ti serve un profilo specifico, caricalo con `ICCProfile.getInstance(path)` e assegnalo a `JpegOptions`.

## Domande frequenti

**Q: Cos'è Aspose.PSD per Java?**  
A: Aspose.PSD per Java è una libreria commerciale che consente la creazione, manipolazione e conversione di file Photoshop PSD direttamente da applicazioni Java.

**Q: Come installo Aspose.PSD per Java?**  
A: Puoi scaricare la libreria dal [website](https://releases.aspose.com/psd/java/) e aggiungere il JAR al percorso di compilazione del tuo progetto o alle dipendenze Maven/Gradle.

**Q: Posso usare profili colore personalizzati con Aspose.PSD per Java?**  
A: Sì, è possibile caricare profili ICC RGB o CMYK personalizzati e assegnarli a `JpegOptions` prima del salvataggio.

**Q: Quali formati immagine supporta Aspose.PSD per Java?**  
A: Supporta PSD, JPEG, PNG, BMP, TIFF, GIF e oltre 20 formati raster aggiuntivi.

**Q: È disponibile una prova gratuita per Aspose.PSD per Java?**  
A: Sì, puoi scaricare una [free trial](https://releases.aspose.com/) per valutare la libreria prima di acquistare una licenza.

---

**Ultimo aggiornamento:** 2026-10-08  
**Testato con:** Aspose.PSD 24.12 for Java  
**Autore:** Aspose

## Tutorial correlati

- [Elaborazione immagini Java – Supporto per JPEG-LS con CMYK](/psd/java/java-jpeg-image-processing/support-jpeg-ls-cmyk-java/)
- [Salva PSD come JPEG e supporta colore RGB con Aspose.PSD Java](/psd/java/advanced-psd-layer-features-effects/support-rgb-color-psd-files/)
- [Come convertire PSD in formati immagine raster con Aspose.PSD per Java](/psd/java/advanced-techniques/convert-psd-to-raster-formats/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}