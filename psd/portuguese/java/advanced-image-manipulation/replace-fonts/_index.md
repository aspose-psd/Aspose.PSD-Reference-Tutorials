---
date: 2026-02-09
description: Aprenda a usar a substituição de fontes do Aspose PSD em Java para lidar
  com arquivos PSD com fontes ausentes, substituir rapidamente fontes ausentes em
  PSD e exportar imagens.
linktitle: Replace Fonts
second_title: Aspose.PSD Java API
title: Substituição de Fonte PSD da Aspose em Java – Substituir Fontes Ausentes
url: /pt/java/advanced-image-manipulation/replace-fonts/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Substituição de Fontes Aspose PSD em Java

## Introdução

Se você precisa trocar fontes ausentes ou indesejadas dentro de um arquivo Photoshop (PSD), **Aspose PSD font substitution** torna isso simples. Em aplicações Java você pode carregar um PSD, informar ao Aspose qual fonte de fallback usar e, em seguida, salvar o resultado em qualquer formato que desejar. Este tutorial guia você por todo o fluxo de **aspose psd font substitution**, desde a configuração do projeto até a exportação da imagem atualizada, para que você possa lidar de forma confiável com cenários de fontes ausentes em PSD sem abrir o Photoshop.

## Respostas Rápidas
- **Qual biblioteca lida com a substituição de fontes?** Aspose.PSD for Java  
- **Quanto tempo leva a implementação?** Cerca de 5‑10 minutos para um cenário básico  
- **Qual fonte é usada como fallback padrão?** Você pode definir qualquer fonte TrueType, por exemplo, “Arial”  
- **Posso salvar em formatos diferentes de PNG?** Sim – PSD, JPEG, BMP, etc., são suportados  
- **Preciso de licença para produção?** Uma licença válida do Aspose.PSD é necessária para uso não‑trial  

## O que é Aspose PSD Font Substitution?

Aspose PSD font substitution é o processo de especificar uma fonte substituta que a biblioteca usará sempre que encontrar uma fonte ausente ou não suportada em um arquivo PSD. Isso garante que as camadas de texto sejam renderizadas corretamente sem edição manual no Photoshop e permite que você **handle missing fonts PSD** arquivos automaticamente.

## Por que usar Aspose.PSD para Java?

- **Manipulação completa de PSD** – camadas, máscaras, efeitos e texto são todos acessíveis via API.  
- **Multiplataforma** – funciona em qualquer SO que suporte Java.  
- **Sem dependências externas** – a biblioteca lida com a substituição de fontes internamente, portanto você não precisa distribuir fontes extras com seu aplicativo.  

## Como substituir fontes ausentes em PSD usando Aspose PSD

A seguir, um guia passo a passo que mostra **how to replace missing fonts PSD** arquivos com uma fonte de fallback personalizada.

## Pré‑requisitos

Antes de começar, certifique‑se de que você tem:

- **Java Development Kit (JDK)** – versão 8 ou superior instalada.  
- **Aspose.PSD for Java** – baixe o JAR mais recente na [release page](https://releases.aspose.com/psd/java/).  
- **Uma IDE** – IntelliJ IDEA, Eclipse ou qualquer editor de sua preferência.  

## Importar Pacotes

Comece importando as classes que você precisará. Isso lhe dá acesso ao carregamento de imagens, opções de carregamento e funcionalidade de salvamento.

```java
import com.aspose.psd.Image;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
import com.aspose.psd.imageoptions.PngOptions;
```

## Etapa 1: Defina o Diretório do Documento

Defina a pasta que contém o arquivo PSD de origem. Substitua o placeholder pelo caminho real na sua máquina.

```java
String dataDir = "Your Document Directory";
```

## Etapa 2: Carregue a Imagem com uma Fonte de Substituição

Crie uma instância de `PsdLoadOptions`, especifique a fonte de substituição padrão (por exemplo, **Arial**) e carregue o PSD. O Aspose aplicará automaticamente o fallback sempre que encontrar uma fonte ausente.

```java
PsdLoadOptions psdLoadOptions = new PsdLoadOptions(); 
psdLoadOptions.setDefaultReplacementFont("Arial");

PsdImage psdImage = (PsdImage)Image.load(dataDir + "Cloud_AzPlat_Banner3A_SB_EN_US_160x600_chinese_font.psd", psdLoadOptions);
```

## Etapa 3: Salve a Imagem Substituída

Após a substituição de fontes, você pode exportar a imagem em qualquer formato suportado. Aqui salvamos como PNG, mas você também pode escolher JPEG, BMP ou até mesmo gravar novamente em PSD.

```java
PngOptions pngOptions = new PngOptions();
psdImage.save(dataDir + "replaced_font.png", pngOptions);
```

## Problemas Comuns e Soluções

| Problema | Causa | Solução |
|----------|-------|---------|
| Texto aparece corrompido após a substituição | A fonte de fallback não contém os glifos necessários | Escolha uma fonte que suporte o intervalo Unicode necessário (ex.: “Arial Unicode MS”). |
| `OutOfMemoryError` em PSDs grandes | Carregamento de um arquivo de alta resolução sem heap suficiente | Aumente o tamanho do heap JVM (`-Xmx2g`) ou carregue a imagem em modo streaming, se disponível. |
| Exceção de licença | Uso da versão trial em produção | Aplique uma licença permanente ou temporária válida antes de carregar a imagem. |

## Perguntas Frequentes

**Q: Posso substituir fontes em outros formatos de imagem além de PSD?**  
A: Sim. Embora o caso de uso principal seja PSD, o Aspose.PSD também suporta PNG, JPEG, BMP e TIFF, permitindo substituição de fontes onde existam camadas de texto.

**Q: A fonte de substituição padrão é obrigatória?**  
A: Não. Você pode definir qualquer fonte TrueType que preferir, ou omitir a configuração para que o Aspose use seu fallback interno.

**Q: Existem requisitos de licenciamento para usar Aspose.PSD?**  
A: Uma licença comercial é necessária para implantações em produção. Consulte a [purchase page](https://purchase.aspose.com/buy) para detalhes.

**Q: Posso obter uma licença temporária para testes?**  
A: Absolutamente. A Aspose oferece licenças temporárias gratuitas para avaliação – visite a [temporary license page](https://purchase.aspose.com/temporary-license/).

**Q: Onde posso encontrar suporte adicional ou discutir questões relacionadas ao Aspose.PSD?**  
A: O fórum da comunidade é um ótimo lugar para fazer perguntas: [Aspose.PSD forum](https://forum.aspose.com/c/psd/34).

**Q: Como lidar com arquivos PSD que contêm várias fontes ausentes?**  
A: Defina a fonte de substituição padrão uma única vez (conforme mostrado) – ela será aplicada a *todas* as fontes ausentes durante a operação de carregamento.

**Q: É possível substituir fontes após a imagem ter sido salva?**  
A: A substituição de fontes deve ocorrer durante a fase de carregamento. Para mudar fontes depois, recarregue o PSD com uma fonte de substituição diferente e salve novamente.

## Conclusão

Agora você viu um fluxo completo de **aspose psd font substitution** em Java — desde a importação das classes corretas, configuração de uma fonte de fallback, carregamento do PSD, até a exportação da imagem corrigida. Incorpore esse padrão em seus pipelines de processamento de imagens para garantir tipografia consistente em todos os seus ativos PSD e para **handle missing fonts PSD** automaticamente.

---

**Last Updated:** 2026-02-09  
**Tested With:** Aspose.PSD for Java 24.12 (latest at time of writing)  
**Author:** Aspose  

---

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
