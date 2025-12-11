---
date: 2025-12-10
description: Scopri come estrarre i livelli PSD e convertire i livelli PSD in PNG
  usando Aspose.PSD per Java. Ideale per gli sviluppatori che necessitano di una manipolazione
  grafica robusta.
linktitle: Extract PSD Layers and Add Layer Support for PSD Files using Aspose.PSD
  Java
second_title: Aspose.PSD Java API
title: Estrai i livelli PSD e aggiungi il supporto ai livelli per i file PSD con Aspose.PSD
  Java
url: /it/java/advanced-psd-layer-features-effects/add-layer-support-psd-files/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Estrai i livelli PSD e aggiungi il supporto ai livelli per file PSD usando Aspose.PSD Java

## Introduzione
Lavorare con i file Photoshop Document (PSD) è una realtà quotidiana per grafici e sviluppatori. Uno dei compiti più comuni è **estrarre i livelli PSD** in modo da poterli modificare, riutilizzare o convertire in altri formati come PNG. Nelle applicazioni Java, Aspose.PSD rende questo processo semplice e adatto al codice. In questo tutorial vedremo passo passo le operazioni necessarie per estrarre i livelli PSD, abilitare il supporto ai livelli e **convertire i livelli PSD in PNG** — tutto con spiegazioni chiare e consigli pratici.

## Risposte rapide
- **Cosa significa “estrarre i livelli PSD”?** Significa caricare un file PSD e accedere a ciascun livello individuale per manipolarlo o esportarlo.  
- **Quale libreria gestisce questo in Java?** Aspose.PSD per Java fornisce un'elaborazione PSD completa senza la necessità di Photoshop.  
- **Posso convertire i livelli PSD in PNG in un unico passaggio?** Sì — caricando il file con le opzioni corrette e salvandolo con le impostazioni PNG che preservano la trasparenza.  
- **È necessaria una licenza per l'uso in produzione?** È richiesta una licenza commerciale per la produzione; è disponibile una versione di prova gratuita per la valutazione.  
- **Quale versione di Java è richiesta?** JDK 8 o superiore (il tutorial utilizza JDK 11 come esempio).

## Cos'è “estrarre i livelli PSD”?
Estrarre i livelli PSD consiste nel leggere la struttura interna di un file PSD e recuperare ogni livello come oggetto immagine indipendente. Questo consente di modificare, nascondere, riordinare o esportare i livelli singolarmente — esattamente ciò che i designer fanno in Photoshop, ma in modo programmatico.

## Perché estrarre i livelli PSD e convertirli in PNG?
- **Riutilizzo delle risorse:** Estrai icone, pulsanti o elementi UI da un PSD master senza esportazioni manuali.  
- **Automazione:** Genera miniature o immagini pronte per il web al volo.  
- **Preservare la trasparenza:** PNG mantiene i canali alfa, rendendolo perfetto per la grafica web.  

## Prerequisiti
Prima di iniziare, assicurati di avere quanto segue:

1. **Ambiente di sviluppo Java** – JDK installato. Puoi scaricarlo dal [sito Oracle](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).  
2. **Aspose.PSD per Java** – Scarica l'ultima libreria dalla pagina ufficiale di download [qui](https://releases.aspose.com/psd/java/).  
3. **Conoscenze di base di Java** – Familiarità con la compilazione e l'esecuzione di programmi Java.  
4. **IDE** – IntelliJ IDEA, Eclipse o qualsiasi editor tu preferisca.  
5. **Un file PSD** – Usa qualsiasi PSD a tua disposizione, oppure scarica un PSD di esempio per i test.

Una volta pronti questi elementi, sei pronto per iniziare a estrarre i livelli PSD.

## Importa i pacchetti
Per prima cosa, importa le classi necessarie dalla libreria Aspose.PSD.

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
import com.aspose.psd.imageoptions.PngOptions;
```

## Passo 1: Definisci le tue directory
Imposta i percorsi per il PSD di origine e per il PNG di output. Regola `dataDir` in modo che punti alla cartella dove risiedono i tuoi file.

```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "layers.psd";
String output = dataDir + "layers.png";
```

- `dataDir` – Sostituisci `"Your Document Directory"` con il percorso effettivo della tua cartella.  
- `sourceFileName` – Percorso completo del PSD da elaborare.  
- `output` – Percorso di destinazione per il PNG che conterrà i livelli estratti.

## Passo 2: Configura le opzioni di caricamento
Configurare `PsdLoadOptions` garantisce che tutti gli effetti e le risorse dei livelli vengano caricati correttamente, cosa fondamentale quando **estrai i livelli PSD**.

```java
PsdLoadOptions imageLoadOptions = new PsdLoadOptions();
imageLoadOptions.setLoadEffectsResource(true);
imageLoadOptions.setUseDiskForLoadEffectsResource(true);
```

- `setLoadEffectsResource(true)` – Carica effetti aggiuntivi (come le ombre) associati ai livelli.  
- `setUseDiskForLoadEffectsResource(true)` – Sposta le risorse pesanti su disco, riducendo il carico di memoria.

## Passo 3: Carica il file PSD
Ora carichiamo il PSD in un oggetto `PsdImage` usando le opzioni definite sopra.

```java
PsdImage image = (PsdImage) Image.load(sourceFileName, imageLoadOptions);
```

A questo punto, `image` contiene tutti i livelli, le maschere e gli effetti, pronto per l'estrazione.

## Passo 4: Configura le opzioni di salvataggio
Imposta come verrà salvato il PNG. L'uso di `TruecolorWithAlpha` preserva la trasparenza dei livelli originali.

```java
PngOptions saveOptions = new PngOptions();
saveOptions.setColorType(PngColorType.TruecolorWithAlpha);
```

## Passo 5: Salva l'immagine (Converti i livelli PSD in PNG)
Esporta il PSD caricato (con tutti i suoi livelli) in un unico file PNG. Questo passaggio **converte i livelli PSD in PNG** in un'unica operazione.

```java
image.save(output, saveOptions);
```

Se ti serve ogni livello come PNG separato, puoi iterare su `image.getLayers()` — ma per molti casi d'uso un PNG unificato è sufficiente.

## Passo 6: Concludi
Aggiungi un messaggio di console amichevole così saprai che il processo è terminato con successo.

```java
System.out.println("PSD Layers have been successfully converted to PNG!");
```

## Problemi comuni e consigli
- **Errori Out‑of‑Memory:** Se elabori PSD molto grandi, mantieni abilitato `setUseDiskForLoadEffectsResource(true)` per spostare i dati temporanei su disco.  
- **Effetti mancanti:** Assicurati che `setLoadEffectsResource(true)` sia impostato; altrimenti alcuni effetti dei livelli potrebbero essere ignorati.  
- **Problemi di percorso:** Usa `Paths.get(...)` da `java.nio.file` per gestire i percorsi in modo indipendente dalla piattaforma.

## Domande frequenti

**D: Cos'è Aspose.PSD per Java?**  
R: Aspose.PSD per Java è una libreria che consente di manipolare file PSD senza avere Photoshop installato.

**D: Posso usare Aspose.PSD per altri formati di file?**  
R: Sì! Sebbene sia principalmente per file PSD, Aspose offre librerie per vari altri formati.

**D: È disponibile una versione di prova?**  
R: Assolutamente! Puoi scaricare una versione di prova gratuita [qui](https://releases.aspose.com/).

**D: Dove posso ottenere supporto se ho bisogno di aiuto?**  
R: Puoi accedere al supporto nel forum Aspose [qui](https://forum.aspose.com/c/psd/34).

**D: Posso convertire da PNG a PSD?**  
R: La libreria Aspose.PSD è più focalizzata sulla lettura e manipolazione di file PSD piuttosto che sulla conversione di altri formati in PSD.

**D: Come estraggo ogni livello come PNG separato?**  
R: Itera su `image.getLayers()`, crea un nuovo `Bitmap` per ciascun livello e salvalo con le proprie `PngOptions`. Otterrai file PNG individuali per ogni livello.

## Conclusione
Ora sai come **estrarre i livelli PSD**, abilitare il supporto completo ai livelli e **convertire i livelli PSD in PNG** usando Aspose.PSD per Java. Che tu stia costruendo una pipeline automatizzata di asset o aggiungendo capacità grafiche a un'app desktop, questo approccio ti offre un controllo dettagliato sui file Photoshop senza la necessità di Photoshop stesso. Sentiti libero di approfondire — ad esempio applicando filtri, unendo livelli programmaticamente o esportando ogni livello singolarmente.

---

**Ultimo aggiornamento:** 2025-12-10  
**Testato con:** Aspose.PSD per Java 24.11 (ultima versione al momento della stesura)  
**Autore:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}