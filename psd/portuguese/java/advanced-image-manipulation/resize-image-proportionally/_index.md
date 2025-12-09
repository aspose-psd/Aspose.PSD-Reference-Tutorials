---
date: 2025-12-08
description: Aprenda a converter PSD para PNG e redimensionar imagens proporcionalmente
  em Java usando Aspose.PSD. Este tutorial passo a passo aborda o cache de imagens,
  o redimensionamento e a gravação como PNG.
linktitle: Convert PSD to PNG & Resize Proportionally
second_title: Aspose.PSD Java API
title: Como Converter PSD para PNG e Redimensionar Proporcionalmente com Aspose.PSD
  para Java
url: /pt/java/advanced-image-manipulation/resize-image-proportionally/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Como Converter PSD para PNG e Redimensionar Proporcionalmente com Aspose.PSD para Java

## Introdução

Se você precisa **converter PSD para PNG** mantendo a proporção original, você está no lugar certo. Neste tutorial, percorreremos um **tutorial Aspose.PSD** completo que mostra **como redimensionar imagem** proporcionalmente em Java, armazenar em cache a imagem para desempenho ideal e, finalmente, salvar o resultado como PNG. Ao final, você poderá integrar esse fluxo de trabalho em qualquer pipeline de processamento de imagens baseado em Java.

## Respostas Rápidas
- **Aspose.PSD pode converter PSD para PNG?** Sim – basta carregar o PSD e salvá-lo com `PngOptions`.
- **A biblioteca suporta redimensionamento proporcional?** Absolutamente; use `resizeWidthProportionally` e `resizeHeightProportionally`.
- **Preciso armazenar a imagem em cache primeiro?** O cache (`image.cacheData()`) melhora o desempenho para arquivos PSD grandes.
- **Qual versão do Java é necessária?** Java 8 ou superior é totalmente suportado.
- **É necessária uma licença para produção?** Sim, uma licença comercial remove as marcas d'água de avaliação.

## O que é “converter PSD para PNG” e por que isso importa?

Converter um documento Photoshop (PSD) para um arquivo portable network graphics (PNG) permite que você compartilhe designs em camadas como um formato leve e amigável para a web. PNG mantém a transparência e a qualidade sem perdas, tornando‑lo ideal para ativos de UI, miniaturas ou qualquer cenário onde a fidelidade da imagem seja importante.

## Por que redimensionar a imagem proporcionalmente em Java?

Redimensionar **como redimensionar imagem** sem distorcer sua proporção garante que os gráficos pareçam naturais em diferentes telas. A API `Aspose.PSD` fornece métodos dedicados para escalonamento proporcional, que calculam automaticamente a altura ou largura correspondente, poupando você de erros de cálculo manual.

## Pré‑requisitos

Antes de mergulharmos no código, certifique‑se de que você tem:

1. **Java Development Kit (JDK)** – Java 8 ou posterior instalado.
2. **Aspose.PSD for Java** – baixe o JAR mais recente no site oficial [here](https://releases.aspose.com/psd/java/).
3. Um arquivo PSD de exemplo (`sample.psd`) colocado em um diretório que você possa referenciar a partir do seu projeto.

## Importar Pacotes

Adicione as importações necessárias à sua classe Java. Essas classes dão acesso ao carregamento de imagens, cache, redimensionamento e opções de saída PNG.

```java
import com.aspose.psd.Image;
import com.aspose.psd.imageoptions.PngOptions;
```

## Etapa 1: Carregar a Imagem PSD

Primeiro, carregue o arquivo PSD de origem. Se o arquivo for grande, armazenar em cache os dados da imagem reduz o consumo de memória ao executar operações subsequentes.

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

Image image = Image.load(sourceFile);

if (!image.isCached()) {
    // Image caching java – improves performance for large files
    image.cacheData();
}
```

## Etapa 2: Redimensionar a Imagem Proporcionalmente (Java)

Agora decida as novas dimensões. Neste exemplo, reduzimos a imagem para **metade** do seu tamanho original, preservando a proporção. Você pode ajustar a largura ou altura alvo conforme necessário.

```java
int newWidth = image.getWidth() / 2;
image.resizeWidthProportionally(newWidth);

int newHeight = image.getHeight() / 2;
image.resizeHeightProportionally(newHeight);
```

> **Dica profissional:** Use `resizeWidthProportionally` *ou* `resizeHeightProportionally` — a biblioteca calcula automaticamente a outra dimensão para manter a imagem proporcional.

## Etapa 3: Salvar a Imagem Redimensionada como PNG

Finalmente, exporte a imagem redimensionada para o formato PNG. Esta etapa completa o fluxo de trabalho de **converter PSD para PNG**.

```java
String destName = dataDir + "SimpleResizeImageProportionally_out.png";
image.save(destName, new PngOptions());
```

Quando o código for executado, você encontrará um arquivo PNG que tem metade do tamanho do PSD original, com a mesma qualidade visual e sem distorção.

## Problemas Comuns & Soluções

| Problema | Causa | Correção |
|----------|-------|----------|
| **OutOfMemoryError** | PSD grande não armazenado em cache | Chame `image.cacheData()` antes de redimensionar |
| **Saída PNG em branco** | Caminho de arquivo incorreto | Verifique `dataDir` e permissões de gravação |
| **Proporção da imagem parece errada** | Usando largura e altura manualmente | Use os métodos proporcionais fornecidos pelo Aspose.PSD |

## Perguntas Frequentes

**Q: O Aspose.PSD é compatível com todos os formatos de imagem?**  
A: Aspose.PSD suporta PSD, PNG, JPEG, BMP, GIF e muitos outros. Veja a lista completa na [documentação](https://reference.aspose.com/psd/java/).

**Q: Posso usar o Aspose.PSD em projetos comerciais?**  
A: Sim. Compre uma licença comercial na [loja Aspose](https://purchase.aspose.com/buy).

**Q: Licenças temporárias estão disponíveis para testes?**  
A: Absolutamente – solicite uma licença temporária [aqui](https://purchase.aspose.com/temporary-license/) para fins de avaliação.

**Q: Onde posso encontrar suporte da comunidade?**  
A: O [fórum Aspose.PSD](https://forum.aspose.com/c/psd/34) é um ótimo lugar para fazer perguntas e compartilhar soluções.

**Q: Como acesso a referência completa da API?**  
A: Documentação detalhada da API está disponível [aqui](https://reference.aspose.com/psd/java/).

## Conclusão

Agora você sabe como **converter PSD para PNG**, redimensionar a imagem proporcionalmente e lidar com cache de forma eficiente usando Aspose.PSD para Java. Incorpore essas etapas em suas próprias aplicações para oferecer processamento de imagens rápido e de alta qualidade sem depender de instalações nativas do Photoshop.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Last Updated:** 2025-12-08  
**Tested With:** Aspose.PSD 24.12 for Java  
**Author:** Aspose