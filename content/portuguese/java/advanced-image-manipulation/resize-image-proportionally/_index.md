---
title: Redimensione a imagem proporcionalmente com Aspose.PSD para Java
linktitle: Redimensionar imagem proporcionalmente
second_title: API Java Aspose.PSD
description: Aprimore seus aplicativos Java com Aspose.PSD. Siga nosso guia para redimensionar imagens proporcionalmente e sem esforço. Aumente hoje mesmo seus recursos de manipulação de imagens.
type: docs
weight: 17
url: /pt/java/advanced-image-manipulation/resize-image-proportionally/
---
## Introdução

Bem-vindo ao nosso guia passo a passo sobre como redimensionar imagens proporcionalmente usando Aspose.PSD para Java. Se você deseja aprimorar seus aplicativos Java com recursos eficientes de redimensionamento de imagens, você veio ao lugar certo. Neste tutorial, orientaremos você no processo usando etapas claras e concisas.

## Pré-requisitos

Antes de mergulhar no tutorial, certifique-se de ter os seguintes pré-requisitos em vigor:

1. Ambiente Java: Certifique-se de ter o Java instalado em seu sistema.
2.  Biblioteca Aspose.PSD: Baixe e instale a biblioteca Aspose.PSD. Você pode encontrar os recursos necessários[aqui](https://releases.aspose.com/psd/java/).

## Importar pacotes

Depois de classificar seus pré-requisitos, importe os pacotes necessários para seu projeto Java. Certifique-se de que a biblioteca Aspose.PSD esteja referenciada corretamente em seu projeto.

```java
import com.aspose.psd.Image;

import com.aspose.psd.imageoptions.PngOptions;
```

## Etapa 1: carregar a imagem

Comece carregando a imagem que deseja redimensionar em seu aplicativo Java.

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

Image image = Image.load(sourceFile);

if (!image.isCached()) {
    image.cacheData();
}
```

## Etapa 2: especifique largura e altura

Determine a nova largura e altura da imagem redimensionada. Neste exemplo, redimensionaremos a imagem para metade de suas dimensões originais.

```java
int newWidth = image.getWidth() / 2;
image.resizeWidthProportionally(newWidth);

int newHeight = image.getHeight() / 2;
image.resizeHeightProportionally(newHeight);
```

## Etapa 3: salve a imagem redimensionada

Salve a imagem redimensionada no local desejado, especificando as opções de formato (PNG, neste caso).

```java
String destName = dataDir + "SimpleResizeImageProportionally_out.png";
image.save(destName, new PngOptions());
```

E aí está! Você redimensionou proporcionalmente uma imagem usando Aspose.PSD para Java.

## Conclusão

Neste tutorial, cobrimos as etapas essenciais para redimensionar imagens proporcionalmente usando a biblioteca Aspose.PSD para Java. Agora, você pode integrar facilmente essa funcionalidade em seus aplicativos Java para melhorar o manuseio de imagens.

## Perguntas frequentes

### Q1: O Aspose.PSD é compatível com todos os formatos de imagem?

 A1: Aspose.PSD suporta vários formatos de imagem, incluindo PSD, PNG, JPEG e muito mais. Verifica a[documentação](https://reference.aspose.com/psd/java/) para uma lista abrangente.

### Q2: Posso usar Aspose.PSD para projetos comerciais?

 A2: Sim, você pode. Visite a[página de compra](https://purchase.aspose.com/buy) para detalhes de licenciamento.

### P3: As licenças temporárias estão disponíveis para fins de teste?

 A3: Sim, você pode obter uma licença temporária.[aqui](https://purchase.aspose.com/temporary-license/) para avaliação.

### Q4: Onde posso encontrar suporte para Aspose.PSD?

 A4: Visite o[Fórum Aspose.PSD](https://forum.aspose.com/c/psd/34) para apoio e assistência comunitária.

### Q5: Como posso acessar a documentação do Aspose.PSD?

 A5: Consulte a documentação detalhada[aqui](https://reference.aspose.com/psd/java/).
`