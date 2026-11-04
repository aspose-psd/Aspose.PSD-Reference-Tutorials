---
date: 2026-11-04
description: Узнайте, как использовать Aspose.PSD for Java для применения invert adjustment
  layer, batch process PSD‑изображений и создания PSD‑файлов с негативным изображением.
keywords:
- how to use aspose
- batch process psd images
- create negative image psd
- image processing java library
- apply multiple adjustment layers
lastmod: 2026-11-04
linktitle: Invert Adjustment Layer
og_description: Как использовать Aspose.PSD for Java для добавления invert adjustment
  layer, batch process PSD‑изображений и создания PSD с негативным изображением. Следуйте
  пошаговому руководству.
og_image_alt: Screenshot showing Aspose.PSD Java code adding an invert adjustment
  layer
og_title: Как использовать Aspose.PSD для добавления invert adjustment layer в Java
schemas:
- author: Aspose
  dateModified: '2026-11-04'
  description: Learn how to use Aspose.PSD for Java to apply an invert adjustment
    layer, batch process PSD images, and create negative image PSD files.
  headline: How to use Aspose.PSD to add an invert adjustment layer in Java
  type: TechArticle
- questions:
  - answer: Yes, it supports Java 6.0 and later, including Java 8, 11, and 17.
    question: Is Aspose.PSD compatible with all Java versions?
  - answer: Absolutely. After adding the invert layer you can call `addBrightnessAdjustmentLayer()`,
      `addHueSaturationAdjustmentLayer()`, etc., to stack effects.
    question: Can I apply multiple adjustment layers in a single operation?
  - answer: The complete documentation is available [Aspose.PSD Java API reference](https://reference.aspose.com/psd/java/).
    question: Where can I find the full API reference?
  - answer: Yes, you can download a trial version [Aspose.PSD trial download](https://releases.aspose.com/).
    question: Is there a free trial for Aspose.PSD?
  - answer: Request a temporary license [temporary license request page](https://purchase.aspose.com/temporary-license/).
    question: How do I obtain a temporary license for testing?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- aspose psd
- java image processing
- invert adjustment layer
- batch psd processing
title: Как использовать Aspose.PSD для добавления invert adjustment layer в Java
url: /ru/java/advanced-image-manipulation/invert-adjustment-layer/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Как использовать Aspose.PSD для добавления слоя корректировки Инвертировать в Java

## Введение

Если вы ищете надёжную **image processing java library**, Aspose.PSD for Java — один из самых универсальных вариантов на рынке. В этом руководстве вы увидите **how to use Aspose** для вставки **Invert Adjustment Layer** в файл PSD, объедините его с другими корректировками и даже выполните операцию над десятками файлов. Независимо от того, создаёте ли вы инструмент пакетной обработки, серверный сервис изображений или редактор одиночных изображений, нижеописанные шаги позволят вам от исходного PSD получить полностью редактируемое негативное изображение за считанные минуты.

## Быстрые ответы
- **Что делает слой корректировки Инвертировать?** Он инвертирует каждое значение RGB в выбранной области, превращая изображение в фотонегатив.  
- **Какая библиотека предоставляет эту функцию?** Aspose.PSD, ведущая **image processing java library**.  
- **Могу ли я наложить его с другими корректировками?** Да — вы можете **apply multiple adjustment layers** such as Brightness/Contrast, Hue/Saturation, and more.  
- **Нужна ли лицензия для разработки?** Доступна бесплатная пробная версия; лицензия требуется для использования в продакшене.  
- **Сколько времени занимает реализация?** Обычно менее 10 минут для базового случая.  

## Что такое слой корректировки Инвертировать?

Слой корректировки Инвертировать — это недеструктивное редактирование, которое инвертирует цветовые значения каждого затронутого пикселя. Поскольку он находится поверх стека слоёв, вы можете переключать его видимость или менять порядок без постоянного изменения исходных данных изображения. Это самый быстрый способ **create negative image PSD** файлов или достичь классического вида фотонегатива.

## Почему использовать Aspose.PSD в качестве вашей image processing java library?

Aspose.PSD поддерживает **200+ PSD features**, может читать и записывать файлы Photoshop без необходимости наличия Photoshop, и обрабатывает многосотстраничные документы, используя менее 500 МБ памяти кучи. Он работает на любой Java‑runtime (Java 6+), что делает его идеальным для **batch process psd images** на серверах Windows, Linux или macOS.

## Требования

Прежде чем начать, убедитесь, что у вас есть:

1. **Aspose.PSD for Java** – скачайте последнюю JAR с официального сайта [Aspose.PSD for Java download page](https://releases.aspose.com/psd/java/).  
2. **Java Development Kit** – JDK 6.0 или более поздняя версия, установленная и настроенная в вашем `PATH`.  

Теперь вы готовы писать код.

## Импорт пакетов

Класс `PsdImage` представляет весь документ Photoshop в памяти, тогда как классы слоёв корректировок находятся в пакете `com.aspose.psd.layers.adjustments`.

Класс `PsdImage` — это объект верхнего уровня Aspose.PSD, который инкапсулирует структуру и пиксельные данные PSD‑файла. Импортируйте пространства имён, после чего вы сможете загружать, редактировать и сохранять PSD‑файлы.

## Шаг 1: настройте каталог документа

Укажите папку, содержащую ваш исходный PSD‑файл и куда будет сохраняться результат. Использование абсолютных путей предотвращает `NullPointerException`, когда меняется рабочий каталог.

## Шаг 2: загрузите PSD‑файл

Загрузите исходный файл в объект `PsdImage`. Этот объект хранит полную иерархию слоёв в памяти, позволяя выполнять недеструктивные правки.

Класс `PsdImage` предоставляет статический метод `load`, который читает заголовок файла, проверяет формат и создаёт представление в памяти, готовое к манипуляциям.

## Шаг 3: добавьте слой корректировки Инвертировать

Вызовите встроенный метод для вставки Invert Adjustment Layer поверх текущего стека слоёв. Позже вы можете добавить дополнительные слои (например, Brightness, Hue), чтобы **apply multiple adjustment layers** в одном рабочем процессе.

`addInvertAdjustmentLayer()` добавляет Invert Adjustment Layer в коллекцию слоёв PSD.

## Шаг 4: сохраните результат

Сохраните изменённый PSD на диск.  

`save()` записывает PSD‑файл, включая все слои и метаданные, по указанному пути.

Сохранение использует тот же метод `save`, который записывает весь документ, включая все слои корректировок, маски и метаданные, в указанный формат.

### Что только что произошло?

PSD‑файл был загружен в объект `PsdImage`, был создан `InvertAdjustmentLayer` и добавлен как верхний слой, после чего документ был сохранён. Эта последовательность сохраняет исходные данные изображения, одновременно добавляя недеструктивный эффект инверсии, который можно включать/выключать или менять порядок позже.

Теперь вы успешно использовали Aspose.PSD, **image processing java library**, для работы с PSD‑файлом.

## Как пакетно обрабатывать PSD‑изображения с инвертированием?

Загружайте каждый файл внутри цикла `for`, применяйте те же шаги и вызывайте `save` на каждой итерации. Поскольку Aspose.PSD обрабатывает файлы в потоковом режиме, вы можете работать с **hundreds of PSDs**, удерживая использование памяти ниже 300 МБ, переиспользуя один и тот же экземпляр `PsdImage`.

## Как преобразовать PSD в негативное изображение?

Добавьте Invert Adjustment Layer как верхний элемент и сохраните документ — эта операция эквивалентна **convert PSD to negative**. Позже вы можете отключить или удалить слой, чтобы вернуть исходный вид без повторной загрузки исходного файла.

## Распространённые проблемы и советы

| Проблема | Причина | Решение |
|----------|---------|----------|
| **NullPointerException on `Image.load`** | Неправильный путь к файлу или файл отсутствует | Проверьте `dataDir` и имя файла; используйте абсолютные пути для тестирования |
| **Layer order not as expected** | Добавление слоёв после существующих меняет их порядок | Вставьте слой инверсии перед другими корректировками или измените порядок с помощью `psdImage.getLayers().move()` |
| **Performance slowdown on large PSDs** | Загрузка очень больших файлов в память | Увеличьте размер кучи JVM (`-Xmx2g`) или обрабатывайте файлы порциями, используя `psdImage.getPages().get(0).getResources().setMemoryOptimized(true)` |

## Часто задаваемые вопросы

**Q: Совместим ли Aspose.PSD со всеми версиями Java?**  
A: Да, поддерживает Java 6.0 и более поздние, включая Java 8, 11 и 17.

**Q: Могу ли я применить несколько слоёв корректировки за одну операцию?**  
A: Абсолютно. После добавления слоя инверсии вы можете вызвать `addBrightnessAdjustmentLayer()`, `addHueSaturationAdjustmentLayer()` и т.д., чтобы наложить эффекты.

**Q: Где я могу найти полную справочную документацию API?**  
A: Полная документация доступна [Aspose.PSD Java API reference](https://reference.aspose.com/psd/java/).

**Q: Есть ли бесплатная пробная версия Aspose.PSD?**  
A: Да, вы можете скачать пробную версию [Aspose.PSD trial download](https://releases.aspose.com/).

**Q: Как получить временную лицензию для тестирования?**  
A: Запросите временную лицензию [temporary license request page](https://purchase.aspose.com/temporary-license/).

---

**Последнее обновление:** 2026-11-04  
**Тестировано с:** Aspose.PSD 24.12 for Java  
**Автор:** Aspose  









```java
import com.aspose.psd.Image;

import com.aspose.psd.fileformats.psd.PsdImage;
```

```java
String dataDir = "Your Document Directory";
```

```java
String filePath = dataDir + "InvertStripes_before.psd";
String outputPath = dataDir + "InvertStripes_after.psd";

PsdImage im = (PsdImage)Image.load(filePath);
```

```java
im.addInvertAdjustmentLayer();
```

```java
im.save(outputPath);
```

## Связанные руководства

- [Добавить слой корректировки уровня в PSD файлы с Aspose.PSD для Java](/psd/java/modifying-converting-psd-images/add-level-adjustment-layer-psd/)
- [Как добавить слой корректировки – Channel Mixer в PSD (Java)](/psd/java/modifying-converting-psd-images/add-channel-mixer-adjustment-layer-psd/)
- [Как редактировать PSD – добавить слой корректировки кривых с помощью Java](/psd/java/modifying-converting-psd-images/add-curves-adjustment-layer-psd/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}