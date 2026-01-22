---
date: 2026-01-22
description: تعلم كيفية إنشاء صورة PSD في Java باستخدام Aspose.PSD، ورسم الرسومات،
  وتعبئة المضلع، وتصدير PSD إلى BMP. دليل كامل لتعديل الصور في Java.
linktitle: Drawing Using Graphics in Java
second_title: Aspose.PSD Java API
title: إنشاء صورة PSD في Java – الرسم باستخدام Graphics مع Aspose.PSD
url: /ar/java/java-graphics-drawing/drawing-using-graphics/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# الرسم باستخدام الرسومات في Java

## المقدمة
في هذا **java image manipulation tutorial** سنُظهر لك كيفية **create PSD image java** برمجياً باستخدام Aspose.PSD. سواءً كنت بحاجة إلى توليد رسومات في الوقت الفعلي، ملء مضلعات، أو تصدير عملك إلى BMP، فإن هذا الدليل يرافقك في كل خطوة—من إعداد البيئة إلى حفظ الملف النهائي.

## إجابات سريعة
- **ما المكتبة التي تسمح لي بإنشاء صور PSD في Java؟** Aspose.PSD for Java.  
- **هل يمكنني رسم أشكال وملء مضلعات؟** نعم، باستخدام فئات Graphics و Brush.  
- **كيف أقوم بتصدير PSD إلى BMP؟** استدعِ `image.save(..., new BmpOptions())`.  
- **هل أحتاج إلى ترخيص للتطوير؟** ترخيص مؤقت مجاني متاح للتقييم.  
- **ما نسخة Java المطلوبة؟** JDK 8 أو أعلى.

## المتطلبات المسبقة
قبل الغوص في هذا الدرس، تأكد من توفر المتطلبات التالية:
- معرفة أساسية ببرمجة Java.  
- مجموعة تطوير Java (JDK) مثبتة على نظامك.  
- بيئة تطوير متكاملة (IDE) مثل IntelliJ IDEA أو Eclipse.  
- مكتبة Aspose.PSD for Java. يمكنك تنزيلها من [here](https://releases.aspose.com/psd/java/).

## كيفية رسم الرسومات في Java باستخدام Aspose.PSD
للبدء، استورد الحزم الضرورية من Aspose.PSD for Java وغيرها من مكتبات Java القياسية:

```java
import com.aspose.psd.Color;
import com.aspose.psd.Graphics;
import com.aspose.psd.Pen;
import com.aspose.psd.Point;
import com.aspose.psd.Rectangle;
import com.aspose.psd.brushes.LinearGradientBrush;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.BmpOptions;
```

## الخطوة 1: إنشاء كائن صورة
أولاً، أنشئ كائن `PsdImage` بأبعاد محددة:

```java
String dataDir = "Your Document Directory";
PsdImage image = new PsdImage(500, 500);
```

## الخطوة 2: تهيئة كائن Graphics
بعد ذلك، قم بتهيئة كائن `Graphics` باستخدام `PsdImage`:

```java
Graphics graphics = new Graphics(image);
```

## الخطوة 3: مسح سطح الصورة
امسح سطح الصورة بلون محدد (الأبيض في هذا المثال):

```java
graphics.clear(Color.getWhite());
```

## الخطوة 4: إنشاء وتكوين كائن Pen
أنشئ كائن `Pen` لتحديد خصائص الخط (اللون، السمك، إلخ):

```java
Pen pen = new Pen(Color.getBlue());
```

## الخطوة 5: رسم الأشكال – كيفية رسم الرسومات في Java
ارسم إهليلجاً على الصورة باستخدام كائن `Pen` ومستطيل محيط:

```java
graphics.drawEllipse(pen, new Rectangle(10, 10, 150, 100));
```

## تعبئة مضلع في رسومات Java
عرّف واستخدم `LinearGradientBrush` لملء مضلع بتدرج لوني:

```java
LinearGradientBrush linearGradientBrush = new LinearGradientBrush(image.getBounds(), Color.getRed(), Color.getWhite(), 45f);
Point[] points = { new Point(200, 200), new Point(400, 200), new Point(250, 350) };
graphics.fillPolygon(linearGradientBrush, points);
```

## تصدير PSD إلى BMP
أخيراً، احفظ الصورة المعدلة إلى موقع وتنسيق محددين (BMP في هذا المثال):

```java
image.save(dataDir + "DrawingUsingGraphics_output.bmp", new BmpOptions());
```

## الخاتمة
باتباعك لهذا **java image manipulation tutorial**، أصبحت الآن تعرف كيفية **create PSD image java**، رسم الأشكال، تطبيق التدرجات، ملء المضلعات، و**export PSD to BMP** باستخدام Aspose.PSD. جرّب فُرش مختلفة، ألوان، وأشكال لتثري تطبيقات Java الخاصة Asposeقات، ضبط الألوان، وتصيير النصوص.

**س: هل Aspose.PSD مناسب للتطبيقات عالية الأداء؟**  
ج: بالتأكيد، Aspose.PSD مُحسّن للأداء وكفاءة الذاكرة.

**س: أين يمكنني العثور على المزيد من الأمثلة والوثائق؟**  
ج: زر [Aspose.PSD Java documentation](https://reference.aspose.com/psd/java/) للحصول على أدلة شاملة ومراجع API.

**س: هل يدعم Aspose.PSD صيغ صور متعددة للتصدير؟**  
ج: نعم، يمكن لـ Aspose.PSD الت الدعم أو؟**  
ج: تواصل مع مجتمع Aspose.PSD عبر [support forum](https://forum.aspose.com/c/psd/34) أو فكر في الحصول على [temporary license](https://purchase.aspose.com/temporary-license/) للدعم ذو الأولوية.

**آخر تحديث:** 2026-01-22  
**تم الاختبار مع:** Aspose.PSD for Java 24.10  
**المؤلف:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}