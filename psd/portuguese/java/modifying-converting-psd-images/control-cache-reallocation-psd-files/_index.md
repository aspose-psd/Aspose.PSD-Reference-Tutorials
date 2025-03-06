---
title: Controlar a realocação de cache em arquivos PSD
linktitle: Controlar a realocação de cache em arquivos PSD
second_title: API Java Aspose.PSD
description: Gerencie a realocação de cache em arquivos PSD usando Aspose.PSD para Java. Aprenda como otimizar a memória e o manuseio de arquivos com eficiência, ideal para desenvolvedores.
weight: 22
url: /pt/java/modifying-converting-psd-images/control-cache-reallocation-psd-files/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Controlar a realocação de cache em arquivos PSD

## Introdução
Ao trabalhar com imagens e arquivos do Photoshop de forma programática, a eficiência é um fator chave. Aspose.PSD para Java oferece recursos robustos para gerenciar e manipular arquivos PSD perfeitamente. Um dos aspectos fundamentais da otimização do desempenho é controlar a realocação do cache. O gerenciamento de cache ajuda a manter o equilíbrio entre memória e uso de disco, garantindo que seu aplicativo funcione sem problemas, sem travamentos ou lentidão inesperadas. 
## Pré-requisitos
Antes de passarmos para a parte de codificação, há algumas coisas que você precisa garantir para que tudo corra bem:
1. Java Development Kit (JDK): Certifique-se de ter o JDK instalado em sua máquina. Você pode baixá-lo em[Site da Oracle](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).
2. Aspose.PSD para Java: Você precisa baixar a biblioteca Aspose.PSD. Você pode encontrar a versão mais recente[aqui](https://releases.aspose.com/psd/java/).
3. Configuração IDE: Um ambiente de desenvolvimento integrado (IDE) como IntelliJ IDEA ou Eclipse tornará mais fácil para você gerenciar seu código.
4. Compreensão básica de Java: A familiaridade com a programação Java o ajudará a entender melhor os conceitos e trechos de código.
5.  Licença Aspose (opcional): Se você deseja remover marcas d'água e obter funcionalidade completa, considere comprar uma licença[aqui](https://purchase.aspose.com/buy) ou experimentando o teste gratuito[aqui](https://releases.aspose.com/).
## Importar pacotes
Antes de começarmos a escrever o código, vamos nos certificar de que importamos os pacotes necessários. Abaixo está uma breve lista do que incluir no início do seu arquivo Java:
```java
import com.aspose.psd.Cache;
import com.aspose.psd.CacheType;
import com.aspose.psd.Color;
import com.aspose.psd.ColorPalette;
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;
import com.aspose.psd.imageoptions.GifOptions;
import com.aspose.psd.imageoptions.PsdOptions;
import com.aspose.psd.sources.StreamSource;
import com.aspose.psd.system.io.MemoryStream;
```
## Etapa 1: configurando seu diretório de dados
Primeiramente, você precisará configurar um diretório onde deseja que seus arquivos de cache sejam armazenados. Isto é essencial para gerenciar o cache de forma eficaz.
```java
String dataDir = "Your Document Directory";
Cache.setCacheFolder(dataDir);
```

- String dataDir: Defina o diretório para seu cache de documentos.
- Cache.setCacheFolder(dataDir): Este método define a pasta de cache para o diretório especificado. Qualquer cache criado pelo Aspose agora será armazenado aqui em vez do diretório temporário padrão.
## Etapa 2: configurar cache para disco
A seguir, especificaremos que queremos que nosso cache seja armazenado apenas em disco. Isto é particularmente útil se o seu aplicativo usa arquivos grandes e você deseja garantir que a memória permaneça livre.
```java
Cache.setCacheType(CacheType.CacheOnDiskOnly);
```

- Cache.setCacheType(CacheType.CacheOnDiskOnly): Esta opção garante que o cache não seja mantido na memória, o que é benéfico para lidar com arquivos PSD grandes sem consumir muita RAM.
## Etapa 3: definir o tamanho máximo do disco e do cache de memória
Agora, vamos restringir o tamanho do nosso cache. Isto é crucial porque o cache ilimitado pode levar a problemas de desempenho.
```java
Cache.setMaxDiskSpaceForCache(1073741824); // 1 gigabyte
Cache.setMaxMemoryForCache(1073741824); // 1 gigabyte
```

- Cache.setMaxDiskSpaceForCache(1073741824): define um limite de 1 GB para o cache no disco. Você pode ajustar esse tamanho dependendo de suas necessidades.
- Cache.setMaxMemoryForCache(1073741824): Da mesma forma, limita o cache na memória, garantindo que seu aplicativo não use memória excessiva.
## Etapa 4: gerenciar estratégia de realocação de cache
Gerenciar como o cache é realocado é essencial para manter o desempenho. Veja como você pode configurá-lo.
```java
Cache.setExactReallocateOnly(false);
```

- Cache.setExactReallocateOnly(false): Quando definido como false, permite que o Aspose gerencie a realocação de cache com mais flexibilidade, o que pode levar a um melhor desempenho.
## Etapa 5: verifique o tamanho do cache alocado
Esta etapa trata do monitoramento de quantos bytes estão atualmente alocados para o cache na memória ou no disco. Vamos implementar isso:
```java
long l1 = Cache.getAllocatedDiskBytesCount();
long l2 = Cache.getAllocatedMemoryBytesCount();
```

- long l1: Armazena a contagem de bytes alocados no disco.
- long l2: Armazena a contagem de bytes alocados na memória. 
Você pode verificar esses valores a qualquer momento para garantir que seu aplicativo esteja gerenciando a memória e o uso do disco conforme esperado.
## Etapa 6: Criando uma imagem PSD
Agora que configuramos nossas configurações de cache, vamos criar uma imagem PSD simples.
```java
PsdOptions options = new PsdOptions();
Color[] color = { Color.getRed(), Color.getBlue(), Color.getBlack(), Color.getWhite() };
options.setPalette(new ColorPalette(color));
options.setSource(new StreamSource(new ByteArrayInputStream(new byte[0])));
RasterImage image = (RasterImage) Image.create(options, 100, 100);
```

- Opções PsdOptions: Este objeto permite especificar opções ao criar uma imagem no Photoshop.
- Cor[] color: Um array contendo as cores que serão utilizadas na paleta da imagem.
## Etapa 7: salvando dados de pixel na imagem
Agora, vamos preencher nossa imagem com dados de pixel e salvá-la.
```java
Color[] pixels = new Color[10000];
for (int i = 0; i < pixels.length; i++) {
    pixels[i] = Color.getWhite();
}
image.savePixels(image.getBounds(), pixels);
```

- Cor[] pixels: Esta é uma matriz de objetos coloridos. Aqui, estamos preenchendo com pixels brancos.
- image.savePixels(image.getBounds(), pixels): Este método salva os dados de pixel na imagem. Atualiza a imagem com as cores que definimos.
## Etapa 8: Monitorando o cache alocado após a criação da imagem
Depois de criar a imagem, é uma boa prática verificar novamente quantos bytes estão alocados para o cache.
```java
long diskBytes = Cache.getAllocatedDiskBytesCount();
long memoryBytes = Cache.getAllocatedMemoryBytesCount();
```

- long diskBytes: captura a alocação atual no disco após a criação da imagem.
- long memoryBytes: captura a alocação atual na memória. 
Esta etapa ajudará você a determinar quanto cache está sendo consumido após suas operações.
## Etapa 9: Verifique o descarte adequado
Por último, é crucial garantir que todos os objetos Aspose.PSD foram descartados adequadamente para evitar vazamentos de memória.
```java
l1 = Cache.getAllocatedDiskBytesCount();
l2 = Cache.getAllocatedMemoryBytesCount();
```

- l1 e l2: Essas variáveis ajudarão você a verificar a alocação final. Se não forem zero, indica que alguns objetos não foram descartados adequadamente.
## Conclusão
Controlar a realocação de cache no Aspose.PSD para Java pode fazer uma diferença significativa no desempenho do seu aplicativo. Seguindo as etapas descritas acima, você pode gerenciar o cache com eficácia, minimizar o uso de memória e criar lindos arquivos PSD com eficiência. Adote essas técnicas e observe seus aplicativos prosperarem com desempenho ideal!
## Perguntas frequentes
### O que é Aspose.PSD?
Aspose.PSD é uma biblioteca para desenvolvedores .NET e Java criarem, manipularem e converterem arquivos do Photoshop (PSD) programaticamente.
### Como verifico o tamanho do cache alocado?
 Utilize métodos como`Cache.getAllocatedDiskBytesCount()` e`Cache.getAllocatedMemoryBytesCount()` para monitorar o uso atual do cache.
### Posso definir um diretório personalizado para cache?
 Sim, você pode especificar um diretório diferente usando`Cache.setCacheFolder("Your Directory Path")`.
### O uso do Aspose.PSD é gratuito?
Aspose.PSD é uma biblioteca paga, mas você pode começar com uma avaliação gratuita disponível em seu site.[site](https://releases.aspose.com/).
### O que acontece se eu não descartar os objetos?
Não descartar objetos pode causar vazamentos de memória, fazendo com que seu aplicativo utilize mais recursos do que o necessário.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
