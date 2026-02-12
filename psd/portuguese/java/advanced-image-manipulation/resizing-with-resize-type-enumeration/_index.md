---
date: 2026-02-12
description: Aprenda como redimensionar imagens em Java usando Aspose.PSD para Java.
  Guia passo a passo com a enumeração Resize Type, além de dicas sobre como converter
  PSD para JPEG.
linktitle: Resizing with Resize Type Enumeration
second_title: Aspose.PSD Java API
title: Redimensionar Imagem Java - Usando a Enumeração de Tipo de Redimensionamento
  no Aspose.PSD para Java
url: /pt/java/advanced-image-manipulation/resizing-with-resize-type-enumeration/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Redimensionar Imagem Java: Usando a Enumeração Resize Type no Aspose.PSD para Java

## Introdução

Redimensionar imagens é uma necessidade comum em aplicações Java, e as operações **resize image java** se tornam fáceis com Aspose.PSD. Neste tutorial você aprenderá como **resize image java** usando a poderosa Enumeração Resize Type, e também verá como **convert psd to jpeg** após o redimensionamento. Seja você desenvolvendo uma ferramenta desktop ou um serviço server‑side, estas etapas ajudarão a lidar com as dimensões da imagem de forma confiável e alcançar um redimensionamento de alta qualidade.

## Respostas Rápidas
- **Qual biblioteca lida com resize image java?** Aspose.PSD for Java.  
- **Qual tipo de redimensionamento oferece a melhor qualidade?** `ResizeType.LanczosResample`.  
- **Posso converter PSD para JPEG após o redimensionamento?** Sim – basta salvar com `JpegOptions`.  
- **Preciso de licença para produção?** Uma licença válida do Aspose.PSD é necessária para uso em produção.  
- **Esta abordagem é adequada para grandes lotes?** Absolutamente; a API está otimizada para desempenho.

## O que é Resize Image Java?

O termo “resize image java” refere‑se a alterar programaticamente as dimensões em pixels de uma imagem usando código Java. Aspose.PSD fornece uma API concisa que abstrai a manipulação de pixels de baixo nível, permitindo que você se concentre na lógica de negócios em vez dos detalhes de processamento de imagem.

## Por que usar a Enumeração Resize Type?

A Enumeração Resize Type oferece controle granular sobre o algoritmo de reamostragem, permitindo equilibrar velocidade e qualidade. Para a maioria das aplicações, `LanczosResample` oferece um ótimo compromisso, entregando resultados nítidos sem um grande custo de desempenho. Escolher o tipo de redimensionamento correto é fundamental para obter um redimensionamento de imagem de alta qualidade.

## Pré‑requisitos

Antes de iniciar este tutorial, certifique‑se de que você possui os seguintes pré‑requisitos:

1. **Ambiente de Desenvolvimento Java** – um JDK 8+ instalado e configurado.  
2. **Biblioteca Aspose.PSD** – faça download e instale a biblioteca Aspose.PSD a partir do [website](https://releases.aspose.com/psd/java/).  
3. **Arquivo PSD de Exemplo** – tenha um arquivo PSD de exemplo pronto para experimentação. Você pode usar o arquivo [sample.psd](Your Document Directory/sample.psd) para este tutorial.

## Importar Pacotes

Para começar, importe os pacotes necessários ao seu projeto Java:

```java
import com.aspose.psd.Image;
import com.aspose.psd.ResizeType;

import com.aspose.psd.imageoptions.JpegOptions;
```

## Etapa 1: Carregar a Imagem

Comece carregando uma imagem existente em uma instância da classe `RasterImage`. Use o trecho de código a seguir:

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

// Load an existing image into an instance of RasterImage class
Image image = Image.load(sourceFile);
```

## Etapa 2: Redimensionar a Imagem

Agora, redimensione a imagem carregada usando a Enumeração Resize Type. Neste exemplo, usamos o método Lanczos Resample, que é ideal quando você **how to resize image** com alta qualidade:

```java
image.resize(300, 300, ResizeType.LanczosResample);
```

## Etapa 3: Salvar a Imagem Redimensionada

Após o redimensionamento, salve a imagem com as dimensões especificadas e o tipo de redimensionamento escolhido. Aqui, também demonstramos **convert psd to jpeg** salvando o resultado como um arquivo JPEG:

```java
String destName = dataDir + "ResizingwithResizeTypeEnumeration_out.jpg";
image.save(destName, new JpegOptions());
```

Você acabou de executar um fluxo completo de **resize image java** que produz um redimensionamento de imagem de alta qualidade e uma saída JPEG pronta para uso.

## Problemas Comuns e Soluções

- **A imagem fica borrada após o redimensionamento** – Experimente um `ResizeType` diferente, como `Bicubic` ou `NearestNeighbour`, para ver qual produz o melhor resultado visual para sua imagem específica.  
- **OutOfMemoryError em arquivos PSD grandes** – Processar a imagem em blocos menores ou aumentar o tamanho do heap da JVM (flag `-Xmx`).  

## Perguntas Frequentes

### Q1: É o Aspose.PSD para Java adequado tanto para projetos pequenos quanto para projetos de grande escala?

A1: Absolutamente! Aspose.PSD para Java foi projetado para atender projetos de todos os tamanhos, oferecendo escalabilidade e eficiência.

### Q2: Posso usar um tipo de redimensionamento diferente de Lanczos Resample?

A2: Sim, Aspose.PSD para Java oferece vários tipos de redimensionamento, como Nearest Neighbour, Bicubic e outros. Explore a documentação para obter uma lista completa.

### Q3: Onde posso encontrar suporte adicional para Aspose.PSD para Java?

A3: Para quaisquer dúvidas ou assistência, visite o [forum Aspose.PSD](https://forum.aspose.com/c/psd/34).

### Q4: Existe uma versão de avaliação gratuita disponível para Aspose.PSD para Java?

A4: Sim, você pode acessar uma versão de avaliação gratuita [aqui](https://releases.aspose.com/).

### Q5: Como posso obter uma licença temporária para Aspose.PSD para Java?

A5: Para obter uma licença temporária, visite [este link](https://purchase.aspose.com/temporary-license/).

## Perguntas Frequentes

**P: Como converto programaticamente um arquivo PSD para JPEG sem redimensionar?**  
R: Load the PSD with `Image.load`, then call `image.save("output.jpg", new JpegOptions());`.

**P: É possível manter o DPI original ao redimensionar?**  
R: Yes, you can set the `Resolution` property on the `Image` object before saving.

**P: Posso encadear múltiplas operações de redimensionamento?**  
R: While you can call `resize` multiple times, it’s more efficient to calculate the final dimensions and resize once.

## FAQ Adicional

**P: A Enumeração Resize Type afeta a velocidade de processamento?**  
R: Yes, simpler algorithms like `NearestNeighbour` are faster but may produce lower quality results, whereas `LanczosResample` offers higher quality at a modest performance cost.

**P: Posso redimensionar imagens em um ambiente multi‑thread?**  
R: The Aspose.PSD API is thread‑safe for read‑only operations. For concurrent resizing, create separate `Image` instances per thread.

**P: Como lidar com imagens com canais alfa durante o redimensionamento?**  
R: The library preserves alpha transparency by default. If you need to flatten the image, set the background color before saving.

---

**Last Updated:** 2026-02-12  
**Tested With:** Aspose.PSD for Java 24.12  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}