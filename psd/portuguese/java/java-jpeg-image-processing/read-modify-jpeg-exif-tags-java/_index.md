---
date: 2026-10-03
description: Aprenda como ler metadados de imagem em Java e modificar tags EXIF JPEG
  com Aspose.PSD for Java neste guia passo a passo, perfeito para desenvolvedores
  que lidam com metadados de imagem de forma eficiente.
keywords:
- java read image metadata
- read EXIF tags Java
- modify JPEG metadata Java
- Aspose.PSD Java
lastmod: 2026-10-03
linktitle: Ler e Modificar Tags EXIF JPEG em Java
og_description: Aprenda como ler metadados de imagem em Java e modificar tags EXIF
  JPEG com Aspose.PSD for Java. Este guia mostra código passo a passo para extrair
  e atualizar informações EXIF.
og_image_alt: Guide showing how to java read image metadata and edit JPEG EXIF tags
  using Aspose.PSD for Java
og_title: Como ler metadados de imagem em Java e modificar tags EXIF JPEG
schemas:
- author: Aspose
  dateModified: '2026-10-03'
  description: Learn how to java read image metadata and modify JPEG EXIF tags with
    Aspose.PSD for Java in this step‑by‑step guide, perfect for developers handling
    image metadata efficiently.
  headline: How to java read image metadata and modify JPEG EXIF tags
  type: TechArticle
- description: Learn how to java read image metadata and modify JPEG EXIF tags with
    Aspose.PSD for Java in this step‑by‑step guide, perfect for developers handling
    image metadata efficiently.
  name: How to java read image metadata and modify JPEG EXIF tags
  steps:
  - name: '**Java Development Kit (JDK)** – make sure you have JDK 11 or newer. You
      can download it from the [Oracle website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).'
    text: '**Java Development Kit (JDK)** – make sure you have JDK 11 or newer. You
      can download it from the [Oracle website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).'
  - name: '**Aspose.PSD for Java library** – obtain the latest JAR from the [Aspose
      releases page](https://releases.aspose.com/psd/java/).'
    text: '**Aspose.PSD for Java library** – obtain the latest JAR from the [Aspose
      releases page](https://releases.aspose.com/psd/java/).'
  - name: '**IDE** – IntelliJ IDEA, Eclipse, or any editor you prefer.'
    text: '**IDE** – IntelliJ IDEA, Eclipse, or any editor you prefer.'
  - name: '**Basic Java knowledge** – you should be comfortable with creating projects
      and adding external JARs.'
    text: '**Basic Java knowledge** – you should be comfortable with creating projects
      and adding external JARs.'
  type: HowTo
- questions:
  - answer: EXIF (Exchangeable Image File Format) metadata stores camera settings,
      timestamps, GPS coordinates, and other information embedded in JPEG and other
      image files.
    question: What is EXIF data?
  - answer: You can get a free trial from the [Aspose releases page](https://releases.aspose.com/).
    question: Can I use Aspose.PSD for Java for free?
  - answer: Aspose.PSD for Java supports Java SE 7 and above.
    question: Is Aspose.PSD for Java compatible with all versions of Java?
  - answer: Check out the [documentation](https://reference.aspose.com/psd/java/)
      for more details.
    question: Where can I find more documentation on Aspose.PSD for Java?
  - answer: You can get support from the [Aspose PSD support forum](https://forum.aspose.com/c/psd/34/).
    question: How do I get support for Aspose.PSD for Java?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- java image metadata
- exif tags
- aspose psd
- jpeg metadata
- java tutorial
title: Como ler metadados de imagem em Java e modificar tags EXIF JPEG
url: /pt/java/java-jpeg-image-processing/read-modify-jpeg-exif-tags-java/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Ler e modificar tags EXIF de JPEG em Java

## Introdução
Se você precisa **java read image metadata** de arquivos JPEG e alterá‑los programaticamente, chegou ao lugar certo. Neste tutorial vamos percorrer a extração e atualização de tags EXIF usando Aspose.PSD for Java. Ao final, você será capaz de obter detalhes da câmera, orientação e campos personalizados, e gravá‑los de volta no arquivo — tudo sem um editor gráfico.

## Respostas rápidas
- **Qual biblioteca manipula EXIF de JPEG em Java?** Aspose.PSD for Java.  
- **Quantas linhas de código para ler EXIF?** Cerca de três linhas após carregar a imagem.  
- **É possível modificar tags EXIF?** Sim, você pode mudar qualquer tag padrão ou personalizada e salvar o resultado.  
- **Formatos de imagem suportados?** Mais de 150 formatos, incluindo PSD, JPEG, PNG, TIFF e BMP.  
- **Versão mínima do Java?** Java 7 ou superior.

## Por que usar Aspose.PSD for Java?
Aspose.PSD suporta **mais de 150 formatos de imagem** e pode processar arquivos de até **2 GB** sem carregar todo o documento na memória, oferecendo operações de metadados rápidas e de baixo consumo de memória em grandes coleções de fotos. Também fornece uma API simples para leitura e gravação de dados EXIF, IPTC e XMP, tornando o processamento em lote de milhares de imagens eficiente e confiável.

## Pré‑requisitos
1. **Java Development Kit (JDK)** – certifique‑se de que você tem o JDK 11 ou mais recente. Você pode baixá‑lo no [site da Oracle](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).  
2. **Aspose.PSD for Java library** – obtenha o JAR mais recente na [página de releases da Aspose](https://releases.aspose.com/psd/java/).  
3. **IDE** – IntelliJ IDEA, Eclipse ou qualquer editor de sua preferência.  
4. **Conhecimento básico de Java** – você deve estar confortável em criar projetos e adicionar JARs externos.

## O que é java read image metadata?
Java read image metadata refere‑se ao processo de acessar programaticamente informações incorporadas, como EXIF, IPTC e XMP, armazenadas dentro de arquivos de imagem usando código Java. Esses metadados podem incluir configurações da câmera, carimbos de data/hora, coordenadas GPS, avisos de direitos autorais e comentários de usuário, permitindo que aplicações organizem, pesquisem e manipulem imagens com base em seus dados descritivos.

## Importar pacotes
Primeiro, adicione o JAR Aspose.PSD ao classpath do seu projeto e importe as classes necessárias.

O pacote `com.aspose.psd` fornece a API central para carregar imagens e acessar seus recursos.

```java
import com.aspose.psd.Image;
import com.aspose.psd.exif.JpegExifData;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.resources.Thumbnail4Resource;
import com.aspose.psd.fileformats.psd.resources.ThumbnailResource;
```

## Como ler metadados de imagem de arquivos JPEG em Java?
Carregue o JPEG com `PsdImage.load("image.jpg")`, localize o recurso de miniatura que contém os dados EXIF e então chame `ExifData.read()` para obter um objeto `ExifData` preenchido. Essa abordagem de um único passo fornece acesso total a todos os campos EXIF padrão e a quaisquer tags personalizadas que você tenha adicionado.

## Etapa 1: Carregar a imagem PSD
PsdImage é a classe Aspose.PSD que representa um arquivo PSD e fornece métodos para acessar seus recursos e metadados.  
Nesta etapa, vamos carregar a imagem PSD da qual queremos ler os dados EXIF. Certifique‑se de que sua imagem esteja no diretório correto.

```java
String dataDir = "Your Document Directory";
PsdImage image = null;
try {
    image = (PsdImage) Image.load(dataDir + "1280px-Zebras_Serengeti.psd");
} catch (IOException e) {
    e.printStackTrace();
}
```

## Etapa 2: Iterar sobre os recursos da imagem
ThumbnailResource representa uma imagem em miniatura armazenada em um arquivo PSD, frequentemente contendo dados EXIF incorporados.  
Depois que a imagem for carregada, o próximo passo é iterar sobre seus recursos para encontrar o recurso de miniatura, que normalmente contém os dados EXIF.

```java
for (int i = 0; i < image.getImageResources().length; i++) {
    if (image.getImageResources()[i] instanceof ThumbnailResource) {
        ThumbnailResource thumbnail = (ThumbnailResource) image.getImageResources()[i];
        // Proceed to next step
    }
}
```

## Etapa 3: Extrair dados EXIF
JpegExifData é a classe que contém as informações EXIF extraídas de uma imagem JPEG, permitindo ler e modificar tags individuais.  
Agora que temos o recurso de miniatura, podemos extrair os dados EXIF dele. Os dados EXIF incluem informações valiosas como o nome do proprietário da câmera, valor da abertura, orientação e muito mais.

```java
JpegExifData exifData = thumbnail.getJpegOptions().getExifData();
if (exifData != null) {
    System.out.println("Camera Owner Name: " + exifData.getCameraOwnerName());
    System.out.println("Aperture Value: " + exifData.getApertureValue());
    System.out.println("Orientation: " + exifData.getOrientation());
    System.out.println("Focal Length: " + exifData.getFocalLength());
    System.out.println("Compression: " + exifData.getCompression());
}
```

## Etapa 4: Modificar dados EXIF
Após ler os dados EXIF, você pode querer modificar alguns de seus campos. Veja como fazer isso:

```java
if (exifData != null) {
    exifData.setCameraOwnerName("New Camera Owner");
    exifData.setApertureValue(3.5);
    exifData.setOrientation(1);
    exifData.setFocalLength(35.0);
    exifData.setCompression(6);
    thumbnail.getJpegOptions().setExifData(exifData);
}
```

## Etapa 5: Salvar as alterações
Finalmente, após modificar os dados EXIF, salve as alterações em um novo arquivo PSD.

```java
try {
    image.save(dataDir + "Modified_Zebras_Serengeti.psd");
} catch (IOException e) {
    e.printStackTrace();
}
```

## Problemas comuns e soluções
- **Recurso de miniatura ausente** – Alguns JPEGs armazenam EXIF diretamente no cabeçalho da imagem principal. Se o recurso de miniatura estiver ausente, use `image.getExifData()` em vez disso.  
- **Arquivos grandes causam OutOfMemoryError** – Garanta que a JVM seja iniciada com heap suficiente (`-Xmx2g`) ou processe a imagem em modo streaming usando `PsdImage.load(inputStream, loadOptions)`.  
- **Tipos de tag não suportados** – Aspose.PSD suporta todas as tags EXIF padrão; tags personalizadas podem exigir manipulação manual em nível de bytes.

## Perguntas frequentes

**Q: O que são dados EXIF?**  
A: Metadados EXIF (Exchangeable Image File Format) armazenam configurações da câmera, carimbos de data/hora, coordenadas GPS e outras informações incorporadas em arquivos JPEG e outros formatos de imagem.

**Q: Posso usar Aspose.PSD for Java gratuitamente?**  
A: Você pode obter uma avaliação gratuita na [página de releases da Aspose](https://releases.aspose.com/).

**Q: O Aspose.PSD for Java é compatível com todas as versões do Java?**  
A: Aspose.PSD for Java suporta Java SE 7 e superiores.

**Q: Onde encontro mais documentação sobre Aspose.PSD for Java?**  
A: Consulte a [documentação](https://reference.aspose.com/psd/java/) para mais detalhes.

**Q: Como obtenho suporte para Aspose.PSD for Java?**  
A: Você pode obter suporte no [fórum de suporte Aspose PSD](https://forum.aspose.com/c/psd/34/).

## Conclusão
Seguindo estas etapas, você pode **java read image metadata** de qualquer JPEG, ajustar os campos EXIF necessários e gravar os dados atualizados de volta ao arquivo — tudo com poucas linhas de código Java limpo. A API rica do Aspose.PSD torna o manuseio de metadados confiável e performático, permitindo sua integração em pipelines de processamento em lote, ferramentas de gerenciamento de fotos ou qualquer aplicação que precise trabalhar com informações de imagem.

---

**Última atualização:** 2026-10-03  
**Testado com:** Aspose.PSD for Java 24.5  
**Autor:** Aspose

## Tutoriais relacionados

- [Read Specific EXIF Tags Information in Java with Aspose (asp)](/psd/java/java-jpeg-image-processing/read-specific-exif-tags-info-java/)
- [Create XMP Metadata in PSD Files Using Aspose.PSD for Java](/psd/java/image-editing/create-xmp-metadata/)
- [Resize Image with Aspose.PSD for Java – Draw Shapes & Basic Image Operations](/psd/java/basic-image-operations/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}