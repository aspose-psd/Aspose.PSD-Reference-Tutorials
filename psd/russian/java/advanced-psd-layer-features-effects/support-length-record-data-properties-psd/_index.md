---
date: 2026-02-20
description: Узнайте, как поддерживать свойства длины записи и пакетно обрабатывать
  PSD‑файлы с помощью Aspose.PSD для Java. Пошаговое руководство с примерами кода.
linktitle: Support Length Record Data Properties in PSD - Java
second_title: Aspose.PSD Java API
title: Поддержка свойств Length Record – Модификация векторных форм PSD (Java)
url: /ru/java/advanced-psd-layer-features-effects/support-length-record-data-properties-psd/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Поддержка свойств записей длины – Изменение векторных фигур PSD (Java)

## Введение
Если вам нужно **modify PSD vector shapes** программно, библиотека Aspose.PSD for Java предоставляет полный контроль над файлами Photoshop прямо из вашего Java‑кода. В этом руководстве мы пройдемся по всему, что вам необходимо знать, чтобы **support length record properties** — важный шаг, когда вы хотите редактировать слои векторных фигур. К концу вы сможете открыть PSD, изменить свойства его векторных фигур и сохранить обновлённый файл, не покидая IDE. Давайте начнём!

## Быстрые ответы
- **Что означает “modify PSD vector shapes”?** Регулировка геометрии, операций пути или других свойств слоёв, основанных на векторе, внутри файла PSD.  
- **Какая библиотека обрабатывает это?** Aspose.PSD for Java.  
- **Нужна ли лицензия?** Бесплатная пробная версия подходит для оценки; для производства требуется коммерческая лицензия.  
- **Сколько времени занимает реализация?** Около 10‑15 минут для базового скрипта изменения фигур.  
- **Каковы основные предпосылки?** Java JDK, Aspose.PSD for Java и пример файла PSD.

## Что такое “support length record properties”?
Поддержка свойств записей длины означает доступ к объектам `LengthRecord` и их обновление, которые описывают каждый векторный путь внутри PSD. Изменение этих записей позволяет управлять тем, как фигуры комбинируются, пересекаются или вычитаются друг из друга.

## Почему использовать Aspose.PSD for Java для поддержки свойств записей длины?
- **Не требуется Photoshop** — работа напрямую с файлами PSD на любом сервере.  
- **Богатый API** — доступ к слоям, ресурсам и векторным данным с помощью строго типизированных классов.  
- **Кросс‑платформенный** — работает на Windows, Linux или macOS с любой JDK.  
- **Ориентированный на производительность** — эффективное управление памятью и быстрые операции сохранения.  

## Предпосылки
1. **Java Development Kit (JDK)** — скачайте с [Oracle's website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html) или используйте предпочитаемый менеджер пакетов.  
2. **Aspose.PSD for Java** — получите последнюю JAR‑файл со [Aspose releases page](https://releases.aspose.com/psd/java/).  
3. **IDE** — IntelliJ IDEA, Eclipse или любой совместимый с Java редактор.  
4. **Файл PSD** — создайте его в Photoshop или возьмите пример PSD для экспериментов.  
5. **Базовые знания Java** — знакомство с классами, объектами и обработкой исключений.  

## Импорт пакетов
Сначала импортируйте классы, необходимые для работы с файлами PSD и ресурсами векторных фигур.

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.LayerResource;
import com.aspose.psd.fileformats.psd.layers.layerresources.VsmsResource;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.LengthRecord;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.PathOperations;
```

## Шаг 1: Настройте исходные и целевые каталоги
Укажите, где находится оригинальный PSD, и куда следует сохранить изменённый файл.

```java
String sourceDir = "Your Source Directory";
String outputDir = "Your Document Directory";
String inPsdFilePath = sourceDir + "PathOperationsShape.psd";
String outPsdFilePath = outputDir + "out_PathOperationsShape.psd";
```

## Шаг 2: Загрузите файл PSD
Используйте `Image.load` для открытия файла и приведения его к `PsdImage` для специфических возможностей PSD.

```java
PsdImage psdImage = (PsdImage) Image.load(inPsdFilePath);
```

## Шаг 3: Найдите ресурс Vsms в слое
Данные векторных фигур находятся внутри `VsmsResource`. Пройдите в цикле по ресурсам второго слоя, чтобы найти его.

```java
VsmsResource resource = null;
for (LayerResource layerResource : psdImage.getLayers()[1].getResources()) {
    if (layerResource instanceof VsmsResource) {
        resource = (VsmsResource) layerResource;
        break;
    }
}
```

## Шаг 4: Доступ к записям Length
Каждый `LengthRecord` представляет отдельный векторный путь. Получите те, которые вы планируете изменить.

```java
LengthRecord lengthRecord0 = (LengthRecord) resource.getPaths()[2];
LengthRecord lengthRecord1 = (LengthRecord) resource.getPaths()[7];
LengthRecord lengthRecord2 = (LengthRecord) resource.getPaths()[11];
```

## Шаг 5: Измените свойства операций пути
Теперь вы можете **modify PSD vector shapes**, изменяя их `PathOperations`. Это определяет, как фигуры взаимодействуют (например, исключение, пересечение, вычитание).

```java
lengthRecord0.setPathOperations(PathOperations.ExcludeOverlappingShapes);
lengthRecord1.setPathOperations(PathOperations.IntersectShapeAreas);
lengthRecord2.setPathOperations(PathOperations.SubtractFrontShape);
```

## Шаг 6: Сохраните изменённый файл PSD
Сохраните ваши изменения в новый файл.

```java
psdImage.save(outPsdFilePath);
```

## Шаг 7: Очистите ресурсы
Вызовите `dispose` у `PsdImage`, чтобы освободить память.

```java
psdImage.dispose();
```

## Как пакетно обрабатывать файлы PSD с поддержкой свойств записей длины
Если вам нужно применить одинаковые корректировки векторных фигур к множеству PSD, оберните приведённый выше код в цикл, который проходит по каталогу файлов. Обновляйте `inPsdFilePath` и `outPsdFilePath` для каждой итерации, и вы сможете **batch process PSD files** эффективно.

## Распространённые ошибки и советы
- **Проверки на null** — всегда проверяйте, что `resource` не `null`, перед доступом к путям.  
- **Границы индексов пути** — убедитесь, что используемые индексы (`[2]`, `[7]`, `[11]`) существуют в конкретном PSD, который вы редактируете.  
- **Лицензия** — запуск без действующей лицензии добавит водяной знак в сохранённый PSD.  

## Заключение
Теперь у вас есть полный пример от начала до конца, показывающий, как **modify PSD vector shapes**, поддерживая свойства записей длины с помощью Aspose.PSD for Java. Независимо от того, автоматизируете ли вы конвейеры ресурсов или создаёте собственный инструмент дизайна, эти API предоставляют гибкость для манипуляций с векторными слоями без ручной работы в Photoshop. Исследуйте дальше, экспериментируя с другими `PathOperations` или комбинируя несколько правок `LengthRecord` для сложных фигур.

## Часто задаваемые вопросы

**В: Как обрабатывать PSD, не содержащий слоёв векторных фигур?**  
О: `VsmsResource` будет отсутствовать, поэтому `resource` останется `null`. Добавьте проверку и пропустите шаг модификации или уведомите пользователя.

**В: Можно ли изменить другие свойства, например цвет заливки или ширину обводки?**  
О: Да, `LengthRecord` предоставляет дополнительные сеттеры для заливки, обводки и непрозрачности. Обратитесь к документации API для полной информации.

**В: Можно ли пакетно обрабатывать несколько файлов PSD?**  
О: Конечно. Оберните код в цикл, проходящий по каталогу файлов PSD, корректируя пути ввода и вывода каждый раз.

**В: Нужно ли вручную закрывать потоки при загрузке из пути к файлу?**  
О: Метод `Image.load` обрабатывает файловые потоки внутренне, но если вы загружаете из `InputStream`, не забудьте закрыть его после использования.

**В: Какая версия Aspose.PSD требуется для этих API?**  
О: Классы `LengthRecord` и `PathOperations` доступны, начиная с Aspose.PSD 20.10. Рекомендуется использовать последнюю версию.

---

**Последнее обновление:** 2026-02-20  
**Тестировано с:** Aspose.PSD for Java 24.11  
**Автор:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}