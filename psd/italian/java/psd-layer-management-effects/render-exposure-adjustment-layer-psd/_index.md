---
date: 2026-04-05
description: Scopri come renderizzare il livello di regolazione dell'esposizione nei
  file PSD utilizzando Aspose.PSD per Java. Guida passo passo con esempi di codice
  per modificare e aggiungere i livelli di esposizione.
keywords:
- render exposure adjustment layer
- exposure adjustment layer
- Aspose.PSD Java
linktitle: Render del livello di regolazione dell'esposizione nei file PSD - Java
second_title: Aspose.PSD Java API
title: Render del livello di regolazione dell'esposizione nei file PSD - Java
url: /it/java/psd-layer-management-effects/render-exposure-adjustment-layer-psd/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Rendering del livello di regolazione dell'esposizione nei file PSD - Java

## Introduzione

Stai lavorando con file PSD di Photoshop e hai bisogno di **renderizzare il livello di regolazione dell'esposizione** in modo programmatico? Che tu stia modificando i livelli esistenti o aggiungendone di nuovi, Aspose.PSD for Java offre un modo potente e intuitivo per gestire queste attività. In questa guida, ti mostreremo come utilizzare Aspose.PSD for Java per renderizzare e modificare i livelli di regolazione dell'esposizione nei file PSD. Alla fine di questo tutorial, saprai come regolare le impostazioni di esposizione nei livelli esistenti e aggiungere nuovi livelli di regolazione dell'esposizione ai tuoi file PSD. Iniziamo!

## Risposte rapide
- **Quale libreria è necessaria?** Aspose.PSD for Java
- **Posso modificare un livello di esposizione esistente?** Sì, puoi cambiare esposizione, offset e correzione gamma.
- **Come aggiungo un nuovo livello di regolazione dell'esposizione?** Usa `addExposureAdjustmentLayer()` su un'istanza `PsdImage`.
- **È supportata l'esportazione PNG?** Assolutamente – usa `PngOptions` per salvare il risultato come PNG.
- **Ho bisogno di una licenza per la produzione?** È necessaria una licenza commerciale per l'uso in produzione; è disponibile una versione di prova gratuita.

## Cos'è un livello di regolazione dell'esposizione renderizzato?

Un livello di regolazione dell'esposizione è un livello Photoshop non distruttivo che modifica la luminosità, l'offset e la gamma dell'immagine sottostante. Renderizzarlo significa applicare tali impostazioni in modo che il risultato visivo rifletta le regolazioni, che puoi poi esportare in formati come PNG.

## Perché usare Aspose.PSD for Java per renderizzare il livello di regolazione dell'esposizione?

- **Controllo totale** – manipola le proprietà del livello senza aprire Photoshop.
- **Elaborazione batch** – automatizza le regolazioni su molti file.
- **Cross‑platform** – esegui su qualsiasi sistema con JDK.
- **Preserva la struttura PSD** – mantieni i livelli modificabili per future modifiche.

## Prerequisiti

1. **Java Development Kit (JDK)** – almeno JDK 8.
2. **Aspose.PSD for Java** – scaricalo da [here](https://releases.aspose.com/psd/java/).
3. **Conoscenza di base di Java** – dovresti sentirti a tuo agio con la sintassi standard di Java.
4. **IDE o editor di testo** – IntelliJ IDEA, Eclipse, VS Code, o qualsiasi editor tu preferisca.

## Importa pacchetti

Per prima cosa, importa le classi Aspose.PSD necessarie:

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.adjustmentlayers.ExposureLayer;
import com.aspose.psd.imageoptions.PngOptions;
```

## Come renderizzare il livello di regolazione dell'esposizione – Guida passo‑passo

### Passo 1: Carica il file PSD

```java
String dataDir = "Your Document Directory";  // Define your document directory
String sourceFileName = dataDir + "ExposureAdjustmentLayer.psd";  // Source PSD file path

PsdImage im = (PsdImage) Image.load(sourceFileName);  // Load the PSD file
```

Sostituisci `"Your Document Directory"` con la cartella che contiene i tuoi file PSD. Il metodo `Image.load()` restituisce un oggetto `PsdImage` che ti dà pieno accesso ai livelli del documento.

### Passo 2: Modifica un livello di regolazione dell'esposizione esistente

```java
for (int i = 0; i < im.getLayers().length; i++) {
    if (im.getLayers()[i] instanceof ExposureLayer) {
        ExposureLayer expLayer = (ExposureLayer) im.getLayers()[i];
        expLayer.setExposure(2);  // Adjust the exposure level
        expLayer.setOffset(-0.25f);  // Set the offset
        expLayer.setGammaCorrection(0.5f);  // Adjust the gamma correction
    }
}
```

Il ciclo scorre tutti i livelli, trova eventuali `ExposureLayer` e aggiorna i suoi tre parametri chiave. Questo è il cuore del **renderizzare il livello di regolazione dell'esposizione** con i tuoi valori personalizzati.

### Passo 3: Salva il file PSD modificato

```java
String psdPathAfterChange = dataDir + "ExposureAdjustmentLayerChanged.psd";  // Path to save the modified PSD file

im.save(psdPathAfterChange);  // Save the changes to the PSD file
```

Il PSD modificato mantiene intatti tutti i livelli originali, ma la regolazione dell'esposizione ora riflette le nuove impostazioni.

### Passo 4: Esporta il risultato come PNG

```java
String pngExportPath = dataDir + "ExposureAdjustmentLayerChanged.png";  // Path to save the PNG file

PngOptions saveOptions = new PngOptions();  // Create PNG options
saveOptions.setColorType(PngColorType.TruecolorWithAlpha);  // Set color type to Truecolor with Alpha

im.save(pngExportPath, saveOptions);  // Save as PNG
```

Usare `PngOptions` con `TruecolorWithAlpha` garantisce che il PNG esportato mantenga la piena profondità di colore e qualsiasi trasparenza dal PSD.

### Passo 5: Aggiungi un nuovo livello di regolazione dell'esposizione

Se hai bisogno di **aggiungere un nuovo livello di regolazione dell'esposizione** a un documento esistente, usa il seguente codice:

```java
String sourceFileName = dataDir + "PhotoExample.psd";  // Source PSD file path

PsdImage img = (PsdImage) Image.load(sourceFileName);  // Load the PSD file

ExposureLayer newLayer = img.addExposureAdjustmentLayer(2, -0.25f, 2f);  // Add new exposure adjustment layer

String psdPathAfterChange = dataDir + "PhotoExampleAddedExposure.psd";  // Path to save the modified PSD file
String pngExportPath = dataDir + "PhotoExampleAddedExposure.png";  // Path to save the PNG file

img.save(psdPathAfterChange);  // Save the changes to the PSD file

PngOptions options = new PngOptions();  // Create PNG options
options.setColorType(PngColorType.TruecolorWithAlpha);  // Set color type to Truecolor with Alpha

img.save(pngExportPath, options);  // Save as PNG
```

Il metodo `addExposureAdjustmentLayer` crea un nuovo livello di regolazione con i valori di esposizione, offset e gamma specificati, quindi puoi renderizzarlo ed esportarlo come prima.

## Problemi comuni e consigli

- **Layer non trovato** – Assicurati che il PSD contenga effettivamente un `ExposureLayer`. Usa `instanceof ExposureLayer` come mostrato per evitare `ClassCastException`.
- **Errori di percorso file** – Usa percorsi assoluti o verifica che `dataDir` termini con un separatore di file (`/` o `\`).
- **Eccezione di licenza** – L'esecuzione senza una licenza valida aggiungerà una filigrana all'output. Registra la tua licenza all'inizio del codice (`License license = new License(); license.setLicense("Aspose.PSD.lic");`).

## FAQ

### Cos'è Aspose.PSD for Java?

Aspose.PSD for Java è una libreria che consente di creare, modificare e convertire file PSD in modo programmatico usando Java. Offre funzionalità complete per lavorare con documenti Photoshop.

### Posso usare Aspose.PSD for Java per manipolare altri tipi di livelli?

Sì, Aspose.PSD for Java supporta vari tipi di livelli, inclusi livelli di testo, livelli di regolazione e livelli immagine, consentendo una manipolazione estesa dei file PSD.

### Come iniziare con Aspose.PSD for Java?

Puoi iniziare scaricando la libreria dal [website](https://releases.aspose.com/psd/java/) e consultando la [documentation](https://reference.aspose.com/psd/java/) per guide dettagliate ed esempi.

### È disponibile una versione di prova gratuita per Aspose.PSD for Java?

Sì, è disponibile una versione di prova gratuita. Puoi scaricarla [here](https://releases.aspose.com/).

### Come posso ottenere supporto per Aspose.PSD for Java?

Per il supporto, puoi visitare il [Aspose support forum](https://forum.aspose.com/c/psd/34) dove puoi porre domande e ricevere aiuto dalla community.

**Domande aggiuntive**

**Q: Posso elaborare in batch più file PSD?**  
**A: Assolutamente. Avvolgi la logica di caricamento, modifica e salvataggio all'interno di un ciclo che itera su un elenco di percorsi di file.**

**Q: La libreria preserva la gerarchia dei livelli quando aggiungo un nuovo livello di esposizione?**  
**A: Sì. Il nuovo livello viene aggiunto sopra i livelli esistenti, mantenendo la gerarchia originale.**

**Q: Quali formati immagine posso esportare oltre a PNG?**  
**A: Aspose.PSD supporta JPEG, BMP, TIFF e diversi altri formati tramite le classi `*Options` corrispondenti.**

---

**Ultimo aggiornamento:** 2026-04-05  
**Testato con:** Aspose.PSD for Java 24.10  
**Autore:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}