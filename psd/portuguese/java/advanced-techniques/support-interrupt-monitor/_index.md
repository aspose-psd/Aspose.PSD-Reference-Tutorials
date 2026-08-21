---
date: 2026-06-08
description: Aprenda como salvar PSD como PNG usando Aspose.PSD para Java e interromper
  a conversão quando necessário. Gerencie o fluxo de trabalho de imagens de forma
  eficiente.
keywords:
- save psd as png
- how to interrupt conversion
- psd to png conversion
- manage image workflow
linktitle: Suporte ao Interrupt Monitor
schemas:
- author: Aspose
  dateModified: '2026-06-08'
  description: Learn how to save PSD as PNG using Aspose.PSD for Java and interrupt
    conversion when needed. Manage image workflow efficiently.
  headline: How to Save PSD as PNG with Interrupt Monitor in Aspose.PSD for Java
  type: TechArticle
- description: Learn how to save PSD as PNG using Aspose.PSD for Java and interrupt
    conversion when needed. Manage image workflow efficiently.
  name: How to Save PSD as PNG with Interrupt Monitor in Aspose.PSD for Java
  steps:
  - name: Set Your Document Directory
    text: Ensure to replace “Your Document Directory” with the actual path where your
      PSD documents are stored.
  - name: Define Image Options and Output Path
    text: Specify the image options, source PSD file, and the desired output path
      for the converted image.
  - name: Initialize Interrupt Monitor and SaveImageWorker
    text: The `InterruptMonitor` class watches a running conversion and can interrupt
      it when `requestInterrupt()` is called. Create instances of `InterruptMonitor`
      and `SaveImageWorker`, linking the monitor to the image conversion worker.
  - name: Start Image Conversion Thread
    text: Initiate a new thread for the image conversion process and introduce a timeout
      period to anticipate interruption.
  - name: Interrupt the Process
    text: Calling `monitor.requestInterrupt()` signals the monitor to abort the ongoing
      conversion. Interrupt the image conversion process using the `InterruptMonitor`
      and wait for the interruption to complete. Finally, clean up by deleting the
      output file.
  type: HowTo
- questions:
  - answer: Yes, use `InterruptMonitor` to stop the process on demand.
    question: Can I interrupt a PSD‑to‑PNG conversion?
  - answer: Call `save(outputPath, new PngOptions())`.
    question: Which method saves a PSD as PNG?
  - answer: A commercial license is required; a free trial is available.
    question: Do I need a license for production?
  - answer: Java 8 and later are fully supported.
    question: What Java version is supported?
  - answer: Conversions can run in separate threads; the monitor handles interruptions
      safely.
    question: Is the library thread‑safe?
  type: FAQPage
second_title: Aspose.PSD Java API
title: Como salvar PSD como PNG com Interrupt Monitor no Aspose.PSD para Java
url: /pt/java/advanced-techniques/support-interrupt-monitor/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Salvar PSD como PNG com Monitor de Interrupção no Aspose.PSD para Java

## Introdução

Se você precisar **salvar PSD como PNG** mantendo controle total sobre conversões de longa duração, o Monitor de Interrupção do Aspose.PSD para Java oferece exatamente isso. Neste tutorial vamos percorrer a configuração do monitor, a conversão de um arquivo PSD para PNG e a interrupção segura da operação quando necessário. Você também verá como isso se encaixa em um fluxo de trabalho típico de processamento de imagens e por que é essencial para aplicações robustas.

## Respostas Rápidas
- **Posso interromper uma conversão de PSD‑para‑PNG?** Sim, use `InterruptMonitor` para parar o processo sob demanda.  
- **Qual método salva um PSD como PNG?** Chame `save(outputPath, new PngOptions())`.  
- **Preciso de uma licença para produção?** É necessária uma licença comercial; uma avaliação gratuita está disponível.  
- **Qual versão do Java é suportada?** Java 8 e posteriores são totalmente suportados.  
- **A biblioteca é thread‑safe?** As conversões podem ser executadas em threads separadas; o monitor lida com interrupções com segurança.

## Pré-requisitos

Antes de mergulhar nas complexidades do uso do Monitor de Interrupção, certifique‑se de que você tem os seguintes pré‑requisitos em vigor:

- **Ambiente de Desenvolvimento Java:** Configure um ambiente de desenvolvimento Java em seu sistema.  
- **Biblioteca Aspose.PSD:** Obtenha a biblioteca Aspose.PSD para Java. Você pode baixá‑la [aqui](https://releases.aspose.com/psd/java/). Você também pode visitar o site principal da Aspose [aqui](https://releases.aspose.com/).  
- **Diretório de Documentos:** Tenha um diretório designado para seus documentos PSD.

## Importar Pacotes

Comece importando os pacotes necessários para o seu projeto Java. Isso garante que você tenha acesso às funcionalidades do Aspose.PSD.

```java
import com.aspose.psd.ImageOptionsBase;

import static com.aspose.psd.examples.Utils.Utils.getDateTime;
import com.aspose.psd.imageoptions.PngOptions;
import com.aspose.psd.multithreading.InterruptMonitor;
import com.aspose.psd.system.Threading.ThreadStart;
import java.io.File;
```

Agora, vamos dividir o código de exemplo em um guia passo a passo para incorporar o Monitor de Interrupção em seu projeto Aspose.PSD para Java.

## Como salvar PSD como PNG usando o Monitor de Interrupção?

`PsdImage` representa um documento PSD carregado na memória.  
`SaveImageWorker` realiza a conversão da imagem em uma thread separada.  

Carregue seu arquivo PSD com `new PsdImage("source.psd")`, anexe um `InterruptMonitor` ao `SaveImageWorker` e chame `save("output.png", new PngOptions())`. O monitor observa solicitações de cancelamento e aborta a conversão de forma limpa, devolvendo o controle à sua aplicação em milissegundos.

### Etapa 1: Defina Seu Diretório de Documentos

```java
String dataDir = "Your Document Directory";
```

Certifique‑se de substituir “Your Document Directory” pelo caminho real onde seus documentos PSD estão armazenados.

### Etapa 2: Defina as Opções de Imagem e o Caminho de Saída

```java
ImageOptionsBase saveOptions = new PngOptions();
String source = dataDir + "big2.psb";
String output = dataDir + "big_out.png";
```

Especifique as opções de imagem, o arquivo PSD de origem e o caminho de saída desejado para a imagem convertida.

### Etapa 3: Inicializar o Monitor de Interrupção e o SaveImageWorker

A classe `InterruptMonitor` observa uma conversão em execução e pode interrompê‑la quando `requestInterrupt()` é chamado.  

```java
InterruptMonitor monitor = new InterruptMonitor();
SaveImageWorker worker = new SaveImageWorker(source, output, saveOptions, monitor);
```

Crie instâncias de `InterruptMonitor` e `SaveImageWorker`, vinculando o monitor ao worker de conversão de imagem.

### Etapa 4: Iniciar a Thread de Conversão de Imagem

```java
Thread thread = new Thread(worker.ThreadProc());
try {
    thread.start();
    // Add a timeout to allow for potential interruption
    Thread.sleep(3000);
```

Inicie uma nova thread para o processo de conversão de imagem e introduza um período de timeout para antecipar a interrupção.

### Etapa 5: Interromper o Processo

Chamar `monitor.requestInterrupt()` sinaliza ao monitor que ele deve abortar a conversão em andamento.  

```java
    // Interrupt the process
    monitor.interrupt();
    System.out.println("Interrupting the save thread #" + thread.getId() + " at " + getDateTime().toString());

    // Wait for interruption...
    thread.join();
} finally {
    // Delete the output file if it exists
    File f = new File(output);
    if (f.exists()) {
        f.delete();
    }
}
```

Interrompa o processo de conversão de imagem usando o `InterruptMonitor` e aguarde a conclusão da interrupção. Por fim, limpe removendo o arquivo de saída.

## Por que usar o Monitor de Interrupção para conversão de PSD‑para‑PNG?

Aspose.PSD suporta **mais de 30 formatos de saída**, incluindo PNG, JPEG, BMP e TIFF, e pode processar arquivos de até **500 MB** sem carregar o documento inteiro na memória. Ao adicionar um monitor de interrupção você reduz o desperdício de CPU e melhora a capacidade de resposta em pipelines de processamento em lote, especialmente quando uma conversão ultrapassa os limites de tempo esperados.

## Problemas Comuns e Soluções

- **A conversão fica travada indefinidamente:** Certifique‑se de que o monitor está anexado **antes** de chamar `save`.  
- **O arquivo de saída fica corrompido após a interrupção:** O monitor aborta de forma limpa; porém, sempre verifique se o arquivo existe antes de usá‑lo.  
- **Preocupações com thread‑safety:** Execute cada conversão em sua própria thread; o monitor afeta apenas o worker associado.

## Perguntas Frequentes

**Q1: O que é um Monitor de Interrupção no Aspose.PSD para Java?**  
R: O Monitor de Interrupção permite que desenvolvedores pausem ou cancelem conversões de imagens de longa duração, oferecendo controle em tempo real sobre o uso de recursos.

**Q2: Como posso obter a biblioteca Aspose.PSD para Java?**  
R: Você pode baixar a biblioteca Aspose.PSD para Java [aqui](https://releases.aspose.com/psd/java/).

**Q3: Existe uma avaliação gratuita disponível para o Aspose.PSD para Java?**  
R: Sim, você pode explorar uma avaliação gratuita do Aspose.PSD [aqui](https://releases.aspose.com/).

**Q4: Onde posso encontrar suporte para o Aspose.PSD para Java?**  
R: Visite o fórum de suporte do Aspose.PSD para Java [aqui](https://forum.aspose.com/c/psd/34).

**Q5: Como posso comprar uma licença para o Aspose.PSD para Java?**  
R: Você pode comprar uma licença para Aspose.PSD para Java [aqui](https://purchase.aspose.com/buy).

**Q6: Posso converter vários arquivos PSD para PNG em paralelo?**  
R: Sim, crie uma thread separada para cada arquivo e anexe um `InterruptMonitor` individual a cada worker de conversão.

**Q7: A biblioteca lida com perfis de cor durante a conversão de PSD‑para‑PNG?**  
R: Absolutamente; Aspose.PSD preserva perfis ICC incorporados e os aplica ao PNG de saída automaticamente.

---

**Última atualização:** 2026-06-08  
**Testado com:** Aspose.PSD 23.12 for Java  
**Autor:** Aspose  

{{< blocks/products/products-backtop-button >}}

## Tutoriais Relacionados

- [Salvar PSD como PNG e Aplicar Sombra de Renderização no Aspose.PSD para Java](/psd/java/advanced-image-manipulation/rendering-drop-shadow/)
- [Exportar PSD para PNG e Adicionar uma Nova Camada Regular usando Aspose.PSD para Java](/psd/java/advanced-image-effects/add-new-regular-layer/)
- [Suporte ao Monitor de Interrupção em Arquivos PSD - Java](/psd/java/psd-layer-management-effects/support-interrupt-monitor-psd-files/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}