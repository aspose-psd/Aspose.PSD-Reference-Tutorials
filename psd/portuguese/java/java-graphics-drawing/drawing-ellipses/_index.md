---
date: 2026-09-28
description: Aprenda a desenhar ellipse em Java usando Aspose.PSD, o principal tutorial
  de processamento de imagens Java para criar ellipses e outras formas.
keywords:
- how to draw ellipse
- draw shapes java
- java image processing tutorial
- create ellipse image
- draw ellipses java
lastmod: 2026-09-28
linktitle: Desenhando ellipses em Java
og_description: Aprenda a desenhar ellipse em Java usando Aspose.PSD, o principal
  tutorial de processamento de imagens Java que permite criar ellipses, desenhar formas
  e gerar imagens bitmap de forma eficiente.
og_image_alt: Guide showing how to draw an ellipse in Java with Aspose.PSD
og_title: Como desenhar ellipse em Java usando a biblioteca Aspose.PSD
schemas:
- author: Aspose
  dateModified: '2026-09-28'
  description: Learn how to draw ellipse in Java using Aspose.PSD, the leading Java
    image processing tutorial for creating ellipses and other shapes.
  headline: How to draw ellipse in Java using Aspose.PSD library
  type: TechArticle
- questions:
  - answer: Aspose.PSD offers a fully functional trial that lets you evaluate all
      features before purchasing a license.
    question: Can I use Aspose.PSD for free?
  - answer: Visit [Aspose.PSD Documentation](https://reference.aspose.com/psd/java/)
      for comprehensive guides, API references, and sample projects.
    question: Where can I find more examples and documentation?
  - answer: Temporary licenses are available through the Aspose portal at [Aspose.PSD
      Temporary License](https://purchase.aspose.com/temporary-license/).
    question: How do I obtain a temporary license for testing?
  - answer: It supports BMP, PNG, JPEG, TIFF, GIF, and native PSD among others.
    question: What image formats can Aspose.PSD export to?
  - answer: Yes, the library is designed for high‑throughput server environments and
      includes features such as multi‑threaded processing and memory‑efficient streaming.
    question: Is Aspose.PSD suitable for enterprise‑level workloads?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- draw ellipse
- Aspose.PSD
- Java graphics
- image processing
title: Como desenhar ellipse em Java usando a biblioteca Aspose.PSD
url: /pt/java/java-graphics-drawing/drawing-ellipses/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Como desenhar uma elipse em Java usando a biblioteca Aspose.PSD

## Introdução
Neste tutorial você aprenderá **como desenhar uma elipse** em Java com a biblioteca Aspose.PSD. Aspose.PSD for Java é uma API robusta que permite criar, editar e exportar arquivos PSD sem precisar do Adobe Photoshop. Desenhar formas como elipses é uma habilidade essencial para qualquer projeto de processamento de imagens em Java, e este guia o conduzirá por cada etapa — desde a configuração do projeto até a gravação do bitmap final.

## Respostas rápidas
- **Qual biblioteca é a melhor para desenhar elipses em Java?** Aspose.PSD for Java.
- **Quantas linhas de código são necessárias?** Cerca de dez linhas mais algumas instruções de configuração.
- **Preciso de uma licença para desenvolvimento?** Um teste gratuito funciona para testes; uma licença comercial é necessária para produção.
- **Posso exportar para BMP, PNG ou JPEG?** Sim, Aspose.PSD suporta BMP, PNG, JPEG e PSD.
- **A API é compatível com Java 8 e versões mais recentes?** Totalmente suportada no Java 8‑21.

## O que é Aspose.PSD para Java?
Aspose.PSD for Java é uma biblioteca pure‑Java que permite a criação, manipulação e conversão programática de arquivos Photoshop PSD. Ela suporta mais de 100 formatos de imagem e pode lidar com arquivos de até 2 GB sem carregar todo o documento na memória.

## Por que usar Aspose.PSD para desenhar elipses?
Aspose.PSD oferece alto desempenho, processando documentos multi‑página em segundos, enquanto suporta mais de 100 formatos de entrada e saída como BMP, PNG, JPEG e PSD. Ela opera totalmente em Java, eliminando a necessidade do Photoshop nativo e tornando‑a ideal para pipelines CI/CD e serviços baseados em nuvem.

## Pré-requisitos
- Conhecimento básico de programação Java.
- JDK 8 ou superior instalado.
- Uma IDE como IntelliJ IDEA ou Eclipse.
- Biblioteca Aspose.PSD for Java. Você pode baixá‑la na [Aspose.PSD for Java download page](https://releases.aspose.com/psd/java/).

## Importar pacotes
Primeiro, importe as classes que você precisará do namespace Aspose.PSD.

## Como desenhar uma elipse em Java?
Carregue a biblioteca Aspose.PSD, crie uma tela PsdImage em branco, obtenha um objeto Graphics, opcionalmente limpe o plano de fundo e, em seguida, use objetos Pen com as cores e estilos desejados para desenhar elipses dentro dos limites de um Rectangle. Por fim, salve a imagem nos formatos BMP, PNG ou JPEG. Esse processo normalmente requer menos de 15 linhas de código.

## Etapa 1: configurar seu projeto Java
Antes de começar a codificar, certifique‑se de que seu projeto inclua o JAR do Aspose.PSD como dependência Maven/Gradle ou adicione o JAR ao classpath.

## Etapa 2: criar uma instância de PsdImage
PsdImage representa um documento Photoshop em memória e fornece uma tela para desenho.

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

## Etapa 3: inicializar objeto graphics
Graphics fornece métodos de desenho para renderizar formas na superfície de uma imagem.

```java
Image image = new PsdImage(100, 100);
```

## Etapa 4: limpar a superfície graphics
Opcionalmente, limpe a tela com uma cor de fundo para garantir uma área de desenho limpa.

```java
Graphics graphics = new Graphics(image);
```

## Etapa 5: desenhar uma elipse pontilhada
Pen define a cor e o estilo do contorno usado ao desenhar formas.

```java
graphics.clear(Color.getYellow());
```

## Etapa 6: desenhar uma elipse contínua
Pen com um pincel azul sólido cria um contorno contínuo para a segunda elipse.

```java
graphics.drawEllipse(new Pen(Color.getRed()), new Rectangle(30, 10, 40, 80));
```

## Etapa 7: salvar a imagem
BmpOptions especifica as configurações de formato BMP para salvar a imagem.

```java
graphics.drawEllipse(new Pen(new SolidBrush(Color.getBlue())), new Rectangle(10, 30, 80, 40));
```

```java
String outputPath = "Your Document Directory/Ellipse.bmp";
BmpOptions saveOptions = new BmpOptions();
saveOptions.setBitsPerPixel(32);
image.save(outputPath, saveOptions);
```

## Problemas comuns e soluções
- **A imagem aparece em branco:** Certifique‑se de que chamou `graphics.clear()` com uma cor visível antes de desenhar.
- **A elipse parece distorcida:** Verifique se as dimensões do `Rectangle` correspondem à proporção da imagem.
- **Erros de falta de memória em arquivos grandes:** Use a API de streaming do `PsdImage` para processar seções do arquivo em vez de carregar todo o documento.

## Perguntas frequentes

**Q: Posso usar o Aspose.PSD gratuitamente?**  
A: Aspose.PSD oferece um teste totalmente funcional que permite avaliar todos os recursos antes de comprar uma licença.

**Q: Onde posso encontrar mais exemplos e documentação?**  
A: Visite [Aspose.PSD Documentation](https://reference.aspose.com/psd/java/) para guias abrangentes, referências de API e projetos de exemplo.

**Q: Como obtenho uma licença temporária para testes?**  
A: Licenças temporárias estão disponíveis através do portal Aspose em [Aspose.PSD Temporary License](https://purchase.aspose.com/temporary-license/).

**Q: Para quais formatos de imagem o Aspose.PSD pode exportar?**  
A: Ele suporta BMP, PNG, JPEG, TIFF, GIF e PSD nativo, entre outros.

**Q: O Aspose.PSD é adequado para cargas de trabalho de nível empresarial?**  
A: Sim, a biblioteca foi projetada para ambientes de servidor de alta taxa de transferência e inclui recursos como processamento multithread e streaming eficiente em memória.

## Conclusão
Agora você tem um exemplo completo, de ponta a ponta, de **como desenhar uma elipse** em Java usando o Aspose.PSD. Ao configurar um `PsdImage`, usar a API `Graphics` e configurar objetos `Pen`, você pode renderizar elipses pontilhadas e sólidas e salvar o resultado em qualquer um dos formatos de bitmap suportados. Integre essas etapas em suas próprias aplicações para gerar gráficos dinâmicos, miniaturas ou elementos de UI personalizados sem depender de editores gráficos externos.

---

**Última atualização:** 2026-09-28  
**Testado com:** Aspose.PSD for Java 24.12  
**Autor:** Aspose

## Tutoriais Relacionados

- [Desenhar e salvar um retângulo em um PSD usando Aspose.PSD for Java](/psd/java/basic-image-operations/simple-drawing/)
- [Redimensionar imagem com Aspose.PSD for Java – Desenhar formas e operações básicas de imagem](/psd/java/basic-image-operations/)
- [Adicionar assinatura à imagem – Desenhar imagem na tela com Aspose.PSD for Java](/psd/java/advanced-image-effects/add-signature-to-image/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}