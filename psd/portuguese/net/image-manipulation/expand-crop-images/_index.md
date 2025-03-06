---
title: Expandindo e cortando imagens em Aspose.PSD para .NET
linktitle: Expandindo e cortando imagens
second_title: API Aspose.PSD .NET
description: Aprenda como expandir e cortar imagens dinamicamente usando Aspose.PSD para .NET. Siga nosso guia passo a passo para uma manipulação perfeita de imagens.
weight: 13
url: /pt/net/image-manipulation/expand-crop-images/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Expandindo e cortando imagens em Aspose.PSD para .NET

## Introdução

Aspose.PSD for .NET é uma biblioteca de imagens abrangente que permite aos desenvolvedores trabalhar com vários formatos de imagem em seus aplicativos .NET. Um de seus recursos de destaque é a capacidade de manipular imagens com facilidade. Neste tutorial, vamos nos concentrar na expansão e corte de imagens, fornecendo um guia prático para realizar essas tarefas usando Aspose.PSD.

## Pré-requisitos

Antes de mergulhar no tutorial, certifique-se de ter os seguintes pré-requisitos em vigor:

-  Biblioteca Aspose.PSD for .NET: Certifique-se de ter a biblioteca Aspose.PSD for .NET instalada. Você pode baixá-lo no[Documentação Aspose.PSD para .NET](https://reference.aspose.com/psd/net/).

- Imagem de amostra: Prepare um arquivo de imagem de amostra (por exemplo, "example1.psd") que você usará no tutorial.

Agora, vamos começar com o guia passo a passo.

## Importar namespaces

Comece importando os namespaces necessários para aproveitar as funcionalidades fornecidas pelo Aspose.PSD para .NET. Adicione os seguintes namespaces ao seu código:

```csharp
using Aspose.PSD.ImageOptions;
```

## Etapa 1: configurar o projeto

 Certifique-se de ter um projeto configurado com Aspose.PSD para .NET integrado. Se não, siga o[documentação](https://reference.aspose.com/psd/net/) para orientação.

## Etapa 2: carregar a imagem

Carregue a imagem de exemplo usando o seguinte código:

```csharp
string dataDir = RunExamples.GetDataDir_DrawingAndFormattingImages();
string sourceFile = dataDir + @"example1.psd";

// Carregue a imagem
using (RasterImage rasterImage = (RasterImage)Image.Load(sourceFile))
{
    // Código adicional para processamento de imagem irá aqui
}
```

## Etapa 3: armazenar dados de imagem em cache

Armazene em cache os dados da imagem para otimizar o desempenho:

```csharp
rasterImage.CacheData();
```

## Etapa 4: definir o retângulo de destino

Crie uma instância da classe Rectangle e defina X, Y, Largura e Altura do retângulo. Esta será a área para a qual a imagem será expandida ou cortada.

```csharp
Rectangle destRect = new Rectangle { X = -200, Y = -200, Width = 300, Height = 300 };
```

## Etapa 5: salve a imagem de saída

Salve a imagem de saída com as opções especificadas e o retângulo de destino:

```csharp
string destName = dataDir + @"jpeg_out.jpg";
rasterImage.Save(destName, new JpegOptions(), destRect);
```

## Conclusão

Parabéns! Você aprendeu com sucesso como expandir e cortar imagens usando Aspose.PSD para .NET. Esta poderosa biblioteca abre um mundo de possibilidades para manipulação de imagens em seus aplicativos .NET.

## Perguntas frequentes

### Q1: O Aspose.PSD pode lidar com outros formatos de imagem além do PSD?

A1: Sim, Aspose.PSD oferece suporte a uma ampla variedade de formatos de imagem, incluindo JPEG, PNG, GIF e muito mais.

### P2: Onde posso encontrar suporte para Aspose.PSD?

 A2: Você pode encontrar apoio e interagir com a comunidade em[Fórum Aspose.PSD](https://forum.aspose.com/c/psd/34).

### Q3 Existe uma avaliação gratuita disponível para Aspose.PSD para .NET?

 A3: Sim, você pode explorar os recursos com uma avaliação gratuita disponível em[Avaliação gratuita do Aspose.PSD](https://releases.aspose.com/).

### Q4: Como obtenho uma licença temporária para Aspose.PSD?

 A4: Você pode obter uma licença temporária de[Licença temporária Aspose.PSD](https://purchase.aspose.com/temporary-license/).

### Q5: Onde posso comprar Aspose.PSD para .NET?

 A5: Você pode comprar a biblioteca no[Página de compra do Aspose.PSD](https://purchase.aspose.com/buy).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
