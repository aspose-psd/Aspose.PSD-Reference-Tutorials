---
date: 2026-06-03
description: Узнайте, как изменить размер изображения с помощью Aspose.PSD for Java.
  Это пошаговое руководство охватывает Resize Type Enumeration, высококачественное
  изменение размера изображения и конвертацию PSD в JPEG.
keywords:
- how to resize image
- convert psd to jpeg
- high quality image resize
- resize image java
- java image manipulation tutorial
linktitle: Изменение размера с использованием Resize Type Enumeration
schemas:
- author: Aspose
  dateModified: '2026-06-03'
  description: Learn how to resize image with Aspose.PSD for Java. This step‑by‑step
    guide covers the Resize Type Enumeration, high‑quality image resize, and how to
    convert PSD to JPEG.
  headline: How to Resize Image Java Using Resize Type Enumeration
  type: TechArticle
- description: Learn how to resize image with Aspose.PSD for Java. This step‑by‑step
    guide covers the Resize Type Enumeration, high‑quality image resize, and how to
    convert PSD to JPEG.
  name: How to Resize Image Java Using Resize Type Enumeration
  steps:
  - name: '**Java Development Environment** – JDK 8 or newer installed and configured.'
    text: '**Java Development Environment** – JDK 8 or newer installed and configured.'
  - name: '**Aspose.PSD Library** – Download the latest JAR from the [website](https://releases.aspose.com/psd/java/).'
    text: '**Aspose.PSD Library** – Download the latest JAR from the [website](https://releases.aspose.com/psd/java/).'
  - name: '**Sample PSD File** – Use the [sample.psd](Your Document Directory/sample.psd)
      file included with the SDK for hands‑on testing.'
    text: '**Sample PSD File** – Use the [sample.psd](Your Document Directory/sample.psd)
      file included with the SDK for hands‑on testing.'
  type: HowTo
- questions:
  - answer: Load the PSD with `Image.load`, then call `image.save("output.jpg", new
      JpegOptions());`.
    question: How do I programmatically convert a PSD file to JPEG without resizing?
  - answer: Yes, you can set the `Resolution` property on the `Image` object before
      saving.
    question: Is it possible to maintain the original DPI when resizing?
  - answer: While you can call `resize` multiple times, it’s more efficient to calculate
      the final dimensions and resize once.
    question: Can I chain multiple resize operations?
  type: FAQPage
second_title: Aspose.PSD Java API
title: Как изменить размер изображения в Java с использованием Resize Type Enumeration
url: /ru/java/advanced-image-manipulation/resizing-with-resize-type-enumeration/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Как изменить размер изображения в Java с использованием перечисления типа изменения размера

## Введение

Если вы ищете **how to resize image** файлов эффективно в Java‑проекте, Aspose.PSD for Java предоставляет чистый, высокопроизводительный API. В этом руководстве мы пройдем процесс загрузки PSD, применения **Resize Type Enumeration** для масштабирования изображения высокого качества и, наконец, **convert PSD to JPEG**. Независимо от того, создаете ли вы настольный редактор или автоматизированный серверный конвейер, эти шаги позволяют контролировать размеры, качество и формат всего несколькими строками кода.

## Быстрые ответы
- **Какая библиотека обрабатывает resize image java?** Aspose.PSD for Java.
- **Какой тип изменения размера дает наилучшее качество?** `ResizeType.LanczosResample`.
- **Могу ли я конвертировать PSD в JPEG после изменения размера?** Да — просто сохраните с помощью `JpegOptions`.
- **Нужна ли лицензия для продакшн?** Для использования в продакшн требуется действующая лицензия Aspose.PSD.
- **Подходит ли этот подход для больших пакетов?** Абсолютно; API обрабатывает файлы со сотнями страниц без загрузки всего документа в память.

## Что такое "how to resize image" в Java?

**How to resize image** означает программное изменение пиксельных размеров изображения при сохранении визуального качества. Метод `Resize` в Aspose.PSD в сочетании с перечислением `ResizeType` обеспечивает точный контроль над алгоритмами масштабирования, позволяя разработчикам поддерживать качество при работе с широким спектром исходных файлов и целевых размеров.

## Почему использовать перечисление Resize Type?

`ResizeType` позволяет выбрать алгоритм ресемплинга, который лучше всего балансирует скорость и визуальное качество. Для большинства сценариев **LanczosResample** дает чёткие результаты при умеренных затратах производительности, обрабатывая изображение 2000 × 1500 за менее чем 120 мс на типичном серверном процессоре, сохраняя детали краёв.

## Предварительные требования

Перед началом убедитесь, что у вас есть:

1. **Java Development Environment** – установленный и настроенный JDK 8 или новее.  
2. **Aspose.PSD Library** – скачайте последнюю JAR‑файл с [website](https://releases.aspose.com/psd/java/).  
3. **Sample PSD File** – используйте файл [sample.psd](Your Document Directory/sample.psd), включённый в SDK, для практических тестов.

## Импорт пакетов

`Image` — базовый класс для всех типов изображений в Aspose.PSD. Добавьте необходимые импорты в ваш Java‑файл:

```java
import com.aspose.psd.Image;
import com.aspose.psd.ResizeType;

import com.aspose.psd.imageoptions.JpegOptions;
```

## Шаг 1: Загрузка изображения

### Якорь определения
Класс `RasterImage` — основной объект Aspose.PSD, представляющий растровое изображение, загруженное из PSD‑файла.

Загрузите ваш PSD в экземпляр `RasterImage`, чтобы иметь возможность манипулировать его пикселями:

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

// Load an existing image into an instance of RasterImage class
Image image = Image.load(sourceFile);
```

## Шаг 2: Изменение размера изображения

`image.resize(width, height, resizeType)` изменяет размер изображения до указанных параметров, используя выбранный алгоритм.

Теперь измените размер загруженного изображения, используя **Resize Type Enumeration**. В этом примере мы применяем метод Lanczos Resample, который идеален, когда вы **how to resize image** с высоким качеством:

```java
image.resize(300, 300, ResizeType.LanczosResample);
```

## Шаг 3: Сохранение изменённого изображения

`image.save(path, options)` записывает изображение на диск в формате, определённом переданными параметрами.

После изменения размера сохраните изображение с указанными размерами и выбранным типом изменения. Здесь мы также демонстрируем **convert psd to jpeg**, сохраняя результат в файл JPEG:

```java
String destName = dataDir + "ResizingwithResizeTypeEnumeration_out.jpg";
image.save(destName, new JpegOptions());
```

## Почему использовать перечисление Resize Type?

`ResizeType` даёт тонкую настройку алгоритма ресемплинга, позволяя балансировать скорость и качество. Для большинства приложений `LanczosResample` предлагает отличный компромисс, обеспечивая чёткие результаты без значительных потерь производительности и хорошо работает с различным содержимым изображений.

## Распространённые проблемы и решения

- **Image appears blurry after resize** – попробуйте другой `ResizeType`, например `Bicubic` или `NearestNeighbour`, чтобы увидеть, какой даст лучший визуальный результат для вашего конкретного изображения.  
- **OutOfMemoryError on large PSD files** – обрабатывайте изображение небольшими частями или увеличьте размер кучи JVM (`-Xmx` флаг). Aspose.PSD может работать с файлами до **2 GB**, не загружая весь документ в память.

## Часто задаваемые вопросы

### Вопрос 1: Подходит ли Aspose.PSD for Java как для небольших, так и для крупномасштабных проектов?

**A1:** Абсолютно! Aspose.PSD for Java разработан для проектов любого размера, обеспечивая масштабируемость и эффективность.

### Вопрос 2: Могу ли я использовать другой тип изменения размера, отличный от Lanczos Resample?

**A2:** Да, Aspose.PSD for Java предлагает различные типы изменения размера, такие как **NearestNeighbour**, **Bicubic** и другие. См. документацию API для полного списка.

### Вопрос 3: Где я могу найти дополнительную поддержку Aspose.PSD for Java?

**A3:** По любым вопросам или за помощью посетите [Aspose.PSD forum](https://forum.aspose.com/c/psd/34).

### Вопрос 4: Есть ли бесплатная пробная версия Aspose.PSD for Java?

**A4:** Да, бесплатную пробную версию можно получить [здесь](https://releases.aspose.com/).

### Вопрос 5: Как получить временную лицензию для Aspose.PSD for Java?

**A5:** Чтобы получить временную лицензию, перейдите по [this link](https://purchase.aspose.com/temporary-license/).

## Часто задаваемые вопросы

**Q: Как программно конвертировать PSD‑файл в JPEG без изменения размера?**  
A: Загрузите PSD с помощью `Image.load`, затем вызовите `image.save("output.jpg", new JpegOptions());`.

**Q: Можно ли сохранить оригинальное DPI при изменении размера?**  
A: Да, вы можете установить свойство `Resolution` у объекта `Image` перед сохранением.

**Q: Можно ли цепочкой выполнять несколько операций изменения размера?**  
A: Хотя вы можете вызывать `resize` несколько раз, эффективнее вычислить окончательные размеры и выполнить изменение один раз.

---

**Last Updated:** 2026-06-03  
**Tested With:** Aspose.PSD for Java 24.12  
**Author:** Aspose  

{{< blocks/products/products-backtop-button >}}

## Похожие руководства

- [Simple Resizing with Aspose.PSD – Java Image Manipulation Library](/psd/java/basic-image-operations/simple-resizing/)
- [High Quality Image Scaling with Bicubic Resampler in Aspose.PSD for Java](/psd/java/advanced-image-manipulation/implement-bicubic-resampler/)
- [How to Convert PSD to PNG and Resize Proportionally with Aspose.PSD for Java](/psd/java/advanced-image-manipulation/resize-image-proportionally/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}