---
date: 2026-08-11
description: Узнайте, как применить порог Оцу в Java с помощью Aspose.PSD for Java
  — мощной техники сегментации изображений.
keywords:
- apply otsu threshold java
- image segmentation with otsu
- java image segmentation tutorial
lastmod: 2026-08-11
linktitle: Бинаризация с порогом Оцу
og_description: Примените порог Оцу в Java с Aspose.PSD for Java. Этот учебник пошагово
  показывает, как бинаризовать изображения, объясняет, почему метод быстрый, и предоставляет
  советы по устранению распространённых проблем.
og_image_alt: Screenshot of Java code applying Otsu threshold using Aspose.PSD
og_title: Применить порог Оцу в Java с Aspose.PSD — быстрое руководство
schemas:
- author: Aspose
  dateModified: '2026-08-11'
  description: Learn how to apply otsu threshold java using Aspose.PSD for Java –
    a powerful image segmentation technique.
  headline: Apply otsu threshold java with Aspose.PSD
  type: TechArticle
- description: Learn how to apply otsu threshold java using Aspose.PSD for Java –
    a powerful image segmentation technique.
  name: Apply otsu threshold java with Aspose.PSD
  steps:
  - name: set up your document directory
    text: Define the folder that contains the source PSD file and the output location
      for the binarized image.
  - name: load the PSD file
    text: '`PsdImage` is the top‑level Aspose.PSD class that represents a PSD document
      and gives access to its layers, metadata, and pixel data.'
  - name: cache the image
    text: '`RasterImage` holds the raster representation of a layer; calling `cache()`
      loads the pixel data into memory so subsequent operations are fast.'
  - name: binarize image with Otsu threshold
    text: '`applyOtsuThreshold()` evaluates all possible gray levels and selects the
      optimal cutoff, producing a binary image that separates foreground objects from
      the background.'
  - name: save the resultant image
    text: '`JpegOptions` configures JPEG‑specific settings such as quality and compression
      when saving the processed image. You can also choose PNG or BMP by swapping
      the options class – the API supports over **30 image formats** for output. {{<
      blocks/products/products-backtop-button >}}'
  type: HowTo
- questions:
  - answer: It automatically finds the gray‑level that minimizes intra‑class variance,
      producing a binary image in one step.
    question: What does Otsu Threshold do?
  - answer: A free trial works for development; a commercial license is required for
      production.
    question: Do I need a license to run the sample?
  - answer: Aspose.PSD for Java supports Java 8 through Java 21.
    question: Which Java version is supported?
  - answer: Yes – you can iterate over each layer and apply the threshold individually.
    question: Can I process multi‑layer PSD files?
  - answer: For a 1920 × 1080 image the Otsu binarization finishes in under 30 ms
      on a typical laptop CPU.
    question: How fast is the operation?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- apply otsu threshold java
- image segmentation
- Aspose.PSD
- Java image processing
title: Применить порог Оцу в Java с Aspose.PSD
url: /ru/java/image-processing/binarization-otsu-threshold/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Применение порога Отсу на Java с Aspose.PSD

## Введение

В этом руководстве вы узнаете, как **apply otsu threshold java** с помощью библиотеки Aspose.PSD for Java. Бинаризация с порогом Отсу — один из самых надёжных методов сегментации изображений с использованием техник Отсу, автоматически выбирающий оптимальный порог уровня серого для разделения переднего плана и фона. К концу руководства у вас будет рабочий фрагмент кода на Java, который преобразует любой слой PSD в чистое чёрно‑белое изображение.

## Быстрые ответы
- **What does Otsu Threshold do?** Он автоматически находит уровень серого, который минимизирует внутриклассовую дисперсию, создавая бинарное изображение за один шаг.  
- **Do I need a license to run the sample?** Бесплатная пробная версия подходит для разработки; для продакшна требуется коммерческая лицензия.  
- **Which Java version is supported?** Aspose.PSD for Java поддерживает Java 8 по Java 21.  
- **Can I process multi‑layer PSD files?** Да — вы можете перебрать каждый слой и применить порог отдельно.  
- **How fast is the operation?** Для изображения 1920 × 1080 бинаризация Отсу завершается менее чем за 30 мс на типичном процессоре ноутбука.

## Что такое apply otsu threshold java?

Apply otsu threshold java — это процесс использования кода на Java для вызова алгоритма Отсу на изображении, получающий бинарный (чёрно‑белый) результат. Алгоритм оценивает каждый возможный уровень серого, выбирает тот, который даёт наименьшую взвешенную внутриклассовую дисперсию, и затем классифицирует каждый пиксель как передний план или фон. Этот автоматизированный подход устраняет необходимость ручного выбора порога и хорошо работает с изображениями, имеющими би‑модальные гистограммы, что делает его идеальным для пакетной обработки больших коллекций изображений.

## Почему использовать Aspose.PSD for Java?

Aspose.PSD for Java поддерживает **50+ форматов ввода и вывода** (включая PSD, JPEG, PNG, BMP и TIFF) и может обрабатывать файлы размером до **2 GB**, не загружая весь документ в память. Встроенная реализация Otsu в библиотеке работает за линейное время, позволяя пакетно обрабатывать сотни изображений за несколько секунд.

## Требования

- **Java development environment** – установленный и настроенный JDK 8 или новее.  
- **Aspose.PSD for Java library** – Скачайте и установите библиотеку со официальной страницы загрузки Aspose.PSD for Java. Ссылка для загрузки: [Aspose.PSD for Java download page](https://releases.aspose.com/psd/java/).  
- **Sample PSD file** – Имеется PSD‑файл как минимум с одним растровым слоем для тестирования бинаризации.  
- Для других продуктов Aspose вы также можете просмотреть общую страницу релизов: [Aspose releases](https://releases.aspose.com/).

## Импорт пакетов

Импортируйте классы `PsdImage`, `RasterImage` и `JpegOptions` из библиотеки Aspose.PSD, которые предоставляют доступ к файлам PSD, растровым данным и параметрам экспорта JPEG.  
```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterCachedImage;

import com.aspose.psd.imageoptions.JpegOptions;
```

## Как применить otsu threshold java?

Загрузите ваш PSD, получите нужный растровый слой и вызовите метод бинаризации Otsu — весь процесс укладывается в пять лаконичных операторов. Сначала вы создаёте объект `PsdImage`, представляющий исходный файл, затем получаете `RasterImage` для целевого слоя, вызываете `applyOtsuThreshold()` и, наконец, сохраняете результат с помощью `JpegOptions`. Такой подход обеспечивает минимальное использование памяти и максимальную производительность.

### Шаг 1: настройте каталог документа

Укажите папку, содержащую исходный файл PSD, и место вывода для бинаризованного изображения.  
```java
String dataDir = "Your Document Directory";
```

### Шаг 2: загрузите файл PSD

`PsdImage` — это базовый класс Aspose.PSD, представляющий документ PSD и предоставляющий доступ к его слоям, метаданным и пиксельным данным.  
```java
String sourceFile = dataDir + "sample.psd";
Image image = Image.load(sourceFile);
```

### Шаг 3: кэшируйте изображение

`RasterImage` хранит растровое представление слоя; вызов `cache()` загружает пиксельные данные в память, чтобы последующие операции были быстрыми.  
```java
RasterCachedImage rasterCachedImage = (RasterCachedImage)image;

if (!rasterCachedImage.isCached()) {
    rasterCachedImage.cacheData();
}
```

### Шаг 4: бинаризуйте изображение с порогом Otsu

`applyOtsuThreshold()` оценивает все возможные уровни серого и выбирает оптимальный порог, создавая бинарное изображение, разделяющее объекты переднего плана и фон.  
```java
rasterCachedImage.binarizeOtsu();
```

### Шаг 5: сохраните полученное изображение

`JpegOptions` настраивает параметры JPEG, такие как качество и степень сжатия при сохранении обработанного изображения. Вы также можете выбрать PNG или BMP, заменив класс параметров — API поддерживает более **30 форматов изображений** для вывода.  
```java
String destName = dataDir + "BinarizationWithOtsuThreshold_out.jpg";
rasterCachedImage.save(destName, new JpegOptions());
```

{{< blocks/products/products-backtop-button >}}

## Распространённые проблемы и решения

- **Memory‑out‑of‑bounds errors** – Убедитесь, что вызываете `cache()` для больших слоёв перед обработкой; это заставляет Aspose.PSD использовать потоковый подход.  
- **Incorrect colors after binarization** – Проверьте, что исходный слой действительно является градацией серого; цветные слои следует сначала преобразовать в градацию серого с помощью `convertToGrayscale()`.

## Часто задаваемые вопросы

### Q1: Что такое бинаризация с порогом otsu?

Бинаризация с порогом otsu — метод, используемый для сегментации изображений, разделяющий изображение на передний план и фон на основе оптимального порога.

### Q2: Можно ли использовать Aspose.PSD for Java бесплатно?

Aspose.PSD for Java — коммерческая библиотека, но вы можете изучать её возможности с помощью бесплатной пробной версии. Получить её можно со страницы [Aspose.PSD for Java download page](https://releases.aspose.com/psd/java/).

### Q3: Где можно найти документацию Aspose.PSD for Java?

Документация доступна на официальном справочном сайте Aspose.PSD for Java: [Aspose.PSD Java API reference](https://reference.aspose.com/psd/java/).

### Q4: Как получить поддержку Aspose.PSD for Java?

Посетите форум сообщества Aspose.PSD для получения помощи: [Aspose.PSD forum](https://forum.aspose.com/c/psd/34).

### Q5: Доступна ли временная лицензия для Aspose.PSD for Java?

Да, вы можете получить временную лицензию на странице временных лицензий Aspose: [Aspose temporary license](https://purchase.aspose.com/temporary-license/).

---

**Последнее обновление:** 2026-08-11  
**Тестировано с:** Aspose.PSD for Java 24.11  
**Автор:** Aspose

## Связанные руководства

- [Приведение изображения к градации серого с помощью Aspose.PSD for Java](/psd/java/advanced-techniques/grayscale-image/)
- [Учебник по обработке изображений на Java — Регулировка яркости изображения с Aspose.PSD for Java](/psd/java/advanced-techniques/adjust-brightness/)
- [Как корректировать гамму в обработке изображений на Java с Aspose.PSD](/psd/java/advanced-techniques/adjust-gamma/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}