---
date: 2026-01-07
description: Aprenda como recortar imagens em Java usando Aspose.PSD para Java. Guia
  passo a passo para recorte, redimensionamento e conversão de PSD para JPEG.
linktitle: Expand and Crop Images
second_title: Aspose.PSD Java API
title: 'Recortar Imagem Java: Expandir e Recortar Imagens com Aspose.PSD para Java'
url: /pt/java/image-editing/expand-and-crop-images/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Recortar Imagem Java: Expandir e Recortar Imagens com Aspose.PSD para Java

## Introdução

Neste tutorial você descobrirá como **crop image java** com a biblioteca Aspose.PSD. Seja para expandir uma tela, cortar bordas indesejadas ou converter um arquivo PSD para JPEG, as etapas abaixo o guiarão por um processo limpo e repetível. Cobriremos pré‑requisitos, declarações de importação e cada passo de codificação com explicações claras para que você possa aplicar a técnica em projetos do mundo real.

## Respostas Rápidas
- **Qual biblioteca lida com crop image java?** Aspose.PSD for Java.
- **Preciso de licença para desenvolvimento?** Um teste gratuito funciona para testes; uma licença comercial é necessária para produção.
- **Posso converter PSD para JPEG enquanto recorto?** Sim, usando `JpegOptions` junto com um retângulo de recorte.
- **O Java 8 é suportado?** Aspose.PSD suporta Java 8 e versões mais recentes.
- **Quanto tempo leva a implementação?** Normalmente menos de 10 minutos para uma operação básica de recorte.

## O que é “crop image java”?

Recortar uma imagem em Java significa selecionar uma região retangular da imagem fonte e descartar o restante. Com Aspose.PSD você pode definir essa região usando um objeto `Rectangle`, e então salvar o resultado em um formato diferente, como JPEG.

## Por que usar Aspose.PSD para recorte de imagens em Java?

- **Suporte total a PSD** – trabalhe diretamente com arquivos PSD em camadas sem precisar convertê-los primeiro.  
- **Manipulação raster de alto desempenho** – uso eficiente de memória para imagens grandes.  
- **Conversão integrada** – exporte facilmente para JPEG, PNG, BMP, etc., aplicando recorte ou expansão da tela.  
- **Multiplataforma** – funciona em qualquer sistema que execute Java.

## Pré‑requisitos

Antes de começarmos, certifique‑se de que você tem:

1. **Java Development Kit (JDK)** – Java 8 ou posterior instalado.  
2. **Aspose.PSD for Java** – baixe a biblioteca no site oficial **[here](https://releases.aspose.com/psd/java/)**.  

> **Dica profissional:** Adicione o JAR do Aspose.PSD ao classpath do seu projeto ou às dependências Maven/Gradle para evitar `ClassNotFoundException`.

## Importar Pacotes

Adicione as importações necessárias ao seu arquivo fonte Java. Essas classes dão acesso ao carregamento de imagens, manipulação raster, definição de retângulo e opções de exportação JPEG.

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;
import com.aspose.psd.Rectangle;

import com.aspose.psd.imageoptions.JpegOptions;
```

## Etapa 1: Defina o Diretório do Documento

Especifique a pasta que contém o arquivo PSD fonte. Substitua o placeholder pelo caminho real na sua máquina.

```java
String dataDir = "Your Document Directory";
```

## Etapa 2: Especifique os Caminhos de Origem e Destino

Defina de onde ler o PSD e onde gravar o JPEG recortado.

```java
String sourceFile = dataDir + "example1.psd";
String destName = dataDir + "jpeg_out.jpg";
```

## Etapa 3: Carregar e Cachear a Imagem

Carregue o PSD em um objeto `RasterImage`. O cache melhora o desempenho para operações subsequentes, como recorte.

```java
RasterImage rasterImage = (RasterImage)Image.load(sourceFile);
rasterImage.cacheData();
```

## Etapa 4: Criar Retângulo para Recorte

Crie um `Rectangle` que descreve a região que você deseja manter. As coordenadas podem ser negativas para **expandir** a tela antes do recorte, o que é útil para adicionar uma borda ao redor da imagem original.

```java
Rectangle destRect = new Rectangle(-200, -200, 300, 300);
```

> **Por que usar coordenadas negativas?**  
> Valores negativos de X/Y deslocam a área de recorte para a esquerda/acima, adicionando efetivamente espaço vazio (expansão) ao redor do conteúdo original antes do recorte final.

## Etapa 5: Salvar a Imagem Recortada

Finalmente, salve a imagem resultante usando `JpegOptions`. Esta etapa também demonstra **convert psd jpeg** ao aplicar o retângulo de recorte.

```java
rasterImage.save(destName, new JpegOptions(), destRect);
```

> **Resultado:** `jpeg_out.jpg` agora contém uma imagem de 300 × 300 pixels que foi expandida em 200 px em cada lado e então recortada para o retângulo definido.

Parabéns! Você realizou com sucesso **java image cropping**, expandiu a tela e converteu um arquivo PSD para JPEG — tudo em algumas linhas concisas de código.

## Casos de Uso Comuns

- **Preparar ativos para a web** – recorte e redimensione capturas de tela ou designs antes de fazer upload.  
- **Gerar miniaturas** – extraia uma região específica de um PSD grande para fins de pré‑visualização.  
- **Processamento em lote automatizado** – percorra uma pasta de arquivos PSD, aplicando o mesmo retângulo de recorte a cada um.

## Solução de Problemas e Dicas

| Problema | Correção Sugerida |
|----------|-------------------|
| `OutOfMemoryError` ao carregar PSDs grandes | Chame `rasterImage.cacheData()` cedo e considere aumentar o tamanho do heap da JVM (`-Xmx`). |
| Área recortada está fora do centro | Verifique os deslocamentos X/Y do retângulo; lembre‑se que valores negativos expandem a tela. |
| JPEG de saída parece borrado | Ajuste a configuração de qualidade de `JpegOptions` (ex.: `new JpegOptions { Quality = 90 }`). |

## Perguntas Frequentes

### Q1: O Aspose.PSD é compatível com diferentes versões do Java?

A1: Sim, o Aspose.PSD suporta várias versões do Java, garantindo compatibilidade com uma ampla gama de ambientes de desenvolvimento.

### Q2: Posso usar o Aspose.PSD em projetos comerciais?

A2: Absolutamente, o Aspose.PSD oferece licenças comerciais para desenvolvedores, permitindo seu uso tanto em projetos pessoais quanto comerciais.

### Q3: Existem limitações nos formatos de arquivo de imagem suportados?

A3: O Aspose.PSD suporta uma variedade de formatos de arquivo de imagem, incluindo PSD, JPEG, PNG e mais. Consulte a [documentation](https://reference.aspose.com/psd/java/) para a lista completa.

### Q4: Como posso obter suporte para dúvidas relacionadas ao Aspose.PSD?

A4: Visite o [Aspose.PSD forum](https://forum.aspose.com/c/psd/34) para buscar assistência da comunidade ou da equipe de suporte da Aspose.

### Q5: Existe uma versão de teste gratuita disponível?

A5: Sim, você pode explorar o Aspose.PSD com uma versão de teste gratuita. Baixe-a [here](https://releases.aspose.com/).

**Última Atualização:** 2026-01-07  
**Testado com:** Aspose.PSD for Java 24.12  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}