---
date: 2026-04-05
description: Scopri come esportare un PSD in PNG e migliorare senza sforzo il contrasto
  dell’immagine usando Aspose.PSD per Java. Padroneggia i livelli di regolazione con
  questa guida passo‑passo.
keywords:
- export psd to png
- how to adjust levels
- batch process psd files
linktitle: Esporta PSD in PNG e renderizza il livello di regolazione dei livelli in
  Java
second_title: Aspose.PSD Java API
title: Esporta PSD in PNG e renderizza il livello di regolazione in Java
url: /it/java/psd-layer-management-effects/render-level-adjustment-layer-psd/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Esporta PSD in PNG e Applica il Livello di Regolazione dei Livelli in Java

## Introduzione

Hai mai aperto un file PSD solo per accorgerti che i colori appaiono piatti o che il contrasto è sbagliato? Puoi rapidamente **esportare PSD in PNG** affinando l'immagine con un Livello di Regolazione dei Livelli usando Aspose.PSD per Java. In questo tutorial percorreremo l'intero processo—dal caricamento di un PSD, alla regolazione dei suoi livelli, fino al salvataggio del risultato come PNG—così potrai aumentare la vivacità e preparare risorse pronte per il web in pochi minuti.

## Risposte Rapide
- **Che cosa significa “export PSD to PNG”?** Converte un documento Photoshop in un'immagine PNG senza perdita di qualità preservando la trasparenza.  
- **Posso regolare i livelli prima dell'esportazione?** Sì, Aspose.PSD consente di modificare i livelli di ingresso e uscita programmaticamente.  
- **Ho bisogno di una licenza?** Una versione di prova gratuita funziona per lo sviluppo; è necessaria una licenza commerciale per la produzione.  
- **È possibile l'elaborazione batch?** Assolutamente—puoi inserire il codice in un ciclo per gestire più file PSD.  
- **Quale versione di Java è richiesta?** Si consiglia Java 8 o versioni successive.

## Che cos'è “export PSD to PNG”?
Esportare un PSD in PNG significa prendere il file Photoshop a livelli e appiattirlo in un'immagine Portable Network Graphics. PNG supporta compressione senza perdita e un canale alfa, rendendolo ideale per grafiche web e risorse UI.

## Perché regolare i livelli prima dell'esportazione?
Regolare i livelli ti permette di controllare ombre, mezzitoni e luci, migliorando il contrasto complessivo e l'equilibrio cromatico. Questo passaggio assicura che il PNG finale appaia rifinito senza la necessità di modifiche manuali in Photoshop.

## Prerequisiti

- **Java Development Kit (JDK)** – scarica l'ultima versione dal sito Oracle ([https://www.oracle.com/java/technologies/javase-downloads.html](https://www.oracle.com/java/technologies/javase-downloads.html)).  
- **Aspose.PSD for Java Library** – ottienila dalla pagina di download ufficiale ([https://releases.aspose.com/psd/java/](https://releases.aspose.com/psd/java/)). È disponibile una versione di prova gratuita ([https://releases.aspose.com/](https://releases.aspose.com/)).  

## Importa Pacchetti

Prima di immergerti nel codice, importa le classi che ci danno accesso alla manipolazione PSD e all'esportazione PNG:

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.adjustmentlayers.LevelsLayer;
import com.aspose.psd.fileformats.psd.layers.layerresources.LevelChannel;
import com.aspose.psd.imageoptions.PngOptions;
```

## Guida Passo‑Passo

### Passo 1: Definisci i Percorsi dei File (Come automatizzare l'elaborazione PSD)

Imposta variabili chiare e descrittive per il PSD di origine, il PSD modificato e la posizione di esportazione PNG finale.

```java
String dataDir = "Your Document Directory";

String sourceFileName = dataDir + "LevelsAdjustmentLayer.psd";
String psdPathAfterChange = dataDir + "LevelsAdjustmentLayerChanged.psd";
String pngExportPath = dataDir + "LevelsAdjustmentLayerChanged.png";
```

### Passo 2: Carica l'Immagine PSD

Usa `Image.load` per leggere il file PSD in un oggetto `PsdImage`. Aspose.PSD rileva automaticamente il formato.

```java
PsdImage im = (PsdImage)Image.load(sourceFileName);
```

### Passo 3: Itera tra i Livelli (Come regolare i livelli)

Scorri ogni livello per individuare il Livello di Regolazione dei Livelli.

```java
for (int i = 0; i < im.getLayers().length; i++) {
   // ... (code to check for Levels Layer will be added here)
}
```

### Passo 4: Identifica il Livello dei Livelli

Verifica ciascun livello con `instanceof LevelsLayer`. Quando lo trovi, esegui il cast per poter modificare le sue proprietà.

```java
for (int i = 0; i < im.getLayers().length; i++) {
   if (im.getLayers()[i] instanceof LevelsLayer) {
	   LevelsLayer levelsLayer = (LevelsLayer) im.getLayers()[i];
	   // ... (code to adjust levels will be added here)
   }
}
```

### Passo 5: Regola Finemente i Livelli (Come regolare i livelli)

Regola sia i livelli di ingresso che di uscita per il primo canale (di solito il canale composito). Questi valori sono esempi; sentiti libero di sperimentare.

```java
for (int i = 0; i < im.getLayers().length; i++) {
   if (im.getLayers()[i] instanceof LevelsLayer) {
	   LevelsLayer levelsLayer = (LevelsLayer) im.getLayers()[i];
	   LevelChannel channel = levelsLayer.getChannel(0);

	   // Adjust Input Levels (0‑255):
	   channel.setInputShadowLevel((short) 10); // Darken shadows slightly
	   channel.setInputMidtoneLevel(2.0f);     // Increase midtones
	   channel.setInputHighlightLevel((short) 230); // Reduce highlights

	   // Adjust Output Levels (0‑255):
	   channel.setOutputShadowLevel((short) 20); // Darken shadows further
	   channel.setOutputHighlightLevel((short) 200); // Brighten highlights
   }
}
```

### Passo 6: Salva il PSD Modificato (Come automatizzare PSD)

Persisti le modifiche in un nuovo file PSD.

```java
im.save(psdPathAfterChange);
```

### Passo 7: Esporta come PNG (Export PSD to PNG)

Se ti serve una versione PNG, configura `PngOptions` e salva l'immagine.

```java
PngOptions saveOptions = new PngOptions();
saveOptions.setColorType(PngColorType.TruecolorWithAlpha);
im.save(pngExportPath, saveOptions);
```

## Casi d'Uso Comuni

- **Preparazione di asset web:** Converti i mockup PSD forniti dal designer in PNG pronti per i browser.  
- **Elaborazione batch:** Automatizza la conversione di decine di file PSD in una pipeline CI.  
- **Generazione dinamica di immagini:** Regola i livelli al volo in base all'input dell'utente prima dell'esportazione.

## Risoluzione dei Problemi e Suggerimenti

- **Null pointer quando si accede ai livelli:** Assicurati che il PSD contenga effettivamente un Levels Adjustment Layer; altrimenti aggiungi un controllo null.  
- **Colori inattesi dopo l'esportazione:** Verifica che il tipo di colore PNG sia impostato su `TruecolorWithAlpha` per mantenere la trasparenza.  
- **Prestazioni con molti file:** Riutilizza la stessa istanza `PsdImage` durante l'elaborazione batch per ridurre il consumo di memoria.

## Domande Frequenti

**Q: Posso regolare singolarmente i canali colore (RGB) separatamente?**  
A: Sì. Usa `levelsLayer.getChannel(index)` dove `index` = 0 (Rosso), 1 (Verde), 2 (Blu) per modificare ogni canale in modo indipendente.

**Q: Come gestisco più Livelli di Regolazione dei Livelli in un unico PSD?**  
A: Il ciclo elabora ogni livello; ciascun `LevelsLayer` trovato verrà regolato secondo il codice all'interno del blocco `if`.

**Q: Esistono altri modi per migliorare il contrasto oltre ai Livelli?**  
A: Aspose.PSD offre anche regolazioni Curves, Brightness/Contrast e Histogram Equalization.

**Q: Posso automatizzare questo per una cartella di file PSD?**  
A: Avvolgi l'intero flusso di lavoro in un ciclo `File[] files = new File(dataDir).listFiles((d, name) -> name.endsWith(".psd"));` e processa ogni file in sequenza.

**Q: Dove posso trovare ulteriore documentazione e supporto?**  
A: Visita il riferimento ufficiale ([https://reference.aspose.com/psd/java/](https://reference.aspose.com/psd/java/)) e il forum della community ([https://forum.aspose.com/c/psd/34](https://forum.aspose.com/c/psd/34)).

## Conclusione

Padroneggiando il flusso di lavoro **export PSD to PNG** e imparando **come regolare i livelli** programmaticamente, ottieni il pieno controllo sulla qualità dell'immagine senza uscire dall'ambiente Java. Che tu stia preparando risorse per il web, automatizzando una pipeline di design o costruendo un processore batch, Aspose.PSD per Java rende il lavoro semplice e affidabile.

---

**Last Updated:** 2026-04-05  
**Tested With:** Aspose.PSD 24.11 for Java  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}