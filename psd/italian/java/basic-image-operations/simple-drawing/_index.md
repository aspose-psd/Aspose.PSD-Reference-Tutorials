---
date: 2025-12-27
description: Impara a disegnare rettangoli rossi e altre forme nei file PSD usando
  Aspose.PSD per Java. Questa guida passo‑passo copre la creazione di documenti, l'aggiunta
  di livelli e il disegno con esempi di codice.
linktitle: Perform Simple Drawing
second_title: Aspose.PSD Java API
title: Disegna un rettangolo rosso con Aspose.PSD per Java
url: /it/java/basic-image-operations/simple-drawing/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Disegnare un Rettangolo Rosso con Aspose.PSD per Java

## Introduzione

Benvenuti a questa guida passo‑a‑passo su come **disegnare un rettangolo rosso** usando Aspose.PSD per Java! In questo tutorial, illustreremo come creare un nuovo documento PSD, aggiungere un livello e disegnare forme con colori personalizzati. Che tu stia automatizzando risorse grafiche o costruendo il back‑end di uno strumento di design, questo tutorial ti fornisce i blocchi fondamentali.

## Risposte Rapide
- **Qual è la classe principale per creare un file PSD?** `PsdImage`
- **Quale metodo cancella il colore di sfondo di un livello?** `Graphics.clear(Color)`
- **Come si disegna un rettangolo rosso?** `graphic.drawRectangle(new Pen(Color.getRed()), new Rectangle(...))`
- **È necessaria una licenza per lo sviluppo?** Una versione di prova gratuita funziona per i test; è richiesta una licenza per la produzione.
- **Posso manipolare file PSD esistenti con la stessa API?** Sì, Aspose.PSD supporta la modifica completa dei PSD.

## Che cosa significa disegnare un rettangolo rosso in un file PSD?
Disegnare un rettangolo rosso significa utilizzare l'oggetto `Graphics` per renderizzare una forma rettangolare riempita o contornata con il colore rosso su un livello specifico di un'immagine PSD. Questa operazione è comune per evidenziare aree, creare segnaposto o aggiungere grafiche semplici in modo programmatico.

## Perché usare Aspose.PSD per Java per manipolare file PSD?
Aspose.PSD fornisce un'API pura Java che consente di leggere, modificare e scrivere file Photoshop PSD senza la necessità di avere Photoshop installato. Supporta la gestione dei livelli, la manipolazione dei colori e il disegno vettoriale, rendendola ideale per l'elaborazione di immagini lato server, pipeline di asset automatizzate e generazione di grafiche personalizzate.

## Prerequisiti

- Java Development Kit (JDK) installato sulla tua macchina.  
- Libreria Aspose.PSD per Java. Puoi scaricarla dalla [Aspose.PSD for Java Documentation](https://reference.aspose.com/psd/java/).

## Importare i Pacchetti

Per iniziare, importa le classi necessarie nel tuo progetto Java:

```java
import com.aspose.psd.Color;
import com.aspose.psd.Graphics;
import com.aspose.psd.Pen;
import com.aspose.psd.Rectangle;
import com.aspose.psd.brushes.SolidBrush;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.Layer;
```

## Passo 1: Creare un Nuovo Documento

Per prima cosa, crea un nuovo documento PSD con le dimensioni della tela desiderate. Questo documento ospiterà il livello su cui disegneremo.

```java
//ExStart:CreateDocument
String outputDir = "Your Document Directory";
String outPsdFilePath = outputDir + "output.psd";
int width = 100;
int height = 100;

PsdImage image = new PsdImage(width, height);
//ExEnd:CreateDocument
```

## Passo 2: Aggiungere un Livello

Successivamente, aggiungi un nuovo livello vuoto che copra l'intera larghezza e altezza dell'immagine. I livelli sono essenziali per separare le operazioni di disegno.

```java
//ExStart:AddLayer
Layer layer = new Layer();
layer.setBottom(height);
layer.setRight(width);
image.addLayer(layer);
//ExEnd:AddLayer
```

## Passo 3: Disegnare Forme

Utilizzeremo la classe `Graphics` per manipolare i dati pixel del livello. Di seguito tre esempi che illustrano come cancellare lo sfondo e disegnare rettangoli con colori diversi.

### Cancellare il Colore del Livello (impostare lo sfondo su giallo)

```java
//ExStart:DrawRectangleYellow
Graphics graphic = new Graphics(layer);
graphic.clear(Color.getYellow());
//ExEnd:DrawRectangleYellow
```

### Disegnare un Rettangolo Rosso (focus principale)

```java
//ExStart:DrawRedRectangle
graphic.drawRectangle(new Pen(Color.getRed()), new Rectangle(30, 10, 40, 80));
//ExEnd:DrawRedRectangle
```

### Disegnare un Rettangolo Blu (esempio aggiuntivo)

```java
//ExStart:DrawBlueRectangle
graphic.drawRectangle(new Pen(new SolidBrush(Color.getBlue())), new Rectangle(10, 30, 80, 40));
//ExEnd:DrawBlueRectangle
```

## Passo 4: Salvare le Modifiche

Infine, scrivi l'immagine PSD modificata su disco. Il file conterrà il nuovo livello e le forme disegnate.

```java
//ExStart:SaveChanges
image.save(outPsdFilePath);
//ExEnd:SaveChanges
```

## Problemi Comuni e Soluzioni

- **Livello non visibile dopo il disegno:** Assicurati che il livello sia aggiunto all'immagine **prima** di creare l'oggetto `Graphics`.
- **I colori appaiono errati:** Verifica di utilizzare `Color.getRed()` (o altri metodi statici) invece di valori RGB personalizzati che potrebbero essere fuori intervallo.
- **File non salvato:** Controlla che il percorso `outputDir` esista e che l'applicazione abbia i permessi di scrittura.

## Domande Frequenti

### Q1: Posso usare Aspose.PSD per Java per manipolare file PSD esistenti?

A1: Sì, Aspose.PSD per Java fornisce ampie funzionalità per modificare e manipolare file PSD esistenti.

### Q2: Dove posso trovare supporto per Aspose.PSD per Java?

A2: Puoi visitare il [Aspose.PSD for Java Forum](https://forum.aspose.com/c/psd/34) per qualsiasi domanda relativa al supporto.

### Q3: È disponibile una versione di prova gratuita per Aspose.PSD per Java?

A3: Sì, puoi accedere alla versione di prova gratuita [qui](https://releases.aspose.com/).

### Q4: Come posso acquistare una licenza per Aspose.PSD per Java?

A4: Puoi acquistare una licenza dalla [Aspose.PSD Purchase Page](https://purchase.aspose.com/buy).

### Q5: Sono disponibili licenze temporanee per Aspose.PSD per Java?

A5: Sì, puoi ottenere una licenza temporanea [qui](https://purchase.aspose.com/temporary-license/).

## Altre Domande Frequenti

**D: Posso disegnare altre forme oltre ai rettangoli?**  
R: Sì, la classe `Graphics` supporta anche il disegno di ellissi, linee e percorsi personalizzati.

**D: Aspose.PSD supporta la trasparenza nelle forme disegnate?**  
R: Assolutamente; puoi usare `SolidBrush` con un colore ARGB per includere la trasparenza alfa.

**D: È possibile modificare l'opacità di un livello?**  
R: Sì, ogni oggetto `Layer` dispone del metodo `setOpacity` che accetta un valore da 0 a 255.

**D: Come carico un file PSD esistente invece di crearne uno nuovo?**  
R: Usa `PsdImage image = (PsdImage)Image.load("path/to/file.psd");` prima di manipolare i livelli.

## Conclusione

Ora sai come **disegnare un rettangolo rosso** e altre forme di base in un file PSD usando Aspose.PSD per Java. Creando un documento, aggiungendo un livello, cancellando lo sfondo e disegnando con l'API `Graphics`, puoi automatizzare molte attività di design grafico. Esplora ulteriormente sperimentando con diversi pennelli, effetti di livello e formati di file.

---

**Ultimo Aggiornamento:** 2025-12-27  
**Testato Con:** Aspose.PSD per Java 24.12 (ultima versione al momento della scrittura)  
**Autore:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}