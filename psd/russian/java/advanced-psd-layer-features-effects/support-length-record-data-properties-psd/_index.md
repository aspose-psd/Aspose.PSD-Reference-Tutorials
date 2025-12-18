---
date: 2025-12-17
description: Узнайте, как изменять векторные формы PSD, поддерживая свойства данных
  записей длины, с помощью Aspose.PSD для Java. Пошаговое руководство с примерами
  кода.
linktitle: Support Length Record Data Properties in PSD - Java
second_title: Aspose.PSD Java API
title: Как изменить векторные формы PSD – поддержка свойств данных Length Record в
  Java
url: /ru/java/advanced-psd-layer-features-effects/support-length-record-data-properties-psd/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Поддержка свойств данных записей длины в PSD - Java

## Введение
Если вам нужно **модифицировать векторные формы PSD** программно, библиотека Aspose.PSD for Java предоставляет полный контроль над файлами Photoshop прямо из вашего Java‑кода. В этом руководстве мы пройдемся по всем необходимым шагам для поддержки свойств данных записей длины — ключевого этапа при редактировании слоёв векторных форм. К концу вы сможете открыть PSD, изменить свойства его векторных форм и сохранить обновлённый файл, не покидая IDE. Поехали!

## Быстрые ответы
- **Что значит «модифицировать векторные формы PSD»?** Изменение геометрии, операций пути или других свойств векторных слоёв внутри PSD‑файла.  
- **Какая библиотека это делает?** Aspose.PSD for Java.  
- **Нужна ли лицензия?** Бесплатная trial‑версия подходит для оценки; для продакшна требуется коммерческая лицензия.  
- **Сколько времени займет реализация?** Около 10‑15 минут для базового скрипта изменения формы.  
- **Какие основные предпосылки?** Java JDK, Aspose.PSD for Java и пример PSD‑файла.

## Что такое «модифицировать векторные формы PSD»?
Модификация векторных форм PSD подразумевает изменение базовых данных векторного пути — например, записей длины и операций пути — чтобы визуальное представление форм обновилось соответствующим образом. Это особенно полезно для автоматизированных графических конвейеров, пакетной обработки или кастомных дизайнерских инструментов.

## Почему стоит использовать Aspose.PSD for Java для модификации векторных форм PSD?
- **Без Photoshop** — работайте напрямую с PSD‑файлами на любом сервере.  
- **Богатый API** — доступ к слоям, ресурсам и векторным данным через строго типизированные классы.  
- **Кросс‑платформенный** — запускается на Windows, Linux или macOS с любой JDK.  
- **Оптимизированный по производительности** — эффективное управление памятью и быстрые операции сохранения.

## Предпосылки
1. **Java Development Kit (JDK)** — скачайте с [сайта Oracle](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html) или используйте любимый пакетный менеджер.  
2. **Aspose.PSD for Java** — получите последнюю JAR‑ку с [страницы релизов Aspose](https://releases.aspose.com/psd/java/).  
3. **IDE** — IntelliJ IDEA, Eclipse или любой совместимый с Java редактор.  
4. **PSD‑файл** — создайте его в Photoshop или возьмите готовый пример для экспериментов.  
5. **Базовые знания Java** — понимание классов, объектов и обработки исключений.

## Импорт пакетов
Сначала импортируйте классы, необходимые для работы с PSD‑файлами и ресурсами векторных форм.

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.LayerResource;
import com.aspose.psd.fileformats.psd.layers.layerresources.VsmsResource;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.LengthRecord;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.PathOperations;
```

## Шаг 1: Настройка исходных и целевых каталогов
Определите, где находится оригинальный PSD, и куда будет сохранён модифицированный файл.

```java
String sourceDir = "Your Source Directory";
String outputDir = "Your Document Directory";
String inPsdFilePath = sourceDir + "PathOperationsShape.psd";
String outPsdFilePath = outputDir + "out_PathOperationsShape.psd";
```

## Шаг 2: Загрузка PSD‑файла
Используйте `Image.load`, чтобы открыть файл, и приведите его к `PsdImage` для доступа к специфичным для PSD возможностям.

```java
PsdImage psdImage = (PsdImage) Image.load(inPsdFilePath);
```

## Шаг 3: Поиск ресурса Vsms в слое
Данные векторных форм находятся внутри `VsmsResource`. Пройдите по ресурсам второго слоя, чтобы найти его.

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
Каждая `LengthRecord` представляет отдельный векторный путь. Получите те, которые планируете изменить.

```java
LengthRecord lengthRecord0 = (LengthRecord) resource.getPaths()[2];
LengthRecord lengthRecord1 = (LengthRecord) resource.getPaths()[7];
LengthRecord lengthRecord2 = (LengthRecord) resource.getPaths()[11];
```

## Шаг 5: Модификация свойств операций пути
Теперь вы можете **модифицировать векторные формы PSD**, изменяя их `PathOperations`. Это определяет, как формы взаимодействуют (например, исключение, пересечение, вычитание).

```java
lengthRecord0.setPathOperations(PathOperations.ExcludeOverlappingShapes);
lengthRecord1.setPathOperations(PathOperations.IntersectShapeAreas);
lengthRecord2.setPathOperations(PathOperations.SubtractFrontShape);
```

## Шаг 6: Сохранение изменённого PSD‑файла
Запишите изменения в новый файл.

```java
psdImage.save(outPsdFilePath);
```

## Шаг 7: Очистка ресурсов
Вызовите `dispose` у `PsdImage`, чтобы освободить память.

```java
psdImage.dispose();
```

## Распространённые ошибки и советы
- **Проверка на null** — всегда убеждайтесь, что `resource` не `null`, прежде чем обращаться к путям.  
- **Границы индексов пути** — убедитесь, что используемые индексы (`[2]`, `[7]`, `[11]`) действительно существуют в конкретном PSD.  
- **Лицензия** — работа без действующей лицензии добавит водяной знак в сохранённый PSD.  

## Заключение
Теперь у вас есть полноценный пример «сквозного» процесса, показывающий, как **модифицировать векторные формы PSD**, поддерживая свойства записей длины с помощью Aspose.PSD for Java. Будь то автоматизация конвейеров ассетов или создание собственного инструмента дизайна, эти API дают гибкость манипулировать векторными слоями без ручной работы в Photoshop. Экспериментируйте с другими `PathOperations` или комбинируйте несколько правок `LengthRecord` для создания сложных форм.

## Часто задаваемые вопросы

**В: Как обрабатывать PSD, в котором нет векторных слоёв?**  
О: `VsmsResource` будет отсутствовать, поэтому `resource` останется `null`. Добавьте проверку и пропустите шаг модификации или сообщите пользователю.

**В: Можно ли изменить другие свойства, например цвет заливки или толщину обводки?**  
О: Да, `LengthRecord` предоставляет дополнительные сеттеры для заливки, обводки и непрозрачности. Смотрите API‑документацию для подробностей.

**В: Можно ли пакетно обрабатывать несколько PSD‑файлов?**  
О: Конечно. Оберните код в цикл, который проходит по директории с PSD‑файлами, корректируя пути ввода и вывода каждый раз.

**В: Нужно ли вручную закрывать потоки при загрузке из пути к файлу?**  
О: Метод `Image.load` управляет файловыми потоками автоматически, но если вы загружаете из `InputStream`, не забудьте закрыть его после использования.

**В: Какая версия Aspose.PSD требуется для этих API?**  
О: Классы `LengthRecord` и `PathOperations` доступны, начиная с Aspose.PSD 20.10. Рекомендуется использовать последнюю версию.

---

**Последнее обновление:** 2025-12-17  
**Тестировано с:** Aspose.PSD for Java 24.11  
**Автор:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}