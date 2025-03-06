---
title: Állítsa be a kép gammáját az Aspose.PSD for Java segítségével
linktitle: Kép gamma beállítása
second_title: Aspose.PSD Java API
description: Tanulja meg könnyedén beállítani a kép gammát az Aspose.PSD for Java használatával. Kövesse lépésről lépésre útmutatónkat az optimális eredmény érdekében.
weight: 23
url: /hu/java/advanced-techniques/adjust-gamma/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Állítsa be a kép gammáját az Aspose.PSD for Java segítségével

## Bevezetés

A képfeldolgozás területén a kép gammájának beállítása kulcsfontosságú lépés a vizuális vonzerő fokozása érdekében. Az Aspose.PSD for Java hatékony megoldást kínál a Java fejlesztők számára a kép gamma könnyed manipulálására. Ebben az oktatóanyagban megvizsgáljuk, hogyan állíthatjuk be a gammát az Aspose.PSD használatával, és az egyes lépéseket lebontjuk a zökkenőmentes megvalósítás érdekében.

## Előfeltételek

Mielőtt belevágna az oktatóanyagba, győződjön meg arról, hogy beállította a következő előfeltételeket:

1. Java fejlesztői környezet: Győződjön meg arról, hogy Java fejlesztői környezet van telepítve a rendszerére.
2.  Aspose.PSD Library: Töltse le és integrálja az Aspose.PSD könyvtárat Java projektjébe. A szükséges forrásokat megtalálja a[dokumentáció](https://reference.aspose.com/psd/java/).
3. Mintakép: Készítsen minta PSD-képet, amelyet a gamma-korrekció alkalmazásához fog használni.

## Csomagok importálása

folyamat elindításához importálja a szükséges csomagokat a Java projektbe. Ez megteremti a terepet az Aspose.PSD funkciók zökkenőmentes használatához.

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.psd.fileformats.tiff.enums.TiffPhotometrics;
import com.aspose.psd.imageoptions.TiffOptions;
```

## 1. lépés: Töltse be a képet

 Kezdje azzal, hogy betölti a minta PSD-képet a példány egy példányába`RasterImage` osztály. Ez az alapja a későbbi gamma-beállításoknak.

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

// Töltsön be egy meglévő képet a RasterImage osztály egy példányába
Image image = Image.load(sourceFile);

// Kép objektumának átküldése RasterImage-re
RasterImage rasterImage = (RasterImage)image;

// Ellenőrizze, hogy a RasterImage gyorsítótárban van-e a jobb teljesítmény érdekében
if (!rasterImage.isCached()) {
    rasterImage.cacheData();
}
```

## 2. lépés: A gamma beállítása

 Most állítsa be a betöltött kép gammáját a gombbal`adjustGamma` módszer. Finomhangolja a gamma értékeket igényei szerint.

```java
// Állítsa be a gammát
rasterImage.adjustGamma(2.2f, 2.2f, 2.2f);
```

## 3. lépés: Hozzon létre TiffOptions

 Hozzon létre egy példányt a`TiffOptions` az eredményül kapott képhez. Állítson be különféle tulajdonságokat, például bit/minta és fotometriai beállításokat, hogy a kimenetet az Ön specifikációihoz igazítsa.

```java
// Hozzon létre egy TiffOptions példányt az eredményül kapott képhez
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
int[] ushort = { 8, 8, 8 };
tiffOptions.setBitsPerSample(ushort);
tiffOptions.setPhotometric(TiffPhotometrics.Rgb);
```

## 4. lépés: Mentse el a kapott képet

 Mentse el a manipulált képet TIFF formátumba a korábban definiált módon`TiffOptions`.

```java
// Mentse az eredményül kapott képet TIFF formátumba
String destName = dataDir + "AdjustGamma_out.tiff";
rasterImage.save(destName, tiffOptions);
```

## Következtetés

Gratulálok! Sikeresen beállította egy kép gammáját az Aspose.PSD for Java használatával. Ez a folyamat lehetővé teszi a fejlesztők számára, hogy erőfeszítés nélkül javítsák a képminőséget, hozzájárulva a vizuálisan tetszetős felhasználói élményhez.

## GYIK

### 1. kérdés: Hol találom az Aspose.PSD dokumentációt?

 V1: A dokumentációt a címen érheti el[https://reference.aspose.com/psd/java/](https://reference.aspose.com/psd/java/).

### 2. kérdés: Hogyan tölthetem le az Aspose.PSD for Java-t?

 2. válasz: Töltse le a könyvtárat innen[https://releases.aspose.com/psd/java/](https://releases.aspose.com/psd/java/).

### 3. kérdés: Hol vásárolhatom meg az Aspose.PSD-t?

 A3: Látogassa meg[https://purchase.aspose.com/buy](https://purchase.aspose.com/buy) hogy megvásárolja az Aspose.PSD-t.

### 4. kérdés: Van ingyenes próbaverzió?

 4. válasz: Igen, felfedezheti az ingyenes próbaverziót a címen[https://releases.aspose.com/](https://releases.aspose.com/).

### 5. kérdés: Hol kérhetek támogatást az Aspose.PSD-hez?

 5. válasz: Támogatásért keresse fel az Aspose.PSD fórumot a címen[https://forum.aspose.com/c/psd/34](https://forum.aspose.com/c/psd/34).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
