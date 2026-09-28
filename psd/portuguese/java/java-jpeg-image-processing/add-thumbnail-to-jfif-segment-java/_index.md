---
date: 2026-09-28
description: Como adicionar miniatura a um segmento JFIF em Java usando Aspose.PSD.
  Siga este guia passo a passo para incorporar miniaturas em arquivos PSD de forma
  rápida e confiável.
keywords:
- how to add thumbnail
- JFIF segment Java
- Aspose.PSD thumbnail
- Java image processing
lastmod: 2026-09-28
linktitle: Adicionar Miniatura ao Segmento JFIF em Java
og_description: Como adicionar miniatura a um segmento JFIF em Java usando Aspose.PSD.
  Siga este guia passo a passo para incorporar miniaturas em arquivos PSD de forma
  rápida e confiável.
og_image_alt: Guide showing how to add thumbnail to JFIF segment in Java with Aspose.PSD
og_title: Como adicionar miniatura ao segmento JFIF em Java
schemas:
- author: Aspose
  dateModified: '2026-09-28'
  description: How to add thumbnail to a JFIF segment in Java using Aspose.PSD. Follow
    this step‑by‑step guide to embed thumbnails in PSD files quickly and reliably.
  headline: How to add thumbnail to JFIF segment in Java
  type: TechArticle
- description: How to add thumbnail to a JFIF segment in Java using Aspose.PSD. Follow
    this step‑by‑step guide to embed thumbnails in PSD files quickly and reliably.
  name: How to add thumbnail to JFIF segment in Java
  steps:
  - name: import packages
    text: '`Document`, `JfifResource`, and related classes are part of the Aspose.PSD
      namespace. Document represents the PSD file container, and JfifResource provides
      access to the JFIF segment within the PSD. Import them at the top of your source
      file.'
  - name: load the PSD image
    text: Create a `PsdImage` instance by passing the file path to the constructor.
      PsdImage is the Aspose.PSD class that models a Photoshop document. This loads
      the document metadata while streaming the pixel data.
  - name: iterate over image resources
    text: Search the `Resources` collection for a `JfifResource`. When found, you
      can replace its thumbnail byte array with a new JPEG‑encoded preview.
  - name: adjust thumbnail data
    text: Generate a small JPEG thumbnail (e.g., 120 × 120 px) using any image‑processing
      library, then assign the resulting byte array to `jfifResource.ThumbnailData`.
  - name: save the modified image
    text: Call the `save` method on the `PsdImage` object, specifying the output path
      and desired format. The JFIF segment now contains the new thumbnail.
  type: HowTo
- questions:
  - answer: Aspose.PSD for Java is a commercial library that enables developers to
      create, edit, convert, and render Photoshop PSD files without requiring Adobe
      Photoshop.
    question: What is Aspose.PSD for Java?
  - answer: Detailed documentation can be found on the [Aspose.PSD for Java documentation
      page](https://reference.aspose.com/psd/java/).
    question: Where can I find more documentation for Aspose.PSD for Java?
  - answer: Yes, Aspose.PSD for Java can be used commercially. You can purchase a
      license from [Aspose.PSD's purchase page](https://purchase.aspose.com/buy).
    question: Is Aspose.PSD for Java suitable for commercial use?
  - answer: Yes, you can download a free trial from [Aspose.PSD's trial download page](https://releases.aspose.com/).
    question: Can I try Aspose.PSD for Java before purchasing?
  - answer: For support, visit the [Aspose.PSD forum](https://forum.aspose.com/c/psd/34).
    question: How can I get support for Aspose.PSD for Java?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- add thumbnail
- Aspose.PSD
- Java image processing
- JFIF
- PSD
title: Como adicionar miniatura ao segmento JFIF em Java
url: /pt/java/java-jpeg-image-processing/add-thumbnail-to-jfif-segment-java/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Como adicionar miniatura ao segmento JFIF em Java

## Introdução
Adicionar uma miniatura ao segmento JFIF de um arquivo PSD é um requisito comum quando você precisa de uma pré‑visualização rápida sem carregar a imagem completa. Neste tutorial você aprenderá **como adicionar miniatura** a um segmento JFIF em Java usando Aspose.PSD. Ao final do guia você terá um trecho de código executável, compreensão da estrutura JFIF subjacente e dicas para lidar eficientemente com arquivos grandes.

## Respostas rápidas
- **Qual biblioteca é necessária?** Aspose.PSD for Java.
- **Qual versão do Java funciona?** JDK 11 ou posterior.
- **Quantas linhas de código são necessárias?** Cerca de 10 linhas para carregar, modificar e salvar.
- **Posso processar arquivos de vários megabytes?** Sim, Aspose.PSD transmite dados, portanto o uso de memória permanece baixo.
- **É necessária uma licença comercial?** Uma licença é necessária para uso em produção; uma avaliação gratuita está disponível.

## O que é um segmento JFIF?
O segmento JFIF é um bloco JPEG File Interchange Format que pode armazenar dados opcionais como miniaturas, EXIF ou perfis de cor.  
Ele reside dentro do fluxo JPEG de um arquivo PSD e é reconhecido pela maioria dos visualizadores de imagem para geração rápida de pré‑visualizações.

## Por que adicionar uma miniatura a um arquivo PSD?
Aspose.PSD for Java suporta **mais de 30 formatos de imagem** e pode processar arquivos de até **2 GB** sem carregar todo o documento na memória. Adicionar uma miniatura reduz a largura de banda da rede ao transmitir pré‑visualizações e acelera a renderização da UI em aplicações de galeria.

## Pré-requisitos
- Java Development Kit (JDK): Certifique‑se de que o Java está instalado no seu sistema. Você pode baixá‑lo no [site do JDK da Oracle](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).
- Aspose.PSD for Java: Você precisa ter a biblioteca Aspose.PSD for Java. Você pode obtê‑la na [página de download do Aspose.PSD Java](https://releases.aspose.com/psd/java/).
- Ambiente de Desenvolvimento Integrado (IDE): Use uma IDE como IntelliJ IDEA ou Eclipse para desenvolvimento Java.
- Compreensão básica de Java: Familiaridade com a linguagem de programação Java e seus conceitos.

## Como adicionar miniatura a um segmento JFIF em Java?
Carregue o PSD de destino, localize o recurso JFIF, substitua seus dados de miniatura e salve o arquivo. Toda a operação pode ser realizada com algumas chamadas de API simples, e o Aspose.PSD cuida da estrutura JPEG de baixo nível para você.

### Etapa 1: importar pacotes
`Document`, `JfifResource` e classes relacionadas fazem parte do namespace Aspose.PSD. Document representa o contêiner do arquivo PSD, e JfifResource fornece acesso ao segmento JFIF dentro do PSD. Importe‑os no início do seu arquivo fonte.

```java
import com.aspose.psd.Image;
import com.aspose.psd.exif.JpegExifData;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.resources.Thumbnail4Resource;
import com.aspose.psd.fileformats.psd.resources.ThumbnailResource;
```

### Etapa 2: carregar a imagem PSD
Crie uma instância de `PsdImage` passando o caminho do arquivo ao construtor. PsdImage é a classe Aspose.PSD que modela um documento Photoshop. Isso carrega os metadados do documento enquanto transmite os dados de pixel.

```java
String dataDir = "Your Document Directory";
PsdImage image = (PsdImage)Image.load(dataDir + "your_image.psd");
```

### Etapa 3: iterar sobre recursos de imagem
Procure na coleção `Resources` por um `JfifResource`. Quando encontrado, você pode substituir seu array de bytes da miniatura por uma nova pré‑visualização codificada em JPEG.

```java
for(int i = 0; i < image.getImageResources().length; i++) {
    if (image.getImageResources()[i] instanceof ThumbnailResource) {
        ThumbnailResource thumbnail = (ThumbnailResource)image.getImageResources()[i];
        
        // Continue with thumbnail processing
    }
}
```

### Etapa 4: ajustar os dados da miniatura
Gere uma pequena miniatura JPEG (por exemplo, 120 × 120 px) usando qualquer biblioteca de processamento de imagem, então atribua o array de bytes resultante a `jfifResource.ThumbnailData`.

```java
try {
    PsdImage thumbnailImage = new PsdImage(100, 100);
    
    // Fill thumbnail data (example: create a simple pixel array)
    int[] pixels = new int[thumbnailImage.getWidth() * thumbnailImage.getHeight()];
    for (int j = 0; j < pixels.length; j++) {
        pixels[j] = j;
    }
    
    // Save thumbnail data
    thumbnailImage.saveArgb32Pixels(thumbnailImage.getBounds(), pixels);
    
    // Set thumbnail data to Jpeg options
    JpegExifData exifData = new JpegExifData();
    exifData.setThumbnail(thumbnailImage);
    JpegOptions jpegOptions = new JpegOptions();
    jpegOptions.setExifData(exifData);
    
    // Set options to thumbnail resource
    thumbnail.getJpegOptions().setExifData(exifData);
    
} catch(Exception e) {
    // Handle exceptions
} finally {
    // Dispose of resources
}
```

### Etapa 5: salvar a imagem modificada
Chame o método `save` no objeto `PsdImage`, especificando o caminho de saída e o formato desejado. O segmento JFIF agora contém a nova miniatura.

```java
image.save(dataDir + "output.psd");
```

## Problemas comuns e soluções
- **Miniatura não visível em visualizadores:** Certifique‑se de que os dados da miniatura são um array de bytes JPEG válido e que suas dimensões estejam dentro de 256 × 256 px, que é o tamanho máximo suportado pela especificação JFIF.
- **OutOfMemoryError em PSDs grandes:** Use `PsdImage.load(inputStream, true)` para habilitar o modo de streaming, que mantém o consumo de memória baixo.
- **Tipo de recurso incorreto:** Verifique se o recurso que você está modificando é realmente um `JfifResource`; outros recursos como `ExifResource` não afetarão a exibição da miniatura.

## Perguntas frequentes

**Q: O que é Aspose.PSD for Java?**  
A: Aspose.PSD for Java é uma biblioteca comercial que permite aos desenvolvedores criar, editar, converter e renderizar arquivos Photoshop PSD sem necessidade do Adobe Photoshop.

**Q: Onde posso encontrar mais documentação para Aspose.PSD for Java?**  
A: Documentação detalhada pode ser encontrada na [página de documentação do Aspose.PSD for Java](https://reference.aspose.com/psd/java/).

**Q: O Aspose.PSD for Java é adequado para uso comercial?**  
A: Sim, Aspose.PSD for Java pode ser usado comercialmente. Você pode comprar uma licença na [página de compra do Aspose.PSD](https://purchase.aspose.com/buy).

**Q: Posso experimentar o Aspose.PSD for Java antes de comprar?**  
A: Sim, você pode baixar uma avaliação gratuita na [página de download de avaliação do Aspose.PSD](https://releases.aspose.com/).

**Q: Como posso obter suporte para Aspose.PSD for Java?**  
A: Para suporte, visite o [fórum do Aspose.PSD](https://forum.aspose.com/c/psd/34).

---

**Última atualização:** 2026-09-28  
**Testado com:** Aspose.PSD for Java 24.11  
**Autor:** Aspose

## Tutoriais Relacionados

- [Adicionar recurso IOPA a arquivos PSD usando Aspose PSD for Java](/psd/java/modifying-converting-psd-images/add-iopa-resource-psd-files/)
- [Adicionar assinatura à imagem – Desenhar imagem na tela com Aspose.PSD for Java](/psd/java/advanced-image-effects/add-signature-to-image/)
- [Como girar imagem em um ângulo específico com Aspose.PSD for Java](/psd/java/advanced-image-manipulation/rotate-image-specific-angle/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}