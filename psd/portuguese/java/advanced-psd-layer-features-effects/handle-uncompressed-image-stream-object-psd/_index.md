---
date: 2026-08-01
description: Aprenda como exportar PSD para PNG e lidar com fluxos de imagem não compactados
  usando Aspose.PSD para Java.
keywords:
- export psd to png
- save psd as png
- java image manipulation
lastmod: 2026-08-01
linktitle: Manipular objeto de fluxo de imagem não compactado em PSD - Java
og_description: exportar psd para png usando Aspose.PSD para Java. Aprenda a lidar
  com fluxos de imagem não compactados, criar objetos gráficos e salvar PNGs de alta
  qualidade.
og_image_alt: 'Developer guide: Export PSD to PNG with uncompressed stream using Aspose.PSD
  Java'
og_title: exportar psd para png – guia Java para fluxos PSD não compactados
schemas:
- author: Aspose
  dateModified: '2026-08-01'
  description: Learn how to export PSD to PNG and handle uncompressed image streams
    with Aspose.PSD for Java.
  headline: Export PSD to PNG – Create PSD Graphics Object – Uncompressed Stream in
    Java
  type: TechArticle
- questions:
  - answer: Yes. After loading the PSD, retrieve the desired layer via `psdImage.getLayers().get_Item(index)`
      and pass that layer to the `Graphics` constructor.
    question: Can I use the graphics object to edit only one specific layer?
  - answer: Raw stores pixel data without any compression, so the resulting file is
      larger than a compressed PSD, but it guarantees 100 % pixel fidelity.
    question: Does the Raw compression method affect file size?
  - answer: Absolutely. After editing, call `psdImage.save("output.png", new PngOptions())`—this
      is the standard way to **export PSD to PNG** with lossless quality.
    question: Is it possible to export the edited PSD to another format (e.g., PNG)?
  - answer: Aspose.PSD for Java supports JDK 8 and later, including all LTS releases
      up to JDK 21.
    question: What Java version is required?
  - answer: Invoke `psdImage.dispose()` and close any streams (e.g., `ms.close()`)
      to free native memory and avoid leaks.
    question: How do I release resources after processing?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- export psd
- Aspose.PSD
- Java image processing
- uncompressed stream
- PSD graphics
title: Exportar PSD para PNG – Criar objeto gráfico PSD – Fluxo não compactado em
  Java
url: /pt/java/advanced-psd-layer-features-effects/handle-uncompressed-image-stream-object-psd/
weight: 26
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Exportar PSD para PNG – Criar objeto gráfico PSD – Fluxo não compactado em Java

## Introdução
Neste guia passo a passo você **exportará PSD para PNG** enquanto trabalha com um fluxo de imagem não compactado usando Aspose.PSD para Java. Seja automatizando um pipeline de design ou construindo um editor personalizado, a capacidade de renderizar um arquivo Photoshop sem perder qualidade é essencial. Começaremos com a configuração necessária, percorreremos a criação de um objeto `Graphics` e finalizaremos com a exportação PNG sem perdas. Ao final, você entenderá por que o Aspose.PSD lida eficientemente com fluxos brutos e como integrá‑lo a qualquer projeto Java.

## Respostas Rápidas
- **O que significa “criar objeto gráfico PSD”?** Significa instanciar um contexto `Graphics` que permite desenhar ou modificar uma imagem PSD programaticamente.  
- **Qual biblioteca lida com fluxos não compactados?** Aspose.PSD para Java fornece suporte total para dados de imagem brutos (não compactados).  
- **Posso exportar PSD para PNG após a edição?** Sim—uma vez que você tenha um objeto `Graphics` pode renderizar o PSD e salvá‑lo como PNG em uma única chamada.  
- **Preciso de licença para desenvolvimento?** Uma avaliação gratuita funciona para testes; uma licença comercial é necessária para implantações em produção.  
- **A exportação é sem perdas?** Exportar para PNG preserva os dados de pixel originais, oferecendo qualidade sem perdas com um tamanho de arquivo menor que o PSD bruto.

## O que é exportar psd para png?
Exportar PSD para PNG converte um documento Photoshop em camadas em uma imagem raster única e sem perdas que pode ser exibida por qualquer navegador web ou visualizador de imagens. O processo mantém transparência, profundidade de cor e efeitos de camada enquanto descarta metadados específicos do Photoshop. Também preserva o perfil de cor original para reprodução de cor precisa.

## Por que usar Aspose.PSD para Java na manipulação de imagens?
Aspose.PSD suporta **mais de 50** formatos de entrada e saída—including PSD, PNG, JPEG, BMP e TIFF—e pode processar arquivos com **mais de 200** camadas sem carregar todo o documento na memória. Sua opção de compressão `Raw` armazena os dados de pixel sem compactação, garantindo fidelidade pixel‑perfeita para edição posterior ou arquivamento.

## Pré-requisitos
Antes de mergulharmos no código, verifique se você tem o seguinte:

- **Java Development Kit (JDK)** – JDK 8 ou posterior instalado.  
- **Aspose.PSD para Java** – Baixe o JAR mais recente na página oficial de lançamentos: [Aspose.PSD Java download](https://releases.aspose.com/psd/java/). Você também pode acessá‑lo via [este link](https://releases.aspose.com/psd/java/) ou a [página de lançamentos](https://releases.aspose.com/psd/java/). Para outros produtos Aspose, clique [aqui](https://releases.aspose.com/).  
- **IDE** – IntelliJ IDEA, Eclipse ou qualquer editor compatível com Java.  
- **Conhecimento básico de Java** – Familiaridade com classes, métodos e tratamento de exceções.

Com esses itens em mãos, você está pronto para começar a codificar.

## Importar Pacotes
A classe `Graphics` é a superfície de desenho do Aspose.PSD que permite renderizar ou editar dados de pixel diretamente. A classe `PsdImage` representa um arquivo PSD na memória, enquanto `PsdOptions` controla como a imagem é salva.

```java
import com.aspose.psd.Graphics;
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.CompressionMethod;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.PsdOptions;
import java.io.ByteArrayInputStream;
import java.io.ByteArrayOutputStream;
```

Agora, vamos dividir o código em etapas digestíveis para que você possa acompanhar facilmente. Configuraremos o ambiente, carregaremos um arquivo PSD, o manipularemos e, finalmente, salvaremos a saída.

## Etapa 1: Definir o Diretório do Documento
Antes de qualquer operação de arquivo, você precisa informar ao programa onde procurar seus recursos PSD. Este caminho de diretório é usado ao longo do tutorial.

```java
String dataDir = "Your Document Directory";
```

Substitua `"Your Document Directory"` pelo caminho absoluto que contém `layers.psd`. Manter o caminho configurável torna o código reutilizável em diferentes projetos.

## Etapa 2: Criar um ByteArrayOutputStream
Um `ByteArrayOutputStream` é um stream Java que mantém os dados na memória como um array de bytes. Ele funciona como um buffer em memória para a imagem modificada, permitindo capturar os bytes brutos antes de gravá‑los no disco ou enviá‑los pela rede.

```java
ByteArrayOutputStream ms = new ByteArrayOutputStream();
```

A variável `ms` armazenará os dados de imagem não compactados após a operação `save`.

## Etapa 3: Carregar o Arquivo PSD
A classe `PsdImage` carrega um arquivo PSD na memória para manipulação. Carregar o arquivo converte o PSD em disco em um objeto `PsdImage` que pode ser manipulado. Esta etapa é onde o Aspose.PSD lê o cabeçalho do arquivo, camadas e recursos.

```java
PsdImage psdImage = (PsdImage) Image.load(dataDir + "layers.psd");
```

Se o caminho estiver incorreto, o Aspose.PSD lança uma `FileNotFoundException`, que você deve capturar em código de produção.

## Etapa 4: Configurar o PsdOptions para Salvamento
`PsdOptions` especifica os parâmetros de salvamento para arquivos PSD. Definir o método de compressão para `Raw` indica que os dados de pixel devem ser armazenados sem compressão, preservando cada pixel exatamente como aparece na memória.

```java
PsdOptions saveOptions = new PsdOptions();
saveOptions.setCompressionMethod(CompressionMethod.Raw);
```

A opção `CompressionMethod.Raw` armazena os dados de pixel sem qualquer compressão, o que é ideal quando você planeja realizar edições adicionais posteriormente.

## Etapa 5: Salvar a Imagem no Stream de Saída
Agora você persiste o PSD (com quaisquer modificações) no `ByteArrayOutputStream` criado anteriormente. O método `save` respeita as `PsdOptions` configuradas.

```java
psdImage.save(ms, saveOptions);
```

Neste ponto, `ms` contém a representação binária completa do PSD não compactado.

## Etapa 6: Redefinir o Stream de Saída
Após a gravação, o ponteiro interno do stream fica no final. Redefini‑lo rebobina o stream para que você possa ler a partir do início.

```java
ms.reset();
```

Pense nisso como mover a cabeça da fita de volta ao início antes da reprodução.

## Etapa 7: Carregar a Imagem recém‑criada
Agora você pode criar uma nova instância de `PsdImage` diretamente a partir do array de bytes. Esta etapa verifica se os dados salvos podem ser recarregados sem corrupção.

```java
PsdImage img = (PsdImage) Image.load(new ByteArrayInputStream(ms.toByteArray()));
```

Se a imagem for carregada com sucesso, você sabe que o fluxo não compactado foi gravado corretamente.

## Etapa 8: Criar o Objeto Graphics
A classe `Graphics` é a tela de desenho do Aspose.PSD. Ela fornece métodos para desenhar formas, texto e aplicar filtros diretamente na matriz de pixels de um `PsdImage`.

```java
Graphics graphics = new Graphics(psdImage);
```

Com esta instância de `Graphics` você pode pintar novo conteúdo, apagar partes ou compor camadas adicionais.

## Como exportar PSD para PNG usando Aspose.PSD para Java?
Carregue o PSD com `new PsdImage(dataDir + "layers.psd")`, crie um objeto `Graphics`, execute os desenhos necessários e, em seguida, chame `psdImage.save("output.png", new PngOptions())`. Essa sequência renderiza o PSD editado e grava um PNG sem perdas em um único passo, aproveitando o motor de conversão interno do Aspose.PSD.

## Manipular Camadas PSD com o Objeto Graphics
Ter uma instância de `Graphics` oferece controle ao nível de pixel sobre cada camada. Você pode desenhar formas geométricas, renderizar texto ou aplicar filtros personalizados. Como o contexto gráfico trabalha na visualização rasterizada da camada, as alterações são imediatamente visíveis ao salvar a imagem.

## Problemas Comuns e Soluções
- **NullPointerException ao carregar o arquivo** – verifique o caminho `dataDir` e assegure‑se de que o nome do arquivo corresponde exatamente, incluindo diferenciação de maiúsculas e minúsculas.  
- **Saída compactada apesar de usar Raw** – verifique se `saveOptions.setCompressionMethod(CompressionMethod.Raw);` é chamado **antes** de invocar `save`.  
- **Objeto Graphics aparece em branco** – certifique‑se de que está desenhando na instância correta de `PsdImage` (a que foi carregada, não uma imagem vazia recém‑criada).  
- **OutOfMemoryError em arquivos grandes** – use `PsdImage.load(dataDir, LoadOptions)` com `loadOptions.setLoadMode(LoadMode.Memory)` para transmitir arquivos grandes sem carregar todo o documento na RAM.

## Perguntas Frequentes
### O que é Aspose.PSD?
Aspose.PSD é uma biblioteca Java que permite a desenvolvedores criar, editar e converter arquivos Photoshop PSD programaticamente sem precisar do Adobe Photoshop. Ela suporta leitura e gravação de arquivos PSD, manipulação de camadas, máscaras, canais e diversos recursos de imagem, além de fornecer APIs para operações raster e vetoriais, sendo adequada para processamento de imagens no lado do servidor e tarefas de automação.

### Como posso baixar Aspose.PSD para Java?
Você pode baixá‑lo na página oficial de lançamentos: [Aspose.PSD Java download](https://releases.aspose.com/psd/java/).

### Existe uma versão de teste gratuita para Aspose.PSD?
Sim, uma avaliação totalmente funcional está disponível na mesma página de download. Ela funciona para desenvolvimento e avaliação.

### Posso obter suporte para Aspose.PSD?
Absolutamente! O fórum de suporte da Aspose fornece respostas da equipe de produto e da comunidade: [Aspose support forum](https://forum.aspose.com/c/psd/34).

### Como posso obter uma licença temporária para Aspose.PSD?
Você pode solicitar uma licença temporária diretamente no portal de licenciamento da Aspose, que fornece uma chave limitada no tempo válida por 30 dias. Isso permite avaliar toda a funcionalidade do Aspose.PSD sem comprar uma licença comercial. Após o período de avaliação, substitua a chave temporária por uma licença permanente para continuar usando a biblioteca em produção. Visite a página de licença temporária para gerar uma chave limitada: [temporary license page](https://purchase.aspose.com/temporary-license/).

## Perguntas Frequentes

**Q: Posso usar o objeto graphics para editar apenas uma camada específica?**  
A: Sim. Após carregar o PSD, recupere a camada desejada via `psdImage.getLayers().get_Item(index)` e passe essa camada ao construtor `Graphics`.

**Q: O método de compressão Raw afeta o tamanho do arquivo?**  
A: Raw armazena os dados de pixel sem compressão, portanto o arquivo resultante é maior que um PSD compactado, mas garante fidelidade de 100 % dos pixels.

**Q: É possível exportar o PSD editado para outro formato (por exemplo, PNG)?**  
A: Absolutamente. Após a edição, chame `psdImage.save("output.png", new PngOptions())`—este é o modo padrão de **exportar PSD para PNG** com qualidade sem perdas.

**Q: Qual versão do Java é necessária?**  
A: Aspose.PSD para Java suporta JDK 8 e posteriores, incluindo todas as versões LTS até JDK 21.

**Q: Como liberar recursos após o processamento?**  
A: Invocar `psdImage.dispose()` e fechar quaisquer streams (por exemplo, `ms.close()`) para liberar memória nativa e evitar vazamentos.

---

**Última atualização:** 2026-08-01  
**Testado com:** Aspose.PSD para Java (último lançamento)  
**Autor:** Aspose  

{{< blocks/products/products-backtop-button >}}

## Tutoriais Relacionados

- [Save Images to Stream with Aspose.PSD for Java](/psd/java/advanced-techniques/save-images-to-stream/)
- [Export PSD Layer Group to Image using Java](/psd/java/working-with-psd-files/export-psd-layer-group-to-image/)
- [Create Image using Stream in Aspose.PSD for Java](/psd/java/image-editing/create-image-using-stream/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}