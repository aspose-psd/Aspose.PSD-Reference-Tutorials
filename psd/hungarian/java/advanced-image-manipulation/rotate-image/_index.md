---
title: Kép forgatása az Aspose.PSD for Java fájlban
linktitle: Kép elforgatása
second_title: Aspose.PSD Java API
description: Fedezze fel a Java képforgatását könnyedén az Aspose.PSD segítségével. Forgassa el, fordítsa meg és mentse el a PSD-fájlokat egyszerűen.
weight: 19
url: /hu/java/advanced-image-manipulation/rotate-image/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Kép forgatása az Aspose.PSD for Java fájlban

## Bevezetés

Az Aspose.PSD for Java hatékony funkciókat kínál a képekkel való munkavégzéshez, lehetővé téve a fejlesztők számára a PSD-fájlok hatékony kezelését és feldolgozását. Ebben az oktatóanyagban egy konkrét feladatra összpontosítunk: egy kép elforgatására. Függetlenül attól, hogy fotószerkesztő alkalmazást épít, vagy egyszerűen csak a kép tájolását kell módosítania, az Aspose.PSD egyszerűvé teszi a folyamatot.

## Előfeltételek

Mielőtt belevágna az oktatóanyagba, győződjön meg arról, hogy a következő előfeltételeket teljesítette:

-  Aspose.PSD for Java Library: Győződjön meg arról, hogy letöltötte és telepítette az Aspose.PSD for Java könyvtárat. Megtalálható a könyvtár és a részletes dokumentáció[itt](https://reference.aspose.com/psd/java/).

- Java fejlesztői környezet: Győződjön meg arról, hogy be van állítva Java fejlesztői környezet a gépén.

-  Minta PSD-fájl: Készítsen egy minta PSD-fájlt, amelyet el szeretne forgatni. Állítsa be a`sourceFile` változót a példakódban a PSD-fájl elérési útjával.

## Csomagok importálása

Kezdje a szükséges csomagok importálásával, hogy kihasználja az Aspose.PSD képességeit:

```java
import com.aspose.psd.Image;
import com.aspose.psd.RotateFlipType;

import com.aspose.psd.imageoptions.JpegOptions;
```

## 1. lépés: Töltse be a képet

 Töltse be a meglévő képet a`Image` osztály:

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";
Image image = Image.load(sourceFile);
```

## 2. lépés: Forgassa el a képet

 Forgassa el a képet a gombbal`rotateFlip` módszer. Ebben a példában 270 fokkal elforgatjuk a képet:

```java
image.rotateFlip(RotateFlipType.Rotate270FlipNone);
```

## 3. lépés: Mentse el az elforgatott képet

 Mentse el az elforgatott képet a`save` módszer és a kimeneti formátum megadása (jelen esetben JPEG):

```java
String destName = dataDir + "RotatedImage_out.jpg";
image.save(destName, new JpegOptions());
```

## Következtetés

Gratulálok! Sikeresen elforgatott egy képet az Aspose.PSD for Java használatával. Ez az egyszerű, de hatékony könyvtár a lehetőségek világát nyitja meg a Java-alkalmazások képkezelésére.

## GYIK

### 1. kérdés: Az Aspose.PSD kompatibilis a különböző képformátumokkal?

1. válasz: Igen, az Aspose.PSD különféle képformátumokat támogat, beleértve a PSD-t, JPEG-et, PNG-t stb.

### 2. kérdés: Alkalmazhatok egyéni elforgatásokat, nem csak előre meghatározott flipeket?

A2: Abszolút! Az Aspose.PSD rugalmasságot biztosít az egyedi elforgatások alkalmazásához, hogy megfeleljen az Ön egyedi igényeinek.

### 3. kérdés: Hol találhatok további támogatást vagy segítséget?

 3. válasz: Bármilyen kérdés vagy probléma esetén keresse fel a[Aspose.PSD fórum](https://forum.aspose.com/c/psd/34) közösségi támogatásért.

### 4. kérdés: Van ingyenes próbaverzió?

 4. válasz: Igen, felfedezheti az Aspose.PSD-t a[ingyenes próbaverzió](https://releases.aspose.com/).

### 5. kérdés: Hogyan szerezhetek ideiglenes engedélyt?

 V5: Ha ideiglenes engedélyre van szüksége, beszerezhet egyet[itt](https://purchase.aspose.com/temporary-license/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
