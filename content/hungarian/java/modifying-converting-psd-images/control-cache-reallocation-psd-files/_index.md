---
title: A gyorsítótár újraelosztásának vezérlése PSD-fájlokban
linktitle: A gyorsítótár újraelosztásának vezérlése PSD-fájlokban
second_title: Aspose.PSD Java API
description: A PSD-fájlok gyorsítótár-újraelosztásának kezelése az Aspose.PSD for Java segítségével. Ismerje meg, hogyan optimalizálhatja hatékonyan a memóriát és a fájlkezelést – ideális megoldás a fejlesztők számára.
type: docs
weight: 22
url: /hu/java/modifying-converting-psd-images/control-cache-reallocation-psd-files/
---
## Bevezetés
Amikor programozottan dolgozik képekkel és Photoshop-fájlokkal, a hatékonyság kulcsfontosságú tényező. Az Aspose.PSD for Java robusztus szolgáltatásokat kínál a PSD-fájlok zökkenőmentes kezeléséhez és kezeléséhez. A teljesítmény optimalizálásának egyik alapvető szempontja a gyorsítótár újraelosztásának vezérlése. A gyorsítótár-kezelés segít fenntartani az egyensúlyt a memória és a lemezhasználat között, biztosítva az alkalmazás zökkenőmentes működését, váratlan összeomlások és lassulások nélkül. 
## Előfeltételek
Mielőtt rátérnénk a kódolási részre, néhány dolgot meg kell győződnie arról, hogy minden zökkenőmentesen menjen:
1. Java Development Kit (JDK): Győződjön meg arról, hogy a JDK telepítve van a gépen. Letöltheti innen[Az Oracle webhelye](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).
2. Aspose.PSD for Java: Le kell töltenie az Aspose.PSD könyvtárat. A legújabb kiadást megtalálod[itt](https://releases.aspose.com/psd/java/).
3. IDE beállítása: Az integrált fejlesztőkörnyezet (IDE), például az IntelliJ IDEA vagy az Eclipse megkönnyíti a kód kezelését.
4. A Java alapvető ismerete: A Java programozás ismerete segít jobban megérteni a fogalmakat és a kódrészleteket.
5.  Aspose Licenc (opcionális): Ha el szeretné távolítani a vízjeleket, és teljes funkcionalitást szeretne elérni, fontolja meg a licenc megvásárlását[itt](https://purchase.aspose.com/buy) vagy próbálja ki az ingyenes próbaverziót[itt](https://releases.aspose.com/).
## Csomagok importálása
Mielőtt elkezdenénk írni a kódot, győződjünk meg arról, hogy a szükséges csomagok importálva vannak. Az alábbiakban egy rövid lista található arról, hogy mit kell szerepeltetni a Java fájl elején:
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
## 1. lépés: Az adattár beállítása
Először is be kell állítania egy könyvtárat, ahol a gyorsítótár fájljait tárolni szeretné. Ez elengedhetetlen a gyorsítótár hatékony kezeléséhez.
```java
String dataDir = "Your Document Directory";
Cache.setCacheFolder(dataDir);
```

- String dataDir: Határozza meg a dokumentum-gyorsítótár könyvtárát.
- Cache.setCacheFolder(dataDir): Ez a módszer a gyorsítótár mappáját a megadott könyvtárba állítja. Az Aspose által létrehozott gyorsítótárak mostantól itt lesznek tárolva az alapértelmezett ideiglenes könyvtár helyett.
## 2. lépés: A gyorsítótár konfigurálása lemezre
Ezután megadjuk, hogy a gyorsítótárat csak a lemezen szeretnénk tárolni. Ez különösen akkor hasznos, ha az alkalmazás nagy fájlokat használ, és biztosítani szeretné, hogy a memória szabad maradjon.
```java
Cache.setCacheType(CacheType.CacheOnDiskOnly);
```

- Cache.setCacheType(CacheType.CacheOnDiskOnly): Ez a beállítás biztosítja, hogy a gyorsítótár ne legyen a memóriában, ami előnyös a nagy PSD-fájlok kezeléséhez anélkül, hogy túl sok RAM-ot fogyasztana.
## 3. lépés: A lemez- és memória-gyorsítótár maximális méretének beállítása
Most korlátozzuk a gyorsítótár méretét. Ez döntő fontosságú, mert a korlátlan gyorsítótár teljesítményproblémákat okozhat.
```java
Cache.setMaxDiskSpaceForCache(1073741824); // 1 gigabájt
Cache.setMaxMemoryForCache(1073741824); // 1 gigabájt
```

- Cache.setMaxDiskSpaceForCache(1073741824): 1 GB-os korlátot állít be a lemezen lévő gyorsítótár számára. Ezt a méretet igény szerint állíthatja be.
- Cache.setMaxMemoryForCache(1073741824): Hasonlóképpen korlátozza a memórián belüli gyorsítótárat, biztosítva, hogy az alkalmazás ne használjon túl sok memóriát.
## 4. lépés: A gyorsítótár újraelosztási stratégiájának kezelése
A gyorsítótár újraelosztásának kezelése elengedhetetlen a teljesítmény fenntartásához. Így állíthatja be.
```java
Cache.setExactReallocateOnly(false);
```

- Cache.setExactReallocateOnly(false): Ha false értékre van állítva, ez lehetővé teszi az Aspose számára, hogy rugalmasabban kezelje a gyorsítótár újraelosztását, ami jobb teljesítményhez vezethet.
## 5. lépés: Ellenőrizze a lefoglalt gyorsítótár méretét
Ez a lépés annak megfigyeléséről szól, hogy hány bájt van jelenleg lefoglalva a gyorsítótár számára a memóriában vagy a lemezen. Valósítsuk meg:
```java
long l1 = Cache.getAllocatedDiskBytesCount();
long l2 = Cache.getAllocatedMemoryBytesCount();
```

- long l1: Tárolja a lemezen lefoglalt bájtok számát.
- long l2: Tárolja a memóriában lefoglalt bájtok számát. 
Ezeket az értékeket bármikor ellenőrizheti, hogy megbizonyosodjon arról, hogy az alkalmazás a várt módon kezeli a memória- és lemezhasználatot.
## 6. lépés: PSD-kép létrehozása
Most, hogy beállítottuk a gyorsítótár-konfigurációkat, hozzunk létre egy egyszerű PSD-képet.
```java
PsdOptions options = new PsdOptions();
Color[] color = { Color.getRed(), Color.getBlue(), Color.getBlack(), Color.getWhite() };
options.setPalette(new ColorPalette(color));
options.setSource(new StreamSource(new ByteArrayInputStream(new byte[0])));
RasterImage image = (RasterImage) Image.create(options, 100, 100);
```

- PsdOptions beállítások: Ez az objektum lehetővé teszi a beállítások megadását a Photoshop kép létrehozásakor.
- Szín[] szín: A képpalettán használt színeket tartalmazó tömb.
## 7. lépés: Pixeladatok mentése a képre
Most töltsük fel a képünket pixeladatokkal, és mentsük el.
```java
Color[] pixels = new Color[10000];
for (int i = 0; i < pixels.length; i++) {
    pixels[i] = Color.getWhite();
}
image.savePixels(image.getBounds(), pixels);
```

- Szín[] pixel: Ez színes objektumok tömbje. Itt fehér képpontokkal töltjük fel.
- image.savePixels(image.getBounds(), pixels): Ez a módszer a képpontok adatait menti a képbe. Frissíti a képet az általunk meghatározott színekkel.
## 8. lépés: A lefoglalt gyorsítótár figyelése a kép létrehozása után
A kép létrehozása után célszerű újra ellenőrizni, hogy hány bájt van lefoglalva a gyorsítótár számára.
```java
long diskBytes = Cache.getAllocatedDiskBytesCount();
long memoryBytes = Cache.getAllocatedMemoryBytesCount();
```

- long diskBytes: A lemezkép létrehozása után rögzíti az aktuális lefoglalást a lemezen.
- hosszú memóriaBájtok: Rögzíti az aktuális lefoglalást a memóriában. 
Ez a lépés segít meghatározni, hogy a műveletek után mennyi gyorsítótárat használnak fel.
## 9. lépés: Ellenőrizze a megfelelő ártalmatlanítást
Végezetül kulcsfontosságú annak biztosítása, hogy az összes Aspose.PSD objektumot megfelelően ártalmatlanítsa a memóriaszivárgás elkerülése érdekében.
```java
l1 = Cache.getAllocatedDiskBytesCount();
l2 = Cache.getAllocatedMemoryBytesCount();
```

- l1 és l2: Ezek a változók segítenek a végső kiosztás ellenőrzésében. Ha ezek nem nullák, az azt jelzi, hogy egyes tárgyakat nem megfelelően dobtak ki.
## Következtetés
A gyorsítótár újraelosztásának vezérlése az Aspose.PSD for Java programban jelentős változást hozhat az alkalmazás teljesítményében. A fent vázolt lépések követésével hatékonyan kezelheti a gyorsítótárat, minimalizálhatja a memóriahasználatot, és hatékonyan hozhat létre gyönyörű PSD-fájlokat. Használja ezeket a technikákat, és figyelje, hogy alkalmazásai optimális teljesítménnyel fejlődnek!
## GYIK
### Mi az Aspose.PSD?
Az Aspose.PSD egy könyvtár a .NET- és Java-fejlesztők számára Photoshop-fájlok (PSD) programozott létrehozásához, kezeléséhez és konvertálásához.
### Hogyan ellenőrizhetem a lefoglalt gyorsítótár méretét?
 Használjon olyan módszereket, mint pl`Cache.getAllocatedDiskBytesCount()` és`Cache.getAllocatedMemoryBytesCount()` az aktuális gyorsítótár-használat figyelésére.
### Beállíthatok egyéni könyvtárat a gyorsítótárhoz?
 Igen, a használatával megadhat egy másik könyvtárat is`Cache.setCacheFolder("Your Directory Path")`.
### Ingyenesen használható az Aspose.PSD?
Az Aspose.PSD egy fizetős könyvtár, de elkezdheti a rajtuk elérhető ingyenes próbaverzióval[weboldal](https://releases.aspose.com/).
### Mi történik, ha nem dobok ki tárgyakat?
Ha nem dobja ki az objektumokat, az memóriaszivárgáshoz vezethet, ami miatt az alkalmazás a szükségesnél több erőforrást használ fel.