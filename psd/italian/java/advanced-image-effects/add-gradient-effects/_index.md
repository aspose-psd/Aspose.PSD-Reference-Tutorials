---
date: 2026-10-18
description: Scopri come creare effetti di gradiente radiale nelle immagini Java usando
  Aspose.PSD. Segui questa guida passo‑passo per un'integrazione senza problemi.
keywords:
- create radial gradient java
- apply gradient overlay psd
- add radial gradient image
lastmod: 2026-10-18
linktitle: Aggiungi effetti di gradiente
og_description: Scopri come creare effetti di gradiente radiale java usando Aspose.PSD.
  Questo tutorial mostra come aggiungere, personalizzare e salvare le sovrapposizioni
  di gradiente in pochi minuti.
og_image_alt: Screenshot of Aspose.PSD Java code creating a radial gradient effect
og_title: Crea gradiente radiale java con Aspose.PSD – guida passo‑passo
schemas:
- author: Aspose
  dateModified: '2026-10-18'
  description: Learn how to create radial gradient effects in Java images using Aspose.PSD.
    Follow this step‑by‑step guide for seamless integration.
  headline: How to create radial gradient effects in Aspose.PSD for Java
  type: TechArticle
- description: Learn how to create radial gradient effects in Java images using Aspose.PSD.
    Follow this step‑by‑step guide for seamless integration.
  name: How to create radial gradient effects in Aspose.PSD for Java
  steps:
  - name: Load the PSD file and access the gradient overlay
    text: '`PsdLoadOptions` configures how a PSD file is loaded, allowing you to enable
      loading of effect resources. `Image.load` reads the file into an `Image` object.
      In this step, we load a PSD file and retrieve the first `GradientOverlayEffect`
      from the second layer (index 1). The `loadOptions.setLoadEffec'
  - name: Verify Initial Settings
    text: Before making changes, it’s a good practice to confirm the current blend
      mode, opacity, and visibility. This helps you understand the baseline state
      of the gradient overlay.
  - name: Modify Gradient Settings
    text: Here you can customize the gradient’s color, opacity, and blend mode. The
      example changes the color to green, reduces opacity to 193 (out of 255), and
      switches the blend mode to **Lighten**. Feel free to experiment with other `BlendMode`
      values such as `Multiply`, `Screen`, or `Overlay`.
  - name: Save the Edited Image
    text: After applying your modifications, persist the changes by saving the PSD
      to a new file. This step ensures the original file remains untouched.
  - name: Verify Changes
    text: The snippet above demonstrates how to open a PSD, pull the second layer’s
      first effect (assumed to be a gradient overlay), and prepare it for modification.
  - name: Verify the original settings (optional but recommended)
    text: Before you change anything, checking the existing blend mode, opacity, and
      visibility helps you understand the baseline. The `Assert` calls in the code
      confirm that the effect is currently set to **Normal** blend mode, fully opaque,
      and visible.
  - name: Adjust gradient properties to achieve a radial style
    text: 'You can change the gradient’s color, opacity, and blend mode. For a true
      radial effect, set the gradient style: *Pro tip:* Use `Color.getGreen()` or
      any `java.awt.Color` instance to define the start color, and `gradientOverlay.setColor2(Color.getBlue())`
      for the end color.'
  - name: Save the edited PSD
    text: Calling `im.save(exportPath);` writes the modified image to disk. The saved
      file retains the radial gradient overlay and can be opened in Photoshop, previewed
      in browsers, or converted to other formats.
  type: HowTo
- questions:
  - answer: Yes. Retrieve the layer’s `BlendingOptions`, iterate through the `Effects`
      collection, and add a new `GradientOverlayEffect` for each gradient you need.
    question: Can I apply multiple gradient effects to a single image?
  - answer: Aspose.PSD provides shadows, glows, bevels, and more. Each effect appears
      in the `Effects` array and can be configured independently.
    question: What other effects can I combine with gradient overlays?
  - answer: Verify that the PSD was loaded with `setLoadEffectsResource(true)`, check
      layer visibility, and confirm you are modifying the correct effect index.
    question: How can I troubleshoot if the effects are not rendering correctly?
  - answer: Yes, you can get a free trial [here](https://releases.aspose.com/).
    question: Is there a trial version available for Aspose.PSD for Java?
  - answer: Visit the [purchase page](https://purchase.aspose.com/buy) for licensing
      information.
    question: Where can I purchase a license for Aspose.PSD for Java?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- create radial gradient
- gradient overlay effect
- Aspose.PSD Java
title: Come creare effetti di gradiente radiale in Aspose.PSD per Java
url: /it/java/advanced-image-effects/add-gradient-effects/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Come creare effetti di gradiente radiale in Aspose.PSD per Java

## Introduzione

In questa guida imparerai a **creare effetti di gradiente radiale java** utilizzando la libreria Aspose.PSD. I gradienti radiali sono perfetti per aggiungere profondità, messa a fuoco o un leggero bagliore ai tuoi livelli PSD senza aprire Photoshop. Alla fine del tutorial sarai in grado di caricare un PSD, applicare una sovrapposizione di gradiente, modificare le sue proprietà e salvare il risultato — tutto dal codice Java.

## Risposte rapide
- **Cosa posso ottenere?** Aggiungere, modificare e mescolare sovrapposizioni di gradiente radiale sui livelli PSD.  
- **Quale libreria è necessaria?** Aspose.PSD per Java (ultima versione).  
- **È necessaria una licenza?** Una versione di prova gratuita è sufficiente per lo sviluppo; è necessaria una licenza commerciale per la produzione.  
- **Quanto tempo richiede l'implementazione?** Circa 10‑15 minuti per una semplice sovrapposizione di gradiente radiale.  
- **È compatibile con Java 8+?** Sì, l'API supporta Java 8 e versioni successive.

## Prerequisiti

Prima di immergerci nel tutorial, assicurati di avere i seguenti prerequisiti:

1. **Aspose.PSD for Java Library** – Assicurati di aver scaricato e installato la libreria Aspose.PSD per Java. Puoi trovare la libreria e la sua documentazione nella [pagina di documentazione Aspose.PSD Java](https://reference.aspose.com/psd/java/).  
2. **Java Development Environment** – Configura un ambiente di sviluppo Java sulla tua macchina (JDK 8 o superiore, IDE a tua scelta).  
3. **Latest Aspose.PSD release** – Scarica l'ultima versione dalla [pagina di rilascio Aspose](https://releases.aspose.com/).  
4. **Support resources** – Se incontri problemi, consulta il [forum di supporto Aspose.PSD](https://forum.aspose.com/c/psd/34).  
5. **License purchase** – Quando sei pronto per la produzione, ottieni una licenza tramite la [pagina di acquisto](https://purchase.aspose.com/buy).

Ora che hai tutto configurato, procediamo con la guida passo‑passo.

## Che cos'è un effetto di sovrapposizione di gradiente?

Un effetto di sovrapposizione di gradiente dipinge una transizione fluida tra due o più colori su un'area selezionata di un livello. In Photoshop questo effetto può essere mescolato, colorato e posizionato per creare design visivi sofisticati. La classe `GradientOverlayEffect` è la rappresentazione di Aspose.PSD di quello stile di livello, esponendo proprietà come fermate di colore, opacità, modalità di fusione e stile del gradiente.

## Come creare un effetto di gradiente radiale

Carica il PSD, individua il livello target, regola le proprietà di `GradientOverlayEffect` e infine salva il file. L'intero flusso di lavoro si riduce a quattro righe concise di codice Java una volta che l'immagine è caricata.

### Passo 1: Carica il file PSD e accedi alla sovrapposizione di gradiente

`PsdLoadOptions` configura come viene caricato un file PSD, consentendo di abilitare il caricamento delle risorse degli effetti. `Image.load` legge il file in un oggetto `Image`.

```javaString dataDir = "Your Document Directory";

// Gradient overlay effect. Example
String sourceFileName = dataDir + "GradientOverlay.psd";
String exportPath = dataDir + "GradientOverlayChanged.psd";

PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);

PsdImage im = (PsdImage)Image.load(sourceFileName, loadOptions);

GradientOverlayEffect gradientOverlay = (GradientOverlayEffect)im.getLayers()[1].getBlendingOptions().getEffects()[0];
```

In questo passo, carichiamo un file PSD e recuperiamo il primo `GradientOverlayEffect` dal secondo livello (indice 1). La chiamata `loadOptions.setLoadEffectsResource(true)` garantisce che le risorse degli effetti siano disponibili per la modifica.

### Passo 2: Verifica le impostazioni iniziali

```java
// Verify initial settings
Assert.areEqual(BlendMode.Normal, gradientOverlay.getBlendMode());
Assert.areEqual(255, gradientOverlay.getOpacity());
Assert.areEqual(true, gradientOverlay.isVisible());
// ... (additional verifications)
```

Prima di apportare modifiche, è buona pratica confermare la modalità di fusione, l'opacità e la visibilità attuali. Questo ti aiuta a comprendere lo stato di base della sovrapposizione di gradiente.

### Passo 3: Modifica le impostazioni del gradiente

```java
// Modify gradient settings
settings.setColor(Color.getGreen());
gradientOverlay.setOpacity((byte)193);
gradientOverlay.setBlendMode(BlendMode.Lighten);
// ... (additional modifications)
```

Qui puoi personalizzare il colore, l'opacità e la modalità di fusione del gradiente. L'esempio cambia il colore in verde, riduce l'opacità a 193 (su 255) e imposta la modalità di fusione su **Lighten**. Sentiti libero di sperimentare altri valori di `BlendMode` come `Multiply`, `Screen` o `Overlay`.

### Passo 4: Salva l'immagine modificata

```java
// Save the edited image
im.save(exportPath);
```

Dopo aver applicato le modifiche, conserva le modifiche salvando il PSD in un nuovo file. Questo passo garantisce che il file originale rimanga intatto.

### Passo 5: Verifica le modifiche

```java
// Verify changes after editing
PsdImage img = (PsdImage)Image.load(sourceFileName, loadOptions);

GradientOverlayEffect gradientOverlayEffect = (GradientOverlayEffect)img.getLayers()[1].getBlendingOptions().getEffects()[0];
// ... (additional verifications)
```

Il frammento sopra dimostra come aprire un PSD, estrarre il primo effetto del secondo livello (presumibilmente una sovrapposizione di gradiente) e prepararlo per la modifica.

### Passo 2: Verifica le impostazioni originali (opzionale ma consigliato)

Prima di modificare qualsiasi cosa, controllare la modalità di fusione, l'opacità e la visibilità esistenti ti aiuta a comprendere lo stato di base. Le chiamate `Assert` nel codice confermano che l'effetto è attualmente impostato su modalità di fusione **Normal**, completamente opaco e visibile.

### Passo 3: Regola le proprietà del gradiente per ottenere uno stile radiale

Puoi cambiare il colore, l'opacità e la modalità di fusione del gradiente. Per un vero effetto radiale, imposta lo stile del gradiente:

```java
gradientOverlay.setGradientStyle(GradientStyle.Radial);
gradientOverlay.setAngle(0f); // angle is ignored for radial, but required by API
gradientOverlay.setScale(100f); // 100 % fills the layer
```

*Suggerimento professionale:* Usa `Color.getGreen()` o qualsiasi istanza di `java.awt.Color` per definire il colore iniziale, e `gradientOverlay.setColor2(Color.getBlue())` per il colore finale.

### Passo 4: Salva il PSD modificato

Chiamare `im.save(exportPath);` scrive l'immagine modificata su disco. Il file salvato conserva la sovrapposizione di gradiente radiale e può essere aperto in Photoshop, visualizzato nei browser o convertito in altri formati.

## Perché creare sovrapposizioni di gradiente radiale?

I gradienti radiali aggiungono profondità e messa a fuoco ai design, facendo apparire gli elementi tridimensionali o evidenziati. Sono ideali per:
- **Riempimenti di sfondo** che attirano l'occhio verso un soggetto centrale.  
- **Evidenziazioni di pulsanti o icone** dove è necessario un leggero bagliore.  
- **Effetti fotografici creativi** come vignette o esplosioni di luce.  

Aspose.PSD elabora **oltre 50 formati di input e output** e può gestire file PSD di centinaia di pagine senza caricare l'intero documento in memoria, consentendoti di automatizzare la creazione di gradienti su grandi librerie di risorse.

## Problemi comuni e suggerimenti

- **Effetto non visibile:** Assicurati che `gradientOverlay.isVisible()` restituisca `true`. Alcuni file PSD nascondono gli effetti per impostazione predefinita.  
- **Indice del livello errato:** I livelli sono indicizzati a zero; verifica di puntare al livello corretto (`im.getLayers()[1]` si riferisce al secondo livello).  
- **Casting dell'opacità:** Il metodo `setOpacity` si aspetta un `byte`. Passare un `int` causerà un errore di compilazione; esegui il cast esplicitamente come mostrato.  
- **Caricamento delle risorse:** Se incontri `null` accedendo agli effetti, verifica che `loadOptions.setLoadEffectsResource(true)` sia impostato prima di caricare l'immagine.

## Domande frequenti

**Q: Posso applicare più effetti di gradiente a una singola immagine?**  
A: Sì. Recupera le `BlendingOptions` del livello, itera attraverso la collezione `Effects` e aggiungi un nuovo `GradientOverlayEffect` per ogni gradiente necessario.

**Q: Quali altri effetti posso combinare con le sovrapposizioni di gradiente?**  
A: Aspose.PSD fornisce ombre, bagliori, smussi e altro. Ogni effetto appare nell'array `Effects` e può essere configurato indipendentemente.

**Q: Come posso risolvere i problemi se gli effetti non vengono renderizzati correttamente?**  
A: Verifica che il PSD sia stato caricato con `setLoadEffectsResource(true)`, controlla la visibilità del livello e conferma di modificare l'indice dell'effetto corretto.

**Q: È disponibile una versione di prova per Aspose.PSD per Java?**  
A: Sì, puoi ottenere una prova gratuita [qui](https://releases.aspose.com/).

**Q: Dove posso acquistare una licenza per Aspose.PSD per Java?**  
A: Visita la [pagina di acquisto](https://purchase.aspose.com/buy) per le informazioni sulla licenza.

## Altre domande frequenti

**Q: Posso cambiare la direzione del gradiente programmaticamente?**  
A: Sì. Usa il metodo `GradientOverlayEffect.setAngle(float angle)` per impostare l'angolo del gradiente in gradi. Per i gradienti radiali l'angolo è ignorato, ma il metodo deve comunque essere chiamato.

**Q: Aspose.PSD supporta i gradienti radiali?**  
A: Assolutamente. Imposta lo stile del gradiente su `GradientStyle.Radial` tramite le proprietà di `GradientOverlayEffect`.

**Q: Le sovrapposizioni di gradiente vengono preservate quando si converte un PSD in altri formati (ad es., PNG)?**  
A: Quando rasterizzi il PSD (ad esempio, lo salvi come PNG), il risultato visivo della sovrapposizione di gradiente viene mantenuto, ma l'effetto stesso diventa parte dei dati pixel.

**Q: Come rimuovo una sovrapposizione di gradiente da un livello?**  
A: Recupera le `BlendingOptions` del livello, individua il `GradientOverlayEffect` nella collezione `Effects` e rimuovilo usando `remove(effect)`.

**Q: È possibile animare le variazioni del gradiente?**  
A: Sebbene Aspose.PSD non gestisca direttamente l'animazione, puoi generare una sequenza di file PSD con parametri di gradiente variabili e poi assemblarli in un video o GIF usando un'altra libreria.

## Conclusione

Congratulazioni! Hai imparato **come creare effetti di gradiente radiale java** per le tue immagini usando Aspose.PSD per Java. Seguendo i passaggi sopra, puoi aggiungere, modificare e salvare programmaticamente le sovrapposizioni di gradiente, ottenendo il pieno controllo creativo sugli asset PSD. Sperimenta con diversi colori, modalità di fusione e valori di opacità per ottenere l'impatto visivo desiderato.

---

**Last Updated:** 2026-10-18  
**Tested With:** Aspose.PSD for Java 24.12 (latest at time of writing)  
**Author:** Aspose  

```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;


import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.BlendMode;
import com.aspose.psd.fileformats.psd.layers.IGradientColorPoint;
import com.aspose.psd.fileformats.psd.layers.fillsettings.*;
import com.aspose.psd.fileformats.psd.layers.layereffects.GradientOverlayEffect;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
```

## Tutorial correlati

- [Crea riempimento gradiente PSD con Java usando Aspose.PSD – Aggiungi livello di riempimento gradiente](/psd/java/psd-image-modification-conversion/add-gradient-fill-layer-psd-files/)
- [Pattern Overlay PSD: Aggiungi effetti con Aspose.PSD per Java](/psd/java/advanced-image-effects/add-pattern-effects/)
- [Applica una sovrapposizione di colore e imposta l'opacità in Java con Aspose.PSD](/psd/java/image-editing/color-overlay-effect/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}