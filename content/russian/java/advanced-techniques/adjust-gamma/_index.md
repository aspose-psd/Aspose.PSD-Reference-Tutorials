---
title: Настройте гамму изображения с помощью Aspose.PSD для Java
linktitle: Настройка гаммы изображения
second_title: Aspose.PSD Java API
description: Научитесь легко настраивать гамму изображения с помощью Aspose.PSD для Java. Следуйте нашему пошаговому руководству для достижения оптимальных результатов.
type: docs
weight: 23
url: /ru/java/advanced-techniques/adjust-gamma/
---
## Введение

В области обработки изображений настройка гаммы изображения является важным шагом для повышения его визуальной привлекательности. Aspose.PSD для Java предлагает мощное решение для разработчиков Java, позволяющее легко манипулировать гаммой изображений. В этом уроке мы рассмотрим, как настроить гамму с помощью Aspose.PSD, разбив каждый шаг, чтобы обеспечить плавную реализацию.

## Предварительные условия

Прежде чем приступить к изучению руководства, убедитесь, что у вас настроены следующие предварительные условия:

1. Среда разработки Java: убедитесь, что в вашей системе установлена среда разработки Java.
2.  Библиотека Aspose.PSD: загрузите и интегрируйте библиотеку Aspose.PSD в свой Java-проект. Необходимые ресурсы вы можете найти в[документация](https://reference.aspose.com/psd/java/).
3. Образец изображения: подготовьте образец PSD-изображения, которое вы будете использовать для применения настройки гаммы.

## Импортировать пакеты

Чтобы начать процесс, импортируйте необходимые пакеты в свой Java-проект. Это создает основу для беспрепятственного использования функций Aspose.PSD.

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.psd.fileformats.tiff.enums.TiffPhotometrics;
import com.aspose.psd.imageoptions.TiffOptions;
```

## Шаг 1. Загрузите изображение.

 Начните с загрузки образца PSD-изображения в экземпляр`RasterImage` класс. Это основа для последующих корректировок гаммы.

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

// Загрузите существующее изображение в экземпляр класса RasterImage.
Image image = Image.load(sourceFile);

// Приведение объекта изображения к RasterImage
RasterImage rasterImage = (RasterImage)image;

// Проверьте, кэшируется ли RasterImage для повышения производительности.
if (!rasterImage.isCached()) {
    rasterImage.cacheData();
}
```

## Шаг 2. Отрегулируйте гамму

 Теперь отрегулируйте гамму загруженного изображения с помощью`adjustGamma` метод. Точная настройка значений гаммы в соответствии с вашими требованиями.

```java
// Отрегулируйте гамму
rasterImage.adjustGamma(2.2f, 2.2f, 2.2f);
```

## Шаг 3: Создайте TiffOptions

 Создайте экземпляр`TiffOptions` для полученного изображения. Установите различные свойства, такие как количество битов на образец и параметры фотометрии, чтобы адаптировать выходные данные в соответствии с вашими требованиями.

```java
// Создайте экземпляр TiffOptions для полученного изображения.
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
int[] ushort = { 8, 8, 8 };
tiffOptions.setBitsPerSample(ushort);
tiffOptions.setPhotometric(TiffPhotometrics.Rgb);
```

## Шаг 4. Сохраните полученное изображение.

 Сохраните обработанное изображение в формате TIFF, используя ранее определенный`TiffOptions`.

```java
// Сохраните полученное изображение в формате TIFF.
String destName = dataDir + "AdjustGamma_out.tiff";
rasterImage.save(destName, tiffOptions);
```

## Заключение

Поздравляем! Вы успешно настроили гамму изображения с помощью Aspose.PSD для Java. Этот процесс позволяет разработчикам без особых усилий повысить качество изображения, способствуя визуальному удобству взаимодействия с пользователем.

## Часто задаваемые вопросы

### Вопрос 1: Где я могу найти документацию Aspose.PSD?

 A1: Вы можете получить доступ к документации по адресу[https://reference.aspose.com/psd/java/](https://reference.aspose.com/psd/java/).

### Вопрос 2: Как загрузить Aspose.PSD для Java?

 A2: Загрузите библиотеку с[https://releases.aspose.com/psd/java/](https://releases.aspose.com/psd/java/).

### В3: Где я могу приобрести Aspose.PSD?

 А3: Посетите[https://purchase.aspose.com/buy](https://purchase.aspose.com/buy) приобрести Aspose.PSD.

### В4: Доступна ли бесплатная пробная версия?

 О4: Да, вы можете воспользоваться бесплатной пробной версией на сайте[https://releases.aspose.com/](https://releases.aspose.com/).

### В5: Где я могу получить поддержку для Aspose.PSD?

 A5: Для получения поддержки посетите форум Aspose.PSD по адресу:[https://forum.aspose.com/c/psd/34](https://forum.aspose.com/c/psd/34).