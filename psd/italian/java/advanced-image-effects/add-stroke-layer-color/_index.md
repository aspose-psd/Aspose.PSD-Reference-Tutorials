---
date: 2026-02-07
description: Scopri come cambiare il colore del tratto in un file PSD usando Aspose.PSD
  per Java. Segui questa guida passo passo per modificare il colore del livello di
  tratto, l'opacità e altro ancora.
linktitle: Add Stroke Layer Color
second_title: Aspose.PSD Java API
title: Come cambiare il colore del tratto in Aspose.PSD per Java
url: /it/java/advanced-image-effects/add-stroke-layer-color/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Come cambiare il colore del contorno in Aspose.PSD per Java

## Introduzione

Se hai bisogno di **come cambiare il colore del contorno** in un documento Photoshop programmaticamente, Aspose.PSD per Java lo rende semplice. In questo tutorial vedremo come aggiungere un livello di contorno, cambiarne il colore, regolare l'opacità e salvare il risultato. Alla fine vedrai anche come modificare il contorno di qualsiasi livello esistente, dandoti il pieno controllo creativo dal tuo codice Java.

## Risposte rapide
- **Quale libreria è necessaria?** Aspose.PSD for Java (ultima versione).  
- **Posso cambiare il colore del contorno?** Sì – usa `ColorFillSettings` per impostare qualsiasi `Color`.  
- **Ho bisogno di una licenza?** Una licenza temporanea è sufficiente per la valutazione; è necessaria una licenza completa per la produzione.  
- **Quale versione di Java è supportata?** Java 8 o superiore.  
- **Quanto tempo richiede l'implementazione?** Tipicamente meno di 10 minuti per una semplice modifica del contorno.

## Cos'è un livello di contorno in un PSD?
Un livello di contorno è un effetto vettoriale che disegna un contorno attorno al contenuto di un livello. Può essere personalizzato con colore, spessore, opacità e modalità di fusione. Modificare questo effetto programmaticamente consente branding automatizzato, elaborazione batch o generazione dinamica di grafiche.

## Perché usare Aspose.PSD per cambiare il colore del contorno?
- **Nessun Photoshop richiesto** – lavora interamente in Java.  
- **Conformità completa alle specifiche PSD** – tutte le funzionalità PSD moderne sono supportate.  
- **Alte prestazioni** – elabora rapidamente file di grandi dimensioni.  
- **Cross‑platform** – esegui su qualsiasi OS con una JVM.

## Come cambiare il colore del contorno programmaticamente
Di seguito è riportata una guida concisa, passo‑passo, che dimostra esattamente come cambiare il colore del contorno usando Aspose.PSD per Java. Ogni passaggio include una breve spiegazione seguita dal blocco di codice originale (invariato).

### Prerequisiti

- **Libreria Aspose.PSD** – scarica dalla [documentazione ufficiale](https://reference.aspose.com/psd/java/).  
- **Java Development Kit (JDK)** – versione 8 o successiva.  
- **IDE** – Eclipse, IntelliJ IDEA o qualsiasi editor compatibile con Java.

### Importa i pacchetti

Per prima cosa, importa le classi necessarie. Questo fornisce al tuo progetto l'accesso alle API di gestione PSD e agli effetti di contorno.

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

### Passo 1: Configura il tuo progetto

Crea un nuovo progetto Java, aggiungi il JAR di Aspose.PSD al percorso di compilazione e verifica che la libreria venga caricata senza errori.

### Passo 2: Carica il file PSD

Abilita il caricamento delle risorse degli effetti affinché le informazioni sul contorno siano disponibili.

```java
String dataDir = "Your Document Directory";

String sourceFileName = dataDir + "Stroke.psd";
String exportPath = dataDir + "StrokeGradientChanged.psd";

PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);

PsdImage im = (PsdImage)Image.load(sourceFileName, loadOptions);
```

### Passo 3: Accedi al livello di effetto contorno

Recupera il primo effetto di contorno dal secondo livello (indice 1).

```java
StrokeEffect colorStroke = (StrokeEffect)im.getLayers()[1].getBlendingOptions().getEffects()[0];
```

### Passo 4: Convalida le proprietà del contorno

Conferma le proprietà esistenti prima di apportare modifiche. Questo aiuta a evitare risultati inattesi.

```java
Assert.areEqual(BlendMode.Normal, colorStroke.getBlendMode());
Assert.areEqual(255, colorStroke.getOpacity());
Assert.areEqual(true, colorStroke.isVisible());
```

### Passo 5: Imposta colore e opacità (Come cambiare il colore del contorno)

Qui **cambiamo il colore del contorno** in giallo e riduciamo l'opacità al 50 % (127 / 255).

```java
ColorFillSettings fillSettings = (ColorFillSettings)colorStroke.getFillSettings();
fillSettings.setColor(Color.getYellow());

colorStroke.setOpacity((byte)127);
```

### Passo 6: Salva il PSD modificato

Scrivi l'immagine aggiornata su disco. Il nuovo file ora contiene il contorno modificato.

```java
im.save(exportPath);
```

## Casi d'uso comuni per cambiare il colore del contorno
- **Automazione del branding:** Applica un colore aziendale ai loghi su centinaia di asset PSD in un'unica esecuzione batch.  
- **Generazione dinamica di UI:** Cambia i colori del contorno al volo in base ai temi selezionati dall'utente in uno strumento di design basato sul web.  
- **Preparazione pre‑flight:** Assicura che tutti i colori del contorno soddisfino le specifiche di stampa prima di inviare i file alla tipografia.

## Problemi comuni e consigli

- **Controlli null** – verifica sempre che `getEffects()` restituisca un array non nullo prima del cast.  
- **Indice del livello** – i livelli PSD partono da zero; assicurati di puntare al livello corretto.  
- **Formato colore** – `Color.getYellow()` è solo un esempio; puoi creare colori personalizzati con `new Color(r, g, b)`.  
- **Intervallo opacità** – l'opacità è un byte (0–255); i valori superiori a 255 verranno limitati.  
- **Caricamento risorse** – dimenticare `loadOptions.setLoadEffectsResource(true)` produrrà un array di effetti `null`.

## Domande frequenti

**D: Posso usare Aspose.PSD con altre librerie grafiche Java?**  
R: Sì, Aspose.PSD può essere combinato con librerie come Apache Commons Imaging o Java2D per funzionalità estese.

**D: Aspose.PSD è compatibile con il formato PSD più recente?**  
R: Assolutamente. La libreria viene aggiornata regolarmente per supportare le ultime specifiche di Photoshop.

**D: Come gestisco le eccezioni usando Aspose.PSD?**  
R: Consulta il [forum di supporto](https://forum.aspose.com/c/psd/34) per una risoluzione dettagliata dei problemi e esempi di codice di gestione degli errori.

**D: Posso provare Aspose.PSD prima di acquistarlo?**  
R: Certamente! Scarica una [prova gratuita](https://releases.aspose.com/) per esplorare tutte le funzionalità.

**D: Dove posso ottenere una licenza temporanea per Aspose.PSD?**  
R: Ottieni una [licenza temporanea](https://purchase.aspose.com/temporary-license/) per valutare la libreria nel tuo ambiente di sviluppo.

---

**Ultimo aggiornamento:** 2026-02-07  
**Testato con:** Aspose.PSD 24.11 for Java  
**Autore:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}