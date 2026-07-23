---
date: 2026-02-20
description: Scopri come supportare le proprietà dei record di lunghezza e processare
  in batch i file PSD usando Aspose.PSD per Java. Guida passo‑passo con esempi di
  codice.
linktitle: Support Length Record Data Properties in PSD - Java
second_title: Aspose.PSD Java API
title: Supporto alle proprietà di registrazione della lunghezza – Modifica forme vettoriali
  PSD (Java)
url: /it/java/advanced-psd-layer-features-effects/support-length-record-data-properties-psd/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Supportare le proprietà del record di lunghezza – Modificare le forme vettoriali PSD (Java)

## Introduzione
Se hai bisogno di **modificare le forme vettoriali PSD** in modo programmatico, la libreria Aspose.PSD per Java ti offre il pieno controllo sui file Photoshop direttamente dal tuo codice Java. In questo tutorial vedremo tutto ciò che devi sapere per **supportare le proprietà del record di lunghezza**—un passaggio essenziale quando vuoi modificare i livelli di forme vettoriali. Alla fine, sarai in grado di aprire un PSD, regolare le sue proprietà di forma vettoriale e salvare il file aggiornato senza mai uscire dal tuo IDE. Immergiamoci!

## Risposte rapide
- **Cosa significa “modificare le forme vettoriali PSD”?** Regolare la geometria, le operazioni di percorso o altre proprietà dei livelli basati su vettori all'interno di un file PSD.  
- **Quale libreria gestisce questo?** Aspose.PSD per Java.  
- **È necessaria una licenza?** Una versione di prova gratuita è sufficiente per la valutazione; è richiesta una licenza commerciale per la produzione.  
- **Quanto tempo richiede l'implementazione?** Circa 10‑15 minuti per uno script di modifica di forma di base.  
- **Quali sono i prerequisiti principali?** Java JDK, Aspose.PSD per Java e un file PSD di esempio.

## Che cosa significa “supportare le proprietà del record di lunghezza”?
Supportare le proprietà del record di lunghezza significa accedere e aggiornare gli oggetti `LengthRecord` che descrivono ogni percorso vettoriale all'interno di un PSD. Modificando questi record è possibile controllare come le forme si combinano, si intersecano o si sottraggono l'una dall'altra.

## Perché usare Aspose.PSD per Java per supportare le proprietà del record di lunghezza?
- **Nessun Photoshop necessario** – lavora direttamente con i file PSD su qualsiasi server.  
- **API ricca** – accedi a livelli, risorse e dati vettoriali con classi tipizzate.  
- **Cross‑platform** – funziona su Windows, Linux o macOS con qualsiasi JDK.  
- **Ottimizzata per le prestazioni** – gestione efficiente della memoria e operazioni di salvataggio rapide.  

## Prerequisiti
1. **Java Development Kit (JDK)** – scaricalo dal [sito di Oracle](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html) o usa il tuo gestore di pacchetti preferito.  
2. **Aspose.PSD per Java** – ottieni l'ultimo JAR dalla [pagina dei rilasci Aspose](https://releases.aspose.com/psd/java/).  
3. **IDE** – IntelliJ IDEA, Eclipse o qualsiasi editor compatibile con Java.  
4. **Un file PSD** – creane uno in Photoshop o prendi un PSD di esempio per sperimentare.  
5. **Conoscenza di base di Java** – familiarità con classi, oggetti e gestione delle eccezioni.

## Importare i pacchetti
Per prima cosa, importa le classi necessarie per lavorare con i file PSD e le risorse di forme vettoriali.

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
Ora puoi **modificare le forme vettoriali PSD** cambiando le loro `PathOperations`. Questo determina come le forme interagiscono (ad es., esclusione, intersezione, sottrazione).

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
Chiudi il `PsdImage` per liberare la memoria.

```java
psdImage.dispose();
```

## Come elaborare in batch i file PSD con supporto alle proprietà del record di lunghezza
Se devi applicare le stesse regolazioni di forme vettoriali a molti PSD, avvolgi il codice sopra in un ciclo che itera su una cartella di file. Aggiorna `inPsdFilePath` e `outPsdFilePath` per ogni iterazione, e potrai **elaborare in batch i file PSD** in modo efficiente.

## Problemi comuni e consigli
- **Controlli null** – verifica sempre che `resource` non sia `null` prima di accedere ai percorsi.  
- **Limiti degli indici di percorso** – assicurati che gli indici che usi (`[2]`, `[7]`, `[11]`) esistano per il PSD specifico che stai modificando.  
- **Licenza** – l'esecuzione senza licenza valida inserirà una filigrana nel PSD salvato.  

## Conclusione
Ora disponi di un esempio completo, end‑to‑end, su come **modificare le forme vettoriali PSD** supportando le proprietà del record di lunghezza con Aspose.PSD per Java. Che tu stia automatizzando pipeline di asset o costruendo uno strumento di design personalizzato, queste API ti offrono la flessibilità per manipolare i livelli vettoriali senza interventi manuali in Photoshop. Esplora ulteriormente sperimentando altre `PathOperations` o combinando più modifiche di `LengthRecord` per forme complesse.

## Domande frequenti

**D: Come gestisco un PSD che non contiene livelli di forme vettoriali?**  
R: La `VsmsResource` sarà assente, quindi `resource` rimarrà `null`. Aggiungi un controllo e salta il passo di modifica o informa l'utente.

**D: Posso cambiare altre proprietà come colore di riempimento o spessore del tratto?**  
R: Sì, `LengthRecord` fornisce altri setter per riempimento, tratto e opacità. Consulta la documentazione API per tutti i dettagli.

**D: È possibile elaborare in batch più file PSD?**  
R: Assolutamente. Avvolgi il codice in un ciclo che itera su una cartella di file PSD, regolando i percorsi di input e output ad ogni iterazione.

**D: Devo chiudere manualmente gli stream quando carico da un percorso file?**  
R: Il metodo `Image.load` gestisce gli stream dei file internamente, ma se carichi da un `InputStream`, ricordati di chiuderlo dopo l'uso.

**D: Quale versione di Aspose.PSD è necessaria per queste API?**  
R: Le classi `LengthRecord` e `PathOperations` sono disponibili da Aspose.PSD 20.10. Si consiglia di utilizzare l'ultima versione.

---

**Ultimo aggiornamento:** 2026-02-20  
**Testato con:** Aspose.PSD per Java 24.11  
**Autore:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}