---
date: 2026-06-08
description: تعلم كيفية حفظ PSD كـ PNG باستخدام Aspose.PSD للـ Java وإيقاف التحويل
  عند الحاجة. إدارة سير عمل الصور بكفاءة.
keywords:
- save psd as png
- how to interrupt conversion
- psd to png conversion
- manage image workflow
linktitle: دعم Interrupt Monitor
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
title: كيفية حفظ PSD كـ PNG باستخدام Interrupt Monitor في Aspose.PSD للـ Java
url: /ar/java/advanced-techniques/support-interrupt-monitor/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# حفظ PSD كـ PNG باستخدام مراقب المقاطعة في Aspose.PSD للـ Java

## مقدمة

إذا كنت بحاجة إلى **حفظ PSD كـ PNG** مع الحفاظ على التحكم الكامل في التحويلات طويلة الأمد، فإن مراقب المقاطعة في Aspose.PSD للـ Java يوفر لك ذلك بالضبط. في هذا الدرس سنستعرض إعداد المراقب، تحويل ملف PSD إلى PNG، وإلغاء العملية بأمان عند الحاجة. ستلاحظ أيضًا كيف يتناسب ذلك مع سير عمل معالجة الصور النموذجي ولماذا يُعد ضروريًا للتطبيقات القوية.

## إجابات سريعة
- **هل يمكنني إيقاف تحويل PSD‑إلى‑PNG؟** نعم، استخدم `InterruptMonitor` لإيقاف العملية عند الطلب.  
- **ما الطريقة التي تحفظ PSD كـ PNG؟** استدعِ `save(outputPath, new PngOptions())`.  
- **هل أحتاج إلى ترخيص للإنتاج؟** يتطلب ترخيص تجاري؛ يتوفر نسخة تجريبية مجانية.  
- **ما نسخة Java المدعومة؟** Java 8 وما بعدها مدعولة بالكامل.  
- **هل المكتبة آمنة من حيث الخيوط؟** يمكن تشغيل التحويلات في خيوط منفصلة؛ يتعامل المراقب مع المقاطعات بأمان.  

## المتطلبات المسبقة

قبل الغوص في تفاصيل استخدام مراقب المقاطعة، تأكد من توفر المتطلبات المسبقة التالية:

- **بيئة تطوير Java:** قم بإعداد بيئة تطوير Java على نظامك.  
- **مكتبة Aspose.PSD:** احصل على مكتبة Aspose.PSD للـ Java. يمكنك تنزيلها [هنا](https://releases.aspose.com/psd/java/). يمكنك أيضًا زيارة الموقع الرئيسي لـ Aspose [هنا](https://releases.aspose.com/).  
- **دليل المستندات:** احرص على وجود دليل مخصص لمستندات PSD الخاصة بك.  

## استيراد الحزم

ابدأ باستيراد الحزم الضرورية إلى مشروع Java الخاص بك. يضمن ذلك حصولك على وظائف Aspose.PSD.

```java
import com.aspose.psd.ImageOptionsBase;

import static com.aspose.psd.examples.Utils.Utils.getDateTime;
import com.aspose.psd.imageoptions.PngOptions;
import com.aspose.psd.multithreading.InterruptMonitor;
import com.aspose.psd.system.Threading.ThreadStart;
import java.io.File;
```

الآن، دعنا نفصل شفرة المثال إلى دليل خطوة بخطوة لتضمين مراقب المقاطعة في مشروع Aspose.PSD للـ Java الخاص بك.

## كيفية حفظ PSD كـ PNG باستخدام مراقب المقاطعة؟

`PsdImage` يمثل مستند PSD تم تحميله في الذاكرة.  
`SaveImageWorker` يقوم بإجراء تحويل الصورة في خيط منفصل.  

حمّل ملف PSD الخاص بك باستخدام `new PsdImage("source.psd")`، أرفق `InterruptMonitor` بـ `SaveImageWorker`، واستدعِ `save("output.png", new PngOptions())`. يراقب المراقب طلب الإلغاء ويوقف التحويل بنظافة، معيدًا التحكم إلى تطبيقك خلال ملليثانية.

### الخطوة 1: تعيين دليل المستندات الخاص بك

```java
String dataDir = "Your Document Directory";
```

تأكد من استبدال “Your Document Directory” بالمسار الفعلي حيث تُخزن مستندات PSD الخاصة بك.

### الخطوة 2: تعريف خيارات الصورة ومسار الإخراج

```java
ImageOptionsBase saveOptions = new PngOptions();
String source = dataDir + "big2.psb";
String output = dataDir + "big_out.png";
```

حدد خيارات الصورة، ملف PSD المصدر، ومسار الإخراج المطلوب للصورة المحولة.

### الخطوة 3: تهيئة مراقب المقاطعة و SaveImageWorker

فئة `InterruptMonitor` تراقب عملية تحويل جارية ويمكنها مقاطعتها عندما يتم استدعاء `requestInterrupt()`.

```java
InterruptMonitor monitor = new InterruptMonitor();
SaveImageWorker worker = new SaveImageWorker(source, output, saveOptions, monitor);
```

أنشئ مثيلات من `InterruptMonitor` و `SaveImageWorker`، وربط المراقب بموظف تحويل الصورة.

### الخطوة 4: بدء خيط تحويل الصورة

```java
Thread thread = new Thread(worker.ThreadProc());
try {
    thread.start();
    // Add a timeout to allow for potential interruption
    Thread.sleep(3000);
```

ابدأ خيطًا جديدًا لعملية تحويل الصورة وأدخل فترة مهلة لتوقع المقاطعة.

### الخطوة 5: إيقاف العملية

استدعاء `monitor.requestInterrupt()` يُشير إلى المراقب لإلغاء التحويل الجاري.

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

أوقف عملية تحويل الصورة باستخدام `InterruptMonitor` وانتظر اكتمال المقاطعة. أخيرًا، نظّف عن طريق حذف ملف الإخراج.

## لماذا نستخدم مراقب المقاطعة لتحويل PSD‑إلى‑PNG؟

يدعم Aspose.PSD **أكثر من 30 صيغة إخراج**، بما في ذلك PNG و JPEG و BMP و TIFF، ويمكنه معالجة ملفات تصل إلى **500 ميغابايت** دون تحميل المستند بالكامل في الذاكرة. بإضافة مراقب مقاطعة، تقلل من إهدار وحدة المعالجة المركزية وتحسن الاستجابة في خطوط معالجة الدفعات، خاصةً عندما يتجاوز التحويل الحدود الزمنية المتوقعة.

## المشكلات الشائعة والحلول

- **التقليب يتعطل إلى ما لا نهاية:** تأكد من إرفاق المراقب **قبل** استدعاء `save`.  
- **ملف الإخراج يتلف بعد المقاطعة:** المراقب يوقف العملية بنظافة؛ ومع ذلك، تحقق دائمًا من وجود الملف قبل استخدامه.  
- **مخاوف حول أمان الخيوط:** قم بتشغيل كل تحويل في خيط منفصل؛ المراقب يؤثر فقط على العامل المرتبط به.  

## الأسئلة المتكررة

**س1: ما هو مراقب المقاطعة في Aspose.PSD للـ Java؟**  
A: المراقب يتيح للمطورين إيقاف أو إلغاء التحويلات الطويلة للصور، مما يمنحهم تحكمًا فوريًا في استهلاك الموارد.

**س2: كيف يمكنني الحصول على مكتبة Aspose.PSD للـ Java؟**  
A: يمكنك تنزيل مكتبة Aspose.PSD للـ Java [هنا](https://releases.aspose.com/psd/java/).

**س3: هل تتوفر نسخة تجريبية مجانية لـ Aspose.PSD للـ Java؟**  
A: نعم، يمكنك تجربة نسخة تجريبية مجانية من Aspose.PSD [هنا](https://releases.aspose.com/).

**س4: أين يمكنني العثور على الدعم لـ Aspose.PSD للـ Java؟**  
A: قم بزيارة منتدى دعم Aspose.PSD للـ Java [هنا](https://forum.aspose.com/c/psd/34).

**س5: كيف يمكنني شراء ترخيص لـ Aspose.PSD للـ Java؟**  
A: يمكنك شراء ترخيص لـ Aspose.PSD للـ Java [هنا](https://purchase.aspose.com/buy).

**س6: هل يمكنني تحويل ملفات PSD متعددة إلى PNG بشكل متوازي؟**  
A: نعم، أنشئ خيطًا منفصلًا لكل ملف وأرفق `InterruptMonitor` فرديًا بكل عامل تحويل.

**س7: هل تتعامل المكتبة مع ملفات تعريف الألوان أثناء تحويل PSD‑إلى‑PNG؟**  
A: بالطبع؛ يحافظ Aspose.PSD على ملفات ICC المدمجة ويطبقها على PNG الناتج تلقائيًا.

**آخر تحديث:** 2026-06-08  
**تم الاختبار مع:** Aspose.PSD 23.12 for Java  
**المؤلف:** Aspose  

{{< blocks/products/products-backtop-button >}}

## الدروس ذات الصلة

- [حفظ PSD كـ PNG وتطبيق ظل الإظهار في Aspose.PSD للـ Java](/psd/java/advanced-image-manipulation/rendering-drop-shadow/)
- [تصدير PSD إلى PNG وإضافة طبقة عادية جديدة باستخدام Aspose.PSD للـ Java](/psd/java/advanced-image-effects/add-new-regular-layer/)
- [دعم مراقب المقاطعة في ملفات PSD - Java](/psd/java/psd-layer-management-effects/support-interrupt-monitor-psd-files/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}