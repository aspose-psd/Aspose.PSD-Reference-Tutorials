---
date: 2026-09-28
description: Aprenda como exportar PSD como PNG definindo o modo de cor do PSD para
  escala de cinza de 16 bits usando Aspose.PSD for Java. Guia passo a passo com exemplos
  de código.
keywords:
- export psd as png
- how to convert psd to png
- 16-bit grayscale java
lastmod: 2026-09-28
linktitle: Exportar PSD como PNG – Escala de Cinza de 16 bits – Java
og_description: Exportar PSD como PNG com escala de cinza de 16 bits usando Aspose.PSD
  for Java. Siga este tutorial passo a passo para preservar 65,536 tons de cinza.
og_image_alt: Guide showing how to export PSD as PNG with 16-bit grayscale using Aspose.PSD
  Java
og_title: Exportar PSD como PNG com escala de cinza de 16 bits em Java – Guia Aspose.PSD
schemas:
- author: Aspose
  dateModified: '2026-09-28'
  description: Learn how to export PSD as PNG while setting PSD color mode to 16-bit
    grayscale using Aspose.PSD for Java. Step‑by‑step guide with code examples.
  headline: How to export PSD as PNG with 16‑bit grayscale color mode in Java
  type: TechArticle
- description: Learn how to export PSD as PNG while setting PSD color mode to 16-bit
    grayscale using Aspose.PSD for Java. Step‑by‑step guide with code examples.
  name: How to export PSD as PNG with 16‑bit grayscale color mode in Java
  steps:
  - name: '**Java Development Kit (JDK)** – Install the latest JDK from [Oracle''s
      site](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).'
    text: '**Java Development Kit (JDK)** – Install the latest JDK from [Oracle''s
      site](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).'
  - name: '**Aspose.PSD for Java library** – Download the JAR from the [Aspose download
      page](https://releases.aspose.com/psd/java/).'
    text: '**Aspose.PSD for Java library** – Download the JAR from the [Aspose download
      page](https://releases.aspose.com/psd/java/).'
  - name: '**An IDE** – IntelliJ IDEA, Eclipse, or Visual Studio Code works perfectly.'
    text: '**An IDE** – IntelliJ IDEA, Eclipse, or Visual Studio Code works perfectly.'
  - name: '**Basic Java knowledge** – You should be comfortable creating classes,
      handling exceptions, and working with file paths.'
    text: '**Basic Java knowledge** – You should be comfortable creating classes,
      handling exceptions, and working with file paths.'
  - name: '**A sample PSD file** – Create one in Adobe Photoshop or grab a free sample
      online.'
    text: '**A sample PSD file** – Create one in Adobe Photoshop or grab a free sample
      online.'
  type: HowTo
- questions:
  - answer: It provides 65 536 shades of gray, delivering far more tonal detail than
      the standard 8‑bit (256 shades).
    question: What is 16‑bit grayscale color mode?
  - answer: Absolutely! Aspose.PSD supports RGB, CMYK, Lab, Indexed, and many other
      color modes.
    question: Can I use Aspose.PSD for non‑grayscale images?
  - answer: Yes, you can try a free trial version of Aspose.PSD. Just head to the
      [Aspose download page](https://releases.aspose.com/).
    question: Is there a trial version of Aspose.PSD?
  - answer: Check the official [documentation](https://reference.aspose.com/psd/java/)
      for in‑depth tutorials, API references, and sample projects.
    question: Where can I find more Aspose.PSD examples?
  - answer: You can buy a license by visiting the [Aspose purchase page](https://purchase.aspose.com/buy).
    question: How do I purchase a license for Aspose.PSD?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- convert psd
- Aspose.PSD
- Java image processing
title: Como exportar PSD como PNG com modo de cor em escala de cinza de 16 bits em
  Java
url: /pt/java/advanced-psd-layer-features-effects/support-16-bit-grayscale-color-mode-psd/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Exportar PSD como PNG com modo de cor em escala de cinza de 16‑bits em Java

## Introdução
Exportar PSD como PNG mantendo um modo de cor em escala de cinza de 16‑bits oferece a profundidade de uma fotografia profissional e a compatibilidade universal do PNG. Neste guia você aprenderá como **definir o modo de cor do PSD para escala de cinza de 16‑bits** e então **exportar o PSD como PNG** usando Aspose.PSD para Java. O tutorial cobre tudo, desde pré‑requisitos até solução de problemas, para que você possa integrar o fluxo de trabalho em qualquer pipeline de imagens baseado em Java.

## Respostas rápidas
- **O que envolve “exportar PSD como PNG”?** Carregar um PSD, opcionalmente mudar seu modo de cor e salvá‑lo como um arquivo PNG.  
- **Qual classe da Aspose lida com a conversão?** `PsdImage` carrega o PSD e `PngOptions` define as configurações de saída PNG.  
- **Preciso de uma licença para produção?** Sim – uma versão de avaliação funciona para testes, mas uma licença paga é necessária para uso comercial.  
- **A profundidade de 16‑bits pode ser mantida no PNG?** Absolutamente, usando `PngColorType.GrayscaleWithAlpha`.  
- **Quais IDEs são suportadas?** Qualquer IDE Java – IntelliJ IDEA, Eclipse, VS Code ou NetBeans.

## O que é exportar PSD como PNG?
Exportar PSD como PNG é o processo de converter um documento do Adobe Photoshop (PSD) em um arquivo Portable Network Graphics (PNG) preservando os dados de pixel e a profundidade de cor da imagem. Essa conversão é comumente usada para compartilhar recursos em escala de cinza de alta qualidade na web sem perder detalhes tonais.

## Por que exportar PSD como PNG com escala de cinza de 16‑bits?
Exportar para PNG mantendo a escala de cinza de 16‑bits preserva 65 536 tons de cinza, o que oferece muito mais riqueza tonal do que imagens de 8‑bits. O suporte universal do PNG garante que os arquivos possam ser exibidos em navegadores, aplicativos móveis e editores de desktop sem perda, enquanto a compressão sem perdas do Aspose.PSD garante que nenhum artefato seja introduzido.

## Pré-requisitos
Antes de começarmos, certifique‑se de que você tem os seguintes itens prontos:

1. **Java Development Kit (JDK)** – Instale o JDK mais recente a partir do [site da Oracle](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).  
2. **Biblioteca Aspose.PSD para Java** – Baixe o JAR na [página de download da Aspose](https://releases.aspose.com/psd/java/).  
3. **Uma IDE** – IntelliJ IDEA, Eclipse ou Visual Studio Code funcionam perfeitamente.  
4. **Conhecimento básico de Java** – Você deve estar confortável em criar classes, tratar exceções e trabalhar com caminhos de arquivos.  
5. **Um arquivo PSD de exemplo** – Crie um no Adobe Photoshop ou obtenha um exemplo gratuito online.

## Como exportar PSD como PNG passo a passo

## Como definir o modo de cor do PSD para escala de cinza de 16‑bits?
PsdImage é a classe Aspose.PSD que carrega e representa um arquivo PSD na memória.  
ColorMode é uma enumeração que define o modo de cor de uma imagem PSD.  

Carregue o PSD com `PsdImage`, altere seu modo de cor usando a propriedade `ColorMode` e então salve o arquivo modificado. Esta operação ocorre totalmente na memória, eliminando a necessidade de arquivos intermediários e garantindo que a conversão seja rápida e eficiente.

```java
import com.aspose.psd.*;
import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.fileformats.psd.ColorModes;
import com.aspose.psd.fileformats.psd.CompressionMethod;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.PngOptions;
import com.aspose.psd.imageoptions.PsdOptions;
import com.aspose.psd.system.Enum;
```

Essas importações dão acesso às funcionalidades que você usará para manipular arquivos PSD, definir o modo de cor e exportar o resultado como PNG.

## Como definir diretórios de origem e saída?
`File` é uma classe java.io que representa um caminho de arquivo ou diretório no sistema de arquivos.  

Você precisa informar ao programa onde ler o PSD original e onde gravar o PNG convertido. Usar caminhos absolutos ou relativos funciona, mas mantenha‑os consistentes entre ambientes para evitar erros de resolução de caminho.

```java
String sourceDir = "Your Source Directory"; // Change to your source directory
String outputDir = "Your Document Directory"; // Change to your output directory
```

Substitua as strings de espaço reservado pelos caminhos reais na sua máquina.

## Como encapsular a lógica de conversão em um método reutilizável?
`convertPsdToPng` é um método personalizado que encapsula todas as etapas necessárias para converter um arquivo PSD em PNG com configurações opcionais.  

Criar um método dedicado permite reutilizar as mesmas etapas de conversão para vários arquivos ou diferentes configurações. Passe parâmetros como caminho de origem, pasta de destino e nível de compressão opcional, tornando o fluxo de trabalho flexível e fácil de manter.

```java
class LocalScopeExtension {
    void saveToPsdThenLoadAndSaveToPng(
        String file,
        short colorMode,
        short channelBitsCount,
        short channelsCount,
        short compression,
        int layerNumber) {
```

Este método permite que você **defina o modo de cor do PSD** e então **exporte o PSD como PNG** em um único fluxo.

## Como carregar o PSD e aplicar o modo de escala de cinza de 16‑bits?
PsdImage é a classe Aspose.PSD que carrega um arquivo PSD na memória.  
ColorMode.GRAYSCALE_16 é um valor de enumeração que define a imagem como escala de cinza de 16‑bits.  
`channelBitsCount` é uma propriedade que especifica o número de bits por canal.  

Dentro do método de conversão, construa os caminhos completos dos arquivos, instancie `PsdImage` e altere seu `ColorMode` para `ColorMode.GRAYSCALE_16`. A propriedade `channelBitsCount` deve ser definida como 16 para manter a alta profundidade de bits, garantindo que a imagem retenha todas as informações tonais.

```java
String filePath = sourceDir + file + ".psd";
String postfix = Enum.getName(ColorModes.class, colorMode) + channelBitsCount + "_" +
                 channelsCount + "_" + Enum.getName(CompressionMethod.class, compression);
String exportPath = outputDir + file + postfix + ".psd";
String pngExportPath = outputDir + file + postfix + ".png";
// Load a predefined 16-bit grayscale PSD
PsdImage image = (PsdImage)Image.load(filePath);
```

O `postfix` ajuda a rastrear as configurações usadas para cada arquivo exportado.

## Como desenhar uma borda sutil na imagem (etapa opcional)?
`Graphics` é uma classe que fornece capacidades de desenho em uma tela `PsdImage`.  

Você pode opcionalmente desenhar um retângulo cinza ao redor da imagem para tornar a saída mais visível durante os testes. Esta etapa demonstra como trabalhar com camadas e objetos gráficos, e o retângulo é calculado dinamicamente para permanecer centralizado independentemente do tamanho da imagem.

```java
try {
    RasterCachedImage raster = layerNumber >= 0 ? image.getLayers()[layerNumber] : image;
    // Draw a gray inner border around the perimeter of the layer
    Graphics graphics = new Graphics(raster);
    int width = raster.getWidth();
    int height = raster.getHeight();
    Rectangle rect = new Rectangle(
        width / 3,
        height / 3,
        width - (2 * (width / 3)) - 1,
        height - (2 * (height / 3)) - 1);
    graphics.drawRectangle(new Pen(Color.getDarkGray(), 1), rect);
```

O retângulo é calculado dinamicamente para permanecer centralizado independentemente do tamanho da imagem.

## Como salvar o PSD modificado com o novo modo de cor?
`PsdOptions` é uma classe que controla como um arquivo PSD é salvo, incluindo configurações de modo de cor e profundidade de bits.  

Após desenhar (ou pular essa etapa), chame `save` na instância `PsdImage`, passando um objeto `PsdOptions` que preserva a configuração de escala de cinza de 16‑bits. Isso garante que o PSD salvo retenha o modo de cor desejado sem perda de dados.

```java
    // Save a copy of PSD with specific characteristics
    PsdOptions psdOptions = new PsdOptions();
    psdOptions.setColorMode(colorMode);
    psdOptions.setChannelBitsCount(channelBitsCount);
    psdOptions.setChannelsCount(channelsCount);
    psdOptions.setCompressionMethod(compression);
    image.save(exportPath, psdOptions);
}
```

## Como converter o PSD para PNG preservando a profundidade de 16‑bits?
`PngOptions` é uma classe que define as configurações de saída PNG, como tipo de cor e nível de compressão.  
`PngColorType.GrayscaleWithAlpha` é um valor de enumeração que armazena dados de escala de cinza de 16‑bits com um canal alfa.  

Carregue o PSD recém‑salvo, configure `PngOptions` com `PngColorType.GrayscaleWithAlpha` e chame `save`. Isso mantém os dados de escala de cinza de 16‑bits dentro do arquivo PNG, fornecendo uma imagem sem perdas e de alta qualidade, adequada para processamento ou distribuição adicional.

```java
finally {
    image.dispose();
}
// Load the saved PSD
PsdImage image1 = (PsdImage)Image.load(exportPath);
try {
    // Convert the saved PSD to a grayscale PNG image
    PngOptions pngOptions = new PngOptions();
    pngOptions.setColorType(PngColorType.GrayscaleWithAlpha);
    image1.save(pngExportPath, pngOptions); // here should be no exception
}
finally {
    image1.dispose();
}
```

Agora você exportou com sucesso **PSD como PNG** mantendo os dados de escala de cinza de 16‑bits de alta qualidade.

## Problemas comuns e soluções
| Problema | Por que acontece | Solução |
|----------|------------------|---------|
| **Exceção “Unsupported color type”** | Tentando salvar um PSD com uma configuração de canal não suportada. | Certifique‑se de que `channelBitsCount` corresponde à profundidade de bits real (16) e `channelsCount` está correto para escala de cinza (1). |
| **Arquivo não encontrado** | Caminho do diretório de origem incorreto. | Verifique novamente a string `sourceDir` e confirme que o arquivo PSD existe naquele local. |
| **PNG de saída aparece preto** | PNG salvo sem o tratamento adequado de alfa. | Use `PngColorType.GrayscaleWithAlpha` como mostrado acima. |
| **Estouro de memória em PSDs grandes** | Carregando o arquivo inteiro na memória. | Habilite o modo de streaming via `PsdImage.load(inputStream, new LoadOptions())` para processar arquivos grandes de forma eficiente. |

## Perguntas frequentes

**Q: O que é o modo de cor em escala de cinza de 16‑bits?**  
A: Ele fornece 65 536 tons de cinza, oferecendo muito mais detalhe tonal do que o padrão de 8‑bits (256 tons).

**Q: Posso usar Aspose.PSD para imagens que não sejam em escala de cinza?**  
A: Absolutamente! Aspose.PSD suporta RGB, CMYK, Lab, Indexed e muitos outros modos de cor.

**Q: Existe uma versão de avaliação do Aspose.PSD?**  
A: Sim, você pode experimentar uma versão de avaliação gratuita do Aspose.PSD. Basta acessar a [página de download da Aspose](https://releases.aspose.com/).

**Q: Onde posso encontrar mais exemplos do Aspose.PSD?**  
A: Consulte a [documentação oficial](https://reference.aspose.com/psd/java/) para tutoriais aprofundados, referências de API e projetos de exemplo.

**Q: Como comprar uma licença para Aspose.PSD?**  
A: Você pode adquirir uma licença visitando a [página de compra da Aspose](https://purchase.aspose.com/buy).

**Última atualização:** 2026-09-28  
**Testado com:** Aspose.PSD para Java 24.12 (mais recente no momento da escrita)  
**Autor:** Aspose

## Tutoriais Relacionados

- [Converter PSD para PNG com profundidade de bits especificada usando Aspose.PSD para Java](/psd/java/optimizing-png-files/specify-png-bit-depth/)
- [Exportar PSD para PNG com efeitos de camada usando Aspose.PSD para Java](/psd/java/psd-image-modification-conversion/apply-layer-effects-psd-files/)
- [Salvar PSD como JPEG e suportar cor RGB com Aspose.PSD Java](/psd/java/advanced-psd-layer-features-effects/support-rgb-color-psd-files/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}