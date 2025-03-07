---
title: Kép levágása téglalappal az Aspose.PSD for Java-ban
linktitle: Kép levágása téglalap szerint
second_title: Aspose.PSD Java API
description: Fedezze fel a Java zökkenőmentes képkivágási lehetőségeit az Aspose.PSD segítségével. Kövesse lépésenkénti útmutatónkat, hogy könnyedén kivághassa a képeket az Aspose.PSD for Java használatával.
weight: 15
url: /hu/java/image-editing/crop-image-by-rectangle/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Kép levágása téglalappal az Aspose.PSD for Java-ban

## Bevezetés

A Java fejlesztés világában a képek manipulálása gyakori feladat, és az Aspose.PSD for Java hatékony megoldást nyújt a képfeldolgozáshoz. Ebben az oktatóanyagban végigvezetjük a kép téglalap alakú kivágásán az Aspose.PSD for Java segítségével. Kövesse az alábbi lépéseket, hogy ezt könnyedén elérhesse.

## Előfeltételek

Mielőtt belevágna az oktatóanyagba, győződjön meg arról, hogy a következő előfeltételek teljesülnek:

- Java Development Kit (JDK) telepítve a gépére.
- Aspose.PSD a Java könyvtárhoz. Letöltheti a[weboldal](https://releases.aspose.com/psd/java/).

## Csomagok importálása

Ügyeljen arra, hogy a szükséges csomagokat tartalmazza a Java projektben, hogy kihasználja az Aspose.PSD for Java képességeit. Adja hozzá a következő importálási utasításokat a Java fájl elejéhez:

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;
import com.aspose.psd.Rectangle;

import com.aspose.psd.imageoptions.JpegOptions;
```

Most bontsuk le a folyamatot több lépésre, amelyek végigvezetik Önt a kép téglalap alakú kivágásán az Aspose.PSD for Java segítségével.

## 1. lépés: Állítsa be a dokumentumkönyvtárat

```java
String dataDir = "Your Document Directory";
```

 Cserélje ki`"Your Document Directory"` a PSD-fájl tényleges elérési útjával.

## 2. lépés: Adja meg a forrás- és célfájlokat

```java
String sourceFile = dataDir + "sample.psd";
String destName = dataDir + "CroppingByRectangle_out.jpg";
```

Határozza meg a forrás PSD-fájl és a cél JPEG-fájl elérési útját.

## 3. lépés: Töltse be és gyorsítótárazza a képet

```java
RasterImage rasterImage = (RasterImage)Image.load(sourceFile);

if (!rasterImage.isCached()) {
    rasterImage.cacheData();
}
```

 Töltse be a PSD-képet a`RasterImage` példányt, és gyorsítótárazza az adatait.

## 4. lépés: Hozzon létre és definiáljon a vágótéglalapot

```java
Rectangle rectangle = new Rectangle(20, 20, 20, 20);
```

 Hozzon létre egy példányt a`Rectangle` osztály a kívánt mérettel a kivágáshoz.

## 5. lépés: Vágja ki és mentse el a képet

```java
rasterImage.crop(rectangle);
rasterImage.save(destName, new JpegOptions());
```

Végezze el a kivágási műveletet a megadott téglalap használatával, és mentse el az eredményeket JPEG fájlként.

Ismételje meg ezeket a lépéseket szükség szerint, és állítsa be a paramétereket az Ön egyedi igényei szerint.

## Következtetés

Ebben az oktatóanyagban végigvezettük a kép téglalap alakú kivágásának folyamatát az Aspose.PSD for Java segítségével. Az alábbi lépések követésével könnyedén integrálhat hatékony képkezelési képességeket Java-alkalmazásaiba.

## GYIK

### 1. kérdés: Használhatom az Aspose.PSD for Java-t más Java-keretrendszerekkel?

1. válasz: Igen, az Aspose.PSD for Java integrálható különféle Java-keretrendszerekkel, rugalmasságot biztosítva a fejlesztési projektekben.

### 2. kérdés: Elérhető ingyenes próbaverzió az Aspose.PSD for Java számára?

 2. válasz: Igen, hozzáférhet az ingyenes próbaverzióhoz[itt](https://releases.aspose.com/).

### 3. kérdés: Hol találhatok további támogatást vagy segítséget?

 A3: Látogassa meg a[Aspose.PSD fórum](https://forum.aspose.com/c/psd/34) közösségi támogatásra és beszélgetésekre.

### 4. kérdés: Hogyan szerezhetek ideiglenes licencet az Aspose.PSD for Java számára?

 V4: Kaphat ideiglenes engedélyt[itt](https://purchase.aspose.com/temporary-license/).

### 5. kérdés: Melyek a támogatott képformátumok a kivágáshoz az Aspose.PSD for Java programban?

5. válasz: Az Aspose.PSD for Java különféle képformátumokat támogat, beleértve a PSD-t, PNG-t, JPEG-et stb.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
