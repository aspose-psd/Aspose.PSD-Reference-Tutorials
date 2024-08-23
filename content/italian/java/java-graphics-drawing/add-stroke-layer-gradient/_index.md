---
title: Come aggiungere il gradiente del livello tratto in Java
linktitle: Come aggiungere il gradiente del livello tratto in Java
second_title: API Java Aspose.PSD
description: Scopri come aggiungere e personalizzare i gradienti del livello del tratto nei file PSD utilizzando Aspose.PSD per Java con questo tutorial completo passo passo.
type: docs
weight: 10
url: /it/java/java-graphics-drawing/add-stroke-layer-gradient/
---
## Introduzione
Ti sei mai chiesto come aggiungere un gradiente del livello del tratto alle tue immagini utilizzando Java? Bene, sei nel posto giusto! Oggi ci immergiamo nel mondo di Aspose.PSD per Java, una potente libreria che ti aiuta a manipolare facilmente i file PSD. Che tu sia un principiante o uno sviluppatore esperto, questa guida passo passo ti guiderà attraverso il processo di aggiunta di un gradiente del livello tratto ai tuoi file PSD. Quindi, allacciati le cinture e preparati a migliorare le tue capacità di editing grafico!
## Prerequisiti
Prima di iniziare, ci sono alcune cose che devi avere a posto. Assicurati di avere quanto segue:
1.  Java Development Kit (JDK): assicurati di avere JDK installato sul tuo sistema. Puoi scaricarlo da[Il sito web di Oracle](https://www.oracle.com/java/technologies/javase-downloads.html).
2.  Aspose.PSD per Java Library: puoi scaricarlo dal file[Pagina di download di Aspose.PSD](https://releases.aspose.com/psd/java/).
3. Un ambiente di sviluppo integrato (IDE): qualsiasi IDE come IntelliJ IDEA, Eclipse o NetBeans funzionerà.
4.  Una licenza valida: puoi ottenere a[licenza temporanea](https://purchase.aspose.com/temporary-license/) se non ne hai uno completo.
## Importa pacchetti
Per prima cosa importiamo i pacchetti necessari. Questi ci consentiranno di utilizzare le classi e i metodi richiesti per manipolare il file PSD.
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
Ora suddividiamo l'esempio in più passaggi per una migliore comprensione.
## Passaggio 1: carica il file PSD
 Per prima cosa dobbiamo caricare il file PSD che vogliamo modificare. Utilizzeremo il`PsdLoadOptions` per specificare che vogliamo caricare le risorse degli effetti.
```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "Stroke.psd";
String exportPath = dataDir + "StrokeGradientChanged.psd";
PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);
PsdImage im = (PsdImage) Image.load(sourceFileName, loadOptions);
```
## Passaggio 2: accedi all'effetto tratto
Successivamente, dobbiamo accedere all'effetto tratto del livello che ci interessa. Qui assumiamo che sia il terzo livello (indice 2) nel file PSD.
```java
StrokeEffect gradientStroke = (StrokeEffect) im.getLayers()[2].getBlendingOptions().getEffects()[0];
```
## Passaggio 3: verificare le proprietà dell'effetto tratto
Prima di apportare qualsiasi modifica, verifichiamo le proprietà dell'effetto tratto per assicurarci di modificare le impostazioni corrette.
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
## Passaggio 4: modifica le impostazioni di riempimento sfumato
Ora è il momento di modificare le impostazioni di riempimento sfumato in base alle nostre esigenze. Cambieremo il colore, l'opacità, la modalità di fusione e altre proprietà.
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
## Passaggio 5: aggiungi e modifica i punti di colore e trasparenza
Aggiungiamo nuovi punti di colore e trasparenza e modifichiamo quelli esistenti per ottenere l'effetto sfumato desiderato.
```java
// Aggiungi un nuovo punto colore
GradientColorPoint colorPoint = fillSettings.addColorPoint();
colorPoint.setColor(Color.getGreen());
colorPoint.setLocation(4096);
colorPoint.setMedianPointLocation(75);
// Cambia la posizione del punto precedente
fillSettings.getColorPoints()[1].setLocation(1899);
// Aggiungi un nuovo punto di trasparenza
GradientTransparencyPoint transparencyPoint = fillSettings.addTransparencyPoint();
transparencyPoint.setOpacity(25);
transparencyPoint.setMedianPointLocation(25);
transparencyPoint.setLocation(4096);
// Cambia la posizione del punto di trasparenza precedente
fillSettings.getTransparencyPoints()[1].setLocation(2411);
```
## Passaggio 6: salva il file PSD modificato
Dopo aver apportato tutte le modifiche necessarie, dobbiamo salvare il file PSD.
```java
im.save(exportPath);
```
## Passaggio 7: verificare le modifiche
Infine, carichiamo il file PSD salvato e verifichiamo che le nostre modifiche siano state applicate correttamente.
```java
PsdImage img = (PsdImage) Image.load(exportPath, loadOptions);
StrokeEffect gradientStrokeEffect = (StrokeEffect) img.getLayers()[2].getBlendingOptions().getEffects()[0];
Assert.areEqual(BlendMode.Color, gradientStrokeEffect.getBlendMode());
Assert.areEqual(127, gradientStrokeEffect.getOpacity());
Assert.areEqual(true, gradientStrokeEffect.isVisible());
GradientFillSettings fillSetting = (GradientFillSettings) gradientStrokeEffect.getFillSettings();
Assert.areEqual(Color.getGreen(), fillSetting.getColor());
Assert.areEqual(FillType.Gradient, fillSetting.getFillType());
// Controlla i punti di colore
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
// Controlla i punti di trasparenza
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
Ed ecco qua! Ora sai come aggiungere e manipolare i gradienti del livello del tratto nei file PSD utilizzando Aspose.PSD per Java. Questo tutorial ha trattato il caricamento del file PSD, l'accesso e la modifica degli effetti del tratto e il salvataggio delle modifiche. Con queste competenze, puoi creare gradienti visivamente accattivanti e personalizzare i tuoi file PSD in base alle tue esigenze.
## Domande frequenti
### Cos'è Aspose.PSD per Java?
Aspose.PSD per Java è una libreria che consente agli sviluppatori di lavorare con file PSD in applicazioni Java, fornendo funzionalità per creare, manipolare e convertire file PSD.
### Ho bisogno di una licenza per utilizzare Aspose.PSD per Java?
 Sì, è necessaria una licenza valida per utilizzare Aspose.PSD per Java. Puoi ottenere un[licenza temporanea](https://purchase.aspose.com/temporary-license/) a fini di valutazione.
### Posso utilizzare Aspose.PSD per Java per creare file PSD da zero?
Assolutamente! Aspose.PSD per Java fornisce API complete per creare e manipolare file PSD a livello di codice.
### È possibile applicare altri effetti utilizzando Aspose.PSD per Java?
Sì, puoi applicare vari effetti come ombra, bagliore e altro utilizzando Aspose.PSD per Java.
### Dove posso trovare la documentazione per Aspose.PSD per Java?
 Puoi trovare la documentazione[Qui](https://reference.aspose.com/psd/java/).