---
title: Aplicando ajuste de equilíbrio de cores em Aspose.PSD para .NET
linktitle: Aplicando ajuste de equilíbrio de cores
second_title: API Aspose.PSD .NET
description: Aprimore as cores da imagem PSD sem esforço com o recurso de ajuste de equilíbrio de cores do Aspose.PSD para .NET. Siga nosso guia passo a passo para obter resultados impressionantes.
weight: 14
url: /pt/net/image-adjustment/color-balance-adjustment/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aplicando ajuste de equilíbrio de cores em Aspose.PSD para .NET

## Introdução

Bem-vindo a este guia completo sobre como aplicar o ajuste de equilíbrio de cores no Aspose.PSD para .NET! Aspose.PSD é uma biblioteca .NET poderosa que permite aos desenvolvedores trabalhar com arquivos PSD de forma eficiente. Neste tutorial, vamos nos concentrar no recurso Ajuste de equilíbrio de cores, que permite aprimorar o equilíbrio de cores de suas imagens PSD com facilidade.

## Pré-requisitos

Antes de mergulharmos no tutorial, certifique-se de ter os seguintes pré-requisitos em vigor:

-  Biblioteca Aspose.PSD para .NET: Baixe e instale a biblioteca do[Site Aspose.PSD](https://releases.aspose.com/psd/net/).
- Ambiente de desenvolvimento: certifique-se de ter um ambiente de desenvolvimento .NET funcional configurado em sua máquina.
- Arquivo PSD: Tenha um arquivo PSD pronto ao qual deseja aplicar o ajuste de equilíbrio de cores.

## Importar namespaces

Em seu projeto .NET, inclua os namespaces necessários para usar os recursos do Aspose.PSD. Adicione as seguintes linhas ao seu código:

```csharp
using Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers;
```

Agora, vamos dividir o processo de ajuste do equilíbrio de cores em várias etapas:

## Passo 1: Carregue o arquivo PSD

```csharp
string dataDir = "Your Document Directory";
var filePath = dataDir + "ColorBalance.psd";
var outputPath = dataDir + "ColorBalance_out.psd";

using (var im = (FileFormats.Psd.PsdImage)Image.Load(filePath))
{
    // O código para o ajuste do equilíbrio de cores será adicionado nas etapas a seguir.
}
```

## Etapa 2: acessar e ajustar o equilíbrio de cores

```csharp
foreach (var layer in im.Layers)
{
    var cbLayer = layer as ColorBalanceAdjustmentLayer;
    if (cbLayer != null)
    {
        cbLayer.ShadowsCyanRedBalance = 30;
        cbLayer.ShadowsMagentaGreenBalance = -15;
        cbLayer.ShadowsYellowBlueBalance = 40;
        cbLayer.MidtonesCyanRedBalance = -90;
        cbLayer.MidtonesMagentaGreenBalance = -25;
        cbLayer.MidtonesYellowBlueBalance = 20;
        cbLayer.HighlightsCyanRedBalance = -30;
        cbLayer.HighlightsMagentaGreenBalance = 67;
        cbLayer.HighlightsYellowBlueBalance = -95;
        cbLayer.PreserveLuminosity = true;
    }
}
```

## Etapa 3: salve a imagem ajustada

```csharp
im.Save(outputPath);
```

Agora, você aplicou com sucesso o ajuste de equilíbrio de cores ao seu arquivo PSD usando Aspose.PSD para .NET!

## Conclusão

Parabéns! Você aprendeu como aprimorar o equilíbrio de cores de suas imagens PSD com Aspose.PSD for .NET. Experimente diferentes valores de equilíbrio para obter os efeitos visuais desejados.

## Perguntas frequentes

### Q1: Posso aplicar o ajuste de equilíbrio de cores a várias camadas?

A1: Sim, você pode percorrer todas as camadas do seu arquivo PSD e ajustar o equilíbrio de cores conforme necessário.

### Q2: O Aspose.PSD for .NET é adequado para processamento em lote de arquivos PSD?

A2: Com certeza! Aspose.PSD fornece recursos eficientes de processamento em lote para arquivos PSD.

### Q3: Como posso obter uma licença temporária do Aspose.PSD para .NET?

 A3: Visita[Licença temporária Aspose.PSD](https://purchase.aspose.com/temporary-license/) para uma licença temporária.

### P4: Onde posso encontrar mais exemplos e documentação?

 A4: Explore o[Documentação Aspose.PSD](https://reference.aspose.com/psd/net/) para exemplos detalhados e guias.

### Q5: Quais opções de suporte estão disponíveis para Aspose.PSD para .NET?

 A5: Visite o[Fórum Aspose.PSD](https://forum.aspose.com/c/psd/34) para apoio e discussões da comunidade.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
