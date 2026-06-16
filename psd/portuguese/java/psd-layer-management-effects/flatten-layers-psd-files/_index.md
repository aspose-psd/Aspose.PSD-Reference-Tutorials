---
date: 2026-04-03
description: Aprenda como reduzir o tamanho de arquivos PSD achatando camadas com
  Aspose.PSD para Java. Este guia passo a passo mostra como achatar arquivos PSD rapidamente.
keywords:
- reduce psd file size
- how to flatten psd
- flatten visible layers psd
linktitle: Reduza o tamanho do arquivo PSD achatando as camadas – Aspose.PSD Java
second_title: Aspose.PSD Java API
title: Reduza o tamanho do arquivo PSD ao achatar as camadas – Aspose.PSD Java
url: /pt/java/psd-layer-management-effects/flatten-layers-psd-files/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Reduzir o tamanho de arquivo PSD ao achatar camadas – Aspose.PSD Java

## Introdução

Se você já abriu um documento do Photoshop e se perguntou como **reduzir o tamanho de arquivo PSD**, achatar camadas é um dos truques mais eficazes. Com o Aspose.PSD para Java você pode achatar programaticamente um PSD inteiro ou mesclar apenas as camadas que escolher, proporcionando controle detalhado sobre o peso do arquivo sem sacrificar a qualidade visual. Neste tutorial percorreremos ambas as abordagens — achatar a imagem inteira e mesclar camadas específicas — para que você possa reduzir rapidamente seus arquivos PSD e manter seu fluxo de trabalho fluido.

## Respostas Rápidas
- **O que o achatar faz?** Ele mescla camadas visíveis em uma única camada de fundo, removendo informações de camada e frequentemente reduzindo o tamanho do arquivo.  
- **Posso achatar apenas camadas selecionadas?** Sim, você pode mesclar camadas específicas enquanto deixa as outras intactas.  
- **Preciso de uma licença?** Um teste gratuito funciona para desenvolvimento; uma licença comercial é necessária para produção.  
- **Qual versão do Java é necessária?** JDK 8 ou superior.  
- **O achatar afetará a qualidade da imagem?** Não, a aparência visual permanece a mesma; apenas a estrutura de camadas muda.

## O que é “reduzir o tamanho de arquivo PSD”?

Reduzir o tamanho de arquivo PSD significa remover dados desnecessários — como camadas extras, canais ocultos ou metadados excessivos — para que o arquivo fique mais leve e rápido de carregar, compartilhar ou processar. Achatar camadas é uma técnica comum porque descarta os objetos de camada separados enquanto preserva a imagem composta final.

## Por que achatar camadas com Aspose.PSD para Java?

- **Automação:** Não é necessário abrir o Photoshop manualmente; integre diretamente em suas aplicações Java.  
- **Precisão:** Escolha achatar todo o documento ou apenas camadas visíveis (`flattenImage`) ou mesclar camadas selecionadas (`mergeLayers`).  
- **Desempenho:** Arquivos menores carregam mais rápido e consomem menos memória nos processos subsequentes.  
- **Multiplataforma:** Funciona em qualquer SO que suporte Java.

## Pré-requisitos

1. **Java Development Kit (JDK):** JDK 8 ou mais recente instalado.  
2. **Aspose.PSD para Java:** Baixe a biblioteca em [here](https://releases.aspose.com/psd/java/).  
3. **IDE:** IntelliJ IDEA, Eclipse ou qualquer IDE compatível com Java.  
4. **Conhecimento básico de Java:** Útil, mas não obrigatório para seguir os passos.  
5. **PSD de exemplo:** Um arquivo com múltiplas camadas (usaremos `ThreeRegularLayersSemiTransparent.psd`).

Agora que temos tudo configurado, vamos mergulhar no código.

## Importar Pacotes

Para começar, importe as classes essenciais do Aspose.PSD:

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.Layer;
```

Essas importações nos permitem carregar arquivos PSD, trabalhar com suas camadas e salvar os resultados.

## Etapa 1: Achatar a Imagem PSD Inteira

Achatar a imagem inteira é a maneira mais rápida de **reduzir o tamanho de arquivo PSD** porque remove todos os dados individuais das camadas.

### 1.1 Carregar o Arquivo PSD

```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "ThreeRegularLayersSemiTransparent.psd";
PsdImage im = (PsdImage) Image.load(sourceFileName);
```

### 1.2 Achatar a Imagem

```java
im.flattenImage();
```

### 1.3 Salvar a Imagem Achata

```java
String exportPath = dataDir + "ThreeRegularLayersSemiTransparentFlattened.psd";
im.save(exportPath);
```

Seu novo arquivo agora contém uma única camada de fundo, o que normalmente resulta em um tamanho de PSD menor.

## Etapa 2: Mesclar Camadas Específicas (Como achatar PSD seletivamente)

Às vezes você só quer **achatar camadas visíveis** ou combinar um subconjunto de camadas mantendo outras editáveis.

### 2.1 Carregar o Arquivo PSD Novamente

```java
PsdImage img = (PsdImage) Image.load(sourceFileName);
```

### 2.2 Identificar e Selecionar Camadas

```java
Layer bottomLayer = img.getLayers()[0];
Layer middleLayer = img.getLayers()[1];
Layer topLayer = img.getLayers()[2];
```

### 2.3 Mesclar as Camadas

```java
Layer layer1 = img.mergeLayers(bottomLayer, middleLayer);
Layer layer2 = img.mergeLayers(layer1, topLayer);
```

### 2.4 Substituir as Camadas Existentes pela Camada Mesclada

```java
img.setLayers(new Layer[]{layer2});
```

### 2.5 Salvar o Arquivo PSD Atualizado

```java
exportPath = dataDir + "ThreeRegularLayersSemiTransparentFlattenedLayerByLayer.psd";
img.save(exportPath);
```

Agora o PSD contém apenas a camada mesclada, alcançando um tamanho de arquivo reduzido enquanto preserva as camadas que você desejava manter.

## Problemas Comuns e Dicas

- **Backup antes de achatar:** Uma vez que as camadas são achatadas, a operação não pode ser desfeita. Mantenha uma cópia do PSD original.  
- **Visibilidade importa:** `flattenImage()` mescla apenas camadas *visíveis*. Oculte quaisquer camadas que não queira incluir.  
- **Uso de memória:** PSDs grandes podem consumir muita RAM; considere processá-los em uma máquina com memória suficiente.  
- **Modos de mesclagem:** A mesclagem respeita o modo de mesclagem de cada camada, portanto o resultado visual corresponde ao que você veria no Photoshop.

## Perguntas Frequentes

**Q: Posso desfazer o achatar de camadas no Aspose.PSD?**  
A: Não, o achatar é irreversível. Sempre mantenha um backup do arquivo original.

**Q: É possível achatar apenas camadas visíveis?**  
A: Sim. `flattenImage()` respeita a visibilidade das camadas, então oculte quaisquer camadas que não queira achatar antes de chamar o método.

**Q: O achatar camadas reduz o tamanho do arquivo?**  
A: Geralmente, sim. Remover dados de camada e metadados costuma levar a um PSD menor, embora a redução exata dependa do conteúdo.

**Q: Posso mesclar camadas com diferentes modos de mesclagem?**  
A: Absolutamente. O Aspose.PSD mescla camadas preservando a aparência visual criada pelos seus modos de mesclagem.

**Q: O que acontece se eu tentar mesclar camadas não adjacentes?**  
A: O Aspose.PSD permite mesclar quaisquer camadas, independentemente da ordem na pilha; o resultado reflete a aparência combinada.

**Última atualização:** 2026-04-03  
**Testado com:** Aspose.PSD 24.11 for Java  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}
{{< blocks/products/products-backtop-button >}}