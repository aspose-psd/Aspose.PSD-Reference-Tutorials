---
date: 2026-09-28
description: Tutorial de processamento de imagens Java mostra como ajustar o brilho
  de uma imagem usando Aspose.PSD para Java. Siga o código passo a passo para carregar,
  modificar e salvar arquivos PSD ou TIFF.
keywords:
- java image processing
- aspose psd java
- java image manipulation
- adjust brightness java
lastmod: 2026-09-28
linktitle: Ajustar brilho de uma imagem
og_description: Tutorial de processamento de imagens Java mostra como ajustar o brilho
  de uma imagem usando Aspose.PSD para Java. Siga o código passo a passo para carregar,
  modificar e salvar arquivos PSD ou TIFF.
og_image_alt: Guide to adjusting image brightness in Java using Aspose.PSD
og_title: 'Processamento de imagens Java: ajuste de brilho com Aspose.PSD'
schemas:
- author: Aspose
  dateModified: '2026-09-28'
  description: Java image processing tutorial shows how to adjust brightness of an
    image using Aspose.PSD for Java. Follow step‑by‑step code to load, modify, and
    save PSD or TIFF files.
  headline: 'Java image processing: adjust brightness with Aspose.PSD'
  type: TechArticle
- description: Java image processing tutorial shows how to adjust brightness of an
    image using Aspose.PSD for Java. Follow step‑by‑step code to load, modify, and
    save PSD or TIFF files.
  name: 'Java image processing: adjust brightness with Aspose.PSD'
  steps:
  - name: Load the image
    text: The `RasterImage` class represents a rasterized version of a PSD or TIFF
      file in memory. It provides direct pixel access for color‑correction operations.
      In this step, we load the target image and cast it to a `RasterImage` for further
      processing.
  - name: Adjust brightness
    text: '`adjustBrightness(int value)` changes the lightness of every pixel by the
      specified integer value. Positive numbers brighten the image; negative numbers
      darken it. The method processes the image in‑place, so no additional object
      creation is required. Here, we use the `adjustBrightness` method to mod'
  - name: Set TiffOptions
    text: '`TiffOptions` specifies the encoding parameters for TIFF output, such as
      bits per sample and photometric interpretation. It lets you control how the
      resulting file is encoded. Configure the `TiffOptions` for saving the adjusted
      image. Adjust the `bitsPerSample` and `photometric` properties based on '
  - name: Save the resultant image
    text: Calling `save` writes the processed raster data to a file using the previously
      defined options. The operation is atomic and guarantees that the output file
      is a valid TIFF image. Finally, save the modified image using the specified
      `TiffOptions`.
  type: HowTo
- questions:
  - answer: Yes, Aspose.PSD for Java supports JPEG, PNG, BMP, GIF, and many other
      raster formats in addition to PSD and TIFF.
    question: Can I adjust brightness in other image formats besides PSD?
  - answer: Wrap the processing code in a try‑catch block and catch `IOException`
      or `ImageProcessingException` to manage file‑access and raster‑operation errors.
    question: How can I handle errors during the image adjustment process?
  - answer: The method accepts integer values from –255 to +255; values outside this
      range are clamped to the nearest limit.
    question: Is there a limit to the range of brightness adjustment?
  - answer: Yes, a commercial license is required for production use. Purchase a license
      [here](https://purchase.aspose.com/buy).
    question: Can I use Aspose.PSD for Java in commercial projects?
  - answer: Yes, you can explore the library with a free trial from [here](https://releases.aspose.com/).
    question: Is there a free trial available?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- java image processing
- aspose psd
- java image manipulation
title: 'Processamento de imagens Java: ajuste de brilho com Aspose.PSD'
url: /pt/java/advanced-techniques/adjust-brightness/
weight: 21
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Ajustar brilho de uma imagem com Aspose.PSD para Java

## Introdução

Neste tutorial de **java image processing** você aprenderá como ajustar o brilho de uma imagem diretamente a partir do código Java. Ajustar o brilho é uma tarefa frequente para designers gráficos, fotógrafos e qualquer pessoa que construa pipelines de processamento de imagens. Neste guia de **java image manipulation** percorreremos todo o fluxo de trabalho — carregando um PSD/TIFF, aplicando um deslocamento de brilho e salvando o resultado — usando a biblioteca Aspose.PSD para Java.

## Respostas rápidas
- **Qual biblioteca controla o brilho?** Aspose.PSD for Java.  
- **Qual método altera o brilho?** `RasterImage.adjustBrightness()`.  
- **Posso trabalhar com arquivos PSD e TIFF?** Yes, the API supports both formats and 10+ additional image types.  
- **Preciso de uma licença para produção?** A commercial license is required for non‑evaluation use.  
- **Quanto tempo leva a implementação?** Typically under 10 minutes for a basic adjustment.

## O que é java image processing?

`Java image processing` refere-se ao conjunto de técnicas que permitem ler, transformar e gravar dados de imagem programaticamente usando Java. Ajustar o brilho é uma das operações principais que altera a luminosidade geral de cada pixel, tornando áreas escuras mais claras ou áreas claras mais escuras.

## Por que usar Aspose.PSD para Java?

Aspose.PSD para Java fornece uma solução abrangente, pure‑Java, que suporta uma ampla variedade de formatos raster e vetoriais, elimina dependências nativas e oferece cache de alto desempenho para arquivos grandes. Sua API extensa permite que desenvolvedores realizem correções de cor complexas e edições baseadas em camadas com código mínimo, tornando-a ideal tanto para ajustes simples quanto para pipelines avançados de processamento de imagens.

- **Suporta mais de 10 formatos raster e vetoriais** – PSD, TIFF, JPEG, PNG, BMP, GIF e mais.  
- **Implementação Pure‑Java** – sem DLLs nativas ou dependências externas, funcionando em qualquer JVM.  
- **Cache de alto desempenho** – os dados raster podem ser armazenados em cache, permitindo edições repetidas até 2× mais rápidas em arquivos grandes.  
- **Superfície de API rica** – mais de 150 métodos para correção de cor, manipulação de camadas, máscaras e composição.

## Pré-requisitos

Before diving into the tutorial, ensure you have the following prerequisites:

- Aspose.PSD for Java Library: Baixe e instale a biblioteca a partir da [Aspose.PSD for Java documentation](https://reference.aspose.com/psd/java/).  
- Java Development Kit (JDK) 8 ou superior instalado na sua máquina.  
- Um ambiente de desenvolvimento (IDE) como IntelliJ IDEA, Eclipse ou VS Code.

## Importar pacotes

Para começar, importe os pacotes necessários para seu projeto Java. Neste exemplo, usaremos o seguinte:

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.psd.fileformats.tiff.enums.TiffPhotometrics;
import com.aspose.psd.imageoptions.TiffOptions;
```

Now, let's break down the process of adjusting the brightness of an image into simple steps:

## Como ajustar o brilho usando Aspose.PSD?

Carregue sua imagem de origem, aplique um deslocamento de brilho, configure as opções de salvamento e grave o resultado no disco — tudo em quatro etapas concisas. As seções a seguir fornecem um guia passo a passo claro que você pode copiar para seu próprio projeto. Essa abordagem garante que cada operação seja executada de forma eficiente e que a imagem final mantenha a qualidade original enquanto reflete a alteração de brilho desejada.

### Etapa 1: Carregar a imagem

A classe `RasterImage` representa uma versão rasterizada de um arquivo PSD ou TIFF na memória. Ela fornece acesso direto aos pixels para operações de correção de cor.

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";
String destName = dataDir + "AdjustBrightness_out.tiff";

// Load an existing image into an instance of RasterImage class
Image image = Image.load(sourceFile);
// Cast object of Image to RasterImage
RasterImage rasterImage = (RasterImage) image;

// Check if RasterImage is cached and Cache RasterImage for better performance
if (!rasterImage.isCached()) {
    rasterImage.cacheData();
}
```

Nesta etapa, carregamos a imagem alvo e a convertemos para um `RasterImage` para processamento adicional.

### Etapa 2: Ajustar brilho

`adjustBrightness(int value)` altera a luminosidade de cada pixel pelo valor inteiro especificado. Números positivos clareiam a imagem; números negativos escurecem. O método processa a imagem in‑place, portanto não é necessária a criação de objetos adicionais.

```java
// Adjust the brightness
rasterImage.adjustBrightness(-50);
```

Aqui, usamos o método `adjustBrightness` para modificar o brilho da imagem. Neste exemplo, diminuímos o brilho em 50 unidades, mas você pode personalizar esse valor conforme suas necessidades.

### Etapa 3: Definir TiffOptions

`TiffOptions` especifica os parâmetros de codificação para a saída TIFF, como bits por amostra e interpretação fotométrica. Permite controlar como o arquivo resultante é codificado.

```java
int[] ushort = {8, 8, 8};
// Create an instance of TiffOptions for the resultant image
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
tiffOptions.setBitsPerSample(ushort);
tiffOptions.setPhotometric(TiffPhotometrics.Rgb);
```

Configure o `TiffOptions` para salvar a imagem ajustada. Ajuste as propriedades `bitsPerSample` e `photometric` de acordo com suas necessidades específicas.

### Etapa 4: Salvar a imagem resultante

Chamar `save` grava os dados raster processados em um arquivo usando as opções definidas anteriormente. A operação é atômica e garante que o arquivo de saída seja uma imagem TIFF válida.

```java
// Save the resultant image
rasterImage.save(destName, tiffOptions);
```

Finalmente, salve a imagem modificada usando o `TiffOptions` especificado.

## Problemas comuns e soluções

| Issue | Reason | Solution |
|-------|--------|----------|
| **`ClassCastException` ao converter Image** | O arquivo não é uma imagem raster (por exemplo, um PSD vetorial). | Verifique o formato do arquivo de origem ou use `image instanceof RasterImage` antes da conversão. |
| **Alteração de brilho não tem efeito** | A imagem não foi armazenada em cache antes do ajuste. | Chame `rasterImage.cacheData()` como mostrado na Etapa 1. |
| **Arquivo salvo parece corrompido** | Configuração incorreta de `TiffOptions`. | Garanta que `bitsPerSample` corresponda à profundidade da imagem de origem (geralmente 8 bits por canal). |

## Perguntas frequentes

**Q: Posso ajustar o brilho em outros formatos de imagem além de PSD?**  
A: Sim, Aspose.PSD para Java suporta JPEG, PNG, BMP, GIF e muitos outros formatos raster além de PSD e TIFF.

**Q: Como posso lidar com erros durante o processo de ajuste de imagem?**  
A: Envolva o código de processamento em um bloco try‑catch e capture `IOException` ou `ImageProcessingException` para gerenciar erros de acesso a arquivos e operações raster.

**Q: Existe um limite para a faixa de ajuste de brilho?**  
A: O método aceita valores inteiros de –255 a +255; valores fora dessa faixa são limitados ao limite mais próximo.

**Q: Posso usar Aspose.PSD para Java em projetos comerciais?**  
A: Sim, uma licença comercial é necessária para uso em produção. Adquira uma licença [aqui](https://purchase.aspose.com/buy).

**Q: Existe uma versão de avaliação gratuita disponível?**  
A: Sim, você pode explorar a biblioteca com uma avaliação gratuita a partir de [aqui](https://releases.aspose.com/).

**Q: O método `adjustBrightness` afeta a visibilidade das camadas?**  
A: O método opera na imagem composta rasterizada, portanto camadas ocultas são ignoradas durante a rasterização, preservando o resultado visual pretendido.

**Q: Posso encadear múltiplos ajustes (por exemplo, contraste, saturação) juntos?**  
A: Absolutamente. Após ajustar o brilho, você pode chamar `adjustContrast`, `adjustSaturation` ou outros métodos de correção de cor na mesma instância de `RasterImage`.

---

**Última atualização:** 2026-09-28  
**Testado com:** Aspose.PSD for Java 24.12 (latest at time of writing)  
**Autor:** Aspose

## Tutoriais relacionados

- [Biblioteca de Processamento de Imagens Java: Inverter Camada usando Aspose.PSD](/psd/java/advanced-image-manipulation/invert-adjustment-layer/)
- [Converter Imagem para Escala de Cinza Usando Aspose.PSD para Java](/psd/java/advanced-techniques/grayscale-image/)
- [Como Rotacionar Imagem em um Ângulo Específico com Aspose.PSD para Java](/psd/java/advanced-image-manipulation/rotate-image-specific-angle/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}