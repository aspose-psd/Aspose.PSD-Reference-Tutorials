---
date: 2026-03-15
description: Узнайте, как применять фильтры к PNG‑изображениям с помощью Aspose.PSD
  для Java. Это пошаговое руководство охватывает оптимизацию PNG в Java и преобразование
  PSD в PNG с типами фильтров.
linktitle: How to Filter PNG Files in Aspose.PSD for Java
second_title: Aspose.PSD Java API
title: Как отфильтровать PNG‑файлы в Aspose.PSD для Java
url: /ru/java/optimizing-png-files/apply-filters-png-files/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Как фильтровать PNG‑файлы в Aspose.PSD для Java

## Introduction
Если вы задаётесь вопросом **как фильтровать PNG** изображения при работе с Java, вы попали в нужное место. В этом руководстве мы пройдёмся по применению типов PNG‑фильтров с Aspose.PSD for Java, библиотекой, которая также помогает **конвертировать PSD в PNG** и выполнять **java png optimization**. К концу вы сможете точно настроить сжатие, улучшить визуальное качество и интегрировать процесс в любой Java‑проект.

## Quick Answers
- **Какая библиотека поддерживает PNG‑фильтрацию в Java?** Aspose.PSD for Java.  
- **Какой фильтр обеспечивает лучшее сжатие для большинства изображений?** Фильтр Paeth (используется в этом примере).  
- **Нужна ли лицензия для запуска кода?** Бесплатная пробная версия подходит для оценки; лицензия требуется для продакшн.  
- **Могу ли я конвертировать PSD в PNG в том же рабочем процессе?** Да — загрузите PSD и сохраните его как PNG с нужным фильтром.  
- **Какая версия Java требуется?** Java 8 или новее.

## What is “how to filter png” in practice?
Фильтрация PNG‑файла означает выбор алгоритма предварительной обработки, который подготавливает данные пикселей перед сжатием. Тип фильтра влияет на размер файла и то, насколько хорошо сохраняются цвета после сохранения PNG. Aspose.PSD даёт прямой контроль над этим шагом через метод `PngOptions.setFilterType`.

## Why use Aspose.PSD for Java PNG optimization?
- **Полная поддержка PSD:** Открывайте, редактируйте и экспортируйте слои PSD без потери точности.  
- **Встроенный выбор фильтра:** Выбирайте из Paeth, Sub, Up, Average или None.  
- **Кроссплатформенность:** Работает на Windows, Linux и macOS с любой стандартной JDK.  
- **Отсутствие внешних нативных зависимостей:** Чистая Java‑реализация упрощает развёртывание.

## Prerequisites
1. **Java Development Kit (JDK) 8+** – убедитесь, что `java -version` выводит 1.8 или выше.  
2. **IDE (IntelliJ IDEA, Eclipse или VS Code)** – любая среда, в которой вам удобно.  
3. **Библиотека Aspose.PSD for Java** – скачайте её по ссылке [here](https://releases.aspose.com/psd/java/).  
4. **Базовые знания Java** – знакомство с классами, методами и вводом‑выводом файлов.

## Import Packages
First, bring the required Aspose.PSD classes into your Java file:

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.png.PngFilterType;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.PngOptions;
```

> **Pro tip:** Добавьте JAR‑файл Aspose.PSD в путь сборки проекта или в зависимости Maven/Gradle, чтобы импорты разрешались без ошибок.

## Step 1: Set Up the Document Directory
Define the folder that holds your source PSD and where the filtered PNG will be saved.

```java
String dataDir = "Your Document Directory"; // Adjust this path
```

Замените `"Your Document Directory"` на абсолютный или относительный путь на вашем компьютере.

## Step 2: Load the PSD Image
Open the PSD file you want to process. Casting to `PsdImage` gives you PSD‑specific capabilities.

```java
PsdImage psdImage = (PsdImage) Image.load(dataDir + "sample.psd");
```

Если файл отсутствует, `Image.load` бросает исключение — убедитесь, что путь правильный.

## Step 3: Create PNG Options (Java PNG Optimization)
Configure the PNG export settings, including the filter type that directly answers **how to filter png**.

```java
PngOptions options = new PngOptions();
options.setFilterType(PngFilterType.Paeth);
```

Вы можете экспериментировать с другими типами фильтров (`Sub`, `Up`, `Average`, `None`), чтобы увидеть, как они влияют на размер и качество. Этот шаг также демонстрирует **java png optimization**, поскольку выбранный фильтр влияет на эффективность сжатия.

## Step 4: Save the PNG Image
Finally, write the processed image back to disk using the options you defined.

```java
psdImage.save(dataDir + "ApplyFilterMethod_out.png", options);
```

Полученный файл `ApplyFilterMethod_out.png` будет отфильтрованным PNG, готовым к использованию в вебе или на рабочем столе.

## Common Issues and Solutions
| Симптом | Вероятная причина | Решение |
|---------|-------------------|---------|
| `FileNotFoundException` | Неправильный путь `dataDir` | Убедитесь, что строка директории заканчивается разделителем (`/` или `\\`). |
| Эффект фильтра не наблюдается | Используется `PngFilterType.None` | Переключитесь на `Paeth` или другой тип фильтра. |
| Ошибка Out‑of‑memory при больших PSD | Загрузка огромного файла без потоковой обработки | Используйте `PsdImage` с `loadOptions` для ограничения использования памяти. |

## Frequently Asked Questions

**В: Что такое Aspose.PSD for Java?**  
О: Aspose.PSD for Java — это надёжный API, позволяющий разработчикам читать, редактировать и конвертировать PSD‑файлы, применять фильтры и выполнять оптимизацию изображений без необходимости Adobe Photoshop.

**В: Как скачать Aspose.PSD for Java?**  
О: Вы можете скачать его со страницы релизов Aspose [here](https://releases.aspose.com/psd/java/).

**В: Можно ли попробовать Aspose.PSD бесплатно?**  
О: Да, бесплатная пробная версия доступна [here](https://releases.aspose.com/).

**В: Какие типы фильтров можно применить к PNG‑изображениям?**  
О: Aspose.PSD поддерживает Paeth, Sub, Up, Average и None. Выберите тот, который лучше всего балансирует размер и визуальную точность.

**В: Где можно получить поддержку по вопросам Aspose.PSD?**  
О: Вы можете получить помощь, посетив форум Aspose [here](https://forum.aspose.com/c/psd/34).

## Conclusion
Теперь вы знаете **как фильтровать PNG** файлы с помощью Aspose.PSD for Java, как **конвертировать PSD в PNG** и как выполнять **java png optimization** с различными типами фильтров. Экспериментируйте с разными фильтрами, интегрируйте этот процесс в ваш конвейер обработки изображений и получайте более мелкие, высококачественные PNG‑ресурсы.

---

**Последнее обновление:** 2026-03-15  
**Тестировано с:** Aspose.PSD for Java 24.10  
**Автор:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}