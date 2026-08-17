---
date: 2026-08-17
description: Aprenda como cortar arquivo PSD java com Aspose.PSD para Java – uma forma
  rápida e precisa de aparar documentos Photoshop em suas aplicações Java.
keywords:
- crop psd file java
- aspose.psd java
- java image cropping
lastmod: 2026-08-17
linktitle: Cortar arquivo PSD
og_description: Cortar arquivo PSD java usando Aspose.PSD para Java. Este guia mostra
  passo a passo como aparar arquivos Photoshop de forma eficiente, com explicações
  sem código e dicas de boas práticas.
og_image_alt: Guide showing how to crop a PSD file in Java using Aspose.PSD
og_title: Cortar arquivo PSD java com Aspose.PSD – corte rápido de imagens
schemas:
- author: Aspose
  dateModified: '2026-08-17'
  description: Learn how to crop psd file java with Aspose.PSD for Java – a fast,
    precise way to trim Photoshop documents in your Java applications.
  headline: Crop psd file java using Aspose.PSD
  type: TechArticle
- description: Learn how to crop psd file java with Aspose.PSD for Java – a fast,
    precise way to trim Photoshop documents in your Java applications.
  name: Crop psd file java using Aspose.PSD
  steps:
  - name: set document directory
    text: Replace “Your Document Directory” with the absolute or relative path that
      contains the PSD you want to process.
  - name: load PSD file
    text: The `RasterImage` class is Aspose.PSD’s entry point for raster‑based operations
      on a PSD file. Loading the file creates an in‑memory representation that you
      can manipulate.
  - name: define crop area
    text: '`Rectangle` defines the X and Y coordinates together with width and height
      of the region to keep. This class is part of the standard Java AWT package and
      is used by Aspose.PSD to specify cropping bounds.'
  - name: save cropped PSD
    text: After applying the crop, you can persist the result back to PSD format.
      The library writes only the cropped pixels, keeping the original color mode
      and bit depth.
  - name: save cropped image as PNG
    text: If you need a web‑friendly version, export the cropped raster to PNG. Aspose.PSD
      provides PNG save options that let you control compression level and interlacing.
  type: HowTo
- questions:
  - answer: Aspose.PSD for Java.
    question: What library handles PSD cropping in Java?
  - answer: Two API calls after loading the image.
    question: How many lines of code are required for a basic crop?
  - answer: Yes, using the built‑in PNG save options.
    question: Can I export the cropped area as PNG?
  - answer: A commercial license is needed beyond the trial period.
    question: Is a license required for production use?
  - answer: Java 8 and later, including Java 11, 17, and 21.
    question: What Java versions are supported?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- crop psd
- aspose.psd
- java image processing
title: Cortar arquivo PSD java usando Aspose.PSD
url: /pt/java/image-processing/crop-psd-file/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Cortar arquivo PSD em Java usando Aspose.PSD

## Introdução

Se você precisar cortar documentos do Photoshop programaticamente, **crop psd file java** é uma tarefa comum para desenvolvedores Java que trabalham com pipelines gráficos, pipelines de ativos ou fluxos de trabalho de design automatizados. Aspose.PSD para Java fornece uma API dedicada que permite definir um retângulo e extrair a região necessária em apenas algumas linhas de código. Neste tutorial você aprenderá por que a biblioteca foi construída para recorte de alto desempenho, como configurar seu ambiente e os passos exatos para produzir resultados em PSD e PNG.

## Respostas rápidas
- **Qual biblioteca lida com recorte de PSD em Java?** Aspose.PSD for Java.
- **Quantas linhas de código são necessárias para um recorte básico?** Duas chamadas de API após carregar a imagem.
- **Posso exportar a área recortada como PNG?** Sim, usando as opções de salvamento PNG integradas.
- **É necessária uma licença para uso em produção?** Uma licença comercial é necessária após o período de avaliação.
- **Quais versões do Java são suportadas?** Java 8 e posteriores, incluindo Java 11, 17 e 21.

## O que é crop psd file java?

Crop psd file java refere‑se ao processo de cortar programaticamente uma região retangular de um Documento Photoshop (.psd) usando código Java. Com Aspose.PSD você pode executar essa operação sem iniciar o Photoshop, tornando‑a ideal para pipelines de imagem do lado do servidor.

## Por que usar Aspose.PSD para Java?

Aspose.PSD suporta **mais de 30 formatos de entrada e saída** e pode processar arquivos PSD de até **500 MB** sem carregar todo o documento na memória, graças à sua arquitetura de streaming. A biblioteca preserva camadas, máscaras e perfis de cor, entregando um resultado recortado que corresponde à saída nativa do Photoshop. Esse desempenho quantificado permite lidar com trabalhos em lote em hardware comum com uso de memória previsível.

## Pré-requisitos

- **Ambiente de desenvolvimento Java** – JDK 8 ou mais recente instalado e configurado.
- **Aspose.PSD para Java** – baixe o JAR mais recente e a documentação [documentação do Aspose.PSD para Java](https://reference.aspose.com/psd/java/).
- **Arquivo PSD de exemplo** – coloque um arquivo .psd dentro do diretório do seu projeto para que o código possa localizá-lo.

## Como recortar um arquivo PSD em Java?

Carregue o arquivo fonte, defina o retângulo que deseja manter, aplique o recorte e, finalmente, salve o resultado nos formatos desejados. Todo o fluxo de trabalho requer apenas cinco etapas simples, cada uma ilustrada com um espaço reservado onde você inserirá seu próprio código.

### Etapa 1: definir diretório do documento

Substitua “Your Document Directory” pelo caminho absoluto ou relativo que contém o PSD que você deseja processar.

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;
import com.aspose.psd.Rectangle;

import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.imageoptions.PngOptions;
import com.aspose.psd.imageoptions.PsdOptions;
import com.aspose.psd.xmp.types.complex.colorant.ColorType;
```

### Etapa 2: carregar arquivo PSD

A classe `RasterImage` é o ponto de entrada do Aspose.PSD para operações baseadas em raster em um arquivo PSD. Carregar o arquivo cria uma representação em memória que pode ser manipulada.

```java
String dataDir = "Your Document Directory";
```

### Etapa 3: definir área de recorte

`Rectangle` define as coordenadas X e Y juntamente com a largura e altura da região a ser mantida. Essa classe faz parte do pacote padrão Java AWT e é usada pelo Aspose.PSD para especificar os limites do recorte.

```java
String sourceFileName = dataDir + "1.psd";
RasterImage image = (RasterImage)Image.load(sourceFileName);
```

### Etapa 4: salvar PSD recortado

Após aplicar o recorte, você pode persistir o resultado novamente no formato PSD. A biblioteca grava apenas os pixels recortados, mantendo o modo de cor e a profundidade de bits originais.

```java
image.crop(new Rectangle(10, 30, 100, 100));
```

### Etapa 5: salvar imagem recortada como PNG

Se precisar de uma versão amigável para a web, exporte o raster recortado para PNG. Aspose.PSD fornece opções de salvamento PNG que permitem controlar o nível de compressão e o entrelaçamento.

```java
String exportPathPsd = dataDir + "CropTest.psd";
image.save(exportPathPsd, new PsdOptions());
```

## Problemas comuns e soluções

- **Coordenadas do retângulo incorretas** – Certifique-se de que os valores X/Y comecem em 0 para o canto superior esquerdo; valores negativos gerarão uma `ArgumentException`.
- **Picos de memória em arquivos grandes** – Use a opção `loadOptions.setLoadOnlyVisibleLayers(true)` para reduzir o uso de memória quando não precisar de camadas ocultas.
- **Perda de perfil de cor** – Preserve o perfil ICC original chamando `image.getColorProfile()` antes do recorte e reatribuindo‑o após a operação.

## Perguntas frequentes

### Q1: posso usar Aspose.PSD para Java para recortar imagens em outros formatos?

A1: Aspose.PSD tem como foco principal arquivos PSD, mas também suporta BMP, GIF, JPEG, PNG, TIFF e vários outros formatos raster para entrada e saída.

### Q2: o Aspose.PSD para Java é adequado para processamento de imagens em grande escala?

A2: Sim. A arquitetura de streaming da biblioteca processa arquivos PSD com centenas de páginas usando menos de 100 MB de memória, tornando‑a ideal para trabalhos em lote.

### Q3: há considerações de licenciamento ao usar Aspose.PSD para Java?

A3: É necessária uma licença comercial para implantações em produção. Detalhes estão disponíveis na [página de compra do Aspose.PSD para Java](https://purchase.aspose.com/buy).

### Q4: como posso obter suporte para problemas relacionados ao Aspose.PSD para Java?

A4: Visite o [fórum do Aspose.PSD para Java](https://forum.aspose.com/c/psd/34) para fazer perguntas, compartilhar trechos de código e receber ajuda da comunidade e dos engenheiros do produto.

### Q5: posso experimentar o Aspose.PSD para Java antes de comprar?

A5: Sim, um teste gratuito totalmente funcional pode ser baixado [download de teste gratuito do Aspose.PSD](https://releases.aspose.com/).

{{< blocks/products/products-backtop-button >}}

```java
String exportPathPng = dataDir + "CropTest.png";
PngOptions options = new PngOptions();
options.setColorType(PngColorType.TruecolorWithAlpha);
image.save(exportPathPng, options);
```

## Tutoriais Relacionados

- [Recortar Imagem por Retângulo no Aspose.PSD para Java](/psd/java/image-editing/crop-image-by-rectangle/)
- [Recortar Imagem por Deslocamentos no Aspose.PSD para Java](/psd/java/image-editing/crop-image-by-shifts/)
- [Como Rotacionar Imagem em Java com Aspose.PSD](/psd/java/advanced-image-manipulation/rotate-image/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}