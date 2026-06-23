---
date: 2026-06-23
description: Узнайте, как конвертировать PSD в PNG и изменять размер изображений пропорционально
  в Java с использованием Aspose.PSD. Этот пошаговый учебник охватывает кэширование
  изображений, изменение размера и сохранение в формате PNG.
keywords:
- convert psd to png
- save psd as png
- how to cache image
- resize image without distortion
- proportional image scaling
linktitle: Конвертировать PSD в PNG и изменить размер пропорционально
schemas:
- author: Aspose
  dateModified: '2026-06-23'
  description: Learn how to convert PSD to PNG and resize images proportionally in
    Java using Aspose.PSD. This step‑by‑step tutorial covers image caching, resizing,
    and saving as PNG.
  headline: How to Convert PSD to PNG and Resize Proportionally with Aspose.PSD for
    Java
  type: TechArticle
- description: Learn how to convert PSD to PNG and resize images proportionally in
    Java using Aspose.PSD. This step‑by‑step tutorial covers image caching, resizing,
    and saving as PNG.
  name: How to Convert PSD to PNG and Resize Proportionally with Aspose.PSD for Java
  steps:
  - name: '**Java Development Kit (JDK)** – Java 8 or later installed.'
    text: '**Java Development Kit (JDK)** – Java 8 or later installed.'
  - name: '**Aspose.PSD for Java** – download the latest JAR from the official site [here](https://releases.aspose.com/psd/java/).'
    text: '**Aspose.PSD for Java** – download the latest JAR from the official site [here](https://releases.aspose.com/psd/java/).'
  - name: A sample PSD file (`sample.psd`) placed in a directory you can reference
      from your project.
    text: A sample PSD file (`sample.psd`) placed in a directory you can reference
      from your project.
  type: HowTo
- questions:
  - answer: Aspose.PSD supports PSD, PNG, JPEG, BMP, GIF, and many more. See the full
      list in the [documentation](https://reference.aspose.com/psd/java/). For the
      full API reference, see the guide **here**.
    question: Is Aspose.PSD compatible with all image formats?
  - answer: Yes. Purchase a commercial license on the [Aspose store](https://purchase.aspose.com/buy).
    question: Can I use Aspose.PSD for commercial projects?
  - answer: Absolutely – request a temporary license [here](https://purchase.aspose.com/temporary-license/)
      for evaluation purposes.
    question: Are temporary licenses available for testing?
  - answer: The [Aspose.PSD forum](https://forum.aspose.com/c/psd/34) is a great place
      to ask questions and share solutions.
    question: Where can I find community support?
  - answer: Detailed API docs are available [here](https://reference.aspose.com/psd/java/).
    question: How do I access the full API reference?
  type: FAQPage
second_title: Aspose.PSD Java API
title: Как конвертировать PSD в PNG и изменять размер пропорционально с помощью Aspose.PSD
  для Java
url: /ru/java/advanced-image-manipulation/resize-image-proportionally/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Как конвертировать PSD в PNG и масштабировать пропорционально с Aspose.PSD для Java

## Введение

Если вам нужно **конвертировать PSD в PNG**, сохраняя оригинальное соотношение сторон, вы попали в нужное место. В этом **уроке по Aspose.PSD Java** мы пройдем полный **java image processing tutorial**, показывающий, **как масштабировать изображения** пропорционально, кэшировать изображение для оптимальной производительности и, наконец, сохранять результат в формате PNG. К концу вы сможете интегрировать этот рабочий процесс в любой Java‑ориентированный конвейер обработки изображений.

## Быстрые ответы
- **Может ли Aspose.PSD конвертировать PSD в PNG?** Да — просто загрузите PSD и сохраните его с помощью `PngOptions`.
- **Поддерживает ли библиотека пропорциональное масштабирование?** Абсолютно; используйте `resizeWidthProportionally` и `resizeHeightProportionally`.
- **Нужно ли сначала кэшировать изображение?** Кэширование (`image.cacheData()`) улучшает производительность при работе с большими PSD‑файлами.
- **Какая версия Java требуется?** Полностью поддерживается Java 8 и новее.
- **Нужна ли лицензия для продакшна?** Да, коммерческая лицензия убирает водяные знаки оценки.

## Что такое «конвертировать PSD в PNG» и почему это важно?

**Конвертировать PSD в PNG** означает преобразовать многослойный документ Photoshop в однослойный, без потерь PNG‑файл, сохраняющий прозрачность и визуальную точность. Эта конверсия позволяет делиться дизайнами без необходимости в Photoshop, создавать веб‑готовые ресурсы и миниатюры, а также разгружать тяжелые PSD‑файлы из браузеров клиентов, сохраняя качество, необходимое для UI‑компонентов и брендинга.

## Почему масштабировать изображение пропорционально в Java?

Масштабирование изображения **без искажений** сохраняет исходное соотношение ширины к высоте, поэтому графика сохраняет задуманную визуализацию на любом размере экрана. Методы пропорционального масштабирования Aspose.PSD автоматически вычисляют недостающую величину, устраняя ручные расчёты и риск растянутых или сжатых визуалов.

## Почему это важно для разработчиков

Для разработчиков пропорциональное масштабирование и конверсия PSD‑в‑PNG снижают потребление памяти и ускоряют загрузку, обеспечивая эффективную работу приложений с большими графиками. Масштабируя изображения на ранних этапах, вы поддерживаете согласованность UI‑рендеринга на разных устройствах и избавляетесь от необходимости в Photoshop на сборочных серверах, что упрощает развертывание и снижает эксплуатационные расходы.

- **Уменьшенный размер PSD‑файла** — Сжимая большие PSD перед конвертацией, вы снижаете использование памяти и ускоряете последующую обработку.  
- **Согласованный рендеринг UI** — Пропорциональное масштабирование гарантирует, что иконки и графика сохраняют визуальный баланс на всех устройствах.  
- **Отсутствие зависимости от Photoshop** — Вы можете выполнять эти операции на сервере или в CI‑конвейере без установки Photoshop.

## Предварительные требования

Прежде чем перейти к коду, убедитесь, что у вас есть:

1. **Java Development Kit (JDK)** — установлен Java 8 или новее.  
2. **Aspose.PSD for Java** — скачайте последнюю JAR‑файл с официального сайта [здесь](https://releases.aspose.com/psd/java/).  
3. Пример PSD‑файла (`sample.psd`), размещённый в каталоге, доступном вашему проекту.

## Импорт пакетов

Класс `PsdImage` — основной объект Aspose.PSD, представляющий PSD‑файл в памяти. Импортируйте необходимые пространства имён для загрузки, кэширования, масштабирования и экспорта в PNG.

```java
import com.aspose.psd.Image;
import com.aspose.psd.imageoptions.PngOptions;
```

## Шаг 1: Загрузка PSD‑изображения

**Прямой ответ:** Загрузите исходный файл с помощью `new PsdImage("sample.psd")`; затем вызовите `image.cacheData()`, чтобы предварительно загрузить данные изображения, что предотвращает повторные чтения с диска во время последующих операций.

`cacheData()` загружает весь PSD в память, обеспечивая более быструю последующую обработку. Метод `cacheData()` читает весь документ в память, ускоряя последующие операции с большими файлами. Сначала загрузите исходный PSD‑файл. Если файл большой, кэширование данных изображения уменьшает нагрузку памяти при выполнении последующих операций.

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

Image image = Image.load(sourceFile);

if (!image.isCached()) {
    // Image caching java – improves performance for large files
    image.cacheData();
}
```

## Шаг 2: Пропорциональное масштабирование изображения (Java)

**Прямой ответ:** Вызовите `image.resizeWidthProportionally(targetWidth)` (или `resizeHeightProportionally`), чтобы уменьшить изображение, автоматически сохраняя исходное соотношение сторон.

`resizeWidthProportionally(int targetWidth)` масштабирует ширину изображения и автоматически вычисляет соответствующую высоту для сохранения оригинального соотношения сторон. Теперь определите новые размеры. В этом примере мы уменьшаем изображение до **половины** его исходного размера, сохраняя соотношение сторон. При необходимости можно скорректировать целевую ширину или высоту.

Метод `resizeWidthProportionally` рассчитывает соответствующую высоту на основе оригинального соотношения, поэтому изображение масштабируется **без искажений**. Используйте любой из методов — Aspose.PSD автоматически рассчитывает дополнительную величину за вас.

```java
int newWidth = image.getWidth() / 2;
image.resizeWidthProportionally(newWidth);

int newHeight = image.getHeight() / 2;
image.resizeHeightProportionally(newHeight);
```

> **Полезный совет:** Используйте либо `resizeWidthProportionally`, *либо* `resizeHeightProportionally` — библиотека автоматически вычислит другую размерность, чтобы сохранить пропорции изображения.

## Шаг 3: Сохранение масштабированного изображения в PNG

**Прямой ответ:** Создайте экземпляр `PngOptions`, назначьте его изображению и вызовите `image.save("output.png", pngOptions)`, чтобы записать масштабированный файл в формате PNG.

`PngOptions` задаёт параметры экспорта PNG, такие как уровень сжатия и глубина цвета. В конце экспортируйте масштабированное изображение в формат PNG. Этот шаг завершает рабочий процесс **конвертации PSD в PNG**.

При выполнении кода вы получите PNG‑файл, размер которого в два раза меньше оригинального PSD, с тем же визуальным качеством и без искажений.

```java
String destName = dataDir + "SimpleResizeImageProportionally_out.png";
image.save(destName, new PngOptions());
```

При выполнении кода вы получите PNG‑файл, размер которого в два раза меньше оригинального PSD, с тем же визуальным качеством и без искажений.

## Распространённые проблемы и решения

| Проблема | Причина | Решение |
|----------|----------|----------|
| **OutOfMemoryError** | Большой PSD не кэширован | Вызовите `image.cacheData()` перед масштабированием |
| **Пустой PNG‑файл** | Неправильный путь к файлу | Проверьте `dataDir` и права записи |
| **Соотношение сторон выглядит неверно** | Одновременное указание ширины и высоты вручную | Используйте пропорциональные методы, предоставляемые Aspose.PSD |

## Советы по уменьшению размера PSD‑файла

- **Обрезайте ненужные слои** перед загрузкой файла.  
- **Масштабируйте пропорционально**, как показано выше, чтобы уменьшить размеры на ранних этапах.  
- **Сохраняйте в PNG с подходящей глубиной цвета**, чтобы избежать избыточных данных.

## Часто задаваемые вопросы

**В: Совместима ли Aspose.PSD со всеми форматами изображений?**  
О: Aspose.PSD поддерживает PSD, PNG, JPEG, BMP, GIF и многие другие. Полный список см. в [документации](https://reference.aspose.com/psd/java/). Для полной ссылки на API см. руководство **[здесь]**(https://reference.aspose.com/psd/java/).

**В: Можно ли использовать Aspose.PSD в коммерческих проектах?**  
О: Да. Приобретите коммерческую лицензию в [магазине Aspose](https://purchase.aspose.com/buy).

**В: Доступны ли временные лицензии для тестирования?**  
О: Абсолютно — запросите временную лицензию **[здесь](https://purchase.aspose.com/temporary-license/)** для целей оценки.

**В: Где можно получить поддержку сообщества?**  
О: Форум [Aspose.PSD](https://forum.aspose.com/c/psd/34) — отличное место для вопросов и обмена решениями.

**В: Как получить доступ к полной ссылке на API?**  
О: Подробная документация API доступна **[здесь](https://reference.aspose.com/psd/java/)**.

## Заключение

Теперь вы знаете, как **конвертировать PSD в PNG**, **масштабировать изображение пропорционально** и эффективно кэшировать данные с помощью Aspose.PSD для Java. Внедрите эти шаги в свои приложения, чтобы обеспечить быструю, высококачественную обработку изображений без зависимости от Photoshop. Этот **aspose psd java** подход является надёжной частью любого **java image processing tutorial** и помогает контролировать размер PSD‑файлов, сохраняя визуальную точность.

---

**Последнее обновление:** 2026-06-23  
**Тестировано с:** Aspose.PSD 24.12 for Java  
**Автор:** Aspose

{{< blocks/products/products-backtop-button >}}

## Похожие уроки

- [Simple Resizing with Aspose.PSD – Java Image Manipulation Library](/psd/java/basic-image-operations/simple-resizing/)
- [Resize Image Java - Using Resize Type Enumeration in Aspose.PSD for Java](/psd/java/advanced-image-manipulation/resizing-with-resize-type-enumeration/)
- [High Quality Image Scaling with Bicubic Resampler in Aspose.PSD for Java](/psd/java/advanced-image-manipulation/implement-bicubic-resampler/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}