---
date: 2026-04-03
description: Scopri come salvare un PSD come PNG con effetto contorno e riempimento
  colore usando Aspose.PSD per Java. Questa guida passo‑passo mostra come esportare
  rapidamente un PSD in PNG.
keywords:
- save psd as png
- export psd to png
- set stroke color
- apply layer effects
- customize stroke width
linktitle: Salva PSD come PNG con effetto contorno – Java
second_title: Aspose.PSD Java API
title: Salva PSD come PNG con effetto contorno – Java
url: /it/java/psd-layer-management-effects/apply-stroke-effect-color-fill-psd/
weight: 21
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Salva PSD come PNG con effetto contorno e riempimento colore – Java

## Introduzione

In questa guida imparerai a **salvare PSD come PNG** applicando un effetto contorno con un riempimento colore usando Aspose.PSD per Java. Che tu sia uno sviluppatore esperto o alle prime armi, questo tutorial passo‑a‑passo renderà semplice completare il lavoro. Copriremo tutto, dall'impostazione dell'ambiente all'esportazione dell'immagine finale, così potrai rapidamente **esportare PSD in PNG** nei tuoi progetti.

## Risposte rapide
- **Che cosa realizza questo tutorial?** Mostra come salvare un file PSD come PNG dopo aver applicato un effetto contorno personalizzabile.  
- **Quale libreria viene utilizzata?** Aspose.PSD per Java.  
- **È necessaria una licenza?** Una versione di prova gratuita è sufficiente per i test; è necessaria una licenza per la produzione.  
- **Posso cambiare il colore del contorno?** Sì – è possibile impostare qualsiasi colore tramite `ColorFillSettings`.  
- **È possibile elaborare in batch?** Assolutamente – avvolgi il codice in un ciclo per elaborare più file PSD.

## Cos'è “salvare PSD come PNG”?
Salvare un PSD come PNG significa convertire il file a livelli nativo di Photoshop in un formato immagine piatto, adatto al web, mantenendo la fedeltà visiva. Questo è utile quando è necessario visualizzare contenuti PSD su siti web, app mobili o qualsiasi piattaforma che non supporta direttamente i file PSD.

## Perché applicare un effetto contorno con riempimento colore?
Un contorno aggiunge un bordo nitido attorno al contenuto dei livelli, facendo risaltare la grafica su sfondi complessi. Combinarlo con un colore di riempimento personalizzato consente di marchiare le immagini, evidenziare elementi UI o creare miniature accattivanti senza uscire da Photoshop.

## Prerequisiti

1. **Java Development Kit (JDK) 8+** – assicurati che `java` sia nel tuo PATH.  
2. **Aspose.PSD per Java** – scarica dal [sito web](https://releases.aspose.com/psd/java/).  
3. **IDE** – IntelliJ IDEA, Eclipse o qualsiasi editor tu preferisca.  
4. **PSD di esempio** – un file che contiene già un effetto contorno (oppure aggiungine uno in Photoshop).  
5. **Conoscenze di base di Java** – scriverai qualche riga di codice, ma nulla di avanzato.

Una volta pronti, possiamo iniziare a programmare.

## Importa pacchetti

```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.fillsettings.ColorFillSettings;
import com.aspose.psd.fileformats.psd.layers.layereffects.StrokeEffect;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
import com.aspose.psd.imageoptions.PngOptions;
import com.aspose.psd.imageoptions.PsdOptions;
```

Queste importazioni includono tutte le classi necessarie per caricare un PSD, modificare il suo contorno e salvare sia l'output PSD che PNG.

## Come salvare PSD come PNG con effetto contorno

### Passo 1: Carica il file PSD

Per prima cosa, indica la cartella che contiene il tuo PSD di origine.

```java
String dataDir = "Your Document Directory";
```

Sostituisci `"Your Document Directory"` con il percorso reale sul tuo computer.

Ora carica il file preservando eventuali risorse di effetto esistenti:

```java
String sourceFileName = dataDir + "StrokeComplex.psd";

PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);

PsdImage im = (PsdImage) Image.load(sourceFileName, loadOptions);
```

### Passo 2: Imposta il colore del contorno (e opzionalmente personalizza lo spessore)

Il ciclo seguente scorre ogni livello, prende il primo `StrokeEffect` e ne modifica il colore di riempimento. Puoi anche regolare `setWidth` o `setPosition` sull'oggetto `StrokeEffect` se devi **personalizzare lo spessore del contorno**.

```java
for (int i = 0; i < im.getLayers().length; i++) {
    StrokeEffect effect = (StrokeEffect) im.getLayers()[i].getBlendingOptions().getEffects()[0];
    ColorFillSettings settings = (ColorFillSettings) effect.getFillSettings();
    // Set the stroke color – change to any Color you like
    settings.setColor(Color.getDeepPink());
}
```

> **Consiglio professionale:** `Color.getDeepPink()` è solo un esempio. Usa `new Color(r, g, b)` per valori RGB personalizzati.

### Passo 3: Salva il PSD modificato (opzionale)

Se desideri conservare una versione PSD con il contorno aggiornato, salvala così:

```java
String exportPath = dataDir + "StrokeComplexRendering.psd";
im.save(exportPath, new PsdOptions());
```

### Passo 4: Esporta l'immagine come PNG (il passaggio principale “salvare PSD come PNG”)

Infine, converti il PSD modificato in un file PNG pronto per l'uso web:

```java
String exportPathPng = dataDir + "StrokeComplexRendering.png";
PngOptions option = new PngOptions();
option.setColorType(PngColorType.TruecolorWithAlpha);

im.save(exportPathPng, option);
```

Il PNG conserva il contorno rosa intenso impostato in precedenza, e l'opzione `TruecolorWithAlpha` garantisce che la trasparenza venga mantenuta.

## Problemi comuni e soluzioni

| Problema | Motivo | Soluzione |
|----------|--------|-----------|
| **`ArrayIndexOutOfBoundsException`** | Il livello non ha effetti o il primo effetto non è un `StrokeEffect`. | Verifica che il livello contenga effettivamente un contorno o itera attraverso `getEffects()` per trovare il tipo corretto. |
| **Il colore non cambia** | Potresti stare modificando una copia delle impostazioni invece dell'originale. | Assicurati di fare il cast a `ColorFillSettings` direttamente da `effect.getFillSettings()`. |
| **Il PNG appare vuoto** | Il PSD è stato caricato senza rasterizzare il livello. | Chiama `im.save(..., new PngOptions())` dopo tutte le modifiche; evita di salvare l'`im` originale prima delle modifiche. |

## Domande frequenti

**D: Posso applicare più effetti a un singolo livello usando Aspose.PSD per Java?**  
R: Sì, puoi accedere alle opzioni di fusione del livello e aggiungere tutti gli effetti necessari, inclusi ombre, bagliori e contorni.

**D: È possibile automatizzare il processo per un batch di file PSD?**  
R: Assolutamente. Avvolgi la logica di caricamento, applicazione dell'effetto e salvataggio in un ciclo `for‑each` che itera sui file in una directory.

**D: Come posso annullare le modifiche apportate a un file PSD?**  
R: Ricarica il file originale prima di salvare qualsiasi modifica; Aspose.PSD non fornisce una pila di annullamento.

**D: Posso personalizzare lo spessore e la posizione del contorno?**  
R: Sì. Usa `effect.setWidth(float)` e `effect.setPosition(StrokeEffect.Position)` per controllare lo spessore e il posizionamento (interno, esterno o centrato).

**D: La libreria Aspose.PSD per Java è gratuita?**  
R: È disponibile una versione di prova gratuita per la valutazione. La piena funzionalità richiede una licenza acquistata. Consulta le [opzioni di acquisto](https://purchase.aspose.com/buy) per i dettagli.

---

**Ultimo aggiornamento:** 2026-04-03  
**Testato con:** Aspose.PSD 24.12 per Java  
**Autore:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}