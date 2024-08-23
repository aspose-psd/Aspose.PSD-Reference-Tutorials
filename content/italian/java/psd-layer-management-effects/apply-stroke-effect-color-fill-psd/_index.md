---
title: Applica l'effetto tratto con riempimento colore in PSD - Java
linktitle: Applica l'effetto tratto con riempimento colore in PSD - Java
second_title: API Java Aspose.PSD
description: Scopri come applicare un effetto tratto con riempimento colore ai tuoi file PSD utilizzando Aspose.PSD per Java. Segui questa guida passo passo per migliorare le tue immagini con facilità.
type: docs
weight: 21
url: /it/java/psd-layer-management-effects/apply-stroke-effect-color-fill-psd/
---
## Introduzione

In questa guida ti guideremo attraverso il processo di applicazione di un effetto tratto con riempimento di colore ai tuoi file PSD utilizzando Aspose.PSD per Java. Che tu sia uno sviluppatore esperto o che tu abbia appena iniziato, questo tutorial passo passo ti renderà più semplice portare a termine il lavoro. Copriremo tutto, dalla configurazione del tuo ambiente al salvataggio dell'immagine finale con gli effetti applicati.

## Prerequisiti

Prima di iniziare, assicuriamoci di avere tutto ciò di cui hai bisogno per seguire questo tutorial:

1. Java Development Kit (JDK) installato: assicurati di avere JDK 8 o versione successiva installata sul tuo sistema.
2.  Aspose.PSD per la libreria Java: avrai bisogno della libreria Aspose.PSD per Java. Puoi scaricarlo da[sito web](https://releases.aspose.com/psd/java/).
3. Ambiente di sviluppo integrato (IDE): un IDE come IntelliJ IDEA, Eclipse o qualsiasi altro a tua scelta.
4. File PSD di esempio: un file PSD di esempio a cui è possibile applicare l'effetto tratto. Se non ne hai uno, puoi creare un semplice file PSD in Photoshop o scaricarne uno da Internet.
5. Conoscenza di base di Java: sebbene questo tutorial sia adatto ai principianti, sarà utile avere una conoscenza di base di Java.

Una volta stabiliti questi prerequisiti, sei pronto per iniziare ad applicare l'effetto tratto con riempimento colore ai tuoi file PSD.

## Importa pacchetti

Per iniziare a lavorare con Aspose.PSD per Java, dovrai importare i pacchetti necessari nel tuo progetto Java. Ecco come puoi farlo:

```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.fillsettings.ColorFillSettings;
import com.aspose.psd.fileformats.psd.layers.layereffects.StrokeEffect;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
import com.aspose.psd.imageoptions.PngOptions;
import com.aspose.psd.imageoptions.PsdOptions;
```

Queste importazioni introducono tutte le classi necessarie per lavorare con i file PSD, applicare effetti e salvare le immagini nel formato desiderato.

## Passaggio 1: carica il file PSD

 Il primo passo nel nostro processo è caricare il file PSD che desideri modificare. Aspose.PSD per Java lo rende incredibilmente semplice con il suo`PsdImage` classe. Ecco come puoi farlo:

### 1.1 Imposta il percorso della directory

Innanzitutto, definisci il percorso della directory in cui sono archiviati i file PSD:

```java
String dataDir = "Your Document Directory";
```

 Sostituire`"Your Document Directory"` con il percorso effettivo in cui si trova il file PSD.

### 1.2 Carica l'immagine PSD

 Ora carica il file PSD utilizzando il file`PsdLoadOptions` E`PsdImage` classi:

```java
String sourceFileName = dataDir + "StrokeComplex.psd";

PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);

PsdImage im = (PsdImage) Image.load(sourceFileName, loadOptions);
```

 Ecco, il`PsdLoadOptions`è configurato per caricare le risorse degli effetti, garantendo che tutti gli effetti esistenti all'interno del PSD siano accessibili.

## Passaggio 2: applica l'effetto tratto con riempimento colore

Una volta caricato il file PSD, il passaggio successivo consiste nell'applicare l'effetto tratto ai livelli dell'immagine. È qui che avviene la vera magia.

Ogni file PSD può contenere più livelli e dovrai applicare l'effetto a ciascuno di essi. Ecco come farlo:

```java
for (int i = 0; i < im.getLayers().length; i++) {
    StrokeEffect effect = (StrokeEffect) im.getLayers()[i].getBlendingOptions().getEffects()[0];
    ColorFillSettings settings = (ColorFillSettings) effect.getFillSettings();
    settings.setColor(Color.getDeepPink());
}
```

In questo ciclo:

- `im.getLayers()`: recupera tutti i livelli nel file PSD.
- `StrokeEffect effect`: Estrae l'effetto tratto applicato al livello.
- `ColorFillSettings settings`: modifica le impostazioni di riempimento per l'effetto tratto.
- `settings.setColor(Color.getDeepPink())`: imposta il colore del tratto su rosa intenso. Puoi cambiarlo con qualsiasi colore tu preferisca.

## Passaggio 3: salva il PSD modificato ed esporta come PNG

Dopo aver applicato l'effetto tratto, è il momento di salvare le modifiche ed esportare l'immagine.

### 3.1 Salvare il file PSD

Per salvare il file PSD modificato, utilizzare il seguente codice:

```java
String exportPath = dataDir + "StrokeComplexRendering.psd";
im.save(exportPath, new PsdOptions());
```

Ciò salva il file con l'effetto tratto applicato nel percorso specificato.

### 3.2 Esporta come PNG

Per rendere l'immagine più accessibile, potresti voler esportarla come file PNG. Ecco come:

```java
String exportPathPng = dataDir + "StrokeComplexRendering.png";
PngOptions option = new PngOptions();
option.setColorType(PngColorType.TruecolorWithAlpha);

im.save(exportPathPng, option);
```

Questo frammento di codice salva l'immagine come PNG con colori reali e trasparenza alfa, rendendola pronta per l'uso in applicazioni web o altre piattaforme.

## Conclusione

Applicare un effetto tratto con riempimento di colore ai tuoi file PSD utilizzando Aspose.PSD per Java non è solo semplice ma anche incredibilmente potente. Con solo poche righe di codice, puoi automatizzare attività complesse di elaborazione delle immagini, risparmiando tempo e fatica.

Sia che tu stia lavorando su una grande quantità di immagini o che tu abbia semplicemente bisogno di modificare alcuni file, questo metodo fornisce una soluzione flessibile ed efficiente. Ora che conosci le nozioni di base, puoi iniziare a sperimentare diversi effetti e personalizzazioni per far risaltare davvero le tue immagini.

Pronto a provarlo? Prendi il tuo file PSD di esempio e inizia ad aggiungere quegli effetti sorprendenti oggi stesso!

## Domande frequenti

### Posso applicare più effetti a un singolo livello utilizzando Aspose.PSD per Java?
Sì, puoi applicare più effetti a un singolo livello accedendo alle opzioni di fusione del livello e aggiungendo gli effetti desiderati.

### È possibile automatizzare il processo per un batch di file PSD?
Assolutamente! È possibile scorrere una directory di file PSD, applicare l'effetto tratto e salvare automaticamente i risultati.

### Come posso ripristinare le modifiche apportate a un file PSD utilizzando Aspose.PSD per Java?
Per annullare le modifiche, dovrai ricaricare il file PSD originale prima di salvare eventuali modifiche. Non esiste alcuna funzionalità di annullamento diretto in Aspose.PSD.

### Posso personalizzare la larghezza e la posizione del tratto?
 Sì, Aspose.PSD per Java ti consente di personalizzare la larghezza del tratto, la posizione e altre proprietà tramite il file`StrokeEffect` classe.

### La libreria Aspose.PSD per Java è gratuita?
 Aspose.PSD per Java offre una prova gratuita, ma per l'accesso completo a tutte le funzionalità è necessario acquistare una licenza. Puoi esplorare il[acquistare opzioni](https://purchase.aspose.com/buy)sul loro sito web.