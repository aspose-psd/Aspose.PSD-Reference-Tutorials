---
date: 2025-12-17
description: Scopri come modificare le forme vettoriali PSD supportando le proprietà
  dei dati del record di lunghezza utilizzando Aspose.PSD per Java. Guida passo‑passo
  con esempi di codice.
linktitle: Support Length Record Data Properties in PSD - Java
second_title: Aspose.PSD Java API
title: Come modificare le forme vettoriali PSD – Supportare le proprietà dei dati
  del record di lunghezza in Java
url: /it/java/advanced-psd-layer-features-effects/support-length-record-data-properties-psd/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Supporto alle proprietà dei dati di registro di lunghezza in PSD - Java

## Introduzione
Se hai bisogno di **modificare le forme vettoriali PSD** in modo programmatico, la libreria Aspose.PSD per Java ti offre il pieno controllo sui file Photoshop direttamente dal tuo codice Java. In questo tutorial vedremo tutto ciò che devi sapere per supportare le proprietà dei dati di registro di lunghezza—un passaggio fondamentale quando vuoi modificare i livelli di forme vettoriali. Alla fine, sarai in grado di aprire un PSD, regolare le sue proprietà di forma vettoriale e salvare il file aggiornato senza mai uscire dal tuo IDE. Iniziamo!

## Risposte rapide
- **Cosa significa “modificare le forme vettoriali PSD”?** Regolare la geometria, le operazioni di percorso o altre proprietà dei livelli basati su vettori all'interno di un file PSD.  
- **Quale libreria gestisce questo?** Aspose.PSD per Java.  
- **È necessaria una licenza?** Una versione di prova gratuita è sufficiente per la valutazione; è richiesta una licenza commerciale per la produzione.  
- **Quanto tempo richiede l'implementazione?** Circa 10‑15 minuti per uno script di modifica di base delle forme.  
- **Quali sono i requisiti principali?** Java JDK, Aspose.PSD per Java e un file PSD di esempio.

## Cos'è “modificare le forme vettoriali PSD”?
Modificare le forme vettoriali PSD comporta la modifica dei dati di percorso vettoriale sottostanti—come i record di lunghezza e le operazioni di percorso—così che l'aspetto visivo delle forme venga aggiornato di conseguenza. Questo è particolarmente utile per pipeline grafiche automatizzate, elaborazione batch o strumenti di design personalizzati.

## Perché usare Aspose.PSD per Java per modificare le forme vettoriali PSD?
- **Nessun Photoshop richiesto** – lavora direttamente con i file PSD su qualsiasi server.  
- **API ricca** – accedi a livelli, risorse e dati vettoriali con classi tipizzate.  
- **Cross‑platform** – funziona su Windows, Linux o macOS con qualsiasi JDK.  
- **Ottimizzata per le prestazioni** – gestione efficiente della memoria e operazioni di salvataggio rapide.

## Prerequisiti
1. **Java Development Kit (JDK)** – scaricalo dal [sito di Oracle](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html) o usa il tuo gestore di pacchetti preferito.  
2. **Aspose.PSD per Java** – ottieni l'ultimo JAR dalla [pagina di rilascio di Aspose](https://releases.aspose.com/psd/java/).  
3. **IDE** – IntelliJ IDEA, Eclipse o qualsiasi editor compatibile con Java.  
4. **Un file PSD** – creane uno in Photoshop o prendi un PSD di esempio per sperimentare.  
5. **Conoscenze di base di Java** – familiarità con classi, oggetti e gestione delle eccezioni.

## Importare i pacchetti
Per prima cosa, importa le classi necessarie per lavorare con i file PSD e le risorse delle forme vettoriali.

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.LayerResource;
import com.aspose.psd.fileformats.psd.layers.layerresources.VsmsResource;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.LengthRecord;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.PathOperations;
```

## Passo 1: Configurare le directory di origine e destinazione
Definisci dove si trova il PSD originale e dove vuoi salvare il file modificato.

```java
String sourceDir = "Your Source Directory";
String outputDir = "Your Document Directory";
String inPsdFilePath = sourceDir + "PathOperationsShape.psd";
String outPsdFilePath = outputDir + "out_PathOperationsShape.psd";
```

## Passo 2: Caricare il file PSD
Usa `Image.load` per aprire il file e castalo a `PsdImage` per le funzionalità specifiche di PSD.

```java
PsdImage psdImage = (PsdImage) Image.load(inPsdFilePath);
```

## Passo 3: Individuare la risorsa Vsms nel livello
I dati della forma vettoriale risiedono all'interno di una `VsmsResource`. Scorri le risorse del secondo livello per trovarla.

```java
VsmsResource resource = null;
for (LayerResource layerResource : psdImage.getLayers()[1].getResources()) {
    if (layerResource instanceof VsmsResource) {
        resource = (VsmsResource) layerResource;
        break;
    }
}
```

## Passo 4: Accedere ai record di lunghezza
Ogni `LengthRecord` rappresenta un percorso vettoriale distinto. Recupera quelli che intendi modificare.

```java
LengthRecord lengthRecord0 = (LengthRecord) resource.getPaths()[2];
LengthRecord lengthRecord1 = (LengthRecord) resource.getPaths()[7];
LengthRecord lengthRecord2 = (LengthRecord) resource.getPaths()[11];
```

## Passo 5: Modificare le proprietà delle operazioni di percorso
Ora puoi **modificare le forme vettoriali PSD** cambiando le loro `PathOperations`. Questo determina come le forme interagiscono (ad esempio esclusione, intersezione, sottrazione).

```java
lengthRecord0.setPathOperations(PathOperations.ExcludeOverlappingShapes);
lengthRecord1.setPathOperations(PathOperations.IntersectShapeAreas);
lengthRecord2.setPathOperations(PathOperations.SubtractFrontShape);
```

## Passo 6: Salvare il file PSD modificato
Persisti le modifiche in un nuovo file.

```java
psdImage.save(outPsdFilePath);
```

## Passo 7: Pulire le risorse
Rilascia il `PsdImage` per liberare la memoria.

```java
psdImage.dispose();
```

## Problemi comuni e consigli
- **Controlli null** – verifica sempre che `resource` non sia `null` prima di accedere ai percorsi.  
- **Limiti degli indici di percorso** – assicurati che gli indici usati (`[2]`, `[7]`, `[11]`) esistano nel PSD specifico che stai modificando.  
- **Licenza** – l'esecuzione senza licenza valida inserirà una filigrana nel PSD salvato.  

## Conclusione
Ora disponi di un esempio completo, end‑to‑end, su come **modificare le forme vettoriali PSD** supportando le proprietà dei dati di registro di lunghezza con Aspose.PSD per Java. Che tu stia automatizzando pipeline di asset o costruendo uno strumento di design personalizzato, queste API ti offrono la flessibilità di manipolare i livelli vettoriali senza interventi manuali in Photoshop. Approfondisci sperimentando altre `PathOperations` o combinando più modifiche di `LengthRecord` per forme complesse.

## FAQ
### Cos'è Aspose.PSD per Java?
Aspose.PSD per Java è una libreria che consente agli sviluppatori di manipolare e lavorare con i file Photoshop PSD in modo programmatico usando Java.

### Posso usare Aspose.PSD in un progetto gratuito?
Sì, puoi provare la libreria gratuitamente usando la versione di prova disponibile sul sito di Aspose.

### Quali tipi di modifiche posso apportare ai file PSD?
Puoi manipolare livelli, forme, testi, operazioni di percorso e molto altro all'interno dei file PSD.

### Aspose.PSD è compatibile con altri linguaggi di programmazione?
Sì, Aspose offre varie librerie per diversi linguaggi, inclusi .NET e Python.

### Dove posso trovare la documentazione di Aspose.PSD?
Puoi accedere alla documentazione completa [qui](https://reference.aspose.com/psd/java/).

## Domande frequenti

**D: Come gestisco un PSD che non contiene livelli di forme vettoriali?**  
R: La `VsmsResource` sarà assente, quindi `resource` rimarrà `null`. Aggiungi un controllo e salta il passo di modifica o informa l'utente.

**D: Posso cambiare altre proprietà come colore di riempimento o larghezza del tratto?**  
R: Sì, `LengthRecord` fornisce setter aggiuntivi per riempimento, tratto e opacità. Consulta la documentazione API per tutti i dettagli.

**D: È possibile elaborare in batch più file PSD?**  
R: Assolutamente. Avvolgi il codice in un ciclo che itera su una cartella di file PSD, regolando i percorsi di input e output ad ogni iterazione.

**D: Devo chiudere manualmente gli stream quando carico da un percorso file?**  
R: Il metodo `Image.load` gestisce gli stream internamente, ma se carichi da un `InputStream` ricordati di chiuderlo dopo l'uso.

**D: Quale versione di Aspose.PSD è necessaria per queste API?**  
R: Le classi `LengthRecord` e `PathOperations` sono disponibili da Aspose.PSD 20.10. Si consiglia di utilizzare l'ultima versione.

---

**Ultimo aggiornamento:** 2025-12-17  
**Testato con:** Aspose.PSD per Java 24.11  
**Autore:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}