---
date: 2026-04-28
description: Aprenda como adicionar assinatura a uma imagem desenhando uma imagem
  na tela com Aspose.PSD para Java. Este tutorial de processamento de imagens em Java
  mostra como salvar a imagem como PNG e sobrepor gráficos.
keywords:
- add signature to image
- draw image on canvas
- save image as png
- java image processing
- add watermark java
linktitle: Adicionar uma assinatura a uma imagem
second_title: Aspose.PSD Java API
title: Adicionar assinatura à imagem – desenhar imagem no canvas com Aspose.PSD para
  Java
url: /pt/java/advanced-image-effects/add-signature-to-image/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Adicionar Assinatura à Imagem – Desenhar Imagem na Tela com Aspose.PSD para Java

## Introdução

Adicionar uma assinatura manuscrita ou digital **add signature to image** é uma necessidade comum para contratos, faturas ou qualquer documento que precise de prova de autenticidade. Neste tutorial você verá como o Aspose.PSD para Java permite **draw image on canvas** e tratar a assinatura como apenas mais uma camada de sobreposição. Vamos percorrer o carregamento da imagem base, o carregamento do arquivo de assinatura, a inicialização de um contexto gráfico, o desenho da sobreposição e, finalmente, **save image as PNG**. Ao final, você terá um padrão reutilizável para qualquer cenário de **java image processing**, seja uma assinatura, marca d'água ou logotipo.

## Respostas Rápidas
- **What does “draw image on canvas” mean?** Refere‑se à renderização de uma imagem sobre outra usando a classe `Graphics`.  
- **How to add a signature in Java?** Carregue o arquivo de assinatura como um `Image` e use `Graphics.drawImage`.  
- **Which Aspose.PSD version is required?** Qualquer versão recente 24.x; o código funciona com a biblioteca mais recente.  
- **Can I overlay multiple images?** Sim—repita a chamada `drawImage` com fontes diferentes.  
- **Do I need a license?** Um trial funciona para desenvolvimento; uma licença comercial é necessária para produção.

## O Que É “Draw Image on Canvas”?
Na terminologia do Aspose.PSD, desenhar uma imagem na tela significa pintar um objeto `Image` sobre outro usando um contexto `Graphics`. Essa operação é a espinha dorsal das técnicas de **overlay images java**, como adicionar marcas d'água, logotipos ou assinaturas.

## Por Que Usar Aspose.PSD para Sobrepor uma Assinatura?
- **Full PSD support** – funciona com camadas, máscaras e transparência.  
- **No native OS dependencies** – Java puro, perfeito para processamento no lado do servidor.  
- **High‑performance rendering** – otimizado para arquivos grandes e composições complexas.  

## Pré-requisitos
- Java Development Kit (JDK) 8 ou superior.  
- Aspose.PSD for Java JAR adicionado ao classpath do seu projeto.  
- Dois arquivos de imagem: uma imagem base (por exemplo, `layers.psd`) e um gráfico de assinatura (`sample.psd`).  

## Importar Pacotes

```java
import com.aspose.psd.Graphics;
import static com.aspose.psd.GraphicsUnit.Point;
import com.aspose.psd.Image;
import com.aspose.psd.Point;

import com.aspose.psd.imageoptions.PngOptions;
```

## Etapa 1: Carregar Imagens Primária e Secundária

```java
//ExStart:LoadImages
String dataDir = "Your Document Directory";

// Load the primary image (the canvas)
Image canvas = Image.load(dataDir + "layers.psd");

// Load the secondary image containing the signature graphics
Image signature = Image.load(dataDir + "sample.psd");
//ExEnd:LoadImages
```

> **Pro tip:** Mantenha ambas as imagens no mesmo modo de cor (RGB) para evitar alterações inesperadas de cor ao desenhar.

## Etapa 2: Inicializar Graphics (initialize graphics java)

```java
//ExStart:InitializeGraphics
Graphics graphics = new Graphics(canvas);
//ExEnd:InitializeGraphics
```

O objeto `Graphics` funciona como um pincel que permite **draw image on canvas**. Inicializá‑lo com a `Image` primária vincula todos os comandos de desenho subsequentes a essa tela.

## Etapa 3: Adicionar Assinatura à Imagem (how to add signature)

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

Neste trecho, **overlay images java** é realizado posicionando a assinatura no canto inferior direito. Ajuste os valores de `Point` se precisar de um posicionamento diferente.

## Problemas Comuns & Soluções
| Sintoma | Causa | Correção |
|---------|-------|----------|
| A assinatura aparece distorcida | DPI incompatível entre a tela e a assinatura | Use `signature.resize` antes de desenhar ou garanta que ambos os arquivos compartilhem o mesmo DPI. |
| O arquivo de saída é enorme | Salvamento sem compressão | Passe um `PngOptions` configurado com `CompressionLevel` definido para um valor mais alto. |
| Nada é desenhado | Graphics não foi descartado | Chame `graphics.dispose()` após o desenho (opcional, mas boa prática). |

## Dicas Adicionais para Uso no Mundo Real

- **Multiple signatures:** Chame `graphics.drawImage` repetidamente com diferentes objetos `Image` e coordenadas.  
- **Opacity control:** Use `graphics.setOpacity(float opacity)` antes de desenhar para tornar a assinatura semi‑transparente.  
- **Rotating the signature:** Aplique `graphics.rotateTransform(angle)` se precisar de uma assinatura inclinada.  
- **Saving to other formats:** Substitua `PngOptions` por `JpegOptions` ou `BmpOptions` para gerar JPEG, BMP, etc.

## Perguntas Frequentes

### Q1: Can I add multiple signatures to an image?

A1: Sim, você pode adicionar múltiplas assinaturas repetindo as etapas com diferentes imagens de assinatura.

### Q2: Does Aspose.PSD support other image formats?

A2: Sim, o Aspose.PSD suporta uma ampla variedade de formatos de imagem, garantindo flexibilidade no processamento de imagens.

### Q3: Is a license required for using Aspose.PSD for Java?

A3: Sim, você precisa de uma licença válida para usar o Aspose.PSD. Visite [Purchase Aspose.PSD](https://purchase.aspose.com/buy) para detalhes de licenciamento.

### Q4: How can I get support for Aspose.PSD?

A4: Visite o [Aspose.PSD Forum](https://forum.aspose.com/c/psd/34) para suporte da comunidade e discussões.

### Q5: Can I try Aspose.PSD for Java before purchasing?

A5: Sim, você pode obter um [free trial](https://releases.aspose.com/) para explorar os recursos antes de efetuar a compra.

**Additional FAQs**

**Q: How do I change the opacity of the signature?**  
A: Use `graphics.setOpacity(float opacity)` antes de chamar `drawImage`. Os valores variam de 0.0 (transparente) a 1.0 (opaco).

**Q: Is it possible to rotate the signature?**  
A: Sim—aplique uma matriz de transformação via `graphics.rotateTransform(angle)` antes de desenhar.

**Q: Can I draw the signature onto a JPEG instead of PNG?**  
A: Absolutamente. Substitua `PngOptions` por `JpegOptions` e especifique o nível de qualidade desejado.

## Conclusão

Seguindo estas etapas, você aprendeu **how to add signature to image** ao **draw image on canvas** com Aspose.PSD para Java. O mesmo padrão pode ser estendido a marcas d'água, logotipos ou quaisquer gráficos de sobreposição, proporcionando às suas aplicações Java poderosas capacidades de **java image processing**.

---

**Last Updated:** 2026-04-28  
**Tested With:** Aspose.PSD for Java 24.11  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}