---
date: 2026-02-17
description: Scopri come esportare i file PSD in PNG e gestire i flussi di immagini
  non compressi con Aspose.PSD per Java.
linktitle: Handle Uncompressed Image Stream Object in PSD - Java
second_title: Aspose.PSD Java API
title: Esporta PSD in PNG – Crea oggetto grafico PSD – Flusso non compresso in Java
url: /it/java/advanced-psd-layer-features-effects/handle-uncompressed-image-stream-object-psd/
weight: 26
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Esporta PSD in PNG – Crea oggetto grafico PSD – Flusso non compresso in Java

## Introduzione
Benvenuti nel mondo della manipolazione delle immagini in Java! In questo tutorial **creerete un oggetto grafico PSD**, gestirete oggetti di flusso immagine non compressi e imparerete a **esportare PSD in PNG** usando Aspose.PSD per Java. Che siate designer grafici alla ricerca di automatizzare i vostri flussi di lavoro o sviluppatori software desiderosi di integrare potenti capacità di elaborazione delle immagini nelle vostre applicazioni, questa guida è pensata proprio per voi. Vi guideremo passo passo, dai prerequisiti all’esportazione finale, assicurandoci che comprendiate a fondo l’intero processo.

## Risposte rapide
- **Cosa significa “creare oggetto grafico PSD”?** Indica l'istanziazione di un contesto grafico per un file PSD così da poter disegnare o modificare il suo contenuto.  
- **Quale libreria gestisce i flussi non compressi?** Aspose.PSD per Java fornisce pieno supporto per dati immagine grezzi (non compressi).  
- **Posso esportare PSD in PNG dopo la modifica?** Sì—una volta ottenuto un oggetto `Graphics` potete renderizzare il PSD e salvarlo come PNG.  
- **È necessaria una licenza per lo sviluppo?** Una versione di prova gratuita è sufficiente per i test; per la produzione è richiesta una licenza commerciale.  
- **L’esportazione è senza perdita?** L’esportazione in PNG preserva la qualità dell’immagine, mentre la dimensione del file è maggiore rispetto a JPEG ma inferiore a un PSD non compresso.  

## Come esportare PSD in PNG usando Aspose.PSD per Java
Quando dovete **esportare PSD in PNG**, il flusso di lavoro tipico è:

1. Caricare il file PSD (o crearne uno).  
2. Eseguire eventuali disegni o manipolazioni di livello con un oggetto `Graphics`.  
3. Salvare l’immagine risultante usando `PngOptions` (la stessa istanza di `Graphics` può essere riutilizzata).  

Anche se questo tutorial si concentra sulla gestione dei flussi non compressi, lo stesso oggetto `Graphics` che create può essere riutilizzato più tardi nella pipeline per renderizzare il PSD in un file PNG.

## Prerequisiti
Prima di immergerci nel codice, assicuriamoci di avere tutto il necessario per iniziare questo percorso. Ecco i prerequisiti:

### Java Development Kit (JDK)
Assicuratevi di avere il JDK installato sulla vostra macchina. Potete scaricarlo dal sito di Oracle o utilizzare OpenJDK.

### Aspose.PSD per Java
È necessario scaricare e installare la libreria Aspose.PSD. Questa potente libreria consente di manipolare i file PSD con facilità. Potete ottenere l’ultima versione da [questo link](https://releases.aspose.com/psd/java/).

### Integrated Development Environment (IDE)
È consigliabile utilizzare un IDE per scrivere e testare il codice Java. Potete usare IntelliJ IDEA, Eclipse o qualsiasi altro ambiente a vostra preferenza.

### Conoscenza di base di Java
Una familiarità con la programmazione Java renderà il processo più fluido. Assicuratevi di conoscere le basi, come classi, metodi e gestione delle eccezioni.

Con tutto pronto, arrotoliamoci le maniche e passiamo alla parte più entusiasmante: il coding!

## Importare i pacchetti
Per iniziare, dobbiamo importare i pacchetti necessari per lavorare con Aspose.PSD. Di seguito trovate gli import tipici per la gestione dei file PSD.

```java
import com.aspose.psd.Graphics;
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.CompressionMethod;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.PsdOptions;
import java.io.ByteArrayInputStream;
import java.io.ByteArrayOutputStream;
```

Ora, suddivideremo il codice in passaggi digeribili per assicurarci che possiate seguirlo facilmente. Imposteremo, caricheremo un file PSD, lo manipoleremo e salveremo il risultato.

## Passo 1: Definire la directory del documento
Prima di scrivere il codice, dovrete definire dove si trova il vostro file PSD. Questo è essenzialmente il punto di partenza per il progetto.

```java
String dataDir = "Your Document Directory";
```

Sostituite `"Your Document Directory"` con il percorso reale dove è collocato il vostro file PSD (ad esempio, `layers.psd`). Questo facilita il reperimento dei file senza problemi.

## Passo 2: Creare un ByteArrayOutputStream
Avrete bisogno di un luogo dove memorizzare l’immagine modificata prima di fare qualsiasi altra operazione. Un `ByteArrayOutputStream` vi aiuterà a catturare facilmente i dati dell’immagine.

```java
ByteArrayOutputStream ms = new ByteArrayOutputStream();
```

Questa riga inizializza un nuovo oggetto `ByteArrayOutputStream` chiamato `ms`. Lo utilizzerete per salvare la vostra immagine non compressa.

## Passo 3: Caricare il file PSD
È ora di caricare il vero file PSD. Qui inizia la magia!

```java
PsdImage psdImage = (PsdImage) Image.load(dataDir + "layers.psd");
```

Questa riga carica il vostro file PSD in un oggetto `PsdImage`. Assicuratevi di avere il percorso corretto; altrimenti comparirà un errore come un quiz inatteso.

## Passo 4: Configurare le PsdOptions per il salvataggio
Dovete specificare come volete salvare l’immagine — naturalmente non compressa!

```java
PsdOptions saveOptions = new PsdOptions();
saveOptions.setCompressionMethod(CompressionMethod.Raw);
```

Qui create un oggetto `PsdOptions` e impostate il metodo di compressione su `Raw`. Questo metodo garantisce che l’immagine mantenga la massima qualità e venga salvata senza alcuna compressione.

## Passo 5: Salvare l’immagine nello stream di output
```java
psdImage.save(ms, saveOptions);
```

Questa riga salva l’immagine modificata nello `ByteArrayOutputStream` creato nel Passo 2, usando le opzioni definite nel Passo 4. Il metodo `save` si occupa di codificare correttamente l’immagine in base alle impostazioni.

## Passo 6: Resettare lo stream di output
Dopo il salvataggio, lo stream di output si trova alla fine. Dovete resettarlo per leggere dall’inizio.

```java
ms.reset();
```

Il metodo `reset` prepara il vostro `ByteArrayOutputStream` per la lettura dall’inizio. Pensatelo come riavvolgere un nastro prima di ascoltare la vostra canzone preferita!

## Passo 7: Caricare l’immagine appena creata
```java
PsdImage img = (PsdImage) Image.load(new ByteArrayInputStream(ms.toByteArray()));
```

Qui carichiamo nuovamente l’immagine dallo `ByteArrayOutputStream` in un nuovo oggetto `PsdImage`. È il momento di verificare i risultati del lavoro svolto in precedenza.

## Passo 8: Creare l’oggetto Graphics
Per modificare ulteriormente o renderizzare l’immagine, dovrete creare un oggetto graphics.

```java
Graphics graphics = new Graphics(psdImage);
```

Questa riga inizializza un oggetto `Graphics` usando il vostro `psdImage`. Ora potete utilizzare questo oggetto graphics per disegnare o manipolare l’immagine secondo necessità. È come avere un pennello in mano!

## Manipolare i livelli PSD con l’oggetto Graphics
Ora che disponete di un'istanza **Graphics**, potete **manipolare i livelli PSD** — ad esempio, disegnare forme, aggiungere testo o applicare filtri a un livello specifico. Il contesto grafico opera direttamente sui dati pixel sottostanti, offrendovi un controllo granulare sull’aspetto di ciascun livello.

## Problemi comuni e soluzioni
- **NullPointerException durante il caricamento del file** – ricontrollate il percorso `dataDir` e assicuratevi che il nome del file sia corretto.  
- **Output compresso nonostante l’uso di Raw** – verificate che `saveOptions.setCompressionMethod(CompressionMethod.Raw);` sia chiamato prima del metodo `save`.  
- **L’oggetto Graphics appare vuoto** – assicuratevi di disegnare sul corretto istanza di `PsdImage` (usate quella caricata, non quella appena creata, a meno che non sia intenzionale).

## FAQ
### Cos’è Aspose.PSD?
Aspose.PSD è una libreria .NET che consente agli sviluppatori di creare, modificare e manipolare file Photoshop PSD e formati immagine correlati in modo programmatico.

### Come posso scaricare Aspose.PSD per Java?
Potete scaricarla dalla [pagina di rilascio](https://releases.aspose.com/psd/java/).

### Esiste una versione di prova gratuita per Aspose.PSD?
Sì, potete ottenere una versione di prova gratuita da [qui](https://releases.aspose.com/).

### Posso ottenere supporto per Aspose.PSD?
Assolutamente! Potete chiedere aiuto sul [forum di supporto Aspose](https://forum.aspose.com/c/psd/34).

### Come posso ottenere una licenza temporanea per Aspose.PSD?
Visitate la [pagina della licenza temporanea](https://purchase.aspose.com/temporary-license/) per iniziare.

## Domande frequenti

**D: Posso usare l’oggetto graphics per modificare solo un livello specifico?**  
R: Sì. Dopo aver caricato il PSD, selezionate il livello desiderato tramite `psdImage.getLayers().get_Item(index)` e passatelo al costruttore di `Graphics`.

**D: Il metodo di compressione Raw influisce sulla dimensione del file?**  
R: Raw memorizza i dati pixel senza compressione, quindi la dimensione del file sarà maggiore rispetto ai PSD compressi, ma la qualità dell’immagine rimane intatta.

**D: È possibile esportare il PSD modificato in un altro formato (ad es., PNG)?**  
R: Certamente. Utilizzate l’overload appropriato di `Image.save` con `PngOptions` dopo la modifica — questo è il modo standard per **esportare PSD in PNG**.

**D: Quale versione di Java è richiesta?**  
R: Aspose.PSD per Java supporta JDK 8 e versioni successive.

**D: Come libero le risorse dopo l’elaborazione?**  
R: Chiamate `psdImage.dispose()` e chiudete eventuali stream per liberare le risorse native.

---

**Ultimo aggiornamento:** 2026-02-17  
**Testato con:** Aspose.PSD per Java (ultima versione)  
**Autore:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}