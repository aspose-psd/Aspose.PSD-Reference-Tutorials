---
date: 2026-09-08
description: Scopri come creare un'immagine con la classe Graphics Path di Aspose.PSD
  in Java. Questa guida passo‑passo ti mostra come aggiungere testo, forme e cancellare
  lo sfondo dell'immagine in modo efficiente.
keywords:
- how to create image
- add text image java
- clear image background java
lastmod: 2026-09-08
linktitle: Come creare un'immagine usando Graphics Path in Java
og_description: Scopri come creare un'immagine con Aspose.PSD in Java. Questo tutorial
  copre l'aggiunta di testo, forme e la cancellazione dello sfondo dell'immagine usando
  la classe Graphics Path.
og_image_alt: Screenshot of Java code creating an image with graphics path using Aspose.PSD
og_title: Come creare un'immagine usando Graphics Path in Java con Aspose.PSD
schemas:
- author: Aspose
  dateModified: '2026-09-08'
  description: Learn how to create image with Aspose.PSD's Graphics Path class in
    Java. This step‑by‑step guide shows you how to add text, shapes, and clear image
    background efficiently.
  headline: How to create image using Graphics Path in Java
  type: TechArticle
- description: Learn how to create image with Aspose.PSD's Graphics Path class in
    Java. This step‑by‑step guide shows you how to add text, shapes, and clear image
    background efficiently.
  name: How to create image using Graphics Path in Java
  steps:
  - name: '**Java Development Kit (JDK)** – a stable JDK 11+ installed. Download it
      from [Oracle’s site](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).'
    text: '**Java Development Kit (JDK)** – a stable JDK 11+ installed. Download it
      from [Oracle’s site](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).'
  - name: '**Aspose.PSD for Java library** – obtain the latest JAR from [here](https://releases.aspose.com/psd/java/)
      and add it to your project’s classpath.'
    text: '**Aspose.PSD for Java library** – obtain the latest JAR from [here](https://releases.aspose.com/psd/java/)
      and add it to your project’s classpath.'
  - name: '**IDE** – any Java IDE such as Eclipse, IntelliJ IDEA, or VS Code.'
    text: '**IDE** – any Java IDE such as Eclipse, IntelliJ IDEA, or VS Code.'
  type: HowTo
- questions:
  - answer: Aspose.PSD is a Java library that enables you to create, edit, and convert
      Photoshop (PSD) files and other raster formats without requiring Photoshop.
    question: What is Aspose.PSD?
  - answer: Yes – the library supports **50+** formats, including PNG, JPEG, BMP,
      TIFF, and GIF.
    question: Can I work with formats other than PSD?
  - answer: Yes, you can access a free trial of Aspose.PSD [here](https://releases.aspose.com/).
    question: Is a trial version available?
  - answer: You can purchase Aspose.PSD from [here](https://purchase.aspose.com/buy).
    question: How do I purchase a license?
  - answer: You can seek support and discussions on [Aspose’s forum](https://forum.aspose.com/c/psd/34).
    question: Where can I get support?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- graphics path
- Aspose.PSD
- Java image processing
title: Come creare un'immagine usando Graphics Path in Java
url: /it/java/java-graphics-drawing/drawing-using-graphics-path/
weight: 19
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Come creare un'immagine usando Graphics Path in Java

## Introduzione
In questo tutorial imparerai **come creare file immagine** programmaticamente sfruttando la potente classe **Graphics Path** fornita da Aspose.PSD per Java. Che tu debba disegnare forme personalizzate, incorporare testo o cancellare lo sfondo di un'immagine, la guida passo‑passo qui sotto ti mostra esattamente come ottenere risultati di livello professionale con poche righe di codice.

## Risposte rapide
- **Quale libreria gestisce il disegno complesso?** La classe Graphics Path di Aspose.PSD per Java.  
- **Posso aggiungere testo all'immagine?** Sì – usa il metodo `GraphicsPath.addString`.  
- **È supportata la cancellazione dello sfondo?** Assolutamente, riempi il percorso con un pennello trasparente.  
- **Quale versione di Java è necessaria?** JDK 11 o superiore.  
- **È necessaria una licenza per la produzione?** È richiesta una licenza commerciale; è disponibile una versione di prova gratuita.

## Cos'è la classe Graphics Path?
La classe `GraphicsPath` è l'oggetto principale di Aspose.PSD per definire istruzioni di disegno basate su vettori. Ti consente di comporre forme, testo e riempimenti in un unico percorso riutilizzabile che può essere renderizzato su qualsiasi immagine. Creando un percorso, puoi applicare penne, pennelli e trasformazioni in un unico passaggio di rendering, migliorando le prestazioni e mantenendo il codice di disegno organizzato.

## Perché usare Graphics Path per aggiungere testo a un'immagine Java e cancellare lo sfondo dell'immagine Java?
Aspose.PSD supporta **oltre 50 formati di immagine** (inclusi PSD, PNG, JPEG, BMP) e può elaborare file fino a **2 GB** senza caricare l'intero documento in memoria. L'uso di Graphics Path ti permette di combinare disegno, posizionamento del testo e cancellazione dello sfondo in un'unica operazione ad alte prestazioni, riducendo il consumo di memoria fino al **30 %** rispetto agli approcci basati solo su raster.

## Prerequisiti
Prima di iniziare, assicurati di avere quanto segue:

1. **Java Development Kit (JDK)** – un JDK 11+ stabile installato. Scaricalo dal [sito di Oracle](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).  
2. **Libreria Aspose.PSD per Java** – ottieni l'ultimo JAR da [qui](https://releases.aspose.com/psd/java/) e aggiungilo al classpath del tuo progetto.  
3. **IDE** – qualsiasi IDE Java come Eclipse, IntelliJ IDEA o VS Code.

Con questi elementi a disposizione, sei pronto per iniziare a creare immagini.

## Importare i pacchetti
Per lavorare con la grafica, importa gli spazi dei nomi necessari:

```java
import com.aspose.psd.Color;
import com.aspose.psd.Figure;
import com.aspose.psd.Font;
import com.aspose.psd.Graphics;
import com.aspose.psd.GraphicsPath;
import com.aspose.psd.HatchStyle;
import com.aspose.psd.Pen;
import com.aspose.psd.RectangleF;
import com.aspose.psd.StringFormat;
import com.aspose.psd.brushes.HatchBrush;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.shapes.EllipseShape;
import com.aspose.psd.shapes.RectangleShape;
import com.aspose.psd.shapes.TextShape;
```

Queste importazioni espongono le classi di disegno, pennello e penna necessarie per la manipolazione delle immagini.

## Come creare un'immagine con Graphics Path in Java?
Crea una nuova tela raster, collega un oggetto `Graphics` e prepara la superficie di disegno. Questo unico passaggio imposta un bitmap **500 × 500 pixel** pronto per il rendering vettoriale. La tela è inizialmente trasparente, consentendoti di riempirla successivamente con qualsiasi colore o motivo di sfondo tu scelga, il che è fondamentale per scenari di cancellazione dello sfondo.

```java
PsdImage image = new PsdImage(500, 500);
Graphics graphics = new Graphics(image);
graphics.clear(Color.getWhite());
```

## Passo 1: inizializzare immagine e graphics
Qui istanziamo un oggetto `PsdImage` (500 × 500) e otteniamo il suo contesto `Graphics`.  
`PsdImage` rappresenta un'immagine raster in memoria che Aspose.PSD può manipolare e salvare in molti formati.  
`Graphics` fornisce i metodi di disegno che renderizzano forme, testo e percorsi sul `PsdImage`.

## Passo 2: creare e configurare il graphics path
Successivamente, costruiamo un `GraphicsPath` che contiene un cerchio, un rettangolo e un'etichetta di testo.  
`GraphicsPath` è un contenitore per figure geometriche; puoi aggiungere forme, linee e stringhe prima del rendering.

```java
GraphicsPath graphicspath = new GraphicsPath();
Figure figure = new Figure();
figure.addShape(new EllipseShape(new RectangleF(0, 0, 499, 499)));
figure.addShape(new RectangleShape(new RectangleF(0, 0, 499, 499)));
figure.addShape(new TextShape("Aspose.PSD", new RectangleF(170, 225, 170, 100), new TextFont("Arial", 20), StringFormat.getGenericTypographic()));
Figure[] fig = { figure };
graphicspath.addFigures(fig);
```

### Aggiungere testo all'immagine (add text image java)
Il metodo `addString` di `GraphicsPath` posiziona il testo specificato alle coordinate indicate usando il font e il pennello forniti. Questo è il modo più affidabile per incorporare testo nitido e scalabile all'interno del percorso vettoriale.

## Passo 3: disegnare e riempire il percorso
Ora renderizziamo il percorso con una penna blu e lo riempiamo usando un pennello a trama verticale, dimostrando anche come **cancellare lo sfondo dell'immagine java** riempiendo con un pattern trasparente, se desiderato. La `Pen` definisce lo stile del contorno, mentre la `HatchBrush` crea un riempimento a trama.

```java
graphics.drawPath(new Pen(Color.getBlue()), graphicspath);
HatchBrush hatchbrush = new HatchBrush();
hatchbrush.setBackgroundColor(Color.getBrown());
hatchbrush.setForegroundColor(Color.getBlue());
hatchbrush.setHatchStyle(HatchStyle.Vertical);
graphics.fillPath(hatchbrush, graphicspath);
```

## Passo 4: salvare l'immagine
Infine, scrivi l'immagine composta su disco in formato PNG (o in qualsiasi dei 50+ formati supportati). Il metodo `save` determina il tipo di file di output dall'estensione fornita.

```java
String dataDir = "Your Document Directory";
image.save(dataDir + "DrawingUsingGraphicsPath_output.psd");
```

## Problemi comuni e soluzioni
- **Percorso non visibile** – assicurati che il colore della penna contrasti con il pennello di riempimento.  
- **Il testo appare sfocato** – usa un'immagine a risoluzione più alta o un font TrueType con DPI sufficienti.  
- **Errori di out‑of‑memory su file grandi** – abilita `PsdImageOptions.setUseMemoryCache(true)` per lo streaming dei dati invece di caricarli completamente.

## Domande frequenti

**D: Cos'è Aspose.PSD?**  
R: Aspose.PSD è una libreria Java che consente di creare, modificare e convertire file Photoshop (PSD) e altri formati raster senza necessità di Photoshop.

**D: Posso lavorare con formati diversi da PSD?**  
R: Sì – la libreria supporta **oltre 50** formati, inclusi PNG, JPEG, BMP, TIFF e GIF.

**D: È disponibile una versione di prova?**  
R: Sì, puoi accedere a una prova gratuita di Aspose.PSD [qui](https://releases.aspose.com/).

**D: Come acquisto una licenza?**  
R: Puoi acquistare Aspose.PSD da [qui](https://purchase.aspose.com/buy).

**D: Dove posso ottenere supporto?**  
R: Puoi richiedere supporto e partecipare a discussioni sul [forum di Aspose](https://forum.aspose.com/c/psd/34).

## Conclusione
Seguendo questa guida ora sai **come creare file immagine** con forme vettoriali complesse, testo incorporato e sfondi trasparenti usando la classe Graphics Path di Aspose.PSD. Sperimenta con penne, pennelli e geometrie di percorso diversi per creare grafiche più ricche per giochi, elementi UI o generazione automatica di report.

---

**Ultimo aggiornamento:** 2026-09-08  
**Testato con:** Aspose.PSD per Java 24.11  
**Autore:** Aspose

## Tutorial correlati

- [Genera un'immagine PSD in Java impostando il percorso con Aspose.PSD](/psd/java/image-editing/create-image-by-setting-path/)
- [Ridimensiona immagine con Aspose.PSD per Java – Disegna forme e operazioni di base sulle immagini](/psd/java/basic-image-operations/)
- [Aggiungi firma all'immagine – Disegna immagine su canvas con Aspose.PSD per Java](/psd/java/advanced-image-effects/add-signature-to-image/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}