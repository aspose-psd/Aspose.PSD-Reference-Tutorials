---
date: 2026-04-22
description: Scopri come cambiare il colore del tratto in Java con Aspose.PSD per
  Java. Segui questa guida passo passo per modificare il colore del livello di tratto,
  l'opacità e altro.
keywords:
- change stroke color java
- modify stroke opacity
- apply stroke effect
- psd stroke tutorial
- add stroke layer psd
linktitle: Aggiungi colore al livello di contorno
second_title: Aspose.PSD Java API
title: Come cambiare il colore del tratto in Java usando Aspose.PSD
url: /it/java/advanced-image-effects/add-stroke-layer-color/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Come modificare il colore del tratto in Java usando Aspose.PSD

## Introduzione

Se hai bisogno di **cambiare il colore del tratto in Java** in un documento Photoshop in modo programmatico, Aspose.PSD per Java lo rende semplice. In questo tutorial vedremo come aggiungere un livello di tratto, cambiarne il colore, regolare l'opacità e salvare il risultato. Alla fine vedrai anche come modificare il tratto di qualsiasi livello esistente, offrendoti il pieno controllo creativo dal tuo codice Java.

## Risposte rapide
- **Quale libreria è necessaria?** Aspose.PSD per Java (ultima versione).  
- **Posso cambiare il colore del tratto?** Sì – usa `ColorFillSettings` per impostare qualsiasi `Color`.  
- **Ho bisogno di una licenza?** Una licenza temporanea funziona per la valutazione; è necessaria una licenza completa per la produzione.  
- **Quale versione di Java è supportata?** Java 8 o superiore.  
- **Quanto tempo richiede l'implementazione?** Tipicamente meno di 10 minuti per una modifica di base del tratto.

## Cos'è un livello di tratto in un PSD?
Un livello di tratto è un effetto vettoriale che disegna un contorno attorno al contenuto di un livello. Può essere personalizzato con colore, spessore, opacità e modalità di fusione. Modificare questo effetto programmaticamente consente branding automatizzato, elaborazione batch o generazione dinamica di grafica.

## Perché usare Aspose.PSD per cambiare il colore del tratto?
- **Nessun Photoshop richiesto** – lavora interamente in Java.  
- **Conformità completa alla specifica PSD** – tutte le funzionalità PSD moderne sono supportate.  
- **Alte prestazioni** – elabora rapidamente file di grandi dimensioni.  
- **Cross‑platform** – esegui su qualsiasi OS con una JVM.

## Come modificare il colore del tratto in Java programmaticamente
Di seguito trovi una guida concisa, passo‑a‑passo, che dimostra esattamente come cambiare il colore del tratto usando Aspose.PSD per Java. Ogni passo include una breve spiegazione seguita dal blocco di codice originale (invariato).

### Prerequisiti

- **Libreria Aspose.PSD** – scarica dalla [documentazione ufficiale](https://reference.aspose.com/psd/java/).  
- **Java Development Kit (JDK)** – versione 8 o successiva.  
- **IDE** – Eclipse, IntelliJ IDEA o qualsiasi editor compatibile con Java.

### Importare i pacchetti

First, import the classes you’ll need. This gives your project access to the PSD handling and stroke‑effect APIs.

```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;


import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.BlendMode;
import com.aspose.psd.fileformats.psd.layers.fillsettings.ColorFillSettings;
import com.aspose.psd.fileformats.psd.layers.fillsettings.FillType;
import com.aspose.psd.fileformats.psd.layers.layereffects.StrokeEffect;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
```

### Passo 1: Configurare il progetto

Create a new Java project, add the Aspose.PSD JAR to the build path, and verify the library loads without errors.

### Passo 2: Caricare il file PSD

Enable loading of effect resources so the stroke information is available.

```java
String dataDir = "Your Document Directory";

String sourceFileName = dataDir + "Stroke.psd";
String exportPath = dataDir + "StrokeGradientChanged.psd";

PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);

PsdImage im = (PsdImage)Image.load(sourceFileName, loadOptions);
```

### Passo 3: Accedere al livello di effetto tratto

Retrieve the first stroke effect from the second layer (index 1).

```java
StrokeEffect colorStroke = (StrokeEffect)im.getLayers()[1].getBlendingOptions().getEffects()[0];
```

### Passo 4: Convalidare le proprietà del tratto

Confirm the existing properties before making changes. This helps avoid unexpected results.

```java
Assert.areEqual(BlendMode.Normal, colorStroke.getBlendMode());
Assert.areEqual(255, colorStroke.getOpacity());
Assert.areEqual(true, colorStroke.isVisible());
```

### Passo 5: Impostare colore e opacità (Come cambiare il colore del tratto)

Qui **cambiamo il colore del tratto** in giallo e riduciamo l'opacità al 50 % (127 / 255).

```java
ColorFillSettings fillSettings = (ColorFillSettings)colorStroke.getFillSettings();
fillSettings.setColor(Color.getYellow());

colorStroke.setOpacity((byte)127);
```

### Passo 6: Salvare il PSD modificato

Write the updated image back to disk. The new file now contains the modified stroke.

```java
im.save(exportPath);
```

## Come modificare l'opacità del tratto

Se devi solo regolare l'opacità mantenendo il colore originale, modifica il valore di `setOpacity` (0‑255). Ad esempio, `colorStroke.setOpacity((byte)200);` renderà il tratto circa il 78 % opaco.

## Come applicare l'effetto tratto

Per aggiungere un nuovo effetto di tratto a un livello che non ne ha già uno, crea un'istanza `StrokeEffect`, configura il suo `ColorFillSettings` e collegalo alle `BlendingOptions` del livello. Gli stessi metodi `setColor` e `setOpacity` sono usati per definire l'aspetto.

## Tutorial sul tratto PSD: aggiungere un livello di tratto al PSD

I passaggi sopra illustrano come aggiungere un tratto a un livello esistente. Per creare un nuovo livello di tratto, duplica il livello di destinazione, quindi applica il `StrokeEffect`. Questo approccio è utile quando vuoi mantenere intatto il livello originale.

## Casi d'uso comuni per cambiare il colore del tratto
- **Automazione del branding:** Applica un colore aziendale ai loghi su centinaia di asset PSD in un'unica esecuzione batch.  
- **Generazione dinamica di UI:** Cambia i colori del tratto al volo in base ai temi selezionati dall'utente in uno strumento di design basato sul web.  
- **Preparazione pre‑flight:** Assicurati che tutti i colori del tratto soddisfino le specifiche di stampa prima di inviare i file alla tipografia.

## Errori comuni e suggerimenti

- **Controlli null** – verifica sempre che `getEffects()` restituisca un array non nullo prima del cast.  
- **Indice del livello** – i livelli PSD sono indicizzati da zero; assicurati di puntare al livello corretto.  
- **Formato colore** – `Color.getYellow()` è solo un esempio; puoi creare colori personalizzati con `new Color(r, g, b)`.  
- **Intervallo di opacità** – l'opacità è un byte (0–255); i valori superiori a 255 verranno limitati.  
- **Caricamento risorse** – dimenticare `loadOptions.setLoadEffectsResource(true)` produrrà un array di effetti `null`.

## Domande frequenti

**D: Posso usare Aspose.PSD con altre librerie grafiche Java?**  
R: Sì, Aspose.PSD può essere combinato con librerie come Apache Commons Imaging o Java2D per funzionalità estese.

**D: Aspose.PSD è compatibile con l'ultimo formato di file PSD?**  
R: Assolutamente. La libreria è regolarmente aggiornata per supportare le più recenti specifiche di Photoshop.

**D: Come gestisco le eccezioni usando Aspose.PSD?**  
R: Consulta il [forum di supporto](https://forum.aspose.com/c/psd/34) per una risoluzione dettagliata dei problemi e esempi di codice per la gestione degli errori.

**D: Posso provare Aspose.PSD prima di acquistarlo?**  
R: Certamente! Scarica una [prova gratuita](https://releases.aspose.com/) per esplorare tutte le funzionalità.

**D: Dove posso ottenere una licenza temporanea per Aspose.PSD?**  
R: Ottieni una [licenza temporanea](https://purchase.aspose.com/temporary-license/) per valutare la libreria nel tuo ambiente di sviluppo.

**Ultimo aggiornamento:** 2026-04-22  
**Testato con:** Aspose.PSD 24.11 per Java  
**Autore:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}