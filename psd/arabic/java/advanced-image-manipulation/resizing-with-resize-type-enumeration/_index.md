---
date: 2026-06-03
description: تعلم كيفية تغيير حجم الصورة باستخدام Aspose.PSD for Java. يغطي هذا الدليل
  خطوة بخطوة Resize Type Enumeration، تغيير حجم الصورة بجودة عالية، وكيفية تحويل PSD
  إلى JPEG.
keywords:
- how to resize image
- convert psd to jpeg
- high quality image resize
- resize image java
- java image manipulation tutorial
linktitle: تغيير الحجم باستخدام Resize Type Enumeration
schemas:
- author: Aspose
  dateModified: '2026-06-03'
  description: Learn how to resize image with Aspose.PSD for Java. This step‑by‑step
    guide covers the Resize Type Enumeration, high‑quality image resize, and how to
    convert PSD to JPEG.
  headline: How to Resize Image Java Using Resize Type Enumeration
  type: TechArticle
- description: Learn how to resize image with Aspose.PSD for Java. This step‑by‑step
    guide covers the Resize Type Enumeration, high‑quality image resize, and how to
    convert PSD to JPEG.
  name: How to Resize Image Java Using Resize Type Enumeration
  steps:
  - name: '**Java Development Environment** – JDK 8 or newer installed and configured.'
    text: '**Java Development Environment** – JDK 8 or newer installed and configured.'
  - name: '**Aspose.PSD Library** – Download the latest JAR from the [website](https://releases.aspose.com/psd/java/).'
    text: '**Aspose.PSD Library** – Download the latest JAR from the [website](https://releases.aspose.com/psd/java/).'
  - name: '**Sample PSD File** – Use the [sample.psd](Your Document Directory/sample.psd)
      file included with the SDK for hands‑on testing.'
    text: '**Sample PSD File** – Use the [sample.psd](Your Document Directory/sample.psd)
      file included with the SDK for hands‑on testing.'
  type: HowTo
- questions:
  - answer: Load the PSD with `Image.load`, then call `image.save("output.jpg", new
      JpegOptions());`.
    question: How do I programmatically convert a PSD file to JPEG without resizing?
  - answer: Yes, you can set the `Resolution` property on the `Image` object before
      saving.
    question: Is it possible to maintain the original DPI when resizing?
  - answer: While you can call `resize` multiple times, it’s more efficient to calculate
      the final dimensions and resize once.
    question: Can I chain multiple resize operations?
  type: FAQPage
second_title: Aspose.PSD Java API
title: كيفية تغيير حجم الصورة Java باستخدام Resize Type Enumeration
url: /ar/java/advanced-image-manipulation/resizing-with-resize-type-enumeration/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# كيفية تغيير حجم صورة Java باستخدام تعداد نوع التحجيم

## مقدمة

إذا كنت تبحث عن **كيفية تغيير حجم الصورة** بكفاءة في مشروع Java، فإن Aspose.PSD for Java يوفر واجهة برمجة تطبيقات نظيفة وعالية الأداء. في هذا الدرس سنستعرض تحميل ملف PSD، وتطبيق **تعداد نوع التحجيم** لتغيير حجم الصورة بجودة عالية، وأخيرًا **تحويل PSD إلى JPEG**. سواءً كنت تبني محررًا سطح مكتب أو خط أنابيب خادم آلي، فإن هذه الخطوات تتيح لك التحكم بالأبعاد والجودة والصيغة ببضع أسطر من الشيفرة.

## إجابات سريعة
- **ما المكتبة التي تتعامل مع تغيير حجم الصورة في Java؟** Aspose.PSD for Java.
- **أي نوع تحجيم يقدم أفضل جودة؟** `ResizeType.LanczosResample`.
- **هل يمكنني تحويل PSD إلى JPEG بعد تغيير الحجم؟** نعم – فقط احفظ باستخدام `JpegOptions`.
- **هل أحتاج إلى ترخيص للاستخدام في الإنتاج؟** يتطلب الاستخدام في الإنتاج ترخيصًا صالحًا لـ Aspose.PSD.
- **هل هذه الطريقة مناسبة للدفعات الكبيرة؟** بالتأكيد؛ الواجهة البرمجية تعالج ملفات مئات الصفحات دون تحميل المستند بالكامل في الذاكرة.

## ما هو "كيفية تغيير حجم الصورة" في Java؟
تشير **كيفية تغيير حجم الصورة** إلى تعديل أبعاد البكسل لصورة برمجيًا مع الحفاظ على الدقة البصرية. طريقة `Resize` في Aspose.PSD مع تعداد `ResizeType` توفر تحكمًا دقيقًا في خوارزميات التحجيم، مما يسمح للمطورين بالحفاظ على الجودة عبر مجموعة واسعة من ملفات المصدر وأحجام الهدف.

## لماذا نستخدم تعداد نوع التحجيم؟
يتيح لك `ResizeType` اختيار خوارزمية إعادة العينة التي تحقق أفضل توازن بين السرعة والجودة البصرية. في معظم الحالات، يقدم **LanczosResample** نتائج حادة بتكلفة أداء معتدلة، حيث يعالج صورة بحجم 2000 × 1500 في أقل من 120 ms على معالج من فئة الخوادم العادية مع الحفاظ على تفاصيل الحواف.

## المتطلبات المسبقة

قبل أن تبدأ، تأكد من أن لديك:

1. **بيئة تطوير Java** – JDK 8 أو أحدث مثبتة ومُكوَّنة.  
2. **مكتبة Aspose.PSD** – قم بتنزيل أحدث ملف JAR من [الموقع الإلكتروني](https://releases.aspose.com/psd/java/).  
3. **ملف PSD تجريبي** – استخدم ملف [sample.psd](Your Document Directory/sample.psd) المرفق مع SDK للاختبار العملي.

## استيراد الحزم

`Image` هو الفئة الأساسية لجميع أنواع الصور في Aspose.PSD. أضف الاستيرادات المطلوبة إلى ملف مصدر Java الخاص بك:

```java
import com.aspose.psd.Image;
import com.aspose.psd.ResizeType;

import com.aspose.psd.imageoptions.JpegOptions;
```

## الخطوة 1: تحميل الصورة

### تعريف المرجع
فئة `RasterImage` هي الكائن الأساسي في Aspose.PSD الذي يمثل صورة نقطية تم تحميلها من ملف PSD.

حمّل ملف PSD الخاص بك في كائن `RasterImage` حتى تتمكن من تعديل بكسلاته:

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

// Load an existing image into an instance of RasterImage class
Image image = Image.load(sourceFile);
```

## الخطوة 2: تغيير حجم الصورة

`image.resize(width, height, resizeType)` يغيّر حجم الصورة إلى الأبعاد المحددة باستخدام الخوارزمية المختارة.

الآن قم بتغيير حجم الصورة المحملة باستخدام **تعداد نوع التحجيم**. في هذا المثال نستخدم طريقة Lanczos Resample، وهي مثالية عندما تريد **كيفية تغيير حجم الصورة** بجودة عالية:

```java
image.resize(300, 300, ResizeType.LanczosResample);
```

## الخطوة 3: حفظ الصورة بعد تغيير الحجم

`image.save(path, options)` يكتب الصورة إلى **القرص** بالتنسيق المحدد بواسطة الخيارات المقدمة.

بعد تغيير الحجم، احفظ الصورة بالأبعاد المحددة ونوع التحجيم المختار. هنا، نوضح أيضًا **تحويل PSD إلى JPEG** بحفظ النتيجة كملف JPEG:

```java
String destName = dataDir + "ResizingwithResizeTypeEnumeration_out.jpg";
image.save(destName, new JpegOptions());
```

## لماذا نستخدم تعداد نوع التحجيم؟

`ResizeType` يمنحك تحكمًا دقيقًا في خوارزمية إعادة العينة، مما يسمح لك بموازنة السرعة والجودة. بالنسبة لمعظم التطبيقات، يوفر `LanczosResample` توازنًا ممتازًا، حيث يقدم نتائج حادة دون تكلفة أداء كبيرة، ويعمل بشكل جيد عبر مجموعة متنوعة من محتويات الصور.

## المشكلات الشائعة والحلول

- **الصورة تظهر ضبابية بعد التحجيم** – جرّب `ResizeType` مختلف مثل `Bicubic` أو `NearestNeighbour` لترى أيهما يعطي أفضل نتيجة بصرية لصورتك المحددة.  
- **خطأ OutOfMemoryError في ملفات PSD الكبيرة** – عالج الصورة على أجزاء أصغر أو زد حجم الذاكرة المخصصة للـ JVM (`-Xmx` flag). يمكن لـ Aspose.PSD معالجة ملفات تصل إلى **2 GB** دون تحميل المستند بالكامل في الذاكرة.

## الأسئلة المتكررة

### س1: هل Aspose.PSD for Java مناسب للمشاريع الصغيرة والكبيرة الحجم؟

A1: بالتأكيد! تم تصميم Aspose.PSD for Java لتلبية احتياجات المشاريع من جميع الأحجام، مع توفير القابلية للتوسع والكفاءة.

### س2: هل يمكنني استخدام نوع تحجيم مختلف غير Lanczos Resample؟

A2: نعم، يوفر Aspose.PSD for Java أنواعًا متعددة من التحجيم، مثل **NearestNeighbour** و **Bicubic** وغيرها. راجع وثائق API للقائمة الكاملة.

### س3: أين يمكنني العثور على دعم إضافي لـ Aspose.PSD for Java؟

A3: لأي استفسارات أو مساعدة، قم بزيارة [منتدى Aspose.PSD](https://forum.aspose.com/c/psd/34).

### س4: هل هناك نسخة تجريبية مجانية متاحة لـ Aspose.PSD for Java؟

A4: نعم، يمكنك الوصول إلى نسخة تجريبية مجانية [هنا](https://releases.aspose.com/).

### س5: كيف يمكنني الحصول على ترخيص مؤقت لـ Aspose.PSD for Java؟

A5: للحصول على ترخيص مؤقت، قم بزيارة [هذا الرابط](https://purchase.aspose.com/temporary-license/).

## أسئلة شائعة

**س: كيف يمكنني برمجيًا تحويل ملف PSD إلى JPEG دون تغيير الحجم؟**  
A: حمّل ملف PSD باستخدام `Image.load`، ثم استدعِ `image.save("output.jpg", new JpegOptions());`.

**س: هل من الممكن الحفاظ على DPI الأصلي عند تغيير الحجم؟**  
A: نعم، يمكنك ضبط خاصية `Resolution` على كائن `Image` قبل الحفظ.

**س: هل يمكنني ربط عمليات تغيير حجم متعددة؟**  
A: بالرغم من إمكانية استدعاء `resize` عدة مرات، إلا أن حساب الأبعاد النهائية وتغيير الحجم مرة واحدة يكون أكثر كفاءة.

---

**آخر تحديث:** 2026-06-03  
**تم الاختبار مع:** Aspose.PSD for Java 24.12  
**المؤلف:** Aspose  

{{< blocks/products/products-backtop-button >}}

## دروس ذات صلة

- [إعادة تحجيم بسيطة باستخدام Aspose.PSD – مكتبة معالجة الصور في Java](/psd/java/basic-image-operations/simple-resizing/)
- [تحجيم صورة عالي الجودة باستخدام Resampler Bicubic في Aspose.PSD for Java](/psd/java/advanced-image-manipulation/implement-bicubic-resampler/)
- [كيفية تحويل PSD إلى PNG وتغيير الحجم بنسبة متناسبة باستخدام Aspose.PSD for Java](/psd/java/advanced-image-manipulation/resize-image-proportionally/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}