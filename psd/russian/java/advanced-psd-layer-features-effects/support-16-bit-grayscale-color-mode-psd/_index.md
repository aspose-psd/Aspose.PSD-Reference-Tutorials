---
date: 2026-09-28
description: Узнайте, как экспортировать PSD в PNG, задав режим цвета PSD как 16‑битный
  градационный серый, используя Aspose.PSD for Java. Пошаговое руководство с примерами
  кода.
keywords:
- export psd as png
- how to convert psd to png
- 16-bit grayscale java
lastmod: 2026-09-28
linktitle: Экспорт PSD в PNG – 16‑битный градационный серый – Java
og_description: Экспортируйте PSD в PNG с 16‑битным градационным серым, используя
  Aspose.PSD for Java. Следуйте этому пошаговому руководству, чтобы сохранить 65 536
  оттенков серого.
og_image_alt: Guide showing how to export PSD as PNG with 16-bit grayscale using Aspose.PSD
  Java
og_title: Экспорт PSD в PNG с 16‑битным градационным серым в Java – руководство Aspose.PSD
schemas:
- author: Aspose
  dateModified: '2026-09-28'
  description: Learn how to export PSD as PNG while setting PSD color mode to 16-bit
    grayscale using Aspose.PSD for Java. Step‑by‑step guide with code examples.
  headline: How to export PSD as PNG with 16‑bit grayscale color mode in Java
  type: TechArticle
- description: Learn how to export PSD as PNG while setting PSD color mode to 16-bit
    grayscale using Aspose.PSD for Java. Step‑by‑step guide with code examples.
  name: How to export PSD as PNG with 16‑bit grayscale color mode in Java
  steps:
  - name: '**Java Development Kit (JDK)** – Install the latest JDK from [Oracle''s
      site](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).'
    text: '**Java Development Kit (JDK)** – Install the latest JDK from [Oracle''s
      site](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).'
  - name: '**Aspose.PSD for Java library** – Download the JAR from the [Aspose download
      page](https://releases.aspose.com/psd/java/).'
    text: '**Aspose.PSD for Java library** – Download the JAR from the [Aspose download
      page](https://releases.aspose.com/psd/java/).'
  - name: '**An IDE** – IntelliJ IDEA, Eclipse, or Visual Studio Code works perfectly.'
    text: '**An IDE** – IntelliJ IDEA, Eclipse, or Visual Studio Code works perfectly.'
  - name: '**Basic Java knowledge** – You should be comfortable creating classes,
      handling exceptions, and working with file paths.'
    text: '**Basic Java knowledge** – You should be comfortable creating classes,
      handling exceptions, and working with file paths.'
  - name: '**A sample PSD file** – Create one in Adobe Photoshop or grab a free sample
      online.'
    text: '**A sample PSD file** – Create one in Adobe Photoshop or grab a free sample
      online.'
  type: HowTo
- questions:
  - answer: It provides 65 536 shades of gray, delivering far more tonal detail than
      the standard 8‑bit (256 shades).
    question: What is 16‑bit grayscale color mode?
  - answer: Absolutely! Aspose.PSD supports RGB, CMYK, Lab, Indexed, and many other
      color modes.
    question: Can I use Aspose.PSD for non‑grayscale images?
  - answer: Yes, you can try a free trial version of Aspose.PSD. Just head to the
      [Aspose download page](https://releases.aspose.com/).
    question: Is there a trial version of Aspose.PSD?
  - answer: Check the official [documentation](https://reference.aspose.com/psd/java/)
      for in‑depth tutorials, API references, and sample projects.
    question: Where can I find more Aspose.PSD examples?
  - answer: You can buy a license by visiting the [Aspose purchase page](https://purchase.aspose.com/buy).
    question: How do I purchase a license for Aspose.PSD?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- convert psd
- Aspose.PSD
- Java image processing
title: Как экспортировать PSD в PNG с 16‑битным градационным серым в Java
url: /ru/java/advanced-psd-layer-features-effects/support-16-bit-grayscale-color-mode-psd/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Экспорт PSD в PNG с 16‑битовым градационным режимом в Java

## Введение
Экспорт PSD в PNG при сохранении 16‑битового градационного режима даёт глубину профессиональной фотографии и универсальную совместимость PNG. В этом руководстве вы узнаете, как **установить цветовой режим PSD в 16‑битовый градационный** и затем **экспортировать PSD в PNG** с помощью Aspose.PSD for Java. Руководство охватывает всё от требований до устранения неполадок, чтобы вы могли интегрировать процесс в любой Java‑ориентированный конвейер обработки изображений.

## Быстрые ответы
- **Что подразумевается под «экспортом PSD в PNG»?** Загрузить PSD, при необходимости изменить его цветовой режим и сохранить его как файл PNG.  
- **Какой класс Aspose обрабатывает конвертацию?** `PsdImage` загружает PSD, а `PngOptions` определяет параметры вывода PNG.  
- **Нужна ли лицензия для продакшна?** Да — пробная версия подходит для тестирования, но для коммерческого использования требуется платная лицензия.  
- **Можно ли сохранить 16‑битовую глубину в PNG?** Абсолютно, используя `PngColorType.GrayscaleWithAlpha`.  
- **Какие IDE поддерживаются?** Любая Java IDE — IntelliJ IDEA, Eclipse, VS Code или NetBeans.

## Что такое экспорт PSD в PNG?
Экспорт PSD в PNG — это процесс преобразования документа Adobe Photoshop (PSD) в файл Portable Network Graphics (PNG) с сохранением пиксельных данных и цветовой глубины изображения. Такое преобразование часто используется для публикации высококачественных градационных ресурсов в интернете без потери тональных деталей.

## Почему экспортировать PSD в PNG с 16‑битовым градационным режимом?
Экспорт в PNG при сохранении 16‑битового градационного режима сохраняет 65 536 оттенков серого, что обеспечивает значительно большую тональную насыщенность по сравнению с 8‑битовыми изображениями. Универсальная поддержка PNG гарантирует, что файлы будут отображаться в браузерах, мобильных приложениях и настольных редакторах без потерь, а без потерь сжатие Aspose.PSD гарантирует отсутствие артефактов.

## Требования
Перед началом убедитесь, что у вас есть следующие элементы:

1. **Java Development Kit (JDK)** – Установите последнюю JDK с [Oracle's site](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).  
2. **Aspose.PSD for Java library** – Скачайте JAR с [Aspose download page](https://releases.aspose.com/psd/java/).  
3. **IDE** – IntelliJ IDEA, Eclipse или Visual Studio Code работают прекрасно.  
4. **Базовые знания Java** – Вы должны уверенно создавать классы, обрабатывать исключения и работать с файловыми путями.  
5. **Пример файла PSD** – Создайте его в Adobe Photoshop или возьмите бесплатный образец в интернете.

## Как экспортировать PSD в PNG шаг за шагом

## Как установить цветовой режим PSD в 16‑битовый градационный?
`PsdImage` — класс Aspose.PSD, который загружает и представляет PSD‑файл в памяти.  
`ColorMode` — перечисление, определяющее цветовой режим изображения PSD.  

Загрузите PSD с помощью `PsdImage`, измените его цветовой режим, используя свойство `ColorMode`, а затем сохраните изменённый файл. Эта операция полностью выполняется в памяти, устраняя необходимость в промежуточных файлах и обеспечивая быструю и эффективную конвертацию.

```java
import com.aspose.psd.*;
import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.fileformats.psd.ColorModes;
import com.aspose.psd.fileformats.psd.CompressionMethod;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.PngOptions;
import com.aspose.psd.imageoptions.PsdOptions;
import com.aspose.psd.system.Enum;
```

Эти импорты дают вам доступ к функционалу, который вы будете использовать для манипуляции PSD‑файлами, установки цветового режима и экспорта результата в PNG.

## Как определить исходный и целевой каталоги?
`File` — класс java.io, представляющий путь к файлу или каталогу в файловой системе.  

Вам нужно указать программе, где читать исходный PSD и куда записывать конвертированный PNG. Использование абсолютных или относительных путей работает, но держите их согласованными в разных средах, чтобы избежать ошибок разрешения путей.

```java
String sourceDir = "Your Source Directory"; // Change to your source directory
String outputDir = "Your Document Directory"; // Change to your output directory
```

Замените строки‑заполнители фактическими путями на вашем компьютере.

## Как инкапсулировать логику конвертации в переиспользуемый метод?
`convertPsdToPng` — пользовательский метод, инкапсулирующий все шаги, необходимые для конвертации PSD‑файла в PNG с дополнительными настройками.  

Создание отдельного метода позволяет переиспользовать те же шаги конвертации для нескольких файлов или разных настроек. Передавайте параметры, такие как путь к источнику, папка назначения и необязательный уровень сжатия, делая рабочий процесс гибким и поддерживаемым.

```java
class LocalScopeExtension {
    void saveToPsdThenLoadAndSaveToPng(
        String file,
        short colorMode,
        short channelBitsCount,
        short channelsCount,
        short compression,
        int layerNumber) {
```

Этот метод позволяет **установить цветовой режим PSD** и затем **экспортировать PSD в PNG** в одном потоке.

## Как загрузить PSD и применить 16‑битовый градационный режим?
`PsdImage` — класс Aspose.PSD, который загружает PSD‑файл в память.  
`ColorMode.GRAYSCALE_16` — значение перечисления, устанавливающее изображение в 16‑битовый градационный режим.  
`channelBitsCount` — свойство, указывающее количество битов на канал.  

Внутри метода конвертации сформируйте полные пути к файлам, создайте экземпляр `PsdImage` и измените его `ColorMode` на `ColorMode.GRAYSCALE_16`. Свойство `channelBitsCount` должно быть установлено в 16, чтобы сохранить высокую битовую глубину и обеспечить сохранение всей тональной информации.

```java
String filePath = sourceDir + file + ".psd";
String postfix = Enum.getName(ColorModes.class, colorMode) + channelBitsCount + "_" +
                 channelsCount + "_" + Enum.getName(CompressionMethod.class, compression);
String exportPath = outputDir + file + postfix + ".psd";
String pngExportPath = outputDir + file + postfix + ".png";
// Load a predefined 16-bit grayscale PSD
PsdImage image = (PsdImage)Image.load(filePath);
```

`postfix` помогает отслеживать настройки, использованные для каждого экспортированного файла.

## Как нарисовать тонкую рамку на изображении (необязательный шаг)?
`Graphics` — класс, предоставляющий возможности рисования на холсте `PsdImage`.  

При желании можно нарисовать серый прямоугольник вокруг изображения, чтобы сделать вывод более заметным во время тестирования. Этот шаг демонстрирует работу со слоями и графическими объектами, а прямоугольник рассчитывается динамически, поэтому остаётся центрированным независимо от размеров изображения.

```java
try {
    RasterCachedImage raster = layerNumber >= 0 ? image.getLayers()[layerNumber] : image;
    // Draw a gray inner border around the perimeter of the layer
    Graphics graphics = new Graphics(raster);
    int width = raster.getWidth();
    int height = raster.getHeight();
    Rectangle rect = new Rectangle(
        width / 3,
        height / 3,
        width - (2 * (width / 3)) - 1,
        height - (2 * (height / 3)) - 1);
    graphics.drawRectangle(new Pen(Color.getDarkGray(), 1), rect);
```

Прямоугольник рассчитывается динамически, поэтому остаётся центрированным независимо от размеров изображения.

## Как сохранить изменённый PSD с новым цветовым режимом?
`PsdOptions` — класс, контролирующий, как сохраняется PSD‑файл, включая настройки цветового режима и битовой глубины.  

После рисования (или пропуска этого шага) вызовите `save` у экземпляра `PsdImage`, передав объект `PsdOptions`, который сохраняет конфигурацию 16‑битового градационного режима. Это гарантирует, что сохранённый PSD сохраняет желаемый цветовой режим без потери данных.

```java
    // Save a copy of PSD with specific characteristics
    PsdOptions psdOptions = new PsdOptions();
    psdOptions.setColorMode(colorMode);
    psdOptions.setChannelBitsCount(channelBitsCount);
    psdOptions.setChannelsCount(channelsCount);
    psdOptions.setCompressionMethod(compression);
    image.save(exportPath, psdOptions);
}
```

## Как конвертировать PSD в PNG, сохранив 16‑битовую глубину?
`PngOptions` — класс, определяющий параметры вывода PNG, такие как тип цвета и уровень сжатия.  
`PngColorType.GrayscaleWithAlpha` — значение перечисления, сохраняющее 16‑битовые градационные данные с альфа‑каналом.  

Загрузите только что сохранённый PSD, настройте `PngOptions` с `PngColorType.GrayscaleWithAlpha` и вызовите `save`. Это сохраняет 16‑битовые градационные данные внутри PNG‑файла, обеспечивая безпотерьное, высококачественное изображение, подходящее для дальнейшей обработки или распространения.

```java
finally {
    image.dispose();
}
// Load the saved PSD
PsdImage image1 = (PsdImage)Image.load(exportPath);
try {
    // Convert the saved PSD to a grayscale PNG image
    PngOptions pngOptions = new PngOptions();
    pngOptions.setColorType(PngColorType.GrayscaleWithAlpha);
    image1.save(pngExportPath, pngOptions); // here should be no exception
}
finally {
    image1.dispose();
}
```

Теперь вы успешно **экспортировали PSD в PNG**, сохранив высококачественные 16‑битовые градационные данные.

## Распространённые проблемы и решения
| Проблема | Почему происходит | Решение |
|----------|-------------------|---------|
| **«Unsupported color type» исключение** | Попытка сохранить PSD с неподдерживаемой конфигурацией каналов. | Убедитесь, что `channelBitsCount` соответствует реальной битовой глубине (16), а `channelsCount` правильный для градации (1). |
| **Файл не найден** | Неправильный путь к исходному каталогу. | Дважды проверьте строку `sourceDir` и убедитесь, что PSD‑файл существует по указанному пути. |
| **Полученный PNG выглядит чёрным** | PNG сохранён без правильной обработки альфа‑канала. | Используйте `PngColorType.GrayscaleWithAlpha`, как показано выше. |
| **Переполнение памяти при больших PSD** | Загрузка всего файла в память. | Включите режим потоковой загрузки через `PsdImage.load(inputStream, new LoadOptions())` для эффективной обработки больших файлов. |

## Часто задаваемые вопросы

**В: Что такое 16‑битовый градационный цветовой режим?**  
О: Он предоставляет 65 536 оттенков серого, обеспечивая гораздо большую тональную детализацию, чем стандартный 8‑битовый (256 оттенков).

**В: Можно ли использовать Aspose.PSD для не‑градационных изображений?**  
О: Абсолютно! Aspose.PSD поддерживает RGB, CMYK, Lab, Indexed и многие другие цветовые режимы.

**В: Есть ли пробная версия Aspose.PSD?**  
О: Да, вы можете попробовать бесплатную пробную версию Aspose.PSD. Просто перейдите на [Aspose download page](https://releases.aspose.com/).

**В: Где я могу найти больше примеров Aspose.PSD?**  
О: Ознакомьтесь с официальной [documentation](https://reference.aspose.com/psd/java/) для подробных руководств, справочников API и примеров проектов.

**В: Как приобрести лицензию для Aspose.PSD?**  
О: Вы можете купить лицензию, посетив [Aspose purchase page](https://purchase.aspose.com/buy).

**Последнее обновление:** 2026-09-28  
**Тестировано с:** Aspose.PSD for Java 24.12 (latest at time of writing)  
**Автор:** Aspose

## Связанные руководства

- [Конвертировать PSD в PNG с указанной битовой глубиной с помощью Aspose.PSD для Java](/psd/java/optimizing-png-files/specify-png-bit-depth/)
- [Экспортировать PSD в PNG с эффектами слоёв, используя Aspose.PSD для Java](/psd/java/psd-image-modification-conversion/apply-layer-effects-psd-files/)
- [Сохранить PSD как JPEG и поддержать RGB‑цвет с Aspose.PSD Java](/psd/java/advanced-psd-layer-features-effects/support-rgb-color-psd-files/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}