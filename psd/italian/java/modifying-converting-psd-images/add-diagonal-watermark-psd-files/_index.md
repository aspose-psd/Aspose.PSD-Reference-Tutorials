---
date: 2026-03-04
description: Scopri come creare oggetti grafici in Java e aggiungere una filigrana
  diagonale ai file PSD utilizzando Aspose.PSD. Questa guida passo passo copre l'uso
  della libreria Java per le filigrane delle immagini.
linktitle: Add Diagonal Watermark to PSD Files with Java
second_title: Aspose.PSD Java API
title: Crea oggetto Graphics in Java – Filigrana diagonale per PSD
url: /it/java/modifying-converting-psd-images/add-diagonal-watermark-psd-files/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aggiungere filigrana diagonale ai file PSD con Java

## Introduzione
In questo tutorial **create graphics object java** e lo utilizzerai per aggiungere una filigrana diagonale ai file PSD. Che tu sia un designer che protegge le proprie opere o un marketer che brandizza le immagini, una filigrana pulita può far apparire il tuo lavoro professionale e sicuro. Ti guideremo passo passo con spiegazioni chiare, così potrai applicare rapidamente la tecnica nei tuoi progetti.

## Risposte rapide
- **Quale libreria mi serve?** Aspose.PSD for Java (una robusta java image watermark library).  
- **Quale parola chiave primaria copre questo tutorial?** create graphics object java.  
- **Ho bisogno di una licenza?** Una versione di prova gratuita è sufficiente per i test; è necessaria una licenza commerciale per la produzione.  
- **Posso modificare il testo e lo stile della filigrana?** Sì – puoi personalizzare font, colore, opacità e rotazione.  
- **Quali formati di output sono supportati?** L'esempio salva come PNG, ma Aspose.PSD può esportare in PSD, JPEG, BMP e altri.

## Cos'è un Graphics Object in Java?
Un oggetto **Graphics** rappresenta una superficie di disegno per un'immagine. Creando un graphics object, ottieni l'accesso a metodi che ti permettono di renderizzare testo, forme e altri elementi visivi direttamente sul bitmap o sulla tela PSD. Questo è il concetto fondamentale dietro la parola chiave primaria **create graphics object java**.

## Perché usare Aspose.PSD per la filigrana?
Aspose.PSD è una **java image watermark library** dedicata che funziona senza Adobe Photoshop. Ti offre il pieno controllo su livelli, rendering del testo e trasformazioni dell'immagine, rendendola ideale per elaborazioni lato server o operazioni batch.

## Prerequisiti
Prima di immergerci nel codice, assicurati di avere quanto segue:

### 1. Ambiente di sviluppo Java
Installa l'ultima JDK dal [Java website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).

### 2. Libreria Aspose.PSD
Scarica la libreria dalla [Aspose Downloads page](https://releases.aspose.com/psd/java/). Aggiungi il JAR al tuo progetto tramite Maven, Gradle o inclusione manuale nel classpath.

### 3. Conoscenza di base di Java
Familiarità con classi, oggetti e I/O di file ti aiuterà a seguire senza problemi.

### 4. Configurazione IDE
Usa IntelliJ IDEA, Eclipse o NetBeans per un'esperienza di codifica confortevole.

## Importare i pacchetti
Per manipolare i file PSD, importa le classi Aspose.PSD necessarie:

```java
import com.aspose.psd.Color;
import com.aspose.psd.Font;
import com.aspose.psd.Graphics;
import com.aspose.psd.Image;
import com.aspose.psd.Matrix;
import com.aspose.psd.PointF;
import com.aspose.psd.RectangleF;
import com.aspose.psd.StringAlignment;
import com.aspose.psd.StringFormat;
import com.aspose.psd.brushes.SolidBrush;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.PngOptions;
```

Ora che abbiamo sistemato i prerequisiti e importato i pacchetti necessari, procediamo passo passo per aggiungere una filigrana diagonale a un file PSD.

## Passo 1: Configura la tua directory
```java
String dataDir = "Your Document Directory";
```
Sostituisci `"Your Document Directory"` con il percorso della cartella che contiene il tuo file PSD di origine.

## Passo 2: Carica il file PSD
```java
PsdImage psdImage = (PsdImage)Image.load(dataDir + "layers.psd");
```
Il metodo `Image.load` legge il file e lo converte in un `PsdImage` così possiamo lavorare con le funzionalità specifiche di PSD.

## Passo 3: Crea un Graphics Object
```java
Graphics graphics = new Graphics(psdImage);
```
Qui **create graphics object java**—la superficie su cui disegneremo la filigrana.

## Passo 4: Crea un Font per la filigrana
```java
Font font = new Font("Arial", 20.0f);
```
Scegli qualsiasi font installato; la dimensione controlla quanto evidente appare la filigrana.

## Passo 5: Crea un Brush per la filigrana
```java
SolidBrush brush = new SolidBrush(Color.fromArgb(50, 128, 128, 128));
```
Il valore `alpha` (primo parametro) imposta la trasparenza. Un alpha di 50 fornisce un aspetto sottile, semi‑trasparente.

## Passo 6: Configura la matrice di trasformazione
```java
graphics.setTransform(new Matrix());
graphics.getTransform().rotateAt(45, new PointF(psdImage.getWidth() / 2, psdImage.getHeight() / 2));
```
Ruotiamo la superficie di disegno 45° attorno al centro dell'immagine, creando l'effetto diagonale.

## Passo 7: Definisci l'allineamento del testo
```java
StringFormat sf = new StringFormat();
sf.setAlignment(StringAlignment.Center);
```
L'allineamento centrale garantisce che la filigrana si posizioni correttamente al centro del rettangolo ruotato.

## Passo 8: Disegna la filigrana
```java
graphics.drawString("Some watermark text", font, brush, new RectangleF(0, psdImage.getHeight() / 2, psdImage.getWidth(), psdImage.getHeight() / 2), sf);
```
Sostituisci `"Some watermark text"` con il nome del tuo brand o l'avviso di copyright. Il rettangolo definisce dove viene renderizzato il testo.

## Passo 9: Salva l'immagine
```java
psdImage.save(dataDir + "AddDiagnolWatermark_output.png", new PngOptions());
```
L'output viene salvato come PNG, ma puoi scegliere qualsiasi formato supportato da Aspose.PSD.

## Casi d'uso comuni
- **Protezione del brand:** Aggiungi un logo semi‑trasparente per impedire il riutilizzo non autorizzato.  
- **Elaborazione batch:** Automatizza l'applicazione di filigrane per grandi librerie di immagini su un server.  
- **Anteprime creative:** Mostra bozze con filigrana ai clienti mantenendo intatti i file originali.

## Risoluzione dei problemi e consigli
- **Trasparenza non visibile?** Aumenta il valore alpha (es., `100`) per una filigrana più forte.  
- **La filigrana appare fuori centro?** Verifica che il punto di rotazione utilizzi la divisione esatta della larghezza/altezza dell'immagine.  
- **Problemi di prestazioni:** Riutilizza lo stesso oggetto `Graphics` quando elabori più immagini in un ciclo.

## FAQ
### Cos'è Aspose.PSD?
Aspose.PSD è una libreria Java utilizzata per lavorare con e manipolare file PSD senza richiedere Adobe Photoshop.

### Posso usare altri font per la filigrana?
Sì, puoi scegliere qualsiasi font installato sul tuo sistema per la filigrana.

### È possibile personalizzare la trasparenza della filigrana?
Assolutamente! Puoi regolare il valore alpha nello SolidBrush per modificare la trasparenza.

### Posso aggiungere più filigrane?
Sì, puoi chiamare il metodo `drawString` più volte con parametri diversi per aggiungere più filigrane.

### Dove posso trovare più informazioni su Aspose.PSD?
Puoi consultare la documentazione [qui](https://reference.aspose.com/psd/java/).

---

**Ultimo aggiornamento:** 2026-03-04  
**Testato con:** Aspose.PSD 24.12 for Java  
**Autore:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}