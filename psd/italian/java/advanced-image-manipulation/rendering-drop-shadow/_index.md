---
date: 2025-12-05
description: Scopri come salvare PSD come PNG, convertire PSD in PNG e applicare un
  livello di ombra esterna usando Aspose.PSD per Java – una guida completa, passo
  dopo passo.
linktitle: Apply Rendering Drop Shadow
second_title: Aspose.PSD Java API
title: Salva PSD come PNG e applica l'ombra di rendering in Aspose.PSD per Java
url: /it/java/advanced-image-manipulation/rendering-drop-shadow/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Salva PSD come PNG e Applica Rendering Drop Shadow in Aspose.PSD per Java

## Introduzione

Se lavori con file Photoshop in Java, **salvare PSD come PNG** è una delle attività più comuni che incontrerai. Con Aspose.PSD non solo puoi **convertire PSD in PNG**, ma anche migliorare l'immagine **aggiungendo un livello di drop shadow**. In questo tutorial percorreremo l’intero processo—caricamento di un PSD, applicazione di un rendering drop shadow e infine **salvataggio del PSD come file PNG**—in modo da poter integrare il flusso di lavoro nei tuoi progetti con fiducia.

## Risposte Rapide
- **Quale libreria gestisce la conversione da PSD a PNG?** Aspose.PSD per Java.  
- **Quanto tempo richiede l’implementazione del drop‑shadow?** Circa 10‑15 minuti per un esempio base.  
- **È necessaria una licenza per eseguire il codice?** Una versione di prova gratuita è sufficiente per la valutazione; è richiesta una licenza per la produzione.  
- **Posso applicare l’ombra a più livelli?** Sì—basta iterare sui livelli desiderati.  
- **Quale versione di Java è richiesta?** Java 8 o superiore.

## Cos'è “salva PSD come PNG” e perché è importante

Salvare un PSD come PNG crea un’immagine senza perdita di qualità, ampiamente supportata, che conserva la trasparenza. Questo è essenziale quando devi visualizzare risorse Photoshop sul web, in app mobili o come parte di una pipeline di elaborazione immagini più ampia. Aggiungere un drop shadow nello stesso momento ti permette di ottenere un effetto visivo raffinato senza aprire Photoshop.

## Prerequisiti

Prima di iniziare, assicurati di avere:

- **Ambiente di sviluppo Java** – JDK 8 o più recente installato.  
- **Aspose.PSD per Java** – Scarica l’ultimo JAR dalla [pagina di download di Aspose.PSD](https://releases.aspose.com/psd/java/).  
- **Un file PSD** – Il file deve contenere almeno un livello a cui vuoi aggiungere il drop shadow (ad es., *Shadow.psd*).  

## Importa Pacchetti

Per prima cosa, importa le classi necessarie. Questo ti darà accesso al caricamento dell’immagine, agli effetti dei livelli e alle opzioni di esportazione PNG.

```java
import com.aspose.psd.Image;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.layereffects.DropShadowEffect;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
import com.aspose.psd.Color;

import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.imageoptions.PngOptions;
```

## Guida Passo‑Passo

### Passo 1: Definisci la Directory del Documento  
Indica al programma dove si trova il PSD di origine.

```java
String dataDir = "Your Document Directory";
```

### Passo 2: Imposta i Percorsi dei File PSD e PNG  
Specifica sia il PSD di input sia il PNG di output che conterrà il drop shadow renderizzato.

```java
String sourceFileName = dataDir + "Shadow.psd";
String pngExportPath = dataDir + "Shadowchanged1.png";
```

### Passo 3: Carica il File PSD con gli Effetti  
Abilita il caricamento delle risorse degli effetti così da poter manipolare l’effetto drop‑shadow.

```java
PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);

PsdImage im = (PsdImage) Image.load(sourceFileName, loadOptions);
```

### Passo 4: Accedi all'Effetto Drop Shadow  
Recupera il primo effetto drop‑shadow dal secondo livello (indice 1). Qui verificheremo o modificheremo i parametri.

```java
DropShadowEffect shadowEffect = (DropShadowEffect) (im.getLayers()[1].getBlendingOptions().getEffects()[0]);
```

### Passo 5: Convalida le Proprietà dell'Effetto Ombra  
Assicurati che le proprietà dell’effetto corrispondano a quanto ti aspetti prima di salvare. Puoi anche regolare questi valori per ottenere un aspetto diverso.

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

> **Suggerimento professionale:** Regola `setSpread()` o `setNoise()` per creare ombre più morbide o più testurizzate.

### Passo 6: Salva come PNG – il passo “salva PSD come PNG”  
Esporta l’immagine modificata in PNG, preservando il canale alfa affinché l’ombra si fonda correttamente.

```java
PngOptions saveOptions = new PngOptions();
saveOptions.setColorType(PngColorType.TruecolorWithAlpha);
im.save(pngExportPath, saveOptions);
```

A questo punto hai **convertito PSD in PNG** e applicato un rendering drop shadow in un unico flusso di lavoro.

## Problemi Comuni e Soluzioni

| Problema | Probabile Causa | Soluzione |
|----------|-----------------|-----------|
| **Ombra non visibile** | `Opacity` impostata a 0 o livello nascosto | Verifica che `shadowEffect.getOpacity()` sia > 0 e che la visibilità del livello sia attiva. |
| **PNG appare piatto (senza trasparenza)** | Tipo `PngColorType` errato | Usa `PngColorType.TruecolorWithAlpha` come mostrato. |
| **Eccezione durante il caricamento** | Effetti non caricati | Assicurati di chiamare `loadOptions.setLoadEffectsResource(true)`. |
| **Indice del livello errato** | Struttura del PSD diversa | Ispeziona `im.getLayers()` e scegli l’indice corretto. |

## Domande Frequenti

**D: Posso applicare drop shadow a più livelli contemporaneamente?**  
R: Sì. Itera su `im.getLayers()` e aggiungi o modifica un `DropShadowEffect` per ogni livello target.

**D: Cosa controlla il parametro ‘Spread’?**  
R: `Spread` determina quanto rapidamente l’ombra passa da piena opacità a trasparenza. Un valore più alto crea un bordo più netto.

**D: Aspose.PSD è compatibile con tutte le versioni di Photoshop?**  
R: Aspose.PSD supporta file PSD da Photoshop 3.0 fino all’ultima versione, gestendo la maggior parte dei tipi di livello e degli effetti.

**D: Come posso testare il codice prima di acquistare una licenza?**  
R: Scarica la versione di prova gratuita dalla [pagina di download di Aspose.PSD](https://releases.aspose.com/psd/java/) e esegui il campione senza chiave di licenza.

**D: Dove posso trovare aiuto se incontro problemi?**  
R: Pubblica la tua domanda sul [forum di Aspose.PSD](https://forum.aspose.com/c/psd/34) dove la community e gli ingegneri di Aspose possono assisterti.

## Conclusione

Ora sai come **salvare PSD come PNG**, **convertire PSD in PNG** e **applicare un livello di drop shadow** usando Aspose.PSD per Java. Questa combinazione ti consente di automatizzare la preparazione di immagini di alta qualità per web, mobile o applicazioni desktop—senza mai aprire Photoshop.

---

**Ultimo aggiornamento:** 2025-12-05  
**Testato con:** Aspose.PSD 24.11 per Java  
**Autore:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}