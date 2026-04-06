---
date: 2025-12-30
description: Scopri come cambiare il colore dell'ombra e personalizzare gli effetti
  di ombra usando Aspose.PSD per Java. Segui questo tutorial passo‑passo sugli effetti
  di ombra.
linktitle: Support Shadow Effect
second_title: Aspose.PSD Java API
title: Come cambiare il colore dell'ombra con Aspose.PSD per Java
url: /it/java/basic-image-operations/support-shadow-effect/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Modifica il colore dell'ombra con Aspose.PSD for Java

## Introduzione

Aggiungere profondità alle tue grafiche spesso significa **modificare il colore dell'ombra** per adattarlo all'umore del design. Con Aspose.PSD for Java puoi facilmente aggiungere o modificare gli effetti di ombra esterna, controllare l'opacità e perfezionare altri parametri—tutto dal codice Java. In questo **tutorial sugli effetti di ombra** vedremo come caricare un PSD, leggere l'ombra esistente, personalizzarne colore, opacità, distanza e infine salvare il file aggiornato.

## Risposte rapide
- **Cosa significa “cambiare il colore dell'ombra”?** Aggiorna la proprietà colore di un DropShadowEffect applicato a un livello PSD.  
- **Quale libreria lo supporta?** Aspose.PSD for Java fornisce pieno supporto per gli effetti di ombra.  
- **È necessaria una licenza?** Una versione di prova funziona per lo sviluppo; è richiesta una licenza commerciale per la produzione.  
- **Posso impostare l'opacità dell'ombra?** Sì – usa `setOpacity(byte)` per definire la trasparenza (0‑255).  
- **Il codice è compatibile con Java 8+?** Assolutamente, l'API è destinata a Java 8 e versioni successive.

## Che cosa significa “cambiare il colore dell'ombra” nei file PSD?

Modificare il colore dell'ombra cambia la tonalità visiva dell'ombra esterna che appare dietro un livello. Questo è utile per creare illuminazioni realistiche, abbinare i colori del brand o semplicemente aggiungere un tocco artistico.

## Perché usare Aspose.PSD for Java per personalizzare gli effetti di ombra?

- **Fedele riproduzione del PSD** – tutti gli effetti di livello, incluse le ombre, sono preservati.  
- **Nessun Photoshop necessario** – manipola i file programmaticamente su qualsiasi server.  
- **Controllo dettagliato** – regola colore, opacità, distanza, angolo, diffusione e rumore.  
- **Cross‑platform** – funziona su JVM Windows, Linux e macOS.

## Prerequisiti

- Conoscenza di base della programmazione Java.  
- Aspose.PSD for Java installato. Puoi scaricarlo [qui](https://releases.aspose.com/psd/java/).  

## Importare i pacchetti

Prima di iniziare, importa le classi necessarie per lavorare con le immagini e gli effetti di ombra:

```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;


import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.layereffects.DropShadowEffect;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
```

## Guida passo‑passo

### Passo 1: Caricare l'immagine PSD

Per prima cosa, carica il PSD di origine abilitando il caricamento delle risorse degli effetti:

```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "Shadow.psd";
String psdPathAfterChange = dataDir + "ShadowChanged.psd";

PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);

PsdImage im = (PsdImage)Image.load(sourceFileName, loadOptions);
```

### Passo 2: Recuperare l'effetto Drop Shadow esistente

Individua l'effetto ombra sul livello desiderato (in questo esempio, il secondo livello):

```java
DropShadowEffect shadowEffect = (DropShadowEffect)(im.getLayers()[1].getBlendingOptions().getEffects()[0]);
```

### Passo 3: Verificare le impostazioni predefinite (opzionale)

Eseguire queste asserzioni ti aiuta a comprendere i valori originali prima di modificarli:

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

### Passo 4: **Modificare il colore dell'ombra** e personalizzare altre proprietà

Ora **modifichiamo il colore dell'ombra** in verde, regiamo l'opacità, la distanza, la dimensione e altri attributi. Questo dimostra le capacità di **personalizzare l'effetto ombra** di Aspose.PSD:

```java
shadowEffect.setColor(Color.getGreen());          // change shadow color
shadowEffect.setOpacity((byte)128);               // set shadow opacity (50% transparent)
shadowEffect.setDistance(11);                     // move shadow farther from the object
shadowEffect.setUseGlobalLight(false);            // use local lighting
shadowEffect.setSize(9);                          // adjust blur radius
shadowEffect.setAngle(45);                        // rotate light source
shadowEffect.setSpread(3);                        // increase spread
shadowEffect.setNoise(50);                        // add texture noise
```

### Passo 5: Salvare l'immagine modificata

Infine, scrivi il PSD aggiornato su disco:

```java
im.save(psdPathAfterChange);
```

## Problemi comuni e suggerimenti

- **NullPointerException durante il recupero degli effetti** – assicurati di chiamare `setLoadEffectsResource(true)`; altrimenti gli effetti non vengono caricati.  
- **Il colore non cambia** – verifica di modificare l'indice di livello corretto (`im.getLayers()[1]` in questo esempio).  
- **L'opacità sembra invariata** – ricorda che l'opacità è un byte (0‑255). È necessario il cast a `(byte)`.  

## Conclusione

Seguendo questi passaggi puoi **modificare il colore dell'ombra**, **impostare l'opacità dell'ombra** e personalizzare completamente i parametri dell'**effetto ombra** in qualsiasi file PSD usando Aspose.PSD for Java. Questo ti consente di creare grafiche più ricche programmaticamente, senza dover ricorrere a Photoshop manualmente.

## Domande frequenti

**D: Aspose.PSD for Java è adatto a progetti professionali di design grafico?**  
R: Assolutamente! Aspose.PSD for Java è una libreria potente progettata per compiti professionali di design grafico.

**D: Posso usare Aspose.PSD for Java in applicazioni commerciali?**  
R: Sì, Aspose.PSD for Java è un prodotto commerciale. Puoi acquistarlo [qui](https://purchase.aspose.com/buy).

**D: È disponibile una versione di prova gratuita?**  
R: Sì, puoi provare la versione di prova gratuita [qui](https://releases.aspose.com/).

**D: Dove posso trovare la documentazione dettagliata?**  
R: Consulta la documentazione completa [qui](https://reference.aspose.com/psd/java/).

**D: Come posso ottenere supporto per Aspose.PSD for Java?**  
R: Unisciti al forum della community [qui](https://forum.aspose.com/c/psd/34) per qualsiasi domanda di supporto.

---

**Ultimo aggiornamento:** 2025-12-30  
**Testato con:** Aspose.PSD for Java 24.10  
**Autore:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}