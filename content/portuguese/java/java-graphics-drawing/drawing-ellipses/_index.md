---
title: Desenhando elipses em Java
linktitle: Desenhando elipses em Java
second_title: API Java Aspose.PSD
description: Aprenda como desenhar elipses em Java usando Aspose.PSD para design gráfico preciso e manipulação de imagens. Domine tutoriais passo a passo.
type: docs
weight: 15
url: /pt/java/java-graphics-drawing/drawing-ellipses/
---
## Introdução
Neste tutorial, você aprenderá como desenhar elipses usando Aspose.PSD para Java. Aspose.PSD é uma biblioteca poderosa que permite aos desenvolvedores Java trabalhar com arquivos PSD e manipular imagens com facilidade. Desenhar formas como elipses é uma tarefa fundamental no processamento de imagens e no design gráfico. Seguindo este guia, você ganhará experiência prática na criação de elipses programaticamente usando Aspose.PSD.
## Pré-requisitos
Antes de começar, certifique-se de ter o seguinte:
- Conhecimento básico de programação Java.
- JDK (Java Development Kit) instalado em seu sistema.
- Ambiente de desenvolvimento integrado (IDE), como IntelliJ IDEA ou Eclipse.
-  Aspose.PSD para biblioteca Java. Você pode baixá-lo em[aqui](https://releases.aspose.com/psd/java/).
## Importar pacotes
Primeiro, você precisa importar os pacotes necessários do Aspose.PSD:
```java
import com.aspose.psd.Color;
import com.aspose.psd.Graphics;
import com.aspose.psd.Image;
import com.aspose.psd.Pen;
import com.aspose.psd.Rectangle;
import com.aspose.psd.brushes.SolidBrush;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.BmpOptions;
```
## Etapa 1: configure seu projeto Java
Antes de começar a codificar, certifique-se de que seu projeto Java esteja configurado corretamente com Aspose.PSD incluído como dependência.
## Etapa 2: crie uma instância de PsdImage
Inicialize uma nova instância de PsdImage com largura e altura desejadas.
```java
Image image = new PsdImage(100, 100);
```
## Etapa 3: inicializar o objeto gráfico
Crie e inicialize uma instância de Graphics para trabalhar com a imagem.
```java
Graphics graphics = new Graphics(image);
```
## Passo 4: Limpe a superfície gráfica
Antes de desenhar, limpe a superfície gráfica com uma cor específica (opcional).
```java
graphics.clear(Color.getYellow());
```
## Etapa 5: desenhe uma elipse pontilhada
Use um objeto Pen com cor vermelha e desenhe uma elipse pontilhada dentro de um retângulo especificado.
```java
graphics.drawEllipse(new Pen(Color.getRed()), new Rectangle(30, 10, 40, 80));
```
## Etapa 6: desenhe uma elipse contínua
Crie um objeto Pen com um pincel azul sólido e desenhe uma elipse contínua dentro de outro retângulo.
```java
graphics.drawEllipse(new Pen(new SolidBrush(Color.getBlue())), new Rectangle(10, 30, 80, 40));
```
## Etapa 7: salve a imagem
Por fim, salve a imagem gerada em formato BMP em um caminho especificado.
```java
String outputPath = "Your Document Directory/Ellipse.bmp";
BmpOptions saveOptions = new BmpOptions();
saveOptions.setBitsPerPixel(32);
image.save(outputPath, saveOptions);
```

## Conclusão
Parabéns! Você aprendeu com sucesso como desenhar elipses programaticamente usando Aspose.PSD para Java. Este tutorial abordou a configuração do seu projeto, a inicialização de gráficos, o desenho de elipses contínuas e pontilhadas e o salvamento da imagem resultante. Agora você pode integrar essas técnicas em seus aplicativos Java para diversas tarefas de design gráfico e manipulação de imagens.
## Perguntas frequentes
### Posso usar o Aspose.PSD gratuitamente?
Aspose.PSD oferece uma versão de teste gratuita, permitindo avaliar seus recursos antes de comprar.
### Onde posso encontrar mais exemplos e documentação?
 Visita[Documentação Aspose.PSD](https://reference.aspose.com/psd/java/) para guias e exemplos completos.
### Como posso obter licenças temporárias para Aspose.PSD?
 Licenças temporárias podem ser obtidas em[Licença temporária Aspose.PSD](https://purchase.aspose.com/temporary-license/).
### Em quais formatos o Aspose.PSD pode salvar imagens?
Aspose.PSD suporta salvar imagens em vários formatos, incluindo BMP, PNG, JPEG e PSD.
### O Aspose.PSD é adequado para uso empresarial?
Sim, o Aspose.PSD foi projetado para tarefas de processamento de imagens de nível profissional e empresarial.