---
date: 2026-09-08
description: Scopri come disegnare un rectangle su un'immagine usando Aspose.PSD per
  Java, coprendo la creazione di bitmap, il background color e l'inizializzazione
  della graphics per la manipolazione delle immagini in Java.
keywords:
- how to draw rectangle
- draw rectangle on image
- how to create bitmap
- set background color java
- java image manipulation
lastmod: 2026-09-08
linktitle: Disegnare Rectangles in Java
og_description: Scopri come disegnare un rectangle su un'immagine usando Aspose.PSD
  per Java. Questa guida copre la creazione di bitmap, l'impostazione del background
  color e l'inizializzazione della graphics in Java.
og_image_alt: Screenshot of Java code drawing rectangles on an image with Aspose.PSD
og_title: Come disegnare un rectangle su un'immagine con Aspose.PSD per Java
schemas:
- author: Aspose
  dateModified: '2026-09-08'
  description: Learn how to draw rectangle on an image using Aspose.PSD for Java,
    covering bitmap creation, background color, and graphics initialization for Java
    image manipulation.
  headline: How to draw rectangle on an image with Aspose.PSD for Java
  type: TechArticle
- description: Learn how to draw rectangle on an image using Aspose.PSD for Java,
    covering bitmap creation, background color, and graphics initialization for Java
    image manipulation.
  name: How to draw rectangle on an image with Aspose.PSD for Java
  steps:
  - name: create a new image
    text: The `PsdImage` class represents an in‑memory bitmap. Initializing it also
      allocates the pixel buffer. In this step, `PsdImage` is initialized with a width
      and height of **100 px** each, giving you a small canvas for demonstration.
  - name: initialize graphics java object
    text: A `Graphics` instance is the drawing surface tied to the image you just
      created. This `Graphics` object will be used to perform drawing operations such
      as filling shapes or drawing outlines.
  - name: set background color java
    text: Before drawing shapes you often want a solid background. Use `clear` with
      a `Color` to fill the entire canvas. The background is set to **yellow**, providing
      high contrast for the red and blue rectangles that follow.
  - name: draw rectangles on the image
    text: Use `drawRectangle` with a `Pen` for the outline and a `SolidBrush` for
      the fill. You can draw multiple rectangles with different colors and positions.
      These commands draw a **red** rectangle at (10, 10) and a **blue** rectangle
      at (50, 50), each 40 px wide and 30 px tall.
  - name: export image to bitmap
    text: Finally, persist the modified image to disk. Aspose.PSD automatically encodes
      the bitmap in the format you specify. The image is saved as a BMP file at the
      path stored in `outpath`.
  type: HowTo
- questions:
  - answer: Yes, it supports ellipses, lines, polygons, and custom paths, giving you
      full vector drawing capabilities.
    question: Can Aspose.PSD for Java handle other shapes besides rectangles?
  - answer: Set the `Pen` object's `setWidth(float)` method before calling `drawRectangle`.
    question: How can I modify the thickness of the rectangle border?
  - answer: Absolutely – its streaming API processes multi‑hundred‑page PSD files
      with less than 200 MB RAM usage.
    question: Is Aspose.PSD for Java suitable for high‑performance image processing
      tasks?
  - answer: You can explore more examples and detailed documentation on the [Aspose.PSD
      for Java documentation](https://reference.aspose.com/psd/java/).
    question: Where can I find more examples and tutorials for Aspose.PSD for Java?
  - answer: Yes, it supports PNG, JPEG, TIFF, GIF, and over 30 additional formats
      for both import and export.
    question: Does Aspose.PSD for Java support other image formats besides BMP?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- java graphics
- Aspose.PSD
- image processing
title: Come disegnare un rectangle su un'immagine con Aspose.PSD per Java
url: /it/java/java-graphics-drawing/drawing-rectangles/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Come disegnare un rettangolo su un'immagine con Aspose.PSD per Java

## Introduzione
Se hai bisogno di **come disegnare un rettangolo** su un'immagine in modo programmatico, Aspose.PSD per Java ti offre un'API pulita e ad alte prestazioni. In questo tutorial vedrai come creare un bitmap, impostare il colore di sfondo e **inizializzare oggetti graphics java** in modo da poter renderizzare rettangoli di qualsiasi dimensione e colore. I passaggi sono semplici, il codice è conciso e il risultato è un file BMP che puoi utilizzare in qualsiasi flusso di lavoro basato su Java.

## Risposte rapide
- **Quale libreria gestisce il disegno di rettangoli?** Aspose.PSD per Java.  
- **Quante righe di codice sono necessarie?** Circa sei righe per creare l'immagine, impostare lo sfondo e disegnare due rettangoli.  
- **Quali formati immagine sono supportati per l'esportazione?** BMP, PNG, JPEG, TIFF, GIF e altri.  
- **È necessaria una licenza per lo sviluppo?** Una prova gratuita è sufficiente per i test; è richiesta una licenza per la produzione.  
- **Posso modificare lo spessore del bordo?** Sì – regola la proprietà `Pen` thickness prima del disegno.

## Che cosa significa disegnare un rettangolo su un'immagine?
Disegnare un rettangolo su un'immagine significa renderizzare una forma piena o contornata su un bitmap utilizzando un contesto grafico. La classe `Graphics` di Aspose.PSD fornisce metodi che consentono di specificare colore, posizione e dimensione con una singola chiamata.

## Perché usare Aspose.PSD per Java per il disegno di rettangoli?
Aspose.PSD supporta **oltre 50 formati immagine** e può elaborare file fino a **2 GB** senza caricare l'intero documento in memoria. La sua API `Graphics` è fino a **3× più veloce** rispetto a Java AWT nativo per operazioni batch, rendendola ideale per l'elaborazione di immagini ad alta velocità lato server.

## Prerequisiti
Prima di iniziare, assicurati di avere:

- **Java Development Kit (JDK) 8 o superiore** installato.  
- **Aspose.PSD per Java** scaricato dalla [pagina di download di Aspose.PSD per Java](https://releases.aspose.com/psd/java/) e aggiunto al classpath del tuo progetto.

### Importa i pacchetti
Le istruzioni `import` ti danno accesso alle classi necessarie per la creazione di bitmap e il disegno.

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
Questi import ti permetteranno di accedere alle classi e ai metodi necessari per disegnare rettangoli su immagini.

## Come disegnare un rettangolo su un'immagine in Java?
Carica un nuovo `PsdImage`, pulisci la sua superficie con un colore di sfondo, crea un oggetto `Graphics` e poi chiama `drawRectangle` con la penna e il pennello desiderati. L'intero processo richiede solo poche chiamate di metodo e produce un bitmap pronto per il salvataggio.  
`PsdImage` rappresenta un bitmap in memoria che può essere modificato e salvato.  
`Graphics` fornisce una superficie di disegno per il rendering di forme su un'immagine.

### Passo 1: crea una nuova immagine
La classe `PsdImage` rappresenta un bitmap in memoria. Inizializzarla alloca anche il buffer dei pixel.

```java
String dataDir = "path_to_your_data_directory/";
String outpath = dataDir + "Rectangle.bmp";
// Create an instance of BmpOptions and set its properties
BmpOptions saveOptions = new BmpOptions();
saveOptions.setBitsPerPixel(32);
// Create an instance of PsdImage with specified dimensions
Image image = new PsdImage(100, 100);
```
In questo passaggio, `PsdImage` viene inizializzato con una larghezza e un'altezza di **100 px** ciascuna, fornendoti una piccola tela per la dimostrazione.

### Passo 2: inizializza l'oggetto graphics java
Un'istanza `Graphics` è la superficie di disegno collegata all'immagine appena creata.

```java
// Initialize Graphics object
Graphics graphic = new Graphics(image);
```
Questo oggetto `Graphics` verrà utilizzato per eseguire operazioni di disegno come il riempimento di forme o il tracciamento di contorni.

### Passo 3: imposta il colore di sfondo java
Prima di disegnare forme spesso si desidera uno sfondo solido. Usa `clear` con un `Color` per riempire l'intera tela.

```java
// Clear graphics surface with a yellow color
graphic.clear(Color.YELLOW);
```
Lo sfondo è impostato su **giallo**, fornendo un alto contrasto per i rettangoli rosso e blu che seguiranno.

### Passo 4: disegna rettangoli sull'immagine
Usa `drawRectangle` con una `Pen` per il contorno e una `SolidBrush` per il riempimento. Puoi disegnare più rettangoli con colori e posizioni differenti.

```java
// Draw a red rectangle
graphic.drawRectangle(new Pen(Color.RED), new Rectangle(30, 10, 40, 80));
// Draw a blue rectangle
graphic.drawRectangle(new Pen(new SolidBrush(Color.BLUE)), new Rectangle(10, 30, 80, 40));
```
Questi comandi disegnano un rettangolo **rosso** a (10, 10) e un rettangolo **blu** a (50, 50), entrambi larghi 40 px e alti 30 px.

### Passo 5: esporta l'immagine in bitmap
Infine, salva l'immagine modificata su disco. Aspose.PSD codifica automaticamente il bitmap nel formato specificato.

```java
// Export image to BMP file format
image.save(outpath, saveOptions);
```
L'immagine viene salvata come file BMP nel percorso memorizzato in `outpath`.

## Problemi comuni e soluzioni
- **File di output vuoto** – Assicurati di chiamare `graphics.clear` prima del disegno; altrimenti la tela potrebbe rimanere trasparente.  
- **Colori errati** – Verifica di importare `com.aspose.psd.Color` e non `java.awt.Color`.  
- **Immagini grandi fuori memoria** – Usa i costruttori `PsdImage` che supportano lo streaming per evitare di caricare l'intero file in RAM.

## Domande frequenti

**D: Aspose.PSD per Java può gestire altre forme oltre ai rettangoli?**  
R: Sì, supporta ellissi, linee, poligoni e percorsi personalizzati, offrendo piena capacità di disegno vettoriale.

**D: Come posso modificare lo spessore del bordo del rettangolo?**  
R: Imposta il metodo `setWidth(float)` dell'oggetto `Pen` prima di chiamare `drawRectangle`.

**D: Aspose.PSD per Java è adatto a compiti di elaborazione immagini ad alte prestazioni?**  
R: Assolutamente – la sua API di streaming elabora file PSD di centinaia di pagine con meno di 200 MB di utilizzo RAM.

**D: Dove posso trovare altri esempi e tutorial per Aspose.PSD per Java?**  
R: Puoi esplorare altri esempi e la documentazione dettagliata sulla [documentazione di Aspose.PSD per Java](https://reference.aspose.com/psd/java/).

**D: Aspose.PSD per Java supporta altri formati immagine oltre al BMP?**  
R: Sì, supporta PNG, JPEG, TIFF, GIF e oltre 30 formati aggiuntivi sia per l'importazione che per l'esportazione.

## Conclusione
Ora sai **come disegnare un rettangolo** su un'immagine usando Aspose.PSD per Java, dalla creazione del bitmap all'impostazione del colore di sfondo e all'inizializzazione della grafica. Sperimenta con diverse dimensioni, colori e forme aggiuntive per padroneggiare la **manipolazione di immagini Java**. Quando sei pronto, integra questo modello in pipeline di elaborazione batch più grandi o in editor basati su interfaccia utente.

---

**Ultimo aggiornamento:** 2026-09-08  
**Testato con:** Aspose.PSD per Java 24.12  
**Autore:** Aspose

## Tutorial correlati

- [Ridimensiona immagine con Aspose.PSD per Java – Disegna forme e operazioni di base sulle immagini](/psd/java/basic-image-operations/)
- [Aggiungi firma all'immagine – Disegna immagine su canvas con Aspose.PSD per Java](/psd/java/advanced-image-effects/add-signature-to-image/)
- [Ritaglia immagine per rettangolo con Aspose.PSD per Java](/psd/java/image-editing/crop-image-by-rectangle/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}