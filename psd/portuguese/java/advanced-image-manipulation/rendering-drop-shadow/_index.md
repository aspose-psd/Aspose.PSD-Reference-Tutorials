---
date: 2025-12-04
description: Aprenda a salvar PSD como PNG e aplicar uma sombra projetada usando Aspose.PSD
  para Java. Este guia aborda como adicionar sombra, converter PSD para PNG e aplicar
  sombra projetada em Java.
language: pt
linktitle: Apply Rendering Drop Shadow
second_title: Aspose.PSD Java API
title: Salvar PSD como PNG e adicionar sombra projetada com Aspose.PSD Java
url: /java/advanced-image-manipulation/rendering-drop-shadow/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Salvar PSD como PNG e Adicionar Sombra Projetada com Aspose.PSD Java

## Introdução

Se você trabalha com arquivos Photoshop em Java, **salvar PSD como PNG** enquanto adiciona uma sombra projetada de aparência profissional é uma necessidade comum. Aspose.PSD torna essa tarefa simples, permitindo que você **converta PSD para PNG** e **aplique sombra projetada Java** em apenas algumas linhas de código. Neste tutorial, percorreremos todo o processo, desde o carregamento de um arquivo PSD até a exportação do PNG final com o efeito de sombra renderizado.

## Respostas Rápidas
- **O que significa “salvar PSD como PNG”?** Converte um arquivo Photoshop em camadas para uma imagem PNG plana, preservando a transparência.  
- **Posso adicionar uma sombra projetada durante a conversão?** Sim — Aspose.PSD permite modificar os efeitos de camada antes da exportação.  
- **Preciso de licença para executar o código?** Uma avaliação gratuita funciona para testes; uma licença é necessária para produção.  
- **Qual versão do Java é suportada?** Java 8 ou superior.  
- **O efeito de sombra projetada é personalizável?** Absolutamente — você pode ajustar cor, opacidade, distância, tamanho, ângulo e muito mais.

## Pré‑requisitos

Antes de começarmos, certifique‑se de que você tem:

- **Ambiente de Desenvolvimento Java** – JDK 8 ou mais recente instalado.  
- **Biblioteca Aspose.PSD** – Baixe o JAR mais recente no site oficial [here](https://releases.aspose.com/psd/java/).  
- **Um arquivo PSD** – Um arquivo que contenha ao menos uma camada que você deseja realçar com sombra.  

## Como salvar PSD como PNG com sombra projetada em Java?

A seguir, um guia passo a passo. Cada passo inclui uma breve explicação seguida do código exato que você precisa copiar.

### Passo 1: Importar os Pacotes Necessários

Começamos importando as classes que fornecem carregamento de imagem, manipulação de efeitos e exportação para PNG.

```java
import com.aspose.psd.Image;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.layereffects.DropShadowEffect;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
import com.aspose.psd.Color;

import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.imageoptions.PngOptions;
```

### Passo 2: Definir o Diretório do Documento

Defina a pasta onde seu PSD de origem e o PNG resultante ficarão.

```java
String dataDir = "Your Document Directory";
```

### Passo 3: Definir os Caminhos dos Arquivos PSD e PNG

Especifique os caminhos completos para o PSD de entrada e o PNG de saída.

```java
String sourceFileName = dataDir + "Shadow.psd";
String pngExportPath = dataDir + "Shadowchanged1.png";
```

### Passo 4: Carregar o Arquivo PSD com Efeitos Habilitados

Habilitar **loadEffectsResource** garante que os efeitos de camada (como sombras) estejam disponíveis para manipulação.

```java
PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);

PsdImage im = (PsdImage) Image.load(sourceFileName, loadOptions);
```

### Passo 5: Acessar o Efeito de Sombra Projetada

Aqui buscamos o primeiro efeito aplicado à segunda camada (índice 1). É aqui que leremos ou modificaremos os parâmetros da sombra.

```java
DropShadowEffect shadowEffect = (DropShadowEffect) (im.getLayers()[1].getBlendingOptions().getEffects()[0]);
```

### Passo 6: Validar as Propriedades do Efeito de Sombra (Opcional, mas Útil)

Verificar as propriedades existentes ajuda a decidir se você precisa alterar algo. As asserções abaixo confirmam os valores padrão.

```java
Assert.areEqual(Color.getBlack(), shadowEffect.getColor());
Assert.areEqual(255, shadowEffect.getOpacity());
Assert.areEqual(3, shadowEffect.getDistance());
Assert.areEqual(7, shadowEffect.getSize());
Assert.areEqual(true, shadowEffect.getUseGlobalLight());
Assert.areEqual(90, shadowEffect.getAngle());
Assert.areEqual(0, shadowEffect.getSpread());
Assert.areEqual(0, shadowEffect.getNoise());
```

> **Dica profissional:** Se você quiser **como adicionar sombra** com configurações personalizadas, modifique as propriedades em `shadowEffect` antes de salvar (por exemplo, `shadowEffect.setColor(Color.getRed());`).

### Passo 7: Salvar a Imagem Modificada como PNG

Por fim, exportamos o PSD (com a sombra renderizada) para um arquivo PNG. A opção `TruecolorWithAlpha` preserva a transparência.

```java
PngOptions saveOptions = new PngOptions();
saveOptions.setColorType(PngColorType.TruecolorWithAlpha);
im.save(pngExportPath, saveOptions);
```

E pronto — um fluxo completo de **converter PSD para PNG** que também **aplica sombra projetada java** em uma única passagem.

## Por que usar Aspose.PSD para esta tarefa?

- **Nenhum Photoshop nativo necessário** – Funciona em qualquer plataforma que suporte Java.  
- **Fidelidade total ao PSD** – Todas as informações de camada, máscaras e efeitos são preservados.  
- **Controle granular** – Ajuste cada parâmetro da sombra projetada antes da exportação.  
- **Alto desempenho** – Otimizado para arquivos grandes e processamento em lote.

## Problemas Comuns & Solução de Problemas

| Sintoma | Causa provável | Correção |
|---------|----------------|----------|
| `NullPointerException` em `shadowEffect` | A camada alvo não possui efeitos ou o índice está errado. | Verifique o índice da camada (`im.getLayers()[i]`) e assegure que exista um efeito. |
| PNG exportado está em branco | Opções de PNG não configuradas corretamente ou imagem não salva. | Use `PngColorType.TruecolorWithAlpha` e confirme que o caminho em `im.save()` é gravável. |
| Cor da sombra não é visível | Opacidade da sombra definida como 0 ou cor coincide com o fundo. | Defina `shadowEffect.setOpacity(255);` e escolha uma cor contrastante. |

## Perguntas Frequentes

**P: Posso aplicar sombras projetadas a várias camadas ao mesmo tempo?**  
R: Sim. Percorra `im.getLayers()` e modifique cada `DropShadowEffect` conforme necessário.

**P: O que o parâmetro ‘Spread’ faz?**  
R: Controla quão abruptamente a sombra transita de totalmente opaca para transparente. Um spread maior cria uma borda mais dura.

**P: O Aspose.PSD é compatível com todas as versões do Photoshop?**  
R: Ele suporta uma ampla gama de versões PSD, desde lançamentos antigos até os arquivos mais recentes do Photoshop CC.

**P: Como obter ajuda se eu encontrar problemas?**  
R: Visite o [forum Aspose.PSD](https://forum.aspose.com/c/psd/34) para suporte da comunidade e assistência oficial.

**P: Posso testar o Aspose.PSD antes de comprar?**  
R: Absolutamente. Baixe uma avaliação gratuita no [site da Aspose](https://releases.aspose.com/).

---

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

**Última atualização:** 2025-12-04  
**Testado com:** Aspose.PSD 24.12 para Java  
**Autor:** Aspose  

---