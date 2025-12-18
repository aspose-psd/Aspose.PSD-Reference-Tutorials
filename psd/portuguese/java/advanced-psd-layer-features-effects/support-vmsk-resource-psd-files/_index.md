---
date: 2025-12-18
description: Aprenda a criar máscara vetorial (recurso Vmsk) em arquivos PSD usando
  Aspose.PSD para Java. Este tutorial passo a passo mostra como adicionar máscara
  vetorial, converter PSD para PNG e muito mais.
linktitle: Create Vector Mask (Vmsk Resource) in PSD Files with Java
second_title: Aspose.PSD Java API
title: Criar Máscara Vetorial (Recurso Vmsk) em Arquivos PSD com Java
url: /pt/java/advanced-psd-layer-features-effects/support-vmsk-resource-psd-files/
weight: 23
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Criar Máscara Vetorial (Recurso Vmsk) em Arquivos PSD com Java

## Introdução
Se você precisa **criar máscara vetorial** (Vmsk) em arquivos Photoshop (PSD), o Aspose.PSD para Java oferece uma maneira limpa e programática de fazê‑lo. Seja construindo uma ferramenta de automação de design ou adicionando suporte a máscaras personalizadas em um pipeline gráfico existente, este tutorial orienta você em cada passo — carregando um PSD, lendo o recurso Vmsk, ajustando suas propriedades e salvando o resultado. Ao final, você estará confortável manipulando máscaras vetoriais, convertendo PSD para PNG e estendendo o arquivo com dados vetoriais adicionais.

## Respostas Rápidas
- **O que é um recurso Vmsk?** É o dado da máscara vetorial armazenado dentro de um arquivo PSD, definindo formas vetoriais complexas para uma camada.  
- **Qual biblioteca o suporta?** Aspose.PSD para Java fornece acesso completo de leitura/escrita aos recursos Vmsk.  
- **Preciso de licença?** Um teste gratuito está disponível; uma licença comercial é necessária para uso em produção.  
- **Posso converter o PSD editado para PNG?** Sim — após salvar, você pode carregar o PSD e exportar para PNG usando a mesma API.  
- **O suporte ao Maven está disponível?** Absolutamente; o Aspose.PSD pode ser adicionado como dependência Maven (veja a palavra‑chave “aspose psd maven”).

## O que é uma Máscara Vetorial (Recurso Vmsk)?
Uma máscara vetorial (Vmsk) é uma máscara não baseada em pixels que usa curvas Bézier e registros de caminho para definir regiões transparentes e opacas em uma camada. Por ser baseada em vetor, ela escala sem perda de qualidade — ideal para gráficos de alta resolução.

## Por que Criar uma Máscara Vetorial com Aspose.PSD?
- **Automação:** Adicione ou modifique máscaras programaticamente sem abrir o Photoshop.  
- **Consistência:** Garanta que todo PSD gerado siga as mesmas regras de máscara.  
- **Multiplataforma:** Funciona em qualquer SO que suporte Java.  
- **Integração:** Combine com outras APIs Aspose (por exemplo, converter PSD → PNG) para fluxos de trabalho de ponta a ponta.

## Pré‑requisitos
Antes de mergulharmos no código, certifique‑se de que você possui o seguinte:

### O Que Você Precisa
- Java Development Kit (JDK): Verifique se o JDK está instalado na sua máquina. Caso não esteja, faça o download no [site da Oracle](https://www.oracle.com/java/technologies/javase-downloads.html).
- Biblioteca Aspose.PSD para Java: Uma biblioteca poderosa para gerenciar arquivos PSD. Você pode baixá‑la na [página de releases da Aspose](https://releases.aspose.com/psd/java/). Para quem deseja experimentar antes de comprar, também há a opção de iniciar com o [teste gratuito](https://releases.aspose.com/).
- Uma IDE: Qualquer IDE para Java (como IntelliJ IDEA, Eclipse, etc.) funcionará neste projeto.

### Configurando Seu Ambiente de Trabalho
1. **Criar um Novo Projeto Java** – Abra sua IDE preferida e inicie um projeto novo.  
2. **Adicionar a Biblioteca Aspose** – Após baixar o JAR da Aspose, adicione‑o ao caminho de compilação do seu projeto para que você possa acessar todas as classes relacionadas a PSD.

Com o ambiente pronto, vamos à implementação prática.

## Como criar máscara vetorial em arquivos PSD com Java
A seguir, um guia passo a passo. Os blocos de código permanecem inalterados em relação ao tutorial original; adicionamos apenas texto explicativo para tornar cada etapa bem clara.

## Importar Pacotes
Antes de trabalharmos com arquivos PSD, precisamos importar as classes necessárias da biblioteca Aspose.PSD.

```java
import com.aspose.psd.Image;
import com.aspose.psd.Point;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.Layer;
import com.aspose.psd.fileformats.psd.layers.LayerResource;
import com.aspose.psd.fileformats.psd.layers.layerresources.VmskResource;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.BezierKnotRecord;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.InitialFillRuleRecord;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.LengthRecord;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.PathFillRuleRecord;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.VectorPathType;
```

Agora que o cenário está preparado, vamos percorrer cada operação.

## Etapa 1: Carregar Seu Arquivo PSD
A primeira coisa a fazer é carregar seu arquivo PSD. É aqui que a mágica começa.

```java
String dataDir = "Your Document Directory"; // Update this path
String sourceFileName = dataDir + "Rectangle.psd";
PsdImage im = (PsdImage) Image.load(sourceFileName);
```

- Definimos `dataDir` para o diretório do seu arquivo PSD.  
- Criamos uma string `sourceFileName`, combinando o diretório com o nome do arquivo PSD.  
- Por fim, carregamos o arquivo PSD em um objeto `PsdImage` usando `Image.load()`.

## Etapa 2: Recuperar o Recurso Vmsk
Com a imagem PSD carregada, vamos buscar o recurso Vmsk.

```java
VmskResource resource = getVmskResource(im);
```

- Chamamos o método `getVmskResource()` que lida com a busca e recuperação do recurso Vmsk da imagem.

## Etapa 3: Validar as Propriedades do Recurso Vmsk
Antes de prosseguir com modificações, é essencial validar que o recurso Vmsk está no estado esperado.

```java
if (resource.isDisabled() != false ||
	resource.isInverted() != false ||
	resource.isNotLinked() != false ||
	resource.getPaths().length != 7) {
	throw new RuntimeException("VmskResource was read wrong");
}
```

- Aqui verificamos várias propriedades do recurso Vmsk. Queremos garantir que ele não esteja desativado, invertido ou desvinculado, e que possua o número correto de caminhos.

## Etapa 4: Acessar Cada Caminho e Validar
Vamos aprofundar um pouco mais e inspecionar os caminhos dentro do recurso Vmsk.

```java
PathFillRuleRecord pathFillRule = (PathFillRuleRecord) resource.getPaths()[0];
InitialFillRuleRecord initialFillRule = (InitialFillRuleRecord) resource.getPaths()[1];
LengthRecord subpathLength = (LengthRecord) resource.getPaths()[2];
if (pathFillRule.getType() != VectorPathType.PathFillRuleRecord ||
	initialFillRule.getType() != VectorPathType.InitialFillRuleRecord ||
	initialFillRule.isFillStartsWithAllPixels() != false ||
	subpathLength.getType() != VectorPathType.ClosedSubpathLengthRecord ||
	subpathLength.isClosed() != true) {
	throw new RuntimeException("VmskResource paths were read wrong");
}
```

- Extraímos três registros de caminho específicos e validamos seus tipos e propriedades para garantir que atendam aos nossos critérios.

## Etapa 5: Editar o Recurso Vmsk
Agora entramos na parte de modificação! Você pode ajustar as propriedades do recurso Vmsk conforme necessário.

```java
resource.setDisabled(true);
resource.setInverted(true);
resource.setNotLinked(true);
```

- Neste bloco, alternamos várias propriedades do recurso Vmsk. Definindo‑as como `true`, controlamos como a máscara se comporta no arquivo PSD.

## Etapa 6: Modificar os Pontos dos Nós Bézier
Os nós Bézier são críticos para caminhos vetoriais. Vamos alterar alguns valores aqui.

```java
BezierKnotRecord bezierKnot = (BezierKnotRecord) resource.getPaths()[3];
bezierKnot.getPoints()[0] = new Point(0, 0);
bezierKnot = (BezierKnotRecord) resource.getPaths()[4];
bezierKnot.getPoints()[0] = new Point(8039797, 10905190);
```

- Acessamos caminhos específicos `BezierKnotRecord` e alteramos seus pontos para possivelmente remodelar a máscara vetorial.

## Etapa 7: Salvar o Arquivo PSD Modificado
Com todas as edições concluídas, é hora de salvar o arquivo PSD modificado.

```java
String exportPath = dataDir + "Rectangle_changed.psd";
im.save(exportPath);
```

- Definimos o caminho para o PSD exportado e então chamamos `im.save()` para gravar as alterações neste novo arquivo.

## Etapa 8: Liberar Recursos
Por fim, precisamos garantir que o objeto de imagem seja descartado corretamente para liberar recursos.

```java
im.dispose();
```

- É sempre uma boa prática descartar quaisquer recursos quando terminar. Isso ajuda a evitar vazamentos de memória em suas aplicações.

## Conclusão
Parabéns! Você acabou de percorrer um processo detalhado de **criação de máscara vetorial** (Vmsk) em arquivos PSD usando Aspose.PSD para Java. Desde o carregamento da imagem, recuperação e validação do recurso Vmsk, edição de suas propriedades, até a gravação do PSD modificado, você agora tem uma base sólida para automatizar fluxos de trabalho com máscaras vetoriais. Use essas técnicas para enriquecer seus pipelines de design, integrar com outras APIs Aspose (como converter PSD para PNG) ou construir ferramentas gráficas personalizadas.

## Perguntas Frequentes
### O que é um recurso Vmsk?
Um recurso Vmsk é uma máscara vetorial em um arquivo PSD que permite formas vetoriais complexas e recursos de edição.

### Posso usar Aspose.PSD em um projeto Maven?
Sim, você pode incluir o Aspose.PSD como dependência no seu projeto Maven usando suas coordenadas do repositório.

### Em que formato posso salvar meus arquivos PSD modificados?
Você pode salvá‑los novamente como arquivos PSD ou exportá‑los para outros formatos como PNG, JPEG, etc.

### Existe um teste gratuito disponível para Aspose.PSD?
Sim, você pode acessar um teste gratuito do Aspose.PSD para testar seus recursos. Visite o [link de teste gratuito](https://releases.aspose.com/).

### Como posso obter suporte para Aspose.PSD?
Você pode participar do [fórum da Aspose](https://forum.aspose.com/c/psd/34) para obter suporte e ajuda na solução de problemas.

## Perguntas Frequentes Adicionais
**Q: Como adiciono uma nova máscara vetorial a uma camada existente?**  
A: Crie um `VmskResource`, preencha‑o com os registros de caminho necessários (por exemplo, `BezierKnotRecord`) e anexe‑o à coleção de recursos da camada.

**Q: Posso converter o PSD editado diretamente para PNG sem abrir o Photoshop?**  
A: Sim — após salvar o PSD, carregue‑o novamente com `Image.load()` e chame `im.save("output.png")` especificando o formato PNG.

**Q: Existe uma forma de automatizar isso em um pipeline CI/CD?**  
A: Absolutamente. Como o processo é puro Java, você pode incorporá‑lo em builds Maven/Gradle, contêineres Docker ou qualquer sistema CI que suporte Java.

**Q: Quais versões do Aspose.PSD são compatíveis com Java 11+?**  
A: Todas as versões recentes (2024‑2025) suportam Java 8 e superiores, incluindo Java 11, 17 e outras versões LTS mais recentes.

**Q: Preciso de licença para builds de desenvolvimento?**  
A: Uma licença de avaliação gratuita funciona para desenvolvimento e testes. Para implantações em produção, é necessária uma licença comercial.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Última atualização:** 2025-12-18  
**Testado com:** Aspose.PSD 24.11 for Java  
**Autor:** Aspose  

---