---
date: 2025-12-27
description: تعلم كيفية رسم مستطيل أحمر وأشكال أخرى في ملفات PSD باستخدام Aspose.PSD
  للغة Java. يغطي هذا الدليل خطوة بخطوة إنشاء المستندات، إضافة الطبقات، والرسم مع
  أمثلة على الشيفرة.
linktitle: Perform Simple Drawing
second_title: Aspose.PSD Java API
title: رسم مستطيل أحمر باستخدام Aspose.PSD للجافا
url: /ar/java/basic-image-operations/simple-drawing/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# رسم مستطيل أحمر باستخدام Aspose.PSD للغة Java

## المقدمة

مرحبًا بك في هذا الدليل خطوة بخطوة حول كيفية **رسم مستطيل أحمر** باستخدام Aspose.PSD للغة Java! في هذا البرنامج التعليمي، سنستعرض إنشاء مستند PSD جديد، إضافة طبقة، ورسم أشكال بألوان مخصصة. سواءً كنت تقوم بأتمتة أصول الرسوميات أو بناء خلفية أداة تصميم، فإن هذا الدليل يزوّدك بالكتل الأساسية اللازمة.

## إجابات سريعة
- **ما هو الصنف الأساسي لإنشاء ملف PSD؟** `PsdImage`
- **أي طريقة تُمسح لون خلفية الطبقة؟** `Graphics.clear(Color)`
- **كيف تُرسم مستطيلًا أحمر؟** `graphic.drawRectangle(new Pen(Color.getRed()), new Rectangle(...))`
- **هل أحتاج إلى ترخيص للتطوير؟** النسخة التجريبية المجانية تكفي للاختبار؛ الترخيص مطلوب للإنتاج.
- **هل يمكنني تعديل ملفات PSD الموجودة باستخدام نفس الـ API؟** نعم، يدعم Aspose.PSD تحرير ملفات PSD بالكامل.

## ما هو رسم مستطيل أحمر في ملف PSD؟
رسم مستطيل أحمر يعني استخدام كائن `Graphics` لتصيير شكل مستطيل مملوء أو مُحدّد باللون الأحمر على طبقة معينة من صورة PSD. تُستخدم هذه العملية عادةً لتسليط الضوء على مناطق، إنشاء نُقَطَةَ إِحتِياج، أو إضافة رسومات بسيطة برمجيًا.

## لماذا نستخدم Aspose.PSD للغة Java لمعالجة ملفات PSD؟
يوفر Aspose.PSD واجهة برمجة تطبيقات Java صافية تتيح لك قراءة، تعديل، وكتابة ملفات Photoshop PSD دون الحاجة إلى تثبيت Photoshop. يدعم إدارة الطبقات، تعديل الألوان، والرسم المتجه، مما يجعله مثاليًا لمعالجة الصور على الخادم، خطوط أنابيب الأصول المؤتمتة، وتوليد الرسومات المخصصة.

## المتطلبات المسبقة

- مجموعة تطوير جافا (JDK) مثبتة على جهازك.  
- مكتبة Aspose.PSD للغة Java. يمكنك تنزيلها من [توثيق Aspose.PSD للغة Java](https://reference.aspose.com/psd/java/).

## استيراد الحزم

لبدء العمل، استورد الأصناف المطلوبة إلى مشروع Java الخاص بك:

```java
import com.aspose.psd.Color;
import com.aspose.psd.Graphics;
import com.aspose.psd.Pen;
import com.aspose.psd.Rectangle;
import com.aspose.psd.brushes.SolidBrush;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.Layer;
```

## الخطوة 1: إنشاء مستند جديد

أولاً، أنشئ مستند PSD جديد بالحجم المطلوب للوحة الرسم. سيستضيف هذا المستند الطبقة التي سنرسم عليها.

```java
//ExStart:CreateDocument
String outputDir = "Your Document Directory";
String outPsdFilePath = outputDir + "output.psd";
int width = 100;
int height = 100;

PsdImage image = new PsdImage(width, height);
//ExEnd:CreateDocument
```

## الخطوة 2: إضافة طبقة

بعد ذلك، أضف طبقة فارغة تمتد على كامل عرض وارتفاع الصورة. الطبقات ضرورية لفصل عمليات الرسم.

```java
//ExStart:AddLayer
Layer layer = new Layer();
layer.setBottom(height);
layer.setRight(width);
image.addLayer(layer);
//ExEnd:AddLayer
```

## الخطوة 3: رسم الأشكال

سنستخدم صنف `Graphics` للتعامل مع بيانات بكسل الطبقة. فيما يلي ثلاثة أمثلة توضح مسح الخلفية ورسم مستطيلات بألوان مختلفة.

### مسح لون الطبقة (تعيين الخلفية إلى أصفر)

```java
//ExStart:DrawRectangleYellow
Graphics graphic = new Graphics(layer);
graphic.clear(Color.getYellow());
//ExEnd:DrawRectangleYellow
```

### رسم مستطيل أحمر (التركيز الأساسي)

```java
//ExStart:DrawRedRectangle
graphic.drawRectangle(new Pen(Color.getRed()), new Rectangle(30, 10, 40, 80));
//ExEnd:DrawRedRectangle
```

### رسم مستطيل أزرق (مثال إضافي)

```java
//ExStart:DrawBlueRectangle
graphic.drawRectangle(new Pen(new SolidBrush(Color.getBlue())), new Rectangle(10, 30, 80, 40));
//ExEnd:DrawBlueRectangle
```

## الخطوة 4: حفظ التغييرات

أخيرًا، اكتب صورة PSD المعدلة إلى القرص. سيحتوي الملف على الطبقة الجديدة والأشكال المرسومة.

```java
//ExStart:SaveChanges
image.save(outPsdFilePath);
//ExEnd:SaveChanges
```

## المشكلات الشائعة والحلول

- **الطبقة غير مرئية بعد الرسم:** تأكد من إضافة الطبقة إلى الصورة **قبل** إنشاء كائن `Graphics`.
- **الألوان تظهر غير صحيحة:** تحقق من أنك تستخدم `Color.getRed()` (أو الطرق الثابتة الأخرى) بدلاً من قيم RGB مخصصة قد تكون خارج النطاق.
- **الملف غير محفوظ:** تأكد من وجود مسار `outputDir` وأن التطبيق يمتلك صلاحيات الكتابة.

## الأسئلة المتكررة

### س1: هل يمكنني استخدام Aspose.PSD للغة Java لتعديل ملفات PSD الموجودة؟

ج1: نعم، يوفر Aspose.PSD للغة Java وظائف واسعة لتحرير وتعديل ملفات PSD الحالية.

### س2: أين يمكنني العثور على دعم Aspose.PSD للغة Java؟

ج2: يمكنك زيارة [منتدى Aspose.PSD للغة Java](https://forum.aspose.com/c/psd/34) لأي استفسارات متعلقة بالدعم.

### س3: هل هناك نسخة تجريبية مجانية متاحة لـ Aspose.PSD للغة Java؟

ج3: نعم، يمكنك الوصول إلى النسخة التجريبية المجانية [من هنا](https://releases.aspose.com/).

### س4: كيف يمكنني شراء ترخيص لـ Aspose.PSD للغة Java؟

ج4: يمكنك شراء ترخيص من [صفحة شراء Aspose.PSD](https://purchase.aspose.com/buy).

### س5: هل تتوفر تراخيص مؤقتة لـ Aspose.PSD للغة Java؟

ج5: نعم، يمكنك الحصول على ترخيص مؤقت من [هنا](https://purchase.aspose.com/temporary-license/).

## أسئلة متكررة إضافية

**س: هل يمكنني رسم أشكال أخرى غير المستطيلات؟**  
ج: نعم، يدعم صنف `Graphics` رسم الأقواس، الخطوط، والمسارات المخصصة.

**س: هل يدعم Aspose.PSD الشفافية في الأشكال المرسومة؟**  
ج: بالتأكيد؛ يمكنك استخدام `SolidBrush` مع لون ARGB لتضمين شفافية ألفا.

**س: هل يمكن تعديل شفافية الطبقة؟**  
ج: نعم، لكل كائن `Layer` طريقة `setOpacity` تقبل قيمة من 0 إلى 255.

**س: كيف أحمل ملف PSD موجود بدلاً من إنشاء ملف جديد؟**  
ج: استخدم `PsdImage image = (PsdImage)Image.load("path/to/file.psd");` قبل تعديل الطبقات.

## الخاتمة

لقد تعلمت الآن كيفية **رسم مستطيل أحمر** وغيرها من الأشكال الأساسية في ملف PSD باستخدام Aspose.PSD للغة Java. من خلال إنشاء مستند، إضافة طبقة، مسح خلفيتها، والرسم باستخدام واجهة `Graphics`، يمكنك أتمتة العديد من مهام التصميم الجرافيكي. استكشف المزيد بتجربة فُرش مختلفة، تأثيرات الطبقة، وصيغ الملفات المتنوعة.

---

**آخر تحديث:** 2025-12-27  
**تم الاختبار مع:** Aspose.PSD للغة Java 24.12 (أحدث نسخة وقت الكتابة)  
**المؤلف:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}