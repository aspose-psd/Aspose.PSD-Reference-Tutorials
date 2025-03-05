---
title: Állítsa be a kép fényerejét az Aspose.PSD for Java segítségével
linktitle: Állítsa be a kép fényerejét
second_title: Aspose.PSD Java API
description: Növelje a kép fényerejét Java nyelven az Aspose.PSD segítségével. Útmutató lépésről lépésre a kép fényerejének programozott beállításához.
type: docs
weight: 21
url: /hu/java/advanced-techniques/adjust-brightness/
---
## Bevezetés

képek javítása általános követelmény a grafikai tervezésben és a digitális fényképezésben. Az Aspose.PSD for Java hatékony megoldást kínál a kép fényerejének programozott beállítására. Ebben az oktatóanyagban lépésről lépésre megvizsgáljuk, hogyan használhatjuk az Aspose.PSD for Java könyvtárat a kép fényerejének beállítására.

## Előfeltételek

Mielőtt belevágna az oktatóanyagba, győződjön meg arról, hogy rendelkezik a következő előfeltételekkel:

-  Aspose.PSD for Java Library: Töltse le és telepítse a könyvtárat a[Aspose.PSD a Java dokumentációhoz](https://reference.aspose.com/psd/java/).

## Csomagok importálása

Kezdésként importálja a szükséges csomagokat a Java projektbe. Ebben a példában a következőket fogjuk használni:

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.psd.fileformats.tiff.enums.TiffPhotometrics;
import com.aspose.psd.imageoptions.TiffOptions;
```

Most bontsuk le a kép fényerejének beállítását egyszerű lépésekre:

## 1. lépés: Töltse be a képet

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";
String destName = dataDir + "AdjustBrightness_out.tiff";

// Töltsön be egy meglévő képet a RasterImage osztály egy példányába
Image image = Image.load(sourceFile);
// Kép objektumának átküldése RasterImage-re
RasterImage rasterImage = (RasterImage) image;

// Ellenőrizze, hogy a RasterImage gyorsítótárban van-e, és tárolja a RasterImage-t a jobb teljesítmény érdekében
if (!rasterImage.isCached()) {
    rasterImage.cacheData();
}
```

 Ebben a lépésben betöltjük a célképet és leadjuk a`RasterImage` további feldolgozásra.

## 2. lépés: Állítsa be a fényerőt

```java
// Állítsa be a fényerőt
rasterImage.adjustBrightness(-50);
```

 Itt használjuk a`adjustBrightness`módszer a kép fényerejének módosítására. Ebben a példában 50 egységgel csökkentjük a fényerőt, de ezt az értéket az igényei szerint testreszabhatja.

## 3. lépés: Állítsa be a TiffOptions-t

```java
int[] ushort = {8, 8, 8};
// Hozzon létre egy TiffOptions példányt az eredményül kapott képhez
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
tiffOptions.setBitsPerSample(ushort);
tiffOptions.setPhotometric(TiffPhotometrics.Rgb);
```

 Konfigurálja a`TiffOptions` a beállított kép mentéséhez. Állítsa be a`bitsPerSample` és`photometric` az Ön egyedi igényei alapján.

## 4. lépés: Mentse el a kapott képet

```java
// Mentse el a kapott képet
rasterImage.save(destName, tiffOptions);
```

 Végül mentse el a módosított képet a megadott használatával`TiffOptions`.

## Következtetés

A kép fényerejének programozott beállítása egyszerű az Aspose.PSD for Java segítségével. Ez az oktatóanyag átfogó útmutatót nyújt ennek a funkciónak a Java-alkalmazásokban való megvalósításához.

## GYIK

### 1. kérdés: Beállíthatom a fényerőt a PSD-n kívül más képformátumokban is?

1. válasz: Igen, az Aspose.PSD for Java különféle képformátumokat támogat, mint például a JPEG, PNG és TIFF.

### 2. kérdés: Hogyan kezelhetem a hibákat a képbeállítási folyamat során?

2. válasz: A hibakezelést try-catch blokkokkal valósíthatja meg az esetlegesen előforduló kivételek kezelésére.

### 3. kérdés: Van-e korlátozás a fényerő beállítási tartományában?

3. válasz: A beállítási tartomány a kép tartalmától és formátumától függ, de az Aspose.PSD rugalmasságot biztosít a testreszabásban.

### 4. kérdés: Használhatom az Aspose.PSD for Java-t kereskedelmi projektekben?

 4. válasz: Igen, az Aspose.PSD for Java egy kereskedelmi könyvtár, és licencet szerezhet be[itt](https://purchase.aspose.com/buy).

### 5. kérdés: Elérhető az Aspose.PSD for Java ingyenes próbaverziója?

 5. válasz: Igen, felfedezheti a könyvtárat egy ingyenes próbaverzióval[itt](https://releases.aspose.com/).