---
title: Добавьте новый обычный слой в PSD с помощью Aspose.PSD для Java
linktitle: Добавьте новый обычный слой в PSD
second_title: Aspose.PSD Java API
description: Узнайте, как добавить новый обычный слой в PSD-файлы с помощью Aspose.PSD для Java. Следуйте нашему пошаговому руководству, чтобы без проблем манипулировать PSD.
type: docs
weight: 11
url: /ru/java/advanced-image-effects/add-new-regular-layer/
---
## Введение

Добро пожаловать в это подробное руководство по использованию Aspose.PSD для Java для добавления нового обычного слоя в PSD-файл. Aspose.PSD — это мощная библиотека Java, которая позволяет разработчикам эффективно манипулировать PSD-файлами и работать с ними. В этом уроке мы покажем вам процесс добавления нового обычного слоя в PSD-файл, предоставив подробные инструкции и примеры кода.

## Предварительные условия

Прежде чем приступить к изучению руководства, убедитесь, что у вас есть следующие предварительные условия:

- Среда разработки Java: убедитесь, что в вашей системе настроена среда разработки Java.
-  Библиотека Aspose.PSD: Загрузите и установите библиотеку Aspose.PSD для Java. Вы можете найти библиотеку[здесь](https://releases.aspose.com/psd/java/).

## Импортировать пакеты

Для начала импортируйте необходимые пакеты в свой Java-проект. Эти пакеты необходимы для работы с функциями Aspose.PSD. Включите следующие строки в начало вашего Java-файла:

```java
import com.aspose.psd.Image;
import com.aspose.psd.Rectangle;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.Layer;
import com.aspose.psd.imageoptions.PngOptions;
import com.aspose.psd.imageoptions.PsdOptions;
```

## Шаг 1: Загрузите PSD-файл

Загрузите PSD-файл, который хотите редактировать, используя следующий код:

```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "OneLayer.psd";
PsdImage im = (PsdImage)Image.load(sourceFileName);
```

## Шаг 2. Подготовьте массивы данных и прямоугольники

Подготовьте два массива int и два объекта Rectangle следующим образом:

```java
int[] data1 = new int[2500];
int[] data2 = new int[2500];
Rectangle rect1 = new Rectangle(0, 0, 50, 50);
Rectangle rect2 = new Rectangle(0, 0, 100, 25);
```

## Шаг 3. Инициализация данных слоя

Инициализируйте массивы данных значением по умолчанию:

```java
for (int i = 0; i < 2500; i++) {
    data1[i] = -10000000;
    data2[i] = -10000000;
}
```

## Шаг 4: Добавьте обычные слои

Добавьте к PSD-изображению два обычных слоя:

```java
Layer layer1 = im.addRegularLayer();
layer1.setLeft(25);
layer1.setTop(25);
layer1.setRight(75);
layer1.setBottom(75);
layer1.saveArgb32Pixels(rect1, data1);

Layer layer2 = im.addRegularLayer();
layer2.setLeft(25);
layer2.setTop(150);
layer2.setRight(1255);
layer2.setBottom(175);
layer2.saveArgb32Pixels(rect2, data2);
```

## Шаг 5: Сохраните PSD и PNG

Сохраните измененный PSD и дополнительный файл PNG:

```java
im.save(exportPath, new PsdOptions());
im.save(exportPathPng, new PngOptions());
```

Поздравляем! Вы успешно добавили новый обычный слой в PSD-файл с помощью Aspose.PSD для Java.

## Заключение

В этом уроке мы рассмотрели процесс добавления нового обычного слоя в PSD-файл с помощью Aspose.PSD для Java. Эта мощная библиотека упрощает манипуляции с PSD, делая ее доступной для разработчиков Java. Поэкспериментируйте с различными параметрами и функциями, чтобы раскрыть весь потенциал Aspose.PSD.

## Часто задаваемые вопросы

### Вопрос 1: Совместим ли Aspose.PSD с Java 8?

О1: Да, Aspose.PSD поддерживает Java 8 и более поздние версии.

### Вопрос 2: Могу ли я применить преобразования к добавленным слоям?

А2: Абсолютно! Aspose.PSD предоставляет ряд вариантов преобразования слоев.

### Вопрос 3: Где я могу найти дополнительную документацию по Aspose.PSD?

 A3: Вы можете обратиться к документации[здесь](https://reference.aspose.com/psd/java/).

### В4: Как я могу получить временную лицензию на Aspose.PSD?

 А4: Посетите[эта ссылка](https://purchase.aspose.com/temporary-license/) для вариантов временной лицензии.

### Вопрос 5: Существуют ли какие-либо форумы сообщества для поддержки Aspose.PSD?

 A5: Да, вы можете найти поддержку и обсуждения.[здесь](https://forum.aspose.com/c/psd/34).