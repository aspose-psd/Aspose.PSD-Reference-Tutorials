---
date: 2026-09-28
description: Scopri come esportare PSD in PNG impostando la modalità colore PSD a
  scala di grigi a 16 bit usando Aspose.PSD per Java. Guida passo‑passo con esempi
  di codice.
keywords:
- export psd as png
- how to convert psd to png
- 16-bit grayscale java
lastmod: 2026-09-28
linktitle: Esporta PSD in PNG – Scala di grigi a 16 bit – Java
og_description: Esporta PSD in PNG con scala di grigi a 16 bit usando Aspose.PSD per
  Java. Segui questo tutorial passo‑passo per preservare 65.536 tonalità di grigio.
og_image_alt: Guide showing how to export PSD as PNG with 16-bit grayscale using Aspose.PSD
  Java
og_title: Esporta PSD in PNG con scala di grigi a 16 bit in Java – Guida Aspose.PSD
schemas:
- author: Aspose
  dateModified: '2026-09-28'
  description: Learn how to export PSD as PNG while setting PSD color mode to 16-bit
    grayscale using Aspose.PSD for Java. Step‑by‑step guide with code examples.
  headline: How to export PSD as PNG with 16‑bit grayscale color mode in Java
  type: TechArticle
- description: Learn how to export PSD as PNG while setting PSD color mode to 16-bit
    grayscale using Aspose.PSD for Java. Step‑by‑step guide with code examples.
  name: How to export PSD as PNG with 16‑bit grayscale color mode in Java
  steps:
  - name: '**Java Development Kit (JDK)** – Install the latest JDK from [Oracle''s
      site](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).'
    text: '**Java Development Kit (JDK)** – Install the latest JDK from [Oracle''s
      site](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).'
  - name: '**Aspose.PSD for Java library** – Download the JAR from the [Aspose download
      page](https://releases.aspose.com/psd/java/).'
    text: '**Aspose.PSD for Java library** – Download the JAR from the [Aspose download
      page](https://releases.aspose.com/psd/java/).'
  - name: '**An IDE** – IntelliJ IDEA, Eclipse, or Visual Studio Code works perfectly.'
    text: '**An IDE** – IntelliJ IDEA, Eclipse, or Visual Studio Code works perfectly.'
  - name: '**Basic Java knowledge** – You should be comfortable creating classes,
      handling exceptions, and working with file paths.'
    text: '**Basic Java knowledge** – You should be comfortable creating classes,
      handling exceptions, and working with file paths.'
  - name: '**A sample PSD file** – Create one in Adobe Photoshop or grab a free sample
      online.'
    text: '**A sample PSD file** – Create one in Adobe Photoshop or grab a free sample
      online.'
  type: HowTo
- questions:
  - answer: It provides 65 536 shades of gray, delivering far more tonal detail than
      the standard 8‑bit (256 shades).
    question: What is 16‑bit grayscale color mode?
  - answer: Absolutely! Aspose.PSD supports RGB, CMYK, Lab, Indexed, and many other
      color modes.
    question: Can I use Aspose.PSD for non‑grayscale images?
  - answer: Yes, you can try a free trial version of Aspose.PSD. Just head to the
      [Aspose download page](https://releases.aspose.com/).
    question: Is there a trial version of Aspose.PSD?
  - answer: Check the official [documentation](https://reference.aspose.com/psd/java/)
      for in‑depth tutorials, API references, and sample projects.
    question: Where can I find more Aspose.PSD examples?
  - answer: You can buy a license by visiting the [Aspose purchase page](https://purchase.aspose.com/buy).
    question: How do I purchase a license for Aspose.PSD?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- convert psd
- Aspose.PSD
- Java image processing
title: Come esportare PSD in PNG con modalità colore in scala di grigi a 16 bit in
  Java
url: /it/java/advanced-psd-layer-features-effects/support-16-bit-grayscale-color-mode-psd/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Esporta PSD come PNG con modalità colore in scala di grigi a 16‑bit in Java

## Introduzione
Esportare PSD come PNG mantenendo una modalità colore in scala di grigi a 16‑bit ti offre la profondità di una fotografia professionale e la compatibilità universale di PNG. In questa guida imparerai a **impostare la modalità colore del PSD a 16‑bit grayscale** e poi a **esportare il PSD come PNG** usando Aspose.PSD per Java. Il tutorial copre tutto, dai prerequisiti alla risoluzione dei problemi, così potrai integrare il flusso di lavoro in qualsiasi pipeline di immagini basata su Java.

## Risposte rapide
- **Che cosa comporta “export PSD as PNG”?** Carica un PSD, opzionalmente cambia la sua modalità colore e salvalo come file PNG.  
- **Quale classe Aspose gestisce la conversione?** `PsdImage` carica il PSD e `PngOptions` definisce le impostazioni di output PNG.  
- **Ho bisogno di una licenza per la produzione?** Sì – una versione di prova funziona per i test, ma è necessaria una licenza a pagamento per l'uso commerciale.  
- **È possibile mantenere la profondità a 16‑bit in PNG?** Assolutamente, usando `PngColorType.GrayscaleWithAlpha`.  
- **Quali IDE sono supportati?** Qualsiasi IDE Java – IntelliJ IDEA, Eclipse, VS Code o NetBeans.

## Cos'è l'esportazione di PSD come PNG?
Export PSD as PNG è il processo di conversione di un documento Adobe Photoshop (PSD) in un file Portable Network Graphics (PNG) mantenendo i dati dei pixel e la profondità colore dell'immagine. Questa conversione è comunemente usata per condividere risorse in scala di grigi ad alta qualità sul web senza perdere dettagli tonali.

## Perché esportare PSD come PNG con scala di grigi a 16‑bit?
Esportare in PNG mantenendo la scala di grigi a 16‑bit preserva 65 536 tonalità di grigio, offrendo una ricchezza tonale molto superiore rispetto alle immagini a 8‑bit. Il supporto universale di PNG garantisce che i file possano essere visualizzati in browser, app mobili e editor desktop senza perdita, mentre la compressione senza perdita di Aspose.PSD assicura che non vengano introdotti artefatti.

## Prerequisiti
Prima di iniziare, assicurati di avere pronti i seguenti elementi:

1. **Java Development Kit (JDK)** – Installa l'ultima versione del JDK dal [sito di Oracle](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).  
2. **Libreria Aspose.PSD per Java** – Scarica il JAR dalla [pagina di download di Aspose](https://releases.aspose.com/psd/java/).  
3. **Un IDE** – IntelliJ IDEA, Eclipse o Visual Studio Code funzionano perfettamente.  
4. **Conoscenze di base di Java** – Dovresti sentirti a tuo agio nella creazione di classi, nella gestione delle eccezioni e nel lavoro con i percorsi dei file.  
5. **Un file PSD di esempio** – Creane uno in Adobe Photoshop o scarica un esempio gratuito online.

## Come esportare PSD come PNG passo dopo passo

## Come impostare la modalità colore del PSD a scala di grigi a 16‑bit?
PsdImage è la classe Aspose.PSD che carica e rappresenta un file PSD in memoria.  
ColorMode è un'enumerazione che definisce la modalità colore di un'immagine PSD.  

Carica il PSD con `PsdImage`, cambia la sua modalità colore usando la proprietà `ColorMode`, quindi salva il file modificato. Questa operazione avviene interamente in memoria, eliminando la necessità di file intermedi e garantendo che la conversione sia rapida ed efficiente.

```java
import com.aspose.psd.*;
import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.fileformats.psd.ColorModes;
import com.aspose.psd.fileformats.psd.CompressionMethod;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.PngOptions;
import com.aspose.psd.imageoptions.PsdOptions;
import com.aspose.psd.system.Enum;
```

Queste importazioni ti danno accesso alle funzionalità che utilizzerai per manipolare i file PSD, impostare la modalità colore e esportare il risultato come PNG.

## Come definire le directory di origine e di destinazione?
`File` è una classe java.io che rappresenta un percorso di file o directory nel file system.  

Devi indicare al programma dove leggere il PSD originale e dove scrivere il PNG convertito. L'uso di percorsi assoluti o relativi funziona, ma mantienili coerenti tra gli ambienti per evitare errori di risoluzione dei percorsi.

```java
String sourceDir = "Your Source Directory"; // Change to your source directory
String outputDir = "Your Document Directory"; // Change to your output directory
```

Sostituisci le stringhe segnaposto con i percorsi effettivi sulla tua macchina.

## Come incapsulare la logica di conversione in un metodo riutilizzabile?
`convertPsdToPng` è un metodo personalizzato che incapsula tutti i passaggi necessari per convertire un file PSD in PNG con impostazioni opzionali.  

Creare un metodo dedicato ti consente di riutilizzare gli stessi passaggi di conversione per più file o impostazioni diverse. Passa parametri come il percorso di origine, la cartella di destinazione e il livello di compressione opzionale, rendendo il flusso di lavoro flessibile e manutenibile.

```java
class LocalScopeExtension {
    void saveToPsdThenLoadAndSaveToPng(
        String file,
        short colorMode,
        short channelBitsCount,
        short channelsCount,
        short compression,
        int layerNumber) {
```

Questo metodo ti consente di **impostare la modalità colore del PSD** e poi **esportare PSD come PNG** in un unico flusso.

## Come caricare il PSD e applicare la modalità scala di grigi a 16‑bit?
PsdImage è la classe Aspose.PSD che carica un file PSD in memoria.  
ColorMode.GRAYSCALE_16 è un valore di enumerazione che imposta l'immagine a scala di grigi a 16‑bit.  
`channelBitsCount` è una proprietà che specifica il numero di bit per canale.  

All'interno del metodo di conversione, costruisci i percorsi completi dei file, istanzia `PsdImage` e cambia il suo `ColorMode` in `ColorMode.GRAYSCALE_16`. La proprietà `channelBitsCount` deve essere impostata a 16 per mantenere l'alta profondità di bit, garantendo che l'immagine conservi tutte le informazioni tonali.

```java
String filePath = sourceDir + file + ".psd";
String postfix = Enum.getName(ColorModes.class, colorMode) + channelBitsCount + "_" +
                 channelsCount + "_" + Enum.getName(CompressionMethod.class, compression);
String exportPath = outputDir + file + postfix + ".psd";
String pngExportPath = outputDir + file + postfix + ".png";
// Load a predefined 16-bit grayscale PSD
PsdImage image = (PsdImage)Image.load(filePath);
```

Il `postfix` ti aiuta a tenere traccia delle impostazioni usate per ogni file esportato.

## Come disegnare un bordo sottile sull'immagine (passo opzionale)?
`Graphics` è una classe che fornisce capacità di disegno su una tela `PsdImage`.  

Puoi opzionalmente disegnare un rettangolo grigio attorno all'immagine per rendere l'output più visibile durante i test. Questo passo dimostra come lavorare con livelli e oggetti grafici, e il rettangolo è calcolato dinamicamente in modo da rimanere centrato indipendentemente dalle dimensioni dell'immagine.

```java
try {
    RasterCachedImage raster = layerNumber >= 0 ? image.getLayers()[layerNumber] : image;
    // Draw a gray inner border around the perimeter of the layer
    Graphics graphics = new Graphics(raster);
    int width = raster.getWidth();
    int height = raster.getHeight();
    Rectangle rect = new Rectangle(
        width / 3,
        height / 3,
        width - (2 * (width / 3)) - 1,
        height - (2 * (height / 3)) - 1);
    graphics.drawRectangle(new Pen(Color.getDarkGray(), 1), rect);
```

Il rettangolo è calcolato dinamicamente in modo da rimanere centrato indipendentemente dalle dimensioni dell'immagine.

## Come salvare il PSD modificato con la nuova modalità colore?
`PsdOptions` è una classe che controlla come un file PSD viene salvato, includendo le impostazioni di modalità colore e profondità di bit.  

Dopo il disegno (o saltando quel passo), chiama `save` sull'istanza `PsdImage`, passando un oggetto `PsdOptions` che preserva la configurazione a scala di grigi a 16‑bit. Questo garantisce che il PSD salvato mantenga la modalità colore desiderata senza perdita di dati.

```java
    // Save a copy of PSD with specific characteristics
    PsdOptions psdOptions = new PsdOptions();
    psdOptions.setColorMode(colorMode);
    psdOptions.setChannelBitsCount(channelBitsCount);
    psdOptions.setChannelsCount(channelsCount);
    psdOptions.setCompressionMethod(compression);
    image.save(exportPath, psdOptions);
}
```

## Come convertire il PSD in PNG mantenendo la profondità a 16‑bit?
`PngOptions` è una classe che definisce le impostazioni di output PNG come tipo di colore e livello di compressione.  
`PngColorType.GrayscaleWithAlpha` è un valore di enumerazione che memorizza dati a scala di grigi a 16‑bit con canale alfa.  

Carica il PSD appena salvato, configura `PngOptions` con `PngColorType.GrayscaleWithAlpha` e chiama `save`. Questo mantiene i dati a scala di grigi a 16‑bit all'interno del file PNG, fornendo un'immagine senza perdita, di alta qualità, adatta per ulteriori elaborazioni o distribuzione.

```java
finally {
    image.dispose();
}
// Load the saved PSD
PsdImage image1 = (PsdImage)Image.load(exportPath);
try {
    // Convert the saved PSD to a grayscale PNG image
    PngOptions pngOptions = new PngOptions();
    pngOptions.setColorType(PngColorType.GrayscaleWithAlpha);
    image1.save(pngExportPath, pngOptions); // here should be no exception
}
finally {
    image1.dispose();
}
```

Ora hai esportato con successo **PSD come PNG** mantenendo i dati a scala di grigi a 16‑bit di alta qualità.

## Problemi comuni e soluzioni
| Problema | Perché succede | Correzione |
|----------|----------------|------------|
| **“Unsupported color type” exception** | Tentativo di salvare un PSD con una configurazione di canale non supportata. | Assicurati che `channelBitsCount` corrisponda alla reale profondità di bit (16) e che `channelsCount` sia corretto per la scala di grigi (1). |
| **File not found** | Percorso della directory di origine errato. | Controlla nuovamente la stringa `sourceDir` e verifica che il file PSD esista in quella posizione. |
| **Output PNG appears black** | PNG salvato senza una corretta gestione dell'alpha. | Usa `PngColorType.GrayscaleWithAlpha` come mostrato sopra. |
| **Memory overflow on large PSDs** | Caricamento dell'intero file in memoria. | Abilita la modalità streaming tramite `PsdImage.load(inputStream, new LoadOptions())` per elaborare file di grandi dimensioni in modo efficiente. |

## Domande frequenti

**Q: Cos'è la modalità colore in scala di grigi a 16‑bit?**  
A: Fornisce 65 536 tonalità di grigio, offrendo molto più dettaglio tonale rispetto allo standard a 8‑bit (256 tonalità).

**Q: Posso usare Aspose.PSD per immagini non in scala di grigi?**  
A: Assolutamente! Aspose.PSD supporta RGB, CMYK, Lab, Indexed e molte altre modalità colore.

**Q: Esiste una versione di prova di Aspose.PSD?**  
A: Sì, puoi provare una versione di prova gratuita di Aspose.PSD. Vai alla [pagina di download di Aspose](https://releases.aspose.com/).

**Q: Dove posso trovare più esempi di Aspose.PSD?**  
A: Consulta la [documentazione ufficiale](https://reference.aspose.com/psd/java/) per tutorial approfonditi, riferimenti API e progetti di esempio.

**Q: Come acquistare una licenza per Aspose.PSD?**  
A: Puoi acquistare una licenza visitando la [pagina di acquisto di Aspose](https://purchase.aspose.com/buy).

---

**Ultimo aggiornamento:** 2026-09-28  
**Testato con:** Aspose.PSD per Java 24.12 (ultima versione al momento della stesura)  
**Autore:** Aspose

## Tutorial correlati

- [Converti PSD in PNG con profondità di bit specificata usando Aspose.PSD per Java](/psd/java/optimizing-png-files/specify-png-bit-depth/)
- [Esporta PSD in PNG con effetti di livello usando Aspose.PSD per Java](/psd/java/psd-image-modification-conversion/apply-layer-effects-psd-files/)
- [Salva PSD come JPEG e supporta il colore RGB con Aspose.PSD Java](/psd/java/advanced-psd-layer-features-effects/support-rgb-color-psd-files/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}