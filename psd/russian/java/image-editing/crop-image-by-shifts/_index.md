---
date: 2026-07-03
description: Узнайте, как обрезать изображение в Java с помощью Aspose.PSD for Java.
  Этот пошаговый учебник по обрезке изображений охватывает загрузку PSD‑файлов, установку
  значений сдвига и сохранение результата.
keywords:
- crop image java
- how to crop image
- load psd file
- java image processing
- crop image left right
linktitle: Обрезка изображения по сдвигам
schemas:
- author: Aspose
  dateModified: '2026-07-03'
  description: Learn how to crop image java using Aspose.PSD for Java. This step‑by‑step
    image cropping tutorial covers loading PSD files, setting shift values, and saving
    the result.
  headline: Crop Image Java by Shifts with Aspose.PSD
  type: TechArticle
- description: Learn how to crop image java using Aspose.PSD for Java. This step‑by‑step
    image cropping tutorial covers loading PSD files, setting shift values, and saving
    the result.
  name: Crop Image Java by Shifts with Aspose.PSD
  steps:
  - name: Load the Image
    text: '`Image` is the base class for all image types in Aspose.PSD. `RasterImage`
      represents a raster image and provides cropping capabilities.'
  - name: Cache Image Data
    text: '`cacheData()` loads the image data into memory for faster processing.'
  - name: Define Shift Values
    text: Specify the shift values for all four sides of the image (left, top, right,
      bottom) in pixels.
  - name: Apply Cropping
    text: '`crop(left, right, top, bottom)` trims the image by the specified pixel
      shifts on each side.'
  - name: Save the Results
    text: '`JpegOptions` defines JPEG encoding settings such as quality and color
      profile. Congratulations! You''ve successfully cropped an image using Aspose.PSD
      for Java.'
  type: HowTo
- questions:
  - answer: Yes, Aspose.PSD supports over 30 raster formats, including PSD, JPEG,
      PNG, BMP, TIFF, and GIF, ensuring broad compatibility.
    question: Is Aspose.PSD compatible with all image formats?
  - answer: Absolutely. After each `crop` call you receive a new image object, which
      you can crop again as needed.
    question: Can I apply multiple cropping operations to the same image?
  - answer: Yes, you can find support and engage with the community at [Aspose.PSD
      Forum](https://forum.aspose.com/c/psd/34).
    question: Is there a community forum for Aspose.PSD support?
  - answer: Visit [here](https://purchase.aspose.com/temporary-license/) to obtain
      a temporary license.
    question: How can I obtain a temporary license for Aspose.PSD?
  - answer: Explore the documentation and examples at [Aspose.PSD Java Documentation](https://reference.aspose.com/psd/java/).
    question: Are there sample projects showcasing Aspose.PSD functionalities?
  type: FAQPage
second_title: Aspose.PSD Java API
title: Обрезка изображения в Java по сдвигам с Aspose.PSD
url: /ru/java/image-editing/crop-image-by-shifts/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Обрезка изображения Java с помощью сдвигов в Aspose.PSD

## Введение

В обработке изображений на Java **crop image java** является распространённой задачей для подготовки графики, миниатюр или UI‑элементов. Aspose.PSD for Java упрощает эту задачу, предоставляя простой метод `crop`, который работает с любым поддерживаемым растровым форматом. В этом руководстве вы узнаете, как загрузить файл PSD, задать значения сдвигов слева‑справа‑сверху‑снизу, применить обрезку и сохранить результат — без написания собственного кода манипуляции пикселями.

## Быстрые ответы
- **Какая библиотека обрабатывает обрезку?** Aspose.PSD for Java предоставляет встроенный метод `crop`.  
- **Нужна ли лицензия?** Временная лицензия подходит для оценки; полная лицензия требуется для продакшн.  
- **Поддерживаемые форматы?** Более 30 растровых форматов, включая PSD, JPEG, PNG, BMP и TIFF.  
- **Максимальный размер файла?** Обрабатывает файлы до 2 ГБ без загрузки всего изображения в память.  
- **Сколько строк кода?** Всего пять логических шагов — загрузка, кэширование, определение сдвигов, обрезка и сохранение.

## Что такое crop image java?
`crop image java` относится к операции обрезки битмапа в приложении Java. С использованием Aspose.PSD операция выполняется методом `crop`, который принимает значения сдвигов для каждой стороны изображения и возвращает новый экземпляр изображения.

## Почему использовать Aspose.PSD для обрезки изображений?
Aspose.PSD поддерживает **30+** форматов изображений и может обрабатывать многосотстраничные PSD‑файлы, используя менее 150 МБ ОЗУ благодаря своей архитектуре ленивой загрузки. Библиотека также гарантирует пиксель‑точные результаты, сохраняя слои, маски и цветовые профили — то, чего многие общие библиотеки изображений не могут гарантировать.

## Требования

### Java Development Kit (JDK)

Убедитесь, что на вашей системе установлена последняя версия JDK. Вы можете скачать её [здесь](https://www.oracle.com/java/technologies/javase-downloads.html).

### Библиотека Aspose.PSD for Java

Для начала вам необходимо получить библиотеку Aspose.PSD for Java. Перейдите на страницу [скачивания](https://releases.aspose.com/psd/java/) и загрузите последнюю версию.

### Интегрированная среда разработки (IDE)

Выберите вашу любимую Java IDE, например Eclipse или IntelliJ, для комфортной работы с кодом.

## Как обрезать изображение Java?

Загрузите исходный файл, задайте пиксельные сдвиги для каждой стороны и вызовите метод `crop` — весь процесс можно реализовать в пяти лаконичных строках кода. Операция `crop` создает новое изображение, содержащее только указанный регион, оставляя оригинальный файл нетронутым.

### Шаг 1: Загрузка изображения

`Image` — базовый класс для всех типов изображений в Aspose.PSD.  
`RasterImage` представляет растровое изображение и предоставляет возможности обрезки.  
```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.imageoptions.JpegOptions;
```

### Шаг 2: Кэширование данных изображения

`cacheData()` загружает данные изображения в память для более быстрой обработки.  
```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

// Load an existing image into an instance of RasterImage class
RasterImage rasterImage = (RasterImage)Image.load(sourceFile);
```

### Шаг 3: Определение значений сдвигов

Укажите значения сдвигов для всех четырёх сторон изображения (слева, сверху, справа, снизу) в пикселях.  
```java
if (!rasterImage.isCached()) {
  rasterImage.cacheData();
}
```

### Шаг 4: Применение обрезки

`crop(left, right, top, bottom)` обрезает изображение на указанные пиксельные сдвиги по каждой стороне.  
```java
int leftShift = 10;
int rightShift = 10;
int topShift = 10;
int bottomShift = 10;
```

### Шаг 5: Сохранение результатов

`JpegOptions` определяет параметры кодирования JPEG, такие как качество и цветовой профиль.  
```java
rasterImage.crop(leftShift, rightShift, topShift, bottomShift);
```

Поздравляем! Вы успешно обрезали изображение с помощью Aspose.PSD for Java.

## Распространённые проблемы и решения

- **Изображение не изменилось:** Убедитесь, что значения сдвигов положительные и не превышают оригинальные размеры.  
- **OutOfMemoryError при работе с большими файлами:** Включите кэширование, как показано в Шаге 2; это заставит Aspose.PSD использовать временный файл вместо хранения всего изображения в ОЗУ.  
- **Смещение цвета после обрезки:** Убедитесь, что сохраняете цветовой профиль, вызывая `image.save(..., new JpegOptions { ColorProfile = image.ColorProfile })`, если требуется точная цветовая достоверность.

## Часто задаваемые вопросы

**Q: Совместим ли Aspose.PSD со всеми форматами изображений?**  
A: Да, Aspose.PSD поддерживает более 30 растровых форматов, включая PSD, JPEG, PNG, BMP, TIFF и GIF, обеспечивая широкую совместимость.

**Q: Можно ли применить несколько операций обрезки к одному изображению?**  
A: Абсолютно. После каждого вызова `crop` вы получаете новый объект изображения, который можно снова обрезать при необходимости.

**Q: Есть ли форум сообщества для поддержки Aspose.PSD?**  
A: Да, вы можете получить поддержку и общаться с сообществом на [Aspose.PSD Forum](https://forum.aspose.com/c/psd/34).

**Q: Как получить временную лицензию для Aspose.PSD?**  
A: Перейдите [сюда](https://purchase.aspose.com/temporary-license/), чтобы получить временную лицензию.

**Q: Есть ли примерные проекты, демонстрирующие возможности Aspose.PSD?**  
A: Изучите документацию и примеры на странице [Aspose.PSD Java Documentation](https://reference.aspose.com/psd/java/).

---

**Последнее обновление:** 2026-07-03  
**Тестировано с:** Aspose.PSD 24.11 for Java  
**Автор:** Aspose  

{{< blocks/products/products-backtop-button >}}

```java
String destName = dataDir + "CroppingByShifts_out.jpg";
rasterImage.save(destName, new JpegOptions());
```

## Связанные руководства

- [Обрезка изображения по прямоугольнику в Aspose.PSD for Java](/psd/java/image-editing/crop-image-by-rectangle/)
- [Crop Image Java — расширение и обрезка изображений с Aspose.PSD for Java](/psd/java/image-editing/expand-and-crop-images/)
- [Изменение размера изображения Java — использование перечисления Resize Type в Aspose.PSD for Java](/psd/java/advanced-image-manipulation/resizing-with-resize-type-enumeration/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}