---
date: 2026-02-12
description: Scopri come ruotare un'immagine di un angolo specifico in Java usando
  Aspose.PSD. Questa guida mostra come ruotare l'immagine, ruotare l'immagine di gradi
  e gestire i colori di sfondo.
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

Se hai bisogno di **come ruotare l'immagine** programmaticamente in un'applicazione Java, Aspose.PSD per Java offre un'API pulita e ad alte prestazioni che si occupa del lavoro pesante. Che tu stia costruendo un editor fotografico, generando miniature o preparando risorse per un servizio web, ruotare un'immagine di un grado esatto è una necessità comune. In questo tutorial percorreremo l'intero processo—dal caricamento di un file PSD al salvataggio del risultato ruotato—e metteremo in evidenza le migliori pratiche come la cache e la gestione dello sfondo.

## Risposte rapide
- **Qual è la libreria migliore per ruotare le immagini in Java?** Aspose.PSD for Java.  
- **Posso ruotare di qualsiasi grado?** Sì, il metodo `rotate` accetta un angolo di tipo `float` (positivo o negativo).  
- **Ho bisogno di una licenza per lo sviluppo?** Una prova gratuita è sufficiente per i test; è necessaria una licenza per la produzione.  
- **Quali formati immagine sono supportati?** PSD, JPEG, PNG, TIFF, GIF, BMP e molti altri.  
- **Come impostare un colore di sfondo per lo spazio vuoto?** Passare un'istanza `Color` al metodo `rotate`.

## Cos'è la rotazione dell'immagine in Java?

La rotazione dell'immagine significa ruotare la matrice di pixel attorno a un punto di pivot (di solito il centro) di un determinato angolo. In Java, puoi ottenere questo manualmente con `Graphics2D`, ma Aspose.PSD astrae la matematica, gestisce diverse profondità di colore e preserva le informazioni dei livelli quando lavori con file PSD.

## Perché usare Aspose.PSD per ruotare le immagini?

- **Precisione:** Ruota di qualsiasi frazione di grado senza perdita di qualità.  
- **Prestazioni:** La cache integrata (`image.cacheData()`) velocizza i file di grandi dimensioni.  
- **Controllo dello sfondo:** Specificare un colore di sfondo per riempire gli spazi vuoti creati dalla rotazione.  
- **Flessibilità di formato:** Carica PSD, esporta JPEG, PNG o qualsiasi formato supportato.

## Prerequisiti

Prima di iniziare, assicurati di avere quanto segue:

1. **Java Development Kit (JDK 8 o successivo)** – un IDE Java funzionante o un ambiente da riga di comando.  
2. **Aspose.PSD for Java** – scarica l'ultimo JAR dalla [pagina Aspose.PSD Java](https://reference.aspose.com/psd/java/).  
3. **File PSD di esempio** – ad esempio, `sample.psd` posizionato in una cartella a cui puoi fare riferimento dal tuo codice.

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

Puoi cambiare `destName` in qualsiasi estensione supportata (`.png`, `.tiff`, ecc.) a seconda delle tue esigenze di output.

### Passo 3: Carica l'immagine

```java
RasterImage image = (RasterImage)Image.load(sourceFile);
```

`Image.load` rileva automaticamente il formato del file e restituisce un `RasterImage` concreto per operazioni basate su raster.

### Passo 4: Cache dei dati dell'immagine (opzionale ma consigliato)

```java
if (!image.isCached())
{
    image.cacheData();
}
```

La cache memorizza i pixel dell'immagine in memoria, accelerando le trasformazioni successive—particolarmente utile per file PSD di grandi dimensioni.

### Passo 5: Ruota l'immagine

```java
image.rotate(20f, true, Color.getRed());
```

- **20f** – l'angolo di rotazione in gradi (float). Cambia questo valore per ruotare di qualsiasi angolo, ad esempio `-45f` per la rotazione in senso antiorario.  
- **true** – mantiene il rapporto d'aspetto originale espandendo la tela per adattare l'immagine ruotata.  
- **Color.getRed()** – colore di sfondo che riempie gli angoli vuoti creati dalla rotazione. Sostituiscilo con `Color.getWhite()` o qualsiasi colore personalizzato secondo necessità.

#### Ruota l'immagine di gradi in Java

Il metodo `rotate` accetta qualsiasi valore a virgola mobile, quindi puoi **ruotare l'immagine di gradi** come `30f`, `90f` o `-15f`. I valori positivi ruotano in senso orario, mentre i valori negativi ruotano in senso antiorario.

#### Angolo specifico di rotazione dell'immagine usando Aspose.PSD

Poiché il metodo utilizza un `float`, puoi specificare un **angolo specifico di rotazione dell'immagine** come `22.5f` per un controllo preciso nei flussi di lavoro di graphic design.

#### Riepilogo dell'esempio Java per ruotare l'immagine

Tutti i passaggi sopra mostrano un flusso di lavoro completo per **ruotare un'immagine in Java**—dalla lettura del file al salvataggio dell'output ruotato.

### Passo 6: Salva il risultato

```java
image.save(destName, new JpegOptions());
```

`JpegOptions` consente di controllare la qualità, la compressione e altre impostazioni specifiche per JPEG. Per un output senza perdita, sostituiscilo con `PngOptions`.

## Problemi comuni e soluzioni

| Problema | Causa | Soluzione |
|----------|-------|-----------|
| **Angoli vuoti dopo la rotazione** | Nessun colore di sfondo fornito | Passare un `Color` (ad es., `Color.getWhite()`) a `rotate`. |
| **Errore out‑of‑memory su PSD grandi** | Immagine non memorizzata nella cache | Chiamare `image.cacheData()` prima dell'elaborazione. |
| **Direzione dell'angolo errata** | Confusione tra angolo negativo e positivo | Usare valori negativi per la rotazione in senso orario (o vice‑versa a seconda del sistema di coordinate). |
| **Modifiche non salvate** | Dimenticare di chiamare `save` | Assicurarsi che `image.save(...)` venga eseguito dopo la rotazione. |

## Domande frequenti

**D: Posso ruotare immagini con trasparenza usando Aspose.PSD per Java?**  
R: Sì. La libreria preserva i canali alfa; basta non specificare un colore di sfondo opaco se desideri angoli trasparenti.

**D: Ci sono limitazioni sui formati di file immagine supportati per la rotazione?**  
R: No. Aspose.PSD supporta PSD, JPEG, PNG, TIFF, GIF, BMP, JPEG2000, WMF, EMF e molti altri.

**D: Posso ruotare le immagini di un angolo negativo?**  
R: Assolutamente. Passa un float negativo a `rotate` (ad es., `-30f`) per ruotare in senso orario.

**D: Aspose.PSD fornisce un'anteprima immagine in tempo reale durante la rotazione?**  
R: L'API è solo lato server. Per anteprime live, integra il bitmap ruotato in un framework UI (Swing, JavaFX) e aggiorna la vista.

**D: Esiste un forum della community per Aspose.PSD dove posso chiedere aiuto?**  
R: Sì, visita il [forum Aspose.PSD](https://forum.aspose.com/c/psd/34) per porre domande e condividere esperienze.

## Conclusione

Ora sai **come ruotare le immagini** di un angolo specifico usando Aspose.PSD per Java. Sfruttando la cache, il controllo del colore di sfondo e le opzioni di output flessibili, puoi integrare una funzionalità di rotazione precisa in qualsiasi flusso di lavoro di immagini basato su Java.

---

**Ultimo aggiornamento:** 2026-02-12  
**Testato con:** Aspose.PSD for Java 24.11 (ultima versione al momento della scrittura)  
**Autore:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}