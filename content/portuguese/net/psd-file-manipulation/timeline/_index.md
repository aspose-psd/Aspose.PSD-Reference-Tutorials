---
title: Trabalhando com linha do tempo em Aspose.PSD para .NET
linktitle: Trabalhando com linha do tempo
second_title: API Aspose.PSD .NET
description: Aprimore a manipulação de imagens PSD com a classe Aspose.PSD para .NET Timeline. Controle as propriedades dos quadros, os estados das camadas e libere possibilidades criativas sem esforço.
type: docs
weight: 16
url: /pt/net/psd-file-manipulation/timeline/
---
## Introdução
No mundo dinâmico do design gráfico e da manipulação de imagens, a capacidade de controlar e manipular a linha do tempo das imagens é crucial. Aspose.PSD for .NET fornece uma solução poderosa com sua classe Timeline. Este recurso de alto nível permite que os usuários façam alterações na linha do tempo do PsdImage, como alterar o atraso do quadro, editar estados da camada em quadros específicos e muito mais.
## Pré-requisitos
Antes de mergulhar nas possibilidades interessantes que a classe Timeline oferece, certifique-se de ter os seguintes pré-requisitos em vigor:
-  Biblioteca Aspose.PSD for .NET: Certifique-se de ter a biblioteca Aspose.PSD for .NET instalada. Você pode baixá-lo no[Documentação Aspose.PSD para .NET](https://reference.aspose.com/psd/net/).
-  Diretórios de documentos e saída: defina os caminhos para seus diretórios de documentos e saída no código. Ajusta a`baseDir` e`outputDir` variáveis de acordo com a estrutura do seu projeto.
Agora, vamos explorar como utilizar a classe Timeline passo a passo.
## Importar namespaces
Para começar a trabalhar com a classe Timeline, importe os namespaces necessários em seu código:
```csharp
using System;
using System.Collections.Generic;
using System.IO;
using Aspose.PSD.FileFormats.Core.Blending;
using Aspose.PSD.FileFormats.Psd;
using Aspose.PSD.FileFormats.Psd.Layers.Animation;
```
## Etapa 1: carregar imagem PSD
Comece carregando a imagem PSD do arquivo de origem especificado. Certifique-se de que o caminho do arquivo de origem esteja definido corretamente:
```csharp
string sourceFile = Path.Combine(baseDir, "image1219.psd");
using (PsdImage psdImage = (PsdImage)Image.Load(sourceFile))
{
    //Seu código para outras operações vai aqui
}
```
## Passo 2: Acesse a Linha do Tempo
Assim que a imagem PSD for carregada, acesse a Linha do tempo usando o seguinte código:
```csharp
Timeline timeline = psdImage.Timeline;
```
## Etapa 3: alterar o método de descarte
Manipule o método de descarte de um quadro específico. Neste exemplo, alteramos o método de descarte do quadro 1:
```csharp
timeline.Frames[0].DisposalMethod = FrameDisposalMethod.DoNotDispose;
```
## Etapa 4: ajustar o atraso do quadro
Modifique o atraso de um quadro específico. Aqui, alteramos o atraso do quadro 2 para 15:
```csharp
timeline.Frames[1].Delay = 15;
```
## Etapa 5: editar o estado da camada
Altere a opacidade da 'Camada 1' em um quadro específico. Neste caso, definimos a opacidade para 50 no quadro 2:
```csharp
LayerState layerState11 = timeline.Frames[1].LayerStates[1];
layerState11.Opacity = 50;
```
## Etapa 6: mover camada
Mova a 'Camada 1' para o canto inferior esquerdo de um quadro específico (quadro 3 neste exemplo):
```csharp
LayerState layerState21 = timeline.Frames[2].LayerStates[1];
layerState21.PositionOffset = new Point(-50, 230);
```
## Etapa 7: adicionar novo quadro
Adicione um novo quadro à linha do tempo:
```csharp
List<Frame> frames = new List<Frame>(timeline.Frames);
frames.Add(new Frame());
timeline.Frames = frames.ToArray();
```
## Etapa 8: alterar o modo de mesclagem
Altere o modo de mesclagem da 'Camada 1' em um quadro específico (quadro 4 neste caso):
```csharp
LayerState layerState31 = timeline.Frames[3].LayerStates[1];
layerState31.BlendMode = BlendMode.Dissolve;
```
## Etapa 9: salvar alterações
Aplique as alterações de volta à instância PsdImage e salve a imagem PSD modificada:
```csharp
psdImage.Save(outputPsd);
```
## Etapa 10: limpeza
Por fim, limpe excluindo o arquivo de saída temporário:
```csharp
File.Delete(outputPsd);
```
## Conclusão

Concluindo, a classe Timeline no Aspose.PSD for .NET permite que os desenvolvedores tenham controle granular sobre a linha do tempo das imagens PSD. Através de uma série de etapas simples, você pode manipular propriedades de quadros, estados de camadas e muito mais, abrindo um mundo de possibilidades criativas.

## Perguntas frequentes

### Q1: O Aspose.PSD para .NET é adequado para iniciantes?

A1: Com certeza! Aspose.PSD for .NET fornece uma interface amigável e documentação abrangente, tornando-o acessível tanto para iniciantes quanto para desenvolvedores experientes.

### P2: Posso aplicar alterações na linha do tempo a imagens GIF?

A2: A classe Timeline foi projetada especificamente para imagens PSD. Para manipulação de GIF, consulte Aspose.GIF para .NET.

### P3: Onde posso encontrar suporte adicional ou discutir problemas?

 A3: Visite o[Fórum Aspose.PSD](https://forum.aspose.com/c/psd/34) para apoio da comunidade e discussões sobre questões.

### Q4: Como posso obter uma licença temporária do Aspose.PSD para .NET?

 A4: Adquira uma licença temporária[aqui](https://purchase.aspose.com/temporary-license/).

### P5: Quais são os principais benefícios de usar Aspose.PSD para .NET?

A5: Aspose.PSD para .NET oferece recursos avançados de processamento de imagem, manipulação de arquivos PSD e renderização de alto desempenho.