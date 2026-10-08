---
date: 2026-10-08
description: Aprenda a ler tags EXIF em Java usando Aspose.PSD for Java (asp) com
  nosso tutorial passo a passo e aumente suas capacidades de processamento de imagens.
keywords:
- read exif tags java
- java exif tag extraction
- java image metadata extraction
lastmod: 2026-10-08
linktitle: Ler informações específicas de tags EXIF em Java
og_description: Leia tags EXIF. Desenvolvedores Java podem extrair rapidamente metadados
  de imagens usando Aspose.PSD. Este guia orienta você a carregar um PSD, localizar
  recursos de miniatura e imprimir campos‑chave EXIF como WhiteBalance e ISO speed.
og_image_alt: Guide showing how to read EXIF tags from PSD files in Java using Aspose.PSD
og_title: Como ler tags EXIF em Java com Aspose.PSD
schemas:
- author: Aspose
  dateModified: '2026-10-08'
  description: Learn how to read EXIF tags in Java using Aspose.PSD for Java (asp)
    with our step‑by‑step tutorial, and boost your image processing capabilities.
  headline: How to read EXIF tags in Java with Aspose.PSD
  type: TechArticle
- description: Learn how to read EXIF tags in Java using Aspose.PSD for Java (asp)
    with our step‑by‑step tutorial, and boost your image processing capabilities.
  name: How to read EXIF tags in Java with Aspose.PSD
  steps:
  - name: 'Java Development Kit (JDK): Ensure you have JDK installed on your machine.
      You can download it from the [Oracle JDK website](https://www.oracle.com/java/technologies/javase-downloads.html).'
    text: 'Java Development Kit (JDK): Ensure you have JDK installed on your machine.
      You can download it from the [Oracle JDK website](https://www.oracle.com/java/technologies/javase-downloads.html).'
  - name: 'Aspose.PSD for Java: Download the library from the [Aspose.PSD for Java
      download page](https://releases.aspose.com/psd/java/).'
    text: 'Aspose.PSD for Java: Download the library from the [Aspose.PSD for Java
      download page](https://releases.aspose.com/psd/java/).'
  - name: 'Integrated Development Environment (IDE): An IDE like IntelliJ IDEA, Eclipse,
      or NetBeans will make coding more convenient.'
    text: 'Integrated Development Environment (IDE): An IDE like IntelliJ IDEA, Eclipse,
      or NetBeans will make coding more convenient.'
  - name: 'PSD file: A PSD file with EXIF data. You can use the sample provided in
      this tutorial or any other PSD file with EXIF tags.'
    text: 'PSD file: A PSD file with EXIF data. You can use the sample provided in
      this tutorial or any other PSD file with EXIF tags.'
  type: HowTo
- questions:
  - answer: Aspose.PSD (asp)
    question: What library reads EXIF data from PSD in Java?
  - answer: WhiteBalance, PixelXDimension, PixelYDimension, ISOSpeed, FocalLength,
      and more.
    question: Which tags can be extracted?
  - answer: Yes, a commercial license is required; a free trial is available.
    question: Do I need a license for production?
  - answer: The same API supports PNG, JPEG, TIFF via Java image metadata extraction.
    question: Can I use this with other image formats?
  - answer: About 10‑15 minutes for a basic read‑only scenario.
    question: How long does implementation take?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- read exif tags java
- Aspose.PSD
- java image metadata extraction
- EXIF extraction
- PSD processing
title: Como ler tags EXIF em Java com Aspose.PSD
url: /pt/java/java-jpeg-image-processing/read-specific-exif-tags-info-java/
weight: 19
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Ler informações de tags EXIF específicas em Java com Aspose (asp)

## Introdução
Se você precisa **ler tags EXIF em Java**, Aspose.PSD (asp) oferece uma API limpa, pura‑Java que funciona sem o Photoshop. Neste tutorial você aprenderá como extrair dados EXIF de uma imagem PSD, selecionar apenas as tags que lhe interessam e imprimi‑las no console. Cobrir‑emos tudo, desde a configuração do seu ambiente de desenvolvimento até a extração de metadados como WhiteBalance, velocidade ISO e distância focal. Vamos começar!

## Respostas rápidas
- **Qual biblioteca lê dados EXIF de PSD em Java?** Aspose.PSD (asp)  
- **Quais tags podem ser extraídas?** WhiteBalance, PixelXDimension, PixelYDimension, ISOSpeed, FocalLength, e mais.  
- **Preciso de uma licença para produção?** Sim, é necessária uma licença comercial; uma avaliação gratuita está disponível.  
- **Posso usar isso com outros formatos de imagem?** A mesma API suporta PNG, JPEG, TIFF via extração de metadados de imagem Java.  
- **Quanto tempo leva a implementação?** Cerca de 10‑15 minutos para um cenário básico de leitura‑somente.

## O que é asp (Aspose.PSD para Java)?
Aspose.PSD para Java é uma biblioteca pura‑Java que permite aos desenvolvedores trabalhar com arquivos Adobe Photoshop (PSD, PSB) sem instalar o Photoshop. Ela fornece acesso programático a camadas, recursos e metadados — incluindo tags EXIF — tornando‑a ideal para tarefas de **extração de metadados de imagem Java**.

## Por que usar Aspose.PSD (asp) para extração de EXIF?
Você pode extrair tags EXIF em Java com apenas duas chamadas de método, e a biblioteca processa arquivos de até 2 GB sem carregar todo o documento na memória. Ela suporta **30+ formatos de imagem** e preserva as configurações exatas da câmera, proporcionando resultados determinísticos em ambientes Windows, Linux e macOS.

## Pré-requisitos
Antes de mergulharmos no código, há algumas coisas que você precisará ter prontas:

1. Java Development Kit (JDK): Certifique‑se de que o JDK está instalado em sua máquina. Você pode baixá‑lo no [site da Oracle JDK](https://www.oracle.com/java/technologies/javase-downloads.html).  
2. Aspose.PSD para Java: Baixe a biblioteca na [página de download do Aspose.PSD para Java](https://releases.aspose.com/psd/java/).  
3. Ambiente de Desenvolvimento Integrado (IDE): Uma IDE como IntelliJ IDEA, Eclipse ou NetBeans tornará a codificação mais conveniente.  
4. Arquivo PSD: Um arquivo PSD com dados EXIF. Você pode usar o exemplo fornecido neste tutorial ou qualquer outro arquivo PSD com tags EXIF.

## Importar pacotes
Importe as classes necessárias do Aspose.PSD, como Image, PsdImage, ThumbnailResource e JpegExifData, para trabalhar com arquivos PSD.  
```java
import com.aspose.psd.Image;
import com.aspose.psd.exif.JpegExifData;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.resources.Thumbnail4Resource;
import com.aspose.psd.fileformats.psd.resources.ThumbnailResource;
```

## Etapa 1: carregar a imagem PSD
`Image.load()` carrega um arquivo e retorna um objeto Image que representa os dados da imagem.  
`PsdImage` é a classe Aspose.PSD que fornece funcionalidades específicas de PSD.  
O método `Image.load()` carrega qualquer arquivo de imagem suportado na memória, retornando um objeto genérico `Image` que você pode converter (cast) para um tipo específico de PSD.  
```java
String dataDir = "Your Document Directory";
PsdImage image = (PsdImage) Image.load(dataDir + "1280px-Zebras_Serengeti.psd");
```

Nesta etapa, carregamos o arquivo PSD usando o método `Image.load()`. A classe `PsdImage` é usada para representar a imagem PSD, e convertemos a imagem carregada para essa classe para acessar funcionalidades específicas de PSD.

## Etapa 2: iterar sobre os recursos da imagem
`PsdImage.getResources()` retorna uma coleção de recursos incorporados, como miniaturas e dados EXIF.  
A chamada `PsdImage.getResources()` devolve uma coleção de todos os recursos incorporados. Ao iterar sobre essa coleção, você pode localizar recursos de miniatura que contêm metadados EXIF.  
```java
for (int i = 0; i < image.getImageResources().length; i++) {
    if (image.getImageResources()[i] instanceof ThumbnailResource || 
        image.getImageResources()[i] instanceof Thumbnail4Resource) {
        // Further processing will be done here
    }
}
```

Percorremos os recursos da imagem usando um loop `for`. O objetivo é identificar recursos que são instâncias de `ThumbnailResource` ou `Thumbnail4Resource`, pois esses são os tipos que armazenam os dados EXIF.

## Etapa 3: extrair dados EXIF
`ThumbnailResource.getJpegOptions()` fornece acesso às opções JPEG, incluindo metadados EXIF.  
`JpegExifData` contém valores individuais de tags EXIF.  
O método `ThumbnailResource.getJpegOptions()` fornece acesso a um objeto `JpegExifData`, que contém tags EXIF individuais como WhiteBalance, ISOSpeed e FocalLength.  
```java
if (image.getImageResources()[i] instanceof ThumbnailResource) {
    JpegExifData exif = ((ThumbnailResource) image.getImageResources()[i]).getJpegOptions().getExifData();
    if (exif != null) {
        System.out.println("Exif WhiteBalance: " + exif.getWhiteBalance());
        System.out.println("Exif PixelXDimension: " + exif.getPixelXDimension());
        System.out.println("Exif PixelYDimension: " + exif.getPixelYDimension());
        System.out.println("Exif ISOSpeed: " + exif.getISOSpeed());
        System.out.println("Exif FocalLength: " + exif.getFocalLength());
    }
}
```

Usamos uma instrução `if` para verificar se o recurso é uma instância de `ThumbnailResource`. Se for, convertemos (cast) e recuperamos seu `JpegOptions` para acessar o `ExifData`. Por fim, imprimimos várias tags EXIF, como WhiteBalance, Dimensões de Pixel, ISOSpeed e FocalLength.

## Problemas comuns e dicas
- **Dados EXIF nulos:** Alguns arquivos PSD podem não conter um recurso de miniatura com informações EXIF. Sempre verifique se é `null` antes de acessar os valores das tags.  
- **Erros de caminho de arquivo:** Use caminhos absolutos ou certifique‑se de que o diretório de trabalho aponta para a pasta que contém seu arquivo PSD.  
- **Restrições de licença:** A avaliação gratuita limita o número de páginas que você pode processar; atualize para uma licença completa para uso ilimitado.

## Perguntas frequentes
### O que são dados EXIF?
Os dados EXIF (Exchangeable Image File Format) são metadados incorporados em arquivos de imagem, contendo informações como configurações da câmera, data e hora, e dimensões da imagem.

### Posso editar dados EXIF usando Aspose.PSD?
Sim, o Aspose.PSD permite ler e modificar dados EXIF. Você pode atualizar tags e salvar as alterações de volta no arquivo de imagem.

### O Aspose.PSD para Java é gratuito?
O Aspose.PSD oferece uma versão de avaliação gratuita que você pode baixar na [página oficial de lançamentos do Aspose.PSD](https://releases.aspose.com/). Para recursos completos, é necessário adquirir uma licença.

### Quais outros formatos o Aspose.PSD suporta?
O Aspose.PSD suporta vários formatos do Adobe Photoshop, incluindo PSD, PSB e outros. Ele também oferece opções para converter esses formatos para PNG, JPEG, TIFF, etc.

### Como obtenho suporte para Aspose.PSD?
Você pode obter suporte através do [fórum Aspose.PSD](https://forum.aspose.com/c/psd/34).

### Como isso ajuda na **extração de metadados de imagem Java**?
Usando o objeto `JpegExifData`, você pode extrair programaticamente qualquer tag EXIF que precisar, tornando‑a uma base sólida para tarefas mais amplas de extração de metadados em diferentes formatos de imagem.

---

**Última atualização:** 2026-10-08  
**Testado com:** Aspose.PSD for Java 24.11 (mais recente no momento da escrita)  
**Autor:** Aspose

## Tutoriais Relacionados

- [Ler e Modificar Tags Exif JPEG Java](/psd/java/java-jpeg-image-processing/read-modify-jpeg-exif-tags-java/)
- [Processamento de Imagem JPEG Java](/psd/java/java-jpeg-image-processing/)
- [Como Rotacionar Imagem em um Ângulo Específico com Aspose.PSD para Java](/psd/java/advanced-image-manipulation/rotate-image-specific-angle/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}