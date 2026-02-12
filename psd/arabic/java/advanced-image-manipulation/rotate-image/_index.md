---
date: 2026-02-12
description: تعلم كيفية تدوير الصورة وكيفية تدوير الصورة بزاوية 270 درجة باستخدام
  Aspose.PSD للغة Java. يغطي هذا الدليل تدوير ملفات PSD، وعكس الصور، وتحويل PSD إلى
  JPEG دون الحاجة إلى Photoshop.
linktitle: Rotate Image 270 Degrees
second_title: Aspose.PSD Java API
title: كيفية تدوير الصورة 270 درجة باستخدام Aspose.PSD للـ Java
url: /ar/java/advanced-image-manipulation/rotate-image/
weight: 19
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# تدوير الصورة 270 درجة باستخدام Aspose.PSD للـ Java

## المقدمة

في هذا **java image processing tutorial**، ستكتشف **how to rotate image** 270 درجة بسرعة وموثوقية باستخدام Aspose.PSD للـ Java. سواءً كنت تبني أداة تحرير صور، أو تقوم بأتمتة تحويلات دفعة، أو فقط تحتاج إلى إعادة توجيه طبقة PSD، فإن المكتبة تجعل المهمة سهلة. سنستعرض أيضًا تقنيات **flip image java** وتحويل ملف PSD المدور إلى JPEG، لتتمكن من الحصول على سير عمل كامل من البداية إلى النهاية دون الحاجة إلى Photoshop.

## الإجابات السريعة
- **ما المكتبة التي تتعامل مع التدوير؟** Aspose.PSD for Java  
- **ما زاوية التدوير المستخدمة في المثال؟** 270 degrees  
- **هل يمكنني أيضًا عكس الصورة؟** Yes – use `RotateFlipType` options like `Rotate90FlipX`  
- **كيف أحفظ النتيجة؟** In the example we save as JPEG using `JpegOptions`  
- **هل أحتاج إلى ترخيص للإنتاج؟** A valid Aspose.PSD license is required for commercial use  

## ما هو “rotate image 270 degrees”؟

تدوير صورة بزاوية 270 درجة يعني تحويل الصورة إلى ثلاثة أرباع دورة كاملة باتجاه عقارب الساعة (أو 90 درجة عكس اتجاه عقارب الساعة). في العديد من سيناريوهات تحرير الرسومات، يتطابق هذا الاتجاه مع تخطيط البورتريه الأصلي بعد سلسلة من التحويلات.

## لماذا تستخدم Aspose.PSD لهذه المهمة؟

- **Full PSD support** – يعمل مع الطبقات، الأقنعة، وكائنات الضبط.  
- **No native Photoshop required** – يعمل على أي بيئة تشغيل Java.  
- **Simple API** – استدعاء طريقة واحدة (`rotateFlip`) يتعامل مع التدوير والعكس.  
- **Easy format conversion** – تصدير مباشرة إلى JPEG أو PNG أو صيغ شائعة أخرى.

## كيفية تدوير الصورة باستخدام Aspose.PSD للـ Java

فيما يلي دليل خطوة بخطوة يوضح لك كيفية تحميل ملف PSD، تطبيق تدوير 270°، عكس الصورة اختياريًا، وأخيرًا حفظ النتيجة كملف JPEG.

### المتطلبات المسبقة

قبل أن تبدأ، تأكد من أن لديك:

- مكتبة **Aspose.PSD for Java** مثبتة. يمكنك تنزيلها وعرض مرجع API الكامل [هنا](https://reference.aspose.com/psd/java/).  
- بيئة تطوير Java (JDK 8 أو أعلى).  
- ملف PSD تجريبي تريد تدويره. قم بتحديث المتغير `sourceFile` في الكود بالمسار الصحيح لملفك.

### استيراد الحزم

ابدأ باستيراد الفئات اللازمة من حزمة Aspose.PSD:

```java
import com.aspose.psd.Image;
import com.aspose.psd.RotateFlipType;

import com.aspose.psd.imageoptions.JpegOptions;
```

### الخطوة 1: تحميل الصورة

أنشئ كائن `Image` يشير إلى ملف PSD المصدر الخاص بك:

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";
Image image = Image.load(sourceFile);
```

### الخطوة 2: تدوير الصورة 270 درجة

استخدم طريقة `rotateFlip` مع `RotateFlipType.Rotate270FlipNone` لتحقيق تدوير 270 درجة دون أي عكس:

```java
image.rotateFlip(RotateFlipType.Rotate270FlipNone);
```

> **نصيحة احترافية:** إذا كنت بحاجة أيضًا إلى عكس الصورة أفقيًا أو عموديًا، اختر `RotateFlipType` مختلف مثل `Rotate90FlipX` أو `Rotate180FlipY`. هذا هو الطريقة الأكثر شيوعًا لعمليات **flip image java**.

### الخطوة 3: تحويل PSD إلى JPEG وحفظه

بعد التدوير، يمكنك **convert PSD to JPEG** (أو أي صيغة مدعومة أخرى) باستخدام فئة الخيارات المناسبة:

```java
String destName = dataDir + "RotatedImage_out.jpg";
image.save(destName, new JpegOptions());
```

الملف `RotatedImage_out.jpg` الآن يحتوي على محتوى PSD الأصلي المدور بزاوية 270 درجة ومُحفظ كملف JPEG.

## لماذا هذا مهم – حالات الاستخدام في العالم الحقيقي

- **Batch processing of product catalogs** – تدوير العشرات من ملفات PSD إلى اتجاه موحد قبل النشر.  
- **Automated thumbnail generation** – إنشاء معاينات ذات اتجاه صحيح لمعارض الويب دون فتح Photoshop.  
- **Mobile app back‑ends** – إعادة توجيه ملفات PSD التي يرفعها المستخدم على جانب الخادم باستخدام Java النقي.

## المشكلات الشائعة & استكشاف الأخطاء

| المشكلة | الحل |
|-------|----------|
| **Image appears upside‑down** | تحقق من أنك استخدمت `Rotate270FlipNone`. للحصول على تدوير 90 درجة باتجاه عقارب الساعة استخدم `Rotate90FlipNone`. |
| **Output file is corrupted** | تأكد من وجود مجلد الوجهة وأن لديك أذونات كتابة. |
| **License exception** | قم بتثبيت ترخيص Aspose.PSD مؤقت أو دائم قبل تحميل الصورة في بيئة الإنتاج. |
| **Need to rotate image without Photoshop** | تقوم هذه الـ API بتنفيذ التدوير بالكامل في الكود، مما يلغي الاعتماد على Photoshop. |
| **Want to flip image as part of the same operation** | استخدم قيم `RotateFlipType` أخرى مثل `Rotate90FlipX` (يشمل **how to flip image**). |

## الأسئلة المتكررة

**س: هل Aspose.PSD متوافق مع صيغ صور مختلفة؟**  
ج: نعم، يدعم Aspose.PSD صيغ PSD، JPEG، PNG، BMP، GIF، والعديد من صيغ الرسوم النقطية الأخرى.

**س: هل يمكنني تطبيق تدويرات مخصصة، وليس فقط القلب المسبق؟**  
ج: بالتأكيد! بينما توفر `RotateFlipType` الزوايا الشائعة، يمكنك دمج عدة استدعاءات أو استخدام مصفوفات التحويل للحصول على زوايا عشوائية.

**س: كيف أحول ملف PSD المدور إلى صيغة أخرى، مثل PNG؟**  
ج: استبدل `JpegOptions` بـ `PngOptions` (أو فئة الخيارات المناسبة) في طريقة `save`.

**س: أين يمكنني العثور على دعم إضافي أو مساعدة؟**  
ج: للحصول على مساعدة المجتمع، زر [منتدى Aspose.PSD](https://forum.aspose.com/c/psd/34).

**س: هل هناك نسخة تجريبية مجانية متاحة؟**  
ج: نعم، يمكنك تجربة Aspose.PSD عبر [نسخة تجريبية مجانية](https://releases.aspose.com/).

**س: كيف أحصل على ترخيص مؤقت؟**  
ج: إذا كنت بحاجة إلى ترخيص مؤقت، يمكنك الحصول عليه [هنا](https://purchase.aspose.com/temporary-license/).

**س: هل يعمل هذا النهج على الخوادم بدون واجهة رسومية؟**  
ج: نعم، يعمل Aspose.PSD للـ Java في أي بيئة JVM قياسية، مما يجعله مثاليًا لأنابيب CI/CD أو وظائف السحابة.

## الخلاصة

لقد تعلمت الآن **how to rotate image** بزاوية 270 درجة باستخدام Aspose.PSD للـ Java، وكيفية **flip image** عند الحاجة، وكيفية تصدير النتيجة إلى JPEG. يمكن دمج سير العمل البسيط هذا في خطوط معالجة صور مبنية على Java أكبر، مما يمنحك تحكمًا كاملاً في تعديل ملفات PSD دون الاعتماد على Photoshop.

---

**آخر تحديث:** 2026-02-12  
**تم الاختبار مع:** Aspose.PSD for Java 24.12  
**المؤلف:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}