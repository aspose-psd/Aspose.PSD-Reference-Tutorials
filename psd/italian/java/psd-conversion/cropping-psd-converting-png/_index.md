---
date: 2026-03-21
description: Scopri come convertire PSD in PNG e ritagliare file PSD usando Aspose.PSD
  per Java. Questa guida mostra l'elaborazione delle immagini passo‑passo nelle applicazioni
  Java.
linktitle: Cropping PSD when Converting to PNG
second_title: Aspose.PSD Java API
title: Come convertire PSD in PNG con ritaglio usando Aspose.PSD per Java
url: /it/java/psd-conversion/cropping-psd-converting-png/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Come convertire psd in png con ritaglio usando Aspose.PSD per Java

## Introduzione
Nel dinamico mondo dello sviluppo Java, padroneggiare un'elaborazione efficiente delle immagini è fondamentale. In questo tutorial imparerai **come convertire psd in png** e ritagliare l'immagine in un unico flusso di lavoro usando la potente libreria Aspose.PSD per Java. Alla fine di questa guida passo‑a‑passo, sarai in grado di aggiungere un ritaglio preciso alle tue esportazioni PNG e far gestire alle tue applicazioni Java gli asset PSD con sicurezza.

## Risposte rapide
- **Cosa fa il codice?** Carica un PSD, ritaglia un rettangolo e lo salva come PNG.  
- **Quale libreria è necessaria?** Aspose.PSD per Java (ultima versione).  
- **È necessaria una licenza?** Sì, è richiesta una licenza commerciale per l'uso in produzione.  
- **Posso definire qualsiasi regione di ritaglio?** Assolutamente – imposti i valori X, Y, larghezza e altezza di cui hai bisogno.  
- **Questo approccio è veloce per file di grandi dimensioni?** Sì, Aspose.PSD è ottimizzato per un'elaborazione ad alte prestazioni.

## Cos'è la conversione da psd a png?
Convertire PSD in PNG significa prendere un documento Photoshop a più livelli e appiattirlo in un'immagine PNG senza perdita. Questo formato è ideale per la consegna sul web, le miniature o qualsiasi scenario in cui ti serve un'immagine raster senza i livelli originali.

## Perché ritagliare il PSD prima di convertirlo in PNG?
Il ritaglio ti consente di estrarre solo la parte del design di cui hai bisogno, riducendo le dimensioni del file e focalizzandoti sul contenuto visivo rilevante. È particolarmente utile per generare miniature, asset UI o preparare immagini per layout responsivi.

## Prerequisiti
Prima di immergerti nel tutorial, assicurati di avere i seguenti prerequisiti:
- Conoscenza di base della programmazione Java.  
- Java Development Kit (JDK) installato sul tuo sistema.  
- Libreria Aspose.PSD per Java scaricata e aggiunta al tuo progetto.  
- Un file PSD di esempio per sperimentare.

## Importare i pacchetti
Nel tuo progetto Java, assicurati di importare i pacchetti necessari per utilizzare le funzionalità di Aspose.PSD:
```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;
import com.aspose.psd.Rectangle;
import com.aspose.psd.imageoptions.PngOptions;
```

## Passo 1: Configura il tuo progetto
Inizia creando un progetto Java e aggiungendo la libreria Aspose.PSD per Java al classpath del progetto. Questo ti darà accesso a tutte le classi di elaborazione delle immagini di cui avrai bisogno.

## Passo 2: Carica l'immagine PSD
```java
String dataDir = "Your Document Directory";
String srcPath = dataDir + "sample.psd";
// Load an existing PSD image
RasterImage image = (RasterImage)Image.load(srcPath);
```
*Qui carichiamo il file PSD di origine in un oggetto `RasterImage`, che fornisce operazioni basate su raster come il ritaglio.*

## Passo 3: Definisci la regione di ritaglio
```java
// Create an instance of Rectangle class by passing x, y, width, and height
Rectangle cropRegion = new Rectangle(0, 0, 350, 450);
```
*Il `Rectangle` definisce l'area che vuoi conservare. Regola i valori `x`, `y`, `width` e `height` in base al tuo design. Questo passo risponde direttamente alla keyword “definisci regione di ritaglio”.*

## Passo 4: Ritaglia l'immagine PSD
```java
// Call the crop method of Image class and pass the Rectangle instance
image.crop(cropRegion);
```
*Chiamare `crop` modifica l'immagine in memoria, scartando tutto ciò che si trova al di fuori del rettangolo specificato.*

## Passo 5: Imposta le opzioni di esportazione PNG
```java
// Create an instance of PngOptions class
PngOptions pngOptions = new PngOptions();
```
*`PngOptions` ti consente di controllare le impostazioni specifiche del PNG, come il livello di compressione, il tipo di colore e altro.*

## Passo 6: Salva l'immagine ritagliata come PNG
```java
// Provide output path and PngOptions to convert the PSD file to PNG and save the output
String destName = dataDir + "export.png";
image.save(destName, pngOptions);
```
*Il metodo `save` esegue l'operazione di **convertire psd in png** mantenendo il ritaglio che hai definito.*

## Problemi comuni e consigli
- **Dimensioni del rettangolo errate:** Assicurati che larghezza e altezza non superino le dimensioni dell'immagine originale, altrimenti verrà generata un'eccezione.  
- **Utilizzo della memoria con PSD di grandi dimensioni:** Disporre dell'oggetto `RasterImage` (`image.dispose()`) dopo il salvataggio per liberare le risorse native.  
- **Licenza non impostata:** Se esegui il codice senza una licenza valida, comparirà una filigrana sull'output PNG.

## Domande frequenti
### Posso ritagliare file PSD con forme irregolari usando Aspose.PSD per Java?
Sì, Aspose.PSD per Java ti permette di definire una regione di ritaglio personalizzata, consentendoti di ritagliare le immagini in varie forme.

### Aspose.PSD per Java è adatto a compiti di elaborazione immagini su larga scala?
Assolutamente! Aspose.PSD è progettato per gestire immagini di grandi dimensioni in modo efficiente, rendendolo ideale per progetti con requisiti estesi di elaborazione delle immagini.

### È necessaria una licenza per Aspose.PSD per Java?
Sì, è richiesta una licenza valida per l'uso commerciale. Puoi ottenerla da [Aspose Purchase](https://purchase.aspose.com/buy).

### Come posso chiedere aiuto o segnalare problemi con Aspose.PSD per Java?
Visita il [forum Aspose.PSD](https://forum.aspose.com/c/psd/34) per chiedere assistenza, condividere le tue esperienze e segnalare eventuali problemi.

### Posso provare Aspose.PSD per Java prima di acquistarlo?
Certamente! Esplora le funzionalità della libreria con una prova gratuita disponibile [qui](https://releases.aspose.com/).

---

**Ultimo aggiornamento:** 2026-03-21  
**Testato con:** Aspose.PSD per Java 24.12 (ultima al momento della stesura)  
**Autore:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}