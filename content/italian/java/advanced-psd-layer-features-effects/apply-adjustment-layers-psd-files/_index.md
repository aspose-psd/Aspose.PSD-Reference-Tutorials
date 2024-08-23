---
title: Applica livelli di regolazione nei file PSD utilizzando Java
linktitle: Applica livelli di regolazione nei file PSD utilizzando Java
second_title: API Java Aspose.PSD
description: Impara ad applicare i livelli di regolazione nei file PSD utilizzando Aspose.PSD per Java in questa guida passo passo completa per gli sviluppatori.
type: docs
weight: 15
url: /it/java/advanced-psd-layer-features-effects/apply-adjustment-layers-psd-files/
---
## Introduzione
Sei uno sviluppatore Java che desidera migliorare le immagini archiviate nei file PSD? Se è così, sei nel posto giusto! In questo articolo esploreremo come applicare i livelli di regolazione nei file PSD utilizzando la libreria Aspose.PSD per Java. Che tu stia lavorando su un progetto personale o su un'applicazione professionale, capire come manipolare i file PSD può aumentare significativamente le capacità del tuo software. 

## Prerequisiti
Prima di addentrarci nel codice e iniziare ad applicare i livelli di regolazione, sono necessari alcuni prerequisiti:
1. Java Development Kit (JDK): assicurati di avere JDK installato sul tuo computer. Puoi scaricarlo da[Il sito web di Oracle](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).
2.  Libreria Aspose.PSD: se non l'hai già fatto, dovrai scaricare la libreria Aspose.PSD per Java. Puoi trovarlo[Qui](https://releases.aspose.com/psd/java/).
3. Ambiente di sviluppo: configura un ambiente di sviluppo integrato Java (IDE) come IntelliJ IDEA o Eclipse in cui scriverai ed eseguirai il tuo codice.
4. Familiarità di base con Java: una conoscenza generale della programmazione Java ti aiuterà a seguire senza problemi.
5. File PSD: tieni a portata di mano un paio di file PSD a scopo di test. Puoi crearne alcuni utilizzando Adobe Photoshop o scaricare file di esempio da Internet.
## Importa pacchetti
Prima di iniziare a scrivere codice, chiariamo quali pacchetti dobbiamo importare. Aspose.PSD ci consente di lavorare con i file Photoshop in vari modi, quindi prendiamo le classi necessarie per gestire le immagini PSD e i livelli di regolazione.
```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.adjustmentlayers.AdjustmentLayer;
```
Ora che abbiamo preparato i nostri pacchetti, analizziamo gli esempi passo dopo passo!
## Passaggio 1: carica il file PSD
Il primo passo del nostro viaggio è caricare il file PSD. Questo è il file con cui lavoreremo per applicare i nostri livelli di regolazione.
```java
String dataDir = "Your Document Directory";
String sourceFileName1 = dataDir + "ChannelMixerAdjustmentLayer.psd";
PsdImage im = (PsdImage) Image.load(sourceFileName1);
```
 In questo frammento definiamo la directory in cui si trovano i nostri file PSD e carichiamo il file specifico che vogliamo manipolare. Assicurati di sostituire`"Your Document Directory"` con il percorso effettivo dei file PSD sul tuo computer.
## Passaggio 2: iterazione sui livelli
Ora che abbiamo caricato il file PSD, vorremo scorrere i suoi livelli per trovare i nostri livelli di regolazione.
```java
for (int i = 0; i < im.getLayers().length; i++) {
    if (im.getLayers()[i] instanceof AdjustmentLayer) {
        AdjustmentLayer adjustmentLayer = (AdjustmentLayer) im.getLayers()[i];
        
        if (adjustmentLayer != null) {
            adjustmentLayer.mergeLayerTo(im.getLayers()[0]);
        }
    }
}
```
 In questo passaggio, esaminiamo ogni livello del file PSD per identificare quelli che appartengono a`AdjustmentLayer` tipo. Se ne troviamo uno, lo uniamo allo strato base, che solitamente è il primo strato (`im.getLayers()[0]`). Questo processo di fusione applica efficacemente gli aggiustamenti alla nostra immagine. 
## Passaggio 3: salva il file PSD modificato
Dopo aver modificato i livelli, è fondamentale salvare le modifiche apportate. Facciamolo nel passaggio successivo.
```java
String exportPath1 = dataDir + "ChannelMixerAdjustmentLayerChanged.psd";
im.save(exportPath1);
```
 Qui specifichiamo il percorso di esportazione per il nostro file PSD modificato e chiamiamo il file`save()` metodo per scrivere le nostre modifiche su disco.
## Passaggio 4: livello di regolazione dei livelli
Ripetiamo il processo per un diverso tipo di livello di regolazione: il livello di regolazione Livelli. 
### Carica il livello di regolazione dei livelli PSD
```java
String sourceFileName2 = dataDir + "LevelsAdjustmentLayerRgb.psd";
PsdImage img = (PsdImage) Image.load(sourceFileName2);
```
Come prima, carichiamo il file PSD contenente il nostro livello di regolazione Livelli. 
### Itera attraverso i livelli dei livelli
Successivamente, ripeteremo il ciclo tra i livelli, proprio come abbiamo fatto in precedenza, ma ora stiamo lavorando con un altro file PSD.
```java
for (int i = 0; i < img.getLayers().length; i++) {
    if (img.getLayers()[i] instanceof AdjustmentLayer) {
        AdjustmentLayer adjustmentLayer = (AdjustmentLayer) img.getLayers()[i];
        
        if (adjustmentLayer != null) {
            adjustmentLayer.mergeLayerTo(img.getLayers()[0]);
        }
    }
}
```
Questo codice agisce in modo simile all'iterazione precedente; cerca i livelli di regolazione all'interno del file PSD corrente, permettendoci di applicare eventuali regolazioni disponibili.
## Salva il PSD del livello di regolazione dei livelli
Infine, salveremo questo nuovo file dopo aver applicato le modifiche.
```java
String exportPath2 = dataDir + "LevelsAdjustmentLayerRgbChanged.psd";
img.save(exportPath2);
```
Ora abbiamo elaborato con successo il livello di regolazione Livelli!
## Conclusione
Congratulazioni! Hai appena imparato come applicare i livelli di regolazione nei file PSD utilizzando Java e la libreria Aspose.PSD. Che tu stia modificando i colori o regolando i livelli, ora disponi delle competenze fondamentali per manipolare i file PSD a livello di codice.
L'utilizzo di Aspose.PSD può semplificare in modo significativo i flussi di lavoro nell'editing delle immagini, consentendo l'automazione e la personalizzazione in modi che gli strumenti tradizionali potrebbero non fare. Non esitare a esplorare ulteriormente la libreria e sperimentare diversi tipi di livelli per vedere quali possibilità creative sono disponibili.
## Domande frequenti
### Cos'è la libreria Aspose.PSD?
Aspose.PSD è una libreria che consente agli sviluppatori di caricare, manipolare e salvare file PSD di Photoshop nelle applicazioni Java.
### Posso utilizzare Aspose.PSD gratuitamente?
 SÌ! Aspose offre una prova gratuita per esplorare la loro libreria. Puoi iscriverti[Qui](https://releases.aspose.com/).
### Ho bisogno di Photoshop installato per utilizzare Aspose.PSD?
No, non hai bisogno di Photoshop. Aspose.PSD funziona in modo indipendente per manipolare i file PSD a livello di codice.
### Dove posso trovare la documentazione per Aspose.PSD?
Puoi visitare la pagina della documentazione[Qui](https://reference.aspose.com/psd/java/) per esplorare caratteristiche, classi e metodi.
### Come posso ottenere supporto per i prodotti Aspose?
 È possibile accedere al supporto tramite il[Aspose forum](https://forum.aspose.com/c/psd/34) dove puoi porre domande e trovare soluzioni.