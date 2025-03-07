---
title: Aggiungi un nuovo livello regolare a PSD con Aspose.PSD per Java
linktitle: Aggiungi un nuovo livello regolare a PSD
second_title: API Java Aspose.PSD
description: Scopri come aggiungere un nuovo livello regolare ai file PSD utilizzando Aspose.PSD per Java. Segui la nostra guida passo passo per una manipolazione PSD senza soluzione di continuità.
weight: 11
url: /it/java/advanced-image-effects/add-new-regular-layer/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aggiungi un nuovo livello regolare a PSD con Aspose.PSD per Java

## Introduzione

Benvenuti in questo tutorial completo sull'utilizzo di Aspose.PSD per Java per aggiungere un nuovo livello regolare a un file PSD. Aspose.PSD è una potente libreria Java che consente agli sviluppatori di manipolare e lavorare in modo efficiente con i file PSD. In questo tutorial ti guideremo attraverso il processo di aggiunta di un nuovo livello regolare a un file PSD, fornendo passaggi dettagliati ed esempi di codice.

## Prerequisiti

Prima di immergerti nel tutorial, assicurati di avere i seguenti prerequisiti:

- Ambiente di sviluppo Java: assicurati di avere un ambiente di sviluppo Java configurato sul tuo sistema.
-  Libreria Aspose.PSD: scarica e installa la libreria Aspose.PSD per Java. Puoi trovare la biblioteca[Qui](https://releases.aspose.com/psd/java/).

## Importa pacchetti

Per iniziare, importa i pacchetti necessari nel tuo progetto Java. Questi pacchetti sono essenziali per lavorare con le funzionalità Aspose.PSD. Includi le seguenti righe all'inizio del tuo file Java:

```java
import com.aspose.psd.Image;
import com.aspose.psd.Rectangle;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.Layer;
import com.aspose.psd.imageoptions.PngOptions;
import com.aspose.psd.imageoptions.PsdOptions;
```

## Passaggio 1: carica il file PSD

Carica il file PSD che desideri modificare utilizzando il seguente codice:

```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "OneLayer.psd";
PsdImage im = (PsdImage)Image.load(sourceFileName);
```

## Passaggio 2: preparare matrici di dati e rettangoli

Preparare due array int e due oggetti Rectangle come segue:

```java
int[] data1 = new int[2500];
int[] data2 = new int[2500];
Rectangle rect1 = new Rectangle(0, 0, 50, 50);
Rectangle rect2 = new Rectangle(0, 0, 100, 25);
```

## Passaggio 3: inizializzare i dati del livello

Inizializza gli array di dati con un valore predefinito:

```java
for (int i = 0; i < 2500; i++) {
    data1[i] = -10000000;
    data2[i] = -10000000;
}
```

## Passaggio 4: aggiungi livelli regolari

Aggiungi due livelli regolari all'immagine PSD:

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

## Passaggio 5: salva PSD e PNG

Salva il PSD modificato e un file PNG aggiuntivo:

```java
im.save(exportPath, new PsdOptions());
im.save(exportPathPng, new PngOptions());
```

Congratulazioni! Hai aggiunto con successo un nuovo livello regolare a un file PSD utilizzando Aspose.PSD per Java.

## Conclusione

In questo tutorial, abbiamo trattato il processo di aggiunta di un nuovo livello regolare a un file PSD utilizzando Aspose.PSD per Java. Questa potente libreria semplifica la manipolazione di PSD, rendendolo accessibile agli sviluppatori Java. Sperimenta diversi parametri e funzionalità per esplorare tutto il potenziale di Aspose.PSD.

## Domande frequenti

### Q1: Aspose.PSD è compatibile con Java 8?

A1: Sì, Aspose.PSD supporta Java 8 e versioni successive.

### Q2: Posso applicare trasformazioni ai livelli aggiunti?

A2: Assolutamente! Aspose.PSD fornisce una gamma di opzioni di trasformazione per i livelli.

### Q3: Dove posso trovare ulteriore documentazione Aspose.PSD?

 R3: È possibile fare riferimento alla documentazione[Qui](https://reference.aspose.com/psd/java/).

### Q4: Come posso ottenere una licenza temporanea per Aspose.PSD?

 A4: Visita[questo collegamento](https://purchase.aspose.com/temporary-license/) per le opzioni di licenza temporanea.

### Q5: Esistono forum della community per il supporto di Aspose.PSD?

 A5: Sì, puoi trovare supporto e discussioni[Qui](https://forum.aspose.com/c/psd/34).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
