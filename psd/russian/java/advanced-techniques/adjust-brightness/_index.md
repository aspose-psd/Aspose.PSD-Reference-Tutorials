---
date: 2026-09-28
description: Учебник по обработке изображений на Java показывает, как регулировать
  яркость изображения с использованием Aspose.PSD for Java. Следуйте пошаговому коду
  для загрузки, изменения и сохранения файлов PSD или TIFF.
keywords:
- java image processing
- aspose psd java
- java image manipulation
- adjust brightness java
lastmod: 2026-09-28
linktitle: Регулировка яркости изображения
og_description: Учебник по обработке изображений на Java показывает, как регулировать
  яркость изображения с использованием Aspose.PSD for Java. Следуйте пошаговому коду
  для загрузки, изменения и сохранения файлов PSD или TIFF.
og_image_alt: Guide to adjusting image brightness in Java using Aspose.PSD
og_title: 'Обработка изображений на Java: регулировка яркости с помощью Aspose.PSD'
schemas:
- author: Aspose
  dateModified: '2026-09-28'
  description: Java image processing tutorial shows how to adjust brightness of an
    image using Aspose.PSD for Java. Follow step‑by‑step code to load, modify, and
    save PSD or TIFF files.
  headline: 'Java image processing: adjust brightness with Aspose.PSD'
  type: TechArticle
- description: Java image processing tutorial shows how to adjust brightness of an
    image using Aspose.PSD for Java. Follow step‑by‑step code to load, modify, and
    save PSD or TIFF files.
  name: 'Java image processing: adjust brightness with Aspose.PSD'
  steps:
  - name: Load the image
    text: The `RasterImage` class represents a rasterized version of a PSD or TIFF
      file in memory. It provides direct pixel access for color‑correction operations.
      In this step, we load the target image and cast it to a `RasterImage` for further
      processing.
  - name: Adjust brightness
    text: '`adjustBrightness(int value)` changes the lightness of every pixel by the
      specified integer value. Positive numbers brighten the image; negative numbers
      darken it. The method processes the image in‑place, so no additional object
      creation is required. Here, we use the `adjustBrightness` method to mod'
  - name: Set TiffOptions
    text: '`TiffOptions` specifies the encoding parameters for TIFF output, such as
      bits per sample and photometric interpretation. It lets you control how the
      resulting file is encoded. Configure the `TiffOptions` for saving the adjusted
      image. Adjust the `bitsPerSample` and `photometric` properties based on '
  - name: Save the resultant image
    text: Calling `save` writes the processed raster data to a file using the previously
      defined options. The operation is atomic and guarantees that the output file
      is a valid TIFF image. Finally, save the modified image using the specified
      `TiffOptions`.
  type: HowTo
- questions:
  - answer: Yes, Aspose.PSD for Java supports JPEG, PNG, BMP, GIF, and many other
      raster formats in addition to PSD and TIFF.
    question: Can I adjust brightness in other image formats besides PSD?
  - answer: Wrap the processing code in a try‑catch block and catch `IOException`
      or `ImageProcessingException` to manage file‑access and raster‑operation errors.
    question: How can I handle errors during the image adjustment process?
  - answer: The method accepts integer values from –255 to +255; values outside this
      range are clamped to the nearest limit.
    question: Is there a limit to the range of brightness adjustment?
  - answer: Yes, a commercial license is required for production use. Purchase a license
      [here](https://purchase.aspose.com/buy).
    question: Can I use Aspose.PSD for Java in commercial projects?
  - answer: Yes, you can explore the library with a free trial from [here](https://releases.aspose.com/).
    question: Is there a free trial available?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- java image processing
- aspose psd
- java image manipulation
title: 'Обработка изображений на Java: регулировка яркости с помощью Aspose.PSD'
url: /ru/java/advanced-techniques/adjust-brightness/
weight: 21
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Регулировка яркости изображения с помощью Aspose.PSD для Java

## Введение

В этом **java image processing** руководстве вы узнаете, как регулировать яркость изображения непосредственно из кода Java. Регулировка яркости — частая задача для графических дизайнеров, фотографов и всех, кто создает конвейеры обработки изображений. В этом **java image manipulation** руководстве мы пройдем полный рабочий процесс — загрузку PSD/TIFF, применение смещения яркости и сохранение результата — используя библиотеку Aspose.PSD for Java.

## Быстрые ответы
- **Какая библиотека обрабатывает яркость?** Aspose.PSD for Java.  
- **Какой метод изменяет яркость?** `RasterImage.adjustBrightness()`.  
- **Могу ли я работать с файлами PSD и TIFF?** Да, API поддерживает оба формата и более 10 дополнительных типов изображений.  
- **Нужна ли лицензия для продакшна?** Коммерческая лицензия требуется для использования не в режиме оценки.  
- **Сколько времени занимает реализация?** Обычно менее 10 минут для базовой корректировки.

## Что такое java image processing?
`Java image processing` относится к набору техник, позволяющих программно считывать, преобразовывать и записывать данные изображений с помощью Java. Регулировка яркости — одна из основных операций, изменяющая общую светлоту каждого пикселя, делая тёмные области светлее, а светлые — темнее.

## Почему использовать Aspose.PSD for Java?
Aspose.PSD for Java предоставляет комплексное, чисто‑Java решение, поддерживающее широкий спектр растровых и векторных форматов, устраняющее зависимости от нативных библиотек и предлагающее высокопроизводительное кэширование для больших файлов. Его обширный API позволяет разработчикам выполнять сложные коррекции цвета и редактирование слоёв с минимальным кодом, что делает его идеальным как для простых корректировок, так и для продвинутых конвейеров обработки изображений.

- **Поддерживает более 10 растровых и векторных форматов** – PSD, TIFF, JPEG, PNG, BMP, GIF и др.  
- **Чистая Java‑реализация** – без нативных DLL и внешних зависимостей, работает на любой JVM.  
- **Высокопроизводительное кэширование** – растровые данные могут кэшироваться, обеспечивая до 2× более быструю повторную обработку больших файлов.  
- **Богатый набор API** – более 150 методов для коррекции цвета, работы со слоями, масками и композитингом.

## Предварительные требования

Перед тем как приступить к руководству, убедитесь, что у вас есть следующие требования:

- Aspose.PSD for Java Library: Скачайте и установите библиотеку из [Aspose.PSD for Java documentation](https://reference.aspose.com/psd/java/).  
- Java Development Kit (JDK) 8 или выше, установленный на вашем компьютере.  
- Среда разработки (IDE), например IntelliJ IDEA, Eclipse или VS Code.

## Импорт пакетов

Чтобы начать, импортируйте необходимые пакеты в ваш проект Java. В этом примере мы будем использовать следующее:

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.psd.fileformats.tiff.enums.TiffPhotometrics;
import com.aspose.psd.imageoptions.TiffOptions;
```

Теперь давайте разберём процесс регулировки яркости изображения на простые шаги:

## Как регулировать яркость с помощью Aspose.PSD?

Загрузите исходное изображение, примените смещение яркости, настройте параметры сохранения и запишите результат на диск — всё в четырёх лаконичных шагах. Ниже представлены чёткие пошаговые инструкции, которые вы можете скопировать в свой проект. Такой подход гарантирует эффективное выполнение каждой операции и сохранение исходного качества изображения при желаемом изменении яркости.

### Шаг 1: Загрузка изображения

Класс `RasterImage` представляет растровую версию файла PSD или TIFF в памяти. Он предоставляет прямой доступ к пикселям для операций коррекции цвета.

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

В этом шаге мы загружаем целевое изображение и приводим его к типу `RasterImage` для дальнейшей обработки.

### Шаг 2: Регулировка яркости

`adjustBrightness(int value)` изменяет светлоту каждого пикселя на указанное целочисленное значение. Положительные числа делают изображение светлее, отрицательные — темнее. Метод обрабатывает изображение «на месте», без создания дополнительных объектов.

```java
// Adjust the brightness
rasterImage.adjustBrightness(-50);
```

Здесь мы используем метод `adjustBrightness` для изменения яркости изображения. В этом примере яркость уменьшается на 50 единиц, но вы можете задать любое значение в соответствии с вашими требованиями.

### Шаг 3: Настройка TiffOptions

`TiffOptions` задаёт параметры кодирования для вывода TIFF, такие как количество битов на образец и фотометрическая интерпретация. Позволяет контролировать, как будет закодирован результирующий файл.

```java
int[] ushort = {8, 8, 8};
// Create an instance of TiffOptions for the resultant image
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
tiffOptions.setBitsPerSample(ushort);
tiffOptions.setPhotometric(TiffPhotometrics.Rgb);
```

Настройте `TiffOptions` для сохранения скорректированного изображения. Отрегулируйте свойства `bitsPerSample` и `photometric` в соответствии с вашими конкретными потребностями.

### Шаг 4: Сохранение полученного изображения

Вызов `save` записывает обработанные растровые данные в файл, используя ранее определённые параметры. Операция атомарна и гарантирует, что выходной файл будет корректным TIFF‑изображением.

```java
// Save the resultant image
rasterImage.save(destName, tiffOptions);
```

Наконец, сохраните изменённое изображение, используя указанные `TiffOptions`.

## Распространённые проблемы и решения

| Проблема | Причина | Решение |
|----------|---------|----------|
| **`ClassCastException` при приведении Image** | Файл не является растровым изображением (например, векторный PSD). | Проверьте формат исходного файла или используйте `image instanceof RasterImage` перед приведением. |
| **Изменение яркости не оказывает эффекта** | Изображение не было закешировано перед изменением. | Вызовите `rasterImage.cacheData()` как показано в Шаге 1. |
| **Сохранённый файл выглядит повреждённым** | Неправильная конфигурация `TiffOptions`. | Убедитесь, что `bitsPerSample` соответствует глубине исходного изображения (обычно 8‑бит на канал). |

## Часто задаваемые вопросы

**Q: Можно ли регулировать яркость в других форматах изображений, кроме PSD?**  
A: Да, Aspose.PSD for Java поддерживает JPEG, PNG, BMP, GIF и многие другие растровые форматы помимо PSD и TIFF.

**Q: Как обрабатывать ошибки во время процесса регулировки яркости?**  
A: Оберните код обработки в блок try‑catch и перехватывайте `IOException` или `ImageProcessingException` для управления ошибками доступа к файлам и операций над растром.

**Q: Есть ли ограничение диапазона регулировки яркости?**  
A: Метод принимает целые значения от –255 до +255; значения за пределами этого диапазона ограничиваются ближайшим пределом.

**Q: Можно ли использовать Aspose.PSD for Java в коммерческих проектах?**  
A: Да, для продакшн‑использования требуется коммерческая лицензия. Приобрести лицензию можно [здесь](https://purchase.aspose.com/buy).

**Q: Доступна ли бесплатная пробная версия?**  
A: Да, вы можете опробовать библиотеку с бесплатной пробной версией [здесь](https://releases.aspose.com/).

**Q: Влияет ли метод `adjustBrightness` на видимость слоёв?**  
A: Метод работает с растровым составным изображением, поэтому скрытые слои игнорируются при растеризации, сохраняя ожидаемый визуальный результат.

**Q: Можно ли цепочкой применять несколько корректировок (например, контраст, насыщенность)?**  
A: Абсолютно. После регулировки яркости вы можете вызвать `adjustContrast`, `adjustSaturation` или другие методы коррекции цвета на том же экземпляре `RasterImage`.

---

**Последнее обновление:** 2026-09-28  
**Тестировано с:** Aspose.PSD for Java 24.12 (latest at time of writing)  
**Автор:** Aspose

## Связанные руководства

- [Библиотека обработки изображений Java: Инвертировать слой с помощью Aspose.PSD](/psd/java/advanced-image-manipulation/invert-adjustment-layer/)
- [Преобразовать изображение в градации серого с помощью Aspose.PSD for Java](/psd/java/advanced-techniques/grayscale-image/)
- [Как повернуть изображение на определённый угол с помощью Aspose.PSD for Java](/psd/java/advanced-image-manipulation/rotate-image-specific-angle/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}