---
date: 2026-03-13
description: Aprenda a criar projetos Java de imagens PSD enquanto gerencia a realocação
  de cache com Aspose.PSD para Java. Otimize o uso de memória e disco de forma eficiente.
linktitle: Create PSD Image Java – Control Cache Reallocation
second_title: Aspose.PSD Java API
title: Criar Imagem PSD em Java – Controlar Realocação de Cache
url: /pt/java/modifying-converting-psd-images/control-cache-reallocation-psd-files/
weight: 22
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Controlar a Realocação de Cache em Arquivos PSD

## Introdução
Se você precisa **create PSD image java** projetos de forma eficiente, controlar a realocação de cache é essencial. Ao trabalhar com imagens e arquivos Photoshop programaticamente, a eficiência é um fator chave. Aspose.PSD for Java oferece recursos robustos para gerenciar e manipular arquivos PSD sem esforço. Um dos aspectos fundamentais para otimizar o desempenho é controlar a realocação de cache. O gerenciamento de cache ajuda a manter o equilíbrio entre o uso de memória e disco, garantindo que sua aplicação funcione suavemente, sem travamentos ou lentidões inesperadas. 

## Respostas Rápidas
- **O que a realocação de cache faz?** Ela equilibra o uso de memória e disco ao processar arquivos PSD grandes.  
- **Qual tipo de cache é melhor para imagens grandes?** `CacheOnDiskOnly` mantém a memória livre armazenando o cache no disco.  
- **Quanto espaço em disco posso alocar?** Até 1 GB (ou qualquer tamanho que você definir com `setMaxDiskSpaceForCache`).  
- **Preciso de uma licença para usar esses recursos?** Uma licença remove as limitações da versão de avaliação; veja a página de compra da Aspose.  
- **Posso monitorar o uso de cache em tempo de execução?** Sim, use `Cache.getAllocatedDiskBytesCount()` e `Cache.getAllocatedMemoryBytesCount()`.

## Por que Controlar a Realocação de Cache?
Gerenciar o cache é crucial quando você **create PSD image java** aplicações que lidam com arquivos de alta resolução ou multilayer. Configurações adequadas de cache evitam erros de falta de memória, reduzem pausas do GC e proporcionam desempenho previsível em servidores ou aplicativos desktop.

## Pré-requisitos
Antes de mergulharmos na parte de codificação, há algumas coisas que você precisa garantir para que tudo funcione sem problemas:
1. Java Development Kit (JDK): Certifique-se de que o JDK está instalado na sua máquina. Você pode baixá-lo no [site da Oracle](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).
2. Aspose.PSD for Java: Você precisa baixar a biblioteca Aspose.PSD. Você pode encontrar a versão mais recente [aqui](https://releases.aspose.com/psd/java/).
3. Configuração da IDE: Um Ambiente de Desenvolvimento Integrado (IDE) como IntelliJ IDEA ou Eclipse facilitará o gerenciamento do seu código.
4. Compreensão Básica de Java: Familiaridade com programação Java ajudará a entender melhor os conceitos e trechos de código.
5. Licença Aspose (Opcional): Se desejar remover marcas d'água e obter funcionalidade completa, considere comprar uma licença [aqui](https://purchase.aspose.com/buy) ou experimentar o teste gratuito [aqui](https://releases.aspose.com/).

## Importar Pacotes
Antes de começarmos a escrever o código, vamos garantir que os pacotes necessários estejam importados. Abaixo está uma breve lista do que incluir no início do seu arquivo Java:
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

## Como Criar PSD Image Java com Controle de Cache
A seguir, um passo‑a‑passo que vincula a configuração de cache diretamente ao processo de criação de uma imagem PSD em Java.

### Etapa 1: Configurando Seu Diretório de Dados
Primeiro, você precisará configurar um diretório onde deseja que os arquivos de cache sejam armazenados. Isso é essencial para gerenciar o cache de forma eficaz.
```java
String dataDir = "Your Document Directory";
Cache.setCacheFolder(dataDir);
```

- `String dataDir`: Define o diretório para o cache do seu documento.  
- `Cache.setCacheFolder(dataDir)`: Este método define a pasta de cache para o diretório especificado. Qualquer cache criado pela Aspose será agora armazenado aqui em vez do diretório temporário padrão.

### Etapa 2: Configurando o Cache para Disco
Em seguida, especificaremos que queremos que nosso cache seja armazenado apenas no disco. Isso é particularmente útil se sua aplicação usar arquivos grandes e você quiser garantir que a memória permaneça livre.
```java
Cache.setCacheType(CacheType.CacheOnDiskOnly);
```

- `Cache.setCacheType(CacheType.CacheOnDiskOnly)`: Esta opção garante que o cache não seja mantido na memória, o que é benéfico ao lidar com arquivos PSD grandes sem consumir muita RAM.

### Etapa 3: Definindo o Tamanho Máximo de Cache em Disco e Memória
Agora, vamos restringir os tamanhos do cache. Isso é crucial porque um cache ilimitado pode causar problemas de desempenho.
```java
Cache.setMaxDiskSpaceForCache(1073741824); // 1 gigabyte
Cache.setMaxMemoryForCache(1073741824); // 1 gigabyte
```

- `Cache.setMaxDiskSpaceForCache(1073741824)`: Define um limite de 1 GB para o cache em disco. Você pode ajustar esse tamanho conforme suas necessidades.  
- `Cache.setMaxMemoryForCache(1073741824)`: Da mesma forma, limita o cache em memória, garantindo que sua aplicação não use memória excessiva.

### Etapa 4: Gerenciar a Estratégia de Realocação de Cache
Gerenciar como o cache é realocado é essencial para manter o desempenho. Veja como configurá-lo.
```java
Cache.setExactReallocateOnly(false);
```

- `Cache.setExactReallocateOnly(false)`: Quando definido como `false`, permite que a Aspose gerencie a realocação de cache de forma mais flexível, o que pode levar a um melhor desempenho.

### Etapa 5: Verificar o Tamanho de Cache Alocado
Esta etapa trata de monitorar quantos bytes estão atualmente alocados para o cache na memória ou no disco. Vamos implementá-la:
```java
long l1 = Cache.getAllocatedDiskBytesCount();
long l2 = Cache.getAllocatedMemoryBytesCount();
```

- `long l1`: Armazena a contagem de bytes alocados no disco.  
- `long l2`: Armazena a contagem de bytes alocados na memória.  
Você pode verificar esses valores a qualquer momento para garantir que sua aplicação está gerenciando o uso de memória e disco como esperado.

### Etapa 6: Criando uma Imagem PSD
Agora que configuramos nosso cache, vamos criar uma imagem PSD simples.
```java
PsdOptions options = new PsdOptions();
Color[] color = { Color.getRed(), Color.getBlue(), Color.getBlack(), Color.getWhite() };
options.setPalette(new ColorPalette(color));
options.setSource(new StreamSource(new ByteArrayInputStream(new byte[0])));
RasterImage image = (RasterImage) Image.create(options, 100, 100);
```

- `PsdOptions options`: Este objeto permite especificar opções ao criar uma imagem Photoshop.  
- `Color[] color`: Um array contendo as cores que serão usadas na paleta da imagem.

### Etapa 7: Salvando Dados de Pixels na Imagem
Agora, vamos preencher nossa imagem com dados de pixels e salvá‑la.
```java
Color[] pixels = new Color[10000];
for (int i = 0; i < pixels.length; i++) {
    pixels[i] = Color.getWhite();
}
image.savePixels(image.getBounds(), pixels);
```

- `Color[] pixels`: Este é um array de objetos de cor. Aqui, estamos preenchendo‑o com pixels brancos.  
- `image.savePixels(image.getBounds(), pixels)`: Este método salva os dados de pixel na imagem. Ele atualiza a imagem com as cores que definimos.

### Etapa 8: Monitorando o Cache Alocado Após a Criação da Imagem
Após criar a imagem, é uma boa prática verificar novamente quantos bytes estão alocados para o cache.
```java
long diskBytes = Cache.getAllocatedDiskBytesCount();
long memoryBytes = Cache.getAllocatedMemoryBytesCount();
```

- `long diskBytes`: Captura a alocação atual no disco após a criação da imagem.  
- `long memoryBytes`: Captura a alocação atual na memória.  
Esta etapa ajudará a determinar quanto cache está sendo consumido após suas operações.

### Etapa 9: Verificar a Descarte Adequado
Por fim, é crucial garantir que todos os objetos Aspose.PSD foram descartados corretamente para evitar vazamentos de memória.
```java
l1 = Cache.getAllocatedDiskBytesCount();
l2 = Cache.getAllocatedMemoryBytesCount();
```

- `l1` e `l2`: Estas variáveis ajudarão a verificar a alocação final. Se não forem zero, indica que alguns objetos não foram descartados corretamente.

## Problemas Comuns e Soluções
- **Pasta de cache não criada** – Verifique se a aplicação tem permissões de gravação para o caminho passado para `Cache.setCacheFolder`.  
- **Erros de falta de memória** – Verifique novamente se `Cache.setCacheType(CacheType.CacheOnDiskOnly)` está aplicado antes de carregar arquivos PSD grandes.  
- **Tamanho de cache inesperado** – Use os métodos `Cache.getAllocated*BytesCount()` após cada operação importante para acompanhar o crescimento.

## Perguntas Frequentes

**Q: O que é Aspose.PSD?**  
A: Aspose.PSD é uma biblioteca para desenvolvedores .NET e Java criar, manipular e converter arquivos Photoshop (PSD) programaticamente.

**Q: Como verifico o tamanho de cache alocado?**  
A: Use métodos como `Cache.getAllocatedDiskBytesCount()` e `Cache.getAllocatedMemoryBytesCount()` para monitorar o uso atual do cache.

**Q: Posso definir um diretório personalizado para o cache?**  
A: Sim, você pode especificar um diretório diferente usando `Cache.setCacheFolder("Your Directory Path")`.

**Q: O Aspose.PSD é gratuito?**  
A: Aspose.PSD é uma biblioteca paga, mas você pode começar com um teste gratuito disponível no [site](https://releases.aspose.com/).

**Q: O que acontece se eu não descartar os objetos?**  
A: Não descartar os objetos pode levar a vazamentos de memória, fazendo com que sua aplicação use mais recursos do que o necessário.

## Conclusão
Controlar a realocação de cache enquanto você **create PSD image java** aplicações pode fazer uma diferença significativa no desempenho. Seguindo os passos acima, você gerenciará o cache de forma eficiente, minimizará o consumo de memória e gerará arquivos PSD de alta qualidade com Aspose.PSD for Java. Aplique essas técnicas, e seus projetos rodarão de forma mais suave e escalarão melhor.

---

**Last Updated:** 2026-03-13  
**Testado com:** Aspose.PSD for Java (latest release)  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}