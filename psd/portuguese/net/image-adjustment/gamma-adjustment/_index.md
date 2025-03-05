---
title: Implementando ajuste de gama em Aspose.PSD para .NET
linktitle: Implementando ajuste gama
second_title: API Aspose.PSD .NET
description: Explore o poder do Aspose.PSD para .NET com nosso guia passo a passo sobre como implementar o ajuste gama. Ajuste o brilho e o contraste da imagem sem esforço.
type: docs
weight: 12
url: /pt/net/image-adjustment/gamma-adjustment/
---
## Introdução

Bem-vindo a este guia completo sobre como implementar o ajuste de gama no Aspose.PSD para .NET! O ajuste gama é uma técnica crucial de processamento de imagem que permite ajustar o brilho e o contraste de uma imagem. Neste tutorial, orientaremos você no processo usando a poderosa biblioteca Aspose.PSD para .NET.

## Pré-requisitos

Antes de mergulhar na implementação, certifique-se de ter os seguintes pré-requisitos em vigor:

-  Biblioteca Aspose.PSD para .NET: certifique-se de ter a biblioteca Aspose.PSD para .NET instalada. Você pode baixá-lo[aqui](https://releases.aspose.com/psd/net/).

- .NET Framework: Este tutorial pressupõe que você tenha um conhecimento básico de desenvolvimento em .NET e tenha o .NET Framework instalado.

- Ambiente de Desenvolvimento Integrado (IDE): Escolha seu IDE preferido para desenvolvimento .NET, como Visual Studio.

## Importar namespaces

Em seu projeto .NET, comece importando os namespaces necessários para trabalhar com Aspose.PSD:

```csharp
using Aspose.PSD.FileFormats.Tiff.Enums;
using Aspose.PSD.ImageOptions;
```

## Etapa 1: configure seu projeto

Crie um novo projeto .NET no IDE escolhido. Certifique-se de adicionar referências à biblioteca Aspose.PSD.

## Etapa 2: definir o diretório de documentos

```csharp
string dataDir = "Your Document Directory";
```

## Etapa 3: carregar a imagem

```csharp
string sourceFile = dataDir + @"sample.psd";
using (var image = Image.Load(sourceFile))
{
    // Etapas adicionais serão executadas dentro deste bloco using.
}
```

## Etapa 4: transmitir para RasterImage e armazenar dados em cache

```csharp
RasterImage rasterImage = (RasterImage)image;
if (!rasterImage.IsCached)
{
    rasterImage.CacheData();
}
```

## Etapa 5: ajustar gama

```csharp
rasterImage.AdjustGamma(2.2f, 2.2f, 2.2f);
```

## Etapa 6: crie TiffOptions e salve

```csharp
string destName = dataDir + @"AdjustGamma_out.tiff";
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
tiffOptions.BitsPerSample = new ushort[] { 8, 8, 8 };
tiffOptions.Photometric = TiffPhotometrics.Rgb;
rasterImage.Save(destName, tiffOptions);
```

## Conclusão

Parabéns! Você implementou com sucesso o ajuste de gama usando Aspose.PSD para .NET. Esta poderosa biblioteca fornece recursos robustos para processamento de imagens, tornando-a uma ferramenta valiosa para desenvolvedores .NET.

## Perguntas frequentes

### Q1: Onde posso encontrar a documentação do Aspose.PSD?

 A1: Você pode consultar a documentação[aqui](https://reference.aspose.com/psd/net/).

### Q2: Como faço o download do Aspose.PSD para .NET?

 A2: Você pode baixar a biblioteca[aqui](https://releases.aspose.com/psd/net/).

### Q3: Existe um teste gratuito disponível?

 A3: Sim, você pode obter uma avaliação gratuita[aqui](https://releases.aspose.com/).

### Q4: Onde posso obter suporte para Aspose.PSD?

 A4: Você pode visitar o fórum de suporte[aqui](https://forum.aspose.com/c/psd/34).

### P5: Preciso de uma licença temporária?

 A5: Se necessário, você pode obter uma licença temporária[aqui](https://purchase.aspose.com/temporary-license/).