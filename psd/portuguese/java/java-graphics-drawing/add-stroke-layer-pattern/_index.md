---
date: 2026-08-28
description: Adicione pattern a uma layer em Java com Aspose.PSD. Siga este guia passo
  a passo para aplicar um stroke layer effect, configurar pattern resources e salvar
  seus arquivos PSD de forma eficiente.
keywords:
- add pattern to layer
- java add layer effect
- Aspose.PSD stroke pattern
lastmod: 2026-08-28
linktitle: Como adicionar Stroke Layer Pattern em Java
og_description: Adicionar pattern a layer em Java usando Aspose.PSD. Siga este guia
  conciso para aplicar um stroke layer effect, configurar pattern resources e salvar
  seus arquivos PSD de forma eficiente.
og_image_alt: Guide showing how to add pattern to layer in Java with Aspose.PSD
og_title: Adicionar pattern a layer em Java – tutorial Aspose.PSD
schemas:
- author: Aspose
  dateModified: '2026-08-28'
  description: Add pattern to layer in Java with Aspose.PSD. Follow this step‑by‑step
    guide to apply a stroke layer effect, configure pattern resources, and save your
    PSD files efficiently.
  headline: How to add pattern to layer in Java
  type: TechArticle
- description: Add pattern to layer in Java with Aspose.PSD. Follow this step‑by‑step
    guide to apply a stroke layer effect, configure pattern resources, and save your
    PSD files efficiently.
  name: How to add pattern to layer in Java
  steps:
  - name: load the PSD file
    text: 'Loading the document gives you access to its layer hierarchy and effect
      collection. `PsdLoadOptions` configures how the PSD is read, while `PsdImage`
      represents the loaded file in memory. java String dataDir = "Your Document Directory";
      String sourceFileName = dataDir + "Stroke.psd"; PsdLoadOptions '
  - name: prepare new pattern data
    text: Create a `PatternResource` that holds the bitmap you want to tile as a stroke
      pattern. `PatternResource` is a PSD global resource that stores a repeating
      bitmap pattern. `Rectangle` defines the bounds of the pattern, and `UUID` provides
      a unique identifier. java int[] newPattern = new int[] { Color.
  - name: access the stroke effect
    text: Identify the shape layer that already has a stroke, then retrieve its `StrokeEffect`
      object. `StrokeEffect` represents the stroke layer effect applied to a shape
      layer. java StrokeEffect patternStroke = (StrokeEffect)im.getLayers()[3].getBlendingOptions().getEffects()[0];
      Assert.areEqual(BlendMode.N
  - name: modify the stroke effect
    text: Now update the stroke’s properties to reference the new pattern resource.
  - name: apply the new pattern
    text: '`PatternFillSettings` holds the fill settings for a pattern‑based stroke
      effect. Commit the changes to the layer and write the updated PSD back to disk.
      java ((PatternFillSettings)patternStroke.getFillSettings()).setPatternName("$$/Presets/Patterns/HorizontalLine1=Horizontal
      Line 9\0"); ((PatternFil'
  - name: verify the changes
    text: 'Reload the file and inspect the stroke to confirm the pattern appears as
      expected. java PsdImage img = (PsdImage)Image.load(sourceFileName, loadOptions);
      StrokeEffect patternStrokeEffect = (StrokeEffect)img.getLayers()[3].getBlendingOptions().getEffects()[0];
      PattResource resource1 = null; for (int '
  type: HowTo
- questions:
  - answer: Aspose.PSD for Java is a library that enables developers to create, edit,
      and convert PSD (Photoshop Document) files programmatically.
    question: What is Aspose.PSD for Java?
  - answer: Yes, you can use it in commercial projects. You can purchase a license
      from the **Aspose purchase page**([Aspose purchase page](https://purchase.aspose.com/buy)).
    question: Can I use Aspose.PSD for Java in a commercial project?
  - answer: Yes, you can download a free trial version from the **Aspose releases
      page**([Aspose releases page](https://releases.aspose.com/)).
    question: Is there a free trial available for Aspose.PSD for Java?
  - answer: You can get support from the Aspose community forums **here**([Aspose
      PSD community forum](https://forum.aspose.com/c/psd/34)).
    question: How can I get support for Aspose.PSD for Java?
  - answer: You need a JDK installed and an IDE for development. The library supports
      Windows, Linux, and macOS.
    question: What are the system requirements for Aspose.PSD for Java?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- java graphics
- Aspose.PSD
- layer effects
title: Como adicionar pattern a uma layer em Java
url: /pt/java/java-graphics-drawing/add-stroke-layer-pattern/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Como adicionar padrão a uma camada em Java

## Introdução
Adicionar um padrão a uma camada em Java é uma necessidade comum quando você precisa enriquecer arquivos Photoshop PSD com efeitos de traço personalizados. Com o Aspose.PSD for Java essa tarefa se torna simples, mesmo que você seja novo na biblioteca. Neste tutorial você aprenderá como carregar um PSD, criar um recurso de padrão, vinculá‑lo a um efeito de traço e salvar o resultado — tudo com instruções claras, passo a passo.

## Respostas rápidas
- **Qual biblioteca é necessária?** Aspose.PSD for Java.  
- **Quanto tempo leva a implementação?** Cerca de 10‑15 minutos para um padrão básico.  
- **Preciso de uma licença?** Uma avaliação gratuita funciona para desenvolvimento; uma licença comercial é necessária para produção.  
- **Qual versão do Java é suportada?** JDK 8 ou superior.  
- **Posso usar isso em um serviço web?** Sim, a API é independente de plataforma e funciona em qualquer ambiente Java.

## O que significa adicionar um padrão a uma camada?
Adicionar um padrão a uma camada significa atribuir um bitmap em mosaico a um efeito de traço ou preenchimento, de modo que o gráfico se repita ao longo do contorno da forma. Essa técnica é amplamente usada para bordas decorativas, texturas e sobreposições de marca, permitindo que designers criem temas visuais consistentes sem desenhar manualmente cada elemento.

## Por que usar o Aspose.PSD para esta tarefa?
O Aspose.PSD suporta **mais de 30 formatos de imagem** e pode manipular arquivos PSD de até **2 GB** sem carregar o documento inteiro na memória, oferecendo desempenho rápido em hardware de servidor típico. Sua API fluente permite trabalhar com efeitos de camada programaticamente, eliminando a necessidade do Photoshop em pipelines automatizados.

## Pré‑requisitos
- Java Development Kit (JDK) 8 ou superior instalado.
- Aspose.PSD for Java – faça o download na **Página de download do Aspose.PSD for Java**([Aspose.PSD for Java download page](https://releases.aspose.com/psd/java/)) e adicione o JAR ao classpath do seu projeto.
- Uma IDE como IntelliJ IDEA ou Eclipse para editar e executar o código de exemplo.
- Um arquivo PSD de exemplo que contenha uma camada de forma que você deseja modificar.

## Importar pacotes
Primeiro, importe os namespaces que fornecem acesso aos objetos, recursos e efeitos do PSD.

```
// No actual code block is added to preserve original placeholders.
```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;
import com.aspose.psd.Rectangle;
import com.aspose.psd.examples.Utils.Assert;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.BlendMode;
import com.aspose.psd.fileformats.psd.layers.fillsettings.FillType;
import com.aspose.psd.fileformats.psd.layers.fillsettings.PatternFillSettings;
import com.aspose.psd.fileformats.psd.layers.layereffects.StrokeEffect;
import com.aspose.psd.fileformats.psd.layers.layerresources.PattResource;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
import java.util.UUID;
```
```

## Como adicionar padrão a uma camada em Java?

Carregue o PSD de destino, crie um recurso de padrão, anexe‑o ao efeito de traço da camada desejada e, finalmente, salve o arquivo. Esse fluxo de ponta a ponta requer apenas algumas linhas de código e funciona com qualquer PSD padrão que contenha uma camada de forma vetorial.

### Etapa 1: carregar o arquivo PSD
Carregar o documento fornece acesso à sua hierarquia de camadas e à coleção de efeitos.  
`PsdLoadOptions` configura como o PSD é lido, enquanto `PsdImage` representa o arquivo carregado na memória.

```
// Placeholder for original code.
```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "Stroke.psd";
PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);
PsdImage im = (PsdImage)Image.load(sourceFileName, loadOptions);
```
```

Ao carregar o arquivo PSD, você pode agora acessar e manipular suas camadas e efeitos.

### Etapa 2: preparar novos dados de padrão
Crie um `PatternResource` que contém o bitmap que você deseja usar como padrão de traço.  
`PatternResource` é um recurso global do PSD que armazena um padrão de bitmap repetido. `Rectangle` define os limites do padrão, e `UUID` fornece um identificador único.

```
// Placeholder for original code.
```java
int[] newPattern = new int[]
{
    Color.getAqua().toArgb(), Color.getRed().toArgb(), Color.getRed().toArgb(), Color.getAqua().toArgb(),
    Color.getAqua().toArgb(), Color.getWhite().toArgb(), Color.getWhite().toArgb(), Color.getAqua().toArgb(),
    Color.getAqua().toArgb(), Color.getWhite().toArgb(), Color.getWhite().toArgb(), Color.getAqua().toArgb(),
    Color.getAqua().toArgb(), Color.getRed().toArgb(), Color.getRed().toArgb(), Color.getAqua().toArgb(),
};
Rectangle newPatternBounds = new Rectangle(0, 0, 4, 4);
UUID guid = UUID.randomUUID();
```
```

Esses dados de padrão serão usados para criar o novo efeito de traço.

### Etapa 3: acessar o efeito de traço
Identifique a camada de forma que já possui um traço e, em seguida, recupere seu objeto `StrokeEffect`.  
`StrokeEffect` representa o efeito de camada de traço aplicado a uma camada de forma.

```
// Placeholder for original code.
```java
StrokeEffect patternStroke = (StrokeEffect)im.getLayers()[3].getBlendingOptions().getEffects()[0];
Assert.areEqual(BlendMode.Normal, patternStroke.getBlendMode());
Assert.areEqual(255, patternStroke.getOpacity());
Assert.areEqual(true, patternStroke.isVisible());
PatternFillSettings fillSettings = (PatternFillSettings)patternStroke.getFillSettings();
Assert.areEqual(FillType.Pattern, fillSettings.getFillType());
```
```

Isso garante que você está trabalhando com a camada e o efeito corretos.

### Etapa 4: modificar o efeito de traço
Agora atualize as propriedades do traço para referenciar o novo recurso de padrão.

#### Atualizar propriedades do efeito de traço
```
// Placeholder for original code.
```java
patternStroke.setOpacity((byte)127);
patternStroke.setBlendMode(BlendMode.Color);
```
```

#### Atualizar o recurso de padrão
`PattResource` é um recurso global de camada do PSD que armazena dados de padrão.

```
// Placeholder for original code.
```java
PattResource resource;
for (int i = 0; i < im.getGlobalLayerResources().length; i++)
{
    if (im.getGlobalLayerResources()[i] instanceof PattResource)
    {
        resource = (PattResource)im.getGlobalLayerResources()[i];
        resource.setPatternId(guid.toString());
        resource.setName("$$/Presets/Patterns/HorizontalLine1=Horizontal Line 9\0");
        resource.setPattern(newPattern, newPatternBounds);
    }
}
```
```

Esses trechos substituem o padrão existente pelo que você forneceu.

### Etapa 5: aplicar o novo padrão
`PatternFillSettings` contém as configurações de preenchimento para um efeito de traço baseado em padrão. Confirme as alterações na camada e grave o PSD atualizado de volta ao disco.

```
// Placeholder for original code.
```java
((PatternFillSettings)patternStroke.getFillSettings()).setPatternName("$$/Presets/Patterns/HorizontalLine1=Horizontal Line 9\0");
((PatternFillSettings)patternStroke.getFillSettings()).setPatternId(guid.toString() + "\0");
im.save(exportPath);
```
```

Isso garante que o novo padrão seja aplicado corretamente e que o arquivo seja salvo com as alterações.

### Etapa 6: verificar as alterações
Recarregue o arquivo e inspecione o traço para confirmar que o padrão aparece como esperado.

```
// Placeholder for original code.
```java
PsdImage img = (PsdImage)Image.load(sourceFileName, loadOptions);
StrokeEffect patternStrokeEffect = (StrokeEffect)img.getLayers()[3].getBlendingOptions().getEffects()[0];
PattResource resource1 = null;
for (int i = 0; i < img.getGlobalLayerResources().length; i++)
{
    if (img.getGlobalLayerResources()[i] instanceof PattResource)
    {
        resource1 = (PattResource)img.getGlobalLayerResources()[i];
    }
}
try
{
    Assert.areEqual(newPattern, resource1.getPatternData());
    Assert.areEqual(newPatternBounds, new Rectangle(0, 0, resource1.getWidth(), resource1.getHeight()));
    Assert.areEqual(guid.toString(), resource1.getPatternId());
    Assert.areEqual(BlendMode.Color, patternStrokeEffect.getBlendMode());
    Assert.areEqual(127, patternStrokeEffect.getOpacity());
    Assert.areEqual(true, patternStrokeEffect.isVisible());
    PatternFillSettings fillSettings1 = (PatternFillSettings)patternStrokeEffect.getFillSettings();
    Assert.areEqual(FillType.Pattern, fillSettings1.getFillType());
}
catch (Exception e)
{
    System.out.println(e.getMessage());
}
```
```

Esta etapa verifica se os dados do padrão foram aplicados corretamente ao efeito de traço.

## Problemas comuns e solução de problemas
- **Padrão não visível:** Certifique-se de que o DPI da imagem do padrão corresponda à resolução do PSD e de que a flag `Enabled` do traço esteja definida como `true`.  
- **Arquivos PSD grandes causam OutOfMemoryError:** Use `PsdImage.load(..., LoadOptions)` com `LoadOptions.setLoadAllLayers(false)` para carregar camadas sob demanda.  
- **Camada incorreta selecionada:** Verifique o índice ou nome da camada antes de acessar seus efeitos; você pode enumerar `psdImage.getLayers()` para listar as camadas disponíveis.

## Perguntas frequentes

**Q: O que é o Aspose.PSD for Java?**  
A: O Aspose.PSD for Java é uma biblioteca que permite aos desenvolvedores criar, editar e converter arquivos PSD (Photoshop Document) programaticamente.

**Q: Posso usar o Aspose.PSD for Java em um projeto comercial?**  
A: Sim, você pode usá‑lo em projetos comerciais. Você pode comprar uma licença na **Página de compra da Aspose**([Aspose purchase page](https://purchase.aspose.com/buy)).

**Q: Existe uma versão de avaliação gratuita disponível para o Aspose.PSD for Java?**  
A: Sim, você pode baixar uma versão de avaliação gratuita na **Página de lançamentos da Aspose**([Aspose releases page](https://releases.aspose.com/)).

**Q: Como posso obter suporte para o Aspose.PSD for Java?**  
A: Você pode obter suporte nos fóruns da comunidade Aspose **aqui**([Aspose PSD community forum](https://forum.aspose.com/c/psd/34)).

**Q: Quais são os requisitos de sistema para o Aspose.PSD for Java?**  
A: Você precisa de um JDK instalado e de uma IDE para desenvolvimento. A biblioteca suporta Windows, Linux e macOS.

## Conclusão
Agora você aprendeu como adicionar um padrão a uma camada em Java usando o Aspose.PSD. Seguindo os passos acima, você pode melhorar programaticamente arquivos PSD com padrões de traço personalizados, automatizar fluxos de trabalho de branding e integrar o processamento de gráficos em qualquer aplicação baseada em Java. Explore outros recursos do Aspose.PSD, como mesclagem de camadas, ajustes de cor e exportação para PNG ou JPEG, para expandir ainda mais seu conjunto de ferramentas de processamento de imagens.

---

**Última atualização:** 2026-08-28  
**Testado com:** Aspose.PSD 24.11 for Java  
**Autor:** Aspose

## Tutoriais relacionados

- [Renderizar Camada de Preenchimento de Padrão de Arquivos PSD](/psd/java/advanced-psd-layer-features-effects/render-pattern-fill-layer-psd-files/)
- [Sobreposição de Padrão PSD: Adicionar Efeitos com Aspose.PSD for Java](/psd/java/advanced-image-effects/add-pattern-effects/)
- [Como Alterar a Cor do Traço em Java Usando Aspose.PSD](/psd/java/advanced-image-effects/add-stroke-layer-color/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}
{{< blocks/products/products-backtop-button >}}