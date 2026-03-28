---
date: 2026-03-28
description: Scopri come regolare la luminosità di un PSD in Java usando Aspose.PSD
  per Java, incluso come modificare la luminosità e il contrasto dei livelli PSD.
  Ideale per sviluppatori e designer grafici.
linktitle: Adjust Brightness PSD Java – Manage Brightness & Contrast
second_title: Aspose.PSD Java API
title: Regola la luminosità PSD Java – Gestisci luminosità e contrasto
url: /it/java/psd-image-modification-conversion/manage-brightness-contrast-psd-layers/
weight: 21
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Regola la luminosità PSD Java – Gestisci luminosità e contrasto

## Introduzione

Sei un grafico o uno sviluppatore che lavora frequentemente con file PSD (Photoshop Document)? Hai bisogno di **adjust brightness psd java** in modo rapido e affidabile senza uscire dall'ambiente Java? In questo tutorial ti mostreremo esattamente come modificare la luminosità e il contrasto dei livelli PSD usando la libreria Aspose.PSD per Java. Avrai a disposizione uno snippet di codice riutilizzabile da integrare in qualsiasi pipeline automatizzata di elaborazione immagini. Arrotiniamoci le maniche e cominciamo!

## Risposte rapide
- **Quale libreria serve?** Aspose.PSD per Java  
- **Posso modificare più livelli contemporaneamente?** Sì – itera attraverso tutti gli oggetti `BrightnessContrastLayer`.  
- **Quale versione di Java è necessaria?** JDK 8 o superiore.  
- **È necessaria una licenza per la produzione?** Sì, è richiesta una licenza commerciale per l'uso non valutativo.  
- **Il codice è compatibile con progetti Maven/Gradle?** Assolutamente – basta aggiungere la dipendenza Aspose.PSD.

## Cos'è “adjust brightness psd java”?

Regolare la luminosità in un file PSD tramite Java significa modificare programmaticamente i valori di `BrightnessContrastLayer`, consentendo di automatizzare correzioni visive che altrimenti richiederebbero lavoro manuale in Photoshop.

## Perché regolare luminosità e contrasto nei livelli PSD?

- **Accelerare l'elaborazione batch** – ideale per grandi librerie di design.  
- **Mantenere la struttura dei livelli** – solo i livelli di regolazione target vengono modificati, preservando maschere ed effetti.  
- **Integrare nelle pipeline CI/CD** – genera anteprime o miniature automaticamente.

## Prerequisiti

Prima di intraprendere questo entusiasmante viaggio nella manipolazione dei file PSD con Java, è fondamentale assicurarsi di avere tutto il necessario configurato correttamente. Ecco cosa ti servirà per completare con successo questo tutorial:

1. **Java Development Kit (JDK)** – Assicurati di avere JDK 8 o superiore installato sulla tua macchina. Puoi scaricarlo dal [sito di Oracle](https://www.oracle.com/java/technologies/javase-jdk8-downloads.html).

2. **Aspose.PSD per Java Library** – Per lavorare con i file PSD, avrai bisogno della libreria Aspose.PSD. Puoi scaricare l'ultima versione dalla [pagina di rilascio](https://releases.aspose.com/psd/java/).

3. **IDE a tua scelta** – Un Integrated Development Environment (IDE) come IntelliJ IDEA, Eclipse o NetBeans è consigliato per scrivere ed eseguire il codice Java.

4. **Conoscenze di base di Java** – Familiarità con la programmazione Java ti aiuterà a comprendere gli snippet di codice con cui lavoreremo.

Una volta che avrai tutti questi prerequisiti, siamo pronti a procedere. Ora, prendi il tuo editor di codice preferito e cominciamo a programmare!

## Importa pacchetti

Il primo passo del nostro percorso di codifica è importare i pacchetti necessari. Prima di poter utilizzare le funzionalità fornite da Aspose.PSD, devi assicurarti che la libreria sia nel classpath. Ecco come fare:

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.adjustmentlayers.BrightnessContrastLayer;
```

Completando questi passaggi, stai preparando il terreno per lavorare efficacemente con i file PSD!

Ora che abbiamo tutto pronto, è il momento di entrare nel cuore del tutorial: regolare luminosità e contrasto nei livelli PSD. Divideremo questo processo in passaggi chiari per garantirti una facile comprensione.

## Passo 1: Definisci la directory dei documenti

Inizia definendo la directory in cui sono situati i tuoi file PSD. Questo passaggio aiuta a organizzare i file in modo efficiente.

```java
String dataDir = "Your Document Directory";
```

Sostituisci `"Your Document Directory"` con il percorso reale della tua cartella contenente i file PSD.

## Passo 2: Specifica i nomi dei file di origine e destinazione

Successivamente, devi specificare il nome del file di origine del tuo PSD e il file di destinazione dove verrà salvato il PSD modificato.

```java
String sourceFileName = dataDir + "BrightnessContrastModern.psd";
String psdPathAfterChange = dataDir + "BrightnessContrastModernChanged.psd";
```

In questo esempio, assumiamo che nella tua directory sia presente un file PSD chiamato `BrightnessContrastModern.psd`.

## Passo 3: Carica il file PSD

È ora di caricare il file PSD nella tua applicazione così da poterlo manipolare.

```java
PsdImage im = (PsdImage) Image.load(sourceFileName);
```

Questa riga di codice crea un'istanza di `PsdImage` che rappresenta il tuo file PSD. Con questa, puoi accedere a tutti i livelli del PSD.

## Passo 4: Itera attraverso i livelli

Il passo successivo prevede l'iterazione su ciascun livello del tuo file PSD per trovare e modificare le impostazioni di luminosità e contrasto.

```java
for(int i = 0; i < im.getLayers().length; i++) {
    if (im.getLayers()[i] instanceof BrightnessContrastLayer) {
        BrightnessContrastLayer brightnessContrastLayer = (BrightnessContrastLayer)im.getLayers()[i];
```

Il ciclo `for` scorre ogni livello del PSD. Verifichiamo se un livello è un'istanza di `BrightnessContrastLayer`. Questo è fondamentale per assicurarsi di intervenire solo sui livelli corretti.

## Passo 5: Regola luminosità e contrasto

All'interno del ciclo, puoi ora impostare la luminosità e il contrasto per ciascun `BrightnessContrastLayer`.

```java
        brightnessContrastLayer.setBrightness(50);
        brightnessContrastLayer.setContrast(50);
    }
}
```

In questo esempio, impostiamo luminosità e contrasto a `50`. Puoi modificare questi valori in base alle tue esigenze. Un numero più alto aumenta luminosità/contrasto, mentre un numero più basso li diminuisce.

## Passo 6: Salva le modifiche

L'ultimo passo è salvare le modifiche nel file PSD. Dovrai scrivere l'immagine modificata nella destinazione specificata.

```java
im.save(psdPathAfterChange);
```

Questa riga di codice salva il file PSD modificato con le nuove impostazioni di luminosità e contrasto.

## Problemi comuni e soluzioni

| Problema | Perché accade | Soluzione |
|----------|----------------|-----------|
| **Nessun `BrightnessContrastLayer` trovato** | Il PSD potrebbe usare un tipo di regolazione diverso (es. Levels). | Verifica il tipo di livello o converti la regolazione in un `BrightnessContrastLayer`. |
| **Il file salvato appare corrotto** | Licenza mancante o versione obsoleta di Aspose.PSD. | Applica una licenza valida e assicurati di usare l'ultima versione della libreria. |
| **Valori fuori intervallo** | I valori di luminosità/contrasto devono essere compresi tra -100 e 100. | Limita i valori prima di chiamare `setBrightness`/`setContrast`. |

## Domande frequenti

**D: Cos'è Aspose.PSD per Java?**  
R: Aspose.PSD per Java è una libreria che consente agli sviluppatori di manipolare file PSD programmaticamente, permettendo l'automazione di attività legate a Photoshop.

**D: Posso regolare la luminosità e il contrasto di più livelli contemporaneamente?**  
R: Sì, l'approccio usato in questo tutorial itera su tutti i livelli del PSD, consentendo di modificare più istanze di `BrightnessContrastLayer`.

**D: Come ottengo una licenza temporanea per Aspose.PSD?**  
R: Puoi ottenere una licenza temporanea visitando la [pagina della licenza temporanea](https://purchase.aspose.com/temporary-license/).

**D: È disponibile una versione di prova gratuita di Aspose.PSD?**  
R: Sì, puoi scaricare una versione di prova gratuita di Aspose.PSD dalla [pagina di rilascio](https://releases.aspose.com/).

**D: Dove posso trovare supporto aggiuntivo per Aspose.PSD?**  
R: Puoi ottenere supporto per Aspose.PSD sul loro [forum di supporto](https://forum.aspose.com/c/psd/34).

---

**Ultimo aggiornamento:** 2026-03-28  
**Testato con:** Aspose.PSD per Java 24.12 (ultima versione al momento della scrittura)  
**Autore:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}