---
date: 2026-09-23
description: Aprenda como modificar formas vetoriais PSD e processar em lote arquivos
  PSD usando Aspose.PSD for Java. Etapas detalhadas, dicas e marcadores de código
  para uma solução completa.
keywords:
- modify psd vector shapes
- batch process psd files
- Aspose.PSD Java
- vector shape editing
lastmod: 2026-09-23
linktitle: Suporte a Propriedades de Dados de Registro de Comprimento em PSD - Java
og_description: Aprenda como modificar formas vetoriais PSD e processar em lote arquivos
  PSD usando Aspose.PSD for Java. Guia passo a passo com marcadores de código e dicas
  de especialistas.
og_image_alt: Guide showing how to edit vector shapes in PSD files using Aspose.PSD
  for Java
og_title: Modificar formas vetoriais PSD com Aspose.PSD for Java
schemas:
- author: Aspose
  dateModified: '2026-09-23'
  description: Learn how to modify PSD vector shapes and batch process PSD files using
    Aspose.PSD for Java. Detailed steps, tips, and code placeholders for a complete
    solution.
  headline: Modify PSD vector shapes with Aspose.PSD for Java
  type: TechArticle
- description: Learn how to modify PSD vector shapes and batch process PSD files using
    Aspose.PSD for Java. Detailed steps, tips, and code placeholders for a complete
    solution.
  name: Modify PSD vector shapes with Aspose.PSD for Java
  steps:
  - name: '**Java Development Kit (JDK)** – download from [Oracle''s website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html)
      or use your preferred package manager.'
    text: '**Java Development Kit (JDK)** – download from [Oracle''s website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html)
      or use your preferred package manager.'
  - name: '**Aspose.PSD for Java** – obtain the latest JAR from the [Aspose releases
      page](https://releases.aspose.com/psd/java/).'
    text: '**Aspose.PSD for Java** – obtain the latest JAR from the [Aspose releases
      page](https://releases.aspose.com/psd/java/).'
  - name: '**IDE** – IntelliJ IDEA, Eclipse, or any Java‑compatible editor.'
    text: '**IDE** – IntelliJ IDEA, Eclipse, or any Java‑compatible editor.'
  - name: '**A PSD file** – create one in Photoshop or grab a sample PSD to experiment
      with.'
    text: '**A PSD file** – create one in Photoshop or grab a sample PSD to experiment
      with.'
  - name: '**Basic Java knowledge** – familiarity with classes, objects, and exception
      handling.'
    text: '**Basic Java knowledge** – familiarity with classes, objects, and exception
      handling.'
  type: HowTo
- questions:
  - answer: The `VsmsResource` will be absent, so `resource` stays `null`. Add a check
      and skip the modification step or inform the user.
    question: How do I handle a PSD that contains no vector shape layers?
  - answer: Yes, `LengthRecord` provides setters for fill, stroke, and opacity. See
      the API docs for the full list.
    question: Can I change other properties like fill color or stroke width?
  - answer: Absolutely. Wrap the code inside a loop that iterates over a directory
      of PSD files, adjusting the input and output paths each time.
    question: Is it possible to batch‑process multiple PSD files?
  - answer: '`Image.load` handles file streams automatically, but if you load from
      an `InputStream`, remember to close it after use.'
    question: Do I need to close streams manually when loading from a file path?
  - answer: The `LengthRecord` and `PathOperations` classes have been available since
      Aspose.PSD 20.10. Using the latest version (24.11 at time of writing) is recommended.
    question: What version of Aspose.PSD is required for these APIs?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- modify psd vector shapes
- Aspose.PSD
- Java image processing
- batch PSD processing
title: Modificar formas vetoriais PSD com Aspose.PSD for Java
url: /pt/java/advanced-psd-layer-features-effects/support-length-record-data-properties-psd/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Modificar formas vetoriais PSD com Aspose.PSD para Java

## Introdução
Se você precisar **modificar formas vetoriais PSD** programaticamente, o Aspose.PSD para Java oferece controle total sobre arquivos Photoshop diretamente do seu código Java. Este tutorial orienta você sobre como dar suporte às propriedades de registro de comprimento — uma etapa essencial ao editar camadas de formas vetoriais. Ao final, você será capaz de abrir um PSD, ajustar seus dados de forma vetorial e salvar o arquivo atualizado sem nunca abrir o Photoshop.

## Respostas rápidas
- **O que significa “modify PSD vector shapes”?** Ajustar geometria, operações de caminho ou outros atributos de camadas baseadas em vetor dentro de um arquivo PSD.  
- **Qual biblioteca lida com isso?** Aspose.PSD para Java.  
- **Preciso de uma licença?** Um teste gratuito funciona para avaliação; uma licença comercial é necessária para produção.  
- **Quanto tempo leva a implementação?** Cerca de 10‑15 minutos para um script básico de modificação de forma.  
- **Quais são os pré-requisitos principais?** Java JDK, Aspose.PSD para Java e um arquivo PSD de exemplo.

## O que é “support length record properties”?
Dar suporte a propriedades de registro de comprimento significa acessar e atualizar os objetos `LengthRecord` que descrevem cada caminho vetorial dentro de um PSD. Esses registros armazenam informações como o comprimento do caminho, tipo e como ele se une a outros caminhos. Alterá‑los permite controlar como as formas se combinam, intersectam ou se subtraem, possibilitando edição vetorial precisa.

## Por que usar Aspose.PSD para Java para dar suporte a propriedades de registro de comprimento?
Carregue seu PSD, edite os dados vetoriais e salve — tudo sem Photoshop. O Aspose.PSD processa PSDs com centenas de páginas em menos de 2 segundos em um servidor típico, oferece mais de 150 classes (incluindo mais de 30 tipos relacionados a vetores) e funciona no Windows, Linux ou macOS com qualquer JDK 11+. Essa biblioteca focada em desempenho elimina a necessidade de softwares desktop caros.

## Pré-requisitos
1. **Java Development Kit (JDK)** – faça o download em [Oracle's website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html) ou use seu gerenciador de pacotes preferido.  
2. **Aspose.PSD para Java** – obtenha o JAR mais recente na [Aspose releases page](https://releases.aspose.com/psd/java/).  
3. **IDE** – IntelliJ IDEA, Eclipse ou qualquer editor compatível com Java.  
4. **Um arquivo PSD** – crie um no Photoshop ou pegue um PSD de exemplo para experimentar.  
5. **Conhecimento básico de Java** – familiaridade com classes, objetos e tratamento de exceções.

## Importar pacotes
As instruções de importação trazem as classes principais do Aspose.PSD para o escopo, como `PsdImage`, `VsmsResource` e `LengthRecord`.

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.LayerResource;
import com.aspose.psd.fileformats.psd.layers.layerresources.VsmsResource;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.LengthRecord;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.PathOperations;
```

## Etapa 1: Defina seus diretórios de origem e saída
Defina onde o PSD original está localizado e onde o arquivo modificado será gravado.

```java
String sourceDir = "Your Source Directory";
String outputDir = "Your Document Directory";
String inPsdFilePath = sourceDir + "PathOperationsShape.psd";
String outPsdFilePath = outputDir + "out_PathOperationsShape.psd";
```

## Etapa 2: Carregar o arquivo PSD
Use `Image.load` para abrir o arquivo e faça o cast para `PsdImage` para recursos específicos de PSD.

```java
PsdImage psdImage = (PsdImage) Image.load(inPsdFilePath);
```

## Etapa 3: Localizar o recurso Vsms na camada
`VsmsResource` é o contêiner que armazena os dados de forma vetorial de uma camada. Percorra os recursos da segunda camada para encontrá‑lo.

```java
VsmsResource resource = null;
for (LayerResource layerResource : psdImage.getLayers()[1].getResources()) {
    if (layerResource instanceof VsmsResource) {
        resource = (VsmsResource) layerResource;
        break;
    }
}
```

## Etapa 4: Acessar registros de comprimento
`LengthRecord` representa um caminho vetorial distinto. Recupere os registros que você pretende modificar.

```java
LengthRecord lengthRecord0 = (LengthRecord) resource.getPaths()[2];
LengthRecord lengthRecord1 = (LengthRecord) resource.getPaths()[7];
LengthRecord lengthRecord2 = (LengthRecord) resource.getPaths()[11];
```

## Etapa 5: Modificar propriedades de operação de caminho
`PathOperations` define como as formas individuais interagem (por exemplo, exclusão, interseção, subtração). Alterar esses valores atualiza a composição visual da camada vetorial.

```java
lengthRecord0.setPathOperations(PathOperations.ExcludeOverlappingShapes);
lengthRecord1.setPathOperations(PathOperations.IntersectShapeAreas);
lengthRecord2.setPathOperations(PathOperations.SubtractFrontShape);
```

## Etapa 6: Salvar o arquivo PSD modificado
Persista suas alterações em um novo arquivo.

```java
psdImage.save(outPsdFilePath);
```

## Etapa 7: Limpar recursos
Dispose da instância `PsdImage` para liberar memória e evitar vazamentos de recursos.

```java
psdImage.dispose();
```

## Como processar em lote arquivos PSD com suporte a propriedades de registro de comprimento
Envolva o fluxo de trabalho de um único arquivo em um loop que itere sobre um diretório de PSDs, atualizando `inPsdFilePath` e `outPsdFilePath` para cada arquivo. Essa abordagem permite aplicar ajustes idênticos de forma vetorial a dezenas ou centenas de arquivos em minutos, ideal para pipelines automatizados de ativos.

## Armadilhas comuns e dicas
- **Verificações de null** – sempre verifique se `resource` não é `null` antes de acessar seus membros.  
- **Limites de índice de caminho** – assegure‑se de que os índices que você usa (por exemplo, `[2]`, `[7]`, `[11]`) existam para o PSD específico que está editando.  
- **Licença** – executar sem uma licença válida insere uma marca d'água no PSD salvo.  

## Conclusão
Agora você tem um exemplo completo, de ponta a ponta, de como **modificar formas vetoriais PSD** dando suporte a propriedades de registro de comprimento com Aspose.PSD para Java. Seja automatizando um pipeline de ativos ou construindo uma ferramenta de design personalizada, essas APIs oferecem a flexibilidade para manipular camadas vetoriais sem trabalho manual no Photoshop. Experimente outros valores de `PathOperations` ou combine várias edições de `LengthRecord` para criar formas complexas.

## Perguntas frequentes

**Q: Como lidar com um PSD que não contém camadas de forma vetorial?**  
A: O `VsmsResource` estará ausente, portanto `resource` permanecerá `null`. Adicione uma verificação e pule a etapa de modificação ou informe o usuário.

**Q: Posso alterar outras propriedades como cor de preenchimento ou largura do traço?**  
A: Sim, `LengthRecord` fornece setters para preenchimento, traço e opacidade. Consulte a documentação da API para a lista completa.

**Q: É possível processar em lote vários arquivos PSD?**  
A: Absolutamente. Envolva o código dentro de um loop que itere sobre um diretório de arquivos PSD, ajustando os caminhos de entrada e saída a cada iteração.

**Q: Preciso fechar streams manualmente ao carregar de um caminho de arquivo?**  
A: `Image.load` lida com streams de arquivos automaticamente, mas se você carregar de um `InputStream`, lembre‑se de fechá‑lo após o uso.

**Q: Qual versão do Aspose.PSD é necessária para essas APIs?**  
A: As classes `LengthRecord` e `PathOperations` estão disponíveis desde o Aspose.PSD 20.10. Recomenda‑se usar a versão mais recente (24.11 na data de escrita).

---

**Última atualização:** 2026-09-23  
**Testado com:** Aspose.PSD para Java 24.11  
**Autor:** Aspose

## Tutoriais relacionados

- [Converter PSD para PNG e criar máscara vetorial Java – Recurso Vmsk em arquivos PSD](/psd/java/advanced-psd-layer-features-effects/support-vmsk-resource-psd-files/)
- [Converter PSD para PNG com suporte a máscara de camada usando Aspose.PSD para Java](/psd/java/advanced-psd-layer-features-effects/support-layer-mask-psd-files/)
- [Adicionar suporte a camada em arquivos PSD](/psd/java/advanced-psd-layer-features-effects/add-layer-support-psd-files/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}