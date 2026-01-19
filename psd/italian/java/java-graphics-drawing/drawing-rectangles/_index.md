---
date: 2026-01-19
description: Scopri come creare immagini Java e disegnare rettangoli sulle immagini
  usando Aspose.PSD per Java. Questo tutorial passo‑passo di manipolazione di immagini
  Java ti aiuta a disegnare forme su immagini Java in modo efficiente.
linktitle: Create Image Java – Drawing Rectangles with Aspose.PSD
second_title: Aspose.PSD Java API
title: Creare immagine Java – Disegnare rettangoli con Aspose.PSD
url: /it/java/java-graphics-drawing/drawing-rectangles/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Creare Immagine Java – Disegnare Rettangoli

## Introduzione
Se hai bisogno di **creare immagine è un requisito di routineazioni senza dover manipolare i pixel a basso livello. In questo tutorial percorreremo un esempio completo, pratico, che mostra come disegnare rettangoli su un'immagine appena creata, passo dopo passo.

## Risposte Rapide
- **Cosa significa “creare immagine java”?** Indica la generazione di un'immagine raster (ad es. BMP, PNG) dal codice Java usando una libreria di imaging.  
- **Quale libreria è la migliore per disegnare forme?** Aspose.PSD per Java fornisce primitive di disegno robuste come `Graphics`, `Pen` e `SolidBrush`.  
- **Quante righe di codice servono?** Circa 30 righe, includendo import, configurazione immagine, disegno e salvataggio.  
- **Posso cambiare il formato di output?** Sì—sostituisci `BmpOptions` con `PngOptions`, `JpegOptions`, ecc.  
- **È necessaria una licenza per la produzione?** È richiesta una licenza commerciale per l'uso non‑valutativo.

## Cos'è **creare immagine java**?
Creare un'immagine in Java significa istanziare un oggetto bitmap (o PSD) in memoria, disegnare sul suo canvas con primitive grafiche e poi persisterlo in un formato file a scelta. L'API Aspose.PSD astrae i dettagli a basso livello, permettendoti di concentrarti sulla logica visiva.

## Perché usare Aspose.PSD per Java per **disegnare forme su immagine java**?
- **API di disegno completa:** Supporta rettangoli, ellissi, linee, poligoni e percorsi personalizzati.  
- **Supporto multi‑formato:** Scrivi BMP, PNG, JPEG, TIFF, GIF e PSD senza convertitori aggiuntivi.  
- ** diretta.

## Pr iniziare, assicurati di avere:

- **Java Developmentumento di build.  
- **Libreria Aspose.PSD per Java.** Scaricala dalla [pagina di download di Aspose.PSD per Java](https://releases.aspose.com/psd/java/) e aggiungi il JAR al classpath del tuo progetto.  

## Importare i Pacchetti
Per lavorare con la grafica, importa le seguenti classi Aspose.PSD:

```java
import com.aspose.psd.Color;
import com.aspose.psd.Graphics;
import com.aspose.psd.Image;
import com.aspose.psd.Pen;
import com.aspose.psd.Rectangle;
import com.aspose.psd.brushes.SolidBrush;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.BmpOptions;
```

 opzioni istanzia un `PsdImage` con le dimensioni desiderate (100 × 100 px in questo esempio).

```java
String dataDir = "path_to_your_data_directory/";
String outpath = dataDir + "Rectangle.bmp";
// Create an instance of BmpOptions and set its properties
BmpOptions saveOptions = new BmpOptions();
saveOptions.setBitsPerPixel(32);
// Create an instance of PsdImage with specified dimensions
Image image = new PsdImage(100, 100);
```

> **Suggerimento necessaria per il tuo caso d'uso specifico: Inizializzare l'Oggetto Graphics
Crea un oggetto `Graphics` dall'immagine. Questo oggetto è il canvas su cui disegnerai.

```java
// Initialize Graphics object
Graphics graphic = new Graphics(image);
```

## Passo 3: Cancellare la Superficie Grafica
Assegna all'immagine un colore di sfondo. Qui la cancelliamo con il giallo, ma qualsiasi `Color` va bene.

```java
// Clear graphics surface with a yellow color
graphic.clear(Color.YELLOW);
```

## Passo 4: Disegnare Rettangoli
Ora disegna due rettangoli—uno rosso, uno blu—usando `Pen` e `SolidBrush`. Questo dimostra la capacità di **draw rectangle java**.

```java
// Draw a red rectangle
graphic.drawRectangle(new Pen(Color.RED), new Rectangle(30, 10, 40, 80));
// Draw a blue rectangle
graphic.drawRectangle(new Pen(new SolidBrush(Color.BLUE)), new Rectangle(10, 30, 80, 40));
```

Puoi sperimentare con larghezze diverse del `Pen`, stili di tratteggio, o persino riempire il rettangolo con un `SolidBrush`.

## Passo 5: Esmagine
Infine, salva l'immagine modificata su disco. Le `32 bit.

```java
// Export image to BMP file format
image.save(outpath, saveOptions);
```

Dopo aver eseguito il codice, troverai `Rectangle.bmp` nella tua directory dati, mostrando un canvas giallo con un rettangolo rosso e uno blu.

## Problemi Comuni e Suggerimenti
| Problema | Causa | Soluzione |
|----------|-------|-----------|
| **L'immagine appare cancellare o ri di disegnare le forme. |
| **La dimensione del rettangolo è errata** | Parametri `Rectangle` errati (x, y, larghezza, altezza) | Ricontrolla l'ordine degli argomenti; il terzo e quarto valore sono larghezza e altezza, non x2/y2. |
| **File non salvato** | Percorso di output non valido o permessi di scrittura mancanti | Verifica che `outpath` punti a una cartella esistente e che l'applicazione abbia i permessi di scrittura. |
| **I colori appaiono sbiaditi** | Uso di un'opzione a bassa profondità di bit | Usa `BmpOptions.setBitsPerPixel(32)` o passa a PNG per colori lossless. |

## FAQ
### Aspose.PSD per Java può gestire altre forme oltre ai rettangoli?
Aspose.PSD per Java supporta il disegno di varie forme come ellissi, linee e poligoni oltre ai rettangoli.

### Come posso modificare lo spessore del bordo del rettangolo?
Pu Aspose.PSD per Javaaborplesse.

### Dove posso trovare altri esempi e tutorial per Aspose.PSD per Java?
Puoi esplorare altri esempi e la documentazione dettagliata su [Aspose.PSD per Java documentation](https://reference.aspose.com/psd/java/).

### Aspose.PSD per Java supporta altri formati immagine oltre al BMP?
Sì, Aspose.PSD per Java supporta una vasta gamma di formati immagine includendo PNG, JPEG, TIFF e GIF.

## Conclusioneagine, cancellarlo, disegnare rett usando  
**Testato con:** Aspose.PSD per Java 24.12 (ultima versione al momento della scrittura)  
**Autore:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}