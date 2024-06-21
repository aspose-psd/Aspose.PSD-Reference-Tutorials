---
title: Как добавить шаблон слоя обводки в Java
linktitle: Как добавить шаблон слоя обводки в Java
second_title: Aspose.PSD Java API
description: Узнайте, как добавить узор слоя обводки в PSD-файлы с помощью Aspose.PSD для Java. Следуйте этому пошаговому руководству, чтобы легко улучшить ваши изображения.
type: docs
weight: 11
url: /ru/java/java-graphics-drawing/add-stroke-layer-pattern/
---
## Введение
Добавление узора слоя обводки к изображению в Java может показаться сложной задачей, но с Aspose.PSD для Java это проще, чем вы думаете. Независимо от того, разрабатываете ли вы графику или работаете над приложениями для редактирования фотографий, это руководство шаг за шагом проведет вас через этот процесс. Готовы начать? Давайте погрузимся!
## Предварительные условия
Прежде чем начать, вам понадобится несколько вещей:
- Java Development Kit (JDK): убедитесь, что в вашей системе установлен JDK.
-  Aspose.PSD для Java: Загрузите библиотеку с сайта[здесь](https://releases.aspose.com/psd/java/) и включите его в свой проект.
- IDE: используйте свою любимую интегрированную среду разработки (IDE), например IntelliJ IDEA или Eclipse.
## Импортировать пакеты
Прежде всего, вам необходимо импортировать необходимые пакеты в ваш Java-проект. Эти пакеты необходимы для работы с Aspose.PSD.
```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;
import com.aspose.psd.Rectangle;
import com.aspose.psd.examples.Utils.Assert;
import com.aspose.psd.examples.Utils.Utils;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.BlendMode;
import com.aspose.psd.fileformats.psd.layers.fillsettings.FillType;
import com.aspose.psd.fileformats.psd.layers.fillsettings.PatternFillSettings;
import com.aspose.psd.fileformats.psd.layers.layereffects.StrokeEffect;
import com.aspose.psd.fileformats.psd.layers.layerresources.PattResource;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
import java.util.UUID;
```
## Шаг 1. Загрузите PSD-файл
Первым шагом в добавлении узора слоя обводки является загрузка PSD-файла, который вы хотите редактировать.
```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "Stroke.psd";
PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);
PsdImage im = (PsdImage)Image.load(sourceFileName, loadOptions);
```
Загрузив PSD-файл, вы теперь можете получить доступ к его слоям и эффектам и манипулировать ими.
## Шаг 2. Подготовьте новые данные шаблона
Далее вам необходимо подготовить новые данные узора, которые вы примените к слою с обводкой.
```java
int[] newPattern = new int[]
{
    Color.getAqua().toArgb(), Color.getRed().toArgb(), Color.getRed().toArgb(), Color.getAqua().toArgb(),
    Color.getAqua().toArgb(), Color.getWhite().toArgb(), Color.getWhite().toArgb(), Color.getAqua().toArgb(),
    Color.getAqua().toArgb(), Color.getWhite().toArgb(), Color.getWhite().toArgb(), Color.getAqua().toArgb(),
    Color.getAqua().toArgb(), Color.getRed().toArgb(), Color.getRed().toArgb(), Color.getAqua().toArgb(),
};
Rectangle newPatternBounds = new Rectangle(0, 0, 4, 4);
UUID guid = UUID.randomUUID();
```
Эти данные шаблона будут использоваться для создания нового эффекта обводки.
## Шаг 3: доступ к эффекту обводки
Чтобы изменить эффект обводки, вам необходимо получить доступ к определенному слою и параметрам его наложения.
```java
StrokeEffect patternStroke = (StrokeEffect)im.getLayers()[3].getBlendingOptions().getEffects()[0];
Assert.areEqual(BlendMode.Normal, patternStroke.getBlendMode());
Assert.areEqual(255, patternStroke.getOpacity());
Assert.areEqual(true, patternStroke.isVisible());
PatternFillSettings fillSettings = (PatternFillSettings)patternStroke.getFillSettings();
Assert.areEqual(FillType.Pattern, fillSettings.getFillType());
```
Это гарантирует, что вы работаете с правильным слоем и эффектом.
## Шаг 4: Измените эффект обводки
Теперь давайте изменим эффект обводки, используя новые данные узора.
### Обновить свойства эффекта обводки
```java
patternStroke.setOpacity((byte)127);
patternStroke.setBlendMode(BlendMode.Color);
```
### Обновите ресурс шаблона
```java
PattResource resource;
for (int i = 0; i < im.getGlobalLayerResources().length; i++)
{
    if (im.getGlobalLayerResources()[i] instanceof PattResource)
    {
        resource = (PattResource)im.getGlobalLayerResources()[i];
        resource.setPatternId(guid.toString());
        resource.setName("$$/Presets/Patterns/HorizontalLine1=Horizontal Line 9\0");
        resource.setPattern(newPattern, newPatternBounds);
    }
}
```
Этот фрагмент кода обновляет ресурс шаблона новыми данными шаблона.
## Шаг 5: Примените новый узор
Наконец, примените новый узор к эффекту обводки и сохраните изменения.
```java
((PatternFillSettings)patternStroke.getFillSettings()).setPatternName("$$/Presets/Patterns/HorizontalLine1=Horizontal Line 9\0");
((PatternFillSettings)patternStroke.getFillSettings()).setPatternId(guid.toString() + "\0");
im.save(exportPath);
```
Это гарантирует правильное применение нового шаблона и сохранение файла с изменениями.
## Шаг 6. Проверьте изменения.
Чтобы убедиться, что все работает правильно, загрузите файл еще раз и проверьте изменения.
```java
PsdImage img = (PsdImage)Image.load(sourceFileName, loadOptions);
StrokeEffect patternStrokeEffect = (StrokeEffect)img.getLayers()[3].getBlendingOptions().getEffects()[0];
PattResource resource1 = null;
for (int i = 0; i < img.getGlobalLayerResources().length; i++)
{
    if (img.getGlobalLayerResources()[i] instanceof PattResource)
    {
        resource1 = (PattResource)img.getGlobalLayerResources()[i];
    }
}
try
{
    Assert.areEqual(newPattern, resource1.getPatternData());
    Assert.areEqual(newPatternBounds, new Rectangle(0, 0, resource1.getWidth(), resource1.getHeight()));
    Assert.areEqual(guid.toString(), resource1.getPatternId());
    Assert.areEqual(BlendMode.Color, patternStrokeEffect.getBlendMode());
    Assert.areEqual(127, patternStrokeEffect.getOpacity());
    Assert.areEqual(true, patternStrokeEffect.isVisible());
    PatternFillSettings fillSettings1 = (PatternFillSettings)patternStrokeEffect.getFillSettings();
    Assert.areEqual(FillType.Pattern, fillSettings1.getFillType());
}
catch (Exception e)
{
    System.out.println(e.getMessage());
}
```
На этом этапе проверяется, что данные узора были правильно применены к эффекту обводки.
## Заключение
И вот оно! Вы успешно добавили узор слоя обводки в PSD-файл с помощью Aspose.PSD для Java. Следуя этим шагам, вы сможете легко настроить и улучшить свои изображения. Приятного кодирования!
## Часто задаваемые вопросы
### Что такое Aspose.PSD для Java?
Aspose.PSD для Java — это библиотека, которая позволяет разработчикам программно создавать, редактировать и конвертировать файлы PSD (документ Photoshop).
### Могу ли я использовать Aspose.PSD для Java в коммерческом проекте?
 Да, вы можете использовать его в коммерческих проектах. Вы можете приобрести лицензию у[здесь](https://purchase.aspose.com/buy).
### Доступна ли бесплатная пробная версия Aspose.PSD для Java?
 Да, вы можете скачать бесплатную пробную версию с сайта[здесь](https://releases.aspose.com/).
### Как я могу получить поддержку Aspose.PSD для Java?
 Вы можете получить поддержку на форумах сообщества Aspose.[здесь](https://forum.aspose.com/c/psd/34).
### Каковы системные требования для Aspose.PSD для Java?
Вам понадобится установленный JDK и IDE для разработки. Библиотека поддерживает несколько операционных систем, включая Windows, Linux и macOS.