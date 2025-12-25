---
date: 2025-12-25
description: تعلم كيفية تحويل ملفات PSD إلى PNG باستخدام Aspose.PSD للغة Java مع دعم
  مراقبة المقاطعة، بما في ذلك مثال على مقاطعة خيط Java ونصائح لحفظ ملف PSD كـ PNG.
linktitle: Support for Interrupt Monitor
second_title: Aspose.PSD Java API
title: كيفية تحويل PSD إلى PNG مع دعم مراقبة المقاطعة في Aspose.PSD للـ Java
url: /ar/java/advanced-techniques/support-interrupt-monitor/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# تحويل PSD إلى PNG باستخدام مراقب المقاطعة في Aspose.PSD للـ Java

## المقدمة

إذا كنت بحاجة إلى **تحويل PSD إلى PNG** مع الحفاظ على التحكم الكامل في عمليات تحويل الصور طويلة الأمد، فإن مراقب المقاطعة في Aspose.PSD للـ Java هو الأداة التي تبحث عنها. في هذا البرنامج التعليمي سنستعرض مثالًا واقعيًا **لإيقاف خيط Java** يتيح لك إيقاف التحويل في منتصف العملية، مما يمنحك المرونة لإدارة الموارد، فرض مهلات زمنية، أو الاستجابة لإلغاء المستخدم.

## إجابات سريعة
- **ماذا يفعل مراقب المقاطعة؟** يسمح لك بإرسال إشارة لإيقاف عملية تحويل الصورة الجارية بأمان.  
- **هل يمكنني تحويل PSD إلى PNG باستخدامه؟** نعم – يعمل المراقب مع أي عملية حفظ، بما في ذلك PNG.  
- **هل يلزم خيط منفصل؟** عادةً ما تقوم بتشغيل التحويل في خيط منفصل حتى تتمكن من مقاطعته.  
- **ما نسخة Aspose.PSD المطلوبة؟** أي نسخة حديثة تتضمن `com.aspose.psd.multithreading.InterruptMonitor`.  
- **هل أحتاج إلى ترخيص للإنتاج؟** نعم، يلزم وجود ترخيص صالح لـ Aspose.PSD للاستخدام غير التجريبي.

## ما هو “تحويل PSD إلى PNG” باستخدام مراقب المقاطعة؟

تحويل مستند فوتوشوب كبير (PSD/PSB) إلى صورة PNG قد يكون مستهلكًا للمعالج. من خلال ربط **مراقب المقاطعة** بعملية التحويل، تحصل على القدرة على إيقاف العملية برمجيًا — وهو مثالي لخدمات الويب، وظائف الدُفعات، أو تطبيقات الواجهة حيث قد يلغي المستخدمون العمليات.

## لماذا نستخدم مراقب المقاطعة؟

- **واجهة مستخدم سريعة الاستجابة:** يمنع تجميد التطبيق أثناء معالجة ملف كبير.  
- **إدارة الموارد:** إيقاف التحويلات التي تتجاوز حدود الوقت أو الذاكرة.  
- **معالجة الأخطاء:** تنظيف ملفات الإخراج الجزئية بأناقة عند حدوث مقاطعة.

## المتطلبات المسبقة

- بيئة تطوير Java (JDK 8 أو أحدث).  
- مكتبة Aspose.PSD للـ Java – حمّلها **[من هنا](https://releases.aspose.com/psd/java/)**.  
- مجلد يحتوي على ملفات PSD/PSB التي تريد العمل عليها.

## استيراد الحزم

ابدأ باستيراد الفئات المطلوبة. سيمكنك ذلك من الوصول إلى خيارات الصورة، مراقب المقاطعة، وأدوات الخيوط.

```java
import com.aspose.psd.ImageOptionsBase;

import static com.aspose.psd.examples.Utils.Utils.getDateTime;
import com.aspose.psd.imageoptions.PngOptions;
import com.aspose.psd.multithreading.InterruptMonitor;
import com.aspose.psd.system.Threading.ThreadStart;
import java.io.File;
```

## دليل خطوة بخطوة

### الخطوة 1: تعيين دليل المستندات الخاص بك

```java
String dataDir = "Your Document Directory";
```

استبدل `"Your Document Directory"` بالمسار المطلق حيث توجد ملفات PSD الخاصة بك.

### الخطوة 2: تعريف خيارات الصورة ومسار الإخراج

```java
ImageOptionsBase saveOptions = new PngOptions();
String source = dataDir + "big2.psb";
String output = dataDir + "big_out.png";
```

هنا نقوم **بحفظ PSD كـ PNG** باستخدام `PngOptions`. عدّل أسماء الملفات حسب الحاجة.

### الخطوة 3: تهيئة مراقب المقاطعة و SaveImageWorker

```java
InterruptMonitor monitor = new InterruptMonitor();
SaveImageWorker worker = new SaveImageWorker(source, output, saveOptions, monitor);
```

ستُستخدم نسخة `InterruptMonitor` لاحقًا لإيقاف التحويل. يربط `SaveImageWorker` المراقب بمهمة التحويل.

### الخطوة 4: بدء تحويل الصورة في خيط منفصل

```java
Thread thread = new Thread(worker.ThreadProc());
try {
    thread.start();
    // Add a timeout to allow for potential interruption
    Thread.sleep(3000);
```

نطلق عملية التحويل على خيط خلفي حتى يظل الخيط الرئيسي مستجيبًا. استدعاء `Thread.sleep(3000)` يحاكي سيناريو مهلة زمنية.

### الخطوة 5: مقاطعة العملية (مثال إيقاف خيط Java)

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

استدعاء `monitor.interrupt()` يُفعّل منطق **كيفية إيقاف المراقب**. بعد المقاطعة نقوم بتنظيف أي ملف PNG مكتوب جزئيًا.

## المشكلات الشائعة والحلول

| المشكلة | السبب | الحل |
|-------|--------|-----|
| التحويل لا يتوقف أبداً | المراقب غير مرتبط بالـ worker | تأكد من أن `SaveImageWorker` يحصل على نفس نسخة `InterruptMonitor`. |
| يبقى ملف الإخراج بعد المقاطعة | لم يتم تنفيذ كود التنظيف | تحقق من تشغيل كتلة `finally` وصحة مسار الملف. |
| `OutOfMemoryError` عند ملفات PSB الكبيرة | عدم استخدام خيارات البث | استخدم `PsdImage` مع `LoadOptions` التي تتيح تحميلًا موفرًا للذاكرة. |

## الأسئلة المتكررة

### س1: ما هو مراقب المقاطعة في Aspose.PSD للـ Java؟

ج1: يسمح مراقب المقاطعة للمطورين **بإدارة وإيقاف عمليات تحويل الصور**، مما يمنحك تحكمًا دقيقًا في المهام طويلة الأمد.

### س2: كيف يمكنني الحصول على مكتبة Aspose.PSD للـ Java؟

ج2: يمكنك تنزيل مكتبة Aspose.PSD للـ Java **[من هنا](https://releases.aspose.com/psd/java/)**.

### س3: هل هناك نسخة تجريبية مجانية متاحة لـ Aspose.PSD للـ Java؟

ج3: نعم، يمكنك تجربة نسخة تجريبية مجانية من Aspose.PSD **[من هنا](https://releases.aspose.com/)**.

### س4: أين يمكنني العثور على الدعم لـ Aspose.PSD للـ Java؟

ج4: زر منتدى دعم Aspose.PSD للـ Java **[من هنا](https://forum.aspose.com/c/psd/34)**.

### س5: كيف يمكنني شراء ترخيص لـ Aspose.PSD للـ Java؟

ج5: يمكنك شراء ترخيص لـ Aspose.PSD للـ Java **[من هنا](https://purchase.aspose.com/buy)**.

---

**آخر تحديث:** 2025-12-25  
**تم الاختبار مع:** Aspose.PSD 24.11 للـ Java  
**المؤلف:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}