---
date: 2025-12-21
description: Tanulja meg, hogyan végezhet Java képfeldolgozást a kép gamma beállításával
  az Aspose.PSD segítségével. Lépésről lépésre útmutató a PSD TIFF formátumba konvertálásához
  és a gamma korrekció alkalmazásához.
linktitle: Adjust Gamma of an Image
second_title: Aspose.PSD Java API
title: Java képfeldolgozás – Gamma beállítása az Aspose.PSD-vel
url: /hu/java/advanced-techniques/adjust-gamma/
weight: 23
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Java képfeldolgozás – Gamma beállítása az Aspose.PSD-vel

## Bevezetés

Ha **java képfeldolgozással** foglalkozik, egy kép gamma-értékének módosítása alapvető technika fényerő és kontraszt javítására anélkül, hogy részleteket veszítene. Ebben az útmutatóban bemutatjuk, hogyan használhatja a **Aspose.PSD for Java**-t gamma-korrekció alkalmazására egy PSD fájlra, majd az eredmény exportálására TIFF képként. Meg fogja látni, miért gyors, megbízható, és tökéletes a szerveroldali képpipeline-okhoz.

## Gyors válaszok
- **Mi a gamma-korrekció feladata?** Átmapolja a fényességi értékeket, hogy a sötét területek világosabbak, a világos területek sötétebbek legyenek, csak az általános részleteket kell megőrzi.
- **Melyik könyvtár kezeli a feldolgozást?** Az Aspose.PSD for Java egy dedikált `adjustGamma` metódust biztosít raszteres képekhez.
- **Átkonvertálhatom a PSD-t TIFF-re ugyanabban aban?** Igen – a gamma-állítás után a képet közvetlenül TIFF folyamat-ként mentheti a`TiffOptions` segítségével.
- **Szükség van licencre a fejlesztéshez?** Egy ingyenes próba verzió teszteléshez megfelelő; a termeléshez kereskedelmi licenc szükséges.
- **Mely Java verziót támogatja?** Az Aspose.PSD a Java8-at és újabbakat támogatja.

## Mi az a java képfeldolgozás?

A Java képfeldolgozás a vizuális adatok manipulálását, elemzését és átalakítását jelenti a Java könyvtárak segítségével. A feladatok közé tartozik a méretezés, szűrés, színkorrekció és formátumkonverzió – mindez automatizálható asztali vagy webalkalmazásokban.

## Miért használja az Aspose.PSD-t gamma-korrekcióhoz?

Az Aspose.PSD egy magas szintű API‑t kínál, amely elrejti a PSD formátum bonyolultságát, így Ön a tényleges képi beállításra koncentrálhat. Kezeli a gyorsítótárazást, színprofilokat, és egy egyszerű `adjustGamma` hívást biztosít, ami ideálissá teszi a **kép gamma-korrekciót** és a **psd-t tiff-re konvertálást** munkafolyamatokban.

## Előfeltételek

Mielőtt belemerülne az útmutatóba, g egészben, hogy a következő előfeltételek róla telepítve vannak:

1. **Java fejlesztői környezet** – G újra róla, hogy a rendszeren telepítve van egy Java fejlesztői környezet.
2. **Aspose.PSD könyvtár** – Töltse le és integrálja az Aspose.PSD könyvtárat a Java projektjébe. A szükséges erőforrásokat megtalálja a [documentation](https://reference.aspose.com/psd/java/) oldalon.
3. **Minta kép** – Készítsen elő egy PSD mintaképet, amelyet a gamma-állításhoz fog használni.

## Csomagok importálása

A folyamat elindításához importálja a szükséges csomagokat a Java projektjébe. Ez előkészíti az Aspose.PSD funkciók zökkenőmentes használatát.

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.psd.fileformats.tiff.enums.TiffPhotometrics;
import com.aspose.psd.imageoptions.TiffOptions;
```

## 1. lépés: A kép betöltése

Kezdje a mintapéldány PSD kép betöltésével egy `RasterImage` osztályú példányba. Ez a kiindulópont a későbbi gamma‑állításokhoz.

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

// Load an existing image into an instance of RasterImage class
Image image = Image.load(sourceFile);

// Cast object of Image to RasterImage
RasterImage rasterImage = (RasterImage)image;

// Check if RasterImage is cached for better performance
if (!rasterImage.isCached()) {
    rasterImage.cacheData();
}
```

## 2. lépés: Gamma beállítása

Most állítsa be a betöltött kép gamma‑értékét a `adjustGamma` metódus segítségével. Finomhangolja a gamma‑értékeket az igényei szerint.

```java
// Adjust the gamma
rasterImage.adjustGamma(2.2f, 2.2f, 2.2f);
```

## 3. lépés: TiffOptions létrehozása

Hozzon létre egy `TiffOptions` példányt a keletkezett képhez. Állítson be különféle tulajdonságokat, például a mintánkénti bitek számát és a fotometrikus opciókat, hogy a kimenetet az Ön specifikációihoz igazítsa.

```java
// Create an instance of TiffOptions for the resultant image
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
int[] ushort = { 8, 8, 8 };
tiffOptions.setBitsPerSample(ushort);
tiffOptions.setPhotometric(TiffPhotometrics.Rgb);
```

## 4. lépés: Mentse el a kapott képet

Mentse a módosított képet TIFF formátumban a korábban definiált `TiffOptions` használatával.

```java
// Save the resultant image to TIFF format
String destName = dataDir + "AdjustGamma_out.tiff";
rasterImage.save(destName, tiffOptions);
```

## Gyakori problémák és megoldások

| Kiadás | Miért történik | Hogyan javítható |
|-------|----------------|-------------|
| **A kép kifakult** | A gamma érték túl magas (pl. > 2,5) | Csökkentse a gamma tényezőt 1,8 és 2,2 közötti értékre. |
| **`rasterImage.isCached()` hamisat ad vissza** | A kép még nincs betöltve a memóriába | Hívja meg a `rasterImage.cacheData()` metódust a gamma beállítás előtt. |
| **A TIFF fájlméret nagy** | A mintánkénti bitek 16 bites vannak állítva | Használjon 8 bites mintát (`{8,8,8}`), ahogy a példában látható. |

## Gyakran Ismételt Kérdések

**K: Alkalmazhatok különböző gamma értékeket minden színcsatornára?**
V: Igen – a `adjustGamma` metódus külön float értékeket fogad a vörös, zöld és kék csatornához.

**K: Lehetséges több képi beállítást láncolni a mentés előtt?**
V: Teljesen. Méretezést, vágást vagy színkorrekciót hajthat végre sorozatosan ugyanazon a `RasterImage` példányon.

**K: Az Aspose.PSD támogatja a többoldalas PSD fájlokat?**
V: Igen, minden réteg egyenként hozzáférhető és feldolgozható.

**K: Milyen formátumokra exportálhatok a TIFF-en kívül?**
V: Az Aspose.PSD támogatja a PNG, JPEG, BMP és számos más formátumot a megfelelő opcióosztályok segítségével.

## Következtetés

Gratulálunk! Sikeresen végrehajtotta a **java képfeldolgozást** egy PSD fájl gamma-beállításával és TIFF képként való exportálásával az Aspose.PSD for Java segítségével. Ez a munkafolyamat finomhangolt vezérlést biztosít a kép fényerő és kontrasztja felett, így ideális automatizált grafikai pipeline‑okhoz, webszolgáltatásokhoz vagy asztali segédprogramokhoz.

---

**Legutóbb frissítve:** 2025-12-21  
**Tesztelve:** Aspose.PSD 24.11 for Java  
**Szerző:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
