---
date: 2026-01-17
description: Узнайте, как добавить штриховой узор в Java с помощью Aspose.PSD для
  Java. Следуйте этому пошаговому руководству, чтобы быстро улучшить ваши PSD‑изображения.
linktitle: How to Add Stroke Layer Pattern in Java
second_title: Aspose.PSD Java API
title: Как добавить шаблон штриха в Java с использованием Aspose.PSD
url: /ru/java/java-graphics-drawing/add-stroke-layer-pattern/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Как добавить штриховой узор Java с помощью Aspose.PSD

## Введение
Если вам нужно **add stroke pattern java** в файл Photoshop, Aspose.PSD for Java делает это удивительно просто. Независимо от того, создаёте ли вы инструмент графического дизайна, автоматизируете пакетные правки или просто экспериментируете с эффектами слоёв, этот учебник проведёт вас через каждый шаг — от загрузки PSD до проверки нового узора. Давайте погрузимся и посмотрим, как быстро вы можете улучшить свои изображения.

## Быстрые ответы
- **Какая библиотека нужна?** Aspose.PSD for Java  
- **Какая версия Java поддерживается?** JDK 8 or later  
- **Нужна ли лицензия для тестирования?** Бесплатная пробная версия подходит для разработки; лицензия требуется для продакшн  
- **Сколько времени занимает реализация?** Около 10‑15 минут для базового штрихового узора  
- **Можно ли переиспользовать узор на нескольких слоях?** Да, просто назначьте тот же `PattResource` другим слоям  

## Что такое add stroke pattern java?
Добавление штрихового узора в Java означает применение пользовательского заполнения (обычно повторяющегося битмапа) к эффекту обводки слоя. Эта техника позволяет создавать стилизованные контуры — например, пунктирную линию, текстуру кирпича или пользовательскую графическую рамку — не открывая Photoshop и непосредственно внутри файла PSD.

## Почему использовать Aspose.PSD для add stroke pattern java?
- **Полная точность PSD** – Все эффекты слоёв, ресурсы и режимы наложения сохраняются.  
- **Не требуется Photoshop** – Работает на любой ОС с JDK.  
- **Программный контроль** – Автоматизируйте пакетную обработку или интегрируйте в серверные сервисы.  
- **Богатый API** – Доступ к глобальным ресурсам, заполнениям узорами и режимам наложения в едином удобном интерфейсе.

## Требования
- **Java Development Kit (JDK)** – Убедитесь, что установлен JDK 8 или новее.  
- **Aspose.PSD for Java** – Скачайте библиотеку по [ссылке](https://releases.aspose.com/psd/java/) и добавьте JAR в classpath проекта.  
- **IDE** – IntelliJ IDEA, Eclipse или любой другой предпочитаемый редактор.

## Импорт пакетов
Сначала импортируйте классы, необходимые для работы с PSD‑файлами, цветами, прямоугольниками и эффектами обводки.

```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;
import com.aspose.psd.Rectangle;
import com.aspose.psd.examples.Utils.Assert;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.BlendMode;
import com.aspose.psd.fileformats.psd.layers.fillsettings.FillType;
import com.aspose.psd.fileformats.psd.layers.fillsettings.PatternFillSettings;
import com.aspose.psd.fileformats.psd.layers.layereffects.StrokeEffect;
import com.aspose.psd.fileformats.psd.layers.layerresources.PattResource;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
import java.util.UUID;
```

## Шаг 1: Загрузка PSD файла
Загрузите исходный PSD, чтобы иметь возможность работать с его слоями и ресурсами.

```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "Stroke.psd";
PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);
PsdImage im = (PsdImage)Image.load(sourceFileName, loadOptions);
```

## Шаг 2: Подготовка новых данных узора
Создайте простой 4 × 4‑пиксельный узор, который будет использоваться для обводки.

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

## Шаг 3: Доступ к эффекту штриха
Найдите эффект штриха на целевом слое (в этом примере — четвертый слой).

```java
StrokeEffect patternStroke = (StrokeEffect)im.getLayers()[3].getBlendingOptions().getEffects()[0];
Assert.areEqual(BlendMode.Normal, patternStroke.getBlendMode());
Assert.areEqual(255, patternStroke.getOpacity());
Assert.areEqual(true, patternStroke.isVisible());
PatternFillSettings fillSettings = (PatternFillSettings)patternStroke.getFillSettings();
Assert.areEqual(FillType.Pattern, fillSettings.getFillType());
```

## Шаг 4: Изменение эффекта штриха
### Обновление свойств эффекта штриха
Отрегулируйте непрозрачность и режим наложения, чтобы увидеть визуальное влияние нового узора.

```java
patternStroke.setOpacity((byte)127);
patternStroke.setBlendMode(BlendMode.Color);
```

### Обновление ресурса узора
Замените существующий глобальный ресурс узора тем, который вы только что создали.

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

## Шаг 5: Применение нового узора
Привяжите обновлённый ресурс узора к эффекту штриха и сохраните PSD.

```java
((PatternFillSettings)patternStroke.getFillSettings()).setPatternName("$$/Presets/Patterns/HorizontalLine1=Horizontal Line 9\0");
((PatternFillSettings)patternStroke.getFillSettings()).setPatternId(guid.toString() + "\0");
im.save(exportPath);
```

## Шаг 6: Проверка изменений
Перезагрузите файл и убедитесь, что новый узор, непрозрачность и режим наложения применены корректно.

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

## Распространённые проблемы и решения
| Проблема | Причина | Решение |
|----------|---------|----------|
| Узор не отображается | Неправильная ссылка `PatternId` | Убедитесь, что `PatternId`, установленный в `PattResource`, совпадает с тем, что используется в `PatternFillSettings`. |
| Штрих исчезает после сохранения | Прозрачность установлена в 0 или эффект скрыт | Проверьте, что `setOpacity` находится в диапазоне 0‑255 и `isVisible()` возвращает `true`. |
| Неожиданные цвета | Несоответствие режима наложения | Используйте `BlendMode.Color` (или другой режим), соответствующий вашему дизайнерскому замыслу. |

## Часто задаваемые вопросы
### Что такое Aspose.PSD for Java?
Aspose.PSD for Java — это библиотека, позволяющая разработчикам программно создавать, редактировать и конвертировать файлы PSD (Photoshop Document).

### Можно ли использовать Aspose.PSD for Java в коммерческом проекте?
Да, вы можете использовать её в коммерческих проектах. Приобрести лицензию можно [здесь](https://purchase.aspose.com/buy).

### Есть ли бесплатная пробная версия Aspose.PSD for Java?
Да, бесплатную пробную версию можно скачать [здесь](https://releases.aspose.com/).

### Как получить поддержку для Aspose.PSD for Java?
Поддержку можно получить на форумах сообщества Aspose [здесь](https://forum.aspose.com/c/psd/34).

### Каковы системные требования к Aspose.PSD for Java?
Требуется установленный JDK и IDE для разработки. Библиотека поддерживает несколько операционных систем, включая Windows, Linux и macOS.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Последнее обновление:** 2026-01-17  
**Тестировано с:** Aspose.PSD for Java 24.12 (последняя на момент написания)  
**Автор:** Aspose