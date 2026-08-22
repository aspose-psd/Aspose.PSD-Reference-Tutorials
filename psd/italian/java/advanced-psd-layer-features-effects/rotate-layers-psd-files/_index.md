---
date: 2026-07-22
description: Scopri come salvare PSD come PNG, preservare la trasparenza PNG e ruotare
  i livelli PSD in Java con Aspose.PSD. Guida passo‑passo, spiegazioni senza codice
  e consigli per la risoluzione dei problemi.
keywords:
- save psd as png
- export psd layers png
- convert photoshop file png
- psd to png transparency
lastmod: 2026-07-22
linktitle: salva PSD come PNG e ruota i livelli in Java con Aspose.PSD
og_description: salva PSD come PNG con Aspose.PSD per Java. Preserva la trasparenza,
  ruota i livelli e esporta PNG in poche righe di codice—ideale per flussi di lavoro
  automatizzati.
og_image_alt: 'Developer guide: save PSD as PNG and rotate layers using Aspose.PSD
  for Java'
og_title: salva PSD come PNG e ruota i livelli in Java con Aspose.PSD
schemas:
- author: Aspose
  dateModified: '2026-07-22'
  description: Learn how to save psd as png, preserve PNG transparency, and rotate
    PSD layers in Java with Aspose.PSD. Step‑by‑step guide, code‑free explanations,
    and troubleshooting tips.
  headline: save psd as png and rotate layers in Java using Aspose.PSD
  type: TechArticle
- description: Learn how to save psd as png, preserve PNG transparency, and rotate
    PSD layers in Java with Aspose.PSD. Step‑by‑step guide, code‑free explanations,
    and troubleshooting tips.
  name: save psd as png and rotate layers in Java using Aspose.PSD
  steps:
  - name: Set Up Your Java Project
    text: Create a new Java project in your IDE and add the Aspose.PSD JAR to the
      project’s build path.
  - name: Import Required Classes
    text: '`PsdImage` is the core class that represents a Photoshop document in memory.
      `PngOptions` controls PNG‑specific settings, and `RotateFlipType` defines rotation
      and flip operations. These imports give you access to image loading, rotation,
      and PNG‑specific options.'
  - name: Define File Paths
    text: Specify where your source PSD lives and where the output files should be
      written. Using absolute paths during testing avoids “file not found” errors.
      > **Pro tip:** Store paths in a configuration file for easier maintenance in
      larger projects.
  - name: Load the PSD File
    text: '`PsdImage` loads the entire Photoshop document, including all layers, masks,
      and effects, into a manipulable object. Now `im` represents the whole PSD, ready
      for transformations.'
  - name: Rotate the Image (How to rotate PSD)
    text: '`RotateFlipType` enumerates all supported rotations and flips. In this
      example we rotate 270° and flip both axes, which swaps width and height while
      mirroring the image. Feel free to experiment with other values such as `Rotate90FlipNone`
      or `Rotate180FlipX`.'
  - name: Save the Rotated Image as PNG (save PSD as PNG)
    text: Configure `PngOptions` to keep transparency (`PngColorType.TruecolorWithAlpha`)
      and then call `save`. The PNG retains layer transparency, ensuring it works
      seamlessly in web or mobile apps. The resulting PNG preserves alpha channels,
      making it suitable for compositing or further processing.
  - name: Save the Modified PSD (optional)
    text: If you also need a new PSD with the rotation applied, you can save the modified
      `PsdImage` back to disk. You now have both a PNG preview and an updated PSD
      file.
  type: HowTo
- questions:
  - answer: Yes, you can call `layer.rotateFlip(RotateFlipType.Rotate90FlipNone)`
      after iterating through `im.getLayers()`.
    question: Can I rotate a specific layer in a PSD file?
  - answer: The library handles most files efficiently, but extremely large PSDs (>500
      MB) may require additional memory or streaming options.
    question: Is there any performance limitation with Aspose.PSD for Java?
  - answer: Aspose offers a free trial, but a paid license is needed for production.
      See the [temporary license](https://purchase.aspose.com/temporary-license/)
      for testing.
    question: Is Aspose.PSD free to use?
  - answer: Comprehensive docs are available at [Aspose.PSD Documentation](https://reference.aspose.com/psd/java/).
    question: Where can I find detailed documentation?
  - answer: Get help via the [Aspose Support Forum](https://forum.aspose.com/c/psd/34).
    question: What if I encounter issues while using Aspose.PSD?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- convert PSD
- Aspose.PSD
- Java image processing
- rotate PSD layers
title: salva PSD come PNG e ruota i livelli in Java con Aspose.PSD
url: /it/java/advanced-psd-layer-features-effects/rotate-layers-psd-files/
weight: 21
---

## Tutorial correlati

- [Save PSD as PNG and Apply Rendering Drop Shadow in Aspose.PSD for Java](/psd/java/advanced-image-manipulation/rendering-drop-shadow/)
- [How to compress PNG files using Aspose.PSD for Java](/psd/java/optimizing-png-files/compress-png-files/)
- [How to Rotate Image in Java with Aspose.PSD](/psd/java/advanced-image-manipulation/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< blocks/products/pf/main-wrap-class >}}

# salva PSD come PNG e ruota i livelli in Java usando Aspose.PSD

## Introduzione
Se hai bisogno di **salvare PSD come PNG** ruotando anche i livelli, questa guida è per te. Che tu stia creando uno strumento di elaborazione batch, un servizio web che richiede manipolazione di immagini al volo, o semplicemente automatizzando un flusso di lavoro di design, farlo programmaticamente fa risparmiare tempo e rimuove la dipendenza da Adobe Photoshop. In questo tutorial vedremo **come ruotare i livelli PSD** ed esportare il risultato come PNG usando la libreria Aspose.PSD per Java. Arrotiniamoci le maniche e facciamo funzionare senza intoppi il tuo flusso di lavoro di design!

## Risposte rapide
- **Quale libreria posso usare?** Aspose.PSD for Java  
- **Posso sia ruotare che salvare PSD come PNG in un unico passaggio?** Sì – ruota il PSD poi salvalo come PNG  
- **Ho bisogno di una licenza?** Una prova gratuita è sufficiente per i test; è necessaria una licenza a pagamento per la produzione  
- **Quale versione di Java è supportata?** Java 8 e successive  
- **L'output PNG è trasparente?** Sì, quando imposti `PngColorType.TruecolorWithAlpha`

## Cos'è “convertire PSD in PNG”
Convertire un documento Photoshop (PSD) in un'immagine PNG estrae il contenuto visivo — inclusi livelli, maschere e canali alfa — in un formato raster ampiamente supportato che preserva la trasparenza. Questo rende il PNG ideale per grafiche web, miniature e per l'elaborazione di immagini a valle. Il PNG risultante può essere usato direttamente nelle pagine web, nelle app mobili o ulteriormente elaborato da altre librerie di immagini.

## Perché usare Aspose.PSD per Java per salvare PSD come PNG e ruotare i livelli PSD?
Aspose.PSD ti consente di **salvare PSD come PNG** e ruotare i livelli senza installare Photoshop. Supporta **oltre 50 formati di input e output**, elabora file PSD di centinaia di pagine usando meno di 200 MB di RAM, e funziona su Windows, Linux e macOS. L'API richiede solo poche chiamate di metodo, fornendo risultati ad alta fedeltà con gestione integrata di effetti di livello, maschere e canali alfa.

## Prerequisiti
- **Java Development Kit (JDK)** – scarica dal [sito Oracle](https://www.oracle.com/java/technologies/javase-downloads.html).  
- **Integrated Development Environment (IDE)** – IntelliJ IDEA, Eclipse o NetBeans vanno tutti bene.  
- **Libreria Aspose.PSD per Java** – ottieni l'ultimo JAR dalla [pagina di rilascio](https://releases.aspose.com/psd/java/).  
- **Conoscenza di base di Java** – familiarità con classi, oggetti e gestione delle eccezioni.

## Guida passo‑passo

### Passo 1: Configura il tuo progetto Java
Crea un nuovo progetto Java nel tuo IDE e aggiungi il JAR di Aspose.PSD al percorso di compilazione del progetto.

### Passo 2: Importa le classi necessarie
`PsdImage` è la classe principale che rappresenta un documento Photoshop in memoria. `PngOptions` controlla le impostazioni specifiche per PNG, e `RotateFlipType` definisce le operazioni di rotazione e capovolgimento.

```java
import com.aspose.psd.Image;
import com.aspose.psd.RotateFlipType;
import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.PngOptions;
```

Queste importazioni ti danno accesso al caricamento dell'immagine, alla rotazione e alle opzioni specifiche per PNG.

### Passo 3: Definisci i percorsi dei file
Specifica dove si trova il tuo PSD di origine e dove devono essere scritti i file di output. Usare percorsi assoluti durante i test evita errori “file non trovato”.

```java
String dataDir = "Your Document Directory"; // Change this to your actual document directory.
String sourceFile = dataDir + "1.psd"; // Source PSD file
String pngPath = dataDir + "RotateFlipTest2617.png"; // Output PNG file path
String psdPath = dataDir + "RotateFlipTest2617.psd"; // Output PSD file path
```

> **Consiglio professionale:** Conserva i percorsi in un file di configurazione per una manutenzione più semplice nei progetti più grandi.

### Passo 4: Carica il file PSD
`PsdImage` carica l'intero documento Photoshop, inclusi tutti i livelli, le maschere e gli effetti, in un oggetto manipolabile.

```java
PsdImage im = (PsdImage) Image.load(sourceFile);
```

Ora `im` rappresenta l'intero PSD, pronto per le trasformazioni.

### Passo 5: Ruota l'immagine (Come ruotare PSD)
`RotateFlipType` elenca tutte le rotazioni e i capovolgimenti supportati. In questo esempio ruotiamo di 270° e capovolgiamo entrambi gli assi, il che scambia larghezza e altezza mentre si specchia l'immagine.

```java
int flipType = RotateFlipType.Rotate270FlipXY; // Choose the rotation type
im.rotateFlip(flipType); // Rotate the image
```

Sentiti libero di sperimentare altri valori come `Rotate90FlipNone` o `Rotate180FlipX`.

### Passo 6: Salva l'immagine ruotata come PNG (salva PSD come PNG)
Configura `PngOptions` per mantenere la trasparenza (`PngColorType.TruecolorWithAlpha`) e poi chiama `save`. Il PNG conserva la trasparenza dei livelli, garantendo che funzioni senza problemi in app web o mobili.

```java
PngOptions options = new PngOptions();
options.setColorType(PngColorType.TruecolorWithAlpha); // Preserve transparency
im.save(pngPath, options); // Save the rotated image
```

Il PNG risultante preserva i canali alfa, rendendolo adatto per il compositing o ulteriori elaborazioni.

### Passo 7: Salva il PSD modificato (opzionale)
Se hai bisogno anche di un nuovo PSD con la rotazione applicata, puoi salvare il `PsdImage` modificato nuovamente su disco.

```java
im.save(psdPath);
```

Ora hai sia un'anteprima PNG sia un file PSD aggiornato.

## Problemi comuni e soluzioni
- **File non trovato:** Verifica che `dataDir` termini con un separatore di percorso (`/` o `\`).  
- **OutOfMemoryError su PSD grandi:** Aumenta la dimensione dell'heap JVM (`-Xmx2g`).  
- **Trasparenza persa:** Assicurati che `PngColorType.TruecolorWithAlpha` sia impostato; altrimenti il PNG verrà salvato senza alfa.  
- **Capovolgimento dell'immagine PSD non si comporta come previsto:** Ricontrolla la costante `RotateFlipType` selezionata; alcune costanti combinano rotazione e capovolgimento in un unico passaggio.

## Domande frequenti

**Q:** Posso ruotare un livello specifico in un file PSD?  
**A:** Sì, puoi chiamare `layer.rotateFlip(RotateFlipType.Rotate90FlipNone)` dopo aver iterato su `im.getLayers()`.

**Q:** Esiste qualche limitazione di prestazioni con Aspose.PSD per Java?  
**A:** La libreria gestisce la maggior parte dei file in modo efficiente, ma PSD estremamente grandi (>500 MB) potrebbero richiedere memoria aggiuntiva o opzioni di streaming.

**Q:** Aspose.PSD è gratuito?  
**A:** Aspose offre una prova gratuita, ma è necessaria una licenza a pagamento per la produzione. Vedi la [licenza temporanea](https://purchase.aspose.com/temporary-license/) per i test.

**Q:** Dove posso trovare la documentazione dettagliata?  
**A:** Documentazione completa è disponibile su [Aspose.PSD Documentation](https://reference.aspose.com/psd/java/).

**Q:** Cosa fare se incontro problemi usando Aspose.PSD?  
**A:** Ottieni aiuto tramite il [Forum di supporto Aspose](https://forum.aspose.com/c/psd/34).

**Q:** La conversione da PSD a PNG preserva gli effetti di livello?  
**A:** Sì, quando salvi con `PngColorType.TruecolorWithAlpha`, la maggior parte degli effetti visivi viene rasterizzata nel PNG.

**Q:** Posso elaborare in batch più file PSD?  
**A:** Assolutamente. Avvolgi il codice in un ciclo che itera su una cartella di file PSD.

**Q:** È possibile impostare il livello di compressione PNG?  
**A:** `PngOptions` fornisce un metodo `setCompressionLevel(int)` per regolare finemente la dimensione dell'output.

**Q:** Devo chiudere l'oggetto immagine?  
**A:** `PsdImage` implementa `Closeable`; usa try‑with‑resources o chiama `im.close()` in un blocco `finally`.

**Q:** Il PNG ruotato avrà le stesse dimensioni dell'originale?  
**A:** Ruotare di 90° o 270° scambia larghezza e altezza, quindi il PNG riflette automaticamente la nuova orientazione.

## Conclusione
Utilizzando Aspose.PSD per Java, puoi **salvare PSD come PNG**, **preservare la trasparenza PNG** e **ruotare i livelli PSD** con poche righe di codice. Questo approccio elimina la necessità di Photoshop, accelera i flussi di lavoro automatizzati e ti dà il pieno controllo sull'output dell'immagine. Provalo nei tuoi progetti e scopri quanto tempo risparmi!

---

**Ultimo aggiornamento:** 2026-07-22  
**Testato con:** Aspose.PSD for Java 24.11  
**Autore:** Aspose  

{{< blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/products-backtop-button >}}