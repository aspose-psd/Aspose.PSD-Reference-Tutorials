---
date: 2026-03-13
description: Scopri come creare progetti Java per immagini PSD gestendo la riallocazione
  della cache con Aspose.PSD per Java. Ottimizza in modo efficiente l'uso della memoria
  e del disco.
linktitle: Create PSD Image Java – Control Cache Reallocation
second_title: Aspose.PSD Java API
title: Crea immagine PSD Java – Controllo della riallocazione della cache
url: /it/java/modifying-converting-psd-images/control-cache-reallocation-psd-files/
weight: 22
---

 produce final answer.{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Controllo della riallocazione della cache nei file PSD

## Introduzione
Se hai bisogno di **create PSD image java** progetti in modo efficiente, controllare la riallocazione della cache è essenziale. Quando si lavora con immagini e file Photoshop in modo programmatico, l'efficienza è un fattore chiave. Aspose.PSD for Java offre funzionalità robuste per gestire e manipolare i file PSD senza problemi. Uno degli aspetti fondamentali per ottimizzare le prestazioni è il controllo della riallocazione della cache. La gestione della cache aiuta a mantenere l'equilibrio tra l'uso della memoria e del disco, garantendo che la tua applicazione funzioni senza intoppi, senza crash o rallentamenti inaspettati.

## Risposte rapide
- **Che cosa fa la riallocazione della cache?** Equilibra l'uso della memoria e del disco durante l'elaborazione di grandi file PSD.  
- **Quale tipo di cache è migliore per immagini di grandi dimensioni?** `CacheOnDiskOnly` mantiene libera la memoria memorizzando la cache su disco.  
- **Quanta spazio su disco posso allocare?** Fino a 1 GB (o qualsiasi dimensione impostata con `setMaxDiskSpaceForCache`).  
- **È necessaria una licenza per utilizzare queste funzionalità?** Una licenza rimuove le limitazioni della versione di prova; consulta la pagina di acquisto di Aspose.  
- **Posso monitorare l'uso della cache a runtime?** Sì, utilizza `Cache.getAllocatedDiskBytesCount()` e `Cache.getAllocatedMemoryBytesCount()`.

## Perché controllare la riallocazione della cache?
Gestire la cache è fondamentale quando **create PSD image java** applicazioni che gestiscono file ad alta risoluzione o multistrato. Impostazioni corrette della cache prevengono errori di out‑of‑memory, riducono le pause del GC e offrono prestazioni prevedibili su server o applicazioni desktop.

## Prerequisiti
Prima di passare alla parte di codifica, ci sono alcune cose da verificare per garantire che tutto funzioni senza problemi:
1. Java Development Kit (JDK): Assicurati di avere il JDK installato sulla tua macchina. Puoi scaricarlo dal [sito web di Oracle](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).  
2. Aspose.PSD for Java: Devi scaricare la libreria Aspose.PSD. Puoi trovare l'ultima versione [qui](https://releases.aspose.com/psd/java/).  
3. Configurazione IDE: Un Integrated Development Environment (IDE) come IntelliJ IDEA o Eclipse renderà più semplice la gestione del codice.  
4. Conoscenza di base di Java: Familiarità con la programmazione Java ti aiuterà a comprendere meglio i concetti e gli snippet di codice.  
5. Licenza Aspose (Opzionale): Se desideri rimuovere le filigrane e ottenere la piena funzionalità, considera l'acquisto di una licenza [qui](https://purchase.aspose.com/buy) o prova la versione gratuita [qui](https://releases.aspose.com/).

## Importare i pacchetti
Prima di iniziare a scrivere il codice, assicuriamoci di aver importato i pacchetti necessari. Di seguito è riportato un breve elenco di ciò che includere all'inizio del tuo file Java:
```java
import com.aspose.psd.Cache;
import com.aspose.psd.CacheType;
import com.aspose.psd.Color;
import com.aspose.psd.ColorPalette;
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;
import com.aspose.psd.imageoptions.GifOptions;
import com.aspose.psd.imageoptions.PsdOptions;
import com.aspose.psd.sources.StreamSource;
import com.aspose.psd.system.io.MemoryStream;
```

## Come creare PSD Image Java con controllo della cache
Di seguito trovi una guida passo‑passo che collega la configurazione della cache direttamente al processo di creazione di un'immagine PSD in Java.

### Passo 1: Configurare la directory dei dati
Prima di tutto, dovrai impostare una directory dove desideri che i file di cache vengano memorizzati. Questo è essenziale per gestire la cache in modo efficace.
```java
String dataDir = "Your Document Directory";
Cache.setCacheFolder(dataDir);
```

- `String dataDir`: Definisce la directory per la cache del documento.  
- `Cache.setCacheFolder(dataDir)`: Questo metodo imposta la cartella della cache nella directory specificata. Qualsiasi cache creata da Aspose verrà ora memorizzata qui invece della directory temporanea predefinita.

### Passo 2: Configurare la cache su disco
Successivamente, specificheremo che desideriamo che la cache venga memorizzata solo su disco. Questo è particolarmente utile se la tua applicazione utilizza file di grandi dimensioni e vuoi garantire che la memoria rimanga libera.
```java
Cache.setCacheType(CacheType.CacheOnDiskOnly);
```

- `Cache.setCacheType(CacheType.CacheOnDiskOnly)`: Questa opzione garantisce che la cache non venga mantenuta in memoria, il che è vantaggioso per gestire grandi file PSD senza consumare troppa RAM.

### Passo 3: Impostare la dimensione massima della cache su disco e in memoria
Ora, limitiamo le dimensioni della cache. Questo è cruciale perché una cache illimitata può causare problemi di prestazioni.
```java
Cache.setMaxDiskSpaceForCache(1073741824); // 1 gigabyte
Cache.setMaxMemoryForCache(1073741824); // 1 gigabyte
```

- `Cache.setMaxDiskSpaceForCache(1073741824)`: Imposta un limite di 1 GB per la cache su disco. Puoi regolare questa dimensione in base alle tue esigenze.  
- `Cache.setMaxMemoryForCache(1073741824)`: Allo stesso modo, limita la cache in memoria, garantendo che l'applicazione non utilizzi memoria eccessiva.

### Passo 4: Gestire la strategia di riallocazione della cache
Gestire come la cache viene riallocata è essenziale per mantenere le prestazioni. Ecco come configurarlo.
```java
Cache.setExactReallocateOnly(false);
```

- `Cache.setExactReallocateOnly(false)`: Quando impostato a `false`, permette ad Aspose di gestire la riallocazione della cache in modo più flessibile, il che può portare a migliori prestazioni.

### Passo 5: Verificare la dimensione della cache allocata
Questo passo riguarda il monitoraggio di quanti byte sono attualmente allocati per la cache in memoria o su disco. Implementiamolo:
```java
long l1 = Cache.getAllocatedDiskBytesCount();
long l2 = Cache.getAllocatedMemoryBytesCount();
```

- `long l1`: Memorizza il conteggio dei byte allocati su disco.  
- `long l2`: Memorizza il conteggio dei byte allocati in memoria.  
Puoi verificare questi valori in qualsiasi momento per assicurarti che l'applicazione gestisca correttamente l'uso di memoria e disco come previsto.

### Passo 6: Creare un'immagine PSD
Ora che abbiamo configurato la cache, creiamo una semplice immagine PSD.
```java
PsdOptions options = new PsdOptions();
Color[] color = { Color.getRed(), Color.getBlue(), Color.getBlack(), Color.getWhite() };
options.setPalette(new ColorPalette(color));
options.setSource(new StreamSource(new ByteArrayInputStream(new byte[0])));
RasterImage image = (RasterImage) Image.create(options, 100, 100);
```

- `PsdOptions options`: Questo oggetto consente di specificare le opzioni durante la creazione di un'immagine Photoshop.  
- `Color[] color`: Un array contenente i colori che verranno usati nella tavolozza dell'immagine.

### Passo 7: Salvare i dati dei pixel nell'immagine
Ora, popoliamo la nostra immagine con i dati dei pixel e la salviamo.
```java
Color[] pixels = new Color[10000];
for (int i = 0; i < pixels.length; i++) {
    pixels[i] = Color.getWhite();
}
image.savePixels(image.getBounds(), pixels);
```

- `Color[] pixels`: È un array di oggetti colore. Qui lo riempiamo con pixel bianchi.  
- `image.savePixels(image.getBounds(), pixels)`: Questo metodo salva i dati dei pixel nell'immagine. Aggiorna l'immagine con i colori definiti.

### Passo 8: Monitorare la cache allocata dopo la creazione dell'immagine
Dopo aver creato l'immagine, è buona pratica verificare nuovamente quanti byte sono allocati per la cache.
```java
long diskBytes = Cache.getAllocatedDiskBytesCount();
long memoryBytes = Cache.getAllocatedMemoryBytesCount();
```

- `long diskBytes`: Cattura l'allocazione corrente su disco dopo la creazione dell'immagine.  
- `long memoryBytes`: Cattura l'allocazione corrente in memoria.  
Questo passo ti aiuterà a determinare quanta cache viene consumata dopo le tue operazioni.

### Passo 9: Verificare la corretta eliminazione
Infine, è fondamentale assicurarsi che tutti gli oggetti Aspose.PSD siano stati eliminati correttamente per evitare perdite di memoria.
```java
l1 = Cache.getAllocatedDiskBytesCount();
l2 = Cache.getAllocatedMemoryBytesCount();
```

- `l1` e `l2`: Queste variabili ti aiuteranno a verificare l'allocazione finale. Se non sono zero, indica che alcuni oggetti non sono stati eliminati correttamente.

## Problemi comuni e soluzioni
- **Cartella cache non creata** – Verifica che l'applicazione abbia i permessi di scrittura per il percorso passato a `Cache.setCacheFolder`.  
- **Errori out‑of‑memory** – Controlla nuovamente che `Cache.setCacheType(CacheType.CacheOnDiskOnly)` sia applicato prima di caricare grandi file PSD.  
- **Dimensione della cache inaspettata** – Usa i metodi `Cache.getAllocated*BytesCount()` dopo ogni operazione importante per monitorare la crescita.

## Domande frequenti

**D: Cos'è Aspose.PSD?**  
R: Aspose.PSD è una libreria per sviluppatori .NET e Java per creare, manipolare e convertire file Photoshop (PSD) in modo programmatico.

**D: Come verifico la dimensione della cache allocata?**  
R: Usa metodi come `Cache.getAllocatedDiskBytesCount()` e `Cache.getAllocatedMemoryBytesCount()` per monitorare l'uso corrente della cache.

**D: Posso impostare una directory personalizzata per la cache?**  
R: Sì, puoi specificare una directory diversa usando `Cache.setCacheFolder("Your Directory Path")`.

**D: Aspose.PSD è gratuito?**  
R: Aspose.PSD è una libreria a pagamento, ma puoi iniziare con una prova gratuita disponibile sul loro [sito web](https://releases.aspose.com/).

**D: Cosa succede se non elimino gli oggetti?**  
R: Non eliminare gli oggetti può causare perdite di memoria, facendo sì che l'applicazione utilizzi più risorse del necessario.

## Conclusione
Controllare la riallocazione della cache mentre **create PSD image java** applicazioni può fare una differenza significativa nelle prestazioni. Seguendo i passaggi sopra, gestirai la cache in modo efficiente, ridurrai il consumo di memoria e genererai file PSD di alta qualità con Aspose.PSD for Java. Applica queste tecniche e i tuoi progetti funzioneranno più fluidi e scalabili.

---

**Ultimo aggiornamento:** 2026-03-13  
**Testato con:** Aspose.PSD for Java (latest release)  
**Autore:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}