---
date: 2026-04-05
description: Узнайте, как отрисовывать слой коррекции экспозиции в PSD‑файлах с помощью
  Aspose.PSD for Java. Пошаговое руководство с примерами кода по изменению и добавлению
  слоёв экспозиции.
keywords:
- render exposure adjustment layer
- exposure adjustment layer
- Aspose.PSD Java
linktitle: Отрисовка слоя коррекции экспозиции в PSD‑файлах — Java
second_title: Aspose.PSD Java API
title: Отображение слоя коррекции экспозиции в PSD‑файлах — Java
url: /ru/java/psd-layer-management-effects/render-exposure-adjustment-layer-psd/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Отрисовка слоя корректировки экспозиции в PSD‑файлах – Java

## Введение

Вы работаете с PSD‑файлами Photoshop и вам необходимо **render exposure adjustment layer** программно? Независимо от того, меняете ли вы существующие слои или добавляете новые, Aspose.PSD for Java предоставляет мощный и интуитивный способ выполнения этих задач. В этом руководстве мы пошагово покажем, как использовать Aspose.PSD for Java для отрисовки и изменения слоёв корректировки экспозиции в PSD‑файлах. К концу этого урока вы сможете настраивать параметры экспозиции в существующих слоях и добавлять новые слои корректировки экспозиции в ваши PSD‑файлы. Поехали!

## Быстрые ответы
- **What library is needed?** Aspose.PSD for Java
- **Can I edit an existing exposure layer?** Yes, you can change exposure, offset, and gamma correction.
- **How do I add a new exposure adjustment layer?** Use `addExposureAdjustmentLayer()` on a `PsdImage` instance.
- **Is PNG export supported?** Absolutely – use `PngOptions` to save the result as a PNG.
- **Do I need a license for production?** A commercial license is required for production use; a free trial is available.

## Что такое отрисовка слоя корректировки экспозиции?

Слой корректировки экспозиции — это недеструктивный слой Photoshop, который изменяет яркость, смещение и гамму подлежащего изображения. Отрисовка означает применение этих настроек, так что визуальный результат отражает корректировки, которые затем можно экспортировать в такие форматы, как PNG.

## Почему использовать Aspose.PSD for Java для отрисовки слоя корректировки экспозиции?

- **Full control** – manipulate layer properties without opening Photoshop.
- **Batch processing** – automate adjustments across many files.
- **Cross‑platform** – run on any system with a JDK.
- **Preserves PSD structure** – keep layers editable for future edits.

## Требования

1. **Java Development Kit (JDK)** – at least JDK 8.
2. **Aspose.PSD for Java** – download it from [here](https://releases.aspose.com/psd/java/).
3. **Basic Java knowledge** – you should be comfortable with standard Java syntax.
4. **IDE or Text Editor** – IntelliJ IDEA, Eclipse, VS Code, or any editor you prefer.

## Импорт пакетов

First, import the required Aspose.PSD classes:

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.adjustmentlayers.ExposureLayer;
import com.aspose.psd.imageoptions.PngOptions;
```

## Как отрисовать слой корректировки экспозиции – пошаговое руководство

### Шаг 1: Загрузить PSD‑файл

```java
String dataDir = "Your Document Directory";  // Define your document directory
String sourceFileName = dataDir + "ExposureAdjustmentLayer.psd";  // Source PSD file path

PsdImage im = (PsdImage) Image.load(sourceFileName);  // Load the PSD file
```

Замените `"Your Document Directory"` на папку, содержащую ваши PSD‑файлы. Метод `Image.load()` возвращает объект `PsdImage`, который даёт полный доступ к слоям документа.

### Шаг 2: Редактировать существующий слой корректировки экспозиции

```java
for (int i = 0; i < im.getLayers().length; i++) {
    if (im.getLayers()[i] instanceof ExposureLayer) {
        ExposureLayer expLayer = (ExposureLayer) im.getLayers()[i];
        expLayer.setExposure(2);  // Adjust the exposure level
        expLayer.setOffset(-0.25f);  // Set the offset
        expLayer.setGammaCorrection(0.5f);  // Adjust the gamma correction
    }
}
```

Цикл проходит по каждому **слою**, ищет любой `ExposureLayer` и обновляет его три ключевых параметра. Это ядро **rendering the exposure adjustment layer** с вашими пользовательскими значениями.

### Шаг 3: Сохранить изменённый PSD‑файл

```java
String psdPathAfterChange = dataDir + "ExposureAdjustmentLayerChanged.psd";  // Path to save the modified PSD file

im.save(psdPathAfterChange);  // Save the changes to the PSD file
```

Изменённый PSD сохраняет все оригинальные слои нетронутыми, но корректировка экспозиции теперь отражает новые настройки.

### Шаг 4: Экспортировать результат в PNG

```java
String pngExportPath = dataDir + "ExposureAdjustmentLayerChanged.png";  // Path to save the PNG file

PngOptions saveOptions = new PngOptions();  // Create PNG options
saveOptions.setColorType(PngColorType.TruecolorWithAlpha);  // Set color type to Truecolor with Alpha

im.save(pngExportPath, saveOptions);  // Save as PNG
```

Использование `PngOptions` с `TruecolorWithAlpha` гарантирует, что экспортированный PNG сохранит полную глубину цвета и любую прозрачность из PSD.

### Шаг 5: Добавить новый слой корректировки экспозиции

Если вам нужно **add a new exposure adjustment layer** в существующий документ, используйте следующий код:

```java
String sourceFileName = dataDir + "PhotoExample.psd";  // Source PSD file path

PsdImage img = (PsdImage) Image.load(sourceFileName);  // Load the PSD file

ExposureLayer newLayer = img.addExposureAdjustmentLayer(2, -0.25f, 2f);  // Add new exposure adjustment layer

String psdPathAfterChange = dataDir + "PhotoExampleAddedExposure.psd";  // Path to save the modified PSD file
String pngExportPath = dataDir + "PhotoExampleAddedExposure.png";  // Path to save the PNG file

img.save(psdPathAfterChange);  // Save the changes to the PSD file

PngOptions options = new PngOptions();  // Create PNG options
options.setColorType(PngColorType.TruecolorWithAlpha);  // Set color type to Truecolor with Alpha

img.save(pngExportPath, options);  // Save as PNG
```

Метод `addExposureAdjustmentLayer` создаёт новый слой корректировки с указанными значениями экспозиции, смещения и гаммы, после чего вы можете отрисовать и экспортировать его так же, как и раньше.

## Распространённые проблемы и советы

- **Layer not found** – Ensure the PSD actually contains an `ExposureLayer`. Use `instanceof ExposureLayer` as shown to avoid `ClassCastException`.
- **File path errors** – Use absolute paths or verify that `dataDir` ends with a file separator (`/` or `\`).
- **License exception** – Running without a valid license will add a watermark to the output. Register your license early in the code (`License license = new License(); license.setLicense("Aspose.PSD.lic");`).

## Часто задаваемые вопросы

### Что такое Aspose.PSD for Java?

Aspose.PSD for Java — это библиотека, позволяющая программно создавать, редактировать и **convert** PSD‑файлы с помощью Java. Она предоставляет обширный набор функций для работы с документами Photoshop.

### Могу ли я использовать Aspose.PSD for Java для работы с другими типами слоёв?

Да, Aspose.PSD for Java поддерживает различные типы слоёв, включая текстовые слои, слои корректировки и слои изображений, позволяя выполнять обширные манипуляции с PSD‑файлами.

### Как начать работу с Aspose.PSD for Java?

Вы можете начать с загрузки библиотеки с [website](https://releases.aspose.com/psd/java/) и обратиться к [documentation](https://reference.aspose.com/psd/java/) для подробных руководств и примеров.

### Есть ли бесплатная пробная версия Aspose.PSD for Java?

Да, бесплатная пробная версия доступна. Вы можете скачать её [here](https://releases.aspose.com/).

### Как получить поддержку для Aspose.PSD for Java?

Для получения поддержки вы можете посетить [Aspose support forum](https://forum.aspose.com/c/psd/34), где можно задавать вопросы и получать помощь от сообщества.

**Дополнительные вопросы**

**В: Могу ли я пакетно обрабатывать несколько PSD‑файлов?**  
A: Absolutely. Wrap the loading, editing, and saving logic inside a loop that iterates over a list of file paths.

**В: Сохраняет ли библиотека иерархию слоёв при добавлении нового слоя корректировки экспозиции?**  
A: Yes. The new layer is added on top of existing layers, maintaining the original hierarchy.

**В: В какие форматы изображений можно экспортировать помимо PNG?**  
A: Aspose.PSD supports JPEG, BMP, TIFF, and several other formats via the corresponding `*Options` classes.

---

**Последнее обновление:** 2026-04-05  
**Тестировано с:** Aspose.PSD for Java 24.10  
**Автор:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}