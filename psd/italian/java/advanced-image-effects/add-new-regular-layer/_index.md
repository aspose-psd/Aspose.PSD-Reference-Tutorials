---
date: 2026-04-08
description: Scopri come esportare un PSD in PNG e creare un nuovo livello PSD con
  Aspose.PSD per Java utilizzando una licenza temporanea di Aspose. Questo tutorial
  passo‑passo copre la manipolazione delle immagini PSD e l’impostazione della posizione
  del livello.
keywords:
- aspose temporary license
- set layer position
- psd image manipulation
- create new psd layer
linktitle: Aggiungi un nuovo livello normale a PSD
second_title: Aspose.PSD Java API
title: Esporta PSD in PNG e aggiungi un nuovo livello normale con Aspose.PSD per Java
  – licenza temporanea Aspose
url: /it/java/advanced-image-effects/add-new-regular-layer/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Esporta PSD in PNG e aggiungi un nuovo livello regolare usando Aspose.PSD per Java

## Introduzione

In questo **aspose psd tutorial** scoprirai come **esportare PSD in PNG** creando anche **un nuovo livello regolare** nello stesso file, **usando una licenza temporanea di aspose** per lo sviluppo. Che tu debba generare miniature pronte per il web, preparare risorse per una pipeline di design, o semplicemente sperimentare con la **manipolazione di immagini psd**, Aspose.PSD per Java ti offre il pieno controllo programmatico. Ti guideremo passo passo—dal caricamento del file sorgente al salvataggio sia del PSD aggiornato che di una copia PNG—così potrai iniziare a manipolare i livelli PSD subito.

## Risposte rapide
- **Posso esportare PSD in PNG con una sola chiamata?** Sì, dopo aver aggiunto i livelli puoi chiamare `save` con `PngOptions`.
- **È necessaria una licenza per lo sviluppo?** Una licenza temporanea funziona per i test; è richiesta una licenza completa per la produzione.
- **Quale versione di Java è supportata?** Aspose.PSD funziona con Java 8 e versioni successive.
- **Il posizionamento dei livelli è basato sui pixel?** Sì, imposti le coordinate left, top, right, bottom in pixel usando i metodi **set layer position**.
- **Il PNG manterrà la trasparenza del livello?** Il PNG conterrà il risultato unito di tutti i livelli visibili.

## Perché usare una licenza temporanea di Aspose?

Una **licenza temporanea di aspose** ti consente di valutare l'intero set di funzionalità di Aspose.PSD senza restrizioni funzionali. Rimuove la filigrana di valutazione, sblocca tutte le API—including la possibilità di **creare nuovi oggetti livello psd**—e ti permette di testare il tuo codice in un ambiente simile alla produzione prima di acquistare una licenza permanente.

## Prerequisiti

Prima di iniziare, assicurati di avere:

- **Ambiente di sviluppo Java** – JDK 8+ e uno strumento di build (Maven/Gradle) installati.
- **Aspose.PSD per Java** – Scarica l'ultimo JAR dal sito ufficiale [qui](https://releases.aspose.com/psd/java/).
- **Un file PSD di esempio** – Useremo `OneLayer.psd` negli esempi.

## Importa pacchetti

Aggiungi le importazioni necessarie alla tua classe Java. Queste classi forniscono la funzionalità di base per la **manipolazione di immagini psd** e la gestione dei livelli.

```java
import com.aspose.psd.Image;
import com.aspose.psd.Rectangle;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.Layer;
import com.aspose.psd.imageoptions.PngOptions;
import com.aspose.psd.imageoptions.PsdOptions;
```

## Cos'è “set layer position” e perché è importante?

Quando aggiungi un nuovo livello, devi definire dove appare sulla tela. I metodi `setLeft`, `setTop`, `setRight` e `setBottom` **impostano la posizione del livello** in coordinate pixel. Un posizionamento corretto garantisce che la grafica si allinei esattamente dove ti aspetti, cosa cruciale per attività come il compositing di asset UI o la preparazione di file pronti per la stampa.

## Guida passo‑passo

### Passo 1: Carica il file PSD

Per prima cosa, carica il PSD esistente che desideri modificare. Questo ti fornisce un oggetto `PsdImage` con cui lavorare.

```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "OneLayer.psd";
PsdImage im = (PsdImage)Image.load(sourceFileName);
```

### Passo 2: Prepara i dati pixel e i rettangoli

Creeremo due buffer pixel (`int[]`) e definiremo le aree rettangolari dove i nuovi livelli saranno dipinti. Questa è la base per **creare un nuovo livello psd**.

```java
int[] data1 = new int[2500];
int[] data2 = new int[2500];
Rectangle rect1 = new Rectangle(0, 0, 50, 50);
Rectangle rect2 = new Rectangle(0, 0, 100, 25);
```

### Passo 3: Inizializza i dati del livello

Riempiremo i buffer pixel con un valore ARGB predefinito. Il valore `-10000000` corrisponde a una tonalità scura semi‑trasparente.

```java
for (int i = 0; i < 2500; i++) {
    data1[i] = -10000000;
    data2[i] = -10000000;
}
```

### Passo 4: Aggiungi livelli regolari (manipola i livelli PSD)

Ora **aggiungiamo livelli regolari** all'immagine PSD e **impostiamo la posizione del livello** usando le proprietà left, top, right e bottom. Questo dimostra come **manipolare i livelli PSD** programmaticamente.

```java
Layer layer1 = im.addRegularLayer();
layer1.setLeft(25);
layer1.setTop(25);
layer1.setRight(75);
layer1.setBottom(75);
layer1.saveArgb32Pixels(rect1, data1);

Layer layer2 = im.addRegularLayer();
layer2.setLeft(25);
layer2.setTop(150);
layer2.setRight(1255);
layer2.setBottom(175);
layer2.saveArgb32Pixels(rect2, data2);
```

### Passo 5: Esporta PSD in PNG e salva il PSD aggiornato

Dopo aver posizionato i livelli, salva il documento modificato. Prima esportiamo il risultato in PNG (il passo **export psd to png**), poi persi​stiamo il PSD con i nuovi livelli.

```java
String exportPath = dataDir + "Updated.psd";
String exportPathPng = dataDir + "Updated.png";

im.save(exportPath, new PsdOptions());          // Save the updated PSD
im.save(exportPathPng, new PngOptions());       // Export PSD to PNG
```

> **Consiglio esperto:** Se ti serve solo il PNG, puoi saltare la chiamata `save` del PSD e invocare direttamente `save` con `PngOptions`.

## Problemi comuni e risoluzione

| Sintomo | Probabile causa | Soluzione |
|---------|-----------------|-----------|
| Il PNG appare vuoto | I livelli sono invisibili o completamente trasparenti | Assicurati di impostare valori pixel non trasparenti o chiama `layer.setVisible(true)`. |
| `ArrayIndexOutOfBoundsException` | Discrepanza tra la dimensione del rettangolo e la lunghezza dell'array di pixel | Verifica che `rect.width * rect.height == dataArray.length`. |
| LicenseException a runtime | Nessuna licenza valida caricata | Carica una licenza temporanea o permanente prima di chiamare qualsiasi metodo API. |

## Domande frequenti

**D: Aspose.PSD è compatibile con Java 8?**  
R: Sì, Aspose.PSD supporta Java 8 e versioni successive.

**D: Posso applicare trasformazioni (rotazione, scala) ai livelli aggiunti?**  
R: Assolutamente! La classe `Layer` fornisce metodi come `rotate`, `scale` e `translate` per un controllo completo delle trasformazioni.

**D: Dove posso trovare ulteriore documentazione su Aspose.PSD?**  
R: La documentazione API dettagliata è disponibile [qui](https://reference.aspose.com/psd/java/).

**D: Come ottengo una licenza temporanea per Aspose.PSD?**  
R: Visita la pagina della licenza temporanea [qui](https://purchase.aspose.com/temporary-license/).

**D: Esistono forum della community per il supporto di Aspose.PSD?**  
R: Sì, partecipa alle discussioni nei forum Aspose [qui](https://forum.aspose.com/c/psd/34).

## Conclusione

Ora sai come **esportare PSD in PNG** aggiungendo **nuovi livelli regolari** usando Aspose.PSD per Java, e hai visto come una **licenza temporanea di aspose** ti permette di provare questo flusso di lavoro senza restrizioni. Questo tutorial mostra le principali capacità di **manipolazione di immagini psd**: caricamento di un file, creazione di livelli, popolamento dei dati pixel e esportazione della composizione finale. Sentiti libero di sperimentare con diverse dimensioni dei rettangoli, colori dei pixel o effetti di livello per adattare l'output alle esigenze del tuo progetto.

---

**Ultimo aggiornamento:** 2026-04-08  
**Testato con:** Aspose.PSD 24.11 per Java  
**Autore:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}