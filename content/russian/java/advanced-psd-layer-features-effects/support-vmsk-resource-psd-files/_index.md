---
title: Поддержка ресурсов Vmsk в PSD-файлах с помощью Java
linktitle: Поддержка ресурсов Vmsk в PSD-файлах с помощью Java
second_title: Aspose.PSD Java API
description: Легко управляйте ресурсами Vmsk в PSD-файлах с помощью Aspose.PSD для Java. Подробное пошаговое руководство, идеально подходящее как для разработчиков, так и для дизайнеров.
type: docs
weight: 23
url: /ru/java/advanced-psd-layer-features-effects/support-vmsk-resource-psd-files/
---
## Введение
Когда дело доходит до работы с файлами PSD (документ Photoshop), управление ресурсами имеет решающее значение, особенно при интеграции специальных функций, таких как ресурс Vmsk (векторная маска). Ресурсы Vmsk расширяют возможности дизайнеров, добавляя сложные векторные фигуры, что позволяет им без особых усилий создавать потрясающую графику. В этом руководстве мы на практике покажем вам, как поддерживать ресурсы Vmsk в PSD-файлах с помощью Aspose.PSD для Java. Независимо от того, являетесь ли вы разработчиком, желающим улучшить свое приложение, или дизайнером, стремящимся к автоматизации, это руководство шаг за шагом проведет вас через весь процесс, упрощая его выполнение и реализацию.
## Предварительные условия
Прежде чем мы углубимся в пикантные подробности работы с ресурсами Vmsk, давайте убедимся, что у вас есть все необходимое для бесперебойной работы.
### Что вам нужно
-  Комплект разработки Java (JDK): убедитесь, что на вашем компьютере установлен JDK. Если нет, вы можете скачать его с сайта[веб-сайт Oracle](https://www.oracle.com/java/technologies/javase-downloads.html).
- Библиотека Aspose.PSD для Java: это мощная библиотека для управления PSD-файлами. Вы можете скачать его с сайта[Страница релиза Aspose](https://releases.aspose.com/psd/java/) . Для тех, кто хочет попробовать, прежде чем покупать, вы также можете начать с[бесплатная пробная версия](https://releases.aspose.com/).
- IDE: для этого проекта подойдет любая IDE для Java (например, IntelliJ IDEA, Eclipse и т. д.).
### Настройка вашего рабочего пространства
1. Создайте новый проект Java. Запустите предпочитаемую вами среду IDE и создайте новый проект Java. Это ваша площадка для работы с кодом.
2. Добавьте библиотеку Aspose. После загрузки библиотеки Aspose добавьте файл jar в библиотеки вашего проекта. Этот шаг имеет решающее значение, поскольку он позволяет нам использовать все замечательные возможности Aspose.PSD.
Выполнив эти предварительные условия, вы можете приступить к созданию, изменению PSD-файлов и управлению ими с помощью ресурсов Vmsk. Давайте приступим непосредственно к программированию!
## Импортировать пакеты
Прежде чем мы сможем работать с PSD-файлами, нам необходимо импортировать необходимые пакеты. Это основа нашего кода, предоставляющая нам доступ к различным классам и методам, которые предлагает библиотека Aspose.PSD.
```java
import com.aspose.psd.Image;
import com.aspose.psd.Point;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.Layer;
import com.aspose.psd.fileformats.psd.layers.LayerResource;
import com.aspose.psd.fileformats.psd.layers.layerresources.VmskResource;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.BezierKnotRecord;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.InitialFillRuleRecord;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.LengthRecord;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.PathFillRuleRecord;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.VectorPathType;
```
Теперь, когда мы подготовили почву, пришло время действовать! В этом разделе мы разобьем код на управляемые шаги. Эти шаги помогут вам прочитать PSD-файл, обработать ресурс Vmsk и даже отредактировать его.
## Шаг 1. Загрузите PSD-файл
Первое, что вам нужно сделать, это загрузить PSD-файл. Вот тут-то и начинается вся магия.
```java
String dataDir = "Your Document Directory"; // Обновить этот путь
String sourceFileName = dataDir + "Rectangle.psd";
PsdImage im = (PsdImage) Image.load(sourceFileName);
```

-  Мы установили`dataDir` в каталог вашего PSD-файла. 
-  Мы создаем строку для`sourceFileName`, объединяя каталог с именем PSD-файла.
-  Наконец, мы загружаем PSD-файл в`PsdImage` объект с использованием`Image.load()`.
## Шаг 2. Получите ресурс Vmsk
Теперь, когда у нас загружено PSD-изображение, давайте получим ресурс Vmsk.
```java
VmskResource resource = getVmskResource(im);
```

-  Мы называем`getVmskResource()` метод, который обрабатывает поиск и получение ресурса Vmsk из образа.
## Шаг 3. Проверка свойств ресурса Vmsk
Прежде чем приступить к изменениям, важно убедиться, что наш ресурс Vmsk находится в ожидаемом состоянии.
```java
if (resource.isDisabled() != false ||
	resource.isInverted() != false ||
	resource.isNotLinked() != false ||
	resource.getPaths().length != 7) {
	throw new RuntimeException("VmskResource was read wrong");
}
```

- Здесь мы проверяем различные свойства ресурса Vmsk. Мы хотим убедиться, что он не отключен, не инвертирован и не связан, и что он имеет правильное количество путей.
## Шаг 4. Получите доступ к каждому пути и проверьте
Давайте копнем немного глубже и проверим пути внутри ресурса Vmsk.
```java
PathFillRuleRecord pathFillRule = (PathFillRuleRecord) resource.getPaths()[0];
InitialFillRuleRecord initialFillRule = (InitialFillRuleRecord) resource.getPaths()[1];
LengthRecord subpathLength = (LengthRecord) resource.getPaths()[2];
if (pathFillRule.getType() != VectorPathType.PathFillRuleRecord ||
	initialFillRule.getType() != VectorPathType.InitialFillRuleRecord ||
	initialFillRule.isFillStartsWithAllPixels() != false ||
	subpathLength.getType() != VectorPathType.ClosedSubpathLengthRecord ||
	subpathLength.isClosed() != true) {
	throw new RuntimeException("VmskResource paths were read wrong");
}
```

- Мы извлекаем три конкретные записи пути и проверяем их типы и свойства, чтобы убедиться, что они соответствуют нашим критериям.
## Шаг 5. Отредактируйте ресурс Vmsk
Теперь мы переходим к части модификации! При необходимости вы можете настроить свойства ресурса Vmsk.
```java
resource.setDisabled(true);
resource.setInverted(true);
resource.setNotLinked(true);
```

- В этом блоке мы переключаем различные свойства ресурса Vmsk. Установив для них значение true, мы можем контролировать поведение маски в PSD-файле.
## Шаг 6: Измените узлы Безье
Узлы Безье имеют решающее значение для векторных путей. Давайте изменим здесь некоторые значения.
```java
BezierKnotRecord bezierKnot = (BezierKnotRecord) resource.getPaths()[3];
bezierKnot.getPoints()[0] = new Point(0, 0);
bezierKnot = (BezierKnotRecord) resource.getPaths()[4];
bezierKnot.getPoints()[0] = new Point(8039797, 10905190);
```

-  Мы получаем доступ к конкретным`BezierKnotRecord` пути и изменение их точек, чтобы потенциально изменить форму векторной маски.
## Шаг 7. Сохраните измененный PSD-файл.
После завершения всех изменений пришло время сохранить измененный PSD-файл. 
```java
String exportPath = dataDir + "Rectangle_changed.psd";
im.save(exportPath);
```

-  Мы устанавливаем путь к экспортированному PSD-файлу, а затем вызываем`im.save()` чтобы записать изменения в этот новый файл.
## Шаг 8: Очистите ресурсы
Наконец, нам нужно убедиться, что мы правильно избавляемся от образа, чтобы освободить ресурсы.
```java
im.dispose();
```

- Всегда полезно избавиться от любых ресурсов, как только вы закончите. Это помогает избежать утечек памяти в ваших приложениях.
## Заключение
Поздравляем! Вы только что прошли подробный процесс поддержки ресурсов Vmsk в файлах PSD с использованием Aspose.PSD для Java. Загрузив изображение, получив и проверив ресурс Vmsk, отредактировав его свойства и затем сохранив измененный PSD, вы рассмотрели самое необходимое. Обладая этими навыками, вы сможете эффективно управлять и использовать различные ресурсы в файлах PSD, улучшая свои проекты графического дизайна или сценарии автоматизации.
## Часто задаваемые вопросы
### Что такое ресурс Vmsk?
Ресурс Vmsk — это векторная маска в PSD-файле, позволяющая создавать сложные векторные фигуры и функции редактирования.
### Могу ли я использовать Aspose.PSD в проекте Maven?
Да, вы можете включить Aspose.PSD в качестве зависимости в свой проект Maven, используя его координаты из репозитория.
### В каком формате я могу сохранить модифицированные PSD-файлы?
Вы можете сохранить их обратно в формате PSD или экспортировать в другие форматы, такие как PNG, JPEG и т. д.
### Доступна ли бесплатная пробная версия Aspose.PSD?
 Да, вы можете получить доступ к бесплатной пробной версии Aspose.PSD, чтобы протестировать ее функции. Посетите[ссылка на бесплатную пробную версию](https://releases.aspose.com/).
### Как я могу получить поддержку для Aspose.PSD?
 Вы можете присоединиться к[Aspose форум](https://forum.aspose.com/c/psd/34)для поддержки и помощи в устранении неполадок.