---
date: 2025-12-08
description: Scopri come convertire PSD in PNG e ridimensionare le immagini proporzionalmente
  in Java usando Aspose.PSD. Questo tutorial passo‑passo copre la memorizzazione nella
  cache delle immagini, il ridimensionamento e il salvataggio in PNG.
linktitle: Convert PSD to PNG & Resize Proportionally
second_title: Aspose.PSD Java API
title: Come convertire PSD in PNG e ridimensionare proporzionalmente con Aspose.PSD
  per Java
url: /it/java/advanced-image-manipulation/resize-image-proportionally/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Come convertire PSD in PNG e ridimensionare proporzionalmente con Aspose.PSD per Java

## Introduzione

Se hai bisogno di **convertire PSD in PNG** mantenendo il rapporto d'aspetto originale, sei nel posto giusto. In questo tutorial percorreremo un **tutorial completo di Aspose.PSD** che mostra **come ridimensionare l'immagine** in modo proporzionale in Java, mettere in cache l'immagine per prestazioni ottimali e, infine, salvare il risultato come PNG. Alla fine sarai in grado di integrare questo flusso di lavoro in qualsiasi pipeline di elaborazione immagini basata su Java.

## Risposte rapide
- **Aspose.PSD può convertire PSD in PNG?** Sì – basta caricare il PSD e salvarlo con `PngOptions`.
- **La libreria supporta il ridimensionamento proporzionale?** Assolutamente; usa `resizeWidthProportionally` e `resizeHeightProportionally`.
- **Devo prima mettere in cache l'immagine?** La cache (`image.cacheData()`) migliora le prestazioni per file PSD di grandi dimensioni.
- **Quale versione di Java è richiesta?** Java 8 o versioni successive sono pienamente supportate.
- **È necessaria una licenza per la produzione?** Sì, una licenza commerciale rimuove le filigrane di valutazione.

## Cos'è “convertire PSD in PNG” e perché è importante?

Convertire un documento Photoshop (PSD) in un file portable network graphics (PNG) ti consente di condividere design a livelli in un formato leggero e adatto al web. PNG mantiene la trasparenza e la qualità lossless, rendendolo ideale per risorse UI, miniature o qualsiasi scenario in cui la fedeltà dell'immagine è fondamentale.

## Perché ridimensionare l'immagine proporzionalmente in Java?

Ridimensionare **come ridimensionare l'immagine** senza distorcere il rapporto d'aspetto garantisce che la grafica appaia naturale su schermi diversi. L'API `Aspose.PSD` fornisce metodi dedicati per il ridimensionamento proporzionale, che calcolano automaticamente l'altezza o la larghezza corrispondente, evitando errori di calcolo manuale.

## Prerequisiti

Prima di immergerci nel codice, assicurati di avere:

1. **Java Development Kit (JDK)** – Java 8 o successiva installata.
2. **Aspose.PSD per Java** – scarica l'ultimo JAR dal sito ufficiale [qui](https://releases.aspose.com/psd/java/).
3. Un file PSD di esempio (`sample.psd`) posizionato in una directory a cui puoi fare riferimento dal tuo progetto.

## Importare i pacchetti

Aggiungi gli import necessari alla tua classe Java. Queste classi ti danno accesso al caricamento dell'immagine, alla cache, al ridimensionamento e alle opzioni di output PNG.

```java
import com.aspose.psd.Image;
import com.aspose.psd.imageoptions.PngOptions;
```

## Passo 1: Caricare l'immagine PSD

Per prima cosa, carica il file PSD di origine. Se il file è grande, mettere in cache i dati dell'immagine riduce il consumo di memoria quando esegui operazioni successive.

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

Image image = Image.load(sourceFile);

if (!image.isCached()) {
    // Image caching java – improves performance for large files
    image.cacheData();
}
```

## Passo 2: Ridimensionare l'immagine proporzionalmente (Java)

Ora decidi le nuove dimensioni. In questo esempio riduciamo l'immagine alla **metà** della sua dimensione originale mantenendo il rapporto d'aspetto. Puoi regolare la larghezza o l'altezza target secondo le tue necessità.

```java
int newWidth = image.getWidth() / 2;
image.resizeWidthProportionally(newWidth);

int newHeight = image.getHeight() / 2;
image.resizeHeightProportionally(newHeight);
```

> **Consiglio professionale:** Usa `resizeWidthProportionally` *oppure* `resizeHeightProportionally` — la libreria calcola automaticamente l'altra dimensione per mantenere l'immagine proporzionale.

## Passo 3: Salvare l'immagine ridimensionata come PNG

Infine, esporta l'immagine ridimensionata in formato PNG. Questo passaggio completa il flusso di lavoro **convertire PSD in PNG**.

```java
String destName = dataDir + "SimpleResizeImageProportionally_out.png";
image.save(destName, new PngOptions());
```

Quando il codice verrà eseguito, troverai un file PNG che è metà della dimensione del PSD originale, con la stessa qualità visiva e senza distorsioni.

## Problemi comuni e soluzioni

| Problema | Causa | Soluzione |
|----------|-------|-----------|
| **OutOfMemoryError** | PSD di grandi dimensioni non memorizzato nella cache | Chiama `image.cacheData()` prima del ridimensionamento |
| **Blank PNG output** | Percorso file errato | Verifica `dataDir` e i permessi di scrittura |
| **Aspect ratio looks off** | Uso manuale di larghezza e altezza | Usa i metodi proporzionali forniti da Aspose.PSD |

## Domande frequenti

**Q: Aspose.PSD è compatibile con tutti i formati immagine?**  
A: Aspose.PSD supporta PSD, PNG, JPEG, BMP, GIF e molti altri. Vedi l'elenco completo nella [documentazione](https://reference.aspose.com/psd/java/).

**Q: Posso usare Aspose.PSD per progetti commerciali?**  
A: Sì. Acquista una licenza commerciale nello [store Aspose](https://purchase.aspose.com/buy).

**Q: Sono disponibili licenze temporanee per i test?**  
A: Assolutamente – richiedi una licenza temporanea [qui](https://purchase.aspose.com/temporary-license/) per scopi di valutazione.

**Q: Dove posso trovare supporto della community?**  
A: Il [forum Aspose.PSD](https://forum.aspose.com/c/psd/34) è un ottimo posto per porre domande e condividere soluzioni.

**Q: Come accedo alla documentazione completa dell'API?**  
A: Documentazione dettagliata dell'API è disponibile [qui](https://reference.aspose.com/psd/java/).

## Conclusione

Ora sai **come convertire PSD in PNG**, ridimensionare l'immagine proporzionalmente e gestire la cache in modo efficiente usando Aspose.PSD per Java. Integra questi passaggi nelle tue applicazioni per offrire un'elaborazione immagini veloce e di alta qualità senza dipendere da installazioni native di Photoshop.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Ultimo aggiornamento:** 2025-12-08  
**Testato con:** Aspose.PSD 24.12 for Java  
**Autore:** Aspose