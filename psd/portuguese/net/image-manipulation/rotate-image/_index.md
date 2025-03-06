---
title: Girando uma imagem em Aspose.PSD para .NET
linktitle: Girando uma imagem
second_title: API Aspose.PSD .NET
description: Aprenda a girar imagens sem esforço em .NET com Aspose.PSD. Siga nosso tutorial passo a passo.
weight: 15
url: /pt/net/image-manipulation/rotate-image/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Girando uma imagem em Aspose.PSD para .NET

## Introdução

Se você está mergulhando no mundo da manipulação de imagens usando .NET, Aspose.PSD é sua ferramenta ideal para processamento de imagens contínuo e eficiente. Neste tutorial, vamos nos concentrar em uma tarefa fundamental – girar uma imagem usando Aspose.PSD para .NET. Acompanhe enquanto dividimos o processo em etapas simples e práticas.

## Pré-requisitos

Antes de começarmos, certifique-se de ter os seguintes pré-requisitos em vigor:

-  Biblioteca Aspose.PSD para .NET: Baixe e instale a biblioteca do[Documentação Aspose.PSD .NET](https://reference.aspose.com/psd/net/).

- Seu diretório de documentos: configure um diretório onde suas imagens são armazenadas. Substitua "Seu diretório de documentos" no trecho de código pelo caminho para este diretório.

## Importar namespaces

Certifique-se de incluir os namespaces necessários para acessar a funcionalidade Aspose.PSD. Adicione as seguintes linhas no início do seu projeto .NET:

```csharp
using Aspose.PSD.ImageOptions;
```

## Etapa 1: carregar a imagem

```csharp
string sourceFile = dataDir + @"sample.psd";

// Carregar uma imagem existente em uma instância da classe RasterImage
using (Image image = Image.Load(sourceFile))
{
```

## Etapa 2: girar a imagem

```csharp
    // Gire a imagem 270 graus no sentido horário
    image.RotateFlip(RotateFlipType.Rotate270FlipNone);
```

## Etapa 3: salve a imagem girada

```csharp
    // Salve a imagem girada como um arquivo JPEG
    string destName = dataDir + @"RotatingAnImage_out.jpg";
    image.Save(destName, new JpegOptions());
}
```

É isso! Com apenas algumas linhas de código, você girou uma imagem com sucesso usando Aspose.PSD para .NET.

## Conclusão

Neste tutorial, exploramos os fundamentos da rotação de imagens usando Aspose.PSD para .NET. Aspose.PSD fornece um conjunto robusto de ferramentas para manipulação de imagens, tornando-o uma biblioteca essencial para desenvolvedores .NET. Experimente diferentes rotações e explore outros recursos para aprimorar seus fluxos de trabalho de processamento de imagens.

## Perguntas frequentes

### Q1: Posso girar imagens em um ângulo personalizado usando Aspose.PSD?

 Sim, Aspose.PSD permite especificar um ângulo personalizado para rotação. Basta substituir o`RotateFlipType.Rotate270FlipNone` alinhe com o ângulo de rotação desejado.

### Q2: O Aspose.PSD é compatível com vários formatos de imagem?

 Absolutamente. Aspose.PSD oferece suporte a uma ampla variedade de formatos de imagem, incluindo PSD, JPEG, PNG e muito mais. Verifique o[documentação](https://reference.aspose.com/psd/net/) para a lista completa.

### Q3: Como posso obter uma licença temporária para Aspose.PSD?

 Visite o[página de licença temporária](https://purchase.aspose.com/temporary-license/) no site Aspose para obter uma licença temporária para fins de avaliação.

### Q4: Onde posso encontrar suporte para Aspose.PSD?

 Para qualquer dúvida ou assistência, visite o[Fórum Aspose.PSD](https://forum.aspose.com/c/psd/34) e se conectar com a comunidade.

### Q5: Posso comprar Aspose.PSD para uso comercial?

 Certamente. Explorar o[página de compra](https://purchase.aspose.com/buy) para adquirir uma licença adaptada às suas necessidades.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
