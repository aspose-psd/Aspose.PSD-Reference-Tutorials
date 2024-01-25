---
title: Képek arányos átméretezése az Aspose.PSD-ben .NET-hez
linktitle: Képek arányos átméretezése
second_title: Aspose.PSD .NET API
description: Fedezze fel a zökkenőmentes képméretezést az Aspose.PSD for .NET segítségével. Töltse le a könyvtárat, kövesse oktatóanyagunkat, és javítsa képfeldolgozási képességeit.
type: docs
weight: 14
url: /hu/net/image-manipulation/resize-images-proportionally/
---
képkezelés területén az Aspose.PSD for .NET hatékony eszköztárként tűnik ki, amely lehetővé teszi a fejlesztők számára a képek arányos egyszerű átméretezését. Ebben a lépésenkénti útmutatóban végigvezetjük a képek Aspose.PSD for .NET használatával történő átméretezésén, így biztosítva, hogy képei hibátlanul megőrizzék arányaikat.

## Bevezetés

A képek arányos átméretezése sok alkalmazásban gyakori feladat, és az Aspose.PSD for .NET leegyszerűsíti ezt a folyamatot a fejlesztők számára. Függetlenül attól, hogy webalkalmazáson, asztali szoftveren vagy mobilalkalmazáson dolgozik, a képarány megőrzése mellett a képek átméretezésének megértése alapvető fontosságú a vizuális vonzerő és a következetesség megőrzése érdekében.

## Előfeltételek

Mielőtt belevágna az Aspose.PSD for .NET-hez való átméretezési varázslatába, győződjön meg arról, hogy a következő előfeltételek teljesülnek:

1.  Aspose.PSD for .NET Library: Győződjön meg arról, hogy telepítve van az Aspose.PSD for .NET könyvtár. Letöltheti a[Aspose.PSD .NET kiadásokhoz](https://releases.aspose.com/psd/net/) oldalon.

2. Dokumentumkönyvtár: Hozzon létre egy könyvtárat a dokumentumok tárolására, és cserélje ki a „Saját dokumentumkönyvtárat” a megadott kódban a könyvtár tényleges elérési útjával.

Most, hogy az előfeltételeket beállította, ugorjunk bele a lépésről lépésre szóló útmutatóba.

## Névterek importálása

```csharp
using Aspose.PSD.ImageOptions;
```

Importálja a szükséges névtereket a szükséges osztályok és metódusok eléréséhez.

## 1. lépés: Töltse be a képet

```csharp
// A dokumentumok könyvtárának elérési útja.
string dataDir = "Your Document Directory";

string sourceFile = dataDir + @"sample.psd";

// Töltsön be egy meglévő képet a RasterImage osztály egy példányába
using (Image image = Image.Load(sourceFile))
{
	if (!image.IsCached)
	{
		image.CacheData();
	}
	// A többi lépés itt következik
}
```

 Töltse be a forrásképet a`Image.Load` módszer.

## 2. lépés: Adja meg a szélességet és a magasságot

```csharp
// Szélesség és magasság megadása
int newWidth = image.Width / 2;
image.ResizeWidthProportionally(newWidth);

int newHeight = image.Height / 2;
image.ResizeHeightProportionally(newHeight);
```

Határozza meg az átméretezett kép új szélességét és magasságát. Ebben a példában a szélesség és magasság felezve van, de ezeket az értékeket igény szerint módosíthatja.

## 3. lépés: Mentse el az átméretezett képet

```csharp
string destName = dataDir + @"SimpleResizeImageProportionally_out.png";

image.Save(destName, new PngOptions());
```

 Mentse el az átméretezett képet a`Save` módszer meghatározott opciókkal. Ebben az esetben PNG-fájlként mentjük el.

## Következtetés

A képek arányos átméretezése az Aspose.PSD for .NET-ben egy egyszerű folyamat, amely hozzáadott értéket ad a képfeldolgozási munkafolyamathoz. Ez az útmutató felvértezte Önt azokkal a tudással, amelyekkel zökkenőmentesen integrálhatja ezt a funkciót alkalmazásaiba.

## GYIK

### 1. kérdés: Átméretezhetem a képeket meghatározott méretekre?

V1: Igen, testreszabhatja az új szélességet és magasságot az Ön igényei szerint a kódban.

### 2. kérdés: Alkalmas-e az Aspose.PSD for .NET a képek kötegelt átméretezésére?

A2: Abszolút! Ezeket a lépéseket beépítheti egy hurokba több kép kötegelt feldolgozásához.

### 3. kérdés: Vannak más képkezelési funkciók is az Aspose.PSD for .NET-ben?

3. válasz: Igen, az Aspose.PSD for .NET funkciók széles skáláját kínálja, beleértve a kivágást, az elforgatást és a szűrők alkalmazását a képekre.

### 4. kérdés: Elérhető ingyenes próbaverzió az Aspose.PSD for .NET számára?

 4. válasz: Igen, egy ingyenes próbaverzióval felfedezheti az Aspose.PSD for .NET képességeit. Látogatás[itt](https://releases.aspose.com/) kezdeni.

### 5. kérdés: Hol találok támogatást az Aspose.PSD for .NET számára?

 A5: Látogassa meg a[Aspose.PSD .NET fórumhoz](https://forum.aspose.com/c/psd/34) közösségi támogatásra és beszélgetésekre.