---
date: 2026-01-01
description: Aprenda a criar metadados XMP, adicionar XMP a arquivos PSD e atualizar
  os metadados de imagens com Aspose.PSD para Java. Siga este guia passo a passo agora.
linktitle: Create XMP Metadata
second_title: Aspose.PSD Java API
title: Criar Metadados XMP com Aspose.PSD para Java
url: /pt/java/image-editing/create-xmp-metadata/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Criar Metadados XMP com Aspose.PSD para Java

## Introdução

Gerenciar metadados de imagem é uma necessidade comum para desenvolvedores Java que trabalham com arquivos Photoshop (PSD). Neste tutorial você aprenderá **como criar metadados XMP** usando a biblioteca Aspose.PSD, adicionar XMP a uma imagem PSD e atualizar os metadados da imagem programaticamente. Percorreremos cada passo, explicaremos por que cada parte é importante e daremos dicas práticas que você pode aplicar em projetos reais.

## Respostas Rápidas
- **O que são metadados XMP?** Um formato padronizado para incorporar informações descritivas (autor, palavras‑chave, etc.) dentro de arquivos de imagem.  
- **Por que usar Aspose.PSD?** Ele fornece uma API pura‑Java para criar, ler e editar arquivos PSD sem o Photoshop.  
- **Posso adicionar XMP a um PSD existente?** Sim – você pode atualizar os metadados da imagem em tempo real com `setXmpData`.  
- **Quais são os passos principais?** Definir o tamanho da imagem, criar cabeçalho/rodapé, construir pacotes XMP, anexá‑los e salvar.  
- **Preciso de licença?** Uma versão de avaliação gratuita funciona para desenvolvimento; uma licença comercial é necessária para produção.

## O que significa “criar metadados XMP” em Java?

Criar metadados XMP significa construir um pacote XMP (cabeçalho, corpo, rodapé) que descreve a imagem e então incorporar esse pacote em um arquivo PSD. A biblioteca Aspose.PSD abstrai os detalhes de baixo nível, permitindo que você se concentre no conteúdo que deseja armazenar.

## Por que adicionar XMP a arquivos PSD?

- **Facilidade de busca:** Permite buscas poderosas de gerenciamento de ativos baseadas em autor, título ou tags personalizadas.  
- **Interoperabilidade:** XMP é reconhecido pelos produtos Adobe, Lightroom e muitos sistemas DAM.  
- **Controle de versão:** Armazena o histórico de processamento (por exemplo, cidade, modo de cor) diretamente dentro do arquivo.

## Prerequisites

- **Ambiente de Desenvolvimento Java:** JDK 8 ou superior instalado e compreensão básica de Java.  
- **Biblioteca Aspose.PSD:** Baixe e configure a biblioteca Aspose.PSD para Java. Você pode encontrar a biblioteca e a documentação detalhada [aqui](https://reference.aspose.com/psd/java/).  
- **Seu Diretório de Documentos:** Decida onde você lerá/escreverá arquivos PSD no seu sistema.

## Importar Pacotes

In your Java project, import the necessary packages to leverage Aspose.PSD functionalities:

```java
import com.aspose.psd.Rectangle;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.system.io.MemoryStream;
import com.aspose.psd.xmp.XmpHeaderPi;
import com.aspose.psd.xmp.XmpMeta;
import com.aspose.psd.xmp.XmpPacketWrapper;
import com.aspose.psd.xmp.XmpTrailerPi;
import com.aspose.psd.xmp.schemas.dublincore.DublinCorePackage;
import com.aspose.psd.xmp.schemas.photoshop.ColorMode;
import com.aspose.psd.xmp.schemas.photoshop.PhotoshopPackage;
```

## Etapa 1: Especificar o Tamanho da Imagem

Primeiro, defina as dimensões da tela para a nova imagem PSD.

```java
// Specify the size of the image by defining a Rectangle
Rectangle rect = new Rectangle(0, 0, 100, 200);
```

## Etapa 2: Criar uma Nova Imagem

Crie uma imagem PSD em branco que posteriormente iremos enriquecer com metadados XMP.

```java
// Create a brand new image for sample purposes
PsdImage image = new PsdImage(rect.getWidth(), rect.getHeight());
```

## Etapa 3: Criar o Cabeçalho XMP

O cabeçalho contém a instrução de processamento XML de abertura e um GUID que identifica o documento.

```java
// Create an instance of XMP-Header
XmpHeaderPi xmpHeader = new XmpHeaderPi();
xmpHeader.setGuid("Your Document Directory");
```

## Etapa 4: Criar o Rodapé XMP

O rodapé marca o fim do pacote XMP. Definir o parâmetro `true` grava a instrução de processamento de fechamento.

```java
// Create an instance of Xmp-TrailerPi 
XmpTrailerPi xmpTrailer = new XmpTrailerPi(true);
```

## Etapa 5: Criar Metadados XMP

Adicione atributos genéricos como autor e descrição ao objeto central de metadados XMP.

```java
// Create an instance of XMPmeta class to set different attributes
XmpMeta xmpMeta = new XmpMeta();
xmpMeta.addAttribute("Author", "Mr Smith");
xmpMeta.addAttribute("Description", "The fake metadata value");
```

## Etapa 6: Criar o Invólucro do Pacote XMP

Envolva o cabeçalho, o rodapé e os metadados centrais em um único pacote que pode ser anexado à imagem.

```java
// Create an instance of XmpPacketWrapper that contains all metadata
XmpPacketWrapper xmpData = new XmpPacketWrapper(xmpHeader, xmpTrailer, xmpMeta);
```

## Etapa 7: Definir Atributos do Photoshop

Preencha campos específicos do Photoshop (cidade, país, modo de cor) que muitas ferramentas da Adobe esperam.

```java
// Create an instance of Photoshop package and set Photoshop attributes
PhotoshopPackage photoshopPackage = new PhotoshopPackage();
photoshopPackage.setCity("London");
photoshopPackage.setCountry("England");
photoshopPackage.setColorMode(ColorMode.Rgb);
```

## Etapa 8: Adicionar Pacote Photoshop aos Metadados XMP

Anexe o pacote Photoshop ao pacote XMP.

```java
// Add Photoshop package into XMP metadata
xmpData.addPackage(photoshopPackage);
```

## Etapa 9: Definir Atributos DublinCore

Adicione metadados Dublin Core como autor, título e uma tag personalizada de filme.

```java
// Create an instance of DublinCore package and set DublinCore attributes
DublinCorePackage dublinCorePackage = new DublinCorePackage();
dublinCorePackage.setAuthor("Charles Bukowski");
dublinCorePackage.setTitle("Confessions of a Man Insane Enough to Live With the Beasts");
dublinCorePackage.addValue("dc:movie", "Barfly");
```

## Etapa 10: Adicionar Pacote DublinCore aos Metadados XMP

Combine o pacote Dublin Core com o pacote XMP existente.

```java
// Add DublinCore Package into XMP metadata
xmpData.addPackage(dublinCorePackage);
```

## Etapa 11: Atualizar Metadados XMP na Imagem

Agora incorpore o pacote XMP completo na imagem PSD.

```java
// Update XMP metadata into the image
image.setXmpData(xmpData);
```

## Etapa 12: Salvar Imagem

Finalmente, grave o arquivo PSD no disco (ou em um fluxo de memória) para que os metadados sejam persistidos.

```java
// Save the image on the disk or in a memory stream
image.save("Your Document Directory" + "create_XMP_Metadata.psd");
```

## Problemas Comuns e Soluções

| Problema | Por que acontece | Solução |
|----------|------------------|--------|
| **`NullPointerException` on `setXmpData`** | O pacote XMP não foi construído completamente (faltando cabeçalho/rodapé). | Certifique‑se de criar `XmpHeaderPi`, `XmpTrailerPi` e adicionar todos os pacotes antes de chamar `setXmpData`. |
| **Metadata not visible in Photoshop** | O Photoshop espera que o pacote XMP esteja corretamente encapsulado. | Verifique se `XmpTrailerPi(true)` está sendo usado e se o pacote é salvo com a imagem. |
| **File path errors** | Uso de um caminho relativo sem permissões adequadas. | Use um caminho absoluto ou garanta que a aplicação tenha permissão de gravação na pasta de destino. |

## Perguntas Frequentes

**Q: O Aspose.PSD é compatível com diferentes formatos de imagem?**  
A: Sim, o Aspose.PSD suporta PSD, PSB, BMP, GIF, JPEG, PNG, TIFF e mais, oferecendo flexibilidade entre formatos.

**Q: Posso manipular metadados existentes usando Aspose.PSD?**  
A: Absolutamente. Você pode carregar um PSD existente, recuperar seus dados XMP com `getXmpData()`, modificar o pacote e salvá‑lo novamente.

**Q: Existem limitações no tamanho de imagem que o Aspose.PSD pode manipular?**  
A: O Aspose.PSD foi projetado para trabalhar com imagens grandes (até vários gigapixels), limitado apenas pela memória disponível.

**Q: Existe uma versão de avaliação disponível para o Aspose.PSD?**  
A: Sim, você pode explorar os recursos do Aspose.PSD obtendo uma avaliação gratuita [aqui](https://releases.aspose.com/).

**Q: Onde posso buscar suporte para dúvidas relacionadas ao Aspose.PSD?**  
A: Para qualquer assistência ou dúvidas, visite o [fórum Aspose.PSD](https://forum.aspose.com/c/psd/34).

## Conclusão

Agora você dominou **como criar metadados XMP**, adicionar XMP a um PSD e atualizar os metadados da imagem usando Aspose.PSD para Java. Essas etapas dão a você controle total sobre as informações descritivas incorporadas em suas imagens, tornando-as pesquisáveis e prontas para fluxos de trabalho subsequentes. Sinta‑se à vontade para experimentar esquemas XMP adicionais ou integrar este código em pipelines maiores de processamento de imagens.

---

**Last Updated:** 2026-01-01  
**Tested With:** Aspose.PSD for Java 24.12  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}