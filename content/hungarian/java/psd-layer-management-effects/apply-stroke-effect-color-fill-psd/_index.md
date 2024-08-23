---
title: Alkalmazza a Stroke Effect színkitöltést a PSD-ben - Java
linktitle: Alkalmazza a Stroke Effect színkitöltést a PSD-ben - Java
second_title: Aspose.PSD Java API
description: Ismerje meg, hogyan alkalmazhat körvonal-effektust színkitöltéssel a PSD-fájlokra az Aspose.PSD for Java segítségével. Kövesse ezt a lépésenkénti útmutatót a képek egyszerű javításához.
type: docs
weight: 21
url: /hu/java/psd-layer-management-effects/apply-stroke-effect-color-fill-psd/
---
## Bevezetés

Ebben az útmutatóban végigvezetjük az Aspose.PSD for Java használatával színkitöltésű körvonal-effektus alkalmazásának folyamatán a PSD-fájlokon. Akár tapasztalt fejlesztő vagy, akár csak most kezded, ez a lépésről lépésre ismertetett oktatóanyag megkönnyíti a munka elvégzését. A környezet beállításától a végső kép elmentéséig az alkalmazott effektusokkal mindenre kiterjedünk.

## Előfeltételek

Mielőtt elkezdené, győződjön meg arról, hogy mindent megvan, ami ehhez az oktatóanyaghoz szükséges:

1. Java Development Kit (JDK) telepítve: Győződjön meg arról, hogy a JDK 8 vagy újabb verziója van telepítve a rendszerére.
2.  Aspose.PSD for Java Library: Szüksége lesz az Aspose.PSD for Java könyvtárra. Letöltheti a[weboldal](https://releases.aspose.com/psd/java/).
3. Integrált fejlesztőkörnyezet (IDE): Olyan IDE, mint az IntelliJ IDEA, az Eclipse vagy bármely más, amit választott.
4. Minta PSD-fájl: PSD-mintafájl, amelyre a körvonal-effektust alkalmazhatja. Ha nem rendelkezik ilyennel, létrehozhat egy egyszerű PSD-fájlt a Photoshopban, vagy letölthet egyet az internetről.
5. Alapvető Java ismerete: Bár ez az oktatóanyag kezdők számára készült, a Java alapismeretei hasznosak lesznek.

Ha megvannak ezek az előfeltételek, készen áll a körvonal-effektus színkitöltéses alkalmazására a PSD-fájlokon.

## Csomagok importálása

Az Aspose.PSD for Java használatához importálnia kell a szükséges csomagokat a Java-projektbe. A következőképpen teheti meg:

```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.fillsettings.ColorFillSettings;
import com.aspose.psd.fileformats.psd.layers.layereffects.StrokeEffect;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
import com.aspose.psd.imageoptions.PngOptions;
import com.aspose.psd.imageoptions.PsdOptions;
```

Ezek az importálások behozzák az összes szükséges osztályt, amelyre szüksége lesz a PSD-fájlokkal való munkavégzéshez, az effektusok alkalmazásához és a képek kívánt formátumban történő mentéséhez.

## 1. lépés: Töltse be a PSD fájlt

 A folyamat első lépése a módosítani kívánt PSD-fájl betöltése. Az Aspose.PSD for Java ezt hihetetlenül egyszerűvé teszi`PsdImage` osztály. A következőképpen teheti meg:

### 1.1 Állítsa be a könyvtár elérési útját

Először határozza meg a könyvtár elérési útját, ahol a PSD-fájlok tárolásra kerülnek:

```java
String dataDir = "Your Document Directory";
```

 Cserélje ki`"Your Document Directory"` a PSD-fájl tényleges elérési útjával.

### 1.2 Töltse be a PSD-képet

 Most töltse be a PSD-fájlt a`PsdLoadOptions` és`PsdImage` osztályok:

```java
String sourceFileName = dataDir + "StrokeComplex.psd";

PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);

PsdImage im = (PsdImage) Image.load(sourceFileName, loadOptions);
```

 Itt, a`PsdLoadOptions`úgy van beállítva, hogy betöltse az effektus-erőforrásokat, biztosítva, hogy a PSD-n belül minden meglévő effekt elérhető legyen.

## 2. lépés: Alkalmazza a Stroke Effect-et színkitöltéssel

A PSD fájl betöltése után a következő lépés a körvonal effektus alkalmazása a kép rétegeire. Itt történik az igazi varázslat.

Minden PSD-fájl több réteget is tartalmazhat, és mindegyikre alkalmaznia kell a hatást. Íme, hogyan kell csinálni:

```java
for (int i = 0; i < im.getLayers().length; i++) {
    StrokeEffect effect = (StrokeEffect) im.getLayers()[i].getBlendingOptions().getEffects()[0];
    ColorFillSettings settings = (ColorFillSettings) effect.getFillSettings();
    settings.setColor(Color.getDeepPink());
}
```

Ebben a körben:

- `im.getLayers()`: A PSD-fájl összes rétegét lekéri.
- `StrokeEffect effect`: Kivonja a rétegre alkalmazott körvonal-effektust.
- `ColorFillSettings settings`: Módosítja a körvonal-effektus kitöltési beállításait.
- `settings.setColor(Color.getDeepPink())`: A körvonal színét mély rózsaszínre állítja. Ezt bármilyen kívánt színre módosíthatja.

## 3. lépés: Mentse el a módosított PSD-t, és exportálja PNG-ként

Miután alkalmazta a körvonal-effektust, ideje menteni a változtatásokat és exportálni a képet.

### 3.1 Mentse el a PSD-fájlt

A módosított PSD-fájl mentéséhez használja a következő kódot:

```java
String exportPath = dataDir + "StrokeComplexRendering.psd";
im.save(exportPath, new PsdOptions());
```

Ez elmenti a fájlt az alkalmazott körvonal-effektussal a megadott elérési útra.

### 3.2 Exportálás PNG formátumban

A kép hozzáférhetőbbé tétele érdekében érdemes lehet PNG-fájlként exportálni. Íme, hogyan:

```java
String exportPathPng = dataDir + "StrokeComplexRendering.png";
PngOptions option = new PngOptions();
option.setColorType(PngColorType.TruecolorWithAlpha);

im.save(exportPathPng, option);
```

Ez a kódrészlet PNG formátumban menti el a képet valódi színekkel és alfa-átlátszósággal, így készen áll a webalkalmazásokban vagy más platformokon való használatra.

## Következtetés

Az Aspose.PSD for Java segítségével körvonal-effektus színkitöltéssel történő alkalmazása a PSD-fájlokon nem csak egyszerű, hanem hihetetlenül hatékony is. Néhány sornyi kóddal automatizálhatja az összetett képfeldolgozási feladatokat, így időt és erőfeszítést takarít meg.

Akár nagy köteg képen dolgozik, akár csak néhány fájlt kell módosítania, ez a módszer rugalmas és hatékony megoldást kínál. Most, hogy megvan az alapismeretek, elkezdhet kísérletezni a különböző effektusokkal és testreszabásokkal, hogy a képek valóban kitűnjenek.

Készen áll a kipróbálására? Fogja meg a minta PSD-fájlt, és kezdje el hozzáadni ezeket a lenyűgöző effektusokat még ma!

## GYIK

### Alkalmazhatok több effektust egyetlen rétegre az Aspose.PSD for Java használatával?
Igen, több effektust is alkalmazhat egyetlen rétegre, ha eléri a réteg keverési beállításait, és hozzáadja a kívánt effektusokat.

### Lehetséges-e automatizálni a folyamatot egy köteg PSD-fájl esetén?
Teljesen! Végigpörgethet egy PSD-fájlok könyvtárát, alkalmazhatja a körvonal-effektust, és automatikusan mentheti az eredményeket.

### Hogyan állíthatom vissza a PSD-fájlban végrehajtott módosításokat az Aspose.PSD for Java használatával?
A módosítások visszaállításához újra kell töltenie az eredeti PSD-fájlt a módosítások mentése előtt. Az Aspose.PSD-ben nincs közvetlen visszavonási funkció.

### Testreszabhatom a löket szélességét és pozícióját?
 Igen, az Aspose.PSD for Java lehetővé teszi a körvonal szélességének, pozíciójának és egyéb tulajdonságainak testreszabását a`StrokeEffect` osztály.

### Ingyenesen használható az Aspose.PSD for Java könyvtár?
 Az Aspose.PSD for Java ingyenes próbaverziót kínál, de az összes funkcióhoz való teljes hozzáféréshez licencet kell vásárolnia. Feltárhatod a[opciók vásárlása](https://purchase.aspose.com/buy) honlapjukon.