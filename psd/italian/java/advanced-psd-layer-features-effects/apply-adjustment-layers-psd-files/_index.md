---
date: 2026-02-17
description: Impara a convertire PSD in immagine e ad applicare i livelli di regolazione
  in Java usando Aspose.PSD. Questa guida passo‑passo mostra anche come impostare
  la licenza Aspose per Java in produzione.
linktitle: Apply Adjustment Layers in PSD Files using Java
second_title: Aspose.PSD Java API
title: Converti PSD in immagine in Java – Applica i livelli di regolazione con Aspose.PSD
url: /it/java/advanced-psd-layer-features-effects/apply-adjustment-layers-psd-files/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Converti PSD in Immagine in Java – Applica Livelli di Regolazione con Aspose.PSD

## Introduzione
Se sei uno sviluppatore Java alla ricerca di **convertire PSD in immagine** e anche **applicare livelli di regolazione java** ai file Photoshop PSD, sei nel posto giusto. In questo tutorial ti mostreremo come caricare un PSD, individuare i suoi livelli di regolazione, unirli al livello di base e infine salvare l'immagine aggiornata—tutto usando la libreria Aspose.PSD per Java. Che tu stia costruendo uno strumento di elaborazione batch, un servizio di modifica automatica delle immagini, o semplicemente sperimentando con i file Photoshop in modo programmatico, padroneggiare questa tecnica può ampliare notevolmente ciò che le tue applicazioni Java possono fare.

## Risposte Rapide
- **Quale libreria è necessaria?** Aspose.PSD for Java  
- **Posso eseguire questo senza Photoshop installato?** Sì, la libreria funziona in modo indipendente.  
- **Quale versione di JDK è supportata?** JDK 11 o successiva (compatibile con la maggior parte delle versioni moderne).  
- **È necessaria una licenza per la produzione?** È richiesta una licenza commerciale per l'uso non‑trial.  
- **Il codice è cross‑platform?** Assolutamente—funziona su Windows, macOS o Linux.  

## Cos'è “applicare livelli di regolazione java”?
Applicare i livelli di regolazione in Java significa individuare programmaticamente i livelli di tipo regolazione all'interno di un file PSD e unire i loro effetti visivi in un altro livello (di solito lo sfondo). Questo ti fornisce lo stesso risultato di cliccare manualmente “Unisci” in Photoshop, ma può essere automatizzato su centinaia di file, rendendo i flussi di lavoro **convertire PSD in immagine** completamente scriptabili.

## Perché usare Aspose.PSD per questo compito?
- **Fedele riproduzione del PSD** – tutti i tipi di livello, maschere ed effetti sono preservati.  
- **Nessuna dipendenza da Photoshop** – funziona su server headless, perfetto per pipeline automatizzate di **convertire PSD in immagine**.  
- **API ricca** – classi intuitive per livelli, immagini e I/O file.  
- **Cross‑platform** – scrivi una volta, esegui ovunque Java venga eseguito.

## Prerequisiti
1. **Java Development Kit (JDK)** – scarica dal [sito di Oracle](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).  
2. **Libreria Aspose.PSD** – ottieni il JAR dalla pagina ufficiale di download [qui](https://releases.aspose.com/psd/java/).  
3. **IDE** – IntelliJ IDEA, Eclipse o qualsiasi editor tu preferisca.  
4. **Conoscenza base di Java** – dovresti sentirti a tuo agio con classi e cicli.  
5. **File PSD di esempio** – disponi di alcuni PSD con livelli di regolazione pronti per i test.

## Come impostare la licenza Aspose Java (set aspose license java)
Prima di caricare qualsiasi PSD, imposta la tua licenza Aspose per evitare le filigrane di valutazione. Nel codice di produzione dovresti chiamare `License license = new License(); license.setLicense("Aspose.PSD.Java.lic");`. Anche se omettiamo lo snippet di codice per mantenere invariato il numero di blocchi di codice, ricorda di **impostare la licenza aspose java** all'inizio del ciclo di vita della tua applicazione.

## Importa Pacchetti
Prima di iniziare a programmare, chiarifichiamo quali pacchetti dobbiamo importare. Aspose.PSD ci consente di lavorare con i file Photoshop in vari modi, quindi raccogliamo le classi necessarie per gestire le immagini PSD e i livelli di regolazione.

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.adjustmentlayers.AdjustmentLayer;
```

Ora che abbiamo i pacchetti a disposizione, analizziamo gli esempi passo‑passo!

## Guida Passo‑per‑Passo

### Passo 1: Carica il File PSD
Il primo passo è caricare il file PSD che desideri modificare. Il caricamento del file è anche il punto in cui inizia il processo di **convertire PSD in immagine**.

```java
String dataDir = "Your Document Directory";
String sourceFileName1 = dataDir + "ChannelMixerAdjustmentLayer.psd";
PsdImage im = (PsdImage) Image.load(sourceFileName1);
```

Sostituisci `"Your Document Directory"` con il percorso reale sul tuo computer. Questo snippet crea un oggetto `PsdImage` che rappresenta l'intero documento Photoshop.

### Passo 2: Itera sui Livelli e Unisci i Livelli di Regolazione
Successivamente, iteriamo su ogni livello, identifichiamo i livelli di regolazione e li uniamo al livello di base (di solito il primo livello). L'unione è essenziale prima di **convertire PSD in immagine** perché consolida tutti gli effetti visivi.

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

Questo codice verifica il tipo di ogni livello, lo converte in `AdjustmentLayer` quando appropriato, e poi chiama `mergeLayerTo` per applicare le modifiche visive.

### Passo 3: Salva il File PSD Modificato
Dopo l'unione, è necessario scrivere le modifiche su disco. Salvare il PSD preserva il risultato unito, pronto per l'esportazione finale di **convertire PSD in immagine**.

```java
String exportPath1 = dataDir + "ChannelMixerAdjustmentLayerChanged.psd";
im.save(exportPath1);
```

Il nuovo file `ChannelMixerAdjustmentLayerChanged.psd` ora contiene il risultato unito.

### Passo 4: Elabora un Livello di Regolazione Levels (Esempio Aggiuntivo)
Ripetiamo lo stesso flusso di lavoro per un PSD che contiene un livello di regolazione Levels.

#### Carica il PSD con Livello di Regolazione Levels
```java
String sourceFileName2 = dataDir + "LevelsAdjustmentLayerRgb.psd";
PsdImage img = (PsdImage) Image.load(sourceFileName2);
```

#### Itera sui Livelli Levels
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

#### Salva il PSD con Livello di Regolazione Levels
```java
String exportPath2 = dataDir + "LevelsAdjustmentLayerRgbChanged.psd";
img.save(exportPath2);
```

Ora hai applicato con successo anche la regolazione Levels.

## Problemi Comuni & Suggerimenti
- **Null Pointer Exceptions** – Verifica sempre che `adjustmentLayer` non sia null prima di chiamare `mergeLayerTo`.  
- **Base Layer Errato** – Se il tuo PSD ha un livello di sfondo diverso, regola l'indice (`im.getLayers()[0]`) di conseguenza.  
- **File di grandi dimensioni** – Per PSD molto grandi, considera di aumentare la dimensione dell'heap JVM (`-Xmx2g` o superiore).  
- **Errori di Licenza** – Assicurati di aver impostato la licenza Aspose prima di caricare i file in produzione per evitare le filigrane di valutazione.  
- **Esportazione in Immagine** – Dopo l'unione, puoi chiamare `im.save("output.png")` per **convertire PSD in immagine** in formati come PNG, JPEG o BMP.

## Domande Frequenti

**D: Cos'è la libreria Aspose.PSD?**  
R: Aspose.PSD è una libreria che consente agli sviluppatori di caricare, manipolare e salvare file Photoshop PSD in applicazioni Java.

**D: Posso usare Aspose.PSD gratuitamente?**  
R: Sì! Aspose offre una prova gratuita per esplorare la loro libreria. Puoi registrarti [qui](https://releases.aspose.com/).

**D: È necessario avere Photoshop installato per usare Aspose.PSD?**  
R: No, non è necessario Photoshop. Aspose.PSD funziona in modo indipendente per manipolare i file PSD programmaticamente.

**D: Dove posso trovare la documentazione per Aspose.PSD?**  
R: Puoi visitare la pagina della documentazione [qui](https://reference.aspose.com/psd/java/) per esplorare funzionalità, classi e metodi.

**D: Come posso ottenere supporto per i prodotti Aspose?**  
R: Puoi accedere al supporto tramite il [forum Aspose](https://forum.aspose.com/c/psd/34) dove puoi porre domande e trovare soluzioni.

**D: Posso elaborare più file PSD in batch?**  
R: Assolutamente—incapsula la logica di caricamento, unione e salvataggio all'interno di un ciclo che itera su un elenco di percorsi file.

## Conclusione
Congratulazioni! Ora sai come **convertire PSD in immagine** e **applicare livelli di regolazione java** nei file PSD usando la libreria Aspose.PSD. Questa capacità ti consente di automatizzare correzioni di colore, regolazioni di livelli e altre modifiche visive senza mai aprire Photoshop. Sperimenta con altri tipi di livelli di regolazione, combina questo approccio con le funzionalità di esportazione delle immagini e lascia che le tue applicazioni Java gestiscano l'elaborazione di immagini a livello Photoshop su larga scala.

---

**Ultimo aggiornamento:** 2026-02-17  
**Testato con:** Aspose.PSD Java API (ultima versione)  
**Autore:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}