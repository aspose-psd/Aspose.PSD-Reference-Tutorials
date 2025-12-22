---
date: 2025-12-18
description: Scopri come creare una maschera vettoriale (risorsa Vmsk) nei file PSD
  utilizzando Aspose.PSD per Java. Questo tutorial passo‑passo ti mostra come aggiungere
  una maschera vettoriale, convertire un PSD in PNG e molto altro.
linktitle: Create Vector Mask (Vmsk Resource) in PSD Files with Java
second_title: Aspose.PSD Java API
title: Crea maschera vettoriale (risorsa Vmsk) nei file PSD con Java
url: /it/java/advanced-psd-layer-features-effects/support-vmsk-resource-psd-files/
weight: 23
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Creare una Maschera Vettoriale (Risorsa Vmsk) nei File PSD con Java

## Introduzione
Se devi **creare una maschera vettoriale** (Vmsk) all'interno di file Photoshop (PSD), Aspose.PSD per Java ti offre un modo pulito e programmatico per farlo. Che tu stia costruendo uno strumento di automazione del design o aggiungendo supporto per maschere personalizzate a una pipeline grafica esistente, questo tutorial ti guida passo passo—caricamento del PSD, lettura della risorsa Vmsk, modifica delle sue proprietà e salvataggio del risultato. Alla fine, sarai a tuo agio nella gestione delle maschere vettoriali, nella conversione da PSD a PNG e nell'estensione del file con dati vettoriali aggiuntivi.

## Risposte Rapide
- **Che cos'è una risorsa Vmsk?** È il dato della maschera vettoriale memorizzato all'interno di un file PSD, che definisce forme vettoriali complesse per un livello.  
- **Quale libreria la supporta?** Aspose.PSD per Java fornisce pieno accesso in lettura/scrittura alle risorse Vmsk.  
- **È necessaria una licenza?** È disponibile una prova gratuita; per l'uso in produzione è richiesta una licenza commerciale.  
- **Posso convertire il PSD modificato in PNG?** Sì—una volta salvato, puoi caricare il PSD ed esportarlo in PNG con la stessa API.  
- **È disponibile il supporto Maven?** Assolutamente; Aspose.PSD può essere aggiunto come dipendenza Maven (vedi la keyword “aspose psd maven”).

## Che cos'è una Maschera Vettoriale (Risorsa Vmsk)?
Una maschera vettoriale (Vmsk) è una maschera non basata su pixel che utilizza curve Bézier e record di percorso per definire regioni trasparenti e opache su un livello. Poiché è basata su vettori, si scala senza perdita di qualità—perfetta per grafiche ad alta risoluzione.

## Perché Creare una Maschera Vettoriale con Aspose.PSD?
- **Automazione:** Aggiungi o modifica maschere programmaticamente senza aprire Photoshop.  
- **Coerenza:** Garantisce che ogni PSD generato segua le stesse regole di mascheratura.  
- **Cross‑platform:** Funziona su qualsiasi OS che supporta Java.  
- **Integrazione:** Combinala con altre API Aspose (ad es., convertire PSD → PNG) per flussi di lavoro end‑to‑end.

## Prerequisiti
Prima di immergerci nel codice, assicurati di avere quanto segue:

### Cosa Ti Serve
- Java Development Kit (JDK): Assicurati di avere il JDK installato sulla tua macchina. In caso contrario, puoi scaricarlo dal [sito Oracle](https://www.oracle.com/java/technologies/javase-downloads.html).
- Libreria Aspose.PSD per Java: È una libreria potente per gestire file PSD. Puoi scaricarla dalla [pagina di rilascio Aspose](https://releases.aspose.com/psd/java/). Per chi vuole provare prima di acquistare, è disponibile anche la [prova gratuita](https://releases.aspose.com/).
- Un IDE: Qualsiasi IDE per Java (come IntelliJ IDEA, Eclipse, ecc.) funzionerà per questo progetto.

### Configurazione dell'Ambiente di Lavoro
1. **Crea un Nuovo Progetto Java** – Apri il tuo IDE preferito e avvia un nuovo progetto.  
2. **Aggiungi la Libreria Aspose** – Dopo aver scaricato il JAR di Aspose, aggiungilo al percorso di compilazione del progetto così da poter accedere a tutte le classi relative a PSD.

Con l'ambiente pronto, passiamo all'implementazione vera e propria.

## Come creare una maschera vettoriale nei file PSD con Java
Di seguito trovi una guida passo‑a‑passo. I blocchi di codice rimangono invariati rispetto al tutorial originale; abbiamo solo aggiunto testo esplicativo per rendere ogni passaggio più chiaro.

## Importare i Pacchetti
Prima di poter lavorare sui file PSD, dobbiamo importare le classi necessarie dalla libreria Aspose.PSD.

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

Ora che abbiamo impostato il contesto, procediamo con ogni operazione.

## Passo 1: Caricare il Tuo File PSD
La prima cosa da fare è caricare il file PSD. È qui che inizia tutta la magia.

```java
String dataDir = "Your Document Directory"; // Update this path
String sourceFileName = dataDir + "Rectangle.psd";
PsdImage im = (PsdImage) Image.load(sourceFileName);
```

- Impostiamo `dataDir` sulla directory del tuo file PSD.  
- Creiamo una stringa per `sourceFileName`, combinando la directory con il nome del file PSD.  
- Infine, carichiamo il file PSD in un oggetto `PsdImage` usando `Image.load()`.

## Passo 2: Recuperare la Risorsa Vmsk
Ora che l’immagine PSD è caricata, recuperiamo la risorsa Vmsk.

```java
VmskResource resource = getVmskResource(im);
```

- Chiamiamo il metodo `getVmskResource()` che si occupa di cercare e restituire la risorsa Vmsk dall’immagine.

## Passo 3: Convalidare le Proprietà della Risorsa Vmsk
Prima di procedere con le modifiche, è fondamentale verificare che la risorsa Vmsk sia nello stato previsto.

```java
if (resource.isDisabled() != false ||
	resource.isInverted() != false ||
	resource.isNotLinked() != false ||
	resource.getPaths().length != 7) {
	throw new RuntimeException("VmskResource was read wrong");
}
```

- Qui controlliamo varie proprietà della risorsa Vmsk. Vogliamo assicurarci che non sia disabilitata, invertita o non collegata, e che abbia il numero corretto di percorsi.

## Passo 4: Accedere a Ogni Percorso e Convalidare
Andiamo più in profondità e ispezioniamo i percorsi all’interno della risorsa Vmsk.

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

- Estriamo tre record di percorso specifici e ne convalidiamo i tipi e le proprietà per garantire che soddisfino i nostri criteri.

## Passo 5: Modificare la Risorsa Vmsk
Ora entriamo nella fase di modifica! Puoi regolare le proprietà della risorsa Vmsk secondo le necessità.

```java
resource.setDisabled(true);
resource.setInverted(true);
resource.setNotLinked(true);
```

- In questo blocco, attiviamo varie proprietà della risorsa Vmsk. Impostandole su `true`, controlliamo il comportamento della maschera nel file PSD.

## Passo 6: Modificare i Punti dei Nodi Bézier
I nodi Bézier sono fondamentali per i percorsi vettoriali. Cambiamo alcuni valori.

```java
BezierKnotRecord bezierKnot = (BezierKnotRecord) resource.getPaths()[3];
bezierKnot.getPoints()[0] = new Point(0, 0);
bezierKnot = (BezierKnotRecord) resource.getPaths()[4];
bezierKnot.getPoints()[0] = new Point(8039797, 10905190);
```

- Accediamo a percorsi specifici `BezierKnotRecord` e ne modifichiamo i punti per potenzialmente rimodellare la maschera vettoriale.

## Passo 7: Salvare il File PSD Modificato
Una volta completate tutte le modifiche, è il momento di salvare il file PSD modificato.

```java
String exportPath = dataDir + "Rectangle_changed.psd";
im.save(exportPath);
```

- Impostiamo il percorso per il file PSD esportato e poi chiamiamo `im.save()` per scrivere le modifiche in questo nuovo file.

## Passo 8: Pulire le Risorse
Infine, dobbiamo assicurarci di liberare correttamente l’immagine per rilasciare le risorse.

```java
im.dispose();
```

- È sempre buona pratica eliminare qualsiasi risorsa una volta terminato. Questo aiuta a evitare perdite di memoria nelle tue applicazioni.

## Conclusione
Congratulazioni! Hai appena seguito un processo dettagliato per **creare una maschera vettoriale** (Vmsk) nei file PSD usando Aspose.PSD per Java. Dalla lettura dell’immagine, al recupero e alla convalida della risorsa Vmsk, alla modifica delle sue proprietà, fino al salvataggio del PSD modificato, ora possiedi una solida base per automatizzare i flussi di lavoro delle maschere vettoriali. Usa queste tecniche per arricchire le tue pipeline di design, integrarle con altre API Aspose (come la conversione PSD → PNG) o costruire strumenti grafici personalizzati.

## Domande Frequenti
**D: Come aggiungo una nuova maschera vettoriale a un livello esistente?**  
R: Crea un `VmskResource`, popolalo con i record di percorso richiesti (ad es., `BezierKnotRecord`) e allegalo alla collezione di risorse del livello.

**D: Posso convertire il PSD modificato direttamente in PNG senza aprire Photoshop?**  
R: Sì—dopo aver salvato il PSD, ricaricalo con `Image.load()` e chiama `im.save("output.png")` specificando il formato PNG.

**D: È possibile automatizzare questo processo in una pipeline CI/CD?**  
R: Assolutamente. Poiché il processo è puro Java, puoi integrarlo in build Maven/Gradle, container Docker o qualsiasi sistema CI che supporti Java.

**D: Quali versioni di Aspose.PSD sono compatibili con Java 11+?**  
R: Tutte le versioni recenti (2024‑2025) supportano Java 8 e versioni successive, inclusi Java 11, 17 e le più recenti LTS.

**D: È necessaria una licenza per le build di sviluppo?**  
R: Una licenza di valutazione gratuita è sufficiente per sviluppo e test. Per distribuzioni in produzione è richiesta una licenza commerciale.

---

**Ultimo aggiornamento:** 2025-12-18  
**Testato con:** Aspose.PSD 24.11 per Java  
**Autore:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
