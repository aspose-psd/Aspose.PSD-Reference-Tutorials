---
date: 2026-10-08
description: Узнайте, как читать EXIF‑теги в Java с помощью Aspose.PSD for Java (asp)
  в нашем пошаговом руководстве и улучшите возможности обработки изображений.
keywords:
- read exif tags java
- java exif tag extraction
- java image metadata extraction
lastmod: 2026-10-08
linktitle: Чтение конкретных EXIF‑тегов в Java
og_description: 'Чтение EXIF‑тегов: разработчики Java могут быстро извлекать метаданные
  изображений с помощью Aspose.PSD. Это руководство проведёт вас через загрузку PSD,
  поиск ресурсов миниатюр и вывод ключевых полей EXIF, таких как WhiteBalance и ISO
  speed.'
og_image_alt: Guide showing how to read EXIF tags from PSD files in Java using Aspose.PSD
og_title: Как читать EXIF‑теги в Java с Aspose.PSD
schemas:
- author: Aspose
  dateModified: '2026-10-08'
  description: Learn how to read EXIF tags in Java using Aspose.PSD for Java (asp)
    with our step‑by‑step tutorial, and boost your image processing capabilities.
  headline: How to read EXIF tags in Java with Aspose.PSD
  type: TechArticle
- description: Learn how to read EXIF tags in Java using Aspose.PSD for Java (asp)
    with our step‑by‑step tutorial, and boost your image processing capabilities.
  name: How to read EXIF tags in Java with Aspose.PSD
  steps:
  - name: 'Java Development Kit (JDK): Ensure you have JDK installed on your machine.
      You can download it from the [Oracle JDK website](https://www.oracle.com/java/technologies/javase-downloads.html).'
    text: 'Java Development Kit (JDK): Ensure you have JDK installed on your machine.
      You can download it from the [Oracle JDK website](https://www.oracle.com/java/technologies/javase-downloads.html).'
  - name: 'Aspose.PSD for Java: Download the library from the [Aspose.PSD for Java
      download page](https://releases.aspose.com/psd/java/).'
    text: 'Aspose.PSD for Java: Download the library from the [Aspose.PSD for Java
      download page](https://releases.aspose.com/psd/java/).'
  - name: 'Integrated Development Environment (IDE): An IDE like IntelliJ IDEA, Eclipse,
      or NetBeans will make coding more convenient.'
    text: 'Integrated Development Environment (IDE): An IDE like IntelliJ IDEA, Eclipse,
      or NetBeans will make coding more convenient.'
  - name: 'PSD file: A PSD file with EXIF data. You can use the sample provided in
      this tutorial or any other PSD file with EXIF tags.'
    text: 'PSD file: A PSD file with EXIF data. You can use the sample provided in
      this tutorial or any other PSD file with EXIF tags.'
  type: HowTo
- questions:
  - answer: Aspose.PSD (asp)
    question: What library reads EXIF data from PSD in Java?
  - answer: WhiteBalance, PixelXDimension, PixelYDimension, ISOSpeed, FocalLength,
      and more.
    question: Which tags can be extracted?
  - answer: Yes, a commercial license is required; a free trial is available.
    question: Do I need a license for production?
  - answer: The same API supports PNG, JPEG, TIFF via Java image metadata extraction.
    question: Can I use this with other image formats?
  - answer: About 10‑15 minutes for a basic read‑only scenario.
    question: How long does implementation take?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- read exif tags java
- Aspose.PSD
- java image metadata extraction
- EXIF extraction
- PSD processing
title: Как читать EXIF‑теги в Java с Aspose.PSD
url: /ru/java/java-jpeg-image-processing/read-specific-exif-tags-info-java/
weight: 19
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Чтение конкретных тегов EXIF в Java с Aspose (asp)

## Введение
Если вам нужно **read EXIF tags in Java**, Aspose.PSD (asp) предлагает чистый, чисто‑Java API, который работает без Photoshop. В этом руководстве вы узнаете, как извлечь данные EXIF из изображения PSD, выбрать только нужные вам теги и вывести их в консоль. Мы рассмотрим всё, от настройки среды разработки до получения метаданных, таких как WhiteBalance, ISO speed и фокусное расстояние. Давайте начнём!

## Быстрые ответы
- **What library reads EXIF data from PSD in Java?** Aspose.PSD (asp)  
- **Which tags can be extracted?** WhiteBalance, PixelXDimension, PixelYDimension, ISOSpeed, FocalLength и др.  
- **Do I need a license for production?** Да, требуется коммерческая лицензия; доступна бесплатная пробная версия.  
- **Can I use this with other image formats?** Тот же API поддерживает PNG, JPEG, TIFF через извлечение метаданных изображений Java.  
- **How long does implementation take?** Около 10‑15 минут для базового сценария только чтения.

## Что такое asp (Aspose.PSD for Java)?
Aspose.PSD for Java — это чисто‑Java библиотека, позволяющая разработчикам работать с файлами Adobe Photoshop (PSD, PSB) без установки Photoshop. Она предоставляет программный доступ к слоям, ресурсам и метаданным, включая теги EXIF, что делает её идеальной для задач **java image metadata extraction**.

## Почему использовать Aspose.PSD (asp) для извлечения EXIF?
Вы можете извлекать теги EXIF в Java всего двумя вызовами методов, а библиотека обрабатывает файлы до 2 ГБ без загрузки всего документа в память. Она поддерживает **30+ image formats** и сохраняет точные настройки камеры, обеспечивая детерминированные результаты в средах Windows, Linux и macOS.

## Требования
Прежде чем погрузиться в код, вам понадобится несколько вещей:

1. Java Development Kit (JDK): Убедитесь, что JDK установлен на вашем компьютере. Вы можете скачать его с сайта [Oracle JDK website](https://www.oracle.com/java/technologies/javase-downloads.html).  
2. Aspose.PSD for Java: Скачайте библиотеку со страницы [Aspose.PSD for Java download page](https://releases.aspose.com/psd/java/).  
3. Integrated Development Environment (IDE): IDE, такая как IntelliJ IDEA, Eclipse или NetBeans, сделает кодирование более удобным.  
4. PSD file: Файл PSD с данными EXIF. Вы можете использовать пример, предоставленный в этом руководстве, или любой другой файл PSD с тегами EXIF.

## Импорт пакетов
Импортируйте необходимые классы Aspose.PSD, такие как Image, PsdImage, ThumbnailResource и JpegExifData, для работы с файлами PSD.  
```java
import com.aspose.psd.Image;
import com.aspose.psd.exif.JpegExifData;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.resources.Thumbnail4Resource;
import com.aspose.psd.fileformats.psd.resources.ThumbnailResource;
```

## Шаг 1: загрузить изображение PSD
`Image.load()` загружает файл и возвращает объект Image, представляющий данные изображения.  
`PsdImage` — класс Aspose.PSD, предоставляющий функциональность, специфичную для PSD.  
Метод `Image.load()` загружает любой поддерживаемый файл изображения в память, возвращая общий объект `Image`, который можно привести к типу, специфичному для PSD.  
```java
String dataDir = "Your Document Directory";
PsdImage image = (PsdImage) Image.load(dataDir + "1280px-Zebras_Serengeti.psd");
```

На этом этапе мы загружаем файл PSD с помощью метода `Image.load()`. Класс `PsdImage` используется для представления изображения PSD, и мы приводим загруженное изображение к этому классу, чтобы получить доступ к специфичным для PSD функциям.

## Шаг 2: перебрать ресурсы изображения
`PsdImage.getResources()` возвращает коллекцию встроенных ресурсов, таких как миниатюры и данные EXIF.  
Вызов `PsdImage.getResources()` возвращает коллекцию всех встроенных ресурсов. Перебирая эту коллекцию, вы можете находить ресурсы миниатюр, содержащие метаданные EXIF.  
```java
for (int i = 0; i < image.getImageResources().length; i++) {
    if (image.getImageResources()[i] instanceof ThumbnailResource || 
        image.getImageResources()[i] instanceof Thumbnail4Resource) {
        // Further processing will be done here
    }
}
```

Мы проходим по ресурсам изображения с помощью цикла `for`. Цель — определить ресурсы, являющиеся экземплярами `ThumbnailResource` или `Thumbnail4Resource`, так как эти типы содержат данные EXIF.

## Шаг 3: извлечь данные EXIF
`ThumbnailResource.getJpegOptions()` предоставляет доступ к параметрам JPEG, включая метаданные EXIF.  
`JpegExifData` хранит отдельные значения тегов EXIF.  
Метод `ThumbnailResource.getJpegOptions()` предоставляет доступ к объекту `JpegExifData`, который содержит отдельные теги EXIF, такие как WhiteBalance, ISOSpeed и FocalLength.  
```java
if (image.getImageResources()[i] instanceof ThumbnailResource) {
    JpegExifData exif = ((ThumbnailResource) image.getImageResources()[i]).getJpegOptions().getExifData();
    if (exif != null) {
        System.out.println("Exif WhiteBalance: " + exif.getWhiteBalance());
        System.out.println("Exif PixelXDimension: " + exif.getPixelXDimension());
        System.out.println("Exif PixelYDimension: " + exif.getPixelYDimension());
        System.out.println("Exif ISOSpeed: " + exif.getISOSpeed());
        System.out.println("Exif FocalLength: " + exif.getFocalLength());
    }
}
```

Мы используем оператор `if`, чтобы проверить, является ли ресурс экземпляром `ThumbnailResource`. Если да, мы приводим его к этому типу и получаем его `JpegOptions` для доступа к `ExifData`. Затем выводим различные теги EXIF, такие как WhiteBalance, Pixel Dimensions, ISOSpeed и FocalLength.

## Распространённые проблемы и советы
- **Null EXIF data:** Некоторые файлы PSD могут не содержать ресурс миниатюры с информацией EXIF. Всегда проверяйте `null` перед доступом к значениям тегов.  
- **File path errors:** Используйте абсолютные пути или убедитесь, что рабочий каталог указывает на папку, содержащую ваш файл PSD.  
- **License restrictions:** Бесплатная пробная версия ограничивает количество страниц, которые можно обработать; перейдите на полную лицензию для неограниченного использования.

## Часто задаваемые вопросы
### Что такое данные EXIF?
Данные EXIF (Exchangeable Image File Format) — это метаданные, встроенные в файлы изображений, содержащие информацию, такую как настройки камеры, дата и время, а также размеры изображения.

### Можно ли редактировать данные EXIF с помощью Aspose.PSD?
Да, Aspose.PSD позволяет читать и изменять данные EXIF. Вы можете обновлять теги и сохранять изменения обратно в файл изображения.

### Бесплатен ли Aspose.PSD для Java?
Aspose.PSD предлагает бесплатную пробную версию, которую можно скачать со страницы [Aspose.PSD official releases page](https://releases.aspose.com/). Для полного набора функций необходимо приобрести лицензию.

### Какие другие форматы поддерживает Aspose.PSD?
Aspose.PSD поддерживает различные форматы Adobe Photoshop, включая PSD, PSB и другие. Он также предоставляет возможности конвертации этих форматов в PNG, JPEG, TIFF и т.д.

### Как получить поддержку для Aspose.PSD?
Вы можете получить поддержку через [forum](https://forum.aspose.com/c/psd/34) Aspose.PSD.

### Как это помогает с **java image metadata extraction**?
Используя объект `JpegExifData`, вы можете программно извлекать любой необходимый тег EXIF, что делает его надёжной основой для более широких задач извлечения метаданных в разных форматах изображений.

---

**Последнее обновление:** 2026-10-08  
**Тестировано с:** Aspose.PSD for Java 24.11 (последняя версия на момент написания)  
**Автор:** Aspose

## Связанные руководства

- [Чтение и изменение тегов JPEG Exif Java](/psd/java/java-jpeg-image-processing/read-modify-jpeg-exif-tags-java/)
- [Обработка JPEG изображений на Java](/psd/java/java-jpeg-image-processing/)
- [Как повернуть изображение на определённый угол с помощью Aspose.PSD for Java](/psd/java/advanced-image-manipulation/rotate-image-specific-angle/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}