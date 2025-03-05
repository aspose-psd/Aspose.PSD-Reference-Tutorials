---
title: Esegui un disegno semplice con Aspose.PSD per Java
linktitle: Esegui un disegno semplice
second_title: API Java Aspose.PSD
description: Scopri come disegnare forme nei file PSD utilizzando Aspose.PSD per Java. Questa guida passo passo illustra la creazione, l'aggiunta di livelli e il disegno con esempi di codice.
type: docs
weight: 10
url: /it/java/basic-image-operations/simple-drawing/
---
## Introduzione

Benvenuti in questa guida passo passo sull'esecuzione di disegni semplici utilizzando Aspose.PSD per Java! In questo tutorial esploreremo le nozioni di base per creare un nuovo documento PSD, aggiungere livelli e disegnare forme con colori diversi. Aspose.PSD per Java è una potente libreria che consente di manipolare i file PSD a livello di codice, fornendo funzionalità estese per le attività di progettazione grafica.

## Prerequisiti

Prima di immergerti nel tutorial, assicurati di avere i seguenti prerequisiti:

- Java Development Kit (JDK) installato sul tuo computer.
- Aspose.PSD per la libreria Java. Puoi scaricarlo da[Aspose.PSD per la documentazione Java](https://reference.aspose.com/psd/java/).

## Importa pacchetti

Per iniziare, importa i pacchetti necessari nel tuo progetto Java. Includi il seguente codice all'inizio del tuo file Java:

```java
import com.aspose.psd.Color;
import com.aspose.psd.Graphics;
import com.aspose.psd.Pen;
import com.aspose.psd.Rectangle;
import com.aspose.psd.brushes.SolidBrush;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.Layer;
```

## Passaggio 1: crea un nuovo documento

Iniziamo creando un nuovo documento PSD con larghezza e altezza specificate:

```java
//ExStart:Crea documento
String outputDir = "Your Document Directory";
String outPsdFilePath = outputDir + "output.psd";
int width = 100;
int height = 100;

PsdImage image = new PsdImage(width, height);
//ExEnd:Crea documento
```

## Passaggio 2: aggiungi un livello

Ora aggiungiamo un livello al documento utilizzando il costruttore senza argomenti:

```java
//ExStart:AddLayer
Layer layer = new Layer();
layer.setBottom(height);
layer.setRight(width);
image.addLayer(layer);
//ExEnd:AddLayer
```

## Passaggio 3: disegna forme

In questo passaggio utilizzeremo la classe Graphics per disegnare forme sul livello creato:

### Disegna un rettangolo con un colore giallo

```java
//ExStart: Disegna rettangolo giallo
Graphics graphic = new Graphics(layer);
graphic.clear(Color.getYellow());
//ExEnd: Disegna rettangolo giallo
```

### Disegna un rettangolo rosso

```java
//ExStart: Disegna rettangolo rosso
graphic.drawRectangle(new Pen(Color.getRed()), new Rectangle(30, 10, 40, 80));
//ExEnd: Disegna rettangolo rosso
```

### Disegna un rettangolo blu

```java
//ExStart: Disegna rettangolo blu
graphic.drawRectangle(new Pen(new SolidBrush(Color.getBlue())), new Rectangle(10, 30, 80, 40));
//ExEnd: Disegna rettangolo blu
```

## Passaggio 4: salva le modifiche

Infine, salva una copia del file PSD caricato includendo le modifiche:

```java
//ExStart:Salva modifiche
image.save(outPsdFilePath);
//ExEnd:Salva modifiche
```

## Conclusione

Congratulazioni! Hai eseguito con successo un disegno semplice utilizzando Aspose.PSD per Java. Questo tutorial ha trattato la creazione di un nuovo documento, l'aggiunta di livelli e il disegno di rettangoli con colori diversi. Sentiti libero di esplorare le funzionalità più avanzate offerte dalla libreria per le tue esigenze di progettazione grafica.

## Domande frequenti

### Q1: posso utilizzare Aspose.PSD per Java per manipolare file PSD esistenti?

A1: Sì, Aspose.PSD per Java fornisce funzionalità estese per modificare e manipolare file PSD esistenti.

### Q2: Dove posso trovare supporto per Aspose.PSD per Java?

 A2: Puoi visitare il[Aspose.PSD per il forum Java](https://forum.aspose.com/c/psd/34) per qualsiasi domanda relativa al supporto.

### Q3: È disponibile una prova gratuita per Aspose.PSD per Java?

 R3: Sì, puoi accedere alla versione di prova gratuita[Qui](https://releases.aspose.com/).

### Q4: Come posso acquistare una licenza per Aspose.PSD per Java?

 A4: È possibile acquistare una licenza da[Pagina di acquisto Aspose.PSD](https://purchase.aspose.com/buy).

### Q5: Sono disponibili licenze temporanee per Aspose.PSD per Java?

 R5: Sì, puoi ottenere una licenza temporanea da[Qui](https://purchase.aspose.com/temporary-license/).