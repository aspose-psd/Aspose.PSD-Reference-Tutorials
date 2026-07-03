---
date: 2026-07-03
description: Aprenda como recortar imagens em Java usando Aspose.PSD para Java. Este
  tutorial passo a passo de recorte de imagens cobre o carregamento de arquivos PSD,
  a definição de valores de deslocamento e a gravação do resultado.
keywords:
- crop image java
- how to crop image
- load psd file
- java image processing
- crop image left right
linktitle: Cortar Imagem por Deslocamentos
schemas:
- author: Aspose
  dateModified: '2026-07-03'
  description: Learn how to crop image java using Aspose.PSD for Java. This step‑by‑step
    image cropping tutorial covers loading PSD files, setting shift values, and saving
    the result.
  headline: Crop Image Java by Shifts with Aspose.PSD
  type: TechArticle
- description: Learn how to crop image java using Aspose.PSD for Java. This step‑by‑step
    image cropping tutorial covers loading PSD files, setting shift values, and saving
    the result.
  name: Crop Image Java by Shifts with Aspose.PSD
  steps:
  - name: Load the Image
    text: '`Image` is the base class for all image types in Aspose.PSD. `RasterImage`
      represents a raster image and provides cropping capabilities.'
  - name: Cache Image Data
    text: '`cacheData()` loads the image data into memory for faster processing.'
  - name: Define Shift Values
    text: Specify the shift values for all four sides of the image (left, top, right,
      bottom) in pixels.
  - name: Apply Cropping
    text: '`crop(left, right, top, bottom)` trims the image by the specified pixel
      shifts on each side.'
  - name: Save the Results
    text: '`JpegOptions` defines JPEG encoding settings such as quality and color
      profile. Congratulations! You''ve successfully cropped an image using Aspose.PSD
      for Java.'
  type: HowTo
- questions:
  - answer: Yes, Aspose.PSD supports over 30 raster formats, including PSD, JPEG,
      PNG, BMP, TIFF, and GIF, ensuring broad compatibility.
    question: Is Aspose.PSD compatible with all image formats?
  - answer: Absolutely. After each `crop` call you receive a new image object, which
      you can crop again as needed.
    question: Can I apply multiple cropping operations to the same image?
  - answer: Yes, you can find support and engage with the community at [Aspose.PSD
      Forum](https://forum.aspose.com/c/psd/34).
    question: Is there a community forum for Aspose.PSD support?
  - answer: Visit [here](https://purchase.aspose.com/temporary-license/) to obtain
      a temporary license.
    question: How can I obtain a temporary license for Aspose.PSD?
  - answer: Explore the documentation and examples at [Aspose.PSD Java Documentation](https://reference.aspose.com/psd/java/).
    question: Are there sample projects showcasing Aspose.PSD functionalities?
  type: FAQPage
second_title: Aspose.PSD Java API
title: Cortar Imagem Java por Deslocamentos com Aspose.PSD
url: /pt/java/image-editing/crop-image-by-shifts/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Recortar Imagem Java por Deslocamentos com Aspose.PSD

## Introdução

No processamento de imagens em Java, **crop image java** é uma necessidade comum para preparar gráficos, miniaturas ou recursos de UI. Aspose.PSD para Java torna essa tarefa simples ao expor um método `crop` fácil que funciona em qualquer formato raster suportado. Neste tutorial você aprenderá como carregar um arquivo PSD, definir valores de deslocamento esquerda‑direita‑topo‑base, aplicar o recorte e salvar o resultado — tudo sem escrever código personalizado de manipulação de pixels.

## Respostas Rápidas
- **Qual biblioteca lida com recorte?** Aspose.PSD para Java fornece um método `crop` embutido.  
- **Preciso de licença?** Uma licença temporária funciona para avaliação; uma licença completa é necessária para produção.  
- **Formatos suportados?** Mais de 30 formatos raster, incluindo PSD, JPEG, PNG, BMP e TIFF.  
- **Tamanho máximo de arquivo?** Lida com arquivos de até 2 GB sem carregar a imagem inteira na memória.  
- **Quantas linhas de código?** Apenas cinco etapas lógicas — carregar, cache, definir deslocamentos, recortar e salvar.

## O que é crop image java?
`crop image java` refere-se à operação de cortar um bitmap em uma aplicação Java. Usando Aspose.PSD, a operação é realizada pelo método `crop`, que aceita valores de deslocamento para cada lado da imagem e retorna uma nova instância de imagem.

## Por que usar Aspose.PSD para recorte de imagens?
Aspose.PSD suporta **30+** formatos de imagem e pode processar arquivos PSD com centenas de páginas enquanto usa menos de 150 MB de RAM, graças à sua arquitetura de carregamento preguiçoso. A biblioteca também garante resultados pixel‑perfeitos, preservando camadas, máscaras e perfis de cor — algo que muitas bibliotecas de imagem genéricas não podem assegurar.

## Pré-requisitos

### Kit de Desenvolvimento Java (JDK)

Certifique‑se de que você tem a versão mais recente do JDK instalada em seu sistema. Você pode baixá‑la [aqui](https://www.oracle.com/java/technologies/javase-downloads.html).

### Biblioteca Aspose.PSD para Java

Para começar, você precisará obter a biblioteca Aspose.PSD para Java. Acesse a [página de download](https://releases.aspose.com/psd/java/) e obtenha a versão mais recente.

### Ambiente de Desenvolvimento Integrado (IDE)

Escolha seu IDE Java favorito, como Eclipse ou IntelliJ, para uma experiência de codificação fluida.

## Como recortar imagem java?

Carregue seu arquivo fonte, defina os deslocamentos de pixel para cada lado e chame o método `crop` — todo esse fluxo pode ser escrito em cinco linhas concisas de código. A operação `crop` cria uma nova imagem que contém apenas a região especificada, deixando o arquivo original intacto.

### Etapa 1: Carregar a Imagem

`Image` é a classe base para todos os tipos de imagem no Aspose.PSD.  
`RasterImage` representa uma imagem raster e fornece recursos de recorte.  
```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.imageoptions.JpegOptions;
```

### Etapa 2: Cache dos Dados da Imagem

`cacheData()` carrega os dados da imagem na memória para processamento mais rápido.  
```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

// Load an existing image into an instance of RasterImage class
RasterImage rasterImage = (RasterImage)Image.load(sourceFile);
```

### Etapa 3: Definir Valores de Deslocamento

Especifique os valores de deslocamento para os quatro lados da imagem (esquerda, topo, direita, base) em pixels.  
```java
if (!rasterImage.isCached()) {
  rasterImage.cacheData();
}
```

### Etapa 4: Aplicar o Recorte

`crop(left, right, top, bottom)` corta a imagem pelos deslocamentos de pixel especificados em cada lado.  
```java
int leftShift = 10;
int rightShift = 10;
int topShift = 10;
int bottomShift = 10;
```

### Etapa 5: Salvar os Resultados

`JpegOptions` define as configurações de codificação JPEG, como qualidade e perfil de cor.  
```java
rasterImage.crop(leftShift, rightShift, topShift, bottomShift);
```

Parabéns! Você recortou uma imagem com sucesso usando Aspose.PSD para Java.

## Problemas Comuns e Soluções

- **A imagem parece inalterada:** Verifique se os valores de deslocamento são positivos e não excedem as dimensões originais.  
- **OutOfMemoryError em arquivos grandes:** Ative o cache conforme mostrado na Etapa 2; isso força o Aspose.PSD a usar um arquivo temporário em vez de manter a imagem inteira na RAM.  
- **Deslocamento de cor após o recorte:** Certifique‑se de preservar o perfil de cor chamando `image.save(..., new JpegOptions { ColorProfile = image.ColorProfile })` se precisar de fidelidade de cor exata.

## Perguntas Frequentes

**Q: O Aspose.PSD é compatível com todos os formatos de imagem?**  
A: Sim, Aspose.PSD suporta mais de 30 formatos raster, incluindo PSD, JPEG, PNG, BMP, TIFF e GIF, garantindo ampla compatibilidade.

**Q: Posso aplicar múltiplas operações de recorte na mesma imagem?**  
A: Absolutamente. Após cada chamada ao `crop` você recebe um novo objeto de imagem, que pode ser recortado novamente conforme necessário.

**Q: Existe um fórum da comunidade para suporte ao Aspose.PSD?**  
A: Sim, você pode encontrar suporte e interagir com a comunidade em [Aspose.PSD Forum](https://forum.aspose.com/c/psd/34).

**Q: Como posso obter uma licença temporária para Aspose.PSD?**  
A: Visite [aqui](https://purchase.aspose.com/temporary-license/) para obter uma licença temporária.

**Q: Existem projetos de exemplo que demonstram as funcionalidades do Aspose.PSD?**  
A: Explore a documentação e os exemplos em [Aspose.PSD Java Documentation](https://reference.aspose.com/psd/java/).

---

**Última Atualização:** 2026-07-03  
**Testado com:** Aspose.PSD 24.11 for Java  
**Autor:** Aspose  

{{< blocks/products/products-backtop-button >}}

```java
String destName = dataDir + "CroppingByShifts_out.jpg";
rasterImage.save(destName, new JpegOptions());
```

## Tutoriais Relacionados

- [Recortar Imagem por Retângulo no Aspose.PSD para Java](/psd/java/image-editing/crop-image-by-rectangle/)
- [Recortar Imagem Java - Expandir e Recortar Imagens com Aspose.PSD para Java](/psd/java/image-editing/expand-and-crop-images/)
- [Redimensionar Imagem Java - Usando Enumeração Resize Type no Aspose.PSD para Java](/psd/java/advanced-image-manipulation/resizing-with-resize-type-enumeration/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}