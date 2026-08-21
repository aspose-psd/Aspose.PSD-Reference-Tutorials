---
date: 2026-06-23
description: Узнайте, как сохранять PSD в PNG, заменять отсутствующие шрифты и экспортировать
  изображения с помощью Aspose.PSD for Java — быстро обрабатывайте PSD‑файлы с недостающими
  шрифтами.
keywords:
- save psd as png
- how to replace fonts
- convert psd to bmp
- export psd to jpeg
- handle missing fonts psd
linktitle: Заменить шрифты
schemas:
- author: Aspose
  dateModified: '2026-06-23'
  description: Learn how to save PSD as PNG, replace missing fonts, and export images
    using Aspose.PSD for Java – handle missing fonts PSD files quickly.
  headline: How to Save PSD as PNG and Replace Missing Fonts in Java with Aspose
  type: TechArticle
- questions:
  - answer: Yes. While the primary use‑case is PSD, Aspose.PSD also supports PNG,
      JPEG, BMP, and TIFF, allowing font replacement wherever text layers exist.
    question: Can I replace fonts in other image formats besides PSD?
  - answer: No. You can set any TrueType font you prefer, or omit the setting to let
      Aspose use its internal default.
    question: Is the default replacement font mandatory?
  - answer: A commercial license is required for production deployments. See the [purchase
      page](https://purchase.aspose.com/buy) for details.
    question: Are there licensing requirements for using Aspose.PSD?
  - answer: Absolutely. Aspose offers free temporary licenses for evaluation – visit
      the [temporary license page](https://purchase.aspose.com/temporary-license/).
    question: Can I obtain a temporary license for testing?
  - answer: 'The community forum is a great place to ask questions: [Aspose.PSD forum](https://forum.aspose.com/c/psd/34).'
    question: Where can I find additional support or discuss Aspose.PSD‑related issues?
  type: FAQPage
second_title: Aspose.PSD Java API
title: Как сохранить PSD в PNG и заменить отсутствующие шрифты в Java с Aspose.PSD
  for Java
url: /ru/java/advanced-image-manipulation/replace-fonts/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# сохранить psd как png – Замена отсутствующих шрифтов в Java

## Введение

Если вам нужно **save PSD as PNG** и при этом заменить отсутствующие или нежелательные шрифты внутри файла Photoshop (PSD), функция замены шрифтов Aspose PSD делает это без усилий. В Java‑приложениях вы можете загрузить PSD, указать Aspose, какой шрифт‑запас использовать, а затем экспортировать исправленное изображение в любой нужный вам формат. Это руководство проведёт вас через весь процесс — от настройки проекта до экспорта обновлённого PNG — чтобы вы надёжно могли **handle missing fonts PSD** без необходимости открывать Photoshop.

## Быстрые ответы
- **What library handles font substitution?** Aspose.PSD for Java  
- **How long does the implementation take?** About 5‑10 minutes for a basic scenario  
- **Which font is used as the default fallback?** You can set any TrueType font, e.g., “Arial”  
- **Can I save to formats other than PNG?** Yes – PSD, JPEG, BMP, and more are supported  
- **Do I need a license for production?** A valid Aspose.PSD license is required for non‑trial use  

## Что такое Aspose PSD Font Substitution?

Aspose PSD font substitution — это процесс указания заменяющего шрифта, который библиотека будет использовать каждый раз, когда встретит отсутствующий или неподдерживаемый шрифт в файле PSD. Это гарантирует корректный рендеринг текстовых слоёв без ручного редактирования в Photoshop и позволяет автоматически **handle missing fonts PSD** файлы.

## Почему использовать Aspose.PSD for Java?

Aspose.PSD for Java предоставляет всестороннее, высокопроизводительное решение для работы с файлами Photoshop напрямую из Java‑кода, устраняя необходимость в самом Photoshop. Библиотека поддерживает широкий набор типов слоёв, эффектов и большие файлы, предлагая простые API для таких задач, как замена шрифтов, конвертация изображений и работа с метаданными.

- **Full‑featured PSD handling** – Aspose.PSD поддерживает **30+ типов слоёв**, **20+ эффектов** и может обрабатывать файлы размером до **2 GB**, не загружая весь документ в память.  
- **Cross‑platform** – работает на любой ОС, поддерживающей Java 8+.  
- **No external dependencies** – библиотека осуществляет замену шрифтов внутри себя, поэтому вам не нужно поставлять дополнительные шрифты вместе с приложением.  

## Как заменить отсутствующие шрифты в PSD с помощью Aspose PSD

Чтобы заменить отсутствующие шрифты, сначала загрузите PSD с указанием шрифта‑запаса в параметрах загрузки, затем отрендерите или сохраните изображение. Библиотека автоматически подставит указанный шрифт вместо недостающих, обеспечивая визуальный результат без ручного редактирования.

## Предварительные требования

Перед тем как начать, убедитесь, что у вас есть:

- **Java Development Kit (JDK)** — версия 8 или выше.  
- **Aspose.PSD for Java** — скачайте последнюю JAR‑файл со [страницы релизов](https://releases.aspose.com/psd/java/).  
- **IDE** — IntelliJ IDEA, Eclipse или любой другой редактор по вашему выбору.  

## Импорт пакетов

Класс `PsdImage` представляет документ Photoshop в памяти, предоставляя доступ к слоям, тексту и возможностям рендеринга. `PsdLoadOptions` управляет тем, как файл читается, включая шрифт‑запас, а `SaveOptions` (или специализированные подклассы) определяют, как изображение будет записано.

```java
import com.aspose.psd.Image;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
import com.aspose.psd.imageoptions.PngOptions;
```

## Шаг 1: Укажите каталог документа

Укажите папку, содержащую исходный файл PSD. Замените заполнитель реальным путём на вашем компьютере.

Объект `File` просто указывает на PSD, который вы хотите обработать; дополнительной конфигурации здесь не требуется.  

```java
String dataDir = "Your Document Directory";
```

## Шаг 2: Загрузите изображение с заменяющим шрифтом

Создайте экземпляр `PsdLoadOptions`, задайте шрифт‑запас по умолчанию (например, **Arial**) и загрузите PSD. Aspose автоматически применит запасной шрифт каждый раз, когда встретит отсутствующий.

`PsdLoadOptions` позволяет задать поведение загрузки, включая шрифт‑запас, который заменит любой недостающий шрифт во время импорта.  

```java
PsdLoadOptions psdLoadOptions = new PsdLoadOptions(); 
psdLoadOptions.setDefaultReplacementFont("Arial");

PsdImage psdImage = (PsdImage)Image.load(dataDir + "Cloud_AzPlat_Banner3A_SB_EN_US_160x600_chinese_font.psd", psdLoadOptions);
```

## Шаг 3: Сохраните заменённое изображение как PNG

После замены шрифтов вы можете экспортировать изображение в любой поддерживаемый формат. Здесь мы сохраняем его как PNG, но можно выбрать JPEG, BMP или даже вернуть обратно в PSD.

Метод `save` класса `PsdImage` принимает объект `SaveOptions`; использование `PngOptions` гарантирует безпотерянный PNG, подходящий для веба или дальнейшей обработки.  

```java
PngOptions pngOptions = new PngOptions();
psdImage.save(dataDir + "replaced_font.png", pngOptions);
```

## Как сохранить PSD как PNG после замены шрифтов?

Загрузите PSD с шрифтом‑запасом, затем вызовите `psdImage.save("output.png", new PngOptions())`. Эта однострочная операция сохраняет полностью отрендеренный PNG, отражающий заменённый шрифт, позволяя внедрять изображение где угодно без беспокойства о недостающих шрифтах. Убедитесь, что шрифт‑замена применена до сохранения, и при необходимости настройте параметры сжатия PNG через объект `PngOptions` для оптимального размера файла.

## Распространённые проблемы и решения

| Проблема | Причина | Решение |
|----------|---------|---------|
| Текст выглядит искажённым после замены | Шрифт‑запас не содержит нужных глифов | Выберите шрифт, поддерживающий требуемый диапазон Unicode (например, “Arial Unicode MS”). |
| `OutOfMemoryError` при работе с большими PSD | Загрузка файла с высоким разрешением без достаточного объёма heap | Увеличьте размер heap JVM (`-Xmx2g`) или используйте потоковый режим загрузки, если он доступен. |
| Исключение лицензии | Использование trial‑версии в продакшн | Примените действующую постоянную или временную лицензию перед загрузкой изображения. |

## Часто задаваемые вопросы

**Q: Можно ли заменять шрифты в других форматах изображений, кроме PSD?**  
A: Да. Хотя основной сценарий — PSD, Aspose.PSD также поддерживает PNG, JPEG, BMP и TIFF, позволяя заменять шрифты там, где присутствуют текстовые слои.

**Q: Обязательно ли указывать шрифт‑запас по умолчанию?**  
A: Нет. Вы можете задать любой TrueType‑шрифт или вовсе не указывать, тогда Aspose использует свой внутренний шрифт‑запас.

**Q: Требуются ли лицензии для использования Aspose.PSD?**  
A: Коммерческая лицензия необходима для продакшн‑развёртываний. Подробнее см. на [странице покупки](https://purchase.aspose.com/buy).

**Q: Можно ли получить временную лицензию для тестирования?**  
A: Конечно. Aspose предлагает бесплатные временные лицензии для оценки — посетите [страницу временной лицензии](https://purchase.aspose.com/temporary-license/).

**Q: Где можно получить дополнительную поддержку или обсудить вопросы, связанные с Aspose.PSD?**  
A: Форум сообщества — отличное место для вопросов: [Aspose.PSD forum](https://forum.aspose.com/c/psd/34).

**Q: Как обрабатывать PSD‑файлы, содержащие несколько отсутствующих шрифтов?**  
A: Установите шрифт‑запас один раз (как показано) — он будет применён ко *всем* отсутствующим шрифтам во время загрузки.

**Q: Можно ли заменить шрифты после сохранения изображения?**  
A: Замена шрифтов должна происходить на этапе загрузки. Чтобы изменить шрифты позже, перезагрузите PSD с другим шрифтом‑запасом и сохраните заново.

## Заключение

Теперь вы видели полный рабочий процесс **save psd as png** в Java — от импорта нужных классов, настройки шрифта‑запаса, загрузки PSD до экспорта исправленного PNG. Внедрите этот шаблон в свои конвейеры обработки изображений, чтобы обеспечить согласованную типографику во всех PSD‑активах и автоматически **handle missing fonts PSD**.

---

**Last Updated:** 2026-06-23  
**Tested With:** Aspose.PSD for Java 24.12 (latest at time of writing)  
**Author:** Aspose

## Связанные руководства

- [Настройки замены отсутствующих шрифтов в Aspose.PSD для Java](/psd/java/advanced-techniques/settings-replacing-missing-fonts/)
- [Сохранить PSD как PNG и применить отбрасывание тени при рендеринге в Aspose.PSD для Java](/psd/java/advanced-image-manipulation/rendering-drop-shadow/)
- [Как конвертировать PSD в PNG и изменить размер пропорционально с помощью Aspose.PSD для Java](/psd/java/advanced-image-manipulation/resize-image-proportionally/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< blocks/products/products-backtop-button >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}