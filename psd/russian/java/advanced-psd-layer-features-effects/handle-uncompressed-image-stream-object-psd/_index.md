---
date: 2026-08-01
description: Узнайте, как экспортировать PSD в PNG и работать с несжатыми потоками
  изображений с помощью Aspose.PSD for Java.
keywords:
- export psd to png
- save psd as png
- java image manipulation
lastmod: 2026-08-01
linktitle: Работа с объектом Uncompressed Image Stream в PSD – Java
og_description: Экспортируйте psd в png с помощью Aspose.PSD for Java. Узнайте, как
  работать с несжатыми потоками изображений, создавать графические объекты и сохранять
  PNG высокого качества.
og_image_alt: 'Developer guide: Export PSD to PNG with uncompressed stream using Aspose.PSD
  Java'
og_title: Экспорт psd в png – Руководство Java по несжатым потокам PSD
schemas:
- author: Aspose
  dateModified: '2026-08-01'
  description: Learn how to export PSD to PNG and handle uncompressed image streams
    with Aspose.PSD for Java.
  headline: Export PSD to PNG – Create PSD Graphics Object – Uncompressed Stream in
    Java
  type: TechArticle
- questions:
  - answer: Yes. After loading the PSD, retrieve the desired layer via `psdImage.getLayers().get_Item(index)`
      and pass that layer to the `Graphics` constructor.
    question: Can I use the graphics object to edit only one specific layer?
  - answer: Raw stores pixel data without any compression, so the resulting file is
      larger than a compressed PSD, but it guarantees 100 % pixel fidelity.
    question: Does the Raw compression method affect file size?
  - answer: Absolutely. After editing, call `psdImage.save("output.png", new PngOptions())`—this
      is the standard way to **export PSD to PNG** with lossless quality.
    question: Is it possible to export the edited PSD to another format (e.g., PNG)?
  - answer: Aspose.PSD for Java supports JDK 8 and later, including all LTS releases
      up to JDK 21.
    question: What Java version is required?
  - answer: Invoke `psdImage.dispose()` and close any streams (e.g., `ms.close()`)
      to free native memory and avoid leaks.
    question: How do I release resources after processing?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- export psd
- Aspose.PSD
- Java image processing
- uncompressed stream
- PSD graphics
title: Экспорт PSD в PNG – Создание графического объекта PSD – Uncompressed Stream
  в Java
url: /ru/java/advanced-psd-layer-features-effects/handle-uncompressed-image-stream-object-psd/
weight: 26
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Экспорт PSD в PNG – Создание объекта графики PSD – Несжатый поток в Java

## Введение
В этом пошаговом руководстве вы **экспортируете PSD в PNG**, работая с несжатым потоком изображения с помощью Aspose.PSD for Java. Независимо от того, автоматизируете ли вы конвейер дизайна или создаёте собственный редактор, возможность отрисовать файл Photoshop без потери качества имеет решающее значение. Мы начнём с необходимой настройки, пройдём процесс создания объекта `Graphics` и завершим экспортом PNG без потерь. К концу вы поймёте, почему Aspose.PSD эффективно обрабатывает необработанные потоки и как интегрировать его в любой Java‑проект.

## Быстрые ответы
- **Что означает “create PSD graphics object”?** Это означает создание контекста `Graphics`, который позволяет программно рисовать или изменять изображение PSD.  
- **Какая библиотека обрабатывает несжатые потоки?** Aspose.PSD for Java полностью поддерживает необработанные (несжатые) данные изображения.  
- **Могу ли я экспортировать PSD в PNG после редактирования?** Да — как только у вас есть объект `Graphics`, вы можете отрисовать PSD и сохранить его как PNG одним вызовом.  
- **Нужна ли лицензия для разработки?** Бесплатная пробная версия подходит для тестирования; коммерческая лицензия требуется для продакшн‑развертываний.  
- **Является ли экспорт без потерь?** Экспорт в PNG сохраняет оригинальные пиксельные данные, обеспечивая безпотерьное качество при меньшем размере файла, чем у исходного PSD.

## Что такое экспорт PSD в PNG?
Экспорт PSD в PNG преобразует многослойный документ Photoshop в однослойное растровое изображение без потерь, которое может отображаться в любом веб‑браузере или просмотрщике изображений. Процесс сохраняет прозрачность, глубину цвета и эффекты слоёв, одновременно удаляя специфичные для Photoshop метаданные. Он также сохраняет оригинальный цветовой профиль для точного воспроизведения цветов.

## Зачем использовать Aspose.PSD for Java для обработки изображений?
Aspose.PSD поддерживает **более 50** форматов ввода и вывода — включая PSD, PNG, JPEG, BMP и TIFF — и может обрабатывать файлы с **более 200 слоями** без загрузки всего документа в память. Параметр сжатия `Raw` сохраняет пиксельные данные без сжатия, гарантируя пиксельную точность для последующего редактирования или архивирования.

## Требования
Прежде чем погрузиться в код, убедитесь, что у вас есть следующее:

- **Java Development Kit (JDK)** — установлен JDK 8 или новее.  
- **Aspose.PSD for Java** — Скачайте последнюю JAR‑файл с официальной страницы релизов: [Aspose.PSD Java download](https://releases.aspose.com/psd/java/). Вы также можете получить её через [this link](https://releases.aspose.com/psd/java/) или [release page](https://releases.aspose.com/psd/java/). Для других продуктов Aspose нажмите [here](https://releases.aspose.com/).  
- **IDE** — IntelliJ IDEA, Eclipse или любой совместимый с Java редактор.  
- **Базовые знания Java** — знакомство с классами, методами и обработкой исключений.

С этими элементами вы готовы начать кодировать.

## Импорт пакетов
Класс `Graphics` — это поверхность рисования Aspose.PSD, позволяющая напрямую отрисовывать или редактировать пиксельные данные. Класс `PsdImage` представляет файл PSD в памяти, а `PsdOptions` управляет тем, как сохраняется изображение.

```java
import com.aspose.psd.Graphics;
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.CompressionMethod;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.PsdOptions;
import java.io.ByteArrayInputStream;
import java.io.ByteArrayOutputStream;
```

Теперь разберём код на понятные шаги, чтобы вам было легко следовать. Мы настроим окружение, загрузим файл PSD, изменим его и, наконец, сохраним результат.

## Шаг 1: Определите каталог документов
Перед любыми файловыми операциями необходимо указать программе, где искать ваши PSD‑ресурсы. Этот путь к каталогу используется на протяжении всего руководства.

```java
String dataDir = "Your Document Directory";
```

Замените `"Your Document Directory"` на абсолютный путь, содержащий `layers.psd`. Делая путь настраиваемым, вы делаете код переиспользуемым в разных проектах.

## Шаг 2: Создайте ByteArrayOutputStream
`ByteArrayOutputStream` — это поток Java, который хранит данные в памяти в виде массива байтов. Он служит буфером в памяти для изменённого изображения, позволяя захватить необработанные байты перед записью их на диск или отправкой по сети.

```java
ByteArrayOutputStream ms = new ByteArrayOutputStream();
```

Переменная `ms` будет содержать несжатые данные изображения после операции `save`.

## Шаг 3: Загрузите файл PSD
Класс `PsdImage` загружает файл PSD в память для манипуляций. Загрузка файла преобразует PSD, находящийся на диске, в объект `PsdImage`, которым можно управлять. На этом этапе Aspose.PSD читает заголовок файла, слои и ресурсы.

```java
PsdImage psdImage = (PsdImage) Image.load(dataDir + "layers.psd");
```

Если путь неверен, Aspose.PSD бросает `FileNotFoundException`, который следует отлавливать в продакшн‑коде.

## Шаг 4: Настройте PsdOptions для сохранения
`PsdOptions` задаёт параметры сохранения для файлов PSD. Установка метода сжатия в `Raw` указывает, что пиксельные данные должны храниться без сжатия, сохраняя каждый пиксель точно таким, каким он находится в памяти.

```java
PsdOptions saveOptions = new PsdOptions();
saveOptions.setCompressionMethod(CompressionMethod.Raw);
```

Опция `CompressionMethod.Raw` сохраняет пиксельные данные без какого‑либо сжатия, что идеально, если вы планируете выполнять дальнейшее редактирование.

## Шаг 5: Сохраните изображение в поток вывода
Теперь вы сохраняете PSD (с любыми изменениями) в ранее созданный `ByteArrayOutputStream`. Метод `save` учитывает настроенные `PsdOptions`.

```java
psdImage.save(ms, saveOptions);
```

На данном этапе `ms` содержит полное бинарное представление несжатого PSD.

## Шаг 6: Сбросьте поток вывода
После записи внутренний указатель потока находится в конце. Сброс его перемещает поток в начало, чтобы вы могли читать с начала.

```java
ms.reset();
```

Представьте это как перемещение головки ленты обратно в начало перед воспроизведением.

## Шаг 7: Загрузите только что созданное изображение
Теперь вы можете создать новый экземпляр `PsdImage` непосредственно из массива байтов. Этот шаг проверяет, что сохранённые данные могут быть загружены повторно без повреждений.

```java
PsdImage img = (PsdImage) Image.load(new ByteArrayInputStream(ms.toByteArray()));
```

Если изображение загружается успешно, значит, несжатый поток был записан корректно.

## Шаг 8: Создайте объект Graphics
Класс `Graphics` — это холст для рисования Aspose.PSD. Он предоставляет методы для рисования фигур, текста и применения фильтров непосредственно на пиксельную матрицу `PsdImage`.

```java
Graphics graphics = new Graphics(psdImage);
```

С этим экземпляром `Graphics` вы можете рисовать новое содержимое, стирать части или комбинировать дополнительные слои.

## Как экспортировать PSD в PNG с помощью Aspose.PSD for Java?
Загрузите PSD с помощью `new PsdImage(dataDir + "layers.psd")`, создайте объект `Graphics`, выполните необходимые рисования, затем вызовите `psdImage.save("output.png", new PngOptions())`. Эта последовательность отрисовывает отредактированный PSD и записывает безпотерьный PNG за один шаг, используя встроенный в Aspose.PSD механизм конвертации.

## Манипулирование слоями PSD с объектом Graphics
Наличие экземпляра `Graphics` даёт вам контроль над каждым слоем на уровне пикселей. Вы можете рисовать геометрические фигуры, отрисовывать текст или применять пользовательские фильтры. Поскольку графический контекст работает с растровым представлением слоя, изменения сразу видны при сохранении изображения.

## Распространённые проблемы и решения
- **NullPointerException при загрузке файла** — проверьте путь `dataDir` и убедитесь, что имя файла точно совпадает, включая регистр.  
- **Сжатый вывод несмотря на использование Raw** — убедитесь, что `saveOptions.setCompressionMethod(CompressionMethod.Raw);` вызывается **до** вызова `save`.  
- **Объект Graphics выглядит пустым** — убедитесь, что рисуете на правильном экземпляре `PsdImage` (на том, который загрузили, а не на вновь созданном пустом изображении).  
- **OutOfMemoryError при работе с большими файлами** — используйте `PsdImage.load(dataDir, LoadOptions)` с `loadOptions.setLoadMode(LoadMode.Memory)`, чтобы потоково обрабатывать большие файлы без загрузки всего документа в ОЗУ.

## Часто задаваемые вопросы

### Что такое Aspose.PSD?
Aspose.PSD — это библиотека Java, позволяющая разработчикам программно создавать, редактировать и конвертировать файлы Photoshop PSD без необходимости использовать Adobe Photoshop. Она поддерживает чтение и запись PSD‑файлов, работу со слоями, масками, каналами и различными ресурсами изображений, а также предоставляет API для растровых и векторных операций, что делает её подходящей для серверной обработки изображений и автоматизации.

### Как скачать Aspose.PSD for Java?
Вы можете скачать её со страницы официальных релизов: [Aspose.PSD Java download](https://releases.aspose.com/psd/java/).

### Есть ли бесплатная пробная версия Aspose.PSD?
Да, полностью функциональная пробная версия доступна на той же странице загрузки. Она подходит для разработки и оценки.

### Можно ли получить поддержку для Aspose.PSD?
Конечно! Форум поддержки Aspose предоставляет ответы от команды продукта и сообщества: [Aspose support forum](https://forum.aspose.com/c/psd/34).

### Как получить временную лицензию для Aspose.PSD?
Вы можете запросить временную лицензию напрямую через портал лицензирования Aspose, который предоставляет ключ ограниченный по времени, действительный 30 дней. Это позволяет оценить полный функционал Aspose.PSD без покупки коммерческой лицензии. По окончании пробного периода необходимо заменить временный ключ постоянной лицензией для дальнейшего использования библиотеки в продакшн. Посетите страницу временной лицензии, чтобы сгенерировать ограниченный по времени ключ: [temporary license page](https://purchase.aspose.com/temporary-license/).

## Часто задаваемые вопросы

**В: Можно ли использовать объект graphics для редактирования только одного конкретного слоя?**  
**О:** Да. После загрузки PSD получите нужный слой через `psdImage.getLayers().get_Item(index)` и передайте этот слой в конструктор `Graphics`.

**В: Влияет ли метод сжатия Raw на размер файла?**  
**О:** Raw сохраняет пиксельные данные без какого‑либо сжатия, поэтому полученный файл больше, чем сжатый PSD, но гарантирует 100 % точность пикселей.

**В: Можно ли экспортировать отредактированный PSD в другой формат (например, PNG)?**  
**О:** Конечно. После редактирования вызовите `psdImage.save("output.png", new PngOptions())` — это стандартный способ **экспортировать PSD в PNG** с безпотерьным качеством.

**В: Какая версия Java требуется?**  
**О:** Aspose.PSD for Java поддерживает JDK 8 и новее, включая все LTS‑версии до JDK 21.

**В: Как освободить ресурсы после обработки?**  
**О:** Вызовите `psdImage.dispose()` и закройте все потоки (например, `ms.close()`), чтобы освободить нативную память и избежать утечек.

---

**Последнее обновление:** 2026-08-01  
**Тестировано с:** Aspose.PSD for Java (последний релиз)  
**Автор:** Aspose  

{{< blocks/products/products-backtop-button >}}

## Связанные руководства

- [Сохранить изображения в поток с Aspose.PSD for Java](/psd/java/advanced-techniques/save-images-to-stream/)
- [Экспортировать группу слоёв PSD в изображение с помощью Java](/psd/java/working-with-psd-files/export-psd-layer-group-to-image/)
- [Создать изображение с использованием потока в Aspose.PSD for Java](/psd/java/image-editing/create-image-using-stream/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}