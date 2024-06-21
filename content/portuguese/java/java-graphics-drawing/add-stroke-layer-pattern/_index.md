---
title: Como adicionar padrão de camada de traço em Java
linktitle: Como adicionar padrão de camada de traço em Java
second_title: API Java Aspose.PSD
description: Aprenda como adicionar um padrão de camada de traço a arquivos PSD usando Aspose.PSD para Java. Siga este guia passo a passo para aprimorar suas imagens facilmente.
type: docs
weight: 11
url: /pt/java/java-graphics-drawing/add-stroke-layer-pattern/
---
## Introdução
Adicionar um padrão de camada de traço a uma imagem em Java pode parecer uma tarefa difícil, mas com Aspose.PSD para Java é mais fácil do que você pensa. Esteja você projetando gráficos ou trabalhando em aplicativos de edição de fotos, este guia irá guiá-lo passo a passo pelo processo. Pronto para começar? Vamos mergulhar!
## Pré-requisitos
Antes de começar, você precisará de algumas coisas:
- Java Development Kit (JDK): Certifique-se de ter o JDK instalado em seu sistema.
-  Aspose.PSD para Java: Baixe a biblioteca em[aqui](https://releases.aspose.com/psd/java/) e inclua-o em seu projeto.
- Um IDE: Use seu ambiente de desenvolvimento integrado (IDE) favorito, como IntelliJ IDEA ou Eclipse.
## Importar pacotes
Primeiramente, você precisa importar os pacotes necessários para o seu projeto Java. Esses pacotes são essenciais para trabalhar com Aspose.PSD.
```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;
import com.aspose.psd.Rectangle;
import com.aspose.psd.examples.Utils.Assert;
import com.aspose.psd.examples.Utils.Utils;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.BlendMode;
import com.aspose.psd.fileformats.psd.layers.fillsettings.FillType;
import com.aspose.psd.fileformats.psd.layers.fillsettings.PatternFillSettings;
import com.aspose.psd.fileformats.psd.layers.layereffects.StrokeEffect;
import com.aspose.psd.fileformats.psd.layers.layerresources.PattResource;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
import java.util.UUID;
```
## Passo 1: Carregue o arquivo PSD
A primeira etapa para adicionar um padrão de camada de traçado é carregar o arquivo PSD que deseja editar.
```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "Stroke.psd";
PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);
PsdImage im = (PsdImage)Image.load(sourceFileName, loadOptions);
```
Ao carregar o arquivo PSD, agora você pode acessar e manipular suas camadas e efeitos.
## Etapa 2: preparar novos dados de padrão
Em seguida, você precisa preparar os novos dados de padrão que serão aplicados à camada do traço.
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
Esses dados de padrão serão usados para criar o novo efeito de traçado.
## Etapa 3: acesse o efeito do traço
Para modificar o efeito do traço, você precisa acessar a camada específica e suas opções de mesclagem.
```java
StrokeEffect patternStroke = (StrokeEffect)im.getLayers()[3].getBlendingOptions().getEffects()[0];
Assert.areEqual(BlendMode.Normal, patternStroke.getBlendMode());
Assert.areEqual(255, patternStroke.getOpacity());
Assert.areEqual(true, patternStroke.isVisible());
PatternFillSettings fillSettings = (PatternFillSettings)patternStroke.getFillSettings();
Assert.areEqual(FillType.Pattern, fillSettings.getFillType());
```
Isso garante que você esteja trabalhando com a camada e o efeito corretos.
## Etapa 4: modificar o efeito do traço
Agora, vamos modificar o efeito do traço com os novos dados do padrão.
### Atualizar propriedades do efeito do traço
```java
patternStroke.setOpacity((byte)127);
patternStroke.setBlendMode(BlendMode.Color);
```
### Atualizar o recurso padrão
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
Este trecho de código atualiza o recurso padrão com os novos dados padrão.
## Etapa 5: aplique o novo padrão
Por fim, aplique o novo padrão ao efeito do traço e salve as alterações.
```java
((PatternFillSettings)patternStroke.getFillSettings()).setPatternName("$$/Presets/Patterns/HorizontalLine1=Horizontal Line 9\0");
((PatternFillSettings)patternStroke.getFillSettings()).setPatternId(guid.toString() + "\0");
im.save(exportPath);
```
Isso garante que o novo padrão seja aplicado corretamente e que o arquivo seja salvo com as alterações.
## Etapa 6: verifique as alterações
Para ter certeza de que tudo funcionou corretamente, carregue o arquivo novamente e verifique as alterações.
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
Esta etapa verifica se os dados do padrão foram aplicados corretamente ao efeito do traçado.
## Conclusão
E aí está! Você adicionou com sucesso um padrão de camada de traço a um arquivo PSD usando Aspose.PSD para Java. Seguindo essas etapas, você pode personalizar e aprimorar suas imagens com facilidade. Boa codificação!
## Perguntas frequentes
### O que é Aspose.PSD para Java?
Aspose.PSD para Java é uma biblioteca que permite aos desenvolvedores criar, editar e converter arquivos PSD (documento do Photoshop) programaticamente.
### Posso usar Aspose.PSD para Java em um projeto comercial?
 Sim, você pode usá-lo em projetos comerciais. Você pode comprar uma licença de[aqui](https://purchase.aspose.com/buy).
### Existe uma avaliação gratuita disponível para Aspose.PSD para Java?
 Sim, você pode baixar uma versão de avaliação gratuita em[aqui](https://releases.aspose.com/).
### Como posso obter suporte para Aspose.PSD para Java?
 Você pode obter suporte nos fóruns da comunidade Aspose[aqui](https://forum.aspose.com/c/psd/34).
### Quais são os requisitos de sistema para Aspose.PSD para Java?
Você precisa do JDK instalado e de um IDE para desenvolvimento. A biblioteca oferece suporte a vários sistemas operacionais, incluindo Windows, Linux e macOS.