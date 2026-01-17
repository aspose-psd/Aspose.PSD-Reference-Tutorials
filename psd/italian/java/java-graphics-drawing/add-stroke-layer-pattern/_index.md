---
date: 2026-01-17
description: Scopri come aggiungere un pattern di tratto in Java con Aspose.PSD per
  Java. Segui questa guida passo passo per migliorare rapidamente le tue immagini
  PSD.
linktitle: How to Add Stroke Layer Pattern in Java
second_title: Aspose.PSD Java API
title: Come aggiungere un pattern di tratto in Java usando Aspose.PSD
url: /it/java/java-graphics-drawing/add-stroke-layer-pattern/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Come aggiungere un pattern di tratto Java usando Aspose.PSD

## Introduzione
Se hai bisogno di **add stroke pattern java** in un file Photoshop, Aspose.PSD per Java lo rende sorprendentemente semplice. Che tu stia creando uno strumento di graphic‑design, automatizzando modifiche batch o semplicemente sperimentando con gli effetti di livello, questo tutorial ti guida passo passo—dall'apertura del PSD alla verifica del nuovo pattern. Immergiamoci e vediamo quanto rapidamente puoi migliorare le tue immagini.

## Risposte rapide
- **Quale libreria è necessaria?** Aspose.PSD for Java  
- **Quale versione di Java è supportata?** JDK 8 or later  
- **È necessaria una licenza per i test?** A free trial works for development; a license is required for production  
- **Quanto tempo richiede l'implementazione?** Roughly 10‑15 minutes for a basic pattern stroke  
- **Posso riutilizzare il pattern su più livelli?** Yes, just assign the same `PattResource` to other layers  

## Che cos'è add stroke pattern java?
Aggiungere un pattern di tratto in Java significa applicare un riempimento personalizzato (spesso una bitmap ripetuta) all'effetto di tratto di un livello. Questa tecnica ti consente di creare contorni stilizzati—ad esempio una linea tratteggiata, una texture a mattoni o un bordo grafico personalizzato—direttamente all'interno di un file PSD senza aprire Photoshop.

## Perché usare Aspose.PSD per add stroke pattern java?
- **Full PSD fidelity** – All layer effects, resources, and blending modes are preserved.  
- **No native Photoshop required** – Works on any OS with a JDK.  
- **Programmatic control** – Automate batch processing or integrate into server‑side services.  
- **Rich API** – Access to global resources, pattern fills, and blend modes in a single fluent interface.

## Prerequisiti
- **Java Development Kit (JDK)** – Assicurati che JDK 8 or newer is installed.  
- **Aspose.PSD for Java** – Download the library from [here](https://releases.aspose.com/psd/java/) and add the JAR to your project’s classpath.  
- **IDE** – IntelliJ IDEA, Eclipse, or any editor you prefer.

## Importa i pacchetti
Per prima cosa, importa le classi necessarie per gestire i file PSD, i colori, i rettangoli e gli effetti di tratto.

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

## Passo 1: Carica il file PSD
Carica il PSD di origine in modo da poter lavorare con i suoi livelli e le sue risorse.

```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "Stroke.psd";
PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);
PsdImage im = (PsdImage)Image.load(sourceFileName, loadOptions);
```

## Passo 2: Prepara i nuovi dati del pattern
Crea un semplice pattern di 4 × 4 pixel che verrà utilizzato per il tratto.

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

## Passo 3: Accedi all'effetto di tratto
Individua l'effetto di tratto sul livello di destinazione (in questo esempio, il quarto livello).

```java
StrokeEffect patternStroke = (StrokeEffect)im.getLayers()[3].getBlendingOptions().getEffects()[0];
Assert.areEqual(BlendMode.Normal, patternStroke.getBlendMode());
Assert.areEqual(255, patternStroke.getOpacity());
Assert.areEqual(true, patternStroke.isVisible());
PatternFillSettings fillSettings = (PatternFillSettings)patternStroke.getFillSettings();
Assert.areEqual(FillType.Pattern, fillSettings.getFillType());
```

## Passo 4: Modifica l'effetto di tratto
### Aggiorna le proprietà dell'effetto di tratto
Regola l'opacità e la modalità di fusione per vedere l'impatto visivo del nuovo pattern.

```java
patternStroke.setOpacity((byte)127);
patternStroke.setBlendMode(BlendMode.Color);
```

### Aggiorna la risorsa del pattern
Sostituisci la risorsa del pattern globale esistente con quella appena creata.

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

## Passo 5: Applica il nuovo pattern
Associa la risorsa del pattern aggiornata all'effetto di tratto e salva il PSD.

```java
((PatternFillSettings)patternStroke.getFillSettings()).setPatternName("$$/Presets/Patterns/HorizontalLine1=Horizontal Line 9\0");
((PatternFillSettings)patternStroke.getFillSettings()).setPatternId(guid.toString() + "\0");
im.save(exportPath);
```

## Passo 6: Verifica le modifiche
Ricarica il file e conferma che il nuovo pattern, l'opacità e la modalità di fusione siano applicati correttamente.

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

## Problemi comuni e soluzioni
| Problema | Causa | Soluzione |
|----------|-------|-----------|
| Il pattern non appare | Riferimento `PatternId` errato | Assicurati che il `PatternId` impostato su `PattResource` corrisponda a quello usato in `PatternFillSettings`. |
| Il tratto scompare dopo il salvataggio | Opacità impostata a 0 o effetto nascosto | Verifica che `setOpacity` sia tra 0‑255 e che `isVisible()` restituisca `true`. |
| Colori inattesi | Incongruenza della modalità di fusione | Usa `BlendMode.Color` (o un'altra modalità) che corrisponda all'intento del tuo design. |

## FAQ
### Che cos'è Aspose.PSD per Java?
Aspose.PSD per Java è una libreria che consente agli sviluppatori di creare, modificare e convertire file PSD (Photoshop Document) in modo programmatico.

### Posso usare Aspose.PSD per Java in un progetto commerciale?
Sì, puoi usarlo in progetti commerciali. Puoi acquistare una licenza da [here](https://purchase.aspose.com/buy).

### È disponibile una versione di prova gratuita per Aspose.PSD per Java?
Sì, puoi scaricare una versione di prova gratuita da [here](https://releases.aspose.com/).

### Come posso ottenere supporto per Aspose.PSD per Java?
Puoi ottenere supporto dai forum della community di Aspose [here](https://forum.aspose.com/c/psd/34).

### Quali sono i requisiti di sistema per Aspose.PSD per Java?
È necessario avere installato JDK e un IDE per lo sviluppo. La libreria supporta più sistemi operativi, tra cui Windows, Linux e macOS.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Ultimo aggiornamento:** 2026-01-17  
**Testato con:** Aspose.PSD for Java 24.12 (latest at time of writing)  
**Autore:** Aspose