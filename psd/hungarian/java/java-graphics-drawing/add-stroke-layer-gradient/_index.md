---
title: Stroke Layer Gradient hozzáadása Java-ban
linktitle: Stroke Layer Gradient hozzáadása Java-ban
second_title: Aspose.PSD Java API
description: Ezzel az átfogó, lépésenkénti oktatóanyaggal megtudhatja, hogyan adhat hozzá és testre szabhatja a körvonal-réteg színátmeneteit a PSD-fájlokban az Aspose.PSD for Java segítségével.
weight: 10
url: /hu/java/java-graphics-drawing/add-stroke-layer-gradient/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Stroke Layer Gradient hozzáadása Java-ban

## Bevezetés
Elgondolkodott már azon, hogyan adhat vonásréteg-gradienst a képeihez Java használatával? Nos, jó helyen jársz! Ma az Aspose.PSD for Java világában merülünk el, egy hatékony könyvtár, amely segít a PSD-fájlok egyszerű kezelésében. Akár kezdő, akár tapasztalt fejlesztő, ez a lépésről lépésre végigvezeti Önt a körvonal-réteg gradiens hozzáadásának folyamatán a PSD-fájlokon. Szóval, csattal, és készülj fel, hogy javítsa grafikai szerkesztési készségeit!
## Előfeltételek
Mielőtt elkezdenénk, néhány dolgot meg kell tennie. Győződjön meg arról, hogy rendelkezik az alábbiakkal:
1.  Java Development Kit (JDK): Győződjön meg arról, hogy a JDK telepítve van a rendszeren. Letöltheti innen[Az Oracle webhelye](https://www.oracle.com/java/technologies/javase-downloads.html).
2.  Aspose.PSD for Java Library: Letöltheti a[Aspose.PSD letöltési oldal](https://releases.aspose.com/psd/java/).
3. Integrált fejlesztői környezet (IDE): Bármely IDE, például az IntelliJ IDEA, az Eclipse vagy a NetBeans működik.
4.  Érvényes jogosítvány: Kaphat a[ideiglenes engedély](https://purchase.aspose.com/temporary-license/) ha nincs tele.
## Csomagok importálása
Először is importáljuk a szükséges csomagokat. Ezek lehetővé teszik számunkra a PSD-fájl kezeléséhez szükséges osztályok és módszerek használatát.
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
Most bontsuk le a példát több lépésre a jobb megértés érdekében.
## 1. lépés: Töltse be a PSD fájlt
 Először is be kell töltenünk a módosítani kívánt PSD-fájlt. Használjuk a`PsdLoadOptions` annak megadásához, hogy be akarjuk tölteni az effekt erőforrásokat.
```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "Stroke.psd";
String exportPath = dataDir + "StrokeGradientChanged.psd";
PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);
PsdImage im = (PsdImage) Image.load(sourceFileName, loadOptions);
```
## 2. lépés: A Stroke Effect elérése
Ezután el kell érnünk a minket érdeklő réteg körvonal-effektusát. Feltételezzük, hogy ez a harmadik réteg (2. index) a PSD-fájlban.
```java
StrokeEffect gradientStroke = (StrokeEffect) im.getLayers()[2].getBlendingOptions().getEffects()[0];
```
## 3. lépés: Ellenőrizze a Stroke Effect tulajdonságait
Mielőtt bármilyen változtatást végrehajtana, ellenőrizze a körvonal-effektus tulajdonságait, hogy megbizonyosodjon arról, hogy a megfelelő beállításokat módosítjuk.
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
## 4. lépés: Módosítsa a színátmenet kitöltési beállításait
Most itt az ideje, hogy módosítsuk a színátmenet-kitöltés beállításait igényeinknek megfelelően. Megváltoztatjuk a színt, az átlátszatlanságot, a keverési módot és egyéb tulajdonságokat.
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
## 5. lépés: Szín- és átlátszósági pontok hozzáadása és módosítása
Adjunk hozzá új szín- és átlátszósági pontokat, és módosítsuk a meglévőket a kívánt színátmeneti hatás elérése érdekében.
```java
// Új színpont hozzáadása
GradientColorPoint colorPoint = fillSettings.addColorPoint();
colorPoint.setColor(Color.getGreen());
colorPoint.setLocation(4096);
colorPoint.setMedianPointLocation(75);
// Az előző pont helyének módosítása
fillSettings.getColorPoints()[1].setLocation(1899);
// Új átlátszósági pont hozzáadása
GradientTransparencyPoint transparencyPoint = fillSettings.addTransparencyPoint();
transparencyPoint.setOpacity(25);
transparencyPoint.setMedianPointLocation(25);
transparencyPoint.setLocation(4096);
// Módosítsa az előző átlátszósági pont helyét
fillSettings.getTransparencyPoints()[1].setLocation(2411);
```
## 6. lépés: Mentse el a módosított PSD-fájlt
Az összes szükséges módosítás elvégzése után el kell mentenünk a PSD fájlt.
```java
im.save(exportPath);
```
## 7. lépés: Ellenőrizze a módosításokat
Végül töltsük be a mentett PSD-fájlt, és ellenőrizzük, hogy a módosításainkat megfelelően alkalmaztuk-e.
```java
PsdImage img = (PsdImage) Image.load(exportPath, loadOptions);
StrokeEffect gradientStrokeEffect = (StrokeEffect) img.getLayers()[2].getBlendingOptions().getEffects()[0];
Assert.areEqual(BlendMode.Color, gradientStrokeEffect.getBlendMode());
Assert.areEqual(127, gradientStrokeEffect.getOpacity());
Assert.areEqual(true, gradientStrokeEffect.isVisible());
GradientFillSettings fillSetting = (GradientFillSettings) gradientStrokeEffect.getFillSettings();
Assert.areEqual(Color.getGreen(), fillSetting.getColor());
Assert.areEqual(FillType.Gradient, fillSetting.getFillType());
// Ellenőrizze a színpontokat
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
// Ellenőrizze az átlátszósági pontokat
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
## Következtetés
És megvan! Most már tudja, hogyan adhat hozzá és hogyan kezelheti a körvonal-réteg színátmeneteit PSD-fájlokban az Aspose.PSD for Java használatával. Ez az oktatóanyag a PSD-fájl betöltését, a körvonal-effektusok elérését és módosítását, valamint a változtatások mentését tárgyalta. Ezekkel a készségekkel tetszetős színátmeneteket hozhat létre, és az igényeinek megfelelően testreszabhatja PSD-fájljait.
## GYIK
### Mi az Aspose.PSD for Java?
Az Aspose.PSD for Java egy olyan könyvtár, amely lehetővé teszi a fejlesztők számára, hogy PSD-fájlokkal dolgozzanak Java-alkalmazásokban, és szolgáltatásokat biztosítva PSD-fájlok létrehozásához, kezeléséhez és konvertálásához.
### Szükségem van licencre az Aspose.PSD for Java használatához?
 Igen, érvényes licenc szükséges az Aspose.PSD for Java használatához. Kaphatsz a[ideiglenes engedély](https://purchase.aspose.com/temporary-license/) értékelési célokra.
### Használhatom az Aspose.PSD for Java-t PSD-fájlok létrehozásához a semmiből?
Teljesen! Az Aspose.PSD for Java átfogó API-kat biztosít a PSD-fájlok programozott létrehozásához és kezeléséhez.
### Lehetséges más effektusokat alkalmazni az Aspose.PSD for Java használatával?
Igen, az Aspose.PSD for Java segítségével különféle effektusokat, például árnyékot, ragyogást és egyebeket alkalmazhat.
### Hol találom az Aspose.PSD for Java dokumentációját?
 A dokumentációt megtalálod[itt](https://reference.aspose.com/psd/java/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
