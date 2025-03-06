---
title: Supporta l'effetto ombra in Aspose.PSD per Java
linktitle: Supporta l'effetto ombra
second_title: API Java Aspose.PSD
description: Scopri come aggiungere accattivanti effetti ombra alle immagini utilizzando Aspose.PSD per Java. Migliora la tua progettazione grafica con questo tutorial passo passo.
weight: 13
url: /it/java/basic-image-operations/support-shadow-effect/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Supporta l'effetto ombra in Aspose.PSD per Java

## Introduzione

Migliorare le immagini con effetti ombra è una pratica comune nella progettazione grafica, poiché aggiunge profondità e realismo. Aspose.PSD per Java fornisce un solido supporto per gli effetti ombra, consentendo agli sviluppatori di integrare facilmente questi effetti nelle loro applicazioni Java. In questo tutorial esploreremo come supportare gli effetti ombra utilizzando Aspose.PSD, passo dopo passo.

## Prerequisiti

Prima di immergerti nel tutorial, assicurati di avere i seguenti prerequisiti:

- Conoscenza base della programmazione Java.
-  Aspose.PSD per Java installato. Puoi scaricarlo[Qui](https://releases.aspose.com/psd/java/).

## Importa pacchetti

Assicurati di aver importato i pacchetti necessari per sfruttare le funzionalità Aspose.PSD nella tua applicazione Java. Utilizza il seguente snippet di codice come guida:

```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;


import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.layereffects.DropShadowEffect;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
```

## Passaggio 1: carica l'immagine PSD

```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "Shadow.psd";
String psdPathAfterChange = dataDir + "ShadowChanged.psd";

PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);

PsdImage im = (PsdImage)Image.load(sourceFileName, loadOptions);
```

## Passaggio 2: recupera l'effetto ombra

```java
DropShadowEffect shadowEffect = (DropShadowEffect)(im.getLayers()[1].getBlendingOptions().getEffects()[0]);
```

## Passaggio 3: verificare le impostazioni predefinite

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

## Passaggio 4: personalizza l'effetto ombra

```java
shadowEffect.setColor(Color.getGreen());
shadowEffect.setOpacity((byte)128);
shadowEffect.setDistance(11);
shadowEffect.setUseGlobalLight(false);
shadowEffect.setSize(9);
shadowEffect.setAngle(45);
shadowEffect.setSpread(3);
shadowEffect.setNoise(50);
```

## Passaggio 5: salva l'immagine modificata

```java
im.save(psdPathAfterChange);
```

## Conclusione

Con questi semplici passaggi, puoi supportare facilmente gli effetti ombra in Aspose.PSD per Java, migliorando l'attrattiva visiva delle tue immagini.

## Domande frequenti

### Q1: Aspose.PSD per Java è adatto a progetti di progettazione grafica professionale?

R1: Assolutamente! Aspose.PSD per Java è una potente libreria progettata per attività di progettazione grafica professionale.

### Q2: Posso utilizzare Aspose.PSD per Java in applicazioni commerciali?

 A2: Sì, Aspose.PSD per Java è un prodotto commerciale. Puoi acquistarlo[Qui](https://purchase.aspose.com/buy).

### Q3: È disponibile una prova gratuita?

 R3: Sì, puoi esplorare una versione di prova gratuita[Qui](https://releases.aspose.com/).

### Q4: Dove posso trovare la documentazione dettagliata?

 A4: Fare riferimento alla documentazione completa[Qui](https://reference.aspose.com/psd/java/).

### Q5: Come posso ottenere supporto per Aspose.PSD per Java?

 A5: Partecipa al forum della community[Qui](https://forum.aspose.com/c/psd/34) per qualsiasi richiesta di supporto.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
