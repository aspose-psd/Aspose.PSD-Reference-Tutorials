---
date: 2026-02-20
description: Scopri come convertire PSD in PNG impostando la modalità colore del PSD
  a scala di grigi a 16 bit usando Aspose.PSD per Java. Guida passo‑passo con esempi
  di codice.
linktitle: Convert PSD to PNG – 16-bit Grayscale – Java
second_title: Aspose.PSD Java API
title: Come convertire PSD in PNG con modalità colore in scala di grigi a 16 bit in
  Java
url: /it/java/advanced-psd-layer-features-effects/support-16-bit-grayscale-color-mode-psd/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Converti PSD in PNG con modalità colore in scala di grigi a 16 bit in Java

## Introduzione
Quando ti immergi nel mondo del design grafico e della manipolazione delle immagini, sapere **come convertire PSD in PNG** è come avere un'arma segreta. L'uso di una modalità scala di grigi a 16 bit aggiunge una profondità incredibile e una ricchezza tonale, facendo risaltare le tue immagini. In questo tutorial ti guideremo su come **impostare la modalità colore del PSD** a scala di grigi a 16 bit e poi **esportare il PSD come PNG** usando Aspose.PSD per Java. Pronto a migliorare il tuo flusso di lavoro con le immagini? Iniziamo.

## Risposte rapide
- **Cosa comporta “convertire PSD in PNG”?** Caricare un PSD, opzionalmente cambiarne la modalità colore e salvarlo come file PNG.  
- **Quale classe Aspose gestisce la conversione?** `PsdImage` per il caricamento e `PngOptions` per il salvataggio.  
- **Ho bisogno di una licenza speciale?** Una versione di prova funziona per i test; è necessaria una licenza a pagamento per la produzione.  
- **Posso mantenere la profondità a 16 bit nel PNG?** Sì, usando `PngColorType.GrayscaleWithAlpha`.  
- **Quali IDE sono supportati?** Qualsiasi IDE Java – IntelliJ IDEA, Eclipse, VS Code, ecc.

## Perché convertire PSD in PNG con scala di grigi a 16 bit?
* **Preservare i dettagli tonali:** la scala di grigi a 16 bit memorizza 65 536 tonalità di grigio, molto più delle 256 tonalità di un'immagine a 8 bit.  
* **Ampia compatibilità:** PNG è ampiamente supportato su browser, app mobili e strumenti desktop, mantenendo comunque i dati ad alta qualità.  
* **Flusso di lavoro senza perdita:** la conversione con Aspose.PSD garantisce l'assenza di artefatti di compressione indesiderati, ideale per l'archiviazione o ulteriori elaborazioni.

## Prerequisiti
Prima di iniziare, assicuriamoci di avere tutto pronto per ottenere il massimo da questo tutorial. Ecco cosa ti servirà:

1. **Java Development Kit (JDK)** – Assicurati di avere installata l'ultima versione. Puoi scaricarla dal [sito di Oracle](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).  
2. **Libreria Aspose.PSD per Java** – Questo è il motore che ci permetterà di manipolare i file PSD. Scaricala dalla [pagina di download di Aspose](https://releases.aspose.com/psd/java/).  
3. **Un IDE** – IntelliJ IDEA, Eclipse o Visual Studio Code andranno benissimo.  
4. **Conoscenza di base di Java** – Familiarità con la sintassi Java renderà i passaggi più fluidi.  
5. **Un file PSD di esempio** – Creane uno in Adobe Photoshop o scarica un esempio gratuito online.

Pronto? Ottimo! Importiamo i pacchetti necessari e iniziamo a codificare.

## Importa pacchetti
Per iniziare, aggiungi gli import di Aspose.PSD richiesti al tuo file Java:

```java
import com.aspose.psd.*;
import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.fileformats.psd.ColorModes;
import com.aspose.psd.fileformats.psd.CompressionMethod;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.PngOptions;
import com.aspose.psd.imageoptions.PsdOptions;
import com.aspose.psd.system.Enum;
```

Questi import ti danno accesso alle funzionalità che utilizzerai per manipolare i file PSD, impostare la modalità colore e esportare il risultato come PNG.

## Passo 1: Definisci le tue directory
Prima, configura le cartelle di origine e di destinazione. Questo indica al programma dove leggere il PSD originale e dove scrivere i file convertiti.

```java
String sourceDir = "Your Source Directory"; // Change to your source directory
String outputDir = "Your Document Directory"; // Change to your output directory
```

Sostituisci le stringhe segnaposto con i percorsi reali sul tuo computer.

## Passo 2: Crea un metodo per gestire l'elaborazione dell'immagine
Incapsuleremo la logica di conversione all'interno di un metodo riutilizzabile. Riceve tutti i parametri che potresti voler modificare, come modalità colore, profondità di bit e compressione.

```java
class LocalScopeExtension {
    void saveToPsdThenLoadAndSaveToPng(
        String file,
        short colorMode,
        short channelBitsCount,
        short channelsCount,
        short compression,
        int layerNumber) {
```

Questo metodo ti consente di **impostare la modalità colore del PSD** e poi **esportare il PSD come PNG** in un unico flusso.

## Passo 3: Definisci i percorsi dei file e carica il PSD
All'interno del metodo, costruisci i percorsi completi dei file e carica il PSD originale a scala di grigi a 16 bit:

```java
String filePath = sourceDir + file + ".psd";
String postfix = Enum.getName(ColorModes.class, colorMode) + channelBitsCount + "_" +
                 channelsCount + "_" + Enum.getName(CompressionMethod.class, compression);
String exportPath = outputDir + file + postfix + ".psd";
String pngExportPath = outputDir + file + postfix + ".png";
// Load a predefined 16-bit grayscale PSD
PsdImage image = (PsdImage)Image.load(filePath);
```

Il `postfix` ti aiuta a tenere traccia delle impostazioni usate per ogni file esportato.

## Passo 4: Elabora il livello o l'immagine completa
Ora disegniamo su un livello specifico o sull'intera immagine. In questo esempio aggiungiamo un sottile bordo grigio per rendere il risultato più visibile.

```java
try {
    RasterCachedImage raster = layerNumber >= 0 ? image.getLayers()[layerNumber] : image;
    // Draw a gray inner border around the perimeter of the layer
    Graphics graphics = new Graphics(raster);
    int width = raster.getWidth();
    int height = raster.getHeight();
    Rectangle rect = new Rectangle(
        width / 3,
        height / 3,
        width - (2 * (width / 3)) - 1,
        height - (2 * (height / 3)) - 1);
    graphics.drawRectangle(new Pen(Color.getDarkGray(), 1), rect);
```

Il rettangolo è calcolato dinamicamente in modo da rimanere centrato indipendentemente dalla dimensione dell'immagine.

## Passo 5: Salva il file PSD modificato
Dopo il disegno, salviamo il PSD con la modalità colore e la profondità di bit esatte che hai specificato. Questo è il fulcro di **impostare la modalità colore del PSD** prima della conversione.

```java
    // Save a copy of PSD with specific characteristics
    PsdOptions psdOptions = new PsdOptions();
    psdOptions.setColorMode(colorMode);
    psdOptions.setChannelBitsCount(channelBitsCount);
    psdOptions.setChannelsCount(channelsCount);
    psdOptions.setCompressionMethod(compression);
    image.save(exportPath, psdOptions);
}
```

## Passo 6: Converti il PSD in PNG
Infine, carichiamo il PSD appena salvato ed esportiamo come PNG. Usando `PngColorType.GrayscaleWithAlpha` preserviamo la profondità a 16 bit nel file PNG.

```java
finally {
    image.dispose();
}
// Load the saved PSD
PsdImage image1 = (PsdImage)Image.load(exportPath);
try {
    // Convert the saved PSD to a grayscale PNG image
    PngOptions pngOptions = new PngOptions();
    pngOptions.setColorType(PngColorType.GrayscaleWithAlpha);
    image1.save(pngExportPath, pngOptions); // here should be no exception
}
finally {
    image1.dispose();
}
```

Ora hai **convertito con successo PSD in PNG** mantenendo i dati in scala di grigi a 16 bit di alta qualità.

## Problemi comuni e soluzioni
| Problema | Perché accade | Soluzione |
|----------|----------------|-----------|
| **“Eccezione ‘Unsupported color type’”** | Tentativo di salvare un PSD con una configurazione di canale non supportata. | Assicurati che `channelBitsCount` corrisponda alla reale profondità di bit (16) e che `channelsCount` sia corretto per la scala di grigi (1). |
| **File non trovato** | Percorso della directory di origine errato. | Verifica nuovamente la stringa `sourceDir` e assicurati che il file PSD esista. |
| **Il PNG di output appare nero** | PNG salvato senza gestione del canale alfa. | Usa `PngColorType.GrayscaleWithAlpha` come mostrato sopra. |

## Domande frequenti

**Q: Cos'è la modalità colore in scala di grigi a 16 bit?**  
A: Fornisce 65 536 tonalità di grigio, offrendo molto più dettaglio tonale rispetto allo standard a 8 bit (256 tonalità).

**Q: Posso usare Aspose.PSD per immagini non in scala di grigi?**  
A: Assolutamente! Aspose.PSD supporta RGB, CMYK, Lab e molte altre modalità colore.

**Q: Esiste una versione di prova di Aspose.PSD?**  
A: Sì, puoi provare una versione di prova gratuita di Aspose.PSD. Vai alla [pagina di download di Aspose](https://releases.aspose.com/).

**Q: Dove posso trovare più esempi sull'uso di Aspose.PSD?**  
A: Puoi consultare la [documentazione](https://reference.aspose.com/psd/java/) per esempi più approfonditi e tutorial.

**Q: Come posso acquistare una licenza per Aspose.PSD?**  
A: Puoi acquistare una licenza visitando la [pagina di acquisto di Aspose](https://purchase.aspose.com/buy).

---

**Ultimo aggiornamento:** 2026-02-20  
**Testato con:** Aspose.PSD for Java 24.12 (ultima versione al momento della scrittura)  
**Autore:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}