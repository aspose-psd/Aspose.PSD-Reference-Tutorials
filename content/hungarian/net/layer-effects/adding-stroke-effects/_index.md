---
title: Stroke Effects hozzáadása a rétegekhez az Aspose.PSD for .NET-ben
linktitle: Stroke Effects hozzáadása a rétegekhez
second_title: Aspose.PSD .NET API
description: Javítsa a kép esztétikáját az Aspose.PSD for .NET segítségével. Lépésről lépésre tanulja meg a stroke hatások hozzáadását. Töltse le, vásárolja meg vagy próbálja ki az ingyenes próbaverziót most.
type: docs
weight: 10
url: /hu/net/layer-effects/adding-stroke-effects/
---
## Bevezetés

Üdvözöljük ebben a lépésenkénti oktatóanyagban, amely az Aspose.PSD for .NET rétegeihez vonóeffektusok hozzáadásával foglalkozik. A képek vizuális vonzerejének fokozása a körvonal-effektussal gyerekjáték, az Aspose.PSD pedig zökkenőmentessé teszi a .NET-fejlesztők számára. Ebben az útmutatóban végigvezetjük a folyamaton, világos lépéseket és példákat adva, amelyek segítenek elsajátítani ezt a hatékony funkciót.

## Előfeltételek

Mielőtt belevágnánk az oktatóanyagba, győződjön meg arról, hogy a következő előfeltételek teljesülnek:

- Aspose.PSD for .NET: Töltse le és telepítse az Aspose.PSD könyvtárat a[weboldal](https://releases.aspose.com/psd/net/).

- Dokumentumkönyvtár: Készítsen egy könyvtárat, amely tartalmazza azt a PSD-dokumentumot, amelyre a körvonal-effektusokat alkalmazni kívánja.

- Kimeneti könyvtár: Külön könyvtárral kell tárolni a kimeneti képeket körvonal-effektusokkal.

- Visual Studio: Győződjön meg arról, hogy be van állítva a Visual Studio vagy bármely más előnyben részesített .NET fejlesztői környezet.

## Névterek importálása

A .NET-projektben adja meg a szükséges névtereket az Aspose.PSD funkcióinak kihasználásához:

```csharp
using System;
using System.IO;
using Aspose.PSD.FileFormats.Psd;
using Aspose.PSD.FileFormats.Psd.Layers.FillSettings;
using Aspose.PSD.FileFormats.Psd.Layers.LayerEffects;
using Aspose.PSD.ImageLoadOptions;
using Aspose.PSD.ImageOptions;
```

## 1. lépés: Töltse be a PSD-dokumentumot

```csharp
string srcFile = Path.Combine(SourceDir, "AddStrokeEffect.psd");
string outputFilePng = Path.Combine(OutputDir, "AddStrokeEffect.png");

using (var psdImage = (PsdImage)Image.Load(srcFile, new PsdLoadOptions() { LoadEffectsResource = true }))
{
    // Ide kerül a PSD-dokumentum betöltéséhez szükséges kód
}
```

## 2. lépés: Add Color Stroke Effect

```csharp
// Színes kitöltést ad a belső pozícióhoz
strokeEffect = psdImage.Layers[1].BlendingOptions.AddStroke(FillType.Color);
strokeEffect.Size = 7;
strokeEffect.Position = StrokePosition.Inside;
colorFillSettings = strokeEffect.FillSettings as IColorFillSettings;
colorFillSettings.Color = Color.Green;
```

## 3. lépés: Külső pozíció

```csharp
// Színes kitöltést ad a külső pozícióhoz
strokeEffect = psdImage.Layers[2].BlendingOptions.AddStroke(FillType.Color);
strokeEffect.Size = 7;
strokeEffect.Position = StrokePosition.Outside;
colorFillSettings = strokeEffect.FillSettings as IColorFillSettings;
colorFillSettings.Color = Color.Green;
```

## 4. lépés: Középső pozíció

```csharp
// Színes kitöltést ad hozzá a középső pozícióhoz
strokeEffect = psdImage.Layers[3].BlendingOptions.AddStroke(FillType.Color);
strokeEffect.Size = 7;
strokeEffect.Position = StrokePosition.Center;
colorFillSettings = strokeEffect.FillSettings as IColorFillSettings;
colorFillSettings.Color = Color.Green;
```

Ismételje meg a hasonló lépéseket a színátmenet és a minta kitöltésekor, és ennek megfelelően módosítsa a beállításokat.

## Következtetés

Gratulálunk! Sikeresen megtanulta, hogyan adhat körvonal-effektusokat a rétegekhez az Aspose.PSD for .NET használatával. Kísérletezzen különböző beállításokkal, hogy elérje a kívánt vizuális hatást a képeken.

## GYIK

### 1. kérdés: Alkalmazhatok körvonal-effektusokat csak meghatározott rétegekre?

1. válasz: Igen, meghatározott rétegeket célozhat meg a kódban található rétegindex módosításával.

### 2. kérdés: Az Aspose.PSD kompatibilis a legújabb .NET keretrendszerrel?

A2: Abszolút! Az Aspose.PSD-t úgy tervezték, hogy zökkenőmentesen integrálódjon a legújabb .NET-keretrendszerekkel.

### Q3: Hogyan szabhatom testre a körvonal színét?

 A3: Egyszerűen módosítsa a`Color` tulajdonság a kódban a kívánt körvonalszín eléréséhez.

### 4. kérdés: Az Aspose.PSD támogatja több PSD-fájl kötegelt feldolgozását?

4. válasz: Igen, több PSD-fájlt is átlapozhat, és hasonló megközelítéssel alkalmazhatja a körvonal-effektust.

### 5. kérdés: Használhatom a próbaverziót az Aspose.PSD megvásárlása előtt?

 A5: Természetesen! Fogd meg a[ingyenes próbaverzió](https://releases.aspose.com/) hogy vásárlás előtt fedezze fel az Aspose.PSD képességeit.