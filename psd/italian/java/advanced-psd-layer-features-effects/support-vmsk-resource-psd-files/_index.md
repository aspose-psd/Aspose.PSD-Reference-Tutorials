---
title: Supporta la risorsa Vmsk nei file PSD con Java
linktitle: Supporta la risorsa Vmsk nei file PSD con Java
second_title: API Java Aspose.PSD
description: Gestisci senza sforzo le risorse Vmsk nei file PSD utilizzando Aspose.PSD per Java. Un tutorial completo e passo passo, ideale sia per sviluppatori che per designer.
type: docs
weight: 23
url: /it/java/advanced-psd-layer-features-effects/support-vmsk-resource-psd-files/
---
## Introduzione
Quando si tratta di lavorare con file PSD (Photoshop Document), la gestione delle risorse è fondamentale, soprattutto quando si integrano funzionalità speciali come la risorsa Vmsk (Vector Mask). Le risorse Vmsk possono potenziare i progettisti aggiungendo forme vettoriali complesse, consentendo loro di creare grafica straordinaria senza sforzo. In questa guida, adotteremo un approccio pratico per mostrarti come supportare le risorse Vmsk nei file PSD utilizzando Aspose.PSD per Java. Che tu sia uno sviluppatore che cerca di migliorare la tua applicazione o un designer che cerca l'automazione, questo tutorial ti guiderà attraverso il processo passo dopo passo, rendendolo facile da seguire e implementare.
## Prerequisiti
Prima di immergerci nei dettagli succosi della gestione delle risorse Vmsk, assicuriamoci che tu abbia tutto pronto per un'esperienza senza interruzioni.
### Ciò di cui hai bisogno
-  Java Development Kit (JDK): assicurati di avere JDK installato sul tuo computer. In caso contrario, puoi scaricarlo da[Sito web dell'Oracle](https://www.oracle.com/java/technologies/javase-downloads.html).
- Aspose.PSD per Java Library: questa è una potente libreria per la gestione dei file PSD. Puoi scaricarlo da[Aspose la pagina di rilascio](https://releases.aspose.com/psd/java/) . Per chi vuole provare prima di acquistare, si può iniziare anche con il[prova gratuita](https://releases.aspose.com/).
- Un IDE: qualsiasi IDE per Java (come IntelliJ IDEA, Eclipse, ecc.) funzionerà per questo progetto.
### Impostazione dell'area di lavoro
1. Crea un nuovo progetto Java: avvia il tuo IDE preferito e crea un nuovo progetto Java. Questo è il tuo parco giochi per lavorare con il codice.
2. Aggiungi la libreria Aspose: dopo aver scaricato la libreria Aspose, aggiungi il file jar alle librerie del tuo progetto. Questo passaggio è cruciale in quanto ci consente di utilizzare tutte quelle dolci funzionalità di Aspose.PSD.
Con questi prerequisiti in atto, sei pronto per iniziare a creare, modificare e gestire file PSD con le risorse Vmsk. Entriamo subito nella programmazione!
## Importa pacchetti
Prima di poter lavorare sui file PSD, dobbiamo importare i pacchetti necessari. Questa è la spina dorsale del nostro codice, dandoci accesso a varie classi e metodi offerti dalla libreria Aspose.PSD.
```java
import com.aspose.psd.Image;
import com.aspose.psd.Point;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.Layer;
import com.aspose.psd.fileformats.psd.layers.LayerResource;
import com.aspose.psd.fileformats.psd.layers.layerresources.VmskResource;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.BezierKnotRecord;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.InitialFillRuleRecord;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.LengthRecord;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.PathFillRuleRecord;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.VectorPathType;
```
Ora che abbiamo preparato il terreno, è tempo di agire! In questa sezione suddivideremo il codice in passaggi gestibili. Questi passaggi ti guideranno nella lettura di un file PSD, nella gestione della risorsa Vmsk e persino nella modifica.
## Passaggio 1: carica il file PSD
La prima cosa che vuoi fare è caricare il tuo file PSD. È qui che inizia tutta la magia.
```java
String dataDir = "Your Document Directory"; // Aggiorna questo percorso
String sourceFileName = dataDir + "Rectangle.psd";
PsdImage im = (PsdImage) Image.load(sourceFileName);
```

-  Impostiamo il`dataDir` nella directory del file PSD. 
-  Creiamo una stringa per il`sourceFileName`, combinando la directory con il nome del file PSD.
-  Infine, carichiamo il file PSD in un file`PsdImage` oggetto utilizzando`Image.load()`.
## Passaggio 2: recuperare la risorsa Vmsk
Ora che abbiamo caricato la nostra immagine PSD, recuperiamo la risorsa Vmsk.
```java
VmskResource resource = getVmskResource(im);
```

-  Chiamiamo il`getVmskResource()` metodo che gestisce la ricerca e il recupero della risorsa Vmsk dall'immagine.
## Passaggio 3: convalidare le proprietà delle risorse Vmsk
Prima di procedere con le modifiche, è essenziale verificare che la nostra risorsa Vmsk sia nello stato previsto.
```java
if (resource.isDisabled() != false ||
	resource.isInverted() != false ||
	resource.isNotLinked() != false ||
	resource.getPaths().length != 7) {
	throw new RuntimeException("VmskResource was read wrong");
}
```

- Qui stiamo controllando varie proprietà della risorsa Vmsk. Vogliamo assicurarci che non sia disabilitato, invertito o non collegato e che abbia il giusto numero di percorsi.
## Passaggio 4: accedi a ciascun percorso e convalida
Scaviamo un po' più a fondo e ispezioniamo i percorsi all'interno della risorsa Vmsk.
```java
PathFillRuleRecord pathFillRule = (PathFillRuleRecord) resource.getPaths()[0];
InitialFillRuleRecord initialFillRule = (InitialFillRuleRecord) resource.getPaths()[1];
LengthRecord subpathLength = (LengthRecord) resource.getPaths()[2];
if (pathFillRule.getType() != VectorPathType.PathFillRuleRecord ||
	initialFillRule.getType() != VectorPathType.InitialFillRuleRecord ||
	initialFillRule.isFillStartsWithAllPixels() != false ||
	subpathLength.getType() != VectorPathType.ClosedSubpathLengthRecord ||
	subpathLength.isClosed() != true) {
	throw new RuntimeException("VmskResource paths were read wrong");
}
```

- Stiamo estraendo tre record di percorso specifici e convalidando i loro tipi e proprietà per garantire che soddisfino i nostri criteri.
## Passaggio 5: modifica la risorsa Vmsk
Ora stiamo entrando nella parte di modifica! Puoi modificare le proprietà della risorsa Vmsk secondo necessità.
```java
resource.setDisabled(true);
resource.setInverted(true);
resource.setNotLinked(true);
```

- In questo blocco, attiviamo/disattivamo varie proprietà della risorsa Vmsk. Impostandoli su true, possiamo controllare il comportamento della maschera nel file PSD.
## Passaggio 6: modifica i punti del nodo Bezier
nodi Bezier sono fondamentali per i percorsi vettoriali. Cambiamo alcuni valori qui.
```java
BezierKnotRecord bezierKnot = (BezierKnotRecord) resource.getPaths()[3];
bezierKnot.getPoints()[0] = new Point(0, 0);
bezierKnot = (BezierKnotRecord) resource.getPaths()[4];
bezierKnot.getPoints()[0] = new Point(8039797, 10905190);
```

-  Stiamo accedendo allo specifico`BezierKnotRecord` percorsi e modificandone i punti per rimodellare potenzialmente la maschera vettoriale.
## Passaggio 7: salva il file PSD modificato
Una volta completate tutte le modifiche, è il momento di salvare il file PSD modificato. 
```java
String exportPath = dataDir + "Rectangle_changed.psd";
im.save(exportPath);
```

-  Impostiamo il percorso per il file PSD esportato e quindi chiamiamo`im.save()` per scrivere le modifiche a questo nuovo file.
## Passaggio 8: ripulire le risorse
Infine, dobbiamo assicurarci di smaltire correttamente l'immagine per liberare risorse.
```java
im.dispose();
```

- È sempre una buona pratica smaltire le risorse una volta terminato. Ciò aiuta a evitare perdite di memoria nelle applicazioni.
## Conclusione
Congratulazioni! Hai appena seguito un processo dettagliato di supporto delle risorse Vmsk nei file PSD utilizzando Aspose.PSD per Java. Dal caricamento dell'immagine, al recupero e alla convalida della risorsa Vmsk, alla modifica delle sue proprietà e al salvataggio del PSD modificato, hai coperto gli elementi essenziali. Con queste competenze, puoi gestire e utilizzare in modo efficiente varie risorse all'interno dei file PSD, migliorando i tuoi progetti di progettazione grafica o gli script di automazione.
## Domande frequenti
### Cos'è una risorsa Vmsk?
Una risorsa Vmsk è una maschera vettoriale in un file PSD che consente forme vettoriali complesse e funzionalità di modifica.
### Posso utilizzare Aspose.PSD in un progetto Maven?
Sì, puoi includere Aspose.PSD come dipendenza nel tuo progetto Maven utilizzando le sue coordinate dal repository.
### In quale formato posso salvare i miei file PSD modificati?
Puoi salvarli nuovamente come file PSD o esportarli in altri formati come PNG, JPEG, ecc.
### È disponibile una prova gratuita per Aspose.PSD?
 Sì, puoi accedere a una prova gratuita di Aspose.PSD per testarne le funzionalità. Visita il[collegamento di prova gratuita](https://releases.aspose.com/).
### Come posso ottenere supporto per Aspose.PSD?
 Puoi unirti al[Aspose forum](https://forum.aspose.com/c/psd/34)per supporto e aiuto nella risoluzione dei problemi.