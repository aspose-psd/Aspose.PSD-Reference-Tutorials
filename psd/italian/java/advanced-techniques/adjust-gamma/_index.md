---
date: 2025-12-21
description: Impara come eseguire l'elaborazione di immagini Java regolando la gamma
  dell'immagine con Aspose.PSD. Guida passo‑passo per convertire PSD in TIFF e applicare
  la correzione della gamma.
linktitle: Adjust Gamma of an Image
second_title: Aspose.PSD Java API
title: Elaborazione di immagini Java – Regola il gamma con Aspose.PSD
url: /it/java/advanced-techniques/adjust-gamma/
weight: 23
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Elaborazione di Immagini Java – Regola Gamma con Aspose.PSD

## Introduzione

Se lavori su **java image processing**, regolare la gamma di un’immagine è una tecnica fondamentale per migliorare luminosità e contrasto senza perdere dettagli. In questo tutorial vedremo come utilizzare **Aspose.PSD for Java** per applicare la correzione gamma a un file PSD e poi esportare il risultato come immagine TIFF. Scoprirai perché questo approccio è veloce, affidabile e perfetto per pipeline di immagini lato server.

## Risposte Rapide
- **Cosa fa la correzione gamma?** Rimappa i valori di luminanza per rendere le aree scure più luminose o le aree chiare più scure, preservando i dettagli complessivi.  
- **Quale libreria gestisce l’elaborazione?** Aspose.PSD for Java fornisce un metodo dedicato `adjustGamma` per le immagini raster.  
- **Posso convertire PSD in TIFF nello stesso flusso?** Sì – dopo la regolazione della gamma puoi salvare l’immagine direttamente in TIFF usando `TiffOptions`.  
- **È necessaria una licenza per lo sviluppo?** Una versione di prova gratuita è sufficiente per i test; è richiesta una licenza commerciale per l’uso in produzione.  
- **Quale versione di Java è supportata?** Aspose.PSD supporta Java 8 e successive.

## Che cos’è il java image processing?

Il java image processing indica la manipolazione, l’analisi e la trasformazione di dati visivi mediante librerie Java. Le attività includono ridimensionamento, filtraggio, correzione colore e conversione di formato—tutto automatizzabile in applicazioni desktop o web.

## Perché usare Aspose.PSD per la correzione gamma?

Aspose.PSD offre un’API di alto livello che astrae la complessità del formato PSD, permettendoti di concentrarti sulle regolazioni dell’immagine. Gestisce caching, profili colore e fornisce una chiamata semplice `adjustGamma`, rendendola ideale per **image gamma correction** e **convert psd to tiff**.

## Prerequisiti

Prima di immergerti nel tutorial, assicurati di avere i seguenti prerequisiti configurati:

1. **Ambiente di Sviluppo Java** – Verifica di avere un ambiente di sviluppo Java installato sul tuo sistema.  
2. **Libreria Aspose.PSD** – Scarica e integra la libreria Aspose.PSD nel tuo progetto Java. Puoi trovare le risorse necessarie nella [documentazione](https://reference.aspose.com/psd/java/).  
3. **Immagine di Esempio** – Prepara un’immagine PSD di esempio che userai per applicare la regolazione gamma.

## Importare i Pacchetti

Per avviare il processo, importa i pacchetti richiesti nel tuo progetto Java. Questo prepara il terreno per utilizzare le funzionalità di Aspose.PSD senza intoppi.

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.psd.fileformats.tiff.enums.TiffPhotometrics;
import com.aspose.psd.imageoptions.TiffOptions;
```

## Passo 1: Caricare l’Immagine

Inizia caricando l’immagine PSD di esempio in un’istanza della classe `RasterImage`. Questa è la base per le successive regolazioni gamma.

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

// Load an existing image into an instance of RasterImage class
Image image = Image.load(sourceFile);

// Cast object of Image to RasterImage
RasterImage rasterImage = (RasterImage)image;

// Check if RasterImage is cached for better performance
if (!rasterImage.isCached()) {
    rasterImage.cacheData();
}
```

## Passo 2: Regolare la Gamma

Ora regola la gamma dell’immagine caricata usando il metodo `adjustGamma`. Affina i valori di gamma secondo le tue esigenze.

```java
// Adjust the gamma
rasterImage.adjustGamma(2.2f, 2.2f, 2.2f);
```

## Passo 3: Creare TiffOptions

Crea un’istanza di `TiffOptions` per l’immagine risultante. Imposta varie proprietà, come i bit per campione e le opzioni fotometriche, per adattare l’output alle tue specifiche.

```java
// Create an instance of TiffOptions for the resultant image
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
int[] ushort = { 8, 8, 8 };
tiffOptions.setBitsPerSample(ushort);
tiffOptions.setPhotometric(TiffPhotometrics.Rgb);
```

## Passo 4: Salvare l’Immagine Resultante

Salva l’immagine manipolata in formato TIFF usando i `TiffOptions` definiti in precedenza.

```java
// Save the resultant image to TIFF format
String destName = dataDir + "AdjustGamma_out.tiff";
rasterImage.save(destName, tiffOptions);
```

## Problemi Comuni e Soluzioni

| Problema | Perché si Verifica | Come Risolverlo |
|----------|--------------------|-----------------|
| **L’immagine appare sbiadita** | Valore gamma troppo alto (es. > 2.5) | Riduci il fattore gamma a un valore compreso tra 1.8 e 2.2. |
| **`rasterImage.isCached()` restituisce false** | Immagine non ancora caricata in memoria | Chiama `rasterImage.cacheData()` prima di regolare la gamma. |
| **La dimensione del file TIFF è grande** | Bit per campione impostati a 16‑bit | Usa un campione a 8‑bit (`{8,8,8}`) come mostrato nell’esempio. |

## Domande Frequenti

**D: Posso applicare valori gamma diversi a ciascun canale colore?**  
R: Sì – il metodo `adjustGamma` accetta valori float separati per i canali rosso, verde e blu.

**D: È possibile concatenare più regolazioni immagine prima del salvataggio?**  
R: Assolutamente. Puoi eseguire ridimensionamento, ritaglio o correzioni colore in sequenza sulla stessa istanza di `RasterImage`.

**D: Aspose.PSD supporta file PSD multi‑pagina?**  
R: Sì, ogni livello può essere accesso e processato individualmente.

**D: Quali formati posso esportare oltre a TIFF?**  
R: Aspose.PSD supporta PNG, JPEG, BMP e molti altri formati tramite le rispettive classi di opzioni.

## Conclusione

Complimenti! Hai completato con successo **java image processing** regolando la gamma di un file PSD e esportandolo come immagine TIFF usando Aspose.PSD for Java. Questo flusso di lavoro ti offre un controllo granulare su luminosità e contrasto, rendendolo ideale per pipeline grafiche automatizzate, servizi web o utility desktop.

---

**Ultimo Aggiornamento:** 2025-12-21  
**Testato Con:** Aspose.PSD 24.11 for Java  
**Autore:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

## FAQ's

### Q1: Dove posso trovare la documentazione di Aspose.PSD?

A1: Puoi accedere alla documentazione su [https://reference.aspose.com/psd/java/](https://reference.aspose.com/psd/java/).

### Q2: Come scarico Aspose.PSD per Java?

A2: Scarica la libreria da [https://releases.aspose.com/psd/java/](https://releases.aspose.com/psd/java/).

### Q3: Dove posso acquistare Aspose.PSD?

A3: Visita [https://purchase.aspose.com/buy](https://purchase.aspose.com/buy) per acquistare Aspose.PSD.

### Q4: È disponibile una versione di prova gratuita?

A4: Sì, puoi provare la versione di prova gratuita su [https://releases.aspose.com/](https://releases.aspose.com/).

### Q5: Dove posso richiedere supporto per Aspose.PSD?

A5: Per il supporto, visita il forum di Aspose.PSD su [https://forum.aspose.com/c/psd/34](https://forum.aspose.com/c/psd/34).

---