---
date: 2026-03-07
description: Aprenda a ajustar os níveis adicionando uma Camada de Ajuste de Níveis
  em arquivos PSD usando o Aspose.PSD para Java. Domine rapidamente os ajustes tonais.
linktitle: Add Level Adjustment Layer in PSD
second_title: Aspose.PSD Java API
title: Como Ajustar Níveis – Adicionar Camada de Ajuste de Níveis no PSD
url: /pt/java/modifying-converting-psd-images/add-level-adjustment-layer-psd/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Adicionar Camada de Ajuste de Níveis no PSD

## Introduction
Se você está procurando **como ajustar níveis** em seus documentos do Photoshop, a Camada de Ajuste de Níveis é a ferramenta perfeita. Ela permite ajustar finamente sombras, meios‑tons e realces sem alterar permanentemente os pixels originais. Neste tutorial, vamos percorrer a adição de uma Camada de Ajuste de Níveis a um arquivo PSD usando Aspose.PSD for Java, para que você possa alcançar controle tonal de nível profissional em apenas alguns passos.

## Quick Answers
- **O que faz uma Camada de Ajuste de Níveis?** Ela modifica a faixa tonal de uma imagem de forma não destrutiva.  
- **Qual biblioteca é usada?** Aspose.PSD for Java.  
- **Preciso de uma licença?** Uma avaliação gratuita funciona para desenvolvimento; uma licença é necessária para produção.  
- **Quanto tempo leva a implementação?** Cerca de 10‑15 minutos para um ajuste básico.  
- **Posso ajustar múltiplos canais?** Sim, você pode definir níveis de entrada/saída para cada canal de cor individualmente.

## What is a Level Adjustment Layer?
Uma Camada de Ajuste de Níveis permite corrigir o equilíbrio tonal de uma imagem ajustando sombras de entrada, meios‑tons e realces, bem como níveis de saída. Como ela reside em sua própria camada, você pode alternar sua visibilidade ou excluí‑la sem afetar a arte subjacente.

## Why add a Level Adjustment Layer with Aspose.PSD?
- **Automação:** Integre ajustes de níveis em pipelines de processamento em lote.  
- **Multiplataforma:** Funciona em qualquer SO que suporte Java.  
- **Precisão:** Acesse as configurações de cada canal programaticamente para resultados exatos.  

## Prerequisites
1. Java Development Kit (JDK). Se você não o tem, faça o download no [Oracle website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html) ou use OpenJDK.  
2. Biblioteca Aspose.PSD for Java – obtenha o JAR mais recente neste [download link](https://releases.aspose.com/psd/java/).  
3. Conhecimento básico de programação Java.  
4. Uma IDE como IntelliJ IDEA, Eclipse ou NetBeans com o JAR Aspose.PSD adicionado ao classpath do projeto.

## Import Packages
Before we start writing our code, we need to import the necessary packages from the Aspose.PSD library. Here’s how you can do it:
```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.adjustmentlayers.LevelsLayer;
import com.aspose.psd.fileformats.psd.layers.layerresources.LevelChannel;
```
These imports give us access to classes for loading PSD files, working with level adjustment layers, and manipulating individual channel settings.

## How to Adjust Levels in a PSD File
Below is a step‑by‑step guide that shows you exactly **how to adjust levels** programmatically.

### Step 1: Set Up Your File Paths
Define where the source PSD resides and where the edited file will be saved.
```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "LevelsAdjustmentLayer.psd";
String psdPathAfterChange = dataDir + "LevelsAdjustmentLayerChanged.psd";
```
Replace `"Your Document Directory"` with the actual folder on your machine.

### Step 2: Load the PSD File
Create a `PsdImage` instance from the source file.
```java
PsdImage im = (PsdImage) Image.load(sourceFileName);
```
Now you have full access to all layers inside the PSD.

### Step 3: Iterate Through the Layers
Find the Level Adjustment Layer you want to modify.
```java
for (int i = 0; i < im.getLayers().length; i++) {
    if (im.getLayers()[i] instanceof LevelsLayer) {
        LevelsLayer levelsLayer = (LevelsLayer) im.getLayers()[i];
        // Further manipulation will go here...
    }
}
```
The `instanceof LevelsLayer` check ensures we only work with level adjustment layers.

### Step 4: Adjust the Level Channel Settings
Tweak the input and output values for the selected channel.
```java
LevelChannel channel = levelsLayer.getChannel(0);
channel.setInputMidtoneLevel(2.0f);
channel.setInputShadowLevel((short) 10);
channel.setInputHighlightLevel((short) 230);
channel.setOutputShadowLevel((short) 20);
channel.setOutputHighlightLevel((short) 200);
```
- **Nível Médio de Entrada:** Desloca a faixa de meios‑tons.  
- **Nível de Sombra de Entrada:** Escurece ou clareia as sombras.  
- **Nível de Realce de Entrada:** Controla as partes mais claras.  
- **Níveis de Saída de Sombra/Realce:** Definem a faixa final de saída.

Feel free to experiment with different values to see how they affect the image.

### Step 5: Save the Modified PSD File
Persist your changes to a new file.
```java
im.save(psdPathAfterChange);
```
You’ll find the updated PSD at the location you specified in `psdPathAfterChange`.

## Common Issues and Solutions
- **Arquivo não encontrado:** Verifique se `dataDir` aponta para a pasta correta e se o PSD de origem existe.  
- **ClassCastException:** Certifique‑se de que o arquivo carregado é realmente um PSD; outros formatos exigem classes diferentes.  
- **Erros de licença:** Use uma licença válida do Aspose.PSD para builds de produção; a avaliação funciona para desenvolvimento.

## Conclusion
You now know **how to adjust levels** by adding and configuring a Level Adjustment Layer in a PSD file with Aspose.PSD for Java. This technique gives you precise control over tonal balance while keeping your workflow fully automated. Keep experimenting with different channel values and explore batch processing to apply the same adjustments to multiple images.

## Frequently Asked Questions

**Q: What is a Level Adjustment Layer?**  
A: It’s a non‑destructive layer that lets you modify the tonal range (shadows, mid‑tones, highlights) of an image.

**Q: Can I use Aspose.PSD without purchasing a license?**  
A: Yes, you can evaluate the library with a free trial, but a license is required for commercial deployment.

**Q: Where can I find documentation for Aspose.PSD?**  
A: You can find the documentation [here](https://reference.aspose.com/psd/java/).

**Q: Is there community support for Aspose products?**  
A: Absolutely! You can ask questions and get help in the [Aspose forum](https://forum.aspose.com/c/psd/34).

**Q: How can I get a temporary license for Aspose.PSD?**  
A: You can apply for a temporary license [here](https://purchase.aspose.com/temporary-license/).

---

**Última atualização:** 2026-03-07  
**Testado com:** Aspose.PSD última versão (Java)  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}