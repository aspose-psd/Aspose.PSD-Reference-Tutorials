---
date: 2026-10-03
description: Aprenda como extrair thumbnail de PSD em Java usando Aspose.PSD. Este
  guia passo a passo cobre a configuração, trechos de código e a gravação do thumbnail
  como imagem JPEG.
keywords:
- extract thumbnail from psd
- java aspose psd
- psd thumbnail extraction
lastmod: 2026-10-03
linktitle: Extrair thumbnail de PSD em Java
og_description: Aprenda como extrair thumbnail de PSD em Java com Aspose.PSD. Este
  guia orienta você na configuração, carregamento do arquivo, extração do thumbnail
  e salvamento como imagem JPEG.
og_image_alt: Screenshot showing Java code extracting a thumbnail from a PSD file
  using Aspose.PSD
og_title: Extrair thumbnail de PSD em Java usando Aspose.PSD
schemas:
- author: Aspose
  dateModified: '2026-10-03'
  description: Learn how to extract thumbnail from PSD in Java using Aspose.PSD. This
    step‑by‑step guide covers setup, code snippets, and saving the thumbnail as a
    JPEG image.
  headline: Extract thumbnail from PSD in Java
  type: TechArticle
- questions:
  - answer: Aspose.PSD is a Java library that enables programmatic creation, manipulation,
      and conversion of PSD and other raster image formats without requiring Adobe
      Photoshop.
    question: What is Aspose.PSD?
  - answer: You can refer to the [documentation](https://reference.aspose.com/psd/java/)
      for detailed API references and examples.
    question: Where can I find more documentation on Aspose.PSD for Java?
  - answer: Yes, you can download a [free trial](https://releases.aspose.com/) to
      evaluate the library’s capabilities.
    question: Can I try Aspose.PSD for free before purchasing?
  - answer: Temporary licenses are available from the [temporary license](https://purchase.aspose.com/temporary-license/)
      page.
    question: How can I obtain a temporary license for Aspose.PSD?
  - answer: Yes, Aspose.PSD can be used in both personal and commercial projects under
      its licensing terms.
    question: Is Aspose.PSD suitable for commercial use?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- java image processing
- aspose.psd
- thumbnail extraction
title: Extrair thumbnail de PSD em Java
url: /pt/java/java-jpeg-image-processing/extract-thumbnail-from-psd-java/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Extrair miniatura de PSD em Java

## Introdução
Extrair uma miniatura de um arquivo PSD permite gerar visualizações rápidas sem carregar a imagem em resolução completa. Em Java, o Aspose.PSD torna esse processo simples e eficiente. Neste tutorial você aprenderá como configurar a biblioteca, localizar o recurso de miniatura e salvá-lo como um arquivo JPEG — tudo com apenas algumas linhas de código.

## Respostas rápidas
- **Qual biblioteca manipula miniaturas PSD?** Aspose.PSD for Java.
- **Quantas linhas de código são necessárias?** Cerca de cinco linhas para carregar, extrair e salvar.
- **Posso extrair miniaturas de arquivos PSD grandes?** Sim, Aspose.PSD processa arquivos de até 500 MB sem carregar toda a memória.
- **Preciso de licença para desenvolvimento?** Um teste gratuito funciona para avaliação; uma licença é necessária para produção.
- **Quais formatos de saída são suportados?** A miniatura extraída pode ser salva como JPEG, PNG ou BMP.

## O que é extrair miniatura de PSD?
Extrair miniatura de PSD é o processo de ler a pequena imagem de pré‑visualização incorporada dentro de um documento Photoshop (PSD). Essa pré‑visualização é armazenada como um recurso e pode ser salva independentemente para catalogação ou exibição. A miniatura costuma ser uma representação de baixa resolução usada por aplicativos para mostrar um resumo visual rápido sem carregar a imagem em tamanho completo.

## Por que usar Aspose.PSD para esta tarefa?
Aspose.PSD suporta **mais de 30 formatos de imagem** e pode lidar com arquivos PSD de até **500 MB** mantendo o uso de memória baixo, pois lê recursos sob demanda. A API também oferece tratamento robusto de erros, permitindo extrair miniaturas de forma confiável mesmo de arquivos corrompidos.

## Pré-requisitos
Antes de começar, certifique‑se de que você tem:
- Java Development Kit (JDK) instalado.
- Biblioteca Aspose.PSD for Java baixada de [Aspose.PSD for Java download](https://releases.aspose.com/psd/java/).
- Familiaridade básica com a sintaxe Java e configuração de projetos.

## Como extrair uma miniatura de um arquivo PSD em Java?
Carregue o arquivo PSD com `PsdImage`, localize o `ThumbnailResource` e salve seus dados de imagem como JPEG. Aspose.PSD abstrai a análise de baixo nível, de modo que você só precisa chamar `getResources()` e depois `save()` na imagem extraída. Essa abordagem funciona para qualquer PSD que contenha uma miniatura, independentemente do tamanho do arquivo.

## Importar pacotes
`Image` é a classe base para carregamento de imagens. `PsdImage` representa um documento PSD. `ThumbnailResource` e `Thumbnail4Resource` representam recursos de miniatura. `JpegOptions` especifica opções de salvamento JPEG.

```text
```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.resources.Thumbnail4Resource;
import com.aspose.psd.fileformats.psd.resources.ThumbnailResource;
import com.aspose.psd.imageoptions.JpegOptions;
```
```

## Etapa 1: carregar o arquivo PSD
Primeiro, crie uma instância de `PsdImage` apontando para o seu arquivo PSD. O construtor lê apenas o cabeçalho e os recursos necessários, mantendo o uso de memória mínimo.

```text
```java
String dataDir = "Your_Document_Directory/";
PsdImage image = (PsdImage)Image.load(dataDir + "your_file.psd");
```
```

Substitua `"Your_Document_Directory/"` pelo caminho do diretório onde seu arquivo PSD está localizado e `"your_file.psd"` pelo nome do seu arquivo PSD.

## Etapa 2: iterar sobre os recursos da imagem
Aspose.PSD armazena miniaturas como objetos `ThumbnailResource` dentro da coleção de recursos da imagem. Percorra a coleção, verifique o tipo de recurso e capture a primeira miniatura encontrada.

```text
```java
for (int i = 0; i < image.getImageResources().length; i++) {
    if (image.getImageResources()[i] instanceof ThumbnailResource) {
        ThumbnailResource thumbnail = (ThumbnailResource) image.getImageResources()[i];
        
        // Extract thumbnail data
        int[] data = thumbnail.getThumbnailArgb32Data();
        
        // Create a new image with the extracted thumbnail data
        PsdImage extractedThumbnailImage = new PsdImage(thumbnail.getWidth(), thumbnail.getHeight());
        extractedThumbnailImage.saveArgb32Pixels(extractedThumbnailImage.getBounds(), data);
        
        // Save the extracted thumbnail as a separate JPEG file
        extractedThumbnailImage.save(dataDir + "extracted_thumbnail.jpg", new JpegOptions());
        
        // Output success message
        System.out.println("Thumbnail extracted and saved successfully.");
        
        break; // Exit the loop once thumbnail is found and processed
    }
}
```
```

## Etapa 3: salvar a miniatura extraída
Depois de ter a imagem da miniatura, chame seu método `save` para gravá‑la no disco. Você pode escolher JPEG, PNG ou BMP; JPEG é o mais comum para pré‑visualizações web.

## Etapa 4: lidar com diferentes tipos de miniatura
Se um PSD contiver múltiplas variantes de miniatura, como `Thumbnail4Resource`, amplie a lógica de iteração para verificar cada tipo. A API fornece classes separadas para cada recurso, permitindo selecionar a resolução que você precisa.

## Problemas comuns e soluções
- **Miniatura não encontrada:** Nem todos os arquivos PSD incorporam uma pré‑visualização. Verifique o arquivo fonte no painel “Arquivo → Informações do arquivo” do Photoshop.
- **Erro de formato não suportado:** Certifique‑se de que está usando a versão mais recente do Aspose.PSD; versões antigas podem não reconhecer novos tipos de recursos de miniatura.
- **Falta de memória em arquivos grandes:** Use `PsdImage.load(..., LoadOptions)` com `LoadOptions.setLoadResourcesOnly(true)` para evitar carregar os dados completos da imagem quando você só precisa da miniatura.

## Perguntas frequentes

**Q: O que é Aspose.PSD?**  
A: Aspose.PSD é uma biblioteca Java que permite a criação, manipulação e conversão programáticas de arquivos PSD e outros formatos de imagem raster sem exigir o Adobe Photoshop.

**Q: Onde posso encontrar mais documentação sobre Aspose.PSD para Java?**  
A: Você pode consultar a [documentação](https://reference.aspose.com/psd/java/) para referências detalhadas da API e exemplos.

**Q: Posso experimentar Aspose.PSD gratuitamente antes de comprar?**  
A: Sim, você pode baixar uma [versão de avaliação gratuita](https://releases.aspose.com/) para avaliar as capacidades da biblioteca.

**Q: Como posso obter uma licença temporária para Aspose.PSD?**  
A: Licenças temporárias estão disponíveis na página de [licença temporária](https://purchase.aspose.com/temporary-license/).

**Q: O Aspose.PSD é adequado para uso comercial?**  
A: Sim, o Aspose.PSD pode ser usado em projetos pessoais e comerciais de acordo com seus termos de licenciamento.

---

**Última atualização:** 2026-10-03  
**Testado com:** Aspose.PSD for Java 24.12  
**Autor:** Aspose

## Tutoriais relacionados

- [Como converter PSD para formatos de imagem raster com Aspose.PSD para Java](/psd/java/advanced-techniques/convert-psd-to-raster-formats/)
- [Salvar PSD como JPEG e suportar cor RGB com Aspose.PSD Java](/psd/java/advanced-psd-layer-features-effects/support-rgb-color-psd-files/)
- [Redimensionar imagem com Aspose.PSD para Java – desenhar formas e operações básicas de imagem](/psd/java/basic-image-operations/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}