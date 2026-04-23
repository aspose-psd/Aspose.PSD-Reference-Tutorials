---
date: 2026-02-09
description: Impara come utilizzare la sostituzione dei font di Aspose PSD in Java
  per gestire i file PSD con font mancanti, sostituire rapidamente i font mancanti
  nei PSD e esportare le immagini.
linktitle: Replace Fonts
second_title: Aspose.PSD Java API
title: Sostituzione dei font PSD di Aspose in Java – Sostituire i font mancanti
url: /it/java/advanced-image-manipulation/replace-fonts/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Sostituzione dei Font PSD di Aspose in Java

## Introduzione

Se devi sostituire i caratteri mancanti o indesiderati all'interno di un file Photoshop (PSD), **la sostituzione dei font di Aspose PSD** lo rende semplice. Nelle applicazioni Java puoi caricare un PSD, indicare ad Aspose quale font di fallback utilizzare e quindi salvare il risultato in qualsiasi formato desideri. Questo tutorial ti guida attraverso l'intero flusso di lavoro **aspose psd font substitution**, dall'impostazione del progetto all'esportazione dell'immagine aggiornata, così da gestire in modo affidabile gli scenari di font mancanti nei PSD senza aprire Photoshop.

## Risposte Rapide
- **Quale libreria gestisce la sostituzione dei font?** Aspose.PSD per Java  
- **Quanto tempo richiede l'implementazione?** Circa 5‑10 minuti per uno scenario di base  
- **Quale font viene usato come fallback predefinito?** Puoi impostare qualsiasi font TrueType, ad es. “Arial”  
- **Posso salvare in formati diversi da PNG?** Sì – PSD, JPEG, BMP, ecc. sono supportati  
- **È necessaria una licenza per la produzione?** È richiesta una licenza valida di Aspose.PSD per l'uso non‑trial  

## Cos'è la Sostituzione dei Font di Aspose PSD?

La sostituzione dei font di Aspose PSD è il processo di specificare un carattere sostitutivo che la libreria utilizzerà ogni volta che incontra un font mancante o non supportato in un file PSD. Questo garantisce che i livelli di testo vengano renderizzati correttamente senza modifiche manuali in Photoshop e ti consente di **gestire i font mancanti nei PSD** automaticamente.

## Perché Usare Aspose.PSD per Java?

- **Gestione completa dei PSD** – livelli, maschere, effetti e testo sono tutti accessibili tramite l'API.  
- **Cross‑platform** – funziona su qualsiasi OS che supporta Java.  
- **Nessuna dipendenza esterna** – la libreria gestisce internamente la sostituzione dei font, quindi non è necessario includere font aggiuntivi nella tua app.  

## Come Sostituire i Font Mancanti in un PSD con Aspose PSD

Di seguito trovi una guida passo‑passo che mostra **come sostituire i font mancanti nei PSD** con un font di fallback personalizzato.

## Prerequisiti

Prima di iniziare, assicurati di avere:

- **Java Development Kit (JDK)** – versione 8 o superiore installata.  
- **Aspose.PSD per Java** – scarica l'ultima JAR dalla [pagina di rilascio](https://releases.aspose.com/psd/java/).  
- **Un IDE** – IntelliJ IDEA, Eclipse o qualsiasi editor tu preferisca.  

## Importare i Pacchetti

Inizia importando le classi necessarie. Questo ti dà accesso al caricamento dell'immagine, alle opzioni di caricamento e alla funzionalità di salvataggio.

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

Crea un'istanza di `PsdLoadOptions`, specifica il font di fallback predefinito (ad es. **Arial**) e carica il PSD. Aspose applicherà automaticamente il fallback ogni volta che incontra un font mancante.

```java
PsdLoadOptions psdLoadOptions = new PsdLoadOptions(); 
psdLoadOptions.setDefaultReplacementFont("Arial");

PsdImage psdImage = (PsdImage)Image.load(dataDir + "Cloud_AzPlat_Banner3A_SB_EN_US_160x600_chinese_font.psd", psdLoadOptions);
```

## Passo 3: Salvare l'Immagine Sostituita

Dopo la sostituzione del font, puoi esportare l'immagine in qualsiasi formato supportato. Qui la salviamo come PNG, ma potresti anche scegliere JPEG, BMP o persino riscriverla in PSD.

```java
PngOptions pngOptions = new PngOptions();
psdImage.save(dataDir + "replaced_font.png", pngOptions);
```

## Problemi Comuni e Soluzioni

| Problema | Causa | Soluzione |
|----------|-------|-----------|
| Il testo appare illeggibile dopo la sostituzione | Il font di fallback non contiene i glifi necessari | Scegli un font che supporti l'intervallo Unicode richiesto (ad es. “Arial Unicode MS”). |
| `OutOfMemoryError` su PSD di grandi dimensioni | Caricamento di un file ad altissima risoluzione senza sufficiente heap | Aumenta la dimensione dell'heap JVM (`-Xmx2g`) o carica l'immagine in modalità streaming se disponibile. |
| Eccezione di licenza | Uso della versione trial in produzione | Applica una licenza valida permanente o temporanea prima di caricare l'immagine. |

## Domande Frequenti

**D: Posso sostituire i font in altri formati di immagine oltre al PSD?**  
R: Sì. Sebbene il caso d'uso principale sia il PSD, Aspose.PSD supporta anche PNG, JPEG, BMP e TIFF, consentendo la sostituzione dei font dove esistono livelli di testo.

**D: Il font di sostituzione predefinito è obbligatorio?**  
R: No. Puoi impostare qualsiasi font TrueType tu preferisca, oppure omettere l'impostazione per far usare ad Aspose il suo default interno.

**D: Ci sono requisiti di licenza per l'uso di Aspose.PSD?**  
R: È necessaria una licenza commerciale per le distribuzioni in produzione. Consulta la [pagina di acquisto](https://purchase.aspose.com/buy) per i dettagli.

**D: È possibile ottenere una licenza temporanea per i test?**  
R: Assolutamente. Aspose offre licenze temporanee gratuite per la valutazione – visita la [pagina delle licenze temporanee](https://purchase.aspose.com/temporary-license/).

**D: Dove posso trovare supporto aggiuntivo o discutere problemi relativi ad Aspose.PSD?**  
R: Il forum della community è un ottimo posto per porre domande: [forum Aspose.PSD](https://forum.aspose.com/c/psd/34).

**D: Come gestire PSD che contengono più font mancanti?**  
R: Imposta il font di sostituzione predefinito una sola volta (come mostrato) – verrà applicato a *tutti* i font mancanti durante l'operazione di caricamento.

**D: È possibile sostituire i font dopo che l'immagine è stata salvata?**  
R: La sostituzione dei font deve avvenire durante la fase di caricamento. Per cambiare i font in seguito, ricarica il PSD con un diverso font di fallback e salva nuovamente.

## Conclusione

Ora hai visto un flusso di lavoro completo **aspose psd font substitution** in Java—dall'importazione delle classi corrette, alla configurazione di un font di fallback, al caricamento del PSD, fino all'esportazione dell'immagine corretta. Integra questo modello nei tuoi pipeline di elaborazione immagini per garantire una tipografia coerente su tutti i tuoi asset PSD e per **gestire i font mancanti nei PSD** automaticamente.

---

**Ultimo aggiornamento:** 2026-02-09  
**Testato con:** Aspose.PSD per Java 24.12 (ultima versione al momento della scrittura)  
**Autore:** Aspose  

---

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
