---
title: Crie metadados XMP com Aspose.PSD para Java
linktitle: Crie metadados XMP
second_title: API Java Aspose.PSD
description: Aprimore seus aplicativos Java com Aspose.PSD. Aprenda a criar metadados XMP sem esforço. Siga nosso guia passo a passo agora.
type: docs
weight: 12
url: /pt/java/image-editing/create-xmp-metadata/
---
## Introdução

No domínio do desenvolvimento Java, o gerenciamento e a manipulação de metadados de imagens são cruciais para vários aplicativos. Aspose.PSD para Java se destaca como uma ferramenta poderosa para lidar com arquivos PSD e, neste tutorial, nos aprofundaremos na criação de metadados XMP usando esta biblioteca robusta.

## Pré-requisitos

Antes de embarcarmos neste tutorial, certifique-se de ter os seguintes pré-requisitos em vigor:

- Ambiente de Desenvolvimento Java: Tenha o Java instalado em seu sistema e um conhecimento básico de programação Java.
-  Biblioteca Aspose.PSD: Baixe e configure a biblioteca Aspose.PSD para Java. Você pode encontrar a biblioteca e documentação detalhada[aqui](https://reference.aspose.com/psd/java/).
- Seu diretório de documentos: Defina o diretório onde seus arquivos de documentos são armazenados.

## Importar pacotes

Em seu projeto Java, importe os pacotes necessários para aproveitar as funcionalidades do Aspose.PSD:

```java
import com.aspose.psd.Rectangle;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.system.io.MemoryStream;
import com.aspose.psd.xmp.XmpHeaderPi;
import com.aspose.psd.xmp.XmpMeta;
import com.aspose.psd.xmp.XmpPacketWrapper;
import com.aspose.psd.xmp.XmpTrailerPi;
import com.aspose.psd.xmp.schemas.dublincore.DublinCorePackage;
import com.aspose.psd.xmp.schemas.photoshop.ColorMode;
import com.aspose.psd.xmp.schemas.photoshop.PhotoshopPackage;
```

## Etapa 1: especificar o tamanho da imagem

```java
//Especifique o tamanho da imagem definindo um retângulo
Rectangle rect = new Rectangle(0, 0, 100, 200);
```

## Etapa 2: crie uma nova imagem

```java
// Crie uma nova imagem para fins de amostra
PsdImage image = new PsdImage(rect.getWidth(), rect.getHeight());
```

## Etapa 3: criar cabeçalho XMP

```java
// Crie uma instância do XMP-Header
XmpHeaderPi xmpHeader = new XmpHeaderPi();
xmpHeader.setGuid("Your Document Directory");
```

## Etapa 4: criar um trailer XMP

```java
// Crie uma instância do Xmp-TrailerPi
XmpTrailerPi xmpTrailer = new XmpTrailerPi(true);
```

## Etapa 5: criar metadados XMP

```java
// Crie uma instância da classe XMPmeta para definir atributos diferentes
XmpMeta xmpMeta = new XmpMeta();
xmpMeta.addAttribute("Author", "Mr Smith");
xmpMeta.addAttribute("Description", "The fake metadata value");
```

## Etapa 6: Criar wrapper de pacote XMP

```java
// Crie uma instância do XmpPacketWrapper que contenha todos os metadados
XmpPacketWrapper xmpData = new XmpPacketWrapper(xmpHeader, xmpTrailer, xmpMeta);
```

## Etapa 7: definir atributos do Photoshop

```java
// Crie uma instância do pacote Photoshop e defina atributos do Photoshop
PhotoshopPackage photoshopPackage = new PhotoshopPackage();
photoshopPackage.setCity("London");
photoshopPackage.setCountry("England");
photoshopPackage.setColorMode(ColorMode.Rgb);
```

## Etapa 8: Adicionar pacote Photoshop aos metadados XMP

```java
// Adicione o pacote Photoshop aos metadados XMP
xmpData.addPackage(photoshopPackage);
```

## Etapa 9: definir atributos DublinCore

```java
// Crie uma instância do pacote DublinCore e defina os atributos DublinCore
DublinCorePackage dublinCorePackage = new DublinCorePackage();
dublinCorePackage.setAuthor("Charles Bukowski");
dublinCorePackage.setTitle("Confessions of a Man Insane Enough to Live With the Beasts");
dublinCorePackage.addValue("dc:movie", "Barfly");
```

## Etapa 10: Adicionar pacote DublinCore aos metadados XMP

```java
// Adicione o pacote DublinCore aos metadados XMP
xmpData.addPackage(dublinCorePackage);
```

## Etapa 11: atualize os metadados XMP na imagem

```java
//Atualizar metadados XMP na imagem
image.setXmpData(xmpData);
```

## Etapa 12: Salvar imagem

```java
// Salve a imagem no disco ou em um fluxo de memória
image.save("Your Document Directory" + "create_XMP_Metadata.psd");
```

## Conclusão

Parabéns! Você criou metadados XMP para uma imagem usando Aspose.PSD para Java. Este tutorial equipou você com as etapas essenciais para aprimorar e gerenciar metadados em seus aplicativos Java de maneira integrada.

## Perguntas frequentes

### Q1: O Aspose.PSD é compatível com diferentes formatos de imagem?

A1: Sim, Aspose.PSD suporta vários formatos de imagem, proporcionando versatilidade no manuseio de diferentes tipos de arquivos.

### Q2: Posso manipular metadados existentes usando Aspose.PSD?

A2: Com certeza, Aspose.PSD permite modificar e atualizar metadados existentes nas imagens.

### Q3: Há alguma limitação no tamanho da imagem que o Aspose.PSD pode suportar?

A3: O Aspose.PSD foi projetado para lidar com imagens de diversos tamanhos, garantindo escalabilidade para seus projetos.

### Q4: Existe uma versão de teste disponível para Aspose.PSD?

 A4: Sim, você pode explorar os recursos do Aspose.PSD obtendo uma avaliação gratuita.[aqui](https://releases.aspose.com/).

### P5: Onde posso buscar suporte para consultas relacionadas ao Aspose.PSD?

 A5: Para qualquer assistência ou dúvida, visite o[Fórum Aspose.PSD](https://forum.aspose.com/c/psd/34).