---
date: 2025-12-21
description: Aprenda a realizar o processamento de imagens em Java ajustando o gamma
  da imagem com Aspose.PSD. Guia passo a passo para converter PSD em TIFF e aplicar
  correção de gamma.
linktitle: Adjust Gamma of an Image
second_title: Aspose.PSD Java API
title: Processamento de Imagem em Java – Ajustar Gama com Aspose.PSD
url: /pt/java/advanced-techniques/adjust-gamma/
weight: 23
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Processamento de Imagem Java – Ajustar Gamma com Aspose.PSD

## Introdução

Se você está trabalhando com **java image processing**, ajustar o gamma de uma imagem é uma técnica fundamental para melhorar o brilho e o contraste sem perder detalhes. Neste tutorial, vamos mostrar como usar **Aspose.PSD for Java** para aplicar correção de gamma a um arquivo PSD e, em seguida, exportar o resultado como uma imagem TIFF. Você verá por que essa abordagem é rápida, confiável e perfeita para pipelines de imagem do lado do servidor.

## Respostas Rápidas
- **O que a correção de gamma faz?** Ela remapeia os valores de luminância para tornar as áreas escuras mais claras ou as áreas claras mais escuras, preservando o detalhe geral.  
- **Qual biblioteca lida com o processamento?** Aspose.PSD for Java fornece um método dedicado `adjustGamma` para imagens raster.  
- **Posso converter PSD para TIFF no mesmo fluxo?** Sim – após o ajuste de gamma, você pode salvar a imagem diretamente em TIFF usando `TiffOptions`.  
- **Preciso de uma licença para desenvolvimento?** Um teste gratuito funciona para testes; uma licença comercial é necessária para uso em produção.  
- **Qual versão do Java é suportada?** Aspose.PSD suporta Java 8 e posteriores.

## O que é processamento de imagem java?

Processamento de imagem Java refere-se à manipulação, análise e transformação de dados visuais usando bibliotecas Java. As tarefas incluem redimensionamento, filtragem, correção de cor e conversão de formato — tudo isso pode ser automatizado em aplicativos desktop ou web.

## Por que usar Aspose.PSD para correção de gamma?

Aspose.PSD oferece uma API de alto nível que abstrai a complexidade do formato PSD, permitindo que você se concentre nos ajustes reais da imagem. Ela lida com cache, perfis de cor e fornece uma chamada direta `adjustGamma`, tornando-a ideal para **image gamma correction** e **convert psd to tiff** workflows.

## Pré-requisitos

Antes de mergulhar no tutorial, certifique‑se de que você tem os seguintes pré-requisitos configurados:

1. **Java Development Environment** – Certifique‑se de que você tem um ambiente de desenvolvimento Java instalado no seu sistema.  
2. **Aspose.PSD Library** – Baixe e integre a biblioteca Aspose.PSD ao seu projeto Java. Você pode encontrar os recursos necessários na [documentation](https://reference.aspose.com/psd/java/).  
3. **Sample Image** – Prepare uma imagem PSD de exemplo que você usará para aplicar o ajuste de gamma.

## Importar Pacotes

Para iniciar o processo, importe os pacotes necessários no seu projeto Java. Isso prepara o terreno para utilizar as funcionalidades do Aspose.PSD sem problemas.

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.psd.fileformats.tiff.enums.TiffPhotometrics;
import com.aspose.psd.imageoptions.TiffOptions;
```

## Etapa 1: Carregar a Imagem

Comece carregando a imagem PSD de exemplo em uma instância da classe `RasterImage`. Esta é a base para os ajustes de gamma subsequentes.

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

// Load an existing image into an instance of RasterImage class
Image image = Image.load(sourceFile);

// Cast object of Image to RasterImage
RasterImage rasterImage = (RasterImage)image;

// Check if RasterImage is cached for better performance
if (!rasterImage.isCached()) {
    rasterImage.cacheData();
}
```

## Etapa 2: Ajustar Gamma

Agora, ajuste o gamma da imagem carregada usando o método `adjustGamma`. Ajuste finamente os valores de gamma de acordo com seus requisitos.

```java
// Adjust the gamma
rasterImage.adjustGamma(2.2f, 2.2f, 2.2f);
```

## Etapa 3: Criar TiffOptions

Crie uma instância de `TiffOptions` para a imagem resultante. Defina várias propriedades, como bits por amostra e opções fotométricas, para adaptar a saída às suas especificações.

```java
// Create an instance of TiffOptions for the resultant image
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
int[] ushort = { 8, 8, 8 };
tiffOptions.setBitsPerSample(ushort);
tiffOptions.setPhotometric(TiffPhotometrics.Rgb);
```

## Etapa 4: Salvar a Imagem Resultante

Salve a imagem manipulada no formato TIFF usando o `TiffOptions` definido anteriormente.

```java
// Save the resultant image to TIFF format
String destName = dataDir + "AdjustGamma_out.tiff";
rasterImage.save(destName, tiffOptions);
```

## Problemas Comuns e Soluções

| Problema | Por que acontece | Como Corrigir |
|----------|------------------|---------------|
| **A imagem parece desbotada** | Valor de gamma muito alto (por exemplo, > 2.5) | Reduza o fator de gamma para um valor entre 1.8 e 2.2. |
| **`rasterImage.isCached()` returns false** | Imagem ainda não carregada na memória | Chame `rasterImage.cacheData()` antes de ajustar o gamma. |
| **O tamanho do arquivo TIFF é grande** | Bits por amostra configurados para 16‑bits | Use uma amostra de 8‑bits (`{8,8,8}`) como mostrado no exemplo. |

## Perguntas Frequentes

**Q: Posso aplicar valores de gamma diferentes a cada canal de cor?**  
A: Sim – o método `adjustGamma` aceita valores float separados para os canais vermelho, verde e azul.

**Q: É possível encadear múltiplos ajustes de imagem antes de salvar?**  
A: Absolutamente. Você pode realizar redimensionamento, recorte ou correções de cor sequencialmente na mesma instância `RasterImage`.

**Q: O Aspose.PSD suporta arquivos PSD de múltiplas páginas?**  
A: Sim, cada camada pode ser acessada e processada individualmente.

**Q: Para qual formato posso exportar além de TIFF?**  
A: Aspose.PSD suporta PNG, JPEG, BMP e muitos outros formatos através de suas respectivas classes de opções.

## Conclusão

Parabéns! Você realizou com sucesso **java image processing** ajustando o gamma de um arquivo PSD e exportando‑o como uma imagem TIFF usando Aspose.PSD for Java. Esse fluxo de trabalho oferece controle detalhado sobre o brilho e o contraste da imagem, tornando‑o ideal para pipelines de gráficos automatizados, serviços web ou utilitários de desktop.

---

**Última atualização:** 2025-12-21  
**Testado com:** Aspose.PSD 24.11 for Java  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

## Perguntas Frequentes

### Q1: Onde posso encontrar a documentação do Aspose.PSD?

A1: Você pode acessar a documentação em [https://reference.aspose.com/psd/java/](https://reference.aspose.com/psd/java/).

### Q2: Como faço o download do Aspose.PSD para Java?

A2: Baixe a biblioteca em [https://releases.aspose.com/psd/java/](https://releases.aspose.com/psd/java/).

### Q3: Onde posso comprar o Aspose.PSD?

A3: Visite [https://purchase.aspose.com/buy](https://purchase.aspose.com/buy) para comprar o Aspose.PSD.

### Q4: Existe uma versão de teste gratuita disponível?

A4: Sim, você pode experimentar uma versão de teste gratuita em [https://releases.aspose.com/](https://releases.aspose.com/).

### Q5: Onde posso obter suporte para o Aspose.PSD?

A5: Para suporte, visite o fórum Aspose.PSD em [https://forum.aspose.com/c/psd/34](https://forum.aspose.com/c/psd/34).