---
title: Színegyensúly-beállítás alkalmazása az Aspose.PSD-ben .NET-hez
linktitle: Színegyensúly-beállítás alkalmazása
second_title: Aspose.PSD .NET API
description: Fokozza a PSD-képszíneket könnyedén az Aspose.PSD-vel a .NET színegyensúly-beállítási funkciójához. Kövesse lépésről lépésre útmutatónkat a lenyűgöző eredményekért.
type: docs
weight: 14
url: /hu/net/image-adjustment/color-balance-adjustment/
---
## Bevezetés

Üdvözöljük ebben az átfogó útmutatóban a színegyensúly-beállítás alkalmazásáról az Aspose.PSD for .NET-ben! Az Aspose.PSD egy hatékony .NET-könyvtár, amely lehetővé teszi a fejlesztők számára a PSD-fájlok hatékony kezelését. Ebben az oktatóanyagban a Color Balance Adjustment funkcióra összpontosítunk, amely lehetővé teszi a PSD-képek színegyensúlyának egyszerű javítását.

## Előfeltételek

Mielőtt belevágnánk az oktatóanyagba, győződjön meg arról, hogy a következő előfeltételek teljesülnek:

-  Aspose.PSD for .NET Library: Töltse le és telepítse a könyvtárat a[Aspose.PSD weboldal](https://releases.aspose.com/psd/net/).
- Fejlesztői környezet: Győződjön meg arról, hogy működő .NET fejlesztői környezet van beállítva a gépén.
- PSD-fájl: Készítsen egy PSD-fájlt, amelyre alkalmazni szeretné a színegyensúly-beállítást.

## Névterek importálása

A .NET-projektben tartalmazza az Aspose.PSD-szolgáltatások használatához szükséges névtereket. Adja hozzá a következő sorokat a kódhoz:

```csharp
using Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers;
```

Most bontsuk le a színegyensúly beállítási folyamatát több lépésre:

## 1. lépés: Töltse be a PSD fájlt

```csharp
string dataDir = "Your Document Directory";
var filePath = dataDir + "ColorBalance.psd";
var outputPath = dataDir + "ColorBalance_out.psd";

using (var im = (FileFormats.Psd.PsdImage)Image.Load(filePath))
{
    // A színegyensúly beállításának kódja a következő lépésekben lesz hozzáadva.
}
```

## 2. lépés: A színegyensúly elérése és beállítása

```csharp
foreach (var layer in im.Layers)
{
    var cbLayer = layer as ColorBalanceAdjustmentLayer;
    if (cbLayer != null)
    {
        cbLayer.ShadowsCyanRedBalance = 30;
        cbLayer.ShadowsMagentaGreenBalance = -15;
        cbLayer.ShadowsYellowBlueBalance = 40;
        cbLayer.MidtonesCyanRedBalance = -90;
        cbLayer.MidtonesMagentaGreenBalance = -25;
        cbLayer.MidtonesYellowBlueBalance = 20;
        cbLayer.HighlightsCyanRedBalance = -30;
        cbLayer.HighlightsMagentaGreenBalance = 67;
        cbLayer.HighlightsYellowBlueBalance = -95;
        cbLayer.PreserveLuminosity = true;
    }
}
```

## 3. lépés: Mentse el a módosított képet

```csharp
im.Save(outputPath);
```

Sikeresen alkalmazta a Color Balance Adjustment funkciót a PSD-fájlban az Aspose.PSD for .NET segítségével!

## Következtetés

Gratulálunk! Megtanulta, hogyan javíthatja PSD-képeinek színegyensúlyát az Aspose.PSD for .NET segítségével. Kísérletezzen különböző egyensúlyi értékekkel a kívánt vizuális hatások eléréséhez.

## GYIK

### 1. kérdés: Alkalmazhatom a színegyensúly-beállítást több rétegre?

1. válasz: Igen, a PSD-fájl összes rétegét végigjárhatja, és szükség szerint módosíthatja a színegyensúlyt.

### 2. kérdés: Az Aspose.PSD for .NET alkalmas PSD-fájlok kötegelt feldolgozására?

A2: Abszolút! Az Aspose.PSD hatékony kötegelt feldolgozási képességeket biztosít a PSD-fájlokhoz.

### 3. kérdés: Hogyan szerezhetek ideiglenes licencet az Aspose.PSD for .NET számára?

 A3: Látogassa meg[Aspose.PSD ideiglenes licenc](https://purchase.aspose.com/temporary-license/) ideiglenes engedélyért.

### 4. kérdés: Hol találok további példákat és dokumentációt?

 A4: Fedezze fel a[Aspose.PSD dokumentáció](https://reference.aspose.com/psd/net/) részletes példákért és útmutatókért.

### 5. kérdés: Milyen támogatási lehetőségek állnak rendelkezésre az Aspose.PSD for .NET számára?

 A5: Látogassa meg a[Aspose.PSD fórum](https://forum.aspose.com/c/psd/34) közösségi támogatásra és beszélgetésekre.
