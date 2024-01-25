---
title: Adicione uma nova camada regular ao PSD com Aspose.PSD para Java
linktitle: Adicione uma nova camada regular ao PSD
second_title: API Java Aspose.PSD
description: Aprenda como adicionar uma nova camada regular a arquivos PSD usando Aspose.PSD para Java. Siga nosso guia passo a passo para uma manipulação perfeita de PSD.
type: docs
weight: 11
url: /pt/java/advanced-image-effects/add-new-regular-layer/
---
## Introdução

Bem-vindo a este tutorial abrangente sobre como usar Aspose.PSD para Java para adicionar uma nova camada regular a um arquivo PSD. Aspose.PSD é uma poderosa biblioteca Java que permite aos desenvolvedores manipular e trabalhar com arquivos PSD de forma eficiente. Neste tutorial, orientaremos você no processo de adição de uma nova camada regular a um arquivo PSD, fornecendo etapas detalhadas e exemplos de código.

## Pré-requisitos

Antes de mergulhar no tutorial, certifique-se de ter os seguintes pré-requisitos em vigor:

- Ambiente de Desenvolvimento Java: Certifique-se de ter um ambiente de desenvolvimento Java configurado em seu sistema.
-  Biblioteca Aspose.PSD: Baixe e instale a biblioteca Aspose.PSD para Java. Você pode encontrar a biblioteca[aqui](https://releases.aspose.com/psd/java/).

## Importar pacotes

Para começar, importe os pacotes necessários para o seu projeto Java. Esses pacotes são essenciais para trabalhar com as funcionalidades do Aspose.PSD. Inclua as seguintes linhas no início do seu arquivo Java:

```java
import com.aspose.psd.Image;
import com.aspose.psd.Rectangle;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.Layer;
import com.aspose.psd.imageoptions.PngOptions;
import com.aspose.psd.imageoptions.PsdOptions;
```

## Passo 1: Carregar arquivo PSD

Carregue o arquivo PSD que deseja editar usando o seguinte código:

```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "OneLayer.psd";
PsdImage im = (PsdImage)Image.load(sourceFileName);
```

## Etapa 2: preparar matrizes de dados e retângulos

Prepare dois arrays int e dois objetos Rectangle da seguinte forma:

```java
int[] data1 = new int[2500];
int[] data2 = new int[2500];
Rectangle rect1 = new Rectangle(0, 0, 50, 50);
Rectangle rect2 = new Rectangle(0, 0, 100, 25);
```

## Etapa 3: inicializar os dados da camada

Inicialize matrizes de dados com um valor padrão:

```java
for (int i = 0; i < 2500; i++) {
    data1[i] = -10000000;
    data2[i] = -10000000;
}
```

## Etapa 4: adicionar camadas regulares

Adicione duas camadas regulares à imagem PSD:

```java
Layer layer1 = im.addRegularLayer();
layer1.setLeft(25);
layer1.setTop(25);
layer1.setRight(75);
layer1.setBottom(75);
layer1.saveArgb32Pixels(rect1, data1);

Layer layer2 = im.addRegularLayer();
layer2.setLeft(25);
layer2.setTop(150);
layer2.setRight(1255);
layer2.setBottom(175);
layer2.saveArgb32Pixels(rect2, data2);
```

## Etapa 5: salve PSD e PNG

Salve o PSD modificado e um arquivo PNG adicional:

```java
im.save(exportPath, new PsdOptions());
im.save(exportPathPng, new PngOptions());
```

Parabéns! Você adicionou com sucesso uma nova camada regular a um arquivo PSD usando Aspose.PSD para Java.

## Conclusão

Neste tutorial, abordamos o processo de adição de uma nova camada regular a um arquivo PSD usando Aspose.PSD para Java. Esta poderosa biblioteca simplifica a manipulação do PSD, tornando-o acessível para desenvolvedores Java. Experimente diferentes parâmetros e funcionalidades para explorar todo o potencial do Aspose.PSD.

## Perguntas frequentes

### Q1: O Aspose.PSD é compatível com Java 8?

A1: Sim, Aspose.PSD oferece suporte a Java 8 e versões posteriores.

### Q2: Posso aplicar transformações às camadas adicionadas?

A2: Com certeza! Aspose.PSD oferece uma variedade de opções de transformação para camadas.

### Q3: Onde posso encontrar documentação adicional do Aspose.PSD?

 A3: Você pode consultar a documentação[aqui](https://reference.aspose.com/psd/java/).

### Q4: Como posso obter uma licença temporária para Aspose.PSD?

 A4: Visita[esse link](https://purchase.aspose.com/temporary-license/) para opções de licença temporária.

### Q5: Existe algum fórum da comunidade para suporte do Aspose.PSD?

 A5: Sim, você pode encontrar suporte e discussões[aqui](https://forum.aspose.com/c/psd/34).