---
date: 2026-04-08
description: Узнайте, как экспортировать PSD в PNG и создать новый слой PSD с помощью
  Aspose.PSD для Java, используя временную лицензию Aspose. Этот пошаговый учебник
  охватывает манипуляцию изображениями PSD и установку позиции слоя.
keywords:
- aspose temporary license
- set layer position
- psd image manipulation
- create new psd layer
linktitle: Добавить новый обычный слой в PSD
second_title: Aspose.PSD Java API
title: Экспорт PSD в PNG и добавление нового обычного слоя с помощью Aspose.PSD для
  Java – временная лицензия Aspose
url: /ru/java/advanced-image-effects/add-new-regular-layer/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Экспорт PSD в PNG и добавление нового обычного слоя с помощью Aspose.PSD для Java

## Введение

В этом **aspose psd tutorial** вы узнаете, как **export PSD to PNG** одновременно **creating a new regular layer** в том же файле, **using an aspose temporary license** для разработки. Независимо от того, нужно ли вам создавать веб‑готовые миниатюры, готовить ресурсы для конвейера дизайна или просто экспериментировать с **psd image manipulation**, Aspose.PSD for Java предоставляет полный программный контроль. Мы пройдем каждый шаг — от загрузки исходного файла до сохранения как обновлённого PSD, так и копии PNG — чтобы вы могли сразу начать работать с слоями PSD.

## Быстрые ответы

- **Can I export PSD to PNG with one call?** Да, после добавления слоёв вы можете вызвать `save` с `PngOptions`.
- **Do I need a license for development?** Временная лицензия подходит для тестирования; полная лицензия требуется для продакшна.
- **Which Java version is supported?** Aspose.PSD работает с Java 8 и новее.
- **Is layer positioning pixel‑based?** Да, вы задаёте координаты left, top, right, bottom в пикселях, используя методы **set layer position**.
- **Will the PNG retain layer transparency?** PNG будет содержать объединённый результат всех видимых слоёв.

## Зачем использовать временную лицензию aspose?

Временная лицензия **aspose temporary license** позволяет оценить весь набор функций Aspose.PSD без каких‑либо ограничений. Она удаляет водяной знак оценки, разблокирует все API — включая возможность **create new psd layer** объектов — и даёт возможность протестировать ваш код в среде, близкой к продакшну, перед покупкой постоянной лицензии.

## Требования

Before you begin, ensure you have:

- **Java Development Environment** – установлен JDK 8+ и инструмент сборки (Maven/Gradle).
- **Aspose.PSD for Java** – Скачайте последнюю JAR с официального сайта [here](https://releases.aspose.com/psd/java/).
- **A sample PSD file** – В примерах будем использовать `OneLayer.psd`.

## Импорт пакетов

Добавьте необходимые импорты в ваш Java‑класс. Эти классы предоставляют базовый функционал для **psd image manipulation** и работы со слоями.

```java
import com.aspose.psd.Image;
import com.aspose.psd.Rectangle;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.Layer;
import com.aspose.psd.imageoptions.PngOptions;
import com.aspose.psd.imageoptions.PsdOptions;
```

## Что такое «set layer position» и почему это важно?

Когда вы добавляете новый слой, необходимо определить, где он будет размещён на холсте. Методы `setLeft`, `setTop`, `setRight` и `setBottom` **set layer position** в пиксельных координатах. Правильное позиционирование гарантирует, что графика будет точно соответствовать ожидаемому месту, что критично для задач, таких как композитинг UI‑ресурсов или подготовка файлов к печати.

## Пошаговое руководство

### Шаг 1: Загрузка PSD файла

Сначала загрузите существующий PSD, который вы хотите изменить. Это даст вам объект `PsdImage`, с которым можно работать.

```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "OneLayer.psd";
PsdImage im = (PsdImage)Image.load(sourceFileName);
```

### Шаг 2: Подготовка пиксельных данных и прямоугольников

Мы создадим два буфера пикселей (`int[]`) и определим прямоугольные области, где будут рисоваться новые слои. Это основа для **creating a new psd layer**.

```java
int[] data1 = new int[2500];
int[] data2 = new int[2500];
Rectangle rect1 = new Rectangle(0, 0, 50, 50);
Rectangle rect2 = new Rectangle(0, 0, 100, 25);
```

### Шаг 3: Инициализация данных слоя

Заполните буферы пикселей значением ARGB по умолчанию. Значение `-10000000` соответствует полупрозрачному тёмному оттенку.

```java
for (int i = 0; i < 2500; i++) {
    data1[i] = -10000000;
    data2[i] = -10000000;
}
```

### Шаг 4: Добавление обычных слоёв (Манипуляция слоями PSD)

Теперь мы **add regular layers** в изображение PSD и **set layer position** с помощью свойств left, top, right и bottom. Это демонстрирует, как программно **manipulate PSD layers**.

```java
Layer layer1 = im.addRegularLayer();
layer1.setLeft(25);
layer1.setTop(25);
layer1.setRight(75);
layer1.setBottom(75);
layer1.saveArgb32Pixels(rect1, data1);

Layer layer2 = im.addRegularLayer();
layer2.setLeft(25);
layer2.setTop(150);
layer2.setRight(1255);
layer2.setBottom(175);
layer2.saveArgb32Pixels(rect2, data2);
```

### Шаг 5: Экспорт PSD в PNG и сохранение обновлённого PSD

После размещения слоёв сохраните изменённый документ. Сначала мы экспортируем результат в PNG (шаг **export psd to png**), затем сохраняем PSD с новыми слоями.

```java
String exportPath = dataDir + "Updated.psd";
String exportPathPng = dataDir + "Updated.png";

im.save(exportPath, new PsdOptions());          // Save the updated PSD
im.save(exportPathPng, new PngOptions());       // Export PSD to PNG
```

> **Pro tip:** Если вам нужен только PNG, вы можете пропустить вызов `save` для PSD и напрямую вызвать `save` с `PngOptions`.

## Распространённые проблемы и их устранение

| Симптом | Вероятная причина | Решение |
|---------|-------------------|---------|
| PNG отображается пустым | Слои невидимы или полностью прозрачны | Убедитесь, что задаёте непрозрачные значения пикселей или вызываете `layer.setVisible(true)`. |
| `ArrayIndexOutOfBoundsException` | Несоответствие размеров прямоугольника и длины массива пикселей | Проверьте, что `rect.width * rect.height == dataArray.length`. |
| LicenseException at runtime | Не загружена действительная лицензия | Загрузите временную или постоянную лицензию перед вызовом любых методов API. |

## Часто задаваемые вопросы

**Q: Совместим ли Aspose.PSD с Java 8?**  
A: Да, Aspose.PSD поддерживает Java 8 и более поздние версии.

**Q: Могу ли я применять трансформации (поворачивать, масштабировать) к добавленным слоям?**  
A: Конечно! Класс `Layer` предоставляет методы `rotate`, `scale` и `translate` для полного управления трансформациями.

**Q: Где я могу найти дополнительную документацию Aspose.PSD?**  
A: Подробная API‑документация доступна [here](https://reference.aspose.com/psd/java/).

**Q: Как получить временную лицензию для Aspose.PSD?**  
A: Посетите страницу временной лицензии [here](https://purchase.aspose.com/temporary-license/).

**Q: Есть ли сообщества/форумы для поддержки Aspose.PSD?**  
A: Да, присоединяйтесь к обсуждениям на форумах Aspose [here](https://forum.aspose.com/c/psd/34).

## Заключение

Теперь вы знаете, как **export PSD to PNG** одновременно **adding new regular layers** с помощью Aspose.PSD for Java, и увидели, как **aspose temporary license** позволяет попробовать этот процесс без ограничений. Этот урок демонстрирует основные возможности **psd image manipulation**: загрузка файла, создание слоёв, заполнение пиксельных данных и экспорт финальной композиции. Не стесняйтесь экспериментировать с различными размерами прямоугольников, цветами пикселей или эффектами слоёв, чтобы адаптировать результат под нужды вашего проекта.

---

**Последнее обновление:** 2026-04-08  
**Тестировано с:** Aspose.PSD 24.11 for Java  
**Автор:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}