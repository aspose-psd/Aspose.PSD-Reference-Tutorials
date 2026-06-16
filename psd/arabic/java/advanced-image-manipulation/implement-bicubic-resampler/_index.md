---
date: 2026-04-12
description: تعلم كيفية تغيير حجم الصورة في Java باستخدام أداة Bicubic Resampler من
  Aspose.PSD. يوضح هذا الدرس لتكبير الصورة خطوة بخطوة كيفية تحقيق نتائج متفوقة.
keywords:
- resize image java
- image scaling tutorial
- java image library
linktitle: تنفيذ مُعيد العينة البيكوبيكي
second_title: Aspose.PSD Java API
title: تغيير حجم الصورة في جافا – مُعيد التحجيم البيكوبيك لتكبير عالي الجودة
url: /ar/java/advanced-image-manipulation/implement-bicubic-resampler/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# تحجيم الصورة جافا – أداة إعادة التحجيم البيكوبيك لتقليل الحجم بجودة عالية

## مقدمة

إذا كنت بحاجة إلى **resize image java** المشاريع دون فقدان الحدة أو إدخال عيوب، فقد وصلت إلى المكان الصحيح. في هذا **image scaling tutorial** سنستعرض كيفية استخدام Bicubic Resampler من Aspose.PSD — ميزة قوية في **java image library** توفر نتائج ناعمة وواضحة لملفات PSD والعديد من الصيغ الأخرى. بنهاية هذا الدليل ستكون قادرًا على دمج التحجيم عالي الجودة في أي تطبيق Java ببضع أسطر من الشيفرة.

## إجابات سريعة
- **What does the Bicubic Resampler do?** يطبق خوارزمية استيفاء متقدمة تحافظ على التفاصيل عند تحجيم الصور.  
- **Which ResizeType values are available?** `CubicConvolution` و `Bell` هما خيارا البيكوبيك المتاحان من Aspose.PSD.  
- **Do I need a license to run the code?** ترخيص مؤقت من Aspose يعمل للتقييم؛ يتطلب الترخيص الكامل للإنتاج.  
- **What Java version is required?** أي بيئة تشغيل Java 8+ متوافقة مع أحدث مكتبة Aspose.PSD.  
- **Can I resize other formats (PNG, JPEG) with the same API?** نعم، يدعم Aspose.PSD أنواعًا متعددة من الصور، رغم أن الأمثلة تركز على PSD.

## ما هو التحجيم عالي الجودة للصور؟

يشير التحجيم عالي الجودة للصور إلى تغيير حجم الصورة مع الحفاظ على الحواف الحادة، التدرجات السلسة، وتمثيل الألوان الدقيق. يحقق Bicubic Resampler ذلك من خلال مراعاة قيم البكسلات المجاورة (باستخدام cubic convolution أو خوارزمية Bell) لحساب كل بكسل جديد، مما ينتج مظهرًا أكثر طبيعية مقارنةً بأساليب أقرب جار أو ثنائي الخطية.

## لماذا نستخدم Bicubic Resampler للتحجيم عالي الجودة للصور؟

- **Preserves Detail:** القوام الدقيقة وعمل الخط تبقى واضحة حتى بعد تغييرات حجم كبيرة.  
- **Reduces Artifacts:** يقلل من حدوث الهالات والطمس التي تظهر غالبًا مع الخوارزميات الأبسط.  
- **Easy Integration:** استدعاء طريقة سطر واحد (`image.resize`) يتيح لك التبديل بين الخوارزميات دون إعادة كتابة الشيفرة.  

## المتطلبات المسبقة

قبل البدء، تأكد من وجود ما يلي:

- **Aspose.PSD for Java** – قم بتنزيل أحدث ملف JAR من [Aspose.PSD for Java documentation](https://reference.aspose.com/psd/java/).  
- **Java Development Kit** – JDK 8 أو أحدث مثبت ومُعد.  
- **Sample PSD file** – صورة اختبار (مثال: `sample_bicubic.psd`) موجودة في دليل معروف.  

تشكل هذه العناصر معًا أساسًا قويًا لـ **java image library** للدرس.

## استيراد الحزم

أضف الاستيرادات المطلوبة إلى فئة Java الخاصة بك. هذه تجلب الفئات الأساسية من Aspose.PSD وتعداد `ResizeType`.

```java
import com.aspose.psd.Image;
import com.aspose.psd.ResizeType;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.PsdOptions;
```

## كيفية تحجيم الصورة جافا باستخدام Bicubic Resampler

### الخطوة 1: تحميل الصورة

أولاً، قم بتحميل ملف PSD المصدر الذي تريد تحجيمه. استبدل `Your Document Directory` بالمسار الفعلي على جهازك.

```java
String dataDir = "Your Document Directory";
String filePath = dataDir + "sample_bicubic.psd";
PsdImage image = (PsdImage)Image.load(filePath);
```

### الخطوة 2: التحجيم باستخدام Cubic Convolution (جودة عالية)

الآن طبق خوارزمية **Cubic Convolution**، أحد خيارين Bicubic التي توفر تحجيمًا عالي الجودة للصور. المثال يحجم الصورة إلى 300 × 300 بكسل.

```java
String destNameCubicConvolution = dataDir + "ResamplerCubicConvolutionStripes_after.psd";
image.resize(300, 300, ResizeType.CubicConvolution);
image.save(destNameCubicConvolution, new PsdOptions(image));
```

### الخطوة 3: التحجيم باستخدام خوارزمية Bell (جودة عالية بديلة)

إذا كنت تفضل خوارزمية **Bell**، التي تقدم تأثير تنعيم مختلف قليلاً، يمكنك استخدامها بنفس الطريقة. لاحظ أننا نعيد تحميل الصورة الأصلية للحفاظ على مقارنة عادلة.

```java
String destNameBell = dataDir + "ResamplerBellStripes_after.psd";
PsdImage imageBellStripes = (PsdImage)Image.load(filePath);
imageBellStripes.resize(300, 300, ResizeType.Bell);
imageBellStripes.save(destNameBell, new PsdOptions(imageBellStripes));
```

لا تتردد في تجربة أبعاد أو صيغ ملفات أخرى—فقط قم بضبط المعلمات وفقًا لذلك.

## الأخطاء الشائعة والنصائح

- **Incorrect Path:** تأكد من أن `dataDir` ينتهي بفاصل ملف (`/` أو `\`) المناسب لنظام التشغيل الخاص بك.  
- **License Exceptions:** تشغيل البرنامج بدون ترخيص صالح قد يضيف علامة مائية إلى الصورة الناتجة. استخدم **temporary aspose license** للاختبار، ثم انتقل إلى ترخيص دائم للإنتاج.  
- **Memory Usage:** ملفات PSD الكبيرة قد تستهلك ذاكرة كبيرة؛ فكر في تحرير الصور (`image.dispose()`) بعد الحفظ.  

## الأسئلة المتكررة

**Q: Can I use Aspose.PSD for Java with other image formats?**  
A: نعم، تدعم المكتبة صيغ PSD، PNG، JPEG، TIFF، BMP، والعديد غيرها.

**Q: Is a temporary license available for Aspose.PSD for Java?**  
A: نعم، يمكنك الحصول على ترخيص مؤقت من [here](https://purchase.aspose.com/temporary-license/).

**Q: Where can I find support for Aspose.PSD for Java?**  
A: زر منتدى Aspose.PSD [here](https://forum.aspose.com/c/psd/34) لأي استفسارات تتعلق بالدعم.

**Q: Can I download the Aspose.PSD for Java library?**  
A: نعم، قم بتنزيل المكتبة من صفحة الإصدارات [here](https://releases.aspose.com/psd/java/).

**Q: How do I purchase Aspose.PSD for Java?**  
A: يمكنك شراء Aspose.PSD for Java من صفحة الشراء [here](https://purchase.aspose.com/buy).

---

**آخر تحديث:** 2026-04-12  
**تم الاختبار باستخدام:** Aspose.PSD for Java 24.11 (latest at time of writing)  
**المؤلف:** Aspose

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}