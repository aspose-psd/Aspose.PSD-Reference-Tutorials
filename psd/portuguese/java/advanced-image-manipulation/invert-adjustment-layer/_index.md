---
date: 2026-11-04
description: Aprenda a usar Aspose.PSD para Java para aplicar uma camada de ajuste
  de inversão, processar em lote imagens PSD e criar arquivos PSD de imagem negativa.
keywords:
- how to use aspose
- batch process psd images
- create negative image psd
- image processing java library
- apply multiple adjustment layers
lastmod: 2026-11-04
linktitle: Invert Adjustment Layer
og_description: Como usar Aspose.PSD para Java para adicionar uma camada de ajuste
  de inversão, processar em lote imagens PSD e criar um PSD de imagem negativa. Siga
  o guia passo a passo.
og_image_alt: Screenshot showing Aspose.PSD Java code adding an invert adjustment
  layer
og_title: Como usar Aspose.PSD para adicionar uma camada de ajuste de inversão em
  Java
schemas:
- author: Aspose
  dateModified: '2026-11-04'
  description: Learn how to use Aspose.PSD for Java to apply an invert adjustment
    layer, batch process PSD images, and create negative image PSD files.
  headline: How to use Aspose.PSD to add an invert adjustment layer in Java
  type: TechArticle
- questions:
  - answer: Yes, it supports Java 6.0 and later, including Java 8, 11, and 17.
    question: Is Aspose.PSD compatible with all Java versions?
  - answer: Absolutely. After adding the invert layer you can call `addBrightnessAdjustmentLayer()`,
      `addHueSaturationAdjustmentLayer()`, etc., to stack effects.
    question: Can I apply multiple adjustment layers in a single operation?
  - answer: The complete documentation is available [Aspose.PSD Java API reference](https://reference.aspose.com/psd/java/).
    question: Where can I find the full API reference?
  - answer: Yes, you can download a trial version [Aspose.PSD trial download](https://releases.aspose.com/).
    question: Is there a free trial for Aspose.PSD?
  - answer: Request a temporary license [temporary license request page](https://purchase.aspose.com/temporary-license/).
    question: How do I obtain a temporary license for testing?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- aspose psd
- java image processing
- invert adjustment layer
- batch psd processing
title: Como usar Aspose.PSD para adicionar uma camada de ajuste de inversão em Java
url: /pt/java/advanced-image-manipulation/invert-adjustment-layer/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Como usar Aspose.PSD para adicionar uma camada de ajuste Inverter em Java

## Introdução

Se você está procurando uma robusta **biblioteca Java de processamento de imagens**, Aspose.PSD for Java é uma das opções mais versáteis do mercado. Neste tutorial você verá **como usar Aspose** para inserir uma **Camada de Ajuste Inverter** em um arquivo PSD, empilhá‑la com outros ajustes e até executar a operação em dezenas de arquivos. Seja construindo uma ferramenta de processamento em lote, um serviço de imagens no lado do servidor ou um editor de imagem único, os passos abaixo levarão você do PSD de origem a uma imagem negativa totalmente editável em minutos.

## Respostas Rápidas
- **O que a Camada de Ajuste Inverter faz?** Ela inverte cada valor RGB na área selecionada, transformando a imagem em um negativo fotográfico.  
- **Qual biblioteca fornece esse recurso?** Aspose.PSD, uma **biblioteca Java de processamento de imagens** líder.  
- **Posso empilhá‑la com outros ajustes?** Sim – você pode **aplicar múltiplas camadas de ajuste** como Brilho/Contraste, Matiz/Saturação, e mais.  
- **Preciso de uma licença para desenvolvimento?** Uma versão de avaliação gratuita está disponível; uma licença é necessária para uso em produção.  
- **Quanto tempo leva a implementação?** Normalmente menos de 10 minutos para um caso de uso básico.

## O que é a Camada de Ajuste Inverter?

A Camada de Ajuste Inverter é uma edição não destrutiva que inverte os valores de cor de cada pixel que afeta. Como ela fica acima da pilha de camadas, você pode alternar sua visibilidade ou reordená‑la sem alterar permanentemente os dados da imagem original. Esta é a maneira mais rápida de **criar arquivos PSD de imagem negativa** ou obter um visual clássico de negativo de filme.

## Por que usar Aspose.PSD como sua biblioteca Java de processamento de imagens?

Aspose.PSD suporta **mais de 200 recursos PSD**, pode ler e gravar arquivos Photoshop sem precisar do Photoshop, e processa documentos com centenas de páginas usando menos de 500 MB de memória heap. Ele funciona em qualquer runtime Java (Java 6+), tornando‑o ideal para **processamento em lote de imagens PSD** em servidores Windows, Linux ou macOS.

## Pré‑requisitos

Antes de começar, certifique‑se de que você tem:

1. **Aspose.PSD for Java** – faça o download do JAR mais recente no site oficial [Aspose.PSD for Java download page](https://releases.aspose.com/psd/java/).  
2. **Java Development Kit** – JDK 6.0 ou superior instalado e configurado no seu `PATH`.  

Agora você está pronto para escrever o código.

## Importar pacotes

A classe `PsdImage` representa um documento Photoshop completo na memória, enquanto as classes de camada de ajuste estão no pacote `com.aspose.psd.layers.adjustments`.

A classe `PsdImage` é o objeto de nível superior do Aspose.PSD que encapsula a estrutura e os dados de pixel de um arquivo PSD. Importe os namespaces e então você poderá carregar, editar e salvar arquivos PSD.

## Etapa 1: configurar o diretório do documento

Defina a pasta que contém seu arquivo PSD de origem e onde a saída será salva. Usar caminhos absolutos evita `NullPointerException` quando o diretório de trabalho mudar.

## Etapa 2: carregar o arquivo PSD

Carregue o arquivo de origem em um objeto `PsdImage`. Este objeto mantém toda a hierarquia de camadas na memória, permitindo edições não destrutivas.

A classe `PsdImage` fornece um método estático `load` que lê o cabeçalho do arquivo, valida o formato e constrói uma representação em memória pronta para manipulação.

## Etapa 3: adicionar camada de ajuste Inverter

Chame o método incorporado para inserir uma Camada de Ajuste Inverter no topo da pilha de camadas atual. Você pode posteriormente adicionar mais camadas (por exemplo, Brilho, Matiz) para **aplicar múltiplas camadas de ajuste** em um único fluxo de trabalho.

`addInvertAdjustmentLayer()` adiciona uma Camada de Ajuste Inverter à coleção de camadas do PSD.

## Etapa 4: salvar a saída

Grave o PSD modificado no disco.  

`save()` grava o arquivo PSD, incluindo todas as camadas e metadados, no caminho especificado.

A gravação usa o mesmo método `save` que escreve o documento completo, incluindo todas as camadas de ajuste, máscaras e metadados, no formato especificado.

### O que acabou de acontecer?

O arquivo PSD foi carregado em um objeto `PsdImage`, uma `InvertAdjustmentLayer` foi criada e adicionada como a camada superior, e o documento foi salvo. Essa sequência preserva os dados da imagem original enquanto adiciona um efeito de inversão não destrutivo que pode ser alternado ou reordenado posteriormente.

Você usou com sucesso o Aspose.PSD, uma **biblioteca Java de processamento de imagens**, para manipular um arquivo PSD.

## Como processar imagens PSD em lote com ajuste Inverter?

Carregue cada arquivo dentro de um loop `for`, aplique os mesmos passos e chame `save` a cada iteração. Como o Aspose.PSD processa arquivos de forma streaming, você pode lidar com **centenas de PSDs** mantendo o uso de memória abaixo de 300 MB reutilizando a mesma instância `PsdImage`.

## Como converter um PSD em uma imagem negativa?

Adicione a Camada de Ajuste Inverter como o item superior e salve o documento – essa operação equivale a **converter PSD para negativo**. Você pode posteriormente desativar ou excluir a camada para retornar à aparência original sem recarregar o arquivo de origem.

## Problemas comuns e dicas

| Problema | Causa | Solução |
|----------|-------|----------|
| **NullPointerException em `Image.load`** | Caminho do arquivo incorreto ou arquivo ausente | Verifique `dataDir` e o nome do arquivo; use caminhos absolutos para teste |
| **Ordem das camadas não como esperado** | Adicionar camadas após as existentes altera a pilha | Insira a camada Inverter antes de outros ajustes, ou reordene via `psdImage.getLayers().move()` |
| **Desaceleração de desempenho em PSDs grandes** | Carregar arquivos muito grandes na memória | Aumente o heap da JVM (`-Xmx2g`) ou processe arquivos em blocos usando `psdImage.getPages().get(0).getResources().setMemoryOptimized(true)` |

## Perguntas frequentes

**P: O Aspose.PSD é compatível com todas as versões do Java?**  
R: Sim, ele suporta Java 6.0 e posteriores, incluindo Java 8, 11 e 17.

**P: Posso aplicar múltiplas camadas de ajuste em uma única operação?**  
R: Absolutamente. Depois de adicionar a camada Inverter, você pode chamar `addBrightnessAdjustmentLayer()`, `addHueSaturationAdjustmentLayer()`, etc., para empilhar efeitos.

**P: Onde posso encontrar a referência completa da API?**  
R: A documentação completa está disponível [Aspose.PSD Java API reference](https://reference.aspose.com/psd/java/).

**P: Existe uma versão de avaliação gratuita para o Aspose.PSD?**  
R: Sim, você pode baixar uma versão de avaliação [Aspose.PSD trial download](https://releases.aspose.com/).

**P: Como obtenho uma licença temporária para teste?**  
R: Solicite uma licença temporária [temporary license request page](https://purchase.aspose.com/temporary-license/).

---

**Última atualização:** 2026-11-04  
**Testado com:** Aspose.PSD 24.12 for Java  
**Autor:** Aspose  









```java
import com.aspose.psd.Image;

import com.aspose.psd.fileformats.psd.PsdImage;
```

```java
String dataDir = "Your Document Directory";
```

```java
String filePath = dataDir + "InvertStripes_before.psd";
String outputPath = dataDir + "InvertStripes_after.psd";

PsdImage im = (PsdImage)Image.load(filePath);
```

```java
im.addInvertAdjustmentLayer();
```

```java
im.save(outputPath);
```

## Tutoriais Relacionados

- [Adicionar Camada de Ajuste de Nível a Arquivos PSD com Aspose.PSD para Java](/psd/java/modifying-converting-psd-images/add-level-adjustment-layer-psd/)
- [Como Adicionar Camada de Ajuste – Misturador de Canal em PSD (Java)](/psd/java/modifying-converting-psd-images/add-channel-mixer-adjustment-layer-psd/)
- [Como Editar PSD - Adicionar Camada de Ajuste de Curvas Usando Java](/psd/java/modifying-converting-psd-images/add-curves-adjustment-layer-psd/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}