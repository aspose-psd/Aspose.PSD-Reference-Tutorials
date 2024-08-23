---
title: Adicionar camada de ajuste de matiz e saturação ao PSD
linktitle: Adicionar camada de ajuste de matiz e saturação ao PSD
second_title: API Java Aspose.PSD
description: Aprenda como adicionar camadas de ajuste de saturação de matiz ao PSD usando Aspose.PSD para Java neste tutorial passo a passo abrangente. Aprimore seu fluxo de trabalho de design gráfico.
type: docs
weight: 14
url: /pt/java/modifying-converting-psd-images/add-hue-saturation-adjustment-layer-psd/
---
## Introdução
Quando se trata de design gráfico, a manipulação de cores desempenha um papel fundamental – especificamente, ajustar o matiz, a saturação e a luminosidade pode transformar drasticamente o clima e a qualidade de qualquer imagem. Uma maneira eficaz de conseguir isso é através do uso de camadas de ajuste no Photoshop (arquivos PSD). Se você deseja aprimorar seus arquivos PSD programaticamente usando Java, a biblioteca Aspose.PSD está aqui para ajudar! Este tutorial irá guiá-lo pelas etapas para adicionar uma camada de ajuste de saturação de matiz aos seus arquivos PSD, tornando seus fluxos de trabalho mais produtivos e eficientes.
Neste guia, cobriremos tudo, desde a importação dos pacotes necessários até os detalhes essenciais dos exemplos de código.
## Pré-requisitos
Antes de passarmos para o código, certifique-se de ter o seguinte em vigor:
1.  Java Development Kit (JDK): Certifique-se de ter o JDK 8 ou superior instalado em sua máquina. Você pode baixá-lo no[Downloads do kit de desenvolvimento Java SE](https://www.oracle.com/java/technologies/javase-downloads.html).
2.  Biblioteca Aspose.PSD para Java: você precisará ter a biblioteca Aspose.PSD, que pode ser[baixe aqui](https://releases.aspose.com/psd/java/). 
3. IDE: Um ambiente de desenvolvimento integrado (IDE) adequado, como IntelliJ IDEA ou Eclipse para desenvolvimento Java.
4. Conhecimento básico de Java: Familiaridade com programação Java é uma vantagem, mas não se preocupe; orientaremos você no código passo a passo.
Agora que classificamos nossos pré-requisitos, vamos para a parte divertida: codificação!
## Importar pacotes
Para começar a trabalhar com a biblioteca Aspose.PSD, o primeiro passo é importar as classes necessárias. Veja como você pode fazer isso em seu arquivo Java:
```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.adjustmentlayers.HueSaturationLayer;
import com.aspose.psd.fileformats.psd.layers.layerresources.ColorRangeHsl;
```
Certifique-se de ter as bibliotecas apropriadas adicionadas ao seu projeto para que essas importações funcionem perfeitamente.
## Etapa 1: configure seu diretório de documentos
Todo projeto precisa de um ponto de partida e o nosso não é exceção. Você precisa especificar um diretório onde seus arquivos PSD serão armazenados. Isso é crucial para carregar e salvar imagens corretamente.
```java
String dataDir = "Your Document Directory"; // Atualize este caminho para o seu diretório real
```
## Etapa 2: carregar um arquivo PSD existente
Para manipular um arquivo PSD existente, primeiro precisamos carregá-lo em nosso programa. Veja como você pode fazer isso:
```java
String sourceFileName = dataDir + "HueSaturationAdjustmentLayer.psd";
PsdImage im = (PsdImage) Image.load(sourceFileName);
```
 Neste código, atualize`"HueSaturationAdjustmentLayer.psd"` ao nome do arquivo PSD existente que você deseja editar.
## Etapa 3: edite a camada Matiz/Saturação
A seguir, percorreremos as camadas de nossa imagem PSD carregada para localizar e editar quaisquer camadas de Matiz/Saturação existentes. Esta etapa envolve a modificação dos valores de matiz, saturação e luminosidade.
```java
for (int i = 0; i < im.getLayers().length; i++) {
    if (im.getLayers()[i] instanceof HueSaturationLayer) {
        HueSaturationLayer hueLayer = (HueSaturationLayer) im.getLayers()[i];
        hueLayer.setHue((short) -25);
        hueLayer.setSaturation((short) -12);
        hueLayer.setLightness((short) 67);
        ColorRangeHsl colorRange = hueLayer.getRange(2);
        colorRange.setHue((short) -40);
        colorRange.setSaturation((short) 50);
        colorRange.setLightness((short) -20);
        colorRange.setMostLeftBorder((short) 300);
    }
}
```
Neste exemplo:
- Estamos ajustando o matiz para -25, a saturação para -12 e a luminosidade para +67.
-  O`getRange(2)` O método nos permite ajustar intervalos de cores específicos conforme desejado.
## Etapa 4: salve o arquivo PSD modificado
Após fazer os ajustes, o próximo passo é salvar o arquivo. Esta é uma parte vital do nosso processo, garantindo que as alterações que fizemos não sejam perdidas.
```java
String psdPathAfterChange = dataDir + "HueSaturationAdjustmentLayerChanged.psd";
im.save(psdPathAfterChange);
```
## Etapa 5: adicionar uma nova camada de matiz/saturação
Em seguida, você pode querer adicionar uma nova camada de ajuste de Matiz/Saturação a outro arquivo PSD. Basta seguir a mesma abordagem usada anteriormente, mas com arquivos PSD diferentes.
```java
sourceFileName = dataDir + "PhotoExample.psd";
PsdImage img = (PsdImage) Image.load(sourceFileName);
HueSaturationLayer hueLayerNew = img.addHueSaturationAdjustmentLayer();
```
## Etapa 6: definir novos valores de matiz/saturação para a nova camada
Agora que você criou esta nova camada, aplique as configurações desejadas de matiz, saturação e luminosidade como antes.
```java
hueLayerNew.setHue((short) -25);
hueLayerNew.setSaturation((short) -12);
hueLayerNew.setLightness((short) 67);
ColorRangeHsl newColorRange = hueLayerNew.getRange(2);
newColorRange.setHue((short) -160);
newColorRange.setSaturation((short) 100);
newColorRange.setLightness((short) 20);
newColorRange.setMostLeftBorder((short) 300);
```
## Etapa 7: salve o arquivo PSD atualizado
Por fim, salve o arquivo PSD com a camada Matiz/Saturação adicionada para que você possa ver suas alterações.
```java
String psdPathAfterNewLayerChange = dataDir + "PhotoExampleAddedHueSaturation.psd";
img.save(psdPathAfterNewLayerChange);
```
Parabéns! Você manipulou arquivos PSD com sucesso usando Aspose.PSD para Java. Agora você pode experimentar diferentes imagens e alterações mais profundas, dando vida aos seus projetos de design gráfico.
## Conclusão
Trabalhar com gráficos de forma programática abre um mundo de possibilidades. Usar Aspose.PSD para Java para adicionar e modificar camadas de ajuste de saturação de matiz fornece flexibilidade e eficiência que podem agilizar seu fluxo de trabalho de design. Esteja você aprimorando fotos para um projeto ou criando conteúdo visual impressionante, dominar essas ferramentas pode melhorar muito sua produção.
 Sinta-se à vontade para explorar mais funcionalidades do Aspose.PSD mergulhando em[documentação](https://reference.aspose.com/psd/java/) ou considere pegar um[licença temporária](https://purchase.aspose.com/temporary-license/) para testar todo o poder da biblioteca.
## Perguntas frequentes
### O que é uma camada de ajuste de saturação de matiz?
Uma camada de ajuste de matiz e saturação permite modificar as propriedades de cor de uma imagem sem alterar permanentemente os pixels originais.
### Preciso do Photoshop instalado para usar o Aspose.PSD?
Não, Aspose.PSD é uma biblioteca independente que funciona independentemente do Photoshop.
### Posso usar Aspose.PSD para processamento em lote?
Sim, você pode automatizar e processar em lote vários arquivos PSD com Aspose.PSD.
### O Aspose.PSD é gratuito?
Aspose.PSD oferece uma avaliação gratuita, mas é necessária uma licença para uso a longo prazo. Você pode ver os preços[aqui](https://purchase.aspose.com/buy).