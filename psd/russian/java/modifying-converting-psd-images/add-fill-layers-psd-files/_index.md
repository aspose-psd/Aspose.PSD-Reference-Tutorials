---
date: 2026-03-04
description: Узнайте, как программно изменять слои PSD, добавляя слои заливки с помощью
  Aspose.PSD для Java. Следуйте этому пошаговому руководству, чтобы быстро улучшить
  свои дизайны.
linktitle: Modify PSD Layers Programmatically – Add Fill Layers (Java)
second_title: Aspose.PSD Java API
title: Модификация слоёв PSD программно – добавление слоёв‑заполнений (Java)
url: /ru/java/modifying-converting-psd-images/add-fill-layers-psd-files/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Программное изменение слоёв PSD – Добавление слоёв заливки (Java)

Если вы хотите **программно изменять слои PSD**, добавление слоёв заливки — один из самых быстрых способов обогатить ваши документы Photoshop, не открывая сам Photoshop. В этом руководстве мы пройдём по точным шагам, необходимым для создания нового PSD, вставки цветовых, градиентных и шаблонных слоёв заливки, а затем сохранения результата — всё с использованием Aspose.PSD for Java.

## Quick Answers
- **What can I achieve?** Добавить цветовые, градиентные и шаблонные слои заливки в файл PSD программно.  
- **Which library is required?** Aspose.PSD for Java (последний релиз).  
- **Do I need a license?** Бесплатная пробная версия подходит для тестирования; для продакшна требуется коммерческая лицензия.  
- **How long does the implementation take?** Около 10‑15 минут для базового примера.  
- **What Java version is supported?** JDK 11 или новее.

## What is “modify PSD layers programmatically”?
Программное изменение слоёв PSD означает использование кода для создания, редактирования или удаления слоёв внутри документа Photoshop, предоставляя полный контроль над процессом дизайна без ручного взаимодействия с пользовательским интерфейсом.

## Why add fill layers with Aspose.PSD?
- **Automation** – Генерировать десятки PSD в пакетной задаче.  
- **Consistency** – Применять один и тот же цвет, градиент или шаблон во множестве файлов.  
- **Speed** – Пропустить трудоёмкие ручные шаги в Photoshop.  
- **Cross‑platform** – Работает на любой ОС, поддерживающей Java.

## Prerequisites
Перед тем как погрузиться в код, убедитесь, что у вас есть следующее:

1. **Java Development Kit (JDK)** – Установите JDK 11 или новее. Вы можете скачать его с [Oracle website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).  
2. **Aspose.PSD for Java** – Скачайте последнюю библиотеку со страницы официального скачивания [here](https://releases.aspose.com/psd/java/).  
3. **IDE** – IntelliJ IDEA, Eclipse или любой другой редактор по вашему выбору.  
4. **Basic Java knowledge** – Знание классов и методов будет полезным, но руководство объясняет всё пошагово.

## Import Packages
Чтобы начать работу с PSD‑файлами, необходимо импортировать соответствующие классы Aspose.PSD:

```java
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.filllayers.FillLayer;
import com.aspose.psd.fileformats.psd.layers.fillsettings.FillType;
```

Эти импорты дают вам доступ к объекту `PsdImage` (сам документ) и различным типам `FillLayer`, которые мы будем использовать.

## How to Modify PSD Layers Programmatically – Step‑by‑Step Guide

### Step 1: Set Up Your Output Directory
Определите, где будет сохранён результирующий PSD, чтобы позже легко его найти.

```java
String outputDir = "Your Document Directory";
String outPsdFilePath = outputDir + "output.psd";
```

Замените `"Your Document Directory"` на абсолютный или относительный путь на вашем компьютере.

### Step 2: Create a New Photoshop Document
Создайте пустой холст, который будет содержать слои заливки.

```java
PsdImage psdImage = new PsdImage(100, 100);
```

Параметры `100, 100` означают ширину и высоту в пикселях. При необходимости измените их под требования вашего дизайна.

### Step 3: Add a Color Fill Layer
Создайте слой сплошной заливки и задайте ему понятное имя.

```java
FillLayer colorFillLayer = FillLayer.createInstance(FillType.Color);
colorFillLayer.setDisplayName("Color Fill Layer");
psdImage.addLayer(colorFillLayer);
```

Позже вы сможете изменить фактический цвет, получив доступ к настройкам заливки слоя (не показано здесь для краткости).

### Step 4: Add a Gradient Fill Layer
Градиентные заливки добавляют глубину и визуальный интерес.

```java
FillLayer gradientFillLayer = FillLayer.createInstance(FillType.Gradient);
gradientFillLayer.setDisplayName("Gradient Fill Layer");
psdImage.addLayer(gradientFillLayer);
```

Не стесняйтесь экспериментировать с линейными или радиальными градиентами через настройки слоя.

### Step 5: Add a Pattern Fill Layer
Шаблонные заливки позволяют мозаично размещать изображения или текстуры по слою.

```java
FillLayer patternFillLayer = FillLayer.createInstance(FillType.Pattern);
patternFillLayer.setDisplayName("Pattern Fill Layer");
patternFillLayer.setOpacity((byte)50);
psdImage.addLayer(patternFillLayer);
```

Установка непрозрачности в 50 % делает шаблон хорошо сочетающимся с нижележащими слоями.

### Step 6: Save Your PSD File
Сохраните изменения на диск.

```java
psdImage.save(outPsdFilePath);
```

Откройте сохранённый файл в Photoshop или любом просмотрщике PSD, чтобы увидеть три новых слоя заливки.

### Step 7: Clean Up Resources
Всегда освобождайте объект `PsdImage`, чтобы освободить нативную память.

```java
psdImage.dispose();
```

## Common Issues & Tips
- **Invalid output path** – Убедитесь, что каталог существует и у вас есть права на запись.  
- **Memory usage** – Для очень больших холстов вызывайте `psdImage.dispose()` сразу после завершения работы с изображением.  
- **Layer order** – По умолчанию слои добавляются в верхнюю часть стека; используйте `psdImage.insertLayer(layer, index)`, если нужен определённый порядок.

## Frequently Asked Questions

**Q: What types of fill layers can I add using Aspose.PSD for Java?**  
A: Вы можете добавить цветовые, градиентные и шаблонные слои заливки.

**Q: Does Aspose.PSD support other image formats?**  
A: Да, он работает с BMP, JPEG, PNG и многими другими форматами.

**Q: Can I use Aspose.PSD for free?**  
A: Вы можете попробовать бесплатную пробную версию Aspose.PSD for Java [here](https://releases.aspose.com/).

**Q: Where can I find more documentation on Aspose.PSD?**  
A: Полную документацию можно найти [here](https://reference.aspose.com/psd/java/).

**Q: Is there a support community for Aspose.PSD?**  
A: Да, вы можете получить помощь от сообщества на форуме Aspose [here](https://forum.aspose.com/c/psd/34).

## Conclusion
Теперь вы знаете, как **программно изменять слои PSD**, добавляя различные слои заливки с помощью Aspose.PSD for Java. Этот подход экономит время, обеспечивает согласованность проектов и открывает возможности для мощных сценариев пакетной обработки. Экспериментируйте с разными цветами, градиентами и шаблонами, чтобы увидеть, насколько далеко можно продвинуть автоматическое создание дизайна.

---

**Last Updated:** 2026-03-04  
**Tested With:** Aspose.PSD for Java (latest release)  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}