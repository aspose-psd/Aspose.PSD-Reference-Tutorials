---
date: 2025-12-05
description: Scopri come eseguire la sostituzione dei font in Aspose PSD con Java.
  Questo tutorial passo‑passo di manipolazione delle immagini in Java ti mostra come
  sostituire i font nei file PSD in modo efficiente.
language: it
linktitle: Replace Fonts
second_title: Aspose.PSD Java API
title: Sostituzione dei font PSD di Aspose in Java – Sostituisci i font nei file PSD
url: /java/advanced-image-manipulation/replace-fonts/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Sostituzione dei Font Aspose PSD in Java

## Introduzione

Se devi sostituire caratteri mancanti o indesiderati all'interno di un file Photoshop (PSD), la **sostituzione dei font Aspose PSD** lo rende semplice. Nelle applicazioni Java puoi caricare un PSD, indicare ad Aspose quale font di fallback utilizzare, e poi salvare il risultato in qualsiasi formato desideri. Questo tutorial ti guida attraverso l'intero flusso di lavoro della **sostituzione dei font Aspose PSD**, dalla configurazione del progetto all'esportazione dell'immagine aggiornata.

## Risposte Rapide
- **Quale libreria gestisce la sostituzione dei font?** Aspose.PSD per Java  
- **Quanto tempo richiede l'implementazione?** Circa 5‑10 minuti per uno scenario di base  
- **Quale font viene usato come fallback predefinito?** Puoi impostare qualsiasi font TrueType, ad es. “Arial”  
- **Posso salvare in formati diversi da PNG?** Sì – PSD, JPEG, BMP, ecc. sono supportati  
- **È necessaria una licenza per la produzione?** È richiesta una licenza valida di Aspose.PSD per l'uso non‑trial  

## Cos'è la Sostituzione dei Font Aspose PSD?

La sostituzione dei font Aspose PSD è il processo di specificare un carattere sostitutivo che la libreria utilizzerà ogni volta che incontra un font mancante o non supportato in un file PSD. Questo garantisce che i livelli di testo vengano renderizzati correttamente senza dover intervenire manualmente in Photoshop.

## Perché Usare Aspose.PSD per Java?

- **Gestione completa dei PSD** – livelli, maschere, effetti e testo sono tutti accessibili tramite l'API.  
- **Cross‑platform** – funziona su qualsiasi OS che supporta Java.  
- **Nessuna dipendenza esterna** – la libreria gestisce internamente la sostituzione dei font, quindi non è necessario includere font aggiuntivi nella tua app.  

## Prerequisiti

Prima di iniziare, assicurati di avere:

- **Java Development Kit (JDK)** – versione 8 o superiore installata.  
- **Aspose.PSD per Java** – scarica l'ultimo JAR dalla [pagina di rilascio](https://releases.aspose.com/psd/java/).  
- **Un IDE** – IntelliJ IDEA, Eclipse o qualsiasi editor tu preferisca.  

## Importare i Pacchetti

Inizia importando le classi necessarie. Questo ti dà accesso al caricamento delle immagini, alle opzioni di caricamento e alla funzionalità di salvataggio.

```java
import com.aspose.psd.Image;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
import com.aspose.psd.imageoptions.PngOptions;
```

## Passo 1: Impostare la Directory del Documento

Definisci la cartella che contiene il file PSD di origine. Sostituisci il segnaposto con il percorso reale sul tuo computer.

```java
String dataDir = "Your Document Directory";
```

## Passo 2: Caricare l'Immagine con un Font di Sostituzione

Crea un'istanza di `PsdLoadOptions`, specifica il font di sostituzione predefinito (ad es. **Arial**) e carica il PSD. Aspose applicherà automaticamente il fallback ogni volta che incontra un font mancante.

```java
PsdLoadOptions psdLoadOptions = new PsdLoadOptions(); 
psdLoadOptions.setDefaultReplacementFont("Arial");

PsdImage psdImage = (PsdImage)Image.load(dataDir + "Cloud_AzPlat_Banner3A_SB_EN_US_160x600_chinese_font.psd", psdLoadOptions);
```

## Passo 3: Salvare l'Immagine Sostituita

Dopo la sostituzione del font, puoi esportare l'immagine in qualsiasi formato supportato. Qui la salviamo come PNG, ma potresti scegliere JPEG, BMP o persino riscriverla in PSD.

```java
PngOptions pngOptions = new PngOptions();
psdImage.save(dataDir + "replaced_font.png", pngOptions);
```

## Problemi Comuni e Soluzioni

| Problema | Causa | Soluzione |
|----------|-------|-----------|
| Il testo appare illeggibile dopo la sostituzione | Il font di fallback non contiene i glifi richiesti | Scegli un font che supporti l'intervallo Unicode necessario (ad es. “Arial Unicode MS”). |
| `OutOfMemoryError` su PSD di grandi dimensioni | Caricamento di un file ad altissima risoluzione senza sufficiente heap | Aumenta la dimensione dell'heap JVM (`-Xmx2g`) o carica l'immagine in modalità streaming se disponibile. |
| Eccezione di licenza | Uso della versione trial in produzione | Applica una licenza permanente o temporanea valida prima di caricare l'immagine. |

## Domande Frequenti

**D: Posso sostituire i font in altri formati immagine oltre al PSD?**  
R: Sì. Sebbene il caso d'uso principale sia il PSD, Aspose.PSD supporta anche PNG, JPEG, BMP e TIFF, consentendo la sostituzione dei font dove esistono livelli di testo.

**D: Il font di sostituzione predefinito è obbligatorio?**  
R: No. Puoi impostare qualsiasi font TrueType tu preferisca, o omettere l'impostazione per far usare ad Aspose il suo default interno.

**D: Ci sono requisiti di licenza per l'uso di Aspose.PSD?**  
R: È necessaria una licenza commerciale per le distribuzioni in produzione. Consulta la [pagina di acquisto](https://purchase.aspose.com/buy) per i dettagli.

**D: Posso ottenere una licenza temporanea per i test?**  
R: Assolutamente. Aspose offre licenze temporanee gratuite per la valutazione – visita la [pagina della licenza temporanea](https://purchase.aspose.com/temporary-license/).

**D: Dove posso trovare supporto aggiuntivo o discutere problemi relativi ad Aspose.PSD?**  
R: Il forum della community è un ottimo posto per porre domande: [forum Aspose.PSD](https://forum.aspose.com/c/psd/34).

**D: Come gestire PSD che contengono più font mancanti?**  
R: Imposta una volta il font di sostituzione predefinito (come mostrato) – verrà applicato a *tutti* i font mancanti durante l'operazione di caricamento.

**D: È possibile sostituire i font dopo che l'immagine è stata salvata?**  
R: La sostituzione del font deve avvenire durante la fase di caricamento. Per cambiare i font in seguito, ricarica il PSD con un diverso font di sostituzione e salva nuovamente.

## Conclusione

Ora hai visto un flusso di lavoro completo per la **sostituzione dei font Aspose PSD** in Java—dall'importazione delle classi corrette, alla configurazione di un font di fallback, al caricamento del PSD, fino all'esportazione dell'immagine corretta. Integra questo modello nei tuoi pipeline di elaborazione immagini per garantire una tipografia coerente in tutti i tuoi asset PSD.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Ultimo aggiornamento:** 2025-12-05  
**Testato con:** Aspose.PSD per Java 24.12 (ultima versione al momento della scrittura)  
**Autore:** Aspose  

---