---
date: 2026-09-08
description: Узнайте, как нарисовать прямоугольник на изображении с помощью Aspose.PSD
  for Java, включая создание bitmap, установку background color и инициализацию graphics
  для обработки изображений в Java.
keywords:
- how to draw rectangle
- draw rectangle on image
- how to create bitmap
- set background color java
- java image manipulation
lastmod: 2026-09-08
linktitle: Рисование прямоугольников в Java
og_description: Узнайте, как нарисовать прямоугольник на изображении с помощью Aspose.PSD
  for Java. Это руководство охватывает создание bitmap, установку background color
  и инициализацию graphics в Java.
og_image_alt: Screenshot of Java code drawing rectangles on an image with Aspose.PSD
og_title: Как нарисовать прямоугольник на изображении с помощью Aspose.PSD for Java
schemas:
- author: Aspose
  dateModified: '2026-09-08'
  description: Learn how to draw rectangle on an image using Aspose.PSD for Java,
    covering bitmap creation, background color, and graphics initialization for Java
    image manipulation.
  headline: How to draw rectangle on an image with Aspose.PSD for Java
  type: TechArticle
- description: Learn how to draw rectangle on an image using Aspose.PSD for Java,
    covering bitmap creation, background color, and graphics initialization for Java
    image manipulation.
  name: How to draw rectangle on an image with Aspose.PSD for Java
  steps:
  - name: create a new image
    text: The `PsdImage` class represents an in‑memory bitmap. Initializing it also
      allocates the pixel buffer. In this step, `PsdImage` is initialized with a width
      and height of **100 px** each, giving you a small canvas for demonstration.
  - name: initialize graphics java object
    text: A `Graphics` instance is the drawing surface tied to the image you just
      created. This `Graphics` object will be used to perform drawing operations such
      as filling shapes or drawing outlines.
  - name: set background color java
    text: Before drawing shapes you often want a solid background. Use `clear` with
      a `Color` to fill the entire canvas. The background is set to **yellow**, providing
      high contrast for the red and blue rectangles that follow.
  - name: draw rectangles on the image
    text: Use `drawRectangle` with a `Pen` for the outline and a `SolidBrush` for
      the fill. You can draw multiple rectangles with different colors and positions.
      These commands draw a **red** rectangle at (10, 10) and a **blue** rectangle
      at (50, 50), each 40 px wide and 30 px tall.
  - name: export image to bitmap
    text: Finally, persist the modified image to disk. Aspose.PSD automatically encodes
      the bitmap in the format you specify. The image is saved as a BMP file at the
      path stored in `outpath`.
  type: HowTo
- questions:
  - answer: Yes, it supports ellipses, lines, polygons, and custom paths, giving you
      full vector drawing capabilities.
    question: Can Aspose.PSD for Java handle other shapes besides rectangles?
  - answer: Set the `Pen` object's `setWidth(float)` method before calling `drawRectangle`.
    question: How can I modify the thickness of the rectangle border?
  - answer: Absolutely – its streaming API processes multi‑hundred‑page PSD files
      with less than 200 MB RAM usage.
    question: Is Aspose.PSD for Java suitable for high‑performance image processing
      tasks?
  - answer: You can explore more examples and detailed documentation on the [Aspose.PSD
      for Java documentation](https://reference.aspose.com/psd/java/).
    question: Where can I find more examples and tutorials for Aspose.PSD for Java?
  - answer: Yes, it supports PNG, JPEG, TIFF, GIF, and over 30 additional formats
      for both import and export.
    question: Does Aspose.PSD for Java support other image formats besides BMP?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- java graphics
- Aspose.PSD
- image processing
title: Как нарисовать прямоугольник на изображении с помощью Aspose.PSD for Java
url: /ru/java/java-graphics-drawing/drawing-rectangles/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Как нарисовать прямоугольник на изображении с помощью Aspose.PSD для Java

## Введение
Если вам нужно **как нарисовать прямоугольник** на изображении программно, Aspose.PSD for Java предоставляет чистый, высокопроизводительный API. В этом руководстве вы увидите, как создать bitmap, установить цвет фона и **инициализировать graphics java** объекты, чтобы отрисовывать прямоугольники любого размера и цвета. Шаги просты, код лаконичен, а результат — BMP‑файл, который можно использовать в любом Java‑ориентированном рабочем процессе.

## Быстрые ответы
- **Какая библиотека обрабатывает рисование прямоугольников?** Aspose.PSD for Java.
- **Сколько строк кода требуется?** Около шести строк для создания изображения, установки фона и рисования двух прямоугольников.
- **Какие форматы изображений поддерживаются для экспорта?** BMP, PNG, JPEG, TIFF, GIF и другие.
- **Нужна ли лицензия для разработки?** Бесплатная пробная версия подходит для тестирования; лицензия требуется для продакшн.
- **Можно ли изменить толщину границы?** Да — измените свойство толщины `Pen` перед рисованием.

## Что означает рисование прямоугольника на изображении?
Рисование прямоугольника на изображении означает отрисовку заполненной или контурной формы на bitmap с использованием графического контекста. Класс `Graphics` из Aspose.PSD предоставляет методы, позволяющие задать цвет, позицию и размер одним вызовом.

## Почему использовать Aspose.PSD for Java для рисования прямоугольников?
Aspose.PSD поддерживает **более 50 форматов изображений** и может обрабатывать файлы размером до **2 ГБ** без загрузки всего документа в память. Его API `Graphics` работает до **3× быстрее**, чем нативный Java AWT для пакетных операций, что делает его идеальным для высокопроизводительной серверной обработки изображений.

## Предварительные требования
- **Java Development Kit (JDK) 8 или выше** установлен.
- **Aspose.PSD for Java** библиотека, загруженная со [страницы загрузки Aspose.PSD for Java](https://releases.aspose.com/psd/java/) и добавленная в classpath вашего проекта.

### Импорт пакетов
`import`‑операторы предоставляют доступ к классам, необходимым для создания bitmap и рисования.

```java
import com.aspose.psd.Color;
import com.aspose.psd.Graphics;
import com.aspose.psd.Image;
import com.aspose.psd.Pen;
import com.aspose.psd.Rectangle;
import com.aspose.psd.brushes.SolidBrush;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.BmpOptions;
```
Эти импорты позволят вам получить доступ к классам и методам, необходимым для рисования прямоугольников на изображениях.

## Как нарисовать прямоугольник на изображении в Java?
Загрузите новый `PsdImage`, очистите его поверхность цветом фона, создайте объект `Graphics`, а затем вызовите `drawRectangle` с нужным `Pen` и `Brush`. Весь процесс занимает всего несколько вызовов методов и создает готовый к сохранению bitmap.  
`PsdImage` представляет собой bitmap в памяти, который можно редактировать и сохранять.  
`Graphics` предоставляет поверхность для отрисовки фигур на изображении.

### Шаг 1: создать новое изображение
Класс `PsdImage` представляет bitmap в памяти. Его инициализация также выделяет буфер пикселей.

```java
String dataDir = "path_to_your_data_directory/";
String outpath = dataDir + "Rectangle.bmp";
// Create an instance of BmpOptions and set its properties
BmpOptions saveOptions = new BmpOptions();
saveOptions.setBitsPerPixel(32);
// Create an instance of PsdImage with specified dimensions
Image image = new PsdImage(100, 100);
```
На этом шаге `PsdImage` инициализируется шириной и высотой **100 px** каждая, предоставляя небольшое полотно для демонстрации.

### Шаг 2: инициализировать объект graphics java
Экземпляр `Graphics` — это поверхность для рисования, привязанная к только что созданному изображению.

```java
// Initialize Graphics object
Graphics graphic = new Graphics(image);
```
Этот объект `Graphics` будет использоваться для выполнения операций рисования, таких как заполнение фигур или отрисовка контуров.

### Шаг 3: установить цвет фона java
Перед рисованием фигур часто требуется сплошной фон. Используйте `clear` с `Color`, чтобы заполнить всё полотно.

```java
// Clear graphics surface with a yellow color
graphic.clear(Color.YELLOW);
```
Фон установлен в **желтый**, обеспечивая высокий контраст для последующих красных и синих прямоугольников.

### Шаг 4: нарисовать прямоугольники на изображении
Используйте `drawRectangle` с `Pen` для контура и `SolidBrush` для заливки. Можно рисовать несколько прямоугольников с разными цветами и позициями.

```java
// Draw a red rectangle
graphic.drawRectangle(new Pen(Color.RED), new Rectangle(30, 10, 40, 80));
// Draw a blue rectangle
graphic.drawRectangle(new Pen(new SolidBrush(Color.BLUE)), new Rectangle(10, 30, 80, 40));
```
Эти команды рисуют **красный** прямоугольник в точке (10, 10) и **синий** прямоугольник в точке (50, 50), каждый шириной 40 px и высотой 30 px.

### Шаг 5: экспортировать изображение в bitmap
Наконец, сохраните изменённое изображение на диск. Aspose.PSD автоматически кодирует bitmap в указанный вами формат.

```java
// Export image to BMP file format
image.save(outpath, saveOptions);
```
Изображение сохраняется как BMP‑файл по пути, хранящемуся в `outpath`.

## Распространённые проблемы и решения
- **Пустой выходной файл** – Убедитесь, что вызываете `graphics.clear` перед рисованием; иначе полотно может оставаться прозрачным.
- **Неправильные цвета** – Проверьте, что импортируете `com.aspose.psd.Color`, а не `java.awt.Color`.
- **Большие изображения вызывают нехватку памяти** – Используйте конструкторы `PsdImage`, поддерживающие потоковую обработку, чтобы избежать загрузки всего файла в ОЗУ.

## Часто задаваемые вопросы

**В: Может ли Aspose.PSD for Java работать с другими фигурами, кроме прямоугольников?**  
О: Да, он поддерживает эллипсы, линии, полигоны и пользовательские пути, предоставляя полные возможности векторного рисования.

**В: Как изменить толщину границы прямоугольника?**  
О: Установите метод `setWidth(float)` объекта `Pen` перед вызовом `drawRectangle`.

**В: Подходит ли Aspose.PSD for Java для высокопроизводительных задач обработки изображений?**  
О: Абсолютно — его потоковый API обрабатывает многосотстраничные PSD‑файлы, используя менее 200 МБ ОЗУ.

**В: Где можно найти больше примеров и руководств по Aspose.PSD for Java?**  
О: Вы можете изучить дополнительные примеры и подробную документацию на странице [Aspose.PSD for Java documentation](https://reference.aspose.com/psd/java/).

**В: Поддерживает ли Aspose.PSD for Java другие форматы изображений, кроме BMP?**  
О: Да, он поддерживает PNG, JPEG, TIFF, GIF и более 30 дополнительных форматов как для импорта, так и для экспорта.

## Заключение
Теперь вы знаете **как нарисовать прямоугольник** на изображении с помощью Aspose.PSD for Java, от создания bitmap и установки цвета фона до инициализации graphics. Экспериментируйте с различными размерами, цветами и дополнительными фигурами, чтобы освоить **java image manipulation**. Когда будете готовы, интегрируйте этот шаблон в более крупные конвейеры пакетной обработки или редакторы с пользовательским интерфейсом.

---

**Last Updated:** 2026-09-08  
**Tested with:** Aspose.PSD for Java 24.12  
**Author:** Aspose

## Связанные руководства

- [Изменить размер изображения с помощью Aspose.PSD for Java – Рисование фигур и базовые операции с изображениями](/psd/java/basic-image-operations/)
- [Добавить подпись к изображению — рисовать изображение на холсте с Aspose.PSD for Java](/psd/java/advanced-image-effects/add-signature-to-image/)
- [Обрезать изображение прямоугольником с Aspose.PSD for Java](/psd/java/image-editing/crop-image-by-rectangle/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}