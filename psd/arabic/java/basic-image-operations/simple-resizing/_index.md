---
date: 2025-12-27
description: تعلم كيفية تغيير حجم الصورة في Java باستخدام مكتبة معالجة الصور. اتبع
  دليلنا خطوة بخطوة مع Aspose.PSD for Java لمعالجة الصور بكفاءة.
linktitle: Perform Simple Resizing
second_title: Aspose.PSD Java API
title: تغيير حجم بسيط باستخدام Aspose.PSD – مكتبة جافا لمعالجة الصور
url: /ar/java/basic-image-operations/simple-resizing/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# تغيير حجم بسيط باستخدام Aspose.PSD – مكتبة معالجة الصور لجافا

## المقدمة

إذا كنت مطور Java تبحث عن **java image manipulation library** موثوقة، فقد وجدت المكان المناسب. في هذا الدرس سنستعرض **how to resize image java** باستخدام Aspose.PSD for Java – مكتبة قوية تجعل معالجة الصور سريعة ومباشرة. بنهاية هذا الدليل ستحصل على مثال واضح وجاهز للإنتاج يمكنك إدراجه في أي تطبيق Java.

## إجابات سريعة
- **ما المكتبة المستخدمة؟** Aspose.PSD for Java, a leading java image manipulation library.  
- **هل يمكنني تغيير حجم أي PSD؟** Yes – the library supports PSD, JPEG, PNG, and more.  
- **كيف تحدد الحجم؟** Call `image.resize(width, height)` with the desired pixel dimensions.  
- **هل أحتاج إلى ترخيص؟** A free trial works for development; a license is required for production.  
- **ما إصدار Java المطلوب؟** Java 8 or higher.

## ما هي مكتبة معالجة الصور لجافا؟

توفر **java image manipulation library** وصولًا برمجيًا إلى عمليات الرسومات الشائعة — تغيير الحجم، القص، تحويل الصيغ، وإدارة الطبقات — دون الاعتماد على أدوات خارجية. تقدم Aspose.PSD هذه القدرات لمطوري Java، مما يتيح لك العمل مباشرةً مع ملفات PSD وتصديرها إلى الصيغ الشائعة.

## لماذا تستخدم Aspose.PSD لتغيير الحجم البسيط؟

- **Performance‑optimized** خوارزميات تتعامل مع ملفات PSD الكبيرة بكفاءة.  
- **No external dependencies** – pure Java, perfect for server‑side processing.  
- **Rich format support** – beyond PSD you can output JPEG, PNG, TIFF, etc.  
- **Consistent API** – the same methods work across all supported image types.

## المتطلبات المسبقة

قبل أن نبدأ، تأكد من أن لديك ما يلي:

1. **Java Development Kit (JDK)** – download the latest version from the [Java website](https://www.oracle.com/java/).  
2. **Aspose.PSD for Java** – obtain the library from the [Aspose.PSD for Java download page](https://releases.aspose.com/psd/java/).  

وجود هذه العناصر يضمن إعدادًا سلسًا لمثال تغيير الحجم.

## استيراد الحزم

ابدأ باستيراد الفئات الضرورية. ضع هذه الاستيرادات في أعلى ملف المصدر Java الخاص بك:

```java
import com.aspose.psd.Image;
import com.aspose.psd.imageoptions.JpegOptions;
```

تتيح لك هذه الاستيرادات الوصول إلى الفئة الأساسية `Image` وخيارات تصدير JPEG.

## دليل خطوة بخطوة

### الخطوة 1: تعيين دليل المستند الخاص بك

حدد المجلد الذي يحتوي على ملف PSD المصدر. استبدل العنصر النائب بالمسار الفعلي الخاص بك.

```java
String dataDir = "Your Document Directory";
```

### الخطوة 2: تحديد مسارات المصدر والوجهة

أنشئ أسماء ملفات كاملة لملف PSD المدخل وملف JPEG الناتج.

```java
String sourceFile = dataDir + "sample.psd";
String destName = dataDir + "SimpleResizing_out.jpg";
```

### الخطوة 3: تحميل الصورة

حمّل ملف PSD في كائن `Image`.

```java
Image image = Image.load(sourceFile);
```

### الخطوة 4: تغيير حجم الصورة

غيّر الحجم إلى الأبعاد المطلوبة (مثلاً، 300 × 300 بكسل).

```java
image.resize(300, 300);
```

### الخطوة 5: حفظ الصورة المعدلة

صدّر البت ماب المعدل كملف JPEG.

```java
image.save(destName, new JpegOptions());
```

> **نصيحة احترافية:** جرّب قيم عرض/ارتفاع مختلفة أو حافظ على نسبة الأبعاد بحساب أحد الأبعاد من الآخر.

## المشكلات الشائعة والحلول

| Issue | Reason | Fix |
|-------|--------|-----|
| **`OutOfMemoryError`** | ملفات PSD الكبيرة جدًا قد تتجاوز مساحة الذاكرة المخصصة للـ JVM. | زيادة حجم الذاكرة للـ JVM (`-Xmx2g`) أو معالجة الصور على أجزاء. |
| Unsupported format | محاولة تحميل ملف غير PSD دون الخيارات المناسبة. | استخدم التحميل المناسب `Image.load` أو حوّل الملف أولاً. |
| Distorted output | نسبة أبعاد غير صحيحة. | احسب الارتفاع بناءً على نسبة الأبعاد الأصلية أو استخدم `image.resizeProportionally`. |

## الأسئلة المتكررة

### س1: هل يمكنني تغيير حجم الصور إلى أبعاد محددة باستخدام Aspose.PSD for Java؟

**ج:** بالتأكيد. تسمح لك طريقة `resize(width, height)` بتحديد أي حجم بكسل تحتاجه.

### س2: هل Aspose.PSD for Java متوافق مع صيغ صور مختلفة؟

**ج:** نعم. بالإضافة إلى PSD، تدعم المكتبة JPEG، PNG، BMP، TIFF، والعديد غيرها.

### س3: أين يمكنني العثور على وثائق إضافية لـ Aspose.PSD for Java؟

**ج:** راجع [Aspose.PSD for Java documentation](https://reference.aspose.com/psd/java/) للحصول على مرجع كامل للـ API.

### س4: هل يمكنني تجربة Aspose.PSD for Java قبل الشراء؟

**ج:** بالتأكيد! حمّل [free trial version](https://releases.aspose.com/) لاستكشاف جميع الميزات.

### س5: كيف يمكنني الحصول على دعم لـ Aspose.PSD for Java؟

**ج:** زر [Aspose.PSD forum](https://forum.aspose.com/c/psd/34) لطرح الأسئلة ومشاركة التجارب مع المجتمع.

## الخاتمة

في هذا الدرس أظهرنا كيف تجعل **java image manipulation library** مثل Aspose.PSD مهام **how to resize image java** سهلة. باتباع الخطوات المختصرة أعلاه يمكنك دمج تغيير حجم الصور في أي تطبيق Java، مما يضمن نتائج سريعة وموثوقة دون أدوات خارجية.

---

**Last Updated:** 2025-12-27  
**Tested With:** Aspose.PSD for Java 24.12 (latest)  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}