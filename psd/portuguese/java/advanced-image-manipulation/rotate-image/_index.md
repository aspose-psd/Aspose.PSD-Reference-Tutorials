---
date: 2026-05-19
description: Aprenda como converter PSD para JPEG e rotacionar a imagem 270 graus
  usando Aspose.PSD para Java. Este guia mostra como rotacionar arquivos PSD, inverter
  imagens e converter PSD para JPEG.
keywords:
- convert psd to jpeg
- how to rotate psd
- flip image java
- rotate psd layer
- rotate image without photoshop
linktitle: Rotacionar Imagem 270 Graus
schemas:
- author: Aspose
  dateModified: '2026-05-19'
  description: Learn how to convert PSD to JPEG and rotate image 270 degrees using
    Aspose.PSD for Java. This guide shows how to rotate PSD files, flip images, and
    convert PSD to JPEG.
  headline: Convert PSD to JPEG & Rotate 270° with Aspose.PSD for Java
  type: TechArticle
- description: Learn how to convert PSD to JPEG and rotate image 270 degrees using
    Aspose.PSD for Java. This guide shows how to rotate PSD files, flip images, and
    convert PSD to JPEG.
  name: Convert PSD to JPEG & Rotate 270° with Aspose.PSD for Java
  steps:
  - name: Load the PSD File
    text: '`Image` is Aspose.PSD''s core class that represents a single PSD document
      in memory. Instantiating it reads only the header information, keeping memory
      usage low.'
  - name: Rotate the Image 270 Degrees
    text: '`rotateFlip` performs the specified rotation and optional flip on the image.
      `RotateFlipType.Rotate270FlipNone` rotates the canvas 270 degrees clockwise
      while leaving the image orientation unchanged. > **Pro tip:** If you also need
      to flip the image horizontally or vertically, choose a different `Ro'
  - name: Convert PSD to JPEG and Save
    text: '`JpegOptions` defines JPEG‑specific parameters such as compression quality.
      The `save` method writes the transformed image to disk in the desired format.
      The file `RotatedImage_out.jpg` now contains the original PSD content rotated
      270 degrees and saved as a JPEG.'
  type: HowTo
- questions:
  - answer: Yes, Aspose.PSD supports PSD, JPEG, PNG, BMP, GIF, TIFF, and many other
      raster formats.
    question: Is Aspose.PSD compatible with different image formats?
  - answer: Absolutely! While `RotateFlipType` provides common angles, you can chain
      multiple calls or use transformation matrices for arbitrary angles.
    question: Can I apply custom rotations, not just predefined flips?
  - answer: Replace `JpegOptions` with `PngOptions` (or the appropriate options class)
      in the `save` method.
    question: How do I convert the rotated PSD to another format, such as PNG?
  - answer: For community help, visit the [Aspose.PSD Forum](https://forum.aspose.com/c/psd/34).
    question: Where can I find additional support or assistance?
  - answer: Yes, you can explore Aspose.PSD with a [free trial](https://releases.aspose.com/).
    question: Is there a free trial available?
  type: FAQPage
second_title: Aspose.PSD Java API
title: Converter PSD para JPEG e Rotacionar 270° com Aspose.PSD para Java
url: /pt/java/advanced-image-manipulation/rotate-image/
weight: 19
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Converter PSD para JPEG & Rotacionar Imagem 270 Graus com Aspose.PSD para Java

## Introdução

Neste **tutorial de processamento de imagens Java**, você aprenderá a **converter PSD para JPEG** enquanto rotaciona a imagem 270 graus usando Aspose.PSD para Java. Seja construindo um pipeline de processamento em lote, um editor baseado na web ou um utilitário de desktop, a biblioteca permite manipular camadas PSD sem o Photoshop. Também abordaremos a inversão opcional e mostraremos todo o fluxo de ponta a ponta, desde o carregamento de um arquivo PSD até a gravação de um JPEG.

## Respostas Rápidas
- **Qual biblioteca lida com a rotação?** Aspose.PSD para Java  
- **Qual ângulo de rotação o exemplo usa?** 270 graus  
- **Posso também inverter a imagem?** Sim – use as opções `RotateFlipType` como `Rotate90FlipX`  
- **Como salvo o resultado?** No exemplo salvamos como JPEG usando `JpegOptions`  
- **Preciso de licença para produção?** Uma licença válida do Aspose.PSD é necessária para uso comercial  

## O que é “rotacionar imagem 270 graus”?
Rotacionar uma imagem 270 graus significa girar a foto três quartos de uma volta completa no sentido horário (ou 90 graus no sentido anti‑horário). Essa orientação costuma restaurar o layout original de retrato após transformações anteriores e é comumente usada quando as imagens foram capturadas em modo paisagem, mas precisam ser exibidas em retrato. O resultado é uma visualização corretamente orientada sem perda de qualidade.

## Por que usar Aspose.PSD para esta tarefa?
Aspose.PSD suporta **mais de 50 formatos de entrada e saída** — incluindo PSD, JPEG, PNG, BMP, GIF e TIFF — e pode processar arquivos de até **2 GB** sem carregar o documento inteiro na memória. A API funciona em qualquer runtime Java (JDK 8+), não requer instalação nativa do Photoshop e oferece uma única chamada `rotateFlip` que trata rotação e inversão em um passo.

## Pré-requisitos

Antes de começar, certifique‑se de que você tem:

- Biblioteca **Aspose.PSD para Java** instalada. Você pode baixá‑la e visualizar a referência completa da API [aqui](https://reference.aspose.com/psd/java/).  
- Um ambiente de desenvolvimento Java (JDK 8 ou superior).  
- Um arquivo PSD de exemplo que você deseja rotacionar. Atualize a variável `sourceFile` no código com o caminho correto para seu arquivo.

## Importar Pacotes

As classes `Image`, `RotateFlipType` e `JpegOptions` são necessárias para carregar, transformar e salvar o arquivo.  
`Image` é a classe central que representa um documento PSD na memória.  
`RotateFlipType` enumera as operações de rotação e inversão suportadas.  
`JpegOptions` configura as opções de saída JPEG, como qualidade.  

```java
import com.aspose.psd.Image;
import com.aspose.psd.RotateFlipType;

import com.aspose.psd.imageoptions.JpegOptions;
```

## Como Converter PSD para JPEG após rotacionar?

Carregue o PSD de origem, aplique uma rotação de 270 graus e salve imediatamente como JPEG. Esse fluxo de três etapas é executado em menos de um segundo para imagens típicas de 10 MP em uma CPU moderna, tornando‑o ideal para trabalhos em lote de alta taxa. Processando apenas os dados de imagem necessários, o consumo de memória permanece baixo, e o JPEG resultante mantém a fidelidade visual enquanto reduz o tamanho do arquivo.

### Passo 1: Carregar o Arquivo PSD

`Image` é a classe principal do Aspose.PSD que representa um único documento PSD na memória. Instanciá‑la lê apenas as informações de cabeçalho, mantendo o uso de memória baixo.

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";
Image image = Image.load(sourceFile);
```

### Passo 2: Rotacionar a Imagem 270 Graus

`rotateFlip` executa a rotação especificada e a inversão opcional na imagem. `RotateFlipType.Rotate270FlipNone` gira a tela 270 graus no sentido horário, mantendo a orientação da imagem inalterada.

```java
image.rotateFlip(RotateFlipType.Rotate270FlipNone);
```

> **Dica profissional:** Se também precisar inverter a imagem horizontal ou verticalmente, escolha um `RotateFlipType` diferente, como `Rotate90FlipX` ou `Rotate180FlipY`.

### Passo 3: Converter PSD para JPEG e Salvar

`JpegOptions` define parâmetros específicos do JPEG, como qualidade de compressão. O método `save` grava a imagem transformada no disco no formato desejado.

```java
String destName = dataDir + "RotatedImage_out.jpg";
image.save(destName, new JpegOptions());
```

O arquivo `RotatedImage_out.jpg` agora contém o conteúdo original do PSD rotacionado 270 graus e salvo como JPEG.

## Problemas Comuns e Soluções

| Problema | Solução |
|----------|---------|
| **A imagem aparece de cabeça para baixo** | Verifique se você usou `Rotate270FlipNone`. Para uma rotação de 90 graus no sentido horário, use `Rotate90FlipNone`. |
| **Arquivo de saída está corrompido** | Certifique‑se de que a pasta de destino existe e que você tem permissões de gravação. |
| **Exceção de licença** | Instale uma licença temporária ou permanente do Aspose.PSD antes de carregar a imagem em produção. |

## Perguntas Frequentes

**Q:** O Aspose.PSD é compatível com diferentes formatos de imagem?  
**A:** Sim, o Aspose.PSD suporta PSD, JPEG, PNG, BMP, GIF, TIFF e muitos outros formatos raster.

**Q:** Posso aplicar rotações personalizadas, não apenas inversões predefinidas?  
**A:** Absolutamente! Embora `RotateFlipType` forneça ângulos comuns, você pode encadear múltiplas chamadas ou usar matrizes de transformação para ângulos arbitrários.

**Q:** Como converto o PSD rotacionado para outro formato, como PNG?  
**A:** Substitua `JpegOptions` por `PngOptions` (ou a classe de opções apropriada) no método `save`.

**Q:** Onde posso encontrar suporte ou assistência adicional?  
**A:** Para ajuda da comunidade, visite o [Aspose.PSD Forum](https://forum.aspose.com/c/psd/34).

**Q:** Existe uma versão de avaliação gratuita disponível?  
**A:** Sim, você pode explorar o Aspose.PSD com um [teste gratuito](https://releases.aspose.com/).

**Q:** Como obtenho uma licença temporária?  
**A:** Se precisar de uma licença temporária, você pode obtê‑la [aqui](https://purchase.aspose.com/temporary-license/).

**Última atualização:** 2026-05-19  
**Testado com:** Aspose.PSD para Java 24.12  
**Autor:** Aspose  

{{< blocks/products/products-backtop-button >}}

## Tutoriais Relacionados

- [Converter PSD para Formatos de Imagem Raster com Aspose.PSD para Java](/psd/java/advanced-techniques/convert-psd-to-raster-formats/)
- [Converter PSD para PNG e Rotacionar Camadas em Arquivos PSD usando Java](/psd/java/advanced-psd-layer-features-effects/rotate-layers-psd-files/)
- [Como Rotacionar Imagem em Java com Aspose.PSD](/psd/java/advanced-image-manipulation/)

{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}