---
date: 2026-03-28
description: Scopri come creare un nuovo livello PSD e gestirne la data e l'ora di
  creazione utilizzando Aspose.PSD per Java. Questa guida passo passo copre il caricamento,
  la lettura, la convalida e l'aggiunta di livelli.
linktitle: Create New PSD Layer and Manage Creation DateTime in Java
second_title: Aspose.PSD Java API
title: Crea un nuovo livello PSD e gestisci la data e l'ora di creazione in Java
url: /it/java/psd-image-modification-conversion/manage-layer-creation-datetime-psd/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Crea un nuovo livello PSD e gestisci la data/ora di creazione in Java

## Introduzione
Quando lavori con file Photoshop (PSD) in modo programmatico, la possibilità di **creare nuovi livelli PSD** e tenere traccia dei loro timestamp di creazione è davvero rivoluzionaria. Che tu stia costruendo un sistema di versionamento per le risorse di design, automatizzando modifiche batch o semplicemente abbia bisogno di una traccia di audit per progetti collaborativi, sapere come leggere e impostare la data di creazione del livello ti consente di mantenere la piena provenienza di ogni modifica. In questo tutorial percorreremo l’intero processo usando Aspose.PSD per Java — dal caricamento di un PSD, al recupero della data di creazione di un livello, alla sua validazione, fino all’aggiunta di un nuovo livello di regolazione.

## Risposte rapide
- **Quale libreria gestisce i file PSD in Java?** Aspose.PSD per Java  
- **Posso leggere la data di creazione di un livello?** Sì, usando `layer.getLayerCreationDateTime()`  
- **È possibile aggiungere un nuovo livello di regolazione?** Assolutamente – `im.addLevelsAdjustmentLayer()` ne crea uno  
- **È necessaria una licenza per l’uso in produzione?** È richiesta una licenza commerciale per distribuzioni non‑trial  
- **Quale versione di Java è supportata?** JDK 8 o successive  

## Che cosa significa “creare nuovo livello PSD”?
Creare un nuovo livello PSD significa inserire programmaticamente un nuovo oggetto livello — come un livello di regolazione, testo o pixel — in un documento PSD esistente. Questa operazione ti permette di estendere o modificare l’immagine senza aprire manualmente Photoshop.

## Perché gestire la data/ora di creazione del livello?
Tenere traccia della data/ora di creazione di ogni livello ti aiuta a:
- **Audit delle revisioni** – sapere esattamente quando un livello è stato aggiunto.  
- **Sincronizzare le risorse** tra i team confrontando i timestamp.  
- **Automatizzare i flussi di lavoro** che dipendono da regole basate sul tempo (ad es., nascondere i livelli più vecchi di un mese).  

## Prerequisiti
Prima di iniziare, assicurati di avere tutto il necessario:

1. **Java Development Kit (JDK)** – versione 8 o successiva.  
2. **IDE** – IntelliJ IDEA, Eclipse, NetBeans o qualsiasi editor tu preferisca.  
3. **Aspose.PSD per Java** – puoi [scaricarlo qui](https://releases.aspose.com/psd/java/) per l’installazione.  
4. **Conoscenze di base di Java** – se sei nuovo a Java, non preoccuparti; il codice è completamente commentato.

Hai tutto? Ottimo! Passiamo alla parte più divertente del coding.

## Importa i pacchetti
Per prima cosa, importa le classi Aspose.PSD e le utility Java di cui avrai bisogno. Queste importazioni ti danno accesso alla gestione delle immagini, alla manipolazione dei livelli e alla formattazione delle date.

```java
import com.aspose.psd.Image;
import com.aspose.psd.examples.Utils.Assert;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.Layer;
import java.text.DateFormat;
import java.text.SimpleDateFormat;
import java.util.Date;
```

## Passo 1: Configura la directory del documento
Specifica la cartella che contiene il PSD con cui vuoi lavorare. Sostituisci il segnaposto con il percorso assoluto sul tuo computer.

```java
String dataDir = "Your Document Directory";
```

## Passo 2: Carica il file PSD
Crea un’istanza di `PsdImage` caricando il file di destinazione. Questo oggetto è il punto di ingresso per tutte le operazioni sui livelli.

```java
String sourceName = dataDir + "OneLayer.psd";
PsdImage im = (PsdImage) Image.load(sourceName);
```

## Passo 3: Accedi al livello e alla sua data di creazione
Recupera il primo livello (indice 0) e ottieni il suo timestamp di creazione. Questa è la data che confronterai o registrerai in seguito.

```java
Layer layer = im.getLayers()[0];
Date creationDateTime = layer.getLayerCreationDateTime();
```

## Passo 4: Formatta la data di creazione
Converti l’oggetto `Date` grezzo in una stringa leggibile. Modifica il pattern se preferisci un formato diverso.

```java
DateFormat dateFormat = new SimpleDateFormat("yyyy/MM/dd HH:mm:ss");
```

## Passo 5: Valida la data di creazione
Per dimostrazione, confrontiamo la data recuperata con un valore atteso. Nei progetti reali potresti confrontarla con un record di database o un file di configurazione.

```java
Date expectedDateTime = new Date("2018/7/17 8:57:24");
Assert.areEqual(expectedDateTime, creationDateTime);
```

## Passo 6: Crea un nuovo livello
Ora creiamo effettivamente **nuovi livelli PSD**. Qui aggiungiamo un livello di regolazione Levels, che ti consente di modificare le gamme tonali senza alterare i pixel originali.

```java
Date now = new Date();
Layer createdLayer = im.addLevelsAdjustmentLayer();
```

> **Consiglio professionale:** La variabile `now` cattura il momento in cui aggiungi il livello, che potrai poi salvare come metadato se ti serve un timestamp personalizzato.

## Problemi comuni e soluzioni
| Problema | Perché accade | Soluzione |
|----------|---------------|-----------|
| `NullPointerException` su `layer.getLayerCreationDateTime()` | Il PSD non ha livelli o l’indice del livello è fuori intervallo. | Verifica che `im.getLayers().length > 0` prima di accedere. |
| Discrepanza di data nella validazione | Il costruttore `Date` interpreta le stringhe in modo dipendente dalla locale. | Usa `SimpleDateFormat.parse("2018/07/17 08:57:24")` per un parsing affidabile. |
| Nuovo livello non visibile in Photoshop | Il livello di regolazione può essere nascosto di default. | Chiama `createdLayer.setVisible(true);` dopo la creazione. |

## Conclusione
Ora sai come **creare nuovi livelli PSD**, leggere i loro timestamp di creazione, validarli e aggiungere livelli di regolazione — tutto usando Aspose.PSD per Java. Questa capacità apre la porta a automazioni sofisticate, tracciamenti di audit e flussi di lavoro collaborativi in qualsiasi pipeline di elaborazione immagini basata su Java.

Se ti è piaciuto questo tutorial, esplora altre funzionalità di Aspose.PSD come l’unione dei livelli, l’applicazione di filtri o l’esportazione in formati diversi. Le possibilità sono infinite!

## FAQ
### Che cos’è Aspose.PSD?  
Aspose.PSD è una potente libreria per lavorare con file Photoshop (PSD) in modo programmatico.
### Posso usare Aspose.PSD gratuitamente?  
Sì! Puoi iniziare con una prova gratuita disponibile [qui](https://releases.aspose.com/).
### Devo acquistare una licenza per un uso a lungo termine?  
Sì, puoi ottenere una licenza [qui](https://purchase.aspose.com/buy) quando sei pronto.
### Dove posso trovare ulteriori informazioni su Aspose.PSD?  
Puoi consultare la [documentazione](https://reference.aspose.com/psd/java/) per guide dettagliate e riferimenti API.
### Come posso richiedere supporto se incontro problemi con Aspose.PSD?  
Visita il [forum di supporto](https://forum.aspose.com/c/psd/34) per assistenza dalla community.

---

**Ultimo aggiornamento:** 2026-03-28  
**Testato con:** Aspose.PSD per Java 24.10  
**Autore:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}