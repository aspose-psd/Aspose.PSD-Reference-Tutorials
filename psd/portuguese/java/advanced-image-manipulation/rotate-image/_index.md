---
date: 2025-12-06
description: Aprenda como girar a imagem 270 graus usando Aspose.PSD para Java. Este
  guia mostra como girar arquivos PSD, virar imagens e converter PSD para JPEG.
language: pt
linktitle: Rotate Image 270 Degrees
second_title: Aspose.PSD Java API
title: Como girar a imagem 270 graus com Aspose.PSD para Java
url: /java/advanced-image-manipulation/rotate-image/
weight: 19
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Rotacionar Imagem 270 Graus com Aspose.PSD para Java

## Introdução

Neste **tutorial de processamento de imagens java**, você descobrirá como **rotacionar imagem 270 graus** de forma rápida e confiável usando Aspose.PSD para Java. Seja você quem está construindo uma ferramenta de edição de fotos, automatizando conversões em lote ou apenas precisa reorientar uma camada PSD, a biblioteca torna a tarefa indolor. Também abordaremos a inversão de imagens e a conversão do PSD rotacionado para JPEG, para que você tenha um fluxo de trabalho completo de ponta a ponta.

## Respostas Rápidas
- **Qual biblioteca realiza a rotação?** Aspose.PSD para Java  
- **Qual ângulo de rotação o exemplo usa?** 270 graus  
- **Posso também inverter a imagem?** Sim – use as opções `RotateFlipType` como `Rotate90FlipX`  
- **Como salvo o resultado?** No exemplo salvamos como JPEG usando `JpegOptions`  
- **Preciso de licença para produção?** Uma licença válida do Aspose.PSD é necessária para uso comercial  

## O que significa “rotacionar imagem 270 graus”?
Rotacionar uma imagem 270 graus significa girar a foto três quartos de uma volta completa no sentido horário (ou 90 graus no sentido anti‑horário). Em muitos cenários de edição gráfica essa orientação corresponde ao layout original de retrato após uma série de transformações.

## Por que usar Aspose.PSD para esta tarefa?
- **Suporte total a PSD** – funciona com camadas, máscaras e objetos de ajuste.  
- **Nenhum Photoshop nativo necessário** – roda em qualquer runtime Java.  
- **API simples** – uma única chamada de método (`rotateFlip`) lida com rotação e inversão.  
- **Conversão fácil de formatos** – exporte diretamente para JPEG, PNG ou outros formatos comuns.

## Pré‑requisitos

Antes de começar, certifique‑se de que você tem:

- Biblioteca **Aspose.PSD para Java** instalada. Você pode baixá‑la e ver a referência completa da API [aqui](https://reference.aspose.com/psd/java/).  
- Um ambiente de desenvolvimento Java (JDK 8 ou superior).  
- Um arquivo PSD de exemplo que você deseja rotacionar. Atualize a variável `sourceFile` no código com o caminho correto para o seu arquivo.

## Importar Pacotes

Comece importando as classes necessárias do pacote Aspose.PSD:

```java
import com.aspose.psd.Image;
import com.aspose.psd.RotateFlipType;

import com.aspose.psd.imageoptions.JpegOptions;
```

## Como Rotacionar PSD – Etapa 1: Carregar a Imagem

Crie uma instância `Image` que aponte para o seu arquivo PSD de origem:

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";
Image image = Image.load(sourceFile);
```

## Como Rotacionar PSD – Etapa 2: Rotacionar a Imagem 270 Graus

Use o método `rotateFlip` com `RotateFlipType.Rotate270FlipNone` para obter uma rotação de 270 graus sem inversão:

```java
image.rotateFlip(RotateFlipType.Rotate270FlipNone);
```

> **Dica profissional:** Se você também precisar inverter a imagem horizontal ou verticalmente, escolha um `RotateFlipType` diferente, como `Rotate90FlipX` ou `Rotate180FlipY`.

## Como Rotacionar PSD – Etapa 3: Converter PSD para JPEG e Salvar

Após rotacionar, você pode **converter PSD para JPEG** (ou qualquer outro formato suportado) usando a classe de opções apropriada:

```java
String destName = dataDir + "RotatedImage_out.jpg";
image.save(destName, new JpegOptions());
```

O arquivo `RotatedImage_out.jpg` agora contém o conteúdo original do PSD rotacionado 270 graus e salvo como JPEG.

## Problemas Comuns e Soluções

| Problema | Solução |
|----------|----------|
| **A imagem aparece de cabeça para baixo** | Verifique se você usou `Rotate270FlipNone`. Para uma rotação de 90 graus no sentido horário use `Rotate90FlipNone`. |
| **Arquivo de saída está corrompido** | Certifique‑se de que a pasta de destino existe e que você tem permissões de escrita. |
| **Exceção de licença** | Instale uma licença temporária ou permanente do Aspose.PSD antes de carregar a imagem em produção. |

## Perguntas Frequentes

**P: O Aspose.PSD é compatível com diferentes formatos de imagem?**  
R: Sim, o Aspose.PSD suporta PSD, JPEG, PNG, BMP, GIF e muitos outros formatos raster.

**P: Posso aplicar rotações personalizadas, não apenas as inversões predefinidas?**  
R: Absolutamente! Embora `RotateFlipType` ofereça ângulos comuns, você pode combinar várias chamadas ou usar matrizes de transformação para ângulos arbitrários.

**P: Como converto o PSD rotacionado para outro formato, como PNG?**  
R: Substitua `JpegOptions` por `PngOptions` (ou a classe de opções correspondente) no método `save`.

**P: Onde posso encontrar suporte ou assistência adicional?**  
R: Para ajuda da comunidade, visite o [Fórum Aspose.PSD](https://forum.aspose.com/c/psd/34).

**P: Existe uma versão de avaliação gratuita?**  
R: Sim, você pode explorar o Aspose.PSD com um [teste gratuito](https://releases.aspose.com/).

**P: Como obtenho uma licença temporária?**  
R: Se precisar de uma licença temporária, você pode obtê‑la [aqui](https://purchase.aspose.com/temporary-license/).

## Conclusão

Agora você aprendeu como **rotacionar imagem 270 graus** usando Aspose.PSD para Java, inverter imagens quando necessário e exportar o resultado para JPEG. Esse fluxo de trabalho simples pode ser integrado a pipelines maiores de processamento de imagens baseados em Java, oferecendo controle total sobre a manipulação de PSD sem depender do Photoshop.

---

**Última atualização:** 2025-12-06  
**Testado com:** Aspose.PSD para Java 24.12  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}