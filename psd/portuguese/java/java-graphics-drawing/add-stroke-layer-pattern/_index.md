---
date: 2026-01-17
description: Aprenda como adicionar padrão de traço java com Aspose.PSD para Java.
  Siga este guia passo a passo para melhorar suas imagens PSD rapidamente.
linktitle: How to Add Stroke Layer Pattern in Java
second_title: Aspose.PSD Java API
title: Como adicionar padrão de traço em Java usando Aspose.PSD
url: /pt/java/java-graphics-drawing/add-stroke-layer-pattern/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Como Adicionar Padrão de Traço Java Usando Aspose.PSD

## Introdução
Se você precisa **adicionar padrão de traço java** a um arquivo Photoshop, o Aspose.PSD for Java torna isso surpreendentemente simples. Seja construindo uma ferramenta de design gráfico, automatizando edições em lote ou apenas experimentando efeitos de camada, este tutorial orienta você em cada passo — desde o carregamento do PSD até a verificação do novo padrão. Vamos mergulhar e ver como você pode melhorar suas imagens rapidamente.

## Respostas Rápidas
- **Qual biblioteca eu preciso?** Aspose.PSD for Java  
- **Qual versão do Java é suportada?** JDK 8 ou posterior  
- **Preciso de licença para testes?** Uma avaliação gratuita funciona para desenvolvimento; uma licença é necessária para produção  
- **Quanto tempo leva a implementação?** Aproximadamente 10‑15 minutos para um traço de padrão básico  
- **Posso reutilizar o padrão em várias camadas?** Sim, basta atribuir o mesmo `PattResource` a outras camadas  

## O que é adicionar padrão de traço java?
Adicionar um padrão de traço em Java significa aplicar um preenchimento personalizado (geralmente um bitmap repetido) ao efeito de traço de uma camada. Essa técnica permite criar contornos estilizados — pense em uma linha tracejada, uma textura de tijolos ou uma borda gráfica personalizada — diretamente dentro de um arquivo PSD sem abrir o Photoshop.

## Por que usar Aspose.PSD para adicionar padrão de traço java?
- **Fidelidade total ao PSD** – Todos os efeitos de camada, recursos e modos de mesclagem são preservados.  
- **Nenhum Photoshop nativo necessário** – Funciona em qualquer SO com um JDK.  
- **Controle programático** – Automatize o processamento em lote ou integre a serviços de servidor.  
- **API rica** – Acesso a recursos globais, preenchimentos de padrão e modos de mesclagem em uma única interface fluente.

## Pré‑requisitos
- **Java Development Kit (JDK)** – Certifique‑se de que o JDK 8 ou mais recente está instalado.  
- **Aspose.PSD for Java** – Baixe a biblioteca [aqui](https://releases.aspose.com/psd/java/) e adicione o JAR ao classpath do seu projeto.  
- **IDE** – IntelliJ IDEA, Eclipse ou qualquer editor de sua preferência.

## Importar Pacotes
Primeiro, importe as classes que você precisará para manipular arquivos PSD, cores, retângulos e efeitos de traço.

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

## Etapa 1: Carregar o Arquivo PSD
Carregue o PSD de origem para que você possa trabalhar com suas camadas e recursos.

```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "Stroke.psd";
PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);
PsdImage im = (PsdImage)Image.load(sourceFileName, loadOptions);
```

## Etapa 2: Preparar os Dados do Novo Padrão
Crie um padrão simples de 4 × 4 pixels que será usado para o traço.

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

## Etapa 3: Acessar o Efeito de Traço
Localize o efeito de traço na camada alvo (neste exemplo, a quarta camada).

```java
StrokeEffect patternStroke = (StrokeEffect)im.getLayers()[3].getBlendingOptions().getEffects()[0];
Assert.areEqual(BlendMode.Normal, patternStroke.getBlendMode());
Assert.areEqual(255, patternStroke.getOpacity());
Assert.areEqual(true, patternStroke.isVisible());
PatternFillSettings fillSettings = (PatternFillSettings)patternStroke.getFillSettings();
Assert.areEqual(FillType.Pattern, fillSettings.getFillType());
```

## Etapa 4: Modificar o Efeito de Traço
### Atualizar Propriedades do Efeito de Traço
Ajuste a opacidade e o modo de mesclagem para observar o impacto visual do novo padrão.

```java
patternStroke.setOpacity((byte)127);
patternStroke.setBlendMode(BlendMode.Color);
```

### Atualizar o Recurso de Padrão
Substitua o recurso de padrão global existente pelo que você acabou de criar.

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

## Etapa 5: Aplicar o Novo Padrão
Vincule o recurso de padrão atualizado ao efeito de traço e salve o PSD.

```java
((PatternFillSettings)patternStroke.getFillSettings()).setPatternName("$$/Presets/Patterns/HorizontalLine1=Horizontal Line 9\0");
((PatternFillSettings)patternStroke.getFillSettings()).setPatternId(guid.toString() + "\0");
im.save(exportPath);
```

## Etapa 6: Verificar as Alterações
Recarregue o arquivo e confirme que o novo padrão, opacidade e modo de mesclagem foram aplicados corretamente.

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

## Problemas Comuns e Soluções
| Problema | Causa | Solução |
|----------|-------|---------|
| O padrão não aparece | Referência `PatternId` incorreta | Certifique‑se de que o `PatternId` definido em `PattResource` corresponde ao usado em `PatternFillSettings`. |
| O traço desaparece após salvar | Opacidade definida como 0 ou efeito oculto | Verifique se `setOpacity` está entre 0‑255 e se `isVisible()` retorna `true`. |
| Cores inesperadas | Modo de mesclagem incompatível | Use `BlendMode.Color` (ou outro modo) que corresponda à sua intenção de design. |

## Perguntas Frequentes
### O que é Aspose.PSD for Java?
Aspose.PSD for Java é uma biblioteca que permite a desenvolvedores criar, editar e converter arquivos PSD (Photoshop Document) programaticamente.

### Posso usar Aspose.PSD for Java em um projeto comercial?
Sim, você pode usá‑lo em projetos comerciais. Você pode adquirir uma licença [aqui](https://purchase.aspose.com/buy).

### Existe uma avaliação gratuita disponível para Aspose.PSD for Java?
Sim, você pode baixar uma versão de avaliação gratuita [aqui](https://releases.aspose.com/).

### Como posso obter suporte para Aspose.PSD for Java?
Você pode obter suporte nos fóruns da comunidade Aspose [aqui](https://forum.aspose.com/c/psd/34).

### Quais são os requisitos de sistema para Aspose.PSD for Java?
Você precisa do JDK instalado e de uma IDE para desenvolvimento. A biblioteca suporta vários sistemas operacionais, incluindo Windows, Linux e macOS.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Última atualização:** 2026-01-17  
**Testado com:** Aspose.PSD for Java 24.12 (mais recente na data de escrita)  
**Autor:** Aspose