---
title: Redimensionando imagens proporcionalmente em Aspose.PSD para .NET
linktitle: Redimensionando Imagens Proporcionalmente
second_title: API Aspose.PSD .NET
description: Explore o redimensionamento contínuo de imagens com Aspose.PSD para .NET. Baixe a biblioteca, siga nosso tutorial e aprimore suas capacidades de processamento de imagens.
type: docs
weight: 14
url: /pt/net/image-manipulation/resize-images-proportionally/
---
No domínio da manipulação de imagens, Aspose.PSD for .NET se destaca como um kit de ferramentas poderoso, fornecendo aos desenvolvedores a capacidade de redimensionar imagens proporcionalmente com facilidade. Neste guia passo a passo, orientaremos você no processo de redimensionamento de imagens usando Aspose.PSD para .NET, garantindo que suas imagens mantenham suas proporções perfeitamente.

## Introdução

Redimensionar imagens proporcionalmente é uma tarefa comum em muitos aplicativos, e o Aspose.PSD para .NET simplifica esse processo para os desenvolvedores. Esteja você trabalhando em um aplicativo da web, software de desktop ou aplicativo móvel, entender como redimensionar imagens preservando sua proporção é crucial para manter o apelo visual e a consistência.

## Pré-requisitos

Antes de mergulhar na mágica do redimensionamento com Aspose.PSD para .NET, certifique-se de ter os seguintes pré-requisitos em vigor:

1.  Biblioteca Aspose.PSD for .NET: Certifique-se de ter a biblioteca Aspose.PSD for .NET instalada. Você pode baixá-lo no[Aspose.PSD para versões .NET](https://releases.aspose.com/psd/net/) página.

2. Diretório de documentos: crie um diretório para armazenar seus documentos e substitua "Seu diretório de documentos" no código fornecido pelo caminho real para esse diretório.

Agora que você configurou os pré-requisitos, vamos passar ao guia passo a passo.

## Importar namespaces

```csharp
using Aspose.PSD.ImageOptions;
```

Importe os namespaces necessários para acessar as classes e métodos necessários.

## Etapa 1: carregar a imagem

```csharp
// O caminho para o diretório de documentos.
string dataDir = "Your Document Directory";

string sourceFile = dataDir + @"sample.psd";

// Carregar uma imagem existente em uma instância da classe RasterImage
using (Image image = Image.Load(sourceFile))
{
	if (!image.IsCached)
	{
		image.CacheData();
	}
	// O restante das etapas vai aqui
}
```

 Carregue a imagem de origem usando o`Image.Load` método.

## Etapa 2: especifique largura e altura

```csharp
// Especificando largura e altura
int newWidth = image.Width / 2;
image.ResizeWidthProportionally(newWidth);

int newHeight = image.Height / 2;
image.ResizeHeightProportionally(newHeight);
```

Determine a nova largura e altura da imagem redimensionada. Neste exemplo, a largura e a altura são divididas pela metade, mas você pode ajustar esses valores com base em suas necessidades.

## Etapa 3: salve a imagem redimensionada

```csharp
string destName = dataDir + @"SimpleResizeImageProportionally_out.png";

image.Save(destName, new PngOptions());
```

 Salve a imagem redimensionada usando o`Save` método com opções especificadas. Neste caso, estamos salvando-o como um arquivo PNG.

## Conclusão

Redimensionar imagens proporcionalmente no Aspose.PSD for .NET é um processo simples que agrega valor ao seu fluxo de trabalho de processamento de imagens. Este guia equipou você com o conhecimento para integrar perfeitamente essa funcionalidade em seus aplicativos.

## Perguntas frequentes

### Q1: Posso redimensionar imagens para dimensões específicas?

A1: Sim, você pode personalizar a nova largura e altura de acordo com suas necessidades no código.

### Q2: O Aspose.PSD para .NET é adequado para redimensionamento de imagens em lote?

A2: Com certeza! Você pode incorporar essas etapas em um loop para processar várias imagens em lote.

### Q3: Existem outros recursos de manipulação de imagens no Aspose.PSD para .NET?

A3: Sim, Aspose.PSD for .NET oferece uma ampla gama de recursos, incluindo cortar, girar e aplicar filtros a imagens.

### Q4: Existe uma avaliação gratuita disponível para Aspose.PSD para .NET?

 A4: Sim, você pode explorar os recursos do Aspose.PSD para .NET com uma avaliação gratuita. Visita[aqui](https://releases.aspose.com/) para começar.

### P5: Onde posso encontrar suporte para Aspose.PSD para .NET?

 A5: Visite o[Fórum Aspose.PSD para .NET](https://forum.aspose.com/c/psd/34) para apoio e discussões da comunidade.