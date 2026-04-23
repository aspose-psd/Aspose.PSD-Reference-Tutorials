---
date: 2026-03-07
description: Scopri come aggiungere testo ai file PSD in fase di esecuzione usando
  Java e Aspose.PSD. Segui questa guida passo‑passo per creare rapidamente un livello
  di testo in un PSD.
linktitle: Add Text Layer on Runtime in PSD Files using Java
second_title: Aspose.PSD Java API
title: Aggiungi testo ai file PSD in fase di esecuzione con Java
url: /it/java/modifying-converting-psd-images/add-text-layer-runtime-psd-files/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aggiungere testo ai file PSD a runtime usando Java

## Introduzione
Se hai mai modificato manualmente un documento Photoshop, sai quanto siano potenti i livelli. E se potessi **aggiungere testo a PSD** automaticamente dalla tua applicazione Java? Con la libreria Aspose.PSD for Java, puoi creare un livello di testo in un PSD a runtime, aprendo la porta a elaborazioni batch, generazione dinamica di grafiche e flussi di lavoro di branding automatizzati. In questo tutorial percorreremo l’intero processo, dalla configurazione del progetto al salvataggio del file aggiornato.

## Risposte rapide
- **Quale libreria è necessaria?** Aspose.PSD for Java.  
- **Posso aggiungere testo a un PSD esistente?** Sì – basta caricare il file, aggiungere un `TextLayer` e salvare.  
- **È necessaria una licenza per la produzione?** È richiesta una licenza commerciale per l’uso non‑valutativo.  
- **Quale versione di Java è supportata?** JDK 8 o superiore (consigliamo l’ultima LTS).  
- **È adatto per back‑end web?** Assolutamente – l’API funziona in qualsiasi ambiente server basato su Java.

## Che cosa significa “add text to PSD”?
Aggiungere testo a un PSD significa creare programmaticamente un nuovo livello di testo all’interno di un documento Photoshop. Il livello si comporta come qualsiasi altro livello di testo di Photoshop: puoi spostarlo, modificarne il contenuto e applicare stili, il tutto senza aprire Photoshop.

## Perché creare un livello di testo in un PSD con Java?
- **Automazione** – Genera asset di marketing, filigrane o etichette di prodotto in blocco.  
- **Coerenza** – Garantisce lo stesso font, dimensione e posizionamento su migliaia di file.  
- **Integrazione** – Combinalo con altri servizi Java (e‑commerce, reporting, pipeline CI) per fornire grafiche al volo.

## Prerequisiti
Prima di scrivere il codice, assicurati di avere:

1. **Java Development Kit (JDK)** – Installa JDK 8 o più recente. Puoi [scaricarlo qui](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).  
2. **Aspose.PSD for Java** – Scarica l’ultimo JAR dalla [pagina di rilascio di Aspose](https://releases.aspose.com/psd/java/).  
3. **IDE (opzionale ma utile)** – IntelliJ IDEA, Eclipse o qualsiasi editor tu preferisca.  
4. **Conoscenze di base di Java** – Dovresti sentirti a tuo agio con classi, oggetti e I/O di file.  
5. **Un PSD di esempio** – Per questa guida useremo `OneLayer.psd` posizionato in una cartella a tua scelta.

## Importare i pacchetti
Per prima cosa, importa le classi necessarie per lavorare con file PSD e livelli di testo.

```java
import com.aspose.psd.Image;
import com.aspose.psd.Rectangle;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.TextLayer;
```

Queste importazioni ti danno accesso alla funzionalità principale di Aspose.PSD.

## Guida passo‑passo

### Passo 1: Configurare la directory del documento
Definisci la cartella che contiene il tuo PSD di origine e dove verrà salvato l’output.

```java
String dataDir = "Your Document Directory"; 
```

Sostituisci `"Your Document Directory"` con il percorso assoluto o relativo ai tuoi file.

### Passo 2: Caricare il file PSD di origine
Carica il PSD esistente in memoria usando `Image.load()`.

```java
String sourceFileName = dataDir + "OneLayer.psd"; 
Image img = Image.load(sourceFileName);
```

Se il percorso è corretto, `img` ora rappresenta il documento Photoshop caricato.

### Passo 3: Cast a `PsdImage`
Poiché stiamo usando funzionalità specifiche di Photoshop, effettua il cast dell’`Image` generico a `PsdImage`.

```java
PsdImage im = (PsdImage)img;
```

Il cast sblocca metodi come `addTextLayer()`.

### Passo 4: Definire il rettangolo per il livello di testo
Specifica dove deve apparire il nuovo testo. Il rettangolo definisce posizione (x, y) e dimensione (larghezza, altezza).

```java
Rectangle rect = new Rectangle(
    (int)(im.getWidth() * 0.25),
    (int)(im.getHeight() * 0.25),
    (int)(im.getWidth() * 0.5),
    (int)(im.getHeight() * 0.5)
);
```

Sentiti libero di modificare i calcoli per adattarli alle tue esigenze di layout.

### Passo 5: Aggiungere il livello di testo
Crea il livello di testo all’interno del rettangolo definito.

```java
TextLayer layer = im.addTextLayer("Added text", rect);
```

Sostituisci `"Added text"` con qualsiasi stringa desideri far apparire nel PSD. Questo è dove **creiamo il livello di testo PSD** programmaticamente.

### Passo 6: Salvare il file PSD aggiornato
Scrivi il documento modificato in un nuovo file così da non sovrascrivere l’originale.

```java
String psdPath = dataDir + "ImageWithTextLayer.psd";
im.save(psdPath);
```

Dopo l’esecuzione, troverai `ImageWithTextLayer.psd` nella cartella di destinazione, ora contenente il nuovo livello di testo.

## Problemi comuni e soluzioni
| Problema | Motivo | Soluzione |
|----------|--------|-----------|
| **`NullPointerException` su `im.addTextLayer`** | PSD non caricato correttamente (percorso errato). | Verifica che `sourceFileName` punti a un PSD esistente. |
| **Testo non visibile** | Rettangolo posizionato fuori dalla tela o livello nascosto. | Regola le coordinate del rettangolo o controlla la visibilità del livello con `layer.setVisible(true)`. |
| **LicenseException** | Uso della libreria senza licenza valida in produzione. | Acquista una licenza commerciale e impostala tramite `License license = new License(); license.setLicense("Aspose.PSD.lic");`. |

## Domande frequenti

**Q: Posso aggiungere più livelli di testo?**  
A: Sì – basta ripetere i Passi 4 e 5 per ogni pezzo di testo da inserire.

**Q: Come posso stilizzare il testo (font, dimensione, colore)?**  
A: La classe `TextLayer` espone il metodo `getTextData()` dove puoi modificare `Font`, `FontSize`, `Color` e altre proprietà di stile. Consulta la documentazione API di Aspose.PSD per tutti i dettagli.

**Q: E se il mio PSD ha già molti livelli?**  
A: Aspose.PSD gestisce strutture di livello complesse. Puoi mirare a gruppi specifici o inserire il nuovo livello di testo in un indice desiderato usando le overload di `addTextLayer`.

**Q: Questo approccio è adatto per applicazioni web?**  
A: Assolutamente. Finché il tuo server esegue Java, puoi generare o modificare PSD al volo e servirli ai client.

**Q: Dove posso ottenere aiuto se incontro problemi?**  
A: Visita i [forum di supporto Aspose](https://forum.aspose.com/c/psd/34) dove sia la community sia gli ingegneri di Aspose possono assisterti.

## Conclusione
Ora hai visto quanto sia semplice **aggiungere testo a PSD** a runtime usando Java e Aspose.PSD. Questa tecnica ti consente di automatizzare la creazione di grafiche, personalizzare asset e integrare modifiche di livello Photoshop in qualsiasi soluzione basata su Java. Esplora il resto dell’API Aspose.PSD per aggiungere forme, livelli raster o persino applicare filtri per un’automazione ancora più ricca.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Ultimo aggiornamento:** 2026-03-07  
**Testato con:** Aspose.PSD for Java 24.12 (latest at time of writing)  
**Autore:** Aspose  

---