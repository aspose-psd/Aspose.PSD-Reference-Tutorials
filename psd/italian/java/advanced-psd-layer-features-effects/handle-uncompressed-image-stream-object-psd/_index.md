---
date: 2025-12-13
description: Scopri come creare oggetti grafici PSD e manipolare i livelli PSD gestendo
  flussi di immagini non compressi con Aspose.PSD per Java.
linktitle: Handle Uncompressed Image Stream Object in PSD - Java
second_title: Aspose.PSD Java API
title: Crea oggetto grafico PSD – Flusso non compresso in Java
url: /it/java/advanced-psd-layer-features-effects/handle-uncompressed-image-stream-object-psd/
weight: 26
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Crea oggetto grafico PSD – Flusso non compresso in Java

## Introduzione
Benvenuto nel mondo della manipolazione delle immagini in Java! In questo tutorial **creerai un oggetto grafico PSD** e gestirai oggetti di flusso immagine non compressi utilizzando Aspose.PSD per Java. Che tu sia un grafico che desidera automatizzare i propri flussi di lavoro o uno sviluppatore che vuole integrare potenti capacità di elaborazione delle immagini nelle proprie applicazioni, questa guida è pensata proprio per te. Ti guideremo passo passo, dalle premesse alla conclusione, assicurandoci che tu abbia una solida comprensione di come iniziare con Aspose.PSD.

## Risposte rapide
- **What does “create PSD graphics object” mean?** Si riferisce all'istanziazione di un contesto grafico per un file PSD in modo da poter disegnare o modificare il suo contenuto.  
- **Which library handles uncompressed streams?** Aspose.PSD per Java fornisce supporto completo per dati immagine grezzi (non compressi).  
- **Do I need a license for development?** Una versione di prova gratuita è sufficiente per i test; è necessaria una licenza commerciale per la produzione.  
- **Can I manipulate PSD layers after creating the graphics object?** Sì – l'istanza Graphics ti permette di disegnare su qualsiasi layer.  

## Prerequisiti
Prima di tuffarci nel codice, assicuriamoci che tu abbia tutto il necessario per iniziare questo percorso. Ecco i prerequisiti:

### Java Development Kit (JDK)
Assicurati di avere il JDK installato sulla tua macchina. Puoi scaricarlo dal sito di Oracle o utilizzare OpenJDK.

### Aspose.PSD for Java
Devi scaricare e installare la libreria Aspose.PSD. Questa potente libreria ti consente di manipolare i file PSD facilmente. Puoi ottenere l'ultima versione da [questo link](https://releases.aspose.com/psd/java/).

### Integrated Development Environment (IDE)
È consigliabile utilizzare un IDE per scrivere e testare il tuo codice Java. Puoi usare IntelliJ IDEA, Eclipse o qualsiasi altro che preferisci.

### Basic Understanding of Java
Una buona familiarità con la programmazione Java renderà il processo più fluido. Assicurati di conoscere le basi come classi, metodi e gestione delle eccezioni.

Con tutto pronto, arrotoliamo le maniche e passiamo alla parte più entusiasmante – il coding!

## Importa pacchetti
Per iniziare, dobbiamo importare i pacchetti necessari per lavorare con Aspose.PSD. Di seguito trovi gli import tipicamente richiesti per gestire i file PSD.

```java
import com.aspose.psd.Graphics;
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.CompressionMethod;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.PsdOptions;
import java.io.ByteArrayInputStream;
import java.io.ByteArrayOutputStream;
```

Ora, suddivideremo il codice in passaggi digeribili per assicurarti di poter seguire facilmente. Configureremo, caricheremo un file PSD, lo manipoleremo e salveremo il risultato.

## Passo 1: Definisci la directory del documento
Prima di iniziare a scrivere codice, dovrai definire dove si trova il tuo file PSD. Questo è essenzialmente il punto di partenza per il tuo progetto.

```java
String dataDir = "Your Document Directory";
```

Sostituisci `"Your Document Directory"` con il percorso reale dove è situato il tuo file PSD (ad esempio, layers.psd). Questo ti aiuterà a trovare i file senza problemi.

## Passo 2: Crea un ByteArrayOutputStream
Hai bisogno di un luogo dove memorizzare l'immagine modificata prima di fare qualsiasi altra operazione. Un `ByteArrayOutputStream` ti consentirà di catturare facilmente i dati dell'immagine.

```java
ByteArrayOutputStream ms = new ByteArrayOutputStream();
```

Questa riga inizializza un nuovo oggetto `ByteArrayOutputStream` chiamato `ms`. Userai questo oggetto per salvare la tua immagine non compressa.

## Passo 3: Carica il file PSD
È il momento di caricare il file PSD vero e proprio. Qui inizia la magia!

```java
PsdImage psdImage = (PsdImage) Image.load(dataDir + "layers.psd");
```

Questa riga carica il tuo file PSD in un oggetto `PsdImage`. Assicurati di avere il percorso corretto; altrimenti, apparirà un errore come un quiz inatteso.

## Passo 4: Configura le PsdOptions per il salvataggio
Devi specificare come vuoi salvare l'immagine — naturalmente non compressa!

```java
PsdOptions saveOptions = new PsdOptions();
saveOptions.setCompressionMethod(CompressionMethod.Raw);
```

Qui crei un oggetto `PsdOptions` e imposti il metodo di compressione su `Raw`. Questo metodo garantisce che l'immagine mantenga tutta la qualità e venga salvata senza alcuna compressione.

## Passo 5: Salva l'immagine nello stream di output
```java
psdImage.save(ms, saveOptions);
```

Questa riga salva la tua immagine modificata nello `ByteArrayOutputStream` creato al Passo 2, utilizzando le opzioni definite al Passo 4. Il metodo `save` si occupa di codificare correttamente l'immagine in base alle impostazioni.

## Passo 6: Resetta lo stream di output
Dopo il salvataggio, lo stream di output si trova alla fine. Devi resettarlo per leggere dall'inizio.

```java
ms.reset();
```

Questo metodo `reset` prepara il tuo `ByteArrayOutputStream` per la lettura dall'inizio. È come riavvolgere un nastro prima di ascoltare la tua canzone preferita!

## Passo 7: Carica l'immagine appena creata
```java
PsdImage img = (PsdImage) Image.load(new ByteArrayInputStream(ms.toByteArray()));
```

Qui carichiamo nuovamente l'immagine dallo `ByteArrayOutputStream` in un nuovo oggetto `PsdImage`. È qui che puoi verificare i risultati del lavoro precedente.

## Passo 8: Crea l'oggetto Graphics
Per modificare ulteriormente o renderizzare l'immagine, dovrai creare un oggetto graphics.

```java
Graphics graphics = new Graphics(psdImage);
```

Questa riga inizializza un oggetto `Graphics` usando il tuo `psdImage`. Ora puoi utilizzare questo oggetto graphics per disegnare o manipolare l'immagine secondo necessità. È come avere un pennello in mano!

## Manipola i layer PSD con l'oggetto Graphics
Ora che disponi di un'istanza **Graphics**, puoi **manipolare i layer PSD** — ad esempio, disegnare forme, aggiungere testo o applicare filtri a un layer specifico. Il contesto grafico opera direttamente sui dati pixel sottostanti, offrendoti un controllo fine su ogni aspetto del layer.

## Problemi comuni e soluzioni
- **NullPointerException durante il caricamento del file** – verifica il percorso `dataDir` e assicurati che il nome del file sia corretto.  
- **Output compresso nonostante l'uso di Raw** – assicurati che `saveOptions.setCompressionMethod(CompressionMethod.Raw);` sia chiamato prima del metodo `save`.  
- **L'oggetto Graphics appare vuoto** – verifica di stare disegnando sul corretto istanza `PsdImage` (usa quello caricato, non quello appena creato a meno che non sia intenzionale).

## FAQ

### Cos'è Aspose.PSD?
Aspose.PSD è una libreria .NET che consente agli sviluppatori di creare, modificare e manipolare file Photoshop PSD e formati immagine correlati in modo programmatico.

### Come posso scaricare Aspose.PSD per Java?
Puoi scaricarla dalla [pagina di rilascio](https://releases.aspose.com/psd/java/).

### Esiste una versione di prova gratuita per Aspose.PSD?
Sì, puoi ottenere una versione di prova gratuita da [qui](https://releases.aspose.com/).

### Posso ottenere supporto per Aspose.PSD?
Assolutamente! Puoi chiedere aiuto sul [forum di supporto Aspose](https://forum.aspose.com/c/psd/34).

### Come posso ottenere una licenza temporanea per Aspose.PSD?
Visita semplicemente la [pagina della licenza temporanea](https://purchase.aspose.com/temporary-license/) per iniziare.

## Domande frequenti

**Q: Posso usare l'oggetto graphics per modificare solo un layer specifico?**  
A: Sì. Dopo aver caricato il PSD, seleziona il layer desiderato tramite `psdImage.getLayers().get_Item(index)` e passalo al costruttore `Graphics`.

**Q: Il metodo di compressione Raw influisce sulla dimensione del file?**  
A: Raw memorizza i dati pixel senza compressione, quindi la dimensione del file sarà maggiore rispetto ai PSD compressi, ma la qualità dell'immagine rimane intatta.

**Q: È possibile esportare il PSD modificato in un altro formato (ad esempio PNG)?**  
A: Certamente. Usa la sovraccarico appropriata di `Image.save` con `PngOptions` dopo la modifica.

**Q: Quale versione di Java è richiesta?**  
A: Aspose.PSD per Java supporta JDK 8 e versioni successive.

**Q: Come rilascio le risorse dopo l'elaborazione?**  
A: Chiama `psdImage.dispose()` e chiudi eventuali stream per liberare le risorse native.

---  

**Ultimo aggiornamento:** 2025-12-13  
**Testato con:** Aspose.PSD per Java (ultima release)  
**Autore:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}