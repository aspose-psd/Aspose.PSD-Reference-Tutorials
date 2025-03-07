---
title: Корректирующий слой уровня рендеринга в файлах PSD — Java
linktitle: Корректирующий слой уровня рендеринга в файлах PSD — Java
second_title: Aspose.PSD Java API
description: Узнайте, как легко повысить контрастность и яркость изображения с помощью Aspose.PSD для Java. Освойте корректирующие слои уровней с помощью этого пошагового руководства.
weight: 17
url: /ru/java/psd-layer-management-effects/render-level-adjustment-layer-psd/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Корректирующий слой уровня рендеринга в файлах PSD — Java

## Введение

Вы когда-нибудь открывали PSD-файл и обнаруживали, что изображению не хватает контрастности или яркости? Не бойтесь, воины редактирования изображений! Aspose.PSD для Java приходит на помощь благодаря своим мощным возможностям манипулирования корректирующим слоем уровней. Это руководство даст вам знания о том, как с легкостью настроить ваши изображения с помощью уровней. 

## Предварительные условия

- Комплект разработки Java (JDK). Убедитесь, что в вашей системе установлена последняя версия JDK. Его можно скачать с сайта Oracle ([https://www.oracle.com/java/technologies/javase-downloads.html](https://www.oracle.com/java/technologies/javase-downloads.html)).
- Библиотека Aspose.PSD для Java: загрузите библиотеку Aspose.PSD для Java со страницы загрузки ([https://releases.aspose.com/psd/java/](https://releases.aspose.com/psd/java/)). Для использования всех функций вам понадобится действующая лицензия, но для начала доступна бесплатная пробная версия ([https://releases.aspose.com/](https://releases.aspose.com/)).

## Импортировать пакеты

Прежде чем углубиться в код, нам нужно импортировать необходимые классы Aspose.PSD для взаимодействия с PSD-файлами. Вот что вам понадобится:

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.adjustmentlayers.LevelsLayer;
import com.aspose.psd.fileformats.psd.layers.layerresources.LevelChannel;
import com.aspose.psd.imageoptions.PngOptions;
```

`com.aspose.psd` пакет предоставляет доступ к функциям манипулирования PSD, в то время как`com.aspose.psd.imaging.PngOptions` позволяет нам определять параметры при сохранении изображения в формате PNG.

Теперь давайте приступим к нашему приключению по настройке уровней:

## Шаг 1. Настройка путей к файлам:

- Определите переменные для каталога вашего документа (`dataDir`), имя исходного PSD-файла (`sourceFileName`), имя целевого PSD-файла после модификации (`psdPathAfterChange`) и окончательный путь экспорта PNG (`pngExportPath`). Рассмотрите возможность использования описательных имен для улучшения читаемости кода.

```java
String dataDir = "Your Document Directory";

String sourceFileName = dataDir + "LevelsAdjustmentLayer.psd";
String psdPathAfterChange = dataDir + "LevelsAdjustmentLayerChanged.psd";
String pngExportPath = dataDir + "LevelsAdjustmentLayerChanged.png";
```

## Шаг 2. Загрузка PSD-изображения:

-  Используйте`Image.load` способ открыть исходный PSD-файл и сохранить его в`PsdImage`объект (`im`). Aspose.PSD автоматически определяет формат файла.

```java
PsdImage im = (PsdImage)Image.load(sourceFileName);
```

## Шаг 3. Перебор слоев:

- Нам нужно найти корректирующий слой «Уровни» в вашем PSD. Aspose предоставляет удобный способ перебора всех слоев с помощью цикла.

```java
for (int i = 0; i < im.getLayers().length; i++) {
   // ... (здесь будет добавлен код для проверки слоя уровней)
}
```

## Шаг 4: Определение слоя уровней:

- Внутри цикла проверьте, является ли текущий слой (`im.getLayers()[i]` ) является экземпляром`LevelsLayer` класс, используя`instanceof` оператор. 
-  Если это так, приведите слой к`LevelsLayer` объект для дальнейших манипуляций.

```java
for (int i = 0; i < im.getLayers().length; i++) {
   if (im.getLayers()[i] instanceof LevelsLayer) {
	   LevelsLayer levelsLayer = (LevelsLayer) im.getLayers()[i];
	   // ... (здесь будет добавлен код для настройки уровней)
   }
}
```
## Шаг 5. Точная настройка уровней (продолжение):

-  Отрегулируйте выходные уровни с помощью`setOutputShadowLevel` и`setOutputHighlightLevel` для управления темнотой и светлотой получаемого изображения. Эти значения определяют диапазон входных уровней, которые будут сопоставлены с выходным диапазоном.

```java
for (int i = 0; i < im.getLayers().length; i++) {
   if (im.getLayers()[i] instanceof LevelsLayer) {
	   LevelsLayer levelsLayer = (LevelsLayer) im.getLayers()[i];
	   LevelChannel channel = levelsLayer.getChannel(0);

	   // Отрегулируйте входные уровни (0–255):
	   channel.setInputShadowLevel((short) 10); // Немного затемните тени
	   channel.setInputMidtoneLevel(2.0f);     // Увеличьте средние тона
	   channel.setInputHighlightLevel((short) 230); // Уменьшить выделение

	   // Настройка выходных уровней (0–255):
	   channel.setOutputShadowLevel((short) 20); // Далее затемните тени
	   channel.setOutputHighlightLevel((short) 200); //Сделайте блики ярче
   }
}
```

## Шаг 6: Сохранение измененного PSD:

-  Используйте`save` метод`PsdImage` объект для сохранения измененного изображения по указанному пути (`psdPathAfterChange`).

```java
im.save(psdPathAfterChange);
```

## Шаг 7. Экспорт в формате PNG (необязательно):

-  Если вам нужна PNG-версия скорректированного изображения, создайте`PngOptions` объект и установите тип цвета на`TruecolorWithAlpha` . Затем используйте`save` повторите метод с указанием пути экспорта PNG и параметров.

```java
PngOptions saveOptions = new PngOptions();
saveOptions.setColorType(PngColorType.TruecolorWithAlpha);
im.save(pngExportPath, saveOptions);
```

И вот оно! Вы успешно настроили корректирующий слой «Уровни» в своем PSD-файле с помощью Aspose.PSD для Java. Поняв эти шаги и поэкспериментировав с различными значениями, вы сможете улучшить контрастность и общий вид ваших изображений.

## Заключение

Aspose.PSD для Java позволяет вам контролировать процесс редактирования изображений. Освоив корректирующий слой «Уровни», вы сможете вдохнуть новую жизнь в свои фотографии и дизайны. Помните: практика ведет к совершенству, поэтому не стесняйтесь экспериментировать и исследовать весь потенциал этого мощного инструмента.
 
## Часто задаваемые вопросы

### Могу ли я настроить отдельные цветовые каналы (RGB) отдельно? 
Да, вы можете получить доступ к каждому цветовому каналу, используя`getChannel` метод`LevelsLayer` объект и самостоятельно изменять его уровни.

### Как обрабатывать несколько корректирующих слоев уровней в PSD?
Код перебирает все слои, поэтому он автоматически обрабатывает любые дополнительные слои уровней, найденные на изображении.

### Есть ли другие способы настройки контрастности изображения, кроме «Уровней»?
Абсолютно! Aspose.PSD предлагает различные инструменты настройки изображения, такие как кривые, яркость/контрастность и другие.

### Могу ли я автоматизировать этот процесс для нескольких изображений? 
Да, вы можете включить этот код в сценарий циклической или пакетной обработки для эффективной обработки нескольких файлов PSD.

### Где я могу найти дополнительную информацию и поддержку?
Aspose предоставляет обширную документацию ([https://reference.aspose.com/psd/java/](https://reference.aspose.com/psd/java/)) и форум поддержки ([https://forum.aspose.com/c/psd/34](https://forum.aspose.com/c/psd/34)) по любым вопросам или проблемам, с которыми вы можете столкнуться.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
