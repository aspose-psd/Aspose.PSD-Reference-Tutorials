---
title: Come aggiungere il modello di livello del tratto in Java
linktitle: Come aggiungere il modello di livello del tratto in Java
second_title: API Java Aspose.PSD
description: Scopri come aggiungere un modello di livello tratto ai file PSD utilizzando Aspose.PSD per Java. Segui questa guida passo passo per migliorare facilmente le tue immagini.
type: docs
weight: 11
url: /it/java/java-graphics-drawing/add-stroke-layer-pattern/
---
## introduzione
Aggiungere un modello di livello tratto a un'immagine in Java potrebbe sembrare un compito arduo, ma con Aspose.PSD per Java è più facile di quanto pensi. Che tu stia progettando grafica o lavorando su applicazioni di fotoritocco, questa guida ti guiderà attraverso il processo passo dopo passo. Pronti per iniziare? Immergiamoci!
## Prerequisiti
Prima di iniziare, avrai bisogno di alcune cose:
- Java Development Kit (JDK): assicurati di avere JDK installato sul tuo sistema.
-  Aspose.PSD per Java: scarica la libreria da[Qui](https://releases.aspose.com/psd/java/) e includilo nel tuo progetto.
- Un IDE: utilizza il tuo ambiente di sviluppo integrato (IDE) preferito come IntelliJ IDEA o Eclipse.
## Importa pacchetti
Per prima cosa, devi importare i pacchetti necessari nel tuo progetto Java. Questi pacchetti sono essenziali per lavorare con Aspose.PSD.
```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;
import com.aspose.psd.Rectangle;
import com.aspose.psd.examples.Utils.Assert;
import com.aspose.psd.examples.Utils.Utils;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.BlendMode;
import com.aspose.psd.fileformats.psd.layers.fillsettings.FillType;
import com.aspose.psd.fileformats.psd.layers.fillsettings.PatternFillSettings;
import com.aspose.psd.fileformats.psd.layers.layereffects.StrokeEffect;
import com.aspose.psd.fileformats.psd.layers.layerresources.PattResource;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
import java.util.UUID;
```
## Passaggio 1: carica il file PSD
Il primo passaggio per aggiungere un modello di livello tratto è caricare il file PSD che desideri modificare.
```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "Stroke.psd";
PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);
PsdImage im = (PsdImage)Image.load(sourceFileName, loadOptions);
```
Caricando il file PSD, ora puoi accedere e manipolare i suoi livelli ed effetti.
## Passaggio 2: preparare i nuovi dati del modello
Successivamente, devi preparare i nuovi dati del modello che applicherai al livello del tratto.
```java
int[] newPattern = new int[]
{
    Color.getAqua().toArgb(), Color.getRed().toArgb(), Color.getRed().toArgb(), Color.getAqua().toArgb(),
    Color.getAqua().toArgb(), Color.getWhite().toArgb(), Color.getWhite().toArgb(), Color.getAqua().toArgb(),
    Color.getAqua().toArgb(), Color.getWhite().toArgb(), Color.getWhite().toArgb(), Color.getAqua().toArgb(),
    Color.getAqua().toArgb(), Color.getRed().toArgb(), Color.getRed().toArgb(), Color.getAqua().toArgb(),
};
Rectangle newPatternBounds = new Rectangle(0, 0, 4, 4);
UUID guid = UUID.randomUUID();
```
I dati di questo modello verranno utilizzati per creare il nuovo effetto tratto.
## Passaggio 3: accedi all'effetto tratto
Per modificare l'effetto del tratto, è necessario accedere al livello specifico e alle sue opzioni di fusione.
```java
StrokeEffect patternStroke = (StrokeEffect)im.getLayers()[3].getBlendingOptions().getEffects()[0];
Assert.areEqual(BlendMode.Normal, patternStroke.getBlendMode());
Assert.areEqual(255, patternStroke.getOpacity());
Assert.areEqual(true, patternStroke.isVisible());
PatternFillSettings fillSettings = (PatternFillSettings)patternStroke.getFillSettings();
Assert.areEqual(FillType.Pattern, fillSettings.getFillType());
```
Ciò garantisce che stai lavorando con il livello e l'effetto corretti.
## Passaggio 4: modifica l'effetto tratto
Ora modifichiamo l'effetto del tratto con i nuovi dati del modello.
### Aggiorna le proprietà dell'effetto tratto
```java
patternStroke.setOpacity((byte)127);
patternStroke.setBlendMode(BlendMode.Color);
```
### Aggiorna la risorsa modello
```java
PattResource resource;
for (int i = 0; i < im.getGlobalLayerResources().length; i++)
{
    if (im.getGlobalLayerResources()[i] instanceof PattResource)
    {
        resource = (PattResource)im.getGlobalLayerResources()[i];
        resource.setPatternId(guid.toString());
        resource.setName("$$/Presets/Patterns/HorizontalLine1=Horizontal Line 9\0");
        resource.setPattern(newPattern, newPatternBounds);
    }
}
```
Questo frammento di codice aggiorna la risorsa modello con i nuovi dati modello.
## Passaggio 5: applica il nuovo modello
Infine, applica il nuovo modello all'effetto tratto e salva le modifiche.
```java
((PatternFillSettings)patternStroke.getFillSettings()).setPatternName("$$/Presets/Patterns/HorizontalLine1=Horizontal Line 9\0");
((PatternFillSettings)patternStroke.getFillSettings()).setPatternId(guid.toString() + "\0");
im.save(exportPath);
```
Ciò garantisce che il nuovo modello venga applicato correttamente e che il file venga salvato con le modifiche.
## Passaggio 6: verificare le modifiche
Per assicurarti che tutto funzioni correttamente, carica nuovamente il file e verifica le modifiche.
```java
PsdImage img = (PsdImage)Image.load(sourceFileName, loadOptions);
StrokeEffect patternStrokeEffect = (StrokeEffect)img.getLayers()[3].getBlendingOptions().getEffects()[0];
PattResource resource1 = null;
for (int i = 0; i < img.getGlobalLayerResources().length; i++)
{
    if (img.getGlobalLayerResources()[i] instanceof PattResource)
    {
        resource1 = (PattResource)img.getGlobalLayerResources()[i];
    }
}
try
{
    Assert.areEqual(newPattern, resource1.getPatternData());
    Assert.areEqual(newPatternBounds, new Rectangle(0, 0, resource1.getWidth(), resource1.getHeight()));
    Assert.areEqual(guid.toString(), resource1.getPatternId());
    Assert.areEqual(BlendMode.Color, patternStrokeEffect.getBlendMode());
    Assert.areEqual(127, patternStrokeEffect.getOpacity());
    Assert.areEqual(true, patternStrokeEffect.isVisible());
    PatternFillSettings fillSettings1 = (PatternFillSettings)patternStrokeEffect.getFillSettings();
    Assert.areEqual(FillType.Pattern, fillSettings1.getFillType());
}
catch (Exception e)
{
    System.out.println(e.getMessage());
}
```
Questo passaggio verifica che i dati del modello siano stati applicati correttamente all'effetto tratto.
## Conclusione
E il gioco è fatto! Hai aggiunto con successo un modello di livello del tratto a un file PSD utilizzando Aspose.PSD per Java. Seguendo questi passaggi, puoi personalizzare e migliorare le tue immagini con facilità. Buona programmazione!
## Domande frequenti
### Cos'è Aspose.PSD per Java?
Aspose.PSD per Java è una libreria che consente agli sviluppatori di creare, modificare e convertire file PSD (Photoshop Document) a livello di codice.
### Posso utilizzare Aspose.PSD per Java in un progetto commerciale?
 Sì, puoi usarlo in progetti commerciali. È possibile acquistare una licenza da[Qui](https://purchase.aspose.com/buy).
### È disponibile una prova gratuita per Aspose.PSD per Java?
 Sì, puoi scaricare una versione di prova gratuita da[Qui](https://releases.aspose.com/).
### Come posso ottenere supporto per Aspose.PSD per Java?
 Puoi ottenere supporto dai forum della comunità Aspose[Qui](https://forum.aspose.com/c/psd/34).
### Quali sono i requisiti di sistema per Aspose.PSD per Java?
È necessario che JDK sia installato e un IDE per lo sviluppo. La libreria supporta più sistemi operativi tra cui Windows, Linux e macOS.