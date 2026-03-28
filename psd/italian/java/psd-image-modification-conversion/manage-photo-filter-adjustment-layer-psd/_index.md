---
date: 2026-03-28
description: Scopri come creare un livello di filtro fotografico e aggiungere un livello
  di regolazione ai file PSD utilizzando Aspose.PSD per Java. Segui questa guida per
  modificare e aggiungere filtri senza sforzo.
linktitle: How to Create Photo Filter Layer in PSD Using Java
second_title: Aspose.PSD Java API
title: Come creare un livello di filtro fotografico in PSD usando Java
url: /it/java/psd-image-modification-conversion/manage-photo-filter-adjustment-layer-psd/
weight: 24
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Gestire il livello di regolazione Filtro Foto in PSD - Java

## Introduzione
Se sei uno sviluppatore Java alla ricerca di **creare oggetti layer di filtro foto** all'interno di file PSD, sei nel posto giusto. In questo tutorial vedremo come utilizzare Aspose.PSD per Java per modificare i Photo Filter Adjustment Layers esistenti e aggiungerne di nuovi. Alla fine saprai esattamente come **creare un layer di filtro foto**, regolarne le proprietà e persino **aggiungere layer di regolazione PSD** in modo programmatico, accelerando il tuo flusso di lavoro di graphic‑design.

## Risposte rapide
- **Quale libreria gestisce i layer PSD in Java?** Aspose.PSD per Java  
- **Posso modificare un layer Photo Filter esistente?** Sì – carica il PSD, individua il `PhotoFilterLayer` e modifica le sue proprietà.  
- **Come aggiungo un nuovo layer filtro?** Usa `addPhotoFilterLayer(Color)` su un'istanza `PsdImage`.  
- **È necessaria una licenza per la produzione?** È richiesta una licenza commerciale; è disponibile una versione di prova gratuita.  
- **Quale versione di Java è supportata?** JDK 8 o superiore (consigliato JDK 11).  

## Che cos'è un Photo Filter Adjustment Layer?
Un Photo Filter Adjustment Layer è un effetto non distruttivo che tinta l'intera immagine con un colore scelto, simile all'applicazione di un filtro fotografico. Vive sul proprio layer, consentendoti di regolare colore, densità e luminosità senza alterare i pixel originali.

## Perché usare Aspose.PSD per creare un layer di filtro foto?
- **Controllo totale** sulla struttura PSD senza Adobe Photoshop.  
- **Cross‑platform**: l'API Java funziona su Windows, Linux e macOS.  
- **Nessuna interop COM** – puro Java, ideale per l'elaborazione lato server.  
- **Supporta la versione PSD 1‑8**, preservando effetti di layer e maschere.

## Prerequisiti
### Software essenziale
1. Java Development Kit (JDK): assicurati di avere una versione compatibile di JDK installata sulla tua macchina. Puoi scaricarla dal sito di [Oracle](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).
2. Aspose.PSD per Java: per manipolare i file PSD, ti serve la libreria Aspose.PSD. Puoi scaricarla dalla [pagina di rilascio di Aspose](https://releases.aspose.com/psd/java/). Non dimenticare di consultare la [documentazione di Aspose](https://reference.aspose.com/psd/java/) per ulteriori dettagli.
3. IDE (Integrated Development Environment): un buon IDE come IntelliJ IDEA o Eclipse renderà più fluida la tua esperienza di codifica.

### Comprendere le basi
Familiarità con la programmazione Java e una conoscenza di base di come funzionano i file PSD saranno utili. Se sei nuovo all'uso di librerie in Java, è consigliabile abituarsi a importare e utilizzare framework.

## Importare i pacchetti
Per iniziare, dobbiamo importare le classi necessarie dalla libreria Aspose.PSD. Ecco una semplice istruzione di importazione di cui avrai bisogno all'inizio del tuo file Java:
```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.adjustmentlayers.PhotoFilterLayer;
```
Incolla semplicemente questo all'inizio del tuo file Java e sei pronto per lavorare con le immagini PSD!

## Modifica di un Photo Filter Layer esistente
### Passo 1: Configurare la directory dei dati
Innanzitutto, devi definire la directory in cui sono archiviati i tuoi file PSD. Sostituisci `"Your Document Directory"` con il percorso reale. Questo ti aiuterà a tenere tutto organizzato:
```java
String dataDir = "Your Document Directory";
```

### Passo 2: Caricare il tuo file PSD
Ora, carichiamo il file PSD che **vuoi modificare**. Assicurati che `PhotoFilterAdjustmentLayer.psd` esista nella directory specificata.
```java
String sourceFileName = dataDir + "PhotoFilterAdjustmentLayer.psd";
```

### Passo 3: Inizializzare l'oggetto immagine
Utilizzando la funzionalità integrata di Aspose, **carichiamo** l'immagine nel nostro **progetto**:
```java
PsdImage im = (PsdImage) Image.load(sourceFileName);
```

### Passo 4: Iterare attraverso i layer
Successivamente, esamineremo i layer presenti nel file PSD. Il nostro obiettivo è individuare il `PhotoFilterLayer`:
```java
for(int i = 0; i < im.getLayers().length; i++) {
    if (im.getLayers()[i] instanceof PhotoFilterLayer) {
        PhotoFilterLayer photoLayer = (PhotoFilterLayer) im.getLayers()[i];
        // Make changes to the layer
    }
}
```

### Passo 5: Personalizzare il Photo Filter Layer
Ecco dove avviene la magia! Puoi modificare il `Color` e la `Density`. Ad esempio, possiamo impostare il colore su un rosso vibrante e regolare la densità:
```java
photoLayer.setColor(Color.fromArgb(255, 60, 60));
photoLayer.setDensity(78);
photoLayer.setPreserveLuminosity(false);
```

### Passo 6: Salvare il file PSD modificato
Infine, salva le modifiche per creare un nuovo file PSD con le tue regolazioni:
```java
String psdPathAfterChange = dataDir + "PhotoFilterAdjustmentLayerChanged.psd";
im.save(psdPathAfterChange);
```
Hai appena modificato un Photo Filter Adjustment Layer in un file PSD.

## Aggiungere un nuovo Photo Filter Layer
### Passo 1: Configurare il percorso della directory
Come prima, iniziamo definendo la nostra directory dei dati:
```java
String dataDir = "Your Document Directory";
```

### Passo 2: Caricare il file sorgente
Per questo esempio, carichiamo un diverso file PSD in cui vogliamo **aggiungere un layer di regolazione PSD**:
```java
String sourceFileName = dataDir + "PhotoExample.psd";
```

### Passo 3: Inizializzare nuovamente l'oggetto immagine
Dobbiamo creare una nuova istanza `PsdImage`, quindi carichiamo il file:
```java
PsdImage img = (PsdImage) Image.load(sourceFileName);
```

### Passo 4: Aggiungere un Photo Filter Layer
Ora possiamo aggiungere un nuovo Photo Filter layer con un colore personalizzato. Ecco come si fa:
```java
PhotoFilterLayer layer = img.addPhotoFilterLayer(Color.fromArgb(25, 255, 35));
```

### Passo 5: Salvare il nuovo file PSD
Ancora una volta, è il momento di salvare le modifiche. Ecco la riga di codice per farlo:
```java
String psdPathAfterChange = dataDir + "PhotoExampleAddedPhotoFilter.psd";
img.save(psdPathAfterChange);
```
Hai aggiunto con successo un nuovo layer di filtro foto al tuo file PSD.

## Problemi comuni e soluzioni
- **`ClassCastException` durante il caricamento dell'immagine** – Assicurati che il file caricato sia un PSD; altri formati richiedono classi diverse.  
- **I valori di colore appaiono errati** – Usa `Color.fromArgb(alpha, red, green, blue)` dove ogni componente è compreso tra 0‑255.  
- **Layer non trovato** – Verifica che il PSD sorgente contenga effettivamente un `PhotoFilterLayer`. Usa `im.getLayers().length` per il debug.

## Domande frequenti
### Che cos'è Aspose.PSD?
Aspose.PSD è una libreria .NET e Java per creare, modificare e convertire file PSD.

### Posso provare Aspose.PSD gratuitamente?
Sì, Aspose offre una versione di prova gratuita. Scoprila [qui](https://releases.aspose.com/).

### Dove posso trovare la documentazione?
Puoi trovare la documentazione completa nella [pagina di riferimento di Aspose](https://reference.aspose.com/psd/java/).

### Come posso acquistare Aspose.PSD?
Puoi acquistare il software da [questo link](https://purchase.aspose.com/buy).

### È disponibile supporto per Aspose.PSD?
Assolutamente! Puoi ottenere supporto tramite il forum di supporto Aspose [qui](https://forum.aspose.com/c/psd/34).

---

**Ultimo aggiornamento:** 2026-03-28  
**Testato con:** Aspose.PSD per Java 24.11 (ultima versione al 2026)  
**Autore:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}