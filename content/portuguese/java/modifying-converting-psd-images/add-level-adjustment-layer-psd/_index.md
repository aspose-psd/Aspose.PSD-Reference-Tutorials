---
title: Adicionar camada de ajuste de nível em PSD
linktitle: Adicionar camada de ajuste de nível em PSD
second_title: API Java Aspose.PSD
description: Aprenda como adicionar efetivamente uma camada de ajuste de nível em seus arquivos PSD usando Aspose.PSD para Java. Eleve suas habilidades de edição de imagens.
type: docs
weight: 16
url: /pt/java/modifying-converting-psd-images/add-level-adjustment-layer-psd/
---
## Introdução
Quando se trata de edição de imagens, o gerenciamento de níveis pode fazer uma grande diferença na vibração e clareza de suas fotos. Uma ferramenta útil no arsenal do Photoshop é a “Camada de ajuste de nível”, que permite ajustar a faixa de tons e o equilíbrio de cores de suas imagens. Neste guia, orientaremos você sobre como implementar uma camada de ajuste de nível em um arquivo PSD usando Aspose.PSD para Java. Então, pegue seu Java IDE.
## Pré-requisitos
Antes de entrar no mundo dos ajustes de nível, você precisará configurar algumas coisas para garantir uma viagem tranquila:
1.  Java Development Kit (JDK): Certifique-se de ter o JDK instalado em sua máquina. Se você não tiver, você pode pegá-lo no[Site da Oracle](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html) ou use OpenJDK.
2.  Biblioteca Aspose.PSD para Java: Para manipular arquivos PSD, você precisará baixar a biblioteca Aspose.PSD. Você pode obter a versão mais recente deste[link para baixar](https://releases.aspose.com/psd/java/) e certifique-se de ter incluído o JAR na biblioteca do seu projeto.
3. Conhecimento básico de Java: Ter um conhecimento fundamental de programação Java ajudará, pois iremos nos aprofundar nos trechos de código ao longo deste tutorial.
4. Configuração do IDE: você pode usar qualquer IDE Java de sua preferência, como IntelliJ IDEA, Eclipse ou NetBeans, para escrever e executar seu código. Apenas certifique-se de configurar seu projeto Java e adicionar a biblioteca Aspose.PSD.

## Importar pacotes
Antes de começarmos a escrever nosso código, precisamos importar os pacotes necessários da biblioteca Aspose.PSD. Veja como você pode fazer isso:
```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.adjustmentlayers.LevelsLayer;
import com.aspose.psd.fileformats.psd.layers.layerresources.LevelChannel;
```
Ao importar estes pacotes teremos acesso às classes necessárias para carregar, modificar e salvar nossos arquivos PSD.

Agora, vamos dividir o processo em etapas digeríveis. Acompanhe enquanto carregamos um arquivo PSD, ajustamos os níveis e salvamos suas alterações. 
## Etapa 1: configure seus caminhos de arquivo
O primeiro passo é definir onde nosso arquivo PSD está localizado e onde queremos salvar a saída modificada. Você pode personalizar o caminho do diretório para atender às suas necessidades.
```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "LevelsAdjustmentLayer.psd";
String psdPathAfterChange = dataDir + "LevelsAdjustmentLayerChanged.psd";
```
 Aqui, substitua`"Your Document Directory"`com o caminho real em seu sistema onde seu arquivo PSD está armazenado. Isso prepara o terreno para tudo o que faremos a seguir.
## Passo 2: Carregue o arquivo PSD
 Agora, vamos carregar o arquivo PSD usando o`PsdImage` aula. Esta etapa é essencial porque nos permite acessar e manipular as camadas.
```java
PsdImage im = (PsdImage) Image.load(sourceFileName);
```
 Quando você liga`Image.load()` , ele lerá o arquivo PSD e criará uma instância de`PsdImage` com o qual você pode trabalhar.
## Etapa 3: iterar pelas camadas
Como queremos ajustar uma camada de ajuste de nível, precisaremos percorrer cada camada em nosso arquivo PSD. Isso nos ajuda a encontrar a camada específica que queremos modificar.
```java
for (int i = 0; i < im.getLayers().length; i++) {
    if (im.getLayers()[i] instanceof LevelsLayer) {
        LevelsLayer levelsLayer = (LevelsLayer) im.getLayers()[i];
        // Mais manipulação ocorrerá aqui ...
    }
}
```
 Neste circuito,`instanceof LevelsLayer` verifica se a camada atual é uma camada de ajuste de níveis. Se for, podemos prosseguir para ajustar suas propriedades.
## Etapa 4: ajuste as configurações do canal de nível
Depois de identificarmos a camada correta, podemos modificar seus níveis de entrada e saída. É aqui que a mágica acontece! Ajuste diferentes parâmetros para ver como eles afetam a imagem.
```java
LevelChannel channel = levelsLayer.getChannel(0);
channel.setInputMidtoneLevel(2.0f);
channel.setInputShadowLevel((short) 10);
channel.setInputHighlightLevel((short) 230);
channel.setOutputShadowLevel((short) 20);
channel.setOutputHighlightLevel((short) 200);
```
Veja o que cada parâmetro faz:
- Nível de meio-tom de entrada: ajusta os tons médios.
- Nível de sombra de entrada: ajusta as áreas mais escuras da imagem.
- Nível de destaque de entrada: altera as áreas claras da imagem.
- Nível de sombra de saída: define como as sombras escuras aparecerão.
- Nível de realce de saída: define como os realces de luz aparecerão.
Sinta-se à vontade para experimentar valores diferentes!
## Etapa 5: salve o arquivo PSD modificado
Agora que fizemos nossos ajustes, é hora de salvar o arquivo PSD modificado. Esta etapa é crucial para garantir que suas alterações sejam aplicadas e armazenadas.
```java
im.save(psdPathAfterChange);
```
 Agora você pode encontrar seu arquivo PSD ajustado no local especificado`psdPathAfterChange`. 
## Conclusão
Você acabou de aprender como adicionar uma camada de ajuste de nível a um arquivo PSD usando Aspose.PSD para Java! Seguindo este guia, você pode ajustar a qualidade tonal de suas imagens sem esforço, abrindo caminho para uma saída mais vibrante e visualmente atraente. Lembre-se de que a prática leva à perfeição, então sinta-se à vontade para ajustar os ajustes e explorar diferentes arquivos PSD para ver os efeitos de suas alterações.
## Perguntas frequentes
### O que é uma camada de ajuste de nível?
Uma camada de ajuste de nível permite corrigir a faixa tonal em suas imagens, equilibrando sombras, meios-tons e realces.
### Posso usar o Aspose.PSD sem comprar?
Sim! Aspose oferece um teste gratuito para testar a biblioteca antes de comprar.
### Onde posso encontrar documentação para Aspose.PSD?
 Você pode encontrar a documentação[aqui](https://reference.aspose.com/psd/java/).
### Existe algum suporte da comunidade para os produtos Aspose?
 Absolutamente! Você pode tirar dúvidas e obter suporte no[Aspor fórum](https://forum.aspose.com/c/psd/34).
### Como posso obter uma licença temporária para Aspose.PSD?
 Você pode solicitar uma licença temporária[aqui](https://purchase.aspose.com/temporary-license/).