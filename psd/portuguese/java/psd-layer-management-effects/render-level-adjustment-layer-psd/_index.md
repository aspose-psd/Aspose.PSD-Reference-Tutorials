---
title: Camada de ajuste de nível de renderização em arquivos PSD - Java
linktitle: Camada de ajuste de nível de renderização em arquivos PSD - Java
second_title: API Java Aspose.PSD
description: Aprenda como melhorar facilmente o contraste e a vibração da imagem usando Aspose.PSD para Java. Domine as camadas de ajuste de níveis com este guia passo a passo.
weight: 17
url: /pt/java/psd-layer-management-effects/render-level-adjustment-layer-psd/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Camada de ajuste de nível de renderização em arquivos PSD - Java

## Introdução

Você já abriu um arquivo PSD e descobriu que a imagem estava sem contraste ou vibração? Não tenham medo, guerreiros da edição de imagens! Aspose.PSD para Java vem ao resgate com seus poderosos recursos de manipulação de camada de ajuste de níveis. Este guia irá equipá-lo com o conhecimento para ajustar suas imagens usando níveis com facilidade. 

## Pré-requisitos

- Java Development Kit (JDK): Certifique-se de ter uma versão recente do JDK instalada em seu sistema. Você pode baixá-lo no site da Oracle ([https://www.oracle.com/java/technologies/javase-downloads.html](https://www.oracle.com/java/technologies/javase-downloads.html)).
- Biblioteca Aspose.PSD para Java: Baixe a biblioteca Aspose.PSD para Java na página de download ([https://releases.aspose.com/psd/java/](https://releases.aspose.com/psd/java/)). Você precisará de uma licença válida para usar todos os recursos, mas uma avaliação gratuita está disponível para você começar ([https://releases.aspose.com/](https://releases.aspose.com/)).

## Importar pacotes

Antes de mergulhar no código, precisamos importar as classes Aspose.PSD necessárias para interagir com os arquivos PSD. Aqui está o que você precisa:

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.adjustmentlayers.LevelsLayer;
import com.aspose.psd.fileformats.psd.layers.layerresources.LevelChannel;
import com.aspose.psd.imageoptions.PngOptions;
```

 O`com.aspose.psd` pacote fornece acesso a funcionalidades de manipulação de PSD, enquanto`com.aspose.psd.imaging.PngOptions` nos permite definir opções ao salvar a imagem como PNG.

Agora, vamos embarcar em nossa aventura de ajuste de níveis:

## Etapa 1: Configurando caminhos de arquivo:

- Defina variáveis para o seu diretório de documentos (`dataDir`), nome do arquivo PSD de origem (`sourceFileName`), nome do arquivo PSD de destino após modificação (`psdPathAfterChange`) e o caminho final de exportação PNG (`pngExportPath`). Considere usar nomes descritivos para melhorar a legibilidade do código.

```java
String dataDir = "Your Document Directory";

String sourceFileName = dataDir + "LevelsAdjustmentLayer.psd";
String psdPathAfterChange = dataDir + "LevelsAdjustmentLayerChanged.psd";
String pngExportPath = dataDir + "LevelsAdjustmentLayerChanged.png";
```

## Passo 2: Carregando a imagem PSD:

-  Use o`Image.load` método para abrir o arquivo PSD de origem e armazená-lo em um`PsdImage`objeto (`im`). Aspose.PSD detecta automaticamente o formato do arquivo.

```java
PsdImage im = (PsdImage)Image.load(sourceFileName);
```

## Etapa 3: iterando por meio de camadas:

- Precisamos encontrar a camada de ajuste de níveis em seu PSD. Aspose fornece uma maneira conveniente de iterar por todas as camadas usando um loop.

```java
for (int i = 0; i < im.getLayers().length; i++) {
   // ... (o código para verificar a camada de níveis será adicionado aqui)
}
```

## Etapa 4: Identificando a camada de níveis:

- Dentro do loop, verifique se a camada atual (`im.getLayers()[i]` ) é uma instância do`LevelsLayer` aula usando o`instanceof` operador. 
-  Se for, lance a camada para um`LevelsLayer` objeto para manipulação adicional.

```java
for (int i = 0; i < im.getLayers().length; i++) {
   if (im.getLayers()[i] instanceof LevelsLayer) {
	   LevelsLayer levelsLayer = (LevelsLayer) im.getLayers()[i];
	   // ... (o código para ajustar os níveis será adicionado aqui)
   }
}
```
## Etapa 5: Níveis de ajuste fino (continuação):

-  Ajuste os níveis de saída usando`setOutputShadowLevel` e`setOutputHighlightLevel` para controlar a escuridão e a clareza da imagem resultante. Esses valores determinam a faixa de níveis de entrada que serão mapeados para a faixa de saída.

```java
for (int i = 0; i < im.getLayers().length; i++) {
   if (im.getLayers()[i] instanceof LevelsLayer) {
	   LevelsLayer levelsLayer = (LevelsLayer) im.getLayers()[i];
	   LevelChannel channel = levelsLayer.getChannel(0);

	   // Ajustar os níveis de entrada (0-255):
	   channel.setInputShadowLevel((short) 10); // Escurecer ligeiramente as sombras
	   channel.setInputMidtoneLevel(2.0f);     // Aumentar tons médios
	   channel.setInputHighlightLevel((short) 230); // Reduzir destaques

	   // Ajuste os níveis de saída (0-255):
	   channel.setOutputShadowLevel((short) 20); // Escurecer ainda mais as sombras
	   channel.setOutputHighlightLevel((short) 200); //Iluminar destaques
   }
}
```

## Etapa 6: Salvando o PSD modificado:

-  Use o`save` método do`PsdImage` objeto para salvar a imagem modificada no caminho especificado (`psdPathAfterChange`).

```java
im.save(psdPathAfterChange);
```

## Etapa 7: Exportar como PNG (opcional):

-  Se você precisar de uma versão PNG da imagem ajustada, crie um`PngOptions` objeto e defina o tipo de cor como`TruecolorWithAlpha` . Então, use o`save` método novamente com o caminho de exportação PNG e opções.

```java
PngOptions saveOptions = new PngOptions();
saveOptions.setColorType(PngColorType.TruecolorWithAlpha);
im.save(pngExportPath, saveOptions);
```

E aí está! Você ajustou com sucesso a camada de ajuste de níveis em seu arquivo PSD usando Aspose.PSD para Java. Ao compreender essas etapas e experimentar diferentes valores, você pode melhorar o contraste e a aparência geral de suas imagens.

## Conclusão

Aspose.PSD para Java permite que você assuma o controle do processo de edição de imagens. Ao dominar a camada de ajuste de níveis, você pode dar nova vida às suas fotos e designs. Lembre-se de que a prática leva à perfeição, por isso não hesite em experimentar e explorar todo o potencial desta ferramenta poderosa.
 
## Perguntas frequentes

### Posso ajustar canais de cores individuais (RGB) separadamente? 
Sim, você pode acessar cada canal de cores usando o`getChannel` método do`LevelsLayer` objeto e modificar seus níveis de forma independente.

### Como lidar com múltiplas camadas de ajuste de níveis em um PSD?
O código itera por todas as camadas, portanto processará automaticamente quaisquer camadas adicionais de Níveis encontradas na imagem.

### Existem outras maneiras de ajustar o contraste da imagem além dos níveis?
Absolutamente! Aspose.PSD oferece várias ferramentas de ajuste de imagem como Curvas, Brilho/Contraste e muito mais.

### Posso automatizar esse processo para várias imagens? 
Sim, você pode incorporar esse código em um script de processamento em loop ou em lote para processar com eficiência vários arquivos PSD.

### Onde posso encontrar mais informações e suporte?
Aspose fornece documentação extensa ([https://reference.aspose.com/psd/java/](https://reference.aspose.com/psd/java/)) e um fórum de suporte ([https://forum.aspose.com/c/psd/34](https://forum.aspose.com/c/psd/34)) para quaisquer dúvidas ou problemas que você possa encontrar.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
