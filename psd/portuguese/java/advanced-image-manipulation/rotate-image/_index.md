---
date: 2026-02-12
description: Aprenda como girar imagens e como girar imagens em 270 graus usando Aspose.PSD
  para Java. Este guia aborda a rotação de arquivos PSD, a inversão de imagens e a
  conversão de PSD para JPEG sem o Photoshop.
linktitle: Rotate Image 270 Degrees
second_title: Aspose.PSD Java API
title: Como girar a imagem 270 graus com Aspose.PSD para Java
url: /pt/java/advanced-image-manipulation/rotate-image/
weight: 19
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Rotacionar Imagem 270 Graus com Aspose.PSD para Java

## Introdução

Neste **java image processing tutorial**, você descobrirá **how to rotate image** 270 graus de forma rápida e confiável usando Aspose.PSD para Java. Seja construindo uma ferramenta de edição de fotos, automatizando conversões em lote, ou apenas precisando reorientar uma camada PSD, a biblioteca torna a tarefa indolor. Também abordaremos técnicas de **flip image java** e a conversão do PSD rotacionado para JPEG, para que você tenha um fluxo de trabalho completo de ponta a ponta sem Photoshop.

## Respostas Rápidas
- **Qual biblioteca lida com a rotação?** Aspose.PSD for Java  
- **Qual ângulo de rotação o exemplo usa?** 270 graus  
- **Posso também virar a imagem?** Sim – use opções `RotateFlipType` como `Rotate90FlipX`  
- **Como salvo o resultado?** No exemplo salvamos como JPEG usando `JpegOptions`  
- **Preciso de licença para produção?** Uma licença válida do Aspose.PSD é necessária para uso comercial  

## O que é “rotate image 270 degrees”?
Rotacionar uma imagem 270 graus significa girar a foto três quartos de um círculo completo no sentido horário (ou 90 graus no sentido anti‑horário). Em muitos cenários de edição gráfica, essa orientação corresponde ao layout original em retrato após uma série de transformações.

## Por que usar Aspose.PSD para esta tarefa?
- **Suporte completo a PSD** – funciona com camadas, máscaras e objetos de ajuste.  
- **Não requer Photoshop nativo** – execute em qualquer runtime Java.  
- **API simples** – uma única chamada de método (`rotateFlip`) lida com rotação e inversão.  
- **Conversão fácil de formatos** – exporte diretamente para JPEG, PNG ou outros formatos comuns.  

## Como rotacionar imagem com Aspose.PSD para Java
A seguir você encontrará um guia passo a passo que o conduz através do carregamento de um PSD, aplicação de uma rotação de 270°, inversão opcional da imagem e, finalmente, salvamento do resultado como JPEG.

### Pré-requisitos

Antes de começar, certifique‑se de que você tem:

- Biblioteca **Aspose.PSD for Java** instalada. Você pode baixá‑la e visualizar a referência completa da API [aqui](https://reference.aspose.com/psd/java/).  
- Um ambiente de desenvolvimento Java (JDK 8 ou superior).  
- Um arquivo PSD de exemplo que você deseja rotacionar. Atualize a variável `sourceFile` no código com o caminho correto para o seu arquivo.

### Importar Pacotes

Comece importando as classes necessárias do pacote Aspose.PSD:

```java
import com.aspose.psd.Image;
import com.aspose.psd.RotateFlipType;

import com.aspose.psd.imageoptions.JpegOptions;
```

### Etapa 1: Carregar a Imagem

Crie uma instância `Image` que aponta para o seu arquivo PSD de origem:

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";
Image image = Image.load(sourceFile);
```

### Etapa 2: Rotacionar a Imagem 270 Graus

Use o método `rotateFlip` com `RotateFlipType.Rotate270FlipNone` para obter uma rotação de 270 graus sem nenhuma inversão:

```java
image.rotateFlip(RotateFlipType.Rotate270FlipNone);
```

> **Dica profissional:** Se você também precisar inverter a imagem horizontal ou verticalmente, escolha um `RotateFlipType` diferente, como `Rotate90FlipX` ou `Rotate180FlipY`. Esta é a forma mais comum de operações de **flip image java**.

### Etapa 3: Converter PSD para JPEG e Salvar

Após a rotação, você pode **convert PSD to JPEG** (ou qualquer outro formato suportado) usando a classe de opções apropriada:

```java
String destName = dataDir + "RotatedImage_out.jpg";
image.save(destName, new JpegOptions());
```

O arquivo `RotatedImage_out.jpg` agora contém o conteúdo original do PSD rotacionado 270 graus e salvo como JPEG.

## Por que isso importa – Casos de uso reais
- **Processamento em lote de catálogos de produtos** – rotacione dezenas de ativos PSD para uma orientação uniforme antes da publicação.  
- **Geração automática de miniaturas** – crie pré‑visualizações corretamente orientadas para galerias web sem abrir o Photoshop.  
- **Back‑ends de aplicativos móveis** – reoriente arquivos PSD enviados por usuários no lado do servidor usando Java puro.

## Armadilhas comuns e solução de problemas

| Problema | Solução |
|----------|---------|
| **A imagem aparece de cabeça para baixo** | Verifique se você usou `Rotate270FlipNone`. Para uma rotação de 90 graus no sentido horário use `Rotate90FlipNone`. |
| **O arquivo de saída está corrompido** | Certifique‑se de que a pasta de destino existe e que você tem permissões de gravação. |
| **Exceção de licença** | Instale uma licença temporária ou permanente do Aspose.PSD antes de carregar a imagem em produção. |
| **Precisa rotacionar a imagem sem Photoshop** | Esta API realiza a rotação totalmente em código, removendo a dependência do Photoshop. |
| **Deseja inverter a imagem como parte da mesma operação** | Use outros valores `RotateFlipType` como `Rotate90FlipX` (cobre **how to flip image**). |

## Perguntas Frequentes

**Q: O Aspose.PSD é compatível com diferentes formatos de imagem?**  
A: Sim, o Aspose.PSD suporta PSD, JPEG, PNG, BMP, GIF e muitos outros formatos raster.

**Q: Como posso aplicar rotações personalizadas, não apenas inversões predefinidas?**  
A: Absolutamente! Embora `RotateFlipType` forneça ângulos comuns, você pode combinar múltiplas chamadas ou usar matrizes de transformação para ângulos arbitrários.

**Q: Como converto o PSD rotacionado para outro formato, como PNG?**  
A: Substitua `JpegOptions` por `PngOptions` (ou a classe de opções apropriada) no método `save`.

**Q: Onde posso encontrar suporte ou assistência adicional?**  
A: Para ajuda da comunidade, visite o [Aspose.PSD Forum](https://forum.aspose.com/c/psd/34).

**Q: Existe um teste gratuito disponível?**  
A: Sim, você pode explorar o Aspose.PSD com um [free trial](https://releases.aspose.com/).

**Q: Como obtenho uma licença temporária?**  
A: Se precisar de uma licença temporária, você pode obter uma [aqui](https://purchase.aspose.com/temporary-license/).

**Q: Essa abordagem funciona em servidores sem interface gráfica?**  
A: Sim, o Aspose.PSD para Java roda em qualquer ambiente JVM padrão, tornando‑o ideal para pipelines CI/CD ou funções em nuvem.

## Conclusão

Agora você aprendeu **how to rotate image** 270 graus usando Aspose.PSD para Java, como **flip image** quando necessário, e como exportar o resultado para JPEG. Este fluxo de trabalho simples pode ser integrado a pipelines de processamento de imagens baseados em Java maiores, dando a você controle total sobre a manipulação de PSD sem depender do Photoshop.

---

**Última atualização:** 2026-02-12  
**Testado com:** Aspose.PSD for Java 24.12  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}