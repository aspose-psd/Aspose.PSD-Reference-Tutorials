---
title: Ajuste o contraste de uma imagem com Aspose.PSD para Java
linktitle: Ajustar o contraste de uma imagem
second_title: API Java Aspose.PSD
description: Explore o mundo do ajuste de contraste de imagens em Java com Aspose.PSD. Siga nosso guia passo a passo para uma manipulação perfeita de imagens.
weight: 22
url: /pt/java/advanced-techniques/adjust-contrast/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Ajuste o contraste de uma imagem com Aspose.PSD para Java

## Introdução

No domínio do processamento de imagens com Java, Aspose.PSD se destaca como uma ferramenta poderosa. Entre seus inúmeros recursos, ajustar o contraste da imagem é um requisito comum. Este tutorial orientará você no processo de ajuste do contraste da imagem usando Aspose.PSD para Java. Quer você seja um desenvolvedor experiente ou esteja apenas começando, este guia o ajudará a dominar esse aspecto essencial da manipulação de imagens.

## Pré-requisitos

Antes de mergulhar no tutorial, certifique-se de ter os seguintes pré-requisitos em vigor:

- Compreensão básica de programação Java.
-  Biblioteca Aspose.PSD para Java instalada. Você pode baixá-lo[aqui](https://releases.aspose.com/psd/java/).

## Importar pacotes

Para começar, você precisa importar os pacotes necessários para o seu projeto Java. Adicione as seguintes linhas ao seu código:

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.psd.fileformats.tiff.enums.TiffPhotometrics;
import com.aspose.psd.imageoptions.TiffOptions;
```

## Etapa 1: carregar a imagem

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

// Carregar uma imagem existente em uma instância da classe RasterImage
Image image = Image.load(sourceFile);
```

 Nesta etapa, carregamos a imagem de amostra ("sample.psd") usando o`Image.load` método.

## Etapa 2: transmitir para RasterImage e armazenar dados em cache

```java
// Transmitir objeto de imagem para RasterImage
RasterImage rasterImage = (RasterImage)image;

// Verifique se RasterImage está armazenado em cache e Cache RasterImage para melhor desempenho
if (!rasterImage.isCached()) {
    rasterImage.cacheData();
}
```

 Aqui, lançamos o genérico`Image` opor-se a um`RasterImage` para processamento específico. Armazenar em cache os dados da imagem melhora o desempenho.

## Etapa 3: ajustar o contraste

```java
// Ajuste o contraste
rasterImage.adjustContrast(50);
```

 O`adjustContrast`método é usado para modificar o contraste da imagem. Neste exemplo, o contraste é aumentado em 50%.

## Etapa 4: crie TiffOptions e salve

```java
// Crie uma instância de TiffOptions para a imagem resultante
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
int[] ushort = { 8, 8, 8 };
tiffOptions.setBitsPerSample(ushort);
tiffOptions.setPhotometric(TiffPhotometrics.Rgb);

// Salve a imagem resultante no formato TIFF
String destName = dataDir + "AdjustContrast_out.tiff";
rasterImage.save(destName, tiffOptions);
```

 Aqui, montamos`TiffOptions` para a imagem de saída, especificando o formato e outras propriedades. A imagem final é então salva em um arquivo TIFF.

## Conclusão

Parabéns! Você ajustou com sucesso o contraste de uma imagem usando Aspose.PSD para Java. Este tutorial abordou as etapas essenciais, desde a importação de pacotes até salvar a imagem processada.

## Perguntas frequentes

### Q1: O Aspose.PSD é compatível com diferentes formatos de imagem?

A1: Sim, Aspose.PSD suporta vários formatos de imagem, proporcionando flexibilidade em seus projetos.

### Q2: Como posso obter uma licença temporária para Aspose.PSD?

 A2: Você pode obter uma licença temporária[aqui](https://purchase.aspose.com/temporary-license/).

### Q3: Onde posso encontrar a documentação do Aspose.PSD?

A3: A documentação está disponível[aqui](https://reference.aspose.com/psd/java/).

### Q4: Quais opções de suporte estão disponíveis para Aspose.PSD?

 A4: Para obter suporte, visite o[Fórum Aspose.PSD](https://forum.aspose.com/c/psd/34).

### Q5: Posso comprar Aspose.PSD?

 A5: Sim, você pode comprar Aspose.PSD[aqui](https://purchase.aspose.com/buy).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
