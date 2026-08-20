---
date: 2026-05-19
description: Scopri come ruotare un'immagine a un angolo specifico in Java usando
  Aspose.PSD. La guida copre rotate image java, rotate image specific angle, background
  handling e altro.
keywords:
- how to rotate image
- rotate image specific angle
- rotate image java
- rotate image background
- rotate image degrees
linktitle: Come ruotare un'immagine a un angolo specifico
schemas:
- author: Aspose
  dateModified: '2026-05-19'
  description: Learn how to rotate image on a specific angle in Java using Aspose.PSD.
    The guide covers rotate image java, rotate image specific angle, background handling
    and more.
  headline: How to Rotate Image on a Specific Angle with Aspose.PSD for Java
  type: TechArticle
- description: Learn how to rotate image on a specific angle in Java using Aspose.PSD.
    The guide covers rotate image java, rotate image specific angle, background handling
    and more.
  name: How to Rotate Image on a Specific Angle with Aspose.PSD for Java
  steps:
  - name: Define Your Document Directory
    text: Set the folder that holds the source PSD and where the output will be written.
      Using an absolute path or `System.getProperty("user.dir")` eliminates relative‑path
      surprises.
  - name: Specify Source and Destination File Paths
    text: Provide the full file names for the input PSD and the desired output format
      (e.g., PNG, JPEG, TIFF). Changing the extension in `destName` automatically
      selects the appropriate encoder.
  - name: Load the Image
    text: The `Image.load` method detects the file format and returns a concrete `RasterImage`
      instance ready for raster operations. The `Image` class is a factory that reads
      a file from disk and creates an in‑memory representation suitable for further
      processing. It supports automatic format detection for al
  - name: Cache Image Data (Optional but Recommended)
    text: Calling `image.cacheData()` stores pixel data in memory, dramatically speeding
      up subsequent transformations—especially for large PSD files that would otherwise
      trigger repeated disk I/O. The `cacheData()` method forces the image to be fully
      loaded into RAM, reducing the overhead of lazy loading dur
  - name: Rotate the Image
    text: 'Invoke `rotate` with three arguments: the rotation angle (float), a flag
      to expand the canvas, and the background color for the newly exposed corners.
      The `rotate` method rotates the image around its centre, optionally enlarging
      the canvas to accommodate the rotated bounds. The background `Color` fi'
  - name: Save the Result
    text: Choose an encoder (JPEG, PNG, etc.) and call `save`. `JpegOptions` lets
      you adjust quality, while `PngOptions` provides lossless output. The `save`
      method writes the transformed image to disk using the specified options object,
      ensuring that compression level and color depth are preserved as require
  type: HowTo
- questions:
  - answer: Yes. The library preserves alpha channels; omit an opaque background color
      to keep corners transparent.
    question: Can I rotate images with transparency using Aspose.PSD for Java?
  - answer: No. Aspose.PSD supports PSD, JPEG, PNG, TIFF, GIF, BMP, JPEG2000, WMF,
      EMF, and 30+ additional formats.
    question: Are there any limitations on the image file formats supported for rotation?
  - answer: Absolutely. Pass a negative float to `rotate` (e.g., `-30f`) to rotate
      clockwise.
    question: Can I rotate images by a negative angle?
  - answer: The API is server‑side only. For live previews, render the rotated bitmap
      in a UI framework such as Swing or JavaFX and refresh the view.
    question: Does Aspose.PSD provide real‑time image preview during rotation?
  - answer: Yes, visit the [Aspose.PSD forum](https://forum.aspose.com/c/psd/34) to
      ask questions and share experiences.
    question: Is there a community forum for Aspose.PSD where I can seek help?
  type: FAQPage
second_title: Aspose.PSD Java API
title: Come ruotare un'immagine a un angolo specifico con Aspose.PSD per Java
url: /it/java/advanced-image-manipulation/rotate-image-specific-angle/
weight: 20
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Come ruotare un'immagine di un angolo specifico con Aspose.PSD per Java

Se hai bisogno di **come ruotare l'immagine** programmaticamente in un'applicazione Java, Aspose.PSD per Java offre un'API pulita e ad alte prestazioni che si occupa del lavoro pesante. Che tu stia creando un editor fotografico, generando miniature o preparando risorse per un servizio web, ruotare un'immagine di un angolo preciso è una necessità comune. In questo tutorial percorreremo l'intero processo—from loading a PSD file to saving the rotated result—while highlighting best practices such as caching and background handling.

## Risposte rapide
- **Qual è la libreria migliore per ruotare le immagini in Java?** Aspose.PSD per Java fornisce il motore di rotazione più affidabile.  
- **Posso ruotare di qualsiasi angolo?** Sì, il metodo `rotate` accetta un angolo di tipo `float`, positivo o negativo.  
- **Ho bisogno di una licenza per lo sviluppo?** Una prova gratuita funziona per i test; è necessaria una licenza commerciale per la produzione.  
- **Quali formati immagine sono supportati?** PSD, JPEG, PNG, TIFF, GIF, BMP, JPEG2000, WMF, EMF e oltre 30 formati aggiuntivi.  
- **Come impostare un colore di sfondo per lo spazio vuoto?** Passa un'istanza `Color` al metodo `rotate`.

## Come ruotare un'immagine di un angolo specifico con Aspose.PSD per Java?

Carica il tuo file sorgente, chiama `image.rotate(angle, true, backgroundColor)` e poi salva—tre passaggi concisi che gestiscono tutta la matematica complessa per te. Aspose.PSD preserva i livelli, i profili colore e i canali alfa espandendo la tela per evitare il ritaglio, così l'output appare esattamente come previsto anche per angoli frazionari come 12,5°. Questo approccio funziona per file che vanno da pochi kilobyte a PSD di centinaia di pagine senza esaurire la memoria.

## Cos'è la rotazione delle immagini in Java?

La rotazione delle immagini è la trasformazione geometrica che ruota una matrice di pixel attorno a un punto di pivot—di solito il centro dell'immagine—di un angolo specificato. In Java puro dovresti manipolare un oggetto `Graphics2D`, calcolare gli offset trigonometrici e gestire manualmente lo sfondo. Aspose.PSD astrae tutta questa complessità, gestendo automaticamente le profondità di colore, le maschere dei livelli e i diversi formati di file.

## Perché usare Aspose.PSD per ruotare le immagini?

Aspose.PSD supporta **oltre 30 formati di input e output** e può elaborare **file PSD di 500 pagine in meno di 5 secondi** su una tipica CPU di classe server. Il caching integrato della libreria (`image.cacheData()`) riduce l'uso della memoria fino al 60 % per risorse di grandi dimensioni, e il metodo `rotate` ti consente di specificare un colore di sfondo, preservando gli angoli trasparenti quando necessario. Questi vantaggi quantificati lo rendono la scelta standard del settore per pipeline di immagini ad alta velocità.

## Prerequisiti

Prima di iniziare, assicurati di avere:

1. **Java Development Kit (JDK 8 o successivo)** – qualsiasi IDE o ambiente da riga di comando va bene.  
2. **Aspose.PSD per Java** – scarica l'ultimo JAR dalla [pagina Aspose.PSD Java](https://reference.aspose.com/psd/java/).  
3. **Un file PSD di esempio** – ad es., `sample.psd` posizionato in una cartella che puoi riferire dal tuo codice.

## Importa pacchetti

La classe `RasterImage` e le utility correlate sono il nucleo del flusso di lavoro di rotazione.

La classe `RasterImage` è l'oggetto principale di Aspose.PSD per la manipolazione di immagini raster. Fornisce metodi per caricare, trasformare e salvare immagini raster preservando i metadati.

## Guida passo‑passo

### Passo 1: Definisci la directory del documento

Imposta la cartella che contiene il PSD sorgente e dove verrà scritto l'output. Usare un percorso assoluto o `System.getProperty("user.dir")` elimina sorprese legate ai percorsi relativi.

```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.imageoptions.JpegOptions;
```

### Passo 2: Specifica i percorsi dei file di origine e destinazione

Fornisci i nomi completi dei file per il PSD di input e il formato di output desiderato (ad es., PNG, JPEG, TIFF). Cambiando l'estensione in `destName` si seleziona automaticamente l'encoder appropriato.

```java
String dataDir = "Your Document Directory";
```

### Passo 3: Carica l'immagine

Il metodo `Image.load` rileva il formato del file e restituisce un'istanza concreta di `RasterImage` pronta per le operazioni raster.

La classe `Image` è una factory che legge un file dal disco e crea una rappresentazione in memoria adatta per ulteriori elaborazioni. Supporta il rilevamento automatico del formato per tutti i più di 30 tipi supportati.

```java
String sourceFile = dataDir + "sample.psd";
String destName = dataDir + "RotatingImageOnSpecificAngle_out.jpg";
```

### Passo 4: Cache dei dati immagine (Opzionale ma consigliato)

Chiamare `image.cacheData()` memorizza i dati dei pixel in memoria, accelerando notevolmente le trasformazioni successive—specialmente per file PSD di grandi dimensioni che altrimenti provocherebbero I/O disco ripetuto.

Il metodo `cacheData()` forza l'immagine a essere completamente caricata in RAM, riducendo l'overhead del caricamento lazy durante operazioni intensive.

```java
RasterImage image = (RasterImage)Image.load(sourceFile);
```

### Passo 5: Ruota l'immagine

Invoca `rotate` con tre argomenti: l'angolo di rotazione (float), un flag per espandere la tela e il colore di sfondo per gli angoli appena esposti.

Il metodo `rotate` ruota l'immagine attorno al suo centro, ingrandendo opzionalmente la tela per contenere i limiti ruotati. Il `Color` di sfondo riempie qualsiasi spazio vuoto, evitando angoli trasparenti o neri.

- **20f** – angolo di rotazione in gradi (float). Cambia questo valore per qualsiasi angolo, ad es., `-45f` per rotazione in senso orario.  
- **true** – mantiene il rapporto d'aspetto originale mentre espande la tela.  
- **Color.getRed()** – colore di sfondo che riempie gli angoli vuoti; sostituiscilo con `Color.getWhite()` o qualsiasi colore personalizzato secondo necessità.

```java
if (!image.isCached())
{
    image.cacheData();
}
```

### Passo 6: Salva il risultato

Scegli un encoder (JPEG, PNG, ecc.) e chiama `save`. `JpegOptions` ti permette di regolare la qualità, mentre `PngOptions` fornisce un output senza perdita.

Il metodo `save` scrive l'immagine trasformata su disco usando l'oggetto opzioni specificato, garantendo che il livello di compressione e la profondità di colore siano preservati come richiesto.

```java
image.rotate(20f, true, Color.getRed());
```

## Problemi comuni e soluzioni

| Issue | Cause | Fix |
|-------|-------|-----|
| **Angoli vuoti dopo la rotazione** | Nessun colore di sfondo fornito | Passa un `Color` (ad es., `Color.getWhite()`) a `rotate`. |
| **Errore out‑of‑memory su PSD grandi** | Immagine non cacheata | Chiama `image.cacheData()` prima dell'elaborazione. |
| **Direzione dell'angolo errata** | Confusione tra angolo negativo e positivo | Usa valori negativi per rotazione in senso orario (o vice‑versa a seconda del tuo sistema di coordinate). |
| **Modifiche non salvate** | Dimenticare di chiamare `save` | Assicurati che `image.save(...)` venga eseguito dopo la rotazione. |

## Domande frequenti

**Q: Posso ruotare immagini con trasparenza usando Aspose.PSD per Java?**  
A: Sì. La libreria preserva i canali alfa; ometti un colore di sfondo opaco per mantenere gli angoli trasparenti.

**Q: Ci sono limitazioni sui formati di file immagine supportati per la rotazione?**  
A: No. Aspose.PSD supporta PSD, JPEG, PNG, TIFF, GIF, BMP, JPEG2000, WMF, EMF e oltre 30 formati aggiuntivi.

**Q: Posso ruotare le immagini di un angolo negativo?**  
A: Assolutamente. Passa un float negativo a `rotate` (ad es., `-30f`) per ruotare in senso orario.

**Q: Aspose.PSD fornisce un'anteprima immagine in tempo reale durante la rotazione?**  
A: L'API è solo lato server. Per anteprime live, renderizza il bitmap ruotato in un framework UI come Swing o JavaFX e aggiorna la vista.

**Q: Esiste un forum della community per Aspose.PSD dove posso chiedere aiuto?**  
A: Sì, visita il [forum Aspose.PSD](https://forum.aspose.com/c/psd/34) per fare domande e condividere esperienze.

---

**Last Updated:** 2026-05-19  
**Testato con:** Aspose.PSD per Java 24.11 (ultima versione al momento della scrittura)  
**Autore:** Aspose  

{{< blocks/products/products-backtop-button >}}

```java
image.save(destName, new JpegOptions());
```

## Tutorial correlati

- [Ridimensionamento di immagini ad alta qualità con Bicubic Resampler in Aspose.PSD per Java](/psd/java/advanced-image-manipulation/implement-bicubic-resampler/)
- [Ridimensiona immagine Java - Utilizzando l'enumerazione Resize Type in Aspose.PSD per Java](/psd/java/advanced-image-manipulation/resizing-with-resize-type-enumeration/)
- [Sfoca immagine Java con Aspose.PSD – Aggiungi effetto blur](/psd/java/advanced-techniques/blur-image/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}