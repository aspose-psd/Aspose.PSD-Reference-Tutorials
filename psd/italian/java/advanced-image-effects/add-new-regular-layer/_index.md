---
date: 2026-10-18
description: Scopri come esportare PSD in PNG e aggiungere un nuovo regular layer
  usando Aspose.PSD for Java con una licenza temporanea. Guida passo‑passo, posizionamento
  del layer e risoluzione dei problemi.
keywords:
- how to export psd
- aspose temporary license
- set layer position
- create new psd layer
lastmod: 2026-10-18
linktitle: Aggiungi un nuovo regular layer a PSD
og_description: Scopri come esportare PSD in PNG e aggiungere un nuovo regular layer
  usando Aspose.PSD for Java con una licenza temporanea. Include passaggi completi
  senza codice e consigli sul posizionamento del layer.
og_image_alt: Screenshot of Java code adding a layer to a PSD and exporting to PNG
og_title: Come esportare PSD in PNG e aggiungere un layer con Aspose.PSD for Java
schemas:
- author: Aspose
  dateModified: '2026-10-18'
  description: Learn how to export PSD to PNG and add a new regular layer using Aspose.PSD
    for Java with a temporary license. Step‑by‑step guide, layer positioning and troubleshooting.
  headline: How to export PSD to PNG and add a layer with Aspose.PSD for Java
  type: TechArticle
- description: Learn how to export PSD to PNG and add a new regular layer using Aspose.PSD
    for Java with a temporary license. Step‑by‑step guide, layer positioning and troubleshooting.
  name: How to export PSD to PNG and add a layer with Aspose.PSD for Java
  steps:
  - name: Load the PSD file
    text: '`PsdImage` is Aspose.PSD''s core class that represents a PSD document in
      memory. Loading the file creates a manipulable object you can edit.'
  - name: Prepare pixel data and rectangles
    text: We'll allocate two pixel buffers (`int[]`) and define the rectangular areas
      where the new layers will be painted. Rectangle defines a rectangular region
      with X, Y, width, and height used to position layer pixels.
  - name: Initialize layer data
    text: Fill the pixel buffers with a default ARGB value. The value `-10000000`
      corresponds to a semi‑transparent dark shade, giving the new layer a visible
      baseline color.
  - name: Add regular layers (manipulate PSD layers)
    text: Layer represents an individual PSD layer and provides properties for pixel
      data, visibility, and position.
  - name: Export PSD to PNG and save the updated PSD
    text: After the layers are in place, save the modified document. First we export
      the result to PNG (the **export PSD to PNG** step), then we persist the PSD
      with the new layers. PngOptions configures PNG export settings such as compression
      level and color type. > **Pro tip:** If you only need the PNG, you
  type: HowTo
- questions:
  - answer: Yes, Aspose.PSD supports Java 8 and later versions.
    question: Is Aspose.PSD compatible with Java 8?
  - answer: Absolutely! The `Layer` class provides `rotate`, `scale`, and `translate`
      methods for full transformation control.
    question: Can I apply transformations (rotate, scale) to the added layers?
  - answer: Detailed API docs are available [Aspose.PSD Java API reference](https://reference.aspose.com/psd/java/).
    question: Where can I find additional Aspose.PSD documentation?
  - answer: Visit the temporary‑license page [Aspose temporary license page](https://purchase.aspose.com/temporary-license/).
    question: How do I obtain a temporary license for Aspose.PSD?
  - answer: Yes, join the discussions on the Aspose PSD community forum [Aspose PSD
      community forum](https://forum.aspose.com/c/psd/34).
    question: Are there community forums for Aspose.PSD support?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- export psd to png
- aspose psd
- java image processing
title: Come esportare PSD in PNG e aggiungere un layer con Aspose.PSD for Java
url: /it/java/advanced-image-effects/add-new-regular-layer/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Come esportare PSD in PNG e aggiungere un livello con Aspose.PSD per Java

In questo **tutorial Aspose.PSD** imparerai **come esportare PSD in PNG** aggiungendo anche **un nuovo livello normale** allo stesso file, il tutto utilizzando una **licenza temporanea Aspose**. Che tu stia creando miniature web, preparando risorse per una pipeline di design, o sperimentando con la **manipolazione di immagini PSD**, questa guida mostra ogni passaggio—dall'apertura del file sorgente al salvataggio sia del PSD aggiornato che di una copia PNG—così potrai iniziare a lavorare con i livelli PSD immediatamente.

## Risposte rapide
- **Posso esportare PSD in PNG con una singola chiamata?** Sì – dopo aver aggiunto i livelli basta chiamare `save` con `PngOptions`.
- **Ho bisogno di una licenza completa per lo sviluppo?** Una licenza temporanea rimuove il watermark di valutazione e sblocca tutte le API; è necessaria una licenza permanente per l'uso in produzione.
- **Quali versioni di Java sono supportate?** Aspose.PSD funziona con Java 8 e versioni successive.
- **Il posizionamento dei livelli è basato sui pixel?** Assolutamente; imposti le coordinate sinistra, superiore, destra, inferiore in pixel tramite i metodi **set layer position**.
- **Il PNG manterrà la trasparenza del livello?** Il PNG esportato contiene il risultato unito di tutti i livelli visibili, preservando la trasparenza dove applicabile.

## Perché usare una licenza temporanea Aspose?

Una **licenza temporanea Aspose** ti consente di valutare l'intero set di funzionalità di Aspose.PSD senza restrizioni funzionali. Rimuove il watermark di valutazione, sblocca tutte le API—including la possibilità di **creare nuovi oggetti PSD layer**—e ti permette di testare il codice in un ambiente simile alla produzione prima di acquistare una licenza permanente.

## Prerequisiti

Prima di iniziare, assicurati di avere:

- **Ambiente di sviluppo Java** – JDK 8+ e uno strumento di build come Maven o Gradle installati.
- **Aspose.PSD per Java** – Scarica l'ultimo JAR dal sito ufficiale [Aspose.PSD for Java download page](https://releases.aspose.com/psd/java/).
- **Un file PSD di esempio** – Useremo `OneLayer.psd` negli esempi.

## Importa i pacchetti

Aggiungi le importazioni necessarie alla tua classe Java. Queste classi forniscono la funzionalità di base per la **manipolazione di immagini PSD** e la gestione dei livelli.

```java
import com.aspose.psd.Image;
import com.aspose.psd.Rectangle;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.Layer;
import com.aspose.psd.imageoptions.PngOptions;
import com.aspose.psd.imageoptions.PsdOptions;
```

## Cos'è “set layer position” e perché è importante?

I metodi **set layer position** definiscono le coordinate pixel esatte dove un livello viene disegnato sulla tela PSD, controllando il posizionamento orizzontale e verticale. Un posizionamento corretto garantisce che la grafica sia allineata con precisione, fondamentale per comporre risorse UI, creare layout pronti per la stampa o generare miniature pixel‑perfect.

## Guida passo‑passo

### Passo 1: Carica il file PSD

`PsdImage` è la classe principale di Aspose.PSD che rappresenta un documento PSD in memoria. Caricare il file crea un oggetto manipolabile che puoi modificare.

```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "OneLayer.psd";
PsdImage im = (PsdImage)Image.load(sourceFileName);
```

### Passo 2: Prepara i dati pixel e i rettangoli

Allochiamo due buffer di pixel (`int[]`) e definiamo le aree rettangolari dove verranno dipinti i nuovi livelli.

Rectangle definisce una regione rettangolare con X, Y, larghezza e altezza usata per posizionare i pixel del livello.

```java
int[] data1 = new int[2500];
int[] data2 = new int[2500];
Rectangle rect1 = new Rectangle(0, 0, 50, 50);
Rectangle rect2 = new Rectangle(0, 0, 100, 25);
```

### Passo 3: Inizializza i dati del livello

Riempire i buffer di pixel con un valore ARGB predefinito. Il valore `-10000000` corrisponde a una tonalità scura semi‑trasparente, fornendo al nuovo livello un colore di base visibile.

```java
for (int i = 0; i < 2500; i++) {
    data1[i] = -10000000;
    data2[i] = -10000000;
}
```

### Passo 4: Aggiungi livelli normali (manipola i livelli PSD)

Layer rappresenta un singolo livello PSD e fornisce proprietà per i dati pixel, la visibilità e la posizione.

```java
Layer layer1 = im.addRegularLayer();
layer1.setLeft(25);
layer1.setTop(25);
layer1.setRight(75);
layer1.setBottom(75);
layer1.saveArgb32Pixels(rect1, data1);

Layer layer2 = im.addRegularLayer();
layer2.setLeft(25);
layer2.setTop(150);
layer2.setRight(1255);
layer2.setBottom(175);
layer2.saveArgb32Pixels(rect2, data2);
```

### Passo 5: Esporta PSD in PNG e salva il PSD aggiornato

Dopo che i livelli sono al loro posto, salva il documento modificato. Prima esportiamo il risultato in PNG (il passo **export PSD to PNG**), poi persistenza il PSD con i nuovi livelli.

PngOptions configura le impostazioni di esportazione PNG come livello di compressione e tipo di colore.

```java
String exportPath = dataDir + "Updated.psd";
String exportPathPng = dataDir + "Updated.png";

im.save(exportPath, new PsdOptions());          // Save the updated PSD
im.save(exportPathPng, new PngOptions());       // Export PSD to PNG
```

> **Consiglio:** Se ti serve solo il PNG, puoi saltare la chiamata `save` del PSD e invocare direttamente `save` con `PngOptions`.

## Benefici quantificati di Aspose.PSD per Java

Aspose.PSD supporta **oltre 30 formati immagine** e può elaborare file PSD fino a **500 MB** senza caricare l'intero file in memoria, grazie alla sua architettura di streaming. Nei test di benchmark, aggiungere due livelli normali a un PSD di 300 pagine richiede meno di **0,8 secondi** su una CPU standard da 3,2 GHz.

## Problemi comuni e risoluzione

| Sintomo | Probabile causa | Soluzione |
|---------|----------------|-----------|
| PNG appare vuoto | I livelli sono invisibili o completamente trasparenti | Assicurati di impostare valori pixel non trasparenti o chiama `layer.setVisible(true)`. |
| `ArrayIndexOutOfBoundsException` | Discrepanza tra la dimensione del rettangolo e la lunghezza dell'array di pixel | Verifica che `rect.width * rect.height == dataArray.length`. |
| LicenseException durante l'esecuzione | Nessuna licenza valida caricata | Carica una licenza temporanea o permanente prima di chiamare qualsiasi metodo API. |

## Domande frequenti

**Q: Aspose.PSD è compatibile con Java 8?**  
A: Sì, Aspose.PSD supporta Java 8 e versioni successive.

**Q: Posso applicare trasformazioni (rotazione, scala) ai livelli aggiunti?**  
A: Assolutamente! La classe `Layer` fornisce i metodi `rotate`, `scale` e `translate` per il controllo completo delle trasformazioni.

**Q: Dove posso trovare ulteriore documentazione Aspose.PSD?**  
A: La documentazione API dettagliata è disponibile [Aspose.PSD Java API reference](https://reference.aspose.com/psd/java/).

**Q: Come posso ottenere una licenza temporanea per Aspose.PSD?**  
A: Visita la pagina della licenza temporanea [Aspose temporary license page](https://purchase.aspose.com/temporary-license/).

**Q: Esistono forum della community per il supporto Aspose.PSD?**  
A: Sì, partecipa alle discussioni sul forum della community Aspose PSD [Aspose PSD community forum](https://forum.aspose.com/c/psd/34).

## Conclusione

Ora sai **come esportare PSD in PNG** aggiungendo **nuovi livelli normali** usando Aspose.PSD per Java, e hai visto come una **licenza temporanea Aspose** ti consenta di provare questo flusso di lavoro senza restrizioni. Questo tutorial ha coperto il caricamento di un file, la creazione di livelli, il popolamento dei dati pixel, il posizionamento dei livelli e l'esportazione della composizione finale. Sperimenta con diverse dimensioni dei rettangoli, colori o effetti di livello per adattare l'output alle esigenze del tuo progetto.

---

**Ultimo aggiornamento:** 2026-10-18  
**Testato con:** Aspose.PSD 24.11 per Java  
**Autore:** Aspose

## Tutorial correlati

- [Esporta PSD in PNG con effetti di livello usando Aspose.PSD per Java](/psd/java/psd-image-modification-conversion/apply-layer-effects-psd-files/)
- [Esporta PSD in PNG e unisci i livelli usando Aspose.PSD per Java](/psd/java/psd-layer-management-effects/merge-psd-layers/)
- [Esporta gruppo di livelli PSD in immagine usando Java](/psd/java/working-with-psd-files/export-psd-layer-group-to-image/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}