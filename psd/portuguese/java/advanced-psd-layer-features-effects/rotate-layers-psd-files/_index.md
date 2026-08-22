---
date: 2026-07-22
description: Aprenda como salvar psd como png, preservar a transparência PNG e girar
  camadas PSD em Java com Aspose.PSD. Guia passo a passo, explicações sem código e
  dicas de solução de problemas.
keywords:
- save psd as png
- export psd layers png
- convert photoshop file png
- psd to png transparency
lastmod: 2026-07-22
linktitle: salvar psd como png e girar camadas em Java usando Aspose.PSD
og_description: salvar psd como png com Aspose.PSD para Java. Preserve a transparência,
  gire camadas e exporte PNG em apenas algumas linhas de código — ideal para fluxos
  de trabalho automatizados.
og_image_alt: 'Developer guide: save PSD as PNG and rotate layers using Aspose.PSD
  for Java'
og_title: salvar psd como png e girar camadas em Java usando Aspose.PSD
schemas:
- author: Aspose
  dateModified: '2026-07-22'
  description: Learn how to save psd as png, preserve PNG transparency, and rotate
    PSD layers in Java with Aspose.PSD. Step‑by‑step guide, code‑free explanations,
    and troubleshooting tips.
  headline: save psd as png and rotate layers in Java using Aspose.PSD
  type: TechArticle
- description: Learn how to save psd as png, preserve PNG transparency, and rotate
    PSD layers in Java with Aspose.PSD. Step‑by‑step guide, code‑free explanations,
    and troubleshooting tips.
  name: save psd as png and rotate layers in Java using Aspose.PSD
  steps:
  - name: Set Up Your Java Project
    text: Create a new Java project in your IDE and add the Aspose.PSD JAR to the
      project’s build path.
  - name: Import Required Classes
    text: '`PsdImage` is the core class that represents a Photoshop document in memory.
      `PngOptions` controls PNG‑specific settings, and `RotateFlipType` defines rotation
      and flip operations. These imports give you access to image loading, rotation,
      and PNG‑specific options.'
  - name: Define File Paths
    text: Specify where your source PSD lives and where the output files should be
      written. Using absolute paths during testing avoids “file not found” errors.
      > **Pro tip:** Store paths in a configuration file for easier maintenance in
      larger projects.
  - name: Load the PSD File
    text: '`PsdImage` loads the entire Photoshop document, including all layers, masks,
      and effects, into a manipulable object. Now `im` represents the whole PSD, ready
      for transformations.'
  - name: Rotate the Image (How to rotate PSD)
    text: '`RotateFlipType` enumerates all supported rotations and flips. In this
      example we rotate 270° and flip both axes, which swaps width and height while
      mirroring the image. Feel free to experiment with other values such as `Rotate90FlipNone`
      or `Rotate180FlipX`.'
  - name: Save the Rotated Image as PNG (save PSD as PNG)
    text: Configure `PngOptions` to keep transparency (`PngColorType.TruecolorWithAlpha`)
      and then call `save`. The PNG retains layer transparency, ensuring it works
      seamlessly in web or mobile apps. The resulting PNG preserves alpha channels,
      making it suitable for compositing or further processing.
  - name: Save the Modified PSD (optional)
    text: If you also need a new PSD with the rotation applied, you can save the modified
      `PsdImage` back to disk. You now have both a PNG preview and an updated PSD
      file.
  type: HowTo
- questions:
  - answer: Yes, you can call `layer.rotateFlip(RotateFlipType.Rotate90FlipNone)`
      after iterating through `im.getLayers()`.
    question: Can I rotate a specific layer in a PSD file?
  - answer: The library handles most files efficiently, but extremely large PSDs (>500
      MB) may require additional memory or streaming options.
    question: Is there any performance limitation with Aspose.PSD for Java?
  - answer: Aspose offers a free trial, but a paid license is needed for production.
      See the [temporary license](https://purchase.aspose.com/temporary-license/)
      for testing.
    question: Is Aspose.PSD free to use?
  - answer: Comprehensive docs are available at [Aspose.PSD Documentation](https://reference.aspose.com/psd/java/).
    question: Where can I find detailed documentation?
  - answer: Get help via the [Aspose Support Forum](https://forum.aspose.com/c/psd/34).
    question: What if I encounter issues while using Aspose.PSD?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- convert PSD
- Aspose.PSD
- Java image processing
- rotate PSD layers
title: salvar psd como png e girar camadas em Java usando Aspose.PSD
url: /pt/java/advanced-psd-layer-features-effects/rotate-layers-psd-files/
weight: 21
---

## Tutoriais Relacionados

- [Salvar PSD como PNG e Aplicar Sombra de Renderização em Aspose.PSD para Java](/psd/java/advanced-image-manipulation/rendering-drop-shadow/)
- [Como compactar arquivos PNG usando Aspose.PSD para Java](/psd/java/optimizing-png-files/compress-png-files/)
- [Como Rotacionar Imagem em Java com Aspose.PSD](/psd/java/advanced-image-manipulation/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< blocks/products/pf/main-wrap-class >}}

# salvar psd como png e girar camadas em Java usando Aspose.PSD

## Introdução
Se você precisa **salvar PSD como PNG** enquanto também gira camadas, este guia é para você. Seja construindo uma ferramenta de processamento em lote, um serviço web que necessita de manipulação de imagens em tempo real, ou simplesmente automatizando um fluxo de trabalho de design, fazer isso programaticamente economiza tempo e elimina a dependência do Adobe Photoshop. Neste tutorial, vamos percorrer **como girar camadas PSD** e exportar o resultado como PNG usando a biblioteca Aspose.PSD para Java. Vamos arregaçar as mangas e fazer seu fluxo de trabalho de design funcionar sem problemas!

## Respostas Rápidas
- **Qual biblioteca posso usar?** Aspose.PSD for Java  
- **Posso girar e salvar PSD como PNG de uma só vez?** Sim – gire o PSD e depois salve como PNG  
- **Preciso de licença?** Uma avaliação gratuita funciona para testes; uma licença paga é necessária para produção  
- **Qual versão do Java é suportada?** Java 8 e posteriores  
- **A saída PNG é transparente?** Sim, quando você define `PngColorType.TruecolorWithAlpha`

## O que é “converter PSD para PNG”?
Converter um documento Photoshop (PSD) para uma imagem PNG extrai o conteúdo visual — incluindo camadas, máscaras e canais alfa — para um formato raster amplamente suportado que preserva a transparência. Isso torna o PNG ideal para gráficos web, miniaturas e processamento de imagens subsequente. O PNG resultante pode ser usado diretamente em páginas web, aplicativos móveis ou processado adicionalmente por outras bibliotecas de imagem.

## Por que usar Aspose.PSD para Java para salvar PSD como PNG e girar camadas PSD?
Aspose.PSD permite que você **salve PSD como PNG** e gire camadas sem instalar o Photoshop. Ele suporta **mais de 50 formatos de entrada e saída**, processa arquivos PSD de várias centenas de páginas usando menos de 200 MB de RAM, e funciona no Windows, Linux e macOS. A API requer apenas algumas chamadas de método, entregando resultados de alta fidelidade com tratamento interno de efeitos de camada, máscaras e canais alfa.

## Pré-requisitos
Antes de mergulharmos no código, certifique‑se de que você tem o seguinte:

- **Java Development Kit (JDK)** – faça o download no [site da Oracle](https://www.oracle.com/java/technologies/javase-downloads.html).  
- **Ambiente de Desenvolvimento Integrado (IDE)** – IntelliJ IDEA, Eclipse ou NetBeans são todos adequados.  
- **Biblioteca Aspose.PSD para Java** – obtenha o JAR mais recente na [página de lançamentos](https://releases.aspose.com/psd/java/).  
- **Conhecimento básico de Java** – familiaridade com classes, objetos e tratamento de exceções.

## Guia Passo a Passo

### Etapa 1: Configurar Seu Projeto Java
Crie um novo projeto Java em sua IDE e adicione o JAR do Aspose.PSD ao caminho de compilação do projeto.

### Etapa 2: Importar Classes Necessárias
`PsdImage` é a classe central que representa um documento Photoshop na memória. `PngOptions` controla as configurações específicas de PNG, e `RotateFlipType` define as operações de rotação e espelhamento.

```java
import com.aspose.psd.Image;
import com.aspose.psd.RotateFlipType;
import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.PngOptions;
```

Essas importações dão acesso ao carregamento de imagens, rotação e opções específicas de PNG.

### Etapa 3: Definir Caminhos de Arquivo
Especifique onde seu PSD de origem está localizado e onde os arquivos de saída devem ser gravados. Usar caminhos absolutos durante os testes evita erros de “arquivo não encontrado”.

```java
String dataDir = "Your Document Directory"; // Change this to your actual document directory.
String sourceFile = dataDir + "1.psd"; // Source PSD file
String pngPath = dataDir + "RotateFlipTest2617.png"; // Output PNG file path
String psdPath = dataDir + "RotateFlipTest2617.psd"; // Output PSD file path
```

> **Dica profissional:** Armazene os caminhos em um arquivo de configuração para facilitar a manutenção em projetos maiores.

### Etapa 4: Carregar o Arquivo PSD
`PsdImage` carrega todo o documento Photoshop, incluindo todas as camadas, máscaras e efeitos, em um objeto manipulável.

```java
PsdImage im = (PsdImage) Image.load(sourceFile);
```

Agora `im` representa todo o PSD, pronto para transformações.

### Etapa 5: Rotacionar a Imagem (Como girar PSD)
`RotateFlipType` enumera todas as rotações e espelhamentos suportados. Neste exemplo giramos 270° e espelhamos ambos os eixos, o que troca largura e altura enquanto espelha a imagem.

```java
int flipType = RotateFlipType.Rotate270FlipXY; // Choose the rotation type
im.rotateFlip(flipType); // Rotate the image
```

Sinta‑se à vontade para experimentar outros valores, como `Rotate90FlipNone` ou `Rotate180FlipX`.

### Etapa 6: Salvar a Imagem Rotacionada como PNG (salvar PSD como PNG)
Configure `PngOptions` para manter a transparência (`PngColorType.TruecolorWithAlpha`) e então chame `save`. O PNG mantém a transparência das camadas, garantindo que funcione perfeitamente em aplicativos web ou móveis.

```java
PngOptions options = new PngOptions();
options.setColorType(PngColorType.TruecolorWithAlpha); // Preserve transparency
im.save(pngPath, options); // Save the rotated image
```

O PNG resultante preserva os canais alfa, tornando‑o adequado para composição ou processamento adicional.

### Etapa 7: Salvar o PSD Modificado (opcional)
Se você também precisar de um novo PSD com a rotação aplicada, pode salvar o `PsdImage` modificado de volta ao disco.

```java
im.save(psdPath);
```

Agora você tem tanto uma pré‑visualização PNG quanto um arquivo PSD atualizado.

## Problemas Comuns e Soluções
- **Arquivo não encontrado:** Verifique se `dataDir` termina com um separador de caminho (`/` ou `\`).  
- **OutOfMemoryError em PSDs grandes:** Aumente o tamanho do heap da JVM (`-Xmx2g`).  
- **Transparência perdida:** Certifique‑se de que `PngColorType.TruecolorWithAlpha` está definido; caso contrário o PNG será salvo sem alfa.  
- **Imagem PSD espelhada não se comporta como esperado:** Verifique novamente a constante `RotateFlipType` selecionada; algumas constantes combinam rotação e espelhamento em um único passo.

## Perguntas Frequentes

**Q: Posso girar uma camada específica em um arquivo PSD?**  
A: Sim, você pode chamar `layer.rotateFlip(RotateFlipType.Rotate90FlipNone)` após iterar por `im.getLayers()`.

**Q: Existe alguma limitação de desempenho com Aspose.PSD para Java?**  
A: A biblioteca lida com a maioria dos arquivos de forma eficiente, mas PSDs extremamente grandes (>500 MB) podem exigir memória adicional ou opções de streaming.

**Q: O Aspose.PSD é gratuito para uso?**  
A: A Aspose oferece uma avaliação gratuita, mas uma licença paga é necessária para produção. Veja a [licença temporária](https://purchase.aspose.com/temporary-license/) para testes.

**Q: Onde posso encontrar documentação detalhada?**  
A: Documentação completa está disponível em [Aspose.PSD Documentation](https://reference.aspose.com/psd/java/).

**Q: O que fazer se eu encontrar problemas ao usar Aspose.PSD?**  
A: Obtenha ajuda através do [Fórum de Suporte da Aspose](https://forum.aspose.com/c/psd/34).

**Q: A conversão de PSD para PNG preserva efeitos de camada?**  
A: Sim, ao salvar com `PngColorType.TruecolorWithAlpha`, a maioria dos efeitos visuais são rasterizados no PNG.

**Q: Posso processar em lote vários arquivos PSD?**  
A: Absolutamente. Envolva o código em um loop que itere sobre um diretório de arquivos PSD.

**Q: É possível definir o nível de compressão PNG?**  
A: `PngOptions` fornece o método `setCompressionLevel(int)` para ajuste fino do tamanho de saída.

**Q: Preciso fechar o objeto de imagem?**  
A: `PsdImage` implementa `Closeable`; use try‑with‑resources ou chame `im.close()` em um bloco `finally`.

**Q: O PNG rotacionado terá as mesmas dimensões do original?**  
A: Rotacionar 90° ou 270° troca largura e altura, portanto o PNG reflete a nova orientação automaticamente.

## Conclusão
Ao aproveitar o Aspose.PSD para Java, você pode **salvar PSD como PNG**, **preservar a transparência do PNG** e **girar camadas PSD** com apenas algumas linhas de código. Essa abordagem elimina a necessidade do Photoshop, acelera fluxos de trabalho automatizados e lhe dá controle total sobre a saída de imagens. Experimente em seus próprios projetos e veja quanto tempo você economiza!

---

**Última atualização:** 2026-07-22  
**Testado com:** Aspose.PSD for Java 24.11  
**Autor:** Aspose  

{{< blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/products-backtop-button >}}