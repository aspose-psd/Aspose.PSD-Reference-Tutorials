---
date: 2026-06-13
description: Scopri come disegnare un rettangolo nei file PSD usando Aspose.PSD per
  Java. Questa guida mostra codice passo‑passo, aggiunta di livelli, elaborazione
  di immagini lato server e disegno di forme.
keywords:
- how to draw rectangle
- how to create psd
- java graphics draw rectangle
- server side image processing
- add layer to psd
linktitle: Esegui un disegno semplice
schemas:
- author: Aspose
  dateModified: '2026-06-13'
  description: Learn how to draw rectangle in PSD files using Aspose.PSD for Java.
    This guide shows step‑by‑step code, adding layers, server‑side image processing
    and shape drawing.
  headline: How to Draw Rectangle in PSD with Aspose.PSD for Java
  type: TechArticle
- questions:
  - answer: Yes, the `Graphics` class also supports drawing ellipses, lines, and custom
      paths via the `drawPath` method.
    question: Can I draw other shapes besides rectangles?
  - answer: Absolutely; you can use `SolidBrush` with an ARGB color to include alpha
      transparency, enabling semi‑transparent overlays.
    question: Does Aspose.PSD support transparency in drawn shapes?
  - answer: Yes, each `Layer` object has a `setOpacity` method that accepts a value
      from 0 to 255, allowing fine‑grained control over layer transparency.
    question: Is it possible to edit the opacity of a layer?
  - answer: Use `PsdImage image = (PsdImage)Image.load("path/to/file.psd");` before
      manipulating layers. The loaded image retains all original layers and masks.
    question: How do I load an existing PSD file instead of creating a new one?
  type: FAQPage
second_title: Aspose.PSD Java API
title: Come disegnare un rettangolo in PSD con Aspose.PSD per Java
url: /it/java/basic-image-operations/simple-drawing/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Come disegnare un rettangolo in PSD con Aspose.PSD per Java

## Introduzione

In questo tutorial scoprirai **come disegnare un rettangolo** all'interno di un file Photoshop PSD utilizzando la libreria pure‑Java Aspose.PSD. Che tu stia costruendo una pipeline di asset lato server, automatizzando la creazione di miniature, o aggiungendo grafiche dinamiche a design esistenti, i passaggi seguenti ti offrono una soluzione completa, pronta per la produzione. Copriremo la creazione di un nuovo documento PSD, l'aggiunta di un livello, la pulizia dello sfondo e, infine, il disegno di rettangoli rossi e blu—tutto senza mai avviare Photoshop.

## Risposte rapide
- **Qual è la classe principale per creare un file PSD?** `PsdImage`
- **Quale metodo cancella il colore di sfondo di un livello?** `Graphics.clear(Color)`
- **Come si disegna un rettangolo rosso?** `graphic.drawRectangle(new Pen(Color.getRed()), new Rectangle(...))`
- **È necessaria una licenza per lo sviluppo?** Una versione di prova gratuita funziona per i test; è richiesta una licenza per la produzione.
- **Posso manipolare file PSD esistenti con la stessa API?** Sì, Aspose.PSD supporta la modifica completa dei PSD.

## Che cosa significa disegnare un rettangolo rosso in un file PSD?

Disegnare un rettangolo rosso significa utilizzare l'oggetto `Graphics` per renderizzare una forma rettangolare riempita o contornata con il colore rosso su uno specifico livello di un'immagine PSD. Questa operazione è comune per evidenziare aree, creare segnaposto o aggiungere grafiche semplici in modo programmatico.

## Perché usare Aspose.PSD per Java per manipolare file PSD?

Aspose.PSD per Java supporta **oltre 50 formati di input e output**, può elaborare file PSD con centinaia di pagine senza caricare l'intero file in memoria e funziona su qualsiasi piattaforma che supporti Java 8 o superiore. Il suo motore di elaborazione immagini lato server elimina la necessità di Photoshop, riduce i costi di licenza e consente flussi di lavoro automatizzati che gestiscono fino a **10 GB** di dati immagine all'ora su una VM modesta.

## Prerequisiti

- Java Development Kit (JDK) 8 o successivo installato sulla tua macchina.  
- Libreria Aspose.PSD per Java. Puoi scaricarla dalla [Aspose.PSD for Java Documentation](https://reference.aspose.com/psd/java/).

## Importare i pacchetti

Le istruzioni `import` portano le classi necessarie nello scope così da poter lavorare con immagini PSD, livelli, colori e grafica.

La classe `PsdImage` è l'oggetto di livello superiore di Aspose.PSD che rappresenta un singolo file PSD in memoria.  
`Graphics` fornisce primitive di disegno come linee, rettangoli ed ellissi.  
`Color` e `Pen` consentono di specificare i colori di traccia e lo spessore.  
La classe `Layer` rappresenta un singolo livello immagine all'interno di un documento PSD.  
La classe `Rectangle` definisce la posizione e le dimensioni di un'area rettangolare usata per le operazioni di disegno.  
La classe `SolidBrush` riempie le forme con un colore solido.

## Qual è il primo passo per creare un documento PSD?

Instanzi `PsdImage` fornendo la larghezza e l'altezza della tela in pixel, il che crea una struttura di file PSD vuota. Dopo aver impostato eventuali livelli iniziali o lo sfondo, invoca il metodo `save` con un percorso file per scrivere il documento su disco. Questo prepara l'immagine per le successive operazioni di modifica.

## Passo 1: Creare un nuovo documento

Per prima cosa, crea un nuovo documento PSD con le dimensioni della tela desiderate. Questo documento ospiterà il livello su cui disegneremo.

```java
import com.aspose.psd.Color;
import com.aspose.psd.Graphics;
import com.aspose.psd.Pen;
import com.aspose.psd.Rectangle;
import com.aspose.psd.brushes.SolidBrush;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.Layer;
```

## Come aggiungere un nuovo livello vuoto a un'immagine PSD?

Per prima cosa, crea una nuova istanza `Layer` con la stessa larghezza e altezza del `PsdImage` genitore. Quindi aggiungi questo livello alla collezione `Layers` dell'immagine usando il metodo `add`. Una volta che il livello fa parte dell'immagine, recupera il suo oggetto `Graphics` per eseguire le operazioni di disegno; senza questo passaggio i disegni non appariranno.

## Passo 2: Aggiungere un livello

Successivamente, aggiungi un nuovo livello vuoto che copra tutta la larghezza e altezza dell'immagine. I livelli sono essenziali per separare le operazioni di disegno.

```java
//ExStart:CreateDocument
String outputDir = "Your Document Directory";
String outPsdFilePath = outputDir + "output.psd";
int width = 100;
int height = 100;

PsdImage image = new PsdImage(width, height);
//ExEnd:CreateDocument
```

## Qual è lo scopo di cancellare il colore di sfondo di un livello?

Chiamare `Graphics.clear` con un `Color` specifico riempie l'intero livello con quel colore, resettando effettivamente tutti i dati pixel. Questo garantisce che eventuali contenuti precedenti vengano rimossi e che il livello parta da uno sfondo noto, evitando trasparenze o mescolamenti di colore inaspettati quando il PSD viene successivamente aperto o modificato in Photoshop.

## Passo 3: Disegnare forme

Useremo la classe `Graphics` per manipolare i dati pixel del livello. Di seguito tre esempi che illustrano la pulizia dello sfondo e il disegno di rettangoli con colori diversi.

### Cancella il colore del livello (imposta lo sfondo su giallo)

```java
//ExStart:AddLayer
Layer layer = new Layer();
layer.setBottom(height);
layer.setRight(width);
image.addLayer(layer);
//ExEnd:AddLayer
```

### Disegna un rettangolo rosso (focus principale)

```java
//ExStart:DrawRectangleYellow
Graphics graphic = new Graphics(layer);
graphic.clear(Color.getYellow());
//ExEnd:DrawRectangleYellow
```

### Disegna un rettangolo blu (esempio aggiuntivo)

```java
//ExStart:DrawRedRectangle
graphic.drawRectangle(new Pen(Color.getRed()), new Rectangle(30, 10, 40, 80));
//ExEnd:DrawRedRectangle
```

## Come salvare il file PSD modificato su disco?

Usa il metodo `save` sull'oggetto `PsdImage`, passando il percorso file completo e, facoltativamente, specificando il formato immagine desiderato (PSD di default). Questo scrive tutti i livelli, le maschere e i comandi di disegno in un unico file PSD conforme alla specifica Photoshop, consentendo l'apertura senza avvisi.

## Passo 4: Salvare le modifiche

Infine, scrivi l'immagine PSD modificata su disco. Il file conterrà il nuovo livello e le forme disegnate.

```java
//ExStart:DrawBlueRectangle
graphic.drawRectangle(new Pen(new SolidBrush(Color.getBlue())), new Rectangle(10, 30, 80, 40));
//ExEnd:DrawBlueRectangle
```

## Problemi comuni e soluzioni

- **Livello non visibile dopo il disegno:** Assicurati che il livello sia aggiunto all'immagine **prima** di creare l'oggetto `Graphics`. La superficie di disegno deve essere collegata a un livello valido.
- **I colori appaiono errati:** Verifica di utilizzare `Color.getRed()` (o `Color.getBlue()`) invece di costruire un valore RGB personalizzato che superi l'intervallo 0‑255.
- **File non salvato:** Conferma che il percorso `outputDir` esista e che l'applicazione abbia i permessi di scrittura. Su Linux potresti dover regolare la proprietà della cartella o usare `Files.createDirectories`.
- **Rallentamento delle prestazioni su file grandi:** Usa `setLoadOptions` di `PsdImage` per caricare solo i canali necessari, riducendo il consumo di memoria per PSD superiori a 200 MB.

## Domande frequenti

**Q1: Posso usare Aspose.PSD per Java per manipolare file PSD esistenti?**  
A1: Sì, Aspose.PSD per Java offre funzionalità estese per modificare e manipolare file PSD esistenti, inclusi riordino dei livelli, regolazioni delle maschere e disegno vettoriale.

**Q2: Dove posso trovare supporto per Aspose.PSD per Java?**  
A2: Puoi visitare il [Aspose.PSD for Java Forum](https://forum.aspose.com/c/psd/34) per assistenza dalla community e risposte ufficiali di Aspose.

**Q3: È disponibile una versione di prova gratuita per Aspose.PSD per Java?**  
A3: Sì, puoi accedere alla versione di prova gratuita [qui](https://releases.aspose.com/). La prova include tutte le funzionalità ma aggiunge una filigrana ai file salvati.

**Q4: Come posso acquistare una licenza per Aspose.PSD per Java?**  
A4: Puoi acquistare una licenza dalla [Aspose.PSD Purchase Page](https://purchase.aspose.com/buy). Le opzioni di licenza includono licenze perpetue, in abbonamento e per sito.

**Q5: Sono disponibili licenze temporanee per Aspose.PSD per Java?**  
A5: Sì, puoi ottenere una licenza temporanea [qui](https://purchase.aspose.com/temporary-license/).

## Altre domande frequenti

**Q: Posso disegnare altre forme oltre ai rettangoli?**  
A: Sì, la classe `Graphics` supporta anche il disegno di ellissi, linee e percorsi personalizzati tramite il metodo `drawPath`.

**Q: Aspose.PSD supporta la trasparenza nelle forme disegnate?**  
A: Assolutamente; puoi usare `SolidBrush` con un colore ARGB per includere la trasparenza alfa, consentendo sovrapposizioni semi‑trasparenti.

**Q: È possibile modificare l'opacità di un livello?**  
A: Sì, ogni oggetto `Layer` dispone del metodo `setOpacity` che accetta un valore da 0 a 255, permettendo un controllo fine sulla trasparenza del livello.

**Q: Come carico un file PSD esistente invece di crearne uno nuovo?**  
A: Usa `PsdImage image = (PsdImage)Image.load("path/to/file.psd");` prima di manipolare i livelli. L'immagine caricata conserva tutti i livelli e le maschere originali.

## Conclusione

Ora hai padroneggiato **come disegnare rettangoli** e manipolare i livelli all'interno di un file PSD usando Aspose.PSD per Java. Creando un documento, aggiungendo un livello, pulendo lo sfondo e disegnando con l'API `Graphics`, puoi automatizzare innumerevoli attività di design grafico lato server. Sperimenta con penne, pennelli ed effetti di livello diversi per estendere questa base in pipeline di generazione di immagini complete.

```java
//ExStart:SaveChanges
image.save(outPsdFilePath);
//ExEnd:SaveChanges
```

{{< blocks/products/products-backtop-button >}}

## Tutorial correlati

- [How to Draw Shapes Java – Basic Image Operations](/psd/java/basic-image-operations/)
- [Simple Resizing with Aspose.PSD – Java Image Manipulation Library](/psd/java/basic-image-operations/simple-resizing/)
- [Crop Image by Rectangle in Aspose.PSD for Java](/psd/java/image-editing/crop-image-by-rectangle/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

---

**Last Updated:** 2026-06-13  
**Tested With:** Aspose.PSD for Java 24.12 (latest at time of writing)  
**Author:** Aspose