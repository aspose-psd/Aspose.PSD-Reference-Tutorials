---
title: قص PSD عند التحويل إلى PNG باستخدام Aspose.PSD لـ Java
linktitle: قص PSD عند التحويل إلى PNG
second_title: Aspose.PSD جافا API
description: تعرف على كيفية قص ملفات PSD وتحويلها إلى PNG باستخدام Aspose.PSD لـ Java. قم بتحسين تطبيقات Java الخاصة بك من خلال معالجة الصور بكفاءة.
weight: 13
url: /ar/java/psd-conversion/cropping-psd-converting-png/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# قص PSD عند التحويل إلى PNG باستخدام Aspose.PSD لـ Java

## مقدمة
في عالم تطوير Java الديناميكي، يعد إتقان المعالجة الفعالة للصور أمرًا بالغ الأهمية. سيرشدك هذا البرنامج التعليمي خلال عملية قص ملفات PSD عند تحويلها إلى PNG باستخدام مكتبة Aspose.PSD القوية لـ Java. بحلول نهاية هذا الدليل المفصّل خطوة بخطوة، ستكون مجهزًا بالمعرفة اللازمة لتحسين تطبيقات Java الخاصة بك من خلال معالجة سلسة للصور.
## المتطلبات الأساسية
قبل الغوص في البرنامج التعليمي، تأكد من توفر المتطلبات الأساسية التالية:
- المعرفة الأساسية ببرمجة جافا.
- تم تثبيت Java Development Kit (JDK) على نظامك.
- تم تنزيل Aspose.PSD لمكتبة Java وإضافتها إلى مشروعك.
- نموذج لملف PSD للتجربة.
## حزم الاستيراد
في مشروع Java الخاص بك، تأكد من استيراد الحزم اللازمة لاستخدام وظائف Aspose.PSD:
```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;
import com.aspose.psd.Rectangle;
import com.aspose.psd.imageoptions.PngOptions;
```
## الخطوة 1: قم بإعداد مشروعك
ابدأ بإنشاء مشروع Java وإضافة مكتبة Aspose.PSD لـ Java إلى مسار الفصل الخاص بمشروعك.
## الخطوة 2: تحميل صورة PSD
```java
String dataDir = "Your Document Directory";
String srcPath = dataDir + "sample.psd";
// قم بتحميل صورة PSD موجودة
RasterImage image = (RasterImage)Image.load(srcPath);
```
## الخطوة 3: تحديد منطقة المحاصيل
```java
// قم بإنشاء مثيل لفئة المستطيل عن طريق تمرير x وy والعرض والارتفاع
Rectangle cropRegion = new Rectangle(0, 0, 350, 450);
```
## الخطوة 4: قص صورة PSD
```java
// استدعاء طريقة الاقتصاص لفئة الصورة وتمرير مثيل المستطيل
image.crop(cropRegion);
```
## الخطوة 5: قم بتعيين خيارات تصدير PNG
```java
// قم بإنشاء مثيل لفئة PngOptions
PngOptions pngOptions = new PngOptions();
```
## الخطوة 6: حفظ الصورة التي تم اقتصاصها بصيغة PNG
```java
// قم بتوفير مسار الإخراج وPngOptions لتحويل ملف PSD إلى PNG وحفظ الإخراج
String destName = dataDir + "export.png";
image.save(destName, pngOptions);
```
## خاتمة
تهانينا! لقد تعلمت بنجاح كيفية قص ملفات PSD عند تحويلها إلى PNG باستخدام Aspose.PSD لـ Java. ستعمل هذه المهارة بلا شك على تعزيز قدرات معالجة الصور لديك في تطبيقات Java.
## الأسئلة المتداولة
### هل يمكنني قص ملفات PSD بأشكال غير منتظمة باستخدام Aspose.PSD لـ Java؟
نعم، يتيح لك Aspose.PSD for Java تحديد منطقة اقتصاص مخصصة، مما يتيح لك اقتصاص الصور إلى أشكال مختلفة.
### هل Aspose.PSD for Java مناسب لمهام معالجة الصور واسعة النطاق؟
قطعاً! تم تصميم Aspose.PSD للتعامل مع الصور الكبيرة بكفاءة، مما يجعله مثاليًا للمشاريع ذات متطلبات معالجة الصور الشاملة.
### هل أحتاج إلى ترخيص Aspose.PSD لـ Java؟
 نعم، مطلوب ترخيص ساري المفعول للاستخدام التجاري. يمكنك الحصول عليه من[Aspose الشراء](https://purchase.aspose.com/buy).
### كيف يمكنني طلب المساعدة أو الإبلاغ عن مشكلات تتعلق بـ Aspose.PSD لـ Java؟
 قم بزيارة[منتدى Aspose.PSD](https://forum.aspose.com/c/psd/34) لطلب المساعدة ومشاركة تجاربك والإبلاغ عن أي مشكلات تواجهك.
### هل يمكنني تجربة Aspose.PSD لـ Java قبل الشراء؟
 بالتأكيد! استكشف ميزات المكتبة من خلال النسخة التجريبية المجانية المتاحة[هنا](https://releases.aspose.com/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
