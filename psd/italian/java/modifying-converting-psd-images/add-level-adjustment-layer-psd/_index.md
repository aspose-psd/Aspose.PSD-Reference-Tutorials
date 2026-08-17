---
date: 2026-03-07
description: Impara come regolare i livelli aggiungendo un livello di regolazione
  nei file PSD usando Aspose.PSD per Java. Padroneggia le regolazioni tonali rapidamente.
linktitle: Add Level Adjustment Layer in PSD
second_title: Aspose.PSD Java API
title: Come regolare i livelli – Aggiungi livello di regolazione dei livelli in PSD
url: /it/java/modifying-converting-psd-images/add-level-adjustment-layer-psd/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aggiungere Livello di Regolazione dei Livelli in PSD

## Introduzione
Se stai cercando **come regolare i livelli** nei tuoi documenti Photoshop, il Livello di Regolazione dei Livelli è lo strumento perfetto. Ti consente di perfezionare ombre, mezzitoni e luci senza alterare permanentemente i pixel originali. In questo tutorial vedremo come aggiungere un Livello di Regolazione dei Livelli a un file PSD usando Aspose.PSD per Java, così potrai ottenere un controllo tonale di livello professionale in pochi passaggi.

## Risposte Rapide
- **Che cosa fa un Livello di Regolazione dei Livelli?** Modifica l'intervallo tonale di un'immagine in modo non distruttivo.  
- **Quale libreria viene utilizzata?** Aspose.PSD per Java.  
- **È necessaria una licenza?** Una versione di prova gratuita è sufficiente per lo sviluppo; è necessaria una licenza per la produzione.  
- **Quanto tempo richiede l'implementazione?** Circa 10‑15 minuti per una regolazione di base.  
- **Posso regolare più canali?** Sì, è possibile impostare i livelli di ingresso/uscita per ciascun canale colore singolarmente.

## Cos'è un Livello di Regolazione dei Livelli?
Un Livello di Regolazione dei Livelli ti consente di correggere l'equilibrio tonale di un'immagine regolando le ombre di ingresso, i mezzitoni e le luci, così come i livelli di uscita. Poiché vive sul proprio livello, puoi attivare/disattivare la sua visibilità o eliminarlo senza influire sull'opera sottostante.

## Perché aggiungere un Livello di Regolazione dei Livelli con Aspose.PSD?
- **Automazione:** Integra le regolazioni dei livelli nei flussi di lavoro di elaborazione batch.  
- **Cross‑platform:** Funziona su qualsiasi OS che supporta Java.  
- **Precisione:** Accedi alle impostazioni di ciascun canale programmaticamente per risultati precisi.  

## Prerequisiti
1. Java Development Kit (JDK). Se non lo possiedi, scaricalo dal [sito Oracle](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html) o usa OpenJDK.  
2. Libreria Aspose.PSD per Java – ottieni l'ultimo JAR da questo [link di download](https://releases.aspose.com/psd/java/).  
3. Conoscenza di base della programmazione Java.  
4. Un IDE come IntelliJ IDEA, Eclipse o NetBeans con il JAR di Aspose.PSD aggiunto al classpath del progetto.

## Importa Pacchetti
Prima di iniziare a scrivere il codice, dobbiamo importare i pacchetti necessari dalla libreria Aspose.PSD. Ecco come fare:
```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.adjustmentlayers.LevelsLayer;
import com.aspose.psd.fileformats.psd.layers.layerresources.LevelChannel;
```
Queste importazioni ci danno accesso alle classi per caricare file PSD, lavorare con i livelli di regolazione dei livelli e manipolare le impostazioni dei singoli canali.

## Come Regolare i Livelli in un File PSD
Di seguito trovi una guida passo‑passo che mostra esattamente **come regolare i livelli** programmaticamente.

### Passo 1: Configura i Percorsi dei File
Definisci dove si trova il PSD di origine e dove verrà salvato il file modificato.
```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "LevelsAdjustmentLayer.psd";
String psdPathAfterChange = dataDir + "LevelsAdjustmentLayerChanged.psd";
```
Sostituisci `"Your Document Directory"` con la cartella reale sul tuo computer.

### Passo 2: Carica il File PSD
Crea un'istanza di `PsdImage` dal file di origine.
```java
PsdImage im = (PsdImage) Image.load(sourceFileName);
```
Ora hai pieno accesso a tutti i livelli all'interno del PSD.

### Passo 3: Itera Attraverso i Livelli
Trova il Livello di Regolazione dei Livelli che desideri modificare.
```java
for (int i = 0; i < im.getLayers().length; i++) {
    if (im.getLayers()[i] instanceof LevelsLayer) {
        LevelsLayer levelsLayer = (LevelsLayer) im.getLayers()[i];
        // Further manipulation will go here...
    }
}
```
Il controllo `instanceof LevelsLayer` garantisce che lavoriamo solo con i livelli di regolazione dei livelli.

### Passo 4: Regola le Impostazioni del Canale di Livello
Modifica i valori di ingresso e uscita per il canale selezionato.
```java
LevelChannel channel = levelsLayer.getChannel(0);
channel.setInputMidtoneLevel(2.0f);
channel.setInputShadowLevel((short) 10);
channel.setInputHighlightLevel((short) 230);
channel.setOutputShadowLevel((short) 20);
channel.setOutputHighlightLevel((short) 200);
```
- **Livello di Mezzitono di Ingresso:** Sposta l'intervallo dei mezzitoni.  
- **Livello di Ombra di Ingresso:** Oscura o schiarisce le ombre.  
- **Livello di Evidenziazione di Ingresso:** Controlla le parti più luminose.  
- **Livelli di Ombra/Evidenziazione di Uscita:** Definiscono l'intervallo finale di uscita.

Sentiti libero di sperimentare con valori diversi per vedere come influenzano l'immagine.

### Passo 5: Salva il File PSD Modificato
Salva le modifiche in un nuovo file.
```java
im.save(psdPathAfterChange);
```
Troverai il PSD aggiornato nella posizione specificata in `psdPathAfterChange`.

## Problemi Comuni e Soluzioni
- **File non trovato:** Verifica che `dataDir` punti alla cartella corretta e che il PSD di origine esista.  
- **ClassCastException:** Assicurati che il file caricato sia effettivamente un PSD; altri formati richiedono classi diverse.  
- **Errori di licenza:** Usa una licenza valida di Aspose.PSD per le build di produzione; la versione di prova funziona per lo sviluppo.

## Conclusione
Ora sai **come regolare i livelli** aggiungendo e configurando un Livello di Regolazione dei Livelli in un file PSD con Aspose.PSD per Java. Questa tecnica ti offre un controllo preciso sull'equilibrio tonale mantenendo il flusso di lavoro completamente automatizzato. Continua a sperimentare con valori di canale diversi ed esplora l'elaborazione batch per applicare le stesse regolazioni a più immagini.

## Domande Frequenti

**Q: Cos'è un Livello di Regolazione dei Livelli?**  
A: È un livello non distruttivo che ti consente di modificare l'intervallo tonale (ombre, mezzitoni, luci) di un'immagine.

**Q: Posso usare Aspose.PSD senza acquistare una licenza?**  
A: Sì, puoi valutare la libreria con una versione di prova gratuita, ma è necessaria una licenza per l'uso commerciale.

**Q: Dove posso trovare la documentazione per Aspose.PSD?**  
A: Puoi trovare la documentazione [qui](https://reference.aspose.com/psd/java/).

**Q: Esiste supporto della community per i prodotti Aspose?**  
A: Assolutamente! Puoi porre domande e ottenere aiuto nel [forum Aspose](https://forum.aspose.com/c/psd/34).

**Q: Come posso ottenere una licenza temporanea per Aspose.PSD?**  
A: Puoi richiedere una licenza temporanea [qui](https://purchase.aspose.com/temporary-license/).

---

**Ultimo aggiornamento:** 2026-03-07  
**Testato con:** Aspose.PSD ultima versione (Java)  
**Autore:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}