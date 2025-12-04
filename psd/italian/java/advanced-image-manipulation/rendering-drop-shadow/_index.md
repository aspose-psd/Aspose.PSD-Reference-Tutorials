---
date: 2025-12-04
description: Scopri come salvare un PSD come PNG e applicare un'ombra proiettata di
  rendering usando Aspose.PSD per Java. Questa guida spiega come aggiungere l'ombra,
  convertire un PSD in PNG e applicare l'ombra proiettata in Java.
language: it
linktitle: Apply Rendering Drop Shadow
second_title: Aspose.PSD Java API
title: Salva PSD come PNG e aggiungi ombra proiettata con Aspose.PSD Java
url: /java/advanced-image-manipulation/rendering-drop-shadow/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Salva PSD come PNG e aggiungi ombra esterna con Aspose.PSD Java

## Introduzione

Se lavori con file Photoshop in Java, **salvare PSD come PNG** aggiungendo un'ombra esterna dall'aspetto professionale è una necessità comune. Aspose.PSD rende questo compito semplice, consentendoti di **convertire PSD in PNG** e **applicare ombra esterna Java** in poche righe di codice. In questo tutorial vedremo l'intero processo, dal caricamento di un file PSD all'esportazione del PNG finale con l'effetto ombra renderizzato.

## Risposte rapide
- **Cosa significa “salvare PSD come PNG”?** Converte un file Photoshop a più livelli in un'immagine PNG piatta, preservando la trasparenza.  
- **Posso aggiungere un'ombra esterna durante la conversione?** Sì—Aspose.PSD ti permette di modificare gli effetti dei livelli prima dell'esportazione.  
- **È necessaria una licenza per eseguire il codice?** Una versione di prova gratuita è sufficiente per la valutazione; è richiesta una licenza per la produzione.  
- **Quale versione di Java è supportata?** Java 8 o superiore.  
- **L'effetto ombra esterna è personalizzabile?** Assolutamente—puoi regolare colore, opacità, distanza, dimensione, angolo e altro.

## Prerequisiti

Prima di iniziare, assicurati di avere:

- **Ambiente di sviluppo Java** – JDK 8 o più recente installato.  
- **Libreria Aspose.PSD** – Scarica l'ultimo JAR dal sito ufficiale [qui](https://releases.aspose.com/psd/java/).  
- **Un file PSD** – Un file che contenga almeno un livello a cui vuoi aggiungere un'ombra.  

## Come salvare PSD come PNG con un'ombra esterna in Java?

Di seguito trovi una guida passo‑passo. Ogni passaggio include una breve spiegazione seguita dal codice esatto da copiare.

### Passo 1: Importa i pacchetti richiesti

Iniziamo importando le classi che forniscono il caricamento dell'immagine, la gestione degli effetti e le capacità di esportazione PNG.

```java
import com.aspose.psd.Image;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.layereffects.DropShadowEffect;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
import com.aspose.psd.Color;

import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.imageoptions.PngOptions;
```

### Passo 2: Definisci la directory del documento

Imposta la cartella in cui risiederanno il tuo PSD di origine e il PNG risultante.

```java
String dataDir = "Your Document Directory";
```

### Passo 3: Imposta i percorsi dei file PSD e PNG

Specifica i percorsi completi per il PSD di input e il PNG di output.

```java
String sourceFileName = dataDir + "Shadow.psd";
String pngExportPath = dataDir + "Shadowchanged1.png";
```

### Passo 4: Carica il file PSD con gli effetti abilitati

Abilitare **loadEffectsResource** garantisce che gli effetti dei livelli (come le ombre) siano disponibili per la manipolazione.

```java
PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);

PsdImage im = (PsdImage) Image.load(sourceFileName, loadOptions);
```

### Passo 5: Accedi all'effetto Ombra Esterna

Qui recuperiamo il primo effetto applicato al secondo livello (indice 1). È qui che leggeremo o modificheremo i parametri dell'ombra.

```java
DropShadowEffect shadowEffect = (DropShadowEffect) (im.getLayers()[1].getBlendingOptions().getEffects()[0]);
```

### Passo 6: Convalida le proprietà dell'effetto ombra (Opzionale ma utile)

Verificare le proprietà esistenti ti aiuta a decidere se è necessario modificare qualcosa. Le asserzioni qui sotto confermano i valori predefiniti.

```java
Assert.areEqual(Color.getBlack(), shadowEffect.getColor());
Assert.areEqual(255, shadowEffect.getOpacity());
Assert.areEqual(3, shadowEffect.getDistance());
Assert.areEqual(7, shadowEffect.getSize());
Assert.areEqual(true, shadowEffect.getUseGlobalLight());
Assert.areEqual(90, shadowEffect.getAngle());
Assert.areEqual(0, shadowEffect.getSpread());
Assert.areEqual(0, shadowEffect.getNoise());
```

> **Consiglio:** Se vuoi **come aggiungere ombra** con impostazioni personalizzate, modifica le proprietà su `shadowEffect` prima di salvare (ad es., `shadowEffect.setColor(Color.getRed());`).

### Passo 7: Salva l'immagine modificata come PNG

Infine, esportiamo il PSD (con l'ombra renderizzata) in un file PNG. L'opzione `TruecolorWithAlpha` preserva la trasparenza.

```java
PngOptions saveOptions = new PngOptions();
saveOptions.setColorType(PngColorType.TruecolorWithAlpha);
im.save(pngExportPath, saveOptions);
```

Ecco fatto—un flusso di lavoro completo per **convertire PSD in PNG** che **applica ombra esterna java** in un'unica operazione.

## Perché usare Aspose.PSD per questo compito?

- **Nessun Photoshop nativo richiesto** – Funziona su qualsiasi piattaforma che supporti Java.  
- **Fidelità totale del PSD** – Tutte le informazioni dei livelli, le maschere e gli effetti sono preservati.  
- **Controllo granulare** – Regola ogni parametro dell'ombra esterna prima dell'esportazione.  
- **Alte prestazioni** – Ottimizzato per file di grandi dimensioni e elaborazione batch.

## Problemi comuni e risoluzione

| Sintomo | Probabile causa | Soluzione |
|---------|-----------------|-----------|
| `NullPointerException` su `shadowEffect` | Il livello target non ha effetti o l'indice è errato. | Verifica l'indice del livello (`im.getLayers()[i]`) e assicurati che esista un effetto. |
| PNG esportato è vuoto | Opzioni PNG non impostate correttamente o immagine non salvata. | Usa `PngColorType.TruecolorWithAlpha` e conferma che il percorso di `im.save()` sia scrivibile. |
| Il colore dell'ombra non è visibile | Opacità dell'ombra impostata a 0 o colore uguale allo sfondo. | Imposta `shadowEffect.setOpacity(255);` e scegli un colore contrastante. |

## Domande frequenti

**D: Posso applicare ombre esterne a più livelli contemporaneamente?**  
R: Sì. Scorri `im.getLayers()` e modifica il `DropShadowEffect` di ciascun livello secondo necessità.

**D: Cosa fa il parametro “Spread”?**  
R: Controlla quanto rapidamente l'ombra passa da completamente opaca a trasparente. Un valore più alto crea un bordo più netto.

**D: Aspose.PSD è compatibile con tutte le versioni di Photoshop?**  
R: Supporta un'ampia gamma di versioni PSD, dalle prime release fino agli ultimi file Photoshop CC.

**D: Come posso ottenere supporto se incontro problemi?**  
R: Visita il [forum Aspose.PSD](https://forum.aspose.com/c/psd/34) per il supporto della community e assistenza ufficiale.

**D: Posso provare Aspose.PSD prima di acquistarlo?**  
R: Assolutamente. Scarica una versione di prova gratuita dal [sito Aspose](https://releases.aspose.com/).

---

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

**Ultimo aggiornamento:** 2025-12-04  
**Testato con:** Aspose.PSD 24.12 per Java  
**Autore:** Aspose  

---