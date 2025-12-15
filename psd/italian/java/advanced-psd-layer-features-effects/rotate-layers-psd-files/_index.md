---
date: 2025-12-15
description: Scopri come convertire PSD in PNG e ruotare i livelli PSD in Java usando
  Aspose.PSD. Guida passo‑passo con esempi di codice.
linktitle: Convert PSD to PNG and Rotate Layers in PSD Files using Java
second_title: Aspose.PSD Java API
title: Converti PSD in PNG e ruota i livelli nei file PSD usando Java
url: /it/java/advanced-psd-layer-features-effects/rotate-layers-psd-files/
weight: 21
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Convertire PSD in PNG e ruotare i livelli nei file PSD usando Java

## Introduzione
Se hai bisogno di **convertire PSD in PNG** ruotando anche i livelli, questa guida è per te. Che tu stia creando uno strumento di elaborazione batch o integrando la manipolazione di immagini in un servizio web, farlo programmaticamente fa risparmiare tempo e rimuove la dipendenza da Adobe Photoshop. In questo tutorial ti mostreremo **come ruotare i livelli PSD** ed esportare il risultato come PNG usando la libreria Aspose.PSD per Java. Arrotoliamo le maniche e facciamo funzionare il tuo flusso di lavoro di design!

## Risposte rapide
- **Quale libreria posso usare?** Aspose.PSD per Java  
- **Posso sia ruotare che convertire in un unico passaggio?** Sì – ruota il PSD poi salva come PNG  
- **È necessaria una licenza?** Una prova gratuita è sufficiente per i test; per la produzione è richiesta una licenza a pagamento  
- **Quale versione di Java è supportata?** Java 8 e successive  
- **L'output PNG è trasparente?** Sì, impostando `PngColorType.TruecolorWithAlpha`

## Cos’è “convertire PSD in PNG”?
Convertire un documento Photoshop (PSD) in un'immagine PNG significa estrarre il contenuto visivo — inclusi tutti i livelli, le maschere e la trasparenza — in un formato raster ampiamente supportato. PNG conserva i canali alfa, rendendolo ideale per grafiche web, miniature e ulteriori elaborazioni di immagine.

## Perché usare Aspose.PSD per Java per convertire PSD in PNG e ruotare i livelli PSD?
- **Nessun Photoshop richiesto** – funziona su qualsiasi server o ambiente CI  
- **Supporto completo dei livelli** – mantiene trasparenza ed effetti dei livelli intatti  
- **API semplice** – ruota, capovolgi e salva con poche chiamate di metodo  
- **Cross‑platform** – gira su Windows, Linux e macOS  

## Prerequisiti
Prima di immergerci nel codice, assicurati di avere quanto segue:

- **Java Development Kit (JDK)** – scaricalo dal [sito Oracle](https://www.oracle.com/java/technologies/javase-downloads.html).  
- **Integrated Development Environment (IDE)** – IntelliJ IDEA, Eclipse o NetBeans vanno tutti bene.  
- **Libreria Aspose.PSD per Java** – ottieni l'ultimo JAR dalla [pagina di rilascio](https://releases.aspose.com/psd/java/).  
- **Conoscenze di base di Java** – familiarità con classi, oggetti e gestione delle eccezioni.

## Guida passo‑passo

### Passo 1: Configura il tuo progetto Java
Crea un nuovo progetto Java nel tuo IDE e aggiungi il JAR di Aspose.PSD al percorso di compilazione del progetto.

### Passo 2: Importa le classi necessarie
Aggiungi i seguenti import all'inizio del tuo file sorgente Java:

```java
import com.aspose.psd.Image;
import com.aspose.psd.RotateFlipType;
import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.PngOptions;
```

Queste classi ti danno accesso al caricamento dell'immagine, alla rotazione e alle opzioni specifiche per PNG.

### Passo 3: Definisci i percorsi dei file
Specifica dove si trova il tuo PSD di origine e dove devono essere scritti i file di output.

```java
String dataDir = "Your Document Directory"; // Change this to your actual document directory.
String sourceFile = dataDir + "1.psd"; // Source PSD file
String pngPath = dataDir + "RotateFlipTest2617.png"; // Output PNG file path
String psdPath = dataDir + "RotateFlipTest2617.psd"; // Output PSD file path
```

> **Suggerimento professionale:** Usa un percorso assoluto durante i test per evitare errori “file non trovato”.

### Passo 4: Carica il file PSD
Carica il PSD in un oggetto manipolabile.

```java
PsdImage im = (PsdImage) Image.load(sourceFile);
```

Ora `im` rappresenta l'intero documento Photoshop, inclusi tutti i livelli.

### Passo 5: Ruota l'immagine (Come ruotare un PSD)
Scegli un tipo di rotazione da `RotateFlipType`. In questo esempio ruotiamo di 270° e capovolgiamo entrambi gli assi.

```java
int flipType = RotateFlipType.Rotate270FlipXY; // Choose the rotation type
im.rotateFlip(flipType); // Rotate the image
```

Sentiti libero di sperimentare con altri valori come `Rotate90FlipNone` o `Rotate180FlipX`.

### Passo 6: Salva l'immagine ruotata come PNG (convertire PSD in PNG)
Configura le opzioni PNG per mantenere la trasparenza, quindi salva.

```java
PngOptions options = new PngOptions();
options.setColorType(PngColorType.TruecolorWithAlpha); // Preserve transparency
im.save(pngPath, options); // Save the rotated image
```

Il PNG risultante conserva la trasparenza dei livelli, pronto per l'uso sul web.

### Passo 7: Salva il PSD modificato (opzionale)
Se ti serve anche un nuovo PSD con la rotazione applicata, salvalo nuovamente.

```java
im.save(psdPath);
```

Ora hai sia un'anteprima PNG sia un file PSD aggiornato.

## Problemi comuni e soluzioni
- **File non trovato:** Verifica che `dataDir` termini con un separatore di percorso (`/` o `\`).  
- **OutOfMemoryError su PSD di grandi dimensioni:** Aumenta la dimensione dell'heap JVM (`-Xmx2g`).  
- **Trasparenza persa:** Assicurati che `PngColorType.TruecolorWithAlpha` sia impostato; altrimenti il PNG verrà salvato senza alfa.

## FAQ
### Posso ruotare un livello specifico in un file PSD?
Sì, puoi usare `Layer.rotateFlip()` sui singoli livelli dopo aver iterato su `im.getLayers()`.

### Esistono limitazioni di prestazioni con Aspose.PSD per Java?
La libreria gestisce la maggior parte dei file in modo efficiente, ma PSD estremamente grandi (>500 MB) potrebbero richiedere memoria aggiuntiva.

### Aspose.PSD è gratuito?
Aspose offre una prova gratuita, ma per la produzione è necessaria una licenza a pagamento. Consulta la [licenza temporanea](https://purchase.aspose.com/temporary-license/) per i test.

### Dove posso trovare la documentazione dettagliata?
Puoi trovare la documentazione completa su [Aspose.PSD Documentation](https://reference.aspose.com/psd/java/).

### Cosa fare se incontro problemi usando Aspose.PSD?
Chiedi aiuto sul [Forum di Supporto Aspose](https://forum.aspose.com/c/psd/34).

## Altre domande frequenti

**D: La conversione da PSD a PNG preserva gli effetti di livello?**  
R: Sì, quando salvi con `PngColorType.TruecolorWithAlpha`, la maggior parte degli effetti visivi viene rasterizzata nel PNG.

**D: Posso elaborare più file PSD in batch?**  
R: Assolutamente. Avvolgi il codice in un ciclo che itera su una cartella di file PSD.

**D: È possibile impostare il livello di compressione PNG?**  
R: La classe `PngOptions` fornisce il metodo `setCompressionLevel(int)` per una regolazione fine.

**D: Devo chiudere l'oggetto immagine?**  
R: `PsdImage` implementa `Closeable`; chiama `im.close()` in un blocco `finally` o usa il try‑with‑resources.

**D: Il PNG ruotato avrà le stesse dimensioni dell'originale?**  
R: Ruotare di 90° o 270° scambia larghezza e altezza. Il PNG rifletterà la nuova orientazione.

## Conclusione
Sfruttando Aspose.PSD per Java, puoi **convertire PSD in PNG** e **ruotare i livelli PSD** con poche righe di codice. Questo approccio elimina la necessità di Photoshop, accelera i flussi di lavoro automatizzati e ti dà il pieno controllo sull'output dell'immagine. Provalo nei tuoi progetti e scopri quanto tempo puoi risparmiare!

---

**Ultimo aggiornamento:** 2025-12-15  
**Testato con:** Aspose.PSD per Java 24.11  
**Autore:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}