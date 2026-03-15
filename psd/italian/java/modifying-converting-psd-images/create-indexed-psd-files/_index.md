---
date: 2026-03-15
description: Scopri come creare file PSD, generare la palette di colori PSD e impostare
  la modalità colore PSD utilizzando Aspose.PSD per Java in questa guida passo‑passo.
linktitle: Create Indexed PSD Files using Aspose.PSD for Java
second_title: Aspose.PSD Java API
title: Come creare file PSD usando Aspose.PSD per Java
url: /it/java/modifying-converting-psd-images/create-indexed-psd-files/
weight: 23
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Come creare file PSD usando Aspose.PSD per Java

## Introduzione
Se ti sei mai chiesto **come creare PSD** file programmaticamente, sei nel posto giusto. Aspose.PSD per Java ti dà il pieno controllo sui documenti Photoshop, permettendoti di generare, modificare e salvare file PSD senza aprire mai Photoshop. In questo tutorial vedremo come creare un **PSD indicizzato**, impostare la modalità colore del PSD e generare una palette di colori personalizzata—tutto con codice Java chiaro, passo dopo passo. Che tu stia costruendo una pipeline grafica, automatizzando la creazione di asset, o semplicemente sperimentando, i concetti qui ti aiuteranno a dare vita alle tue idee visive.

## Risposte rapide
- **Quale libreria serve?** Aspose.PSD per Java
- **Posso creare un PSD indicizzato?** Sì, impostando la modalità colore su `Indexed`
- **È necessario avere Photoshop installato?** No, Aspose.PSD funziona in modo indipendente
- **Quale versione di Java è richiesta?** JDK 8 o successiva
- **Quanto grande può essere la tela?** Qualsiasi dimensione; questo esempio usa 500 × 500 px

## Cos'è un file PSD indicizzato?
Un PSD indicizzato memorizza i colori in una palette anziché valori a colori completi per ogni pixel. Questo riduce le dimensioni del file ed è ideale per grafiche con colori limitati, come icone o asset UI. Generando una palette personalizzata controlli esattamente quali colori compaiono nell'immagine finale.

## Perché generare una palette di colori PSD?
Creare una **palette di colori PSD** ti permette di:
- Mantenere le dimensioni dei file ridotte per uso web o mobile  
- Garantire coerenza di branding limitando i colori alla tua palette aziendale  
- Accelerare il rendering in applicazioni che supportano immagini indicizzate  

## Prerequisiti
Prima di immergerci nel codice, assicurati di avere quanto segue:

1. **Conoscenza di base di Java** – dovresti sentirti a tuo agio con classi, metodi e creazione di oggetti.  
2. **Java Development Kit (JDK) 8+** – installato e configurato nel tuo IDE.  
3. **IDE (IntelliJ IDEA, Eclipse, ecc.)** – opzionale ma fortemente consigliato per un debug più semplice.  
4. **Libreria Aspose.PSD per Java** – scaricala **[qui](https://releases.aspose.com/psd/java/)** e aggiungi il JAR al classpath del tuo progetto.  
5. **Concetti fondamentali di graphic design** – la comprensione delle modalità colore, delle palette e delle forme di base ti aiuterà a seguire.  

## Importare i pacchetti
Prima di procedere con il codice, assicuriamoci di aver importato tutti i pacchetti necessari nella tua applicazione Java. Ecco ciò di cui avrai bisogno:

```java
import com.aspose.psd.Color;
import com.aspose.psd.Graphics;
import com.aspose.psd.Image;
import com.aspose.psd.Pen;
import com.aspose.psd.Rectangle;
import com.aspose.psd.fileformats.psd.ColorModes;
import com.aspose.psd.fileformats.psd.CompressionMethod;
import com.aspose.psd.fileformats.psd.PsdColorPalette;
import com.aspose.psd.imageoptions.PsdOptions;
import com.aspose.psd.sources.FileCreateSource;
```

Queste importazioni ti consentiranno di lavorare con le opzioni PSD, i colori e la manipolazione grafica tramite Aspose.PSD.

Ora, analizziamo il codice passo dopo passo per **come creare PSD** file con una modalità colore indicizzata.

## Passo 1: Configura la directory del documento
Prima, definisci dove verrà salvato il PSD generato.

```java
String dataDir = "Your Document Directory";
```

Sostituisci `"Your Document Directory"` con un percorso assoluto o relativo, ad esempio `"/Users/YourName/Documents/"`.

## Passo 2: Crea un'istanza di PsdOptions
`PsdOptions` contiene tutte le impostazioni per il file che stai per generare.

```java
PsdOptions createOptions = new PsdOptions();
```

## Passo 3: Imposta le proprietà principali di PsdOptions
Qui specifichiamo la destinazione di output, il **set psd color mode** a `Indexed`, e la versione PSD.

```java
createOptions.setSource(new FileCreateSource(dataDir + "Newsample_out.psd", false));
createOptions.setColorMode(ColorModes.Indexed);
createOptions.setVersion(5);
```

- **Source** – il percorso completo del nuovo file.  
- **Color Mode** – `Indexed` indica ad Aspose.PSD di usare un'immagine basata su palette.  
- **Version** – versione del formato PSD (5 funziona per la maggior parte delle versioni moderne di Photoshop).

## Passo 4: Creare una palette di colori (Generare una palette di colori PSD)
Definisci i colori che saranno disponibili nell'immagine indicizzata.

```java
Color[] palette = { Color.getRed(), Color.getGreen(), Color.getBlue(), Color.getYellow() };
createOptions.setPalette(new PsdColorPalette(palette));
createOptions.setCompressionMethod(CompressionMethod.RLE);
```

- L'array `palette` contiene fino a 256 oggetti `Color`.  
- `CompressionMethod.RLE` fornisce una compressione lossless efficiente per le immagini indicizzate.

## Passo 5: Creare la tela dell'immagine PSD
Ora creiamo un PSD vuoto con le dimensioni desiderate.

```java
Image psd = Image.create(createOptions, 500, 500);
```

Questo crea una tela di 500 × 500 pixel che utilizza la palette definita in precedenza.

## Passo 6: Disegnare grafica sul PSD
Aggiungi contenuto visivo—qui disegniamo una semplice ellisse rossa su sfondo bianco.

```java
Graphics graphics = new Graphics(psd);
graphics.clear(Color.getWhite());
graphics.drawEllipse(new Pen(Color.getRed(), 6), new Rectangle(0, 0, 400, 400));
```

- `clear(Color.getWhite())` riempie lo sfondo di bianco.  
- `drawEllipse` disegna un'ellisse rossa con un contorno di 6 pixel.

## Passo 7: Salvare il file PSD
Infine, persisti l'immagine su disco.

```java
psd.save();
```

Il file `Newsample_out.psd` apparirà nella directory specificata in precedenza.

## Problemi comuni e consigli
- **Dimensione palette** – Se hai bisogno di più di 4 colori, aggiungili semplicemente all'array `palette` (fino a 256).  
- **Permessi file** – Assicurati che il processo Java abbia accesso in scrittura a `dataDir`.  
- **Modalità colore errata** – Dimenticare `createOptions.setColorMode(ColorModes.Indexed)` produrrà un PSD RGB invece di uno indicizzato.  

## Domande frequenti

**D: Cos'è Aspose.PSD per Java?**  
A: Aspose.PSD per Java è una libreria che consente la manipolazione di file PSD (Photoshop) programmaticamente usando Java.

**D: Posso usare Aspose.PSD gratuitamente?**  
A: Sì, puoi accedere a una versione di prova gratuita di Aspose.PSD **[qui](https://releases.aspose.com/)**.

**D: È necessario avere Photoshop installato per lavorare con Aspose.PSD?**  
A: No, puoi creare e manipolare file PSD senza Photoshop, poiché Aspose.PSD gestisce tutte le operazioni in modo indipendente.

**D: Come ottengo una licenza temporanea per Aspose.PSD?**  
A: Puoi richiedere una licenza temporanea **[qui](https://purchase.aspose.com/temporary-license/)**.

**D: Dove posso ottenere supporto per Aspose.PSD?**  
A: Puoi ottenere supporto dal forum Aspose **[qui](https://forum.aspose.com/c/psd/34)**.

## Conclusione
Hai appena imparato **come creare PSD** file con una modalità colore indicizzata, generato una palette personalizzata e aggiunto grafica semplice—tutto usando Aspose.PSD per Java. Con questi blocchi di costruzione puoi espandere a disegni più complessi, gestione dei livelli e elaborazione batch. Per un'esplorazione più approfondita, consulta il riferimento API ufficiale **[qui](https://reference.aspose.com/psd/java/)** e continua a sperimentare con diverse palette e primitive di disegno.

---

**Last Updated:** 2026-03-15  
**Tested With:** Aspose.PSD for Java 24.12 (latest)  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}