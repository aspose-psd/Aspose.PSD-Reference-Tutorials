---
date: 2026-01-09
description: Aprenda como converter PSD para PNG usando a limiarização Bradley no
  Aspose.PSD para Java. Este guia mostra como escolher o limiar ideal e binarizar
  a imagem PSD de forma eficiente.
linktitle: Bradley Thresholding
second_title: Aspose.PSD Java API
title: Converter PSD para PNG com Limiarização Bradley (Aspose.PSD Java)
url: /pt/java/image-processing/bradley-thresholding/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Converter PSD para PNG com Bradley Thresholding (Aspose.PSD Java)

Bem‑vindo a este guia completo sobre **converter PSD para PNG** usando Bradley Thresholding no Aspose.PSD para Java. Nos próximos minutos, você verá por que esta técnica é ideal para criar arquivos PNG binarizados de alto contraste a partir de documentos do Photoshop, e terá um passo a passo prático.

## Respostas Rápidas
- **Posso converter PSD para PNG com Aspose.PSD?** Sim – carregue o PSD, aplique `binarizeBradley` e salve como PNG.  
- **O que significa “escolher limiar ótimo”?** É o valor de sensibilidade (0‑1) que decide como os pixels escuros/claros são classificados.  
- **Preciso de licença para uso em produção?** É necessária uma licença comercial; uma versão de avaliação gratuita funciona para testes.  
- **Quais formatos de imagem são suportados para salvamento?** PNG, JPEG, BMP e muitos outros via as classes `ImageOptions`.  
- **O código é compatível com Java 8 e posteriores?** Absolutamente – a API Aspose.PSD Java suporta Java 8+.

## O que é Bradley Thresholding?
Bradley Thresholding é um algoritmo adaptativo de binarização que calcula uma média local para cada pixel e compara a intensidade do pixel com essa média multiplicada por um limiar definido pelo usuário. O resultado é uma imagem preto‑e‑branco limpa que preserva detalhes importantes.

## Por que Converter PSD para PNG com Bradley Thresholding?
- **Preservar bordas nítidas** – Ideal para OCR, detecção de códigos de barras ou qualquer fluxo de trabalho que precise de separação clara entre primeiro plano e fundo.  
- **Reduzir tamanho do arquivo** – PNG é sem perdas, mas costuma ficar menor após a binarização.  
- **Compatibilidade multiplataforma** – PNG funciona em qualquer lugar, enquanto PSD é específico do Photoshop.  

## Pré‑requisitos
Antes de começar, verifique se você tem:

1. **Ambiente de Desenvolvimento Java** – JDK 8 ou superior instalado.  
2. **Biblioteca Aspose.PSD** – Baixe o JAR mais recente [aqui](https://releases.aspose.com/psd/java/).  
3. **Imagem PSD de Exemplo** – Qualquer arquivo PSD que você queira converter; você também pode usar o exemplo fornecido nos exemplos da Aspose.

## Importar Pacotes
Comece importando as classes necessárias para o seu projeto Java:

```java
import com.aspose.psd.Image;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.PngOptions;
```

## Como Converter PSD para PNG Usando Bradley Thresholding
A seguir está o fluxo completo dividido em etapas numeradas claras. Cada etapa inclui uma breve explicação seguida do código exato que você deve copiar‑colar.

### Etapa 1: Carregar a Imagem PSD
Primeiro, aponte para o seu arquivo de origem e carregue‑o com Aspose.PSD.

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";
String destName = dataDir + "binarized_out.png";

// Load an image
PsdImage image = (PsdImage)Image.load(sourceFile);
```

### Etapa 2: Escolher Limiar Ótimo
O valor do limiar (intervalo 0 – 1) controla a agressividade da binarização. Um ponto de partida típico é **0,15**, mas você pode ajustá‑lo conforme a sua imagem.

```java
// Define threshold value
double threshold = 0.15;
```

### Etapa 3: Binarizar a Imagem PSD
Agora aplique o algoritmo Bradley. Esta etapa **binariza a imagem PSD** com base no limiar selecionado.

```java
// Call BinarizeBradley method and pass the threshold value as a parameter
image.binarizeBradley(threshold);
```

### Etapa 4: Salvar a Saída como PNG
Por fim, grave a imagem processada no disco no formato PNG.

```java
// Save the output image
image.save(destName, new PngOptions());
```

Repita estas etapas para quantos arquivos PSD precisar processar, ajustando o limiar conforme necessário para obter o melhor resultado visual.

## Problemas Comuns & Dicas
- **Limiar muito baixo/alto:** Se a saída parecer muito ruidosa ou desbotada, ajuste o valor `threshold` incrementalmente (ex.: 0,10 – 0,20).  
- **Consumo de memória:** Arquivos PSD grandes podem consumir muita memória. Considere processá‑los um de cada vez ou aumentar o heap da JVM (`-Xmx`).  
- **Pré‑visualização antes de salvar:** Use `image.save("preview.bmp", new BmpOptions());` para inspecionar o resultado binarizado antes da exportação final para PNG.

## Perguntas Frequentes

**Q: Qual a diferença entre `binarizeBradley` e outros métodos de limiarização?**  
A: `binarizeBradley` calcula uma média local para cada pixel, tornando‑a mais robusta para imagens com iluminação desigual em comparação com a limiarização global.

**Q: Posso aplicar Bradley Thresholding a arquivos JPEG ou BMP?**  
A: Sim. Carregue qualquer formato suportado com `Image.load(...)` e, em seguida, chame `binarizeBradley` antes de salvar.

**Q: Existe uma forma de pré‑visualizar a imagem binarizada antes de salvar?**  
A: Absolutamente. Use qualquer das opções de salvamento de imagem do Aspose.PSD (por exemplo, BMP) para gravar um arquivo de pré‑visualização temporário.

**Q: Onde posso encontrar mais suporte e recursos?**  
A: Visite o [fórum Aspose.PSD](https://forum.aspose.com/c/psd/34) para ajuda da comunidade e explore a documentação completa [aqui](https://reference.aspose.com/psd/java/) para cenários avançados.

## Conclusão
Agora você aprendeu como **converter PSD para PNG** de forma eficiente ao **escolher um limiar ótimo** e **binarizar a imagem PSD** com Bradley Thresholding. Essa abordagem é perfeita para fluxos de trabalho que exigem saídas PNG limpas e de alto contraste a partir de arquivos Photoshop complexos.

---

**Última atualização:** 2026-01-09  
**Testado com:** Aspose.PSD Java 23.12 (mais recente na data de escrita)  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}