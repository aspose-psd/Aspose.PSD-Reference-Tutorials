---
date: 2026-03-13
description: Scopri come aggiungere un livello di tonalità e saturazione ai file PSD
  utilizzando Aspose.PSD per Java. Questa guida mostra anche come elaborare in batch
  i file PSD e creare programmaticamente un livello di regolazione della tonalità.
linktitle: Add Hue Saturation Layer to PSD
second_title: Aspose.PSD Java API
title: Aggiungi livello di tonalità e saturazione al PSD con Aspose.PSD per Java
url: /it/java/modifying-converting-psd-images/add-hue-saturation-adjustment-layer-psd/
weight: 14
---

- Keep backtop button shortcode.

- Footer lines: "Last Updated:", "Tested With:", "Author:" translate? Probably keep as is? The content is not part of main translation? It is text, so translate. Keep dates unchanged.

- Ensure no extra spaces.

Proceed.{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aggiungi livello di tonalità e saturazione a PSD

## Introduzione
Nel campo del design grafico, la manipolazione del colore svolge un ruolo fondamentale—in particolare, modificare tonalità, saturazione e luminosità può trasformare drasticamente l'umore e la qualità di qualsiasi immagine. Un modo efficace per ottenere ciò è utilizzare i livelli di regolazione in Photoshop (file PSD). Se desideri **aggiungere un livello di tonalità e saturazione** in modo programmatico usando Java, la libreria Aspose.PSD è qui per aiutarti! Questo tutorial ti guiderà passo passo nell'aggiungere un livello di regolazione Tonalità‑Saturazione ai tuoi file PSD, rendendo il tuo flusso di lavoro più produttivo ed efficiente.

## Risposte rapide
- **Quale libreria consente di aggiungere un livello di tonalità e saturazione in Java?** Aspose.PSD for Java.  
- **È necessario avere Photoshop installato?** No, la libreria funziona indipendentemente da Photoshop.  
- **Posso elaborare in batch i file PSD con questo approccio?** Sì—una volta automatizzati i passaggi, puoi applicarli a molti file.  
- **Quale versione di Java è richiesta?** JDK 8 o successiva.  
- **È necessaria una licenza per l'uso in produzione?** Sì, è richiesta una licenza commerciale dopo il periodo di prova.

## Che cos'è un'operazione “add hue saturation layer”?
Un'operazione **add hue saturation layer** crea un livello di regolazione non distruttivo che ti permette di modificare i valori di tonalità, saturazione e luminosità senza alterare i dati pixel originali. Questo è ideale per perfezionare i colori su un'intera composizione o su specifici intervalli di colore.

## Perché usare Aspose.PSD per Java?
- **Nessuna dipendenza da Photoshop** – funziona su qualsiasi piattaforma che esegue Java.  
- **Fedele riproduzione del PSD** – preserva tutte le informazioni dei livelli, le maschere e gli effetti.  
- **Pronto per il batch** – puoi scorrere cartelle e applicare la stessa regolazione a decine di file.  
- **Ottimizzato per le prestazioni** – progettato per documenti di grandi dimensioni e automazione lato server.

## Prerequisiti
Prima di passare al codice, assicurati di avere quanto segue:

1. **Java Development Kit (JDK):** Verifica di avere JDK 8 o superiore installato sulla tua macchina. Puoi scaricarlo dal [Java SE Development Kit Downloads](https://www.oracle.com/java/technologies/javase-downloads.html).  
2. **Libreria Aspose.PSD per Java:** Avrai bisogno della libreria Aspose.PSD, che puoi [download here](https://releases.aspose.com/psd/java/).  
3. **IDE:** Un ambiente di sviluppo integrato (IDE) come IntelliJ IDEA o Eclipse per lo sviluppo Java.  
4. **Conoscenze di base di Java:** Familiarità con la programmazione Java è un plus, ma non preoccuparti—ti guideremo attraverso ogni riga.

Ora che abbiamo sistemato i prerequisiti, passiamo alla parte più divertente—scrivere il codice!

## Importa i pacchetti
Per iniziare a lavorare con la libreria Aspose.PSD, il primo passo è importare le classi necessarie. Ecco come farlo nel tuo file Java:

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.adjustmentlayers.HueSaturationLayer;
import com.aspose.psd.fileformats.psd.layers.layerresources.ColorRangeHsl;
```

Assicurati di aver aggiunto le librerie appropriate al tuo progetto affinché questi import funzionino senza problemi.

## Passo 1: Configura la directory del documento
Ogni progetto ha un punto di partenza, e il nostro non fa eccezione. Devi specificare una directory dove sono archiviati i tuoi file PSD. Questo è fondamentale per caricare e salvare correttamente le immagini.

```java
String dataDir = "Your Document Directory"; // Update this path to your actual directory
```

## Passo 2: Carica un file PSD esistente
Per manipolare un file PSD esistente, dobbiamo prima caricarlo nel nostro programma. Ecco come fare:

```java
String sourceFileName = dataDir + "HueSaturationAdjustmentLayer.psd";
PsdImage im = (PsdImage) Image.load(sourceFileName);
```

In questo codice, aggiorna `"HueSaturationAdjustmentLayer.psd"` con il nome del tuo file PSD esistente che desideri modificare.

## Passo 3: Modifica il livello di tonalità/saturazione
Successivamente, scorreremo i livelli della nostra immagine PSD caricata per trovare e modificare eventuali livelli di Tonalità/Saturazione esistenti. Questo passaggio prevede la modifica dei valori di tonalità, saturazione e luminosità.

```java
for (int i = 0; i < im.getLayers().length; i++) {
    if (im.getLayers()[i] instanceof HueSaturationLayer) {
        HueSaturationLayer hueLayer = (HueSaturationLayer) im.getLayers()[i];
        hueLayer.setHue((short) -25);
        hueLayer.setSaturation((short) -12);
        hueLayer.setLightness((short) 67);
        ColorRangeHsl colorRange = hueLayer.getRange(2);
        colorRange.setHue((short) -40);
        colorRange.setSaturation((short) 50);
        colorRange.setLightness((short) -20);
        colorRange.setMostLeftBorder((short) 300);
    }
}
```

In questo esempio:  
- Stiamo impostando la tonalità a **-25**, la saturazione a **-12** e la luminosità a **+67**.  
- Il metodo `getRange(2)` ci consente di regolare intervalli di colore specifici secondo le necessità.

## Passo 4: Salva il file PSD modificato
Dopo aver effettuato le regolazioni, il passo successivo è salvare il file. Questa è una parte fondamentale del processo, per garantire che le modifiche non vadano perse.

```java
String psdPathAfterChange = dataDir + "HueSaturationAdjustmentLayerChanged.psd";
im.save(psdPathAfterChange);
```

## Passo 5: Aggiungi un nuovo livello di tonalità/saturazione
Se devi **creare un livello di regolazione tonalità** da zero, puoi aggiungere un nuovo livello di regolazione Tonalità/Saturazione a un altro file PSD. Segui lo stesso schema di caricamento ma utilizza il metodo `addHueSaturationAdjustmentLayer()`.

```java
sourceFileName = dataDir + "PhotoExample.psd";
PsdImage img = (PsdImage) Image.load(sourceFileName);
HueSaturationLayer hueLayerNew = img.addHueSaturationAdjustmentLayer();
```

## Passo 6: Imposta i nuovi valori di tonalità/saturazione per il nuovo livello
Ora che hai creato questo nuovo livello, applica le impostazioni desiderate di tonalità, saturazione e luminosità proprio come prima.

```java
hueLayerNew.setHue((short) -25);
hueLayerNew.setSaturation((short) -12);
hueLayerNew.setLightness((short) 67);
ColorRangeHsl newColorRange = hueLayerNew.getRange(2);
newColorRange.setHue((short) -160);
newColorRange.setSaturation((short) 100);
newColorRange.setLightness((short) 20);
newColorRange.setMostLeftBorder((short) 300);
```

## Passo 7: Salva il file PSD aggiornato
Infine, salva il file PSD con il livello di Tonalità/Saturazione aggiunto così da poter vedere le modifiche.

```java
String psdPathAfterNewLayerChange = dataDir + "PhotoExampleAddedHueSaturation.psd";
img.save(psdPathAfterNewLayerChange);
```

Congratulazioni! Hai manipolato con successo i file PSD usando Aspose.PSD for Java. Ora puoi sperimentare con immagini diverse e modifiche più profonde, dando vita ai tuoi progetti di design grafico.

## Come elaborare in batch i file PSD con regolazioni di tonalità
Poiché il codice sopra è completamente scriptabile, puoi racchiudere l'intera sequenza in un ciclo che itera su ogni file `.psd` in una cartella. Questo ti consente di **elaborare in batch i file psd** e applicare le stesse modifiche di tonalità, saturazione e luminosità in un'unica esecuzione—perfetto per aggiornamenti di branding su larga scala.

## Problemi comuni e soluzioni
- **NullPointerException durante il caricamento di un file:** Verifica che `dataDir` termini con il separatore di file appropriato (`/` o `\`) e che il nome del file sia corretto.  
- **Valori di regolazione fuori intervallo:** Tonalità, saturazione e luminosità accettano valori da -255 a 255. Mantieni i numeri entro questo intervallo.  
- **Livello non trovato:** Se il PSD non contiene un livello di Tonalità/Saturazione, il controllo `instanceof` salterà il blocco. Usa `addHueSaturationAdjustmentLayer()` per crearne uno prima.

## Domande frequenti

**D: Cos'è un livello di regolazione Tonalità‑Saturazione?**  
R: Consente di modificare le proprietà cromatiche di un'immagine senza alterare permanentemente i pixel originali.

**D: È necessario avere Photoshop installato per usare Aspose.PSD?**  
R: No, Aspose.PSD è una libreria autonoma che funziona indipendentemente da Photoshop.

**D: Posso usare Aspose.PSD per l'elaborazione batch?**  
R: Sì, puoi automatizzare e processare in batch più file PSD con Aspose.PSD.

**D: Aspose.PSD è gratuito?**  
R: Aspose.PSD offre una versione di prova gratuita, ma è necessaria una licenza per l'uso a lungo termine. Puoi consultare i prezzi [qui](https://purchase.aspose.com/buy).

## Conclusione
Lavorare con la grafica in modo programmatico apre un mondo di possibilità. Usare Aspose.PSD for Java per **aggiungere un livello di tonalità e saturazione** e per **creare un livello di regolazione tonalità** offre flessibilità ed efficienza che possono semplificare il tuo flusso di lavoro di design. Che tu stia migliorando foto per un progetto o creando contenuti visivi sorprendenti, padroneggiare questi strumenti può migliorare notevolmente il tuo risultato.

Sentiti libero di esplorare altre funzionalità di Aspose.PSD consultando la [documentazione](https://reference.aspose.com/psd/java/) o considera di ottenere una [licenza temporanea](https://purchase.aspose.com/temporary-license/) per testare tutta la potenza della libreria.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Ultimo aggiornamento:** 2026-03-13  
**Testato con:** Aspose.PSD for Java 24.12 (ultima versione al momento della stesura)  
**Autore:** Aspose  

---