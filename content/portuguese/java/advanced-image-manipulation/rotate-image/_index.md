---
title: Girar uma imagem em Aspose.PSD para Java
linktitle: Girar uma imagem
second_title: API Java Aspose.PSD
description: Explore a rotação de imagens em Java sem esforço com Aspose.PSD. Gire, inverta e salve arquivos PSD facilmente.
type: docs
weight: 19
url: /pt/java/advanced-image-manipulation/rotate-image/
---
## Introdução

Aspose.PSD para Java fornece um poderoso conjunto de recursos para trabalhar com imagens, permitindo aos desenvolvedores manipular e processar arquivos PSD com eficiência. Neste tutorial, focaremos em uma tarefa específica: girar uma imagem. Esteja você criando um aplicativo de edição de fotos ou simplesmente precise ajustar a orientação de uma imagem, o Aspose.PSD torna o processo simples.

## Pré-requisitos

Antes de mergulhar no tutorial, certifique-se de ter os seguintes pré-requisitos em vigor:

-  Biblioteca Aspose.PSD para Java: Certifique-se de ter baixado e instalado a biblioteca Aspose.PSD para Java. Você pode encontrar a biblioteca e documentação detalhada[aqui](https://reference.aspose.com/psd/java/).

- Ambiente de desenvolvimento Java: certifique-se de ter um ambiente de desenvolvimento Java configurado em sua máquina.

-  Arquivo PSD de amostra: prepare um arquivo PSD de amostra que você deseja girar. Ajusta a`sourceFile` variável no código de exemplo com o caminho para seu arquivo PSD.

## Importar pacotes

Comece importando os pacotes necessários para aproveitar os recursos do Aspose.PSD:

```java
import com.aspose.psd.Image;
import com.aspose.psd.RotateFlipType;

import com.aspose.psd.imageoptions.JpegOptions;
```

## Etapa 1: carregar a imagem

 Carregue a imagem existente em uma instância do`Image` aula:

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";
Image image = Image.load(sourceFile);
```

## Etapa 2: girar a imagem

 Gire a imagem usando o`rotateFlip` método. Neste exemplo, giramos a imagem em 270 graus:

```java
image.rotateFlip(RotateFlipType.Rotate270FlipNone);
```

## Etapa 3: salve a imagem girada

 Salve a imagem girada usando o`save` método e especificando o formato de saída (JPEG, neste caso):

```java
String destName = dataDir + "RotatedImage_out.jpg";
image.save(destName, new JpegOptions());
```

## Conclusão

Parabéns! Você girou uma imagem com sucesso usando Aspose.PSD para Java. Esta biblioteca simples, mas poderosa, abre um mundo de possibilidades para manipulação de imagens em seus aplicativos Java.

## Perguntas frequentes

### Q1: O Aspose.PSD é compatível com diferentes formatos de imagem?

A1: Sim, Aspose.PSD suporta vários formatos de imagem, incluindo PSD, JPEG, PNG e muito mais.

### P2: Posso aplicar rotações personalizadas, não apenas inversões predefinidas?

A2: Com certeza! Aspose.PSD oferece flexibilidade para aplicar rotações personalizadas para atender aos seus requisitos específicos.

### P3: Onde posso encontrar suporte ou assistência adicional?

 A3: Para qualquer dúvida ou problema, visite o[Fórum Aspose.PSD](https://forum.aspose.com/c/psd/34) para apoio comunitário.

### Q4: Existe um teste gratuito disponível?

 A4: Sim, você pode explorar Aspose.PSD com um[teste grátis](https://releases.aspose.com/).

### P5: Como obtenho uma licença temporária?

 A5: Se precisar de uma licença temporária, você pode obter uma[aqui](https://purchase.aspose.com/temporary-license/).