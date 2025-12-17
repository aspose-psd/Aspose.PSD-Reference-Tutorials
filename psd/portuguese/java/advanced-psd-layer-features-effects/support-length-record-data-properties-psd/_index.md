---
date: 2025-12-17
description: Aprenda a modificar formas vetoriais PSD suportando propriedades de dados
  de registro de comprimento usando o Aspose.PSD para Java. Guia passo a passo com
  exemplos de código.
linktitle: Support Length Record Data Properties in PSD - Java
second_title: Aspose.PSD Java API
title: Como modificar formas vetoriais PSD – Suporte a propriedades de dados de registro
  de comprimento em Java
url: /pt/java/advanced-psd-layer-features-effects/support-length-record-data-properties-psd/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Suporte às Propriedades de Dados de Registro de Comprimento em PSD - Java

## Introdução
Se você precisa **modify PSD vector shapes** programaticamente, a biblioteca Aspose.PSD for Java oferece controle total sobre arquivos Photoshop diretamente do seu código Java. Neste tutorial vamos percorrer tudo o que você precisa saber para suportar propriedades de dados de registro de comprimento — uma etapa essencial quando você deseja editar camadas de formas vetoriais. Ao final, você poderá abrir um PSD, ajustar suas propriedades de forma vetorial e salvar o arquivo atualizado sem nunca sair da sua IDE. Vamos mergulhar!

## Respostas Rápidas
- **O que significa “modify PSD vector shapes”?** Ajustar a geometria, operações de caminho ou outras propriedades de camadas baseadas em vetor dentro de um arquivo PSD.  
- **Qual biblioteca lida com isso?** Aspose.PSD for Java.  
- **Preciso de uma licença?** Uma versão de avaliação gratuita funciona para avaliação; uma licença comercial é necessária para produção.  
- **Quanto tempo leva a implementação?** Cerca de 10‑15 minutos para um script básico de modificação de forma.  
- **Quais são os pré-requisitos principais?** Java JDK, Aspose.PSD for Java e um arquivo PSD de exemplo.

## O que é “modify PSD vector shapes”?
Modificar PSD vector shapes envolve alterar os dados subjacentes do caminho vetorial — como registros de comprimento e operações de caminho — de modo que a aparência visual das formas seja atualizada consequentemente. Isso é especialmente útil para pipelines de gráficos automatizados, processamento em lote ou ferramentas de design personalizadas.

## Por que usar Aspose.PSD for Java para modificar PSD vector shapes?
- **Nenhum Photoshop necessário** – trabalhe diretamente com arquivos PSD em qualquer servidor.  
- **API rica** – acesse camadas, recursos e dados vetoriais com classes tipadas.  
- **Multiplataforma** – execute em Windows, Linux ou macOS com qualquer JDK.  
- **Foco em desempenho** – gerenciamento de memória eficiente e operações de salvamento rápidas.

## Pré-requisitos
1. **Java Development Kit (JDK)** – faça o download em [Oracle's website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html) ou use seu gerenciador de pacotes preferido.  
2. **Aspose.PSD for Java** – obtenha o JAR mais recente na [Aspose releases page](https://releases.aspose.com/psd/java/).  
3. **IDE** – IntelliJ IDEA, Eclipse ou qualquer editor compatível com Java.  
4. **Um arquivo PSD** – crie um no Photoshop ou pegue um PSD de exemplo para experimentar.  
5. **Conhecimento básico de Java** – familiaridade com classes, objetos e tratamento de exceções.

## Importar Pacotes
Primeiro, importe as classes que você precisará para trabalhar com arquivos PSD e recursos de formas vetoriais.

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.LayerResource;
import com.aspose.psd.fileformats.psd.layers.layerresources.VsmsResource;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.LengthRecord;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.PathOperations;
```

## Etapa 1: Configure seus Diretórios de Origem e Saída
Defina onde o PSD original está localizado e onde você deseja que o arquivo modificado seja salvo.

```java
String sourceDir = "Your Source Directory";
String outputDir = "Your Document Directory";
String inPsdFilePath = sourceDir + "PathOperationsShape.psd";
String outPsdFilePath = outputDir + "out_PathOperationsShape.psd";
```

## Etapa 2: Carregue o Arquivo PSD
Use `Image.load` para abrir o arquivo e faça o cast para `PsdImage` para recursos específicos de PSD.

```java
PsdImage psdImage = (PsdImage) Image.load(inPsdFilePath);
```

## Etapa 3: Localize o Recurso Vsms na Camada
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

## Etapa 4: Acesse os Registros de Comprimento
Cada `LengthRecord` representa um caminho vetorial distinto. Pegue aqueles que você pretende modificar.

```java
LengthRecord lengthRecord0 = (LengthRecord) resource.getPaths()[2];
LengthRecord lengthRecord1 = (LengthRecord) resource.getPaths()[7];
LengthRecord lengthRecord2 = (LengthRecord) resource.getPaths()[11];
```

## Etapa 5: Modifique as Propriedades de Operação de Caminho
Agora você pode **modify PSD vector shapes** alterando seus `PathOperations`. Isso determina como as formas interagem (por exemplo, exclusão, interseção, subtração).

```java
lengthRecord0.setPathOperations(PathOperations.ExcludeOverlappingShapes);
lengthRecord1.setPathOperations(PathOperations.IntersectShapeAreas);
lengthRecord2.setPathOperations(PathOperations.SubtractFrontShape);
```

## Etapa 6: Salve o Arquivo PSD Modificado
Persista suas alterações em um novo arquivo.

```java
psdImage.save(outPsdFilePath);
```

## Etapa 7: Limpe os Recursos
Dispose do `PsdImage` para liberar memória.

```java
psdImage.dispose();
```

## Armadilhas Comuns & Dicas
- **Verificações de null** – sempre verifique se `resource` não é `null` antes de acessar caminhos.  
- **Limites de índice de caminho** – garanta que os índices que você usa (`[2]`, `[7]`, `[11]`) existam para o PSD específico que está editando.  
- **Licença** – executar sem uma licença válida incorporará uma marca d'água no PSD salvo.

## Conclusão
Você agora tem um exemplo completo, de ponta a ponta, de como **modify PSD vector shapes** suportando propriedades de dados de registro de comprimento com Aspose.PSD for Java. Seja automatizando pipelines de ativos ou construindo uma ferramenta de design personalizada, essas APIs dão a flexibilidade de manipular camadas vetoriais sem trabalho manual no Photoshop. Explore mais experimentando outras `PathOperations` ou combinando múltiplas edições de `LengthRecord` para formas complexas.

## Perguntas Frequentes
### O que é Aspose.PSD for Java?
Aspose.PSD for Java é uma biblioteca que permite aos desenvolvedores manipular e trabalhar com arquivos Photoshop PSD programaticamente usando Java.

### Posso usar Aspose.PSD em um projeto gratuito?
Sim, você pode experimentar a biblioteca gratuitamente usando uma versão de avaliação disponível no site da Aspose.

### Que tipos de modificações posso fazer em arquivos PSD?
Você pode manipular camadas, formas, textos, operações de caminho e muito mais dentro de arquivos PSD.

### O Aspose.PSD é compatível com outras linguagens de programação?
Sim, a Aspose oferece várias bibliotecas para diferentes linguagens de programação, incluindo .NET e Python.

### Onde posso encontrar a documentação do Aspose.PSD?
Você pode acessar a documentação completa [aqui](https://reference.aspose.com/psd/java/).

## Perguntas Frequentes

**Q: Como devo lidar com um PSD que não contém camadas de forma vetorial?**  
A: O `VsmsResource` estará ausente, portanto `resource` permanecerá `null`. Adicione uma verificação e pule a etapa de modificação ou informe o usuário.

**Q: Posso alterar outras propriedades como cor de preenchimento ou largura do traço?**  
A: Sim, `LengthRecord` fornece setters adicionais para preenchimento, traço e opacidade. Consulte a documentação da API para detalhes completos.

**Q: É possível processar vários arquivos PSD em lote?**  
A: Absolutamente. Envolva o código dentro de um loop que itere sobre um diretório de arquivos PSD, ajustando os caminhos de entrada e saída a cada iteração.

**Q: Preciso fechar streams manualmente ao carregar de um caminho de arquivo?**  
A: O método `Image.load` gerencia streams de arquivos internamente, mas se você carregar de um `InputStream`, lembre‑se de fechá‑lo após o uso.

**Q: Qual versão do Aspose.PSD é necessária para essas APIs?**  
A: As classes `LengthRecord` e `PathOperations` estão disponíveis desde o Aspose.PSD 20.10. Recomenda‑se usar a versão mais recente.

---

**Última atualização:** 2025-12-17  
**Testado com:** Aspose.PSD for Java 24.11  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}