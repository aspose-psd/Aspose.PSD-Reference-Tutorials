---
date: 2026-01-14
description: Scopri come creare un livello di contorno sfumato e personalizzare i
  gradienti del contorno nei file PSD usando Aspose.PSD per Java con questo tutorial
  passo‑passo.
linktitle: How to Create Gradient Stroke Layer in Java
second_title: Aspose.PSD Java API
title: Come creare un livello di tratto sfumato in Java
url: /it/java/java-graphics-drawing/add-stroke-layer-gradient/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Come creare un livello di tratto sfumato in Java

## Introduzione
Ti sei mai chiesto come **creare un livello di tratto sfumato** nei tuoi file PSD usando Java? Sei nel posto giusto! Oggi approfondiremo Aspose.PSD per Java, una libreria potente che ti consente di manipolare i file PSD senza sforzo. Che tu sia nuovo alla programmazione grafica o desideri perfezionare design esistenti, questa guida ti accompagnerà passo passo nell'aggiungere e personalizzare i gradienti di tratto.

## Risposte rapide
- **Qual è l'obiettivo principale?** Creare un livello di tratto sfumato su un file PSD.  
- **Quale libreria è necessaria?** Aspose.PSD per Java.  
- **È necessaria una licenza?** Sì, è richiesta una licenza valida (o temporanea) per la produzione.  
- **Quale versione di Java funziona?** Java 8 o superiore.  
- **Quanto tempo richiede l'implementazione?** Circa 10‑15 minuti per un tratto sfumato di base.

## Che cos'è un livello di tratto sfumato?
Un livello di tratto sfumato è un contorno vettoriale attorno a una forma o a del testo che passa gradualmente da un colore all'altro. Con Aspose.PSD è possibile defin programmaticamente i colori, l'opacità, l'angolo e il tipo (lineare, radiale, ecc.) del tratto.

## Perché usare Aspose.PSD per Java?
- **Supporto completo PSD** – leggi, modifica e scrivi file PSD senza Photoshop.  
- **API ricca di effetti** – accedi a tratto, ombra, bagliore e molti altri effetti di livello.  
- **Cross‑platform** – funziona su qualsiasi OS che supporta Java.  
- **Nessuna dipendenza nativa** – puro Java, facile da integrare nei pipeline CI.

## Prerequisiti
1. **Java Development Kit (JDK)** – Installa l'ultima versione del JDK dal [sito di Oracle](https://www.oracle.com/java/technologies/javase-downloads.html).  
2. **Aspose.PSD per Java** – Scarica la libreria dalla [pagina di download di Aspose.PSD](https://releases.aspose.com/psd/java/).  
3. **IDE** – IntelliJ IDEA, Eclipse o NetBeans.  
4. **Licenza** – Ottieni una [licenza temporanea](https://purchase.aspose.com/temporary-license/) se non possiedi una licenza completa.

## Importare i pacchetti
Per prima cosa, importa le classi necessarie per caricare il PSD, accedere agli effetti e configurare i riempimenti gradienti.

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

Ora suddividiamo il processo in passaggi chiari.

## Passo 1: Caricare il file PSD
Carichiamo il PSD di origine e abilitiamo le risorse degli effetti affinché il tratto sia disponibile.

```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "Stroke.psd";
String exportPath = dataDir + "StrokeGradientChanged.psd";
PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);
PsdImage im = (PsdImage) Image.load(sourceFileName, loadOptions);
```

## Passo : Accedere all'effetto Stroke
Supponendo che il tratto da modificare appartenga al terzo livello (indice 2), recuperiamo il suo `StrokeEffect`.

```java
StrokeEffect gradientStroke = (StrokeEffect) im.getLayers()[2].getBlendingOptions().getEffects()[0];
```

## Passo 3: Verificare le proprietà dell'effetto Stroke
Prima di apportare modifiche, confermiamo le impostazioni esistenti così da sapere esattamente cosa stiamo aggiornando.

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

## Passo 4: Modificare le impostazioni del riempimento gradiente
Qui cambiamo colore, opacità, modalità di fusione e altre proprietà per ottenere l'aspetto desiderato.

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

## Passo 5: Aggiungere e modificare i punti di colore e trasparenza
Aggiungiamo nuovi punti di colore e trasparenza, poi regoliamo quelli esistenti per modellare il gradiente.

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

## Passo 6: Salvare il file PSD modificato
Dopo tutti gli aggiustamenti, scriviamo il file aggiornato su disco.

```java
im.save(exportPath);
```

## Passo 7: Verificare le modifiche
Carichiamo il file salvato e verifichiamo che ogni proprietà rifletta le modifiche applicate.

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
Assert.areEqual(50, transparencyPoint.getMedianPointLocation());
Assert.areEqual(100, transparencyPoint.getOpacity());
Assert.areEqual(2411, transparencyPoint.getLocation());
transparencyPoint1 = fillSettings.getTransparencyPoints()[2];
Assert.areEqual(25, transparencyPoint.getMedianPointLocation());
Assert.areEqual(25, transparencyPoint.getOpacity());
Assert.areEqual(4096, transparencyPoint.getLocation());
```

## Conclusione
Ora sai come **creare un livello di tratto sfumato** nei file PSD usando Aspose.PSD per Java. Caricando un PSD, accedendo all'effetto Stroke, regolando le impostazioni del riempimento gradiente e salvando il risultato, puoi produrre grafiche di livello professionale in modo programmatico senza mai aprire Photoshop.

## FAQ
### Che cos'è Aspose.PSD per Java?
Aspose.PSD per Java è una libreria che consente agli sviluppatori di lavorare con file PSD in applicazioni Java, offrendo funzionalità per creare, manipolare e convertire file PSD.

### È necessaria una licenza per usare Aspose.PSD per Java?
Sì,aria una licenza valida per usare Aspose.PSD per Java. Puoi ottenere una [licenza temporanea](https://purchase.aspose.com/temporary-license/) per scopi di valutazione.

### Posso usare Aspose.PSD per Java per creare file PSD da zero?
Assolutamente! Aspose.PSD per Java fornisce API complete per creare e manipolare file PSD programmaticamente.

### È possibile applicare altri effetti usando Aspose.PSD per Java?
Sì, puoi applicare vari effetti come ombra, bagliore e molti altri usando Aspose.PSD per Java.

### Dove posso trovare la documentazione per Aspose.PSD per Java?
Puoi trovare la documentazione [qui](https://reference.aspose.com/psd/java/).

---

**Ultimo aggiornamento:** 2026-01-14  
**Testato con:** Aspose.PSD per Java 24.11  
**Autore:** Aspose

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
