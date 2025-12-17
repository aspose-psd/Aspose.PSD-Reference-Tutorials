---
date: 2025-12-17
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

# Converti PSD in PNG con modalità colore Grayscale a 16‑bit in Java

## Introduction
Quando ti immergi nel mondo del design grafico e della manipolazione delle immagini, capire come **convertire PSD in PNG** è come avere un'arma segreta. In particolare, usare una modalità grayscale a 16 bit conferisce alle tue immagini una profondità e un dettaglio sorprendenti che le fanno davvero risaltare. In questo tutorial ti guideremo passo passo su come **impostare la modalità colore del PSD** a grayscale a 16 bit e poi **esportare il PSD come PNG** usando Aspose.PSD per Java. Pronto a migliorare il tuo flusso di lavoro con le immagini? Iniziamo.

## Quick Answers
- **Cosa comporta “convertire PSD in PNG”?** Caricare un PSD, eventualmente cambiarne la modalità colore e salvarlo come file PNG.  
- **Quale classe Aspose gestisce la conversione?** `PsdImage` per il caricamento e `PngOptions` per il salvataggio.  
- **È necessaria una licenza speciale?** Una versione di prova funziona per i test; è richiesta una licenza a pagamento per la produzione.  
- **Posso mantenere la profondità a 16 bit nel PNG?** Sì, usando `PngColorType.GrayscaleWithAlpha`.  
- **Quali IDE sono supportati?** Qualsiasi IDE Java – IntelliJ IDEA, Eclipse, VS Code, ecc.

## Prerequisites
Prima di iniziare, assicuriamoci di avere tutto il necessario per ottenere il massimo da questo tutorial. Ecco cosa ti serve:

1. **Java Development Kit (JDK)** – Assicurati di avere installata l'ultima versione. Puoi scaricarla dal [sito di Oracle](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).  
2. **Libreria Aspose.PSD per Java** – È il motore che ci permette di manipolare i file PSD. Scaricala dalla [pagina di download di Aspose](https://releases.aspose.com/psd/java/).  
3. **Un IDE** – IntelliJ IDEA, Eclipse o Visual Studio Code vanno benissimo.  
4. **Conoscenze di base di Java** – Familiarità con la sintassi Java renderà i passaggi più fluidi.  
5. **Un file PSD di esempio** – Creane uno in Adobe Photoshop o scarica un campione gratuito online.

Pronto? Ottimo! Importiamo i pacchetti necessari e iniziamo a programmare.

## Import Packages
Per iniziare, aggiungi le importazioni Aspose.PSD richieste al tuo file Java:

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

Queste importazioni ti danno accesso alle funzionalità che userai per manipolare i file PSD, impostare la modalità colore e esportare il risultato come PNG.

## Step 1: Define Your Directories
Per prima cosa, imposta le cartelle di origine e di destinazione. Questo indica al programma dove leggere il PSD originale e dove scrivere i file convertiti.

```java
String sourceDir = "Your Source Directory"; // Change to your source directory
String outputDir = "Your Document Directory"; // Change to your output directory
```

Sostituisci le stringhe segnaposto con i percorsi effettivi sulla tua macchina.

## Step 2: Create a Method to Handle Image Processing
Incapsuleremo la logica di conversione all'interno di un metodo riutilizzabile. Riceve tutti i parametri che potresti voler modificare, come la modalità colore, la profondità di bit e la compressione.

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

Questo metodo ti permette di **impostare la modalità colore del PSD** e poi **esportare il PSD come PNG** in un unico flusso.

## Step 3: Define File Paths and Load the PSD
All'interno del metodo, costruisci i percorsi completi dei file e carica il PSD originale in scala di grigi a 16 bit:

```java
String filePath = sourceDir + file + ".psd";
String postfix = Enum.getName(ColorModes.class, colorMode) + channelBitsCount + "_" +
                 channelsCount + "_" + Enum.getName(CompressionMethod.class, compression);
String exportPath = outputDir + file + postfix + ".psd";
String pngExportPath = outputDir + file + postfix + ".png";
// Load a predefined 16-bit grayscale PSD
PsdImage image = (PsdImage)Image.load(filePath);
```

Il `postfix` ti aiuta a tenere traccia delle impostazioni usate per ciascun file esportato.

## Step 4: Process the Layer or Full Image
Ora disegniamo su uno specifico livello o sull'intera immagine. In questo esempio aggiungiamo un sottile bordo grigio per rendere il risultato più visibile.

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

Il rettangolo è calcolato dinamicamente in modo da rimanere centrato indipendentemente dalle dimensioni dell'immagine.

## Step 5: Save the Modified PSD File
Dopo il disegno, salviamo il PSD con la modalità colore e la profondità di bit esattamente specificate. Questo è il fulcro dell'**impostazione della modalità colore del PSD** prima della conversione.

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

## Step 6: Convert the PSD to PNG
Infine, carichiamo il PSD appena salvato ed esportiamo come PNG. Utilizzando `PngColorType.GrayscaleWithAlpha` manteniamo la profondità a 16 bit nel file PNG.

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

Ora hai convertito con successo **PSD in PNG** mantenendo i dati grayscale a 16 bit di alta qualità.

## Common Issues and Solutions
| Problema | Perché accade | Soluzione |
|----------|----------------|-----------|
| **Eccezione “Unsupported color type”** | Tentativo di salvare un PSD con una configurazione di canale non supportata. | Assicurati che `channelBitsCount` corrisponda alla reale profondità di bit (16) e che `channelsCount` sia corretto per il grayscale (1). |
| **File non trovato** | Percorso della directory di origine errato. | Ricontrolla la stringa `sourceDir` e verifica che il file PSD esista. |
| **PNG di output appare nero** | PNG salvato senza gestione del canale alpha. | Usa `PngColorType.GrayscaleWithAlpha` come mostrato sopra. |

## Frequently Asked Questions

**Q: Cos'è la modalità colore grayscale a 16‑bit?**  
A: Fornisce 65 536 tonalità di grigio, offrendo molto più dettaglio tonale rispetto allo standard a 8 bit (256 tonalità).

**Q: Posso usare Aspose.PSD per immagini non‑grayscale?**  
A: Assolutamente! Aspose.PSD supporta RGB, CMYK, Lab e molte altre modalità colore.

**Q: Esiste una versione di prova di Aspose.PSD?**  
A: Sì, puoi provare una versione di prova gratuita di Aspose.PSD. Vai alla [pagina di download di Aspose](https://releases.aspose.com/).

**Q: Dove posso trovare altri esempi di utilizzo di Aspose.PSD?**  
A: Puoi consultare la [documentazione](https://reference.aspose.com/psd/java/) per esempi più approfonditi e tutorial.

**Q: Come acquisto una licenza per Aspose.PSD?**  
A: Puoi acquistare una licenza visitando la [pagina di acquisto di Aspose](https://purchase.aspose.com/buy).

---

**Ultimo aggiornamento:** 2025-12-17  
**Testato con:** Aspose.PSD per Java 24.12 (ultima versione al momento della stesura)  
**Autore:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}