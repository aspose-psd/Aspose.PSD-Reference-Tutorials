---
date: 2026-03-31
description: Scopri come salvare i file PSD in PNG usando Aspose.PSD per Java. Questo
  tutorial sul mixer di canali PSD mostra come convertire i PSD in PNG, modificare
  i livelli RGB e CMYK e processare in batch i file PSD.
linktitle: Export Channel Mixer Adjustment Layer in PSD - Java
second_title: Aspose.PSD Java API
title: Come salvare PSD come PNG con il livello di regolazione Channel Mixer in Java
url: /it/java/psd-layer-management-effects/export-channel-mixer-adjustment-layer-psd/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Come salvare PSD come PNG con il livello di regolazione Channel Mixer in Java

## Introduzione

## Risposte rapide
- **Cosa significa “save PSD as PNG”?** Converte un documento Photoshop in un PNG senza perdita mantenendo la trasparenza.  
- **Quale libreria gestisce la conversione?** Aspose.PSD per Java fornisce pieno supporto per i livelli di regolazione.  
- **Posso lavorare sia con file RGB che CMYK?** Sì – l'API include le classi `RgbChannelMixerLayer` e `CmykChannelMixerLayer`.  
- **È necessaria una licenza per l'uso in produzione?** È richiesta una versione con licenza; è disponibile una licenza temporanea per i test.  
- **È possibile il batch processing?** Assolutamente – è possibile iterare su una cartella e applicare gli stessi passaggi a ogni PSD.

## Che cos'è un livello di regolazione Channel Mixer?

Un livello di regolazione Channel Mixer ti consente di rimescolare i contributi dei canali Rosso, Verde, Blu (o Ciano, Magenta, Giallo, Nero) per ottenere un bilanciamento cromatico preciso. A differenza di un livello normale, è non‑distruttivo, il che significa che i dati pixel originali rimangono intatti.

## Perché usare Aspose.PSD per **convertire PSD in PNG**?

- **Fedele riproduzione dei livelli** – tutti i livelli di regolazione sono preservati durante la conversione.  
- **Nessun Photoshop richiesto** – esegui il codice su qualsiasi server o pipeline CI.  
- **Supporta sia RGB che CMYK** – ideale per flussi di lavoro pronti per la stampa.  

## Prerequisiti

1. **Aspose.PSD per Java** – scaricalo dalla [download page](https://releases.aspose.com/psd/java/).  
2. **Java Development Kit (JDK) 8+** – assicurati che `java` sia nel tuo PATH.  
3. **IDE** – IntelliJ IDEA, Eclipse o qualsiasi editor tu preferisca.  
4. **File PSD di esempio** – file che contengono livelli di regolazione Channel Mixer (sia varianti RGB che CMYK).

## Importa i pacchetti

Per prima cosa, importa le classi di cui avremo bisogno. Questo imposta l'ambiente per lavorare con file PSD e opzioni di esportazione PNG.

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.adjustmentlayers.CmykChannelMixerLayer;
import com.aspose.psd.fileformats.psd.layers.adjustmentlayers.RgbChannelMixerLayer;
import com.aspose.psd.imageoptions.PngOptions;
```

## Come **salvare PSD come PNG** – Esempio RGB

### Passo 1: Carica il file PSD che contiene un livello Channel Mixer RGB

```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "ChannelMixerAdjustmentLayerRgb.psd";

PsdImage im = (PsdImage) Image.load(sourceFileName);
```

Indichiamo la cartella che contiene il nostro PSD (`dataDir`) e carichiamo il file in un oggetto `PsdImage`, che ci dà pieno accesso ai suoi livelli.

### Passo 2: Modifica il livello Channel Mixer RGB

```java
for (int i = 0; i < im.getLayers().length; i++) {
    if (im.getLayers()[i] instanceof RgbChannelMixerLayer) {
        RgbChannelMixerLayer rgbLayer = (RgbChannelMixerLayer) im.getLayers()[i];
        rgbLayer.getRedChannel().setBlue((short) 100);
        rgbLayer.getBlueChannel().setGreen((short) -100);
        rgbLayer.getGreenChannel().setConstant((short) 50);
    }
}
```

Iteriamo su ogni livello, individuiamo il `RgbChannelMixerLayer` e ne regiamo i valori dei canali. Questo esempio aumenta il contributo del blu nel canale rosso, riduce il verde nel canale blu e aggiunge un offset costante al canale verde.

### Passo 3: Salva il PSD modificato (ancora un PSD)

```java
String psdPathAfterChange = dataDir + "ChannelMixerAdjustmentLayerRgbChanged.psd";
im.save(psdPathAfterChange);
```

Il salvataggio del file preserva il livello di regolazione così puoi riaprirlo più tardi in Photoshop se necessario.

### Passo 4: Esporta l'immagine in PNG (il passaggio **salvare PSD come PNG**)

```java
String pngExportPath = dataDir + "ChannelMixerAdjustmentLayerRgbChanged.png";
PngOptions saveOptions = new PngOptions();
saveOptions.setColorType(PngColorType.TruecolorWithAlpha);
im.save(pngExportPath, saveOptions);
```

Creiamo un'istanza di `PngOptions`, impostiamo il tipo di colore su `TruecolorWithAlpha` per mantenere la trasparenza, e poi esportiamo l'immagine.

## Come **salvare PSD come PNG** – Esempio CMYK

### Passo 5: Carica il file PSD che contiene un livello Channel Mixer CMYK

```java
sourceFileName = dataDir + "ChannelMixerAdjustmentLayerCmyk.psd";
PsdImage img = (PsdImage) Image.load(sourceFileName);
```

Il processo di caricamento è identico; lavoriamo semplicemente con un file diverso che utilizza il modello colore CMYK.

### Passo 6: Modifica il livello Channel Mixer CMYK

```java
for (int i = 0; i < img.getLayers().length; i++) {
    if (img.getLayers()[i] instanceof CmykChannelMixerLayer) {
        CmykChannelMixerLayer cmykLayer = (CmykChannelMixerLayer) img.getLayers()[i];
        cmykLayer.getCyanChannel().setBlack((short) 20);
        cmykLayer.getMagentaChannel().setYellow((short) 50);
        cmykLayer.getYellowChannel().setCyan((short) -25);
        cmykLayer.getBlackChannel().setYellow((short) 25);
    }
}
```

Qui regiamo i canali CMYK: aggiungendo nero al ciano, modificando la componente gialla del magenta, ecc. Questo dimostra la flessibilità dell'API per file destinati alla stampa.

### Passo 7: Salva il PSD CMYK modificato

```java
psdPathAfterChange = dataDir + "ChannelMixerAdjustmentLayerCmykChanged.psd";
img.save(psdPathAfterChange);
```

Ancora, manteniamo una versione PSD con le nuove regolazioni.

### Passo 8: Esporta l'immagine CMYK in PNG

```java
pngExportPath = dataDir + "ChannelMixerAdjustmentLayerCmykChanged.png";
PngOptions options = new PngOptions();
options.setColorType(PngColorType.TruecolorWithAlpha);
img.save(pngExportPath, options);
```

Anche se la sorgente è CMYK, l'esportazione PNG la converte automaticamente in un PNG basato su RGB mantenendo la trasparenza.

## Problemi comuni e soluzioni

| Problema | Perché accade | Soluzione |
|----------|----------------|-----------|
| Il PNG appare con colori errati | Conversione CMYK → RGB senza profilo corretto | Assicurati che il PSD di origine abbia un profilo ICC incorporato; Aspose.PSD lo rispetta durante l'esportazione. |
| Livello di regolazione non trovato | Mancata corrispondenza del tipo di livello (ad es., un livello “Color Balance” invece) | Verifica la classe del livello (`RgbChannelMixerLayer` o `CmykChannelMixerLayer`) prima del cast. |
| Eccezione di licenza durante l'esecuzione | Uso della libreria senza licenza valida | Applica una licenza temporanea dalla pagina [temporary license](https://purchase.aspose.com/temporary-license/) durante lo sviluppo. |

## Domande frequenti

**Q: Posso usare Aspose.PSD per Java con altri formati immagine?**  
A: Sì, la libreria supporta PNG, JPEG, BMP, TIFF e molti altri oltre a PSD.

**Q: Come gestisco altri livelli di regolazione come Curve o Livelli?**  
A: Ogni tipo di regolazione ha la sua classe (ad esempio `CurvesAdjustmentLayer`). Puoi manipolarli in modo simile all'esempio del channel mixer.

**Q: Esiste un modo per **processare in batch file PSD** in PNG?**  
A: Assolutamente. Avvolgi i passaggi sopra in un ciclo `for‑each` che itera sui file in una directory, applicando le stesse modifiche e la logica di esportazione.

**Q: Qual è la migliore pratica per mantenere la massima qualità dell'immagine durante la conversione?**  
A: Usa `PngOptions` con `TruecolorWithAlpha` ed evita il down‑sampling. Inoltre, conserva il PSD originale se hai bisogno di modifiche senza perdita in seguito.

**Q: È necessaria una licenza a pagamento per l'uso in produzione?**  
A: Sì. Una licenza temporanea è sufficiente per la valutazione, ma è necessaria una licenza completa per il deployment commerciale.

---

**Ultimo aggiornamento:** 2026-03-31  
**Testato con:** Aspose.PSD per Java 24.12  
**Autore:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}