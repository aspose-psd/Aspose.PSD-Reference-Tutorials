---
date: 2026-04-08
description: Aprenda a exportar PSD para PNG e criar uma nova camada PSD com Aspose.PSD
  para Java usando uma licença temporária da Aspose. Este tutorial passo a passo cobre
  a manipulação de imagens PSD e a definição da posição da camada.
keywords:
- aspose temporary license
- set layer position
- psd image manipulation
- create new psd layer
linktitle: Adicionar uma nova camada regular ao PSD
second_title: Aspose.PSD Java API
title: Exportar PSD para PNG e adicionar uma nova camada regular usando Aspose.PSD
  para Java – licença temporária da Aspose
url: /pt/java/advanced-image-effects/add-new-regular-layer/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Exportar PSD para PNG e Adicionar uma Nova Camada Regular usando Aspose.PSD para Java

## Introdução

Neste **aspose psd tutorial** você descobrirá como **exportar PSD para PNG** enquanto também **cria uma nova camada regular** dentro do mesmo arquivo, **usando uma licença temporária da aspose** para desenvolvimento. Seja para gerar miniaturas prontas para a web, preparar ativos para um pipeline de design ou simplesmente experimentar com **psd image manipulation**, o Aspose.PSD para Java oferece controle total programático. Vamos percorrer cada passo — desde o carregamento do arquivo fonte até a gravação tanto do PSD atualizado quanto de uma cópia PNG — para que você possa começar a manipular camadas PSD imediatamente.

## Respostas Rápidas
- **Posso exportar PSD para PNG com uma única chamada?** Sim, após adicionar camadas você pode chamar `save` com `PngOptions`.
- **Preciso de uma licença para desenvolvimento?** Uma licença temporária funciona para testes; uma licença completa é necessária para produção.
- **Qual versão do Java é suportada?** Aspose.PSD funciona com Java 8 e versões mais recentes.
- **O posicionamento de camada é baseado em pixels?** Sim, você define as coordenadas left, top, right, bottom em pixels usando os métodos **set layer position**.
- **O PNG manterá a transparência das camadas?** O PNG conterá o resultado mesclado de todas as camadas visíveis.

## Por que usar uma licença temporária da aspose?

Uma **aspose temporary license** permite que você avalie o conjunto completo de recursos do Aspose.PSD sem quaisquer restrições funcionais. Ela remove a marca d'água de avaliação, desbloqueia todas as APIs — incluindo a capacidade de **create new psd layer** objetos — e permite testar seu código em um ambiente semelhante ao de produção antes de adquirir uma licença permanente.

## Pré-requisitos

- **Java Development Environment** – JDK 8+ e uma ferramenta de build (Maven/Gradle) instalada.
- **Aspose.PSD for Java** – Baixe o JAR mais recente no site oficial [here](https://releases.aspose.com/psd/java/).
- **A sample PSD file** – Usaremos `OneLayer.psd` nos exemplos.

## Importar Pacotes

Adicione as importações necessárias à sua classe Java. Essas classes fornecem a funcionalidade central para **psd image manipulation** e manipulação de camadas.

```java
import com.aspose.psd.Image;
import com.aspose.psd.Rectangle;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.Layer;
import com.aspose.psd.imageoptions.PngOptions;
import com.aspose.psd.imageoptions.PsdOptions;
```

## O que é “set layer position” e por que isso importa?

Ao adicionar uma nova camada, você precisa definir onde ela aparece na tela. Os métodos `setLeft`, `setTop`, `setRight` e `setBottom` **set layer position** em coordenadas de pixel. O posicionamento correto garante que seus gráficos se alinhem exatamente onde você espera, o que é crucial para tarefas como composição de ativos de UI ou preparação de arquivos prontos para impressão.

## Guia passo a passo

### Passo 1: Carregar o Arquivo PSD

Primeiro, carregue o PSD existente que você deseja modificar. Isso fornece um objeto `PsdImage` com o qual você pode trabalhar.

```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "OneLayer.psd";
PsdImage im = (PsdImage)Image.load(sourceFileName);
```

### Passo 2: Preparar Dados de Pixels e Retângulos

Criaremos dois buffers de pixels (`int[]`) e definiremos as áreas retangulares onde as novas camadas serão pintadas. Esta é a base para **creating a new psd layer**.

```java
int[] data1 = new int[2500];
int[] data2 = new int[2500];
Rectangle rect1 = new Rectangle(0, 0, 50, 50);
Rectangle rect2 = new Rectangle(0, 0, 100, 25);
```

### Passo 3: Inicializar Dados da Camada

Preencha os buffers de pixels com um valor ARGB padrão. O valor `-10000000` corresponde a um tom escuro semitransparente.

```java
for (int i = 0; i < 2500; i++) {
    data1[i] = -10000000;
    data2[i] = -10000000;
}
```

### Passo 4: Adicionar Camadas Regulares (Manipular Camadas PSD)

Agora nós **add regular layers** à imagem PSD e **set layer position** usando as propriedades left, top, right e bottom. Isso demonstra como **manipulate PSD layers** programaticamente.

```java
Layer layer1 = im.addRegularLayer();
layer1.setLeft(25);
layer1.setTop(25);
layer1.setRight(75);
layer1.setBottom(75);
layer1.saveArgb32Pixels(rect1, data1);

Layer layer2 = im.addRegularLayer();
layer2.setLeft(25);
layer2.setTop(150);
layer2.setRight(1255);
layer2.setBottom(175);
layer2.saveArgb32Pixels(rect2, data2);
```

### Passo 5: Exportar PSD para PNG e Salvar o PSD Atualizado

Depois que as camadas estiverem no lugar, salve o documento modificado. Primeiro exportamos o resultado para PNG (a etapa **export psd to png**), depois persistimos o PSD com as novas camadas.

```java
String exportPath = dataDir + "Updated.psd";
String exportPathPng = dataDir + "Updated.png";

im.save(exportPath, new PsdOptions());          // Save the updated PSD
im.save(exportPathPng, new PngOptions());       // Export PSD to PNG
```

> **Dica profissional:** Se você só precisar do PNG, pode pular a chamada `save` do PSD e invocar diretamente `save` com `PngOptions`.

## Problemas Comuns & Solução de Problemas

| Sintoma | Causa Provável | Correção |
|---------|----------------|----------|
| PNG aparece em branco | Camadas estão invisíveis ou totalmente transparentes | Certifique-se de definir valores de pixel não transparentes ou chamar `layer.setVisible(true)`. |
| `ArrayIndexOutOfBoundsException` | Incompatibilidade entre o tamanho do retângulo e o comprimento do array de pixels | Verifique se `rect.width * rect.height == dataArray.length`. |
| LicenseException at runtime | Nenhuma licença válida carregada | Carregue uma licença temporária ou permanente antes de chamar quaisquer métodos da API. |

## Perguntas Frequentes

**Q: O Aspose.PSD é compatível com Java 8?**  
A: Sim, o Aspose.PSD suporta Java 8 e versões posteriores.

**Q: Posso aplicar transformações (rotacionar, escalar) às camadas adicionadas?**  
A: Absolutamente! A classe `Layer` fornece métodos como `rotate`, `scale` e `translate` para controle total de transformações.

**Q: Onde posso encontrar documentação adicional do Aspose.PSD?**  
A: Documentação detalhada da API está disponível [here](https://reference.aspose.com/psd/java/).

**Q: Como obtenho uma licença temporária para o Aspose.PSD?**  
A: Visite a página de licença temporária [here](https://purchase.aspose.com/temporary-license/).

**Q: Existem fóruns da comunidade para suporte ao Aspose.PSD?**  
A: Sim, participe das discussões nos fóruns da Aspose [here](https://forum.aspose.com/c/psd/34).

## Conclusão

Agora você aprendeu como **exportar PSD para PNG** enquanto **adiciona novas camadas regulares** usando Aspose.PSD para Java, e viu como uma **aspose temporary license** permite experimentar este fluxo de trabalho sem restrições. Este tutorial demonstra as principais capacidades de **psd image manipulation**: carregar um arquivo, criar camadas, preencher dados de pixels e exportar a composição final. Sinta-se à vontade para experimentar diferentes tamanhos de retângulo, cores de pixel ou efeitos de camada para adaptar a saída às necessidades do seu projeto.

---

**Última atualização:** 2026-04-08  
**Testado com:** Aspose.PSD 24.11 for Java  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}