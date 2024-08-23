---
title: Egyszínű vonásréteg hozzáadása az Aspose.PSD for .NET-hez
linktitle: Körvonalas réteg hozzáadása egyszínű színnel
second_title: Aspose.PSD .NET API
description: Növelje .NET képkezelési készségeit az Aspose.PSD segítségével. Lépésről lépésre tanulja meg a körvonal-rétegek hozzáadását egyszínű színekkel.
type: docs
weight: 11
url: /hu/net/layer-effects/adding-stroke-layer-solid-color/
---
## Bevezetés

A .NET fejlesztés területén általános követelmény a tetszetős képek létrehozása. Az Aspose.PSD for .NET hatékony eszközkészletet biztosít a képek zökkenőmentes kezeléséhez és javításához. Az egyik alapvető funkció egy egyszínű körvonalréteg hozzáadása, amely élénkséget és mélységet kölcsönöz a képeknek. Ebben az oktatóanyagban lépésről lépésre végigvezetjük a folyamaton az Aspose.PSD for .NET használatával.

## Előfeltételek

Mielőtt belevágna az oktatóanyagba, győződjön meg arról, hogy rendelkezik a következő előfeltételekkel:

- .NET fejlesztési alapismeretek.
- A Visual Studio telepítve van a gépedre.
- Aspose.PSD .NET könyvtárhoz. Letöltheti a[weboldal](https://releases.aspose.com/psd/net/).

## Névterek importálása

Kezdje a szükséges névterek importálásával, hogy kihasználja az Aspose.PSD for .NET funkcióit:

```csharp
using Aspose.PSD.FileFormats.Psd;
using Aspose.PSD.FileFormats.Psd.Layers.FillSettings;
using Aspose.PSD.FileFormats.Psd.Layers.LayerEffects;
using Aspose.PSD.ImageLoadOptions;
using System;
using Aspose.PSD.FileFormats.Core.Blending;
```

## 1. lépés: Töltse be a PSD fájlt

Kezdje a PSD-fájl betöltésével, amelyet egy körvonalréteggel szeretne javítani. Győződjön meg arról, hogy a megfelelő fájl elérési útja van:

```csharp
string dataDir = "Your Document Directory";
string sourceFileName = dataDir + "Stroke.psd";

var loadOptions = new PsdLoadOptions()
{
    LoadEffectsResource = true
};

using (var im = (PsdImage)Image.Load(sourceFileName, loadOptions))
{
    // A további lépések kódja itt lesz hozzáadva
}
```

## 2. lépés: Nyissa meg a Stroke Effect tulajdonságait

A stroke effektus tulajdonságainak lekérése a PSD-fájlból:

```csharp
var colorStroke = (StrokeEffect)im.Layers[1].BlendingOptions.Effects[0];

if ((colorStroke.BlendMode != BlendMode.Normal) ||
    (colorStroke.Opacity != 255) ||
    (colorStroke.IsVisible != true))
{
    throw new Exception("Color stroke effect was read wrong");
}
```

## 3. lépés: Állítsa be a löketbeállításokat

Módosítsa a löketbeállításokat saját igényei szerint. Ebben a példában a színt sárgára változtatjuk, az átlátszatlanságot 127-re állítjuk, és a Színkeverési módot használjuk:

```csharp
var fillSettings = (ColorFillSettings)colorStroke.FillSettings;

if ((fillSettings.Color != Color.Black) || (fillSettings.FillType != FillType.Color))
{
    throw new Exception("Color stroke effect settings were read wrong");
}

fillSettings.Color = Color.Yellow;
colorStroke.Opacity = 127;
colorStroke.BlendMode = BlendMode.Color;
```

## 4. lépés: Mentse el a szerkesztett képet

Mentse el a képet a körvonal-réteg módosításainak alkalmazása után:

```csharp
string exportPath = dataDir + "StrokeGradientChanged.psd";
im.Save(exportPath);
```

## 5. lépés: Ellenőrizze a változtatásokat

A szerkesztett kép betöltésével és ellenőrzésével győződjön meg a módosítások helyes alkalmazásáról:

```csharp
using (var im = (PsdImage)Image.Load(exportPath, loadOptions))
{
    // Itt lesz hozzáadva a módosítások ellenőrzéséhez szükséges kód
}
```

Ismételje meg ezeket a lépéseket a további beállításokhoz, vagy kísérletezzen különböző vonáseffektusokkal a kívánt vizuális hatás elérése érdekében.

## Következtetés

Gratulálok! Sikeresen megtanulta, hogyan adhat hozzá egyszínű körvonalréteget az Aspose.PSD for .NET használatával. Ez a hatékony funkció a lehetőségek világát nyitja meg a képek tökéletesítésére a .NET környezetben.

## GYIK

### 1. kérdés: Az Aspose.PSD for .NET kompatibilis a legújabb .NET-keretrendszer-verziókkal?

1. válasz: Igen, az Aspose.PSD for .NET rendszeresen frissül, hogy biztosítsa a kompatibilitást a legújabb .NET-keretrendszer-verziókkal.

### 2. kérdés: Használhatom az Aspose.PSD-t .NET-hez kereskedelmi projektekhez?

A2: Abszolút! Az Aspose.PSD for .NET egy kereskedelmi termék, és licenc megvásárlásával használhatja projektjeihez.

### 3. kérdés: Hol találok további példákat és dokumentációt az Aspose.PSD for .NET-hez?

 A3: Fedezze fel a[dokumentáció](https://reference.aspose.com/psd/net/) átfogó példákért és útmutatásért.

### 4. kérdés: Elérhető ingyenes próbaverzió az Aspose.PSD for .NET számára?

 V4: Igen, ingyenes próbaverziót kaphat a[kiadások oldala](https://releases.aspose.com/).

### 5. kérdés: Hogyan kaphatok támogatást az Aspose.PSD for .NET számára?

 A5: Látogassa meg a[Aspose.PSD fórum](https://forum.aspose.com/c/psd/34) segítséget kérni és kapcsolatba lépni a közösséggel.