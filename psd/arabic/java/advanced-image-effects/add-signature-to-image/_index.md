---
date: 2026-02-04
description: تعلم كيفية رسم لوحة صورة وتراكب توقيع في Java باستخدام Aspose.PSD. اتبع
  هذا الدرس خطوة بخطوة لمعالجة الصور في Java واحفظ النتيجة بصيغة PNG.
linktitle: Add a Signature to an Image
second_title: Aspose.PSD Java API
title: رسم لوحة صورة – إضافة توقيع باستخدام Aspose.PSD للغة Java
url: /ar/java/advanced-image-effects/add-signature-to-image/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# رسم صورة على Canvas – إضافة توقيع باستخدام Aspose.PSD للـ Java

## المقدمة

إضافة توقيع يدوي أو رقمي إلى صورة هو طلب شائع للعقود، الفواتير، أو أي مستند يحتاج إلى إثبات الأصالة. باستخدام **Aspose.PSD for Java** يمكنك **draw image canvas** ومعاملة التوقيع كطبقة تراكب أخرى. في هذا **java image processing tutorial** سنستعرض سير العمل بالكامل — من تحميل الصورة الأساسية وملف التوقيع، إلى تهيئة الرسومات، رسم التراكب، وأخيرًا **save image png java**‑style.

## إجابات سريعة
- **ماذا يعني “draw image canvas”؟** يشير إلى رسم صورة واحدة فوق أخرى باستخدام الفئة `Graphics`.  
- **كيف أضيف توقيعًا في Java؟** حمّل ملف التوقيع كـ `Image` واستخدم `Graphics.drawImage`.  
- **أي إصدار من Aspose.PSD مطلوب؟** أي إصدار حديث 24.x؛ الكود يعمل مع أحدث المكتبة.  
- **هل يمكنني تراكب صور متعددة؟** نعم — كرّر استدعاء `drawImage` بمصادر مختلفة، مما يتيح **multiple image overlay**.  
- **هل أحتاج إلى ترخيص؟** الإصدار التجريبي يعمل للتطوير؛ الترخيص التجاري مطلوب للإنتاجحات Aspose.PSD، يعني رسم صورة على Canvas طلاء كائن `Image` واحد على آخر باستخدام سياق `Graphics`. هذه العملية هي العمود الفقري لتقنيات **overlay images java** مثل إضافة العلامات المائية، الشعارات، أو التوقيعات.

## كيفية رسم صورة على Canvas باستخدام Aspose.PSD
فيما يلي العملية خطوة بخطوة التي ستتبعها لوضع توقيع على أي ملف PSD أو صورة نقطية.

## لماذا نستخدم Aspose.PSD لتراكب توقيع؟
- **دعم كامل لـ PSD** – يعمل مع الطبقات، الأقنعة، والشفافية.  
- **بدون تبعيات نظام تشغيل** – Java خالص، مثالي للمعالجة على الخادم.  
- **أداء عالي في التصيير** – مُحسّن للملفات الكبيرة والتركيبات المعقدة.  

## المتطلبات المسبقة
- مجموعة تطوير Java (JDK) 8 أو أعلى.  
- Aspose.PSD for Java JAR مضاف إلى مسار مشروعك.  
- ملفا صورة: صورة أساسية (مثال: `layers.psd`) وصورة توقيع (`sample.psd`).  

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

> **نصيحة احترافية:** احرص على أن تكون الصورتان في نفس وضع اللون (RGB) لتجنب تغيرات اللون غير المتوقعة أثناء الرسم.

## الخطوة 2: تهيئة Graphics (initialize graphics java)

```java
//ExStart:InitializeGraphics
Graphics graphics = new Graphics(canvas);
//ExEnd:InitializeGraphics
```

كائن `Graphics` يعمل كفرشاة تسمح لك **draw image canvas**. تهيئته مع الـ `Image` الأساسي يربط جميع أوامر الرسم اللاحقة بهذا الـ Canvas.

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
| التوقيع يظهر مشوّهًا | اختلاف DPI بين الـ canvas والتوقيع | استخدم `signature.resize` قبل الرسم أو تأكد من أن كلا الملفين يشاركان نفس DPI. |
| ملف الإخراج كبير جدًا | الحفظ بدون ضغط | مرّر `PngOptions` مُكوَّنًا مع ضبط `CompressionLevel` إلى قيمة أعلى. |
| لا شيء يتم رسمه | Graphics لم يتم تحريره | استدعِ `graphics.dispose()` بعد الرسم (اختياري، لكنه ممارسة جيدة). |

## توسيع التقنية

- **إضافة علامة مائية java:** استبدل صورة التوقيع بعلامة مائية`.  
- **تدوير الصورة java:** استدعِ `graphics.rotateTransform(angle)` قبل `drawImage` لإمالة التوقيع أو العلامة المائية.  
- **ضبط شفافية الصورة:** عدّل شفافية أي تراكب باستخدام `graphics.setOpacity(float opacity)` حيث `0.0` يعني شفاف تمامًا و`1.0` يعني غير شفاف.  

## الخلا to draw image canvas** وإضافة توق Aspose.PSD للـ Java. يمكن توسيع هذه التقنية لتشمل العلامات المائية، الشعارات، أو أي **multiple image overlay**، مما يمنح تطبيقات Java الخاصة بك قدرات قوية في **java image processing**.

## الأسئلة المتكررة

### س1: هل يمكنني إضافة توقيعات متعددة إلى صورة؟

نعم، يمكنك إضافة توقيعات متعددة عن طريق تكرار الخطوات مع صور توقيع مختلفة، مما يتيح سيناريو **multiple image overlay**.

### س2: هل يدعم Aspose.PSD صيغ صور أخرى؟

نعم، يدعم Aspose.PSD مجموعة واسعة من صيغ الصور، مما يضمن المرونة في معالجة الصور.

### س3: هل يلزم الحصول على ترخيص لاستخدام Aspose.PSD للـ Java؟

نعم، تحتاج إلى ترخيص صالح لاستخدام Aspose.PSD. زر [Purchase Aspose.PSD](https://purchase.aspose.com/buy) للحصول على تفاصيل الترخيص.

### س4: كيف يمكنني الحصول على دعم Aspose.PSD؟

زر [Aspose.PSD Forum](https://forum.aspose.com/c/psd/34) للحصول على دعم المجتمع والنقاشات.

### س5: هل يمكنني تجربة Aspose.PSD للـ Java قبل الشراء؟

نعم، يمكنك الحصول على [free trial](https://releases.aspose.com/) لاستكشاف الميزات قبل الشراء.

## أسئلة متكررة إضافية

**س: كيف أغيّر شفافية التوقيع؟**  
ج: استخدم `graphics.setOpacity(float opacity)` قبل استدعاء `drawImage`. القيم تتراوح من 0.0 (شفاف) إلى 1.0 (غير شفاف).

**س: هل من الممكن تدوير التوقيع؟**  
ج: نعم — طبّق مصفوفة تحويل:  
ج: بالتأكيد. استبدل `PngOptions`` وحدد مستوى الجودة المطلوب.

**آخر تحديث:** 2026-02-04  
**تم الاختبار مع:** Aspose.PSD for Java 24.11  
**المؤلف:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}