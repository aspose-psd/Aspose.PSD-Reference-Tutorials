---
title: Kontrasztbeállítás megvalósítása az Aspose.PSD for .NET-ben
linktitle: A kontrasztbeállítás végrehajtása
second_title: Aspose.PSD .NET API
description: Ebből a lépésről lépésre szóló útmutatóból megtudhatja, hogyan valósíthatja meg a kontraszt beállítását az Aspose.PSD for .NET-ben.
type: docs
weight: 11
url: /hu/net/image-adjustment/contrast-adjustment/
---
## Bevezetés

Üdvözöljük ebben az átfogó útmutatóban az Aspose.PSD for .NET kontrasztbeállításának megvalósításáról! Ebben az oktatóanyagban a kép kontrasztjának növelésének folyamatát vizsgáljuk meg az Aspose.PSD, egy hatékony .NET képalkotási könyvtár használatával. Az útmutató végére alapos ismerete lesz arról, hogyan alkalmazhat zökkenőmentesen kontrasztbeállításokat a képeken.

## Előfeltételek

Mielőtt belemerülnénk a lépésről lépésre történő folyamatba, győződjön meg arról, hogy a következő előfeltételekkel rendelkezik:

1.  Aspose.PSD for .NET Library: Töltse le és telepítse az Aspose.PSD for .NET könyvtárat. A letöltési linket megtalálod[itt](https://releases.aspose.com/psd/net/).

2. Dokumentumkönyvtár: Állítson be egy könyvtárat, ahol a forrás- és célfájlok tárolódnak. Cserélje le a „Saját dokumentumkönyvtárat” a megadott kódban a könyvtár elérési útjával.

Most, hogy az előfeltételeink rendben vannak, folytassuk a megvalósítást.

## Névterek importálása

Ebben a lépésben importáljuk a szükséges névtereket az Aspose.PSD könyvtár által biztosított funkciók eléréséhez.

```csharp
using Aspose.PSD.FileFormats.Tiff.Enums;
using Aspose.PSD.ImageOptions;
```

## 1. lépés: Töltse be a képet

 Töltse be a forrásképet a`RasterImage` osztály.

```csharp
//ExStart:LoadImage
string sourceFile = dataDir + @"sample.psd";
using (var image = Image.Load(sourceFile))
{
    RasterImage rasterImage = (RasterImage)image;
    if (!rasterImage.IsCached)
    {
        rasterImage.CacheData();
    }
    // Folytassa a következő lépéssel...
}
//ExEnd:Image betöltése
```

## 2. lépés: Állítsa be a kontrasztot

Ebben a lépésben a betöltött kép kontrasztját állítjuk be.

```csharp
//ExStart: AdjustContrast
rasterImage.AdjustContrast(50); // Állítsa be a kontrasztot 50%-kal
// Folytassa a következő lépéssel...
//ExEnd: AdjustContrast
```

## 3. lépés: Hozzon létre TIFF-beállításokat

 Hozzon létre egy példányt a`TiffOptions` az eredményül kapott képhez állítson be különböző tulajdonságokat, és mentse el a képet TIFF formátumban.

```csharp
//ExStart:CreateTiffOptions
string destName = dataDir + @"AdjustContrast_out.tiff";
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
tiffOptions.BitsPerSample = new ushort[] { 8, 8, 8 };
tiffOptions.Photometric = TiffPhotometrics.Rgb;
rasterImage.Save(destName, tiffOptions);
//ExEnd:CreateTiffOptions
```

Gratulálunk! Sikeresen végrehajtotta a kontrasztbeállítást az Aspose.PSD for .NET használatával.

## Következtetés

Ebben az oktatóanyagban megvizsgáltuk a képkontraszt növelésének folyamatát az Aspose.PSD for .NET segítségével. A könyvtár egyszerű módot kínál a képtulajdonságok manipulálására, lehetővé téve a fejlesztők számára, hogy tetszetős képeket hozzanak létre könnyedén.

## GYIK

### 1. kérdés: Az Aspose.PSD for .NET megfelelő kezdőknek?

1. válasz: Az Aspose.PSD for .NET fejlesztőbarát, így kezdők és tapasztalt fejlesztők számára egyaránt alkalmas.

### 2. kérdés: Használhatom az Aspose.PSD-t kereskedelmi projektekhez?

 2. válasz: Igen, az Aspose.PSD for .NET használható kereskedelmi projektekben. Az engedélyezés részleteiért látogasson el a webhelyre[itt](https://purchase.aspose.com/buy).

### 3. kérdés: Van ingyenes próbaverzió?

 3. válasz: Igen, felfedezheti az Aspose.PSD .NET ingyenes próbaverzióját[itt](https://releases.aspose.com/).

### 4. kérdés: Hol találok támogatást az Aspose.PSD for .NET számára?

 4. válasz: Keresse fel az Aspose.PSD for .NET támogatási fórumát[itt](https://forum.aspose.com/c/psd/34) segítségért.

### 5. kérdés: Hogyan szerezhetek ideiglenes engedélyt?

 V5: Szükség esetén ideiglenes engedélyt szerezhet[itt](https://purchase.aspose.com/temporary-license/).