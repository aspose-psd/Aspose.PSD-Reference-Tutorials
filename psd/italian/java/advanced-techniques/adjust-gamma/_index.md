---
date: 2026-02-27
description: Scopri come regolare la gamma nell'elaborazione di immagini Java con
  Aspose.PSD, convertire PSD in TIFF e correggere le immagini sbiadite in un tutorial
  conciso.
linktitle: Adjust Gamma of an Image
second_title: Aspose.PSD Java API
title: Come regolare il gamma nell'elaborazione di immagini Java con Aspose.PSD
url: /it/java/advanced-techniques/adjust-gamma/
weight: 23
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Come regolare il gamma nella elaborazione di immagini Java con Aspose.PSD

## Introduzione

Se lavori su **java image processing**, imparare **come regolare il gamma** è una tecnica fondamentale per migliorare luminosità e contrasto senza perdere dettagli. In questo tutorial vedremo come utilizzare **Aspose.PSD for Java** per applicare la correzione gamma a un file PSD, **convertire PSD in TIFF**, e evitare un **immagine sbiadita**. Scoprirai perché questo approccio è veloce, affidabile e perfetto per pipeline di immagini lato server.

## Risposte rapide
- **Cosa fa la correzione gamma?** Rimappa i valori di luminanza per rendere le aree scure più luminose o le aree chiare più scure, preservando i dettagli complessivi.  
- **Quale libreria gestisce l'elaborazione?** Aspose.PSD for Java fornisce un metodo dedicato `adjustGamma` per le immagini raster.  
- **Posso convertire PSD in TIFF nello stesso flusso?** Sì – dopo la regolazione del gamma puoi salvare l'immagine direttamente in TIFF usando `TiffOptions`.  
- **È necessaria una licenza per lo sviluppo?** Una prova gratuita è sufficiente per i test; è richiesta una licenza commerciale per l'uso in produzione.  
- **Quale versione di Java è supportata?** Aspose.PSD supporta Java 8 e successive.

## Come regolare il gamma nella elaborazione di immagini Java
Regolare il gamma è una parte centrale di qualsiasi **java image processing tutorial** che tratta luminosità o contrasto. Di seguito scomponiamo i passaggi, spieghiamo perché ogni riga è importante e ti mostriamo come integrare il processo nel tuo codice esistente.

## Cos'è la correzione gamma in Java?
La correzione gamma modifica la relazione non lineare tra i valori di pixel codificati e la luminosità visualizzata. Regolando la curva gamma puoi **correggere problemi di immagine sbiadita** o migliorare i dettagli nelle ombre senza sovra‑esporre le alte luci.

## Perché usare Aspose.PSD per la correzione gamma?
Aspose.PSD agisce come una potente **java image processing library** che astrae le complessità del formato PSD. Gestisce profili colore, caching e fornisce una semplice chiamata `adjustGamma`, rendendola ideale per **java gamma correction** e flussi di lavoro **convert PSD to TIFF**.

## Prerequisiti

1. **Ambiente di sviluppo Java** – Java 8 o successiva installata.  
2. **Libreria Aspose.PSD** – Scarica e aggiungi il JAR al tuo progetto. Vedi la [documentazione](https://reference.aspose.com/psd/java/) ufficiale.  
3. **Immagine di esempio** – Un file PSD che desideri elaborare (ad es. `sample.psd`).  

## Importare i pacchetti

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.psd.fileformats.tiff.enums.TiffPhotometrics;
import com.aspose.psd.imageoptions.TiffOptions;
```

## Passo 1: Caricare l'immagine

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

**Consiglio:** Caching dei dati raster una sola volta riduce il consumo di memoria quando applichi più regolazioni consecutivamente.

## Passo 2: Regolare il gamma

```java
// Adjust the gamma
rasterImage.adjustGamma(2.2f, 2.2f, 2.2f);
```

Puoi passare valori diversi per i canali rosso, verde e blu se hai bisogno di regolazioni specifiche per canale.

## Passo 3: Creare TiffOptions

```java
// Create an instance of TiffOptions for the resultant image
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
int[] ushort = { 8, 8, 8 };
tiffOptions.setBitsPerSample(ushort);
tiffOptions.setPhotometric(TiffPhotometrics.Rgb);
```

Impostare un campione a 8 bit (`{8,8,8}`) mantiene la dimensione del file TIFF ragionevole preservando la fedeltà del colore.

## Passo 4: Salvare l'immagine risultante

```java
// Save the resultant image to TIFF format
String destName = dataDir + "AdjustGamma_out.tiff";
rasterImage.save(destName, tiffOptions);
```

Dopo il salvataggio, puoi inviare il TIFF a sistemi a valle come servizi di stampa o API web.

## Casi d'uso comuni

- **Pipeline grafiche automatizzate** – Regola il gamma al volo prima di generare miniature.  
- **Strumenti di conversione batch** – Converti grandi archivi PSD in TIFF normalizzando la luminosità.  
- **Servizi web** – Esporre un endpoint che riceve un PSD, applica la correzione gamma e restituisce un TIFF per il client.

## Problemi comuni e soluzioni

| Problema | Perché accade | Come risolvere |
|----------|----------------|----------------|
| **L'immagine appare sbiadita** | Valore gamma troppo alto (es. > 2.5) | Riduci il fattore gamma a un valore tra 1.8 e 2.2. |
| **`rasterImage.isCached()` restituisce false** | Immagine non ancora caricata in memoria | Chiama `rasterImage.cacheData()` prima di regolare il gamma. |
| **La dimensione del file TIFF è grande** | Bits per campione impostati a 16 bit | Usa un campione a 8 bit (`{8,8,8}`) come mostrato nell'esempio. |

## Domande frequenti

**D: Posso applicare valori gamma diversi a ciascun canale colore?**  
R: Sì – il metodo `adjustGamma` accetta valori float separati per i canali rosso, verde e blu.

**D: È possibile concatenare più regolazioni di immagine prima del salvataggio?**  
R: Assolutamente. Puoi eseguire ridimensionamento, ritaglio o correzioni colore in sequenza sulla stessa istanza `RasterImage`.

**D: Aspose.PSD supporta file PSD multi‑pagina?**  
R: Sì, ogni livello può essere accesso e processato individualmente.

**D: In quale formato posso esportare oltre a TIFF?**  
R: Aspose.PSD supporta PNG, JPEG, BMP e molti altri formati tramite le rispettive classi di opzioni.

**D: Come evito un'immagine sbiadita dopo la correzione gamma?**  
R: Inizia con un gamma moderato (intorno a 2.0) e visualizza l'anteprima; riduci il valore se l'immagine risulta troppo luminosa.

## Conclusione

Congratulazioni! Hai appreso con successo **come regolare il gamma** in un flusso di lavoro **java image processing**, convertito un PSD in TIFF e evitato le insidie comuni come una **immagine sbiadita**. Questo modello ti offre un controllo fine su luminosità e contrasto, rendendolo ideale per pipeline grafiche automatizzate, servizi web o utility desktop.

---

**Ultimo aggiornamento:** 2026-02-27  
**Testato con:** Aspose.PSD 24.11 per Java  
**Autore:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}