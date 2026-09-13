---
date: 2026-09-13
description: Scopri come disegnare un'ellisse e altre forme in Java con Aspose.PSD.
  Questo tutorial passo‑passo di Java graphics mostra gradient fills, polygon fills
  e image export.
keywords:
- how to draw ellipse
- draw shapes java
- how to create gradient
- java graphics tutorial
- fill polygon java
lastmod: 2026-09-13
linktitle: Disegno usando Graphics in Java
og_description: Scopri come disegnare un'ellisse in Java usando Aspose.PSD. Questo
  tutorial Java graphics copre shape drawing, gradient fills, polygon filling e exporting
  images.
og_image_alt: Screenshot of Java code drawing an ellipse with Aspose.PSD
og_title: Come disegnare un'ellisse usando la grafica in Java con Aspose.PSD
schemas:
- author: Aspose
  dateModified: '2026-09-13'
  description: Learn how to draw an ellipse and other shapes in Java with Aspose.PSD.
    This step‑by‑step Java graphics tutorial shows gradient fills, polygon fills,
    and image export.
  headline: How to draw ellipse using graphics in Java with Aspose.PSD
  type: TechArticle
- questions:
  - answer: Yes, it supports layer merging, channel adjustments, text rendering, and
      advanced masking in addition to shape drawing.
    question: Can Aspose.PSD handle complex image manipulations?
  - answer: Absolutely; the library is optimized for speed and can process a 10 MP
      image in under 2 seconds on a typical server.
    question: Is Aspose.PSD suitable for high‑performance applications?
  - answer: Visit the [Aspose.PSD Java documentation](https://reference.aspose.com/psd/java/)
      for comprehensive guides and API references.
    question: Where can I find more examples and documentation?
  - answer: Yes, you can export to BMP, PNG, JPEG, TIFF, GIF, and PSD among others.
    question: Does Aspose.PSD support multiple image formats for export?
  - answer: Reach out to the Aspose.PSD community on the [support forum](https://forum.aspose.com/c/psd/34)
      or consider a [temporary license](https://purchase.aspose.com/temporary-license/)
      for priority assistance.
    question: How can I get support or assistance if I encounter issues?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- java graphics
- Aspose.PSD
- drawing shapes java
- gradient fill java
- initialize graphics java
title: Come disegnare un'ellisse usando la grafica in Java con Aspose.PSD
url: /it/java/java-graphics-drawing/drawing-using-graphics/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Come disegnare un'ellisse usando la grafica in Java con Aspose.PSD

## Introduzione
In questo tutorial di grafica Java scoprirai **come disegnare oggetti ellisse** e altre forme programmaticamente usando Aspose.PSD per Java. Che tu debba generare miniature dinamiche, creare elementi UI personalizzati o automatizzare flussi di lavoro di design, padroneggiare il disegno di ellissi e i riempimenti a gradiente ti offre un controllo visivo preciso. I passaggi seguenti ti guidano nell'inizializzare la grafica, configurare penne e pennelli, ed esportare il risultato nei formati immagine più comuni.

## Risposte rapide
- **Quale libreria è necessaria?** Aspose.PSD per Java (scaricabile dal sito ufficiale).  
- **Su quale forma si concentra il tutorial?** Disegnare un'ellisse e riempire un poligono.  
- **Posso esportare in formati diversi da BMP?** Sì – PNG, JPEG, TIFF e altri sono supportati.  
- **È necessaria una licenza per lo sviluppo?** Una licenza temporanea gratuita funziona per i test; è richiesta una licenza completa per la produzione.  
- **L'API è adatta a immagini di grandi dimensioni?** Aspose.PSD elabora file fino a 500 MB senza caricare l'intero bitmap in memoria.

## Come disegnare un'ellisse in Java?
Carica un `PsdImage` con la larghezza e altezza desiderate, crea un oggetto `Graphics`, imposta una `Pen` e chiama `drawEllipse` con un rettangolo di delimitazione. L'intera operazione richiede solo poche chiamate di metodo e viene eseguita in meno di un secondo per immagini tipiche 800×600 su hardware moderno.

## Cos'è Aspose.PSD per Java?
Aspose.PSD per Java è una **libreria pure‑Java che fornisce oltre 50 conversioni di formati immagine e capacità complete di editing PSD** senza la necessità di Adobe Photoshop. Può renderizzare, modificare ed esportare file multi‑layer mantenendo un basso utilizzo di memoria, rendendola ideale per la generazione di grafica lato server.

## Perché usare Aspose.PSD per disegnare forme?
Aspose.PSD offre alte prestazioni, ampio supporto di formati e rendering preciso, rendendola ideale per la generazione di grafica lato server e per il disegno di forme complesse.

- **Prestazioni:** Gestisce immagini fino a 500 MB con meno di 150 MB di heap (≈30 % in meno rispetto a librerie concorrenti).  
- **Supporto formati:** Oltre 50 formati di input e output, inclusi BMP, PNG, JPEG, TIFF e PSD.  
- **Precisione:** Il rendering sub‑pixel garantisce ellissi nitide e gradienti fluidi su display ad alta DPI.

## Prerequisiti
- Conoscenza di base della programmazione Java.  
- Java Development Kit (JDK) installato.  
- Un IDE come IntelliJ IDEA o Eclipse.  
- Libreria Aspose.PSD per Java. Puoi scaricarla da [Aspose.PSD Java download](https://releases.aspose.com/psd/java/).

## Importa pacchetti
Per iniziare, importa le classi Aspose.PSD necessarie e le utility Java standard. Le classi seguenti forniscono primitive di disegno e gestione dei colori:
```java
import com.aspose.psd.Color;
import com.aspose.psd.Graphics;
import com.aspose.psd.Pen;
import com.aspose.psd.Point;
import com.aspose.psd.Rectangle;
import com.aspose.psd.brushes.LinearGradientBrush;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.BmpOptions;
```

## Passo 1: crea un oggetto immagine
`PsdImage` rappresenta una tela raster in memoria su cui è possibile disegnare e salvare in vari formati.
```java
String dataDir = "Your Document Directory";
PsdImage image = new PsdImage(500, 500);
```

## Passo 2: inizializza l'oggetto grafico
`Graphics` è la superficie di disegno collegata a un `PsdImage`, consentendo operazioni vettoriali come il disegno di forme.
```java
Graphics graphics = new Graphics(image);
```

## Passo 3: pulisci la superficie dell'immagine
`clear` riempie l'intera tela con un unico colore di sfondo.
```java
graphics.clear(Color.getWhite());
```

## Passo 4: crea e configura l'oggetto penna
`Pen` definisce il colore, la larghezza e lo stile del tratto usato per disegnare i contorni.
```java
Pen pen = new Pen(Color.getBlue());
```

## Passo 5: disegna le forme
`drawEllipse` rende un'ellisse che si adatta al rettangolo specificato usando la penna corrente.
```java
graphics.drawEllipse(pen, new Rectangle(10, 10, 150, 100));
```

## Passo 6: usa i pennelli per il riempimento
`LinearGradientBrush` crea un riempimento a gradiente che transita tra due colori su un'area definita.
```java
LinearGradientBrush linearGradientBrush = new LinearGradientBrush(image.getBounds(), Color.getRed(), Color.getWhite(), 45f);
Point[] points = { new Point(200, 200), new Point(400, 200), new Point(250, 350) };
graphics.fillPolygon(linearGradientBrush, points);
```

## Passo 7: salva l'immagine modificata
`save` scrive il `PsdImage` su disco nel formato scelto, come BMP o PNG.
```java
image.save(dataDir + "DrawingUsingGraphics_output.bmp", new BmpOptions());
```

## Problemi comuni e risoluzione
- **NullPointerException sulla grafica:** Assicurati che il `PsdImage` sia completamente istanziato prima di creare l'oggetto `Graphics`.  
- **Colori errati:** Usa `Color.fromArgb` per specificare valori ARGB esatti quando la palette predefinita non corrisponde alle aspettative.  
- **Ritardi di prestazioni su immagini grandi:** Abilita `PsdImageOptions` con `compression = CompressionType.Rle` per ridurre l'overhead di memoria.

## Domande frequenti

**D: Aspose.PSD può gestire manipolazioni di immagine complesse?**  
R: Sì, supporta la fusione di livelli, regolazioni di canale, rendering di testo e mascheramento avanzato oltre al disegno di forme.

**D: Aspose.PSD è adatto per applicazioni ad alte prestazioni?**  
R: Assolutamente; la libreria è ottimizzata per la velocità e può elaborare un'immagine da 10 MP in meno di 2 secondi su un server tipico.

**D: Dove posso trovare più esempi e documentazione?**  
R: Visita la [documentazione Aspose.PSD Java](https://reference.aspose.com/psd/java/) per guide complete e riferimenti API.

**D: Aspose.PSD supporta più formati immagine per l'esportazione?**  
R: Sì, puoi esportare in BMP, PNG, JPEG, TIFF, GIF e PSD, tra gli altri.

**D: Come posso ottenere supporto o assistenza se incontro problemi?**  
R: Rivolgiti alla community Aspose.PSD sul [forum di supporto](https://forum.aspose.com/c/psd/34) o considera una [licenza temporanea](https://purchase.aspose.com/temporary-license/) per assistenza prioritaria.

---

**Ultimo aggiornamento:** 2026-09-13  
**Testato con:** Aspose.PSD per Java 24.10  
**Autore:** Aspose

## Tutorial correlati

- [Ridimensiona immagine con Aspose.PSD per Java – Disegna forme e operazioni di base sull'immagine](/psd/java/basic-image-operations/)
- [Disegna e salva un rettangolo in un PSD usando Aspose.PSD per Java](/psd/java/basic-image-operations/simple-drawing/)
- [Aggiungi firma all'immagine – Disegna immagine su canvas con Aspose.PSD per Java](/psd/java/advanced-image-effects/add-signature-to-image/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}