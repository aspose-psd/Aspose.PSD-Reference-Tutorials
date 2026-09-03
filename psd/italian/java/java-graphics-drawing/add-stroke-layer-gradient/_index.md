---
date: 2026-09-03
description: Scopri come creare gradient stroke java e personalizzare stroke gradients
  nei file PSD usando Aspose.PSD per Java. Guida passo‑passo per gli sviluppatori.
keywords:
- create gradient stroke java
- add gradient stroke psd
- Aspose.PSD Java
- PSD gradient stroke
lastmod: 2026-09-03
linktitle: Come creare Gradient Stroke Layer in Java
og_description: Crea gradient stroke java con Aspose.PSD per Java in pochi minuti.
  Questo tutorial mostra come aggiungere e personalizzare gradient strokes nei file
  PSD, completo di code snippets e best practices.
og_image_alt: Screenshot of a PSD file showing a gradient stroke applied via Aspose.PSD
  Java API
og_title: Crea gradient stroke java – Guida tutorial Aspose.PSD
schemas:
- author: Aspose
  dateModified: '2026-09-03'
  description: Learn how to create gradient stroke java and customize stroke gradients
    in PSD files using Aspose.PSD for Java. Step‑by‑step guide for developers.
  headline: Create gradient stroke java – Aspose.PSD tutorial guide
  type: TechArticle
- description: Learn how to create gradient stroke java and customize stroke gradients
    in PSD files using Aspose.PSD for Java. Step‑by‑step guide for developers.
  name: Create gradient stroke java – Aspose.PSD tutorial guide
  steps:
  - name: '**Java Development Kit (JDK)** – Install the latest JDK from [Oracle''s
      website](https://www.oracle.com/java/technologies/javase-downloads.html).'
    text: '**Java Development Kit (JDK)** – Install the latest JDK from [Oracle''s
      website](https://www.oracle.com/java/technologies/javase-downloads.html).'
  - name: '**Aspose.PSD for Java** – Download the library from the [Aspose.PSD download
      page](https://releases.aspose.com/psd/java/).'
    text: '**Aspose.PSD for Java** – Download the library from the [Aspose.PSD download
      page](https://releases.aspose.com/psd/java/).'
  - name: '**IDE** – IntelliJ IDEA, Eclipse, or NetBeans.'
    text: '**IDE** – IntelliJ IDEA, Eclipse, or NetBeans.'
  - name: '**License** – Obtain a [temporary license](https://purchase.aspose.com/temporary-license/)
      if you don’t have a full commercial license.'
    text: '**License** – Obtain a [temporary license](https://purchase.aspose.com/temporary-license/)
      if you don’t have a full commercial license.'
  type: HowTo
- questions:
  - answer: Aspose.PSD for Java is a pure‑Java library that lets developers create,
      edit, convert, and render Photoshop PSD files without requiring Adobe Photoshop.
    question: What is Aspose.PSD for Java?
  - answer: Yes, a valid license is required for production use. You can obtain a
      [temporary license](https://purchase.aspose.com/temporary-license/) for evaluation.
    question: Do I need a license to use Aspose.PSD for Java?
  - answer: Absolutely. Aspose.PSD provides APIs to build a new PSD document, add
      layers, apply effects, and save the file entirely programmatically.
    question: Can I create PSD files from scratch with this library?
  - answer: Yes, you can apply shadows, glows, bevels, and many other layer effects
      using the same effect‑based API.
    question: Is it possible to apply other effects besides gradient strokes?
  - answer: The official documentation is available in the [Aspose.PSD Java API reference](https://reference.aspose.com/psd/java/).
    question: Where can I find the full reference documentation?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- gradient stroke
- Aspose.PSD
- Java graphics
title: Crea gradient stroke java – Guida tutorial Aspose.PSD
url: /it/java/java-graphics-drawing/add-stroke-layer-gradient/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Come creare un contorno gradiente java con Aspose.PSD

## Introduzione
Se hai bisogno di **create gradient stroke java** effetti senza aprire Photoshop, sei nel posto giusto. In questo tutorial imparerai a utilizzare Aspose.PSD per Java — una libreria pure‑Java che ti offre il pieno controllo programmatico sui file PSD. Vedremo come caricare un PSD, accedere all'effetto di contorno di un livello, configurare un riempimento gradiente e infine salvare il risultato. Alla fine sarai in grado di aggiungere contorni gradiente di livello professionale a forme o testo in poche righe di codice.

## Risposte rapide
- **Qual è l'obiettivo principale?** Creare un livello di contorno gradiente su un file PSD usando Java.  
- **Quale libreria fornisce l'API?** Aspose.PSD per Java (supporta Java 8 +).  
- **È necessaria una licenza per la produzione?** Sì – è richiesta una licenza valida o temporanea.  
- **Quanto tempo richiede un'implementazione di base?** Circa 10‑15 minuti per un semplice contorno.  
- **Posso personalizzare il tipo di gradiente?** Assolutamente – i gradienti lineari, radiali e basati sull'angolo sono tutti supportati.

## Cos'è un livello di contorno gradiente?
Un livello di contorno gradiente è un contorno vettoriale il cui colore passa gradualmente da una tonalità all'altra. Può essere applicato a forme, testo o a qualsiasi maschera vettoriale all'interno di un file PSD, offrendo ai designer un effetto visivo dinamico senza rasterizzare l'opera.

## Perché usare Aspose.PSD per Java?
Aspose.PSD per Java fornisce **supporto completo per PSD** per più di 100 funzionalità — inclusi livelli, maschere, livelli di regolazione e effetti di livello — e può elaborare file fino a 2 GB senza caricare l'intero documento in memoria. La libreria funziona su qualsiasi sistema operativo che supporti Java, non ha dipendenze native e viene aggiornata mensilmente per rimanere compatibile con le ultime specifiche dei file Photoshop.

## Prerequisiti
1. **Java Development Kit (JDK)** – Installa l'ultima versione del JDK dal [sito di Oracle](https://www.oracle.com/java/technologies/javase-downloads.html).  
2. **Aspose.PSD per Java** – Scarica la libreria dalla [pagina di download di Aspose.PSD](https://releases.aspose.com/psd/java/).  
3. **IDE** – IntelliJ IDEA, Eclipse o NetBeans.  
4. **Licenza** – Ottieni una [licenza temporanea](https://purchase.aspose.com/temporary-license/) se non possiedi una licenza commerciale completa.

## Importa i pacchetti
Le istruzioni `import` portano le classi necessarie nello scope.  

```text
```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;
import com.aspose.psd.examples.Utils.Assert;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.BlendMode;
import com.aspose.psd.fileformats.psd.layers.IGradientColorPoint;
import com.aspose.psd.fileformats.psd.layers.fillsettings.FillType;
import com.aspose.psd.fileformats.psd.layers.fillsettings.GradientColorPoint;
import com.aspose.psd.fileformats.psd.layers.fillsettings.GradientFillSettings;
import com.aspose.psd.fileformats.psd.layers.fillsettings.GradientTransparencyPoint;
import com.aspose.psd.fileformats.psd.layers.fillsettings.GradientType;
import com.aspose.psd.fileformats.psd.layers.fillsettings.IGradientTransparencyPoint;
import com.aspose.psd.fileformats.psd.layers.layereffects.StrokeEffect;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
```
```

Ora suddividiamo il processo in passaggi chiari.

## Passo 1: Carica il file PSD
Caricare il file sorgente è il primo passo; è necessario abilitare le risorse degli effetti affinché le informazioni sul contorno siano disponibili per la modifica. **PsdLoadOptions** configura il modo in cui un file PSD viene caricato, consentendo di abilitare o disabilitare risorse specifiche.  

```text
```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "Stroke.psd";
String exportPath = dataDir + "StrokeGradientChanged.psd";
PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);
PsdImage im = (PsdImage) Image.load(sourceFileName, loadOptions);
```
```

## Passo 2: Accedi all'effetto di contorno
**StrokeEffect** rappresenta lo stile del contorno applicato a un livello, includendo larghezza, colore e riempimento gradiente.  

```text
```java
StrokeEffect gradientStroke = (StrokeEffect) im.getLayers()[2].getBlendingOptions().getEffects()[0];
```
```

## Passo 3: Verifica le proprietà dell'effetto di contorno
Prima di modificare qualsiasi cosa, è buona pratica leggere le proprietà esistenti. Questo ti aiuta a comprendere la configurazione corrente ed evitare di sovrascrivere impostazioni importanti. **GradientFillSettings** contiene la configurazione del riempimento gradiente per un effetto di contorno.  

```text
```java
Assert.areEqual(BlendMode.Normal, gradientStroke.getBlendMode());
Assert.areEqual(255, gradientStroke.getOpacity());
Assert.areEqual(true, gradientStroke.isVisible());
GradientFillSettings fillSettings = (GradientFillSettings) gradientStroke.getFillSettings();
Assert.areEqual(Color.getBlack(), fillSettings.getColor());
Assert.areEqual(FillType.Gradient, fillSettings.getFillType());
Assert.areEqual(true, fillSettings.getAlignWithLayer());
Assert.areEqual(GradientType.Linear, fillSettings.getGradientType());
Assert.isTrue(Math.abs(90 - fillSettings.getAngle()) < 0.001, "Angle is incorrect");
Assert.areEqual(false, fillSettings.getDither());
Assert.isTrue(Math.abs(0 - fillSettings.getHorizontalOffset()) < 0.001, "Horizontal offset is incorrect");
Assert.isTrue(Math.abs(0 - fillSettings.getVerticalOffset()) < 0.001, "Vertical offset is incorrect");
Assert.areEqual(false, fillSettings.getReverse());
```
```

## Passo 4: Modifica le impostazioni del riempimento gradiente
`GradientFill` definisce come i colori passano attraverso il contorno. Puoi cambiarne il tipo (lineare, radiale), l'angolo e il blend mode, quindi assegnare nuovi punti di colore e trasparenza.  

```text
```java
fillSettings.setColor(Color.getGreen());
gradientStroke.setOpacity((byte) 127);
gradientStroke.setBlendMode(BlendMode.Color);
fillSettings.setAlignWithLayer(false);
fillSettings.setGradientType(GradientType.Radial);
fillSettings.setAngle(45);
fillSettings.setDither(true);
fillSettings.setHorizontalOffset(15);
fillSettings.setVerticalOffset(11);
fillSettings.setReverse(true);
```
```

## Passo 5: Aggiungi e modifica i punti di colore e trasparenza
Un gradiente è costruito da una serie di punti di arresto di colore e di opacità. **GradientColorPoint** definisce un punto di colore in un gradiente, specificandone il colore e la posizione. **GradientTransparencyPoint** definisce un punto di opacità in un gradiente, specificandone l'opacità e la posizione. Aggiungere o regolare questi punti ti permette di modellare il flusso visivo del contorno.  

```text
```java
// Add new color point
GradientColorPoint colorPoint = fillSettings.addColorPoint();
colorPoint.setColor(Color.getGreen());
colorPoint.setLocation(4096);
colorPoint.setMedianPointLocation(75);
// Change location of previous point
fillSettings.getColorPoints()[1].setLocation(1899);
// Add new transparency point
GradientTransparencyPoint transparencyPoint = fillSettings.addTransparencyPoint();
transparencyPoint.setOpacity(25);
transparencyPoint.setMedianPointLocation(25);
transparencyPoint.setLocation(4096);
// Change location of previous transparency point
fillSettings.getTransparencyPoints()[1].setLocation(2411);
```
```

## Passo 6: Salva il file PSD modificato
Dopo tutte le regolazioni, scrivi il documento aggiornato su disco. Aspose.PSD preserva automaticamente tutti gli altri livelli e risorse.  

```text
```java
im.save(exportPath);
```
```

## Passo 7: Verifica le modifiche
Ricarica il file salvato e verifica che le proprietà del gradiente del contorno corrispondano ai valori impostati. Questo passaggio di verifica è essenziale per pipeline automatizzate. **Assert** fornisce semplici asserzioni di test per verificare le condizioni durante l'esecuzione.  

```text
```java
PsdImage img = (PsdImage) Image.load(exportPath, loadOptions);
StrokeEffect gradientStrokeEffect = (StrokeEffect) img.getLayers()[2].getBlendingOptions().getEffects()[0];
Assert.areEqual(BlendMode.Color, gradientStrokeEffect.getBlendMode());
Assert.areEqual(127, gradientStrokeEffect.getOpacity());
Assert.areEqual(true, gradientStrokeEffect.isVisible());
GradientFillSettings fillSetting = (GradientFillSettings) gradientStrokeEffect.getFillSettings();
Assert.areEqual(Color.getGreen(), fillSetting.getColor());
Assert.areEqual(FillType.Gradient, fillSetting.getFillType());
// Check color points
Assert.areEqual(3, fillSetting.getColorPoints().length);
IGradientColorPoint point = fillSetting.getColorPoints()[0];
Assert.areEqual(50, point.getMedianPointLocation());
Assert.areEqual(Color.getBlack(), point.getColor());
Assert.areEqual(0, point.getLocation());
point = fillSettings.getColorPoints()[1];
Assert.areEqual(50, point.getMedianPointLocation());
Assert.areEqual(Color.getWhite(), point.getColor());
Assert.areEqual(1899, point.getLocation());
point = fillSettings.getColorPoints()[2];
Assert.areEqual(75, point.getMedianPointLocation());
Assert.areEqual(Color.getGreen(), point.getColor());
Assert.areEqual(4096, point.getLocation());
// Check transparency points
Assert.areEqual(3, fillSettings.getTransparencyPoints().length);
IGradientTransparencyPoint transparencyPoint1 = fillSettings.getTransparencyPoints()[0];
Assert.areEqual(50, transparencyPoint1.getMedianPointLocation());
Assert.areEqual(100, transparencyPoint1.getOpacity());
Assert.areEqual(0, transparencyPoint1.getLocation());
transparencyPoint1 = fillSettings.getTransparencyPoints()[1];
Assert.areEqual(50, transparencyPoint1.getMedianPointLocation());
Assert.areEqual(100, transparencyPoint1.getOpacity());
Assert.areEqual(2411, transparencyPoint1.getLocation());
transparencyPoint1 = fillSettings.getTransparencyPoints()[2];
Assert.areEqual(25, transparencyPoint1.getMedianPointLocation());
Assert.areEqual(25, transparencyPoint1.getOpacity());
Assert.areEqual(4096, transparencyPoint1.getLocation());
```
```

## Problemi comuni e suggerimenti per la risoluzione
- **Errore di licenza mancante** – Se visualizzi un'eccezione di licenza, verifica che il file di licenza temporanea sia caricato correttamente prima di qualsiasi chiamata API.  
- **Gradiente non visibile** – Assicurati che il flag `strokeEnabled` del livello di destinazione sia impostato su `true`; altrimenti l'effetto viene ignorato durante il rendering.  
- **Prestazioni su file di grandi dimensioni** – Per PSD superiori a 500 MB, considera l'uso di `PsdImage.load(..., LoadOptions)` con `loadResources = false` e abilita solo le risorse necessarie.

## Domande frequenti

**D: Cos'è Aspose.PSD per Java?**  
**R:** Aspose.PSD per Java è una libreria pure‑Java che consente agli sviluppatori di creare, modificare, convertire e renderizzare file Photoshop PSD senza richiedere Adobe Photoshop.

**D: È necessaria una licenza per usare Aspose.PSD per Java?**  
**R:** Sì, è richiesta una licenza valida per l'uso in produzione. È possibile ottenere una [licenza temporanea](https://purchase.aspose.com/temporary-license/) per la valutazione.

**D: Posso creare file PSD da zero con questa libreria?**  
**R:** Assolutamente. Aspose.PSD fornisce API per costruire un nuovo documento PSD, aggiungere livelli, applicare effetti e salvare il file interamente in modo programmatico.

**D: È possibile applicare altri effetti oltre ai contorni gradiente?**  
**R:** Sì, è possibile applicare ombre, bagliori, smussi e molti altri effetti di livello usando la stessa API basata sugli effetti.

**D: Dove posso trovare la documentazione completa di riferimento?**  
**R:** La documentazione ufficiale è disponibile nella [riferimento API di Aspose.PSD Java](https://reference.aspose.com/psd/java/).

## Conclusione
Ora disponi di una soluzione completa, end‑to‑end, per **create gradient stroke java** effetti nei file PSD usando Aspose.PSD. Caricando un PSD, accedendo all'effetto di contorno, configurando un riempimento gradiente e salvando il file, puoi automatizzare flussi di lavoro grafici sofisticati che altrimenti richiederebbero lavoro manuale in Photoshop. Sperimenta con diversi tipi di gradiente, blend mode e punti di opacità per ottenere l'aspetto esatto di cui ha bisogno la tua applicazione.

---

**Ultimo aggiornamento:** 2026-09-03  
**Testato con:** Aspose.PSD per Java 24.11  
**Autore:** Aspose

## Tutorial correlati

- [Crea riempimento gradiente PSD con Java usando Aspose.PSD – Aggiungi livello di riempimento gradiente](/psd/java/psd-image-modification-conversion/add-gradient-fill-layer-psd-files/)
- [Come creare effetti di gradiente radiale in Aspose.PSD per Java](/psd/java/advanced-image-effects/add-gradient-effects/)
- [Come cambiare il colore del contorno Java usando Aspose.PSD](/psd/java/advanced-image-effects/add-stroke-layer-color/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}