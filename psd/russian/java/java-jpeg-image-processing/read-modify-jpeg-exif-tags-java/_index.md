---
date: 2026-10-03
description: Узнайте, как на Java считывать метаданные изображения и изменять теги
  JPEG EXIF с помощью Aspose.PSD for Java в этом пошаговом руководстве, идеальном
  для разработчиков, эффективно работающих с метаданными изображений.
keywords:
- java read image metadata
- read EXIF tags Java
- modify JPEG metadata Java
- Aspose.PSD Java
lastmod: 2026-10-03
linktitle: Чтение и изменение тегов JPEG EXIF на Java
og_description: Узнайте, как на Java считывать метаданные изображения и изменять теги
  JPEG EXIF с помощью Aspose.PSD for Java. Это руководство демонстрирует пошаговый
  код для извлечения и обновления информации EXIF.
og_image_alt: Guide showing how to java read image metadata and edit JPEG EXIF tags
  using Aspose.PSD for Java
og_title: Как на Java считывать метаданные изображения и изменять теги JPEG EXIF
schemas:
- author: Aspose
  dateModified: '2026-10-03'
  description: Learn how to java read image metadata and modify JPEG EXIF tags with
    Aspose.PSD for Java in this step‑by‑step guide, perfect for developers handling
    image metadata efficiently.
  headline: How to java read image metadata and modify JPEG EXIF tags
  type: TechArticle
- description: Learn how to java read image metadata and modify JPEG EXIF tags with
    Aspose.PSD for Java in this step‑by‑step guide, perfect for developers handling
    image metadata efficiently.
  name: How to java read image metadata and modify JPEG EXIF tags
  steps:
  - name: '**Java Development Kit (JDK)** – make sure you have JDK 11 or newer. You
      can download it from the [Oracle website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).'
    text: '**Java Development Kit (JDK)** – make sure you have JDK 11 or newer. You
      can download it from the [Oracle website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).'
  - name: '**Aspose.PSD for Java library** – obtain the latest JAR from the [Aspose
      releases page](https://releases.aspose.com/psd/java/).'
    text: '**Aspose.PSD for Java library** – obtain the latest JAR from the [Aspose
      releases page](https://releases.aspose.com/psd/java/).'
  - name: '**IDE** – IntelliJ IDEA, Eclipse, or any editor you prefer.'
    text: '**IDE** – IntelliJ IDEA, Eclipse, or any editor you prefer.'
  - name: '**Basic Java knowledge** – you should be comfortable with creating projects
      and adding external JARs.'
    text: '**Basic Java knowledge** – you should be comfortable with creating projects
      and adding external JARs.'
  type: HowTo
- questions:
  - answer: EXIF (Exchangeable Image File Format) metadata stores camera settings,
      timestamps, GPS coordinates, and other information embedded in JPEG and other
      image files.
    question: What is EXIF data?
  - answer: You can get a free trial from the [Aspose releases page](https://releases.aspose.com/).
    question: Can I use Aspose.PSD for Java for free?
  - answer: Aspose.PSD for Java supports Java SE 7 and above.
    question: Is Aspose.PSD for Java compatible with all versions of Java?
  - answer: Check out the [documentation](https://reference.aspose.com/psd/java/)
      for more details.
    question: Where can I find more documentation on Aspose.PSD for Java?
  - answer: You can get support from the [Aspose PSD support forum](https://forum.aspose.com/c/psd/34/).
    question: How do I get support for Aspose.PSD for Java?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- java image metadata
- exif tags
- aspose psd
- jpeg metadata
- java tutorial
title: Как на Java считывать метаданные изображения и изменять теги JPEG EXIF
url: /ru/java/java-jpeg-image-processing/read-modify-jpeg-exif-tags-java/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Чтение и изменение тегов JPEG EXIF в Java

## Введение
Если вам нужно **java read image metadata** из JPEG‑файлов и изменить их программно, вы попали в нужное место. В этом руководстве мы пройдем процесс извлечения и обновления тегов EXIF с помощью Aspose.PSD for Java. К концу вы сможете получить детали камеры, ориентацию и пользовательские поля, а затем записать их обратно в файл — без использования графического редактора.

## Быстрые ответы
- **Какая библиотека обрабатывает JPEG EXIF в Java?** Aspose.PSD for Java.
- **Сколько строк кода требуется для чтения EXIF?** Около трёх строк после загрузки изображения.
- **Можно ли изменять теги EXIF?** Да, вы можете изменить любой стандартный или пользовательский тег и сохранить результат.
- **Поддерживаемые форматы изображений?** Более 150 форматов, включая PSD, JPEG, PNG, TIFF и BMP.
- **Минимальная версия Java?** Java 7 или выше.

## Почему использовать Aspose.PSD for Java?
Aspose.PSD поддерживает **150+ форматов изображений** и может обрабатывать файлы размером до **2 GB**, не загружая весь документ в память, что обеспечивает быстрые операции с метаданными при низком потреблении памяти для больших коллекций фотографий. Он также предоставляет простой API для чтения и записи данных EXIF, IPTC и XMP, делая пакетную обработку тысяч изображений эффективной и надёжной.

## Требования
1. **Java Development Kit (JDK)** – убедитесь, что у вас установлен JDK 11 или новее. Вы можете скачать его с [веб‑сайт Oracle](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).  
2. **Aspose.PSD for Java library** – получите последнюю JAR с [страницы выпусков Aspose](https://releases.aspose.com/psd/java/).  
3. **IDE** – IntelliJ IDEA, Eclipse или любой редактор по вашему выбору.  
4. **Basic Java knowledge** – вам следует уверенно создавать проекты и добавлять внешние JAR‑файлы.

## Что такое Java read image metadata?
Java read image metadata относится к процессу программного доступа к встроенной информации, такой как EXIF, IPTC и XMP, хранящейся в файлах изображений с помощью кода на Java. Эти метаданные могут включать настройки камеры, метки времени, координаты GPS, уведомления об авторском праве и пользовательские комментарии, позволяя приложениям организовывать, искать и манипулировать изображениями на основе их описательных данных.

## Импорт пакетов
Сначала добавьте JAR‑файл Aspose.PSD в classpath вашего проекта и импортируйте необходимые классы.

Пакет `com.aspose.psd` предоставляет основной API для загрузки изображений и доступа к их ресурсам.

```java
import com.aspose.psd.Image;
import com.aspose.psd.exif.JpegExifData;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.resources.Thumbnail4Resource;
import com.aspose.psd.fileformats.psd.resources.ThumbnailResource;
```

## Как читать метаданные изображений из JPEG‑файлов в Java?
Загрузите JPEG с помощью `PsdImage.load("image.jpg")`, найдите ресурс миниатюры, содержащий данные EXIF, а затем вызовите `ExifData.read()`, чтобы получить заполненный объект `ExifData`. Этот одношаговый подход предоставляет полный доступ ко всем стандартным полям EXIF и любым пользовательским тегам, которые вы могли добавить.

## Шаг 1: Загрузка PSD‑изображения
PsdImage — это класс Aspose.PSD, представляющий файл PSD и предоставляющий методы доступа к его ресурсам и метаданным.  
На этом этапе мы загрузим PSD‑изображение, из которого хотим прочитать данные EXIF. Убедитесь, что ваше изображение находится в правильном каталоге.

```java
String dataDir = "Your Document Directory";
PsdImage image = null;
try {
    image = (PsdImage) Image.load(dataDir + "1280px-Zebras_Serengeti.psd");
} catch (IOException e) {
    e.printStackTrace();
}
```

## Шаг 2: Итерация по ресурсам изображения
ThumbnailResource представляет собой миниатюру, хранящуюся в файле PSD и часто содержащую встроенные данные EXIF.  
После загрузки изображения следующий шаг — пройтись по его ресурсам, чтобы найти ресурс миниатюры, который обычно содержит данные EXIF.

```java
for (int i = 0; i < image.getImageResources().length; i++) {
    if (image.getImageResources()[i] instanceof ThumbnailResource) {
        ThumbnailResource thumbnail = (ThumbnailResource) image.getImageResources()[i];
        // Proceed to next step
    }
}
```

## Шаг 3: Извлечение данных EXIF
JpegExifData — это класс, содержащий информацию EXIF, извлечённую из JPEG‑изображения, позволяющий читать и изменять отдельные теги.  
Теперь, когда у нас есть ресурс миниатюры, мы можем извлечь из него данные EXIF. Данные EXIF включают ценную информацию, такую как имя владельца камеры, значение диафрагмы, ориентацию и многое другое.

```java
JpegExifData exifData = thumbnail.getJpegOptions().getExifData();
if (exifData != null) {
    System.out.println("Camera Owner Name: " + exifData.getCameraOwnerName());
    System.out.println("Aperture Value: " + exifData.getApertureValue());
    System.out.println("Orientation: " + exifData.getOrientation());
    System.out.println("Focal Length: " + exifData.getFocalLength());
    System.out.println("Compression: " + exifData.getCompression());
}
```

## Шаг 4: Изменение данных EXIF
После чтения данных EXIF вы можете захотеть изменить некоторые их поля. Вот как это сделать:

```java
if (exifData != null) {
    exifData.setCameraOwnerName("New Camera Owner");
    exifData.setApertureValue(3.5);
    exifData.setOrientation(1);
    exifData.setFocalLength(35.0);
    exifData.setCompression(6);
    thumbnail.getJpegOptions().setExifData(exifData);
}
```

## Шаг 5: Сохранение изменений
Наконец, после изменения данных EXIF сохраните изменения в новый PSD‑файл.

```java
try {
    image.save(dataDir + "Modified_Zebras_Serengeti.psd");
} catch (IOException e) {
    e.printStackTrace();
}
```

## Распространённые проблемы и решения
- **Missing thumbnail resource** – Некоторые JPEG‑файлы хранят EXIF непосредственно в заголовке основного изображения. Если ресурс миниатюры отсутствует, используйте `image.getExifData()`.  
- **Large files cause OutOfMemoryError** – Убедитесь, что JVM запущена с достаточным объёмом кучи (`-Xmx2g`) или обрабатывайте изображение в режиме потоковой передачи с помощью `PsdImage.load(inputStream, loadOptions)`.  
- **Unsupported tag types** – Aspose.PSD поддерживает все стандартные теги EXIF; пользовательские теги могут потребовать ручной обработки на уровне байтов.

## Часто задаваемые вопросы

**Q: Что такое данные EXIF?**  
A: Метаданные EXIF (Exchangeable Image File Format) хранят настройки камеры, метки времени, координаты GPS и другую информацию, встроенную в JPEG и другие файлы изображений.

**Q: Можно ли использовать Aspose.PSD for Java бесплатно?**  
A: Вы можете получить бесплатную пробную версию со [страницы выпусков Aspose](https://releases.aspose.com/).

**Q: Совместим ли Aspose.PSD for Java со всеми версиями Java?**  
A: Aspose.PSD for Java поддерживает Java SE 7 и выше.

**Q: Где можно найти дополнительную документацию по Aspose.PSD for Java?**  
A: Ознакомьтесь с [документацией](https://reference.aspose.com/psd/java/) для получения более подробной информации.

**Q: Как получить поддержку по Aspose.PSD for Java?**  
A: Вы можете получить поддержку на [форуме поддержки Aspose PSD](https://forum.aspose.com/c/psd/34/).

## Заключение
Следуя этим шагам, вы сможете **java read image metadata** из любого JPEG, настроить необходимые поля EXIF и записать обновлённые данные обратно в файл — всё это с помощью нескольких строк чистого кода на Java. Богатый API Aspose.PSD делает работу с метаданными надёжной и производительной, позволяя интегрировать её в конвейеры пакетной обработки, инструменты управления фотографиями или любое приложение, которому необходимо работать с информацией об изображениях.

---

**Последнее обновление:** 2026-10-03  
**Тестировано с:** Aspose.PSD for Java 24.5  
**Автор:** Aspose

## Связанные руководства

- [Чтение информации о конкретных тегах EXIF в Java с Aspose (asp)](/psd/java/java-jpeg-image-processing/read-specific-exif-tags-info-java/)
- [Создание XMP‑метаданных в PSD‑файлах с помощью Aspose.PSD for Java](/psd/java/image-editing/create-xmp-metadata/)
- [Изменение размера изображения с Aspose.PSD for Java – рисование фигур и базовые операции с изображениями](/psd/java/basic-image-operations/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}