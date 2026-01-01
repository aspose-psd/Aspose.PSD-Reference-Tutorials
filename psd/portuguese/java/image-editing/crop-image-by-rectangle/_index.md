---
date: 2026-01-01
description: Explore como recortar imagens em Java usando Aspose.PSD para Java. Siga
  nosso guia passo a passo para carregar um arquivo PSD, recortar um retângulo da
  imagem e converter o PSD em JPEG.
linktitle: Crop Image by Rectangle
second_title: Aspose.PSD Java API
title: 'Cortar Imagem Java: Cortar Imagem por Retângulo com Aspose.PSD'
url: /pt/java/image-editing/crop-image-by-rectangle/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Crop Image Java: Crop Image by Rectangle with Aspose.PSD

## Introduction

Manipular gráficos é uma parte rotineira do **processamento de imagens java**, e o Aspose.PSD for Java oferece uma API limpa e de alto desempenho para trabalhar com arquivos PSD. Neste tutorial você aprenderá **como recortar uma imagem** usando um retângulo, carregar um arquivo PSD e, finalmente, converter o resultado para JPEG — tudo com apenas algumas linhas de código Java.

## Quick Answers
- **O que significa “crop image java”?** Refere‑se a cortar uma imagem para um retângulo definido usando código Java.  
- **Qual biblioteca realiza a operação?** Aspose.PSD for Java fornece as classes necessárias.  
- **Preciso de licença para testes?** Um teste gratuito está disponível; a licença é necessária para produção.  
- **Posso converter o PSD recortado para JPEG?** Sim — use `JpegOptions` ao salvar.  
- **Quanto tempo leva a implementação?** Normalmente menos de 10 minutos para um cenário básico.

## What is cropping an image rectangle in Java?

Recortar um retângulo de imagem significa selecionar uma área específica (definida por X, Y, largura e altura) e descartar tudo que está fora dessa área. Essa operação é comum quando você precisa focar em uma região particular de um documento PSD maior.

## Why use Aspose.PSD for this task?

- **Sem dependências externas** – funciona com Java puro.  
- **Suporta PSD, PNG, JPEG e muitos outros formatos** – você pode **converter PSD para JPEG** instantaneamente.  
- **Renderização de alta fidelidade** – mantém informações de camada e perfis de cor durante o recorte.  

## Prerequisites

- Java Development Kit (JDK) instalado.  
- Biblioteca Aspose.PSD for Java – faça o download a partir do [site](https://releases.aspose.com/psd/java/).  

## Import Packages

Certifique-se de incluir os pacotes necessários em seu projeto Java para aproveitar as capacidades do Aspose.PSD for Java. Adicione as seguintes instruções de importação no início do seu arquivo Java:

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;
import com.aspose.psd.Rectangle;

import com.aspose.psd.imageoptions.JpegOptions;
```

Agora, vamos dividir o processo em várias etapas para guiá‑lo no recorte de uma imagem por retângulo usando Aspose.PSD for Java.

## Step 1: Set up Your Document Directory

```java
String dataDir = "Your Document Directory";
```

Substitua `"Your Document Directory"` pelo caminho real onde seu arquivo PSD está localizado.

## Step 2: Specify Source and Destination Files

```java
String sourceFile = dataDir + "sample.psd";
String destName = dataDir + "CroppingByRectangle_out.jpg";
```

Defina os caminhos para o seu arquivo PSD de origem e o arquivo JPEG de destino.

## Step 3: Load and Cache the Image

```java
RasterImage rasterImage = (RasterImage)Image.load(sourceFile);

if (!rasterImage.isCached()) {
    rasterImage.cacheData();
}
```

Aqui nós **carregamos o arquivo PSD** em uma instância `RasterImage` e armazenamos em cache seus dados para melhorar o desempenho.

## Step 4: Create and Define the Crop Rectangle

```java
Rectangle rectangle = new Rectangle(20, 20, 20, 20);
```

Crie uma instância da classe `Rectangle` com o tamanho desejado para o recorte. Os parâmetros representam **X**, **Y**, **largura** e **altura**, respectivamente.

## Step 5: Crop and Save the Image

```java
rasterImage.crop(rectangle);
rasterImage.save(destName, new JpegOptions());
```

Execute a operação de recorte usando o retângulo especificado e **converta PSD para JPEG** salvando o resultado com `JpegOptions`.

Repita estas etapas conforme necessário, ajustando os parâmetros de acordo com seus requisitos específicos.

## Common Issues & Tips

- **Retângulo fora dos limites da imagem** – garanta que as coordenadas do retângulo estejam dentro das dimensões da imagem de origem.  
- **Consumo de memória** – chame `rasterImage.dispose()` após terminar para liberar recursos nativos.  
- **Controle de qualidade** – você pode definir `JpegOptions.setQuality(int)` para controlar o nível de compressão do JPEG de saída.

## Conclusion

Neste tutorial percorremos o processo de **crop image java** por um retângulo usando Aspose.PSD for Java. Seguindo estas etapas, você pode integrar facilmente recursos poderosos de manipulação de imagens — carregar um arquivo PSD, recortar uma região específica e converter o resultado para JPEG — em qualquer aplicação Java.

## FAQ's

### Q1: Posso usar Aspose.PSD for Java com outros frameworks Java?

A1: Sim, o Aspose.PSD for Java pode ser integrado a diversos frameworks Java, oferecendo flexibilidade em seus projetos de desenvolvimento.

### Q2: Existe uma versão de teste gratuita do Aspose.PSD for Java?

A2: Sim, você pode acessar a versão de teste gratuita [aqui](https://releases.aspose.com/).

### Q3: Onde posso encontrar suporte ou assistência adicional?

A3: Visite o [fórum Aspose.PSD](https://forum.aspose.com/c/psd/34) para suporte da comunidade e discussões.

### Q4: Como obtenho uma licença temporária para Aspose.PSD for Java?

A4: Você pode adquirir uma licença temporária [aqui](https://purchase.aspose.com/temporary-license/).

### Q5: Quais são os formatos de imagem suportados para recorte no Aspose.PSD for Java?

A5: O Aspose.PSD for Java suporta vários formatos de imagem, incluindo PSD, PNG, JPEG e outros.

---

**Last Updated:** 2026-01-01  
**Tested With:** Aspose.PSD for Java 24.12  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}