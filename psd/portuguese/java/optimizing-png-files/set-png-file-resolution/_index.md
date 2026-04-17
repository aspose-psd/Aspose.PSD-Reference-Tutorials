---
date: 2026-03-18
description: Aprenda como alterar a resolução de PNG em Java e definir a resolução
  de imagens em Java com Aspose.PSD para Java. Siga este guia passo a passo para otimizar
  suas imagens rapidamente.
linktitle: Change PNG resolution java using Aspose.PSD
second_title: Aspose.PSD Java API
title: Alterar a resolução PNG em Java usando Aspose.PSD
url: /pt/java/optimizing-png-files/set-png-file-resolution/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Alterar resolução PNG java usando Aspose.PSD

## Introdução
Se você precisa **alterar a resolução PNG java** de forma rápida e confiável, está no lugar certo. Neste tutorial vamos percorrer passo a passo as etapas necessárias para ajustar a resolução de um arquivo PNG com Aspose.PSD para Java. Seja você quem esteja construindo uma ferramenta de processamento em lote, um serviço web ou apenas aprimorando alguns recursos, a mesma abordagem funciona em qualquer cenário. Pegue sua IDE favorita e vamos começar!

## Respostas Rápidas
- **Qual biblioteca lida com a resolução PNG?** Aspose.PSD for Java  
- **Método principal?** `PngOptions.setResolutionSettings`  
- **Valores típicos de DPI?** 72 × 96 para imagens prontas para web  
- **Preciso de licença?** Uma versão de avaliação funciona para testes; uma licença é necessária para produção  
- **JDK suportado?** Java 8 ou superior  

## O que é “alterar resolução PNG java”?
Alterar a resolução PNG em Java significa modificar os metadados DPI (pontos por polegada) que indicam aos navegadores e impressoras o tamanho que a imagem deve aparecer. Os dados de pixel permanecem os mesmos, mas a tag de resolução é atualizada, o que pode afetar o tamanho e a qualidade da impressão.

## Por que usar Aspose.PSD para esta tarefa?
Aspose.PSD fornece uma API de alto nível que abstrai o manuseio de PNG de baixo nível, permitindo que você se concentre na lógica de negócios em vez das particularidades do formato de arquivo. Ele suporta centenas de recursos de PSD, funciona em qualquer plataforma que execute Java e não requer bibliotecas nativas.

## Pré-requisitos
Antes de começar, certifique‑se de que você tem:

1. **Java Development Kit (JDK) 8+** – o código roda em qualquer JDK recente.  
2. **Aspose.PSD for Java** – faça o download a partir do [link de download](https://releases.aspose.com/psd/java/).  
3. **Uma IDE** – IntelliJ IDEA, Eclipse ou VS Code com suporte a Java.  
4. **Um arquivo PSD de exemplo** – vamos convertê‑lo para PNG e alterar sua resolução.  
5. **Conhecimento básico de Java** – você entenderá os trechos de código sem explicações adicionais.

## Importar Pacotes
Agora que tudo está configurado, importe as classes que você precisará. Essas importações dão acesso ao carregamento de imagens, configurações de resolução e opções de exportação PNG.

```java
import com.aspose.psd.Image;
import com.aspose.psd.ResolutionSetting;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.PngOptions;
```

## Etapa 1: Configurar seu Projeto Java
Crie um novo projeto Java (ou módulo Maven/Gradle) e adicione o JAR do Aspose.PSD ao caminho de compilação. Se estiver usando Maven, adicione a dependência apropriada do repositório Aspose.

## Etapa 2: Definir o Diretório do Documento
Informe ao programa onde encontrar o arquivo PSD de origem e onde gravar o PNG de saída.

```java
String dataDir = "Your Document Directory"; // Update with your folder path
```

Substitua `"Your Document Directory"` pelo caminho absoluto ou relativo que contém `sample.psd`.

## Etapa 3: Carregar a Imagem PSD
Use a classe `PsdImage` para ler o arquivo PSD do disco.

```java
PsdImage psdImage = (PsdImage) Image.load(dataDir + "sample.psd");
```

Certifique‑se de que o nome do arquivo corresponde ao PSD real que você deseja processar.

## Etapa 4: Criar e Configurar as Opções PNG
Aqui é onde realmente **alteramos a resolução PNG java**. Instanciamos `PngOptions` e definimos os valores DPI horizontal e vertical via `ResolutionSetting`.

```java
PngOptions options = new PngOptions();
options.setResolutionSettings(new ResolutionSetting(72, 96)); // 72 DPI horizontal, 96 DPI vertical
```

Sinta‑se à vontade para substituir `72` e `96` por quaisquer valores que atendam ao seu dispositivo alvo. Este é o núcleo da operação **set image resolution java**.

## Etapa 5: Salvar o PNG Resultante
Por fim, exporte o PSD como PNG com os novos metadados de resolução.

```java
psdImage.save(dataDir + "SettingResolution_output.png", options);
```

O arquivo `SettingResolution_output.png` aparecerá na mesma pasta, agora contendo os valores DPI que você especificou.

## Armadilhas Comuns & Dicas
- **Caminho incorreto** – Verifique se `dataDir` termina com um separador de arquivos (`/` ou `\`).  
- **DPI não suportado** – A maioria dos navegadores ignora valores DPI acima de 300; mantenha‑os razoáveis.  
- **Uso de memória** – PSDs grandes podem consumir muita RAM; considere descartar `psdImage` após salvar (`psdImage.dispose()`).  

## Conclusão
Você acabou de aprender como **alterar a resolução PNG java** usando Aspose.PSD. Ajustando `ResolutionSetting`, você controla como seus PNGs são interpretados por impressoras e ferramentas de design sem alterar os dados de pixel. Explore outras opções como nível de compressão, profundidade de cor ou processamento em lote para automatizar ainda mais seu fluxo de trabalho.

Para exploração mais profunda, consulte a oficial [Documentação do Aspose.PSD](https://reference.aspose.com/psd/java/).

## Perguntas Frequentes
### Quais formatos posso converter arquivos PSD usando Aspose.PSD para Java?
Você pode converter arquivos PSD para formatos como PNG, JPEG, BMP e TIFF.  
### Preciso de licença para usar Aspose.PSD para Java?
Sim, embora haja uma versão de avaliação gratuita, uma licença válida é necessária para uso contínuo após a avaliação.  
### Posso alterar a resolução mais de uma vez em um programa?
Absolutamente! Você pode criar diferentes instâncias de `PngOptions` para várias configurações de exportação dentro da mesma aplicação.  
### E se meu arquivo PSD estiver corrompido?
Aspose.PSD lida com muitos problemas comuns, mas se um arquivo estiver gravemente corrompido, pode não ser carregado. Sempre mantenha um backup.  
### O Aspose.PSD é adequado para aplicações de alto desempenho?
Sim, ele foi projetado para lidar com arquivos grandes de forma eficiente e é adequado para tarefas de processamento de imagem intensivas em desempenho.

## Perguntas Frequentes
**Q: Como eu programaticamente defino um DPI diferente para os eixos horizontal e vertical?**  
A: Use `new ResolutionSetting(horizontalDpi, verticalDpi)` conforme mostrado no exemplo de opções PNG.  

**Q: Posso processar vários arquivos PSD em lote em uma única execução?**  
A: Sim—envolva as etapas de carregamento, configuração de opções e salvamento dentro de um loop que itere sobre sua coleção de arquivos.  

**Q: Alterar o DPI afeta o tamanho do arquivo?**  
A: Normalmente não; DPI é metadado. O tamanho do arquivo só muda se você modificar a compressão ou as dimensões dos pixels.  

**Q: Existe uma maneira de ler o DPI atual de um PNG existente?**  
A: Carregue o PNG com `Image.load()` e inspecione `image.getResolutionSettings()` (disponível para arquivos PNG).  

**Q: Quais versões do JDK são oficialmente suportadas?**  
A: Aspose.PSD for Java suporta JDK 8 até JDK 21.  

**Última atualização:** 2026-03-18  
**Testado com:** Aspose.PSD for Java 24.10  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}