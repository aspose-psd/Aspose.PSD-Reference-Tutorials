---
title: Szintbeállító réteg hozzáadása a PSD-hez
linktitle: Szintbeállító réteg hozzáadása a PSD-hez
second_title: Aspose.PSD Java API
description: Ismerje meg, hogyan adhat hozzá hatékonyan Level Adjustment Layer-t PSD-fájljaihoz az Aspose.PSD for Java segítségével. Növelje képszerkesztési készségeit.
type: docs
weight: 16
url: /hu/java/modifying-converting-psd-images/add-level-adjustment-layer-psd/
---
## Bevezetés
Ami a képszerkesztést illeti, a szintek kezelése világméretű változást hozhat a fényképek élénkségében és tisztaságában. A Photoshop arzenáljának egyik praktikus eszköze a "Level Adjustment Layer", amely lehetővé teszi a képek tónustartományának és színegyensúlyának beállítását. Ebben az útmutatóban végigvezetjük, hogyan valósíthat meg egy szintbeállító réteget PSD-fájlban az Aspose.PSD for Java használatával. Tehát fogd meg a Java IDE-t.
## Előfeltételek
Mielőtt belevágna a szintbeállítások világába, be kell állítania néhány dolgot a zökkenőmentes utazás érdekében:
1.  Java Development Kit (JDK): Győződjön meg arról, hogy a JDK telepítve van a gépen. Ha nincs meg, akkor megragadhatja a[Oracle webhely](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html) vagy használja az OpenJDK-t.
2.  Aspose.PSD for Java Library: A PSD-fájlok kezeléséhez le kell töltenie az Aspose.PSD könyvtárat. Innen szerezheti be a legújabb verziót[letöltési link](https://releases.aspose.com/psd/java/) és győződjön meg róla, hogy a JAR-t belefoglalta a projekt könyvtárába.
3. Alapvető Java ismeretek: A Java programozás alapvető ismerete segít, mivel ebben az oktatóanyagban a kódrészletekbe merülünk bele.
4. IDE beállítása: Bármilyen Java IDE-t használhat – például IntelliJ IDEA, Eclipse vagy NetBeans – a kód írásához és futtatásához. Csak győződjön meg arról, hogy beállította a Java projektet, és hozzáadta az Aspose.PSD könyvtárat.

## Csomagok importálása
Mielőtt elkezdenénk írni a kódunkat, importálnunk kell a szükséges csomagokat az Aspose.PSD könyvtárból. A következőképpen teheti meg:
```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.adjustmentlayers.LevelsLayer;
import com.aspose.psd.fileformats.psd.layers.layerresources.LevelChannel;
```
Ezen csomagok importálásával hozzáférünk a PSD-fájlok betöltéséhez, módosításához és mentéséhez szükséges osztályokhoz.

Most bontsuk le a folyamatot emészthető lépésekre. Kövesse a PSD-fájl betöltését, a szintek beállítását, majd a módosítások mentését. 
## 1. lépés: Állítsa be a fájl elérési útját
Az első lépés az, hogy meghatározzuk, hol található a PSD fájlunk, és hova szeretnénk menteni a módosított kimenetet. Testreszabhatja a könyvtár elérési útját igényeinek megfelelően.
```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "LevelsAdjustmentLayer.psd";
String psdPathAfterChange = dataDir + "LevelsAdjustmentLayerChanged.psd";
```
 Tessék, cserélje ki`"Your Document Directory"` rendszer tényleges elérési útjával, ahol a PSD-fájl tárolva van. Ez megadja a terepet mindannak, amit a továbbiakban fogunk tenni.
## 2. lépés: Töltse be a PSD fájlt
 Most töltsük be a PSD-fájlt a`PsdImage` osztály. Ez a lépés elengedhetetlen, mivel lehetővé teszi számunkra a rétegek elérését és kezelését.
```java
PsdImage im = (PsdImage) Image.load(sourceFileName);
```
 Amikor hívsz`Image.load()` , akkor beolvassa a PSD-fájlt, és létrehoz egy példányt`PsdImage` amellyel dolgozhat.
## 3. lépés: Ismétlés a rétegeken keresztül
Mivel be akarunk állítani egy szintbeállító réteget, át kell lépnünk a PSD-fájlunkban minden egyes rétegen. Ez segít megtalálni a módosítani kívánt réteget.
```java
for (int i = 0; i < im.getLayers().length; i++) {
    if (im.getLayers()[i] instanceof LevelsLayer) {
        LevelsLayer levelsLayer = (LevelsLayer) im.getLayers()[i];
        // A további manipuláció itt megy majd...
    }
}
```
 Ebben a hurokban`instanceof LevelsLayer` ellenőrzi, hogy az aktuális fólia szintbeállító réteg-e. Ha igen, akkor módosíthatjuk a tulajdonságait.
## 4. lépés: Állítsa be a Level Channel beállításokat
Miután azonosítottuk a megfelelő réteget, módosíthatjuk a bemeneti és kimeneti szintjeit. Itt történik a varázslat! Állítsa be a különböző paramétereket, hogy megtudja, hogyan befolyásolják a képet.
```java
LevelChannel channel = levelsLayer.getChannel(0);
channel.setInputMidtoneLevel(2.0f);
channel.setInputShadowLevel((short) 10);
channel.setInputHighlightLevel((short) 230);
channel.setOutputShadowLevel((short) 20);
channel.setOutputHighlightLevel((short) 200);
```
Íme az egyes paraméterek feladata:
- Input Midtone Level: A középhangok beállítása.
- Beviteli árnyékszint: A kép sötétebb területeit módosítja.
- Bemeneti kiemelési szint: Módosítja a kép világos területeit.
- Output Shadow Level: Beállítja, hogyan jelenjenek meg a sötét árnyékok.
- Kimeneti kiemelés szintje: Beállítja, hogyan jelenjenek meg a világos kiemelések.
Kísérletezzen bátran különböző értékekkel!
## 5. lépés: Mentse el a módosított PSD-fájlt
Most, hogy elvégeztük a beállításokat, ideje elmenteni a módosított PSD-fájlt. Ez a lépés kulcsfontosságú a módosítások alkalmazásának és tárolásának biztosításához.
```java
im.save(psdPathAfterChange);
```
 A módosított PSD-fájlt most a megadott helyen találja`psdPathAfterChange`. 
## Következtetés
Éppen most tanulta meg, hogyan adhat hozzá szintbeállító réteget egy PSD-fájlhoz az Aspose.PSD for Java használatával! Ennek az útmutatónak a követésével könnyedén beállíthatja a képek tónusának minőségét, megnyitva ezzel az utat az élénkebb és tetszetősebb kimenet felé. Ne feledje, a gyakorlat teszi a mestert, ezért nyugodtan módosítsa a beállításokat, és fedezze fel a különböző PSD-fájlokat, hogy lássa a változtatások hatását.
## GYIK
### Mi az a szintbeállító réteg?
Level Adjustment Layer segítségével korrigálhatja a képek tónustartományát, kiegyensúlyozva az árnyékokat, a középtónusokat és a csúcsfényeket.
### Használhatom az Aspose.PSD-t vásárlás nélkül?
Igen! Az Aspose ingyenes próbaverziót kínál a könyvtár tesztelésére a vásárlás előtt.
### Hol találom az Aspose.PSD dokumentációját?
 A dokumentációt megtalálod[itt](https://reference.aspose.com/psd/java/).
### Van-e közösségi támogatás az Aspose termékekhez?
 Teljesen! Kérdéseket tehet fel és támogatást kérhet a[Aspose fórum](https://forum.aspose.com/c/psd/34).
### Hogyan szerezhetek ideiglenes licencet az Aspose.PSD-hez?
 Ideiglenes jogosítványt igényelhet[itt](https://purchase.aspose.com/temporary-license/).