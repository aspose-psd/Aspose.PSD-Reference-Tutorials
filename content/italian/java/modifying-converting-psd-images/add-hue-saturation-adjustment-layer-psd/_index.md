---
title: Aggiungi il livello di regolazione della saturazione della tonalità a PSD
linktitle: Aggiungi il livello di regolazione della saturazione della tonalità a PSD
second_title: API Java Aspose.PSD
description: Scopri come aggiungere livelli di regolazione della saturazione della tonalità a PSD utilizzando Aspose.PSD per Java in questo tutorial completo passo dopo passo. Migliora il flusso di lavoro della progettazione grafica.
type: docs
weight: 14
url: /it/java/modifying-converting-psd-images/add-hue-saturation-adjustment-layer-psd/
---
## Introduzione
Quando si tratta di progettazione grafica, la manipolazione del colore gioca un ruolo fondamentale: in particolare, modificare tonalità, saturazione e luminosità può trasformare drasticamente l'atmosfera e la qualità di qualsiasi immagine. Un modo efficace per raggiungere questo obiettivo è attraverso l'uso dei livelli di regolazione in Photoshop (file PSD). Se stai cercando di migliorare i tuoi file PSD a livello di codice utilizzando Java, la libreria Aspose.PSD è qui per aiutarti! Questo tutorial ti guiderà attraverso i passaggi per aggiungere un livello di regolazione della saturazione della tonalità ai tuoi file PSD, rendendo i tuoi flussi di lavoro più produttivi ed efficienti.
In questa guida tratteremo tutto, dall'importazione dei pacchetti necessari ai dettagli essenziali degli esempi di codice.
## Prerequisiti
Prima di addentrarci nel codice, assicurati di avere quanto segue:
1.  Java Development Kit (JDK): assicurati di avere JDK 8 o versione successiva installata sul tuo computer. Puoi scaricarlo da[Download del kit di sviluppo Java SE](https://www.oracle.com/java/technologies/javase-downloads.html).
2.  Aspose.PSD per Java Library: avrai bisogno della libreria Aspose.PSD, cosa che puoi[scarica qui](https://releases.aspose.com/psd/java/). 
3. IDE: un ambiente di sviluppo integrato (IDE) adatto come IntelliJ IDEA o Eclipse per lo sviluppo Java.
4. Conoscenza di base di Java: la familiarità con la programmazione Java è un vantaggio, ma non preoccuparti; ti guideremo attraverso il codice passo dopo passo.
Ora che abbiamo sistemato i prerequisiti, passiamo alla parte divertente: la codifica!
## Importa pacchetti
Per iniziare a lavorare con la libreria Aspose.PSD, il primo passo è importare le classi necessarie. Ecco come puoi farlo nel tuo file Java:
```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.adjustmentlayers.HueSaturationLayer;
import com.aspose.psd.fileformats.psd.layers.layerresources.ColorRangeHsl;
```
Assicurati di aver aggiunto le librerie appropriate al tuo progetto in modo che queste importazioni funzionino senza problemi.
## Passaggio 1: imposta la directory dei documenti
Ogni progetto ha bisogno di un punto di partenza e il nostro non fa eccezione. È necessario specificare una directory in cui sono archiviati i file PSD. Questo è fondamentale per caricare e salvare correttamente le immagini.
```java
String dataDir = "Your Document Directory"; // Aggiorna questo percorso nella tua directory effettiva
```
## Passaggio 2: carica un file PSD esistente
Per manipolare un file PSD esistente, dobbiamo prima caricarlo nel nostro programma. Ecco come puoi farlo:
```java
String sourceFileName = dataDir + "HueSaturationAdjustmentLayer.psd";
PsdImage im = (PsdImage) Image.load(sourceFileName);
```
 In questo codice, aggiorna`"HueSaturationAdjustmentLayer.psd"` al nome del file PSD esistente che desideri modificare.
## Passaggio 3: modifica il livello Tonalità/Saturazione
Successivamente, scorreremo i livelli dell'immagine PSD caricata per trovare e modificare eventuali livelli Tonalità/Saturazione esistenti. Questo passaggio prevede la modifica dei valori di tonalità, saturazione e luminosità.
```java
for (int i = 0; i < im.getLayers().length; i++) {
    if (im.getLayers()[i] instanceof HueSaturationLayer) {
        HueSaturationLayer hueLayer = (HueSaturationLayer) im.getLayers()[i];
        hueLayer.setHue((short) -25);
        hueLayer.setSaturation((short) -12);
        hueLayer.setLightness((short) 67);
        ColorRangeHsl colorRange = hueLayer.getRange(2);
        colorRange.setHue((short) -40);
        colorRange.setSaturation((short) 50);
        colorRange.setLightness((short) -20);
        colorRange.setMostLeftBorder((short) 300);
    }
}
```
In questo esempio:
- Stiamo regolando la tonalità su -25, la saturazione su -12 e la luminosità su +67.
-  IL`getRange(2)` Il metodo ci consente di modificare gamme di colori specifiche come desiderato.
## Passaggio 4: salva il file PSD modificato
Dopo aver apportato le modifiche, il passaggio successivo è salvare il file. Questa è una parte vitale del nostro processo, poiché garantisce che le modifiche apportate non vadano perse.
```java
String psdPathAfterChange = dataDir + "HueSaturationAdjustmentLayerChanged.psd";
im.save(psdPathAfterChange);
```
## Passaggio 5: aggiungi un nuovo livello di tonalità/saturazione
Successivamente, potresti voler aggiungere un nuovo livello di regolazione Tonalità/Saturazione a un altro file PSD. Segui semplicemente lo stesso approccio utilizzato in precedenza ma con file PSD diversi.
```java
sourceFileName = dataDir + "PhotoExample.psd";
PsdImage img = (PsdImage) Image.load(sourceFileName);
HueSaturationLayer hueLayerNew = img.addHueSaturationAdjustmentLayer();
```
## Passaggio 6: imposta i nuovi valori di tonalità/saturazione per il nuovo livello
Ora che hai creato questo nuovo livello, applica le impostazioni di tonalità, saturazione e luminosità desiderate proprio come prima.
```java
hueLayerNew.setHue((short) -25);
hueLayerNew.setSaturation((short) -12);
hueLayerNew.setLightness((short) 67);
ColorRangeHsl newColorRange = hueLayerNew.getRange(2);
newColorRange.setHue((short) -160);
newColorRange.setSaturation((short) 100);
newColorRange.setLightness((short) 20);
newColorRange.setMostLeftBorder((short) 300);
```
## Passaggio 7: salva il file PSD aggiornato
Infine, salva il file PSD con il livello Tonalità/Saturazione aggiunto in modo da poter vedere le modifiche.
```java
String psdPathAfterNewLayerChange = dataDir + "PhotoExampleAddedHueSaturation.psd";
img.save(psdPathAfterNewLayerChange);
```
Congratulazioni! Hai manipolato con successo i file PSD utilizzando Aspose.PSD per Java. Ora puoi sperimentare immagini diverse e alterazioni più profonde, dando vita ai tuoi progetti di design grafico.
## Conclusione
Lavorare con la grafica in modo programmatico apre un mondo di possibilità. L'utilizzo di Aspose.PSD per Java per aggiungere e modificare i livelli di regolazione della saturazione della tonalità offre flessibilità ed efficienza in grado di semplificare il flusso di lavoro di progettazione. Che tu stia migliorando le foto per un progetto o creando contenuti visivi straordinari, padroneggiare questi strumenti può migliorare notevolmente il tuo risultato.
 Sentiti libero di esplorare più funzionalità di Aspose.PSD immergendoti[documentazione](https://reference.aspose.com/psd/java/) o considera di impigliarti a[licenza temporanea](https://purchase.aspose.com/temporary-license/) per testare tutta la potenza della libreria.
## Domande frequenti
### Cos'è un livello di regolazione della saturazione della tonalità?
Un livello di regolazione della saturazione della tonalità consente di modificare le proprietà del colore di un'immagine senza alterare in modo permanente i pixel originali.
### Ho bisogno di Photoshop installato per utilizzare Aspose.PSD?
No, Aspose.PSD è una libreria autonoma che funziona indipendentemente da Photoshop.
### Posso utilizzare Aspose.PSD per l'elaborazione batch?
Sì, puoi automatizzare ed elaborare in batch più file PSD con Aspose.PSD.
### Aspose.PSD è gratuito?
Aspose.PSD offre una prova gratuita, ma è necessaria una licenza per l'uso a lungo termine. Puoi visualizzare i prezzi[Qui](https://purchase.aspose.com/buy).