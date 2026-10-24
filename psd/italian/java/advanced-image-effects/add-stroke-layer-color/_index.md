---
date: 2026-10-24
description: Scopri come creare un livello di contorno Java con Aspose.PSD per Java.
  Questa guida passo‑passo ti mostra come aggiungere un livello di contorno, cambiarne
  il colore, regolare l'opacità e salvare il PSD.
keywords:
- create stroke layer java
- change stroke color java
- modify stroke opacity
- apply stroke effect
- psd stroke tutorial
lastmod: 2026-10-24
linktitle: Aggiungi colore al livello di contorno
og_description: Crea livello di contorno java usando Aspose.PSD per Java. Segui questo
  tutorial conciso per aggiungere un livello di contorno, cambiarne il colore, regolare
  l'opacità ed esportare il file PSD.
og_image_alt: Screenshot of a Java IDE showing Aspose.PSD code that creates and modifies
  a stroke layer in a PSD file
og_title: Crea livello di contorno java con Aspose.PSD – Guida rapida
schemas:
- author: Aspose
  dateModified: '2026-10-24'
  description: Learn how to create stroke layer Java with Aspose.PSD for Java. This
    step‑by‑step guide shows you how to add a stroke layer, change its color, adjust
    opacity, and save the PSD.
  headline: How to create stroke layer Java using Aspose.PSD
  type: TechArticle
- description: Learn how to create stroke layer Java with Aspose.PSD for Java. This
    step‑by‑step guide shows you how to add a stroke layer, change its color, adjust
    opacity, and save the PSD.
  name: How to create stroke layer Java using Aspose.PSD
  steps:
  - name: set up your project
    text: Create a new Java project, add the Aspose.PSD JAR to the build path, and
      verify the library loads without errors.
  - name: load the PSD file
    text: Enable loading of effect resources so the stroke information is available.
  - name: access the stroke effect layer
    text: '`StrokeEffect` is Aspose.PSD’s class that represents a vector outline applied
      to a layer. Retrieve the first stroke effect from the second layer (index 1).'
  - name: validate stroke properties
    text: '`ColorFillSettings` holds the color and opacity values for a stroke. Confirm
      the existing properties before making changes to avoid unexpected results.'
  - name: set color and opacity (how to change stroke color)
    text: Here we **change stroke color** to yellow and reduce opacity to 50 % (127
      / 255). `ColorFillSettings` also lets you specify blend mode and size.
  - name: save the modified PSD
    text: Write the updated image back to disk. The new file now contains the modified
      stroke.
  type: HowTo
- questions:
  - answer: Yes, Aspose.PSD can be combined with libraries such as Apache Commons
      Imaging or Java2D for extended functionality.
    question: Can I use Aspose.PSD with other Java graphic libraries?
  - answer: Absolutely. The library supports the newest Photoshop specifications and
      over 150 PSD features.
    question: Is Aspose.PSD compatible with the latest PSD file format?
  - answer: Wrap your code in try‑catch blocks and consult the [support forum](https://forum.aspose.com/c/psd/34)
      for detailed troubleshooting examples.
    question: How do I handle exceptions while using Aspose.PSD?
  - answer: Certainly! Grab a [free trial](https://releases.aspose.com/) to explore
      all features.
    question: Can I try Aspose.PSD before purchasing?
  - answer: Obtain a [temporary license](https://purchase.aspose.com/temporary-license/)
      to evaluate the library in your development environment.
    question: Where can I get a temporary license for Aspose.PSD?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- create stroke layer
- Aspose.PSD
- Java image processing
title: Come creare un livello di contorno Java con Aspose.PSD
url: /it/java/advanced-image-effects/add-stroke-layer-color/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Come creare un livello di contorno Java usando Aspose.PSD

## Introduzione

Se hai bisogno di **creare stroke layer Java** in un documento Photoshop in modo programmatico, Aspose.PSD per Java ti offre un approccio pulito, code‑first. In questo tutorial imparerai come aggiungere un nuovo livello di contorno, cambiarne il colore, regolare l'opacità e salvare il risultato—tutto senza avviare Photoshop. Alla fine saprai anche come modificare il contorno di un livello esistente, dandoti il pieno controllo creativo direttamente dalla tua applicazione Java.

## Risposte rapide
- **Quale libreria è necessaria?** Aspose.PSD for Java (latest version).  
- **Posso cambiare il colore del contorno?** Sì – usa `ColorFillSettings` per impostare qualsiasi `Color`.  
- **Ho bisogno di una licenza?** Una licenza temporanea funziona per la valutazione; è necessaria una licenza completa per la produzione.  
- **Quale versione di Java è supportata?** Java 8 o superiore.  
- **Quanto tempo richiede l'implementazione?** Tipicamente meno di 10 minuti per una modifica di base del contorno.

## Cos'è un livello di contorno in un PSD?
Un livello di contorno è un effetto vettoriale che disegna un contorno attorno al contenuto di un livello. Può essere personalizzato con colore, spessore, opacità e modalità di fusione. Modificare questo effetto programmaticamente consente branding automatizzato, elaborazione batch o generazione dinamica di grafica.

## Perché usare Aspose.PSD per cambiare il colore del contorno?
Aspose.PSD supporta **150+** funzionalità PSD—incluse maschere vettoriali, oggetti intelligenti e effetti di livello—mentre elabora file con centinaia di pagine senza caricare l'intero documento in memoria. La libreria funziona su qualsiasi OS con una JVM, offre prestazioni inferiori al secondo per le risorse tipiche e non richiede l'installazione di Photoshop.

## Come creare un livello di contorno Java?

Carica il PSD, aggiungi un effetto di contorno, configura il suo aspetto e salva il file—tutto in poche righe semplici. La risposta qui sotto ti indica esattamente cosa fare prima di immergerci nella guida passo‑passo.

**Risposta diretta (40‑70 parole):**  
`PsdImage` rappresenta un documento PSD e fornisce metodi per caricare e salvare file. Inizia caricando il tuo PSD con `PsdImage.load("input.psd", loadOptions)`. Crea un nuovo `StrokeEffect`, imposta il suo `ColorFillSettings` al `Color` desiderato, regola opacità e dimensione, quindi collega l'effetto alle `BlendingOptions` del livello di destinazione. Infine, chiama `psd.save("output.psd", SaveFormat.PSD)`. Questa sequenza crea un livello di contorno in Java con Aspose.PSD.

### Prerequisiti

- **Libreria Aspose.PSD** – scarica dalla [documentazione ufficiale](https://reference.aspose.com/psd/java/).  
- **Java Development Kit (JDK)** – versione 8 o più recente.  
- **IDE** – Eclipse, IntelliJ IDEA, o qualsiasi editor compatibile con Java.

### Importa pacchetti

Per prima cosa, importa le classi di cui avrai bisogno. Questo fornisce al tuo progetto l'accesso alla gestione PSD e alle API per gli effetti di contorno.

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

### Passo 1: configura il tuo progetto

Crea un nuovo progetto Java, aggiungi il JAR di Aspose.PSD al percorso di compilazione e verifica che la libreria venga caricata senza errori.

### Passo 2: carica il file PSD

Abilita il caricamento delle risorse degli effetti in modo che le informazioni del contorno siano disponibili.

```java
String dataDir = "Your Document Directory";

String sourceFileName = dataDir + "Stroke.psd";
String exportPath = dataDir + "StrokeGradientChanged.psd";

PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);

PsdImage im = (PsdImage)Image.load(sourceFileName, loadOptions);
```

### Passo 3: accedi al livello dell'effetto di contorno

`StrokeEffect` è la classe di Aspose.PSD che rappresenta un contorno vettoriale applicato a un livello. Recupera il primo effetto di contorno dal secondo livello (indice 1).

```java
StrokeEffect colorStroke = (StrokeEffect)im.getLayers()[1].getBlendingOptions().getEffects()[0];
```

### Passo 4: valida le proprietà del contorno

`ColorFillSettings` contiene i valori di colore e opacità per un contorno. Conferma le proprietà esistenti prima di apportare modifiche per evitare risultati inattesi.

```java
Assert.areEqual(BlendMode.Normal, colorStroke.getBlendMode());
Assert.areEqual(255, colorStroke.getOpacity());
Assert.areEqual(true, colorStroke.isVisible());
```

### Passo 5: imposta colore e opacità (come cambiare il colore del contorno)

Qui **cambiamo il colore del contorno** in giallo e riduciamo l'opacità al 50 % (127 / 255). `ColorFillSettings` consente anche di specificare la modalità di fusione e la dimensione.

```java
ColorFillSettings fillSettings = (ColorFillSettings)colorStroke.getFillSettings();
fillSettings.setColor(Color.getYellow());

colorStroke.setOpacity((byte)127);
```

### Passo 6: salva il PSD modificato

Scrivi l'immagine aggiornata su disco. Il nuovo file ora contiene il contorno modificato.

```java
im.save(exportPath);
```

## Come cambiare il colore del contorno Java?

`Color` rappresenta un valore di colore ARGB. Carica il tuo PSD, individua il livello di destinazione, aggiorna il `ColorFillSettings` con un nuovo `Color` e salva il file. Questa operazione richiede solo poche righe di codice e si completa in meno di un secondo per le risorse tipiche, rendendola veloce ed efficiente.

**Risposta diretta (40‑70 parole):**  
Usa `layer.getEffects().getStrokeEffect()` per ottenere il contorno esistente, chiama `stroke.getColorFillSettings().setColor(Color.getRed())` (o qualsiasi `Color` ti serva), opzionalmente regola `setOpacity((byte)200)` per un'opacità del 78 %, quindi salva il PSD con `psd.save("output.psd", SaveFormat.PSD)`. La modifica viene applicata istantaneamente senza dover rieseguire il rendering dell'intero documento.

## Come modificare l'opacità del contorno?

Se devi solo regolare l'opacità mantenendo il colore originale, modifica il valore `setOpacity` (0‑255) su `ColorFillSettings`. Ad esempio, `colorStroke.setOpacity((byte)200);` renderà il contorno circa al 78 % opaco. Regolare l'opacità ti consente di creare contorni sottili o completamente solidi, a seconda dei requisiti del tuo design.

**Risposta diretta (40‑70 parole):**  
Recupera il `StrokeEffect` dal livello desiderato, quindi chiama `stroke.getColorFillSettings().setOpacity((byte)desiredValue)`, dove `desiredValue` varia da 0 (trasparente) a 255 (completamente opaco). Salva il PSD e la nuova opacità sarà riflessa immediatamente. Questo approccio funziona per qualsiasi contorno esistente, indipendentemente dal colore originale.

## Come applicare l'effetto di contorno?

Per aggiungere un nuovo effetto di contorno a un livello che non ne ha già uno, crea un'istanza `StrokeEffect`, configura il suo `ColorFillSettings` e collegalo alle `BlendingOptions` del livello. Gli stessi metodi `setColor` e `setOpacity` vengono usati per definire l'aspetto complessivo.

**Risposta diretta (40‑70 parole):**  
Istanzia `StrokeEffect newStroke = new StrokeEffect(); newStroke.getColorFillSettings().setColor(Color.getBlue()); newStroke.getColorFillSettings().setOpacity((byte)255); layer.getBlendingOptions().setEffect(newStroke);`. Dopo aver collegato l'effetto, salva il PSD. Questo aggiunge un nuovo livello di contorno completamente personalizzabile a qualsiasi livello esistente nel tuo documento.

## Casi d'uso comuni per cambiare il colore del contorno
- **Automazione del branding:** Applica un colore aziendale ai loghi su centinaia di asset PSD in un'unica esecuzione batch.  
- **Generazione dinamica di UI:** Cambia i colori del contorno al volo in base ai temi selezionati dall'utente in uno strumento di design basato sul web.  
- **Preparazione pre‑flight:** Assicura che tutti i colori del contorno soddisfino le specifiche di stampa prima di inviare i file alla tipografia.

## Problemi comuni e consigli

- **Controlli null** – verifica sempre che `getEffects()` restituisca un array non null prima del cast.  
- **Indice del livello** – i livelli PSD partono da zero; assicurati di puntare al livello corretto.  
- **Formato colore** – `Color.getYellow()` è solo un esempio; puoi creare colori personalizzati con `new Color(r, g, b)`.  
- **Intervallo opacità** – l'opacità è un byte (0–255); valori superiori a 255 verranno limitati.  
- **Caricamento risorse** – dimenticare `loadOptions.setLoadEffectsResource(true)` porterà a un array di effetti `null`.

## Domande frequenti

**Q: Posso usare Aspose.PSD con altre librerie grafiche Java?**  
A: Sì, Aspose.PSD può essere combinato con librerie come Apache Commons Imaging o Java2D per funzionalità estese.

**Q: Aspose.PSD è compatibile con l'ultimo formato file PSD?**  
A: Assolutamente. La libreria supporta le più recenti specifiche Photoshop e oltre 150 funzionalità PSD.

**Q: Come gestisco le eccezioni usando Aspose.PSD?**  
A: Avvolgi il tuo codice in blocchi try‑catch e consulta il [forum di supporto](https://forum.aspose.com/c/psd/34) per esempi dettagliati di risoluzione dei problemi.

**Q: Posso provare Aspose.PSD prima di acquistarlo?**  
A: Certamente! Ottieni una [prova gratuita](https://releases.aspose.com/) per esplorare tutte le funzionalità.

**Q: Dove posso ottenere una licenza temporanea per Aspose.PSD?**  
A: Ottieni una [licenza temporanea](https://purchase.aspose.com/temporary-license/) per valutare la libreria nel tuo ambiente di sviluppo.

---

**Ultimo aggiornamento:** 2026-10-24  
**Testato con:** Aspose.PSD 24.11 for Java  
**Autore:** Aspose

## Tutorial correlati

- [Come cambiare il colore del contorno Java usando Aspose.PSD](/psd/java/advanced-image-effects/add-stroke-layer-color/)
- [Come aggiungere l'ombra in PSD usando Java – Effetti avanzati di livello](/psd/java/advanced-psd-layer-features-effects/)
- [Pattern Overlay PSD: aggiungi effetti con Aspose.PSD per Java](/psd/java/advanced-image-effects/add-pattern-effects/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}