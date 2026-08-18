---
date: 2026-03-26
description: Impara a esportare i livelli PSD in PNG usando Aspose.PSD per Java. Converti
  i file PSD in immagini raster ed esporta in batch i livelli PSD in modo efficiente.
linktitle: Export psd layers to png using Java
second_title: Aspose.PSD Java API
title: Esporta i livelli PSD in PNG con Java
url: /it/java/psd-image-modification-conversion/export-psd-layers-raster-images/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Esporta i livelli PSD in PNG usando Java

## Introduzione

Nel mondo del design digitale, lavorare con immagini a più livelli può essere sia un vantaggio sia una sfida. Immagina di aver trascorso ore a creare un’immagine fantastica in Photoshop (formato PSD), completa di più livelli che danno vita al tuo progetto. Ora potresti voler **export psd layers to png** in modo indipendente per un utilizzo successivo. È qui che Aspose.PSD per Java brilla, automatizzando il compito noioso di convertire ogni livello di un file PSD in immagini raster di alta qualità come PNG. In questa guida completa, ti accompagneremo attraverso l’intero processo, dalla configurazione dell’ambiente all’esportazione batch dei livelli PSD con poche righe di codice.

## Risposte rapide
- **Di cosa tratta il tutorial?** Esportare ogni livello PSD in un file PNG usando Aspose.PSD per Java.  
- **Beneficio principale?** Risparmia ore rispetto all'estrazione manuale in Photoshop.  
- **Prerequisiti?** JDK 8+, libreria Aspose.PSD e un file PSD di esempio.  
- **Posso esportare in altri formati raster?** Sì – è possibile convertire PSD in formati raster come BMP, TIFF o JPEG.  
- **È supportata l'elaborazione batch?** Assolutamente; il ciclo nel codice consente di esportare batch i livelli PSD in un'unica esecuzione.

## Che cosa significa “psd layers to png”?
Esportare **psd layers to png** significa prendere ogni singolo livello da un documento Photoshop e salvarlo come immagine PNG separata. PNG conserva la trasparenza, rendendolo ideale per grafiche web, asset UI e ulteriori elaborazioni di immagine.

## Perché usare Aspose.PSD per Java?
- **Nessun Photoshop necessario** – funziona su qualsiasi server o ambiente CI.  
- **Alta fedeltà** – conserva gli effetti dei livelli, le maschere e i canali alfa.  
- **Scalabile** – perfetto per l'esportazione batch dei livelli PSD in pipeline automatizzate.  

## Prerequisiti

Prima di immergerti nel codice, assicurati di avere quanto segue:

1. **Java Development Kit (JDK)** – versione 8 o superiore.  
2. **Aspose.PSD per Java** – scarica l'ultima libreria da [Aspose Releases](https://releases.aspose.com/psd/java/).  
3. **IDE** – IntelliJ IDEA, Eclipse o qualsiasi editor preferisci.  
4. **File PSD di esempio** – ad es., `sample.psd`, posizionato nella cartella del progetto.

Ora che sei pronto, iniziamo a programmare!

## Importa i pacchetti

Per prima cosa, importa le classi necessarie dalla libreria Aspose.PSD:

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.PngOptions;
```

Queste importazioni ti danno accesso al caricamento delle immagini, alle opzioni PNG e alla manipolazione dei livelli.

## Passo 1: Definisci la directory del documento

Specifica dove si trovano il PSD di origine e i file PNG risultanti:

```java
String dataDir = "Your Document Directory";
```

Sostituisci `"Your Document Directory"` con il percorso assoluto o relativo a `sample.psd`.

## Passo 2: Carica il file PSD

Carica il PSD in un oggetto `PsdImage` così da poter lavorare con i suoi livelli:

```java
PsdImage psdImage = (PsdImage) Image.load(dataDir + "sample.psd");
```

Il cast a `PsdImage` sblocca le funzionalità specifiche dei livelli.

## Passo 3: Configura le opzioni PNG

Imposta i parametri di esportazione PNG. Usare `TruecolorWithAlpha` mantiene intatta la trasparenza:

```java
PngOptions pngOptions = new PngOptions();
pngOptions.setColorType(PngColorType.TruecolorWithAlpha);
```

## Passo 4: Cicla attraverso i livelli ed esportane ciascuno

Itera su ogni livello e salvalo come file PNG individuale. Questo ciclo abilita **batch export psd layers** automaticamente:

```java
for (int i = 0; i < psdImage.getLayers().length; i++) {
    // Convert and save the layer to PNG file format.
    psdImage.getLayers()[i].save(dataDir + String.format("layer_out%d.png", i + 1), pngOptions);
}
```

Ogni iterazione produce `layer_out1.png`, `layer_out2.png` e così via.

## Problemi comuni e soluzioni

- **FileNotFoundException** – Verifica che `dataDir` punti alla cartella corretta e che `sample.psd` esista.  
- **OutOfMemoryError** – Per file PSD molto grandi, considera di elaborare i livelli in batch più piccoli o aumentare la dimensione dell'heap JVM (`-Xmx`).  
- **Trasparenza mancante** – Assicurati che `pngOptions.setColorType(PngColorType.TruecolorWithAlpha)` sia impostato; altrimenti, il PNG verrà salvato senza canale alfa.

## Domande frequenti

### Che cos'è Aspose.PSD per Java?
Aspose.PSD per Java è una potente libreria che consente agli sviluppatori di creare, modificare, convertire e renderizzare file Photoshop senza la necessità di Adobe Photoshop.

### Posso esportare i livelli in formati diversi da PNG?
Sì, Aspose.PSD supporta BMP, TIFF, JPEG e molti altri formati raster. Basta istanziare la classe di opzioni corrispondente (ad es., `JpegOptions`) e passarla al metodo `save`.

### È disponibile una versione di prova gratuita per Aspose.PSD?
Assolutamente! Puoi provare Aspose.PSD gratuitamente scaricandolo dalla loro [pagina di prova gratuita](https://releases.aspose.com/).

### Cosa fare se incontro problemi usando Aspose.PSD?
Puoi cercare aiuto e supporto nella community di Aspose. Visita i loro forum di supporto [qui](https://forum.aspose.com/c/psd/34).

### Dove posso acquistare una licenza per Aspose.PSD?
Puoi acquistare facilmente una licenza per Aspose.PSD dalla loro pagina di acquisto [qui](https://purchase.aspose.com/buy).

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Ultimo aggiornamento:** 2026-03-26  
**Testato con:** Aspose.PSD for Java 24.12 (latest)  
**Autore:** Aspose