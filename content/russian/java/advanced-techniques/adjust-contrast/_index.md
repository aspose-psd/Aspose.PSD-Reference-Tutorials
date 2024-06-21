---
title: Отрегулируйте контрастность изображения с помощью Aspose.PSD для Java
linktitle: Настройка контрастности изображения
second_title: Aspose.PSD Java API
description: Исследуйте мир настройки контрастности изображений в Java с помощью Aspose.PSD. Следуйте нашему пошаговому руководству, чтобы без проблем манипулировать изображениями.
type: docs
weight: 22
url: /ru/java/advanced-techniques/adjust-contrast/
---
## Введение

В области обработки изображений с помощью Java Aspose.PSD выделяется как мощный инструмент. Среди множества функций частым требованием является настройка контрастности изображения. Это руководство проведет вас через процесс настройки контрастности изображения с помощью Aspose.PSD для Java. Независимо от того, являетесь ли вы опытным разработчиком или только начинаете, это руководство поможет вам освоить этот важный аспект манипулирования изображениями.

## Предварительные условия

Прежде чем приступить к изучению руководства, убедитесь, что у вас есть следующие предварительные условия:

- Базовое понимание программирования на Java.
-  Установлена библиотека Aspose.PSD для Java. Вы можете скачать его[здесь](https://releases.aspose.com/psd/java/).

## Импортировать пакеты

Для начала вам необходимо импортировать необходимые пакеты в ваш Java-проект. Добавьте в свой код следующие строки:

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.psd.fileformats.tiff.enums.TiffPhotometrics;
import com.aspose.psd.imageoptions.TiffOptions;
```

## Шаг 1. Загрузите изображение.

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

// Загрузите существующее изображение в экземпляр класса RasterImage.
Image image = Image.load(sourceFile);
```

 На этом этапе мы загружаем образец изображения («sample.psd»), используя`Image.load` метод.

## Шаг 2. Преобразование в RasterImage и кэширование данных

```java
// Приведение объекта изображения к RasterImage
RasterImage rasterImage = (RasterImage)image;

// Проверьте, кэшируется ли RasterImage, и кэшируйте RasterImage для повышения производительности.
if (!rasterImage.isCached()) {
    rasterImage.cacheData();
}
```

 Здесь мы приводим общий`Image` возражать против`RasterImage` для конкретной обработки. Кэширование данных изображения повышает производительность.

## Шаг 3. Отрегулируйте контраст.

```java
// Отрегулируйте контраст
rasterImage.adjustContrast(50);
```

`adjustContrast`Метод используется для изменения контрастности изображения. В этом примере контраст увеличен на 50%.

## Шаг 4. Создайте TiffOptions и сохраните

```java
// Создайте экземпляр TiffOptions для полученного изображения.
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
int[] ushort = { 8, 8, 8 };
tiffOptions.setBitsPerSample(ushort);
tiffOptions.setPhotometric(TiffPhotometrics.Rgb);

// Сохраните полученное изображение в формате TIFF.
String destName = dataDir + "AdjustContrast_out.tiff";
rasterImage.save(destName, tiffOptions);
```

 Здесь мы установили`TiffOptions` для выходного изображения, указав формат и другие свойства. Окончательное изображение затем сохраняется в файл TIFF.

## Заключение

Поздравляем! Вы успешно отрегулировали контрастность изображения с помощью Aspose.PSD для Java. В этом руководстве описаны основные шаги: от импорта пакетов до сохранения обработанного изображения.

## Часто задаваемые вопросы

### Вопрос 1: Совместим ли Aspose.PSD с различными форматами изображений?

О1: Да, Aspose.PSD поддерживает различные форматы изображений, обеспечивая гибкость в ваших проектах.

### В2: Как я могу получить временную лицензию на Aspose.PSD?

 A2: Вы можете получить временную лицензию[здесь](https://purchase.aspose.com/temporary-license/).

### Вопрос 3: Где я могу найти документацию Aspose.PSD?

A3: документация доступна.[здесь](https://reference.aspose.com/psd/java/).

### Вопрос 4: Какие варианты поддержки доступны для Aspose.PSD?

 A4: Для получения поддержки посетите[Форум Aspose.PSD](https://forum.aspose.com/c/psd/34).

### В5: Могу ли я приобрести Aspose.PSD?

 О5: Да, вы можете купить Aspose.PSD.[здесь](https://purchase.aspose.com/buy).