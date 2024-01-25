---
title: Ajuste a gama de uma imagem com Aspose.PSD para Java
linktitle: Ajustar gama de uma imagem
second_title: API Java Aspose.PSD
description: Aprenda a ajustar a gama da imagem sem esforço usando Aspose.PSD para Java. Siga nosso guia passo a passo para obter os melhores resultados.
type: docs
weight: 23
url: /pt/java/advanced-techniques/adjust-gamma/
---
## Introdução

No domínio do processamento de imagens, ajustar a gama de uma imagem é um passo crucial para melhorar o seu apelo visual. Aspose.PSD para Java oferece uma solução poderosa para desenvolvedores Java manipularem facilmente a gama de imagens. Neste tutorial, exploraremos como ajustar gama usando Aspose.PSD, detalhando cada etapa para garantir uma implementação perfeita.

## Pré-requisitos

Antes de mergulhar no tutorial, certifique-se de ter os seguintes pré-requisitos configurados:

1. Ambiente de desenvolvimento Java: certifique-se de ter um ambiente de desenvolvimento Java instalado em seu sistema.
2.  Biblioteca Aspose.PSD: Baixe e integre a biblioteca Aspose.PSD ao seu projeto Java. Você pode encontrar os recursos necessários no[documentação](https://reference.aspose.com/psd/java/).
3. Imagem de amostra: prepare uma imagem PSD de amostra que você usará para aplicar o ajuste de gama.

## Importar pacotes

Para iniciar o processo, importe os pacotes necessários em seu projeto Java. Isso prepara o terreno para a utilização perfeita das funcionalidades do Aspose.PSD.

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.psd.fileformats.tiff.enums.TiffPhotometrics;
import com.aspose.psd.imageoptions.TiffOptions;
```

## Etapa 1: carregar a imagem

 Comece carregando a imagem PSD de amostra em uma instância do`RasterImage` aula. Esta é a base para ajustes gama subsequentes.

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

// Carregar uma imagem existente em uma instância da classe RasterImage
Image image = Image.load(sourceFile);

// Transmitir objeto de imagem para RasterImage
RasterImage rasterImage = (RasterImage)image;

// Verifique se o RasterImage está armazenado em cache para melhor desempenho
if (!rasterImage.isCached()) {
    rasterImage.cacheData();
}
```

## Etapa 2: ajustar gama

 Agora, ajuste a gama da imagem carregada usando o`adjustGamma` método. Ajuste os valores gama de acordo com suas necessidades.

```java
// Ajuste a gama
rasterImage.adjustGamma(2.2f, 2.2f, 2.2f);
```

## Etapa 3: criar opções Tiff

 Crie uma instância de`TiffOptions` para a imagem resultante. Defina diversas propriedades, como bits por amostra e opções fotométricas, para adaptar a saída às suas especificações.

```java
// Crie uma instância de TiffOptions para a imagem resultante
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
int[] ushort = { 8, 8, 8 };
tiffOptions.setBitsPerSample(ushort);
tiffOptions.setPhotometric(TiffPhotometrics.Rgb);
```

## Etapa 4: salve a imagem resultante

 Salve a imagem manipulada no formato TIFF usando o formato previamente definido`TiffOptions`.

```java
// Salve a imagem resultante no formato TIFF
String destName = dataDir + "AdjustGamma_out.tiff";
rasterImage.save(destName, tiffOptions);
```

## Conclusão

Parabéns! Você ajustou com sucesso a gama de uma imagem usando Aspose.PSD para Java. Esse processo permite que os desenvolvedores melhorem a qualidade da imagem sem esforço, contribuindo para uma experiência do usuário visualmente atraente.

## Perguntas frequentes

### Q1: Onde posso encontrar a documentação do Aspose.PSD?

 A1: Você pode acessar a documentação em[https://reference.aspose.com/psd/java/](https://reference.aspose.com/psd/java/).

### Q2: Como faço o download do Aspose.PSD para Java?

 A2: Baixe a biblioteca de[https://releases.aspose.com/psd/java/](https://releases.aspose.com/psd/java/).

### Q3: Onde posso comprar o Aspose.PSD?

 A3: Visita[https://purchase.aspose.com/buy](https://purchase.aspose.com/buy) para comprar Aspose.PSD.

### Q4: Existe um teste gratuito disponível?

 A4: Sim, você pode explorar uma avaliação gratuita em[https://releases.aspose.com/](https://releases.aspose.com/).

### Q5: Onde posso procurar suporte para Aspose.PSD?

 A5: Para suporte, visite o fórum Aspose.PSD em[https://forum.aspose.com/c/psd/34](https://forum.aspose.com/c/psd/34).