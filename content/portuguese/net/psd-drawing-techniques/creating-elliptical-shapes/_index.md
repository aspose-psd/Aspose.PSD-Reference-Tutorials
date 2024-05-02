---
title: Criando formas elípticas com Aspose.PSD para .NET
linktitle: Criando formas elípticas com Aspose.PSD para .NET
second_title: API Aspose.PSD .NET
description: Aprenda como desenhar formas elípticas em .NET usando Aspose.PSD. Guia passo a passo com exemplos de código. Crie gráficos impressionantes sem esforço.
type: docs
weight: 13
url: /pt/net/psd-drawing-techniques/creating-elliptical-shapes/
---
## Introdução

Bem-vindo ao nosso guia completo sobre como criar formas elípticas usando Aspose.PSD para .NET. Aspose.PSD é uma biblioteca .NET poderosa que permite aos desenvolvedores manipular e converter arquivos do Photoshop sem a necessidade do Adobe Photoshop. Neste tutorial, orientaremos você no processo de desenho de formas elípticas usando a biblioteca.

## Pré-requisitos

Antes de mergulharmos no tutorial, certifique-se de ter os seguintes pré-requisitos em vigor:

- Biblioteca Aspose.PSD para .NET: certifique-se de ter a biblioteca Aspose.PSD instalada em seu projeto .NET. Você pode baixá-lo no[Documentação Aspose.PSD para .NET](https://reference.aspose.com/psd/net/).

- Ambiente .NET: Este tutorial pressupõe que você tenha conhecimento prático do .NET framework.

## Importar namespaces

Para começar, importe os namespaces necessários para o seu projeto. Isso garante que você tenha acesso às classes e aos métodos necessários para desenhar formas elípticas. Aqui está um exemplo:

```csharp
using Aspose.PSD.Brushes;
using Aspose.PSD.FileFormats.Psd;
using Aspose.PSD.ImageOptions;
```

Agora, vamos dividir o processo de criação de formas elípticas em várias etapas:

## Etapa 1: configurar o diretório de documentos

```csharp
// O caminho para o diretório de documentos.
string dataDir = "Your Document Directory";
```

## Etapa 2: crie uma instância de BmpOptions

```csharp
// Crie uma instância de BmpOptions e defina suas diversas propriedades
string outpath = dataDir + "Ellipse.bmp";
BmpOptions saveOptions = new BmpOptions();
saveOptions.BitsPerPixel = 32;
```

## Etapa 3: crie uma instância de imagem

```csharp
// Crie uma instância de imagem
using (Image image = new PsdImage(100, 100))
{
    // Crie e inicialize uma instância da classe Graphics e da superfície Clear Graphics
    Graphics graphic = new Graphics(image);
    graphic.Clear(Color.Yellow);
```

## Etapa 4: desenhe uma forma de elipse pontilhada

```csharp
    // Desenhe uma forma de elipse pontilhada especificando o objeto Pen com a cor vermelha e um retângulo ao redor
    graphic.DrawEllipse(new Pen(Color.Red), new Rectangle(30, 10, 40, 80));
```

## Etapa 5: desenhe uma forma de elipse contínua

```csharp
    //Desenhe uma forma de elipse contínua especificando o objeto Caneta com um pincel sólido de cor azul e um retângulo circundante
    graphic.DrawEllipse(new Pen(new SolidBrush(Color.Blue)), new Rectangle(10, 30, 80, 40));

    // Exporte a imagem para o formato de arquivo bmp.
    image.Save(outpath, saveOptions);
}
```

## Conclusão

Parabéns! Você criou formas elípticas com sucesso usando Aspose.PSD para .NET. Este tutorial abordou as etapas essenciais, desde a configuração do ambiente até o desenho de formas elipses contínuas e pontilhadas.

## Perguntas frequentes

### Q1: Onde posso encontrar a documentação do Aspose.PSD para .NET?

 A1: A documentação está disponível[aqui](https://reference.aspose.com/psd/net/).

### Q2: Como faço o download do Aspose.PSD para .NET?

 A2: Você pode baixá-lo na página de lançamento[aqui](https://releases.aspose.com/psd/net/).

### Q3: Existe um teste gratuito disponível?

 A3: Sim, você pode acessar a avaliação gratuita[aqui](https://releases.aspose.com/).

### Q4: Como posso obter suporte para Aspose.PSD para .NET?

 A4: Visite o fórum de suporte[aqui](https://forum.aspose.com/c/psd/34).

### P5: Preciso de uma licença temporária para testes?

 A5: Sim, você pode obter uma licença temporária[aqui](https://purchase.aspose.com/temporary-license/).