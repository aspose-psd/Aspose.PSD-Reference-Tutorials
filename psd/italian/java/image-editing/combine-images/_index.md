---
date: 2025-12-30
description: Scopri come creare un file PSD in Java combinando due immagini con Aspose.PSD.
  Segui la nostra guida passo passo per unire rapidamente le immagini in un file PSD.
linktitle: Combine Images
second_title: Aspose.PSD Java API
title: Come creare un file PSD in Java – Unire le immagini con Aspose.PSD
url: /it/java/image-editing/combine-images/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Crea file PSD in Java – Unisci immagini con Aspose.PSD

## Introduzione

Se devi **creare un file PSD in Java** unendo diverse immagini, Aspose.PSD rende il lavoro semplice. In questo tutorial vedremo come combinare due immagini in un unico canvas PSD, spiegheremo perché questo approccio è utile e ti forniremo del codice pronto all'uso. Alla fine sarai in grado di **unire due immagini in stile Java** e generare un file a più livelli dall'aspetto professionale.

## Risposte rapide
- **Quale libreria è la migliore per unire immagini in PSD?** Aspose.PSD per Java.  
- **Quanto tempo richiede l'implementazione?** Circa 10‑15 minuti per una combinazione di base.  
- **È necessaria una licenza?** Una versione di prova gratuita è sufficiente per i test; per la produzione è richiesta una licenza commerciale.  
- **Posso aggiungere più di due immagini?** Sì – ripeti le chiamate a `drawImage` per ogni livello aggiuntivo.  
- **Quale versione di Java è supportata?** Java 8 e successive.

## Prerequisiti

Prima di iniziare, assicurati di avere quanto segue:

1. **Libreria Aspose.PSD** – scaricala da [qui](https://releases.aspose.com/psd/java/).  
2. **Java Development Kit (JDK)** – è consigliato Java 8+.  
3. **Cartella dei documenti** – una directory sul tuo computer dove saranno memorizzate le immagini di origine e il PSD risultante.

## Importa i pacchetti

Inizia importando le classi Aspose.PSD necessarie nel tuo progetto:

```java
import com.aspose.psd.Color;
import com.aspose.psd.Graphics;
import com.aspose.psd.Image;

import com.aspose.psd.imageoptions.PsdOptions;
import com.aspose.psd.sources.FileCreateSource;
```

## Guida passo‑passo

### Passo 1: Crea le opzioni PSD (prepara il file)

Creiamo prima un'istanza di `PsdOptions` che conterrà le impostazioni di output.

```java
PsdOptions imageOptions = new PsdOptions();
```

### Passo 2: Imposta il FileCreateSource (definisci dove verrà salvato il PSD)

Assegna un `FileCreateSource` alle opzioni, indicando il percorso del file di risultato desiderato.

```java
imageOptions.setSource(new FileCreateSource(dataDir + "Two_images_result_out.psd", false));
```

### Passo 3: Crea l'istanza Image (inizializza le dimensioni del canvas)

Crea un oggetto `Image` con le opzioni e specifica un canvas di 600 × 600 pixel.

```java
Image image = Image.create(imageOptions, 600, 600);
```

### Passo 4: Inizializza Graphics e disegna la prima immagine

Un oggetto `Graphics` ci permette di dipingere sul canvas. Puliamo lo sfondo con il bianco e disegniamo la prima immagine di origine nella metà sinistra.

```java
Graphics graphics = new Graphics(image);
graphics.clear(Color.getWhite());
graphics.drawImage(Image.load(dataDir + "example1.psd"), 0, 0, 300, 600);
```

### Passo 5: Disegna la seconda immagine (completa la combinazione)

Ora posizioniamo la seconda immagine nella metà destra dello stesso canvas.

```java
graphics.drawImage(Image.load(dataDir + "example2.psd"), 300, 0, 300, 600);
```

### Passo 6: Salva il file PSD risultante

Infine, persisti il canvas combinato su disco.

```java
image.save();
```

Congratulazioni! Hai **unito con successo le immagini in PSD** e creato un file PSD in Java.

## Perché combinare immagini con Aspose.PSD?

- **Consapevolezza dei livelli** – ogni chiamata a `drawImage` aggiunge un livello separato che può essere modificato in seguito.  
- **Flessibilità di formato** – supporta PSD, PNG, JPEG, BMP e molti altri.  
- **Nessuna dipendenza nativa** – Java puro, funziona su qualsiasi OS che esegue il JDK.  

## Problemi comuni e soluzioni

| Problema | Causa | Soluzione |
|----------|-------|-----------|
| Errore `File not found` durante il caricamento delle immagini di origine | Percorso `dataDir` errato | Verifica che `dataDir` punti alla cartella contenente `example1.psd` e `example2.psd`. |
| Il PSD di output è vuoto | `graphics.clear` chiamato dopo il disegno | Assicurati che `graphics.clear(Color.getWhite())` venga eseguito **prima** di qualsiasi chiamata a `drawImage`. |
| Eccezione di licenza a runtime | Licenza Aspose.PSD mancante o scaduta | Applica una licenza valida usando `License license = new License(); license.setLicense("Aspose.PSD.lic");` prima di qualsiasi chiamata API. |

## Domande frequenti

### Q1: Aspose.PSD è compatibile con tutti i formati immagine?
A1: Aspose.PSD si concentra principalmente sul formato PSD. Tuttavia, supporta vari altri formati per input e output.

### Q2: Posso eseguire modifiche aggiuntive sull'immagine combinata?
A2: Assolutamente! Dopo aver combinato le immagini, puoi manipolare ulteriormente il PSD risultante usando le numerose funzionalità di Aspose.PSD.

### Q3: Ci sono requisiti di licenza per l'uso di Aspose.PSD?
A3: Sì, è necessaria una licenza valida per l'uso commerciale. Ottienila da [qui](https://purchase.aspose.com/buy).

### Q4: È disponibile una versione di prova gratuita per Aspose.PSD?
A4: Sì, puoi provare Aspose.PSD con una versione di prova gratuita [qui](https://releases.aspose.com/).

### Q5: Dove posso trovare supporto per domande relative ad Aspose.PSD?
A5: Visita il [forum Aspose.PSD](https://forum.aspose.com/c/psd/34) per supporto della community e discussioni.

---

**Ultimo aggiornamento:** 2025-12-30  
**Testato con:** Aspose.PSD 24.11 per Java  
**Autore:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}