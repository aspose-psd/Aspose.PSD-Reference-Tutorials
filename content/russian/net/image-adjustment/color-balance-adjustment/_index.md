---
title: Применение настройки цветового баланса в Aspose.PSD для .NET
linktitle: Применение настройки цветового баланса
second_title: Aspose.PSD .NET API
description: Улучшайте цвета PSD-изображений без особых усилий с помощью функции регулировки цветового баланса Aspose.PSD for .NET. Следуйте нашему пошаговому руководству, чтобы получить потрясающие результаты.
type: docs
weight: 14
url: /ru/net/image-adjustment/color-balance-adjustment/
---
## Введение

Добро пожаловать в это подробное руководство по применению настройки цветового баланса в Aspose.PSD для .NET! Aspose.PSD — это мощная библиотека .NET, которая позволяет разработчикам эффективно работать с файлами PSD. В этом уроке мы сосредоточимся на функции регулировки цветового баланса, которая позволит вам легко улучшить цветовой баланс ваших PSD-изображений.

## Предварительные условия

Прежде чем мы углубимся в руководство, убедитесь, что у вас есть следующие предварительные условия:

-  Aspose.PSD для библиотеки .NET: загрузите и установите библиотеку из[Сайт Aspose.PSD](https://releases.aspose.com/psd/net/).
- Среда разработки: убедитесь, что на вашем компьютере установлена работающая среда разработки .NET.
- PSD-файл: подготовьте PSD-файл, к которому вы хотите применить коррекцию цветового баланса.

## Импортировать пространства имен

В свой проект .NET включите необходимые пространства имен для использования функций Aspose.PSD. Добавьте в свой код следующие строки:

```csharp
using Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers;
```

Теперь давайте разобьем процесс настройки цветового баланса на несколько этапов:

## Шаг 1. Загрузите PSD-файл

```csharp
string dataDir = "Your Document Directory";
var filePath = dataDir + "ColorBalance.psd";
var outputPath = dataDir + "ColorBalance_out.psd";

using (var im = (FileFormats.Psd.PsdImage)Image.Load(filePath))
{
    // Код для настройки цветового баланса будет добавлен на следующих этапах.
}
```

## Шаг 2. Доступ и настройка цветового баланса

```csharp
foreach (var layer in im.Layers)
{
    var cbLayer = layer as ColorBalanceAdjustmentLayer;
    if (cbLayer != null)
    {
        cbLayer.ShadowsCyanRedBalance = 30;
        cbLayer.ShadowsMagentaGreenBalance = -15;
        cbLayer.ShadowsYellowBlueBalance = 40;
        cbLayer.MidtonesCyanRedBalance = -90;
        cbLayer.MidtonesMagentaGreenBalance = -25;
        cbLayer.MidtonesYellowBlueBalance = 20;
        cbLayer.HighlightsCyanRedBalance = -30;
        cbLayer.HighlightsMagentaGreenBalance = 67;
        cbLayer.HighlightsYellowBlueBalance = -95;
        cbLayer.PreserveLuminosity = true;
    }
}
```

## Шаг 3. Сохраните откорректированное изображение.

```csharp
im.Save(outputPath);
```

Теперь вы успешно применили настройку цветового баланса к своему PSD-файлу с помощью Aspose.PSD для .NET!

## Заключение

Поздравляем! Вы узнали, как улучшить цветовой баланс ваших PSD-изображений с помощью Aspose.PSD для .NET. Поэкспериментируйте с различными значениями баланса, чтобы добиться желаемых визуальных эффектов.

## Часто задаваемые вопросы

### Вопрос 1. Могу ли я применить настройку цветового баланса к нескольким слоям?

О1: Да, вы можете перебирать все слои вашего PSD-файла и при необходимости корректировать цветовой баланс.

### Вопрос 2: Подходит ли Aspose.PSD для .NET для пакетной обработки PSD-файлов?

А2: Абсолютно! Aspose.PSD предоставляет эффективные возможности пакетной обработки файлов PSD.

### В3: Как я могу получить временную лицензию на Aspose.PSD для .NET?

 А3: Посетите[Временная лицензия Aspose.PSD](https://purchase.aspose.com/temporary-license/) на временную лицензию.

### Вопрос 4. Где я могу найти дополнительные примеры и документацию?

 А4: Исследуйте[Документация Aspose.PSD](https://reference.aspose.com/psd/net/) подробные примеры и руководства.

### Вопрос 5: Какие варианты поддержки доступны для Aspose.PSD для .NET?

 A5: Посетите[Форум Aspose.PSD](https://forum.aspose.com/c/psd/34) за поддержку сообщества и обсуждения.
