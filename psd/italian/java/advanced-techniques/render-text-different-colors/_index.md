---
date: 2026-05-29
description: Scopri come salvare un PSD come PNG con testo colorato usando Aspose.PSD
  per Java. Questa guida passo‑passo mostra come convertire PSD in PNG in modo efficiente.
keywords:
- save psd as png
- convert psd to png
- Aspose.PSD Java
linktitle: Renderizza testo con colori diversi nel livello di testo
schemas:
- author: Aspose
  dateModified: '2026-05-29'
  description: Learn how to save PSD as PNG with colored text using Aspose.PSD for
    Java. This step‑by‑step guide shows how to convert PSD to PNG efficiently.
  headline: Save PSD as PNG with Colored Text using Aspose.PSD for Java
  type: TechArticle
- questions:
  - answer: Aspose.PSD is primarily designed for Java, but Aspose provides similar
      libraries for various programming languages.
    question: Can I use Aspose.PSD for Java with other programming languages?
  - answer: Yes, you can obtain a free trial version from [Aspose.PSD](https://releases.aspose.com/).
    question: Is there a trial version available for Aspose.PSD for Java?
  - answer: Visit the [Aspose.PSD forum](https://forum.aspose.com/c/psd/34) for community
      support and discussions.
    question: Where can I find additional support or assistance?
  - answer: You can request a temporary license from [Aspose.PSD](https://purchase.aspose.com/temporary-license/).
    question: How can I obtain a temporary license for Aspose.PSD for Java?
  - answer: Yes, explore the [Aspose.PSD documentation](https://reference.aspose.com/psd/java/)
      for more tutorials and examples.
    question: Are there other tutorials available for Aspose.PSD?
  type: FAQPage
second_title: Aspose.PSD Java API
title: Salva PSD come PNG con testo colorato usando Aspose.PSD per Java
url: /it/java/advanced-techniques/render-text-different-colors/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Salva PSD come PNG con Testo Colorato usando Aspose.PSD per Java

Benvenuti alla nostra guida passo‑passo su come **salvare PSD come PNG** con testo di diversi colori usando Aspose.PSD per Java. Aspose.PSD è una potente libreria Java che consente di manipolare i file Photoshop programmaticamente, offrendoti ampie capacità di lavorare con i formati di file PSD e PSB.

In questo tutorial, ti guideremo attraverso il processo di rendering del testo con vari colori in un livello di testo usando Aspose.PSD. Alla fine di questa guida, avrai una chiara comprensione di come eseguire questa operazione senza problemi.

## Risposte Rapide
- **Come salvare PSD come PNG?** Usa la classe `PsdImage` di Aspose.PSD per caricare il PSD e chiamare `save` con `PngOptions`.
- **Posso renderizzare più colori in un unico livello di testo?** Sì, assegna diversi oggetti `Color` a ciascuna `Portion` del testo.
- **Quale versione di Java è richiesta?** È supportata Java 8 o superiore.
- **È necessaria una licenza per la produzione?** È richiesta una licenza commerciale; è disponibile una versione di prova gratuita.
- **La libreria è efficiente in termini di memoria per file di grandi dimensioni?** Può gestire file fino a 2 GB senza caricarli completamente in memoria.

## Come salvare PSD come PNG con testo colorato?

Carica il tuo file PSD, modifica le porzioni del livello di testo per assegnare colori distinti, quindi salva l'immagine come PNG—tutto questo flusso di lavoro viene eseguito in poche righe di codice Java. Aspose.PSD rasterizza automaticamente il livello modificato, preservando trasparenza e fedeltà dei colori, così il PNG risultante corrisponde al design originale.

## Cos'è Aspose.PSD per Java?

Aspose.PSD per Java è una libreria che consente la creazione, la modifica e la conversione programmatica di file Photoshop (PSD/PSB). Supporta **oltre 50 formati immagine** e può elaborare documenti con centinaia di pagine senza caricare l'intero file in memoria, offrendo alte prestazioni per l'automazione lato server.

## Prerequisiti

- Conoscenza di base della programmazione Java.
- Libreria Aspose.PSD per Java installata. Puoi scaricarla dalla [documentazione di Aspose.PSD per Java](https://reference.aspose.com/psd/java/).

## Importa Pacchetti

`Image` è la classe base per caricare e salvare file immagine. `PsdImage` rappresenta un documento Photoshop, mentre `TextLayer` fornisce l'accesso alle proprietà del livello di testo. `PngOptions` definisce le impostazioni per l'esportazione PNG.  
```java
import com.aspose.psd.Image;

import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.TextLayer;
import com.aspose.psd.imageoptions.PngOptions;
```

## Passo 1: Configura il tuo progetto

Crea un nuovo progetto Java e includi la libreria Aspose.PSD. Assicurati di avere le autorizzazioni necessarie per accedere e modificare i file nella directory del tuo progetto.

## Passo 2: Definisci le directory di origine e di output

Specifica le directory di origine e di output dove si trovano i tuoi file PSD e dove verranno salvate le immagini risultanti. Aggiorna le variabili `sourceDir` e `outputDir` di conseguenza.  
```java
String sourceDir = "Your Document Directory";
String outputDir = "Your Document Directory";
```

## Passo 3: Carica il file PSD e accedi al livello di testo

`PsdImage` carica un file PSD in memoria, e `TextLayer` consente la manipolazione del contenuto testuale all'interno di quel livello.  
```java
String targetFilePath = sourceDir + "text_ethalon_different_colors.psd";
String resultFilePath = outputDir + "RenderTextWithDifferentColorsInTextLayer_out.png";

PsdImage psdImage = null;
try
{
    psdImage = (PsdImage) Image.load(targetFilePath);
    TextLayer txtLayer = (TextLayer)psdImage.getLayers()[1];
    txtLayer.getTextData().updateLayerData();
```

## Passo 4: Imposta le opzioni PNG e salva l'immagine risultante

`PngOptions` configura i parametri di output PNG come il tipo di colore e la compressione.  
```java
    PngOptions pngOptions = new PngOptions();
    pngOptions.setColorType(PngColorType.TruecolorWithAlpha);
    psdImage.save(resultFilePath, pngOptions);
}
finally
{
    if (psdImage != null) psdImage.dispose();
}
```

## Problemi comuni e soluzioni

- **Eccezione di licenza mancante:** Assicurati di aver applicato un file di licenza valido prima di eseguire qualsiasi operazione di salvataggio.
- **Colore non applicato:** Verifica che ogni `Portion` nel livello di testo abbia la proprietà `Color` impostata correttamente.
- **Utilizzo di memoria per file di grandi dimensioni:** Usa la sovraccarico `load` di `PsdImage` con `loadOptions` per lo streaming di file di grandi dimensioni.

## Domande frequenti

**Q: Posso usare Aspose.PSD per Java con altri linguaggi di programmazione?**  
A: Aspose.PSD è principalmente progettato per Java, ma Aspose fornisce librerie simili per vari linguaggi di programmazione.

**Q: È disponibile una versione di prova per Aspose.PSD per Java?**  
A: Sì, puoi ottenere una versione di prova gratuita da [Aspose.PSD](https://releases.aspose.com/).

**Q: Dove posso trovare supporto o assistenza aggiuntiva?**  
A: Visita il [forum di Aspose.PSD](https://forum.aspose.com/c/psd/34) per supporto della community e discussioni.

**Q: Come posso ottenere una licenza temporanea per Aspose.PSD per Java?**  
A: Puoi richiedere una licenza temporanea da [Aspose.PSD](https://purchase.aspose.com/temporary-license/).

**Q: Ci sono altri tutorial disponibili per Aspose.PSD?**  
A: Sì, esplora la [documentazione di Aspose.PSD](https://reference.aspose.com/psd/java/) per ulteriori tutorial ed esempi.

**Q: La libreria supporta la conversione batch di più file PSD in PNG?**  
A: Sì, puoi iterare su una cartella di file PSD, applicare la stessa logica di colore del testo e salvare ciascuno come PNG usando un ciclo.

**Q: L'output PNG è lossless?**  
A: PNG salvato tramite Aspose.PSD mantiene la piena qualità lossless, preservando tutte le informazioni di colore e trasparenza.

---

**Ultimo aggiornamento:** 2026-05-29  
**Testato con:** Aspose.PSD 24.12 for Java  
**Autore:** Aspose

{{< blocks/products/products-backtop-button >}}

## Tutorial correlati

- [Esporta PSD in PNG e aggiungi un nuovo livello regolare usando Aspose.PSD per Java](/psd/java/advanced-image-effects/add-new-regular-layer/)
- [Salva PSD come PNG e applica l'ombra proiettata di rendering in Aspose.PSD per Java](/psd/java/advanced-image-manipulation/rendering-drop-shadow/)
- [Converti PSD in PNG con sovrapposizione di colore – Aspose.PSD per Java](/psd/java/advanced-image-manipulation/rendering-color-effect/)

{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}