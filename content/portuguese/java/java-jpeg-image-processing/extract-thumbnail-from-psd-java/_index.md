---
title: Extraia miniatura do PSD em Java
linktitle: Extraia miniatura do PSD em Java
second_title: API Java Aspose.PSD
description: Aprenda como extrair miniaturas de arquivos PSD usando Aspose.PSD para Java. Este guia passo a passo cobre tudo, desde a configuração até o salvamento das imagens extraídas.
type: docs
weight: 15
url: /pt/java/java-jpeg-image-processing/extract-thumbnail-from-psd-java/
---
## Introdução
Neste tutorial, exploraremos como extrair miniaturas de arquivos PSD usando Aspose.PSD para Java. As miniaturas podem ser úteis para visualizações rápidas ou para criar versões menores de imagens incorporadas em documentos PSD. Vamos mergulhar nas etapas necessárias para conseguir isso usando Aspose.PSD.
## Pré-requisitos
Antes de começarmos, certifique-se de ter a seguinte configuração:
- Java Development Kit (JDK) instalado em seu sistema.
-  Aspose.PSD para biblioteca Java. Você pode baixá-lo em[aqui](https://releases.aspose.com/psd/java/).
- Conhecimento básico de programação Java.
## Importar pacotes
Para começar, inclua o pacote Aspose.PSD necessário em sua classe Java:
```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.resources.Thumbnail4Resource;
import com.aspose.psd.fileformats.psd.resources.ThumbnailResource;
import com.aspose.psd.imageoptions.JpegOptions;
```
## Passo 1: Carregue o arquivo PSD
Primeiro, carregue o arquivo PSD que contém a miniatura que deseja extrair.
```java
String dataDir = "Your_Document_Directory/";
PsdImage image = (PsdImage)Image.load(dataDir + "your_file.psd");
```
 Substituir`"Your_Document_Directory/"` com o caminho do diretório onde seu arquivo PSD está localizado e`"your_file.psd"` com o nome do seu arquivo PSD.
## Etapa 2: iterar sobre recursos de imagem
Itere pelos recursos de imagem para encontrar o recurso de miniatura.
```java
for (int i = 0; i < image.getImageResources().length; i++) {
    if (image.getImageResources()[i] instanceof ThumbnailResource) {
        ThumbnailResource thumbnail = (ThumbnailResource) image.getImageResources()[i];
        
        // Extraia dados de miniaturas
        int[] data = thumbnail.getThumbnailArgb32Data();
        
        // Crie uma nova imagem com os dados extraídos da miniatura
        PsdImage extractedThumbnailImage = new PsdImage(thumbnail.getWidth(), thumbnail.getHeight());
        extractedThumbnailImage.saveArgb32Pixels(extractedThumbnailImage.getBounds(), data);
        
        // Salve a miniatura extraída como um arquivo JPEG separado
        extractedThumbnailImage.save(dataDir + "extracted_thumbnail.jpg", new JpegOptions());
        
        // Mensagem de sucesso de saída
        System.out.println("Thumbnail extracted and saved successfully.");
        
        break; // Saia do loop assim que a miniatura for encontrada e processada
    }
}
```
## Etapa 3: salve a miniatura extraída
Salve a miniatura extraída como um arquivo de imagem separado (neste caso, como um arquivo JPEG).
## Etapa 4: lidar com diferentes tipos de miniaturas
 Se o seu arquivo PSD puder conter vários tipos de miniaturas, como`Thumbnail4Resource`, você pode estender a lógica para lidar com esses casos de forma semelhante.

## Conclusão
Neste tutorial, exploramos como extrair miniaturas de arquivos PSD usando Aspose.PSD para Java. Seguindo as etapas descritas acima, você pode recuperar e salvar com eficiência miniaturas incorporadas em seus documentos PSD.

## Perguntas frequentes
### O que é Aspose.PSD?
Aspose.PSD é uma biblioteca Java que permite aos desenvolvedores trabalhar com PSD e outros formatos de arquivo de imagem de forma programática.
### Onde posso encontrar mais documentação sobre Aspose.PSD para Java?
 Você pode consultar o[documentação](https://reference.aspose.com/psd/java/) para referências e exemplos detalhados de API.
### Posso experimentar o Aspose.PSD gratuitamente antes de comprar?
 Sim, você pode baixar um[teste gratuito](https://releases.aspose.com/) para avaliar as capacidades da biblioteca.
### Como posso obter licenças temporárias para Aspose.PSD?
 Licenças temporárias podem ser obtidas em[aqui](https://purchase.aspose.com/temporary-license/).
### O Aspose.PSD é adequado para uso comercial?
Sim, o Aspose.PSD pode ser usado para projetos pessoais e comerciais sob seus termos de licenciamento.