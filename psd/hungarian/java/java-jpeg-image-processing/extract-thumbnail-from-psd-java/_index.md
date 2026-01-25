---
date: 2026-01-25
description: Tanulja meg, hogyan lehet bélyegképet kinyerni PSD fájlokból az Aspose.PSD
  for Java használatával. Kövesse ezt a lépésről‑lépésre útmutatót a betöltéshez,
  kinyeréshez és a bélyegképek gyors mentéséhez.
linktitle: Extract Thumbnail from PSD in Java
second_title: Aspose.PSD Java API
title: Miniatűr kinyerése PSD‑ből Java‑ban
url: /hu/java/java-jpeg-image-processing/extract-thumbnail-from-psd-java/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Miniatűr kinyerése PSD-ből Java-ban

## Bevezetés
Ebben az útmutatóban megtanulja, **hogyan nyerjen ki miniatűrt PSD** fájlokból az Aspose.PSD Java könyvtár segítségével. A miniatűrök apró előnézeti képek, amelyek a PSD dokumentumokba vannak beágyazva, és ezek kinyerése segíthet gyors előnézetek generálásában, képgalériák létrehozásában, vagy a tárolás csökkentésében, ha csak a műalkotás kis reprezentációjára van szükség. Lépésről lépésre végigvezetünk a projekt beállításától a kinyert miniatűr szabványos képfájlként történő mentéséig.

## Gyors válaszok
- **Miről szól ez az útmutató?** Miniatűr kép kinyerése és mentése PSD fájlból az Aspose.PSD for Java segítségével.  
- **Melyik könyvtár szükséges?** Aspose.PSD for Java (letölthető a hivatalos Aspose weboldalról).  
- **Szükség van licencre?** Ideiglenes vagy teljes licenc szükséges a termelési használathoz; ingyenes próbaverzió elérhető.  
- **Milyen kimeneti formátumot használ?** A példa a miniatűrt JPEG fájlként menti, de bármely támogatott formátum választható.  
- **Mennyi időt vesz igénybe a megvalósítás?** Körülbelül 5‑10 perc egy olyan fejlesztőnek, aki ismeri az alap Java koncepciókat.

## Mi az a „thumbnail kinyerése PSD-ből”?
A thumbnail kinyerése PSD-ből azt jelenti, hogy elolvassuk a Photoshop által a fájl erőforrás szekciójában tárolt kis előnézeti képet. Ez az előnézet általában alacsony felbontású változata a teljes vásznak, így ideális a gyors betöltéshez fájl böngészőkben vagy web galériákban.

## Miért érdemes thumbnail-eket kinyerni az Aspose.PSD-vel?
- **Sebesség:** Nem kell megnyitni a teljes PSD-t egy grafikus szerkesztőben; a thumbnail már be van ágyazva.  
- **Automatizálás:** Tökéletes nagy képtárak kötegelt feldolgozásához.  
- **Kereszt‑platform:** Minden olyan operációs rendszeren működik, amely támogatja a Java-t, Photoshop nélkül.  
- **Formátum rugalmasság:** A thumbnail átalakítható JPEG, PNG vagy bármely, az Aspose.PSD által támogatott formátumba.

## Előfeltételek
Mielőtt elkezdenénk, győződjön meg arról, hogy a következők be vannak állítva:
- Java Development Kit (JDK) telepítve van a rendszerén.  
- Aspose.PSD for Java könyvtár. Letöltheti [innen](https://releases.aspose.com/psd/java/).  
- Alapvető Java programozási ismeretek.

## Csomagok importálása
A kezdéshez vegye fel a szükséges Aspose.PSD csomagot a Java osztályába:
```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.resources.Thumbnail4Resource;
import com.aspose.psd.fileformats.psd.resources.ThumbnailResource;
import com.aspose.psd.imageoptions.JpegOptions;
```

## Hogyan nyerjünk ki thumbnail-t PSD-ből az Aspose.PSD for Java használatával
Az alábbiakban a lépésről‑lépésre útmutató. Minden lépés rövid magyarázatot tartalmaz, majd a pontos kódot, amelyet másolni kell.

### 1. lépés: PSD fájl betöltése
Először töltse be azt a PSD fájlt, amely a kinyerni kívánt thumbnail-t tartalmazza.
```java
String dataDir = "Your_Document_Directory/";
PsdImage image = (PsdImage)Image.load(dataDir + "your_file.psd");
```
Cserélje le a `"Your_Document_Directory/"`-t a PSD fájlja elérési útjára, és a `"your_file.psd"`-t a PSD fájl nevére.

### 2. lépés: Képernyő erőforrások iterálása
Iteráljon a képernyő erőforrásokon, hogy megtalálja a thumbnail erőforrást.
```java
for (int i = 0; i < image.getImageResources().length; i++) {
    if (image.getImageResources()[i] instanceof ThumbnailResource) {
        ThumbnailResource thumbnail = (ThumbnailResource) image.getImageResources()[i];
        
        // Extract thumbnail data
        int[] data = thumbnail.getThumbnailArgb32Data();
        
        // Create a new image with the extracted thumbnail data
        PsdImage extractedThumbnailImage = new PsdImage(thumbnail.getWidth(), thumbnail.getHeight());
        extractedThumbnailImage.saveArgb32Pixels(extractedThumbnailImage.getBounds(), data);
        
        // Save the extracted thumbnail as a separate JPEG file
        extractedThumbnailImage.save(dataDir + "extracted_thumbnail.jpg", new JpegOptions());
        
        // Output success message
        System.out.println("Thumbnail extracted and saved successfully.");
        
        break; // Exit the loop once thumbnail is found and processed
    }
}
```

### 3. lépés: Kinyert thumbnail mentése
Az előző lépésben lévő kód már elmenti a thumbnail-t JPEG fájlként `extracted_thumbnail.jpg` néven ugyanabban a könyvtárban. A fájl nevét vagy formátumát a `save` metódus paramétereinek módosításával változtathatja meg.

### 4. lépés: Különböző thumbnail típusok kezelése
Ha a PSD fájl többféle thumbnail típust is tartalmazhat, például `Thumbnail4Resource`, a logikát hasonlóan kibővítheti ezek kezelésére. Egyszerűen adjon hozzá egy `instanceof Thumbnail4Resource` ellenőrzést a ciklusba, és dolgozza fel ugyanazzal a mintával.

## Gyakori problémák és megoldások
- **Nem található thumbnail:** Nem minden PSD fájl tartalmaz thumbnail erőforrást. Ellenőrizze a forrásfájlt Photoshopban (File → Export → Thumbnail), vagy használjon egy másik PSD-t, amely tartalmaz előnézetet.  
- **Nem támogatott képformátum hiba:** Győződjön meg róla, hogy a legújabb Aspose.PSD verziót használja, amely támogatja a célformátumot.  
- **Jogosultsági hiba mentéskor:** Ellenőrizze, hogy az alkalmazásnak írási joga van-e a kimeneti könyvtárhoz.

## Gyakran feltett kérdések

**Q: Mi az Aspose.PSD?**  
A: Az Aspose.PSD egy Java könyvtár, amely lehetővé teszi a fejlesztők számára, hogy programozott módon dolgozzanak PSD és más képformátumokkal.

**Q: Hol találok további dokumentációt az Aspose.PSD for Java-hoz?**  
A: A részletes API referenciákért és példákért tekintse meg a [dokumentációt](https://reference.aspose.com/psd/java/).

**Q: Próbálhatom-e ingyenesen az Aspose.PSD-t vásárlás előtt?**  
A: Igen, letölthet egy [ingyenes próbaverziót](https://releases.aspose.com/), hogy felmérje a könyvtár képességeit.

**Q: Hogyan szerezhetek ideiglenes licencet az Aspose.PSD-hez?**  
A: Ideiglenes licenceket itt szerezhet: [here](https://purchase.aspose.com/temporary-license/).

**Q: Alkalmas-e az Aspose.PSD kereskedelmi felhasználásra?**  
A: Igen, az Aspose.PSD személyes és kereskedelmi projektekben is használható a licencfeltételek szerint.

## Összegzés
Ebben az útmutatóban megvizsgáltuk, hogyan **nyerhetünk ki thumbnail-t PSD** fájlokból az Aspose.PSD for Java használatával. A fenti lépések követésével hatékonyan lekérheti és elmentheti a PSD dokumentumokba beágyazott thumbnail-eket, ami gyorsabb előnézeteket és egyszerűbb képfolyamatokat tesz lehetővé.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Last Updated:** 2026-01-25  
**Tested With:** Aspose.PSD for Java (latest release)  
**Author:** Aspose