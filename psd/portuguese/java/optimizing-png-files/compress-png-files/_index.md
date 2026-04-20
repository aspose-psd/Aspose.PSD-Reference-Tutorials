---
date: 2026-03-15
description: Aprenda a comprimir arquivos PNG usando Aspose.PSD para Java, um guia
  passo a passo sobre como comprimir PNG, otimizar o tamanho do PNG e converter PSD
  para PNG de forma eficiente.
linktitle: Compress PNG Files using Aspose.PSD for Java
second_title: Aspose.PSD Java API
title: Como compactar arquivos PNG usando Aspose.PSD para Java
url: /pt/java/optimizing-png-files/compress-png-files/
weight: 12
---

 to keep bold formatting.

Translate table headings.

Translate FAQ.

Let's craft.

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Como comprimir arquivos PNG usando Aspose.PSD para Java

## Introdução

Quando se trata de manipular imagens no desenvolvimento de software, aprender **como comprimir PNG** de forma eficiente pode melhorar drasticamente o tempo de carregamento das páginas e reduzir o uso de largura de banda. Aspose.PSD para Java é uma biblioteca poderosa que permite trabalhar com arquivos Photoshop (PSD) e exportá‑los para diversos formatos, incluindo PNG. Seja para **otimizar o tamanho do PNG**, converter PSD para PNG para uma galeria web ou ajustar **níveis de compressão PNG**, este tutorial o guiará por um exemplo completo, pronto para produção.

## Respostas Rápidas
- **O que significa “como comprimir PNG”?** Refere‑se à redução do tamanho de arquivo de uma imagem PNG mantendo a qualidade visual, tipicamente ajustando parâmetros de compressão.  
- **Qual biblioteca é a melhor para compressão PNG em Java?** Aspose.PSD para Java oferece opções de PNG integradas e suporta toda a gama de níveis de compressão (0‑9).  
- **Preciso de licença?** Um teste gratuito funciona para avaliação; uma licença comercial é necessária para uso em produção.  
- **Posso automatizar múltiplos níveis de compressão?** Sim—percorrendo a propriedade `setCompressionLevel` você pode gerar PNGs em todos os níveis.  
- **Esta abordagem é adequada para arquivos PSD grandes?** Absolutamente; Aspose.PSD transmite dados de forma eficiente, sendo seguro para ativos de alta resolução.

## O que é compressão PNG?

PNG usa compressão sem perdas, ou seja, a qualidade da imagem permanece intacta enquanto o tamanho do arquivo é reduzido. Ao ajustar o **nível de compressão PNG** (0 = sem compressão, 9 = compressão máxima) você controla quão agressivamente os dados são compactados. Níveis mais altos demoram um pouco mais para processar, mas resultam em arquivos menores—perfeito para otimização web.

## Por que usar Aspose.PSD para Java para comprimir PNG?

- **Suporte total a PSD** – Abra, edite e exporte camadas PSD sem perder informações.  
- **Controle granular** – Defina níveis exatos de compressão PNG, tipo de cor e profundidade de bits.  
- **Multiplataforma** – Funciona em qualquer ambiente compatível com Java, de aplicativos desktop a serviços em nuvem.  
- **Desempenho** – Código nativo otimizado garante processamento rápido mesmo para imagens grandes.  

## Pré‑requisitos

Antes de mergulharmos no código, verifique se você possui o seguinte:

1. **Java JDK** – Baixe o JDK mais recente no [site da Oracle](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).  
2. **Biblioteca Aspose.PSD para Java** – Baixe o JAR mais novo na página oficial de download [aqui](https://releases.aspose.com/psd/java/).  
3. **IDE ou editor de código** – IntelliJ IDEA, Eclipse ou VS Code funcionam perfeitamente.  
4. **Conhecimento básico de Java** – Familiaridade com tratamento de exceções e I/O de arquivos acelera a curva de aprendizado.  
5. **Arquivo PSD de exemplo** – Coloque um arquivo PSD (por exemplo, `sample.psd`) em uma pasta que você referenciará como diretório de documentos.

Ter esses itens prontos permitirá que você se concentre nas etapas de **otimização de imagem java** em vez de lidar com problemas de configuração.

## Importar Pacotes

Os imports a seguir dão acesso às classes principais do Aspose.PSD e às opções de PNG:

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.PngOptions;
```

Essas classes permitem carregar um PSD, configurar as opções de PNG e salvar o resultado.

## Etapa 1: Configurar Seu Projeto

Crie um novo projeto Java (por exemplo, `PsdImageCompressor`) e adicione o JAR do Aspose.PSD ao caminho de compilação. Isso garante que o compilador encontre as classes referenciadas acima.

## Etapa 2: Definir Seu Diretório de Documentos

Informe ao programa onde encontrar o arquivo PSD de origem e onde gravar os PNGs comprimidos:

```java
String dataDir = "Your Document Directory"; // Replace with actual path
```

Substitua `"Your Document Directory"` pelo caminho absoluto ou relativo que contém `sample.psd`. Manter o caminho configurável facilita **converter PSD para PNG** em diferentes ambientes.

## Etapa 3: Carregar a Imagem PSD

Carregue o arquivo PSD na memória. Esta etapa é análoga a abrir um livro antes de começar a lê‑lo:

```java
PsdImage psdImage = (PsdImage)Image.load(dataDir + "sample.psd");
```

Se o arquivo não for encontrado, Aspose.PSD lançará uma exceção informativa—verifique novamente o nome e o caminho do arquivo.

## Etapa 4: Percorrer os Níveis de Compressão

Para explorar cada **nível de compressão png** possível, usamos um simples loop `for`. Ele cria automaticamente nove PNGs adicionais, cada um com uma configuração de compressão diferente:

```java
for (int i = 0; i <= 9; i++) {
    // Create a new instance of PngOptions
    PngOptions options = new PngOptions();
    options.setCompressionLevel(i); // Set the compression level
```

O loop vai de 0 (sem compressão) a 9 (compressão máxima), oferecendo uma visão clara do trade‑off entre tamanho do arquivo e tempo de processamento.

## Etapa 5: Salvar os Arquivos PNG Comprimidos

Dentro do loop, salve cada PNG usando um nome de arquivo que reflita seu nível de compressão. Isso torna a comparação direta:

```java
    psdImage.save(dataDir + i + "_out.png", options);
}
```

Ao final do loop, você terá arquivos chamados `0_out.png`, `1_out.png`, … `9_out.png` no seu diretório.

## Problemas Comuns e Soluções

| Problema | Por que acontece | Solução |
|----------|------------------|---------|
| **FileNotFoundException** | Caminho `dataDir` incorreto ou `sample.psd` ausente. | Verifique a string de caminho e assegure que o arquivo PSD exista. |
| **OutOfMemoryError** em PSDs grandes | Carregamento de um PSD enorme sem heap suficiente. | Aumente o heap da JVM (`-Xmx2g`) ou processe a imagem em partes. |
| **PNG comprimido parece inalterado** | Uso de nível de compressão baixo (0‑2). | Aumente o nível para 5‑9 para redução de tamanho perceptível. |
| **LicenseException** | Execução sem licença válida do Aspose.PSD. | Aplique uma licença de teste ou adquira uma licença completa. |

## Perguntas Frequentes

**P: O que é Aspose.PSD para Java?**  
R: Aspose.PSD para Java é uma biblioteca que permite a desenvolvedores manipular arquivos Photoshop programaticamente, incluindo leitura, edição e exportação para formatos como PNG, JPEG e TIFF.

**P: Posso comprimir outros formatos de imagem além de PNG?**  
R: Este tutorial foca em PNG, mas Aspose.PSD suporta PSD, TIFF, JPEG, BMP e mais. Você pode trocar a classe de opções de saída para direcionar outro formato.

**P: Preciso de licença para usar Aspose.PSD?**  
R: Embora seja possível avaliar a biblioteca com um teste gratuito, uma licença completa é necessária para implantações em produção. Você pode obtê‑la [aqui](https://purchase.aspose.com/buy).

**P: E se eu encontrar um erro ao executar o código?**  
R: Verifique novamente seus caminhos de arquivo, assegure que todas as instruções de importação estejam presentes e confirme que está usando uma versão compatível do JAR do Aspose.PSD.

**P: Onde encontro mais documentação sobre Aspose.PSD para Java?**  
R: Referências detalhadas da API e exemplos adicionais estão disponíveis na [referência Aspose.PSD](https://reference.aspose.com/psd/java/).

---

**Última atualização:** 2026-03-15  
**Testado com:** Aspose.PSD para Java 24.12 (mais recente na data de escrita)  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}