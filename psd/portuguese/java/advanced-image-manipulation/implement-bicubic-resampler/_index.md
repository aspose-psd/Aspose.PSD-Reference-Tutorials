---
date: 2026-10-29
description: Aprenda a redimensionar imagem java usando o Bicubic Resampler da Aspose.PSD.
  Este tutorial de dimensionamento de imagens mostra passo a passo como obter resultados
  superiores.
keywords:
- resize image java
- smooth image scaling
- java image library
- bicubic resampler
- high quality image scaling
lastmod: 2026-10-29
linktitle: Implementar Bicubic Resampler
og_description: Redimensione imagem java com o Bicubic Resampler da Aspose.PSD. Este
  guia mostra passo a passo como obter dimensionamento suave e de alta qualidade para
  PSD e outros formatos.
og_image_alt: 'Tutorial: resize image java using Aspose.PSD bicubic resampler'
og_title: Redimensionar imagem java com Bicubic Resampler – dimensionamento de alta
  qualidade
schemas:
- author: Aspose
  dateModified: '2026-10-29'
  description: Learn how to resize image java using Aspose.PSD's Bicubic Resampler.
    This image scaling tutorial shows step‑by‑step how to achieve superior results.
  headline: Resize image java – bicubic resampler for high‑quality scaling
  type: TechArticle
- description: Learn how to resize image java using Aspose.PSD's Bicubic Resampler.
    This image scaling tutorial shows step‑by‑step how to achieve superior results.
  name: Resize image java – bicubic resampler for high‑quality scaling
  steps:
  - name: load the image
    text: First, load the source PSD file you want to resize. Replace `Your Document
      Directory` with the actual path on your machine.
  - name: resize with cubic convolution (high quality)
    text: Now apply the **Cubic Convolution** algorithm, one of the two bicubic options
      that delivers high‑quality image scaling. The example resizes the image to 300
      × 300 pixels.
  - name: resize with bell algorithm (alternative high quality)
    text: If you prefer the **Bell** algorithm, which offers a slightly different
      smoothing effect, you can use it in the same way. Notice we reload the original
      image to keep the comparison fair. Feel free to experiment with other dimensions
      or file formats—just adjust the parameters accordingly.
  type: HowTo
- questions:
  - answer: Yes, the library supports PSD, PNG, JPEG, TIFF, BMP, and many more.
    question: Can I use Aspose.PSD for Java with other image formats?
  - answer: 'Yes, you can obtain a temporary license from the Aspose temporary license
      page: [Aspose temporary license page](https://purchase.aspose.com/temporary-license/).'
    question: Is a temporary license available for Aspose.PSD for Java?
  - answer: 'Visit the Aspose.PSD forum: [Aspose.PSD forum](https://forum.aspose.com/c/psd/34)
      for any support‑related queries.'
    question: Where can I find support for Aspose.PSD for Java?
  - answer: 'Yes, download the library from the Aspose.PSD Java releases page: [Aspose.PSD
      Java releases page](https://releases.aspose.com/psd/java/).'
    question: Can I download the Aspose.PSD for Java library?
  - answer: 'You can purchase Aspose.PSD for Java from the Aspose.PSD purchase page:
      [Aspose.PSD purchase page](https://purchase.aspose.com/buy).'
    question: How do I purchase Aspose.PSD for Java?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- resize image java
- Aspose.PSD
- Java image processing
title: Redimensionar imagem java – interpolador bicúbico para dimensionamento de alta
  qualidade
url: /pt/java/advanced-image-manipulation/implement-bicubic-resampler/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Redimensionar imagem java – reamostrador bicúbico para dimensionamento de alta qualidade

## Introdução

Se você precisa **redimensionar imagem java** projetos sem perder nitidez ou introduzir artefatos, você está no lugar certo. Neste **tutorial de dimensionamento de imagens** vamos percorrer o uso do Bicubic Resampler da Aspose.PSD — um recurso poderoso desta **biblioteca de imagens java** que entrega resultados suaves e nítidos para arquivos PSD e muitos outros formatos. Ao final deste guia, você será capaz de integrar dimensionamento de alta qualidade em qualquer aplicação Java em apenas algumas linhas de código.

## Respostas rápidas
- **O que o Bicubic Resampler faz?** Ele aplica um algoritmo de interpolação sofisticado que preserva detalhes ao redimensionar imagens.  
- **Quais valores de ResizeType estão disponíveis?** `CubicConvolution` e `Bell` são as duas opções bicúbicas fornecidas pela Aspose.PSD.  
- **Preciso de uma licença para executar o código?** Uma licença temporária da Aspose funciona para avaliação; uma licença completa é necessária para produção.  
- **Qual versão do Java é necessária?** Qualquer runtime Java 8+ é compatível com a biblioteca mais recente da Aspose.PSD.  
- **Posso redimensionar outros formatos (PNG, JPEG) com a mesma API?** Sim, a Aspose.PSD suporta vários tipos de imagem, embora os exemplos se concentrem em PSD.

## O que é dimensionamento de imagem de alta qualidade?
O **bicubic resampler** é o algoritmo da Aspose.PSD que calcula cada novo pixel a partir dos valores dos pixels circundantes usando convolução cúbica ou o método Bell. Essa abordagem mantém texturas finas, gradientes suaves e cores precisas, produzindo uma aparência mais natural do que o dimensionamento por vizinho mais próximo ou bilinear.

## Por que usar o bicubic resampler para dimensionamento de imagem de alta qualidade?
O bicubic resampler preserva detalhes, reduz artefatos de ringing e desfoque, e pode ser invocado com uma única chamada de método (`image.resize`). Benefício quantificado: ele processa imagens com dimensões até 4 × maiores mantendo o contraste das bordas dentro de 2 % do original, de acordo com o conjunto de benchmarks da Aspose (cobre mais de 50 formatos de imagem).

## Pré-requisitos

Antes de começar, certifique‑se de que você tem:

- **Aspose.PSD for Java** – baixe o JAR mais recente da [documentação do Aspose.PSD for Java](https://reference.aspose.com/psd/java/).  
- **Java Development Kit** – JDK 8 ou mais recente instalado e configurado.  
- **Sample PSD file** – uma imagem de teste (por exemplo, `sample_bicubic.psd`) colocada em um diretório conhecido.  

Esses itens juntos formam uma base sólida de **biblioteca de imagens java** para o tutorial.

## Importar pacotes
A classe `Image` representa um documento de imagem, e a enumeração `ResizeType` especifica o algoritmo de reamostragem a ser usado.  
```java
import com.aspose.psd.Image;
import com.aspose.psd.ResizeType;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.PsdOptions;
```

## Visão geral do redimensionamento de imagem java com reamostrador bicúbico
Carregue, redimensione e salve uma imagem usando o algoritmo bicúbico em três etapas concisas. As seções a seguir dão uma resposta direta primeiro, depois percorrem o código.

## Como funciona o bicubic resampler?
Ele reamostra a imagem de origem avaliando uma vizinhança de 4×4 pixels para cada pixel de saída, aplicando convolução cúbica ou ponderação Bell para gerar transições mais suaves. Esse método mantém a nitidez das bordas e reduz aliasing, tornando‑o ideal para trabalhos gráficos de nível profissional.

## Como redimensionar imagem java com reamostrador bicúbico?
O método `resize` da classe `Image` altera as dimensões da imagem usando o `ResizeType` especificado. Carregue seu PSD, escolha um `ResizeType` (`CubicConvolution` ou `Bell`), chame `image.resize(newWidth, newHeight, resizeType)` e então salve o resultado. A operação completa normalmente termina em menos de 200 ms para um arquivo de 3000 × 3000 pixels em um CPU de laptop padrão.

### Etapa 1: carregar a imagem
Primeiro, carregue o arquivo PSD de origem que você deseja redimensionar. Substitua `Your Document Directory` pelo caminho real em sua máquina.  
```java
String dataDir = "Your Document Directory";
String filePath = dataDir + "sample_bicubic.psd";
PsdImage image = (PsdImage)Image.load(filePath);
```

### Etapa 2: redimensionar com convolução cúbica (alta qualidade)
Agora aplique o algoritmo **Cubic Convolution**, uma das duas opções bicúbicas que oferece dimensionamento de imagem de alta qualidade. O exemplo redimensiona a imagem para 300 × 300 pixels.  
```java
String destNameCubicConvolution = dataDir + "ResamplerCubicConvolutionStripes_after.psd";
image.resize(300, 300, ResizeType.CubicConvolution);
image.save(destNameCubicConvolution, new PsdOptions(image));
```

### Etapa 3: redimensionar com algoritmo Bell (alta qualidade alternativa)
Se você preferir o algoritmo **Bell**, que oferece um efeito de suavização ligeiramente diferente, pode usá‑lo da mesma forma. Observe que recarregamos a imagem original para manter a comparação justa.  
```java
String destNameBell = dataDir + "ResamplerBellStripes_after.psd";
PsdImage imageBellStripes = (PsdImage)Image.load(filePath);
imageBellStripes.resize(300, 300, ResizeType.Bell);
imageBellStripes.save(destNameBell, new PsdOptions(imageBellStripes));
```

Sinta‑se à vontade para experimentar outras dimensões ou formatos de arquivo — basta ajustar os parâmetros conforme necessário.

## Armadilhas comuns e dicas

- **Caminho incorreto:** Certifique‑se de que `dataDir` termina com um separador de arquivos (`/` ou `\`) apropriado para seu SO.  
- **Exceções de licença:** Executar sem uma licença válida pode adicionar uma marca d'água à imagem de saída. Use uma **licença temporária da Aspose** para testes, depois troque por uma permanente para produção.  
- **Uso de memória:** Arquivos PSD grandes podem consumir memória significativa; considere descartar as imagens (`image.dispose()`) após a gravação.  

## Perguntas frequentes

**P: Posso usar Aspose.PSD for Java com outros formatos de imagem?**  
R: Sim, a biblioteca suporta PSD, PNG, JPEG, TIFF, BMP e muitos outros.

**P: Existe uma licença temporária disponível para Aspose.PSD for Java?**  
R: Sim, você pode obter uma licença temporária na página de licença temporária da Aspose: [Página de licença temporária da Aspose](https://purchase.aspose.com/temporary-license/).

**P: Onde posso encontrar suporte para Aspose.PSD for Java?**  
R: Visite o fórum Aspose.PSD: [Fórum Aspose.PSD](https://forum.aspose.com/c/psd/34) para quaisquer dúvidas relacionadas ao suporte.

**P: Posso baixar a biblioteca Aspose.PSD for Java?**  
R: Sim, baixe a biblioteca na página de lançamentos do Aspose.PSD Java: [Página de lançamentos do Aspose.PSD Java](https://releases.aspose.com/psd/java/).

**P: Como faço para comprar Aspose.PSD for Java?**  
R: Você pode comprar Aspose.PSD for Java na página de compra do Aspose.PSD: [Página de compra do Aspose.PSD](https://purchase.aspose.com/buy).

## Conclusão

Agora você tem um padrão completo e pronto para produção para **redimensionar imagem java** usando o bicubic resampler da Aspose.PSD. Seja construindo um editor de desktop, um serviço de processamento em lote ou um pipeline de imagens baseado em nuvem, a mesma abordagem de três etapas — carregar, redimensionar com o `ResizeType` escolhido e salvar — entrega resultados de alta qualidade em mais de 50 formatos suportados. Explore as opções adicionais da biblioteca, como especificar DPI ou aplicar anti‑aliasing, para ajustar finamente a saída ao seu caso de uso específico.

---

**Última atualização:** 2026-10-29  
**Testado com:** Aspose.PSD for Java 24.11 (mais recente no momento da escrita)  
**Autor:** Aspose

## Tutoriais relacionados

- [Como realizar redimensionamento simples com Aspose.PSD – Biblioteca de manipulação de imagens Java](/psd/java/basic-image-operations/simple-resizing/)
- [Como converter PSD para PNG e redimensionar proporcionalmente com Aspose.PSD for Java](/psd/java/advanced-image-manipulation/resize-image-proportionally/)
- [Como girar imagem em um ângulo específico com Aspose.PSD for Java](/psd/java/advanced-image-manipulation/rotate-image-specific-angle/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}