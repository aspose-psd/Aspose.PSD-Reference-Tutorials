---
date: 2026-03-02
description: Scopri come aggiungere il riempimento creando un livello di riempimento
  colore nei file PSD usando Java e Aspose.PSD. Segui la nostra guida passo‑passo
  per impostare rapidamente il colore del livello di riempimento.
linktitle: Add Color Fill Layer to PSD Files using Java
second_title: Aspose.PSD Java API
title: 'Come aggiungere il riempimento: aggiungere un livello di riempimento colore
  ai file PSD usando Java'
url: /it/java/modifying-converting-psd-images/add-color-fill-layer-psd-files/
weight: 20
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aggiungere un livello di riempimento colore ai file PSD usando Java

## Introduzione
Ti è mai capitato di dover manipolare file Photoshop in modo programmatico, magari per aggiungere un tocco di colore a un progetto? Se ti chiedi **come aggiungere un riempimento** a un PSD, sei nel posto giusto. In questo tutorial vedremo come aggiungere un livello di riempimento colore ai file PSD (Photoshop Document) usando Java e la libreria Aspose.PSD. Pensa al tuo PSD come a una tela digitale—al termine saprai come creare un livello di riempimento colore, impostare il colore del livello di riempimento e salvare il file aggiornato in poche righe di codice.

## Risposte rapide
- **Quale libreria è necessaria?** Aspose.PSD for Java  
- **Caso d'uso principale?** Aggiungere o modificare programmaticamente i colori di riempimento PSD  
- **Quanto tempo richiede l'implementazione?** Circa 10‑15 minuti per uno scenario di base  
- **È necessaria una licenza?** Una prova gratuita è sufficiente per la valutazione; è richiesta una licenza commerciale per la produzione  
- **Versione Java supportata?** Java 8 e successive  

## Cos'è un livello di riempimento colore?
Un livello di riempimento colore è una sovrapposizione di colore solido che si trova sopra gli altri livelli in un documento Photoshop. Viene spesso usato per aggiungere colore di sfondo, creare maschere o cambiare rapidamente il tema visivo di un progetto senza modificare i singoli pixel.

## Perché aggiungere un livello di riempimento colore con il codice?
- **Automazione:** Generare risorse di branding coerenti su molti file.  
- **Elaborazione batch:** Aggiornare decine di PSD in pochi secondi invece di farlo manualmente.  
- **Design dinamici:** Cambiare i colori al volo in base all'input dell'utente o a fonti di dati.

## Prerequisiti
Prima di immergerci nel codice, assicuriamoci di avere tutto il necessario:

1. **Java Development Kit (JDK)** – JDK 8 o più recente installato.  
2. **Libreria Aspose.PSD** – Scarica l'ultimo JAR dalla [pagina Aspose Releases](https://releases.aspose.com/psd/java/).  
3. **IDE** – IntelliJ IDEA, Eclipse, NetBeans o qualsiasi editor tu preferisca.  
4. **Conoscenza di base di Java** – Familiarità con oggetti, cicli e gestione delle eccezioni.

## Importare i pacchetti
Ora che abbiamo coperto le basi, importiamo le classi necessarie. Queste importazioni ci danno accesso alla gestione dei PSD e alla manipolazione dei livelli di riempimento.

```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.filllayers.FillLayer;
import com.aspose.psd.fileformats.psd.layers.fillsettings.FillType;
import com.aspose.psd.fileformats.psd.layers.fillsettings.IColorFillSettings;
```

## Come aggiungere il riempimento – Guida passo‑passo

### Passo 1: Configura l'ambiente
Definisci dove si trova il tuo PSD di origine e dove verrà salvato il file modificato, quindi carica il documento.

```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "ColorFillLayer.psd";
String exportPath     = dataDir + "ColorFillLayer_output.psd";
PsdImage im = (PsdImage) Image.load(sourceFileName);
```

- `dataDir` punta alla cartella contenente il tuo PSD.  
- `sourceFileName` è il file originale che modificherai.  
- `exportPath` è il percorso dove verrà scritto il nuovo file con il **livello di riempimento colore aggiunto**.  

### Passo 2: Scorri i livelli
Dobbiamo individuare eventuali livelli di riempimento esistenti così da poterli modificare o crearne uno nuovo.

```java
for (int i = 0; i < im.getLayers().length; i++) {
    if (im.getLayers()[i] instanceof FillLayer) {
        FillLayer fillLayer = (FillLayer) im.getLayers()[i];
```

- Il ciclo `for` itera su ogni livello nel PSD.  
- Il controllo `instanceof FillLayer` garantisce che lavoriamo solo con i livelli di riempimento.

### Passo 3: Verifica il tipo di riempimento
Assicurati che il livello trovato sia un **livello di riempimento colore** prima di tentare di cambiarne il colore.

```java
if (fillLayer.getFillSettings().getFillType() != FillType.Color) {
    throw new Exception("Wrong Fill Layer");
}
```

Se il tipo di riempimento non è `FillType.Color`, interrompiamo l'operazione per evitare di modificare involontariamente riempimenti a gradiente o pattern.

### Passo 4: Imposta il colore del riempimento
Qui è dove **impostiamo il colore del livello di riempimento**. L'esempio cambia il livello in rosso, ma puoi sostituire `Color.getRed()` con qualsiasi altro `Color` necessario (ad es., `Color.getBlue()`, `new Color(255, 165, 0)` per l'arancione).

```java
IColorFillSettings settings = (IColorFillSettings) fillLayer.getFillSettings();
settings.setColor(Color.getRed());
fillLayer.update();
```

- `settings.setColor(...)` cambia il colore effettivo del riempimento.  
- `fillLayer.update()` aggiorna il livello in modo che il nuovo colore venga applicato.  

### Passo 5: Salva le modifiche
Infine, scrivi il PSD modificato nuovamente su disco.

```java
im.save(exportPath);
break;
```

- Il `break` interrompe il ciclo dopo che il primo livello di riempimento corrispondente è stato aggiornato, il che è solitamente ciò che si desidera quando si deve **cambiare il colore di riempimento PSD** una sola volta.

## Problemi comuni e consigli
- **Nessun FillLayer trovato:** Se il tuo PSD non contiene un livello di riempimento, dovrai crearne uno usando `new FillLayer(im)` e aggiungerlo a `im.getLayers()`.  
- **Il colore non si aggiorna:** Assicurati di chiamare `fillLayer.update()` dopo aver impostato il colore.  
- **File non salvato:** Verifica che `exportPath` punti a una directory scrivibile e che tu abbia i permessi per scrivere file lì.  

## Domande frequenti

**Q: Cos'è Aspose.PSD?**  
A: Aspose.PSD è una robusta libreria Java che consente di creare, modificare e convertire file Photoshop PSD senza necessità di Adobe Photoshop.

**Q: Posso usare Aspose.PSD gratuitamente?**  
A: Sì, è disponibile una prova gratuita sulla [pagina Aspose Releases](https://releases.aspose.com/).  

**Q: Quali formati di file posso utilizzare oltre al PSD?**  
A: Aspose.PSD supporta PSD, PSB, BMP, JPEG, PNG, GIF, TIFF e altri.

**Q: Come posso ottenere supporto se incontro problemi?**  
A: Puoi porre domande sul [Forum di supporto Aspose](https://forum.aspose.com/c/psd/34).  

**Q: Dove posso acquistare una licenza completa?**  
A: Le licenze sono vendute tramite la [pagina di acquisto Aspose](https://purchase.aspose.com/buy).

## Conclusione
Ora sai **come aggiungere un riempimento** a un documento Photoshop in modo programmatico con Java. Creando o individuando un livello di riempimento colore, impostandone il colore e salvando il risultato, puoi automatizzare attività di design ripetitive, generare risorse dinamiche o integrare la manipolazione dei PSD in applicazioni Java più ampie. Provalo: sperimenta con colori diversi, aggiungi più livelli di riempimento o combina questa tecnica con altre funzionalità di Aspose.PSD per pipeline di elaborazione immagini potenti.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Ultimo aggiornamento:** 2026-03-02  
**Testato con:** Aspose.PSD for Java 24.11 (latest at time of writing)  
**Autore:** Aspose  

---