---
date: 2026-05-29
description: تعلم كيفية حفظ ملف PSD كـ PNG مع نص ملون باستخدام Aspose.PSD for Java.
  يوضح هذا الدليل خطوة بخطوة كيفية تحويل PSD إلى PNG بكفاءة.
keywords:
- save psd as png
- convert psd to png
- Aspose.PSD Java
linktitle: عرض النص بألوان مختلفة في طبقة النص
schemas:
- author: Aspose
  dateModified: '2026-05-29'
  description: Learn how to save PSD as PNG with colored text using Aspose.PSD for
    Java. This step‑by‑step guide shows how to convert PSD to PNG efficiently.
  headline: Save PSD as PNG with Colored Text using Aspose.PSD for Java
  type: TechArticle
- questions:
  - answer: Aspose.PSD is primarily designed for Java, but Aspose provides similar
      libraries for various programming languages.
    question: Can I use Aspose.PSD for Java with other programming languages?
  - answer: Yes, you can obtain a free trial version from [Aspose.PSD](https://releases.aspose.com/).
    question: Is there a trial version available for Aspose.PSD for Java?
  - answer: Visit the [Aspose.PSD forum](https://forum.aspose.com/c/psd/34) for community
      support and discussions.
    question: Where can I find additional support or assistance?
  - answer: You can request a temporary license from [Aspose.PSD](https://purchase.aspose.com/temporary-license/).
    question: How can I obtain a temporary license for Aspose.PSD for Java?
  - answer: Yes, explore the [Aspose.PSD documentation](https://reference.aspose.com/psd/java/)
      for more tutorials and examples.
    question: Are there other tutorials available for Aspose.PSD?
  type: FAQPage
second_title: Aspose.PSD Java API
title: حفظ ملف PSD كـ PNG مع نص ملون باستخدام Aspose.PSD for Java
url: /ar/java/advanced-techniques/render-text-different-colors/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# حفظ PSD كـ PNG مع نص ملون باستخدام Aspose.PSD للـ Java

مرحبًا بكم في دليلنا خطوة بخطوة حول كيفية **حفظ PSD كـ PNG** بنص ملون بألوان مختلفة باستخدام Aspose.PSD للـ Java. Aspose.PSD هي مكتبة Java قوية تتيح لك التعامل مع ملفات Photoshop برمجيًا، وتوفر لك إمكانيات واسعة للعمل مع صيغ ملفات PSD و PSB.

في هذا البرنامج التعليمي، سنرشدك خلال عملية تصيير النص بألوان مختلفة في طبقة النص باستخدام Aspose.PSD. بحلول نهاية هذا الدليل، ستحصل على فهم واضح لكيفية إنجاز هذه المهمة بسلاسة.

## إجابات سريعة
- **كيف يمكن حفظ PSD كـ PNG؟** استخدم فئة `PsdImage` في Aspose.PSD لتحميل ملف PSD واستدعاء `save` مع `PngOptions`.
- **هل يمكنني تصيير ألوان متعددة في طبقة نص واحدة؟** نعم، قم بتعيين كائنات `Color` مختلفة لكل `Portion` من النص.
- **ما نسخة Java المطلوبة؟** تدعم Java 8 أو أعلى.
- **هل أحتاج إلى ترخيص للإنتاج؟** يلزم الحصول على ترخيص تجاري؛ يتوفر نسخة تجريبية مجانية.
- **هل المكتبة فعّالة في استهلاك الذاكرة للملفات الكبيرة؟** يمكنها معالجة ملفات تصل إلى 2 GB دون تحميل كامل في الذاكرة.

## كيفية حفظ PSD كـ PNG مع نص ملون؟

حمّل ملف PSD الخاص بك، عدّل أجزاء طبقة النص لتعيين ألوان مميزة، ثم احفظ الصورة كـ PNG—كل هذه العملية تُنفّذ ببضع أسطر فقط من كود Java. يقوم Aspose.PSD تلقائيًا بتحويل الطبقة المعدلة إلى نقطية، مع الحفاظ على الشفافية ودقة الألوان، بحيث يتطابق PNG الناتج مع التصميم الأصلي.

## ما هو Aspose.PSD للـ Java؟

Aspose.PSD للـ Java هي مكتبة تمكّن من إنشاء وتحرير وتحويل ملفات Photoshop (PSD/PSB) برمجيًا. تدعم **أكثر من 50 صيغة صورة** ويمكنها معالجة مستندات مئات الصفحات دون تحميل الملف بالكامل إلى الذاكرة، مما يوفّر أداءً عاليًا لأتمتة الخوادم.

## المتطلبات المسبقة

- معرفة أساسية ببرمجة Java.
- مكتبة Aspose.PSD للـ Java مثبتة. يمكنك تنزيلها من [توثيق Aspose.PSD للـ Java](https://reference.aspose.com/psd/java/).

## استيراد الحزم

`Image` هي الفئة الأساسية لتحميل وحفظ ملفات الصور. `PsdImage` تمثل مستند Photoshop، بينما `TextLayer` توفر الوصول إلى خصائص طبقة النص. `PngOptions` يحدد إعدادات تصدير PNG.  
```java
import com.aspose.psd.Image;

import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.TextLayer;
import com.aspose.psd.imageoptions.PngOptions;
```

## الخطوة 1: إعداد مشروعك

أنشئ مشروع Java جديدًا وقم بإضافة مكتبة Aspose.PSD. تأكد من أن لديك الأذونات اللازمة للوصول إلى الملفات وتعديلها في دليل المشروع.

## الخطوة 2: تحديد مجلدات المصدر والإخراج

حدد مجلدات المصدر والإخراج حيث توجد ملفات PSD الخاصة بك وحيث سيتم حفظ الصور الناتجة. قم بتحديث المتغيرين `sourceDir` و `outputDir` وفقًا لذلك.  
```java
String sourceDir = "Your Document Directory";
String outputDir = "Your Document Directory";
```

## الخطوة 3: تحميل ملف PSD والوصول إلى طبقة النص

`PsdImage` يحمل ملف PSD إلى الذاكرة، و`TextLayer` يسمح بالتلاعب بمحتوى النص داخل تلك الطبقة.  
```java
String targetFilePath = sourceDir + "text_ethalon_different_colors.psd";
String resultFilePath = outputDir + "RenderTextWithDifferentColorsInTextLayer_out.png";

PsdImage psdImage = null;
try
{
    psdImage = (PsdImage) Image.load(targetFilePath);
    TextLayer txtLayer = (TextLayer)psdImage.getLayers()[1];
    txtLayer.getTextData().updateLayerData();
```

## الخطوة 4: ضبط خيارات PNG وحفظ الصورة الناتجة

`PngOptions` يضبط معلمات إخراج PNG مثل نوع اللون والضغط.  
```java
    PngOptions pngOptions = new PngOptions();
    pngOptions.setColorType(PngColorType.TruecolorWithAlpha);
    psdImage.save(resultFilePath, pngOptions);
}
finally
{
    if (psdImage != null) psdImage.dispose();
}
```

## المشكلات الشائعة والحلول

- **استثناء الترخيص المفقود:** تأكد من تطبيق ملف ترخيص صالح قبل استدعاء أي عملية حفظ.
- **عدم تطبيق اللون:** تحقق من أن كل `Portion` في طبقة النص لديه خاصية `Color` مضبوطة بشكل صحيح.
- **استخدام الذاكرة للملفات الكبيرة:** استخدم التحميل الزائد `load` في `PsdImage` مع `loadOptions` لتدفق الملفات الكبيرة.

## الأسئلة المتكررة

**س: هل يمكنني استخدام Aspose.PSD للـ Java مع لغات برمجة أخرى؟**  
ج: تم تصميم Aspose.PSD أساسًا لـ Java، لكن Aspose توفر مكتبات مشابهة لمختلف لغات البرمجة.

**س: هل تتوفر نسخة تجريبية من Aspose.PSD للـ Java؟**  
ج: نعم، يمكنك الحصول على نسخة تجريبية مجانية من [Aspose.PSD](https://releases.aspose.com/).

**س: أين يمكنني العثور على دعم أو مساعدة إضافية؟**  
ج: زر [منتدى Aspose.PSD](https://forum.aspose.com/c/psd/34) للحصول على دعم المجتمع والنقاشات.

**س: كيف يمكنني الحصول على ترخيص مؤقت لـ Aspose.PSD للـ Java؟**  
ج: يمكنك طلب ترخيص مؤقت من [Aspose.PSD](https://purchase.aspose.com/temporary-license/).

**س: هل توجد دروس أخرى متاحة لـ Aspose.PSD؟**  
ج: نعم، استكشف [توثيق Aspose.PSD](https://reference.aspose.com/psd/java/) للمزيد من الدروس والأمثلة.

**س: هل تدعم المكتبة التحويل الجماعي لعدة ملفات PSD إلى PNG؟**  
ج: نعم، يمكنك التكرار على مجلد من ملفات PSD، وتطبيق نفس منطق لون النص، وحفظ كل ملف كـ PNG باستخدام حلقة.

**س: هل PNG الناتج غير مضغوط (lossless)؟**  
ج: PNG المحفوظ عبر Aspose.PSD يحتفظ بجودة غير مضغوطة بالكامل، مع الحفاظ على جميع معلومات اللون والشفافية.

---

**آخر تحديث:** 2026-05-29  
**تم الاختبار مع:** Aspose.PSD 24.12 للـ Java  
**المؤلف:** Aspose

{{< blocks/products/products-backtop-button >}}

## دروس ذات صلة

- [تصدير PSD إلى PNG وإضافة طبقة عادية جديدة باستخدام Aspose.PSD للـ Java](/psd/java/advanced-image-effects/add-new-regular-layer/)
- [حفظ PSD كـ PNG وتطبيق ظل إسقاط في Aspose.PSD للـ Java](/psd/java/advanced-image-manipulation/rendering-drop-shadow/)
- [تحويل PSD إلى PNG مع تراكب لون – Aspose.PSD للـ Java](/psd/java/advanced-image-manipulation/rendering-color-effect/)

{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}