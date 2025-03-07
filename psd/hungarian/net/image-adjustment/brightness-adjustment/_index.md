---
title: Fényerő-szabályozás megvalósítása az Aspose.PSD for .NET-ben
linktitle: Fényerő-szabályozás végrehajtása
second_title: Aspose.PSD .NET API
description: Fedezze fel az Aspose.PSD for .NET erejét a kép fényerejének beállításában. Kövesse lépésenkénti útmutatónkat a zökkenőmentes megvalósítás érdekében.
weight: 10
url: /hu/net/image-adjustment/brightness-adjustment/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Fényerő-szabályozás megvalósítása az Aspose.PSD for .NET-ben

## Bevezetés

A képattribútumok javítása és módosítása gyakori követelmény a különféle alkalmazásokban, és az Aspose.PSD for .NET hatékony megoldást kínál a PSD-fájlok zökkenőmentes kezeléséhez. Az egyik ilyen manipuláció a fényerő beállítása, amellyel könnyedén módosíthatja a kép fényerejét.

Ebben az oktatóanyagban végigvezetjük a fényerő beállításának folyamatát az Aspose.PSD for .NET használatával. Kövesse az alábbi lépéseket, hogy átfogó képet kapjon a fényerő-beállítások beépítéséről a PSD-fájlokba.

## Előfeltételek

Mielőtt belevágna az oktatóanyagba, győződjön meg arról, hogy a következő előfeltételek teljesülnek:

-  Aspose.PSD for .NET Library: Töltse le és telepítse az Aspose.PSD for .NET könyvtárat a[letöltési link](https://releases.aspose.com/psd/net/).

-  Dokumentumkönyvtár: Állítson be egy könyvtárat a PSD-fájlok tárolására, és frissítse a`dataDir` változót a megadott kódrészletben a dokumentumkönyvtár elérési útjával.

## Névterek importálása

.NET-projektben tartalmazza az Aspose.PSD funkció eléréséhez szükséges névtereket. Adja hozzá a következő névtereket a kódhoz:

```csharp
using Aspose.PSD.FileFormats.Psd;
using Aspose.PSD.FileFormats.Tiff.Enums;
using Aspose.PSD.ImageOptions;
```

Most bontsuk fel a példát több lépésre:

## 1. lépés: Töltse be a PSD fájlt

```csharp
// A dokumentumok könyvtárának elérési útja.
string dataDir = "Your Document Directory";
string sourceFile = dataDir + @"sample.psd";

// Töltse be a PSD-fájlt az Aspose.PSD használatával
using (var image = (PsdImage)Image.Load(sourceFile))
{
    // A további lépésekhez szükséges kód itt található
}
```

## 2. lépés: Szerezzen raszterképet

```csharp
// Szerezze meg a raszterképet a betöltött PSD-fájlból
RasterCachedImage rasterImage = image;
```

## 3. lépés: Állítsa be a fényerőt

```csharp
// Állítsa be a fényerő értékét. A fényerő elfogadott értékei a [-255, 255] tartományban vannak.
rasterImage.AdjustBrightness(-50);
```

## 4. lépés: Mentse el a módosított képet

```csharp
// Mentse el a módosított képet beállított fényerővel
string destName = dataDir + @"AdjustBrightness_out.tiff";
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
rasterImage.Save(destName, tiffOptions);
```

Most, hogy a példát kezelhető lépésekre bontottuk, az Aspose.PSD segítségével zökkenőmentesen integrálhatja a fényerő beállítását .NET-projektjébe.

## Következtetés

Az Aspose.PSD for .NET leegyszerűsíti a fényerő-beállítások végrehajtását a PSD-fájlokban. A fenti, lépésenkénti útmutató követésével könnyedén javíthatja képei látványosságát. Kísérletezzen különböző fényerőértékekkel a kívánt eredmény elérése érdekében.

## GYIK

### 1. kérdés: Hol találom az Aspose.PSD for .NET dokumentációját?

 V1: A dokumentáció elérhető[itt](https://reference.aspose.com/psd/net/).

### 2. kérdés: Hogyan tölthetem le az Aspose.PSD for .NET könyvtárat?

 2. válasz: A könyvtárat letöltheti a[kiadási oldal](https://releases.aspose.com/psd/net/).

### 3. kérdés: Elérhető ingyenes próbaverzió az Aspose.PSD for .NET számára?

 3. válasz: Igen, hozzáférhet az ingyenes próbaverzióhoz[itt](https://releases.aspose.com/).

### 4. kérdés: Hol kaphatok támogatást az Aspose.PSD for .NET számára?

 A4: Támogatásért keresse fel a[Aspose.PSD fórum](https://forum.aspose.com/c/psd/34).

### 5. kérdés: Hogyan szerezhetek ideiglenes licencet az Aspose.PSD for .NET számára?

 V5: Kaphat ideiglenes engedélyt[itt](https://purchase.aspose.com/temporary-license/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
