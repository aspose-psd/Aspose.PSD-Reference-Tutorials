---
date: 2026-02-20
description: تعلم كيفية تصدير ملفات PSD إلى PNG مع دعم قناع الطبقة باستخدام Aspose.PSD
  للـ Java – دليل خطوة بخطوة لتحويل الصور في Java.
linktitle: Export PSD to PNG with Layer Mask Support in Java
second_title: Aspose.PSD Java API
title: كيفية تصدير ملف PSD إلى PNG مع دعم قناع الطبقة في جافا
url: /ar/java/advanced-psd-layer-features-effects/support-layer-mask-psd-files/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# تصدير PSD إلى PNG مع دعم أقنعة الطبقة في Java

## المقدمة
إذا كنت تبحث عن **how to export PSD** ملفات إلى PNG مع الحفاظ على أقنعة الطبقة المعقدة، فقد وجدت المكان المناسب. عندما تحتاج إلى **export PSD to PNG** مع الحفاظ على تلك الأقنعة سليمة، يمكن لمكتبة Java موثوقة أن توفر لك ساعات من العمل اليدوي. في هذا الدرس سنستعرض العملية بالكامل باستخدام **Aspose.PSD Java API**، مع تغطية كل شيء من تحميل ملف PSD إلى حفظه كصورة PNG مع دعم كامل لقناة ألفا. سواءً كنت تبني أداة معالجة دفعات، أو خط أنابيب أصول مؤتمت، أو فقط تحتاج إلى سكريبت تحويل سريع، ستجد خطوات واضحة ومحادثة تجعل المهمة بسيطة.

## إجابات سريعة
- **What does “export PSD to PNG” mean?** تحويل ملف Photoshop PSD إلى صورة PNG نقطية مع الحفاظ على الدقة البصرية.  
- **Which library handles layer masks?** Aspose.PSD for Java يوفر دعمًا مدمجًا للأقنعة وقنوات ألفا.  
- **Do I need a license?** نسخة تجريبية مجانية تعمل للاختبار؛ تحتاج إلى ترخيص تجاري للاستخدام في الإنتاج.  
- **Can I run this on any OS?** نعم – API Java مستقل عن النظام الأساسي.  
- **How long does the conversion take?** عادةً أقل من ثانية للملفات ذات الحجم القياسي.

## كيفية تصدير PSD إلى PNG مع دعم أقنعة الطبقة
تصدير PSD إلى PNG أمر أساسي عندما تريد مشاركة أعمال Photoshop على الويب، أو تضمينها في التطبيقات، أو إنشاء صور مصغرة. PNG يحافظ على الشفافية، مما يجعله مثاليًا للأصول التي تتضمن أقنعة الطبقة. من خلال أتمتة التحويل باستخدام Java، تلغي خطوات التصدير اليدوية وتضمن نتائج متسقة عبر دفعات كبيرة.

## لماذا تستخدم Aspose.PSD Java لهذه المهمة؟
- **Full mask handling** – API يقرأ أقنعة PSD ويكتبها إلى قناة ألفا في PNG تلقائيًا.  
- **Java image conversion** – لا حاجة لأدوات خارجية؛ كل شيء يعمل داخل عملية Java الخاصة بك.  
- **Batch‑ready** – دمج الكود مع حلقة لتنفيذ تحويلات **batch PSD to PNG** خلال دقائق.  
- **Cross‑platform** – يعمل على Windows و macOS و Linux دون تبعيات محلية.

## المتطلبات المسبقة
قبل الغوص في الكود، تأكد من أن لديك ما يلي:

- **Java Development Kit (JDK)** – تحقق باستخدام `java -version`. حمّل من [Oracle's website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html) إذا لزم الأمر.  
- **Aspose.PSD library** – احصل على أحدث JAR من [download page](https://releases.aspose.com/psd/java/) أو أضفه عبر Maven/Gradle.  
- **IDE** – IntelliJ IDEA أو Eclipse أو أي محرر تفضله لتطوير Java.

### 1. بيئة تطوير Java
JDK حديث (11 أو أحدث) يضمن التوافق مع Aspose.PSD API.

### 2. مكتبة Aspose.PSD
المكتبة تتعامل مع **java image conversion**، وتحليل الأقنعة، وخيارات تصدير PNG.

### 3. IDE (بيئة التطوير المتكاملة)
استخدام IDE يبسط عملية تصحيح الأخطاء وإعداد المشروع.

## استيراد الحزم
أضف الاستيرادات المطلوبة إلى فئة Java الخاصة بك. هذه الفئات تسمح لك بتحميل ملفات PSD، والعمل مع الأقنعة، وتكوين إعدادات تصدير PNG.

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.PngOptions;
```

## دليل خطوة بخطوة

### الخطوة 1: إعداد دليل المشروع الخاص بك
حدد المجلد الذي يحتوي على ملف PSD المصدر وسيحفظ PNG الناتج.

```java
String dataDir = "Your Document Directory";
```

استبدل `Your Document Directory` بالمسار المطلق على جهازك.

### الخطوة 2: تحديد ملف PSD المصدر
أشر إلى ملف PSD الذي تريد تحويله. في هذا المثال نستخدم ملفًا يحتوي على قناع معقد.

```java
String sourceFileName = dataDir + "MaskComplex.psd";
```

### الخطوة 3: تحديد مسار تصدير PNG
أخبر البرنامج أين يكتب ملف PNG الناتج.

```java
String exportPath = dataDir + "MaskComplex.png";
```

### الخطوة 4: تحميل ملف PSD
هذه هي خطوة **how to load PSD**. طريقة `Image.load` تقرأ الملف إلى كائن `PsdImage`.

```java
PsdImage im = (PsdImage) Image.load(sourceFileName);
```

### الخطوة 5: إعداد خيارات تصدير PNG
قم بتكوين PNG للحفاظ على قناة ألفا، وهو أمر حاسم لشفافية قناع الطبقة.

```java
PngOptions saveOptions = new PngOptions();
saveOptions.setColorType(PngColorType.TruecolorWithAlpha);
```

### الخطوة 6: حفظ ملف PNG
أخيرًا، نفّذ عملية **convert PSD to PNG**.

```java
im.save(exportPath, saveOptions);
```

إذا تم إعداد كل شيء بشكل صحيح، ستجد `MaskComplex.png` في مجلد الإخراج، يعرض مناطق القناع الأصلية في PSD بشكل مثالي.

## المشكلات الشائعة والحلول
- **File‑not‑found errors** – تحقق مرة أخرى من `dataDir` وتأكد من أن اسم ملف PSD يطابق تمامًا، بما في ذلك حساسية الأحرف.  
- **Missing transparency** – تأكد من تطبيق `saveOptions.setColorType(PngColorType.TruecolorWithAlpha)`؛ وإلا سيُحفظ PNG بدون قناة ألفا.  
- **Out‑of‑memory for large files** – فكر في زيادة حجم ذاكرة JVM (`-Xmx2g`) عند معالجة ملفات PSD الكبيرة جدًا.  
- **Batch conversion tip** – ضع الخطوات السابقة داخل حلقة `for` تتكرر على قائمة بأسماء ملفات PSD لتحقيق معالجة **batch PSD to PNG**.

## الأسئلة المتكررة

**Q: What is a layer mask in PSD files?**  
A: قناع الطبقة يتحكم في شفافية الطبقة، مما يسمح لك بإخفاء أو إظهار أجزاء من الصورة دون مسح البكسلات بشكل دائم.

**Q: Can I work with PSD files without programming knowledge?**  
A: على الرغم من أن Aspose.PSD يتطلب كتابة كود، يمكن لمصممي الجرافيك استخدام Photoshop أو أدوات واجهة المستخدم الرسومية الأخرى للتحويل اليدوي.

**Q: Is Aspose.PSD free to use?**  
A: يتوفر نسخة تجريبية مجانية من صفحة التحميل؛ ويتطلب ترخيص مدفوع للمشاريع التجارية.

**Q: What happens if my PSD file contains no masks?**  
A: لا يزال التحويل يعمل؛ سيظهر PNG الناتج بدون تأثيرات شفافية القناع.

**Q: Where can I get support if I have issues?**  
A: قم بزيارة [support forum](https://forum.aspose.com/c/psd/34) للحصول على مساعدة من خبراء Aspose والمجتمع.

## الخلاصة
لقد تعلمت الآن **how to export PSD to PNG** مع الحفاظ على أقنعة الطبقة باستخدام Aspose.PSD Java API. هذا النهج يبسط **java image conversion**، يدعم المعالجة الدفعية، ويضمن أن أصولك البصرية تحتفظ بالشفافية المقصودة. لا تتردد في تجربة خيارات PNG المختلفة أو دمج هذا سير العمل في خطوط أنابيب أتمتة أكبر.

---

**آخر تحديث:** 2026-02-20  
**تم الاختبار مع:** Aspose.PSD for Java 24.12  
**المؤلف:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}