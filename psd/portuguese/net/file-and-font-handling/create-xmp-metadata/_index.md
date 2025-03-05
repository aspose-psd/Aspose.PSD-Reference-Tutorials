---
title: Criando metadados XMP em Aspose.PSD para .NET
linktitle: Criando Metadados XMP
second_title: API Aspose.PSD .NET
description: Explore a criação de metadados XMP em Aspose.PSD para .NET. Melhore a organização da imagem com manipulação perfeita.
type: docs
weight: 10
url: /pt/net/file-and-font-handling/create-xmp-metadata/
---
## Introdução

No mundo dinâmico do desenvolvimento .NET, a manipulação de imagens com precisão é um aspecto crucial de muitos aplicativos. Este tutorial explora a criação de metadados XMP em Aspose.PSD for .NET, uma biblioteca poderosa que simplifica tarefas de processamento de imagens. XMP (Extensible Metadata Platform) permite incorporar metadados em arquivos de imagem, facilitando a organização eficiente e a recuperação de informações associadas às imagens.

## Pré-requisitos

Antes de mergulhar no tutorial, certifique-se de ter os seguintes pré-requisitos em vigor:

-  Biblioteca Aspose.PSD para .NET: Baixe e instale a biblioteca do[Documentação Aspose.PSD](https://reference.aspose.com/psd/net/).

- Ambiente de desenvolvimento: configure um ambiente de desenvolvimento .NET com o Visual Studio ou seu IDE preferido.

- Conhecimento básico do .NET: familiarize-se com os conceitos básicos do .NET, pois este tutorial pressupõe uma compreensão básica do desenvolvimento do .NET.

## Importar namespaces

Em seu projeto .NET, inclua os namespaces necessários para acessar a funcionalidade Aspose.PSD:

```csharp
using Aspose.PSD.FileFormats.Psd;
using Aspose.PSD.Xmp;
using Aspose.PSD.Xmp.Schemas.DublinCore;
using Aspose.PSD.Xmp.Schemas.Photoshop;
using System;
using System.IO;
```

Agora, vamos dividir o processo de criação de metadados XMP em uma série de etapas abrangentes.

## Etapa 1: especificar o tamanho e o retângulo da imagem

```csharp
// O caminho para o diretório de documentos.
string dataDir = RunExamples.GetDataDir_DrawingAndFormattingImages();

//Especifique o tamanho da imagem definindo um retângulo
Rectangle rect = new Rectangle(0, 0, 100, 200);
```

## Etapa 2: crie uma nova imagem

```csharp
// Crie a nova imagem para fins de amostra
using (var image = new PsdImage(rect.Width, rect.Height))
{
    // O código de manipulação de imagem vai aqui...
}
```

## Etapa 3: Criar cabeçalho XMP e trailer XMP

```csharp
// Crie uma instância do XMP-Header
XmpHeaderPi xmpHeader = new XmpHeaderPi(Guid.NewGuid().ToString());

// Crie uma instância de XMP-TrailerPi, classe XMPmeta para definir diferentes atributos
XmpTrailerPi xmpTrailer = new XmpTrailerPi(true);
XmpMeta xmpMeta = new XmpMeta();
```

## Etapa 4: definir atributos XMP

```csharp
// Defina atributos XMP, por exemplo:
xmpMeta.AddAttribute("Author", "Mr Smith");
xmpMeta.AddAttribute("Description", "The fake metadata value");
```

## Etapa 5: criar wrapper de pacote XMP

```csharp
// Crie uma instância do XmpPacketWrapper que contenha todos os metadados
XmpPacketWrapper xmpData = new XmpPacketWrapper(xmpHeader, xmpTrailer, xmpMeta);
```

## Etapa 6: Criar pacote Photoshop e definir atributos

```csharp
// Crie uma instância do pacote Photoshop e defina atributos do Photoshop
PhotoshopPackage photoshopPackage = new PhotoshopPackage();
photoshopPackage.SetCity("London");
photoshopPackage.SetCountry("England");
photoshopPackage.SetColorMode(ColorMode.Rgb);
photoshopPackage.SetCreatedDate(DateTime.UtcNow);
```

## Etapa 7: adicionar pacote Photoshop aos metadados XMP

```csharp
// Adicione o pacote Photoshop aos metadados XMP
xmpData.AddPackage(photoshopPackage);
```

## Etapa 8: Criar pacote DublinCore e definir atributos

```csharp
// Crie uma instância do pacote DublinCore e defina atributos dublinCore
DublinCorePackage dublinCorePackage = new DublinCorePackage();
dublinCorePackage.SetAuthor("Mudassir Fayyaz");
dublinCorePackage.SetTitle("Confessions of a Man Insane Enough to Live With the Beasts");
dublinCorePackage.AddValue("dc:movie", "Barfly");
```

## Etapa 9: Adicionar pacote DublinCore aos metadados XMP

```csharp
// Adicione o pacote dublinCore aos metadados XMP
xmpData.AddPackage(dublinCorePackage);
```

## Etapa 10: atualize os metadados XMP e salve a imagem

```csharp
using (var ms = new MemoryStream())
{
    // Atualize os metadados XMP na imagem e salve a imagem no disco ou em um fluxo de memória
    image.XmpData = xmpData;
    image.Save(ms);
    image.Save(dataDir + "ee.psd");
    ms.Seek(0, System.IO.SeekOrigin.Begin);
}
```

## Etapa 11: carregar imagem e ler metadados

```csharp
// Carregue a imagem do fluxo de memória ou do disco para ler/obter os metadados
using (var img = (PsdImage)Image.Load(ms))
{
    // Obtendo os metadados XMP
    XmpPacketWrapper imgXmpData = img.XmpData;
    foreach (XmpPackage package in imgXmpData.Packages)
    {
        // Usar dados do pacote...
    }
}
```

## Conclusão

Parabéns! Você criou metadados XMP com sucesso em Aspose.PSD para .NET. Esse poderoso recurso aprimora suas capacidades de processamento de imagens, permitindo organização e recuperação eficientes de informações vitais.

## Perguntas frequentes

### Q1: O Aspose.PSD for .NET é compatível com todos os formatos de imagem?

A1: Aspose.PSD concentra-se principalmente no formato de arquivo PSD (Adobe Photoshop), mas oferece suporte a vários outros formatos.

### Q2: Posso manipular metadados XMP existentes usando Aspose.PSD para .NET?

A2: Sim, Aspose.PSD permite ler e modificar metadados XMP existentes.

### Q3: Há alguma limitação no tamanho da imagem ao usar Aspose.PSD para .NET?

R3: Aspose.PSD pode lidar com imagens de tamanhos variados, mas imagens extremamente grandes podem exigir considerações adicionais.

### Q4: Com que frequência o Aspose.PSD para .NET é atualizado?

A4: As atualizações são lançadas regularmente para garantir a compatibilidade com as versões mais recentes do .NET Framework e os padrões do setor.

### Q5: Existe um fórum da comunidade para suporte do Aspose.PSD?

 R: Sim, você pode encontrar suporte e discussões no[Fórum Aspose.PSD](https://forum.aspose.com/c/psd/34).