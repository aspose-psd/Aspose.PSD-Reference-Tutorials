---
title: Добавьте корректирующий слой «Насыщенность оттенка» в PSD
linktitle: Добавьте корректирующий слой «Насыщенность оттенка» в PSD
second_title: Aspose.PSD Java API
description: Узнайте, как добавить корректирующие слои насыщенности оттенка в PSD с помощью Aspose.PSD для Java, в этом подробном пошаговом руководстве. Улучшите свой рабочий процесс графического дизайна.
weight: 14
url: /ru/java/modifying-converting-psd-images/add-hue-saturation-adjustment-layer-psd/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Добавьте корректирующий слой «Насыщенность оттенка» в PSD

## Введение
Когда дело доходит до графического дизайна, манипуляции с цветом играют ключевую роль — в частности, настройка оттенка, насыщенности и яркости может радикально изменить настроение и качество любого изображения. Один из эффективных способов добиться этого — использование корректирующих слоев в Photoshop (файлы PSD). Если вы хотите программно улучшить свои PSD-файлы с помощью Java, вам поможет библиотека Aspose.PSD! В этом руководстве вы узнаете, как добавить корректирующий слой «Насыщенность оттенка» в ваши PSD-файлы, что сделает ваши рабочие процессы более продуктивными и эффективными.
В этом руководстве мы рассмотрим все: от импорта необходимых пакетов до мельчайших деталей примеров кода.
## Предварительные условия
Прежде чем мы перейдем к коду, убедитесь, что у вас есть следующее:
1.  Java Development Kit (JDK): убедитесь, что на вашем компьютере установлен JDK 8 или более поздней версии. Вы можете скачать его с сайта[Загрузки комплекта разработки Java SE](https://www.oracle.com/java/technologies/javase-downloads.html).
2.  Aspose.PSD для библиотеки Java: вам понадобится библиотека Aspose.PSD, которую вы можете[скачать здесь](https://releases.aspose.com/psd/java/). 
3. IDE: подходящая интегрированная среда разработки (IDE), такая как IntelliJ IDEA или Eclipse, для разработки на Java.
4. Базовые знания Java: Знание программирования на Java будет плюсом, но не волнуйтесь; мы шаг за шагом проведем вас через код.
Теперь, когда мы разобрались с предварительными условиями, давайте перейдем к самому интересному — кодированию!
## Импортировать пакеты
Чтобы начать работу с библиотекой Aspose.PSD, первым делом необходимо импортировать необходимые классы. Вот как вы можете сделать это в своем Java-файле:
```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.adjustmentlayers.HueSaturationLayer;
import com.aspose.psd.fileformats.psd.layers.layerresources.ColorRangeHsl;
```
Убедитесь, что в ваш проект добавлены соответствующие библиотеки, чтобы импорт работал без проблем.
## Шаг 1. Настройте каталог документов
Каждому проекту нужна отправная точка, и наш не исключение. Вам необходимо указать каталог, в котором хранятся ваши PSD-файлы. Это крайне важно для правильной загрузки и сохранения изображений.
```java
String dataDir = "Your Document Directory"; // Обновите этот путь до вашего фактического каталога.
```
## Шаг 2. Загрузите существующий PSD-файл
Чтобы манипулировать существующим PSD-файлом, нам сначала необходимо загрузить его в нашу программу. Вот как вы можете это сделать:
```java
String sourceFileName = dataDir + "HueSaturationAdjustmentLayer.psd";
PsdImage im = (PsdImage) Image.load(sourceFileName);
```
 В этом коде обновите`"HueSaturationAdjustmentLayer.psd"` к имени существующего PSD-файла, который вы хотите отредактировать.
## Шаг 3. Отредактируйте слой «Цветовой тон/Насыщенность»
Далее мы пройдемся по слоям загруженного PSD-изображения, чтобы найти и отредактировать любые существующие слои оттенка/насыщенности. Этот шаг включает в себя изменение значений оттенка, насыщенности и яркости.
```java
for (int i = 0; i < im.getLayers().length; i++) {
    if (im.getLayers()[i] instanceof HueSaturationLayer) {
        HueSaturationLayer hueLayer = (HueSaturationLayer) im.getLayers()[i];
        hueLayer.setHue((short) -25);
        hueLayer.setSaturation((short) -12);
        hueLayer.setLightness((short) 67);
        ColorRangeHsl colorRange = hueLayer.getRange(2);
        colorRange.setHue((short) -40);
        colorRange.setSaturation((short) 50);
        colorRange.setLightness((short) -20);
        colorRange.setMostLeftBorder((short) 300);
    }
}
```
В этом примере:
- Мы регулируем оттенок до -25, насыщенность до -12 и яркость до +67.
- `getRange(2)` Метод позволяет нам настраивать определенные цветовые диапазоны по желанию.
## Шаг 4. Сохраните измененный PSD-файл.
После внесения изменений следующим шагом будет сохранение файла. Это жизненно важная часть нашего процесса, гарантирующая, что внесенные нами изменения не будут потеряны.
```java
String psdPathAfterChange = dataDir + "HueSaturationAdjustmentLayerChanged.psd";
im.save(psdPathAfterChange);
```
## Шаг 5. Добавьте новый слой «Цветовой тон/Насыщенность»
Затем вы можете добавить новый корректирующий слой «Цветовой тон/Насыщенность» в другой PSD-файл. Просто следуйте тому же подходу, который вы использовали ранее, но с другими файлами PSD.
```java
sourceFileName = dataDir + "PhotoExample.psd";
PsdImage img = (PsdImage) Image.load(sourceFileName);
HueSaturationLayer hueLayerNew = img.addHueSaturationAdjustmentLayer();
```
## Шаг 6. Установите новые значения оттенка/насыщенности для нового слоя
Теперь, когда вы создали этот новый слой, примените желаемые настройки оттенка, насыщенности и яркости, как и раньше.
```java
hueLayerNew.setHue((short) -25);
hueLayerNew.setSaturation((short) -12);
hueLayerNew.setLightness((short) 67);
ColorRangeHsl newColorRange = hueLayerNew.getRange(2);
newColorRange.setHue((short) -160);
newColorRange.setSaturation((short) 100);
newColorRange.setLightness((short) 20);
newColorRange.setMostLeftBorder((short) 300);
```
## Шаг 7. Сохраните обновленный PSD-файл.
Наконец, сохраните PSD-файл с добавленным слоем «Цветовой тон/Насыщенность», чтобы увидеть изменения.
```java
String psdPathAfterNewLayerChange = dataDir + "PhotoExampleAddedHueSaturation.psd";
img.save(psdPathAfterNewLayerChange);
```
Поздравляем! Вы успешно обработали PSD-файлы с помощью Aspose.PSD для Java. Теперь вы можете экспериментировать с различными изображениями и более глубокими изменениями, воплощая в жизнь свои проекты графического дизайна.
## Заключение
Работа с графикой программно открывает целый мир возможностей. Использование Aspose.PSD для Java для добавления и изменения слоев настройки насыщенности оттенка обеспечивает гибкость и эффективность, которые могут оптимизировать рабочий процесс проектирования. Независимо от того, улучшаете ли вы фотографии для проекта или создаете потрясающий визуальный контент, освоение этих инструментов может значительно улучшить ваши результаты.
 Не стесняйтесь изучить дополнительные возможности Aspose.PSD, углубившись в[документация](https://reference.aspose.com/psd/java/) или подумайте о том, чтобы поймать[временная лицензия](https://purchase.aspose.com/temporary-license/) чтобы проверить всю мощь библиотеки.
## Часто задаваемые вопросы
### Что такое корректирующий слой насыщенности оттенка?
Корректирующий слой «Насыщенность оттенка» позволяет изменять цветовые свойства изображения без постоянного изменения исходных пикселей.
### Нужен ли мне установленный Photoshop для использования Aspose.PSD?
Нет, Aspose.PSD — это отдельная библиотека, работающая независимо от Photoshop.
### Могу ли я использовать Aspose.PSD для пакетной обработки?
Да, вы можете автоматизировать и пакетно обрабатывать несколько файлов PSD с помощью Aspose.PSD.
### Является ли Aspose.PSD бесплатным?
Aspose.PSD предлагает бесплатную пробную версию, но для долгосрочного использования требуется лицензия. Вы можете посмотреть цены[здесь](https://purchase.aspose.com/buy).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
