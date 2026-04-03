---
date: 2026-04-03
description: Scopri come ridurre le dimensioni dei file PSD appiattendo i livelli
  con Aspose.PSD per Java. Questa guida passo passo mostra come appiattire rapidamente
  i file PSD.
keywords:
- reduce psd file size
- how to flatten psd
- flatten visible layers psd
linktitle: Riduci la dimensione del file PSD appiattendo i livelli – Aspose.PSD Java
second_title: Aspose.PSD Java API
title: Riduci le dimensioni del file PSD appiattendo i livelli – Aspose.PSD Java
url: /it/java/psd-layer-management-effects/flatten-layers-psd-files/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Ridurre le dimensioni del file PSD appiattendo i livelli – Aspose.PSD Java

## Introduzione

Se hai mai aperto un documento Photoshop e ti sei chiesto come **reduce PSD file size**, l'appiattimento dei livelli è uno dei trucchi più efficaci. Con Aspose.PSD per Java puoi appiattire programmaticamente un intero PSD o unire solo i livelli che scegli, ottenendo un controllo fine sul peso del file senza sacrificare la qualità visiva. In questo tutorial vedremo entrambi gli approcci—appiattire l'intera immagine e unire livelli specifici—così potrai ridurre rapidamente i tuoi file PSD e mantenere fluido il tuo flusso di lavoro.

## Risposte rapide
- **Cosa fa l'appiattimento?** Unisce i livelli visibili in un unico livello di sfondo, rimuovendo le informazioni dei livelli e spesso riducendo le dimensioni del file.  
- **Posso appiattire solo i livelli selezionati?** Sì, puoi unire livelli specifici lasciando gli altri intatti.  
- **Ho bisogno di una licenza?** Una versione di prova gratuita funziona per lo sviluppo; è necessaria una licenza commerciale per la produzione.  
- **Quale versione di Java è richiesta?** JDK 8 o superiore.  
- **L'appiattimento influisce sulla qualità dell'immagine?** No, l'aspetto visivo rimane lo stesso; cambia solo la struttura dei livelli.

## Cos'è “reduce PSD file size”?

Ridurre le dimensioni del file PSD significa rimuovere dati non necessari—come livelli extra, canali nascosti o metadati eccessivi—così il file diventa più leggero e più veloce da caricare, condividere o elaborare. L'appiattimento dei livelli è una tecnica comune perché elimina gli oggetti dei singoli livelli preservando l'immagine composita finale.

## Perché appiattire i livelli con Aspose.PSD per Java?

- **Automazione:** Nessuna necessità di aprire Photoshop manualmente; integra direttamente nelle tue applicazioni Java.  
- **Precisione:** Scegli di appiattire l'intero documento o solo i livelli visibili (`flattenImage`) o di unire i livelli selezionati (`mergeLayers`).  
- **Prestazioni:** File più piccoli si caricano più rapidamente e consumano meno memoria nei processi successivi.  
- **Cross‑platform:** Funziona su qualsiasi OS che supporta Java.

## Prerequisiti

1. **Java Development Kit (JDK):** JDK 8 o più recente installato.  
2. **Aspose.PSD for Java:** Scarica la libreria da [qui](https://releases.aspose.com/psd/java/).  
3. **IDE:** IntelliJ IDEA, Eclipse o qualsiasi IDE compatibile con Java.  
4. **Conoscenze di base di Java:** Utili ma non obbligatorie per seguire i passaggi.  
5. **Sample PSD:** Un file con più livelli (useremo `ThreeRegularLayersSemiTransparent.psd`).

Ora che abbiamo tutto pronto, immergiamoci nel codice.

## Importa i pacchetti

Per iniziare, importa le classi essenziali di Aspose.PSD:

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.Layer;
```

Queste importazioni ci permettono di caricare file PSD, lavorare con i loro livelli e salvare i risultati.

## Passo 1: Appiattire l'intera immagine PSD

Appiattire l'intera immagine è il modo più rapido per **reduce PSD file size** perché rimuove tutti i dati dei singoli livelli.

### 1.1 Carica il file PSD

```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "ThreeRegularLayersSemiTransparent.psd";
PsdImage im = (PsdImage) Image.load(sourceFileName);
```

### 1.2 Appiattire l'immagine

```java
im.flattenImage();
```

### 1.3 Salva l'immagine appiattita

```java
String exportPath = dataDir + "ThreeRegularLayersSemiTransparentFlattened.psd";
im.save(exportPath);
```

Il tuo nuovo file ora contiene un unico livello di sfondo, il che di solito porta a una dimensione PSD più piccola.

## Passo 2: Unire livelli specifici (Come appiattire PSD selettivamente)

A volte vuoi solo **flatten visible layers** o combinare un sottoinsieme di livelli mantenendo gli altri modificabili.

### 2.1 Carica nuovamente il file PSD

```java
PsdImage img = (PsdImage) Image.load(sourceFileName);
```

### 2.2 Identifica e seleziona i livelli

```java
Layer bottomLayer = img.getLayers()[0];
Layer middleLayer = img.getLayers()[1];
Layer topLayer = img.getLayers()[2];
```

### 2.3 Unisci i livelli

```java
Layer layer1 = img.mergeLayers(bottomLayer, middleLayer);
Layer layer2 = img.mergeLayers(layer1, topLayer);
```

### 2.4 Sostituisci i livelli esistenti con il livello unito

```java
img.setLayers(new Layer[]{layer2});
```

### 2.5 Salva il file PSD aggiornato

```java
exportPath = dataDir + "ThreeRegularLayersSemiTransparentFlattenedLayerByLayer.psd";
img.save(exportPath);
```

Ora il PSD contiene solo il livello unito, ottenendo una dimensione ridotta del file mantenendo i livelli che volevi conservare.

## Problemi comuni e suggerimenti

- **Backup prima dell'appiattimento:** Una volta che i livelli sono appiattiti, l'operazione non può essere annullata. Conserva una copia del PSD originale.  
- **La visibilità è importante:** `flattenImage()` unisce solo i livelli *visibili*. Nascondi i livelli che non vuoi includere.  
- **Uso della memoria:** PSD di grandi dimensioni possono consumare molta RAM; considera di elaborarli su una macchina con sufficiente memoria.  
- **Modalità di fusione:** L'unione rispetta la modalità di fusione di ciascun livello, quindi il risultato visivo corrisponde a quello che vedresti in Photoshop.

## Domande frequenti

**Q: Posso annullare l'appiattimento dei livelli in Aspose.PSD?**  
A: No, l'appiattimento è irreversibile. Conserva sempre un backup del file originale.

**Q: È possibile appiattire solo i livelli visibili?**  
A: Sì. `flattenImage()` rispetta la visibilità dei livelli, quindi nascondi i livelli che non vuoi appiattire prima di chiamare il metodo.

**Q: L'appiattimento dei livelli riduce le dimensioni del file?**  
A: Generalmente sì. Rimuovere i dati dei livelli e i metadati porta spesso a un PSD più piccolo, anche se la riduzione esatta dipende dal contenuto.

**Q: Posso unire livelli con modalità di fusione diverse?**  
A: Assolutamente. Aspose.PSD unisce i livelli preservando l'aspetto visivo creato dalle loro modalità di fusione.

**Q: Cosa succede se provo a unire livelli non adiacenti?**  
A: Aspose.PSD consente di unire qualsiasi livello indipendentemente dall'ordine nello stack; il risultato riflette l'aspetto combinato.

---

**Ultimo aggiornamento:** 2026-04-03  
**Testato con:** Aspose.PSD 24.11 for Java  
**Autore:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}
{{< blocks/products/products-backtop-button >}}