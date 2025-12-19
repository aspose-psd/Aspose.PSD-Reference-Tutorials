---
date: 2025-12-19
description: Узнайте, как регулировать яркость изображения с помощью Aspose.PSD для
  Java. Этот учебник по работе с изображениями на Java предоставляет пошаговое руководство.
linktitle: Adjust Brightness of an Image
second_title: Aspose.PSD Java API
title: Как отрегулировать яркость изображения с помощью Aspose.PSD для Java
url: /ru/java/advanced-techniques/adjust-brightness/
weight: 21
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Регулировка яркости изображения с помощью Aspose.PSD for Java

## Introduction

Если вам нужно **узнать, как регулировать яркость** изображения напрямую из кода Java, вы попали в нужное место. Регулировка яркости — частая задача для графических дизайнеров, фотографов и всех, кто создает конвейеры обработки изображений. В этом **java image manipulation tutorial** мы пройдем полный рабочий процесс — загрузка PSD/TIFF, применение смещения яркости и сохранение результата — используя библиотеку Aspose.PSD for Java.

## Quick Answers
- **Какая библиотека обрабатывает яркость?** Aspose.PSD for Java  
- **Какой метод изменяет яркость?** `RasterImage.adjustBrightness()`  
- **Можно ли работать с файлами PSD и TIFF?** Да, API поддерживает оба формата.  
- **Нужна ли лицензия для продакшна?** Требуется коммерческая лицензия для использования не в режиме оценки.  
- **Сколько времени занимает реализация?** Обычно менее 10 минут для базовой регулировки.

## What is Image Brightness Adjustment?

Регулировка яркости изображения изменяет общую светлоту каждого пикселя в изображении. Увеличение яркости делает темные области светлее, а уменьшение затемняет всю картинку. Эта операция полезна для коррекции недоэкспонированных фотографий, подготовки материалов к печати или создания визуальных эффектов в приложениях.

## Why Use Aspose.PSD for Java?

- **Полная поддержка форматов** – PSD, TIFF, JPEG, PNG и др.  
- **Отсутствие внешних нативных зависимостей** – чистый Java, легко интегрировать.  
- **Высокопроизводительное кэширование** – растровые данные могут кэшироваться для более быстрых повторных операций.  
- **Богатый API** – методы для коррекции цвета, слоев, масок и других продвинутых правок.

## Prerequisites

Перед тем как приступить к уроку, убедитесь, что у вас есть следующие предварительные требования:

- Aspose.PSD for Java Library: Download and install the library from the [Aspose.PSD for Java documentation](https://reference.aspose.com/psd/java/).

## Import Packages

Чтобы начать, импортируйте необходимые пакеты в ваш проект Java. В этом примере мы будем использовать следующее:

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.psd.fileformats.tiff.enums.TiffPhotometrics;
import com.aspose.psd.imageoptions.TiffOptions;
```

Теперь разберём процесс регулировки яркости изображения на простые шаги:

## How to Adjust Brightness Using Aspose.PSD

### Step 1: Load the Image

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";
String destName = dataDir + "AdjustBrightness_out.tiff";

// Load an existing image into an instance of RasterImage class
Image image = Image.load(sourceFile);
// Cast object of Image to RasterImage
RasterImage rasterImage = (RasterImage) image;

// Check if RasterImage is cached and Cache RasterImage for better performance
if (!rasterImage.isCached()) {
    rasterImage.cacheData();
}
```

На этом шаге мы загружаем целевое изображение и приводим его к типу `RasterImage` для дальнейшей обработки.

### Step 2: Adjust Brightness

```java
// Adjust the brightness
rasterImage.adjustBrightness(-50);
```

Здесь мы используем метод `adjustBrightness` для изменения яркости изображения. В этом примере мы уменьшаем яркость на 50 единиц, но вы можете настроить это значение в соответствии с вашими требованиями.

### Step 3: Set TiffOptions

```java
int[] ushort = {8, 8, 8};
// Create an instance of TiffOptions for the resultant image
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
tiffOptions.setBitsPerSample(ushort);
tiffOptions.setPhotometric(TiffPhotometrics.Rgb);
```

Настраиваем `TiffOptions` для сохранения отрегулированного изображения. Отрегулируйте свойства `bitsPerSample` и `photometric` в зависимости от ваших конкретных потребностей.

### Step 4: Save the Resultant Image

```java
// Save the resultant image
rasterImage.save(destName, tiffOptions);
```

Наконец, сохраняем изменённое изображение, используя указанные `TiffOptions`.

## Common Issues and Solutions

| Issue | Reason | Solution |
|-------|--------|----------|
| **`ClassCastException` when casting Image** | Файл не является растровым изображением (например, векторный PSD). | Проверьте формат исходного файла или используйте `image instanceof RasterImage` перед приведением типа. |
| **Brightness change has no effect** | Изображение не было закешировано перед изменением. | Вызовите `rasterImage.cacheData()` как показано в Шаге 1. |
| **Saved file appears corrupted** | Неправильная конфигурация `TiffOptions`. | Убедитесь, что `bitsPerSample` соответствует глубине исходного изображения (обычно 8‑бит на канал). |

## Frequently Asked Questions

### Q1: Можно ли регулировать яркость в других форматах изображений, кроме PSD?

A1: Да, Aspose.PSD for Java поддерживает различные форматы изображений, такие как JPEG, PNG и TIFF.

### Q2: Как обрабатывать ошибки во время процесса регулировки изображения?

A2: Вы можете реализовать обработку ошибок с помощью блоков try‑catch для управления возникающими исключениями.

### Q3: Есть ли ограничение диапазона регулировки яркости?

A3: Диапазон регулировки зависит от содержимого и формата изображения, но Aspose.PSD предоставляет гибкость в настройке.

### Q4: Можно ли использовать Aspose.PSD for Java в коммерческих проектах?

A4: Да, Aspose.PSD for Java — коммерческая библиотека, и вы можете получить лицензию по ссылке [here](https://purchase.aspose.com/buy).

### Q5: Доступна ли бесплатная пробная версия Aspose.PSD for Java?

A5: Да, вы можете ознакомиться с библиотекой, используя бесплатную пробную версию по ссылке [here](https://releases.aspose.com/).

### Q6: Влияет ли метод `adjustBrightness` на видимость слоёв?

A6: Метод работает с растровым составным изображением, поэтому видимость слоёв учитывается при растеризации.

### Q7: Можно ли последовательно применять несколько регулировок (например, контраст, насыщенность)?

A7: Конечно. После регулировки яркости вы можете вызвать `adjustContrast`, `adjustSaturation` и т.д. на том же экземпляре `RasterImage`.

---

**Последнее обновление:** 2025-12-19  
**Тестировано с:** Aspose.PSD for Java 24.12 (latest at time of writing)  
**Автор:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}