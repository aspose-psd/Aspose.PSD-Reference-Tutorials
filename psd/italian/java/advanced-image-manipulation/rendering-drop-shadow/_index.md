---
title: Applica l'ombra esterna del rendering in Aspose.PSD per Java
linktitle: Applica l'ombra esterna del rendering
second_title: API Java Aspose.PSD
description: Esplora la guida passo passo per applicare il rendering delle ombre esterne in Aspose.PSD per Java, migliorando le tue capacità di elaborazione delle immagini senza sforzo.
type: docs
weight: 16
url: /it/java/advanced-image-manipulation/rendering-drop-shadow/
---
## Introduzione

Se ti stai immergendo nell'elaborazione delle immagini con Java, Aspose.PSD è il tuo strumento di riferimento per una manipolazione fluida ed efficiente dei file PSD. In questo tutorial, esploreremo il processo di applicazione di un'ombra esterna di rendering utilizzando Aspose.PSD per Java. Allacciate le cinture, mentre analizziamo i passaggi per voi.

## Prerequisiti

Prima di intraprendere questo viaggio, assicurati di possedere i seguenti prerequisiti:

- Ambiente di sviluppo Java: assicurati di avere Java installato sul tuo computer.
- Libreria Aspose.PSD: scarica e configura la libreria Aspose.PSD. Puoi trovare la biblioteca[Qui](https://releases.aspose.com/psd/java/).
- File PSD: prepara un file PSD contenente il livello su cui desideri applicare l'ombra esterna.

## Importa pacchetti

Cominciamo importando i pacchetti necessari. Questo passaggio garantisce di avere a disposizione gli strumenti essenziali per un'esecuzione fluida del codice.

```java
import com.aspose.psd.Image;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.layereffects.DropShadowEffect;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
import com.aspose.psd.Color;

import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.imageoptions.PngOptions;
```

Ora analizziamo ogni passaggio.

## Passaggio 1: definire la directory dei documenti

Inizia specificando la directory in cui si trova il tuo file PSD.

```java
String dataDir = "Your Document Directory";
```

## Passaggio 2: imposta i percorsi dei file PSD e PNG

Definisci i percorsi per il file PSD di origine e il file PNG di destinazione.

```java
String sourceFileName = dataDir + "Shadow.psd";
String pngExportPath = dataDir + "Shadowchanged1.png";
```

## Passaggio 3: carica il file PSD con effetti

Carica il file PSD, abilitando il caricamento delle risorse degli effetti.

```java
PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);

PsdImage im = (PsdImage) Image.load(sourceFileName, loadOptions);
```

## Passaggio 4: accedi all'effetto ombra esterna

Recupera l'effetto ombra esterna dal livello specificato.

```java
DropShadowEffect shadowEffect = (DropShadowEffect) (im.getLayers()[1].getBlendingOptions().getEffects()[0]);
```

## Passaggio 5: convalida delle proprietà dell'effetto ombra

Assicurati che le proprietà dell'effetto ombra esterna soddisfino le tue aspettative.

```java
Assert.areEqual(Color.getBlack(), shadowEffect.getColor());
Assert.areEqual(255, shadowEffect.getOpacity());
Assert.areEqual(3, shadowEffect.getDistance());
Assert.areEqual(7, shadowEffect.getSize());
Assert.areEqual(true, shadowEffect.getUseGlobalLight());
Assert.areEqual(90, shadowEffect.getAngle());
Assert.areEqual(0, shadowEffect.getSpread());
Assert.areEqual(0, shadowEffect.getNoise());
```

## Passaggio 6: salva come PNG

Salva l'immagine modificata come file PNG.

```java
PngOptions saveOptions = new PngOptions();
saveOptions.setColorType(PngColorType.TruecolorWithAlpha);
im.save(pngExportPath, saveOptions);
```

Ed eccola qua: una guida passo passo per applicare il rendering delle ombre esterne in Aspose.PSD per Java.

## Conclusione

Padroneggiare la manipolazione delle immagini in Java diventa un gioco da ragazzi con Aspose.PSD. Hai appena svelato i segreti per il rendering delle ombre esterne, aprendo un mondo di possibilità creative.

## Domande frequenti

### Q1: Posso applicare ombre esterne a più livelli contemporaneamente?

R1: Sì, puoi scorrere i livelli e applicare ombre esterne secondo necessità.

### Q2: Qual è il significato del parametro 'Diffusione' nelle ombre esterne?

A2: Il parametro 'Spread' controlla la transizione tra le aree d'ombra e quelle non d'ombra.

### Q3: Aspose.PSD è compatibile con tutte le versioni dei file Photoshop?

A3: Aspose.PSD fornisce compatibilità con un'ampia gamma di versioni di file PSD, garantendo versatilità.

### Q4: Come posso segnalare problemi o chiedere assistenza con Aspose.PSD?

 A4: Vai al[Forum Aspose.PSD](https://forum.aspose.com/c/psd/34) per un supporto completo.

### Q5: Posso testare Aspose.PSD prima di effettuare un acquisto?

 A5: Assolutamente, usa il file[prova gratuita](https://releases.aspose.com/) esplorare le funzionalità prima di impegnarsi in un acquisto.