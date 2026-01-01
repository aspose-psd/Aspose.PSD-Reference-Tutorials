---
date: 2026-01-01
description: Scopri come creare metadati XMP, aggiungere XMP ai file PSD e aggiornare
  i metadati delle immagini con Aspose.PSD per Java. Segui ora questa guida passo
  passo.
linktitle: Create XMP Metadata
second_title: Aspose.PSD Java API
title: Crea metadati XMP con Aspose.PSD per Java
url: /it/java/image-editing/create-xmp-metadata/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Crea metadati XMP con Aspose.PSD per Java

## Introduzione

Gestire i metadati delle immagini è una necessità comune per gli sviluppatori Java che lavorano con file Photoshop (PSD). In questo tutorial imparerai **come creare metadati XMP** usando la libreria Aspose.PSD, aggiungere XMP a un'immagine PSD e aggiornare i metadati dell'immagine in modo programmatico. Ti guideremo passo passo, spiegheremo perché ogni elemento è importante e ti forniremo consigli pratici da applicare nei progetti reali.

## Risposte rapide
- **Che cos'è il metadato XMP?** Un formato standardizzato per incorporare informazioni descrittive (autore, parole‑chiave, ecc.) all'interno dei file immagine.  
- **Perché usare Aspose.PSD?** Fornisce un'API pure‑Java per creare, leggere e modificare file PSD senza Photoshop.  
- **Posso aggiungere XMP a un PSD esistente?** Sì – puoi aggiornare i metadati dell'immagine al volo con `setXmpData`.  
- **Quali sono i passaggi principali?** Impostare la dimensione dell'immagine, creare header/trailer, costruire i pacchetti XMP, allegarli e salvare.  
- **È necessaria una licenza?** Una versione di prova gratuita è sufficiente per lo sviluppo; è richiesta una licenza commerciale per la produzione.

## Che cosa significa “creare metadati XMP” in Java?

Creare metadati XMP significa costruire un pacchetto XMP (header, corpo, trailer) che descrive l'immagine e poi incorporare quel pacchetto in un file PSD. La libreria Aspose.PSD astrae i dettagli a basso livello, permettendoti di concentrarti sul contenuto da memorizzare.

## Perché aggiungere XMP ai file PSD?

- **Ricercabilità:** Consente ricerche potenti nella gestione delle risorse basate su autore, titolo o tag personalizzati.  
- **Interoperabilità:** XMP è riconosciuto dai prodotti Adobe, Lightroom e da molti sistemi DAM.  
- **Controllo di versione:** Memorizza la cronologia di elaborazione (ad es. città, modalità colore) direttamente nel file.

## Prerequisiti

- **Ambiente di sviluppo Java:** JDK 8 o superiore installato e una conoscenza di base di Java.  
- **Libreria Aspose.PSD:** Scarica e configura la libreria Aspose.PSD per Java. Puoi trovare la libreria e la documentazione dettagliata [qui](https://reference.aspose.com/psd/java/).  
- **Directory dei documenti:** Decidi dove leggerai/scriverai i file PSD sul tuo sistema.

## Importa i pacchetti

Nel tuo progetto Java, importa i pacchetti necessari per sfruttare le funzionalità di Aspose.PSD:

```java
import com.aspose.psd.Rectangle;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.system.io.MemoryStream;
import com.aspose.psd.xmp.XmpHeaderPi;
import com.aspose.psd.xmp.XmpMeta;
import com.aspose.psd.xmp.XmpPacketWrapper;
import com.aspose.psd.xmp.XmpTrailerPi;
import com.aspose.psd.xmp.schemas.dublincore.DublinCorePackage;
import com.aspose.psd.xmp.schemas.photoshop.ColorMode;
import com.aspose.psd.xmp.schemas.photoshop.PhotoshopPackage;
```

## Passo 1: Specifica la dimensione dell'immagine

Definisci prima le dimensioni della tela per la nuova immagine PSD.

```java
// Specify the size of the image by defining a Rectangle
Rectangle rect = new Rectangle(0, 0, 100, 200);
```

## Passo 2: Crea una nuova immagine

Crea un'immagine PSD vuota che arricchiremo successivamente con i metadati XMP.

```java
// Create a brand new image for sample purposes
PsdImage image = new PsdImage(rect.getWidth(), rect.getHeight());
```

## Passo 3: Crea l'header XMP

L'header contiene l'istruzione di elaborazione XML di apertura e un GUID che identifica il documento.

```java
// Create an instance of XMP-Header
XmpHeaderPi xmpHeader = new XmpHeaderPi();
xmpHeader.setGuid("Your Document Directory");
```

## Passo 4: Crea il trailer XMP

Il trailer segna la fine del pacchetto XMP. Impostare il flag `true` scrive l'istruzione di chiusura.

```java
// Create an instance of Xmp-TrailerPi 
XmpTrailerPi xmpTrailer = new XmpTrailerPi(true);
```

## Passo 5: Crea i metadati XMP

Aggiungi attributi generici come autore e descrizione all'oggetto principale dei metadati XMP.

```java
// Create an instance of XMPmeta class to set different attributes
XmpMeta xmpMeta = new XmpMeta();
xmpMeta.addAttribute("Author", "Mr Smith");
xmpMeta.addAttribute("Description", "The fake metadata value");
```

## Passo 6: Crea il wrapper del pacchetto XMP

Raggruppa header, trailer e metadati principali in un unico pacchetto che può essere allegato all'immagine.

```java
// Create an instance of XmpPacketWrapper that contains all metadata
XmpPacketWrapper xmpData = new XmpPacketWrapper(xmpHeader, xmpTrailer, xmpMeta);
```

## Passo 7: Imposta gli attributi Photoshop

Popola i campi specifici di Photoshop (città, paese, modalità colore) che molti strumenti Adobe si aspettano.

```java
// Create an instance of Photoshop package and set Photoshop attributes
PhotoshopPackage photoshopPackage = new PhotoshopPackage();
photoshopPackage.setCity("London");
photoshopPackage.setCountry("England");
photoshopPackage.setColorMode(ColorMode.Rgb);
```

## Passo 8: Aggiungi il pacchetto Photoshop ai metadati XMP

Allega il pacchetto Photoshop al pacchetto XMP.

```java
// Add Photoshop package into XMP metadata
xmpData.addPackage(photoshopPackage);
```

## Passo 9: Imposta gli attributi DublinCore

Aggiungi metadati Dublin Core come autore, titolo e un tag personalizzato per il film.

```java
// Create an instance of DublinCore package and set DublinCore attributes
DublinCorePackage dublinCorePackage = new DublinCorePackage();
dublinCorePackage.setAuthor("Charles Bukowski");
dublinCorePackage.setTitle("Confessions of a Man Insane Enough to Live With the Beasts");
dublinCorePackage.addValue("dc:movie", "Barfly");
```

## Passo 10: Aggiungi il pacchetto DublinCore ai metadati XMP

Combina il pacchetto Dublin Core con il pacchetto XMP esistente.

```java
// Add DublinCore Package into XMP metadata
xmpData.addPackage(dublinCorePackage);
```

## Passo 11: Aggiorna i metadati XMP nell'immagine

Ora incorpora il pacchetto XMP completo nell'immagine PSD.

```java
// Update XMP metadata into the image
image.setXmpData(xmpData);
```

## Passo 12: Salva l'immagine

Infine, scrivi il file PSD su disco (o su uno stream di memoria) in modo che i metadati vengano persistiti.

```java
// Save the image on the disk or in a memory stream
image.save("Your Document Directory" + "create_XMP_Metadata.psd");
```

## Problemi comuni e soluzioni

| Problema | Perché accade | Soluzione |
|----------|----------------|-----------|
| **`NullPointerException` su `setXmpData`** | Il pacchetto XMP non è stato costruito completamente (header/trailer mancanti). | Assicurati di creare `XmpHeaderPi`, `XmpTrailerPi` e di aggiungere tutti i pacchetti prima di chiamare `setXmpData`. |
| **I metadati non sono visibili in Photoshop** | Photoshop si aspetta che il pacchetto XMP sia avvolto correttamente. | Verifica che venga usato `XmpTrailerPi(true)` e che il pacchetto sia salvato con l'immagine. |
| **Errori di percorso file** | Uso di un percorso relativo senza le corrette autorizzazioni. | Usa un percorso assoluto o assicurati che l'applicazione abbia i permessi di scrittura sulla cartella di destinazione. |

## Domande frequenti

**D: Aspose.PSD è compatibile con diversi formati immagine?**  
R: Sì, Aspose.PSD supporta PSD, PSB, BMP, GIF, JPEG, PNG, TIFF e molti altri, offrendoti flessibilità tra i formati.

**D: Posso manipolare i metadati esistenti usando Aspose.PSD?**  
R: Assolutamente. Puoi caricare un PSD esistente, recuperare i suoi dati XMP con `getXmpData()`, modificare il pacchetto e salvarlo nuovamente.

**D: Ci sono limitazioni sulla dimensione dell'immagine che Aspose.PSD può gestire?**  
R: Aspose.PSD è progettato per lavorare con immagini di grandi dimensioni (fino a diversi gigapixel), limitate solo dalla memoria disponibile.

**D: È disponibile una versione di prova di Aspose.PSD?**  
R: Sì, puoi esplorare le funzionalità di Aspose.PSD ottenendo una prova gratuita [qui](https://releases.aspose.com/).

**D: Dove posso trovare supporto per domande relative ad Aspose.PSD?**  
R: Per qualsiasi assistenza o domanda, visita il [forum Aspose.PSD](https://forum.aspose.com/c/psd/34).

## Conclusione

Ora hai imparato **come creare metadati XMP**, aggiungere XMP a un PSD e aggiornare i metadati dell'immagine usando Aspose.PSD per Java. Questi passaggi ti danno il pieno controllo sulle informazioni descrittive incorporate nelle tue immagini, rendendole ricercabili, gestibili e pronte per flussi di lavoro successivi. Sentiti libero di sperimentare con schemi XMP aggiuntivi o di integrare questo codice in pipeline di elaborazione immagini più ampie.

---

**Ultimo aggiornamento:** 2026-01-01  
**Testato con:** Aspose.PSD per Java 24.12  
**Autore:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}