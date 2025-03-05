---
title: Renderelési szint beállítási réteg a PSD-fájlokban – Java
linktitle: Renderelési szint beállítási réteg a PSD-fájlokban – Java
second_title: Aspose.PSD Java API
description: Ismerje meg, hogyan javíthatja könnyedén a kép kontrasztját és élénkségét az Aspose.PSD for Java segítségével. Master Levels Adjustment Layers ezzel a lépésről lépésre útmutatóval.
type: docs
weight: 17
url: /hu/java/psd-layer-management-effects/render-level-adjustment-layer-psd/
---
## Bevezetés

Előfordult már, hogy megnyitott egy PSD-fájlt csak azért, hogy megtalálja a képen a kontrasztot vagy az élénkséget? Ne féljetek, képszerkesztő harcosok! Az Aspose.PSD for Java nagy teljesítményű Levels Adjustment Layer manipulációs képességeivel segít. Ez az útmutató felvértezi azokat az ismereteket, amelyek segítségével gyorsan finomhangolhatja képeit a Levels segítségével. 

## Előfeltételek

- Java Development Kit (JDK): Győződjön meg arról, hogy a JDK legújabb verziója van telepítve a rendszerére. Letöltheti az Oracle webhelyéről ([https://www.oracle.com/java/technologies/javase-downloads.html](https://www.oracle.com/java/technologies/javase-downloads.html)).
- Aspose.PSD for Java Library: Töltse le az Aspose.PSD for Java könyvtárat a letöltési oldalról ([https://releases.aspose.com/psd/java/](https://releases.aspose.com/psd/java/)). A teljes funkciók használatához érvényes licencre lesz szüksége, de ingyenes próbaverzió áll rendelkezésre a kezdéshez ([https://releases.aspose.com/](https://releases.aspose.com/)).

## Csomagok importálása

Mielőtt belemerülnénk a kódba, importálnunk kell a szükséges Aspose.PSD osztályokat a PSD fájlokkal való interakcióhoz. Íme, amire szüksége lesz:

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.adjustmentlayers.LevelsLayer;
import com.aspose.psd.fileformats.psd.layers.layerresources.LevelChannel;
import com.aspose.psd.imageoptions.PngOptions;
```

 A`com.aspose.psd` csomag hozzáférést biztosít a PSD-manipulációs funkciókhoz, míg`com.aspose.psd.imaging.PngOptions` Lehetővé teszi számunkra, hogy a kép PNG formátumban történő mentésekor beállításokat adjunk meg.

Most pedig induljunk a Szintek beállítása kalandunkba:

## 1. lépés: Fájlútvonalak beállítása:

- Határozzon meg változókat a dokumentumkönyvtárhoz (`dataDir`), forrás PSD fájl neve (`sourceFileName`), a cél PSD-fájl neve a módosítás után (`psdPathAfterChange`), és a végső PNG-exportálási útvonalat (`pngExportPath`). Fontolja meg a leíró nevek használatát a kód olvashatóságának javítása érdekében.

```java
String dataDir = "Your Document Directory";

String sourceFileName = dataDir + "LevelsAdjustmentLayer.psd";
String psdPathAfterChange = dataDir + "LevelsAdjustmentLayerChanged.psd";
String pngExportPath = dataDir + "LevelsAdjustmentLayerChanged.png";
```

## 2. lépés: A PSD-kép betöltése:

-  Használja a`Image.load` módszerrel megnyithatja a forrás PSD fájlt és tárolhatja a`PsdImage`tárgy (`im`). Az Aspose.PSD automatikusan felismeri a fájlformátumot.

```java
PsdImage im = (PsdImage)Image.load(sourceFileName);
```

## 3. lépés: Iteráció rétegeken keresztül:

- Meg kell találnunk a PSD-n belül a Levels Adjustment Layert. Az Aspose kényelmes módot biztosít az összes rétegen való áthaladásra hurok segítségével.

```java
for (int i = 0; i < im.getLayers().length; i++) {
   // ... (ide kerül hozzáadásra a szintréteg ellenőrzésére szolgáló kód)
}
```

## 4. lépés: A szintréteg azonosítása:

- A hurkon belül ellenőrizze, hogy az aktuális réteg (`im.getLayers()[i]` ) egy példánya a`LevelsLayer` osztály segítségével a`instanceof` operátor. 
-  Ha igen, öntse a réteget a`LevelsLayer` tárgyat a további manipulációhoz.

```java
for (int i = 0; i < im.getLayers().length; i++) {
   if (im.getLayers()[i] instanceof LevelsLayer) {
	   LevelsLayer levelsLayer = (LevelsLayer) im.getLayers()[i];
	   // ... (itt lesz hozzáadva a szintek beállításához szükséges kód)
   }
}
```
## 5. lépés: Finomhangolási szintek (folytatás):

-  Állítsa be a kimeneti szinteket a gombbal`setOutputShadowLevel` és`setOutputHighlightLevel` hogy szabályozza a kapott kép sötétségét és világosságát. Ezek az értékek határozzák meg a kimeneti tartományra leképezett bemeneti szintek tartományát.

```java
for (int i = 0; i < im.getLayers().length; i++) {
   if (im.getLayers()[i] instanceof LevelsLayer) {
	   LevelsLayer levelsLayer = (LevelsLayer) im.getLayers()[i];
	   LevelChannel channel = levelsLayer.getChannel(0);

	   // Bemeneti szintek beállítása (0-255):
	   channel.setInputShadowLevel((short) 10); // Enyhén sötétítse az árnyékokat
	   channel.setInputMidtoneLevel(2.0f);     // Növelje a középtónusokat
	   channel.setInputHighlightLevel((short) 230); // Csökkentse a kiemeléseket

	   // Kimeneti szintek beállítása (0-255):
	   channel.setOutputShadowLevel((short) 20); // Sötétítse tovább az árnyékokat
	   channel.setOutputHighlightLevel((short) 200); //Világosítsa meg a kiemeléseket
   }
}
```

## 6. lépés: A módosított PSD mentése:

-  Használja a`save` módszere a`PsdImage` objektum a módosított kép mentéséhez a megadott elérési útra (`psdPathAfterChange`).

```java
im.save(psdPathAfterChange);
```

## 7. lépés: Exportálás PNG-ként (opcionális):

-  Ha szüksége van a módosított kép PNG-változatára, hozzon létre a`PngOptions` objektumot, és állítsa be a színtípust`TruecolorWithAlpha` . Ezután használja a`save` módszert ismét a PNG exportálási útvonallal és opciókkal.

```java
PngOptions saveOptions = new PngOptions();
saveOptions.setColorType(PngColorType.TruecolorWithAlpha);
im.save(pngExportPath, saveOptions);
```

És megvan! Sikeresen beállította a Levels Adjustment Layert a PSD-fájlban az Aspose.PSD for Java használatával. E lépések megértésével és különböző értékekkel kísérletezve javíthatja a képek kontrasztját és általános megjelenését.

## Következtetés

Az Aspose.PSD for Java lehetővé teszi a képszerkesztési folyamat irányítását. A Levels Adjustment Layer elsajátításával új életet lehelhet fényképeibe és terveibe. Ne feledje, a gyakorlat teszi a mestert, ezért ne habozzon kísérletezni és felfedezni ebben a hatékony eszközben rejlő lehetőségeket.
 
## GYIK

### Beállíthatom külön az egyes színcsatornákat (RGB)? 
Igen, minden színcsatornához hozzáférhet a`getChannel` módszere a`LevelsLayer` objektumot, és függetlenül módosíthatja a szintjeit.

### Hogyan kezelhetek több szintbeállító réteget egy PSD-ben?
A kód az összes rétegen keresztül iterál, így automatikusan feldolgozza a képen található további szintrétegeket.

### Vannak más módok a kép kontrasztjának beállítására a Szintek mellett?
Teljesen! Az Aspose.PSD különféle képbeállító eszközöket kínál, mint például a görbék, a fényerő/kontraszt stb.

### Automatizálhatom ezt a folyamatot több kép esetén? 
Igen, beépítheti ezt a kódot egy hurok- vagy kötegelt feldolgozási szkriptbe több PSD-fájl hatékony feldolgozásához.

### Hol találhatok további információt és támogatást?
Az Aspose kiterjedt dokumentációt biztosít ([https://reference.aspose.com/psd/java/](https://reference.aspose.com/psd/java/)) és egy támogató fórum ([https://forum.aspose.com/c/psd/34](https://forum.aspose.com/c/psd/34)), ha bármilyen kérdése vagy probléma merül fel.