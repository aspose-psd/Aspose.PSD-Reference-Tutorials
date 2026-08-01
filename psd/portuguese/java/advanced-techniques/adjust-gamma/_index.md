---
date: 2026-08-01
description: Aprenda a ajustar o gamma no processamento de imagens em Java com Aspose.PSD,
  converter PSD para TIFF e corrigir imagens desbotadas em um tutorial conciso.
keywords:
- how to adjust gamma
- fix washed out image
- java image processing
- convert psd to tiff
- server side image processing
lastmod: 2026-08-01
linktitle: Ajustar o Gamma de uma Imagem
og_description: Aprenda a ajustar o gamma no processamento de imagens em Java usando
  Aspose.PSD – uma biblioteca rápida, server‑side, que corrige imagens desbotadas
  e converte PSD para TIFF em apenas algumas linhas de código.
og_image_alt: 'Guide: Adjust gamma in Java images with Aspose.PSD, convert PSD to
  TIFF'
og_title: como ajustar gamma – processamento em Java com Aspose.PSD
schemas:
- author: Aspose
  dateModified: '2026-08-01'
  description: Learn how to adjust gamma in Java image processing with Aspose.PSD,
    convert PSD to TIFF, and fix washed‑out images in a concise tutorial.
  headline: How to Adjust Gamma in Java Image Processing with Aspose.PSD
  type: TechArticle
- description: Learn how to adjust gamma in Java image processing with Aspose.PSD,
    convert PSD to TIFF, and fix washed‑out images in a concise tutorial.
  name: How to Adjust Gamma in Java Image Processing with Aspose.PSD
  steps:
  - name: '**Java Development Environment** – Java 8 or later installed.'
    text: '**Java Development Environment** – Java 8 or later installed.'
  - name: '**Aspose.PSD Library** – Download and add the JAR to your project. See
      the official [documentation](https://reference.aspose.com/psd/java/).'
    text: '**Aspose.PSD Library** – Download and add the JAR to your project. See
      the official [documentation](https://reference.aspose.com/psd/java/).'
  - name: '**Sample Image** – A PSD file you want to process (e.g., `sample.psd`).'
    text: '**Sample Image** – A PSD file you want to process (e.g., `sample.psd`).'
  type: HowTo
- questions:
  - answer: Yes – the `adjustGamma` method accepts separate float values for red,
      green, and blue channels.
    question: Can I apply different gamma values to each colour channel?
  - answer: Absolutely. You can perform resizing, cropping, or colour corrections
      sequentially on the same `RasterImage` instance.
    question: Is it possible to chain multiple image adjustments before saving?
  - answer: Yes, each layer can be accessed and processed individually.
    question: Does Aspose.PSD support multi‑page PSD files?
  - answer: Aspose.PSD supports PNG, JPEG, BMP, and many other formats via their respective
      options classes.
    question: What format can I export to besides TIFF?
  - answer: Start with a moderate gamma (around 2.0) and preview the result; adjust
      downwards if the image looks too bright.
    question: How do I avoid a washed‑out image after gamma correction?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- adjust gamma
- Aspose.PSD
- Java image processing
- PSD to TIFF
- server side processing
title: Como Ajustar o Gamma no Processamento de Imagens em Java com Aspose.PSD
url: /pt/java/advanced-techniques/adjust-gamma/
weight: 23
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Como Ajustar Gamma no Processamento de Imagens Java com Aspose.PSD

## Introdução

Se você está trabalhando em **java image processing**, aprender **how to adjust gamma** é uma técnica fundamental para melhorar o brilho e o contraste sem perder detalhes. Neste tutorial, vamos percorrer como usar **Aspose.PSD for Java** para aplicar correção de gamma a um arquivo PSD, **convert PSD to TIFF**, e evitar uma **washed‑out image**. Você verá por que essa abordagem é rápida, confiável e perfeita para pipelines de **server‑side image processing**.

## Respostas Rápidas
- **O que a correção de gamma faz?** Ele remapeia os valores de luminância para tornar áreas escuras mais claras ou áreas claras mais escuras, preservando os detalhes gerais.  
- **Qual biblioteca lida com o processamento?** Aspose.PSD for Java fornece um método dedicado `adjustGamma` para imagens raster.  
- **Posso converter PSD para TIFF no mesmo fluxo?** Sim – após o ajuste de gamma, você pode salvar a imagem diretamente em TIFF usando `TiffOptions`.  
- **Preciso de uma licença para desenvolvimento?** Um teste gratuito funciona para testes; uma licença comercial é necessária para uso em produção.  
- **Qual versão do Java é suportada?** Aspose.PSD suporta Java 8 e posteriores.

## O que é Correção de Gamma em Java?

A correção de gamma altera a relação não linear entre os valores de pixel codificados e o brilho exibido. Ajustando a curva de gamma, você pode **fix washed out image** problemas ou melhorar detalhes nas sombras sem superexpor os realces. Ela funciona aplicando uma função de lei de potência a cada pixel, que clareia tons escuros e comprime os realces, resultando em uma aparência visual mais natural.

## Por que Usar Aspose.PSD para Correção de Gamma?

Aspose.PSD é uma **java image processing library** que abstrai as complexidades do formato PSD. Ela suporta o processamento de arquivos de até 2 GB, lida com mais de 50 formatos de imagem diferentes e fornece uma chamada simples `adjustGamma`, tornando-a ideal para **java gamma correction** e fluxos de trabalho **convert PSD to TIFF**.

## Pré-requisitos

1. **Java Development Environment** – Java 8 ou posterior instalado.  
2. **Aspose.PSD Library** – Baixe e adicione o JAR ao seu projeto. Veja a [documentation](https://reference.aspose.com/psd/java/).  
3. **Sample Image** – Um arquivo PSD que você deseja processar (por exemplo, `sample.psd`).  

## Importar Pacotes

Antes de começar, importe os namespaces essenciais que dão acesso ao manuseio raster e às opções de formato de arquivo.

## Etapa 1: Carregar a Imagem

A classe `RasterImage` representa os dados de pixel rasterizados de uma camada PSD na memória. Carregar a imagem uma vez e armazená‑la em cache reduz o consumo de memória para ajustes subsequentes.

## Etapa 2: Ajustar Gamma

Carregue seu PSD com `new RasterImage("sample.psd")` e chame `rasterImage.adjustGamma(2.0f)` — essa única linha aplica um gamma de 2.0 em todos os canais de cor, clareando sombras enquanto mantém os realces intactos. Você pode passar valores separados para vermelho, verde e azul se ajustes específicos de canal forem necessários.

## Etapa 3: Criar TiffOptions

`TiffOptions` permite controlar compressão, bits por amostra e outras configurações específicas do TIFF. Definir uma amostra de 8 bits (`{8,8,8}`) mantém o tamanho do arquivo TIFF razoável enquanto preserva a fidelidade de cor.

## Etapa 4: Salvar a Imagem Resultante

Chame `rasterImage.save("output.tif", tiffOptions)` para gravar a imagem processada no disco. Após salvar, você pode enviar o TIFF para sistemas downstream, como serviços de impressão ou APIs web.

## Casos de Uso Comuns

- **Automated graphics pipelines** – Ajuste gamma em tempo real antes de gerar miniaturas.  
- **Batch conversion tools** – Converta grandes arquivos PSD para TIFF enquanto normaliza o brilho.  
- **Web services** – Exponha um endpoint que recebe um PSD, aplica correção de gamma e retorna um TIFF para consumo do cliente.

## Problemas Comuns e Soluções

| Issue | Why it Happens | How to Fix |
|-------|----------------|------------|
| **A imagem aparece washed out** | Valor de gamma muito alto (por exemplo, > 2.5) | Reduza o fator gamma para um valor entre 1.8 e 2.2. |
| **`rasterImage.isCached()` returns false** | Imagem ainda não carregada na memória | Chame `rasterImage.cacheData()` antes de ajustar o gamma. |
| **O tamanho do arquivo TIFF é grande** | Bits por amostra definidos como 16‑bit | Use uma amostra de 8‑bit (`{8,8,8}`) como mostrado no exemplo. |

## Perguntas Frequentes

**Q: Posso aplicar valores de gamma diferentes para cada canal de cor?**  
A: Sim – o método `adjustGamma` aceita valores float separados para os canais vermelho, verde e azul.

**Q: É possível encadear múltiplos ajustes de imagem antes de salvar?**  
A: Absolutamente. Você pode realizar redimensionamento, recorte ou correções de cor sequencialmente na mesma instância `RasterImage`.

**Q: O Aspose.PSD suporta arquivos PSD multi‑page?**  
A: Sim, cada camada pode ser acessada e processada individualmente.

**Q: Em que formato posso exportar além de TIFF?**  
A: Aspose.PSD suporta PNG, JPEG, BMP e muitos outros formatos através de suas respectivas classes de opções.

**Q: Como evito uma imagem washed‑out após a correção de gamma?**  
A: Comece com um gamma moderado (cerca de 2.0) e pré-visualize o resultado; reduza se a imagem parecer muito clara.

## Conclusão

Parabéns! Você aprendeu com sucesso **how to adjust gamma** em um fluxo de trabalho de **java image processing**, converteu um PSD para TIFF e evitou armadilhas comuns como uma **washed‑out image**. Esse padrão oferece controle granular sobre brilho e contraste, tornando-o ideal para pipelines de gráficos automatizados, serviços web ou utilitários de desktop.

---

**Última atualização:** 2026-08-01  
**Testado com:** Aspose.PSD 24.11 for Java  
**Autor:** Aspose  

{{< blocks/products/products-backtop-button >}}

## Tutoriais Relacionados

- [Tutorial de Processamento de Imagens Java - Ajustar Brilho de uma Imagem com Aspose.PSD for Java](/psd/java/advanced-techniques/adjust-brightness/)
- [Como Converter PSD para TIFF e Ajustar Contraste com Aspose.PSD for Java](/psd/java/advanced-techniques/adjust-contrast/)
- [Converter PSD para Imagem em Java – Aplicar Camadas de Ajuste com Aspose.PSD](/psd/java/advanced-psd-layer-features-effects/apply-adjustment-layers-psd-files/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.psd.fileformats.tiff.enums.TiffPhotometrics;
import com.aspose.psd.imageoptions.TiffOptions;
```

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

// Load an existing image into an instance of RasterImage class
Image image = Image.load(sourceFile);

// Cast object of Image to RasterImage
RasterImage rasterImage = (RasterImage)image;

// Check if RasterImage is cached for better performance
if (!rasterImage.isCached()) {
    rasterImage.cacheData();
}
```

```java
// Adjust the gamma
rasterImage.adjustGamma(2.2f, 2.2f, 2.2f);
```

```java
// Create an instance of TiffOptions for the resultant image
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
int[] ushort = { 8, 8, 8 };
tiffOptions.setBitsPerSample(ushort);
tiffOptions.setPhotometric(TiffPhotometrics.Rgb);
```

```java
// Save the resultant image to TIFF format
String destName = dataDir + "AdjustGamma_out.tiff";
rasterImage.save(destName, tiffOptions);
```