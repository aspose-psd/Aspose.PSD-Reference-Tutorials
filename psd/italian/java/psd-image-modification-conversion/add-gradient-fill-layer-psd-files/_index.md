---
title: Aggiungi un livello di riempimento sfumato nei file PSD con Java
linktitle: Aggiungi un livello di riempimento sfumato nei file PSD con Java
second_title: API Java Aspose.PSD
description: Modifica i livelli di riempimento sfumato nei file PSD utilizzando Aspose.PSD per Java. Scopri come modificare colori, trasparenza e altre proprietà del gradiente a livello di codice.
weight: 15
url: /it/java/psd-image-modification-conversion/add-gradient-fill-layer-psd-files/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aggiungi un livello di riempimento sfumato nei file PSD con Java

## Introduzione

Hai mai desiderato quel tocco in più di magia visiva per i tuoi file PSD? Le sfumature offrono un modo straordinario per aggiungere profondità e dimensione ai tuoi progetti. Ma cosa succede se si desidera manipolare a livello di codice questi gradienti utilizzando Java? Aspose.PSD viene in soccorso! Questa guida completa ti consentirà di modificare i livelli di riempimento sfumato all'interno dei file PSD utilizzando Aspose.PSD, guidandoti passo dopo passo attraverso l'entusiasmante processo.

## Prerequisiti

Prima di immergerti, assicurati di avere quanto segue:

-  Java Development Kit (JDK): è necessaria una versione stabile di JDK per eseguire il codice Java. Puoi scaricarlo dal sito web di Oracle:[Collegamento alla pagina di download di Oracle JDK]
-  Aspose.PSD per Java: questa potente libreria ti consente di lavorare con file PSD nelle tue applicazioni Java. Scaricatelo dal sito Aspose:[Collegamento ad Aspose.PSD per il download di Java] (prova gratuita disponibile)

## Importa pacchetti

Iniziamo importando i pacchetti Aspose.PSD essenziali necessari per lavorare con i file PSD:

```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.IGradientColorPoint;
import com.aspose.psd.fileformats.psd.layers.filllayers.FillLayer;
import com.aspose.psd.fileformats.psd.layers.fillsettings.FillType;
import com.aspose.psd.fileformats.psd.layers.fillsettings.GradientColorPoint;
import com.aspose.psd.fileformats.psd.layers.fillsettings.GradientTransparencyPoint;
import com.aspose.psd.fileformats.psd.layers.fillsettings.IGradientFillSettings;
import com.aspose.psd.fileformats.psd.layers.fillsettings.IGradientTransparencyPoint;
import com.aspose.psd.imageoptions.PsdOptions;
import java.util.ArrayList;
import java.util.Collections;
import java.util.List;
```

Queste importazioni forniscono l'accesso a classi e metodi per caricare, manipolare e salvare file PSD.

Ora preparati per l'entusiasmante viaggio di modifica dei livelli di riempimento sfumato!

## Passaggio 1: carica il file PSD

 Per prima cosa dobbiamo caricare il file PSD contenente il livello di riempimento sfumato che desideri modificare. Usa il`Image.load` metodo, specificando il percorso del file:

```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "ComplexGradientFillLayer.psd";
String outputFile = dataDir + "ComplexGradientFillLayer_output.psd";
PsdImage image = (PsdImage)Image.load(sourceFileName);
```

 Questo frammento di codice carica il file PSD dalla directory specificata e lo memorizza nel file`image` variabile.

## Passaggio 2: identificare il livello di riempimento sfumato

 I file PSD possono contenere numerosi livelli. Dobbiamo isolare il livello specifico contenente il riempimento sfumato che vogliamo modificare. Scorrere il file`image.getLayers()` array per trovare il livello desiderato:

```java
for (int i = 0; i < image.getLayers().length; i++) {
if (image.getLayers()[i] instanceof FillLayer) {
   FillLayer fillLayer = (FillLayer) image.getLayers()[i];
   // Ulteriori controlli e modifiche avverranno qui
   break;
}
}
```

 Questo ciclo controlla ogni livello. Se uno strato è a`FillLayer` , viene lanciato su`FillLayer` digitare e archiviare nel file`fillLayer`variabile per ulteriori elaborazioni. Possiamo aggiungere ulteriori controlli all'interno del ciclo se hai criteri specifici per identificare il livello di destinazione (ad esempio, il nome del livello).

## Passaggio 3: verificare il tipo di riempimento sfumato

Non tutti i livelli di riempimento utilizzano gradienti. Questo frammento di codice conferma se il livello identificato contiene effettivamente un riempimento sfumato:

```java
if (fillLayer.getFillSettings().getFillType() != FillType.Gradient) {
   throw new Exception("Wrong Fill Layer");
}
```

 Se il`getFillType` il metodo non restituisce`FillType.Gradient`, viene generata un'eccezione, che indica che stiamo lavorando con il livello sbagliato.

## Passaggio 4: accedi e modifica le proprietà del gradiente

 La magia avviene qui! Aspose.PSD fornisce l'accesso a varie proprietà di riempimento sfumato tramite`IGradientFillSettings` interfaccia. Possiamo recuperarli e modificarli secondo necessità:

```java
IGradientFillSettings settings = (IGradientFillSettings) fillLayer.getFillSettings();

// Modifica proprietà (sostituisci con i valori desiderati)
settings.setAngle(0.0);  // Imposta l'angolo su 0 gradi
settings.setDither(false);  // Disabilita dithering
settings.setAlignWithLayer(true); // Allinea il gradiente al livello
settings.setReverse(true);  // Invertire la direzione del gradiente
settings.setHorizontalOffset(25);  // Imposta l'offset orizzontale
settings.setVerticalOffset(-15);  // Imposta l'offset verticale
```

 Questo codice recupera il file`IGradientFillSettings`oggetto e quindi modifica proprietà come angolo, dithering, allineamento e offset. Sostituisci i valori forniti con le impostazioni desiderate per ottenere l'effetto sfumato che immagini.

## Passaggio 5: manipolare i punti di colore e trasparenza

I gradienti sono definiti dai punti di colore e trasparenza lungo uno spettro. Aspose.PSD ti consente di modificare questi punti per un controllo preciso:

```java
List<IGradientColorPoint> colorPoints = new ArrayList<IGradientColorPoint>();
Collections.addAll(colorPoints, settings.getColorPoints());
List<IGradientTransparencyPoint> transparencyPoints = new ArrayList<IGradientTransparencyPoint>();
Collections.addAll(transparencyPoints, settings.getTransparencyPoints());

// Aggiungi un nuovo punto colore
GradientColorPoint gr1 = new GradientColorPoint();
gr1.setColor(Color.getViolet());
gr1.setLocation(4096);
gr1.setMedianPointLocation(75);
colorPoints.add(gr1);

// Modifica un punto colore esistente
colorPoints.get(1).setLocation(3000);

// Aggiungi un nuovo punto di trasparenza
GradientTransparencyPoint gr2 = new GradientTransparencyPoint();
gr2.setOpacity(80.0);
gr2.setLocation(4096);
gr2.setMedianPointLocation(25);
transparencyPoints.add(gr2);

// Modifica un punto di trasparenza esistente
transparencyPoints.get(2).setLocation(3000);

settings.setColorPoints(colorPoints.toArray(new IGradientColorPoint[0]));
settings.setTransparencyPoints(transparencyPoints.toArray(new IGradientTransparencyPoint[0]));
```

## Passaggio 6: aggiorna e salva il file PSD

Dopo aver apportato le modifiche necessarie, aggiorna il livello di riempimento e salva il file PSD:

```java
fillLayer.update();
image.save(outputFile, new PsdOptions(image));
```

 IL`fillLayer.update()` Il metodo applica le modifiche al livello di riempimento sfumato e`image.save` salva il file PSD modificato nel percorso di output specificato.

## Conclusione

Hai imparato con successo l'arte di modificare i livelli di riempimento sfumato nei file PSD utilizzando Aspose.PSD per Java! Seguendo questi passaggi, puoi liberare la tua creatività e creare straordinari effetti visivi con precisione programmatica.

## Domande frequenti

### Posso aggiungere più punti di colore e trasparenza a una sfumatura?
Assolutamente! È possibile aggiungere tutti i punti di colore e trasparenza necessari per ottenere l'effetto sfumato desiderato. Basta creare nuovi punti e aggiungerli ai rispettivi elenchi.

### Come rimuovo un punto di colore o di trasparenza da una sfumatura?
 Per rimuovere un punto, utilizzare l'elenco appropriato`remove` metodo. Per esempio,`colorPoints.remove(index)` rimuoverebbe il punto di colore nell'indice specificato.

### Posso cambiare il tipo di gradiente (lineare, radiale, ecc.)?
Aspose.PSD attualmente supporta i gradienti lineari. Anche se nelle versioni future potrebbero essere supportati altri tipi di gradiente, è possibile ottenere effetti simili manipolando i punti di colore e trasparenza in modo creativo.

### C'è un impatto sulle prestazioni quando si modificano i gradienti?
L'impatto sulle prestazioni dipende dalla complessità del gradiente e dal numero di modifiche apportate. Per la maggior parte dei casi d'uso pratici, le prestazioni dovrebbero essere accettabili. Tuttavia, per l'elaborazione delle immagini su larga scala, valuta la possibilità di ottimizzare il codice per migliorarne l'efficienza.

### Posso applicare questa tecnica a più livelli di riempimento sfumato in un file PSD?
Sì, puoi scorrere i livelli e applicare le modifiche a ciascun livello di riempimento sfumato che soddisfa i tuoi criteri.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
