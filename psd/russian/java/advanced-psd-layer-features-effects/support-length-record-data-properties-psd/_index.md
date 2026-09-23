---
date: 2026-09-23
description: Узнайте, как изменять векторные фигуры PSD и выполнять пакетную обработку
  файлов PSD с помощью Aspose.PSD for Java. Подробные шаги, рекомендации и шаблоны
  кода для полного решения.
keywords:
- modify psd vector shapes
- batch process psd files
- Aspose.PSD Java
- vector shape editing
lastmod: 2026-09-23
linktitle: Поддержка свойств Length Record Data в PSD - Java
og_description: Узнайте, как изменять векторные фигуры PSD и выполнять пакетную обработку
  файлов PSD с помощью Aspose.PSD for Java. Пошаговое руководство с шаблонами кода
  и советами экспертов.
og_image_alt: Guide showing how to edit vector shapes in PSD files using Aspose.PSD
  for Java
og_title: Изменение векторных фигур PSD с помощью Aspose.PSD for Java
schemas:
- author: Aspose
  dateModified: '2026-09-23'
  description: Learn how to modify PSD vector shapes and batch process PSD files using
    Aspose.PSD for Java. Detailed steps, tips, and code placeholders for a complete
    solution.
  headline: Modify PSD vector shapes with Aspose.PSD for Java
  type: TechArticle
- description: Learn how to modify PSD vector shapes and batch process PSD files using
    Aspose.PSD for Java. Detailed steps, tips, and code placeholders for a complete
    solution.
  name: Modify PSD vector shapes with Aspose.PSD for Java
  steps:
  - name: '**Java Development Kit (JDK)** – download from [Oracle''s website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html)
      or use your preferred package manager.'
    text: '**Java Development Kit (JDK)** – download from [Oracle''s website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html)
      or use your preferred package manager.'
  - name: '**Aspose.PSD for Java** – obtain the latest JAR from the [Aspose releases
      page](https://releases.aspose.com/psd/java/).'
    text: '**Aspose.PSD for Java** – obtain the latest JAR from the [Aspose releases
      page](https://releases.aspose.com/psd/java/).'
  - name: '**IDE** – IntelliJ IDEA, Eclipse, or any Java‑compatible editor.'
    text: '**IDE** – IntelliJ IDEA, Eclipse, or any Java‑compatible editor.'
  - name: '**A PSD file** – create one in Photoshop or grab a sample PSD to experiment
      with.'
    text: '**A PSD file** – create one in Photoshop or grab a sample PSD to experiment
      with.'
  - name: '**Basic Java knowledge** – familiarity with classes, objects, and exception
      handling.'
    text: '**Basic Java knowledge** – familiarity with classes, objects, and exception
      handling.'
  type: HowTo
- questions:
  - answer: The `VsmsResource` will be absent, so `resource` stays `null`. Add a check
      and skip the modification step or inform the user.
    question: How do I handle a PSD that contains no vector shape layers?
  - answer: Yes, `LengthRecord` provides setters for fill, stroke, and opacity. See
      the API docs for the full list.
    question: Can I change other properties like fill color or stroke width?
  - answer: Absolutely. Wrap the code inside a loop that iterates over a directory
      of PSD files, adjusting the input and output paths each time.
    question: Is it possible to batch‑process multiple PSD files?
  - answer: '`Image.load` handles file streams automatically, but if you load from
      an `InputStream`, remember to close it after use.'
    question: Do I need to close streams manually when loading from a file path?
  - answer: The `LengthRecord` and `PathOperations` classes have been available since
      Aspose.PSD 20.10. Using the latest version (24.11 at time of writing) is recommended.
    question: What version of Aspose.PSD is required for these APIs?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- modify psd vector shapes
- Aspose.PSD
- Java image processing
- batch PSD processing
title: Изменение векторных фигур PSD с помощью Aspose.PSD for Java
url: /ru/java/advanced-psd-layer-features-effects/support-length-record-data-properties-psd/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Изменение векторных фигур PSD с помощью Aspose.PSD for Java

## Введение
Если вам необходимо **изменять векторные фигуры PSD** программно, Aspose.PSD for Java предоставляет полный контроль над файлами Photoshop непосредственно из вашего Java‑кода. Это руководство проведёт вас через поддержку свойств записей длины — необходимый шаг при редактировании слоёв векторных фигур. К концу вы сможете открыть PSD, скорректировать данные векторных фигур и сохранить обновлённый файл, не запуская Photoshop.

## Быстрые ответы
- **Что означает «изменять векторные фигуры PSD»?** Корректировка геометрии, операций пути или других атрибутов векторных слоёв внутри файла PSD.  
- **Какая библиотека это делает?** Aspose.PSD for Java.  
- **Нужна ли лицензия?** Бесплатная пробная версия подходит для оценки; для производства требуется коммерческая лицензия.  
- **Сколько времени занимает реализация?** Около 10‑15 минут для базового скрипта изменения фигур.  
- **Какие основные предварительные условия?** Java JDK, Aspose.PSD for Java и пример файла PSD.

## Что такое «поддержка свойств записей длины»?
Поддержка свойств записей длины означает доступ к объектам `LengthRecord`, описывающим каждый векторный путь внутри PSD. Эти записи хранят информацию о длине пути, типе и способе соединения с другими путями. Их изменение позволяет управлять тем, как фигуры объединяются, пересекаются или вычитаются друг из друга, обеспечивая точное векторное редактирование.

## Почему использовать Aspose.PSD for Java для поддержки свойств записей длины?
Загружайте PSD, редактируйте векторные данные и сохраняйте — всё без Photoshop. Aspose.PSD обрабатывает многосотенные PSD за менее чем 2 секунды на типичном сервере, предлагает более 150 классов (включая более 30 векторных типов) и работает под Windows, Linux или macOS с любой JDK 11+. Эта ориентированная на производительность библиотека устраняет необходимость в дорогостоящем настольном ПО.

## Требования
1. **Java Development Kit (JDK)** – загрузите с [Oracle's website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html) или используйте предпочитаемый менеджер пакетов.  
2. **Aspose.PSD for Java** – получите последнюю JAR‑файл со [Aspose releases page](https://releases.aspose.com/psd/java/).  
3. **IDE** – IntelliJ IDEA, Eclipse или любой совместимый с Java редактор.  
4. **Файл PSD** – создайте его в Photoshop или возьмите пример PSD для экспериментов.  
5. **Базовые знания Java** – знакомство с классами, объектами и обработкой исключений.

## Импорт пакетов
Операторы импорта подключают основные классы Aspose.PSD, такие как `PsdImage`, `VsmsResource` и `LengthRecord`.

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.LayerResource;
import com.aspose.psd.fileformats.psd.layers.layerresources.VsmsResource;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.LengthRecord;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.PathOperations;
```

## Шаг 1: Настройте исходные и выходные каталоги
Определите, где находится оригинальный PSD, и куда будет записан изменённый файл.

```java
String sourceDir = "Your Source Directory";
String outputDir = "Your Document Directory";
String inPsdFilePath = sourceDir + "PathOperationsShape.psd";
String outPsdFilePath = outputDir + "out_PathOperationsShape.psd";
```

## Шаг 2: Загрузите файл PSD
Используйте `Image.load` для открытия файла и приведения его к `PsdImage` для PSD‑специфических возможностей.

```java
PsdImage psdImage = (PsdImage) Image.load(inPsdFilePath);
```

## Шаг 3: Найдите ресурс Vsms в слое
`VsmsResource` — контейнер, хранящий данные векторных фигур слоя. Пройдите ресурсы второго слоя, чтобы найти его.

```java
VsmsResource resource = null;
for (LayerResource layerResource : psdImage.getLayers()[1].getResources()) {
    if (layerResource instanceof VsmsResource) {
        resource = (VsmsResource) layerResource;
        break;
    }
}
```

## Шаг 4: Доступ к записям длины
`LengthRecord` представляет отдельный векторный путь. Получите записи, которые планируете изменить.

```java
LengthRecord lengthRecord0 = (LengthRecord) resource.getPaths()[2];
LengthRecord lengthRecord1 = (LengthRecord) resource.getPaths()[7];
LengthRecord lengthRecord2 = (LengthRecord) resource.getPaths()[11];
```

## Шаг 5: Измените свойства операций пути
`PathOperations` определяет, как отдельные фигуры взаимодействуют (например, исключение, пересечение, вычитание). Изменение этих значений обновит визуальную композицию векторного слоя.

```java
lengthRecord0.setPathOperations(PathOperations.ExcludeOverlappingShapes);
lengthRecord1.setPathOperations(PathOperations.IntersectShapeAreas);
lengthRecord2.setPathOperations(PathOperations.SubtractFrontShape);
```

## Шаг 6: Сохраните изменённый файл PSD
Сохраните внесённые изменения в новый файл.

```java
psdImage.save(outPsdFilePath);
```

## Шаг 7: Очистка ресурсов
Освободите экземпляр `PsdImage`, чтобы освободить память и избежать утечек ресурсов.

```java
psdImage.dispose();
```

## Как пакетно обрабатывать файлы PSD с поддержкой свойств записей длины
Обёрните процесс работы с одним файлом в цикл, который проходит по каталогу PSD, обновляя `inPsdFilePath` и `outPsdFilePath` для каждого файла. Такой подход позволяет применять одинаковые корректировки векторных фигур к десяткам или сотням файлов за несколько минут, что идеально подходит для автоматизированных конвейеров ресурсов.

## Распространённые подводные камни и советы
- **Проверка на null** – всегда проверяйте, что `resource` не равен `null`, прежде чем обращаться к его членам.  
- **Границы индексов пути** – убедитесь, что используемые индексы (например, `[2]`, `[7]`, `[11]`) существуют в конкретном PSD, который редактируете.  
- **Лицензия** – запуск без действующей лицензии добавит водяной знак в сохранённый PSD.  

## Заключение
Теперь у вас есть полный пример от начала до конца, показывающий, как **изменять векторные фигуры PSD**, поддерживая свойства записей длины с помощью Aspose.PSD for Java. Независимо от того, автоматизируете ли вы конвейер ресурсов или создаёте собственный инструмент дизайна, эти API дают гибкость для манипуляций с векторными слоями без ручной работы в Photoshop. Поэкспериментируйте с другими значениями `PathOperations` или комбинируйте несколько правок `LengthRecord` для создания сложных фигур.

## Часто задаваемые вопросы

**В: Как обработать PSD, в котором нет слоёв векторных фигур?**  
О: `VsmsResource` будет отсутствовать, поэтому `resource` останется `null`. Добавьте проверку и пропустите шаг модификации или сообщите пользователю.

**В: Можно ли изменить другие свойства, например цвет заливки или толщину обводки?**  
О: Да, `LengthRecord` предоставляет сеттеры для заливки, обводки и непрозрачности. См. документацию API для полного списка.

**В: Возможно ли пакетно обрабатывать несколько файлов PSD?**  
О: Абсолютно. Оберните код в цикл, проходящий по каталогу PSD‑файлов, корректируя пути ввода и вывода каждый раз.

**В: Нужно ли закрывать потоки вручную при загрузке из пути к файлу?**  
О: `Image.load` автоматически управляет файловыми потоками, но если вы загружаете из `InputStream`, не забудьте закрыть его после использования.

**В: Какая версия Aspose.PSD требуется для этих API?**  
О: Классы `LengthRecord` и `PathOperations` доступны, начиная с Aspose.PSD 20.10. Рекомендуется использовать последнюю версию (24.11 на момент написания).

---

**Last Updated:** 2026-09-23  
**Tested With:** Aspose.PSD for Java 24.11  
**Author:** Aspose

## Связанные руководства

- [Convert PSD to PNG and Create Vector Mask Java – Vmsk Resource in PSD Files](/psd/java/advanced-psd-layer-features-effects/support-vmsk-resource-psd-files/)
- [Convert PSD to PNG with Layer Mask Support Using Aspose.PSD for Java](/psd/java/advanced-psd-layer-features-effects/support-layer-mask-psd-files/)
- [Add Layer Support Psd Files](/psd/java/advanced-psd-layer-features-effects/add-layer-support-psd-files/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}