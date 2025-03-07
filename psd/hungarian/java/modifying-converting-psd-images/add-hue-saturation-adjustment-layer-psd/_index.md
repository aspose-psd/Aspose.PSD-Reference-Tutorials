---
title: Adja hozzá a színtelítettség korrekciós réteget a PSD-hez
linktitle: Adja hozzá a színtelítettség korrekciós réteget a PSD-hez
second_title: Aspose.PSD Java API
description: Ebben az átfogó, lépésenkénti oktatóanyagban megtudhatja, hogyan adhat hozzá színtelítettség-beállító rétegeket a PSD-hez az Aspose.PSD for Java segítségével. Javítsa grafikai tervezési munkafolyamatát.
weight: 14
url: /hu/java/modifying-converting-psd-images/add-hue-saturation-adjustment-layer-psd/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Adja hozzá a színtelítettség korrekciós réteget a PSD-hez

## Bevezetés
Ami a grafikai tervezést illeti, a színmanipuláció kulcsszerepet játszik – konkrétan az árnyalat, a telítettség és a világosság módosítása drasztikusan megváltoztathatja bármely kép hangulatát és minőségét. Ennek egyik hatékony módja a Photoshop korrekciós rétegeinek (PSD-fájlok) használata. Ha szeretné programozottan javítani PSD-fájljain a Java használatával, az Aspose.PSD könyvtár segít! Ez az oktatóanyag végigvezeti Önt azokon a lépéseken, amelyekkel színtelítettségi korrekciós réteget adhat hozzá PSD-fájlokhoz, így munkafolyamatait termelékenyebbé és hatékonyabbá teheti.
Ebben az útmutatóban mindent lefedünk, a szükséges csomagok importálásától a kódpéldák aprólékos részleteiig.
## Előfeltételek
Mielőtt belevágnánk a kódba, győződjön meg arról, hogy a következő a helyén van:
1.  Java Development Kit (JDK): Győződjön meg arról, hogy a JDK 8 vagy újabb verziója telepítve van a gépére. Letöltheti a[Java SE fejlesztőkészlet letöltések](https://www.oracle.com/java/technologies/javase-downloads.html).
2.  Aspose.PSD for Java Library: rendelkeznie kell az Aspose.PSD könyvtárral, amelyet[letöltés itt](https://releases.aspose.com/psd/java/). 
3. IDE: Megfelelő integrált fejlesztői környezet (IDE), például az IntelliJ IDEA vagy az Eclipse a Java fejlesztéshez.
4. Alapszintű Java ismeretek: A Java programozás ismerete előnyt jelent, de ne aggódjon; lépésről lépésre végigvezetjük a kódon.
Most, hogy az előfeltételeinket rendeztük, térjünk át a szórakoztató részre – a kódolásra!
## Csomagok importálása
Az Aspose.PSD könyvtárral való munka megkezdéséhez az első lépés a szükséges osztályok importálása. Ezt a következőképpen teheti meg a Java fájlban:
```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.adjustmentlayers.HueSaturationLayer;
import com.aspose.psd.fileformats.psd.layers.layerresources.ColorRangeHsl;
```
Győződjön meg arról, hogy a megfelelő könyvtárakat hozzáadta a projekthez, hogy ezek az importálások zökkenőmentesen működjenek.
## 1. lépés: Állítsa be a dokumentumkönyvtárat
Minden projektnek szüksége van egy kiindulási pontra, ez alól a miénk sem kivétel. Meg kell adnia egy könyvtárat, ahol a PSD-fájlokat tárolja. Ez kulcsfontosságú a képek megfelelő betöltéséhez és mentéséhez.
```java
String dataDir = "Your Document Directory"; // Frissítse ezt az elérési utat a tényleges könyvtárhoz
```
## 2. lépés: Töltsön be egy meglévő PSD-fájlt
Egy meglévő PSD-fájl kezeléséhez először be kell töltenünk a programunkba. Ezt a következőképpen teheti meg:
```java
String sourceFileName = dataDir + "HueSaturationAdjustmentLayer.psd";
PsdImage im = (PsdImage) Image.load(sourceFileName);
```
 Ebben a kódban frissítse`"HueSaturationAdjustmentLayer.psd"` a szerkeszteni kívánt meglévő PSD-fájl nevére.
## 3. lépés: Szerkessze az árnyalat/telítettség réteget
Ezután végigpörgetjük a betöltött PSD-képünk rétegeit, hogy megkeressük és szerkeszthessük a meglévő színárnyalat/telítettség rétegeket. Ez a lépés magában foglalja a színárnyalat, a telítettség és a világosság értékek módosítását.
```java
for (int i = 0; i < im.getLayers().length; i++) {
    if (im.getLayers()[i] instanceof HueSaturationLayer) {
        HueSaturationLayer hueLayer = (HueSaturationLayer) im.getLayers()[i];
        hueLayer.setHue((short) -25);
        hueLayer.setSaturation((short) -12);
        hueLayer.setLightness((short) 67);
        ColorRangeHsl colorRange = hueLayer.getRange(2);
        colorRange.setHue((short) -40);
        colorRange.setSaturation((short) 50);
        colorRange.setLightness((short) -20);
        colorRange.setMostLeftBorder((short) 300);
    }
}
```
Ebben a példában:
- A színárnyalatot -25-re, a telítettséget -12-re, a világosságot pedig +67-re állítjuk.
-  A`getRange(2)` módszer lehetővé teszi, hogy tetszés szerint módosítsunk bizonyos színtartományokat.
## 4. lépés: Mentse el a módosított PSD-fájlt
A beállítások elvégzése után a következő lépés a fájl mentése. Ez folyamatunk létfontosságú része, amely biztosítja, hogy az általunk végrehajtott változtatások ne vesszenek el.
```java
String psdPathAfterChange = dataDir + "HueSaturationAdjustmentLayerChanged.psd";
im.save(psdPathAfterChange);
```
## 5. lépés: Új színárnyalat/telítettségi réteg hozzáadása
Ezután érdemes lehet egy új színárnyalat/telítettség beállító réteget hozzáadni egy másik PSD-fájlhoz. Csak kövesse ugyanazt a megközelítést, amelyet korábban használt, de különböző PSD-fájlokkal.
```java
sourceFileName = dataDir + "PhotoExample.psd";
PsdImage img = (PsdImage) Image.load(sourceFileName);
HueSaturationLayer hueLayerNew = img.addHueSaturationAdjustmentLayer();
```
## 6. lépés: Állítson be új árnyalat/telítettség értékeket az új réteghez
Most, hogy létrehozta ezt az új réteget, ugyanúgy alkalmazza a kívánt színárnyalat, telítettség és világosság beállításokat, mint korábban.
```java
hueLayerNew.setHue((short) -25);
hueLayerNew.setSaturation((short) -12);
hueLayerNew.setLightness((short) 67);
ColorRangeHsl newColorRange = hueLayerNew.getRange(2);
newColorRange.setHue((short) -160);
newColorRange.setSaturation((short) 100);
newColorRange.setLightness((short) 20);
newColorRange.setMostLeftBorder((short) 300);
```
## 7. lépés: Mentse el a frissített PSD-fájlt
Végül mentse el a PSD-fájlt a hozzáadott színárnyalat/telítettség réteggel, hogy láthassa a módosításokat.
```java
String psdPathAfterNewLayerChange = dataDir + "PhotoExampleAddedHueSaturation.psd";
img.save(psdPathAfterNewLayerChange);
```
Gratulálok! Sikeresen kezelte a PSD-fájlokat az Aspose.PSD for Java használatával. Most már kísérletezhet különböző képekkel és mélyebb módosításokkal, életre keltve grafikai tervezési projektjeit.
## Következtetés
grafikus programozással végzett munka a lehetőségek világát nyitja meg. Az Aspose.PSD for Java használata Hue Saturation Adjustment Layers hozzáadásához és módosításához olyan rugalmasságot és hatékonyságot biztosít, amely egyszerűsítheti a tervezési munkafolyamatot. Akár fotókat javít egy projekthez, akár lenyűgöző vizuális tartalmat hoz létre, ezen eszközök elsajátítása nagymértékben javíthatja a teljesítményt.
 Nyugodtan fedezze fel az Aspose.PSD további funkcióit[dokumentáció](https://reference.aspose.com/psd/java/) vagy fontolóra veszi az elcsípést a[ideiglenes engedély](https://purchase.aspose.com/temporary-license/) hogy kipróbálja a könyvtár teljes erejét.
## GYIK
### Mi az a színárnyalat-telítettség-beállító réteg?
A Hue Saturation Adjustment Layer lehetővé teszi a kép színtulajdonságainak módosítását anélkül, hogy az eredeti pixeleket véglegesen megváltoztatná.
### Az Aspose.PSD használatához telepíteni kell a Photoshop programot?
Nem, az Aspose.PSD egy önálló könyvtár, amely a Photoshoptól függetlenül működik.
### Használhatom az Aspose.PSD-t kötegelt feldolgozáshoz?
Igen, automatizálhat és kötegelt feldolgozhat több PSD-fájlt az Aspose.PSD segítségével.
### Az Aspose.PSD ingyenes?
Az Aspose.PSD ingyenes próbaverziót kínál, de a hosszú távú használathoz licenc szükséges. Megtekintheti az árakat[itt](https://purchase.aspose.com/buy).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
