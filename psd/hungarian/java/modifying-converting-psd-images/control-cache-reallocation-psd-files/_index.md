---
date: 2026-03-13
description: Tanulja meg, hogyan hozzon létre PSD képes Java projekteket, miközben
  a gyorsítótár átcsoportosítását kezeli az Aspose.PSD for Java segítségével. Optimalizálja
  a memória- és lemezhasználatot hatékonyan.
linktitle: Create PSD Image Java – Control Cache Reallocation
second_title: Aspose.PSD Java API
title: PSD kép létrehozása Java‑ban – Gyorsítótár újraelosztásának szabályozása
url: /hu/java/modifying-converting-psd-images/control-cache-reallocation-psd-files/
weight: 22
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Cache újraelosztásának vezérlése PSD fájlokban

## Bevezetés
Ha hatékonyan kell **create PSD image java** projekteket készítenie, a cache újraelosztásának vezérlése elengedhetetlen. Képek és Photoshop fájlok programozott kezelése során a hatékonyság kulcsfontosságú tényező. Az Aspose.PSD for Java robusztus funkciókat kínál a PSD fájlok zökkenőmentes kezelésére és manipulálására. A teljesítmény optimalizálásának egyik alapvető szempontja a cache újraelosztásának vezérlése. A cache kezelése segít fenntartani az egyensúlyt a memória és a lemezhasználat között, biztosítva, hogy az alkalmazás zökkenőmentesen fusson, váratlan összeomlások vagy lassulások nélkül. 

## Gyors válaszok
- **Mi a cache újraelosztás feladata?** Egyensúlyba hozza a memória és a lemezhasználatot nagy PSD fájlok feldolgozása közben.  
- **Melyik cache típus a legjobb nagy képekhez?** A `CacheOnDiskOnly` a memóriát szabadon tartja, a cache-t lemezen tárolja.  
- **Mennyi lemezterületet oszthatok ki?** Legfeljebb 1 GB (vagy bármilyen méret, amit a `setMaxDiskSpaceForCache`‑el beállít).  
- **Szükségem van licencre ezen funkciók használatához?** A licenc eltávolítja a próbaidő korlátozásait; lásd az Aspose vásárlási oldalt.  
- **Figyelhetem a cache használatát futás közben?** Igen, használd a `Cache.getAllocatedDiskBytesCount()` és `Cache.getAllocatedMemoryBytesCount()` metódusokat.

## Miért fontos a cache újraelosztás vezérlése?
A cache kezelése kulcsfontosságú, amikor **create PSD image java** alkalmazásokat fejlesztesz, amelyek nagy felbontású vagy több rétegből álló fájlokkal dolgoznak. A megfelelő cache beállítások megakadályozzák a memóriahiányos hibákat, csökkentik a GC szüneteket, és kiszámítható teljesítményt biztosítanak szervereken vagy asztali alkalmazásokban.

## Előkövetelmények
1. Java Development Kit (JDK): Győződjön meg róla, hogy a gépén telepítve van a JDK. Letöltheti a [Oracle weboldaláról](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).
2. Aspose.PSD for Java: Le kell töltenie az Aspose.PSD könyvtárat. A legújabb kiadást megtalálja [itt](https://releases.aspose.com/psd/java/).
3. IDE beállítás: Egy integrált fejlesztőkörnyezet (IDE), például az IntelliJ IDEA vagy az Eclipse megkönnyíti a kód kezelését.
4. Alapvető Java ismeretek: A Java programozás ismerete segít jobban megérteni a koncepciókat és a kódrészleteket.
5. Aspose licenc (opcionális): Ha el szeretné távolítani a vízjeleket és teljes funkcionalitást szeretne, fontolja meg egy licenc megvásárlását [itt](https://purchase.aspose.com/buy) vagy próbálja ki az ingyenes próbaverziót [itt](https://releases.aspose.com/).

## Csomagok importálása
Mielőtt elkezdenénk a kódírást, győződjünk meg róla, hogy a szükséges csomagok importálva vannak. Az alábbiakban egy rövid lista látható arról, hogy mit kell a Java fájl elején szerepeltetni:
```java
import com.aspose.psd.Cache;
import com.aspose.psd.CacheType;
import com.aspose.psd.Color;
import com.aspose.psd.ColorPalette;
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;
import com.aspose.psd.imageoptions.GifOptions;
import com.aspose.psd.imageoptions.PsdOptions;
import com.aspose.psd.sources.StreamSource;
import com.aspose.psd.system.io.MemoryStream;
```

## Hogyan hozzunk létre PSD Image Java-t cache vezérléssel
Az alábbiakban egy lépésről‑lépésre útmutató látható, amely a cache konfigurációt közvetlenül összekapcsolja a PSD kép Java‑ban történő létrehozásának folyamatával.

### 1. lépés: Az adatkönyvtár beállítása
Először is be kell állítania egy könyvtárat, ahová a cache fájlokat szeretné tárolni. Ez elengedhetetlen a cache hatékony kezelése érdekében.
```java
String dataDir = "Your Document Directory";
Cache.setCacheFolder(dataDir);
```

- `String dataDir`: A dokumentum cache könyvtárának meghatározása.  
- `Cache.setCacheFolder(dataDir)`: Ez a metódus a cache mappát a megadott könyvtárra állítja. Az Aspose által létrehozott cache most itt lesz tárolva az alapértelmezett ideiglenes könyvtár helyett.

### 2. lépés: Cache lemezre konfigurálása
Ezután megadjuk, hogy a cache csak lemezen legyen tárolva. Ez különösen hasznos, ha az alkalmazás nagy fájlokat használ, és biztosítani szeretné, hogy a memória szabad maradjon.
```java
Cache.setCacheType(CacheType.CacheOnDiskOnly);
```

- `Cache.setCacheType(CacheType.CacheOnDiskOnly)`: Ez a beállítás biztosítja, hogy a cache ne legyen memóriában, ami előnyös nagy PSD fájlok kezelésekor anélkül, hogy túl sok RAM-ot fogyasztana.

### 3. lépés: Maximális lemez- és memória cache méret beállítása
Most korlátozzuk a cache méreteket. Ez kulcsfontosságú, mivel a korlátlan cache teljesítményproblémákat okozhat.
```java
Cache.setMaxDiskSpaceForCache(1073741824); // 1 gigabyte
Cache.setMaxMemoryForCache(1073741824); // 1 gigabyte
```

- `Cache.setMaxDiskSpaceForCache(1073741824)`: 1 GB limitet állít be a lemezen lévő cache számára. A méretet igényei szerint módosíthatja.  
- `Cache.setMaxMemoryForCache(1073741824)`: Hasonlóan korlátozza a memóriában lévő cache-t, biztosítva, hogy az alkalmazás ne használjon túl sok memóriát.

### 4. lépés: Cache újraelosztási stratégia kezelése
A cache újraelosztásának kezelése elengedhetetlen a teljesítmény fenntartásához. Íme, hogyan állíthatja be.
```java
Cache.setExactReallocateOnly(false);
```

- `Cache.setExactReallocateOnly(false)`: Ha `false`‑ra van állítva, az Aspose rugalmasabban kezeli a cache újraelosztását, ami jobb teljesítményhez vezethet.

### 5. lépés: Allokált cache méret ellenőrzése
Ez a lépés a cache memória- vagy lemezre allokált bájtjainak nyomon követéséről szól. Implementáljuk ezt:
```java
long l1 = Cache.getAllocatedDiskBytesCount();
long l2 = Cache.getAllocatedMemoryBytesCount();
```

- `long l1`: A lemezen allokált bájtok számát tárolja.  
- `long l2`: A memóriában allokált bájtok számát tárolja.  
Ezeket az értékeket bármikor ellenőrizheti, hogy biztosítsa, hogy az alkalmazás a várt módon kezeli a memória- és lemezhasználatot.

### 6. lépés: PSD kép létrehozása
Miután beállítottuk a cache konfigurációkat, hozzunk létre egy egyszerű PSD képet.
```java
PsdOptions options = new PsdOptions();
Color[] color = { Color.getRed(), Color.getBlue(), Color.getBlack(), Color.getWhite() };
options.setPalette(new ColorPalette(color));
options.setSource(new StreamSource(new ByteArrayInputStream(new byte[0])));
RasterImage image = (RasterImage) Image.create(options, 100, 100);
```

- `PsdOptions options`: Ez az objektum lehetővé teszi a Photoshop kép létrehozásakor megadandó beállítások specifikálását.  
- `Color[] color`: Egy tömb, amely a képpalettában használandó színeket tartalmazza.

### 7. lépés: Pixeladatok mentése a képbe
Most töltsük fel a képet pixeladatokkal, és mentsük el.
```java
Color[] pixels = new Color[10000];
for (int i = 0; i < pixels.length; i++) {
    pixels[i] = Color.getWhite();
}
image.savePixels(image.getBounds(), pixels);
```

- `Color[] pixels`: Ez egy színobjektumok tömbje. Itt fehér pixelekkel töltjük fel.  
- `image.savePixels(image.getBounds(), pixels)`: Ez a metódus elmenti a pixeladatokat a képbe. Frissíti a képet a definiált színekkel.

### 8. lépés: Allokált cache nyomon követése a kép létrehozása után
A kép létrehozása után jó gyakorlat újra ellenőrizni, hány bájt lett allokálva a cache‑hez.
```java
long diskBytes = Cache.getAllocatedDiskBytesCount();
long memoryBytes = Cache.getAllocatedMemoryBytesCount();
```

- `long diskBytes`: Rögzíti a kép létrehozása utáni aktuális lemezre allokálást.  
- `long memoryBytes`: Rögzíti a memóriában lévő aktuális allokációt.  
Ez a lépés segít meghatározni, mennyi cache kerül felhasználásra a műveletek után.

### 9. lépés: Helyes felszabadítás ellenőrzése
Végül kulcsfontosságú, hogy minden Aspose.PSD objektumot megfelelően felszabadítsunk a memória szivárgások elkerülése érdekében.
```java
l1 = Cache.getAllocatedDiskBytesCount();
l2 = Cache.getAllocatedMemoryBytesCount();
```

- `l1` és `l2`: Ezek a változók segítenek ellenőrizni a végső allokációt. Ha nem nulla, az azt jelzi, hogy néhány objektum nincs megfelelően felszabadítva.

## Gyakori problémák és megoldások
- **Cache mappa nem jött létre** – Ellenőrizze, hogy az alkalmazásnak írási jogosultsága van‑e a `Cache.setCacheFolder`‑nak megadott útvonalra.  
- **Memóriahiányos hibák** – Győződjön meg róla, hogy a `Cache.setCacheType(CacheType.CacheOnDiskOnly)` alkalmazva van a nagy PSD fájlok betöltése előtt.  
- **Váratlan cache méret** – Használja a `Cache.getAllocated*BytesCount()` metódusokat minden nagyobb művelet után a növekedés nyomon követéséhez.

## Gyakran ismételt kérdések

**Q: Mi az Aspose.PSD?**  
A: Az Aspose.PSD egy .NET és Java fejlesztők számára készült könyvtár, amely programozottan képes Photoshop (PSD) fájlok létrehozására, manipulálására és konvertálására.

**Q: Hogyan ellenőrizhetem az allokált cache méretet?**  
A: Használja a `Cache.getAllocatedDiskBytesCount()` és `Cache.getAllocatedMemoryBytesCount()` metódusokat a jelenlegi cache használat nyomon követéséhez.

**Q: Beállíthatok egy egyéni könyvtárat a cache‑hez?**  
A: Igen, megadhat egy másik könyvtárat a `Cache.setCacheFolder("Your Directory Path")` használatával.

**Q: Ingyen használható az Aspose.PSD?**  
A: Az Aspose.PSD egy fizetős könyvtár, de ingyenes próbaverzióval kezdhet, amely elérhető a [weboldalukon](https://releases.aspose.com/).

**Q: Mi történik, ha nem szabadítom fel az objektumokat?**  
A: Az objektumok felszabadításának elmulasztása memória szivárgáshoz vezethet, ami miatt az alkalmazás több erőforrást használ, mint szükséges.

## Összegzés
A cache újraelosztásának vezérlése a **create PSD image java** alkalmazások fejlesztése során jelentős teljesítménykülönbséget eredményezhet. A fenti lépések követésével hatékonyan kezelheti a cache‑t, minimalizálhatja a memóriahasználatot, és magas minőségű PSD fájlokat generálhat az Aspose.PSD for Java‑val. Alkalmazza ezeket a technikákat, és a projektjei simábban fognak futni, valamint jobban skálázhatók lesznek.

---

**Last Updated:** 2026-03-13  
**Tested With:** Aspose.PSD for Java (latest release)  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}