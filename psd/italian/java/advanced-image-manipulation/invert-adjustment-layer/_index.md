---
date: 2026-11-04
description: Scopri come utilizzare Aspose.PSD per Java per applicare un invert adjustment
  layer, elaborare in batch immagini PSD e creare file PSD di immagine negativa.
keywords:
- how to use aspose
- batch process psd images
- create negative image psd
- image processing java library
- apply multiple adjustment layers
lastmod: 2026-11-04
linktitle: Invert Adjustment Layer
og_description: Come utilizzare Aspose.PSD per Java per aggiungere un invert adjustment
  layer, elaborare in batch immagini PSD e creare un'immagine negativa PSD. Segui
  la guida passo‑passo.
og_image_alt: Screenshot showing Aspose.PSD Java code adding an invert adjustment
  layer
og_title: Come utilizzare Aspose.PSD per aggiungere un invert adjustment layer in
  Java
schemas:
- author: Aspose
  dateModified: '2026-11-04'
  description: Learn how to use Aspose.PSD for Java to apply an invert adjustment
    layer, batch process PSD images, and create negative image PSD files.
  headline: How to use Aspose.PSD to add an invert adjustment layer in Java
  type: TechArticle
- questions:
  - answer: Yes, it supports Java 6.0 and later, including Java 8, 11, and 17.
    question: Is Aspose.PSD compatible with all Java versions?
  - answer: Absolutely. After adding the invert layer you can call `addBrightnessAdjustmentLayer()`,
      `addHueSaturationAdjustmentLayer()`, etc., to stack effects.
    question: Can I apply multiple adjustment layers in a single operation?
  - answer: The complete documentation is available [Aspose.PSD Java API reference](https://reference.aspose.com/psd/java/).
    question: Where can I find the full API reference?
  - answer: Yes, you can download a trial version [Aspose.PSD trial download](https://releases.aspose.com/).
    question: Is there a free trial for Aspose.PSD?
  - answer: Request a temporary license [temporary license request page](https://purchase.aspose.com/temporary-license/).
    question: How do I obtain a temporary license for testing?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- aspose psd
- java image processing
- invert adjustment layer
- batch psd processing
title: Come utilizzare Aspose.PSD per aggiungere un invert adjustment layer in Java
url: /it/java/advanced-image-manipulation/invert-adjustment-layer/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Come utilizzare Aspose.PSD per aggiungere un livello di regolazione Invert in Java

## Introduzione

Se stai cercando una robusta **image processing java library**, Aspose.PSD per Java è una delle opzioni più versatili sul mercato. In questo tutorial vedrai **come usare Aspose** per inserire un **Invert Adjustment Layer** in un file PSD, impilarlo con altre regolazioni e persino eseguire l'operazione su decine di file. Che tu stia creando uno strumento di elaborazione batch, un servizio di immagini lato server o un editor di immagini singole, i passaggi seguenti ti porteranno dal PSD di origine a un'immagine negativa completamente modificabile in pochi minuti.

## Risposte rapide

- **Che cosa fa l'Invert Adjustment Layer?** Inverte ogni valore RGB nell'area selezionata, trasformando l'immagine in un negativo fotografico.  
- **Quale libreria fornisce questa funzionalità?** Aspose.PSD, una **image processing java library** leader.  
- **Posso impilarlo con altre regolazioni?** Sì – puoi **applicare più livelli di regolazione** come Luminosità/Contrasto, Tinta/Saturazione e altro.  
- **Ho bisogno di una licenza per lo sviluppo?** È disponibile una versione di prova gratuita; è necessaria una licenza per l'uso in produzione.  
- **Quanto tempo richiede l'implementazione?** Tipicamente meno di 10 minuti per un caso d'uso di base.

## Che cos'è l'Invert Adjustment Layer?

Il livello di regolazione Invert è una modifica non distruttiva che inverte i valori di colore di ogni pixel che colpisce. Poiché si trova sopra lo stack dei livelli, puoi attivare/disattivare la sua visibilità o riordinarlo senza alterare permanentemente i dati dell'immagine originale. Questo è il modo più rapido per **creare file PSD di immagine negativa** o ottenere un aspetto classico di negativo cinematografico.

## Perché usare Aspose.PSD come la tua image processing java library?

Aspose.PSD supporta **oltre 200 funzionalità PSD**, può leggere e scrivere file Photoshop senza richiedere Photoshop, e elabora documenti multi‑centinaia di pagine usando meno di 500 MB di memoria heap. Funziona su qualsiasi runtime Java (Java 6+), rendendolo ideale per **elaborare in batch immagini psd** su server Windows, Linux o macOS.

## Prerequisiti

Prima di iniziare, assicurati di avere:

1. **Aspose.PSD for Java** – scarica l'ultimo JAR dal sito ufficiale [Aspose.PSD for Java download page](https://releases.aspose.com/psd/java/).  
2. **Java Development Kit** – JDK 6.0 o successivo installato e configurato nel tuo `PATH`.  

Ora sei pronto per scrivere il codice.

## Importa pacchetti

La classe `PsdImage` rappresenta un intero documento Photoshop in memoria, mentre le classi dei livelli di regolazione si trovano nel pacchetto `com.aspose.psd.layers.adjustments`.

La classe `PsdImage` è l'oggetto di livello superiore di Aspose.PSD che incapsula la struttura e i dati pixel di un file PSD. Importa gli spazi dei nomi, quindi potrai caricare, modificare e salvare file PSD.

## Passo 1: configura la directory del documento

Definisci la cartella che contiene il tuo file PSD di origine e dove verrà salvato l'output. L'uso di percorsi assoluti evita `NullPointerException` quando la directory di lavoro cambia.

## Passo 2: carica il file PSD

Carica il file di origine in un oggetto `PsdImage`. Questo oggetto contiene l'intera gerarchia dei livelli in memoria, consentendo modifiche non distruttive.

La classe `PsdImage` fornisce un metodo statico `load` che legge l'intestazione del file, ne valida il formato e costruisce una rappresentazione in memoria pronta per la manipolazione.

## Passo 3: aggiungi il livello di regolazione Invert

Chiama il metodo incorporato per inserire un Invert Adjustment Layer sopra lo stack dei livelli corrente. Puoi successivamente aggiungere altri livelli (ad es., Luminosità, Tinta) per **applicare più livelli di regolazione** in un unico flusso di lavoro.

`addInvertAdjustmentLayer()` aggiunge un Invert Adjustment Layer alla collezione dei livelli del PSD.

## Passo 4: salva l'output

Salva il PSD modificato su disco.  

`save()` scrive il file PSD, includendo tutti i livelli e i metadati, nel percorso specificato.

Il salvataggio utilizza lo stesso metodo `save` che scrive l'intero documento, includendo tutti i livelli di regolazione, le maschere e i metadati, nel formato specificato.

### Cosa è successo?

Il file PSD è stato caricato in un oggetto `PsdImage`, è stato creato un `InvertAdjustmentLayer` e aggiunto come livello più alto, e il documento è stato salvato. Questa sequenza preserva i dati originali dell'immagine aggiungendo un effetto invert non distruttivo che può essere attivato/disattivato o riordinato in seguito.

Ora hai usato con successo Aspose.PSD, una **image processing java library**, per manipolare un file PSD.

## Come elaborare in batch immagini PSD con regolazione invert?

Carica ogni file all'interno di un ciclo `for`, applica gli stessi passaggi e chiama `save` per ogni iterazione. Poiché Aspose.PSD elabora i file in modalità streaming, puoi gestire **centinaia di PSD** mantenendo l'uso di memoria sotto i 300 MB riutilizzando la stessa istanza `PsdImage`.

## Come convertire un PSD in un'immagine negativa?

Aggiungi il Invert Adjustment Layer come elemento più alto e salva il documento – questa operazione è equivalente a **convert PSD to negative**. Puoi successivamente disabilitare o eliminare il livello per tornare all'aspetto originale senza ricaricare il file di origine.

## Problemi comuni e suggerimenti

| Issue | Cause | Solution |
|-------|-------|----------|
| **NullPointerException su `Image.load`** | Percorso file errato o file mancante | Verifica `dataDir` e il nome del file; usa percorsi assoluti per i test |
| **Ordine dei livelli non come previsto** | Aggiungere livelli dopo quelli esistenti modifica lo stacking | Inserisci il livello invert prima di altre regolazioni, o riordina tramite `psdImage.getLayers().move()` |
| **Rallentamento delle prestazioni su PSD grandi** | Caricamento di file molto grandi in memoria | Aumenta l'heap JVM (`-Xmx2g`) o elabora i file a blocchi usando `psdImage.getPages().get(0).getResources().setMemoryOptimized(true)` |

## Domande frequenti

**Q: Aspose.PSD è compatibile con tutte le versioni Java?**  
**A:** Sì, supporta Java 6.0 e successive, incluse Java 8, 11 e 17.

**Q: Posso applicare più livelli di regolazione in un'unica operazione?**  
**A:** Assolutamente. Dopo aver aggiunto il livello invert puoi chiamare `addBrightnessAdjustmentLayer()`, `addHueSaturationAdjustmentLayer()`, ecc., per impilare gli effetti.

**Q: Dove posso trovare la documentazione completa dell'API?**  
**A:** La documentazione completa è disponibile [Aspose.PSD Java API reference](https://reference.aspose.com/psd/java/).

**Q: È disponibile una versione di prova gratuita per Aspose.PSD?**  
**A:** Sì, puoi scaricare una versione di prova [Aspose.PSD trial download](https://releases.aspose.com/).

**Q: Come posso ottenere una licenza temporanea per i test?**  
**A:** Richiedi una licenza temporanea [temporary license request page](https://purchase.aspose.com/temporary-license/).

---

**Ultimo aggiornamento:** 2026-11-04  
**Testato con:** Aspose.PSD 24.12 per Java  
**Autore:** Aspose  









```java
import com.aspose.psd.Image;

import com.aspose.psd.fileformats.psd.PsdImage;
```

```java
String dataDir = "Your Document Directory";
```

```java
String filePath = dataDir + "InvertStripes_before.psd";
String outputPath = dataDir + "InvertStripes_after.psd";

PsdImage im = (PsdImage)Image.load(filePath);
```

```java
im.addInvertAdjustmentLayer();
```

```java
im.save(outputPath);
```

## Tutorial correlati

- [Aggiungi livello di regolazione Livello ai file PSD con Aspose.PSD per Java](/psd/java/modifying-converting-psd-images/add-level-adjustment-layer-psd/)
- [Come aggiungere livello di regolazione – Mixer di canale in PSD (Java)](/psd/java/modifying-converting-psd-images/add-channel-mixer-adjustment-layer-psd/)
- [Come modificare PSD - Aggiungere livello di regolazione Curve usando Java](/psd/java/modifying-converting-psd-images/add-curves-adjustment-layer-psd/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}