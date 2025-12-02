---
date: 2025-12-02
description: تعلم كيفية رسم صورة على لوحة قماشية وتراكب توقيع في جافا باستخدام Aspose.PSD.
  اتبع هذا الدليل خطوة بخطوة لمعالجة الصور في جافا واحفظ النتيجة كملف PNG.
language: ar
linktitle: Add a Signature to an Image
second_title: Aspose.PSD Java API
title: رسم صورة على اللوحة – إضافة توقيع باستخدام Aspose.PSD للـ Java
url: /java/advanced-image-effects/add-signature-to-image/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# رسم صورة على القماش – إضافة توقيع باستخدام Aspose.PSD للـ Java

## المقدمة

إضافة توقيع يدوي أو رقمي إلى صورة هو طلب شائع للعقود، الفواتير، أو أي مستند يحتاج إلى إثبات الأصالة. باستخدام **Aspose.PSD للـ Java** يمكنك **رسم صورة على القماش** ومعاملة التوقيع كطبقة تغطية إضافية. في هذا **دروس معالجة الصور بجافا** سنستعرض سير العمل بالكامل—من تحميل الصورة الأساسية وملف التوقيع، إلى تهيئة الرسومات، رسم الطبقة الفوقية، وأخيرًا **حفظ الصورة بصيغة png بجافا**.

## إجابات سريعة
- **ماذا يعني “رسم صورة على القماش”؟** يشير إلى عرض صورة واحدة فوق أخرى باستخدام فئة `Graphics`.  
- **كيف أضيف توقيعًا في جافا؟** حمّل ملف التوقيع كـ `Image` واستخدم `Graphics.drawImage`.  
- **ما نسخة Aspose.PSD المطلوبة؟** أي إصدار حديث 24.x؛ الكود يعمل مع أحدث مكتبة.  
- **هل يمكنني وضع عدة صور فوق بعضها؟** نعم—كرر استدعاء `drawImage` بمصادر مختلفة.  
- **هل أحتاج إلى ترخيص؟** الإصدار التجريبي يكفي للتطوير؛ الترخيص التجاري مطلوب للإنتاج.

## ما هو “رسم صورة على القماش”؟
في مصطلحات Aspose.PSD، يعني رسم صورة على القماش صب صورة `Image` واحدة فوق أخرى باستخدام سياق `Graphics`. هذه العملية هي العمود الفقري لتقنيات **overlay images java** مثل إضافة العلامات المائية، الشعارات، أو التوقيعات.

## لماذا نستخدم Aspose.PSD لتغطية توقيع؟
- **دعم كامل لملفات PSD** – يعمل مع الطبقات، الأقنعة، والشفافية.  
- **بدون تبعيات نظام تشغيل** – جافا صافية، مثالية للمعالجة على الخادم.  
- **أداء عالٍ في العرض** – مُحسّن للملفات الكبيرة والتراكيب المعقدة.  

## المتطلبات المسبقة
- مجموعة تطوير جافا (JDK) 8 أو أعلى.  
- ملف JAR الخاص بـ Aspose.PSD للـ Java مضاف إلى مسار الفئة في مشروعك.  
- ملفا صورة: صورة أساسية (مثال: `layers.psd`) ورسمة توقيع (`sample.psd`).  

## استيراد الحزم

```java
import com.aspose.psd.Graphics;
import static com.aspose.psd.GraphicsUnit.Point;
import com.aspose.psd.Image;
import com.aspose.psd.Point;

import com.aspose.psd.imageoptions.PngOptions;
```

## الخطوة 1: تحميل الصور الأساسية والثانوية

```java
//ExStart:LoadImages
String dataDir = "Your Document Directory";

// Load the primary image (the canvas)
Image canvas = Image.load(dataDir + "layers.psd");

// Load the secondary image containing the signature graphics
Image signature = Image.load(dataDir + "sample.psd");
//ExEnd:LoadImages
```

> **نصيحة احترافية:** احرص على أن تكون الصورتان بنفس وضع اللون (RGB) لتجنب تغيرات اللون غير المتوقعة عند الرسم.

## الخطوة 2: تهيئة الرسومات (initialize graphics java)

```java
//ExStart:InitializeGraphics
Graphics graphics = new Graphics(canvas);
//ExEnd:InitializeGraphics
```

كائن `Graphics` يعمل كفرشاة تسمح لك **برسم صورة على القماش**. تهيئته مع الصورة الأساسية تجعل جميع أوامر الرسم اللاحقة تُطبق على هذا القماش.

## الخطوة 3: إضافة التوقيع إلى الصورة (how to add signature)

```java
//ExStart:AddSignatureToImage
graphics.drawImage(
    signature,
    new Point(
        canvas.getHeight() - signature.getHeight(),   // X‑coordinate (bottom)
        canvas.getWidth() - signature.getWidth()      // Y‑coordinate (right)
    )
);
canvas.save(dataDir + "AddSignatureToImage_out.png", new PngOptions());
//ExEnd:AddSignatureToImage
```

في هذا المقتطف نقوم بـ **overlay images java** عن طريق وضع التوقيع في الزاوية السفلية‑اليمنى. عدّل قيم `Point` إذا كنت تحتاج إلى موضع مختلف.

## المشكلات الشائعة والحلول
| العَرَض | السبب | الحل |
|---------|-------|-----|
| التوقيع يظهر مشوّهًا | اختلاف DPI بين القماش والتوقيع | استخدم `signature.resize` قبل الرسم أو تأكد من أن كلا الملفين يشاركان نفس DPI. |
| ملف الإخراج كبير جدًا | حفظ دون ضغط | مرّر `PngOptions` مُعدّة مع `CompressionLevel` مضبوطة على قيمة أعلى. |
| لا يتم رسم شيء | عدم التخلص من كائن Graphics | استدعِ `graphics.dispose()` بعد الرسم (اختياري، لكنه ممارسة جيدة). |

## الخاتمة

باتباع هذه الخطوات تعلمت **كيفية رسم صورة على القماش** وإضافة **توقيع** بسلاسة باستخدام Aspose.PSD للـ Java. يمكن توسيع هذه التقنية لتشمل العلامات المائية، الشعارات، أو أي رسومات تغطية، مما يمنح تطبيقات جافا الخاصة بك قدرات قوية في **معالجة الصور بجافا**.

## الأسئلة المتكررة

### س1: هل يمكنني إضافة عدة توقيعات إلى صورة؟

ج1: نعم، يمكنك إضافة عدة توقيعات بتكرار الخطوات مع صور توقيع مختلفة.

### س2: هل يدعم Aspose.PSD صيغ صور أخرى؟

ج2: نعم، يدعم Aspose.PSD مجموعة واسعة من صيغ الصور، مما يضمن مرونة في معالجة الصور.

### س3: هل يلزم ترخيص لاستخدام Aspose.PSD للـ Java؟

ج3: نعم، تحتاج إلى ترخيص صالح لاستخدام Aspose.PSD. زر [Purchase Aspose.PSD](https://purchase.aspose.com/buy) للحصول على تفاصيل الترخيص.

### س4: كيف يمكنني الحصول على دعم لـ Aspose.PSD؟

ج4: زر [منتدى Aspose.PSD](https://forum.aspose.com/c/psd/34) للحصول على دعم المجتمع والنقاشات.

### س5: هل يمكن تجربة Aspose.PSD للـ Java قبل الشراء؟

ج5: نعم، يمكنك الحصول على [إصدار تجريبي مجاني](https://releases.aspose.com/) لاستكشاف الميزات قبل الشراء.

## أسئلة متكررة إضافية

**س: كيف أغيّر شفافية التوقيع؟**  
ج: استخدم `graphics.setOpacity(float opacity)` قبل استدعاء `drawImage`. القيم تتراوح بين 0.0 (شفاف) إلى 1.0 (معتم).

**س: هل يمكن تدوير التوقيع؟**  
ج: نعم—طبق مصفوفة تحويل عبر `graphics.rotateTransform(angle)` قبل الرسم.

**س: هل يمكنني رسم التوقيع على JPEG بدلاً من PNG؟**  
ج: بالتأكيد. استبدل `PngOptions` بـ `JpegOptions` وحدد مستوى الجودة المطلوب.

---

**آخر تحديث:** 2025-12-02  
**تم الاختبار مع:** Aspose.PSD للـ Java 24.11  
**المؤلف:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}