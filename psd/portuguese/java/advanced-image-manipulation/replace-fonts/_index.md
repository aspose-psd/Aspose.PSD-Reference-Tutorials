---
date: 2026-06-23
description: Aprenda como salvar PSD como PNG, substituir fontes ausentes e exportar
  imagens usando Aspose.PSD para Java – trate rapidamente arquivos PSD com fontes
  ausentes.
keywords:
- save psd as png
- how to replace fonts
- convert psd to bmp
- export psd to jpeg
- handle missing fonts psd
linktitle: Substituir fontes
schemas:
- author: Aspose
  dateModified: '2026-06-23'
  description: Learn how to save PSD as PNG, replace missing fonts, and export images
    using Aspose.PSD for Java – handle missing fonts PSD files quickly.
  headline: How to Save PSD as PNG and Replace Missing Fonts in Java with Aspose
  type: TechArticle
- questions:
  - answer: Yes. While the primary use‑case is PSD, Aspose.PSD also supports PNG,
      JPEG, BMP, and TIFF, allowing font replacement wherever text layers exist.
    question: Can I replace fonts in other image formats besides PSD?
  - answer: No. You can set any TrueType font you prefer, or omit the setting to let
      Aspose use its internal default.
    question: Is the default replacement font mandatory?
  - answer: A commercial license is required for production deployments. See the [purchase
      page](https://purchase.aspose.com/buy) for details.
    question: Are there licensing requirements for using Aspose.PSD?
  - answer: Absolutely. Aspose offers free temporary licenses for evaluation – visit
      the [temporary license page](https://purchase.aspose.com/temporary-license/).
    question: Can I obtain a temporary license for testing?
  - answer: 'The community forum is a great place to ask questions: [Aspose.PSD forum](https://forum.aspose.com/c/psd/34).'
    question: Where can I find additional support or discuss Aspose.PSD‑related issues?
  type: FAQPage
second_title: Aspose.PSD Java API
title: Como salvar PSD como PNG e substituir fontes ausentes em Java com Aspose
url: /pt/java/advanced-image-manipulation/replace-fonts/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# salvar psd como png – Substituir fontes ausentes em Java

## Introdução

Se você precisa **save PSD as PNG** enquanto troca fontes ausentes ou indesejadas dentro de um arquivo Photoshop (PSD), a substituição de fontes Aspose PSD torna isso simples. Em aplicações Java você pode carregar um PSD, informar ao Aspose qual fonte de fallback usar e, em seguida, exportar a imagem corrigida em qualquer formato que desejar. Este tutorial guia você por todo o fluxo de trabalho — da configuração do projeto à exportação do PNG atualizado — para que você possa **handle missing fonts PSD** sem nunca abrir o Photoshop.

## Respostas rápidas
- **Qual biblioteca lida com substituição de fontes?** Aspose.PSD for Java  
- **Quanto tempo leva a implementação?** Cerca de 5‑10 minutos para um cenário básico  
- **Qual fonte é usada como fallback padrão?** Você pode definir qualquer fonte TrueType, por exemplo, “Arial”  
- **Posso salvar em formatos diferentes de PNG?** Sim – PSD, JPEG, BMP e outros são suportados  
- **Preciso de uma licença para produção?** É necessária uma licença válida do Aspose.PSD para uso non‑trial  

## O que é a substituição de fontes Aspose PSD?

A substituição de fontes Aspose PSD é o processo de especificar uma fonte substituta que a biblioteca usará sempre que encontrar uma fonte ausente ou não suportada em um arquivo PSD. Isso garante que as camadas de texto sejam renderizadas corretamente sem edição manual no Photoshop e permite que você **handle missing fonts PSD** arquivos automaticamente.

## Por que usar Aspose.PSD para Java?

Aspose.PSD for Java fornece uma solução abrangente e de alto desempenho para trabalhar com arquivos Photoshop diretamente a partir de código Java, eliminando a necessidade do próprio Photoshop. Ele suporta uma ampla variedade de tipos de camada, efeitos e tamanhos de arquivo grandes, oferecendo APIs simples para tarefas como substituição de fontes, conversão de imagens e manipulação de metadados.

- **Manipulação completa de PSD** – Aspose.PSD suporta **30+ tipos de camada**, **20+ efeitos**, e pode processar arquivos de até **2 GB** sem carregar todo o documento na memória.  
- **Multiplataforma** – funciona em qualquer SO que suporte Java 8+.  
- **Sem dependências externas** – a biblioteca lida com substituição de fontes internamente, portanto você não precisa distribuir fontes adicionais com seu aplicativo.  

## Como substituir fontes ausentes em PSD usando Aspose PSD

Para substituir fontes ausentes, primeiro carregue o PSD com uma fonte de fallback definida nas opções de carregamento, depois renderize ou salve a imagem. A biblioteca substitui automaticamente as fontes ausentes pela fonte que você especificar, garantindo que a saída visual corresponda às suas expectativas sem edição manual.

## Pré-requisitos

- **Java Development Kit (JDK)** – versão 8 ou superior instalada.  
- **Aspose.PSD for Java** – faça o download do JAR mais recente na [release page](https://releases.aspose.com/psd/java/).  
- **An IDE** – IntelliJ IDEA, Eclipse ou qualquer editor de sua preferência.  

## Importar pacotes

A classe `PsdImage` representa um documento Photoshop na memória, fornecendo acesso a camadas, texto e recursos de renderização. `PsdLoadOptions` controla como o arquivo é lido, incluindo a fonte de fallback, enquanto `SaveOptions` (ou subclasses específicas de formato) definem como a imagem é escrita.

```java
import com.aspose.psd.Image;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
import com.aspose.psd.imageoptions.PngOptions;
```

## Etapa 1: Defina o diretório do seu documento

Especifique a pasta que contém o arquivo PSD de origem. Substitua o placeholder pelo caminho real na sua máquina.

O objeto `File` simplesmente aponta para o PSD que você deseja processar; nenhuma configuração adicional é necessária aqui.  

```java
String dataDir = "Your Document Directory";
```

## Etapa 2: Carregue a imagem com uma fonte de substituição

Crie uma instância de `PsdLoadOptions`, defina a fonte de substituição padrão (por exemplo, **Arial**) e carregue o PSD. Aspose aplicará automaticamente o fallback sempre que encontrar uma fonte ausente.

`PsdLoadOptions` permite definir o comportamento de carregamento, incluindo a fonte de fallback que substitui qualquer tipo de letra ausente durante a fase de importação.  

```java
PsdLoadOptions psdLoadOptions = new PsdLoadOptions(); 
psdLoadOptions.setDefaultReplacementFont("Arial");

PsdImage psdImage = (PsdImage)Image.load(dataDir + "Cloud_AzPlat_Banner3A_SB_EN_US_160x600_chinese_font.psd", psdLoadOptions);
```

## Etapa 3: Salve a imagem substituída como PNG

Após a substituição de fontes, você pode exportar a imagem em qualquer formato suportado. Aqui salvamos como PNG, mas também poderia escolher JPEG, BMP ou até mesmo gravar novamente como PSD.

O método `save` de `PsdImage` aceita um objeto `SaveOptions`; usar `PngOptions` garante que a saída seja um PNG sem perdas adequado para web ou processamento posterior.  

```java
PngOptions pngOptions = new PngOptions();
psdImage.save(dataDir + "replaced_font.png", pngOptions);
```

## Como salvar PSD como PNG após substituir fontes?

Carregue o PSD com uma fonte de fallback, então chame `psdImage.save("output.png", new PngOptions())`. Esta operação de salvamento em uma única linha grava um PNG totalmente renderizado que reflete a fonte substituída, permitindo que você incorpore a imagem em qualquer lugar sem se preocupar com fontes ausentes. Certifique‑se de ter aplicado a fonte de substituição antes de salvar e, opcionalmente, ajuste as configurações de compressão PNG via objeto `PngOptions` para obter o tamanho de arquivo ideal.

## Problemas comuns e soluções

| Problema | Causa | Solução |
|----------|-------|---------|
| Texto aparece corrompido após substituição | A fonte de fallback não contém os glifos necessários | Escolha uma fonte que suporte a faixa Unicode necessária (por exemplo, “Arial Unicode MS”). |
| `OutOfMemoryError` em PSDs grandes | Carregando um arquivo de altíssima resolução sem heap suficiente | Aumente o tamanho do heap da JVM (`-Xmx2g`) ou carregue a imagem em modo de streaming, se disponível. |
| Exceção de licença | Uso da versão de avaliação em produção | Aplique uma licença permanente ou temporária válida antes de carregar a imagem. |

## Perguntas frequentes

**Q: Posso substituir fontes em outros formatos de imagem além de PSD?**  
A: Sim. Embora o caso de uso principal seja PSD, o Aspose.PSD também suporta PNG, JPEG, BMP e TIFF, permitindo substituição de fontes onde existam camadas de texto.

**Q: A fonte de substituição padrão é obrigatória?**  
A: Não. Você pode definir qualquer fonte TrueType que preferir, ou omitir a configuração para que o Aspose use seu padrão interno.

**Q: Existem requisitos de licenciamento para usar o Aspose.PSD?**  
A: Uma licença comercial é necessária para implantações em produção. Veja a [purchase page](https://purchase.aspose.com/buy) para detalhes.

**Q: Posso obter uma licença temporária para testes?**  
A: Absolutamente. A Aspose oferece licenças temporárias gratuitas para avaliação – visite a [temporary license page](https://purchase.aspose.com/temporary-license/).

**Q: Onde posso encontrar suporte adicional ou discutir questões relacionadas ao Aspose.PSD?**  
A: O fórum da comunidade é um ótimo lugar para fazer perguntas: [Aspose.PSD forum](https://forum.aspose.com/c/psd/34).

**Q: Como lidar com arquivos PSD que contêm várias fontes ausentes?**  
A: Defina a fonte de substituição padrão uma vez (conforme mostrado) – ela será aplicada a *todas* as fontes ausentes durante a operação de carregamento.

**Q: É possível substituir fontes após a imagem ter sido salva?**  
A: A substituição de fontes deve ocorrer durante a fase de carregamento. Para mudar fontes depois, recarregue o PSD com uma fonte de substituição diferente e salve novamente.

## Conclusão

Você viu agora um fluxo completo de **save psd as png** em Java — desde a importação das classes corretas, configuração de uma fonte de fallback, carregamento do PSD, até a exportação do PNG corrigido. Incorpore esse padrão em seus pipelines de processamento de imagens para garantir tipografia consistente em todos os seus ativos PSD e para **handle missing fonts PSD** automaticamente.

---

**Última atualização:** 2026-06-23  
**Testado com:** Aspose.PSD for Java 24.12 (latest at time of writing)  
**Autor:** Aspose

## Tutoriais relacionados

- [Configurações para substituir fontes ausentes no Aspose.PSD para Java](/psd/java/advanced-techniques/settings-replacing-missing-fonts/)
- [Salvar PSD como PNG e aplicar sombra projetada no Aspose.PSD para Java](/psd/java/advanced-image-manipulation/rendering-drop-shadow/)
- [Como converter PSD para PNG e redimensionar proporcionalmente com Aspose.PSD para Java](/psd/java/advanced-image-manipulation/resize-image-proportionally/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< blocks/products/products-backtop-button >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}