---
date: 2026-03-23
description: Scopri come creare file PSD con riempimento a gradiente usando Java e
  Aspose.PSD. Questa guida mostra come modificare i livelli a gradiente dei PSD, regolare
  i colori, la trasparenza e altre proprietà in modo programmatico.
linktitle: Create Gradient Fill PSD with Java – Add Gradient Fill Layer
second_title: Aspose.PSD Java API
title: Crea un PSD con riempimento gradiente in Java – Aggiungi un livello di riempimento
  gradiente
url: /it/java/psd-image-modification-conversion/add-gradient-fill-layer-psd-files/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aggiungi livello di riempimento gradiente nei file PSD con Java

## Introduzione

Hai mai desiderato quel tocco extra di magia visiva per i tuoi file PSD e ti sei chiesto **come creare un riempimento gradiente PSD** con Java? I gradienti danno profondità ai tuoi progetti, ma modificarli manualmente può essere noioso. Con **Aspose.PSD for Java**, puoi modificare programmaticamente i gradienti PSD, cambiare i colori, regolare la trasparenza e perfezionare ogni proprietà—risparmiando tempo e garantendo coerenza su decine di file.

## Risposte rapide
- **Quale libreria consente di modificare i gradienti PSD in Java?** Aspose.PSD for Java.  
- **Quale metodo carica un file PSD?** `Image.load(path)`.  
- **Come si cambia l'angolo del gradiente?** `settings.setAngle(double)`.  
- **Puoi aggiungere nuovi punti colore?** Sì—crea oggetti `GradientColorPoint` e aggiungili alla lista dei punti colore.  
- **È necessaria una licenza per l'uso in produzione?** È richiesta una licenza commerciale; è disponibile una prova gratuita per la valutazione.

## Cos'è “creare un riempimento gradiente PSD”?
Creare un riempimento gradiente PSD significa inserire o modificare programmaticamente un livello di riempimento basato su gradiente all'interno di un documento Photoshop. Questo consente stilizzazione automatizzata, elaborazione batch e generazione dinamica di immagini senza aprire Photoshop.

## Perché usare Aspose.PSD per modificare i gradienti PSD?
- **Supporto completo .PSD** – funziona con tutti i tipi di livello, inclusi gli smart object.  
- **Nessun Photoshop richiesto** – esegui su qualsiasi server o pipeline CI.  
- **Controllo granulare** – regola angolo, offset, dithering, punti colore e punti trasparenza tramite una pulita API Java.  

## Prerequisiti

Prima di iniziare, assicurati di avere quanto segue:

- Java Development Kit (JDK):  Una versione stabile del JDK è necessaria per eseguire il codice Java. Puoi scaricarla dal sito Oracle: [Link to Oracle JDK download page]
- Aspose.PSD for Java: Questa potente libreria ti consente di lavorare con file PSD nelle tue applicazioni Java. Scaricala dal sito Aspose: [Link to Aspose.PSD for Java download] (Prova gratuita disponibile)

## Importa pacchetti

Iniziamo importando i pacchetti Aspose.PSD essenziali per lavorare con i file PSD:

```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.IGradientColorPoint;
import com.aspose.psd.fileformats.psd.layers.filllayers.FillLayer;
import com.aspose.psd.fileformats.psd.layers.fillsettings.FillType;
import com.aspose.psd.fileformats.psd.layers.fillsettings.GradientColorPoint;
import com.aspose.psd.fileformats.psd.layers.fillsettings.GradientTransparencyPoint;
import com.aspose.psd.fileformats.psd.layers.fillsettings.IGradientFillSettings;
import com.aspose.psd.fileformats.psd.layers.fillsettings.IGradientTransparencyPoint;
import com.aspose.psd.imageoptions.PsdOptions;
import java.util.ArrayList;
import java.util.Collections;
import java.util.List;
```

Queste importazioni forniscono l'accesso a classi e metodi per caricare, manipolare e salvare file PSD.

Ora, allacciati per l'entusiasmante viaggio di modifica dei livelli di riempimento gradiente!

## Come creare un riempimento gradiente PSD con Java

### Passo 1: Carica il file PSD

Innanzitutto, dobbiamo caricare il file PSD contenente il livello di riempimento gradiente che desideri modificare. Usa il metodo `Image.load`, specificando il percorso del file:

```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "ComplexGradientFillLayer.psd";
String outputFile = dataDir + "ComplexGradientFillLayer_output.psd";
PsdImage image = (PsdImage)Image.load(sourceFileName);
```

Questo frammento di codice carica il file PSD dalla directory specificata e lo memorizza nella variabile `image`.

### Passo 2: Identifica il livello di riempimento gradiente

I file PSD possono contenere numerosi livelli. Dobbiamo isolare il livello specifico che contiene il riempimento gradiente che vogliamo modificare. Itera attraverso l'array `image.getLayers()` per trovare il livello desiderato:

```java
for (int i = 0; i < image.getLayers().length; i++) {
if (image.getLayers()[i] instanceof FillLayer) {
   FillLayer fillLayer = (FillLayer) image.getLayers()[i];
   // Further checks and modifications will happen here
   break;
}
}
```

Questo ciclo controlla ogni livello. Se un livello è un `FillLayer`, viene convertito al tipo `FillLayer` e memorizzato nella variabile `fillLayer` per ulteriori elaborazioni. Possiamo aggiungere controlli aggiuntivi all'interno del ciclo se hai criteri specifici per identificare il livello target (ad es., nome del livello).

### Passo 3: Verifica il tipo di riempimento gradiente

Non tutti i livelli di riempimento utilizzano gradienti. Questo frammento di codice conferma se il livello identificato contiene effettivamente un riempimento gradiente:

```java
if (fillLayer.getFillSettings().getFillType() != FillType.Gradient) {
   throw new Exception("Wrong Fill Layer");
}
```

Se il metodo `getFillType` non restituisce `FillType.Gradient`, viene lanciata un'eccezione, indicando che stiamo lavorando sul livello sbagliato.

## Come modificare il gradiente PSD usando Aspose.PSD

### Passo 4: Accedi e modifica le proprietà del gradiente

Qui avviene la magia! Aspose.PSD fornisce l'accesso a varie proprietà del riempimento gradiente tramite l'interfaccia `IGradientFillSettings`. Possiamo recuperarle e modificarle secondo necessità:

```java
IGradientFillSettings settings = (IGradientFillSettings) fillLayer.getFillSettings();

// Modify properties (replace with desired values)
settings.setAngle(0.0);  // Set angle to 0 degrees
settings.setDither(false);  // Disable dithering
settings.setAlignWithLayer(true); // Align gradient with layer
settings.setReverse(true);  // Reverse gradient direction
settings.setHorizontalOffset(25);  // Set horizontal offset
settings.setVerticalOffset(-15);  // Set vertical offset
```

Questo codice recupera l'oggetto `IGradientFillSettings` e poi modifica proprietà come angolo, dithering, allineamento e offset. Sostituisci i valori forniti con le impostazioni desiderate per ottenere l'effetto gradiente che immagini.

### Passo 5: Manipola i punti colore e trasparenza

I gradienti sono definiti da punti colore e trasparenza lungo uno spettro. Aspose.PSD ti consente di modificare questi punti per un controllo preciso:

```java
List<IGradientColorPoint> colorPoints = new ArrayList<IGradientColorPoint>();
Collections.addAll(colorPoints, settings.getColorPoints());
List<IGradientTransparencyPoint> transparencyPoints = new ArrayList<IGradientTransparencyPoint>();
Collections.addAll(transparencyPoints, settings.getTransparencyPoints());

// Add a new color point
GradientColorPoint gr1 = new GradientColorPoint();
gr1.setColor(Color.getViolet());
gr1.setLocation(4096);
gr1.setMedianPointLocation(75);
colorPoints.add(gr1);

// Modify an existing color point
colorPoints.get(1).setLocation(3000);

// Add a new transparency point
GradientTransparencyPoint gr2 = new GradientTransparencyPoint();
gr2.setOpacity(80.0);
gr2.setLocation(4096);
gr2.setMedianPointLocation(25);
transparencyPoints.add(gr2);

// Modify an existing transparency point
transparencyPoints.get(2).setLocation(3000);

settings.setColorPoints(colorPoints.toArray(new IGradientColorPoint[0]));
settings.setTransparencyPoints(transparencyPoints.toArray(new IGradientTransparencyPoint[0]));
```

### Passo 6: Aggiorna e salva il file PSD

Una volta apportate le modifiche necessarie, aggiorna il livello di riempimento e salva il file PSD:

```java
fillLayer.update();
image.save(outputFile, new PsdOptions(image));
```

Il metodo `fillLayer.update()` applica le modifiche al livello di riempimento gradiente, e `image.save` salva il file PSD modificato nel percorso di output specificato.

## Problemi comuni e soluzioni

- **Eccezione “Wrong Fill Layer”** – Assicurati di puntare a un `FillLayer` che effettivamente utilizza un gradiente. Controlla il nome o l'indice del livello prima del cast.  
- **I punti colore non riflettono le modifiche** – Dopo aver modificato la lista dei punti, chiama sempre `settings.setColorPoints(...)` e `settings.setTransparencyPoints(...)` per inviare gli aggiornamenti al livello.  
- **Prestazioni su PSD di grandi dimensioni** – Se elabori molti file, riutilizza la stessa istanza `PsdOptions` e chiudi le immagini prontamente con `image.dispose()` per liberare memoria.

## Domande frequenti

**Q: Posso aggiungere più punti colore e trasparenza a un gradiente?**  
A: Assolutamente! Puoi aggiungere quanti punti colore e trasparenza desideri per ottenere l'effetto gradiente desiderato. Basta creare nuovi punti e aggiungerli alle rispettive liste.

**Q: Come rimuovo un punto colore o trasparenza da un gradiente?**  
A: Usa il metodo `remove` della lista, ad esempio `colorPoints.remove(index)`, per eliminare il punto indesiderato prima di chiamare `setColorPoints`.

**Q: Posso cambiare il tipo di gradiente (lineare, radiale, ecc.)?**  
A: Attualmente Aspose.PSD supporta i gradienti lineari. Future versioni potrebbero aggiungere altri tipi, ma è possibile simulare altri effetti manipolando i punti colore e trasparenza.

**Q: C'è un impatto sulle prestazioni quando si modificano i gradienti?**  
A: L'impatto dipende dalla complessità del gradiente e dal numero di modifiche. Per i casi d'uso tipici l'overhead è minimo, ma l'elaborazione batch di file di grandi dimensioni può beneficiare di ottimizzazioni nella gestione della memoria.

**Q: Posso applicare questa tecnica a più livelli di riempimento gradiente in un file PSD?**  
A: Sì. Itera attraverso `image.getLayers()`, controlla ogni `FillLayer` per `FillType.Gradient` e applica le stesse modifiche secondo necessità.

**Q: È necessaria una licenza commerciale per l'uso in produzione?**  
A: È richiesta una licenza valida di Aspose.PSD per le distribuzioni in produzione. È disponibile una prova gratuita per scopi di valutazione.

---

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

**Last Updated:** 2026-03-23  
**Tested With:** Aspose.PSD for Java 24.11 (latest)  
**Author:** Aspose