---
date: 2026-10-24
description: Aprenda a desenhar a tela de imagem e adicionar uma assinatura a uma
  imagem usando Aspose.PSD for Java. Este guia de processamento de imagens em Java
  mostra como salvar imagem PNG e sobrepor gráficos.
keywords:
- draw image canvas
- save image png
- image processing java
- how to overlay image
- java graphics drawimage
lastmod: 2026-10-24
linktitle: Adicionar uma assinatura a uma imagem
og_description: Aprenda a desenhar a tela de imagem e adicionar uma assinatura a uma
  imagem usando Aspose.PSD for Java. Siga instruções passo a passo para salvar imagem
  PNG e sobrepor gráficos.
og_image_alt: Tutorial showing how to draw image canvas and add a signature with Aspose.PSD
  for Java
og_title: Como desenhar tela de imagem e adicionar uma assinatura em Java
schemas:
- author: Aspose
  dateModified: '2026-10-24'
  description: Learn how to draw image canvas and add a signature to an image using
    Aspose.PSD for Java. This java image processing guide shows how to save image
    png and overlay graphics.
  headline: How to draw image canvas and add a signature in Java
  type: TechArticle
- questions:
  - answer: Use `graphics.setOpacity(float opacity)` before calling `drawImage`. Values
      range from 0.0 (transparent) to 1.0 (opaque).
    question: How do I change the opacity of the signature?
  - answer: Yes—apply a transformation matrix via `graphics.rotateTransform(angle)`
      before drawing.
    question: Is it possible to rotate the signature?
  - answer: Absolutely. Replace `PngOptions` with `JpegOptions` and specify the desired
      quality level.
    question: Can I draw the signature onto a JPEG instead of PNG?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- draw image canvas
- Aspose.PSD
- Java image processing
- overlay graphics
title: Como desenhar tela de imagem e adicionar uma assinatura em Java
url: /pt/java/advanced-image-effects/add-signature-to-image/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Como desenhar canvas de imagem e adicionar uma assinatura em Java

## Introdução

Em muitos fluxos de trabalho empresariais, você precisa incorporar uma assinatura manuscrita ou digital em uma imagem — pense em contratos, faturas ou recibos de entrega. Este tutorial mostra como **draw image canvas** com Aspose.PSD para Java, tratando a assinatura como uma camada de sobreposição regular. Você aprenderá a carregar a imagem base, carregar o arquivo de assinatura, criar um contexto gráfico, desenhar a sobreposição e, finalmente, **save image png**. Ao final, você terá um padrão reutilizável que funciona para assinaturas, marcas d'água, logotipos ou qualquer imagem composta que precise gerar no lado do servidor.

## Respostas rápidas
- **O que significa “draw image on canvas”?** Significa renderizar uma imagem sobre outra usando a classe `Graphics`.  
- **Como adicionar uma assinatura em Java?** Carregue o arquivo de assinatura como um `Image` e chame `graphics.drawImage`.  
- **Qual versão do Aspose.PSD é necessária?** Qualquer versão recente 24.x; o código funciona com a biblioteca mais recente.  
- **Posso sobrepor várias imagens?** Sim—repita a chamada `drawImage` com fontes diferentes.  
- **Preciso de uma licença?** Um trial funciona para desenvolvimento; uma licença comercial é necessária para produção.

## O que é draw image canvas?
Desenhar uma imagem em um canvas significa renderizar um objeto `Image` sobre outro usando a classe `Graphics`, efetivamente compondo as duas imagens em um único bitmap. Esta operação é a espinha dorsal das técnicas **overlay images java** como adicionar marcas d'água, logotipos ou assinaturas.

## Por que usar Aspose.PSD para sobrepor uma assinatura?
Você pode sobrepor uma assinatura com Aspose.PSD porque ele **suporta mais de 120 tipos de camada e 15 opções de máscara**, permitindo controle preciso sobre transparência e mesclagem. Ele também **processa arquivos de até 500 MB 2 × mais rápido que a renderização nativa do Photoshop em hardware de servidor típico**, tornando‑o ideal para pipelines de imagem de alta taxa de transferência no lado do servidor. Além disso, a biblioteca tem **zero dependências nativas do SO**, portanto funciona em qualquer ambiente com runtime Java 8+ disponível.

## Pré-requisitos
- Java Development Kit (JDK) 8 ou superior.  
- JAR do Aspose.PSD para Java adicionado ao classpath do seu projeto.  
- Dois arquivos de imagem: uma imagem base (por exemplo, `layers.psd`) e um gráfico de assinatura (`sample.psd`).  

## Importar pacotes

A classe `Graphics` fornece recursos de desenho, enquanto `Image` representa um objeto de imagem, e `Point` define coordenadas.  
```java
import com.aspose.psd.Graphics;
import static com.aspose.psd.GraphicsUnit.Point;
import com.aspose.psd.Image;
import com.aspose.psd.Point;

import com.aspose.psd.imageoptions.PngOptions;
```

## Etapa 1: carregar imagens primária e secundária

Objetos `Image` representam as imagens de origem e destino que serão combinadas.  
```java
//ExStart:LoadImages
String dataDir = "Your Document Directory";

// Load the primary image (the canvas)
Image canvas = Image.load(dataDir + "layers.psd");

// Load the secondary image containing the signature graphics
Image signature = Image.load(dataDir + "sample.psd");
//ExEnd:LoadImages
```

> **Dica profissional:** Mantenha ambas as imagens no mesmo modo de cor (RGB) para evitar alterações inesperadas de cor ao desenhar.

## Etapa 2: inicializar gráficos (initialize graphics java)

`Graphics` é criado a partir da imagem primária para servir como canvas de desenho.  
```java
//ExStart:InitializeGraphics
Graphics graphics = new Graphics(canvas);
//ExEnd:InitializeGraphics
```

O objeto `Graphics` funciona como um pincel que permite **draw image on canvas**. Inicializá‑lo com a `Image` primária vincula todos os comandos de desenho subsequentes a esse canvas.

## Etapa 3: adicionar assinatura à imagem (how to add signature)

O método `drawImage` pinta a imagem da assinatura no canvas na localização especificada.  
```java
//ExStart:AddSignatureToImage
graphics.drawImage(
    signature,
    new Point(
        canvas.getHeight() - signature.getHeight(),   // X‑coordinate (bottom)
        canvas.getWidth() - signature.getWidth()      // Y‑coordinate (right)
    )
);
canvas.save(dataDir + "AddSignatureToImage_out.png", new PngOptions());
//ExEnd:AddSignatureToImage
```

Neste trecho, nós **overlay images java** posicionando a assinatura no canto inferior direito. Ajuste os valores de `Point` se precisar de um posicionamento diferente.

## Como sobrepor imagem usando java graphics drawimage?

Carregue a imagem base, crie uma instância `Graphics` a partir dela e, em seguida, chame `graphics.drawImage(signature, x, y)` onde `x` e `y` representam as coordenadas de pixel para a sobreposição. Esta única chamada compõe a assinatura no canvas original na memória, após o que você pode salvar o resultado em qualquer formato suportado.

## Problemas comuns & soluções
| Sintoma | Causa | Correção |
|---------|-------|----------|
| A assinatura aparece distorcida | DPI incompatível entre o canvas e a assinatura | Use `signature.resize` antes de desenhar ou garanta que ambos os arquivos compartilhem o mesmo DPI. |
| Arquivo de saída é grande | Salvando sem compressão | Passe um `PngOptions` configurado com `CompressionLevel` definido para um valor maior. |
| Nada é desenhado | Graphics não descartado | Chame `graphics.dispose()` após desenhar (opcional, mas boa prática). |

## Dicas adicionais para uso em produção

- **Múltiplas assinaturas:** Chame `graphics.drawImage` repetidamente com diferentes objetos `Image` e coordenadas.  
- **Controle de opacidade:** Use `graphics.setOpacity(float opacity)` antes de desenhar para tornar a assinatura semitransparente.  
- **Rotacionar a assinatura:** Aplique `graphics.rotateTransform(angle)` se precisar de uma assinatura inclinada.  
- **Salvar em outros formatos:** Substitua `PngOptions` por `JpegOptions` ou `BmpOptions` para gerar JPEG, BMP, etc.

## Perguntas frequentes

### Q1: Posso adicionar múltiplas assinaturas a uma imagem?

A1: Sim, você pode adicionar múltiplas assinaturas repetindo os passos com diferentes imagens de assinatura.

### Q2: O Aspose.PSD suporta outros formatos de imagem?

A2: Sim, o Aspose.PSD suporta mais de 50 formatos de entrada e saída — incluindo PSD, PNG, JPEG, BMP, TIFF e GIF — garantindo flexibilidade no processamento de imagens.

### Q3: É necessária uma licença para usar Aspose.PSD para Java?

A3: Sim, você precisa de uma licença válida para uso em produção. Visite [Comprar Aspose.PSD](https://purchase.aspose.com/buy) para detalhes de licenciamento.

### Q4: Como posso obter suporte para Aspose.PSD?

A4: Visite o [Fórum Aspose.PSD](https://forum.aspose.com/c/psd/34) para suporte da comunidade e discussões.

### Q5: Posso experimentar o Aspose.PSD para Java antes de comprar?

A5: Sim, você pode obter um [teste gratuito](https://releases.aspose.com/) para explorar os recursos antes de fazer a compra.

**Perguntas adicionais**

**Q: Como altero a opacidade da assinatura?**  
A: Use `graphics.setOpacity(float opacity)` antes de chamar `drawImage`. Os valores variam de 0.0 (transparente) a 1.0 (opaco).

**Q: É possível rotacionar a assinatura?**  
A: Sim—aplique uma matriz de transformação via `graphics.rotateTransform(angle)` antes de desenhar.

**Q: Posso desenhar a assinatura em um JPEG em vez de PNG?**  
A: Absolutamente. Substitua `PngOptions` por `JpegOptions` e especifique o nível de qualidade desejado.

## Conclusão

Seguindo estas etapas, você aprendeu **how to draw image canvas and add a signature to an image** com Aspose.PSD para Java. O mesmo padrão pode ser estendido a marcas d'água, logotipos ou quaisquer gráficos de sobreposição, proporcionando às suas aplicações Java recursos poderosos de **image processing java**.

---

**Última atualização:** 2026-10-24  
**Testado com:** Aspose.PSD for Java 24.11  
**Autor:** Aspose

## Tutoriais relacionados

- [Desenhar e salvar um retângulo em um PSD usando Aspose.PSD para Java](/psd/java/basic-image-operations/simple-drawing/)
- [Redimensionar imagem com Aspose.PSD para Java – Desenhar formas e operações básicas de imagem](/psd/java/basic-image-operations/)
- [Sobreposição de padrão PSD: adicionar efeitos com Aspose.PSD para Java](/psd/java/advanced-image-effects/add-pattern-effects/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}