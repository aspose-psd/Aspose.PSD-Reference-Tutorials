---
date: 2026-06-08
description: Узнайте, как сохранить PSD в PNG с использованием Aspose.PSD for Java
  и при необходимости прерывать конвертацию. Эффективно управляйте процессом обработки
  изображений.
keywords:
- save psd as png
- how to interrupt conversion
- psd to png conversion
- manage image workflow
linktitle: Поддержка Interrupt Monitor
schemas:
- author: Aspose
  dateModified: '2026-06-08'
  description: Learn how to save PSD as PNG using Aspose.PSD for Java and interrupt
    conversion when needed. Manage image workflow efficiently.
  headline: How to Save PSD as PNG with Interrupt Monitor in Aspose.PSD for Java
  type: TechArticle
- description: Learn how to save PSD as PNG using Aspose.PSD for Java and interrupt
    conversion when needed. Manage image workflow efficiently.
  name: How to Save PSD as PNG with Interrupt Monitor in Aspose.PSD for Java
  steps:
  - name: Set Your Document Directory
    text: Ensure to replace “Your Document Directory” with the actual path where your
      PSD documents are stored.
  - name: Define Image Options and Output Path
    text: Specify the image options, source PSD file, and the desired output path
      for the converted image.
  - name: Initialize Interrupt Monitor and SaveImageWorker
    text: The `InterruptMonitor` class watches a running conversion and can interrupt
      it when `requestInterrupt()` is called. Create instances of `InterruptMonitor`
      and `SaveImageWorker`, linking the monitor to the image conversion worker.
  - name: Start Image Conversion Thread
    text: Initiate a new thread for the image conversion process and introduce a timeout
      period to anticipate interruption.
  - name: Interrupt the Process
    text: Calling `monitor.requestInterrupt()` signals the monitor to abort the ongoing
      conversion. Interrupt the image conversion process using the `InterruptMonitor`
      and wait for the interruption to complete. Finally, clean up by deleting the
      output file.
  type: HowTo
- questions:
  - answer: Yes, use `InterruptMonitor` to stop the process on demand.
    question: Can I interrupt a PSD‑to‑PNG conversion?
  - answer: Call `save(outputPath, new PngOptions())`.
    question: Which method saves a PSD as PNG?
  - answer: A commercial license is required; a free trial is available.
    question: Do I need a license for production?
  - answer: Java 8 and later are fully supported.
    question: What Java version is supported?
  - answer: Conversions can run in separate threads; the monitor handles interruptions
      safely.
    question: Is the library thread‑safe?
  type: FAQPage
second_title: Aspose.PSD Java API
title: Как сохранить PSD в PNG с помощью Interrupt Monitor в Aspose.PSD for Java
url: /ru/java/advanced-techniques/support-interrupt-monitor/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Сохранить PSD как PNG с помощью Interrupt Monitor в Aspose.PSD для Java

## Введение

Если вам нужно **сохранить PSD как PNG**, сохраняя полный контроль над длительными конверсиями, Interrupt Monitor в Aspose.PSD для Java предоставляет именно это. В этом руководстве мы пройдем настройку монитора, конвертацию файла PSD в PNG и безопасное прерывание операции при необходимости. Вы также увидите, как это вписывается в типичный рабочий процесс обработки изображений и почему это необходимо для надёжных приложений.

## Быстрые ответы
- **Можно ли прервать конверсию PSD‑в‑PNG?** Да, используйте `InterruptMonitor` для остановки процесса по требованию.  
- **Какой метод сохраняет PSD как PNG?** Вызовите `save(outputPath, new PngOptions())`.  
- **Нужна ли лицензия для продакшна?** Требуется коммерческая лицензия; доступна бесплатная пробная версия.  
- **Какая версия Java поддерживается?** Полностью поддерживаются Java 8 и более новые версии.  
- **Является ли библиотека потокобезопасной?** Конверсии могут выполняться в отдельных потоках; монитор безопасно обрабатывает прерывания.

## Предварительные требования

Прежде чем погрузиться в детали использования Interrupt Monitor, убедитесь, что у вас есть следующие предварительные требования:

- **Среда разработки Java:** Настройте среду разработки Java на вашей системе.  
- **Библиотека Aspose.PSD:** Получите библиотеку Aspose.PSD для Java. Вы можете скачать её [здесь](https://releases.aspose.com/psd/java/). Вы также можете посетить основной сайт Aspose [здесь](https://releases.aspose.com/).  
- **Каталог документов:** Иметь назначенный каталог для ваших PSD‑документов.

## Импорт пакетов

Начните с импорта необходимых пакетов в ваш Java‑проект. Это гарантирует доступ к функционалу Aspose.PSD.

```java
import com.aspose.psd.ImageOptionsBase;

import static com.aspose.psd.examples.Utils.Utils.getDateTime;
import com.aspose.psd.imageoptions.PngOptions;
import com.aspose.psd.multithreading.InterruptMonitor;
import com.aspose.psd.system.Threading.ThreadStart;
import java.io.File;
```

Теперь разберём пример кода шаг за шагом, чтобы внедрить Interrupt Monitor в ваш проект Aspose.PSD для Java.

## Как сохранить PSD как PNG с помощью Interrupt Monitor?

`PsdImage` представляет PSD‑документ, загруженный в память.  
`SaveImageWorker` выполняет конвертацию изображения в отдельном потоке.  

Загрузите ваш PSD‑файл с помощью `new PsdImage("source.psd")`, прикрепите `InterruptMonitor` к `SaveImageWorker` и вызовите `save("output.png", new PngOptions())`. Монитор отслеживает запрос отмены и чисто прерывает конверсию, возвращая управление вашему приложению в течение миллисекунд.

### Шаг 1: Установите каталог документов

```java
String dataDir = "Your Document Directory";
```

Убедитесь, что заменили “Your Document Directory” на фактический путь, где хранятся ваши PSD‑документы.

### Шаг 2: Определите параметры изображения и путь вывода

```java
ImageOptionsBase saveOptions = new PngOptions();
String source = dataDir + "big2.psb";
String output = dataDir + "big_out.png";
```

Укажите параметры изображения, исходный PSD‑файл и желаемый путь вывода для конвертированного изображения.

### Шаг 3: Инициализируйте Interrupt Monitor и SaveImageWorker

Класс `InterruptMonitor` отслеживает текущую конверсию и может прервать её, когда вызывается `requestInterrupt()`.

```java
InterruptMonitor monitor = new InterruptMonitor();
SaveImageWorker worker = new SaveImageWorker(source, output, saveOptions, monitor);
```

Создайте экземпляры `InterruptMonitor` и `SaveImageWorker`, связывая монитор с работником конвертации изображения.

### Шаг 4: Запустите поток конвертации изображения

```java
Thread thread = new Thread(worker.ThreadProc());
try {
    thread.start();
    // Add a timeout to allow for potential interruption
    Thread.sleep(3000);
```

Запустите новый поток для процесса конвертации изображения и задайте период тайм‑аута для предвидения прерывания.

### Шаг 5: Прервите процесс

Вызов `monitor.requestInterrupt()` сигнализирует монитору о необходимости прервать текущую конверсию.

```java
    // Interrupt the process
    monitor.interrupt();
    System.out.println("Interrupting the save thread #" + thread.getId() + " at " + getDateTime().toString());

    // Wait for interruption...
    thread.join();
} finally {
    // Delete the output file if it exists
    File f = new File(output);
    if (f.exists()) {
        f.delete();
    }
}
```

Прервите процесс конвертации изображения с помощью `InterruptMonitor` и дождитесь завершения прерывания. В конце очистите, удалив выходной файл.

## Почему использовать Interrupt Monitor для конвертации PSD‑в‑PNG?

Aspose.PSD поддерживает **более 30 форматов вывода**, включая PNG, JPEG, BMP и TIFF, и может обрабатывать файлы размером до **500 МБ** без загрузки всего документа в память. Добавив Interrupt Monitor, вы уменьшаете нагрузку на CPU и повышаете отзывчивость в пакетных конвейерах обработки, особенно когда конверсия превышает ожидаемые временные ограничения.

## Распространённые проблемы и решения

- **Конверсия зависает бесконечно:** Убедитесь, что монитор прикреплен **до** вызова `save`.  
- **Выходной файл повреждён после прерывания:** Монитор чисто прерывает процесс; однако всегда проверяйте, существует ли файл перед его использованием.  
- **Проблемы потокобезопасности:** Выполняйте каждую конверсию в отдельном потоке; монитор влияет только на связанного с ним работника.

## Часто задаваемые вопросы

**Q1: Что такое Interrupt Monitor в Aspose.PSD для Java?**  
A: Interrupt Monitor позволяет разработчикам приостанавливать или отменять длительные конвертации изображений, предоставляя контроль над использованием ресурсов в реальном времени.

**Q2: Как получить библиотеку Aspose.PSD для Java?**  
A: Вы можете скачать библиотеку Aspose.PSD для Java [здесь](https://releases.aspose.com/psd/java/).

**Q3: Доступна ли бесплатная пробная версия Aspose.PSD для Java?**  
A: Да, вы можете ознакомиться с бесплатной пробной версией Aspose.PSD [здесь](https://releases.aspose.com/).

**Q4: Где можно получить поддержку Aspose.PSD для Java?**  
A: Посетите форум поддержки Aspose.PSD для Java [здесь](https://forum.aspose.com/c/psd/34).

**Q5: Как приобрести лицензию на Aspose.PSD для Java?**  
A: Вы можете купить лицензию на Aspose.PSD для Java [здесь](https://purchase.aspose.com/buy).

**Q6: Можно ли конвертировать несколько PSD‑файлов в PNG параллельно?**  
A: Да, создайте отдельный поток для каждого файла и прикрепите индивидуальный `InterruptMonitor` к каждому работнику конвертации.

**Q7: Обрабатывает ли библиотека цветовые профили при конвертации PSD‑в‑PNG?**  
A: Абсолютно; Aspose.PSD сохраняет встроенные ICC‑профили и автоматически применяет их к выходному PNG.

---

**Последнее обновление:** 2026-06-08  
**Тестировано с:** Aspose.PSD 23.12 for Java  
**Автор:** Aspose  

{{< blocks/products/products-backtop-button >}}

## Связанные руководства

- [Сохранить PSD как PNG и применить Rendering Drop Shadow в Aspose.PSD для Java](/psd/java/advanced-image-manipulation/rendering-drop-shadow/)
- [Экспортировать PSD в PNG и добавить новый обычный слой с помощью Aspose.PSD для Java](/psd/java/advanced-image-effects/add-new-regular-layer/)
- [Поддержка Interrupt Monitor в PSD‑файлах — Java](/psd/java/psd-layer-management-effects/support-interrupt-monitor-psd-files/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}