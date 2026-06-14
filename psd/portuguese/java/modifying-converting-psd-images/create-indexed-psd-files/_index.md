---
date: 2026-03-15
description: Aprenda a criar arquivos PSD, gerar a paleta de cores PSD e definir o
  modo de cor PSD usando o Aspose.PSD para Java neste guia passo a passo.
linktitle: Create Indexed PSD Files using Aspose.PSD for Java
second_title: Aspose.PSD Java API
title: Como criar arquivos PSD usando Aspose.PSD para Java
url: /pt/java/modifying-converting-psd-images/create-indexed-psd-files/
weight: 23
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Como Criar Arquivos PSD Usando Aspose.PSD para Java

## Introdução
Se você já se perguntou **como criar PSD** programaticamente, está no lugar certo. Aspose.PSD para Java oferece controle total sobre documentos do Photoshop, permitindo gerar, editar e salvar arquivos PSD sem nunca abrir o Photoshop. Neste tutorial, vamos percorrer a criação de um arquivo **PSD indexado**, definir o modo de cor do PSD e gerar uma paleta de cores personalizada — tudo com código Java claro, passo a passo. Seja você quem está construindo um pipeline gráfico, automatizando a criação de ativos ou apenas experimentando, os conceitos aqui ajudarão a transformar suas ideias visuais em realidade.

## Respostas Rápidas
- **Qual biblioteca eu preciso?** Aspose.PSD para Java  
- **Posso criar um PSD indexado?** Sim, definindo o modo de cor para `Indexed`  
- **Preciso ter o Photoshop instalado?** Não, Aspose.PSD funciona de forma independente  
- **Qual versão do Java é necessária?** JDK 8 ou superior  
- **Qual o tamanho máximo da tela?** Qualquer tamanho; este exemplo usa 500 × 500 px  

## O que é um Arquivo PSD Indexado?
Um PSD indexado armazena as cores em uma paleta ao invés de valores de cor completos para cada pixel. Isso reduz o tamanho do arquivo e é ideal para gráficos com cores limitadas, como ícones ou ativos de UI. Ao gerar uma paleta personalizada, você controla exatamente quais cores aparecerão na imagem final.

## Por que Gerar uma Paleta de Cores PSD?
Criar uma **paleta de cores PSD** permite:
- Manter os tamanhos de arquivo pequenos para uso web ou mobile  
- Garantir consistência de marca limitando as cores à sua paleta corporativa  
- Acelerar a renderização em aplicações que suportam imagens indexadas  

## Pré‑requisitos
Antes de mergulharmos no código, certifique‑se de que você possui o seguinte:

1. **Conhecimento Básico de Java** – você deve estar confortável com classes, métodos e criação de objetos.  
2. **Java Development Kit (JDK) 8+** – instalado e configurado no seu IDE.  
3. **IDE (IntelliJ IDEA, Eclipse, etc.)** – opcional, mas altamente recomendado para depuração mais fácil.  
4. **Biblioteca Aspose.PSD para Java** – faça o download **[aqui](https://releases.aspose.com/psd/java/)** e adicione o JAR ao classpath do seu projeto.  
5. **Conceitos Fundamentais de Design Gráfico** – entender modos de cor, paletas e formas básicas ajudará a acompanhar o tutorial.  

## Importar Pacotes
Antes de prosseguirmos com o código, vamos garantir que todos os pacotes necessários estejam importados na sua aplicação Java. Veja o que você precisará:

```java
import com.aspose.psd.Color;
import com.aspose.psd.Graphics;
import com.aspose.psd.Image;
import com.aspose.psd.Pen;
import com.aspose.psd.Rectangle;
import com.aspose.psd.fileformats.psd.ColorModes;
import com.aspose.psd.fileformats.psd.CompressionMethod;
import com.aspose.psd.fileformats.psd.PsdColorPalette;
import com.aspose.psd.imageoptions.PsdOptions;
import com.aspose.psd.sources.FileCreateSource;
```

Essas importações permitem trabalhar com opções de PSD, cores e manipulação gráfica através do Aspose.PSD.

Agora, vamos detalhar o código passo a passo para **como criar PSD** com modo de cor indexado.

## Etapa 1: Configurar o Diretório do Documento
Primeiro, defina onde o PSD gerado será salvo.

```java
String dataDir = "Your Document Directory";
```

Substitua `"Your Document Directory"` por um caminho absoluto ou relativo, por exemplo, `"/Users/YourName/Documents/"`.

## Etapa 2: Criar uma Instância de PsdOptions
`PsdOptions` contém todas as configurações para o arquivo que você está prestes a gerar.

```java
PsdOptions createOptions = new PsdOptions();
```

## Etapa 3: Definir Propriedades Principais de PsdOptions
Aqui especificamos o local de saída, o **modo de cor do PSD** para `Indexed` e a versão do PSD.

```java
createOptions.setSource(new FileCreateSource(dataDir + "Newsample_out.psd", false));
createOptions.setColorMode(ColorModes.Indexed);
createOptions.setVersion(5);
```

- **Source** – o caminho completo do novo arquivo.  
- **Color Mode** – `Indexed` indica ao Aspose.PSD que a imagem usará uma paleta.  
- **Version** – versão do formato PSD (5 funciona na maioria das versões modernas do Photoshop).  

## Etapa 4: Criar uma Paleta de Cores (Gerar Paleta de Cores PSD)
Defina as cores que estarão disponíveis na imagem indexada.

```java
Color[] palette = { Color.getRed(), Color.getGreen(), Color.getBlue(), Color.getYellow() };
createOptions.setPalette(new PsdColorPalette(palette));
createOptions.setCompressionMethod(CompressionMethod.RLE);
```

- O array `palette` comporta até 256 objetos `Color`.  
- `CompressionMethod.RLE` fornece compressão lossless eficiente para imagens indexadas.  

## Etapa 5: Criar a Tela da Imagem PSD
Agora criamos um PSD em branco com as dimensões desejadas.

```java
Image psd = Image.create(createOptions, 500, 500);
```

Isso cria uma tela de 500 × 500 pixels que utiliza a paleta definida anteriormente.

## Etapa 6: Desenhar Gráficos no PSD
Adicione conteúdo visual — aqui desenhamos uma elipse vermelha simples sobre um fundo branco.

```java
Graphics graphics = new Graphics(psd);
graphics.clear(Color.getWhite());
graphics.drawEllipse(new Pen(Color.getRed(), 6), new Rectangle(0, 0, 400, 400));
```

- `clear(Color.getWhite())` preenche o fundo com branco.  
- `drawEllipse` renderiza uma elipse vermelha com traço de 6 pixels.  

## Etapa 7: Salvar o Arquivo PSD
Por fim, persista a imagem no disco.

```java
psd.save();
```

O arquivo `Newsample_out.psd` aparecerá no diretório que você especificou anteriormente.

## Problemas Comuns & Dicas
- **Tamanho da Paleta** – Se precisar de mais de 4 cores, basta adicioná‑las ao array `palette` (até 256).  
- **Permissões de Arquivo** – Garanta que o processo Java tenha permissão de escrita em `dataDir`.  
- **Modo de Cor Incorreto** – Esquecer `createOptions.setColorMode(ColorModes.Indexed)` resultará em um PSD RGB ao invés de um indexado.  

## Perguntas Frequentes

**Q: O que é Aspose.PSD para Java?**  
A: Aspose.PSD para Java é uma biblioteca que permite a manipulação de arquivos PSD (Photoshop) programaticamente usando Java.

**Q: Posso usar o Aspose.PSD gratuitamente?**  
A: Sim, você pode acessar uma versão de avaliação gratuita do Aspose.PSD **[aqui](https://release.aspose.com/)**.

**Q: Preciso ter o Photoshop instalado para trabalhar com Aspose.PSD?**  
A: Não, você pode criar e manipular arquivos PSD sem o Photoshop, pois o Aspose.PSD lida com todas as operações de forma independente.

**Q: Como obtenho uma licença temporária para Aspose.PSD?**  
A: Você pode solicitar uma licença temporária **[aqui](https://purchase.aspose.com/temporary-license/)**.

**Q: Onde posso obter suporte para Aspose.PSD?**  
A: Você pode obter suporte no fórum da Aspose **[aqui](https://forum.aspose.com/c/psd/34)**.

## Conclusão
Você acabou de aprender **como criar PSD** com modo de cor indexado, gerar uma paleta personalizada e adicionar gráficos simples — tudo usando Aspose.PSD para Java. Com esses blocos de construção, você pode expandir para desenhos mais complexos, gerenciamento de camadas e processamento em lote. Para uma exploração mais profunda, consulte a referência oficial da API **[aqui](https://reference.aspose.com/psd/java/)** e continue experimentando diferentes paletas e primitivas de desenho.

---

**Última atualização:** 2026-03-15  
**Testado com:** Aspose.PSD para Java 24.12 (mais recente)  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}