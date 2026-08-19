---
date: 2026-04-03
description: Aprenda a salvar PSD como PNG com efeito de contorno e preenchimento
  de cor usando Aspose.PSD para Java. Este guia passo a passo mostra como exportar
  PSD para PNG rapidamente.
keywords:
- save psd as png
- export psd to png
- set stroke color
- apply layer effects
- customize stroke width
linktitle: Salvar PSD como PNG com efeito de contorno – Java
second_title: Aspose.PSD Java API
title: Salvar PSD como PNG com efeito de contorno – Java
url: /pt/java/psd-layer-management-effects/apply-stroke-effect-color-fill-psd/
weight: 21
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Salvar PSD como PNG com Efeito de Contorno e Preenchimento de Cor – Java

## Introdução

Neste guia, você aprenderá como **salvar PSD como PNG** aplicando um efeito de contorno com preenchimento de cor usando Aspose.PSD para Java. Seja você um desenvolvedor experiente ou iniciante, este tutorial passo a passo tornará fácil concluir a tarefa. Cobriremos tudo, desde a configuração do ambiente até a exportação da imagem final, para que você possa rapidamente **exportar PSD para PNG** em seus próprios projetos.

## Respostas Rápidas
- **Qual é o objetivo deste tutorial?** Ele mostra como salvar um arquivo PSD como PNG após aplicar um efeito de contorno personalizável.  
- **Qual biblioteca é usada?** Aspose.PSD para Java.  
- **Preciso de uma licença?** Um teste gratuito funciona para testes; uma licença é necessária para produção.  
- **Posso mudar a cor do contorno?** Sim – você pode definir qualquer cor via `ColorFillSettings`.  
- **É possível processamento em lote?** Absolutamente – envolva o código em um loop para processar vários arquivos PSD.

## O que é “salvar PSD como PNG”?
Salvar um PSD como PNG significa converter o arquivo nativo em camadas do Photoshop em um formato de imagem plano, amigável para a web, preservando a fidelidade visual. Isso é útil quando você precisa exibir conteúdo PSD em sites, aplicativos móveis ou qualquer plataforma que não suporte arquivos PSD diretamente.

## Por que aplicar um efeito de contorno com preenchimento de cor?
Um contorno adiciona um traço nítido ao redor do conteúdo da camada, fazendo com que os gráficos se destaquem em fundos complexos. Combiná‑lo com uma cor de preenchimento personalizada permite que você marque imagens, destaque elementos de UI ou crie miniaturas chamativas sem sair do Photoshop.

## Pré‑requisitos

1. **Java Development Kit (JDK) 8+** – certifique‑se de que `java` está no seu PATH.  
2. **Aspose.PSD para Java** – faça o download no [site](https://releases.aspose.com/psd/java/).  
3. **IDE** – IntelliJ IDEA, Eclipse ou qualquer editor de sua preferência.  
4. **PSD de exemplo** – um arquivo que já contém um efeito de contorno (ou adicione um no Photoshop).  
5. **Conhecimento básico de Java** – você escreverá algumas linhas de código, mas nada avançado.

Depois de ter tudo pronto, podemos começar a programar.

## Importar Pacotes

```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.fillsettings.ColorFillSettings;
import com.aspose.psd.fileformats.psd.layers.layereffects.StrokeEffect;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
import com.aspose.psd.imageoptions.PngOptions;
import com.aspose.psd.imageoptions.PsdOptions;
```

Essas importações trazem todas as classes necessárias para carregar um PSD, modificar seu contorno e salvar as saídas tanto em PSD quanto em PNG.

## Como Salvar PSD como PNG com Efeito de Contorno

### Etapa 1: Carregar o Arquivo PSD

Primeiro, aponte para a pasta que contém seu PSD de origem.

```java
String dataDir = "Your Document Directory";
```

Substitua `"Your Document Directory"` pelo caminho real na sua máquina.

Agora carregue o arquivo preservando quaisquer recursos de efeito existentes:

```java
String sourceFileName = dataDir + "StrokeComplex.psd";

PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);

PsdImage im = (PsdImage) Image.load(sourceFileName, loadOptions);
```

### Etapa 2: Definir Cor do Contorno (e opcionalmente personalizar a largura)

O loop abaixo percorre cada camada, obtém o primeiro `StrokeEffect` e altera sua cor de preenchimento. Você também pode ajustar `setWidth` ou `setPosition` no objeto `StrokeEffect` se precisar **personalizar a largura do contorno**.

```java
for (int i = 0; i < im.getLayers().length; i++) {
    StrokeEffect effect = (StrokeEffect) im.getLayers()[i].getBlendingOptions().getEffects()[0];
    ColorFillSettings settings = (ColorFillSettings) effect.getFillSettings();
    // Set the stroke color – change to any Color you like
    settings.setColor(Color.getDeepPink());
}
```

> **Dica profissional:** `Color.getDeepPink()` é apenas um exemplo. Use `new Color(r, g, b)` para valores RGB personalizados.

### Etapa 3: Salvar o PSD Modificado (opcional)

Se quiser manter uma versão PSD com o contorno atualizado, salve-a assim:

```java
String exportPath = dataDir + "StrokeComplexRendering.psd";
im.save(exportPath, new PsdOptions());
```

### Etapa 4: Exportar a Imagem como PNG (a etapa central de “salvar PSD como PNG”)

Por fim, converta o PSD editado para um arquivo PNG pronto para uso na web:

```java
String exportPathPng = dataDir + "StrokeComplexRendering.png";
PngOptions option = new PngOptions();
option.setColorType(PngColorType.TruecolorWithAlpha);

im.save(exportPathPng, option);
```

O PNG mantém o contorno rosa‑vivo que você definiu anteriormente, e a opção `TruecolorWithAlpha` garante que a transparência seja preservada.

## Problemas Comuns & Soluções

| Problema | Motivo | Correção |
|----------|--------|----------|
| **`ArrayIndexOutOfBoundsException`** | A camada não possui efeitos ou o primeiro efeito não é um `StrokeEffect`. | Verifique se a camada realmente contém um contorno ou itere através de `getEffects()` para encontrar o tipo correto. |
| **Cor não está mudando** | Você pode estar editando uma cópia das configurações em vez da original. | Certifique‑se de fazer cast direto para `ColorFillSettings` a partir de `effect.getFillSettings()`. |
| **PNG aparece em branco** | O PSD foi carregado sem rasterizar a camada. | Chame `im.save(..., new PngOptions())` após todas as modificações; evite salvar o `im` original antes das alterações. |

## Perguntas Frequentes

**Q: Posso aplicar múltiplos efeitos a uma única camada usando Aspose.PSD para Java?**  
A: Sim, você pode acessar as opções de mesclagem da camada e adicionar quantos efeitos forem necessários, incluindo sombras, brilhos e contornos.

**Q: É possível automatizar o processo para um lote de arquivos PSD?**  
A: Absolutamente. Envolva a lógica de carregamento, aplicação de efeito e salvamento em um loop `for‑each` que itere sobre os arquivos em um diretório.

**Q: Como posso reverter alterações feitas em um arquivo PSD?**  
A: Recarregue o arquivo original antes de salvar quaisquer modificações; o Aspose.PSD não fornece uma pilha de desfazer.

**Q: Posso personalizar a largura e a posição do contorno?**  
A: Sim. Use `effect.setWidth(float)` e `effect.setPosition(StrokeEffect.Position)` para controlar a espessura e o posicionamento (dentro, fora ou centralizado).

**Q: A biblioteca Aspose.PSD para Java é gratuita para uso?**  
A: Um teste gratuito está disponível para avaliação. A funcionalidade completa requer uma licença adquirida. Veja as [opções de compra](https://purchase.aspose.com/buy) para detalhes.

---

**Última atualização:** 2026-04-03  
**Testado com:** Aspose.PSD 24.12 para Java  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}