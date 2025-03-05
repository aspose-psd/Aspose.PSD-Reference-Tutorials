---
title: كيفية إضافة تدرج طبقة السكتة الدماغية في جافا
linktitle: كيفية إضافة تدرج طبقة السكتة الدماغية في جافا
second_title: Aspose.PSD جافا API
description: تعرف على كيفية إضافة تدرجات طبقة الحد وتخصيصها في ملفات PSD باستخدام Aspose.PSD لـ Java من خلال هذا البرنامج التعليمي الشامل خطوة بخطوة.
type: docs
weight: 10
url: /ar/java/java-graphics-drawing/add-stroke-layer-gradient/
---
## مقدمة
هل تساءلت يومًا عن كيفية إضافة تدرج لطبقة الحد إلى صورك باستخدام Java؟ حسنا، أنت في المكان الصحيح! اليوم، نتعمق في عالم Aspose.PSD for Java، وهي مكتبة قوية تساعدك على التعامل مع ملفات PSD بسهولة. سواء كنت مبتدئًا أو مطورًا متمرسًا، سيرشدك هذا الدليل خطوة بخطوة خلال عملية إضافة تدرج طبقة الحد إلى ملفات PSD الخاصة بك. لذلك، اربط حزام الأمان واستعد لتعزيز مهاراتك في تحرير الرسومات!
## المتطلبات الأساسية
قبل أن نبدأ، هناك بعض الأشياء التي يجب أن تكون لديك. تأكد من أن لديك ما يلي:
1.  Java Development Kit (JDK): تأكد من تثبيت JDK على نظامك. يمكنك تنزيله من[موقع أوراكل](https://www.oracle.com/java/technologies/javase-downloads.html).
2.  Aspose.PSD لمكتبة Java: يمكنك تنزيله من ملف[صفحة تحميل Aspose.PSD](https://releases.aspose.com/psd/java/).
3. بيئة التطوير المتكاملة (IDE): أي بيئة تطوير متكاملة مثل IntelliJ IDEA أو Eclipse أو NetBeans ستعمل.
4.  ترخيص ساري المفعول: يمكنك الحصول على[ترخيص مؤقت](https://purchase.aspose.com/temporary-license/) إذا لم يكن لديك واحدة كاملة.
## حزم الاستيراد
أول الأشياء أولاً، فلنستورد الحزم الضرورية. سيمكننا ذلك من استخدام الفئات والأساليب المطلوبة لمعالجة ملف PSD.
```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;
import com.aspose.psd.examples.Utils.Assert;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.BlendMode;
import com.aspose.psd.fileformats.psd.layers.IGradientColorPoint;
import com.aspose.psd.fileformats.psd.layers.fillsettings.FillType;
import com.aspose.psd.fileformats.psd.layers.fillsettings.GradientColorPoint;
import com.aspose.psd.fileformats.psd.layers.fillsettings.GradientFillSettings;
import com.aspose.psd.fileformats.psd.layers.fillsettings.GradientTransparencyPoint;
import com.aspose.psd.fileformats.psd.layers.fillsettings.GradientType;
import com.aspose.psd.fileformats.psd.layers.fillsettings.IGradientTransparencyPoint;
import com.aspose.psd.fileformats.psd.layers.layereffects.StrokeEffect;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
```
الآن، دعونا نقسم المثال إلى خطوات متعددة لفهم أفضل.
## الخطوة 1: قم بتحميل ملف PSD
 أولاً، نحتاج إلى تحميل ملف PSD الذي نريد تعديله. سوف نستخدم`PsdLoadOptions` لتحديد أننا نريد تحميل موارد التأثيرات.
```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "Stroke.psd";
String exportPath = dataDir + "StrokeGradientChanged.psd";
PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);
PsdImage im = (PsdImage) Image.load(sourceFileName, loadOptions);
```
## الخطوة 2: الوصول إلى تأثير السكتة الدماغية
بعد ذلك، نحتاج إلى الوصول إلى تأثير الحد للطبقة التي نهتم بها. هنا، نفترض أنها الطبقة الثالثة (الفهرس 2) في ملف PSD.
```java
StrokeEffect gradientStroke = (StrokeEffect) im.getLayers()[2].getBlendingOptions().getEffects()[0];
```
## الخطوة 3: التحقق من خصائص تأثير السكتة الدماغية
قبل إجراء أي تغييرات، دعونا نتحقق من خصائص تأثير الحد للتأكد من أننا نقوم بتعديل الإعدادات الصحيحة.
```java
Assert.areEqual(BlendMode.Normal, gradientStroke.getBlendMode());
Assert.areEqual(255, gradientStroke.getOpacity());
Assert.areEqual(true, gradientStroke.isVisible());
GradientFillSettings fillSettings = (GradientFillSettings) gradientStroke.getFillSettings();
Assert.areEqual(Color.getBlack(), fillSettings.getColor());
Assert.areEqual(FillType.Gradient, fillSettings.getFillType());
Assert.areEqual(true, fillSettings.getAlignWithLayer());
Assert.areEqual(GradientType.Linear, fillSettings.getGradientType());
Assert.isTrue(Math.abs(90 - fillSettings.getAngle()) < 0.001, "Angle is incorrect");
Assert.areEqual(false, fillSettings.getDither());
Assert.isTrue(Math.abs(0 - fillSettings.getHorizontalOffset()) < 0.001, "Horizontal offset is incorrect");
Assert.isTrue(Math.abs(0 - fillSettings.getVerticalOffset()) < 0.001, "Vertical offset is incorrect");
Assert.areEqual(false, fillSettings.getReverse());
```
## الخطوة 4: تعديل إعدادات التعبئة المتدرجة
حان الوقت الآن لتعديل إعدادات التعبئة المتدرجة وفقًا لمتطلباتنا. سنقوم بتغيير اللون، والتعتيم، ووضع المزج، وغيرها من الخصائص.
```java
fillSettings.setColor(Color.getGreen());
gradientStroke.setOpacity((byte) 127);
gradientStroke.setBlendMode(BlendMode.Color);
fillSettings.setAlignWithLayer(false);
fillSettings.setGradientType(GradientType.Radial);
fillSettings.setAngle(45);
fillSettings.setDither(true);
fillSettings.setHorizontalOffset(15);
fillSettings.setVerticalOffset(11);
fillSettings.setReverse(true);
```
## الخطوة 5: إضافة وتعديل نقاط اللون والشفافية
دعونا نضيف نقاط لون وشفافية جديدة ونقوم بتعديل النقاط الموجودة لتحقيق تأثير التدرج المطلوب.
```java
// أضف نقطة لون جديدة
GradientColorPoint colorPoint = fillSettings.addColorPoint();
colorPoint.setColor(Color.getGreen());
colorPoint.setLocation(4096);
colorPoint.setMedianPointLocation(75);
// تغيير موقع النقطة السابقة
fillSettings.getColorPoints()[1].setLocation(1899);
// أضف نقطة شفافية جديدة
GradientTransparencyPoint transparencyPoint = fillSettings.addTransparencyPoint();
transparencyPoint.setOpacity(25);
transparencyPoint.setMedianPointLocation(25);
transparencyPoint.setLocation(4096);
// تغيير موقع نقطة الشفافية السابقة
fillSettings.getTransparencyPoints()[1].setLocation(2411);
```
## الخطوة 6: احفظ ملف PSD المعدل
بعد إجراء كافة التعديلات اللازمة، نحتاج إلى حفظ ملف PSD.
```java
im.save(exportPath);
```
## الخطوة 7: التحقق من التعديلات
أخيرًا، لنقم بتحميل ملف PSD المحفوظ والتحقق من تطبيق التغييرات بشكل صحيح.
```java
PsdImage img = (PsdImage) Image.load(exportPath, loadOptions);
StrokeEffect gradientStrokeEffect = (StrokeEffect) img.getLayers()[2].getBlendingOptions().getEffects()[0];
Assert.areEqual(BlendMode.Color, gradientStrokeEffect.getBlendMode());
Assert.areEqual(127, gradientStrokeEffect.getOpacity());
Assert.areEqual(true, gradientStrokeEffect.isVisible());
GradientFillSettings fillSetting = (GradientFillSettings) gradientStrokeEffect.getFillSettings();
Assert.areEqual(Color.getGreen(), fillSetting.getColor());
Assert.areEqual(FillType.Gradient, fillSetting.getFillType());
// تحقق من نقاط اللون
Assert.areEqual(3, fillSetting.getColorPoints().length);
IGradientColorPoint point = fillSetting.getColorPoints()[0];
Assert.areEqual(50, point.getMedianPointLocation());
Assert.areEqual(Color.getBlack(), point.getColor());
Assert.areEqual(0, point.getLocation());
point = fillSettings.getColorPoints()[1];
Assert.areEqual(50, point.getMedianPointLocation());
Assert.areEqual(Color.getWhite(), point.getColor());
Assert.areEqual(1899, point.getLocation());
point = fillSettings.getColorPoints()[2];
Assert.areEqual(75, point.getMedianPointLocation());
Assert.areEqual(Color.getGreen(), point.getColor());
Assert.areEqual(4096, point.getLocation());
// تحقق من نقاط الشفافية
Assert.areEqual(3, fillSettings.getTransparencyPoints().length);
IGradientTransparencyPoint transparencyPoint1 = fillSettings.getTransparencyPoints()[0];
Assert.areEqual(50, transparencyPoint1.getMedianPointLocation());
Assert.areEqual(100, transparencyPoint1.getOpacity());
Assert.areEqual(0, transparencyPoint1.getLocation());
transparencyPoint1 = fillSettings.getTransparencyPoints()[1];
Assert.areEqual(50, transparencyPoint.getMedianPointLocation());
Assert.areEqual(100, transparencyPoint.getOpacity());
Assert.areEqual(2411, transparencyPoint.getLocation());
transparencyPoint1 = fillSettings.getTransparencyPoints()[2];
Assert.areEqual(25, transparencyPoint.getMedianPointLocation());
Assert.areEqual(25, transparencyPoint.getOpacity());
Assert.areEqual(4096, transparencyPoint.getLocation());
```
## خاتمة
وهنا لديك! أنت تعرف الآن كيفية إضافة تدرجات طبقة الحد ومعالجتها في ملفات PSD باستخدام Aspose.PSD لـ Java. يغطي هذا البرنامج التعليمي تحميل ملف PSD، والوصول إلى تأثيرات الحدود وتعديلها، وحفظ التغييرات. باستخدام هذه المهارات، يمكنك إنشاء تدرجات جذابة بصريًا وتخصيص ملفات PSD الخاصة بك لتناسب احتياجاتك.
## الأسئلة الشائعة
### ما هو Aspose.PSD لجافا؟
Aspose.PSD for Java هي مكتبة تتيح للمطورين العمل مع ملفات PSD في تطبيقات Java، وتوفر ميزات لإنشاء ملفات PSD ومعالجتها وتحويلها.
### هل أحتاج إلى ترخيص لاستخدام Aspose.PSD لـ Java؟
 نعم، أنت بحاجة إلى ترخيص صالح لاستخدام Aspose.PSD لـ Java. يمكنك الحصول على[ترخيص مؤقت](https://purchase.aspose.com/temporary-license/) لأغراض التقييم.
### هل يمكنني استخدام Aspose.PSD لـ Java لإنشاء ملفات PSD من البداية؟
قطعاً! يوفر Aspose.PSD for Java واجهات برمجة تطبيقات شاملة لإنشاء ملفات PSD ومعالجتها برمجيًا.
### هل من الممكن تطبيق تأثيرات أخرى باستخدام Aspose.PSD لـ Java؟
نعم، يمكنك تطبيق تأثيرات متنوعة مثل الظل والتوهج والمزيد باستخدام Aspose.PSD لـ Java.
### أين يمكنني العثور على الوثائق الخاصة بـ Aspose.PSD لـ Java؟
 يمكنك العثور على الوثائق[هنا](https://reference.aspose.com/psd/java/).