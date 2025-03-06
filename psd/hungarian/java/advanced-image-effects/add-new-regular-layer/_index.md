---
title: Adjon hozzá egy új normál réteget a PSD-hez az Aspose.PSD for Java segítségével
linktitle: Adjon hozzá egy új szabályos réteget a PSD-hez
second_title: Aspose.PSD Java API
description: Ismerje meg, hogyan adhat hozzá új normál réteget PSD-fájlokhoz az Aspose.PSD for Java használatával. Kövesse lépésről lépésre útmutatónkat a zökkenőmentes PSD-manipuláció érdekében.
weight: 11
url: /hu/java/advanced-image-effects/add-new-regular-layer/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Adjon hozzá egy új normál réteget a PSD-hez az Aspose.PSD for Java segítségével

## Bevezetés

Üdvözöljük ebben az átfogó oktatóanyagban, amely az Aspose.PSD for Java használatáról szól, amellyel egy új normál réteget adhat hozzá egy PSD-fájlhoz. Az Aspose.PSD egy hatékony Java-könyvtár, amely lehetővé teszi a fejlesztők számára, hogy hatékonyan kezeljék a PSD-fájlokat és dolgozzanak velük. Ebben az oktatóanyagban végigvezetjük Önt egy új normál réteg PSD-fájlhoz való hozzáadásának folyamatán, részletes lépésekkel és kódpéldákkal.

## Előfeltételek

Mielőtt belevágna az oktatóanyagba, győződjön meg arról, hogy a következő előfeltételeket teljesítette:

- Java fejlesztői környezet: Győződjön meg arról, hogy a rendszeren be van állítva Java fejlesztői környezet.
-  Aspose.PSD Library: Töltse le és telepítse az Aspose.PSD for Java könyvtárat. Megtalálhatod a könyvtárat[itt](https://releases.aspose.com/psd/java/).

## Csomagok importálása

A kezdéshez importálja a szükséges csomagokat a Java projektbe. Ezek a csomagok elengedhetetlenek az Aspose.PSD funkciókkal való együttműködéshez. Írja be a következő sorokat a Java fájl elejére:

```java
import com.aspose.psd.Image;
import com.aspose.psd.Rectangle;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.Layer;
import com.aspose.psd.imageoptions.PngOptions;
import com.aspose.psd.imageoptions.PsdOptions;
```

## 1. lépés: Töltse be a PSD-fájlt

Töltse be a szerkeszteni kívánt PSD-fájlt a következő kóddal:

```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "OneLayer.psd";
PsdImage im = (PsdImage)Image.load(sourceFileName);
```

## 2. lépés: Készítsen adattömböket és téglalapokat

Készítsen elő két int tömböt és két téglalap objektumot az alábbiak szerint:

```java
int[] data1 = new int[2500];
int[] data2 = new int[2500];
Rectangle rect1 = new Rectangle(0, 0, 50, 50);
Rectangle rect2 = new Rectangle(0, 0, 100, 25);
```

## 3. lépés: A rétegadatok inicializálása

Adattömbök inicializálása alapértelmezett értékkel:

```java
for (int i = 0; i < 2500; i++) {
    data1[i] = -10000000;
    data2[i] = -10000000;
}
```

## 4. lépés: Szabályos rétegek hozzáadása

Adjon hozzá két normál réteget a PSD-képhez:

```java
Layer layer1 = im.addRegularLayer();
layer1.setLeft(25);
layer1.setTop(25);
layer1.setRight(75);
layer1.setBottom(75);
layer1.saveArgb32Pixels(rect1, data1);

Layer layer2 = im.addRegularLayer();
layer2.setLeft(25);
layer2.setTop(150);
layer2.setRight(1255);
layer2.setBottom(175);
layer2.saveArgb32Pixels(rect2, data2);
```

## 5. lépés: PSD és PNG mentése

Mentse el a módosított PSD-t és egy további PNG-fájlt:

```java
im.save(exportPath, new PsdOptions());
im.save(exportPathPng, new PngOptions());
```

Gratulálok! Sikeresen hozzáadott egy új normál réteget egy PSD-fájlhoz az Aspose.PSD for Java használatával.

## Következtetés

Ebben az oktatóanyagban az Aspose.PSD for Java segítségével új normál réteg hozzáadásának folyamatát ismertettük egy PSD-fájlhoz. Ez a hatékony könyvtár leegyszerűsíti a PSD kezelését, így elérhetővé teszi a Java fejlesztők számára. Kísérletezzen különböző paraméterekkel és funkciókkal az Aspose.PSD teljes potenciáljának felfedezéséhez.

## GYIK

### 1. kérdés: Az Aspose.PSD kompatibilis a Java 8-cal?

1. válasz: Igen, az Aspose.PSD támogatja a Java 8 és újabb verzióit.

### 2. kérdés: Alkalmazhatok átalakításokat a hozzáadott rétegekre?

A2: Abszolút! Az Aspose.PSD számos átalakítási lehetőséget biztosít a rétegekhez.

### 3. kérdés: Hol találok további Aspose.PSD dokumentációt?

 V3: Olvassa el a dokumentációt[itt](https://reference.aspose.com/psd/java/).

### 4. kérdés: Hogyan szerezhetek ideiglenes licencet az Aspose.PSD-hez?

 A4: Látogassa meg[ezt a linket](https://purchase.aspose.com/temporary-license/) ideiglenes licencelési lehetőségekért.

### 5. kérdés: Vannak közösségi fórumok az Aspose.PSD támogatására?

 V5: Igen, találhat támogatást és megbeszéléseket[itt](https://forum.aspose.com/c/psd/34).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
