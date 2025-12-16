---
date: 2025-12-15
description: Naučte se, jak převést PSD na PNG a otáčet vrstvy PSD v Javě pomocí Aspose.PSD.
  Krok za krokem průvodce s ukázkami kódu.
linktitle: Convert PSD to PNG and Rotate Layers in PSD Files using Java
second_title: Aspose.PSD Java API
title: Převod PSD na PNG a otáčení vrstev v souborech PSD pomocí Javy
url: /cs/java/advanced-psd-layer-features-effects/rotate-layers-psd-files/
weight: 21
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Převod PSD na PNG a otáčení vrstev v souborech PSD pomocí Javy

## Úvod
Pokud potřebujete **převést PSD na PNG** a zároveň otáčet vrstvy, tento průvodce je pro vás. Ať už vytváříte nástroj pro dávkové zpracování nebo integrujete manipulaci s obrázky do webové služby, programové řešení šetří čas a odstraňuje závislost na Adobe Photoshopu. V tomto tutoriálu vám ukážeme **jak otáčet vrstvy PSD** a exportovat výsledek jako PNG pomocí knihovny Aspose.PSD pro Javu. Pojďme si zapřát rukávy a zefektivnit váš designový workflow!

## Rychlé odpovědi
- **Jakou knihovnu mohu použít?** Aspose.PSD for Java  
- **Mohu otáčet a převádět najednou?** Ano – otočte PSD a poté uložte jako PNG  
- **Potřebuji licenci?** Bezplatná zkušební verze funguje pro testování; placená licence je vyžadována pro produkci  
- **Jaká verze Javy je podporována?** Java 8 a novější  
- **Je výstup PNG průhledný?** Ano, pokud nastavíte `PngColorType.TruecolorWithAlpha`

## Co je „převod PSD na PNG“?
Převod Photoshop dokumentu (PSD) na PNG obrázek znamená extrahování vizuálního obsahu – včetně všech vrstev, masek a průhlednosti – do široce podporovaného rastrového formátu. PNG zachovává alfa kanály, což jej činí ideálním pro webovou grafiku, miniatury a další zpracování obrázků.

## Proč použít Aspose.PSD pro Javu k převodu PSD na PNG a otáčení vrstev PSD?
- **Není potřeba Photoshop** – funguje na jakémkoli serveru nebo v CI prostředí  
- **Plná podpora vrstev** – zachovává průhlednost a efekty vrstev  
- **Jednoduché API** – otáčejte, převracujte a ukládejte pomocí několika volání metod  
- **Cross‑platform** – běží na Windows, Linuxu i macOS  

## Předpoklady
Než se ponoříme do kódu, ujistěte se, že máte následující:

- **Java Development Kit (JDK)** – stáhněte z [Oracle website](https://www.oracle.com/java/technologies/javase-downloads.html).  
- **Integrated Development Environment (IDE)** – IntelliJ IDEA, Eclipse nebo NetBeans jsou všechny v pořádku.  
- **Aspose.PSD for Java library** – získejte nejnovější JAR ze [release page](https://releases.aspose.com/psd/java/).  
- **Základní znalosti Javy** – povědomí o třídách, objektech a zpracování výjimek.

## Průvodce krok za krokem

### Krok 1: Nastavte svůj Java projekt
Vytvořte nový Java projekt ve svém IDE a přidejte Aspose.PSD JAR do cesty sestavení projektu.

### Krok 2: Importujte požadované třídy
Přidejte následující importy na začátek vašeho Java zdrojového souboru:

```java
import com.aspose.psd.Image;
import com.aspose.psd.RotateFlipType;
import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.PngOptions;
```

Tyto třídy vám poskytují přístup k načítání obrázku, otáčení a specifickým možnostem pro PNG.

### Krok 3: Definujte cesty k souborům
Určete, kde se nachází váš zdrojový PSD a kam mají být výstupní soubory zapsány.

```java
String dataDir = "Your Document Directory"; // Change this to your actual document directory.
String sourceFile = dataDir + "1.psd"; // Source PSD file
String pngPath = dataDir + "RotateFlipTest2617.png"; // Output PNG file path
String psdPath = dataDir + "RotateFlipTest2617.psd"; // Output PSD file path
```

> **Pro tip:** Používejte absolutní cestu během testování, abyste se vyhnuli chybám „file not found“.

### Krok 4: Načtěte soubor PSD
Načtěte PSD do manipulovatelného objektu.

```java
PsdImage im = (PsdImage) Image.load(sourceFile);
```

Nyní `im` představuje celý Photoshop dokument, včetně všech vrstev.

### Krok 5: Otočte obrázek (Jak otočit PSD)
Vyberte typ otáčení z `RotateFlipType`. V tomto příkladu otáčíme o 270° a převracíme obě osy.

```java
int flipType = RotateFlipType.Rotate270FlipXY; // Choose the rotation type
im.rotateFlip(flipType); // Rotate the image
```

Klidně experimentujte s jinými hodnotami, jako je `Rotate90FlipNone` nebo `Rotate180FlipX`.

### Krok 6: Uložte otočený obrázek jako PNG (převod PSD na PNG)
Nastavte PNG možnosti tak, aby zachovaly průhlednost, a poté uložte.

```java
PngOptions options = new PngOptions();
options.setColorType(PngColorType.TruecolorWithAlpha); // Preserve transparency
im.save(pngPath, options); // Save the rotated image
```

Výsledné PNG si zachovává průhlednost vrstev, takže je připravené pro webové použití.

### Krok 7: Uložte upravený PSD (volitelné)
Pokud potřebujete také nový PSD s aplikovaným otáčením, uložte jej zpět.

```java
im.save(psdPath);
```

Nyní máte jak PNG náhled, tak aktualizovaný soubor PSD.

## Časté problémy a řešení
- **File not found:** Ověřte, že `dataDir` končí oddělovačem cesty (`/` nebo `\`).  
- **OutOfMemoryError on large PSDs:** Zvyšte velikost haldy JVM (`-Xmx2g`).  
- **Transparency lost:** Ujistěte se, že je nastaveno `PngColorType.TruecolorWithAlpha`; jinak bude PNG uloženo bez alfa kanálu.

## Často kladené otázky

### Můžu otočit konkrétní vrstvu v souboru PSD?
Ano, můžete použít `Layer.rotateFlip()` na jednotlivých vrstvách po iteraci přes `im.getLayers()`.

### Existují nějaká omezení výkonu u Aspose.PSD pro Javu?
Knihovna zvládá většinu souborů efektivně, ale extrémně velké PSD (>500 MB) mohou vyžadovat další paměť.

### Je Aspose.PSD zdarma k použití?
Aspose nabízí bezplatnou zkušební verzi, ale pro produkci je potřeba placená licence. Podívejte se na [temporary license](https://purchase.aspose.com/temporary-license/) pro testování.

### Kde najdu podrobnou dokumentaci?
Komplexní dokumentaci najdete na [Aspose.PSD Documentation](https://reference.aspose.com/psd/java/).

### Co dělat, když narazím na problémy s Aspose.PSD?
Požádejte o pomoc na [Aspose Support Forum](https://forum.aspose.com/c/psd/34).

## Další často kladené otázky

**Q: Zachovává převod PSD na PNG efekty vrstev?**  
**A:** Ano, když uložíte s `PngColorType.TruecolorWithAlpha`, většina vizuálních efektů je rasterizována do PNG.

**Q: Můžu dávkově zpracovat více souborů PSD?**  
**A:** Rozhodně. Zabalte kód do smyčky, která iteruje přes adresář souborů PSD.

**Q: Je možné nastavit úroveň komprese PNG?**  
**A:** Třída `PngOptions` poskytuje metodu `setCompressionLevel(int)` pro jemné ladění.

**Q: Potřebuji zavřít objekt obrázku?**  
**A:** `PsdImage` implementuje `Closeable`; zavolejte `im.close()` v `finally` bloku nebo použijte try‑with‑resources.

**Q: Bude otočené PNG mít stejné rozměry jako originál?**  
**A:** Otáčení o 90° nebo 270° prohodí šířku a výšku. PNG bude odrážet novou orientaci.

## Závěr
Využitím Aspose.PSD pro Javu můžete **převést PSD na PNG** a **otočit vrstvy PSD** pomocí několika řádků kódu. Tento přístup eliminuje potřebu Photoshopu, urychluje automatizované workflow a dává vám plnou kontrolu nad výstupem obrázku. Vyzkoušejte to ve svých projektech a uvidíte, kolik času ušetříte!

---

**Last Updated:** 2025-12-15  
**Tested With:** Aspose.PSD for Java 24.11  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}