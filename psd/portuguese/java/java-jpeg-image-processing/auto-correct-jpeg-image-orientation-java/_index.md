---
title: Correção automática da orientação da imagem JPEG em Java
linktitle: Correção automática da orientação da imagem JPEG em Java
second_title: API Java Aspose.PSD
description: Aprenda a corrigir automaticamente a orientação da imagem JPEG em Java usando Aspose.PSD. Aprimore suas habilidades de processamento de imagens sem esforço.
type: docs
weight: 12
url: /pt/java/java-jpeg-image-processing/auto-correct-jpeg-image-orientation-java/
---
## Introdução
Na era digital de hoje, a manipulação e otimização de imagens de forma programática tornou-se uma tarefa crucial para desenvolvedores em vários domínios. Aspose.PSD para Java capacita os desenvolvedores com ferramentas robustas para lidar com PSD, JPEG e outros formatos de imagem com eficiência. Este tutorial se aprofunda em uma tarefa específica: corrigir automaticamente a orientação da imagem JPEG usando Aspose.PSD para Java. Esteja você criando um aplicativo de edição de fotos, gerenciando recursos de imagem em um sistema de gerenciamento de conteúdo ou automatizando fluxos de trabalho de processamento de imagens, este guia fornecerá o conhecimento necessário para integrar perfeitamente essa funcionalidade em seus aplicativos Java.
## Pré-requisitos
Antes de mergulhar neste tutorial, certifique-se de ter os seguintes pré-requisitos configurados:
- Ambiente de Desenvolvimento Java: Certifique-se de ter o Java Development Kit (JDK) instalado em seu sistema.
-  Aspose.PSD para Java JAR: Baixe a biblioteca Aspose.PSD para Java em[aqui](https://releases.aspose.com/psd/java/).
- Ambiente de Desenvolvimento Integrado (IDE): Use IntelliJ IDEA, Eclipse ou qualquer IDE de sua escolha para desenvolvimento Java.
- Compreensão básica de Java e processamento de imagens: A familiaridade com programação Java e conceitos básicos de processamento de imagens será benéfica.

## Importar pacotes
Antes de começar com o exemplo, certifique-se de importar os pacotes necessários do Aspose.PSD para Java:
```java
import com.aspose.psd.Image;
import com.aspose.psd.exif.JpegExifData;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.resources.Thumbnail4Resource;
import com.aspose.psd.fileformats.psd.resources.ThumbnailResource;
```
## Passo 1: Carregue a imagem PSD
Primeiramente, carregue a imagem PSD que contém a miniatura JPEG cuja orientação precisa de correção:
```java
String dataDir = "Your Document Directory";
PsdImage image = (PsdImage)Image.load(dataDir + "1280px-Zebras_Serengeti.psd");
```
 Substituir`"Your Document Directory"` com o caminho real do diretório onde seu arquivo PSD está localizado.
## Etapa 2: iterar sobre recursos de imagem
Em seguida, percorra os recursos de imagem para encontrar o recurso de miniatura JPEG:
```java
for (int i = 0; i < image.getImageResources().length; i++) {
    // Encontre recursos de miniaturas. Normalmente eles estão no formato de arquivo Jpeg.
    if (image.getImageResources()[i] instanceof ThumbnailResource || image.getImageResources()[i] instanceof Thumbnail4Resource) {
        // Ajuste os dados das miniaturas.
        ThumbnailResource thumbnail = (ThumbnailResource) image.getImageResources()[i];
        JpegExifData exifData = thumbnail.getJpegOptions().getExifData();
        if (exifData != null && exifData.getThumbnail() != null) {
            // Se houver uma miniatura armazenada, gire-a automaticamente.
            PsdImage jpegImage = (PsdImage) exifData.getThumbnail();
            if (jpegImage != null) {
                jpegImage.autoRotate();
            }
        }
    }
}
```
## Etapa 3: salve a imagem
Por fim, salve a imagem corrigida após aplicar a rotação automática:
```java
image.save();
```
Esta etapa garante que as alterações feitas na imagem sejam persistidas.

## Conclusão
Concluindo, usar Aspose.PSD para Java fornece uma solução poderosa para corrigir automaticamente as orientações de imagens JPEG em arquivos PSD. Seguindo as etapas descritas neste tutorial, os desenvolvedores podem aprimorar seus fluxos de trabalho de processamento de imagens, garantindo que as imagens sejam exibidas corretamente em várias plataformas e dispositivos.
## Perguntas frequentes
### O que é Aspose.PSD para Java?
Aspose.PSD for Java é uma biblioteca poderosa que permite aos desenvolvedores Java trabalhar com PSD, JPEG e outros formatos de imagem de forma programática.
### Como posso baixar Aspose.PSD para Java?
 Você pode baixar a biblioteca em[aqui](https://releases.aspose.com/psd/java/).
### O Aspose.PSD para Java oferece suporte à manipulação de imagens?
Sim, ele oferece suporte a várias tarefas de manipulação de imagens, como redimensionamento, corte e ajuste de orientação.
### Onde posso encontrar documentação para Aspose.PSD para Java?
 Documentação abrangente está disponível[aqui](https://reference.aspose.com/psd/java/).
### Posso experimentar o Aspose.PSD para Java gratuitamente?
 Sim, você pode obter um teste gratuito em[aqui](https://releases.aspose.com/).