---
title: Cortando imagens por turnos em Aspose.PSD para .NET
linktitle: Cortar imagens por turnos
second_title: API Aspose.PSD .NET
description: Aprenda a cortar imagens sem esforço usando Aspose.PSD para .NET. Siga nosso guia passo a passo para ajustes precisos de imagem.
type: docs
weight: 12
url: /pt/net/image-manipulation/crop-image-shifts/
---
## Introdução

No domínio do desenvolvimento .NET, Aspose.PSD se destaca como um poderoso kit de ferramentas para tarefas de processamento de imagens. Uma de suas características notáveis é a capacidade de cortar imagens com precisão, graças à funcionalidade ‘Cortar por turnos’. Neste guia passo a passo, orientaremos você no processo de corte de imagens perfeitamente usando Aspose.PSD para .NET.

## Pré-requisitos

Antes de se aprofundar no tutorial, certifique-se de ter os seguintes pré-requisitos em vigor:

-  Biblioteca Aspose.PSD para .NET: Certifique-se de ter a biblioteca instalada. Caso contrário, você pode baixá-lo no[página de lançamento](https://releases.aspose.com/psd/net/).

- Ambiente .NET: certifique-se de ter um ambiente de desenvolvimento .NET configurado em sua máquina.

- Imagem de amostra: prepare uma imagem de amostra no formato PSD com a qual você gostaria de trabalhar.

## Importar namespaces

Comece importando os namespaces necessários para o seu projeto .NET. Esses namespaces fornecem acesso às classes e métodos Aspose.PSD necessários para o corte de imagens.

```csharp
using Aspose.PSD.ImageOptions;
```

## Etapa 1: Defina seu diretório de documentos

Defina o caminho para o diretório do documento onde os arquivos de origem e destino estarão localizados.

```csharp
string dataDir = "Your Document Directory";
```

## Etapa 2: carregar a imagem de origem

Carregue a imagem PSD que deseja cortar. Certifique-se de substituir “sample.psd” pelo nome do seu arquivo de origem.

```csharp
string sourceFile = dataDir + @"sample.psd";
string destName = dataDir + @"CroppingByShifts_out.jpg";
```

## Etapa 3: armazenar dados de imagem em cache para melhor desempenho

Antes de cortar, é aconselhável armazenar em cache os dados da imagem para melhorar o desempenho.

```csharp
using (RasterImage rasterImage = (RasterImage)Image.Load(sourceFile))
{
    if (!rasterImage.IsCached)
    {
        rasterImage.CacheData();
    }
```

## Etapa 4: definir valores de deslocamento para corte

Especifique os valores de deslocamento para os lados esquerdo, direito, superior e inferior da imagem. Ajuste esses valores com base nas suas necessidades de cultivo.

```csharp
int leftShift = 10;
int rightShift = 10;
int topShift = 10;
int bottomShift = 10;
```

## Etapa 5: aplicar corte e salvar resultados

 Utilize o`Crop` método para aplicar as mudanças especificadas e salvar a imagem cortada no arquivo de destino.

```csharp
rasterImage.Crop(leftShift, rightShift, topShift, bottomShift);
rasterImage.Save(destName, new JpegOptions());
}
```

## Conclusão

Parabéns! Você aprendeu com sucesso como cortar imagens por turnos usando Aspose.PSD para .NET. Essa poderosa funcionalidade fornece a precisão e o controle necessários para diversas tarefas de processamento de imagens.

## Perguntas frequentes

### Q1: Posso cortar imagens de diferentes formatos, não apenas PSD?

A1: Sim, Aspose.PSD suporta vários formatos de imagem, permitindo cortar imagens em formatos como JPEG, PNG e muito mais.

### Q2: Existe uma versão de teste disponível antes de comprar o Aspose.PSD para .NET?

 A2: Certamente! Você pode explorar o kit de ferramentas com uma avaliação gratuita disponível[aqui](https://releases.aspose.com/).

### Q3: Como obtenho uma licença temporária do Aspose.PSD para .NET?

 A3: Você pode adquirir uma licença temporária para fins de teste.[aqui](https://purchase.aspose.com/temporary-license/).

### P4: Onde posso encontrar suporte e discussões adicionais relacionadas ao Aspose.PSD?

 A4: Visite o[Fórum Aspose.PSD](https://forum.aspose.com/c/psd/34) para suporte e discussões envolventes.

### Q5: Posso comprar Aspose.PSD para .NET diretamente do site?

 R5: Sim, você pode comprar a biblioteca com segurança no site[página de compra](https://purchase.aspose.com/buy).
