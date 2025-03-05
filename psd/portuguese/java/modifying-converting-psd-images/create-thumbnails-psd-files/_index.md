---
title: Crie miniaturas de arquivos PSD usando Java
linktitle: Crie miniaturas de arquivos PSD usando Java
second_title: API Java Aspose.PSD
description: Aprenda como criar miniaturas de arquivos PSD sem esforço usando Java e Aspose.PSD. Siga nosso guia passo a passo para um processamento de imagem perfeito.
type: docs
weight: 24
url: /pt/java/modifying-converting-psd-images/create-thumbnails-psd-files/
---
## Introdução
No mundo do design gráfico, trabalhar com arquivos PSD (Photoshop Document) é comum. Quer você seja um desenvolvedor experiente, um designer gráfico ou apenas alguém que deseja mergulhar no processamento de imagens, a criação de miniaturas a partir de arquivos PSD pode economizar tempo e agilizar seu fluxo de trabalho. Este tutorial irá guiá-lo por todo o processo usando Aspose.PSD para Java. Aspose.PSD não é apenas uma biblioteca robusta para gerenciar arquivos do Photoshop, mas também torna a tarefa intuitiva e gerenciável. Você está pronto para aprender como criar miniaturas de arquivos PSD com eficiência?
## Pré-requisitos
Antes de mergulharmos nos detalhes da criação de miniaturas, vamos abordar o que você precisa para começar.
### Ambiente de Desenvolvimento Java
-  Java JDK: Certifique-se de ter o Java Development Kit (JDK) instalado em seu computador. Você pode baixá-lo[aqui](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).
- IDE: Um ambiente de desenvolvimento integrado (IDE) como IntelliJ IDEA, Eclipse ou NetBeans tornará a codificação mais fácil.
### Biblioteca Aspose.PSD
- Você precisa incluir a biblioteca Aspose.PSD em seu projeto. Você pode[baixe a versão mais recente aqui](https://releases.aspose.com/psd/java/).
### Conhecimento básico de Java
- A familiaridade com os fundamentos do Java o ajudará a navegar pelo código de exemplo com mais eficiência. Conceitos como classes, objetos e loops serão empregados com frequência.
## Importar pacotes
Comece importando as classes necessárias da biblioteca Aspose.PSD. Esta etapa é crucial porque permite aproveitar as funcionalidades da biblioteca em seu código.
```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.resources.ThumbnailFormat;
import com.aspose.psd.fileformats.psd.resources.ThumbnailResource;
```
Com os pré-requisitos resolvidos, vamos para o evento principal! A criação de miniaturas de arquivos PSD envolve algumas etapas simples e vou detalhar para você.
## Etapa 1: configure seu ambiente
Veja como iniciar seu projeto e se preparar para a geração de miniaturas.
1. Crie um projeto Java:
   - Abra seu IDE e crie um novo projeto Java.
   - Nomeie-o como "PsdThumbnailGenerator".
2. Incluir biblioteca Aspose.PSD:
   -  Adicione o arquivo JAR Aspose.PSD ao caminho de construção do seu projeto. Se você estiver usando o Maven, inclua-o em seu`pom.xml`:
     ```xml
     <dependency>
         <groupId>com.aspose</groupId>
         <artifactId>aspose-psd</artifactId>
         <version>your_version_here</version>
     </dependency>
     ```
## Passo 2: Carregue o arquivo PSD
Em seguida, precisamos carregar o arquivo PSD a partir do qual queremos criar as miniaturas. 
1. Especifique seu diretório de documentos:
   Defina o diretório onde seu arquivo PSD está localizado.
   ```java
   String dataDir = "Your Document Directory"; // Substitua pelo seu caminho
   ```
2. Carregue o arquivo PSD:
    Use o`PsdImage` class para carregar seu arquivo PSD.
   ```java
   PsdImage image = (PsdImage) Image.load(dataDir + "sample.psd");
   ```
 Aqui,`sample.psd` é o nome do seu arquivo PSD. Ajuste isso de acordo com o nome do seu arquivo.
## Etapa 3: iterar sobre recursos PSD
Agora que carregamos nossa imagem PSD, o próximo passo é examinar seus recursos.
1. Obtenha contagem de recursos:
   Percorreremos todos os recursos do arquivo PSD.
   ```java
   for (int i = 0; i < image.getImageResources().length; i++) {
       // Processando recursos
   }
   ```
   
2. Identifique recursos de miniatura:
   Dentro do loop, verifique se um recurso é uma miniatura.
   ```java
   if (image.getImageResources()[i] instanceof ThumbnailResource) {
       // Processar a miniatura
   }
   ```
## Etapa 4: processar a miniatura
Depois de identificarmos um recurso de miniatura, precisaremos tratá-lo adequadamente.
1. Recuperar e verificar o formato da miniatura:
   Se o recurso for de fato uma miniatura, recupere-o e verifique seu formato.
   ```java
   ThumbnailResource thumbnail = (ThumbnailResource) image.getImageResources()[i];
   if (thumbnail.getFormat() == ThumbnailFormat.KJpegRgb) {
       // Crie e salve a miniatura
   }
   ```
## Etapa 5: crie e salve a miniatura
É aqui que a mágica acontece! Criaremos uma nova imagem a partir dos dados da miniatura e a salvaremos.
1. Crie uma nova imagem:
   Usaremos a largura e a altura do recurso de miniatura para criar uma nova imagem bitmap.
   ```java
   PsdImage thumbnailImage = new PsdImage(thumbnail.getWidth(), thumbnail.getHeight());
   ```
2. Armazene pixels na nova imagem:
   Transfira os dados da miniatura para a imagem recém-criada.
   ```java
   thumbnailImage.savePixels(thumbnailImage.getBounds(), thumbnail.getThumbnailData());
   ```
3. Salve a imagem em miniatura:
   Por fim, salve a imagem em miniatura no diretório de documentos com um nome exclusivo.
   ```java
   thumbnailImage.save(dataDir + "CreateThumbnailsFromPSDFiles_out_" + i + ".bmp");
   ```

## Conclusão
Criar miniaturas de arquivos PSD usando Java e Aspose.PSD pode ser uma tarefa simples, uma vez dividida em etapas gerenciáveis. Com este tutorial, agora você tem o poder de extrair miniaturas de seus arquivos PSD com facilidade, oferecendo uma ferramenta bacana para aprimorar seu fluxo de trabalho. Então, o que está impedindo você? Obtenha alguns arquivos PSD e experimente!
## Perguntas frequentes
### O que é Aspose.PSD?
Aspose.PSD é uma biblioteca Java que permite aos desenvolvedores trabalhar com arquivos do Photoshop, facilitando a manipulação e o gerenciamento de arquivos PSD de forma programática.
### Posso usar o Aspose.PSD gratuitamente?
Sim, o Aspose oferece uma avaliação gratuita que você pode usar para testar a biblioteca antes de comprar uma licença.
### Em quais formatos posso salvar as miniaturas?
Neste exemplo, salvamos as miniaturas no formato BMP, mas Aspose.PSD também suporta vários outros formatos.
### Preciso do Photoshop instalado para usar o Aspose.PSD?
Não, o Aspose.PSD funciona independentemente do Photoshop.
### Onde posso encontrar mais informações sobre o Aspose.PSD?
 Você pode conferir o[Documentação Aspose.PSD](https://reference.aspose.com/psd/java/) para obter mais detalhes, tutoriais e recursos.