---
date: 2026-03-26
description: Scopri come modificare i livelli di testo nei file PSD e cambiare il
  colore del testo PSD usando Aspose.PSD per Java. Una guida passo‑passo per sviluppatori
  e designer.
linktitle: Edit Text Layers PSD Files using Java
second_title: Aspose.PSD Java API
title: Modifica i livelli di testo dei file PSD con Java – Tutorial Aspose.PSD
url: /it/java/psd-image-modification-conversion/format-text-portions-psd-files/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Modifica i Livelli di Testo dei File PSD con Java

## Introduzione

Nel nostro mondo sempre più visuale, la possibilità di **modificare i livelli di testo PSD** programmaticamente può farti risparmiare ore di lavoro manuale. Che tu sia un designer che deve aggiornare in batch le grafiche o uno sviluppatore che costruisce un servizio dinamico di generazione di immagini, Aspose.PSD per Java ti offre il potere di modificare il testo PSD esattamente come faresti in Photoshop—solo con il codice. In questo tutorial percorreremo l’intero processo di modifica dei file PSD con livelli di testo, incluso come **cambiare il colore del testo PSD** per singole porzioni.

## Risposte Rapide
- **Quale libreria consente di modificare i livelli di testo PSD?** Aspose.PSD per Java  
- **È possibile cambiare il colore del testo PSD programmaticamente?** Sì, usando `ITextStyle.setFillColor`  
- **È necessaria una licenza per la produzione?** È richiesta una licenza commerciale; è disponibile una versione di prova gratuita.  
- **Quale versione di Java è supportata?** Java 8 e successive.  
- **È necessario gestire la memoria?** Sì—disporre del `PsdImage` dopo il salvataggio.

## Che cosa significa modificare i livelli di testo PSD?

Modificare i livelli di testo PSD significa accedere ai dati di testo memorizzati all’interno di un file Photoshop PSD, modificare i caratteri, gli stili o la formattazione, e poi scrivere tali modifiche nel file. Questa capacità è essenziale per automatizzare aggiornamenti di brand, creare grafiche localizzate o generare asset di marketing personalizzati senza interazione manuale con Photoshop.

## Perché modificare i livelli di testo PSD con Aspose.PSD?

- **Controllo totale** – Cambia font, colori, allineamento e persino aggiungi o rimuovi porzioni di testo.  
- **Cross‑platform** – Funziona su qualsiasi OS che supporta Java.  
- **Nessun Photoshop necessario** – Esegui operazioni batch su un server o in una pipeline CI.  
- **Alta fedeltà** – Conserva gli effetti di livello, le maschere e le altre funzionalità PSD.

## Prerequisiti

Prima di passare al codice, assicurati di avere quanto segue:

1. **Java Development Kit (JDK)** – Java 8+ installato e configurato.  
2. **Aspose.PSD per Java Library** – Scaricala da [qui](https://releases.aspose.com/psd/java/) o inizia con una [versione di prova gratuita](https://releases.aspose.com/).  
3. **IDE per sviluppo Java** – IntelliJ IDEA, Eclipse o NetBeans, con il JAR di Aspose.PSD aggiunto al classpath del progetto.  
4. **Conoscenze di base di Java** – Familiarità con oggetti, cicli e gestione delle eccezioni.

## Importazione dei Pacchetti Necessari

Quando usi Aspose.PSD per Java, devi importare i pacchetti specifici per accedere alle classi e ai metodi che utilizzerai. Ecco quali:

```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.Layer;
import com.aspose.psd.fileformats.psd.layers.TextLayer;
import com.aspose.psd.fileformats.psd.layers.text.ITextPortion;
import com.aspose.psd.fileformats.psd.layers.text.ITextStyle;
import com.aspose.psd.imageoptions.PsdOptions;
import com.aspose.psd.internal.Exceptions.Exception;
```

Queste importazioni ti danno accesso alle funzionalità essenziali di Aspose.PSD necessarie nel nostro esempio.

## Passo 1: Definisci le Tue Directory

Prima di iniziare a lavorare con il file PSD, dobbiamo definire dove si trova il nostro file PSD sorgente e dove vogliamo salvare il file modificato.

```java
String sourceDir = "Your Source Directory";
String outputDir = "Your Document Directory";
String inPsdFilePath = sourceDir + "ThreeColorsParagraphs.psd";
String outPsdFilePath = outputDir + "ThreeColorsParagraph_out.psd";
```

Sostituisci i percorsi segnaposto con le posizioni effettive sul tuo computer.

## Passo 2: Carica il File PSD

Il passo successivo è caricare il file PSD con cui vuoi lavorare. Aspose rende questo processo molto semplice.

```java
PsdImage psdImage = (PsdImage) Image.load(inPsdFilePath);
```

`Image.load` apre il file così possiamo iniziare a ispezionare i suoi livelli.

## Passo 3: Scorri i Livelli

Una volta caricato il file PSD, è il momento di approfondire i suoi livelli. Non tutti i livelli contengono testo, e noi vogliamo trovare solo i livelli di testo. Filtriamoli:

```java
for (Layer layer : psdImage.getLayers()) {
    if (!(layer instanceof TextLayer)) {
        continue;
    }
    // Process only text layers…
}
```

Il ciclo itera su ogni livello, e saltiamo quelli che non sono istanze di `TextLayer`.

## Passo 4: Accedi alle Porzioni di Testo

Dopo aver identificato un livello di testo, possiamo accedere alle sue porzioni di testo per modificarle. È qui che inizia la magia!

```java
TextLayer textLayer = (TextLayer) layer;
ITextPortion[] portions = textLayer.getTextData().getItems();
```

Considera le porzioni di testo come le singole parole o frasi che puoi modificare in modo indipendente.

## Passo 5: Modifica le Porzioni di Testo

Ora, modifichiamo il testo. Cambieremo il testo esistente, rimuoveremo alcune porzioni e ne aggiungeremo di nuove:

```java
portions[0].setText("Hello ");
portions[1].setText("World");
// Removing text portions
textLayer.getTextData().removePortion(3);
textLayer.getTextData().removePortion(2);
// Adding new text portion
ITextPortion createdPortion = textLayer.getTextData().producePortion();
createdPortion.setText("!!!\r");
textLayer.getTextData().addPortion(createdPortion);
```

Vedi quanto è semplice riscrivere o eliminare parti del paragrafo.

## Passo 6: Allinea e Stila il Testo

Dopo aver modificato il testo, potremmo voler regolare lo stile. Sei pronto per un restyling? Regoliamo l’allineamento e i colori del testo:

```java
// Set right justification
portions[0].getParagraph().setJustification(1); // Right
portions[1].getParagraph().setJustification(1);
portions[2].getParagraph().setJustification(1);

// Set fill colors individually
portions[0].getStyle().setFillColor(Color.getAquamarine());
portions[1].getStyle().setFillColor(Color.getViolet());
portions[2].getStyle().setFillColor(Color.getLightBlue());
```

Qui **cambiamo il colore del testo PSD** per ogni porzione impostando un diverso `fillColor`. Questo conferisce a ogni parola una propria identità visiva.

## Passo 7: Aggiorna i Dati del Livello

Dopo aver effettuato tutte queste modifiche, dobbiamo assicurarci che siano riflesse nei dati del livello:

```java
textLayer.getTextData().updateLayerData();
```

Questa chiamata conferma le modifiche nella struttura PSD sottostante.

## Passo 8: Salva il File PSD Modificato

Infine, salviamo le modifiche apportate al file PSD:

```java
psdImage.save(outPsdFilePath, new PsdOptions(psdImage));
```

Specifica il percorso di output dove vuoi che il file modificato venga scritto.

## Passo 9: Rilascia le Risorse

Per mantenere basso l’utilizzo di memoria, rilascia sempre le risorse dell’immagine quando hai finito:

```java
finally {
    psdImage.dispose();
}
```

Pulire le risorse evita perdite di memoria, specialmente quando si elaborano molti file in batch.

## Problemi Comuni e Soluzioni

| Problema | Motivo | Correzione |
|----------|--------|------------|
| **NullPointerException su `portions[2]`** | Il PSD sorgente ha meno di tre porzioni. | Verifica il numero di porzioni con `portions.length` prima di accedere agli indici. |
| **I colori non vengono applicati** | Uso di una versione obsoleta di Aspose.PSD. | Aggiorna all’ultima release di Aspose.PSD per Java. |
| **File non trovato** | Percorso errato in `sourceDir` o `outputDir`. | Usa percorsi assoluti o ricontrolla i percorsi relativi. |
| **Licenza non impostata** | La versione di prova può aggiungere filigrane. | Applica una licenza valida con `License license = new License(); license.setLicense("Aspose.PSD.lic");` |

## Domande Frequenti

### Che cos’è Aspose.PSD per Java?
Aspose.PSD per Java è una libreria che consente agli sviluppatori di manipolare e lavorare con i file Photoshop PSD in modo programmatico.

### Posso usare Aspose.PSD gratuitamente?
Sì, puoi iniziare con una versione di prova gratuita disponibile sul sito Aspose prima di decidere di acquistare.

### Quali prerequisiti sono necessari?
Hai bisogno del Java Development Kit (JDK) installato, della libreria Aspose.PSD e di conoscenze di base della programmazione Java.

### Ci sono limitazioni nella versione di prova?
Sì, la versione di prova può avere alcune limitazioni riguardo alle funzionalità disponibili, come filigrane o utilizzo limitato.

### Dove posso trovare ulteriori informazioni su Aspose.PSD?
Puoi consultare la documentazione per scenari d’uso dettagliati e riferimenti API [qui](https://reference.aspose.com/psd/java/).

---

**Ultimo aggiornamento:** 2026-03-26  
**Testato con:** Aspose.PSD per Java 24.12  
**Autore:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}