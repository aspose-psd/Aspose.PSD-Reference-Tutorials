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

## Introduction

Ha **java képfeldolgozással** foglalkozik, egy kép gamma‑értékének módosítása alapvető technika a fényerő és kontraszt javítására anélkül, hogy részleteket veszítene. Ebben az útmutatóban bemutatjuk, hogyan használhatja a **Aspose.PSD for Java**‑t gamma‑korrekció alkalmazására egy PSD fájlra, majd az eredmény exportálására TIFF képként. Meg fogja látni, miért gyors, megbízható, és tökéletes a szerver‑oldali képpipeline‑okhoz.

## Quick Answers
- **Mi a gamma‑korrekció feladata?** Átmapolja a fényességi értékeket, hogy a sötét területek világosabbak, a világos területek sötétebbek legyenek, miközben az általános részleteket megőrzi.  
- **Melyik könyvtár kezeli a feldolgozást?** Az Aspose.PSD for Java egy dedikált `adjustGamma` metódust biztosít raszteres képekhez.  
- **Átkonvertálhatom a PSD‑t TIFF‑re ugyanabban a folyamatban?** Igen – a gamma‑állítás után a képet közvetlenül TIFF‑ként mentheti a `TiffOptions` használatával.  
- **Szükség van licencre a fejlesztéshez?** Egy ingyenes próba verzió teszteléshez megfelelő; a termeléshez kereskedelmi licenc szükséges.  
- **Mely Java verziót támogatja?** Az Aspose.PSD a Java 8‑at és újabbakat támogatja.

## What is java image processing?

A Java képfeldolgozás a vizuális adatok manipulálását, elemzését és átalakítását jelenti Java könyvtárak segítségével. A feladatok közé tartozik a méretezés, szűrés, színkorrekció és formátumkonverzió – mindez automatizálható asztali vagy webalkalmazásokban.

## Why use Aspose.PSD for gamma correction?

Az Aspose.PSD egy magas szintű API‑t kínál, amely elrejti a PSD formátum bonyolultságát, így Ön a tényleges képi beállításokra koncentrálhat. Kezeli a gyorsítótárazást, színprofilokat, és egy egyszerű `adjustGamma` hívást biztosít, ami ideálissá teszi a **kép gamma‑korrekciót** és a **psd‑t tiff‑re konvertálást** munkafolyamatokban.

## Prerequisites

Mielőtt belemerülne az útmutatóba, győződjön meg róla, hogy a következő előfeltételek telepítve vannak:

1. **Java fejlesztői környezet** – Győződjön meg róla, hogy a rendszerén telepítve van egy Java fejlesztői környezet.  
2. **Aspose.PSD könyvtár** – Töltse le és integrálja az Aspose.PSD könyvtárat a Java projektjébe. A szükséges erőforrásokat megtalálja a [documentation](https://reference.aspose.com/psd/java/) oldalon.  
3. **Minta kép** – Készítsen elő egy PSD mintaképet, amelyet a gamma‑állításhoz fog használni.

## Import Packages

A folyamat elindításához importálja a szükséges csomagokat a Java projektjébe. Ez előkészíti az Aspose.PSD funkciók zökkenőmentes használatát.

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.psd.fileformats.tiff.enums.TiffPhotometrics;
import com.aspose.psd.imageoptions.TiffOptions;
```

## Step 1: Load the Image

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

## Step 2: Adjust Gamma

Most állítsa be a betöltött kép gamma‑értékét a `adjustGamma` metódus segítségével. Finomhangolja a gamma‑értékeket az igényei szerint.

```java
// Adjust the gamma
rasterImage.adjustGamma(2.2f, 2.2f, 2.2f);
```

## Step 3: Create TiffOptions

Hozzon létre egy `TiffOptions` példányt a keletkezett képhez. Állítson be különféle tulajdonságokat, például a mintánkénti bitek számát és a fotometrikus opciókat, hogy a kimenetet az Ön specifikációihoz igazítsa.

```java
// Create an instance of TiffOptions for the resultant image
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
int[] ushort = { 8, 8, 8 };
tiffOptions.setBitsPerSample(ushort);
tiffOptions.setPhotometric(TiffPhotometrics.Rgb);
```

## Step 4: Save the Resultant Image

Mentse a módosított képet TIFF formátumban a korábban definiált `TiffOptions` használatával.

```java
// Save the resultant image to TIFF format
String destName = dataDir + "AdjustGamma_out.tiff";
rasterImage.save(destName, tiffOptions);
```

## Common Issues and Solutions

| Issue | Why it Happens | How to Fix |
|-------|----------------|------------|
| **A kép kifakult** | A gamma érték túl magas (pl. > 2,5) | Csökkentse a gamma tényezőt 1,8 és 2,2 közötti értékre. |
| **`rasterImage.isCached()` hamisat ad vissza** | A kép még nincs betöltve a memóriába | Hívja meg a `rasterImage.cacheData()` metódust a gamma beállítása előtt. |
| **A TIFF fájl mérete nagy** | A mintánkénti bitek 16‑bitre vannak állítva | Használjon 8‑bit mintát (`{8,8,8}`), ahogy a példában látható. |

## Frequently Asked Questions

**K: Alkalmazhatok különböző gamma értékeket minden színcsatornára?**  
V: Igen – a `adjustGamma` metódus külön float értékeket fogad a vörös, zöld és kék csatornákhoz.

**K: Lehetséges több képi beállítást láncolni a mentés előtt?**  
V: Teljesen. Méretezést, vágást vagy színkorrekciót hajthat végre sorozatosan ugyanazon a `RasterImage` példányon.

**K: Az Aspose.PSD támogatja a többoldalas PSD fájlokat?**  
V: Igen, minden réteg egyenként hozzáférhető és feldolgozható.

**K: Milyen formátumokra exportálhatok a TIFF-en kívül?**  
V: Az Aspose.PSD támogatja a PNG, JPEG, BMP és számos más formátumot a megfelelő opcióosztályok segítségével.

## Conclusion

Gratulálunk! Sikeresen végrehajtotta a **java képfeldolgozást** egy PSD fájl gamma‑beállításával és TIFF képként való exportálásával az Aspose.PSD for Java segítségével. Ez a munkafolyamat finomhangolt vezérlést biztosít a kép fényerő és kontrasztja felett, így ideális automatizált grafikai pipeline‑okhoz, webszolgáltatásokhoz vagy asztali segédprogramokhoz.

---

**Legutóbb frissítve:** 2025-12-21  
**Tesztelve:** Aspose.PSD 24.11 for Java  
**Szerző:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

## GYIK

### Q1: Where can I find the Aspose.PSD documentation?

V1: A dokumentációt a [https://reference.aspose.com/psd/java/](https://reference.aspose.com/psd/java/) oldalon érheti el.

### Q2: How do I download Aspose.PSD for Java?

V2: A könyvtárat a [https://releases.aspose.com/psd/java/](https://releases.aspose.com/psd/java/) oldalról töltheti le.

### Q3: Where can I purchase Aspose.PSD?

V3: Az Aspose.PSD megvásárlásához látogassa meg a [https://purchase.aspose.com/buy](https://purchase.aspose.com/buy) oldalt.

### Q4: Is there a free trial available?

V4: Igen, egy ingyenes próbaverziót a [https://releases.aspose.com/](https://releases.aspose.com/) oldalon tekinthet meg.

### Q5: Where can I seek support for Aspose.PSD?

V5: Támogatásért látogassa meg az Aspose.PSD fórumot a [https://forum.aspose.com/c/psd/34](https://forum.aspose.com/c/psd/34) oldalon.