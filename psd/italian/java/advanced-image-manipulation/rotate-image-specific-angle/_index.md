---
date: 2025-12-08
description: Scopri come ruotare un'immagine di un angolo specifico in Java usando
  Aspose.PSD. La guida copre la rotazione dell'immagine in Java, la rotazione dell'immagine
  a un angolo specifico, la gestione dello sfondo e altro.
linktitle: How to Rotate Image on a Specific Angle
second_title: Aspose.PSD Java API
title: Come ruotare un'immagine di un angolo specifico con Aspose.PSD per Java
url: /it/java/advanced-image-manipulation/rotate-image-specific-angle/
weight: 20
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Come ruotare un'immagine di un angolo specifico con Aspose.PSD per Java

## Introduzione

Se hai bisogno di **come ruotare un'immagine** programmaticamente in un'applicazione Java, Aspose.PSD per Java offre un'API pulita e ad alte prestazioni che si occupa del lavoro pesante. Che tu stia creando un editor fotografico, generando miniature o preparando risorse per un servizio web, ruotare un'immagine di un grado esatto è una necessità comune. In questo tutorial percorreremo l'intero processo — dal caricamento di un file PSD al salvataggio del risultato ruotato — evidenziando le migliori pratiche come la cache e la gestione dello sfondo.

> **Risposte rapide**  
> - **Quale libreria è la migliore per ruotare immagini in Java?** Aspose.PSD per Java.  
> - **Posso ruotare di qualsiasi grado?** Sì, il metodo `rotate` accetta un angolo `float` (positivo o negativo).  
> - **È necessaria una licenza per lo sviluppo?** Una prova gratuita è sufficiente per i test; è richiesta una licenza per la produzione.  
> - **Quali formati immagine sono supportati?** PSD, JPEG, PNG, TIFF, GIF, BMP e molti altri.  
> - **Come impostare un colore di sfondo per lo spazio vuoto?** Passa un'istanza `Color` al metodo `rotate`.

## Che cos'è la rotazione di immagine in Java?

La rotazione di immagine significa girare la matrice di pixel attorno a un punto di pivot (di solito il centro) di un determinato angolo. In Java, puoi ottenerla manualmente con `Graphics2D`, ma Aspose.PSD astrae i calcoli, gestisce diverse profondità di colore e preserva le informazioni dei livelli quando lavori con file PSD.

## Perché usare Aspose.PSD per ruotare le immagini?

- **Precisione:** Ruota di qualsiasi frazione di grado senza perdita di qualità.  
- **Prestazioni:** La cache integrata (`image.cacheData()`) velocizza i file di grandi dimensioni.  
- **Controllo dello sfondo:** Specifica un colore di sfondo per riempire gli spazi vuoti creati dalla rotazione.  
- **Flessibilità di formato:** Carica PSD, esporta JPEG, PNG o qualsiasi formato supportato.

## Prerequisiti

Prima di iniziare, assicurati di avere quanto segue:

1. **Java Development Kit (JDK 8 o successivo)** – un IDE Java funzionante o un ambiente da riga di comando.  
2. **Aspose.PSD per Java** – scarica l'ultimo JAR dalla [pagina Aspose.PSD Java](https://reference.aspose.com/psd/java/).  
3. **File PSD di esempio** – ad es. `sample.psd` posizionato in una cartella a cui puoi fare riferimento dal tuo codice.

## Importare i pacchetti

Per prima cosa, importa le classi di cui avremo bisogno. Queste importazioni rimangono invariate indipendentemente dall'angolo di rotazione scelto.

```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.imageoptions.JpegOptions;
```

## Guida passo‑passo

### Passo 1: Definisci la directory del documento

Imposta la cartella che contiene il PSD di origine e dove verrà scritto l'output.

```java
String dataDir = "Your Document Directory";
```

> **Consiglio professionale:** Usa un percorso assoluto o `System.getProperty("user.dir")` per evitare sorprese con i percorsi relativi.

### Passo 2: Specifica i percorsi dei file di origine e destinazione

```java
String sourceFile = dataDir + "sample.psd";
String destName = dataDir + "RotatingImageOnSpecificAngle_out.jpg";
```

Puoi cambiare `destName` con qualsiasi estensione supportata (`.png`, `.tiff`, ecc.) a seconda delle tue esigenze di output.

### Passo 3: Carica l'immagine

```java
RasterImage image = (RasterImage)Image.load(sourceFile);
```

`Image.load` rileva automaticamente il formato del file e restituisce un `RasterImage` concreto per le operazioni raster.

### Passo 4: Cache dei dati immagine (opzionale ma consigliato)

```java
if (!image.isCached())
{
    image.cacheData();
}
```

La cache memorizza i pixel dell'immagine in memoria, velocizzando le trasformazioni successive — particolarmente utile per file PSD di grandi dimensioni.

### Passo 5: Ruota l'immagine

```java
image.rotate(20f, true, Color.getRed());
```

- **20f** – l'angolo di rotazione in gradi (float). Modifica questo valore per ruotare di qualsiasi angolo, ad es. `-45f` per la rotazione antioraria.  
- **true** – mantieni il rapporto d'aspetto originale espandendo la tela per contenere l'immagine ruotata.  
- **Color.getRed()** – colore di sfondo che riempie gli angoli vuoti creati dalla rotazione. Sostituiscilo con `Color.getWhite()` o qualsiasi colore personalizzato secondo necessità.

### Passo 6: Salva il risultato

```java
image.save(destName, new JpegOptions());
```

`JpegOptions` ti consente di controllare qualità, compressione e altre impostazioni specifiche per JPEG. Per un output senza perdita, sostituiscilo con `PngOptions`.

## Problemi comuni e soluzioni

| Problema | Causa | Soluzione |
|----------|-------|-----------|
| **Angoli vuoti dopo la rotazione** | Nessun colore di sfondo fornito | Passa un `Color` (es. `Color.getWhite()`) a `rotate`. |
| **Errore out‑of‑memory su PSD grandi** | Immagine non cached | Chiama `image.cacheData()` prima dell'elaborazione. |
| **Direzione dell'angolo errata** | Confusione tra angolo negativo e positivo | Usa valori negativi per la rotazione in senso orario (o viceversa a seconda del tuo sistema di coordinate). |
| **Modifiche non salvate** | Dimenticato di chiamare `save` | Assicurati che `image.save(...)` venga eseguito dopo la rotazione. |

## Domande frequenti

**D: Posso ruotare immagini con trasparenza usando Aspose.PSD per Java?**  
R: Sì. La libreria preserva i canali alfa; evita di specificare un colore di sfondo opaco se desideri angoli trasparenti.

**D: Ci sono limitazioni sui formati di file immagine supportati per la rotazione?**  
R: No. Aspose.PSD supporta PSD, JPEG, PNG, TIFF, GIF, BMP, JPEG2000, WMF, EMF e molti altri.

**D: Posso ruotare le immagini di un angolo negativo?**  
R: Assolutamente. Passa un float negativo a `rotate` (es. `-30f`) per ruotare in senso orario.

**D: Aspose.PSD fornisce un'anteprima in tempo reale durante la rotazione?**  
R: L'API è solo lato server. Per anteprime live, integra il bitmap ruotato in un framework UI (Swing, JavaFX) e aggiorna la vista.

**D: Esiste un forum della community per Aspose.PSD dove posso chiedere aiuto?**  
R: Sì, visita il [forum Aspose.PSD](https://forum.aspose.com/c/psd/34) per porre domande e condividere esperienze.

## Conclusione

Ora sai **come ruotare un'immagine** di un angolo specifico usando Aspose.PSD per Java. Sfruttando la cache, il controllo del colore di sfondo e le opzioni di output flessibili, puoi integrare una funzionalità di rotazione precisa in qualsiasi flusso di lavoro di immagini basato su Java.

---

**Ultimo aggiornamento:** 2025-12-08  
**Testato con:** Aspose.PSD per Java 24.11 (ultima versione al momento della stesura)  
**Autore:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}