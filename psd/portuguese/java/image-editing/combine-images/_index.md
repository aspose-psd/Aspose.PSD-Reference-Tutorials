---
date: 2025-12-30
description: Aprenda como criar um arquivo PSD em Java combinando duas imagens usando
  Aspose.PSD. Siga nosso guia passo a passo para mesclar imagens em um arquivo PSD
  rapidamente.
linktitle: Combine Images
second_title: Aspose.PSD Java API
title: Como criar um arquivo PSD em Java – Combine imagens com Aspose.PSD
url: /pt/java/image-editing/combine-images/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Criar arquivo PSD em Java – Combinar Imagens usando Aspose.PSD

## Introdução

Se você precisa **criar um arquivo PSD em Java** mesclando várias imagens, o Aspose.PSD torna a tarefa simples. Neste tutorial vamos percorrer o processo de combinar duas imagens em uma única tela PSD, explicar por que essa abordagem é útil e fornecer código pronto‑para‑executar. Ao final, você será capaz de **combinar duas imagens em Java** e gerar um arquivo em camadas com aparência profissional.

## Respostas rápidas
- **Qual biblioteca é a melhor para mesclar imagens em PSD?** Aspose.PSD for Java.  
- **Quanto tempo leva a implementação?** Cerca de 10‑15 minutos para uma combinação básica.  
- **Preciso de licença?** Uma avaliação gratuita funciona para testes; uma licença comercial é necessária para produção.  
- **Posso adicionar mais de duas imagens?** Sim – repita as chamadas `drawImage` para cada camada adicional.  
- **Qual versão do Java é suportada?** Java 8 e superior.

## Pré‑requisitos

Antes de começar, certifique‑se de que você tem o seguinte:

1. **Biblioteca Aspose.PSD** – faça o download em [here](https://releases.aspose.com/psd/java/).  
2. **Java Development Kit (JDK)** – recomenda‑se Java 8+.  
3. **Diretório de documentos** – uma pasta na sua máquina onde as imagens de origem e o PSD resultante serão armazenados.

## Importar pacotes

Comece importando as classes necessárias do Aspose.PSD para o seu projeto:

```java
import com.aspose.psd.Color;
import com.aspose.psd.Graphics;
import com.aspose.psd.Image;

import com.aspose.psd.imageoptions.PsdOptions;
import com.aspose.psd.sources.FileCreateSource;
```

## Guia passo a passo

### Etapa 1: Criar opções de PSD (preparar o arquivo)

Primeiro criamos uma instância `PsdOptions` que conterá as configurações de saída.

```java
PsdOptions imageOptions = new PsdOptions();
```

### Etapa 2: Definir o FileCreateSource (especificar onde o PSD será salvo)

Atribua um `FileCreateSource` às opções, apontando para o arquivo de resultado desejado.

```java
imageOptions.setSource(new FileCreateSource(dataDir + "Two_images_result_out.psd", false));
```

### Etapa 3: Criar instância de Image (inicializar o tamanho da tela)

Crie um objeto `Image` com as opções e especifique uma tela de 600 × 600 pixels.

```java
Image image = Image.create(imageOptions, 600, 600);
```

### Etapa 4: Inicializar Graphics e desenhar a primeira imagem

Um objeto `Graphics` permite pintar na tela. Limpe o fundo para branco e desenhe a primeira imagem de origem na metade esquerda.

```java
Graphics graphics = new Graphics(image);
graphics.clear(Color.getWhite());
graphics.drawImage(Image.load(dataDir + "example1.psd"), 0, 0, 300, 600);
```

### Etapa 5: Desenhar a segunda imagem (concluir a combinação)

Agora posicionamos a segunda imagem na metade direita da mesma tela.

```java
graphics.drawImage(Image.load(dataDir + "example2.psd"), 300, 0, 300, 600);
```

### Etapa 6: Salvar o arquivo PSD resultante

Por fim, persista a tela combinada no disco.

```java
image.save();
```

Parabéns! Você combinou imagens em PSD com sucesso e criou um arquivo PSD em Java.

## Por que combinar imagens com Aspose.PSD?

- **Consciente de camadas** – cada chamada `drawImage` adiciona uma camada separada que pode ser editada posteriormente.  
- **Flexibilidade de formato** – suporta PSD, PNG, JPEG, BMP e muito mais.  
- **Sem dependências nativas** – Java puro, funciona em qualquer SO que execute o JDK.  

## Problemas comuns e soluções

| Problema | Causa | Solução |
|----------|-------|---------|
| Erro `File not found` ao carregar imagens de origem | Caminho `dataDir` incorreto | Verifique se `dataDir` aponta para a pasta que contém `example1.psd` e `example2.psd`. |
| PSD de saída está em branco | `graphics.clear` chamado após o desenho | Garanta que `graphics.clear(Color.getWhite())` seja executado **antes** de qualquer chamada `drawImage`. |
| Exceção de licença em tempo de execução | Licença Aspose.PSD ausente ou expirada | Aplique uma licença válida usando `License license = new License(); license.setLicense("Aspose.PSD.lic");` antes de qualquer chamada de API. |

## Perguntas frequentes

### Q1: O Aspose.PSD é compatível com todos os formatos de imagem?
A1: O Aspose.PSD foca principalmente no formato de arquivo PSD. No entanto, ele suporta vários outros formatos para entrada e saída.

### Q2: Posso realizar modificações adicionais na imagem combinada?
A2: Absolutamente! Após combinar as imagens, você pode manipular ainda mais o PSD resultante usando os recursos extensos do Aspose.PSD.

### Q3: Existem requisitos de licenciamento para usar o Aspose.PSD?
A3: Sim, uma licença válida é necessária para uso comercial. Obtenha-a em [here](https://purchase.aspose.com/buy).

### Q4: Há uma avaliação gratuita disponível para o Aspose.PSD?
A4: Sim, você pode explorar o Aspose.PSD com uma avaliação gratuita [here](https://releases.aspose.com/).

### Q5: Onde posso encontrar suporte para dúvidas relacionadas ao Aspose.PSD?
A5: Visite o [Aspose.PSD forum](https://forum.aspose.com/c/psd/34) para suporte da comunidade e discussões.

---

**Última atualização:** 2025-12-30  
**Testado com:** Aspose.PSD 24.11 for Java  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}