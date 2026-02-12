---
date: 2026-02-12
description: Aprenda como girar uma imagem em um ângulo específico em Java usando
  Aspose.PSD. Este guia mostra como girar a imagem, girar a imagem por graus e lidar
  com cores de fundo.
linktitle: How to Rotate Image on a Specific Angle
second_title: Aspose.PSD Java API
title: Como girar imagem em um ângulo específico com Aspose.PSD para Java
url: /pt/java/advanced-image-manipulation/rotate-image-specific-angle/
weight: 20
---

 top and bottom.

Let's produce the translated version.

We need to translate:

- Title: "How to Rotate Image on a Specific Angle with Aspose.PSD for Java" => "Como Rotacionar Imagem em um Ângulo Específico com Aspose.PSD para Java"

- Introduction, Quick Answers, etc.

We must keep bullet points, but translate text.

Also tables.

Make sure not to translate URLs.

Also keep code block placeholders unchanged.

Also keep the "## Quick Answers" etc.

Let's produce.

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Como Rotacionar Imagem em um Ângulo Específico com Aspose.PSD para Java

## Introdução

Se você precisa **rotacionar imagem** programaticamente em uma aplicação Java, o Aspose.PSD para Java oferece uma API limpa e de alto desempenho que cuida do trabalho pesado. Seja você quem está construindo um editor de fotos, gerando miniaturas ou preparando ativos para um serviço web, rotacionar uma imagem por um grau exato é um requisito comum. Neste tutorial vamos percorrer todo o processo — desde o carregamento de um arquivo PSD até a gravação do resultado rotacionado — destacando boas práticas como cache e tratamento em segundo plano.

## Respostas Rápidas
- **Qual biblioteca é a melhor para rotacionar imagens em Java?** Aspose.PSD para Java.  
- **Posso rotacionar em qualquer grau?** Sim, o método `rotate` aceita um ângulo `float` (positivo ou negativo).  
- **Preciso de licença para desenvolvimento?** Um trial gratuito funciona para testes; uma licença é necessária para produção.  
- **Quais formatos de imagem são suportados?** PSD, JPEG, PNG, TIFF, GIF, BMP e muitos outros.  
- **Como definir uma cor de fundo para o espaço vazio?** Passe uma instância `Color` para o método `rotate`.

## O que é Rotação de Imagem em Java?

Rotação de imagem significa girar a matriz de pixels ao redor de um ponto de pivô (geralmente o centro) por um ângulo determinado. Em Java, você pode fazer isso manualmente com `Graphics2D`, mas o Aspose.PSD abstrai a matemática, trata diferentes profundidades de cor e preserva informações de camada ao trabalhar com arquivos PSD.

## Por que Usar Aspose.PSD para Rotacionar Imagens?

- **Precisão:** Rotacione por qualquer grau fracionado sem perda de qualidade.  
- **Desempenho:** Cache interno (`image.cacheData()`) acelera arquivos grandes.  
- **Controle de Fundo:** Especifique uma cor de fundo para preencher os vazios criados pela rotação.  
- **Flexibilidade de Formato:** Carregue PSD, exporte JPEG, PNG ou qualquer formato suportado.

## Pré‑requisitos

Antes de começar, certifique‑se de que você tem o seguinte:

1. **Java Development Kit (JDK 8 ou superior)** – um IDE Java funcional ou configuração via linha de comando.  
2. **Aspose.PSD para Java** – baixe o JAR mais recente na [página Aspose.PSD Java](https://reference.aspose.com/psd/java/).  
3. **Arquivo PSD de exemplo** – por exemplo, `sample.psd` colocado em uma pasta que você possa referenciar no código.

## Importar Pacotes

Primeiro, importe as classes que usaremos. Essas importações permanecem as mesmas independentemente do ângulo de rotação escolhido.

```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.imageoptions.JpegOptions;
```

## Guia Passo a Passo

### Passo 1: Defina Seu Diretório de Documentos

Defina a pasta que contém o PSD de origem e onde a saída será gravada.

```java
String dataDir = "Your Document Directory";
```

> **Dica profissional:** Use um caminho absoluto ou `System.getProperty("user.dir")` para evitar surpresas com caminhos relativos.

### Passo 2: Especifique os Caminhos de Arquivo de Origem e Destino

```java
String sourceFile = dataDir + "sample.psd";
String destName = dataDir + "RotatingImageOnSpecificAngle_out.jpg";
```

Você pode mudar `destName` para qualquer extensão suportada (`.png`, `.tiff`, etc.) conforme suas necessidades de saída.

### Passo 3: Carregue a Imagem

```java
RasterImage image = (RasterImage)Image.load(sourceFile);
```

`Image.load` detecta automaticamente o formato do arquivo e devolve um `RasterImage` concreto para operações baseadas em raster.

### Passo 4: Cache dos Dados da Imagem (Opcional, mas Recomendado)

```java
if (!image.isCached())
{
    image.cacheData();
}
```

O cache armazena os pixels da imagem na memória, o que acelera transformações subsequentes — especialmente útil para arquivos PSD grandes.

### Passo 5: Rotacione a Imagem

```java
image.rotate(20f, true, Color.getRed());
```

- **20f** – ângulo de rotação em graus (float). Altere esse valor para rotacionar em qualquer ângulo, por exemplo, `-45f` para sentido anti‑horário.  
- **true** – mantém a proporção original enquanto expande a tela para acomodar a imagem rotacionada.  
- **Color.getRed()** – cor de fundo que preenche os cantos vazios criados pela rotação. Substitua por `Color.getWhite()` ou qualquer cor personalizada conforme necessário.

#### Rotacionar Imagem por Graus em Java

O método `rotate` aceita qualquer valor de ponto flutuante, então você pode **rotacionar imagem por graus** como `30f`, `90f` ou `-15f`. Valores positivos giram no sentido horário, enquanto valores negativos giram no sentido anti‑horário.

#### Rotacionar Imagem em Ângulo Específico Usando Aspose.PSD

Como o método trabalha com um `float`, você pode especificar um **rotate image specific angle** como `22.5f` para controle preciso em fluxos de trabalho de design gráfico.

#### Resumo do Exemplo de Rotação de Imagem em Java

Todas as etapas acima demonstram um fluxo completo de **rotate image java** — do carregamento do arquivo à gravação da saída rotacionada.

### Passo 6: Salve o Resultado

```java
image.save(destName, new JpegOptions());
```

`JpegOptions` permite controlar qualidade, compressão e outras configurações específicas do JPEG. Para saída sem perdas, troque por `PngOptions`.

## Problemas Comuns e Soluções

| Problema | Causa | Solução |
|----------|-------|---------|
| **Cantos vazios após a rotação** | Nenhuma cor de fundo fornecida | Passe um `Color` (ex.: `Color.getWhite()`) para `rotate`. |
| **Erro de falta de memória em PSDs grandes** | Imagem não foi cacheada | Chame `image.cacheData()` antes do processamento. |
| **Direção do ângulo incorreta** | Confusão entre ângulo negativo e positivo | Use valores negativos para rotação no sentido horário (ou vice‑versa, dependendo do seu sistema de coordenadas). |
| **Alterações não salvas** | Esquecimento de chamar `save` | Garanta que `image.save(...)` seja executado após a rotação. |

## Perguntas Frequentes

**P: Posso rotacionar imagens com transparência usando Aspose.PSD para Java?**  
R: Sim. A biblioteca preserva canais alfa; basta não especificar uma cor de fundo opaca se quiser cantos transparentes.

**P: Existem limitações nos formatos de arquivo suportados para rotação?**  
R: Não. Aspose.PSD suporta PSD, JPEG, PNG, TIFF, GIF, BMP, JPEG2000, WMF, EMF e muitos outros.

**P: Posso rotacionar imagens por um ângulo negativo?**  
R: Absolutamente. Passe um float negativo para `rotate` (ex.: `-30f`) para girar no sentido horário.

**P: Aspose.PSD fornece pré‑visualização em tempo real durante a rotação?**  
R: A API funciona apenas no lado do servidor. Para pré‑visualizações ao vivo, integre o bitmap rotacionado a um framework UI (Swing, JavaFX) e atualize a visualização.

**P: Existe um fórum da comunidade para Aspose.PSD onde eu possa buscar ajuda?**  
R: Sim, visite o [fórum Aspose.PSD](https://forum.aspose.com/c/psd/34) para fazer perguntas e compartilhar experiências.

## Conclusão

Agora você sabe **como rotacionar imagem** em um ângulo específico usando Aspose.PSD para Java. Aproveitando cache, controle de cor de fundo e opções flexíveis de saída, você pode integrar funcionalidade de rotação precisa em qualquer fluxo de trabalho de imagens baseado em Java.

---

**Última atualização:** 2026-02-12  
**Testado com:** Aspose.PSD para Java 24.11 (última versão na data de escrita)  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}