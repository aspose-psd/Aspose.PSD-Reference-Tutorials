---
date: 2026-06-13
description: Узнайте, как заменить шрифты в PSD‑файлах с помощью Aspose.PSD for Java,
  конвертировать PSD в PNG и эффективно работать с отсутствующими шрифтами.
keywords:
- how to replace fonts
- convert psd to png
- handle missing fonts psd
linktitle: Настройки замены отсутствующих шрифтов
schemas:
- author: Aspose
  dateModified: '2026-06-13'
  description: Learn how to replace fonts in PSD files using Aspose.PSD for Java,
    convert PSD to PNG, and handle missing fonts efficiently.
  headline: How to Replace Fonts in PSD Files with Aspose.PSD for Java
  type: TechArticle
- questions:
  - answer: '`PsdImage` is the core class that represents a PSD document in memory.'
    question: What is the primary class for loading PSD files?
  - answer: Use `PsdLoadOptions.setDefaultFontName("Arial")`.
    question: Which option sets a default replacement font?
  - answer: Yes—call `psdImage.save("output.png", new PngOptions())`.
    question: Can I save the result as PNG?
  - answer: A temporary license works for testing; a full license is required for
      production.
    question: Do I need a license for development?
  - answer: Aspose.PSD for Java supports Java 8 and later.
    question: What Java version is supported?
  type: FAQPage
second_title: Aspose.PSD Java API
title: Как заменить шрифты в PSD‑файлах с помощью Aspose.PSD for Java
url: /ru/java/advanced-techniques/settings-replacing-missing-fonts/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Как заменить шрифты в PSD‑файлах с помощью Aspose.PSD для Java

В современном Java‑разработке **как заменить шрифты** в файле Photoshop (PSD) — распространённая задача, которая может нарушить визуальное расположение ваших дизайнов. Aspose.PSD для Java предоставляет мощный API, автоматизирующий замену шрифтов, позволяя сохранять изображения точно такими, как задумано. Это руководство проведёт вас через каждый шаг — от настройки окружения до сохранения окончательного PNG‑файла — чтобы вы могли уверенно работать с отсутствующими шрифтами в PSD‑файлах.

## Быстрые ответы
- **Какой основной класс для загрузки PSD‑файлов?** `PsdImage` — основной класс, представляющий PSD‑документ в памяти.  
- **Какая опция задаёт шрифт замены по умолчанию?** Используйте `PsdLoadOptions.setDefaultFontName("Arial")`.  
- **Можно ли сохранить результат в PNG?** Да — вызовите `psdImage.save("output.png", new PngOptions())`.  
- **Нужна ли лицензия для разработки?** Временная лицензия подходит для тестирования; полная лицензия требуется для продакшна.  
- **Какая версия Java поддерживается?** Aspose.PSD для Java поддерживает Java 8 и новее.

## Как заменить шрифты в PSD‑файле с помощью Aspose.PSD для Java?

Загрузите исходный PSD с помощью `PsdLoadOptions`, указав резервный шрифт, затем сохраните изображение в нужном формате. API автоматически заменяет любые отсутствующие глифы шрифтом по умолчанию, устраняя ошибки рендеринга без ручного редактирования. Такой одношаговый подход работает с файлами любого размера и сохраняет слои, маски и эффекты.

## Что такое `PsdLoadOptions`?

`PsdLoadOptions` — объект конфигурации, управляющий тем, как Aspose.PSD разбирает PSD‑файл. Он позволяет задать шрифт замены по умолчанию, контролировать загрузку слоёв и задавать параметры обработки отсутствующих ресурсов. Настраивая его свойства, разработчики могут обеспечить согласованное отображение текста и других элементов в разных окружениях и избежать ошибок выполнения из‑за недоступных шрифтов.

## Почему заменять отсутствующие шрифты в PSD‑файлах?

Aspose.PSD поддерживает **более 50 форматов ввода и вывода** и может обрабатывать многосотстраничные PSD‑файлы без полной загрузки документа в память. Замена отсутствующих шрифтов предотвращает поломку текстовых слоёв, сокращает время ручной коррекции до **80 %**, и гарантирует, что экспортированные PNG сохраняют исходную точность дизайна.

## Предварительные требования

1. **Библиотека Aspose.PSD** – скачайте и установите библиотеку Aspose.PSD для Java со [страницы релизов](https://releases.aspose.com/psd/java/).  
2. **Среда разработки Java** – JDK 8+ и предпочитаемая IDE (Eclipse, IntelliJ IDEA и т.д.).  

Теперь, когда всё готово, приступим к реализации.

## Импорт пакетов

Импортируйте необходимые пространства имён, чтобы компилятор нашёл классы Aspose.PSD.

```java
import com.aspose.psd.Image;

import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
import com.aspose.psd.imageoptions.PngOptions;
```

## Шаг 1: Настройте каталог документа

Определите папку, содержащую исходный PSD и куда будет записан результат. Этот путь используется загрузчиком и сохранителем.

```java
String dataDir = "Your Document Directory";
```

## Шаг 2: Укажите исходный и целевой файлы

Задайте абсолютные или относительные пути к оригинальному PSD и целевому PNG. Чёткое именование помогает избежать перезаписи файлов.

```java
String sourceFile = dataDir + "sample.psd";
String destName = dataDir + "result.png";
```

## Шаг 3: Настройте параметры замены шрифтов

Создайте экземпляр `PsdLoadOptions` и задайте шрифт замены по умолчанию — **Arial** (или любой шрифт, установленный в системе). Это указывает движку, какой шрифт использовать, когда оригинальный недоступен.

```java
PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setDefaultReplacementFont("Arial");
```

## Шаг 4: Загрузите PSD‑изображение и замените шрифты

Загрузите PSD, используя сконфигурированные параметры. Aspose.PSD автоматически заменит отсутствующие шрифты во время загрузки, дополнительный код не требуется.

```java
Image image = Image.load(sourceFile, loadOptions);
PsdImage psdImage = (PsdImage) image;
```

## Шаг 5: Сохраните изменённое изображение

Выберите `PngOptions` для экспорта изображения в полноцветный PNG с альфа‑каналом. Полученный файл отобразит заменённые шрифты корректно.

```java
PngOptions options = new PngOptions();
options.setColorType(PngColorType.TruecolorWithAlpha);
psdImage.save(destName, options);
```

## Распространённые проблемы и решения

| Проблема | Причина | Решение |
|----------|---------|---------|
| Текст отображается искажённо | Шрифт замены не содержит нужных глифов | Выберите шрифт с более широким диапазоном Unicode (например, **Arial Unicode MS**). |
| Ошибка «файл не найден» | Неправильный путь в шаге 1 или 2 | Проверьте строки каталогов и используйте `File.separator` для кросс‑платформенной совместимости. |
| Исключение лицензии | Запуск без действующей лицензии | Примените временную лицензию для тестирования или приобретите полную лицензию для продакшна. |

## Часто задаваемые вопросы

### В1: Совместим ли Aspose.PSD со всеми версиями PSD‑файлов?

О1: Aspose.PSD поддерживает версии PSD от **4.0** до последнего выпуска Photoshop, обеспечивая широкую совместимость как со старыми, так и с современными дизайнами.

### В2: Можно ли использовать пользовательские шрифты для замены в Aspose.PSD?

О2: Да, можно указать любой установленный TrueType или OpenType шрифт, передав его имя в `setDefaultFontName`. Это даёт полный контроль над визуальным результатом.

### В3: Какие варианты лицензирования доступны для Aspose.PSD?

О3: Ознакомьтесь с вариантами лицензирования [здесь](https://purchase.aspose.com/buy), чтобы выбрать лучший план для вашей организации, включая лицензии для разработчиков, сайта и OEM.

### В4: Есть ли форум сообщества для поддержки Aspose.PSD?

О4: Да, посетите [форум Aspose.PSD](https://forum.aspose.com/c/psd/34) для получения помощи от сообщества, примеров кода и советов по устранению неполадок от других разработчиков.

### В5: Как получить временную лицензию для Aspose.PSD?

О5: Получите временную лицензию [здесь](https://purchase.aspose.com/temporary-license/) для оценки, тестирования или проектов proof‑of‑concept без каких‑либо затрат.

---

**Последнее обновление:** 2026-06-13  
**Тестировано с:** Aspose.PSD 24.12 for Java  
**Автор:** Aspose  

{{< blocks/products/products-backtop-button >}}

## Похожие руководства

- [Конвертация PSD в PNG с наложением цвета – Aspose.PSD для Java](/psd/java/advanced-image-manipulation/rendering-color-effect/)
- [Как конвертировать PSD в PNG и изменять размер пропорционально с Aspose.PSD для Java](/psd/java/advanced-image-manipulation/resize-image-proportionally/)
- [Конвертация PSD в растровые форматы изображений с Aspose.PSD для Java](/psd/java/advanced-techniques/convert-psd-to-raster-formats/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}