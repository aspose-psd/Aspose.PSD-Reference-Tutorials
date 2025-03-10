---
title: Пропорционально измените размер изображения с помощью Aspose.PSD для Java
linktitle: Измените размер изображения пропорционально
second_title: Aspose.PSD Java API
description: Улучшите свои Java-приложения с помощью Aspose.PSD. Следуйте нашему руководству, чтобы легко и пропорционально изменить размер изображений. Расширьте свои возможности обработки изображений уже сегодня.
weight: 17
url: /ru/java/advanced-image-manipulation/resize-image-proportionally/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Пропорционально измените размер изображения с помощью Aspose.PSD для Java

## Введение

Добро пожаловать в наше пошаговое руководство по пропорциональному изменению размера изображений с помощью Aspose.PSD для Java. Если вы хотите улучшить свои Java-приложения с помощью эффективных возможностей изменения размера изображений, вы попали по адресу. В этом уроке мы покажем вам весь процесс, используя четкие и краткие шаги.

## Предварительные условия

Прежде чем приступить к изучению руководства, убедитесь, что у вас есть следующие предварительные условия:

1. Среда Java: убедитесь, что в вашей системе установлена Java.
2.  Библиотека Aspose.PSD: Загрузите и установите библиотеку Aspose.PSD. Вы можете найти необходимые ресурсы[здесь](https://releases.aspose.com/psd/java/).

## Импортировать пакеты

После того, как вы отсортировали все необходимые условия, импортируйте необходимые пакеты в свой проект Java. Убедитесь, что в вашем проекте правильно указана библиотека Aspose.PSD.

```java
import com.aspose.psd.Image;

import com.aspose.psd.imageoptions.PngOptions;
```

## Шаг 1. Загрузите изображение

Начните с загрузки изображения, размер которого вы хотите изменить, в свое Java-приложение.

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

Image image = Image.load(sourceFile);

if (!image.isCached()) {
    image.cacheData();
}
```

## Шаг 2. Укажите ширину и высоту

Определите новую ширину и высоту для изображения с измененным размером. В этом примере мы изменим размер изображения до половины его исходного размера.

```java
int newWidth = image.getWidth() / 2;
image.resizeWidthProportionally(newWidth);

int newHeight = image.getHeight() / 2;
image.resizeHeightProportionally(newHeight);
```

## Шаг 3. Сохраните изображение с измененным размером

Сохраните изображение с измененным размером в нужное место, указав параметры формата (в данном случае PNG).

```java
String destName = dataDir + "SimpleResizeImageProportionally_out.png";
image.save(destName, new PngOptions());
```

И вот оно! Вы успешно пропорционально изменили размер изображения с помощью Aspose.PSD для Java.

## Заключение

В этом уроке мы рассмотрели основные шаги по пропорциональному изменению размера изображений с использованием библиотеки Aspose.PSD для Java. Теперь вы можете легко интегрировать эту функцию в свои приложения Java для улучшения обработки изображений.

## Часто задаваемые вопросы

### Вопрос 1: Совместим ли Aspose.PSD со всеми форматами изображений?

 A1: Aspose.PSD поддерживает различные форматы изображений, включая PSD, PNG, JPEG и другие. Проверьте[документация](https://reference.aspose.com/psd/java/) для получения полного списка.

### В2: Могу ли я использовать Aspose.PSD для коммерческих проектов?

 А2: Да, вы можете. Посетите[страница покупки](https://purchase.aspose.com/buy) для получения подробной информации о лицензировании.

### Вопрос 3. Доступны ли временные лицензии для целей тестирования?

 О3: Да, вы можете получить временную лицензию.[здесь](https://purchase.aspose.com/temporary-license/) для оценки.

### Вопрос 4: Где я могу найти поддержку Aspose.PSD?

 А4: Посетите[Форум Aspose.PSD](https://forum.aspose.com/c/psd/34) за общественную поддержку и помощь.

### Вопрос 5: Как я могу получить доступ к документации Aspose.PSD?

 A5: обратитесь к подробной документации.[здесь](https://reference.aspose.com/psd/java/).
`
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
