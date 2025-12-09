---
date: 2025-12-09
description: Scopri come collegare i livelli nei file PSD usando Aspose.PSD per Java.
  Questo tutorial passo‑passo ti mostra come gestire i livelli PSD, scollegare i livelli
  PSD e padroneggiare il tutorial di Aspose.PSD.
language: it
linktitle: How to Link Layers in PSD Files Using Java
second_title: Aspose.PSD Java API
title: Come collegare i livelli nei file PSD usando Java
url: /java/advanced-psd-layer-features-effects/add-linked-layer-support-psd-files/
weight: 19
---

{{< blocks/products/pf/main-wrap-class >}}  
{{< blocks/products/pf/main-container >}}  
{{< blocks/products/pf/tutorial-page-section >}}  

# Come collegare i livelli nei file PSD usando Java  

## Introduzione  
Il formato `.PSD` di Adobe Photoshop è lo standard di settore per la grafica a livelli, e molti sviluppatori hanno bisogno di manipolare questi livelli in modo programmatico. Una delle tecniche più potenti è **collegare i livelli**, che consente di spostare o modificare un gruppo di livelli come un’unica unità mantenendo intatte le proprietà individuali di ciascun livello. In questo **tutorial Aspose.PSD** vedremo **come collegare i livelli** in un file PSD usando Java, e mostreremo anche come **gestire i livelli PSD**, **scollegare i livelli PSD** e salvare le modifiche su disco. Che tu stia costruendo una pipeline di automazione del design o estendendo un’app desktop, questi passaggi ti daranno il pieno controllo sulle relazioni tra i livelli.  

## Risposte rapide  
- **Cosa significa “collegare i livelli”?** Crea un gruppo logico in modo che i livelli si muovano insieme senza essere appiattiti.  
- **Quale libreria gestisce questa funzionalità?** Aspose.PSD per Java fornisce l’API `LinkedLayersManager`.  
- **È necessaria una licenza?** Una versione di prova gratuita è sufficiente per lo sviluppo; per la produzione è richiesta una licenza commerciale.  
- **Posso scollegare in seguito?** Sì—usa i metodi `unlinkLayer` o `unlinkLayers`.  
- **Versioni Java supportate?** Java 8 o successive.  

## Che cosa significa collegare i livelli in un file PSD?  
Collegare i livelli è una funzionalità di Photoshop che unisce più livelli in modo che si comportino come un’unica entità quando vengono trasformati, spostati o stilizzati. I dati sottostanti rimangono separati, il che significa che in seguito è possibile **scollegare i livelli PSD** e modificare ciascuno indipendentemente.  

## Perché usare Aspose.PSD per Java per gestire i livelli PSD?  
- **API completa** – Accesso a ogni costrutto di Photoshop senza avviare Photoshop stesso.  
- **Cross‑platform** – Funziona su qualsiasi OS che supporti Java.  
- **Nessuna dipendenza UI** – Ideale per elaborazioni batch lato server o pipeline CI.  

## Prerequisiti  
Prima di immergerci nel codice, assicurati di avere:  

1. **Java Development Kit (JDK) 8+** – Si consiglia l’ultima versione del JDK.  
2. **Aspose.PSD per Java** – Scaricalo dalla [pagina di rilascio Aspose](https://releases.aspose.com/psd/java/).  
3. **IDE o editor** – Eclipse, IntelliJ IDEA, VS Code, ecc.  
4. **File PSD di esempio** – Creane uno in Photoshop o prendi un campione gratuito per i test.  

## Importare i pacchetti  
Prima di scrivere il codice, importa le classi necessarie di Aspose.PSD:  

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.Layer;
```  

Queste importazioni ti danno accesso alla gestione di base delle immagini, alle funzionalità specifiche di PSD e ai metodi di manipolazione dei livelli.  

## Guida passo‑passo  

### Passo 1: Caricare il file PSD  
Apri il PSD con cui vuoi lavorare.  

```java
String dataDir = "Your Document Directory"; // specify your document directory
PsdImage psd = (PsdImage) Image.load(dataDir + "LinkedLayerexample.psd");
```  

Assicurati che il percorso punti a un file esistente; altrimenti, `Image.load()` genererà un’eccezione.  

### Passo 2: Recuperare tutti i livelli (Gestire i livelli PSD)  
Ottieni ogni livello così da poter decidere quali raggruppare.  

```java
Layer[] layers = psd.getLayers();
```  

L’array `layers` contiene ora l’intera pila di livelli del documento.  

### Passo 3: Collegare i livelli  
Crea un gruppo di livelli collegati usando l’API del manager.  

```java
short layersLinkGroupId = psd.getLinkedLayersManager().linkLayers(layers);
```  

Questa chiamata restituisce un **group ID** che identifica in modo univoco il nuovo gruppo di collegamento.  

### Passo 4: Verificare il Group ID del collegamento  
Controlla che l’ID restituito corrisponda a quello memorizzato per il primo livello.  

```java
short linkGroupId = psd.getLinkedLayersManager().getLinkGroupId(layers[0]);
if (layersLinkGroupId != linkGroupId) {
    throw new Exception("layersLinkGroupId and linkGroupId are not equal.");
}
```  

Se gli ID differiscono, qualcosa è andato storto durante il collegamento.  

### Passo 5: Recuperare e scollegare i livelli (Scollegare i livelli PSD)  
Quando è necessario rompere l’associazione, recupera i livelli collegati per group ID e scollegali uno a uno.  

```java
Layer[] linkedLayers = psd.getLinkedLayersManager().getLayersByLinkGroupId(linkGroupId);
for (Layer linkedLayer : linkedLayers) {
    psd.getLinkedLayersManager().unlinkLayer(linkedLayer);
}
```  

Ogni iterazione rimuove il collegamento preservando i dati originali del livello.  

### Passo 6: Convalidare il processo di scollegamento  
Verifica che nessun livello rimanga nel gruppo.  

```java
linkedLayers = psd.getLinkedLayersManager().getLayersByLinkGroupId(linkGroupId);
if (linkedLayers != null) {
    throw new Exception("The linkedLayers field is not NULL.");
}
```  

Se `linkedLayers` è ancora popolato, l’operazione di scollegamento è fallita.  

### Passo 7: Salvare il PSD aggiornato  
Scrivi il documento modificato su disco.  

```java
psd.save(dataDir + "LinkedLayerexample_output.psd");
```  

Il salvataggio preserva tutte le modifiche, incluso il nuovo gruppo di collegamento o la sua rimozione.  

### Passo 8: Rilasciare l’oggetto PSD  
Libera le risorse native per evitare perdite di memoria.  

```java
finally {
    psd.dispose();
}
```  

Chiamare `dispose()` è una buona pratica, soprattutto quando si elaborano molti file in un ciclo.  

## Problemi comuni e consigli  

- **Percorso file errato** – Usa sempre percorsi assoluti o verifica la directory di lavoro.  
- **Licenza mancante** – La versione di prova è valida per la valutazione, ma una licenza completa rimuove le filigrane di valutazione.  
- **Collegare solo un sottoinsieme** – Se ti serve solo una parte della pila di livelli, crea un nuovo `Layer[]` con i livelli desiderati prima di chiamare `linkLayers`.  
- **Sicurezza dei thread** – Le istanze di `PsdImage` non sono thread‑safe; crea un’istanza separata per ogni thread.  

## Conclusione  
Ora disponi di un flusso di lavoro completo e pronto per la produzione su **come collegare i livelli** nei file PSD usando Aspose.PSD per Java. Padroneggiando queste API potrai automatizzare compiti di design complessi, costruire editor personalizzati o integrare la gestione dei livelli in stile Photoshop in qualsiasi applicazione Java. Continua a sperimentare con altre funzionalità come effetti di livello, maschere e oggetti intelligenti per ampliare ulteriormente il tuo toolkit.  

## FAQ  

### Che cos’è Aspose.PSD per Java?  
Aspose.PSD per Java è una libreria che consente agli sviluppatori di manipolare programmaticamente i file Photoshop PSD.  

### Posso usare Aspose.PSD su qualsiasi sistema operativo?  
Sì, essendo una libreria basata su Java, funziona su qualsiasi piattaforma che supporti Java.  

### È disponibile una versione di prova?  
Sì, puoi provare Aspose.PSD per Java gratuitamente. Consulta il [link per la prova gratuita](https://releases.aspose.com/).  

### Dove posso trovare ulteriore documentazione?  
Puoi esplorare la documentazione completa [qui](https://reference.aspose.com/psd/java/).  

### Come posso ottenere supporto in caso di problemi?  
Se incontri difficoltà, puoi trovare aiuto nel [forum di supporto](https://forum.aspose.com/c/psd/34).  

---  

**Ultimo aggiornamento:** 2025-12-09  
**Testato con:** Aspose.PSD 24.12 per Java  
**Autore:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}  

{{< /blocks/products/pf/main-container >}}  
{{< /blocks/products/pf/main-wrap-class >}}  

{{< blocks/products/products-backtop-button >}}