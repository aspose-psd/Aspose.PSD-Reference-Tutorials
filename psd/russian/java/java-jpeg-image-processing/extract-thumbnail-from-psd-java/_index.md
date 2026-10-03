---
date: 2026-10-03
description: Узнайте, как извлечь миниатюру из PSD на Java с помощью Aspose.PSD. Это
  пошаговое руководство охватывает настройку, примеры кода и сохранение миниатюры
  в виде изображения JPEG.
keywords:
- extract thumbnail from psd
- java aspose psd
- psd thumbnail extraction
lastmod: 2026-10-03
linktitle: Извлечение миниатюры из PSD на Java
og_description: Узнайте, как извлечь миниатюру из PSD на Java с Aspose.PSD. Это руководство
  проведет вас через настройку, загрузку файла, извлечение миниатюры и сохранение
  её в виде изображения JPEG.
og_image_alt: Screenshot showing Java code extracting a thumbnail from a PSD file
  using Aspose.PSD
og_title: Извлечение миниатюры из PSD на Java с использованием Aspose.PSD
schemas:
- author: Aspose
  dateModified: '2026-10-03'
  description: Learn how to extract thumbnail from PSD in Java using Aspose.PSD. This
    step‑by‑step guide covers setup, code snippets, and saving the thumbnail as a
    JPEG image.
  headline: Extract thumbnail from PSD in Java
  type: TechArticle
- questions:
  - answer: Aspose.PSD is a Java library that enables programmatic creation, manipulation,
      and conversion of PSD and other raster image formats without requiring Adobe
      Photoshop.
    question: What is Aspose.PSD?
  - answer: You can refer to the [documentation](https://reference.aspose.com/psd/java/)
      for detailed API references and examples.
    question: Where can I find more documentation on Aspose.PSD for Java?
  - answer: Yes, you can download a [free trial](https://releases.aspose.com/) to
      evaluate the library’s capabilities.
    question: Can I try Aspose.PSD for free before purchasing?
  - answer: Temporary licenses are available from the [temporary license](https://purchase.aspose.com/temporary-license/)
      page.
    question: How can I obtain a temporary license for Aspose.PSD?
  - answer: Yes, Aspose.PSD can be used in both personal and commercial projects under
      its licensing terms.
    question: Is Aspose.PSD suitable for commercial use?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- java image processing
- aspose.psd
- thumbnail extraction
title: Извлечение миниатюры из PSD на Java
url: /ru/java/java-jpeg-image-processing/extract-thumbnail-from-psd-java/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Извлечение миниатюры из PSD в Java

## Введение
Извлечение миниатюры из файла PSD позволяет быстро создавать превью без загрузки изображения в полном разрешении. В Java библиотека Aspose.PSD делает этот процесс простым и производительным. В этом руководстве вы узнаете, как настроить библиотеку, найти ресурс миниатюры и сохранить его как JPEG‑файл — всё это с помощью всего нескольких строк кода.

## Быстрые ответы
- **Какая библиотека обрабатывает миниатюры PSD?** Aspose.PSD for Java.  
- **Сколько строк кода требуется?** Около пяти строк для загрузки, извлечения и сохранения.  
- **Можно ли извлекать миниатюры из больших файлов PSD?** Да, Aspose.PSD обрабатывает файлы до 500 MB без полной загрузки в память.  
- **Нужна ли лицензия для разработки?** Бесплатная пробная версия подходит для оценки; лицензия требуется для продакшн.  
- **Какие форматы вывода поддерживаются?** Извлечённую миниатюру можно сохранить как JPEG, PNG или BMP.

## Что такое извлечение миниатюры из PSD?
Извлечение миниатюры из PSD — это процесс чтения небольшого изображения‑превью, встроенного в документ Photoshop (PSD). Этот превью хранится как ресурс и может быть сохранён отдельно для каталогизации или отображения. Миниатюра обычно представляет собой низкоразрешённое изображение, которое приложения используют для быстрой визуализации без загрузки полного изображения.

## Почему использовать Aspose.PSD для этой задачи?
Aspose.PSD поддерживает **более 30 форматов изображений** и может работать с файлами PSD размером до **500 MB**, при этом потребление памяти остаётся низким, поскольку ресурсы читаются по требованию. API также обеспечивает надёжную обработку ошибок, позволяя стабильно извлекать миниатюры даже из повреждённых файлов.

## Требования
- Установлен Java Development Kit (JDK).  
- Библиотека Aspose.PSD for Java загружена с [Aspose.PSD for Java download](https://releases.aspose.com/psd/java/).  
- Базовое знакомство с синтаксисом Java и настройкой проекта.

## Как извлечь миниатюру из файла PSD в Java?
Загрузите файл PSD с помощью `PsdImage`, найдите `ThumbnailResource` и сохраните его данные изображения как JPEG. Aspose.PSD абстрагирует низкоуровневый парсинг, поэтому достаточно вызвать `getResources()` и затем `save()` у извлечённого изображения. Этот подход работает с любым PSD, содержащим миниатюру, независимо от размера файла.

## Импорт пакетов
`Image` — базовый класс для загрузки изображений. `PsdImage` представляет документ PSD. `ThumbnailResource` и `Thumbnail4Resource` представляют ресурсы миниатюр. `JpegOptions` задаёт параметры сохранения JPEG.

```text
```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.resources.Thumbnail4Resource;
import com.aspose.psd.fileformats.psd.resources.ThumbnailResource;
import com.aspose.psd.imageoptions.JpegOptions;
```
```

## Шаг 1: загрузка файла PSD
Сначала создайте экземпляр `PsdImage`, указывая путь к вашему файлу PSD. Конструктор читает только заголовок и необходимые ресурсы, минимизируя использование памяти.

```text
```java
String dataDir = "Your_Document_Directory/";
PsdImage image = (PsdImage)Image.load(dataDir + "your_file.psd");
```
```

Замените `"Your_Document_Directory/"` на путь к каталогу, где находится ваш файл PSD, а `"your_file.psd"` — на имя вашего файла PSD.

## Шаг 2: перебор ресурсов изображения
Aspose.PSD хранит миниатюры как объекты `ThumbnailResource` внутри коллекции ресурсов изображения. Пройдите по коллекции, проверьте тип ресурса и извлеките первую найденную миниатюру.

```text
```java
for (int i = 0; i < image.getImageResources().length; i++) {
    if (image.getImageResources()[i] instanceof ThumbnailResource) {
        ThumbnailResource thumbnail = (ThumbnailResource) image.getImageResources()[i];
        
        // Extract thumbnail data
        int[] data = thumbnail.getThumbnailArgb32Data();
        
        // Create a new image with the extracted thumbnail data
        PsdImage extractedThumbnailImage = new PsdImage(thumbnail.getWidth(), thumbnail.getHeight());
        extractedThumbnailImage.saveArgb32Pixels(extractedThumbnailImage.getBounds(), data);
        
        // Save the extracted thumbnail as a separate JPEG file
        extractedThumbnailImage.save(dataDir + "extracted_thumbnail.jpg", new JpegOptions());
        
        // Output success message
        System.out.println("Thumbnail extracted and saved successfully.");
        
        break; // Exit the loop once thumbnail is found and processed
    }
}
```
```

## Шаг 3: сохранение извлечённой миниатюры
После получения изображения миниатюры вызовите его метод `save`, чтобы записать его на диск. Вы можете выбрать JPEG, PNG или BMP; JPEG наиболее распространён для веб‑превью.

## Шаг 4: обработка разных типов миниатюр
Если PSD содержит несколько вариантов миниатюр, например `Thumbnail4Resource`, расширьте логику итерации, проверяя каждый тип. API предоставляет отдельные классы для каждого ресурса, позволяя выбрать нужное разрешение.

## Распространённые проблемы и решения
- **Миниатюра не найдена:** Не все файлы PSD содержат встроенный предварительный просмотр. Проверьте исходный файл в панели Photoshop «File → File Info».  
- **Ошибка неподдерживаемого формата:** Убедитесь, что используете последнюю версию Aspose.PSD; более старые релизы могут не поддерживать новые типы ресурсов миниатюр.  
- **Недостаток памяти при работе с большими файлами:** Используйте `PsdImage.load(..., LoadOptions)` с `LoadOptions.setLoadResourcesOnly(true)`, чтобы не загружать полные данные изображения, когда нужна только миниатюра.

## Часто задаваемые вопросы

**Q: Что такое Aspose.PSD?**  
A: Aspose.PSD — это Java‑библиотека, позволяющая программно создавать, изменять и конвертировать файлы PSD и другие растровые форматы изображений без необходимости установки Adobe Photoshop.

**Q: Где я могу найти более подробную документацию по Aspose.PSD for Java?**  
A: Вы можете обратиться к [documentation](https://reference.aspose.com/psd/java/) для получения подробных справочных материалов API и примеров.

**Q: Можно ли попробовать Aspose.PSD бесплатно перед покупкой?**  
A: Да, вы можете скачать [free trial](https://releases.aspose.com/) для оценки возможностей библиотеки.

**Q: Как я могу получить временную лицензию для Aspose.PSD?**  
A: Временные лицензии доступны на странице [temporary license](https://purchase.aspose.com/temporary-license/).

**Q: Подходит ли Aspose.PSD для коммерческого использования?**  
A: Да, Aspose.PSD может использоваться как в личных, так и в коммерческих проектах в соответствии с условиями лицензии.

---

**Последнее обновление:** 2026-10-03  
**Тестировано с:** Aspose.PSD for Java 24.12  
**Автор:** Aspose

## Связанные руководства

- [Как конвертировать PSD в растровые форматы изображений с помощью Aspose.PSD for Java](/psd/java/advanced-techniques/convert-psd-to-raster-formats/)
- [Сохранить PSD как JPEG и поддержка RGB‑цвета с Aspose.PSD Java](/psd/java/advanced-psd-layer-features-effects/support-rgb-color-psd-files/)
- [Изменение размера изображения с Aspose.PSD for Java – рисование фигур и базовые операции с изображениями](/psd/java/basic-image-operations/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}