---
date: 2026-03-23
description: تعلم كيفية إنشاء ملفات PSD ذات تعبئة تدرجية باستخدام Java و Aspose.PSD.
  يوضح هذا الدليل كيفية تعديل طبقات التدرج في ملفات PSD، وضبط الألوان والشفافية وغيرها
  من الخصائص برمجيًا.
linktitle: Create Gradient Fill PSD with Java – Add Gradient Fill Layer
second_title: Aspose.PSD Java API
title: إنشاء ملف PSD لتعبئة التدرج باستخدام Java – إضافة طبقة تعبئة التدرج
url: /ar/java/psd-image-modification-conversion/add-gradient-fill-layer-psd-files/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# إضافة طبقة تعبئة متدرجة في ملفات PSD باستخدام Java

## مقدمة

هل رغبت يومًا في إضافة لمسة سحرية بصرية إضافية لملفات PSD الخاصة بك وتساءلت **how to create gradient fill PSD** باستخدام Java؟ تمنحك التدرجات عمقًا لتصاميمك، لكن تعديلها يدويًا قد يكون مرهقًا. باستخدام **Aspose.PSD for Java**، يمكنك تعديل تدرجات PSD برمجيًا، تغيير الألوان، ضبط الشفافية، وضبط كل خاصية بدقة—مما يوفر وقتك ويضمن التناسق عبر العشرات من الملفات.

## إجابات سريعة
- **ما المكتبة التي تسمح لك بتحرير تدرجات PSD في Java؟** Aspose.PSD for Java.  
- **أي طريقة تقوم بتحميل ملف PSD؟** `Image.load(path)`.  
- **كيف تغير زاوية التدرج؟** `settings.setAngle(double)`.  
- **هل يمكنك إضافة نقاط لون جديدة؟** نعم—أنشئ كائنات `GradientColorPoint` وأضفها إلى قائمة نقاط اللون.  
- **هل تحتاج إلى ترخيص للاستخدام الإنتاجي؟** يلزم الحصول على ترخيص تجاري؛ يتوفر نسخة تجريبية مجانية للتقييم.

## ما هو “create gradient fill PSD”؟

إنشاء PSD بتعبئة متدرجة يعني إدراج أو تعديل طبقة تعبئة تعتمد على التدرج داخل مستند Photoshop برمجيًا. يتيح ذلك تنسيقًا تلقائيًا، ومعالجة دفعات، وتوليد صور ديناميكي دون فتح Photoshop.

## لماذا تستخدم Aspose.PSD لتحرير تدرجات PSD؟

- **دعم كامل لملفات .PSD** – يعمل مع جميع أنواع الطبقات، بما في ذلك الكائنات الذكية.  
- **لا حاجة لـ Photoshop** – يمكن تشغيله على أي خادم أو خط أنابيب CI.  
- **تحكم دقيق** – ضبط الزاوية، الإزاحات، التمويه، نقاط اللون، ونقاط الشفافية عبر واجهة برمجة تطبيقات Java نظيفة.  

## المتطلبات المسبقة

قبل الغوص في التفاصيل، تأكد من وجود ما يلي:

- Java Development Kit (JDK): نسخة مستقرة من JDK ضرورية لتشغيل كود Java. يمكنك تنزيلها من موقع Oracle: [Link to Oracle JDK download page]
- Aspose.PSD for Java: هذه المكتبة القوية تتيح لك العمل مع ملفات PSD في تطبيقات Java الخاصة بك. قم بتنزيلها من موقع Aspose: [Link to Aspose.PSD for Java download] (يتوفر نسخة تجريبية مجانية)

## استيراد الحزم

لنبدأ باستيراد حزم Aspose.PSD الأساسية اللازمة للعمل مع ملفات PSD:

```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.IGradientColorPoint;
import com.aspose.psd.fileformats.psd.layers.filllayers.FillLayer;
import com.aspose.psd.fileformats.psd.layers.fillsettings.FillType;
import com.aspose.psd.fileformats.psd.layers.fillsettings.GradientColorPoint;
import com.aspose.psd.fileformats.psd.layers.fillsettings.GradientTransparencyPoint;
import com.aspose.psd.fileformats.psd.layers.fillsettings.IGradientFillSettings;
import com.aspose.psd.fileformats.psd.layers.fillsettings.IGradientTransparencyPoint;
import com.aspose.psd.imageoptions.PsdOptions;
import java.util.ArrayList;
import java.util.Collections;
import java.util.List;
```

توفر هذه الاستيرادات الوصول إلى الفئات والطرق لتحميل، تعديل، وحفظ ملفات PSD.

الآن استعد للرحلة المثيرة لتعديل طبقات التعبئة المتدرجة!

## كيفية إنشاء PSD بتعبئة متدرجة باستخدام Java

### الخطوة 1: تحميل ملف PSD

أولاً، نحتاج إلى تحميل ملف PSD الذي يحتوي على طبقة التعبئة المتدرجة التي تريد تعديلها. استخدم طريقة `Image.load` مع تحديد مسار الملف:

```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "ComplexGradientFillLayer.psd";
String outputFile = dataDir + "ComplexGradientFillLayer_output.psd";
PsdImage image = (PsdImage)Image.load(sourceFileName);
```

يقوم هذا المقتطف بتحميل ملف PSD من الدليل المحدد وتخزينه في المتغير `image`.

### الخطوة 2: تحديد طبقة التعبئة المتدرجة

يمكن أن تحتوي ملفات PSD على العديد من الطبقات. نحتاج إلى عزل الطبقة المحددة التي تحتوي على التعبئة المتدرجة التي نريد تحريرها. قم بالتكرار عبر مصفوفة `image.getLayers()` للعثور على الطبقة المطلوبة:

```java
for (int i = 0; i < image.getLayers().length; i++) {
if (image.getLayers()[i] instanceof FillLayer) {
   FillLayer fillLayer = (FillLayer) image.getLayers()[i];
   // Further checks and modifications will happen here
   break;
}
}
```

يتحقق هذا الحلقة من كل طبقة. إذا كانت الطبقة من نوع `FillLayer`، يتم تحويلها إلى نوع `FillLayer` وتخزينها في المتغير `fillLayer` للمعالجة اللاحقة. يمكننا إضافة فحوصات إضافية داخل الحلقة إذا كان لديك معايير محددة لتحديد الطبقة المستهدفة (مثل اسم الطبقة).

### الخطوة 3: التحقق من نوع التعبئة المتدرجة

ليس كل طبقات التعبئة تستخدم التدرجات. يؤكد هذا المقتطف ما إذا كانت الطبقة المحددة تحتوي بالفعل على تعبئة متدرجة:

```java
if (fillLayer.getFillSettings().getFillType() != FillType.Gradient) {
   throw new Exception("Wrong Fill Layer");
}
```

إذا لم تُرجع طريقة `getFillType` القيمة `FillType.Gradient`، يتم رمي استثناء، مما يشير إلى أننا نتعامل مع الطبقة الخاطئة.

## كيفية تحرير تدرج PSD باستخدام Aspose.PSD

### الخطوة 4: الوصول إلى خصائص التدرج وتعديلها

السحر يحدث هنا! يوفر Aspose.PSD إمكانية الوصول إلى مختلف خصائص تعبئة التدرج عبر واجهة `IGradientFillSettings`. يمكننا استرجاعها وتعديلها حسب الحاجة:

```java
IGradientFillSettings settings = (IGradientFillSettings) fillLayer.getFillSettings();

// Modify properties (replace with desired values)
settings.setAngle(0.0);  // Set angle to 0 degrees
settings.setDither(false);  // Disable dithering
settings.setAlignWithLayer(true); // Align gradient with layer
settings.setReverse(true);  // Reverse gradient direction
settings.setHorizontalOffset(25);  // Set horizontal offset
settings.setVerticalOffset(-15);  // Set vertical offset
```

يقوم هذا الكود باسترجاع كائن `IGradientFillSettings` ثم تعديل خصائص مثل الزاوية، التمويه، المحاذاة، والإزاحات. استبدل القيم المقدمة بالإعدادات التي تريدها لتحقيق تأثير التدرج الذي تتصوره.

### الخطوة 5: تعديل نقاط اللون والشفافية

يتم تعريف التدرجات بنقاط اللون والشفافية على طول طيف. يتيح لك Aspose.PSD تعديل هذه النقاط للتحكم الدقيق:

```java
List<IGradientColorPoint> colorPoints = new ArrayList<IGradientColorPoint>();
Collections.addAll(colorPoints, settings.getColorPoints());
List<IGradientTransparencyPoint> transparencyPoints = new ArrayList<IGradientTransparencyPoint>();
Collections.addAll(transparencyPoints, settings.getTransparencyPoints());

// Add a new color point
GradientColorPoint gr1 = new GradientColorPoint();
gr1.setColor(Color.getViolet());
gr1.setLocation(4096);
gr1.setMedianPointLocation(75);
colorPoints.add(gr1);

// Modify an existing color point
colorPoints.get(1).setLocation(3000);

// Add a new transparency point
GradientTransparencyPoint gr2 = new GradientTransparencyPoint();
gr2.setOpacity(80.0);
gr2.setLocation(4096);
gr2.setMedianPointLocation(25);
transparencyPoints.add(gr2);

// Modify an existing transparency point
transparencyPoints.get(2).setLocation(3000);

settings.setColorPoints(colorPoints.toArray(new IGradientColorPoint[0]));
settings.setTransparencyPoints(transparencyPoints.toArray(new IGradientTransparencyPoint[0]));
```

### الخطوة 6: تحديث وحفظ ملف PSD

بعد إجراء التعديلات اللازمة، قم بتحديث طبقة التعبئة واحفظ ملف PSD:

```java
fillLayer.update();
image.save(outputFile, new PsdOptions(image));
```

طريقة `fillLayer.update()` تطبق التغييرات على طبقة التعبئة المتدرجة، و`image.save` يحفظ ملف PSD المعدل إلى مسار الإخراج المحدد.

## المشكلات الشائعة والحلول

- **استثناء “Wrong Fill Layer”** – تأكد من استهداف `FillLayer` يستخدم فعليًا تدرجًا. تحقق من اسم الطبقة أو الفهرس قبل التحويل.  
- **نقاط اللون لا تعكس التغييرات** – بعد تعديل قائمة النقاط، احرص دائمًا على استدعاء `settings.setColorPoints(...)` و `settings.setTransparencyPoints(...)` لإرسال التحديثات إلى الطبقة.  
- **الأداء على ملفات PSD الكبيرة** – إذا كنت تعالج العديد من الملفات، أعد استخدام نفس كائن `PsdOptions` وأغلق الصور فورًا باستخدام `image.dispose()` لتحرير الذاكرة.

## الأسئلة المتكررة

**س: هل يمكنني إضافة نقاط لون وشفافية متعددة إلى تدرج؟**  
ج: بالتأكيد! يمكنك إضافة عدد غير محدود من نقاط اللون والشفافية حسب الحاجة لتحقيق تأثير التدرج المطلوب. فقط أنشئ نقاطًا جديدة وأضفها إلى القوائم المعنية.

**س: كيف أزيل نقطة لون أو شفافية من تدرج؟**  
ج: استخدم طريقة `remove` للقائمة، مثل `colorPoints.remove(index)`, لحذف النقطة غير المرغوبة قبل استدعاء `setColorPoints`.

**س: هل يمكنني تغيير نوع التدرج (خطّي، دائري، إلخ)؟**  
ج: يدعم Aspose.PSD حاليًا التدرجات الخطية. قد تضيف الإصدارات المستقبلية أنواعًا أخرى، لكن يمكنك محاكاة تأثيرات أخرى عبر تعديل نقاط اللون والشفافية.

**س: هل هناك تأثير على الأداء عند تعديل التدرجات؟**  
ج: يعتمد التأثير على تعقيد التدرج وعدد التعديلات. في الاستخدامات العادية يكون الحمل ضئيلًا، لكن معالجة دفعات من الملفات الكبيرة قد تستفيد من تحسين إدارة الذاكرة.

**س: هل يمكنني تطبيق هذه التقنية على عدة طبقات تعبئة متدرجة في ملف PSD؟**  
ج: نعم. قم بالتكرار عبر `image.getLayers()`، وتحقق من كل `FillLayer` إذا كان `FillType.Gradient`، ثم طبّق نفس التعديلات حسب الحاجة.

**س: هل أحتاج إلى ترخيص تجاري للاستخدام الإنتاجي؟**  
ج: يلزم وجود ترخيص Aspose.PSD صالح للنشر في بيئات الإنتاج. تتوفر نسخة تجريبية مجانية لأغراض التقييم.

---

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

**آخر تحديث:** 2026-03-23  
**تم الاختبار مع:** Aspose.PSD for Java 24.11 (latest)  
**المؤلف:** Aspose