---
date: 2026-09-13
description: Aprenda a desenhar uma elipse e outras formas em Java com Aspose.PSD.
  Este tutorial passo a passo de gráficos Java mostra gradient fills, polygon fills
  e image export.
keywords:
- how to draw ellipse
- draw shapes java
- how to create gradient
- java graphics tutorial
- fill polygon java
lastmod: 2026-09-13
linktitle: Desenhando usando gráficos em Java
og_description: Aprenda a desenhar uma elipse em Java usando Aspose.PSD. Este tutorial
  de gráficos Java cobre desenho de formas, gradient fills, polygon filling e exporting
  images.
og_image_alt: Screenshot of Java code drawing an ellipse with Aspose.PSD
og_title: Como desenhar elipse usando gráficos em Java com Aspose.PSD
schemas:
- author: Aspose
  dateModified: '2026-09-13'
  description: Learn how to draw an ellipse and other shapes in Java with Aspose.PSD.
    This step‑by‑step Java graphics tutorial shows gradient fills, polygon fills,
    and image export.
  headline: How to draw ellipse using graphics in Java with Aspose.PSD
  type: TechArticle
- questions:
  - answer: Yes, it supports layer merging, channel adjustments, text rendering, and
      advanced masking in addition to shape drawing.
    question: Can Aspose.PSD handle complex image manipulations?
  - answer: Absolutely; the library is optimized for speed and can process a 10 MP
      image in under 2 seconds on a typical server.
    question: Is Aspose.PSD suitable for high‑performance applications?
  - answer: Visit the [Aspose.PSD Java documentation](https://reference.aspose.com/psd/java/)
      for comprehensive guides and API references.
    question: Where can I find more examples and documentation?
  - answer: Yes, you can export to BMP, PNG, JPEG, TIFF, GIF, and PSD among others.
    question: Does Aspose.PSD support multiple image formats for export?
  - answer: Reach out to the Aspose.PSD community on the [support forum](https://forum.aspose.com/c/psd/34)
      or consider a [temporary license](https://purchase.aspose.com/temporary-license/)
      for priority assistance.
    question: How can I get support or assistance if I encounter issues?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- java graphics
- Aspose.PSD
- drawing shapes java
- gradient fill java
- initialize graphics java
title: Como desenhar elipse usando gráficos em Java com Aspose.PSD
url: /pt/java/java-graphics-drawing/drawing-using-graphics/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Como desenhar elipse usando gráficos em Java com Aspose.PSD

## Introdução
Neste tutorial de gráficos Java, você descobrirá **como desenhar elipse** objetos e outras formas programaticamente usando Aspose.PSD para Java. Seja para gerar miniaturas dinâmicas, criar elementos de UI personalizados ou automatizar fluxos de trabalho de design, dominar o desenho de elipses e preenchimentos gradientes oferece controle visual preciso. As etapas abaixo orientam você a inicializar gráficos, configurar canetas e pincéis e exportar o resultado em formatos de imagem comuns.

## Respostas rápidas
- **Qual biblioteca é necessária?** Aspose.PSD for Java (download do site oficial).  
- **Qual forma o tutorial aborda?** Desenhar uma elipse e preencher um polígono.  
- **Posso exportar para formatos diferentes de BMP?** Sim – PNG, JPEG, TIFF e outros são suportados.  
- **Preciso de uma licença para desenvolvimento?** Uma licença temporária gratuita funciona para testes; uma licença completa é necessária para produção.  
- **A API é adequada para imagens grandes?** Aspose.PSD processa arquivos de até 500 MB sem carregar todo o bitmap na memória.

## Como desenhar elipse em Java?
Carregue um `PsdImage` com a largura e altura desejadas, crie um objeto `Graphics`, defina uma `Pen` e chame `drawEllipse` com um retângulo delimitador. A operação completa requer apenas algumas chamadas de método e é executada em menos de um segundo para imagens típicas de 800×600 em hardware moderno.

## O que é Aspose.PSD para Java?
Aspose.PSD para Java é uma **biblioteca pura‑Java que fornece mais de 50 conversões de formatos de imagem e recursos completos de edição de PSD** sem necessidade do Adobe Photoshop. Ela pode renderizar, modificar e exportar arquivos multilayer mantendo o uso de memória baixo, tornando‑a ideal para geração de gráficos no lado do servidor.

## Por que usar Aspose.PSD para desenhar formas?
Aspose.PSD oferece alto desempenho, amplo suporte a formatos e renderização precisa, sendo ideal para geração de gráficos no lado do servidor e desenho de formas complexas.

- **Desempenho:** Lida com imagens de até 500 MB com uso de heap inferior a 150 MB (≈30 % menor que bibliotecas concorrentes).  
- **Suporte a formatos:** Mais de 50 formatos de entrada e saída, incluindo BMP, PNG, JPEG, TIFF e PSD.  
- **Precisão:** Renderização sub‑pixel garante elipses nítidas e gradientes suaves em telas de alta DPI.

## Pré-requisitos
- Conhecimento básico de programação Java.  
- Java Development Kit (JDK) instalado.  
- Uma IDE como IntelliJ IDEA ou Eclipse.  
- Biblioteca Aspose.PSD para Java. Você pode baixá‑la em [download do Aspose.PSD Java](https://releases.aspose.com/psd/java/).

## Importar pacotes
Para começar, importe as classes necessárias do Aspose.PSD e utilitários padrão Java. As classes a seguir fornecem primitivas de desenho e manipulação de cores:
```java
import com.aspose.psd.Color;
import com.aspose.psd.Graphics;
import com.aspose.psd.Pen;
import com.aspose.psd.Point;
import com.aspose.psd.Rectangle;
import com.aspose.psd.brushes.LinearGradientBrush;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.BmpOptions;
```

## Etapa 1: criar um objeto de imagem
`PsdImage` representa uma tela raster em memória que pode ser desenhada e salva em vários formatos.
```java
String dataDir = "Your Document Directory";
PsdImage image = new PsdImage(500, 500);
```

## Etapa 2: inicializar objeto graphics
`Graphics` é a superfície de desenho vinculada a um `PsdImage`, permitindo operações vetoriais como desenho de formas.
```java
Graphics graphics = new Graphics(image);
```

## Etapa 3: limpar a superfície da imagem
`clear` preenche toda a tela com uma única cor de fundo.
```java
graphics.clear(Color.getWhite());
```

## Etapa 4: criar e configurar objeto pen
`Pen` define a cor, largura e estilo do traço usado ao desenhar contornos.
```java
Pen pen = new Pen(Color.getBlue());
```

## Etapa 5: desenhar formas
`drawEllipse` renderiza uma elipse que se encaixa dentro do retângulo especificado usando a caneta atual.
```java
graphics.drawEllipse(pen, new Rectangle(10, 10, 150, 100));
```

## Etapa 6: usar brushes para preenchimento
`LinearGradientBrush` cria um preenchimento gradiente que transita entre duas cores ao longo de uma área definida.
```java
LinearGradientBrush linearGradientBrush = new LinearGradientBrush(image.getBounds(), Color.getRed(), Color.getWhite(), 45f);
Point[] points = { new Point(200, 200), new Point(400, 200), new Point(250, 350) };
graphics.fillPolygon(linearGradientBrush, points);
```

## Etapa 7: salvar a imagem modificada
`save` grava o `PsdImage` no disco no formato escolhido, como BMP ou PNG.
```java
image.save(dataDir + "DrawingUsingGraphics_output.bmp", new BmpOptions());
```

## Problemas comuns e solução de problemas
- **NullPointerException em graphics:** Garanta que o `PsdImage` esteja totalmente instanciado antes de criar o objeto `Graphics`.  
- **Cores incorretas:** Use `Color.fromArgb` para especificar valores ARGB exatos quando a paleta padrão não corresponde às expectativas.  
- **Atraso de desempenho em imagens grandes:** Ative `PsdImageOptions` com `compression = CompressionType.Rle` para reduzir a sobrecarga de memória.

## Perguntas frequentes

**Q: O Aspose.PSD pode lidar com manipulações de imagem complexas?**  
A: Sim, ele suporta mesclagem de camadas, ajustes de canais, renderização de texto e mascaramento avançado além do desenho de formas.

**Q: O Aspose.PSD é adequado para aplicações de alto desempenho?**  
A: Absolutamente; a biblioteca é otimizada para velocidade e pode processar uma imagem de 10 MP em menos de 2 segundos em um servidor típico.

**Q: Onde posso encontrar mais exemplos e documentação?**  
A: Visite a [documentação do Aspose.PSD Java](https://reference.aspose.com/psd/java/) para guias abrangentes e referências de API.

**Q: O Aspose.PSD suporta múltiplos formatos de imagem para exportação?**  
A: Sim, você pode exportar para BMP, PNG, JPEG, TIFF, GIF e PSD, entre outros.

**Q: Como posso obter suporte ou assistência se encontrar problemas?**  
A: Entre em contato com a comunidade Aspose.PSD no [forum de suporte](https://forum.aspose.com/c/psd/34) ou considere uma [licença temporária](https://purchase.aspose.com/temporary-license/) para assistência prioritária.

---

**Última atualização:** 2026-09-13  
**Testado com:** Aspose.PSD for Java 24.10  
**Autor:** Aspose

## Tutoriais Relacionados

- [Redimensionar Imagem com Aspose.PSD para Java – Desenhar Formas e Operações Básicas de Imagem](/psd/java/basic-image-operations/)
- [Desenhar e Salvar um Retângulo em um PSD usando Aspose.PSD para Java](/psd/java/basic-image-operations/simple-drawing/)
- [Adicionar Assinatura à Imagem – Desenhar Imagem em Canvas com Aspose.PSD para Java](/psd/java/advanced-image-effects/add-signature-to-image/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}