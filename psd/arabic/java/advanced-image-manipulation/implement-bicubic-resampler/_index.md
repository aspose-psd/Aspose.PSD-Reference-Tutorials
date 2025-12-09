---
date: 2025-12-01
description: تعلم كيفية تحقيق تحجيم صور عالي الجودة في Java باستخدام أداة Bicubic
  Resampler من Aspose.PSD. اتبع دليلنا خطوة بخطوة للحصول على نتائج متميزة.
linktitle: Implement Bicubic Resampler
second_title: Aspose.PSD Java API
title: تحجيم الصور بجودة عالية باستخدام مُعيد التحجيم البيكوبيك في Aspose.PSD للـ
  Java
url: /ar/java/advanced-image-manipulation/implement-bicubic-resampler/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# تحجيم الصور عالي الجودة باستخدام مُعيد التحجيم البيكوبيك في Aspose.PSD للغة Java

## المقدمة

تحجيم الصور عالي الجودة هو طلب شائع عندما تحتاج إلى تغيير حجم الرسومات دون التضحية بالدقة البصرية. يقدم Aspose.PSD للغة Java **مُعيد التحجيم البيكوبيك** الذي يوفر نتائج ناعمة وواضحة لملفات PSD وغيرها من الصيغ المدعومة. في هذا البرنامج التعليمي ستتعلم بالضبط كيفية تنفيذ مُعيد التحجيم البيكوبيك، خطوة بخطوة، لتتمكن من إضافة تحجيم صور عالي الجودة إلى تطبيقات Java الخاصة بك اليوم.

## إجابات سريعة
- **ماذا يفعل مُعيد التحجيم البيكوبيك؟** يطبق خوارزمية استيفاء متقدمة تحافظ على التفاصيل عند تغيير حجم الصور.  
- **ما هي قيم ResizeType المتاحة؟** `CubicConvolution` و `Bell` هما الخياران البيكوبيكان المتوفران في Aspose.PSD.  
- **هل أحتاج إلى ترخيص لتشغيل الكود؟** الترخيص المؤقت يكفي للتقييم؛ الترخيص الكامل مطلوب للإنتاج.  
- **ما نسخة Java المطلوبة؟** أي بيئة تشغيل Java 8+ متوافقة مع أحدث مكتبة Aspose.PSD.  
- **هل يمكنني تحجيم صيغ أخرى (PNG، JPEG) باستخدام نفس الـ API؟** نعم، يدعم Aspose.PSD عدة صيغ صور، رغم أن الأمثلة تركز على PSD.

## ما هو تحجيم الصور عالي الجودة؟

تحجيم الصور عالي الجودة يعني تغيير حجم الصورة مع الحفاظ على الحواف الحادة، التدرجات السلسة، وتمثيل الألوان الدقيق. يحقق مُعيد التحجيم البيكوبيك ذلك من خلال أخذ قيم البكسلات المجاورة في الاعتبار (باستخدام Cubic Convolution أو خوارزمية Bell) لحساب كل بكسل جديد، مما ينتج مظهرًا أكثر طبيعية مقارنةً بطرق الجار الأقرب أو Bilinear.

## لماذا نستخدم مُعيد التحجيم البيكوبيك لتحجيم الصور عالي الجودة؟

- **يحافظ على التفاصيل:** القوام الدقيقة والخطوط تظل واضحة حتى بعد تغييرات حجم كبيرة.  
- **يقلل التشويهات:** يقلل من الظواهر مثل الـ ringing والتمويه التي تظهر غالبًا مع الخوارزميات الأبسط.  
- **تكامل سهل:** استدعاء طريقة سطر واحد (`image.resize`) يتيح لك التبديل بين الخوارزميات دون إعادة كتابة الكود.  

## المتطلبات المسبقة

قبل البدء، تأكد من وجود ما يلي:

- **Aspose.PSD للغة Java** – قم بتحميل أحدث ملف JAR من [توثيق Aspose.PSD للغة Java](https://reference.aspose.com/psd/java/).  
- **مجموعة تطوير Java** – JDK 8 أو أحدث مثبت ومُعد.  
- **ملف PSD تجريبي** – صورة اختبار (مثال: `sample_bicubic.psd`) موجودة في دليل معروف.

## استيراد الحزم

أضف الاستيرادات المطلوبة إلى فئة Java الخاصة بك. هذه الاستيرادات تجلب الفئات الأساسية من Aspose.PSD وتعداد `ResizeType`.

```java
import com.aspose.psd.Image;
import com.aspose.psd.ResizeType;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.PsdOptions;
```

## الخطوة 1: تحميل الصورة

أولاً، قم بتحميل ملف PSD المصدر الذي تريد تحجيمه. استبدل `Your Document Directory` بالمسار الفعلي على جهازك.

```java
String dataDir = "Your Document Directory";
String filePath = dataDir + "sample_bicubic.psd";
PsdImage image = (PsdImage)Image.load(filePath);
```

## الخطوة 2: التحجيم باستخدام Cubic Convolution (جودة عالية)

الآن طبّق خوارزمية **Cubic Convolution**، أحد الخيارين البيكوبيكان الذين يوفران تحجيم صور عالي الجودة. المثال يغيّر حجم الصورة إلى 300 × 300 بكسل.

```java
String destNameCubicConvolution = dataDir + "ResamplerCubicConvolutionStripes_after.psd";
image.resize(300, 300, ResizeType.CubicConvolution);
image.save(destNameCubicConvolution, new PsdOptions(image));
```

## الخطوة 3: التحجيم باستخدام خوارزمية Bell (جودة عالية بديلة)

إذا كنت تفضّل خوارزمية **Bell**، التي تقدم تأثير تنعيم مختلف قليلاً، يمكنك استخدامها بنفس الطريقة. لاحظ أننا نعيد تحميل الصورة الأصلية للحفاظ على مقارنة عادلة.

```java
String destNameBell = dataDir + "ResamplerBellStripes_after.psd";
PsdImage imageBellStripes = (PsdImage)Image.load(filePath);
imageBellStripes.resize(300, 300, ResizeType.Bell);
imageBellStripes.save(destNameBell, new PsdOptions(imageBellStripes));
```

لا تتردد في تجربة أبعاد أو صيغ ملفات أخرى—فقط عدّل المعلمات وفقًا لذلك.

## المشكلات الشائعة والنصائح

- **مسار غير صحيح:** تأكد من أن `dataDir` ينتهي بفاصل ملفات (`/` أو `\`) المناسب لنظام التشغيل الخاص بك.  
- **استثناءات الترخيص:** تشغيل البرنامج بدون ترخيص صالح قد يضيف علامة مائية إلى الصورة الناتجة.  
- **استخدام الذاكرة:** ملفات PSD الكبيرة قد تستهلك ذاكرة كبيرة؛ فكر في تحرير الصور (`image.dispose()`) بعد الحفظ.  

## الأسئلة المتكررة

**س: هل يمكنني استخدام Aspose.PSD للغة Java مع صيغ صور أخرى؟**  
ج: نعم، تدعم المكتبة PSD، PNG، JPEG، TIFF، BMP، والعديد غيرها.

**س: هل تتوفر ترخيص مؤقت لـ Aspose.PSD للغة Java؟**  
ج: نعم، يمكنك الحصول على ترخيص مؤقت من [هنا](https://purchase.aspose.com/temporary-license/).

**س: أين يمكنني العثور على الدعم لـ Aspose.PSD للغة Java؟**  
ج: زر منتدى Aspose.PSD [هنا](https://forum.aspose.com/c/psd/34) لأي استفسارات تتعلق بالدعم.

**س: هل يمكنني تحميل مكتبة Aspose.PSD للغة Java؟**  
ج: نعم، حمّل المكتبة من صفحة الإصدارات [هنا](https://releases.aspose.com/psd/java/).

**س: كيف يمكنني شراء Aspose.PSD للغة Java؟**  
ج: يمكنك شراء Aspose.PSD للغة Java من صفحة الشراء [هنا](https://purchase.aspose.com/buy).

---

**آخر تحديث:** 2025-12-01  
**تم الاختبار مع:** Aspose.PSD للغة Java 24.11 (أحدث نسخة وقت الكتابة)  
**المؤلف:** Aspose

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}