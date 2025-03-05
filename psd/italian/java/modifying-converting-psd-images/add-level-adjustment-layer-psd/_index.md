---
title: Aggiungi il livello di regolazione del livello in PSD
linktitle: Aggiungi il livello di regolazione del livello in PSD
second_title: API Java Aspose.PSD
description: Scopri come aggiungere in modo efficace un livello di regolazione del livello nei file PSD utilizzando Aspose.PSD per Java. Migliora le tue capacità di editing delle immagini.
type: docs
weight: 16
url: /it/java/modifying-converting-psd-images/add-level-adjustment-layer-psd/
---
## Introduzione
Quando si tratta di editing delle immagini, la gestione dei livelli può fare un'enorme differenza nella vivacità e nella chiarezza delle tue foto. Uno strumento utile nell'arsenale di Photoshop è il "Livello di regolazione del livello", che ti consente di modificare la gamma tonale e il bilanciamento del colore delle tue immagini. In questa guida ti spiegheremo come implementare un livello di regolazione del livello in un file PSD utilizzando Aspose.PSD per Java. Quindi, prendi il tuo IDE Java.
## Prerequisiti
Prima di tuffarti nel mondo delle regolazioni di livello, dovrai impostare alcune cose per garantire una guida fluida:
1.  Java Development Kit (JDK): assicurati di avere il JDK installato sul tuo computer. Se non ce l'hai, puoi prenderlo da[Sito web dell'Oracle](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html) oppure usa OpenJDK.
2.  Aspose.PSD per libreria Java: per manipolare i file PSD, dovrai scaricare la libreria Aspose.PSD. Puoi ottenere l'ultima versione da questo[collegamento per il download](https://releases.aspose.com/psd/java/) e assicurati di aver incluso il JAR nella libreria del tuo progetto.
3. Conoscenza di base di Java: avere una conoscenza fondamentale della programmazione Java sarà utile, poiché in questo tutorial approfondiremo i frammenti di codice.
4. Configurazione IDE: puoi utilizzare qualsiasi IDE Java che preferisci, come IntelliJ IDEA, Eclipse o NetBeans, per scrivere ed eseguire il tuo codice. Assicurati solo di aver impostato il tuo progetto Java e aggiunto la libreria Aspose.PSD.

## Importa pacchetti
Prima di iniziare a scrivere il nostro codice, dobbiamo importare i pacchetti necessari dalla libreria Aspose.PSD. Ecco come puoi farlo:
```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.adjustmentlayers.LevelsLayer;
import com.aspose.psd.fileformats.psd.layers.layerresources.LevelChannel;
```
Importando questi pacchetti avremo accesso alle classi necessarie per caricare, modificare e salvare i nostri file PSD.

Ora suddividiamo il processo in passaggi digeribili. Segui mentre procediamo attraverso il caricamento di un file PSD, la regolazione dei livelli e il salvataggio delle modifiche. 
## Passaggio 1: imposta i percorsi dei file
Il primo passo è definire dove si trova il nostro file PSD e dove vogliamo salvare l'output modificato. È possibile personalizzare il percorso della directory in base alle proprie esigenze.
```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "LevelsAdjustmentLayer.psd";
String psdPathAfterChange = dataDir + "LevelsAdjustmentLayerChanged.psd";
```
 Ecco, sostituisci`"Your Document Directory"`con il percorso effettivo sul tuo sistema in cui è archiviato il tuo file PSD. Questo pone le basi per tutto ciò che faremo dopo.
## Passaggio 2: carica il file PSD
 Ora carichiamo il file PSD utilizzando il file`PsdImage` classe. Questo passaggio è essenziale in quanto ci consente di accedere e manipolare i livelli.
```java
PsdImage im = (PsdImage) Image.load(sourceFileName);
```
 Quando chiami`Image.load()` , leggerà il file PSD e creerà un'istanza di`PsdImage` con cui puoi lavorare.
## Passaggio 3: scorrere i livelli
Poiché vogliamo regolare un livello di regolazione del livello, dovremo scorrere ogni livello nel nostro file PSD. Questo ci aiuta a trovare il livello specifico che vogliamo modificare.
```java
for (int i = 0; i < im.getLayers().length; i++) {
    if (im.getLayers()[i] instanceof LevelsLayer) {
        LevelsLayer levelsLayer = (LevelsLayer) im.getLayers()[i];
        // Ulteriori manipolazioni andranno qui...
    }
}
```
 In questo ciclo,`instanceof LevelsLayer` controlla se il livello corrente è un livello di regolazione dei livelli. Se lo è, possiamo procedere a modificare le sue proprietà.
## Passaggio 4: regolare le impostazioni del canale di livello
Una volta identificato il livello corretto, possiamo modificare i suoi livelli di input e output. È qui che avviene la magia! Regola diversi parametri per vedere come influenzano l'immagine.
```java
LevelChannel channel = levelsLayer.getChannel(0);
channel.setInputMidtoneLevel(2.0f);
channel.setInputShadowLevel((short) 10);
channel.setInputHighlightLevel((short) 230);
channel.setOutputShadowLevel((short) 20);
channel.setOutputHighlightLevel((short) 200);
```
Ecco cosa fa ciascun parametro:
- Livello dei toni medi in ingresso: regola i toni medi.
- Livello ombra input: modifica le aree più scure dell'immagine.
- Livello evidenziazione input: altera le aree luminose dell'immagine.
- Livello ombra di output: imposta il modo in cui appariranno le ombre scure.
- Livello evidenziazione output: imposta la modalità di visualizzazione delle evidenziazioni luminose.
Sentiti libero di sperimentare valori diversi!
## Passaggio 5: salva il file PSD modificato
Ora che abbiamo apportato le modifiche, è il momento di salvare il file PSD modificato. Questo passaggio è fondamentale per garantire che le modifiche vengano applicate e archiviate.
```java
im.save(psdPathAfterChange);
```
 Ora puoi trovare il file PSD modificato nel formato specificato`psdPathAfterChange`. 
## Conclusione
Hai appena imparato come aggiungere un livello di regolazione del livello a un file PSD utilizzando Aspose.PSD per Java! Seguendo questa guida, puoi regolare facilmente la qualità tonale delle tue immagini, aprendo la strada a un risultato più vibrante e visivamente accattivante. Ricorda, la pratica rende perfetti, quindi sentiti libero di modificare le regolazioni ed esplorare diversi file PSD per vedere gli effetti delle tue modifiche.
## Domande frequenti
### Cos'è un livello di regolazione del livello?
Un livello di regolazione del livello ti consente di correggere la gamma tonale delle tue immagini, bilanciando ombre, mezzitoni e luci.
### Posso utilizzare Aspose.PSD senza acquistare?
SÌ! Aspose offre una prova gratuita per testare la libreria prima dell'acquisto.
### Dove posso trovare la documentazione per Aspose.PSD?
 Puoi trovare la documentazione[Qui](https://reference.aspose.com/psd/java/).
### Esiste un supporto comunitario per i prodotti Aspose?
 Assolutamente! Puoi porre domande e ottenere supporto nel[Aspose forum](https://forum.aspose.com/c/psd/34).
### Come posso ottenere una licenza temporanea per Aspose.PSD?
 Puoi richiedere una licenza temporanea[Qui](https://purchase.aspose.com/temporary-license/).