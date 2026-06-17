---
date: 2026-03-13
description: Aprenda como adicionar camada de matiz e saturação a arquivos PSD usando
  Aspose.PSD para Java. Este guia também mostra como processar em lote arquivos PSD
  e criar camada de ajuste de matiz programaticamente.
linktitle: Add Hue Saturation Layer to PSD
second_title: Aspose.PSD Java API
title: Adicionar camada de matiz e saturação ao PSD com Aspose.PSD para Java
url: /pt/java/modifying-converting-psd-images/add-hue-saturation-adjustment-layer-psd/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Adicionar Camada de Matiz e Saturação ao PSD

## Introdução
Quando se trata de design gráfico, a manipulação de cores desempenha um papel fundamental—especificamente, ajustar matiz, saturação e luminosidade pode transformar drasticamente o humor e a qualidade de qualquer imagem. Uma maneira eficaz de conseguir isso é usando camadas de ajuste no Photoshop (arquivos PSD). Se você deseja **add hue saturation layer** programaticamente usando Java, a biblioteca Aspose.PSD está aqui para ajudar! Este tutorial guiará você pelos passos para adicionar uma Camada de Ajuste de Matiz e Saturação ao seus arquivos PSD, tornando seu fluxo de trabalho mais produtivo e eficiente.

## Respostas Rápidas
- **Qual biblioteca permite adicionar uma camada de matiz e saturação em Java?** Aspose.PSD for Java.  
- **Preciso ter o Photoshop instalado?** Não, a biblioteca funciona independentemente do Photoshop.  
- **Posso processar em lote arquivos PSD com esta abordagem?** Sim—uma vez que você automatiza as etapas, pode aplicá-las a muitos arquivos.  
- **Qual versão do Java é necessária?** JDK 8 ou superior.  
- **É necessária uma licença para uso em produção?** Sim, uma licença comercial é necessária após o período de avaliação.

## O que é uma operação de “add hue saturation layer”?
Uma operação **add hue saturation layer** cria uma camada de ajuste não destrutiva que permite modificar os valores de matiz, saturação e luminosidade sem alterar os dados de pixel originais. Isso é ideal para afinar cores em toda a composição ou em intervalos de cor específicos.

## Por que usar Aspose.PSD para Java?
- **Sem dependência do Photoshop** – funciona em qualquer plataforma que execute Java.  
- **Fidelidade total ao PSD** – preserva todas as informações de camadas, máscaras e efeitos.  
- **Pronto para lote** – você pode percorrer pastas e aplicar o mesmo ajuste a dezenas de arquivos.  
- **Foco em desempenho** – otimizado para documentos grandes e automação no lado do servidor.

## Pré-requisitos
Antes de mergulharmos no código, certifique-se de que você tem o seguinte:

1. **Java Development Kit (JDK):** Certifique‑se de que o JDK 8 ou superior esteja instalado em sua máquina. Você pode baixá‑lo em [Java SE Development Kit Downloads](https://www.oracle.com/java/technologies/javase-downloads.html).  
2. **Aspose.PSD for Java Library:** Você precisará da biblioteca Aspose.PSD, que pode [baixar aqui](https://releases.aspose.com/psd/java/).  
3. **IDE:** Um Ambiente de Desenvolvimento Integrado (IDE) adequado, como IntelliJ IDEA ou Eclipse, para desenvolvimento Java.  
4. **Conhecimento Básico de Java:** Familiaridade com programação Java é um diferencial, mas não se preocupe—nós guiaremos você linha por linha.

Agora que organizamos nossos pré‑requisitos, vamos para a parte divertida—codificar!

## Importar Pacotes
Para começar a trabalhar com a biblioteca Aspose.PSD, o primeiro passo é importar as classes necessárias. Veja como fazer isso no seu arquivo Java:

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.adjustmentlayers.HueSaturationLayer;
import com.aspose.psd.fileformats.psd.layers.layerresources.ColorRangeHsl;
```

Certifique‑se de que as bibliotecas apropriadas estejam adicionadas ao seu projeto para que essas importações funcionem sem problemas.

## Etapa 1: Configurar o Diretório do Documento
Todo projeto precisa de um ponto de partida, e o nosso não é exceção. Você precisa especificar um diretório onde seus arquivos PSD estão armazenados. Isso é crucial para carregar e salvar imagens corretamente.

```java
String dataDir = "Your Document Directory"; // Update this path to your actual directory
```

## Etapa 2: Carregar um Arquivo PSD Existente
Para manipular um arquivo PSD existente, primeiro precisamos carregá‑lo em nosso programa. Veja como fazer isso:

```java
String sourceFileName = dataDir + "HueSaturationAdjustmentLayer.psd";
PsdImage im = (PsdImage) Image.load(sourceFileName);
```

Neste código, atualize `"HueSaturationAdjustmentLayer.psd"` para o nome do seu arquivo PSD existente que você deseja editar.

## Etapa 3: Editar a Camada Hue/Saturation
Em seguida, percorreremos as camadas da nossa imagem PSD carregada para encontrar e editar quaisquer camadas Hue/Saturation existentes. Esta etapa envolve modificar os valores de matiz, saturação e luminosidade.

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
- Estamos ajustando o matiz para **-25**, a saturação para **-12** e a luminosidade para **+67**.  
- O método `getRange(2)` permite ajustar intervalos de cores específicos conforme desejado.

## Etapa 4: Salvar o Arquivo PSD Modificado
Depois de fazer os ajustes, o próximo passo é salvar o arquivo. Esta é uma parte vital do nosso processo, garantindo que as alterações feitas não sejam perdidas.

```java
String psdPathAfterChange = dataDir + "HueSaturationAdjustmentLayerChanged.psd";
im.save(psdPathAfterChange);
```

## Etapa 5: Adicionar uma Nova Camada Hue/Saturation
Se você precisar **create hue adjustment layer** do zero, pode adicionar uma nova camada de ajuste Hue/Saturation a outro arquivo PSD. Siga o mesmo padrão de carregamento, mas use o método `addHueSaturationAdjustmentLayer()`.

```java
sourceFileName = dataDir + "PhotoExample.psd";
PsdImage img = (PsdImage) Image.load(sourceFileName);
HueSaturationLayer hueLayerNew = img.addHueSaturationAdjustmentLayer();
```

## Etapa 6: Definir Novos Valores de Hue/Saturation para a Nova Camada
Agora que você criou essa nova camada, aplique as configurações desejadas de matiz, saturação e luminosidade como antes.

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

## Etapa 7: Salvar o Arquivo PSD Atualizado
Finalmente, salve o arquivo PSD com a camada Hue/Saturation adicionada para que você possa ver suas alterações.

```java
String psdPathAfterNewLayerChange = dataDir + "PhotoExampleAddedHueSaturation.psd";
img.save(psdPathAfterNewLayerChange);
```

Parabéns! Você manipulou arquivos PSD com sucesso usando Aspose.PSD for Java. Agora pode experimentar diferentes imagens e alterações mais profundas, dando vida aos seus projetos de design gráfico.

## Como processar arquivos PSD em lote com ajustes de matiz
Como o código acima é totalmente scriptável, você pode envolver toda a sequência em um loop que itere sobre cada arquivo `.psd` em uma pasta. Isso permite **batch process psd files** e aplicar os mesmos ajustes de matiz, saturação e luminosidade em uma única execução—perfeito para atualizações de branding em grande escala.

## Problemas Comuns e Soluções
- **NullPointerException ao carregar um arquivo:** Verifique se `dataDir` termina com o separador de arquivos apropriado (`/` ou `\`) e se o nome do arquivo está correto.  
- **Valores de ajuste fora do intervalo:** Matiz, saturação e luminosidade aceitam valores de -255 a 255. Mantenha seus números dentro desse intervalo.  
- **Camada não encontrada:** Se o PSD não possuir camada Hue/Saturation, a verificação `instanceof` ignorará o bloco. Use `addHueSaturationAdjustmentLayer()` para criar uma primeiro.

## Perguntas Frequentes

**Q: O que é uma Camada de Ajuste de Matiz e Saturação?**  
A: Ela permite modificar as propriedades de cor de uma imagem sem alterar permanentemente os pixels originais.

**Q: Preciso ter o Photoshop instalado para usar o Aspose.PSD?**  
A: Não, o Aspose.PSD é uma biblioteca autônoma que funciona independentemente do Photoshop.

**Q: Posso usar o Aspose.PSD para processamento em lote?**  
A: Sim, você pode automatizar e processar em lote múltiplos arquivos PSD com o Aspose.PSD.

**Q: O Aspose.PSD é gratuito?**  
A: O Aspose.PSD oferece um teste gratuito, mas uma licença é necessária para uso a longo prazo. Você pode ver os preços [aqui](https://purchase.aspose.com/buy).

## Conclusão
Trabalhar com gráficos programaticamente abre um mundo de possibilidades. Usar Aspose.PSD for Java para **add hue saturation layer** e para **create hue adjustment layer** fornece flexibilidade e eficiência que podem otimizar seu fluxo de trabalho de design. Seja aprimorando fotos para um projeto ou criando conteúdo visual impressionante, dominar essas ferramentas pode melhorar significativamente sua produção.

Sinta‑se à vontade para explorar mais funcionalidades do Aspose.PSD mergulhando na [documentation](https://reference.aspose.com/psd/java/) ou considere adquirir uma [temporary license](https://purchase.aspose.com/temporary-license/) para testar todo o poder da biblioteca.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Última atualização:** 2026-03-13  
**Testado com:** Aspose.PSD for Java 24.12 (latest at time of writing)  
**Autor:** Aspose  

---