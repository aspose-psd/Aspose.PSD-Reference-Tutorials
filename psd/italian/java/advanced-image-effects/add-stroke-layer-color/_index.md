---
date: 2025-11-30
description: Scopri come aggiungere il tratto e modificare il colore del tratto PSD
  usando Aspose.PSD per Java. Segui questa guida passo passo per modificare il colore
  e l'opacità del livello del tratto.
linktitle: Add Stroke Layer Color
second_title: Aspose.PSD Java API
title: Come aggiungere il colore del contorno del livello in Aspose.PSD per Java
url: /it/java/advanced-image-effects/add-stroke-layer-color/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Come aggiungere il colore del livello di contorno in Aspose.PSD per Java

## Introduzione

Se hai bisogno di **come aggiungere un contorno** a un documento Photoshop in modo programmatico, Aspose.PSD per Java lo rende semplice. In questo tutorial vedremo come aggiungere il colore di un livello di contorno, regolare la sua opacità e salvare il risultato. Alla fine vedrai anche come **come cambiare il colore del contorno** (o *cambiare il colore del contorno PSD*) per qualsiasi livello esistente, offrendoti il pieno controllo creativo dal tuo codice Java.

## Risposte rapide
- **Quale libreria è necessaria?** Aspose.PSD per Java (ultima versione).  
- **Posso cambiare il colore del contorno?** Sì – usa `ColorFillSettings` per impostare qualsiasi `Color`.  
- **È necessaria una licenza?** Una licenza temporanea funziona per la valutazione; è necessaria una licenza completa per la produzione.  
- **Quale versione di Java è supportata?** Java 8 o superiore.  
- **Quanto tempo richiede l'implementazione?** Tipicamente meno di 10 minuti per una modifica di base del contorno.

## Che cos'è un livello di contorno in un PSD?
Un livello di contorno è un effetto vettoriale che disegna un contorno attorno al contenuto di un livello. Può essere personalizzato con colore, spessore, opacità e modalità di fusione. Modificare questo effetto programmaticamente consente di automatizzare branding, elaborazione batch o generazione dinamica di grafiche.

## Perché usare Aspose.PSD per cambiare il colore del contorno?
- **Nessun Photoshop necessario** – lavora interamente in Java.  
- **Piena conformità alle specifiche PSD** – tutte le funzionalità PSD moderne sono supportate.  
- **Alte prestazioni** – elabora file di grandi dimensioni rapidamente.  
- **Cross‑platform** – funziona su qualsiasi OS con una JVM.

## Prerequisiti

- **Libreria Aspose.PSD** – scaricala dalla [documentazione ufficiale](https://reference.aspose.com/psd/java/).  
- **Java Development Kit (JDK)** – versione 8 o successiva.  
- **IDE** – Eclipse, IntelliJ IDEA o qualsiasi editor compatibile con Java.

## Importare i pacchetti

Per prima cosa, importa le classi di cui avrai bisogno. Questo dà al tuo progetto l'accesso alla gestione PSD e alle API degli effetti di contorno.

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

## Passo 1: Configura il tuo progetto

Crea un nuovo progetto Java, aggiungi il JAR di Aspose.PSD al percorso di compilazione e verifica che la libreria venga caricata senza errori.

## Passo 2: Carica il file PSD

Abilita il caricamento delle risorse di effetto in modo che le informazioni sul contorno siano disponibili.

```java
String dataDir = "Your Document Directory";

String sourceFileName = dataDir + "Stroke.psd";
String exportPath = dataDir + "StrokeGradientChanged.psd";

PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);

PsdImage im = (PsdImage)Image.load(sourceFileName, loadOptions);
```

## Passo 3: Accedi al livello di effetto contorno

Recupera il primo effetto di contorno dal secondo livello (indice 1).

```java
StrokeEffect colorStroke = (StrokeEffect)im.getLayers()[1].getBlendingOptions().getEffects()[0];
```

## Passo 4: Convalida le proprietà del contorno

Conferma le proprietà esistenti prima di apportare modifiche. Questo aiuta a evitare risultati inattesi.

```java
Assert.areEqual(BlendMode.Normal, colorStroke.getBlendMode());
Assert.areEqual(255, colorStroke.getOpacity());
Assert.areEqual(true, colorStroke.isVisible());
```

## Passo 5: Imposta colore e opacità (Come cambiare il colore del contorno)

Qui **cambiamo il colore del contorno PSD** in giallo e riduciamo l'opacità al 50 % (127 / 255).

```java
ColorFillSettings fillSettings = (ColorFillSettings)colorStroke.getFillSettings();
fillSettings.setColor(Color.getYellow());

colorStroke.setOpacity((byte)127);
```

## Passo 6: Salva il PSD modificato

Scrivi l'immagine aggiornata su disco. Il nuovo file contiene ora il contorno modificato.

```java
im.save(exportPath);
```

## Problemi comuni e consigli

- **Controlli null** – verifica sempre che `getEffects()` restituisca un array non nullo prima del cast.  
- **Indice del livello** – i livelli PSD sono indicizzati a zero; assicurati di puntare al livello corretto.  
- **Formato colore** – `Color.getYellow()` è solo un esempio; puoi creare colori personalizzati con `new Color(r, g, b)`.  
- **Intervallo opacità** – l'opacità è un byte (0–255); i valori superiori a 255 verranno limitati.

## Conclusione

Ora hai imparato **come aggiungere un contorno** a un file PSD e **come cambiare il colore del contorno** usando Aspose.PSD per Java. Sperimenta con diversi colori, modalità di fusione e opacità per ottenere lo stile visivo esatto di cui il tuo progetto ha bisogno.

## Domande frequenti

**D: Posso usare Aspose.PSD con altre librerie grafiche Java?**  
R: Sì, Aspose.PSD può essere combinato con librerie come Apache Commons Imaging o Java2D per funzionalità estese.

**D: Aspose.PSD è compatibile con l'ultimo formato di file PSD?**  
R: Assolutamente. La libreria è regolarmente aggiornata per supportare le più recenti specifiche di Photoshop.

**D: Come gestisco le eccezioni usando Aspose.PSD?**  
R: Consulta il [forum di supporto](https://forum.aspose.com/c/psd/34) per una risoluzione dettagliata dei problemi e esempi di codice per la gestione degli errori.

**D: Posso provare Aspose.PSD prima di acquistarlo?**  
R: Certamente! Ottieni una [prova gratuita](https://releases.aspose.com/) per esplorare tutte le funzionalità.

**D: Dove posso ottenere una licenza temporanea per Aspose.PSD?**  
R: Ottieni una [licenza temporanea](https://purchase.aspose.com/temporary-license/) per valutare la libreria nel tuo ambiente di sviluppo.

---

**Ultimo aggiornamento:** 2025-11-30  
**Testato con:** Aspose.PSD 24.11 per Java  
**Autore:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}