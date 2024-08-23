---
title: Controlla la riallocazione della cache nei file PSD
linktitle: Controlla la riallocazione della cache nei file PSD
second_title: API Java Aspose.PSD
description: Gestisci la riallocazione della cache nei file PSD utilizzando Aspose.PSD per Java. Scopri come ottimizzare la memoria e la gestione dei file in modo efficiente ideale per gli sviluppatori.
type: docs
weight: 22
url: /it/java/modifying-converting-psd-images/control-cache-reallocation-psd-files/
---
## Introduzione
Quando si lavora con immagini e file Photoshop a livello di codice, l'efficienza è un fattore chiave. Aspose.PSD per Java offre robuste funzionalità per gestire e manipolare i file PSD senza problemi. Uno degli aspetti fondamentali dell'ottimizzazione delle prestazioni è il controllo della riallocazione della cache. La gestione della cache aiuta a mantenere l'equilibrio tra memoria e utilizzo del disco, garantendo che l'applicazione funzioni senza intoppi, senza arresti anomali o rallentamenti imprevisti. 
## Prerequisiti
Prima di passare alla parte di codifica, ci sono alcune cose di cui devi assicurarti affinché tutto funzioni senza intoppi:
1. Java Development Kit (JDK): assicurati di avere JDK installato sul tuo computer. Puoi scaricarlo da[Il sito web di Oracle](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).
2. Aspose.PSD per Java: è necessario scaricare la libreria Aspose.PSD. Puoi trovare l'ultima versione[Qui](https://releases.aspose.com/psd/java/).
3. Configurazione IDE: un ambiente di sviluppo integrato (IDE) come IntelliJ IDEA o Eclipse semplificherà la gestione del codice.
4. Comprensione di base di Java: la familiarità con la programmazione Java ti aiuterà a comprendere meglio i concetti e i frammenti di codice.
5.  Licenza Aspose (facoltativa): se desideri rimuovere filigrane e ottenere la piena funzionalità, considera l'acquisto di una licenza[Qui](https://purchase.aspose.com/buy) o provando la prova gratuita[Qui](https://releases.aspose.com/).
## Importa pacchetti
Prima di iniziare a scrivere il codice, assicuriamoci di aver importato i pacchetti necessari. Di seguito è riportato un breve elenco di cosa includere all'inizio del file Java:
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
## Passaggio 1: configurazione della directory dei dati
Per prima cosa, dovrai impostare una directory in cui desideri archiviare i file della cache. Questo è essenziale per gestire la cache in modo efficace.
```java
String dataDir = "Your Document Directory";
Cache.setCacheFolder(dataDir);
```

- String dataDir: definisce la directory per la cache dei documenti.
- Cache.setCacheFolder(dataDir): questo metodo imposta la cartella della cache nella directory specificata. Qualsiasi cache creata da Aspose verrà ora archiviata qui anziché nella directory temporanea predefinita.
## Passaggio 2: configurazione della cache su disco
Successivamente, specificheremo che vogliamo che la nostra cache sia archiviata solo su disco. Ciò è particolarmente utile se la tua applicazione utilizza file di grandi dimensioni e vuoi assicurarti che la memoria rimanga libera.
```java
Cache.setCacheType(CacheType.CacheOnDiskOnly);
```

- Cache.setCacheType(CacheType.CacheOnDiskOnly): questa opzione garantisce che la cache non venga mantenuta in memoria, il che è utile per gestire file PSD di grandi dimensioni senza consumare troppa RAM.
## Passaggio 3: impostazione della dimensione massima della cache del disco e della memoria
Ora limitiamo le dimensioni della cache. Questo è fondamentale perché la cache illimitata può portare a problemi di prestazioni.
```java
Cache.setMaxDiskSpaceForCache(1073741824); // 1 gigabyte
Cache.setMaxMemoryForCache(1073741824); // 1 gigabyte
```

- Cache.setMaxDiskSpaceForCache(1073741824): imposta un limite di 1 GB per la cache su disco. Puoi regolare questa dimensione in base alle tue esigenze.
- Cache.setMaxMemoryForCache(1073741824): analogamente, limita la cache in memoria, garantendo che l'applicazione non utilizzi memoria eccessiva.
## Passaggio 4: gestire la strategia di riallocazione della cache
Gestire la modalità di riallocazione della cache è essenziale per mantenere le prestazioni. Ecco come puoi configurarlo.
```java
Cache.setExactReallocateOnly(false);
```

- Cache.setExactReallocateOnly(false): se impostato su false, consente ad Aspose di gestire la riallocazione della cache in modo più flessibile, il che può portare a prestazioni migliori.
## Passaggio 5: controlla la dimensione della cache allocata
Questo passaggio riguarda il monitoraggio del numero di byte attualmente allocati per la cache in memoria o su disco. Implementiamolo:
```java
long l1 = Cache.getAllocatedDiskBytesCount();
long l2 = Cache.getAllocatedMemoryBytesCount();
```

- long l1: memorizza il conteggio dei byte allocati sul disco.
- long l2: memorizza il conteggio dei byte allocati in memoria. 
Puoi controllare questi valori in qualsiasi momento per assicurarti che l'applicazione gestisca la memoria e l'utilizzo del disco come previsto.
## Passaggio 6: creazione di un'immagine PSD
Ora che abbiamo impostato le configurazioni della cache, creiamo una semplice immagine PSD.
```java
PsdOptions options = new PsdOptions();
Color[] color = { Color.getRed(), Color.getBlue(), Color.getBlack(), Color.getWhite() };
options.setPalette(new ColorPalette(color));
options.setSource(new StreamSource(new ByteArrayInputStream(new byte[0])));
RasterImage image = (RasterImage) Image.create(options, 100, 100);
```

- Opzioni PsdOptions: questo oggetto consente di specificare le opzioni durante la creazione di un'immagine Photoshop.
- Colore[] color: un array contenente i colori che verranno utilizzati nella tavolozza delle immagini.
## Passaggio 7: salvataggio dei dati pixel nell'immagine
Ora popoliamo la nostra immagine con i dati dei pixel e salviamola.
```java
Color[] pixels = new Color[10000];
for (int i = 0; i < pixels.length; i++) {
    pixels[i] = Color.getWhite();
}
image.savePixels(image.getBounds(), pixels);
```

- Colore[] pixel: si tratta di un array di oggetti colorati. Qui lo stiamo riempiendo con pixel bianchi.
- image.savePixels(image.getBounds(), pixels): questo metodo salva i dati dei pixel nell'immagine. Aggiorna l'immagine con i colori che abbiamo definito.
## Passaggio 8: monitoraggio della cache allocata dopo la creazione dell'immagine
Dopo aver creato l'immagine, è buona norma verificare nuovamente quanti byte sono allocati per la cache.
```java
long diskBytes = Cache.getAllocatedDiskBytesCount();
long memoryBytes = Cache.getAllocatedMemoryBytesCount();
```

- long diskBytes: acquisisce l'allocazione corrente sul disco dopo la creazione dell'immagine.
- long memoryBytes: cattura l'allocazione corrente in memoria. 
Questo passaggio ti aiuterà a determinare la quantità di cache utilizzata dopo le operazioni.
## Passaggio 9: verificare il corretto smaltimento
Infine, è fondamentale garantire che tutti gli oggetti Aspose.PSD siano stati eliminati correttamente per evitare perdite di memoria.
```java
l1 = Cache.getAllocatedDiskBytesCount();
l2 = Cache.getAllocatedMemoryBytesCount();
```

- l1 e l2: queste variabili ti aiuteranno a verificare l'allocazione finale. Se non sono zero, significa che alcuni oggetti non sono stati smaltiti correttamente.
## Conclusione
Il controllo della riallocazione della cache in Aspose.PSD per Java può fare una differenza significativa nelle prestazioni della tua applicazione. Seguendo i passaggi sopra descritti, puoi gestire in modo efficace la cache, ridurre al minimo l'utilizzo della memoria e creare bellissimi file PSD in modo efficiente. Abbraccia queste tecniche e osserva le tue applicazioni prosperare con prestazioni ottimali!
## Domande frequenti
### Cos'è Aspose.PSD?
Aspose.PSD è una libreria per sviluppatori .NET e Java per creare, manipolare e convertire file Photoshop (PSD) a livello di codice.
### Come posso verificare la dimensione della cache allocata?
 Usa metodi come`Cache.getAllocatedDiskBytesCount()` E`Cache.getAllocatedMemoryBytesCount()` per monitorare l'utilizzo corrente della cache.
### Posso impostare una directory personalizzata per la cache?
 Sì, puoi specificare una directory diversa utilizzando`Cache.setCacheFolder("Your Directory Path")`.
### Aspose.PSD è gratuito?
Aspose.PSD è una libreria a pagamento, ma puoi iniziare con una prova gratuita disponibile su di essa[sito web](https://releases.aspose.com/).
### Cosa succede se non smaltimento gli oggetti?
La mancata eliminazione degli oggetti può causare perdite di memoria, facendo sì che l'applicazione utilizzi più risorse del necessario.