---
title: Поворот изображения в Aspose.PSD для .NET
linktitle: Поворот изображения
second_title: Aspose.PSD .NET API
description: Научитесь легко поворачивать изображения в .NET с помощью Aspose.PSD. Следуйте нашему пошаговому руководству.
weight: 15
url: /ru/net/image-manipulation/rotate-image/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Поворот изображения в Aspose.PSD для .NET

## Введение

Если вы погружаетесь в мир манипулирования изображениями с помощью .NET, Aspose.PSD — ваш идеальный инструмент для плавной и эффективной обработки изображений. В этом уроке мы сосредоточимся на фундаментальной задаче — повороте изображения с помощью Aspose.PSD для .NET. Следуйте инструкциям, которые разобьют процесс на простые и действенные шаги.

## Предварительные условия

Прежде чем мы начнем, убедитесь, что у вас есть следующие предварительные условия:

-  Aspose.PSD для библиотеки .NET: загрузите и установите библиотеку из[Документация Aspose.PSD .NET](https://reference.aspose.com/psd/net/).

- Каталог ваших документов: настройте каталог, в котором будут храниться ваши изображения. Замените «Каталог ваших документов» во фрагменте кода на путь к этому каталогу.

## Импортировать пространства имен

Обязательно включите необходимые пространства имен для доступа к функциям Aspose.PSD. Добавьте следующие строки в начало вашего .NET-проекта:

```csharp
using Aspose.PSD.ImageOptions;
```

## Шаг 1. Загрузите изображение

```csharp
string sourceFile = dataDir + @"sample.psd";

// Загрузите существующее изображение в экземпляр класса RasterImage.
using (Image image = Image.Load(sourceFile))
{
```

## Шаг 2. Поверните изображение

```csharp
    // Поворот изображения на 270 градусов по часовой стрелке
    image.RotateFlip(RotateFlipType.Rotate270FlipNone);
```

## Шаг 3. Сохраните повернутое изображение

```csharp
    // Сохраните повернутое изображение в формате JPEG.
    string destName = dataDir + @"RotatingAnImage_out.jpg";
    image.Save(destName, new JpegOptions());
}
```

Вот и все! С помощью всего лишь нескольких строк кода вы успешно повернули изображение с помощью Aspose.PSD для .NET.

## Заключение

В этом уроке мы изучили основы вращения изображений с помощью Aspose.PSD для .NET. Aspose.PSD предоставляет надежный набор инструментов для манипулирования изображениями, что делает его незаменимой библиотекой для разработчиков .NET. Поэкспериментируйте с различными поворотами и изучите дополнительные возможности для улучшения рабочих процессов обработки изображений.

## Часто задаваемые вопросы

### Вопрос 1: Могу ли я повернуть изображения на нужный угол с помощью Aspose.PSD?

 Да, Aspose.PSD позволяет вам указать собственный угол поворота. Просто замените`RotateFlipType.Rotate270FlipNone` линия с желаемым углом поворота.

### Вопрос 2: Совместим ли Aspose.PSD с различными форматами изображений?

 Абсолютно. Aspose.PSD поддерживает широкий спектр форматов изображений, включая PSD, JPEG, PNG и другие. Проверьте[документация](https://reference.aspose.com/psd/net/) для полного списка.

### В3: Как я могу получить временную лицензию на Aspose.PSD?

 Посетите[страница временной лицензии](https://purchase.aspose.com/temporary-license/) на веб-сайте Aspose, чтобы получить временную лицензию для ознакомительных целей.

### Вопрос 4: Где я могу найти поддержку Aspose.PSD?

 По любым вопросам или помощи посетите[Форум Aspose.PSD](https://forum.aspose.com/c/psd/34) и связаться с сообществом.

### В5: Могу ли я приобрести Aspose.PSD для коммерческого использования?

 Конечно. Исследуйте[страница покупки](https://purchase.aspose.com/buy) приобрести лицензию, соответствующую вашим потребностям.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
