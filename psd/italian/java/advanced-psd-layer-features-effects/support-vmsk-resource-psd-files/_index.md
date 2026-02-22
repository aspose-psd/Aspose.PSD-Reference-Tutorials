---
date: 2026-02-22
description: Scopri come creare una maschera vettoriale in Java usando Aspose.PSD
  per Java, aggiungere una maschera vettoriale PSD e manipolare le risorse Vmsk programmaticamente.
linktitle: Create Vector Mask Java – Vmsk Resource in PSD Files
second_title: Aspose.PSD Java API
title: Crea maschera vettoriale Java – Risorsa Vmsk nei file PSD
url: /it/java/advanced-psd-layer-features-effects/support-vmsk-resource-psd-files/
weight: 23
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Crea Maschera Vettoriale Java – Risorsa Vmsk nei File PSD

## Introduzione
Se hai bisogno di **create vector mask** (Vmsk) resources all'interno dei file Photoshop (PSD), Aspose.PSD per Java ti offre un modo pulito e programmatico per farlo. Che tu stia costruendo uno strumento di automazione del design o aggiungendo supporto per maschere personalizzate a una pipeline grafica esistente, questo tutorial ti guida passo passo—caricando un PSD, leggendo la risorsa Vmsk, modificandone le proprietà e salvando il risultato. Alla fine, sarai a tuo agio nella gestione delle maschere vettoriali, nella conversione da PSD a PNG e nell'estendere il file con dati vettoriali aggiuntivi—tutto con le tecniche **create vector mask java**.

## Risposte Rapide
- **What is a Vmsk resource?** È il dato della maschera vettoriale memorizzato all'interno di un file PSD, che definisce forme vettoriali complesse per un livello.  
- **Which library supports it?** Aspose.PSD for Java fornisce pieno accesso in lettura/scrittura alle risorse Vmsk.  
- **Do I need a license?** È disponibile una prova gratuita; è necessaria una licenza commerciale per l'uso in produzione.  
- **Can I convert the edited PSD to PNG?** Sì—una volta salvato, puoi caricare il PSD e esportarlo in PNG con la stessa API.  
- **Is Maven support available?** Assolutamente; Aspose.PSD può essere aggiunto come dipendenza Maven (vedi la keyword “aspose psd maven”).

## Cos'è una Maschera Vettoriale (Risorsa Vmsk)?
Una maschera vettoriale (Vmsk) è una maschera non basata su pixel che utilizza curve Bézier e record di percorso per definire regioni trasparenti e opache su un livello. Poiché è basata su vettori, si scala senza perdita di qualità—perfetta per grafiche ad alta risoluzione.

## Perché Creare una Maschera Vettoriale con Aspose.PSD?
- **Automation:** Aggiungi o modifica maschere programmaticamente senza aprire Photoshop.  
- **Consistency:** Garantisce che ogni PSD generato segua le stesse regole di maschera.  
- **Cross‑platform:** Funziona su qualsiasi OS che supporta Java.  
- **Integration:** Combinala con altre API Aspose (ad es., convertire PSD → PNG) per flussi di lavoro end‑to‑end.  
- **Scalability:** Le maschere vettoriali rimangono nitide a qualsiasi dimensione, rendendole ideali per design responsivi.

## Perché Questo è Importante per gli Sviluppatori Java
Utilizzare le tecniche **create vector mask java** ti consente di incorporare logica grafica sofisticata direttamente nei servizi back‑end, nelle pipeline CI o nelle utility desktop. Non avrai più bisogno di un designer per aggiungere manualmente le maschere; il tuo codice può generarle o modificarle al volo, risparmiando tempo e riducendo gli errori umani.

## Prerequisiti
Prima di immergerci nel codice, assicurati di avere quanto segue:

### Cosa Serve
- Java Development Kit (JDK): Assicurati di avere il JDK installato sulla tua macchina. In caso contrario, puoi scaricarlo dal [sito Oracle](https://www.oracle.com/java/technologies/javase-downloads.html).
- Aspose.PSD for Java Library: È una libreria potente per gestire i file PSD. Puoi scaricarla dalla [pagina di rilascio Aspose](https://releases.aspose.com/psd/java/). Per chi vuole provare prima di acquistare, è possibile iniziare con la [prova gratuita](https://releases.aspose.com/).
- Un IDE: Qualsiasi IDE per Java (come IntelliJ IDEA, Eclipse, ecc.) funzionerà per questo progetto.

### Configurazione dell'Ambiente di Lavoro
1. **Create a New Java Project** – Apri il tuo IDE preferito e avvia un nuovo progetto.  
2. **Add the Aspose Library** – Dopo aver scaricato il JAR di Aspose, aggiungilo al percorso di compilazione del tuo progetto così potrai accedere a tutte le classi relative ai PSD.

Con l'ambiente pronto, passiamo all'implementazione reale.

## Come creare una maschera vettoriale nei file PSD con Java
Di seguito trovi una guida passo‑passo. I blocchi di codice sono invariati rispetto al tutorial originale; abbiamo solo aggiunto testo esplicativo per rendere ogni passaggio chiaro come il cristallo.

### Importa Pacchetti
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

Ora che abbiamo impostato il contesto, esaminiamo ogni operazione.

### Passo 1: Carica il Tuo File PSD
La prima cosa da fare è caricare il tuo file PSD. È qui che inizia tutta la magia.

```java
String dataDir = "Your Document Directory"; // Update this path
String sourceFileName = dataDir + "Rectangle.psd";
PsdImage im = (PsdImage) Image.load(sourceFileName);
```

- Impostiamo `dataDir` sulla directory del tuo file PSD.  
- Creiamo una stringa per `sourceFileName`, combinando la directory con il nome del file PSD.  
- Infine, carichiamo il file PSD in un oggetto `PsdImage` usando `Image.load()`.

### Passo 2: Recupera la Risorsa Vmsk
Ora che abbiamo caricato l'immagine PSD, recuperiamo la risorsa Vmsk.

```java
VmskResource resource = getVmskResource(im);
```

- Chiamiamo il metodo `getVmskResource()` che gestisce la ricerca e il recupero della risorsa Vmsk dall'immagine.

### Passo 3: Convalida le Proprietà della Risorsa Vmsk
Prima di procedere con le modifiche, è essenziale convalidare che la nostra risorsa Vmsk sia nello stato previsto.

```java
if (resource.isDisabled() != false ||
	resource.isInverted() != false ||
	resource.isNotLinked() != false ||
	resource.getPaths().length != 7) {
	throw new RuntimeException("VmskResource was read wrong");
}
```

- Qui stiamo controllando varie proprietà della risorsa Vmsk. Vogliamo assicurarci che non sia disabilitata, invertita o non collegata, e che abbia il numero corretto di percorsi.

### Passo 4: Accedi a Ogni Percorso e Convalidalo
Approfondiamo un po' e ispezioniamo i percorsi all'interno della risorsa Vmsk.

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

- Stiamo estraendo tre record di percorso specifici e convalidando i loro tipi e proprietà per assicurarci che soddisfino i nostri criteri.

### Passo 5: Modifica la Risorsa Vmsk
Ora entriamo nella fase di modifica! Puoi regolare le proprietà della risorsa Vmsk secondo necessità.

```java
resource.setDisabled(true);
resource.setInverted(true);
resource.setNotLinked(true);
```

- In questo blocco, stiamo attivando/disattivando varie proprietà della risorsa Vmsk. Impostandole su `true`, possiamo controllare il comportamento della maschera nel file PSD.

### Passo 6: Modifica i Punti dei Nodi Bézier
I nodi Bézier sono fondamentali per i percorsi vettoriali. Modifichiamo alcuni valori qui.

```java
BezierKnotRecord bezierKnot = (BezierKnotRecord) resource.getPaths()[3];
bezierKnot.getPoints()[0] = new Point(0, 0);
bezierKnot = (BezierKnotRecord) resource.getPaths()[4];
bezierKnot.getPoints()[0] = new Point(8039797, 10905190);
```

- Stiamo accedendo a percorsi specifici `BezierKnotRecord` e modificando i loro punti per potenzialmente rimodellare la maschera vettoriale.

### Passo 7: Salva il File PSD Modificato
Una volta completate tutte le modifiche, è il momento di salvare il file PSD modificato.

```java
String exportPath = dataDir + "Rectangle_changed.psd";
im.save(exportPath);
```

- Impostiamo il percorso per il file PSD esportato e poi chiamiamo `im.save()` per scrivere le modifiche in questo nuovo file.

### Passo 8: Pulisci le Risorse
Infine, dobbiamo assicurarci di liberare correttamente l'immagine per rilasciare le risorse.

```java
im.dispose();
```

- È sempre una buona pratica liberare qualsiasi risorsa una volta terminato. Questo aiuta a evitare perdite di memoria nelle tue applicazioni.

## Problemi Comuni e Soluzioni
| Issue | Why it Happens | How to Fix |
|-------|----------------|------------|
| **`VmskResource` not found** | Il PSD non contiene un livello di maschera vettoriale. | Verifica che il PSD di origine abbia una maschera vettoriale o aggiungine una manualmente in Photoshop prima di eseguire il codice. |
| **`ArrayIndexOutOfBoundsException` on path access** | Il numero previsto di record di percorso è diverso. | Ispeziona `resource.getPaths().length` e regola l'uso degli indici di conseguenza. |
| **License exception** | Esecuzione senza una licenza valida di Aspose.PSD. | Applica una licenza di prova o acquistata usando `License license = new License(); license.setLicense("Aspose.PSD.lic");`. |
| **Memory leak** | Immagine non liberata in processi a lunga esecuzione. | Chiama sempre `im.dispose()` in un blocco `finally` o usa try‑with‑resources se supportato. |

## Domande Frequenti

**Q: Come aggiungo una nuova maschera vettoriale a un livello esistente?**  
A: Crea un `VmskResource`, popolalo con i record di percorso richiesti (ad es., `BezierKnotRecord`) e allegalo alla collezione delle risorse del livello.

**Q: Posso convertire il PSD modificato direttamente in PNG senza aprire Photoshop?**  
A: Sì—dopo aver salvato il PSD, ricaricalo con `Image.load()` e chiama `im.save("output.png")` specificando il formato PNG.

**Q: Esiste un modo per automatizzare questo in una pipeline CI/CD?**  
A: Assolutamente. Poiché il processo è puro Java, puoi integrarlo in build Maven/Gradle, contenitori Docker o qualsiasi sistema CI che supporti Java.

**Q: Quali versioni di Aspose.PSD sono compatibili con Java 11+?**  
A: Tutte le versioni recenti (2024‑2025) supportano Java 8 e successive, inclusi Java 11, 17 e le versioni LTS più recenti.

**Q: È necessaria una licenza per le build di sviluppo?**  
A: Una licenza di valutazione gratuita è sufficiente per sviluppo e test. Per le distribuzioni in produzione è richiesta una licenza commerciale.

---

**Ultimo Aggiornamento:** 2026-02-22  
**Testato Con:** Aspose.PSD 24.11 for Java  
**Autore:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}