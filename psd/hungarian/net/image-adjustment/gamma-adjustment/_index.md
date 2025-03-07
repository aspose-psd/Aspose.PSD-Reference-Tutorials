---
title: Gamma-korrekció megvalósítása az Aspose.PSD for .NET-ben
linktitle: Gamma-beállítás végrehajtása
second_title: Aspose.PSD .NET API
description: Fedezze fel az Aspose.PSD for .NET erejét a Gamma Adjustment megvalósításáról szóló, lépésenkénti útmutatónkkal. Könnyedén finomhangolhatja a kép fényerejét és kontrasztját.
weight: 12
url: /hu/net/image-adjustment/gamma-adjustment/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Gamma-korrekció megvalósítása az Aspose.PSD for .NET-ben

## Bevezetés

Üdvözöljük ebben az átfogó útmutatóban az Aspose.PSD for .NET gamma-korrekciójának megvalósításáról! A gamma beállítás kulcsfontosságú képfeldolgozási technika, amely lehetővé teszi a kép fényerejének és kontrasztjának finomhangolását. Ebben az oktatóanyagban végigvezetjük a folyamaton a hatékony Aspose.PSD .NET könyvtár használatával.

## Előfeltételek

Mielőtt belevágna a megvalósításba, győződjön meg arról, hogy a következő előfeltételek teljesülnek:

-  Aspose.PSD for .NET Library: Győződjön meg arról, hogy telepítve van az Aspose.PSD .NET könyvtárhoz. Letöltheti[itt](https://releases.aspose.com/psd/net/).

- .NET-keretrendszer: Ez az oktatóanyag feltételezi, hogy rendelkezik alapvető ismeretekkel a .NET-fejlesztésről, és telepítve van a .NET-keretrendszer.

- Integrált fejlesztői környezet (IDE): Válassza ki a kívánt IDE-t a .NET-fejlesztéshez, például a Visual Studio-t.

## Névterek importálása

A .NET-projektben először importálja az Aspose.PSD-vel való munkához szükséges névtereket:

```csharp
using Aspose.PSD.FileFormats.Tiff.Enums;
using Aspose.PSD.ImageOptions;
```

## 1. lépés: Állítsa be projektjét

Hozzon létre egy új .NET-projektet a választott IDE-ben. Ügyeljen arra, hogy hivatkozásokat adjon hozzá az Aspose.PSD könyvtárhoz.

## 2. lépés: Határozza meg a dokumentumkönyvtárat

```csharp
string dataDir = "Your Document Directory";
```

## 3. lépés: Töltse be a képet

```csharp
string sourceFile = dataDir + @"sample.psd";
using (var image = Image.Load(sourceFile))
{
    // A blokkon belül további lépéseket hajtanak végre.
}
```

## 4. lépés: Átküldés a RasterImage-be és a Cache Databa

```csharp
RasterImage rasterImage = (RasterImage)image;
if (!rasterImage.IsCached)
{
    rasterImage.CacheData();
}
```

## 5. lépés: A gamma beállítása

```csharp
rasterImage.AdjustGamma(2.2f, 2.2f, 2.2f);
```

## 6. lépés: Hozzon létre TiffOptions és Mentse

```csharp
string destName = dataDir + @"AdjustGamma_out.tiff";
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
tiffOptions.BitsPerSample = new ushort[] { 8, 8, 8 };
tiffOptions.Photometric = TiffPhotometrics.Rgb;
rasterImage.Save(destName, tiffOptions);
```

## Következtetés

Gratulálok! Sikeresen megvalósította a Gamma Adjustment funkciót az Aspose.PSD for .NET használatával. Ez a nagy teljesítményű könyvtár robusztus képességeket biztosít a képfeldolgozáshoz, így értékes eszköz a .NET-fejlesztők számára.

## GYIK

### 1. kérdés: Hol találom az Aspose.PSD dokumentációt?

 V1: Tekintse meg a dokumentációt[itt](https://reference.aspose.com/psd/net/).

### 2. kérdés: Hogyan tölthetem le az Aspose.PSD-t .NET-hez?

 2. válasz: Letöltheti a könyvtárat[itt](https://releases.aspose.com/psd/net/).

### 3. kérdés: Van ingyenes próbaverzió?

 V3: Igen, ingyenes próbaverziót kaphat[itt](https://releases.aspose.com/).

### 4. kérdés: Hol kaphatok támogatást az Aspose.PSD-hez?

 V4: Látogassa meg a támogatási fórumot[itt](https://forum.aspose.com/c/psd/34).

### 5. kérdés: Szükségem van ideiglenes engedélyre?

 V5: Szükség esetén ideiglenes engedélyt szerezhet[itt](https://purchase.aspose.com/temporary-license/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
