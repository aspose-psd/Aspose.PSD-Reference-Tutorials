---
title: Kép elforgatása az Aspose.PSD for .NET fájlban
linktitle: Kép elforgatása
second_title: Aspose.PSD .NET API
description: Tanulja meg a képeket könnyedén elforgatni .NET-ben az Aspose.PSD segítségével. Kövesse lépésről lépésre bemutató oktatóanyagunkat.
type: docs
weight: 15
url: /hu/net/image-manipulation/rotate-image/
---
## Bevezetés

Ha a .NET használatával történő képmanipuláció világába merül, az Aspose.PSD a tökéletes eszköz a zökkenőmentes és hatékony képfeldolgozáshoz. Ebben az oktatóanyagban egy alapvető feladatra összpontosítunk – egy kép elforgatására az Aspose.PSD for .NET használatával. Kövesse a folyamatot egyszerű, végrehajtható lépésekre bontva.

## Előfeltételek

Mielőtt elkezdené, győződjön meg arról, hogy a következő előfeltételeket teljesítette:

-  Aspose.PSD for .NET Library: Töltse le és telepítse a könyvtárat a[Aspose.PSD .NET dokumentáció](https://reference.aspose.com/psd/net/).

- Dokumentumkönyvtár: Állítson be egy könyvtárat, ahol a képeket tárolja. Cserélje le a „Saját dokumentumkönyvtár” szöveget a kódrészletben a könyvtár elérési útjával.

## Névterek importálása

Ügyeljen arra, hogy tartalmazza az Aspose.PSD funkció eléréséhez szükséges névtereket. Adja hozzá a következő sorokat a .NET-projekt elejéhez:

```csharp
using Aspose.PSD.ImageOptions;
```

## 1. lépés: Töltse be a képet

```csharp
string sourceFile = dataDir + @"sample.psd";

// Töltsön be egy meglévő képet a RasterImage osztály egy példányába
using (Image image = Image.Load(sourceFile))
{
```

## 2. lépés: Forgassa el a képet

```csharp
    // Forgassa el a képet 270 fokkal az óramutató járásával megegyező irányba
    image.RotateFlip(RotateFlipType.Rotate270FlipNone);
```

## 3. lépés: Mentse el az elforgatott képet

```csharp
    // Mentse el az elforgatott képet JPEG fájlként
    string destName = dataDir + @"RotatingAnImage_out.jpg";
    image.Save(destName, new JpegOptions());
}
```

Ennyi! Néhány sornyi kóddal sikeresen elforgatott egy képet az Aspose.PSD for .NET használatával.

## Következtetés

Ebben az oktatóanyagban megvizsgáltuk a képek elforgatásának alapjait az Aspose.PSD for .NET használatával. Az Aspose.PSD robusztus eszközkészletet biztosít a képkezeléshez, így a .NET-fejlesztők nélkülözhetetlen könyvtárává válik. Kísérletezzen a különböző forgatásokkal, és fedezze fel a további lehetőségeket a képfeldolgozási munkafolyamatok javítása érdekében.

## GYIK

### 1. kérdés: Elforgathatom a képeket egyéni szögben az Aspose.PSD használatával?

 Igen, az Aspose.PSD lehetővé teszi egyéni elforgatási szög megadását. Egyszerűen cserélje ki a`RotateFlipType.Rotate270FlipNone` egy vonalba a kívánt elforgatási szöggel.

### 2. kérdés: Az Aspose.PSD kompatibilis a különböző képformátumokkal?

 Teljesen. Az Aspose.PSD a képformátumok széles skáláját támogatja, beleértve a PSD-t, JPEG-et, PNG-t stb. Ellenőrizze a[dokumentáció](https://reference.aspose.com/psd/net/) a teljes listához.

### 3. kérdés: Hogyan szerezhetek ideiglenes licencet az Aspose.PSD-hez?

 Látogassa meg a[ideiglenes licenc oldal](https://purchase.aspose.com/temporary-license/) az Aspose webhelyén, hogy ideiglenes engedélyt szerezzen értékelési célokra.

### 4. kérdés: Hol találok támogatást az Aspose.PSD-hez?

 Bármilyen kérdéssel vagy segítséggel kapcsolatban keresse fel a[Aspose.PSD fórum](https://forum.aspose.com/c/psd/34) és kapcsolatba lépni a közösséggel.

### 5. kérdés: Megvásárolhatom az Aspose.PSD-t kereskedelmi használatra?

 Biztosan. Fedezze fel a[vásárlási oldal](https://purchase.aspose.com/buy) hogy az Ön igényeire szabott licencet szerezzen.