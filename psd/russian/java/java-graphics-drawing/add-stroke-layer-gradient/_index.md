---
title: Как добавить градиент слоя обводки в Java
linktitle: Как добавить градиент слоя обводки в Java
second_title: Aspose.PSD Java API
description: Узнайте, как добавлять и настраивать градиенты слоя обводки в файлах PSD с помощью Aspose.PSD для Java, с помощью этого подробного пошагового руководства.
weight: 10
url: /ru/java/java-graphics-drawing/add-stroke-layer-gradient/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Как добавить градиент слоя обводки в Java

## Введение
Вы когда-нибудь задумывались, как добавить градиент слоя обводки к вашим изображениям с помощью Java? Ну, вы в правильном месте! Сегодня мы погружаемся в мир Aspose.PSD для Java, мощной библиотеки, которая помогает вам с легкостью манипулировать PSD-файлами. Независимо от того, являетесь ли вы новичком или опытным разработчиком, это пошаговое руководство проведет вас через процесс добавления градиента слоя обводки в ваши PSD-файлы. Итак, пристегнитесь и приготовьтесь улучшить свои навыки графического редактирования!
## Предварительные условия
Прежде чем мы начнем, вам нужно кое-что сделать. Убедитесь, что у вас есть следующее:
1.  Комплект разработки Java (JDK): убедитесь, что в вашей системе установлен JDK. Вы можете скачать его с[сайт Oracle](https://www.oracle.com/java/technologies/javase-downloads.html).
2.  Aspose.PSD для библиотеки Java: его можно загрузить с сайта[Страница загрузки Aspose.PSD](https://releases.aspose.com/psd/java/).
3. Интегрированная среда разработки (IDE). Подойдет любая IDE, например IntelliJ IDEA, Eclipse или NetBeans.
4.  Действующая лицензия: вы можете получить[временная лицензия](https://purchase.aspose.com/temporary-license/) если у вас нет полного.
## Импортировать пакеты
Перво-наперво, давайте импортируем необходимые пакеты. Это позволит нам использовать классы и методы, необходимые для управления PSD-файлом.
```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;
import com.aspose.psd.examples.Utils.Assert;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.BlendMode;
import com.aspose.psd.fileformats.psd.layers.IGradientColorPoint;
import com.aspose.psd.fileformats.psd.layers.fillsettings.FillType;
import com.aspose.psd.fileformats.psd.layers.fillsettings.GradientColorPoint;
import com.aspose.psd.fileformats.psd.layers.fillsettings.GradientFillSettings;
import com.aspose.psd.fileformats.psd.layers.fillsettings.GradientTransparencyPoint;
import com.aspose.psd.fileformats.psd.layers.fillsettings.GradientType;
import com.aspose.psd.fileformats.psd.layers.fillsettings.IGradientTransparencyPoint;
import com.aspose.psd.fileformats.psd.layers.layereffects.StrokeEffect;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
```
Теперь давайте разобьем пример на несколько этапов для лучшего понимания.
## Шаг 1. Загрузите PSD-файл
 Сначала нам нужно загрузить PSD-файл, который мы хотим изменить. Мы будем использовать`PsdLoadOptions` чтобы указать, что мы хотим загрузить ресурсы эффектов.
```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "Stroke.psd";
String exportPath = dataDir + "StrokeGradientChanged.psd";
PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);
PsdImage im = (PsdImage) Image.load(sourceFileName, loadOptions);
```
## Шаг 2: доступ к эффекту обводки
Далее нам нужно получить доступ к эффекту обводки интересующего нас слоя. Здесь мы предполагаем, что это третий слой (индекс 2) в PSD-файле.
```java
StrokeEffect gradientStroke = (StrokeEffect) im.getLayers()[2].getBlendingOptions().getEffects()[0];
```
## Шаг 3. Проверьте свойства эффекта обводки
Прежде чем вносить какие-либо изменения, давайте проверим свойства эффекта обводки, чтобы убедиться, что мы изменяем правильные настройки.
```java
Assert.areEqual(BlendMode.Normal, gradientStroke.getBlendMode());
Assert.areEqual(255, gradientStroke.getOpacity());
Assert.areEqual(true, gradientStroke.isVisible());
GradientFillSettings fillSettings = (GradientFillSettings) gradientStroke.getFillSettings();
Assert.areEqual(Color.getBlack(), fillSettings.getColor());
Assert.areEqual(FillType.Gradient, fillSettings.getFillType());
Assert.areEqual(true, fillSettings.getAlignWithLayer());
Assert.areEqual(GradientType.Linear, fillSettings.getGradientType());
Assert.isTrue(Math.abs(90 - fillSettings.getAngle()) < 0.001, "Angle is incorrect");
Assert.areEqual(false, fillSettings.getDither());
Assert.isTrue(Math.abs(0 - fillSettings.getHorizontalOffset()) < 0.001, "Horizontal offset is incorrect");
Assert.isTrue(Math.abs(0 - fillSettings.getVerticalOffset()) < 0.001, "Vertical offset is incorrect");
Assert.areEqual(false, fillSettings.getReverse());
```
## Шаг 4. Измените настройки градиентной заливки
Теперь пришло время изменить настройки градиентной заливки в соответствии с нашими требованиями. Мы изменим цвет, непрозрачность, режим наложения и другие свойства.
```java
fillSettings.setColor(Color.getGreen());
gradientStroke.setOpacity((byte) 127);
gradientStroke.setBlendMode(BlendMode.Color);
fillSettings.setAlignWithLayer(false);
fillSettings.setGradientType(GradientType.Radial);
fillSettings.setAngle(45);
fillSettings.setDither(true);
fillSettings.setHorizontalOffset(15);
fillSettings.setVerticalOffset(11);
fillSettings.setReverse(true);
```
## Шаг 5. Добавьте и измените точки цвета и прозрачности
Давайте добавим новые точки цвета и прозрачности и изменим существующие, чтобы добиться желаемого эффекта градиента.
```java
// Добавить новую цветовую точку
GradientColorPoint colorPoint = fillSettings.addColorPoint();
colorPoint.setColor(Color.getGreen());
colorPoint.setLocation(4096);
colorPoint.setMedianPointLocation(75);
// Изменить местоположение предыдущей точки
fillSettings.getColorPoints()[1].setLocation(1899);
// Добавить новую точку прозрачности
GradientTransparencyPoint transparencyPoint = fillSettings.addTransparencyPoint();
transparencyPoint.setOpacity(25);
transparencyPoint.setMedianPointLocation(25);
transparencyPoint.setLocation(4096);
// Изменить местоположение предыдущей точки прозрачности
fillSettings.getTransparencyPoints()[1].setLocation(2411);
```
## Шаг 6. Сохраните измененный PSD-файл.
После внесения всех необходимых изменений нам нужно сохранить PSD-файл.
```java
im.save(exportPath);
```
## Шаг 7. Проверьте изменения
Наконец, давайте загрузим сохраненный PSD-файл и проверим, что наши изменения были применены правильно.
```java
PsdImage img = (PsdImage) Image.load(exportPath, loadOptions);
StrokeEffect gradientStrokeEffect = (StrokeEffect) img.getLayers()[2].getBlendingOptions().getEffects()[0];
Assert.areEqual(BlendMode.Color, gradientStrokeEffect.getBlendMode());
Assert.areEqual(127, gradientStrokeEffect.getOpacity());
Assert.areEqual(true, gradientStrokeEffect.isVisible());
GradientFillSettings fillSetting = (GradientFillSettings) gradientStrokeEffect.getFillSettings();
Assert.areEqual(Color.getGreen(), fillSetting.getColor());
Assert.areEqual(FillType.Gradient, fillSetting.getFillType());
// Проверьте цветовые точки
Assert.areEqual(3, fillSetting.getColorPoints().length);
IGradientColorPoint point = fillSetting.getColorPoints()[0];
Assert.areEqual(50, point.getMedianPointLocation());
Assert.areEqual(Color.getBlack(), point.getColor());
Assert.areEqual(0, point.getLocation());
point = fillSettings.getColorPoints()[1];
Assert.areEqual(50, point.getMedianPointLocation());
Assert.areEqual(Color.getWhite(), point.getColor());
Assert.areEqual(1899, point.getLocation());
point = fillSettings.getColorPoints()[2];
Assert.areEqual(75, point.getMedianPointLocation());
Assert.areEqual(Color.getGreen(), point.getColor());
Assert.areEqual(4096, point.getLocation());
// Проверьте точки прозрачности
Assert.areEqual(3, fillSettings.getTransparencyPoints().length);
IGradientTransparencyPoint transparencyPoint1 = fillSettings.getTransparencyPoints()[0];
Assert.areEqual(50, transparencyPoint1.getMedianPointLocation());
Assert.areEqual(100, transparencyPoint1.getOpacity());
Assert.areEqual(0, transparencyPoint1.getLocation());
transparencyPoint1 = fillSettings.getTransparencyPoints()[1];
Assert.areEqual(50, transparencyPoint.getMedianPointLocation());
Assert.areEqual(100, transparencyPoint.getOpacity());
Assert.areEqual(2411, transparencyPoint.getLocation());
transparencyPoint1 = fillSettings.getTransparencyPoints()[2];
Assert.areEqual(25, transparencyPoint.getMedianPointLocation());
Assert.areEqual(25, transparencyPoint.getOpacity());
Assert.areEqual(4096, transparencyPoint.getLocation());
```
## Заключение
И вот оно! Теперь вы знаете, как добавлять градиенты слоя обводки в PSD-файлах и управлять ими с помощью Aspose.PSD для Java. В этом уроке рассказывается о загрузке PSD-файла, доступе и изменении эффектов обводки, а также сохранении изменений. Обладая этими навыками, вы сможете создавать визуально привлекательные градиенты и настраивать PSD-файлы в соответствии со своими потребностями.
## Часто задаваемые вопросы
### Что такое Aspose.PSD для Java?
Aspose.PSD для Java — это библиотека, которая позволяет разработчикам работать с PSD-файлами в приложениях Java, предоставляя функции для создания, управления и преобразования PSD-файлов.
### Нужна ли мне лицензия для использования Aspose.PSD для Java?
 Да, вам нужна действующая лицензия для использования Aspose.PSD для Java. Вы можете получить[временная лицензия](https://purchase.aspose.com/temporary-license/) в целях оценки.
### Могу ли я использовать Aspose.PSD для Java для создания PSD-файлов с нуля?
Абсолютно! Aspose.PSD для Java предоставляет комплексные API для программного создания файлов PSD и управления ими.
### Можно ли применить другие эффекты с помощью Aspose.PSD для Java?
Да, вы можете применять различные эффекты, такие как тень, свечение и т. д., используя Aspose.PSD для Java.
### Где я могу найти документацию по Aspose.PSD для Java?
 Вы можете найти документацию[здесь](https://reference.aspose.com/psd/java/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
