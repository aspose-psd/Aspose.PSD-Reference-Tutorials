---
date: 2026-06-13
description: Узнайте, как изменить размер изображения в Java, используя Java image
  manipulation library. Следуйте нашему пошаговому руководству с Aspose.PSD for Java
  для эффективной image manipulation.
keywords:
- java image manipulation library
- how to resize image java
- change image dimensions java
linktitle: Выполнить простое изменение размера
schemas:
- author: Aspose
  dateModified: '2026-06-13'
  description: Learn how to resize image Java using a java image manipulation library.
    Follow our step‑by‑step guide with Aspose.PSD for Java for efficient image manipulation.
  headline: Simple Resizing with Aspose.PSD – Java Image Manipulation Library
  type: TechArticle
- description: Learn how to resize image Java using a java image manipulation library.
    Follow our step‑by‑step guide with Aspose.PSD for Java for efficient image manipulation.
  name: Simple Resizing with Aspose.PSD – Java Image Manipulation Library
  steps:
  - name: Set Your Document Directory
    text: Define the folder that contains the source PSD file. Replace the placeholder
      with your actual path.
  - name: Specify Source and Destination Paths
    text: Create full file names for the input PSD and the output JPEG.
  - name: Load the Image
    text: '`Image.load(path)` reads an image file from the given path and returns
      an `Image` instance. Load the PSD into an `Image` object.'
  - name: Resize the Image
    text: '`image.resize(width, height)` changes the image dimensions to the specified
      pixel size. Resize to the desired dimensions (e.g., 300 × 300 pixels).'
  - name: Save the Resized Image
    text: '`image.save(path, options)` writes the image to the specified file using
      the given format options. Export the resized bitmap as a JPEG file. > **Pro
      tip:** Experiment with different width/height values or maintain the aspect
      ratio by calculating one dimension from the other.'
  type: HowTo
- questions:
  - answer: Absolutely. The `resize(width, height)` method lets you define any pixel
      size you need.
    question: Can I resize images to specific dimensions using Aspose.PSD for Java?
  - answer: Yes. Besides PSD, the library supports JPEG, PNG, BMP, TIFF, and many
      more.
    question: Is Aspose.PSD for Java compatible with different image formats?
  - answer: Refer to the [Aspose.PSD for Java documentation](https://reference.aspose.com/psd/java/)
      for a full API reference.
    question: Where can I find additional documentation for Aspose.PSD for Java?
  - answer: Certainly! Download the [free trial version](https://releases.aspose.com/)
      to explore all features.
    question: Can I try Aspose.PSD for Java before purchasing?
  - answer: Visit the [Aspose.PSD forum](https://forum.aspose.com/c/psd/34) to ask
      questions and share experiences with the community.
    question: How can I get support for Aspose.PSD for Java?
  type: FAQPage
second_title: Aspose.PSD Java API
title: Простое изменение размера с Aspose.PSD – Java Image Manipulation Library
url: /ru/java/basic-image-operations/simple-resizing/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Простое изменение размера с Aspose.PSD – библиотека Java для обработки изображений

## Введение

Если вы разработчик Java и ищете надежную **java image manipulation library**, вы попали по адресу. В этом руководстве мы пройдемся по **how to resize image java** проектам, используя Aspose.PSD for Java — мощную библиотеку, которая делает обработку изображений быстрой и простой. К концу этого руководства у вас будет понятный, готовый к продакшену пример, который можно внедрить в любое Java‑приложение.

## Краткие ответы

- **Какая библиотека используется?** Aspose.PSD for Java, ведущая java image manipulation library.  
- **Могу ли я изменить размер любого PSD?** Да — библиотека поддерживает PSD, JPEG, PNG и другие форматы.  
- **Как указать размер?** Вызовите `image.resize(width, height)` с желаемыми пиксельными размерами.  
- **Нужна ли лицензия?** Бесплатная пробная версия подходит для разработки; для продакшена требуется лицензия.  
- **Какая версия Java требуется?** Java 8 или выше.

## Что такое Java Image Manipulation Library?

Это **java image manipulation library** — набор Java API, позволяющих программно редактировать растровую графику — изменение размера, обрезку, конвертацию форматов и работу со слоями — без внешних инструментов. Aspose.PSD предоставляет эти возможности для PSD и многих других форматов, предлагая чистый объектно‑ориентированный API для разработчиков.

## Почему использовать Aspose.PSD для простого изменения размера?

Aspose.PSD предоставляет **performance‑optimized** алгоритмы, которые могут обрабатывать файлы с более чем 500 слоями менее чем за секунду на типичном сервере, и работает полностью на Java — без нативных DLL или внешних бинарных файлов. Библиотека поддерживает **30+ image formats** (включая PSD, JPEG, PNG, TIFF, BMP, GIF) и может работать с файлами размером более 200 МБ, не загружая весь документ в память, что делает её идеальной для высокопроизводительных серверных конвейеров.

## Требования

Перед началом убедитесь, что у вас есть следующее:

1. **Java Development Kit (JDK)** – загрузите последнюю версию с сайта [Java website](https://www.oracle.com/java/).  
2. **Aspose.PSD for Java** – получите библиотеку со страницы [Aspose.PSD for Java download page](https://releases.aspose.com/psd/java/).  

Наличие этих компонентов обеспечивает плавную настройку примера изменения размера.

## Импорт пакетов

Класс `Image` и связанные параметры экспорта требуются для загрузки и сохранения файлов.

`Image` — основной класс, представляющий изображение, которое можно загрузить, отредактировать и сохранить.

`JpegOptions` задаёт настройки сохранения изображения в формате JPEG.

Эти импорты предоставляют доступ к основному классу `Image` и параметрам экспорта JPEG.

```java
import com.aspose.psd.Image;
import com.aspose.psd.imageoptions.JpegOptions;
```

## Пошаговое руководство

### Шаг 1: Установите каталог документа

Определите папку, содержащую исходный файл PSD. Замените заполнитель на ваш реальный путь.

```java
String dataDir = "Your Document Directory";
```

### Шаг 2: Укажите пути источника и назначения

Создайте полные имена файлов для входного PSD и выходного JPEG.

```java
String sourceFile = dataDir + "sample.psd";
String destName = dataDir + "SimpleResizing_out.jpg";
```

### Шаг 3: Загрузите изображение

`Image.load(path)` читает файл изображения по указанному пути и возвращает экземпляр `Image`.

Загрузите PSD в объект `Image`.

```java
Image image = Image.load(sourceFile);
```

### Шаг 4: Измените размер изображения

`image.resize(width, height)` изменяет размеры изображения до указанных пиксельных значений.

Измените размер до требуемых параметров (например, 300 × 300 пикселей).

```java
image.resize(300, 300);
```

### Шаг 5: Сохраните изменённое изображение

`image.save(path, options)` записывает изображение в указанный файл с использованием заданных параметров формата.

Экспортируйте изменённый bitmap в файл JPEG.

```java
image.save(destName, new JpegOptions());
```

> **Pro tip:** Экспериментируйте с разными значениями ширины/высоты или сохраняйте соотношение сторон, вычисляя одну размерность из другой.

## Как изменить размеры изображения в Java?

Используйте метод `resize(width, height)` у экземпляра `Image`, передавая точные пиксельные значения, которые вам нужны. Например, `image.resize(800, 600)` создаст изображение размером 800 × 600 пикселей, сохраняя глубину цвета и метаданные. Если нужно сохранить исходное соотношение сторон, вычислите вторую размерность на основе оригинального отношения ширины к высоте перед вызовом `resize`.

## Распространённые проблемы и решения

| Проблема | Причина | Решение |
|-------|--------|-----|
| **`OutOfMemoryError`** | Очень большие файлы PSD могут превышать размер кучи JVM. | Увеличьте размер кучи JVM (`-Xmx2g`) или обрабатывайте изображения частями. |
| **Unsupported format** | Попытка загрузить файл, не являющийся PSD, без соответствующих параметров. | Используйте соответствующую перегрузку `Image.load` или сначала конвертируйте файл. |
| **Distorted output** | Неправильное соотношение сторон. | Вычислите высоту на основе оригинального соотношения сторон или используйте `image.resizeProportionally`. |

## Часто задаваемые вопросы

**Q:** Могу ли я изменять размер изображений до конкретных размеров с помощью Aspose.PSD for Java?  
**A:** Конечно. Метод `resize(width, height)` позволяет задать любой необходимый размер в пикселях.

**Q:** Совместима ли Aspose.PSD for Java с различными форматами изображений?  
**A:** Да. Помимо PSD, библиотека поддерживает JPEG, PNG, BMP, TIFF и многие другие.

**Q:** Где я могу найти дополнительную документацию по Aspose.PSD for Java?  
**A:** Обратитесь к [Aspose.PSD for Java documentation](https://reference.aspose.com/psd/java/) для полного справочника API.

**Q:** Могу ли я попробовать Aspose.PSD for Java перед покупкой?  
**A:** Конечно! Скачайте [free trial version](https://releases.aspose.com/) чтобы ознакомиться со всеми функциями.

**Q:** Как я могу получить поддержку по Aspose.PSD for Java?  
**A:** Посетите [Aspose.PSD forum](https://forum.aspose.com/c/psd/34), чтобы задавать вопросы и делиться опытом с сообществом.

## Заключение

В этом руководстве мы продемонстрировали, как **java image manipulation library** вроде Aspose.PSD упрощает задачи **how to resize image java**. Следуя изложенным выше кратким шагам, вы сможете интегрировать изменение размера изображений в любое Java‑приложение, обеспечивая быстрые и надёжные результаты без внешних инструментов.

---

**Последнее обновление:** 2026-06-13  
**Тестировано с:** Aspose.PSD for Java 24.12 (latest)  
**Автор:** Aspose

## Связанные руководства

- [Изменение размера изображения Java — использование перечисления Resize Type в Aspose.PSD for Java](/psd/java/advanced-image-manipulation/resizing-with-resize-type-enumeration/)
- [Масштабирование изображений высокого качества с Bicubic Resampler в Aspose.PSD for Java](/psd/java/advanced-image-manipulation/implement-bicubic-resampler/)
- [Как конвертировать PSD в PNG и изменить размер пропорционально с Aspose.PSD for Java](/psd/java/advanced-image-manipulation/resize-image-proportionally/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< blocks/products/products-backtop-button >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}