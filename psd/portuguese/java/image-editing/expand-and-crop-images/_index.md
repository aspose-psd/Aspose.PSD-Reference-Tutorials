---
date: 2026-07-08
description: 'Tutorial da biblioteca Java de edição de imagens: aprenda como recortar
  imagens em Java usando Aspose.PSD for Java, redimensionar, expandir a tela e converter
  PSD para JPEG.'
keywords:
- java image editing library
- java image processing tutorial
- how to crop image java
lastmod: 2026-07-08
linktitle: Expandir e Recortar Imagens
og_description: Tutorial da biblioteca Java de edição de imagens mostra como recortar,
  expandir a tela e converter PSD para JPEG usando Aspose.PSD for Java em minutos.
og_image_alt: 'Guide: Crop and expand images in Java with Aspose.PSD'
og_title: Biblioteca Java de Edição de Imagens – Recortar Imagem com Aspose.PSD
schemas:
- author: Aspose
  dateModified: '2026-07-08'
  description: 'Java image editing library tutorial: learn how to crop image java
    using Aspose.PSD for Java, resize, expand canvas, and convert PSD to JPEG.'
  headline: Java Image Editing Library – Crop Image with Aspose.PSD
  type: TechArticle
- questions:
  - answer: Aspose.PSD for Java.
    question: What library handles crop image java?
  - answer: A free trial works for testing; a commercial license is required for production.
    question: Do I need a license for development?
  - answer: Yes, using `JpegOptions` together with a cropping rectangle.
    question: Can I convert PSD to JPEG while cropping?
  - answer: Aspose.PSD supports Java 8 and newer versions.
    question: Is Java 8 supported?
  - answer: Typically under 10 minutes for a basic crop operation.
    question: How long does the implementation take?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- java image editing
- Aspose.PSD
- image cropping
- PSD to JPEG
title: Biblioteca Java de Edição de Imagens – Recortar Imagem com Aspose.PSD
url: /pt/java/image-editing/expand-and-crop-images/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Biblioteca Java de Edição de Imagens: Recortar Imagem Java com Aspose.PSD

## Introdução

Neste tutorial você aprenderá a usar uma **java image editing library** — especificamente o Aspose.PSD para Java — para recortar, expandir e converter arquivos PSD em JPEG. Seja preparando recursos para um portal web ou automatizando a geração de miniaturas, os passos abaixo fornecem um fluxo de trabalho repetível e pronto para produção que você pode integrar a qualquer projeto Java 8+.

## Respostas Rápidas
- **Qual biblioteca lida com crop image java?** Aspose.PSD for Java.  
- **Preciso de licença para desenvolvimento?** Uma versão de avaliação gratuita funciona para testes; uma licença comercial é necessária para produção.  
- **Posso converter PSD para JPEG enquanto recorto?** Sim, usando `JpegOptions` junto com um retângulo de recorte.  
- **O Java 8 é suportado?** Aspose.PSD suporta Java 8 e versões mais recentes.  
- **Quanto tempo leva a implementação?** Normalmente menos de 10 minutos para uma operação básica de recorte.

## O que é “crop image java”?

Crop image java significa selecionar uma região retangular da imagem fonte e descartar tudo que está fora dessa região. Com o Aspose.PSD, você cria um `Rectangle` que define a área, aplica‑o a um `RasterImage` e então salva o resultado em qualquer formato suportado, como JPEG.

## Por que usar Aspose.PSD para recorte de imagens Java?

Aspose.PSD fornece uma **java image editing library** que manipula arquivos PSD nativamente, suporta mais de 100 recursos de camada e pode processar imagens de até 10 000 × 10 000 pixels mantendo o uso de memória abaixo de 500 MB. Também oferece conversão integrada para JPEG, PNG, BMP e mais, tudo sem precisar de ferramentas externas. Isso torna os pipelines de processamento em lote rápidos, confiáveis e fáceis de manter.

## Pré-requisitos

1. **Java Development Kit (JDK)** – Java 8 ou posterior instalado.  
2. **Aspose.PSD for Java** – faça o download da biblioteca no site oficial **[aqui](https://releases.aspose.com/psd/java/)**.  

> **Dica profissional:** Adicione o JAR do Aspose.PSD ao classpath do seu projeto ou às dependências Maven/Gradle para evitar `ClassNotFoundException`.

## Importar Pacotes

Adicione as importações necessárias ao seu arquivo Java. Essas classes dão acesso ao carregamento de imagens, manipulação raster, definição de retângulo e opções de exportação JPEG.

## Como Recortar Imagem Java Usando Aspose.PSD?

Carregue o PSD fonte com `RasterImage`, defina um `Rectangle` que descreve a área de recorte (coordenadas negativas podem expandir a tela) e, finalmente, salve o resultado com `JpegOptions`. Esse fluxo de três etapas lida tanto com recorte quanto com conversão de formato em uma única passagem, eliminando a necessidade de arquivos intermediários.

## Etapa 1: Defina o Diretório do Seu Documento

Especifique a pasta que contém o arquivo PSD fonte. Substitua o placeholder pelo caminho real na sua máquina.

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;
import com.aspose.psd.Rectangle;

import com.aspose.psd.imageoptions.JpegOptions;
```

## Etapa 2: Especifique os Caminhos de Origem e Destino

Defina de onde ler o PSD e onde gravar o JPEG recortado.

```java
String dataDir = "Your Document Directory";
```

## Etapa 3: Carregue e Armazene em Cache a Imagem

`RasterImage` representa uma versão rasterizada de um arquivo PSD na memória.  
Carregue o PSD em um objeto `RasterImage`. O cache melhora o desempenho para operações subsequentes, como recorte.

```java
String sourceFile = dataDir + "example1.psd";
String destName = dataDir + "jpeg_out.jpg";
```

## Etapa 4: Crie um Rectangle para Recorte

`Rectangle` define as coordenadas X, Y e a largura/altura da região de recorte.  
Crie um `Rectangle` que descreve a região que você deseja manter. As coordenadas podem ser negativas para **expandir** a tela antes do recorte, o que é útil para adicionar uma borda ao redor da imagem original.

```java
RasterImage rasterImage = (RasterImage)Image.load(sourceFile);
rasterImage.cacheData();
```

> **Por que usar coordenadas negativas?**  
> Valores negativos de X/Y deslocam a área de recorte para a esquerda/acima, efetivamente adicionando espaço vazio (expansão) ao redor do conteúdo original antes do recorte final.

## Etapa 5: Salve a Imagem Recortada

`JpegOptions` especifica configurações para a saída JPEG, como qualidade e compressão.  
Finalmente, salve a imagem resultante usando `JpegOptions`. Esta etapa também demonstra **convert psd jpeg** ao aplicar o retângulo de recorte.

```java
Rectangle destRect = new Rectangle(-200, -200, 300, 300);
```

> **Resultado:** `jpeg_out.jpg` agora contém uma imagem de 300 × 300 pixels que foi expandida em 200 px em cada lado e então recortada para o retângulo definido.

Parabéns! Você realizou com sucesso **java image cropping**, expandiu a tela e converteu um arquivo PSD em JPEG — tudo em algumas linhas concisas de código.

## Casos de Uso Comuns

- **Preparar recursos para a web** – recorte e redimensione capturas de tela ou designs antes de fazer upload.  
- **Gerar miniaturas** – extraia uma região específica de um PSD grande para fins de visualização.  
- **Processamento em lote automatizado** – percorra uma pasta de arquivos PSD, aplicando o mesmo retângulo de recorte a cada um.

## Solução de Problemas e Dicas

| Problema | Correção Sugerida |
|----------|-------------------|
| `OutOfMemoryError` ao carregar PSDs grandes | Chame `rasterImage.cacheData()` cedo e considere aumentar o tamanho do heap da JVM (`-Xmx`). |
| A área recortada está fora do centro | Verifique os deslocamentos X/Y do retângulo; lembre‑se de que valores negativos expandem a tela. |
| O JPEG de saída parece borrado | Ajuste a configuração de qualidade de `JpegOptions` (por exemplo, `new JpegOptions { Quality = 90 }`). |

## Perguntas Frequentes

### Q1: O Aspose.PSD é compatível com diferentes versões do Java?

A1: Sim, o Aspose.PSD suporta Java 8, 11, 17 e versões mais recentes, garantindo ampla compatibilidade em diferentes ambientes de desenvolvimento.

### Q2: Posso usar o Aspose.PSD em projetos comerciais?

A2: Absolutamente, o Aspose.PSD oferece licenças comerciais para desenvolvedores, permitindo seu uso tanto em aplicações pessoais quanto comerciais.

### Q3: Existem limitações nos formatos de arquivo de imagem suportados?

A3: O Aspose.PSD suporta mais de 30 formatos de imagem, incluindo PSD, JPEG, PNG, BMP, TIFF e mais. Consulte a [documentação](https://reference.aspose.com/psd/java/) para a lista completa.

### Q4: Como posso obter suporte para dúvidas relacionadas ao Aspose.PSD?

A4: Visite o [fórum Aspose.PSD](https://forum.aspose.com/c/psd/34) para buscar ajuda da comunidade ou da equipe de suporte da Aspose.

### Q5: Há uma versão de avaliação gratuita disponível?

A5: Sim, você pode explorar o Aspose.PSD com uma avaliação gratuita. Baixe‑o [aqui](https://releases.aspose.com/).

**Última atualização:** 2026-07-08  
**Testado com:** Aspose.PSD for Java 24.12  
**Autor:** Aspose  

{{< blocks/products/products-backtop-button >}}

```java
rasterImage.save(destName, new JpegOptions(), destRect);
```

## Tutoriais Relacionados

- [Redimensionamento Simples com Aspose.PSD – Biblioteca Java de Manipulação de Imagens](/psd/java/basic-image-operations/simple-resizing/)
- [Como Rotacionar Imagem 270 Graus com Aspose.PSD para Java](/psd/java/advanced-image-manipulation/rotate-image/)
- [Como Ajustar Gamma no Processamento de Imagens Java com Aspose.PSD](/psd/java/advanced-techniques/adjust-gamma/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}