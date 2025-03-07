---
title: Aggiungi l'effetto del livello ombra interno in PSD con Java
linktitle: Aggiungi l'effetto del livello ombra interno in PSD con Java
second_title: API Java Aspose.PSD
description: Scopri come aggiungere un effetto ombra interna ai file PSD utilizzando Aspose.PSD per Java con questo tutorial passo passo, inclusi suggerimenti e best practice.
weight: 12
url: /it/java/advanced-psd-layer-features-effects/add-inner-shadow-layer-effect-psd/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aggiungi l'effetto del livello ombra interno in PSD con Java

## Introduzione
Sei pronto a tuffarti nel mondo della programmazione del graphic design? Se hai mai desiderato manipolare i file PSD in modo programmatico, sei nel posto giusto! Oggi esploreremo come aggiungere un effetto di livello ombra interno a un PSD (documento Photoshop) utilizzando Aspose.PSD per Java. Questa potente libreria consente agli sviluppatori Java di lavorare in modo efficiente con i file PSD, consentendo una vasta gamma di manipolazioni delle immagini, da semplici modifiche a effetti complessi.
## Prerequisiti
Prima di addentrarci nella codifica, vediamo la configurazione. Ecco cosa devi avere a disposizione:
1.  Java Development Kit (JDK): assicurati di avere JDK installato sul tuo sistema. È essenziale per compilare ed eseguire il codice Java. Se non lo hai ancora, puoi scaricarlo dal[Sito web dell'Oracle](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).
2. Libreria Aspose.PSD: avrai bisogno dell'accesso alla libreria Aspose.PSD. Puoi scaricarlo facilmente da[Rilasci Aspose](https://releases.aspose.com/psd/java/). È uno strumento robusto per gestire i file PSD, quindi assicurati di procurarti la versione più recente.
3. Un ambiente di sviluppo integrato (IDE): sebbene sia possibile utilizzare qualsiasi editor di testo, è consigliabile utilizzare un IDE come IntelliJ IDEA, Eclipse o NetBeans. Questi forniscono funzionalità utili come l'evidenziazione della sintassi e strumenti di debug.
4. Conoscenza di base di Java: la familiarità con le nozioni di base di Java come variabili, classi e metodi ti aiuterà a seguire senza problemi.
5. File PSD di esempio: per testare il codice, assicurati di avere un file PSD di esempio. Puoi crearne uno in Adobe Photoshop o scaricare un campione gratuito online.
## Importa pacchetti
Una volta che tutto è configurato e pronto per l'uso, il primo passo è importare i pacchetti necessari nella tua classe Java. Questo è fondamentale per accedere alle funzioni Aspose.PSD. 
## Importa i pacchetti richiesti
```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.Layer;
import com.aspose.psd.fileformats.psd.layers.layereffects.IShadowEffect;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
import com.aspose.psd.imageoptions.PsdOptions;
```
In queste righe, stiamo introducendo le classi di cui abbiamo bisogno dalla libreria Aspose.
Ora che abbiamo importato i nostri pacchetti e configurato il nostro ambiente, passiamo al nocciolo della questione del codice. Lo suddividerò in passaggi gestibili.
## Passaggio 1: definire le directory
In questo passaggio specificheremo dove si trova il nostro file PSD sorgente e dove vogliamo salvare la versione modificata. 
```java
String sourceDir = "Your Source Directory";
String outputDir = "Your Document Directory";
String sourceFile = sourceDir + "sample.psd";
String destName = outputDir + "sample_out.psd";
```
 Sostituire`"Your Source Directory"` E`"Your Document Directory"` con i percorsi effettivi sul tuo computer. Qui è dove dici al tuo programma dove cercare il file PSD e dove salvare la nuova versione.
## Passaggio 2: carica il file PSD
 Successivamente, dobbiamo caricare il file PSD esistente in un file`PsdImage` oggetto. Configureremo anche le opzioni di caricamento per includere effetti.
```java
PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);
PsdImage image = (PsdImage) Image.load(sourceFile, loadOptions);
```
 Qui stiamo creando un'istanza di`PsdLoadOptions` , configurandolo per caricare le risorse degli effetti e quindi caricando il nostro file PSD di esempio in un oggetto chiamato`image`. È come aprire un libro prima di leggerlo!
## Passaggio 3: accedi al livello per l'effetto
Ora accediamo all'ultimo livello del nostro file PSD (supponendo che sia quello a cui vogliamo applicare il nostro effetto).
```java
try {
    Layer layer = image.getLayers()[image.getLayers().length - 1];
```
Questa linea accede all'ultimo livello della nostra immagine PSD. In Photoshop, i livelli sono come fogli trasparenti impilati uno sopra l'altro e quello più in alto è spesso quello che vedi per primo.
## Passaggio 4: configura l'effetto ombra interna
Questo frammento di codice applicherà l'effetto ombra interna al nostro livello. 
```java
    IShadowEffect shadowEffect = (IShadowEffect) layer.getBlendingOptions().getEffects()[0];
    shadowEffect.setColor(Color.getGreen());
    shadowEffect.setOpacity((byte) 128);
    shadowEffect.setDistance(1);
    shadowEffect.setUseGlobalLight(false);
    shadowEffect.setSize(2);
    shadowEffect.setAngle(45);
    shadowEffect.setSpread(50);
    shadowEffect.setNoise(5);
```
Ecco dove avviene la magia! Questo codice cattura l'effetto ombra dalle opzioni di fusione del livello e ne regola le proprietà:
- Colore: imposta l'ombra sul verde.
- Opacità: lo rende semitrasparente.
- Distanza: sposta leggermente l'ombra dal bordo del livello.
- Dimensione: determina quanto è grande l'ombra.
- Angolo: specifica la direzione della sorgente luminosa.
- Diffusione e rumore: apri opzioni creative per l'aspetto dell'ombra.
## Passaggio 5: salva il PSD modificato
Una volta applicate tutte le impostazioni, il passaggio successivo è salvare il nostro file PSD modificato.
```java
    image.save(destName, new PsdOptions(image));
```
Questa riga salva le nostre modifiche. Il file di output viene denominato`sample_out.psd`e include tutti gli effetti appena applicati. È come fare clic su "Salva" in Photoshop dopo aver apportato le modifiche.
## Passaggio 6: ripulire le risorse
Infine, ci assicureremo di liberare tutte le risorse che abbiamo utilizzato.
```java
} finally {
    image.dispose();
}
```
 Questa è una buona pratica per prevenire perdite di memoria. Smaltendo il`image` oggetto, ci assicuriamo che la nostra applicazione funzioni in modo fluido ed efficiente.
## Conclusione
Ed ecco qua! In pochi semplici passaggi, hai imparato come aggiungere un effetto ombra interna ai livelli in un file PSD utilizzando Aspose.PSD per Java. Questa libreria offre fantastiche funzionalità per chiunque desideri automatizzare le attività di progettazione grafica o integrare funzionalità di manipolazione delle immagini nelle proprie applicazioni Java. 

## Domande frequenti
### Cos'è Aspose.PSD?  
Aspose.PSD è una libreria Java per lavorare con file PSD, che consente agli sviluppatori di manipolare gli effetti dei livelli, le maschere e le proprietà dell'immagine a livello di codice.
### Ho bisogno di Photoshop per utilizzare Aspose.PSD?  
No, non è necessario Photoshop per utilizzare Aspose.PSD. La libreria funziona in modo indipendente per la manipolazione dei file PSD.
### Posso applicare più effetti allo stesso livello?  
Assolutamente! Puoi applicare più effetti accedendo a ciascun tipo di effetto in modo simile a come abbiamo avuto accesso all'effetto ombra interna.
### Aspose.PSD è gratuito?  
Aspose.PSD è un prodotto commerciale; tuttavia, puoi utilizzare una prova gratuita disponibile tramite Aspose.
### Dove posso trovare ulteriore documentazione?  
 È possibile trovare la documentazione completa per Aspose.PSD[Qui](https://reference.aspose.com/psd/java/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
