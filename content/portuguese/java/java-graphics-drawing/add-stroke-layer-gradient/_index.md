---
title: Como adicionar gradiente de camada de traço em Java
linktitle: Como adicionar gradiente de camada de traço em Java
second_title: API Java Aspose.PSD
description: Aprenda como adicionar e personalizar gradientes de camada de traçado em arquivos PSD usando Aspose.PSD para Java com este tutorial passo a passo abrangente.
type: docs
weight: 10
url: /pt/java/java-graphics-drawing/add-stroke-layer-gradient/
---
## Introdução
Já se perguntou como adicionar um gradiente de camada de traço às suas imagens usando Java? Bem, você está no lugar certo! Hoje estamos mergulhando no mundo do Aspose.PSD para Java, uma biblioteca poderosa que ajuda você a manipular arquivos PSD com facilidade. Quer você seja um desenvolvedor iniciante ou experiente, este guia passo a passo irá orientá-lo no processo de adição de um gradiente de camada de traço aos seus arquivos PSD. Então, aperte o cinto e prepare-se para aprimorar suas habilidades de edição gráfica!
## Pré-requisitos
Antes de começarmos, há algumas coisas que você precisa ter em mente. Certifique-se de ter o seguinte:
1.  Kit de desenvolvimento Java (JDK): certifique-se de ter o JDK instalado em seu sistema. Você pode baixá-lo em[Site da Oracle](https://www.oracle.com/java/technologies/javase-downloads.html).
2.  Biblioteca Aspose.PSD para Java: você pode baixá-lo em[Página de download do Aspose.PSD](https://releases.aspose.com/psd/java/).
3. Um Ambiente de Desenvolvimento Integrado (IDE): Qualquer IDE como IntelliJ IDEA, Eclipse ou NetBeans funcionará.
4.  Uma licença válida: você pode obter uma[licença temporária](https://purchase.aspose.com/temporary-license/) se você não tiver um completo.
## Importar pacotes
Primeiramente, vamos importar os pacotes necessários. Isso nos permitirá usar as classes e métodos necessários para manipular o arquivo PSD.
```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;
import com.aspose.psd.examples.Utils.Assert;
import com.aspose.psd.examples.Utils.Utils;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.BlendMode;
import com.aspose.psd.fileformats.psd.layers.IGradientColorPoint;
import com.aspose.psd.fileformats.psd.layers.fillsettings.FillType;
import com.aspose.psd.fileformats.psd.layers.fillsettings.GradientColorPoint;
import com.aspose.psd.fileformats.psd.layers.fillsettings.GradientFillSettings;
import com.aspose.psd.fileformats.psd.layers.fillsettings.GradientTransparencyPoint;
import com.aspose.psd.fileformats.psd.layers.fillsettings.GradientType;
import com.aspose.psd.fileformats.psd.layers.fillsettings.IGradientTransparencyPoint;
import com.aspose.psd.fileformats.psd.layers.layereffects.StrokeEffect;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
```
Agora, vamos dividir o exemplo em várias etapas para melhor compreensão.
## Passo 1: Carregue o arquivo PSD
 Primeiro precisamos carregar o arquivo PSD que queremos modificar. Usaremos o`PsdLoadOptions` para especificar que queremos carregar os recursos de efeitos.
```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "Stroke.psd";
String exportPath = dataDir + "StrokeGradientChanged.psd";
PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);
PsdImage im = (PsdImage) Image.load(sourceFileName, loadOptions);
```
## Passo 2: Acesse o efeito Stroke
Em seguida, precisamos acessar o efeito de traço da camada que nos interessa. Aqui, assumimos que é a terceira camada (índice 2) no arquivo PSD.
```java
StrokeEffect gradientStroke = (StrokeEffect) im.getLayers()[2].getBlendingOptions().getEffects()[0];
```
## Etapa 3: verificar as propriedades do efeito do traço
Antes de fazer qualquer alteração, vamos verificar as propriedades do efeito do traço para garantir que estamos modificando as configurações corretas.
```java
Assert.areEqual(BlendMode.Normal, gradientStroke.getBlendMode());
Assert.areEqual(255, gradientStroke.getOpacity());
Assert.areEqual(true, gradientStroke.isVisible());
GradientFillSettings fillSettings = (GradientFillSettings) gradientStroke.getFillSettings();
Assert.areEqual(Color.getBlack(), fillSettings.getColor());
Assert.areEqual(FillType.Gradient, fillSettings.getFillType());
Assert.areEqual(true, fillSettings.getAlignWithLayer());
Assert.areEqual(GradientType.Linear, fillSettings.getGradientType());
Assert.isTrue(Math.abs(90 - fillSettings.getAngle()) < 0.001, "Angle is incorrect");
Assert.areEqual(false, fillSettings.getDither());
Assert.isTrue(Math.abs(0 - fillSettings.getHorizontalOffset()) < 0.001, "Horizontal offset is incorrect");
Assert.isTrue(Math.abs(0 - fillSettings.getVerticalOffset()) < 0.001, "Vertical offset is incorrect");
Assert.areEqual(false, fillSettings.getReverse());
```
## Etapa 4: modificar as configurações de preenchimento gradiente
Agora é hora de modificar as configurações de preenchimento gradiente de acordo com nossos requisitos. Alteraremos a cor, a opacidade, o modo de mesclagem e outras propriedades.
```java
fillSettings.setColor(Color.getGreen());
gradientStroke.setOpacity((byte) 127);
gradientStroke.setBlendMode(BlendMode.Color);
fillSettings.setAlignWithLayer(false);
fillSettings.setGradientType(GradientType.Radial);
fillSettings.setAngle(45);
fillSettings.setDither(true);
fillSettings.setHorizontalOffset(15);
fillSettings.setVerticalOffset(11);
fillSettings.setReverse(true);
```
## Etapa 5: adicionar e modificar pontos de cor e transparência
Vamos adicionar novos pontos de cor e transparência e modificar os existentes para obter o efeito gradiente desejado.
```java
// Adicionar novo ponto de cor
GradientColorPoint colorPoint = fillSettings.addColorPoint();
colorPoint.setColor(Color.getGreen());
colorPoint.setLocation(4096);
colorPoint.setMedianPointLocation(75);
// Alterar localização do ponto anterior
fillSettings.getColorPoints()[1].setLocation(1899);
// Adicionar novo ponto de transparência
GradientTransparencyPoint transparencyPoint = fillSettings.addTransparencyPoint();
transparencyPoint.setOpacity(25);
transparencyPoint.setMedianPointLocation(25);
transparencyPoint.setLocation(4096);
// Alterar localização do ponto de transparência anterior
fillSettings.getTransparencyPoints()[1].setLocation(2411);
```
## Etapa 6: salve o arquivo PSD modificado
Depois de fazer todas as modificações necessárias, precisamos salvar o arquivo PSD.
```java
im.save(exportPath);
```
## Etapa 7: verifique as modificações
Por fim, vamos carregar o arquivo PSD salvo e verificar se nossas alterações foram aplicadas corretamente.
```java
PsdImage img = (PsdImage) Image.load(exportPath, loadOptions);
StrokeEffect gradientStrokeEffect = (StrokeEffect) img.getLayers()[2].getBlendingOptions().getEffects()[0];
Assert.areEqual(BlendMode.Color, gradientStrokeEffect.getBlendMode());
Assert.areEqual(127, gradientStrokeEffect.getOpacity());
Assert.areEqual(true, gradientStrokeEffect.isVisible());
GradientFillSettings fillSetting = (GradientFillSettings) gradientStrokeEffect.getFillSettings();
Assert.areEqual(Color.getGreen(), fillSetting.getColor());
Assert.areEqual(FillType.Gradient, fillSetting.getFillType());
// Verifique os pontos de cor
Assert.areEqual(3, fillSetting.getColorPoints().length);
IGradientColorPoint point = fillSetting.getColorPoints()[0];
Assert.areEqual(50, point.getMedianPointLocation());
Assert.areEqual(Color.getBlack(), point.getColor());
Assert.areEqual(0, point.getLocation());
point = fillSettings.getColorPoints()[1];
Assert.areEqual(50, point.getMedianPointLocation());
Assert.areEqual(Color.getWhite(), point.getColor());
Assert.areEqual(1899, point.getLocation());
point = fillSettings.getColorPoints()[2];
Assert.areEqual(75, point.getMedianPointLocation());
Assert.areEqual(Color.getGreen(), point.getColor());
Assert.areEqual(4096, point.getLocation());
// Verifique os pontos de transparência
Assert.areEqual(3, fillSettings.getTransparencyPoints().length);
IGradientTransparencyPoint transparencyPoint1 = fillSettings.getTransparencyPoints()[0];
Assert.areEqual(50, transparencyPoint1.getMedianPointLocation());
Assert.areEqual(100, transparencyPoint1.getOpacity());
Assert.areEqual(0, transparencyPoint1.getLocation());
transparencyPoint1 = fillSettings.getTransparencyPoints()[1];
Assert.areEqual(50, transparencyPoint.getMedianPointLocation());
Assert.areEqual(100, transparencyPoint.getOpacity());
Assert.areEqual(2411, transparencyPoint.getLocation());
transparencyPoint1 = fillSettings.getTransparencyPoints()[2];
Assert.areEqual(25, transparencyPoint.getMedianPointLocation());
Assert.areEqual(25, transparencyPoint.getOpacity());
Assert.areEqual(4096, transparencyPoint.getLocation());
```
## Conclusão
E aí está! Agora você sabe adicionar e manipular gradientes de camada de traçado em arquivos PSD usando Aspose.PSD para Java. Este tutorial abordou o carregamento do arquivo PSD, o acesso e a modificação dos efeitos do traçado e o salvamento das alterações. Com essas habilidades, você pode criar gradientes visualmente atraentes e personalizar seus arquivos PSD para atender às suas necessidades.
## Perguntas frequentes
### O que é Aspose.PSD para Java?
Aspose.PSD for Java é uma biblioteca que permite aos desenvolvedores trabalhar com arquivos PSD em aplicativos Java, fornecendo recursos para criar, manipular e converter arquivos PSD.
### Preciso de uma licença para usar Aspose.PSD para Java?
 Sim, você precisa de uma licença válida para usar Aspose.PSD para Java. Você pode obter um[licença temporária](https://purchase.aspose.com/temporary-license/) para fins de avaliação.
### Posso usar Aspose.PSD para Java para criar arquivos PSD do zero?
Absolutamente! Aspose.PSD para Java fornece APIs abrangentes para criar e manipular arquivos PSD programaticamente.
### É possível aplicar outros efeitos usando Aspose.PSD para Java?
Sim, você pode aplicar vários efeitos como sombra, brilho e muito mais usando Aspose.PSD para Java.
### Onde posso encontrar a documentação do Aspose.PSD para Java?
 Você pode encontrar a documentação[aqui](https://reference.aspose.com/psd/java/).