---
date: 2026-08-28
description: Aggiungi un pattern a un livello in Java con Aspose.PSD. Segui questa
  guida passo‑passo per applicare un effetto stroke layer, configurare le risorse
  pattern e salvare i tuoi file PSD in modo efficiente.
keywords:
- add pattern to layer
- java add layer effect
- Aspose.PSD stroke pattern
lastmod: 2026-08-28
linktitle: Come aggiungere un pattern Stroke Layer in Java
og_description: Aggiungi un pattern a un livello in Java usando Aspose.PSD. Segui
  questa guida concisa per applicare un effetto stroke layer, configurare le risorse
  pattern e salvare i tuoi file PSD in modo efficiente.
og_image_alt: Guide showing how to add pattern to layer in Java with Aspose.PSD
og_title: Aggiungi un pattern a un livello in Java – tutorial Aspose.PSD
schemas:
- author: Aspose
  dateModified: '2026-08-28'
  description: Add pattern to layer in Java with Aspose.PSD. Follow this step‑by‑step
    guide to apply a stroke layer effect, configure pattern resources, and save your
    PSD files efficiently.
  headline: How to add pattern to layer in Java
  type: TechArticle
- description: Add pattern to layer in Java with Aspose.PSD. Follow this step‑by‑step
    guide to apply a stroke layer effect, configure pattern resources, and save your
    PSD files efficiently.
  name: How to add pattern to layer in Java
  steps:
  - name: load the PSD file
    text: 'Loading the document gives you access to its layer hierarchy and effect
      collection. `PsdLoadOptions` configures how the PSD is read, while `PsdImage`
      represents the loaded file in memory. java String dataDir = "Your Document Directory";
      String sourceFileName = dataDir + "Stroke.psd"; PsdLoadOptions '
  - name: prepare new pattern data
    text: Create a `PatternResource` that holds the bitmap you want to tile as a stroke
      pattern. `PatternResource` is a PSD global resource that stores a repeating
      bitmap pattern. `Rectangle` defines the bounds of the pattern, and `UUID` provides
      a unique identifier. java int[] newPattern = new int[] { Color.
  - name: access the stroke effect
    text: Identify the shape layer that already has a stroke, then retrieve its `StrokeEffect`
      object. `StrokeEffect` represents the stroke layer effect applied to a shape
      layer. java StrokeEffect patternStroke = (StrokeEffect)im.getLayers()[3].getBlendingOptions().getEffects()[0];
      Assert.areEqual(BlendMode.N
  - name: modify the stroke effect
    text: Now update the stroke’s properties to reference the new pattern resource.
  - name: apply the new pattern
    text: '`PatternFillSettings` holds the fill settings for a pattern‑based stroke
      effect. Commit the changes to the layer and write the updated PSD back to disk.
      java ((PatternFillSettings)patternStroke.getFillSettings()).setPatternName("$$/Presets/Patterns/HorizontalLine1=Horizontal
      Line 9\0"); ((PatternFil'
  - name: verify the changes
    text: 'Reload the file and inspect the stroke to confirm the pattern appears as
      expected. java PsdImage img = (PsdImage)Image.load(sourceFileName, loadOptions);
      StrokeEffect patternStrokeEffect = (StrokeEffect)img.getLayers()[3].getBlendingOptions().getEffects()[0];
      PattResource resource1 = null; for (int '
  type: HowTo
- questions:
  - answer: Aspose.PSD for Java is a library that enables developers to create, edit,
      and convert PSD (Photoshop Document) files programmatically.
    question: What is Aspose.PSD for Java?
  - answer: Yes, you can use it in commercial projects. You can purchase a license
      from the **Aspose purchase page**([Aspose purchase page](https://purchase.aspose.com/buy)).
    question: Can I use Aspose.PSD for Java in a commercial project?
  - answer: Yes, you can download a free trial version from the **Aspose releases
      page**([Aspose releases page](https://releases.aspose.com/)).
    question: Is there a free trial available for Aspose.PSD for Java?
  - answer: You can get support from the Aspose community forums **here**([Aspose
      PSD community forum](https://forum.aspose.com/c/psd/34)).
    question: How can I get support for Aspose.PSD for Java?
  - answer: You need a JDK installed and an IDE for development. The library supports
      Windows, Linux, and macOS.
    question: What are the system requirements for Aspose.PSD for Java?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- java graphics
- Aspose.PSD
- layer effects
title: Come aggiungere un pattern a un livello in Java
url: /it/java/java-graphics-drawing/add-stroke-layer-pattern/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Come aggiungere un motivo a un livello in Java

## Introduzione
Aggiungere un motivo a un livello in Java è una necessità comune quando è necessario arricchire i file Photoshop PSD con effetti di contorno personalizzati. Con Aspose.PSD per Java questo compito diventa semplice, anche se sei nuovo alla libreria. In questo tutorial imparerai come caricare un PSD, creare una risorsa di motivo, collegarla a un effetto di contorno e salvare il risultato — il tutto con istruzioni chiare passo passo.

## Risposte rapide
- **Quale libreria è necessaria?** Aspose.PSD for Java.  
- **Quanto tempo richiede l'implementazione?** Circa 10‑15 minuti per un motivo di base.  
- **È necessaria una licenza?** Una versione di prova gratuita funziona per lo sviluppo; è necessaria una licenza commerciale per la produzione.  
- **Quale versione di Java è supportata?** JDK 8 o successiva.  
- **Posso usarlo in un servizio web?** Sì, l'API è indipendente dalla piattaforma e funziona in qualsiasi ambiente Java.

## Che cosa significa aggiungere un motivo a un livello?
Aggiungere un motivo a un livello significa assegnare una bitmap a tasselli a un effetto di contorno o riempimento in modo che il grafico si ripeta lungo il contorno della forma. Questa tecnica è ampiamente usata per bordi decorativi, texture e sovrapposizioni di branding, consentendo ai designer di creare temi visivi coerenti senza dover disegnare manualmente ogni elemento.

## Perché usare Aspose.PSD per questo compito?
Aspose.PSD supporta **oltre 30 formati immagine** e può manipolare file PSD fino a **2 GB** senza caricare l'intero documento in memoria, offrendo prestazioni rapide su hardware server tipico. La sua API fluida consente di lavorare con gli effetti dei livelli in modo programmatico, eliminando la necessità di Photoshop nei flussi di lavoro automatizzati.

## Prerequisiti
- Java Development Kit (JDK) 8 o successivo installato.
- Aspose.PSD for Java – scaricalo dalla **pagina di download di Aspose.PSD for Java**([Aspose.PSD for Java download page](https://releases.aspose.com/psd/java/)) e aggiungi il JAR al classpath del tuo progetto.
- Un IDE come IntelliJ IDEA o Eclipse per modificare ed eseguire il codice di esempio.
- Un file PSD di esempio che contiene un livello forma che desideri modificare.

## Importa pacchetti
Per prima cosa, importa gli spazi dei nomi che forniscono l'accesso agli oggetti PSD, alle risorse e agli effetti.

```
// No actual code block is added to preserve original placeholders.
```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;
import com.aspose.psd.Rectangle;
import com.aspose.psd.examples.Utils.Assert;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.BlendMode;
import com.aspose.psd.fileformats.psd.layers.fillsettings.FillType;
import com.aspose.psd.fileformats.psd.layers.fillsettings.PatternFillSettings;
import com.aspose.psd.fileformats.psd.layers.layereffects.StrokeEffect;
import com.aspose.psd.fileformats.psd.layers.layerresources.PattResource;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
import java.util.UUID;
```
```

## Come aggiungere un motivo a un livello in Java?

Carica il PSD di destinazione, crea una risorsa di motivo, collegala all'effetto di contorno del livello desiderato e infine salva il file. Questo flusso end‑to‑end richiede solo poche righe di codice e funziona con qualsiasi PSD standard che contenga un livello forma vettoriale.

### Passo 1: caricare il file PSD
Caricare il documento ti dà accesso alla sua gerarchia di livelli e alla collezione di effetti.  
`PsdLoadOptions` configura come viene letto il PSD, mentre `PsdImage` rappresenta il file caricato in memoria.

```
// Placeholder for original code.
```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "Stroke.psd";
PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);
PsdImage im = (PsdImage)Image.load(sourceFileName, loadOptions);
```
```

Caricando il file PSD, ora puoi accedere e manipolare i suoi livelli e i suoi effetti.

### Passo 2: preparare i nuovi dati del motivo
Crea un `PatternResource` che contiene la bitmap che desideri ripetere come motivo di contorno.  
`PatternResource` è una risorsa globale PSD che memorizza un motivo bitmap ripetuto. `Rectangle` definisce i confini del motivo, e `UUID` fornisce un identificatore unico.

```
// Placeholder for original code.
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
```

Questi dati del motivo saranno usati per creare il nuovo effetto di contorno.

### Passo 3: accedere all'effetto di contorno
Identifica il livello forma che ha già un contorno, quindi recupera il suo oggetto `StrokeEffect`.  
`StrokeEffect` rappresenta l'effetto di contorno del livello applicato a un livello forma.

```
// Placeholder for original code.
```java
StrokeEffect patternStroke = (StrokeEffect)im.getLayers()[3].getBlendingOptions().getEffects()[0];
Assert.areEqual(BlendMode.Normal, patternStroke.getBlendMode());
Assert.areEqual(255, patternStroke.getOpacity());
Assert.areEqual(true, patternStroke.isVisible());
PatternFillSettings fillSettings = (PatternFillSettings)patternStroke.getFillSettings();
Assert.areEqual(FillType.Pattern, fillSettings.getFillType());
```
```

Ciò garantisce che tu stia lavorando con il livello e l'effetto corretti.

### Passo 4: modificare l'effetto di contorno
Ora aggiorna le proprietà del contorno per fare riferimento alla nuova risorsa di motivo.

#### Aggiorna le proprietà dell'effetto di contorno
```
// Placeholder for original code.
```java
patternStroke.setOpacity((byte)127);
patternStroke.setBlendMode(BlendMode.Color);
```
```

#### Aggiorna la risorsa del motivo
`PattResource` è una risorsa di livello globale PSD che memorizza i dati del motivo.

```
// Placeholder for original code.
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
```

Questi frammenti sostituiscono il motivo esistente con quello fornito.

### Passo 5: applicare il nuovo motivo
`PatternFillSettings` contiene le impostazioni di riempimento per un effetto di contorno basato su motivo. Applica le modifiche al livello e scrivi il PSD aggiornato su disco.

```
// Placeholder for original code.
```java
((PatternFillSettings)patternStroke.getFillSettings()).setPatternName("$$/Presets/Patterns/HorizontalLine1=Horizontal Line 9\0");
((PatternFillSettings)patternStroke.getFillSettings()).setPatternId(guid.toString() + "\0");
im.save(exportPath);
```
```

Ciò garantisce che il nuovo motivo sia applicato correttamente e che il file sia salvato con le modifiche.

### Passo 6: verificare le modifiche
Ricarica il file e ispeziona il contorno per confermare che il motivo appare come previsto.

```
// Placeholder for original code.
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
```

Questo passaggio verifica che i dati del motivo siano stati applicati correttamente all'effetto di contorno.

## Problemi comuni e risoluzione
- **Motivo non visibile:** Assicurati che i DPI dell'immagine del motivo corrispondano alla risoluzione del PSD e che il flag `Enabled` del contorno sia impostato su `true`.  
- **File PSD di grandi dimensioni causano OutOfMemoryError:** Usa `PsdImage.load(..., LoadOptions)` con `LoadOptions.setLoadAllLayers(false)` per caricare i livelli su richiesta.  
- **Livello errato selezionato:** Verifica l'indice o il nome del livello prima di accedere ai suoi effetti; puoi enumerare `psdImage.getLayers()` per elencare i livelli disponibili.

## Domande frequenti

**Q: Che cos'è Aspose.PSD per Java?**  
A: Aspose.PSD for Java è una libreria che consente agli sviluppatori di creare, modificare e convertire file PSD (Photoshop Document) programmaticamente.

**Q: Posso usare Aspose.PSD per Java in un progetto commerciale?**  
A: Sì, puoi usarlo in progetti commerciali. Puoi acquistare una licenza dalla **pagina di acquisto di Aspose**([Aspose purchase page](https://purchase.aspose.com/buy)).

**Q: È disponibile una versione di prova gratuita per Aspose.PSD per Java?**  
A: Sì, puoi scaricare una versione di prova gratuita dalla **pagina di rilascio di Aspose**([Aspose releases page](https://releases.aspose.com/)).

**Q: Come posso ottenere supporto per Aspose.PSD per Java?**  
A: Puoi ottenere supporto dai forum della community di Aspose **qui**([Aspose PSD community forum](https://forum.aspose.com/c/psd/34)).

**Q: Quali sono i requisiti di sistema per Aspose.PSD per Java?**  
A: È necessario avere installato un JDK e un IDE per lo sviluppo. La libreria supporta Windows, Linux e macOS.

## Conclusione
Hai ora imparato come aggiungere un motivo a un livello in Java usando Aspose.PSD. Seguendo i passaggi sopra, puoi migliorare programmaticamente i file PSD con motivi di contorno personalizzati, automatizzare i flussi di lavoro di branding e integrare l'elaborazione grafica in qualsiasi applicazione basata su Java. Esplora altre funzionalità di Aspose.PSD come l'unione dei livelli, le regolazioni di colore e l'esportazione in PNG o JPEG per ampliare ulteriormente il tuo toolkit di elaborazione delle immagini.

---

**Ultimo aggiornamento:** 2026-08-28  
**Testato con:** Aspose.PSD 24.11 for Java  
**Autore:** Aspose

## Tutorial correlati

- [Render Pattern Fill Layer File PSD](/psd/java/advanced-psd-layer-features-effects/render-pattern-fill-layer-psd-files/)
- [Pattern Overlay PSD: Aggiungi effetti con Aspose.PSD per Java](/psd/java/advanced-image-effects/add-pattern-effects/)
- [Come cambiare il colore del contorno in Java usando Aspose.PSD](/psd/java/advanced-image-effects/add-stroke-layer-color/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}
{{< blocks/products/products-backtop-button >}}