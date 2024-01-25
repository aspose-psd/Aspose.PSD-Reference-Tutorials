---
title: A kép arányos átméretezése az Aspose.PSD for Java segítségével
linktitle: Kép arányos átméretezése
second_title: Aspose.PSD Java API
description: Bővítse Java-alkalmazásait az Aspose.PSD segítségével. Kövesse útmutatónkat a képek arányos átméretezéséhez, könnyedén. Növelje képkezelési képességeit még ma.
type: docs
weight: 17
url: /hu/java/advanced-image-manipulation/resize-image-proportionally/
---
## Bevezetés

Üdvözöljük a képek arányos átméretezéséről szóló, lépésről lépésre szóló útmutatónkban az Aspose.PSD for Java használatával. Ha Java-alkalmazásait hatékony képátméretezési lehetőségekkel szeretné bővíteni, akkor jó helyen jár. Ebben az oktatóanyagban világos és tömör lépésekkel végigvezetjük a folyamaton.

## Előfeltételek

Mielőtt belevágna az oktatóanyagba, győződjön meg arról, hogy a következő előfeltételek teljesülnek:

1. Java környezet: Győződjön meg arról, hogy a Java telepítve van a rendszeren.
2.  Aspose.PSD Library: Töltse le és telepítse az Aspose.PSD könyvtárat. Megtalálhatja a szükséges forrásokat[itt](https://releases.aspose.com/psd/java/).

## Csomagok importálása

Miután rendezte az előfeltételeket, importálja a szükséges csomagokat a Java projektbe. Győződjön meg arról, hogy az Aspose.PSD könyvtárra megfelelően hivatkozik a projektben.

```java
import com.aspose.psd.Image;

import com.aspose.psd.imageoptions.PngOptions;
```

## 1. lépés: Töltse be a képet

Kezdje azzal, hogy betölti az átméretezni kívánt képet a Java alkalmazásba.

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

Image image = Image.load(sourceFile);

if (!image.isCached()) {
    image.cacheData();
}
```

## 2. lépés: Adja meg a szélességet és a magasságot

Határozza meg az átméretezett kép új szélességét és magasságát. Ebben a példában átméretezzük a képet az eredeti méretének felére.

```java
int newWidth = image.getWidth() / 2;
image.resizeWidthProportionally(newWidth);

int newHeight = image.getHeight() / 2;
image.resizeHeightProportionally(newHeight);
```

## 3. lépés: Mentse el az átméretezett képet

Mentse el az átméretezett képet a kívánt helyre, megadva a formázási beállításokat (ebben az esetben PNG).

```java
String destName = dataDir + "SimpleResizeImageProportionally_out.png";
image.save(destName, new PngOptions());
```

És megvan! Sikeresen átméretezett egy képet arányosan az Aspose.PSD for Java használatával.

## Következtetés

Ebben az oktatóanyagban bemutattuk a képek arányos átméretezésének alapvető lépéseit a Java Aspose.PSD könyvtár használatával. Most már könnyedén integrálhatja ezt a funkciót Java-alkalmazásaiba a jobb képkezelés érdekében.

## GYIK

### 1. kérdés: Az Aspose.PSD kompatibilis az összes képformátummal?

 1. válasz: Az Aspose.PSD különféle képformátumokat támogat, beleértve a PSD-t, PNG-t, JPEG-et stb. Ellenőrizd a[dokumentáció](https://reference.aspose.com/psd/java/) átfogó listáért.

### 2. kérdés: Használhatom az Aspose.PSD-t kereskedelmi projektekhez?

 A2: Igen, megteheti. Meglátogatni a[vásárlási oldal](https://purchase.aspose.com/buy) az engedélyezési részletekért.

### 3. kérdés: Rendelkezésre állnak-e ideiglenes licencek tesztelési célokra?

 V3: Igen, beszerezhet ideiglenes engedélyt[itt](https://purchase.aspose.com/temporary-license/) értékeléshez.

### 4. kérdés: Hol találok támogatást az Aspose.PSD-hez?

 A4: Látogassa meg a[Aspose.PSD fórum](https://forum.aspose.com/c/psd/34) közösségi támogatásért és segítségért.

### 5. kérdés: Hogyan férhetek hozzá az Aspose.PSD dokumentációhoz?

 V5: Lásd a részletes dokumentációt[itt](https://reference.aspose.com/psd/java/).
`