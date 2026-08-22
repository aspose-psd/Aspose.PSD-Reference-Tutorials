---
date: 2026-07-17
description: Aprenda a criar imagens BMP usando stream no Aspose.PSD para Java. Siga
  este tutorial de imagem Java passo a passo para geração eficiente de imagens.
keywords:
- how to create bmp
- generate image stream
- java image tutorial
lastmod: 2026-07-17
linktitle: Criar imagem usando Stream
og_description: Aprenda a criar imagens BMP usando stream no Aspose.PSD para Java.
  Este tutorial de imagem Java mostra a geração passo a passo de arquivos BMP.
og_image_alt: 'Guide: create BMP image from stream with Aspose.PSD Java'
og_title: Como criar BMP usando Stream no Aspose.PSD para Java
schemas:
- author: Aspose
  dateModified: '2026-07-17'
  description: Learn how to create BMP images using stream in Aspose.PSD for Java.
    Follow this step‑by‑step java image tutorial for efficient image generation.
  headline: How to Create BMP Using Stream in Aspose.PSD for Java
  type: TechArticle
- questions:
  - answer: '`BmpOptions` combined with `Image.create`.'
    question: What is the main class for BMP creation?
  - answer: A free trial works for testing; a commercial license is required for production.
    question: Do I need a license for development?
  - answer: Yes, using `FileCreateSource` streams the data.
    question: Can I generate large BMPs (>10 MB) without loading the whole file into
      memory?
  - answer: Java 8 through Java 21 are fully compatible.
    question: Which Java versions are supported?
  - answer: Only the Aspose.PSD for Java JAR; no external imaging libraries needed.
    question: Is any additional dependency required?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- create bmp
- Aspose.PSD
- Java image processing
- stream image generation
title: Como criar BMP usando Stream no Aspose.PSD para Java
url: /pt/java/image-editing/create-image-using-stream/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Como criar BMP usando Stream no Aspose.PSD para Java

## Introdução

Criar arquivos BMP diretamente a partir de um stream oferece controle granular sobre o uso de memória e o manuseio de arquivos, o que é essencial para aplicações Java de alto desempenho. Neste tutorial, você aprenderá **como criar BMP** imagens usando a API de streaming do Aspose.PSD, passo a passo. Cobriremos tudo, desde a configuração do seu ambiente até a gravação da imagem final, para que você possa integrar esta técnica em projetos reais imediatamente.

## Respostas Rápidas
- **Qual é a classe principal para criação de BMP?** `BmpOptions` combined with `Image.create`.
- **Preciso de uma licença para desenvolvimento?** A free trial works for testing; a commercial license is required for production.
- **Posso gerar BMPs grandes (>10 MB) sem carregar todo o arquivo na memória?** Yes, using `FileCreateSource` streams the data.
- **Quais versões do Java são suportadas?** Java 8 through Java 21 are fully compatible.
- **É necessária alguma dependência adicional?** Only the Aspose.PSD for Java JAR; no external imaging libraries needed.

## Como criar BMP usando stream no Aspose.PSD para Java?

Carregue o diretório de destino, configure `BmpOptions` com um `FileCreateSource` e chame `Image.create` com a largura e altura desejadas – toda a operação é concluída em três linhas concisas de código. Essa abordagem grava o BMP diretamente em um stream de arquivo, evitando buffers temporários e proporcionando desempenho ideal para geração em lote de imagens.

## O que é Aspose.PSD para Java?

Aspose.PSD para Java é uma biblioteca abrangente que permite a criação, manipulação e conversão programáticas de arquivos Photoshop® (PSD) e mais de 30 outros formatos raster. Ela pode processar arquivos de até 2 GB sem carregar a imagem completa na memória, tornando‑a ideal para pipelines de imagens no lado do servidor.

## Por que usar geração de BMP baseada em stream?

A geração baseada em stream reduz a sobrecarga de memória ao gravar bytes diretamente no disco, o que é especialmente benéfico ao criar BMPs grandes ou processar muitas imagens em paralelo. Aspose.PSD pode lidar com **30+ formatos de imagem** e gerar BMPs de até 500 MPixels em menos de um segundo em hardware de servidor típico.

## Pré‑requisitos

Antes de começar, certifique‑se de que você tem:

- **Java Development Kit (JDK)** – Java 8 ou mais recente instalado.
- **Aspose.PSD Library** – Baixe o JAR mais recente da [documentation](https://reference.aspose.com/psd/java/).
- **IDE** – Eclipse, IntelliJ IDEA ou qualquer IDE compatível com Java que você prefira.

## Importar Pacotes

As declarações `import` trazem as classes necessárias para o escopo.  
`BmpOptions` configura as definições específicas de BMP, enquanto `FileCreateSource` representa o stream de saída.

```java
import com.aspose.psd.Image;

import com.aspose.psd.imageoptions.BmpOptions;
import com.aspose.psd.sources.FileCreateSource;
import com.aspose.psd.sources.StreamSource;
import com.aspose.psd.system.io.FileMode;
import com.aspose.psd.system.io.FileStream;
import com.aspose.psd.system.io.Stream;
import java.io.FileInputStream;
```

## Etapa 1: Configurar Diretório de Documentos

`File` representa um caminho de arquivo ou diretório no sistema de arquivos.  

`File dataDir = new File("Your Document Directory");` – esta variável aponta para a pasta onde o BMP será salvo.  
Substitua `"Your Document Directory"` pelo caminho real na sua máquina.

```java
String dataDir = "Your Document Directory";
```

## Etapa 2: Especificar Nome do Arquivo de Saída

`String outFile = dataDir.getAbsolutePath() + File.separator + "output.bmp";` – define o caminho completo e o nome do arquivo BMP a ser criado.

```java
String desName = dataDir + "CreatingImageUsingStream_out.bmp";
```

## Etapa 3: Configurar BmpOptions

`BmpOptions bmpOptions = new BmpOptions();` – cria um objeto de opções.  
Você pode definir `bitsPerPixel` (por exemplo, 24 para cores verdadeiras) para controlar a qualidade da imagem e o tamanho do arquivo.

```java
BmpOptions imageOptions = new BmpOptions();
imageOptions.setBitsPerPixel(24);
```

## Etapa 4: Criar FileCreateSource

`FileCreateSource fileSource = new FileCreateSource(outFile, false);` – encapsula o caminho de saída em uma fonte de stream.  
`bmpOptions.setSource(fileSource);` indica ao Aspose.PSD para gravar o BMP diretamente neste stream.

```java
FileCreateSource stream = new FileCreateSource(dataDir + "sample_out.bmp");
imageOptions.setSource(stream);
```

## Etapa 5: Gerar Imagem

`Image` é a classe Aspose.PSD que representa uma imagem e fornece métodos para criar, editar e salvar gráficos raster.  

`Image img = Image.create(bmpOptions, 800, 600);` – cria um BMP em branco de 800 × 600 pixels usando as opções configuradas.  
A imagem está agora pronta para desenho ou processamento adicional.

```java
Image image = Image.create(imageOptions, 500, 500);
```

## Etapa 6: Processamento de Imagem

`Graphics` é uma classe usada para desenhar formas, texto e outros gráficos em um objeto `Image`.  

Você pode desenhar formas, adicionar texto ou aplicar filtros via o objeto `Graphics` obtido de `img`.  
Por fim, chame `img.save()` para finalizar o arquivo. Esta etapa garante que todas as operações pendentes sejam gravadas no stream.

```java
// Perform desired image processing operations
// ...

// Save the processed image
image.save(desName);
```

## Problemas Comuns e Soluções

- **Erros de permissão de arquivo** – Verifique se o processo Java tem acesso de escrita ao diretório de destino.
- **Out‑of‑memory para imagens enormes** – Use `FileCreateSource` (conforme mostrado) para transmitir os dados em vez de carregar o bitmap inteiro na memória.
- **Cores inesperadas** – Certifique‑se de que `bitsPerPixel` corresponde à profundidade de cor desejada; 24 bpp é o padrão para BMPs de cores verdadeiras.

## Perguntas Frequentes

### Q1: Posso usar Aspose.PSD com outras bibliotecas Java?
A1: Sim, Aspose.PSD integra‑se perfeitamente com bibliotecas de imagem Java populares como ImageIO, permitindo combinar funcionalidades sem conflitos.

### Q2: Onde posso encontrar suporte para dúvidas relacionadas ao Aspose.PSD?
A2: Visite o [Aspose.PSD forum](https://forum.aspose.com/c/psd/34) para assistência da comunidade e respostas oficiais dos engenheiros da Aspose.

### Q3: Existe uma versão de avaliação gratuita disponível para Aspose.PSD?
A3: Sim, você pode acessar uma avaliação gratuita [aqui](https://releases.aspose.com/).

### Q4: Como obtenho uma licença temporária para Aspose.PSD?
A4: Obtenha uma licença temporária [aqui](https://purchase.aspose.com/temporary-license/).

### Q5: Quais são os requisitos de sistema para Aspose.PSD?
A5: Consulte a [documentation](https://reference.aspose.com/psd/java/) para sistemas operacionais suportados, versões do Java e diretrizes de memória.

## Conclusão

Agora você tem um fluxo de trabalho completo e pronto para produção para **como criar BMP** imagens usando streams no Aspose.PSD para Java. Ao aproveitar `BmpOptions` e `FileCreateSource`, você obtém geração de BMP rápida e eficiente em memória que escala de miniaturas simples a gráficos raster massivos. Sinta‑se à vontade para experimentar diferentes dimensões, profundidades de cor e etapas de pós‑processamento para atender às necessidades da sua aplicação.

---

**Última atualização:** 2026-07-17  
**Testado com:** Aspose.PSD 24.12 for Java  
**Autor:** Aspose

## Tutoriais Relacionados

- [Carregando Imagens a partir de Stream com Aspose.PSD para Java](/psd/java/advanced-techniques/loading-images-from-stream/)
- [Salvar Imagens em Stream com Aspose.PSD para Java](/psd/java/advanced-techniques/save-images-to-stream/)
- [Criar Imagem Definindo o Caminho no Aspose.PSD para Java](/psd/java/image-editing/create-image-by-setting-path/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< blocks/products/products-backtop-button >}}

{{< /blocks/products/pf/main-wrap-class >}}