---
title: Aggiungi effetti pattern in Aspose.PSD per Java
linktitle: Aggiungi effetti di pattern
second_title: API Java Aspose.PSD
description: Migliora i tuoi modelli di immagini Java senza sforzo con Aspose.PSD per Java. Segui il nostro tutorial passo passo per aggiungere effetti pattern accattivanti.
type: docs
weight: 12
url: /it/java/advanced-image-effects/add-pattern-effects/
---
## introduzione

Nel mondo dello sviluppo Java, migliorare i modelli di immagine è un compito comune e Aspose.PSD per Java fornisce una soluzione solida per questo. Questo tutorial ti guiderà attraverso il processo di aggiunta di effetti pattern utilizzando Aspose.PSD, assicurando che le tue immagini risaltino con sovrapposizioni e miglioramenti unici.

## Prerequisiti

Prima di immergerti nel tutorial, assicurati di avere i seguenti prerequisiti:

- Java Development Kit (JDK) installato sul tuo sistema.
-  Aspose.PSD per la libreria Java scaricata e aggiunta al tuo progetto. Puoi scaricarlo da[Sito web Aspose.PSD](https://releases.aspose.com/psd/java/).

## Importa pacchetti

Nel tuo progetto Java, importa i pacchetti necessari per lavorare con Aspose.PSD. Includi il seguente codice all'inizio della tua classe Java:

```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;
import com.aspose.psd.Rectangle;


import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.BlendMode;
import com.aspose.psd.fileformats.psd.layers.fillsettings.FillType;
import com.aspose.psd.fileformats.psd.layers.fillsettings.PatternFillSettings;
import com.aspose.psd.fileformats.psd.layers.layereffects.PatternOverlayEffect;
import com.aspose.psd.fileformats.psd.layers.layerresources.PattResource;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;

import java.util.UUID;
```

## Passaggio 1: caricare l'immagine

```java
// Carica l'immagine PSD
String sourceFileName = "YourImagePath/PatternOverlay.psd";
String exportPath = "YourExportPath/PatternOverlayChanged.psd";

PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);

PsdImage im = (PsdImage)Image.load(sourceFileName, loadOptions);
```

Assicurati di sostituire "YourImagePath" e "YourExportPath" con i percorsi effettivi nel tuo progetto.

## Passaggio 2: estrarre le informazioni sulla sovrapposizione del modello

```java
// Estrai informazioni sulla sovrapposizione del modello
PatternOverlayEffect patternOverlay = (PatternOverlayEffect)im.getLayers()[1].getBlendingOptions().getEffects()[0];
```

## Passaggio 3: modificare le impostazioni di sovrapposizione del modello

```java
// Modifica le impostazioni di sovrapposizione del modello
PatternFillSettings settings = patternOverlay.getSettings();
settings.setColor(Color.getGreen());
patternOverlay.setOpacity((byte)193);
patternOverlay.setBlendMode(BlendMode.Difference);
settings.setHorizontalOffset(15);
settings.setVerticalOffset(11);
```

## Passaggio 4: modificare i dati del modello

```java
// Modifica i dati del modello
PattResource resource;
UUID guid = UUID.randomUUID();
String newPatternName = "$$/Presets/Patterns/Pattern=Some new pattern name\0";

for (int i = 0; i < im.getGlobalLayerResources().length; i++) {
    if (im.getGlobalLayerResources()[i] instanceof PattResource) {
        resource = (PattResource)im.getGlobalLayerResources()[i];
        resource.setPatternId(guid.toString());
        resource.setName(newPatternName);
        resource.setPattern(new int[]{Color.getAqua().toArgb(), Color.getRed().toArgb(),
                        Color.getRed().toArgb(), Color.getAqua().toArgb(),
                        Color.getAqua().toArgb(), Color.getWhite().toArgb(),
                        Color.getWhite().toArgb(), Color.getAqua().toArgb()}, new Rectangle(0, 0, 4, 2));
    }
}
```

## Passaggio 5: salva l'immagine modificata

```java
// Salva l'immagine modificata
settings.setPatternName(newPatternName);
settings.setPatternId(guid.toString() + "\0");
im.save(exportPath);
```

## Passaggio 6: verificare le modifiche

```java
// Verificare le modifiche nel file modificato
PsdImage img = (PsdImage)Image.load(sourceFileName, loadOptions);
PatternOverlayEffect patternOverlayEffect = (PatternOverlayEffect)img.getLayers()[1].getBlendingOptions().getEffects()[0];

// Aggiungi asserzioni per garantire che le modifiche siano state applicate correttamente
```

## Conclusione

Congratulazioni! Hai imparato con successo come aggiungere effetti pattern utilizzando Aspose.PSD per Java. Questa potente libreria ti consente di creare immagini visivamente accattivanti con motivi personalizzati, offrendo infinite possibilità per i tuoi progetti basati su Java.

## Domande frequenti

### Q1: posso utilizzare Aspose.PSD per Java con altre librerie di elaborazione delle immagini Java?

A1: Aspose.PSD per Java è progettato per funzionare in modo indipendente, ma è possibile integrarlo con altre librerie Java, se necessario.

### Q2: Dove posso trovare la documentazione dettagliata per Aspose.PSD per Java?

 A2: Fare riferimento a[Aspose.PSD per la documentazione Java](https://reference.aspose.com/psd/java/) per informazioni complete.

### Q3: È disponibile una prova gratuita per Aspose.PSD per Java?

 R3: Sì, puoi accedere alla prova gratuita[Qui](https://releases.aspose.com/).

### Q4: Come posso ottenere supporto per Aspose.PSD per Java?

 A4: Visita il[Forum Aspose.PSD](https://forum.aspose.com/c/psd/34) per il supporto della comunità o considera l'acquisto di un piano di supporto.

### Q5: posso ottenere una licenza temporanea per Aspose.PSD per Java?

R5: Sì, puoi ottenere una licenza temporanea[Qui](https://purchase.aspose.com/temporary-license/).