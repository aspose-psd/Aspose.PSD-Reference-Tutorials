---
title: Állítsa be a kép kontrasztját az Aspose.PSD for Java segítségével
linktitle: Állítsa be a kép kontrasztját
second_title: Aspose.PSD Java API
description: Fedezze fel a képkontraszt beállításának világát Java nyelven az Aspose.PSD segítségével. Kövesse lépésről lépésre útmutatónkat a zökkenőmentes képkezeléshez.
type: docs
weight: 22
url: /hu/java/advanced-techniques/adjust-contrast/
---
## Bevezetés

Java képfeldolgozás területén az Aspose.PSD hatékony eszközként tűnik ki. Számtalan funkciója között gyakori követelmény a kép kontrasztjának beállítása. Ez az oktatóanyag végigvezeti a képkontraszt beállításának folyamatán az Aspose.PSD for Java használatával. Akár tapasztalt fejlesztő, akár csak kezdő, ez az útmutató segít elsajátítani a képmanipuláció ezen alapvető aspektusát.

## Előfeltételek

Mielőtt belevágna az oktatóanyagba, győződjön meg arról, hogy a következő előfeltételek teljesülnek:

- A Java programozás alapvető ismerete.
-  Aspose.PSD for Java könyvtár telepítve. Letöltheti[itt](https://releases.aspose.com/psd/java/).

## Csomagok importálása

A kezdéshez importálnia kell a szükséges csomagokat a Java projektbe. Adja hozzá a következő sorokat a kódhoz:

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.psd.fileformats.tiff.enums.TiffPhotometrics;
import com.aspose.psd.imageoptions.TiffOptions;
```

## 1. lépés: Töltse be a képet

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

// Töltsön be egy meglévő képet a RasterImage osztály egy példányába
Image image = Image.load(sourceFile);
```

 Ebben a lépésben betöltjük a mintaképet ("sample.psd") a`Image.load` módszer.

## 2. lépés: Átküldés a RasterImage-be és a Cache Databa

```java
// Kép objektumának átküldése RasterImage-re
RasterImage rasterImage = (RasterImage)image;

// Ellenőrizze, hogy a RasterImage gyorsítótárban van-e, és tárolja a RasterImage-t a jobb teljesítmény érdekében
if (!rasterImage.isCached()) {
    rasterImage.cacheData();
}
```

 Itt megadjuk az általánost`Image` tiltakozik a`RasterImage` speciális feldolgozásra. A képadatok gyorsítótárazása javítja a teljesítményt.

## 3. lépés: Állítsa be a kontrasztot

```java
// Állítsa be a kontrasztot
rasterImage.adjustContrast(50);
```

 A`adjustContrast`módszer a kép kontrasztjának módosítására szolgál. Ebben a példában a kontraszt 50%-kal nő.

## 4. lépés: Hozzon létre TiffOptions és Mentse

```java
// Hozzon létre egy TiffOptions példányt az eredményül kapott képhez
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
int[] ushort = { 8, 8, 8 };
tiffOptions.setBitsPerSample(ushort);
tiffOptions.setPhotometric(TiffPhotometrics.Rgb);

// Mentse az eredményül kapott képet TIFF formátumba
String destName = dataDir + "AdjustContrast_out.tiff";
rasterImage.save(destName, tiffOptions);
```

 Tessék, beállítjuk`TiffOptions` a kimeneti képhez a formátum és egyéb tulajdonságok megadásával. A végső kép ezután egy TIFF fájlba kerül.

## Következtetés

Gratulálok! Sikeresen beállította egy kép kontrasztját az Aspose.PSD for Java segítségével. Ez az oktatóanyag a legfontosabb lépéseket ismertette, a csomagok importálásától a feldolgozott kép mentéséig.

## GYIK

### 1. kérdés: Az Aspose.PSD kompatibilis a különböző képformátumokkal?

1. válasz: Igen, az Aspose.PSD különféle képformátumokat támogat, így rugalmasságot biztosít a projektekben.

### 2. kérdés: Hogyan szerezhetek ideiglenes licencet az Aspose.PSD-hez?

 V2: Kaphat ideiglenes engedélyt[itt](https://purchase.aspose.com/temporary-license/).

### 3. kérdés: Hol találom az Aspose.PSD dokumentációt?

A3: A dokumentáció elérhető[itt](https://reference.aspose.com/psd/java/).

### 4. kérdés: Milyen támogatási lehetőségek állnak rendelkezésre az Aspose.PSD számára?

 A4: Támogatásért keresse fel a[Aspose.PSD fórum](https://forum.aspose.com/c/psd/34).

### 5. kérdés: Megvásárolhatom az Aspose.PSD-t?

 V5: Igen, megvásárolhatja az Aspose.PSD-t[itt](https://purchase.aspose.com/buy).