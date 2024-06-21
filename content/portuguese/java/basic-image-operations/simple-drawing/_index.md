---
title: Execute desenhos simples com Aspose.PSD para Java
linktitle: Execute um desenho simples
second_title: API Java Aspose.PSD
description: Aprenda como desenhar formas em arquivos PSD usando Aspose.PSD para Java. Este guia passo a passo aborda a criação, adição de camadas e desenho com exemplos de código.
type: docs
weight: 10
url: /pt/java/basic-image-operations/simple-drawing/
---
## Introdução

Bem-vindo a este guia passo a passo sobre como realizar desenhos simples usando Aspose.PSD para Java! Neste tutorial, exploraremos os fundamentos da criação de um novo documento PSD, adicionando camadas e desenhando formas com cores diferentes. Aspose.PSD para Java é uma biblioteca poderosa que permite manipular arquivos PSD programaticamente, fornecendo ampla funcionalidade para tarefas de design gráfico.

## Pré-requisitos

Antes de mergulhar no tutorial, certifique-se de ter os seguintes pré-requisitos em vigor:

- Java Development Kit (JDK) instalado em sua máquina.
-  Aspose.PSD para biblioteca Java. Você pode baixá-lo no[Aspose.PSD para documentação Java](https://reference.aspose.com/psd/java/).

## Importar pacotes

Para começar, importe os pacotes necessários para o seu projeto Java. Inclua o seguinte código no início do seu arquivo Java:

```java
import com.aspose.psd.Color;
import com.aspose.psd.Graphics;
import com.aspose.psd.Pen;
import com.aspose.psd.Rectangle;
import com.aspose.psd.brushes.SolidBrush;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.Layer;
```

## Etapa 1: crie um novo documento

Vamos começar criando um novo documento PSD com largura e altura especificadas:

```java
//ExStart:CriarDocumento
String outputDir = "Your Document Directory";
String outPsdFilePath = outputDir + "output.psd";
int width = 100;
int height = 100;

PsdImage image = new PsdImage(width, height);
//ExEnd:CriarDocumento
```

## Etapa 2: adicionar uma camada

Agora, vamos adicionar uma camada ao documento usando o construtor sem argumentos:

```java
//ExStart: Adicionar camada
Layer layer = new Layer();
layer.setBottom(height);
layer.setRight(width);
image.addLayer(layer);
//ExEnd:AddLayer
```

## Etapa 3: desenhar formas

Nesta etapa, utilizaremos a classe Graphics para desenhar formas na camada criada:

### Desenhe um retângulo com cor amarela

```java
//ExStart:DrawRectangleAmarelo
Graphics graphic = new Graphics(layer);
graphic.clear(Color.getYellow());
//ExEnd:DrawRectangleYellow
```

### Desenhe um retângulo vermelho

```java
//ExStart:DrawRedRectangle
graphic.drawRectangle(new Pen(Color.getRed()), new Rectangle(30, 10, 40, 80));
//ExEnd:DrawRedRectangle
```

### Desenhe um retângulo azul

```java
//ExStart:DrawBlueRectangle
graphic.drawRectangle(new Pen(new SolidBrush(Color.getBlue())), new Rectangle(10, 30, 80, 40));
//ExEnd:DrawBlueRectangle
```

## Etapa 4: salve as alterações

Por fim, salve uma cópia do arquivo PSD carregado incluindo as alterações:

```java
//ExStart:Salvar alterações
image.save(outPsdFilePath);
//ExEnd:Salvar alterações
```

## Conclusão

Parabéns! Você executou desenhos simples com sucesso usando Aspose.PSD para Java. Este tutorial abordou a criação de um novo documento, adição de camadas e desenho de retângulos com cores diferentes. Sinta-se à vontade para explorar recursos mais avançados oferecidos pela biblioteca para suas necessidades de design gráfico.

## Perguntas frequentes

### Q1: Posso usar Aspose.PSD para Java para manipular arquivos PSD existentes?

A1: Sim, Aspose.PSD para Java oferece ampla funcionalidade para editar e manipular arquivos PSD existentes.

### P2: Onde posso encontrar suporte para Aspose.PSD para Java?

 A2: Você pode visitar o[Fórum Aspose.PSD para Java](https://forum.aspose.com/c/psd/34) para quaisquer dúvidas relacionadas ao suporte.

### Q3: Existe uma avaliação gratuita disponível para Aspose.PSD para Java?

 A3: Sim, você pode acessar a versão de avaliação gratuita.[aqui](https://releases.aspose.com/).

### Q4: Como posso adquirir uma licença do Aspose.PSD para Java?

 A4: Você pode comprar uma licença no[Página de compra do Aspose.PSD](https://purchase.aspose.com/buy).

### P5: As licenças temporárias estão disponíveis para Aspose.PSD para Java?

 A5: Sim, você pode obter uma licença temporária de[aqui](https://purchase.aspose.com/temporary-license/).