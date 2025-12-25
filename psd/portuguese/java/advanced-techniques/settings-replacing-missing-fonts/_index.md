---
date: 2025-12-25
description: Aprenda a substituir fontes em arquivos PSD com Aspose.PSD para Java
  – um guia passo a passo que também mostra como salvar PSD como PNG e lidar com fontes
  ausentes.
linktitle: Settings for Replacing Missing Fonts
second_title: Aspose.PSD Java API
title: Como substituir fontes no Aspose.PSD para Java
url: /pt/java/advanced-techniques/settings-replacing-missing-fonts/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Como Substituir Fontes no Aspose.PSD para Java

## Introdução

Se você está trabalhando com arquivos Photoshop (PSD) em uma aplicação Java, fontes ausentes podem quebrar o layout visual e causar erros de renderização. **Como substituir fontes** de forma rápida e confiável é essencial para manter a fidelidade do design. Neste tutorial você aprenderá a usar o Aspose.PSD para Java para substituir fontes ausentes, converter o resultado para PNG e manter seu fluxo de conversão de imagens fluido. Ao final, você será capaz de substituir fontes em imagens, salvar PSD como PNG e evitar armadilhas comuns que os desenvolvedores encontram.

## Respostas Rápidas
- **O que significa “substituir fontes” no processamento de PSD?** Substitui tipografias ausentes ou indisponíveis por uma fonte de fallback que você especifica.  
- **Qual biblioteca lida com isso automaticamente?** Aspose.PSD para Java fornece `PsdLoadOptions.setDefaultReplacementFont`.  
- **Posso também converter o PSD para PNG após a substituição?** Sim – use `PngOptions` e chame `psdImage.save`.  
- **Preciso de licença para uso em produção?** Uma licença válida do Aspose.PSD é necessária para builds não‑avaliativos.  
- **Qual versão do Java é suportada?** Qualquer runtime Java 8+ funciona com a versão atual do Aspose.PSD.

## O que é Substituição de Fonte em Arquivos PSD?

Quando um PSD referencia uma fonte que não está instalada na máquina host, o motor de renderização recorre a uma fonte genérica, frequentemente resultando em texto desalinhado. A substituição de fonte permite definir uma fonte padrão (ex.: Arial) que a biblioteca usará sempre que encontrar uma tipografia ausente, garantindo saída visual consistente.

## Por que Substituir Fontes Ausentes com Aspose.PSD?

- **Solução sem dependências** – Não é necessário Photoshop nativo ou ferramentas externas.  
- **Pronta para lote** – Processa dezenas de arquivos em um loop com as mesmas configurações.  
- **Pronta para conversão de imagem** – Após a substituição você pode **salvar PSD como PNG** ou **converter PSD para PNG** sem etapas adicionais.  
- **Multiplataforma** – Funciona em runtimes Java Windows, Linux e macOS.

## Pré‑requisitos

1. **Biblioteca Aspose.PSD** – Baixe e instale a biblioteca Aspose.PSD para Java a partir da [página de releases](https://releases.aspose.com/psd/java/).  
2. **Ambiente de Desenvolvimento Java** – JDK 8 ou superior instalado e configurado.  

Agora que temos o essencial, vamos mergulhar no código.

## Importar Pacotes

Comece importando as classes necessárias do Aspose.PSD. Isso lhe dá acesso ao carregamento de imagens, opções de substituição de fonte e recursos de exportação PNG.

```java
import com.aspose.psd.Image;

import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
import com.aspose.psd.imageoptions.PngOptions;
```

## Etapa 1: Configurar o Diretório do Documento

Defina a pasta que contém o PSD de origem e onde o PNG resultante será salvo.

```java
String dataDir = "Your Document Directory";
```

## Etapa 2: Especificar Arquivos de Origem e Destino

Forneça os caminhos completos para o PSD de entrada e o PNG de saída. Isso torna o fluxo de trabalho claro e mantém o código fácil de manter.

```java
String sourceFile = dataDir + "sample.psd";
String destName = dataDir + "result.png";
```

## Etapa 3: Configurar as Definições de Substituição de Fonte

Crie uma instância de `PsdLoadOptions` e informe ao Aspose.PSD qual fonte usar quando encontrar uma ausente. Neste exemplo usamos **Arial**, mas você pode substituí‑la por qualquer fonte instalada no seu sistema.

```java
PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setDefaultReplacementFont("Arial");
```

## Etapa 4: Carregar a Imagem PSD e Substituir Fontes

Carregue o PSD usando as opções definidas acima. A biblioteca troca automaticamente quaisquer fontes ausentes pela padrão que você especificou.

```java
Image image = Image.load(sourceFile, loadOptions);
PsdImage psdImage = (PsdImage) image;
```

## Etapa 5: Salvar a Imagem Modificada

Configure as opções de exportação PNG — cores verdadeiras com canal alfa — para preservar a transparência. Esta etapa também demonstra **conversão de imagem PSD para PNG** após a substituição de fonte.

```java
PngOptions options = new PngOptions();
options.setColorType(PngColorType.TruecolorWithAlpha);
psdImage.save(destName, options);
```

### O que Acabou de Acontecer?

- O PSD foi aberto com uma fonte de fallback (Arial).  
- Todas as camadas de texto que originalmente referenciavam fontes ausentes agora são renderizadas usando Arial.  
- A imagem final foi salva como PNG, efetivamente **salvando PSD como PNG** enquanto preserva a fidelidade visual.

## Problemas Comuns & Solução de Problemas

| Problema | Causa | Solução |
|----------|-------|----------|
| Texto ainda parece errado | Métricas da fonte diferem (tamanho, peso) | Ajuste programaticamente o tamanho da fonte de substituição ou escolha uma fonte com métricas semelhantes. |
| PNG é maior que o esperado | As opções padrão de PNG usam cor de 32 bits | Troque `PngColorType` para `Truecolor` se o canal alfa não for necessário. |
| Exceção de licença | Execução sem licença válida | Aplique uma licença temporária ou permanente do Aspose.PSD antes de carregar a imagem. |

## Perguntas Frequentes

**P: O Aspose.PSD é compatível com todas as versões de arquivos PSD?**  
R: O Aspose.PSD suporta uma ampla gama de versões PSD, desde as primeiras releases do Photoshop até os recursos mais recentes.

**P: Posso usar fontes personalizadas para substituição no Aspose.PSD?**  
R: Sim, basta passar o nome da fonte personalizada para `setDefaultReplacementFont`. Certifique‑se de que a fonte esteja acessível ao JVM.

**P: Existem opções de licenciamento disponíveis para o Aspose.PSD?**  
R: Explore as opções de licenciamento [aqui](https://purchase.aspose.com/buy) para escolher o plano mais adequado às suas necessidades.

**P: Existe um fórum da comunidade para suporte ao Aspose.PSD?**  
R: Sim, visite o [fórum Aspose.PSD](https://forum.aspose.com/c/psd/34) para suporte da comunidade e discussões.

**P: Como posso obter uma licença temporária para o Aspose.PSD?**  
R: Obtenha uma licença temporária [aqui](https://purchase.aspose.com/temporary-license/) para fins de teste e avaliação.

---

**Última atualização:** 2025-12-25  
**Testado com:** Aspose.PSD 24.11 para Java (mais recente no momento da escrita)  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}
{{< blocks/products/products-backtop-button >}}