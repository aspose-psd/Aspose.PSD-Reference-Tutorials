---
date: 2026-09-23
description: Scopri come modificare le vector shapes PSD e processare in batch i file
  PSD usando Aspose.PSD for Java. Passaggi dettagliati, consigli e segnaposti di codice
  per una soluzione completa.
keywords:
- modify psd vector shapes
- batch process psd files
- Aspose.PSD Java
- vector shape editing
lastmod: 2026-09-23
linktitle: Supporta le proprietà dei dati Length Record in PSD - Java
og_description: Scopri come modificare le vector shapes PSD e processare in batch
  i file PSD usando Aspose.PSD for Java. Guida passo‑passo con segnaposti di codice
  e consigli esperti.
og_image_alt: Guide showing how to edit vector shapes in PSD files using Aspose.PSD
  for Java
og_title: Modifica le vector shapes PSD con Aspose.PSD for Java
schemas:
- author: Aspose
  dateModified: '2026-09-23'
  description: Learn how to modify PSD vector shapes and batch process PSD files using
    Aspose.PSD for Java. Detailed steps, tips, and code placeholders for a complete
    solution.
  headline: Modify PSD vector shapes with Aspose.PSD for Java
  type: TechArticle
- description: Learn how to modify PSD vector shapes and batch process PSD files using
    Aspose.PSD for Java. Detailed steps, tips, and code placeholders for a complete
    solution.
  name: Modify PSD vector shapes with Aspose.PSD for Java
  steps:
  - name: '**Java Development Kit (JDK)** – download from [Oracle''s website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html)
      or use your preferred package manager.'
    text: '**Java Development Kit (JDK)** – download from [Oracle''s website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html)
      or use your preferred package manager.'
  - name: '**Aspose.PSD for Java** – obtain the latest JAR from the [Aspose releases
      page](https://releases.aspose.com/psd/java/).'
    text: '**Aspose.PSD for Java** – obtain the latest JAR from the [Aspose releases
      page](https://releases.aspose.com/psd/java/).'
  - name: '**IDE** – IntelliJ IDEA, Eclipse, or any Java‑compatible editor.'
    text: '**IDE** – IntelliJ IDEA, Eclipse, or any Java‑compatible editor.'
  - name: '**A PSD file** – create one in Photoshop or grab a sample PSD to experiment
      with.'
    text: '**A PSD file** – create one in Photoshop or grab a sample PSD to experiment
      with.'
  - name: '**Basic Java knowledge** – familiarity with classes, objects, and exception
      handling.'
    text: '**Basic Java knowledge** – familiarity with classes, objects, and exception
      handling.'
  type: HowTo
- questions:
  - answer: The `VsmsResource` will be absent, so `resource` stays `null`. Add a check
      and skip the modification step or inform the user.
    question: How do I handle a PSD that contains no vector shape layers?
  - answer: Yes, `LengthRecord` provides setters for fill, stroke, and opacity. See
      the API docs for the full list.
    question: Can I change other properties like fill color or stroke width?
  - answer: Absolutely. Wrap the code inside a loop that iterates over a directory
      of PSD files, adjusting the input and output paths each time.
    question: Is it possible to batch‑process multiple PSD files?
  - answer: '`Image.load` handles file streams automatically, but if you load from
      an `InputStream`, remember to close it after use.'
    question: Do I need to close streams manually when loading from a file path?
  - answer: The `LengthRecord` and `PathOperations` classes have been available since
      Aspose.PSD 20.10. Using the latest version (24.11 at time of writing) is recommended.
    question: What version of Aspose.PSD is required for these APIs?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- modify psd vector shapes
- Aspose.PSD
- Java image processing
- batch PSD processing
title: Modifica le vector shapes PSD con Aspose.PSD for Java
url: /it/java/advanced-psd-layer-features-effects/support-length-record-data-properties-psd/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Modifica forme vettoriali PSD con Aspose.PSD per Java

## Introduzione
Se hai bisogno di **modificare forme vettoriali PSD** programmaticamente, Aspose.PSD per Java ti offre il pieno controllo sui file Photoshop direttamente dal tuo codice Java. Questo tutorial ti guida attraverso il supporto delle proprietà dei record di lunghezza — un passaggio essenziale quando si modificano i livelli di forme vettoriali. Alla fine sarai in grado di aprire un PSD, regolare i suoi dati di forma vettoriale e salvare il file aggiornato senza mai avviare Photoshop.

## Risposte rapide
- **Cosa significa “modify PSD vector shapes”?** Regolare la geometria, le operazioni di percorso o altri attributi dei livelli basati su vettori all'interno di un file PSD.  
- **Quale libreria gestisce questo?** Aspose.PSD for Java.  
- **Ho bisogno di una licenza?** Una versione di prova gratuita è sufficiente per la valutazione; è necessaria una licenza commerciale per la produzione.  
- **Quanto tempo richiede l'implementazione?** Circa 10‑15 minuti per uno script di base di modifica delle forme.  
- **Quali sono i prerequisiti principali?** Java JDK, Aspose.PSD per Java e un file PSD di esempio.

## Che cosa è “support length record properties”?
Il supporto delle proprietà dei record di lunghezza significa accedere e aggiornare gli oggetti `LengthRecord` che descrivono ogni percorso vettoriale all'interno di un PSD. Questi record memorizzano informazioni come la lunghezza del percorso, il tipo e come si unisce ad altri percorsi. Modificarli ti consente di controllare come le forme si combinano, si intersecano o si sottraggono l'una dall'altra, permettendo una modifica vettoriale precisa.

## Perché usare Aspose.PSD per Java per supportare le proprietà dei record di lunghezza?
Carica il tuo PSD, modifica i dati vettoriali e salva — tutto senza Photoshop. Aspose.PSD elabora PSD con centinaia di pagine in meno di 2 secondi su un server tipico, offre oltre 150 classi (incluse più di 30 tipologie relative ai vettori) e funziona su Windows, Linux o macOS con qualsiasi JDK 11+. Questa libreria focalizzata sulle prestazioni elimina la necessità di costosi software desktop.

## Prerequisiti
1. **Java Development Kit (JDK)** – scarica da [Oracle's website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html) o utilizza il tuo gestore di pacchetti preferito.  
2. **Aspose.PSD for Java** – ottieni l'ultimo JAR dalla [Aspose releases page](https://releases.aspose.com/psd/java/).  
3. **IDE** – IntelliJ IDEA, Eclipse o qualsiasi editor compatibile con Java.  
4. **Un file PSD** – creane uno in Photoshop o prendi un PSD di esempio per sperimentare.  
5. **Conoscenze di base di Java** – familiarità con classi, oggetti e gestione delle eccezioni.

## Importa pacchetti
Le istruzioni di importazione portano le classi principali di Aspose.PSD nello scope, come `PsdImage`, `VsmsResource` e `LengthRecord`.

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.LayerResource;
import com.aspose.psd.fileformats.psd.layers.layerresources.VsmsResource;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.LengthRecord;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.PathOperations;
```

## Passo 1: Configura le directory di origine e destinazione
Definisci dove si trova il PSD originale e dove verrà scritto il file modificato.

```java
String sourceDir = "Your Source Directory";
String outputDir = "Your Document Directory";
String inPsdFilePath = sourceDir + "PathOperationsShape.psd";
String outPsdFilePath = outputDir + "out_PathOperationsShape.psd";
```

## Passo 2: Carica il file PSD
Usa `Image.load` per aprire il file e castarlo a `PsdImage` per le funzionalità specifiche del PSD.

```java
PsdImage psdImage = (PsdImage) Image.load(inPsdFilePath);
```

## Passo 3: Individua la risorsa Vsms nel livello
`VsmsResource` è il contenitore che memorizza i dati delle forme vettoriali per un livello. Scorri le risorse del secondo livello per trovarla.

```java
VsmsResource resource = null;
for (LayerResource layerResource : psdImage.getLayers()[1].getResources()) {
    if (layerResource instanceof VsmsResource) {
        resource = (VsmsResource) layerResource;
        break;
    }
}
```

## Passo 4: Accedi ai record di lunghezza
`LengthRecord` rappresenta un percorso vettoriale distinto. Recupera i record che intendi modificare.

```java
LengthRecord lengthRecord0 = (LengthRecord) resource.getPaths()[2];
LengthRecord lengthRecord1 = (LengthRecord) resource.getPaths()[7];
LengthRecord lengthRecord2 = (LengthRecord) resource.getPaths()[11];
```

## Passo 5: Modifica le proprietà delle operazioni di percorso
`PathOperations` definisce come le singole forme interagiscono (ad esempio esclusione, intersezione, sottrazione). Modificando questi valori si aggiorna la composizione visiva del livello vettoriale.

```java
lengthRecord0.setPathOperations(PathOperations.ExcludeOverlappingShapes);
lengthRecord1.setPathOperations(PathOperations.IntersectShapeAreas);
lengthRecord2.setPathOperations(PathOperations.SubtractFrontShape);
```

## Passo 6: Salva il file PSD modificato
Salva le tue modifiche in un nuovo file.

```java
psdImage.save(outPsdFilePath);
```

## Passo 7: Pulisci le risorse
Disporre dell'istanza `PsdImage` per liberare memoria ed evitare perdite di risorse.

```java
psdImage.dispose();
```

## Come elaborare in batch file PSD con supporto alle proprietà dei record di lunghezza
Racchiudi il flusso di lavoro per un singolo file in un ciclo che itera su una directory di PSD, aggiornando `inPsdFilePath` e `outPsdFilePath` per ciascun file. Questo approccio ti consente di applicare le stesse regolazioni delle forme vettoriali a decine o centinaia di file in pochi minuti, ideale per pipeline di asset automatizzate.

## Problemi comuni e consigli
- **Controlli null** – verifica sempre che `resource` non sia `null` prima di accedere ai suoi membri.  
- **Limiti degli indici di percorso** – assicurati che gli indici che usi (ad es., `[2]`, `[7]`, `[11]`) esistano per il PSD specifico che stai modificando.  
- **Licenza** – eseguire senza una licenza valida inserisce una filigrana nel PSD salvato.  

## Conclusione
Ora hai un esempio completo, end‑to‑end, di come **modificare forme vettoriali PSD** supportando le proprietà dei record di lunghezza con Aspose.PSD per Java. Che tu stia automatizzando una pipeline di asset o costruendo uno strumento di design personalizzato, queste API ti offrono la flessibilità di manipolare i livelli vettoriali senza lavoro manuale su Photoshop. Sperimenta con altri valori di `PathOperations` o combina più modifiche di `LengthRecord` per creare forme complesse.

## Domande frequenti

**Q: Come gestire un PSD che non contiene livelli di forme vettoriali?**  
A: Il `VsmsResource` sarà assente, quindi `resource` rimane `null`. Aggiungi un controllo e salta il passo di modifica o informa l'utente.

**Q: Posso cambiare altre proprietà come il colore di riempimento o lo spessore del tratto?**  
A: Sì, `LengthRecord` fornisce i setter per riempimento, tratto e opacità. Consulta la documentazione API per l'elenco completo.

**Q: È possibile elaborare in batch più file PSD?**  
A: Assolutamente. Racchiudi il codice in un ciclo che itera su una directory di file PSD, regolando i percorsi di input e output ad ogni iterazione.

**Q: Devo chiudere manualmente gli stream quando carico da un percorso file?**  
A: `Image.load` gestisce gli stream dei file automaticamente, ma se carichi da un `InputStream`, ricorda di chiuderlo dopo l'uso.

**Q: Quale versione di Aspose.PSD è necessaria per queste API?**  
A: Le classi `LengthRecord` e `PathOperations` sono disponibili da Aspose.PSD 20.10. Si consiglia di utilizzare l'ultima versione (24.11 al momento della stesura).

---

**Ultimo aggiornamento:** 2026-09-23  
**Testato con:** Aspose.PSD for Java 24.11  
**Autore:** Aspose

## Tutorial correlati

- [Converti PSD in PNG e crea maschera vettoriale Java – Risorsa Vmsk nei file PSD](/psd/java/advanced-psd-layer-features-effects/support-vmsk-resource-psd-files/)
- [Converti PSD in PNG con supporto maschera di livello usando Aspose.PSD per Java](/psd/java/advanced-psd-layer-features-effects/support-layer-mask-psd-files/)
- [Aggiungi supporto livello ai file PSD](/psd/java/advanced-psd-layer-features-effects/add-layer-support-psd-files/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}