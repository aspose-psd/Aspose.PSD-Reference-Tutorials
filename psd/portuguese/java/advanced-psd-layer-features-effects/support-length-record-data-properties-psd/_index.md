---
date: 2026-02-20
description: Aprenda a suportar propriedades de registro de comprimento e a processar
  em lote arquivos PSD usando Aspose.PSD para Java. Guia passo a passo com exemplos
  de código.
linktitle: Support Length Record Data Properties in PSD - Java
second_title: Aspose.PSD Java API
title: Suporte a Propriedades de Registro de Comprimento – Modificar Formas Vetoriais
  PSD (Java)
url: /pt/java/advanced-psd-layer-features-effects/support-length-record-data-properties-psd/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Suporte a Propriedades de Registro de Comprimento – Modificar Formas Vetoriais PSD (Java)

## Introdução
Se você precisa **modificar formas vetoriais PSD** programaticamente, a biblioteca Aspose.PSD for Java oferece controle total sobre arquivos Photoshop diretamente do seu código Java. Neste tutorial percorreremos tudo o que você precisa saber para **dar suporte a propriedades de registro de comprimento** — uma etapa essencial quando se deseja editar camadas de formas vetoriais. Ao final, você será capaz de abrir um PSD, ajustar suas propriedades de forma vetorial e salvar o arquivo atualizado sem nunca sair do seu IDE. Vamos lá!

## Respostas Rápidas
- **O que significa “modificar formas vetoriais PSD”?** Ajustar a geometria, operações de caminho ou outras propriedades de camadas baseadas em vetor dentro de um arquivo PSD.  
- **Qual biblioteca lida com isso?** Aspose.PSD for Java.  
- **Preciso de licença?** Uma avaliação gratuita funciona para testes; uma licença comercial é necessária para produção.  
- **Quanto tempo leva a implementação?** Cerca de 10‑15 minutos para um script básico de modificação de forma.  
- **Quais são os principais pré‑requisitos?** Java JDK, Aspose.PSD for Java e um arquivo PSD de exemplo.

## O que significa “dar suporte a propriedades de registro de comprimento”?
Dar suporte a propriedades de registro de comprimento significa acessar e atualizar os objetos `LengthRecord` que descrevem cada caminho vetorial dentro de um PSD. Alterar esses registros permite controlar como as formas se combinam, intersectam ou se subtraem umas das outras.

## Por que usar Aspose.PSD for Java para dar suporte a propriedades de registro de comprimento?
- **Sem necessidade do Photoshop** – trabalhe diretamente com arquivos PSD em qualquer servidor.  
- **API rica** – acesse camadas, recursos e dados vetoriais com classes tipadas.  
- **Multiplataforma** – execute em Windows, Linux ou macOS com qualquer JDK.  
- **Foco em desempenho** – gerenciamento de memória eficiente e operações de salvamento rápidas.  

## Pré‑requisitos
1. **Java Development Kit (JDK)** – faça o download em [site da Oracle](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html) ou use seu gerenciador de pacotes preferido.  
2. **Aspose.PSD for Java** – obtenha o JAR mais recente na [página de releases da Aspose](https://releases.aspose.com/psd/java/).  
3. **IDE** – IntelliJ IDEA, Eclipse ou qualquer editor compatível com Java.  
4. **Um arquivo PSD** – crie um no Photoshop ou pegue um PSD de exemplo para experimentar.  
5. **Conhecimento básico de Java** – familiaridade com classes, objetos e tratamento de exceções.

## Importar Pacotes
Primeiro, importe as classes necessárias para trabalhar com arquivos PSD e recursos de formas vetoriais.

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.LayerResource;
import com.aspose.psd.fileformats.psd.layers.layerresources.VsmsResource;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.LengthRecord;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.PathOperations;
```

## Etapa 1: Configurar Diretórios de Origem e Destino
Defina onde o PSD original está localizado e onde o arquivo modificado será salvo.

```java
String sourceDir = "Your Source Directory";
String outputDir = "Your Document Directory";
String inPsdFilePath = sourceDir + "PathOperationsShape.psd";
String outPsdFilePath = outputDir + "out_PathOperationsShape.psd";
```

## Etapa 2: Carregar o Arquivo PSD
Use `Image.load` para abrir o arquivo e faça o cast para `PsdImage` para acessar recursos específicos de PSD.

```java
PsdImage psdImage = (PsdImage) Image.load(inPsdFilePath);
```

## Etapa 3: Localizar o Recurso Vsms na Camada
Os dados de forma vetorial vivem dentro de um `VsmsResource`. Percorra os recursos da segunda camada para encontrá‑lo.

```java
VsmsResource resource = null;
for (LayerResource layerResource : psdImage.getLayers()[1].getResources()) {
    if (layerResource instanceof VsmsResource) {
        resource = (VsmsResource) layerResource;
        break;
    }
}
```

## Etapa 4: Acessar Registros de Comprimento
Cada `LengthRecord` representa um caminho vetorial distinto. Recupere aqueles que você pretende modificar.

```java
LengthRecord lengthRecord0 = (LengthRecord) resource.getPaths()[2];
LengthRecord lengthRecord1 = (LengthRecord) resource.getPaths()[7];
LengthRecord lengthRecord2 = (LengthRecord) resource.getPaths()[11];
```

## Etapa 5: Modificar Propriedades de Operação de Caminho
Agora você pode **modificar formas vetoriais PSD** alterando seus `PathOperations`. Isso determina como as formas interagem (por exemplo, exclusão, interseção, subtração).

```java
lengthRecord0.setPathOperations(PathOperations.ExcludeOverlappingShapes);
lengthRecord1.setPathOperations(PathOperations.IntersectShapeAreas);
lengthRecord2.setPathOperations(PathOperations.SubtractFrontShape);
```

## Etapa 6: Salvar o Arquivo PSD Modificado
Persista suas alterações em um novo arquivo.

```java
psdImage.save(outPsdFilePath);
```

## Etapa 7: Liberar Recursos
Dispose o `PsdImage` para liberar memória.

```java
psdImage.dispose();
```

## Como processar em lote arquivos PSD com suporte a propriedades de registro de comprimento
Se precisar aplicar os mesmos ajustes de forma vetorial a vários PSDs, envolva o código acima em um loop que itere sobre um diretório de arquivos. Atualize `inPsdFilePath` e `outPsdFilePath` a cada iteração, e você poderá **processar arquivos PSD em lote** de forma eficiente.

## Armadilhas Comuns & Dicas
- **Verificações de null** – sempre verifique se `resource` não é `null` antes de acessar caminhos.  
- **Limites de índice de caminho** – assegure‑se de que os índices usados (`[2]`, `[7]`, `[11]`) existam no PSD específico que está sendo editado.  
- **Licença** – executar sem licença válida inserirá uma marca d'água no PSD salvo.  

## Conclusão
Agora você tem um exemplo completo, de ponta a ponta, de como **modificar formas vetoriais PSD** dando suporte a propriedades de registro de comprimento com Aspose.PSD for Java. Seja automatizando pipelines de ativos ou construindo uma ferramenta de design personalizada, essas APIs oferecem a flexibilidade para manipular camadas vetoriais sem trabalho manual no Photoshop. Explore mais experimentando outros `PathOperations` ou combinando múltiplas edições de `LengthRecord` para formas complexas.

## Perguntas Frequentes

**Q: Como lidar com um PSD que não contém camadas de forma vetorial?**  
A: O `VsmsResource` estará ausente, portanto `resource` permanecerá `null`. Adicione uma verificação e pule a etapa de modificação ou informe o usuário.

**Q: Posso alterar outras propriedades como cor de preenchimento ou largura do traço?**  
A: Sim, `LengthRecord` fornece setters adicionais para preenchimento, traço e opacidade. Consulte a documentação da API para detalhes completos.

**Q: É possível processar vários arquivos PSD em lote?**  
A: Absolutamente. Envolva o código dentro de um loop que itere sobre um diretório de arquivos PSD, ajustando os caminhos de entrada e saída a cada execução.

**Q: Preciso fechar streams manualmente ao carregar a partir de um caminho de arquivo?**  
A: O método `Image.load` gerencia streams de arquivo internamente, mas se você carregar a partir de um `InputStream`, lembre‑se de fechá‑lo após o uso.

**Q: Qual versão do Aspose.PSD é necessária para essas APIs?**  
A: As classes `LengthRecord` e `PathOperations` estão disponíveis desde o Aspose.PSD 20.10. Recomenda‑se usar a versão mais recente.

---

**Última atualização:** 2026-02-20  
**Testado com:** Aspose.PSD for Java 24.11  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}