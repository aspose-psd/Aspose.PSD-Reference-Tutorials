---
title: Livello di regolazione del livello di rendering nei file PSD - Java
linktitle: Livello di regolazione del livello di rendering nei file PSD - Java
second_title: API Java Aspose.PSD
description: Scopri come migliorare facilmente il contrasto e la vivacità dell'immagine utilizzando Aspose.PSD per Java. Livelli di regolazione dei livelli principali con questa guida passo passo.
weight: 17
url: /it/java/psd-layer-management-effects/render-level-adjustment-layer-psd/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Livello di regolazione del livello di rendering nei file PSD - Java

## Introduzione

Ti è mai capitato di aprire un file PSD solo per scoprire che l'immagine mancava di contrasto o vivacità? Non temere, guerrieri dell'editing di immagini! Aspose.PSD per Java viene in soccorso con le sue potenti capacità di manipolazione del livello di regolazione dei livelli. Questa guida ti fornirà le conoscenze per ottimizzare le tue immagini utilizzando i Livelli in un attimo. 

## Prerequisiti

- Java Development Kit (JDK): assicurati di avere una versione recente di JDK installata sul tuo sistema. È possibile scaricarlo dal sito Web Oracle ([https://www.oracle.com/java/technologies/javase-downloads.html](https://www.oracle.com/java/technologies/javase-downloads.html)).
- Aspose.PSD per libreria Java: scaricare la libreria Aspose.PSD per Java dalla pagina di download ([https://releases.aspose.com/psd/java/](https://releases.aspose.com/psd/java/)). Avrai bisogno di una licenza valida per utilizzare tutte le funzionalità, ma per iniziare è disponibile una prova gratuita ([https://releases.aspose.com/](https://releases.aspose.com/)).

## Importa pacchetti

Prima di immergerci nel codice, dobbiamo importare le classi Aspose.PSD necessarie per interagire con i file PSD. Ecco cosa ti servirà:

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.adjustmentlayers.LevelsLayer;
import com.aspose.psd.fileformats.psd.layers.layerresources.LevelChannel;
import com.aspose.psd.imageoptions.PngOptions;
```

 IL`com.aspose.psd` il pacchetto fornisce l'accesso alle funzionalità di manipolazione PSD, mentre`com.aspose.psd.imaging.PngOptions` ci consente di definire le opzioni quando si salva l'immagine come PNG.

Ora iniziamo la nostra avventura di regolazione dei livelli:

## Passaggio 1: impostazione dei percorsi dei file:

- Definire le variabili per la directory dei documenti (`dataDir`), nome del file PSD di origine (`sourceFileName`), nome del file PSD di destinazione dopo la modifica (`psdPathAfterChange`) e il percorso di esportazione PNG finale (`pngExportPath`). Prendi in considerazione l'utilizzo di nomi descrittivi per migliorare la leggibilità del codice.

```java
String dataDir = "Your Document Directory";

String sourceFileName = dataDir + "LevelsAdjustmentLayer.psd";
String psdPathAfterChange = dataDir + "LevelsAdjustmentLayerChanged.psd";
String pngExportPath = dataDir + "LevelsAdjustmentLayerChanged.png";
```

## Passaggio 2: caricamento dell'immagine PSD:

-  Usa il`Image.load` metodo per aprire il file PSD di origine e memorizzarlo in un file`PsdImage`oggetto (`im`). Aspose.PSD rileva automaticamente il formato del file.

```java
PsdImage im = (PsdImage)Image.load(sourceFileName);
```

## Passaggio 3: Iterazione attraverso i livelli:

- Dobbiamo trovare il livello di regolazione dei livelli all'interno del tuo PSD. Aspose fornisce un modo conveniente per scorrere tutti i livelli utilizzando un ciclo.

```java
for (int i = 0; i < im.getLayers().length; i++) {
   // ... (il codice per verificare il livello dei livelli verrà aggiunto qui)
}
```

## Passaggio 4: identificazione del livello dei livelli:

- All'interno del ciclo, controlla se il livello corrente (`im.getLayers()[i]` ) è un'istanza di`LevelsLayer` classe utilizzando il file`instanceof` operatore. 
-  Se lo è, lancia il livello su a`LevelsLayer` oggetto per ulteriore manipolazione.

```java
for (int i = 0; i < im.getLayers().length; i++) {
   if (im.getLayers()[i] instanceof LevelsLayer) {
	   LevelsLayer levelsLayer = (LevelsLayer) im.getLayers()[i];
	   // ... (il codice per regolare i livelli verrà aggiunto qui)
   }
}
```
## Passaggio 5: regolazione fine dei livelli (continua):

-  Regolare i livelli di uscita utilizzando`setOutputShadowLevel` E`setOutputHighlightLevel` per controllare l'oscurità e la luminosità dell'immagine risultante. Questi valori determinano l'intervallo dei livelli di ingresso che verranno mappati sull'intervallo di uscita.

```java
for (int i = 0; i < im.getLayers().length; i++) {
   if (im.getLayers()[i] instanceof LevelsLayer) {
	   LevelsLayer levelsLayer = (LevelsLayer) im.getLayers()[i];
	   LevelChannel channel = levelsLayer.getChannel(0);

	   // Regola i livelli di ingresso (0-255):
	   channel.setInputShadowLevel((short) 10); // Scurisci leggermente le ombre
	   channel.setInputMidtoneLevel(2.0f);     // Aumenta i mezzitoni
	   channel.setInputHighlightLevel((short) 230); // Riduci le luci

	   // Regola i livelli di uscita (0-255):
	   channel.setOutputShadowLevel((short) 20); // Scurisci ulteriormente le ombre
	   channel.setOutputHighlightLevel((short) 200); //Illumina i punti salienti
   }
}
```

## Passaggio 6: salvataggio del PSD modificato:

-  Usa il`save` metodo del`PsdImage` oggetto per salvare l'immagine modificata nel percorso specificato (`psdPathAfterChange`).

```java
im.save(psdPathAfterChange);
```

## Passaggio 7: esportazione come PNG (facoltativo):

-  Se hai bisogno di una versione PNG dell'immagine modificata, crea un file`PngOptions` oggetto e impostare il tipo di colore su`TruecolorWithAlpha` . Quindi, utilizzare il`save` nuovamente il metodo con il percorso e le opzioni di esportazione PNG.

```java
PngOptions saveOptions = new PngOptions();
saveOptions.setColorType(PngColorType.TruecolorWithAlpha);
im.save(pngExportPath, saveOptions);
```

Ed ecco qua! Hai regolato con successo il livello di regolazione dei livelli nel tuo file PSD utilizzando Aspose.PSD per Java. Comprendendo questi passaggi e sperimentando valori diversi, puoi migliorare il contrasto e l'aspetto generale delle tue immagini.

## Conclusione

Aspose.PSD per Java ti consente di prendere il controllo del processo di modifica delle immagini. Padroneggiando il livello di regolazione dei livelli, puoi dare nuova vita alle tue foto e ai tuoi disegni. Ricorda, la pratica rende perfetti, quindi non esitare a sperimentare ed esplorare tutto il potenziale di questo potente strumento.
 
## Domande frequenti

### Posso regolare separatamente i singoli canali colore (RGB)? 
Sì, puoi accedere a ciascun canale di colore utilizzando`getChannel` metodo del`LevelsLayer` oggetto e modificarne i livelli in modo indipendente.

### Come posso gestire più livelli di regolazione dei livelli in un PSD?
Il codice scorre tutti i livelli, quindi elaborerà automaticamente tutti i livelli aggiuntivi presenti nell'immagine.

### Esistono altri modi per regolare il contrasto dell'immagine oltre ai Livelli?
Assolutamente! Aspose.PSD offre vari strumenti di regolazione dell'immagine come Curve, Luminosità/Contrasto e altro.

### Posso automatizzare questo processo per più immagini? 
Sì, puoi incorporare questo codice in uno script di elaborazione in loop o batch per elaborare in modo efficiente più file PSD.

### Dove posso trovare maggiori informazioni e supporto?
Aspose fornisce un'ampia documentazione ([https://reference.aspose.com/psd/java/](https://reference.aspose.com/psd/java/)) e un forum di supporto ([https://forum.aspose.com/c/psd/34](https://forum.aspose.com/c/psd/34)) per qualsiasi domanda o problema che potresti incontrare.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
