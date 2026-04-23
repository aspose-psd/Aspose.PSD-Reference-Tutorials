---
date: 2026-04-12
description: Узнайте, как изменять размер изображения в Java с помощью Bicubic Resampler
  от Aspose.PSD. Этот учебник по масштабированию изображений пошагово показывает,
  как достичь превосходных результатов.
keywords:
- resize image java
- image scaling tutorial
- java image library
linktitle: Реализовать бикубический ресемплер
second_title: Aspose.PSD Java API
title: Изменение размера изображения в Java – бикубический ресемплер для масштабирования
  высокого качества
url: /ru/java/advanced-image-manipulation/implement-bicubic-resampler/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Изменение размера изображения Java – Бикубический ресемплер для масштабирования высокого качества

## Введение

Если вам нужно **resize image java** проекты без потери резкости и появления артефактов, вы попали в нужное место. В этом **image scaling tutorial** мы рассмотрим использование Bicubic Resampler от Aspose.PSD — мощной функции **java image library**, которая обеспечивает плавные, чёткие результаты для файлов PSD и многих других форматов. К концу этого руководства вы сможете интегрировать масштабирование высокого качества в любое Java‑приложение всего несколькими строками кода.

## Быстрые ответы
- **Что делает Bicubic Resampler?** Он применяет сложный алгоритм интерполяции, сохраняющий детали при изменении размера изображений.  
- **Какие значения ResizeType доступны?** `CubicConvolution` и `Bell` — два варианта Bicubic, предоставляемые Aspose.PSD.  
- **Нужна ли лицензия для запуска кода?** Временная лицензия Aspose подходит для оценки; полная лицензия требуется для продакшн.  
- **Какая версия Java требуется?** Любая среда выполнения Java 8+ совместима с последней библиотекой Aspose.PSD.  
- **Можно ли изменять размер других форматов (PNG, JPEG) тем же API?** Да, Aspose.PSD поддерживает несколько типов изображений, хотя примеры сосредоточены на PSD.

## Что такое масштабирование изображений высокого качества?

Масштабирование изображений высокого качества подразумевает изменение размера изображения при сохранении чётких краёв, плавных градиентов и точного цветового представления. Bicubic Resampler достигает этого, учитывая значения соседних пикселей (используя кубическую свёртку или алгоритм Bell) для вычисления каждого нового пикселя, что даёт более естественный вид по сравнению с методами ближайшего соседа или билинейной интерполяции.

## Почему использовать Bicubic Resampler для масштабирования высокого качества?

- **Сохраняет детали:** Тонкие текстуры и линии остаются чёткими даже после значительных изменений размера.  
- **Уменьшает артефакты:** Минимизирует кольца и размытие, часто возникающие при использовании более простых алгоритмов.  
- **Лёгкая интеграция:** Однострочный вызов метода (`image.resize`) позволяет переключать алгоритмы без переписывания кода.  

## Предварительные требования

Before you start, make sure you have:

- **Aspose.PSD for Java** – загрузите последнюю JAR с [Aspose.PSD for Java documentation](https://reference.aspose.com/psd/java/).  
- **Java Development Kit** – установленный и настроенный JDK 8 или новее.  
- **Sample PSD file** – тестовое изображение (например, `sample_bicubic.psd`), размещённое в известном каталоге.  

Эти элементы вместе образуют надёжную основу **java image library** для данного руководства.

## Импорт пакетов

Добавьте необходимые импорты в ваш Java‑класс. Они подключают основные классы Aspose.PSD и перечисление `ResizeType`.

```java
import com.aspose.psd.Image;
import com.aspose.psd.ResizeType;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.PsdOptions;
```

## Как изменить размер изображения Java с помощью Bicubic Resampler

### Шаг 1: Загрузка изображения

Сначала загрузите исходный PSD‑файл, размер которого вы хотите изменить. Замените `Your Document Directory` фактическим путём на вашем компьютере.

```java
String dataDir = "Your Document Directory";
String filePath = dataDir + "sample_bicubic.psd";
PsdImage image = (PsdImage)Image.load(filePath);
```

### Шаг 2: Масштабирование с помощью Cubic Convolution (высокое качество)

Теперь примените алгоритм **Cubic Convolution**, один из двух вариантов Bicubic, обеспечивающих масштабирование изображения высокого качества. В примере изображение масштабируется до 300 × 300 пикселей.

```java
String destNameCubicConvolution = dataDir + "ResamplerCubicConvolutionStripes_after.psd";
image.resize(300, 300, ResizeType.CubicConvolution);
image.save(destNameCubicConvolution, new PsdOptions(image));
```

### Шаг 3: Масштабирование с помощью алгоритма Bell (альтернативное высокое качество)

Если вы предпочитаете алгоритм **Bell**, который даёт слегка иной эффект сглаживания, вы можете использовать его аналогичным образом. Обратите внимание, что мы повторно загружаем оригинальное изображение, чтобы сравнение было справедливым.

```java
String destNameBell = dataDir + "ResamplerBellStripes_after.psd";
PsdImage imageBellStripes = (PsdImage)Image.load(filePath);
imageBellStripes.resize(300, 300, ResizeType.Bell);
imageBellStripes.save(destNameBell, new PsdOptions(imageBellStripes));
```

Не стесняйтесь экспериментировать с другими размерами или форматами файлов — просто скорректируйте параметры соответственно.

## Распространённые ошибки и советы

- **Неправильный путь:** Убедитесь, что `dataDir` заканчивается разделителем файлов (`/` или `\`), соответствующим вашей ОС.  
- **Исключения лицензии:** Запуск без действующей лицензии может добавить водяной знак к выходному изображению. Используйте **temporary aspose license** для тестирования, затем переключитесь на постоянную лицензию для продакшн.  
- **Потребление памяти:** Большие PSD‑файлы могут потреблять значительный объём памяти; рассмотрите возможность освобождения изображений (`image.dispose()`) после сохранения.  

## Часто задаваемые вопросы

**Q: Можно ли использовать Aspose.PSD for Java с другими форматами изображений?**  
A: Да, библиотека поддерживает PSD, PNG, JPEG, TIFF, BMP и многие другие.

**Q: Доступна ли временная лицензия для Aspose.PSD for Java?**  
A: Да, вы можете получить временную лицензию по ссылке [здесь](https://purchase.aspose.com/temporary-license/).

**Q: Где можно найти поддержку для Aspose.PSD for Java?**  
A: Посетите форум Aspose.PSD по ссылке [здесь](https://forum.aspose.com/c/psd/34) для любых вопросов, связанных с поддержкой.

**Q: Можно ли скачать библиотеку Aspose.PSD for Java?**  
A: Да, скачайте библиотеку со страницы релизов по ссылке [здесь](https://releases.aspose.com/psd/java/).

**Q: Как приобрести Aspose.PSD for Java?**  
A: Вы можете приобрести Aspose.PSD for Java на странице покупки по ссылке [здесь](https://purchase.aspose.com/buy).

---

**Последнее обновление:** 2026-04-12  
**Тестировано с:** Aspose.PSD for Java 24.11 (latest at time of writing)  
**Автор:** Aspose

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}