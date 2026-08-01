---
date: 2026-08-01
description: Узнайте, как скорректировать гамму в Java image processing с Aspose.PSD,
  конвертировать PSD в TIFF и исправить выцветшие изображения в кратком руководстве.
keywords:
- how to adjust gamma
- fix washed out image
- java image processing
- convert psd to tiff
- server side image processing
lastmod: 2026-08-01
linktitle: Регулировка Gamma изображения
og_description: Узнайте, как скорректировать gamma в Java image processing с помощью
  Aspose.PSD – быстрая сервер‑side библиотека, исправляющая выцветшие изображения
  и конвертирующая PSD в TIFF всего за несколько строк кода.
og_image_alt: 'Guide: Adjust gamma in Java images with Aspose.PSD, convert PSD to
  TIFF'
og_title: как скорректировать gamma – Java processing с Aspose.PSD
schemas:
- author: Aspose
  dateModified: '2026-08-01'
  description: Learn how to adjust gamma in Java image processing with Aspose.PSD,
    convert PSD to TIFF, and fix washed‑out images in a concise tutorial.
  headline: How to Adjust Gamma in Java Image Processing with Aspose.PSD
  type: TechArticle
- description: Learn how to adjust gamma in Java image processing with Aspose.PSD,
    convert PSD to TIFF, and fix washed‑out images in a concise tutorial.
  name: How to Adjust Gamma in Java Image Processing with Aspose.PSD
  steps:
  - name: '**Java Development Environment** – Java 8 or later installed.'
    text: '**Java Development Environment** – Java 8 or later installed.'
  - name: '**Aspose.PSD Library** – Download and add the JAR to your project. See
      the official [documentation](https://reference.aspose.com/psd/java/).'
    text: '**Aspose.PSD Library** – Download and add the JAR to your project. See
      the official [documentation](https://reference.aspose.com/psd/java/).'
  - name: '**Sample Image** – A PSD file you want to process (e.g., `sample.psd`).'
    text: '**Sample Image** – A PSD file you want to process (e.g., `sample.psd`).'
  type: HowTo
- questions:
  - answer: Yes – the `adjustGamma` method accepts separate float values for red,
      green, and blue channels.
    question: Can I apply different gamma values to each colour channel?
  - answer: Absolutely. You can perform resizing, cropping, or colour corrections
      sequentially on the same `RasterImage` instance.
    question: Is it possible to chain multiple image adjustments before saving?
  - answer: Yes, each layer can be accessed and processed individually.
    question: Does Aspose.PSD support multi‑page PSD files?
  - answer: Aspose.PSD supports PNG, JPEG, BMP, and many other formats via their respective
      options classes.
    question: What format can I export to besides TIFF?
  - answer: Start with a moderate gamma (around 2.0) and preview the result; adjust
      downwards if the image looks too bright.
    question: How do I avoid a washed‑out image after gamma correction?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- adjust gamma
- Aspose.PSD
- Java image processing
- PSD to TIFF
- server side processing
title: Как скорректировать гамму в Java Image Processing с Aspose.PSD
url: /ru/java/advanced-techniques/adjust-gamma/
weight: 23
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Как настроить гамму в обработке изображений Java с Aspose.PSD

## Введение

Если вы работаете над **java image processing**, изучение **как настроить гамму** является базовой техникой улучшения яркости и контрастности без потери деталей. В этом руководстве мы покажем, как использовать **Aspose.PSD for Java** для применения коррекции гаммы к файлу PSD, **convert PSD to TIFF**, и избежать **выцветшего изображения**. Вы увидите, почему этот подход быстрый, надёжный и идеален для **server‑side image processing** конвейеров.

## Быстрые ответы
- **Что делает коррекция гаммы?** Она переназначает значения яркости, делая тёмные области светлее или светлые — темнее, при этом сохраняет общие детали.  
- **Какая библиотека обрабатывает изображения?** Aspose.PSD for Java предоставляет специальный метод `adjustGamma` для растровых изображений.  
- **Могу ли я конвертировать PSD в TIFF в том же процессе?** Да — после корректировки гаммы вы можете сохранить изображение напрямую в TIFF, используя `TiffOptions`.  
- **Нужна ли лицензия для разработки?** Бесплатная пробная версия подходит для тестирования; для использования в продакшене требуется коммерческая лицензия.  
- **Какая версия Java поддерживается?** Aspose.PSD поддерживает Java 8 и более новые версии.

## Что такое коррекция гаммы в Java?

Коррекция гаммы изменяет нелинейную зависимость между закодированными значениями пикселей и отображаемой яркостью. Настраивая кривую гаммы, вы можете **исправить выцветшее изображение** или улучшить детали в тенях без переэкспонирования светлых областей. Она работает, применяя функцию степенного закона к каждому пикселю, что делает тёмные тона светлее и сжимает светлые области, создавая более естественный визуальный вид.

## Почему использовать Aspose.PSD для коррекции гаммы?

Aspose.PSD — это **java image processing library**, которая скрывает сложности формата PSD. Она поддерживает обработку файлов до 2 ГБ, работает с более чем 50 различными форматами изображений и предоставляет простой вызов `adjustGamma`, что делает её идеальной для **java gamma correction** и **convert PSD to TIFF** рабочих процессов.

## Требования

1. **Java Development Environment** – установлен Java 8 или новее.  
2. **Aspose.PSD Library** – Скачайте и добавьте JAR в ваш проект. См. официальную [documentation](https://reference.aspose.com/psd/java/).  
3. **Sample Image** – PSD‑файл, который вы хотите обработать (например, `sample.psd`).  

## Импорт пакетов

Прежде чем начать, импортируйте необходимые пространства имён, которые дают доступ к работе с растром и параметрам форматов файлов.

## Шаг 1: Загрузка изображения

Класс `RasterImage` представляет растровые данные пикселей слоя PSD в памяти. Однократная загрузка изображения и его кэширование снижают нагрузку на память при последующих корректировках.

## Шаг 2: Коррекция гаммы

Загрузите ваш PSD с помощью `new RasterImage("sample.psd")` и вызовите `rasterImage.adjustGamma(2.0f)` — эта единственная строка применяет гамму 2.0 ко всем цветовым каналам, осветляя тени и сохраняя светлые области нетронутыми. При необходимости можно передать отдельные значения для красного, зелёного и синего каналов.

## Шаг 3: Создание TiffOptions

`TiffOptions` позволяет управлять сжатием, битами на образец и другими настройками, специфичными для TIFF. Установка 8‑битного образца (`{8,8,8}`) сохраняет разумный размер TIFF‑файла, одновременно поддерживая точность цветов.

## Шаг 4: Сохранение полученного изображения

Вызовите `rasterImage.save("output.tif", tiffOptions)`, чтобы записать обработанное изображение на диск. После сохранения вы можете передать TIFF в последующие системы, такие как службы печати или веб‑API.

## Распространённые сценарии использования

- **Automated graphics pipelines** – Корректировать гамму в режиме реального времени перед генерацией миниатюр.  
- **Batch conversion tools** – Конвертировать большие архивы PSD в TIFF с нормализацией яркости.  
- **Web services** – Предоставить конечную точку, принимающую PSD, применяющую коррекцию гаммы и возвращающую TIFF для клиента.

## Распространённые проблемы и решения

| Проблема | Почему происходит | Как исправить |
|----------|-------------------|---------------|
| **Изображение выглядит выцветшим** | Значение гаммы слишком высоко (например, > 2.5) | Уменьшите коэффициент гаммы до значения между 1.8 и 2.2. |
| **`rasterImage.isCached()` returns false** | Изображение ещё не загружено в память | Вызовите `rasterImage.cacheData()` перед корректировкой гаммы. |
| **Размер TIFF‑файла большой** | Биты на образец установлены в 16‑бит | Используйте 8‑битный образец (`{8,8,8}`), как показано в примере. |

## Часто задаваемые вопросы

**Q: Могу ли я применять разные значения гаммы к каждому цветному каналу?**  
A: Да — метод `adjustGamma` принимает отдельные значения float для каналов красного, зелёного и синего.

**Q: Можно ли цепочкой применять несколько корректировок изображения перед сохранением?**  
A: Абсолютно. Вы можете последовательно выполнять изменение размера, обрезку или цветовые коррекции на том же экземпляре `RasterImage`.

**Q: Поддерживает ли Aspose.PSD многостраничные PSD‑файлы?**  
A: Да, каждый слой можно получить и обработать отдельно.

**Q: В какой формат ещё можно экспортировать, кроме TIFF?**  
A: Aspose.PSD поддерживает PNG, JPEG, BMP и многие другие форматы через соответствующие классы параметров.

**Q: Как избежать выцветшего изображения после коррекции гаммы?**  
A: Начните с умеренной гаммы (около 2.0) и просмотрите результат; при необходимости уменьшите значение, если изображение выглядит слишком ярким.

## Заключение

Поздравляем! Вы успешно изучили **how to adjust gamma** в рабочем процессе **java image processing**, конвертировали PSD в TIFF и избежали распространённых ошибок, таких как **выцветшее изображение**. Этот подход даёт вам точный контроль над яркостью и контрастом, делая его идеальным для автоматизированных графических конвейеров, веб‑служб или настольных утилит.

---

**Последнее обновление:** 2026-08-01  
**Тестировано с:** Aspose.PSD 24.11 for Java  
**Автор:** Aspose  

{{< blocks/products/products-backtop-button >}}

## Связанные руководства

- [Руководство по обработке изображений Java — Регулировка яркости изображения с Aspose.PSD for Java](/psd/java/advanced-techniques/adjust-brightness/)
- [Как конвертировать PSD в TIFF и скорректировать контраст с Aspose.PSD for Java](/psd/java/advanced-techniques/adjust-contrast/)
- [Конвертировать PSD в изображение в Java — Применить корректирующие слои с Aspose.PSD](/psd/java/advanced-psd-layer-features-effects/apply-adjustment-layers-psd-files/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.psd.fileformats.tiff.enums.TiffPhotometrics;
import com.aspose.psd.imageoptions.TiffOptions;
```

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

// Load an existing image into an instance of RasterImage class
Image image = Image.load(sourceFile);

// Cast object of Image to RasterImage
RasterImage rasterImage = (RasterImage)image;

// Check if RasterImage is cached for better performance
if (!rasterImage.isCached()) {
    rasterImage.cacheData();
}
```

```java
// Adjust the gamma
rasterImage.adjustGamma(2.2f, 2.2f, 2.2f);
```

```java
// Create an instance of TiffOptions for the resultant image
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
int[] ushort = { 8, 8, 8 };
tiffOptions.setBitsPerSample(ushort);
tiffOptions.setPhotometric(TiffPhotometrics.Rgb);
```

```java
// Save the resultant image to TIFF format
String destName = dataDir + "AdjustGamma_out.tiff";
rasterImage.save(destName, tiffOptions);
```