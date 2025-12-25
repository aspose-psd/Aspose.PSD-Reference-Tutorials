---
date: 2025-12-25
description: Scopri come sostituire i font nei file PSD con Aspose.PSD per Java –
  una guida passo‑passo che mostra anche come salvare i PSD in PNG e gestire i font
  mancanti.
linktitle: Settings for Replacing Missing Fonts
second_title: Aspose.PSD Java API
title: Come sostituire i font in Aspose.PSD per Java
url: /it/java/advanced-techniques/settings-replacing-missing-fonts/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Come sostituire i font in Aspose.PSD per Java

## Introduzione

Se lavori con file Photoshop (PSD) in un'applicazione Java, i font mancanti possono rompere il layout visivo e causare errori di rendering. **Come sostituire i font** in modo rapido e affidabile è essenziale per mantenere la fedeltà del design. In questo tutorial imparerai a usare Aspose.PSD per Java per sostituire i font mancanti, convertire il risultato in PNG e mantenere fluido il tuo flusso di lavoro di conversione delle immagini. Alla fine, sarai in grado di sostituire i font nelle immagini, salvare PSD come PNG e evitare le insidie comuni che gli sviluppatori incontrano.

## Risposte rapide
- **Che cosa significa “replace fonts” nell'elaborazione PSD?** Sostituisce i caratteri mancanti o non disponibili con un font di fallback che specifichi.  
- **Quale libreria gestisce questo automaticamente?** Aspose.PSD per Java fornisce `PsdLoadOptions.setDefaultReplacementFont`.  
- **Posso anche convertire il PSD in PNG dopo la sostituzione?** Sì – usa `PngOptions` e chiama `psdImage.save`.  
- **È necessaria una licenza per l'uso in produzione?** È richiesta una licenza valida di Aspose.PSD per build non‑valutazione.  
- **Quale versione di Java è supportata?** Qualsiasi runtime Java 8+ funziona con l'attuale versione di Aspose.PSD.

## Che cos'è la sostituzione dei font nei file PSD?

Quando un PSD fa riferimento a un font che non è installato sulla macchina host, il motore di rendering ricorre a un font generico, spesso provocando testo disallineato. La sostituzione dei font ti permette di definire un font predefinito (ad esempio Arial) che la libreria utilizzerà ogni volta che incontra un tipo di carattere mancante, garantendo un output visivo coerente.

## Perché sostituire i font mancanti con Aspose.PSD?

- **Soluzione a zero dipendenze** – Non è necessario Photoshop nativo o strumenti esterni.  
- **Pronta per il batch** – Elabora decine di file in un ciclo con le stesse impostazioni.  
- **Pronta per la conversione di immagini** – Dopo la sostituzione puoi direttamente **salvare PSD come PNG** o **convertire PSD in PNG** senza passaggi aggiuntivi.  
- **Cross‑platform** – Funziona su runtime Java Windows, Linux e macOS.

## Prerequisiti

1. **Libreria Aspose.PSD** – Scarica e installa la libreria Aspose.PSD per Java dalla [pagina dei rilasci](https://releases.aspose.com/psd/java/).  
2. **Ambiente di sviluppo Java** – JDK 8 o successivo installato e configurato.  

Ora che abbiamo le basi, immergiamoci nel codice.

## Importa i pacchetti

Inizia importando le classi necessarie di Aspose.PSD. Questo ti dà accesso al caricamento delle immagini, alle opzioni di sostituzione dei font e alle capacità di esportazione PNG.

```java
import com.aspose.psd.Image;

import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
import com.aspose.psd.imageoptions.PngOptions;
```

## Passo 1: Configura la directory del documento

Definisci la cartella che contiene il PSD di origine e dove verrà salvato il PNG risultante.

```java
String dataDir = "Your Document Directory";
```

## Passo 2: Specifica i file di origine e destinazione

Fornisci i percorsi completi per il PSD di input e il PNG di output. Questo rende il flusso di lavoro chiaro e mantiene il codice facile da mantenere.

```java
String sourceFile = dataDir + "sample.psd";
String destName = dataDir + "result.png";
```

## Passo 3: Configura le impostazioni di sostituzione dei font

Crea un'istanza di `PsdLoadOptions` e indica ad Aspose.PSD quale font usare quando incontra uno mancante. In questo esempio usiamo **Arial**, ma puoi sostituirlo con qualsiasi font installato sul tuo sistema.

```java
PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setDefaultReplacementFont("Arial");
```

## Passo 4: Carica l'immagine PSD e sostituisci i font

Carica il PSD usando le opzioni definite sopra. La libreria scambia automaticamente i font mancanti con quello predefinito specificato.

```java
Image image = Image.load(sourceFile, loadOptions);
PsdImage psdImage = (PsdImage) image;
```

## Passo 5: Salva l'immagine modificata

Configura le opzioni di esportazione PNG—true color con canale alfa—per preservare la trasparenza. Questo passaggio dimostra anche **image conversion PSD to PNG** dopo la sostituzione dei font.

```java
PngOptions options = new PngOptions();
options.setColorType(PngColorType.TruecolorWithAlpha);
psdImage.save(destName, options);
```

### Cosa è successo?

- Il PSD è stato aperto con un font di fallback (Arial).  
- Tutti i livelli di testo che originariamente facevano riferimento a font mancanti ora vengono renderizzati usando Arial.  
- L'immagine finale è stata salvata come PNG, effettuando effettivamente **salvare PSD come PNG** mantenendo la fedeltà visiva.

## Problemi comuni e risoluzione

| Problema | Causa | Soluzione |
|----------|-------|-----------|
| Il testo appare ancora errato | Le metriche del font differiscono (dimensione, peso) | Regola la dimensione del font di sostituzione programmaticamente o scegli un font con metriche simili. |
| Il PNG è più grande del previsto | Le opzioni PNG predefinite usano colore a 32‑bit | Passa `PngColorType` a `Truecolor` se l'alpha non è necessario. |
| Eccezione di licenza | Esecuzione senza una licenza valida | Applica una licenza temporanea o permanente di Aspose.PSD prima di caricare l'immagine. |

## Domande frequenti

**Q: Aspose.PSD è compatibile con tutte le versioni di file PSD?**  
A: Aspose.PSD supporta un'ampia gamma di versioni PSD, dalle prime release di Photoshop fino alle funzionalità più recenti.

**Q: Posso usare font personalizzati per la sostituzione in Aspose.PSD?**  
A: Sì, basta passare il nome del font personalizzato a `setDefaultReplacementFont`. Assicurati che il font sia accessibile alla JVM.

**Q: Sono disponibili opzioni di licenza per Aspose.PSD?**  
A: Esplora le opzioni di licenza [qui](https://purchase.aspose.com/buy) per scegliere il piano migliore per le tue esigenze.

**Q: Esiste un forum della community per il supporto di Aspose.PSD?**  
A: Sì, visita il [forum Aspose.PSD](https://forum.aspose.com/c/psd/34) per supporto della community e discussioni.

**Q: Come posso ottenere una licenza temporanea per Aspose.PSD?**  
A: Ottieni una licenza temporanea [qui](https://purchase.aspose.com/temporary-license/) per scopi di test e valutazione.

---

**Ultimo aggiornamento:** 2025-12-25  
**Testato con:** Aspose.PSD 24.11 per Java (latest at time of writing)  
**Autore:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}