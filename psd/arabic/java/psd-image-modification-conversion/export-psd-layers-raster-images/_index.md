---
date: 2026-03-26
description: تعلم تصدير طبقات PSD إلى PNG باستخدام Aspose.PSD للغة Java. حوّل ملفات
  PSD إلى صور نقطية وقم بتصدير طبقات PSD دفعة واحدة بكفاءة.
linktitle: Export psd layers to png using Java
second_title: Aspose.PSD Java API
title: تصدير طبقات PSD إلى PNG باستخدام Java
url: /ar/java/psd-image-modification-conversion/export-psd-layers-raster-images/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# تصدير طبقات PSD إلى PNG باستخدام Java

## Introduction

في عالم التصميم الرقمي، يمكن أن يكون العمل مع الصور ذات الطبقات ميزة وتحديًا في آن واحد. تخيل أنك قضيت ساعات في إنشاء صورة رائعة في Photoshop (صيغة PSD)، مع طبقات متعددة تجلب التصميم إلى الحياة. الآن، قد ترغب في **تصدير طبقات PSD إلى PNG** بشكل مستقل للاستخدام لاحقًا. هنا يأتي دور Aspose.PSD for Java، حيث ي automatis عملية تحويل كل طبقة من ملف PSD إلى صور نقطية عالية الجودة مثل PNG. في هذا الدليل الشامل، سنرشدك خلال العملية بأكملها، من إعداد بيئتك إلى تصدير طبقات PSD دفعة واحدة ببضع أسطر من الشيفرة.

## Quick Answers
- **ما يغطي هذا الدرس؟** تصدير كل طبقة من PSD إلى ملف PNG باستخدام Aspose.PSD for Java.  
- **الفائدة الأساسية؟** يوفر ساعات مقارنةً بالاستخراج اليدوي في Photoshop.  
- **المتطلبات المسبقة؟** JDK 8+، مكتبة Aspose.PSD، وملف PSD تجريبي.  
- **هل يمكنني التصدير إلى صيغ نقطية أخرى؟** نعم – يمكنك أيضًا تحويل PSD إلى صيغ نقطية مثل BMP أو TIFF أو JPEG.  
- **هل يدعم المعالجة الدفعية؟** بالتأكيد؛ الحلقة في الشيفرة تتيح لك تصدير طبقات PSD دفعة واحدة في تشغيل واحد.

## What is “psd layers to png”?

تصدير **psd layers to png** يعني أخذ كل طبقة منفصلة من مستند Photoshop وحفظها كصورة PNG مستقلة. تحتفظ PNG بالشفافية، مما يجعلها مثالية للرسومات الويب، وأصول واجهة المستخدم، ومعالجة الصور الإضافية.

## Why use Aspose.PSD for Java?
- **لا حاجة لبرنامج Photoshop** – يعمل على أي خادم أو بيئة تكامل مستمر.  
- **دقة عالية** – يحتفظ بتأثيرات الطبقات، الأقنعة، وقنوات ألفا.  
- **قابل للتوسع** – مثالي لتصدير طبقات PSD دفعةً في خطوط الأنابيب الآلية.  

## Prerequisites

قبل الغوص في الشيفرة، تأكد من أن لديك ما يلي:

1. **Java Development Kit (JDK)** – الإصدار 8 أو أعلى.  
2. **Aspose.PSD for Java** – قم بتنزيل أحدث مكتبة من [Aspose Releases](https://releases.aspose.com/psd/java/).  
3. **IDE** – IntelliJ IDEA أو Eclipse أو أي محرر تفضله.  
4. **Sample PSD file** – مثال: `sample.psd`، وضعه في مجلد المشروع الخاص بك.

الآن بعد أن أصبحت جاهزًا، لنبدأ بالبرمجة!

## Import Packages

أولاً، استورد الفئات التي ستحتاجها من مكتبة Aspose.PSD:

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.PngOptions;
```

هذه الاستيرادات تمنحك إمكانية تحميل الصور، خيارات PNG، ومعالجة الطبقات.

## Step 1: Define Your Document Directory

الخطوة 1: تحديد دليل المستند الخاص بك

حدد مكان وجود ملف PSD المصدر وملفات PNG الناتجة:

```java
String dataDir = "Your Document Directory";
```

استبدل `"Your Document Directory"` بالمسار المطلق أو النسبي إلى `sample.psd`.

## Step 2: Load the PSD File

الخطوة 2: تحميل ملف PSD

حمّل ملف PSD في كائن `PsdImage` لتتمكن من العمل مع طبقاته:

```java
PsdImage psdImage = (PsdImage) Image.load(dataDir + "sample.psd");
```

التحويل إلى `PsdImage` يفتح وظائف خاصة بالطبقات.

## Step 3: Configure PNG Options

الخطوة 3: تكوين خيارات PNG

قم بإعداد معلمات تصدير PNG. استخدام `TruecolorWithAlpha` يحافظ على الشفافية.

```java
PngOptions pngOptions = new PngOptions();
pngOptions.setColorType(PngColorType.TruecolorWithAlpha);
```

## Step 4: Loop Through Layers and Export Each One

الخطوة 4: التكرار عبر الطبقات وتصدير كل واحدة

تكرار عبر كل طبقة وحفظها كملف PNG منفصل. هذه الحلقة تمكّن **batch export psd layers** تلقائيًا:

```java
for (int i = 0; i < psdImage.getLayers().length; i++) {
    // Convert and save the layer to PNG file format.
    psdImage.getLayers()[i].save(dataDir + String.format("layer_out%d.png", i + 1), pngOptions);
}
```

كل تكرار ينتج `layer_out1.png`، `layer_out2.png`، وهكذا.

## Common Issues and Solutions

مشكلات شائعة وحلولها

- **FileNotFoundException** – تحقق من أن `dataDir` يشير إلى المجلد الصحيح وأن `sample.psd` موجود.  
- **OutOfMemoryError** – بالنسبة لملفات PSD الكبيرة جدًا، فكر في معالجة الطبقات على دفعات أصغر أو زيادة حجم الذاكرة المخصصة للـ JVM (`-Xmx`).  
- **Missing Transparency** – تأكد من ضبط `pngOptions.setColorType(PngColorType.TruecolorWithAlpha)`؛ وإلا سيتم حفظ PNG بدون قناة ألفا.

## Frequently Asked Questions

### ما هو Aspose.PSD for Java؟

Aspose.PSD for Java هي مكتبة قوية تمكّن المطورين من إنشاء، تعديل، تحويل، وعرض ملفات Photoshop دون الحاجة إلى Adobe Photoshop.

### هل يمكنني تصدير الطبقات إلى صيغ غير PNG؟

نعم، يدعم Aspose.PSD صيغ BMP، TIFF، JPEG، والعديد من الصيغ النقطية الأخرى. ما عليك سوى إنشاء كائن من فئة الخيارات المقابلة (مثل `JpegOptions`) وتمريره إلى طريقة `save`.

### هل هناك نسخة تجريبية مجانية متاحة لـ Aspose.PSD؟

بالطبع! يمكنك تجربة Aspose.PSD مجانًا بتحميله من [صفحة التجربة المجانية](https://releases.aspose.com/).

### ماذا أفعل إذا واجهت مشكلات أثناء استخدام Aspose.PSD؟

يمكنك طلب المساعدة والدعم من مجتمع Aspose. زر منتديات الدعم الخاصة بهم [هنا](https://forum.aspose.com/c/psd/34).

### أين يمكنني شراء ترخيص لـ Aspose.PSD؟

يمكنك بسهولة شراء ترخيص لـ Aspose.PSD من صفحة الشراء الخاصة بهم [هنا](https://purchase.aspose.com/buy).

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Last Updated:** 2026-03-26  
**Tested With:** Aspose.PSD for Java 24.12 (latest)  
**Author:** Aspose