---
title: Adicionando efeitos de traço a camadas em Aspose.PSD para .NET
linktitle: Adicionando efeitos de traçado a camadas
second_title: API Aspose.PSD .NET
description: Aprimore a estética da imagem com Aspose.PSD para .NET. Aprenda a adicionar efeitos de traçado passo a passo. Baixe, compre ou experimente a avaliação gratuita agora.
type: docs
weight: 10
url: /pt/net/layer-effects/adding-stroke-effects/
---
## Introdução

Bem-vindo a este tutorial passo a passo sobre como adicionar efeitos de traçado a camadas no Aspose.PSD para .NET. Melhorar o apelo visual de suas imagens é muito fácil com o efeito de traço, e o Aspose.PSD o torna perfeito para desenvolvedores .NET. Neste guia, orientaremos você no processo, fornecendo etapas e exemplos claros para ajudá-lo a dominar esse recurso poderoso.

## Pré-requisitos

Antes de mergulharmos no tutorial, certifique-se de ter os seguintes pré-requisitos em vigor:

- Aspose.PSD para .NET: Baixe e instale a biblioteca Aspose.PSD do[local na rede Internet](https://releases.aspose.com/psd/net/).

- Diretório de documentos: prepare um diretório contendo o documento PSD ao qual deseja aplicar efeitos de traçado.

- Diretório de saída: Tenha um diretório separado para armazenar as imagens de saída com efeitos de traçado.

- Visual Studio: certifique-se de ter o Visual Studio ou qualquer outro ambiente de desenvolvimento .NET preferencial configurado.

## Importar namespaces

Em seu projeto .NET, inclua os namespaces necessários para aproveitar a funcionalidade Aspose.PSD:

```csharp
using System;
using System.IO;
using Aspose.PSD.FileFormats.Psd;
using Aspose.PSD.FileFormats.Psd.Layers.FillSettings;
using Aspose.PSD.FileFormats.Psd.Layers.LayerEffects;
using Aspose.PSD.ImageLoadOptions;
using Aspose.PSD.ImageOptions;
```

## Passo 1: Carregue o Documento PSD

```csharp
string srcFile = Path.Combine(SourceDir, "AddStrokeEffect.psd");
string outputFilePng = Path.Combine(OutputDir, "AddStrokeEffect.png");

using (var psdImage = (PsdImage)Image.Load(srcFile, new PsdLoadOptions() { LoadEffectsResource = true }))
{
    // Seu código para carregar o documento PSD vai aqui
}
```

## Etapa 2: adicionar efeito de traço colorido

```csharp
// Adiciona preenchimento de cor, na posição interna
strokeEffect = psdImage.Layers[1].BlendingOptions.AddStroke(FillType.Color);
strokeEffect.Size = 7;
strokeEffect.Position = StrokePosition.Inside;
colorFillSettings = strokeEffect.FillSettings as IColorFillSettings;
colorFillSettings.Color = Color.Green;
```

## Etapa 3: posição externa

```csharp
// Adiciona preenchimento de cor, na posição externa
strokeEffect = psdImage.Layers[2].BlendingOptions.AddStroke(FillType.Color);
strokeEffect.Size = 7;
strokeEffect.Position = StrokePosition.Outside;
colorFillSettings = strokeEffect.FillSettings as IColorFillSettings;
colorFillSettings.Color = Color.Green;
```

## Etapa 4: posição central

```csharp
// Adiciona preenchimento de cor, na posição central
strokeEffect = psdImage.Layers[3].BlendingOptions.AddStroke(FillType.Color);
strokeEffect.Size = 7;
strokeEffect.Position = StrokePosition.Center;
colorFillSettings = strokeEffect.FillSettings as IColorFillSettings;
colorFillSettings.Color = Color.Green;
```

Repita etapas semelhantes para preenchimentos de gradiente e padrão, ajustando as configurações de acordo.

## Conclusão

Parabéns! Você aprendeu com sucesso como adicionar efeitos de traçado a camadas usando Aspose.PSD para .NET. Experimente diferentes configurações para obter o impacto visual desejado em suas imagens.

## Perguntas frequentes

### P1: Posso aplicar efeitos de traçado apenas a camadas específicas?

A1: Sim, você pode direcionar camadas específicas ajustando o índice da camada no código.

### Q2: O Aspose.PSD é compatível com o framework .NET mais recente?

A2: Com certeza! Aspose.PSD foi projetado para integração perfeita com os frameworks .NET mais recentes.

### Q3: Como posso personalizar a cor do traço?

 A3: Basta modificar o`Color` propriedade no código para obter a cor de traço desejada.

### Q4: O Aspose.PSD oferece suporte ao processamento em lote para vários arquivos PSD?

A4: Sim, você pode percorrer vários arquivos PSD e aplicar o efeito de traço usando uma abordagem semelhante.

### Q5: Posso usar a versão de teste antes de comprar o Aspose.PSD?

 A5: Certamente! Pegue o[teste grátis](https://releases.aspose.com/) para explorar os recursos do Aspose.PSD antes de fazer uma compra.