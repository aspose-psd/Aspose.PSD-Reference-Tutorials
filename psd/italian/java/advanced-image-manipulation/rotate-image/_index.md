---
title: Ruota un'immagine in Aspose.PSD per Java
linktitle: Ruota un'immagine
second_title: API Java Aspose.PSD
description: Esplora la rotazione delle immagini in Java senza sforzo con Aspose.PSD. Ruota, capovolgi e salva facilmente i file PSD.
weight: 19
url: /it/java/advanced-image-manipulation/rotate-image/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Ruota un'immagine in Aspose.PSD per Java

## Introduzione

Aspose.PSD per Java fornisce un potente set di funzionalità per lavorare con le immagini, consentendo agli sviluppatori di manipolare ed elaborare in modo efficiente i file PSD. In questo tutorial ci concentreremo su un'attività specifica: ruotare un'immagine. Che tu stia creando un'applicazione di fotoritocco o semplicemente abbia bisogno di regolare l'orientamento di un'immagine, Aspose.PSD semplifica il processo.

## Prerequisiti

Prima di immergerti nel tutorial, assicurati di avere i seguenti prerequisiti:

-  Aspose.PSD per la libreria Java: assicurati di aver scaricato e installato la libreria Aspose.PSD per Java. Potete trovare la libreria e la documentazione dettagliata[Qui](https://reference.aspose.com/psd/java/).

- Ambiente di sviluppo Java: assicurati di avere un ambiente di sviluppo Java configurato sul tuo computer.

-  File PSD di esempio: prepara un file PSD di esempio che desideri ruotare. Regola il`sourceFile` variabile nel codice di esempio con il percorso del file PSD.

## Importa pacchetti

Inizia importando i pacchetti necessari per sfruttare le funzionalità di Aspose.PSD:

```java
import com.aspose.psd.Image;
import com.aspose.psd.RotateFlipType;

import com.aspose.psd.imageoptions.JpegOptions;
```

## Passaggio 1: caricare l'immagine

 Carica l'immagine esistente in un'istanza del file`Image` classe:

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";
Image image = Image.load(sourceFile);
```

## Passaggio 2: ruotare l'immagine

 Ruota l'immagine utilizzando il`rotateFlip` metodo. In questo esempio, ruotiamo l'immagine di 270 gradi:

```java
image.rotateFlip(RotateFlipType.Rotate270FlipNone);
```

## Passaggio 3: salva l'immagine ruotata

 Salvare l'immagine ruotata utilizzando il file`save` metodo e specificando il formato di output (JPEG, in questo caso):

```java
String destName = dataDir + "RotatedImage_out.jpg";
image.save(destName, new JpegOptions());
```

## Conclusione

Congratulazioni! Hai ruotato con successo un'immagine utilizzando Aspose.PSD per Java. Questa libreria semplice ma potente apre un mondo di possibilità per la manipolazione delle immagini nelle tue applicazioni Java.

## Domande frequenti

### Q1: Aspose.PSD è compatibile con diversi formati di immagine?

R1: Sì, Aspose.PSD supporta vari formati di immagine, inclusi PSD, JPEG, PNG e altri.

### Q2: Posso applicare rotazioni personalizzate, non solo inversioni predefinite?

A2: Assolutamente! Aspose.PSD offre flessibilità per l'applicazione di rotazioni personalizzate per soddisfare le vostre esigenze specifiche.

### Q3: Dove posso trovare ulteriore supporto o assistenza?

 R3: Per qualsiasi domanda o problema, visitare il[Aspose.PSD Forum](https://forum.aspose.com/c/psd/34) per il sostegno della comunità.

### Q4: È disponibile una prova gratuita?

 A4: Sì, puoi esplorare Aspose.PSD con a[prova gratuita](https://releases.aspose.com/).

### Q5: Come posso ottenere una licenza temporanea?

 R5: Se hai bisogno di una licenza temporanea, puoi ottenerne una[Qui](https://purchase.aspose.com/temporary-license/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
