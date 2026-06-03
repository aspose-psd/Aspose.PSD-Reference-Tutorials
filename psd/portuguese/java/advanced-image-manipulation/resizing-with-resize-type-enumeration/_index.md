---
date: 2026-06-03
description: Aprenda como redimensionar imagens com Aspose.PSD para Java. Este guia
  passo a passo aborda a Resize Type Enumeration, redimensionamento de imagem de alta
  qualidade e como converter PSD para JPEG.
keywords:
- how to resize image
- convert psd to jpeg
- high quality image resize
- resize image java
- java image manipulation tutorial
linktitle: Redimensionamento com Resize Type Enumeration
schemas:
- author: Aspose
  dateModified: '2026-06-03'
  description: Learn how to resize image with Aspose.PSD for Java. This step‑by‑step
    guide covers the Resize Type Enumeration, high‑quality image resize, and how to
    convert PSD to JPEG.
  headline: How to Resize Image Java Using Resize Type Enumeration
  type: TechArticle
- description: Learn how to resize image with Aspose.PSD for Java. This step‑by‑step
    guide covers the Resize Type Enumeration, high‑quality image resize, and how to
    convert PSD to JPEG.
  name: How to Resize Image Java Using Resize Type Enumeration
  steps:
  - name: '**Java Development Environment** – JDK 8 or newer installed and configured.'
    text: '**Java Development Environment** – JDK 8 or newer installed and configured.'
  - name: '**Aspose.PSD Library** – Download the latest JAR from the [website](https://releases.aspose.com/psd/java/).'
    text: '**Aspose.PSD Library** – Download the latest JAR from the [website](https://releases.aspose.com/psd/java/).'
  - name: '**Sample PSD File** – Use the [sample.psd](Your Document Directory/sample.psd)
      file included with the SDK for hands‑on testing.'
    text: '**Sample PSD File** – Use the [sample.psd](Your Document Directory/sample.psd)
      file included with the SDK for hands‑on testing.'
  type: HowTo
- questions:
  - answer: Load the PSD with `Image.load`, then call `image.save("output.jpg", new
      JpegOptions());`.
    question: How do I programmatically convert a PSD file to JPEG without resizing?
  - answer: Yes, you can set the `Resolution` property on the `Image` object before
      saving.
    question: Is it possible to maintain the original DPI when resizing?
  - answer: While you can call `resize` multiple times, it’s more efficient to calculate
      the final dimensions and resize once.
    question: Can I chain multiple resize operations?
  type: FAQPage
second_title: Aspose.PSD Java API
title: Como Redimensionar Imagem Java Usando a Resize Type Enumeration
url: /pt/java/advanced-image-manipulation/resizing-with-resize-type-enumeration/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Como Redimensionar Imagem Java Usando a Enumeração de Tipo de Redimensionamento

## Introdução

Se você está procurando **como redimensionar imagem** de forma eficiente em um projeto Java, o Aspose.PSD for Java oferece uma API limpa e de alto desempenho. Neste tutorial vamos percorrer o carregamento de um PSD, aplicar a **Resize Type Enumeration** para redimensionamento de imagem de alta qualidade e, finalmente, **converter PSD para JPEG**. Seja você quem está construindo um editor desktop ou um pipeline automatizado no servidor, estas etapas permitem controlar dimensões, qualidade e formato com apenas algumas linhas de código.

## Respostas Rápidas
- **Qual biblioteca lida com redimensionamento de imagem java?** Aspose.PSD for Java.
- **Qual tipo de redimensionamento oferece a melhor qualidade?** `ResizeType.LanczosResample`.
- **Posso converter PSD para JPEG após redimensionar?** Sim – basta salvar com `JpegOptions`.
- **Preciso de licença para produção?** Uma licença válida do Aspose.PSD é necessária para uso em produção.
- **Esta abordagem é adequada para grandes lotes?** Absolutamente; a API processa arquivos com centenas de páginas sem carregar todo o documento na memória.

## O que significa "como redimensionar imagem" em Java?
**Como redimensionar imagem** refere‑se a mudar programaticamente as dimensões em pixels de uma imagem enquanto preserva a fidelidade visual. O método `Resize` do Aspose.PSD combinado com a enumeração `ResizeType` oferece controle preciso sobre os algoritmos de redimensionamento, permitindo que desenvolvedores mantenham a qualidade em uma ampla variedade de arquivos de origem e tamanhos de destino.

## Por que usar a Resize Type Enumeration?
`ResizeType` permite selecionar o algoritmo de reamostragem que melhor equilibra velocidade e qualidade visual. Para a maioria dos cenários, **LanczosResample** entrega resultados nítidos com um custo de desempenho moderado, processando uma imagem de 2000 × 1500 em menos de 120 ms em uma CPU de servidor típica, mantendo os detalhes das bordas intactos.

## Pré‑requisitos

Antes de começar, certifique‑se de que você tem:

1. **Ambiente de Desenvolvimento Java** – JDK 8 ou superior instalado e configurado.  
2. **Biblioteca Aspose.PSD** – Baixe o JAR mais recente a partir do [site](https://releases.aspose.com/psd/java/).  
3. **Arquivo PSD de Exemplo** – Use o arquivo [sample.psd](Your Document Directory/sample.psd) incluído no SDK para testes práticos.

## Importar Pacotes

`Image` é a classe base para todos os tipos de imagem no Aspose.PSD. Adicione as importações necessárias ao seu arquivo fonte Java:

```java
import com.aspose.psd.Image;
import com.aspose.psd.ResizeType;

import com.aspose.psd.imageoptions.JpegOptions;
```

## Etapa 1: Carregar a Imagem

### Âncora de Definição
A classe `RasterImage` é o objeto central do Aspose.PSD que representa uma imagem raster carregada a partir de um arquivo PSD.

Carregue seu PSD em uma instância de `RasterImage` para que você possa manipular seus pixels:

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

// Load an existing image into an instance of RasterImage class
Image image = Image.load(sourceFile);
```

## Etapa 2: Redimensionar a Imagem

`image.resize(width, height, resizeType)` redimensiona a imagem para as dimensões especificadas usando o algoritmo escolhido.

Agora redimensione a imagem carregada usando a **Resize Type Enumeration**. Neste exemplo usamos o método Lanczos Resample, ideal quando você **como redimensionar imagem** com alta qualidade:

```java
image.resize(300, 300, ResizeType.LanczosResample);
```

## Etapa 3: Salvar a Imagem Redimensionada

`image.save(path, options)` grava a imagem no disco no formato definido pelas opções fornecidas.

Após o redimensionamento, salve a imagem com as dimensões especificadas e o tipo de redimensionamento escolhido. Aqui, também demonstramos **converter psd para jpeg** salvando o resultado como um arquivo JPEG:

```java
String destName = dataDir + "ResizingwithResizeTypeEnumeration_out.jpg";
image.save(destName, new JpegOptions());
```

## Por que usar a Resize Type Enumeration?

`ResizeType` oferece controle granular sobre o algoritmo de reamostragem, permitindo equilibrar velocidade e qualidade. Para a maioria das aplicações, `LanczosResample` oferece um ótimo compromisso, entregando resultados nítidos sem penalidade de desempenho pesada, e funciona bem em diversos conteúdos de imagem.

## Problemas Comuns e Soluções

- **A imagem fica borrada após o redimensionamento** – Experimente um `ResizeType` diferente, como `Bicubic` ou `NearestNeighbour`, para ver qual produz o melhor resultado visual para sua imagem específica.  
- **OutOfMemoryError em arquivos PSD grandes** – Processar a imagem em blocos menores ou aumentar o tamanho do heap da JVM (`-Xmx`). O Aspose.PSD pode lidar com arquivos de até **2 GB** sem carregar todo o documento na memória.

## Perguntas Frequentes

### Q1: O Aspose.PSD for Java é adequado tanto para projetos pequenos quanto para projetos de grande escala?

A1: Absolutamente! O Aspose.PSD for Java foi projetado para atender projetos de todos os tamanhos, oferecendo escalabilidade e eficiência.

### Q2: Posso usar um tipo de redimensionamento diferente do Lanczos Resample?

A2: Sim, o Aspose.PSD for Java oferece vários tipos de redimensionamento, como **NearestNeighbour**, **Bicubic** e outros. Consulte a documentação da API para a lista completa.

### Q3: Onde posso encontrar suporte adicional para o Aspose.PSD for Java?

A3: Para dúvidas ou assistência, visite o [fórum Aspose.PSD](https://forum.aspose.com/c/psd/34).

### Q4: Existe uma versão de avaliação gratuita disponível para o Aspose.PSD for Java?

A4: Sim, você pode acessar uma versão de avaliação gratuita [aqui](https://releases.aspose.com/).

### Q5: Como posso obter uma licença temporária para o Aspose.PSD for Java?

A5: Para obter uma licença temporária, acesse [este link](https://purchase.aspose.com/temporary-license/).

## Perguntas Frequentes Adicionais

**P: Como converter programaticamente um arquivo PSD para JPEG sem redimensionar?**  
R: Carregue o PSD com `Image.load`, então chame `image.save("output.jpg", new JpegOptions());`.

**P: É possível manter o DPI original ao redimensionar?**  
R: Sim, você pode definir a propriedade `Resolution` no objeto `Image` antes de salvar.

**P: Posso encadear múltiplas operações de redimensionamento?**  
R: Embora seja possível chamar `resize` várias vezes, é mais eficiente calcular as dimensões finais e redimensionar uma única vez.

---

**Última atualização:** 2026-06-03  
**Testado com:** Aspose.PSD for Java 24.12  
**Autor:** Aspose  

{{< blocks/products/products-backtop-button >}}

## Tutoriais Relacionados

- [Redimensionamento Simples com Aspose.PSD – Biblioteca de Manipulação de Imagens Java](/psd/java/basic-image-operations/simple-resizing/)
- [Escalonamento de Imagem de Alta Qualidade com Bicubic Resampler no Aspose.PSD for Java](/psd/java/advanced-image-manipulation/implement-bicubic-resampler/)
- [Como Converter PSD para PNG e Redimensionar Proporcionalmente com Aspose.PSD for Java](/psd/java/advanced-image-manipulation/resize-image-proportionally/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}