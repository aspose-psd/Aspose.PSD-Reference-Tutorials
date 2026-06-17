---
date: 2026-04-05
description: Aprenda a exportar PSD para PNG e a melhorar o contraste da imagem sem
  esforço usando Aspose.PSD para Java. Domine as Camadas de Ajuste de Níveis com este
  guia passo a passo.
keywords:
- export psd to png
- how to adjust levels
- batch process psd files
linktitle: Exportar PSD para PNG e Renderizar Camada de Ajuste de Níveis em Java
second_title: Aspose.PSD Java API
title: Exportar PSD para PNG e renderizar camada de ajuste de níveis em Java
url: /pt/java/psd-layer-management-effects/render-level-adjustment-layer-psd/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Exportar PSD para PNG e Renderizar Camada de Ajuste de Níveis em Java

## Introdução

Já abriu um arquivo PSD e percebeu que as cores parecem apagadas ou o contraste está errado? Você pode rapidamente **exportar PSD para PNG** enquanto ajusta a imagem com uma Camada de Ajuste de Níveis usando Aspose.PSD para Java. Neste tutorial, percorreremos todo o processo — desde o carregamento de um PSD, ajuste de seus níveis, até salvar o resultado como PNG — para que você aumente a vivacidade e prepare ativos prontos para a web em minutos.

## Respostas Rápidas
- **O que significa “exportar PSD para PNG”?** Converte um documento Photoshop em uma imagem PNG sem perdas, preservando a transparência.  
- **Posso ajustar níveis antes de exportar?** Sim, o Aspose.PSD permite modificar os níveis de entrada e saída programaticamente.  
- **Preciso de uma licença?** Uma avaliação gratuita funciona para desenvolvimento; uma licença comercial é necessária para produção.  
- **É possível processamento em lote?** Absolutamente — você pode colocar o código dentro de um loop para lidar com vários arquivos PSD.  
- **Qual versão do Java é necessária?** Java 8 ou superior é recomendado.

## O que é “exportar PSD para PNG”?
Exportar um PSD para PNG significa pegar o arquivo Photoshop em camadas e achatá‑lo em uma imagem Portable Network Graphics. PNG suporta compressão sem perdas e um canal alfa, tornando‑lo ideal para gráficos web e ativos de interface de usuário.

## Por que ajustar níveis antes de exportar?
Ajustar níveis permite controlar sombras, tons médios e realces, melhorando o contraste geral e o equilíbrio de cores. Esta etapa garante que o PNG final pareça polido sem a necessidade de edição manual no Photoshop.

## Pré-requisitos

- **Java Development Kit (JDK)** – baixe a versão mais recente no site da Oracle ([https://www.oracle.com/java/technologies/javase-downloads.html](https://www.oracle.com/java/technologies/javase-downloads.html)).  
- **Aspose.PSD for Java Library** – obtenha na página oficial de download ([https://releases.aspose.com/psd/java/](https://releases.aspose.com/psd/java/)). Uma avaliação gratuita está disponível ([https://releases.aspose.com/](https://releases.aspose.com/)).  

## Importar Pacotes

Antes de mergulhar no código, importe as classes que nos dão acesso à manipulação de PSD e exportação para PNG:

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.adjustmentlayers.LevelsLayer;
import com.aspose.psd.fileformats.psd.layers.layerresources.LevelChannel;
import com.aspose.psd.imageoptions.PngOptions;
```

## Guia Passo a Passo

### Etapa 1: Definir Caminhos de Arquivo (Como automatizar o processamento de PSD)

Defina variáveis claras e descritivas para o PSD de origem, o PSD modificado e o local de exportação final do PNG.

```java
String dataDir = "Your Document Directory";

String sourceFileName = dataDir + "LevelsAdjustmentLayer.psd";
String psdPathAfterChange = dataDir + "LevelsAdjustmentLayerChanged.psd";
String pngExportPath = dataDir + "LevelsAdjustmentLayerChanged.png";
```

### Etapa 2: Carregar a Imagem PSD

Use `Image.load` para ler o arquivo PSD em um objeto `PsdImage`. Aspose.PSD detecta automaticamente o formato.

```java
PsdImage im = (PsdImage)Image.load(sourceFileName);
```

### Etapa 3: Iterar pelas Camadas (Como ajustar níveis)

Percorra todas as camadas para localizar a Camada de Ajuste de Níveis.

```java
for (int i = 0; i < im.getLayers().length; i++) {
   // ... (code to check for Levels Layer will be added here)
}
```

### Etapa 4: Identificar a Camada de Níveis

Verifique cada camada com `instanceof LevelsLayer`. Quando encontrada, faça o cast para que possamos modificar suas propriedades.

```java
for (int i = 0; i < im.getLayers().length; i++) {
   if (im.getLayers()[i] instanceof LevelsLayer) {
	   LevelsLayer levelsLayer = (LevelsLayer) im.getLayers()[i];
	   // ... (code to adjust levels will be added here)
   }
}
```

### Etapa 5: Ajustar Finamente os Níveis (Como ajustar níveis)

Ajuste os níveis de entrada e saída para o primeiro canal (geralmente o canal composto). Esses valores são exemplos; sinta‑se à vontade para experimentar.

```java
for (int i = 0; i < im.getLayers().length; i++) {
   if (im.getLayers()[i] instanceof LevelsLayer) {
	   LevelsLayer levelsLayer = (LevelsLayer) im.getLayers()[i];
	   LevelChannel channel = levelsLayer.getChannel(0);

	   // Adjust Input Levels (0‑255):
	   channel.setInputShadowLevel((short) 10); // Darken shadows slightly
	   channel.setInputMidtoneLevel(2.0f);     // Increase midtones
	   channel.setInputHighlightLevel((short) 230); // Reduce highlights

	   // Adjust Output Levels (0‑255):
	   channel.setOutputShadowLevel((short) 20); // Darken shadows further
	   channel.setOutputHighlightLevel((short) 200); // Brighten highlights
   }
}
```

### Etapa 6: Salvar o PSD Modificado (Como automatizar PSD)

Persista as alterações de volta a um novo arquivo PSD.

```java
im.save(psdPathAfterChange);
```

### Etapa 7: Exportar como PNG (Exportar PSD para PNG)

Se precisar de uma versão PNG, configure `PngOptions` e salve a imagem.

```java
PngOptions saveOptions = new PngOptions();
saveOptions.setColorType(PngColorType.TruecolorWithAlpha);
im.save(pngExportPath, saveOptions);
```

## Casos de Uso Comuns

- **Preparação de ativos web:** Converta mockups PSD fornecidos por designers em PNGs prontos para navegadores.  
- **Processamento em lote:** Automatize a conversão de dezenas de arquivos PSD em um pipeline de CI.  
- **Geração dinâmica de imagens:** Ajuste níveis em tempo real com base na entrada do usuário antes de exportar.

## Solução de Problemas e Dicas

- **Ponteiro nulo ao acessar camadas:** Certifique‑se de que o PSD realmente contém uma Camada de Ajuste de Níveis; caso contrário, adicione uma verificação de nulo.  
- **Cores inesperadas após exportação:** Verifique se o tipo de cor PNG está definido como `TruecolorWithAlpha` para manter a transparência.  
- **Desempenho com muitos arquivos:** Reutilize a mesma instância `PsdImage` ao processar um lote para reduzir o consumo de memória.

## Perguntas Frequentes

**Q: Posso ajustar canais de cor individuais (RGB) separadamente?**  
A: Sim. Use `levelsLayer.getChannel(index)` onde `index` = 0 (Vermelho), 1 (Verde), 2 (Azul) para ajustar cada canal independentemente.

**Q: Como lidar com múltiplas Camadas de Ajuste de Níveis em um PSD?**  
A: O loop processa cada camada; cada `LevelsLayer` encontrado será ajustado de acordo com o código dentro do bloco `if`.

**Q: Existem outras maneiras de melhorar o contraste além de Níveis?**  
A: Aspose.PSD também oferece ajustes de Curvas, Brilho/Contraste e Equalização de Histograma.

**Q: Posso automatizar isso para uma pasta de arquivos PSD?**  
A: Envolva todo o fluxo de trabalho em um loop `File[] files = new File(dataDir).listFiles((d, name) -> name.endsWith(".psd"));` e processe cada arquivo sequencialmente.

**Q: Onde posso encontrar mais documentação e suporte?**  
A: Visite a referência oficial ([https://reference.aspose.com/psd/java/](https://reference.aspose.com/psd/java/)) e o fórum da comunidade ([https://forum.aspose.com/c/psd/34](https://forum.aspose.com/c/psd/34)).

## Conclusão

Ao dominar o fluxo de trabalho de **exportar PSD para PNG** e aprender **como ajustar níveis** programaticamente, você obtém controle total sobre a qualidade da imagem sem sair do seu ambiente Java. Seja preparando ativos para a web, automatizando um pipeline de design ou construindo um processador em lote, o Aspose.PSD para Java torna a tarefa simples e confiável.

---

**Last Updated:** 2026-04-05  
**Tested With:** Aspose.PSD 24.11 for Java  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}