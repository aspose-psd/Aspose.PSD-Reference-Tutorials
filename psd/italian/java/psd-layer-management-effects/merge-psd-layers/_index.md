---
date: 2026-04-05
description: Scopri come esportare PSD in PNG e unire i livelli PSD usando Aspose.PSD
  per Java. Include la conversione da PSD a JPEG, l'impostazione della qualità JPEG
  e consigli per la conversione da PSD a TIFF.
keywords:
- export psd to png
- convert psd to jpeg
- how to merge psd
- set jpeg quality
- psd to tiff conversion
linktitle: Esporta PSD in PNG e unisci i livelli usando Aspose.PSD per Java
second_title: Aspose.PSD Java API
title: Esporta PSD in PNG e unisci i livelli usando Aspose.PSD per Java
url: /it/java/psd-layer-management-effects/merge-psd-layers/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Esporta PSD in PNG e Unisci i Livelli usando Aspose.PSD per Java

## Introduzione

Ti sei mai chiesto come i grafici ottengono quelle immagini complesse e a più livelli in Photoshop? Il segreto spesso risiede nell'**esportare PSD in PNG** e nell'unire i livelli in modo intelligente. Se lavori con file PSD in Java, padroneggiare queste tecniche può aiutarti a creare immagini composite, ridurre le dimensioni del file e preparare le risorse per il web o il mobile. In questo tutorial vedremo **come unire i livelli PSD** usando Aspose.PSD per Java, e ti mostreremo anche come esportare il risultato in PNG (o JPEG/TIFF quando necessario). Alla fine, sarai in grado di automatizzare la gestione dei livelli e i flussi di lavoro di esportazione direttamente dalla tua applicazione Java.

## Risposte Rapide
- **Quale libreria gestisce i file PSD in Java?** Aspose.PSD for Java.  
- **Posso esportare PSD in PNG?** Sì – basta impostare le opzioni immagine appropriate.  
- **Come unisco più livelli?** Carica il PSD, manipola la collezione `Layer`, poi salva.  
- **Cosa fare se ho bisogno di controllare la qualità JPEG?** Usa `JpegOptions` e imposta la qualità (0‑100).  
- **È necessario Photoshop?** No, Aspose.PSD funziona indipendentemente dal software Adobe.

## Cos'è l'esportazione di PSD in PNG?

Esportare PSD in PNG significa convertire un documento Photoshop (PSD) in un file Portable Network Graphics (PNG) opzionalmente appiattendo o unendo i livelli. PNG conserva la trasparenza ed è ampiamente supportato sul web, rendendolo un formato popolare per le risorse UI.

## Perché unire i livelli PSD programmaticamente?

- **Automazione:** Elabora in batch centinaia di file senza clic manuali.  
- **Prestazioni:** I livelli uniti riducono i tempi di rendering nelle applicazioni successive.  
- **Dimensione del file:** Appiattire i livelli non necessari può ridurre l'immagine finale.  
- **Coerenza:** Garantisce lo stesso ordine dei livelli e la stessa fusione tra le build.

## Prerequisiti

1. **Aspose.PSD for Java Library** – scarica dal [Aspose.PSD for Java download link](https://releases.aspose.com/psd/java/).  
2. **Java Development Environment** – IntelliJ IDEA, Eclipse o qualsiasi IDE tu preferisca.  
3. **Sample PSD File** – un file con più livelli (ad es., `layers.psd`).  
4. **Basic Java Knowledge** – dovresti sentirti a tuo agio con classi e metodi.  
5. **Aspose Temporary License (Optional)** – per file più grandi o per rimuovere le limitazioni di prova, ottieni una [temporary license](https://purchase.aspose.com/temporary-license/).

## Importa Pacchetti

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.JpegOptions;
```

## Guida Passo‑Passo

### Passo 1: Carica il File PSD

```java
String dataDir = "Your Document Directory";
PsdImage psdImage = (PsdImage)Image.load(dataDir + "layers.psd");
```

> Questo carica `layers.psd` in un oggetto `PsdImage`, fornendoti pieno accesso ai suoi livelli.

### Passo 2: Ispeziona i Livelli (come unire psd)

```java
Layer[] layers = psdImage.getLayers();
System.out.println("Total layers: " + layers.length);

for (Layer layer : layers) {
    System.out.println("Layer name: " + layer.getName());
}
```

> Esaminare i nomi dei livelli ti aiuta a decidere quali appiattire o mantenere separati.

### Passo 3: Imposta le Opzioni Immagine (imposta qualità jpeg)

```java
JpegOptions jpgOptions = new JpegOptions();
jpgOptions.setQuality(80); // Set the quality of the JPEG image (0-100)
```

> Se preferisci PNG o TIFF, puoi sostituire `JpegOptions` con `PngOptions` o `TiffOptions` – è qui che verrebbe configurata la **conversione psd in tiff**.

### Passo 4: Salva l'Immagine Unita (esporta psd in png)

```java
psdImage.save(dataDir + "MergePSDlayers_output.png", jpgOptions);
```

> Il metodo `save` scrive il risultato unito in `MergePSDlayers_output.png`.  
> *Suggerimento:* Per esportare in PNG, sostituisci `jpgOptions` con un'istanza `PngOptions`; il resto del codice rimane invariato.

## Problemi Comuni e Soluzioni

- **Eccezione file non trovato:** Verifica che `dataDir` termini con un separatore di percorso (`/` o `\\`) e che `layers.psd` esista.  
- **Colori inaspettati dopo l'unione:** Assicurati che le modalità di fusione dei livelli siano compatibili; puoi regolarle tramite `layer.setBlendMode(...)`.  
- **File di output di grandi dimensioni:** Riduci la qualità JPEG o usa i livelli di compressione PNG per diminuire le dimensioni.

## Domande Frequenti

**Q: È possibile salvare l'immagine unita in formati diversi da JPEG?**  
A: Assolutamente! Aspose.PSD supporta PNG, BMP, TIFF e altro. Basta usare la classe di opzioni corrispondente (`PngOptions`, `BmpOptions`, `TiffOptions`).

**Q: Come posso regolare la qualità dell'immagine per diversi formati di output?**  
A: Ogni classe di opzioni espone le proprie impostazioni di qualità/compressione. Per JPEG, usa `setQuality(int)`. Per PNG, puoi controllare `CompressionLevel`.

**Q: È necessario avere Photoshop installato per usare Aspose.PSD per Java?**  
A: No. Aspose.PSD funziona indipendentemente da Adobe Photoshop, quindi puoi eseguirlo su qualsiasi server o ambiente CI.

**Q: Cosa succede se non imposto le opzioni immagine prima di salvare?**  
A: La libreria applica impostazioni predefinite (ad es., qualità JPEG 75). Specificare le opzioni ti dà il controllo sull'output finale.

**Q: Posso convertire un PSD direttamente in TIFF in un solo passaggio?**  
A: Sì – istanzia `TiffOptions` e chiama `psdImage.save("output.tiff", tiffOptions);`.

---

**Ultimo Aggiornamento:** 2026-04-05  
**Testato Con:** Aspose.PSD for Java 24.12 (latest at time of writing)  
**Autore:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}