---
date: 2026-05-29
description: تعلم كيفية تحويل PSD إلى PNG عن طريق تحميل الصور من دفق باستخدام Aspose.PSD
  for Java. يوضح لك هذا الدرس خطوة بخطوة لمعالجة الصور في Java كيفية قراءة وتحويل
  وحفظ ملفات PSD بكفاءة.
keywords:
- convert psd to png
- how to load psd
- read image from memory
- save image to stream
- java image processing tutorial
linktitle: تحميل الصور من الدفق
schemas:
- author: Aspose
  dateModified: '2026-05-29'
  description: Learn to convert PSD to PNG by loading images from a stream with Aspose.PSD
    for Java. This step‑by‑step Java image processing tutorial shows you how to read,
    convert, and save PSD files efficiently.
  headline: Convert PSD to PNG – Load Images from Stream (Java)
  type: TechArticle
- questions:
  - answer: Absolutely. The library’s streaming architecture lets you loop through
      thousands of PSD files, convert each to PNG, and write directly to output streams
      without excessive memory consumption.
    question: Is Aspose.PSD for Java suitable for batch image processing?
  - answer: Yes, you can explore a free trial version [here](https://releases.aspose.com/).
    question: Can I try Aspose.PSD for Java before purchasing?
  - answer: Join the community at the [Aspose.PSD forum](https://forum.aspose.com/c/psd/34)
      for assistance and discussions.
    question: Where can I find support for Aspose.PSD for Java?
  - answer: Obtain a temporary license [here](https://purchase.aspose.com/temporary-license/)
      for testing Aspose.PSD for Java.
    question: Do I need a temporary license for testing purposes?
  - answer: Visit the [purchase page](https://purchase.aspose.com/buy) to acquire
      Aspose.PSD for Java.
    question: Where can I purchase Aspose.PSD for Java?
  type: FAQPage
second_title: Aspose.PSD Java API
title: تحويل PSD إلى PNG – تحميل الصور من الدفق (Java)
url: /ar/java/advanced-techniques/loading-images-from-stream/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# تحويل PSD إلى PNG – تحميل الصور من التدفق (Java)

## المقدمة

في هذا الدرس ستكتشف كيفية **تحويل PSD إلى PNG** عن طريق تحميل صورة PSD مباشرةً من `InputStream` في Java. تجعل مكتبة Aspose.PSD للـ Java عملية قراءة ملف PSD من الذاكرة، تحويله، وكتابة النتيجة مرة أخرى إلى تدفق كصورة PNG. سنستعرض كل خطوة، نشرح لماذا كل استدعاء API مهم، ونقدم لك نصائح لتجنب المشكلات الشائعة.

## إجابات سريعة
- **ما هي أسهل طريقة لتحويل PSD إلى PNG في Java؟** قم بتحميل ملف PSD باستخدام `Image.load(stream)`، ثم حوله إلى `PsdImage`، ثم استدعِ `save(outputStream, new PngOptions())`.  
- **هل أحتاج إلى ترخيص لتشغيل الكود؟** الترخيص المؤقت يكفي للاختبار؛ الترخيص الكامل مطلوب للإنتاج.  
- **هل يمكنني معالجة ملفات PSD الكبيرة دون استهلاك عالي للذاكرة؟** نعم – Aspose.PSD يعالج الملفات بطريقة تدفقية، يدعم ملفات تصل إلى 2 GB دون تحميل المستند بالكامل في الذاكرة.  
- **ما إصدارات Java المدعومة؟** Java 8 حتى Java 21 مدعومة بالكامل.  
- **أين يمكنني العثور على المزيد من الأمثلة؟** يحتوي [التوثيق الرسمي](https://reference.aspose.com/psd/java/) على العشرات من مقتطفات الشيفرة.

## ما هو تحويل PSD إلى PNG؟
**تحويل PSD إلى PNG** هو عملية قراءة ملف Photoshop (.psd) وتصدير بيانات الصورة النقطية إلى تنسيق Portable Network Graphics (PNG). باستخدام Aspose.PSD، يحدث هذا التحويل في الذاكرة، بحيث يمكنك القراءة أو الكتابة إلى التدفقات دون الحاجة إلى نظام الملفات.

## لماذا تستخدم Aspose.PSD للـ Java؟
تدعم Aspose.PSD **أكثر من 30 تنسيق إدخال وإخراج** ويمكنها التعامل مع **ملفات PSD متعددة المئات من الصفحات حتى 2 GB** مع الحفاظ على استهلاك الذاكرة أقل من 200 MB. توفر المكتبة API نقيّة للـ Java، مما يعني عدم الحاجة إلى مكتبات أصلية أو تثبيت Photoshop، وهو ما يجعلها مثالية لأنابيب معالجة الصور على الخادم.

## المتطلبات المسبقة

قبل البدء، تأكد من وجود ما يلي:

- خبرة أساسية في تطوير Java.  
- مكتبة Aspose.PSD للـ Java مثبتة – قم بتنزيلها من [موقع Aspose](https://releases.aspose.com/psd/java/).  
- بيئة تطوير Java أو أداة بناء (Maven/Gradle) جاهزة لإضافة ملف JAR الخاص بـ Aspose.PSD إلى مشروعك.

## استيراد الحزم

فئة `Image` هي الفئة الأساسية في Aspose.PSD التي تمثل أي صورة نقطية. توفر `PsdImage` ميزات خاصة بـ Photoshop مثل الطبقات والقنوات. تسمح لك `PngOptions` بتكوين إعدادات PNG. `FileInputStream` و `FileOutputStream` هما فئتا I/O القياسيتين في Java لقراءة وكتابة الملفات.

```java
import com.aspose.psd.Image;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.PngOptions;
import com.aspose.psd.system.io.FileMode;
import com.aspose.psd.system.io.FileStream;
import com.aspose.psd.system.io.MemoryStream;
import java.io.FileInputStream;
import java.io.FileNotFoundException;
import java.io.FileOutputStream;
```

## الخطوة 1: إعداد دليل المستند الخاص بك

تأكد من وجود دليل مخصص لملفات PSD المصدرية وصور الإخراج. استبدل `"Your Document Directory"` في الشيفرة بالمسار المطلق الفعلي على جهازك.

```java
String dataDir = "Your Document Directory";
```

## الخطوة 2: تحديد مسارات المصدر والوجهة

حدد مسار ملف PSD كمصدر والمسار المطلوب للإخراج لصورة PNG الناتجة. يساعد هذا الفصل الواضح عندما تنتقل لاحقًا إلى القراءة من قاعدة بيانات أو طلب HTTP.

```java
String sourceFile = dataDir + "sample.psd";
String destName = dataDir + "result.png";
```

## الخطوة 3: إنشاء تدفق الإدخال وتحميل الصورة

`FileInputStream` يقرأ البايتات الخام من ملف على القرص. الطريقة الساكنة `Image.load(InputStream)` تقوم بتحميل صورة من التدفق المحدد وتعيد كائن `Image`.

```java
FileInputStream inputStream = new FileInputStream(sourceFile);
Image image = Image.load(inputStream);
```

## الخطوة 4: تحويل الصورة إلى PsdImage

`PsdImage` تمثل مستند Photoshop، وتكشف عن الطبقات والقنوات والبيانات الخاصة بـ PSD. حول كائن `Image` العام إلى `PsdImage` للعمل مع هذه الميزات.

```java
PsdImage psdImage = (PsdImage)image;
```

## الخطوة 5: حفظ الصورة إلى تدفق مع خيارات PNG

`FileOutputStream` يكتب البايتات الخام إلى ملف. `PngOptions` يضبط مستوى الضغط، نوع اللون، والتداخل لإخراج PNG.

```java
FileOutputStream outputStream = new FileOutputStream(destName);
psdImage.save(outputStream, new PngOptions());
```

تهانينا! لقد نجحت في **تحويل PSD إلى PNG** عن طريق تحميل الصورة من تدفق باستخدام Aspose.PSD للـ Java.

## المشكلات الشائعة والحلول

- **OutOfMemoryError في ملفات PSD الكبيرة جدًا** – تأكد من استخدام API التدفق (`Image.load(InputStream)`) وتجنب استدعاء `save` على كائنات `PsdImage` التي تم تحويلها بالكامل إلى الذاكرة.  
- **فقدان الطبقات بعد التحويل** – تحقق من أنك تعمل مع كائن `PsdImage`؛ كائنات `Image` العامة تفقد معلومات الطبقة.  
- **ألوان أو شفافية غير صحيحة** – اضبط `pngOptions.setColorType(PngColorType.TruecolorWithAlpha)` للحفاظ على قنوات ألفا.

## الأسئلة المتكررة

**س: هل Aspose.PSD للـ Java مناسب لمعالجة الصور على دفعات؟**  
ج: بالتأكيد. تسمح بنية المكتبة التدفقية لك بالتكرار عبر آلاف ملفات PSD، تحويل كل منها إلى PNG، والكتابة مباشرة إلى تدفقات الإخراج دون استهلاك مفرط للذاكرة.

**س: هل يمكنني تجربة Aspose.PSD للـ Java قبل الشراء؟**  
ج: نعم، يمكنك استكشاف نسخة تجريبية مجانية [هنا](https://releases.aspose.com/).

**س: أين يمكنني العثور على دعم Aspose.PSD للـ Java؟**  
ج: انضم إلى المجتمع في [منتدى Aspose.PSD](https://forum.aspose.com/c/psd/34) للحصول على المساعدة والنقاشات.

**س: هل أحتاج إلى ترخيص مؤقت لأغراض الاختبار؟**  
ج: احصل على ترخيص مؤقت [هنا](https://purchase.aspose.com/temporary-license/) لاختبار Aspose.PSD للـ Java.

**س: أين يمكنني شراء Aspose.PSD للـ Java؟**  
ج: زر [صفحة الشراء](https://purchase.aspose.com/buy) للحصول على Aspose.PSD للـ Java.

---

**آخر تحديث:** 2026-05-29  
**تم الاختبار مع:** Aspose.PSD للـ Java 24.12  
**المؤلف:** Aspose

## الدروس ذات الصلة

- [حفظ الصور إلى تدفق باستخدام Aspose.PSD للـ Java](/psd/java/advanced-techniques/save-images-to-stream/)
- [حفظ الصور إلى قرص باستخدام Aspose.PSD للـ Java](/psd/java/advanced-techniques/save-images-to-disk/)
- [تحويل PSD إلى تنسيقات الصور النقطية باستخدام Aspose.PSD للـ Java](/psd/java/advanced-techniques/convert-psd-to-raster-formats/)

{{< /blocks/products/pf/tutorial-page-section >}}
{{< blocks/products/products-backtop-button >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}