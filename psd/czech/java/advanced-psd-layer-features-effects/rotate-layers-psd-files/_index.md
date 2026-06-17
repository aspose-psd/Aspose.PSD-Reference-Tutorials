---
date: 2026-02-17
description: Naučte se, jak převést PSD na PNG, zachovat průhlednost PNG a otáčet
  vrstvy PSD v Javě pomocí Aspose.PSD. Podrobný návod krok za krokem s ukázkami kódu.
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
Pokud potřebujete **převést PSD na PNG** a zároveň otáčet vrstvy, tento průvodce je pro vás. Ať už vytváříte nástroj pro dávkové zpracování, webovou službu, která potřebuje manipulaci s obrázky za běhu, nebo jen automatizujete pracovní postup designu, provádění toho programově šetří čas a odstraňuje závislost na Adobe Photoshopu. V tomto tutoriálu vás provedeme **jak otáčet vrstvy PSD** a exportovat výsledek jako PNG pomocí knihovny Aspose.PSD pro Javu. Pojďme si zapřít rukávy a nechat váš designový workflow běžet hladce!

## Rychlé odpovědi
- **Jakou knihovnu mohu použít?** Aspose.PSD for Java  
- **Mohu otáčet i převádět najednou?** Ano – otočte PSD a poté uložte jako PNG  
- **Potřebuji licenci?** Bezplatná zkušební verze funguje pro testování; pro produkci je vyžadována placená licence  
- **Která verze Javy je podporována?** Java 8 a novější  
- **Je výstup PNG průhledný?** Ano, pokud nastavíte `PngColorType.TruecolorWithAlpha`  

## Co znamená „převod PSD na PNG“?
Převod dokumentu Photoshopu (PSD) na obrázek PNG znamená extrahování vizuálního obsahu – včetně všech vrstev, masek a průhlednosti – do široce podporovaného rastrového formátu. PNG zachovává alfa kanály, což jej činí ideálním pro webovou grafiku, náhledy a další zpracování obrázků.

## Proč použít Aspose.PSD pro Javu k převodu PSD na PNG a otáčení vrstev PSD?
- **Není potřeba Photoshop** – funguje na jakémkoli serveru nebo v CI prostředí  
- **Plná podpora vrstev** – zachovává průhlednost a efekty vrstev  
- **Jednoduché API** – otáčejte, převracíte a ukládejte pomocí několika volání metod  
- **Cross‑platform** – běží na Windows, Linuxu i macOS  
- **Java image conversion** usnadněná jednou knihovnou  

## Požadavky
Než se ponoříme do kódu, ujistěte se, že máte následující:

- **Java Development Kit (JDK)** – stáhněte z [Oracle website](https://www.oracle.com/java/technologies/javase-downloads.html).  
- **Integrované vývojové prostředí (IDE)** – IntelliJ IDEA, Eclipse nebo NetBeans jsou všechny v pořádku.  
- **Aspose.PSD for Java library** – získejte nejnovější JAR ze [release page](https://releases.aspose.com/psd/java/).  
- **Základní znalost Javy** – povědomí o třídách, objektech a zpracování výjimek.  

## Postup krok za krokem

### Krok 1: Nastavte svůj Java projekt
Vytvořte nový Java projekt ve svém IDE a přidejte Aspose.PSD JAR do cesty sestavení projektu.

### Krok 2: Importujte požadované třídy
Přidejte následující importy na začátek svého Java souboru:

```java
import com.aspose.psd.Image;
import com.aspose.psd.RotateFlipType;
import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.PngOptions;
```

Tyto třídy vám poskytují přístup k načítání obrázku, otáčení a možnostem specifickým pro PNG.

### Krok 3: Definujte cesty k souborům
Určete, kde se nachází váš zdrojový PSD a kam mají být zapsány výstupní soubory.

```java
String dataDir = "Your Document Directory"; // Change this to your actual document directory.
String sourceFile = dataDir + "1.psd"; // Source PSD file
String pngPath = dataDir + "RotateFlipTest2617.png"; // Output PNG file path
String psdPath = dataDir + "RotateFlipTest2617.psd"; // Output PSD file path
```

> **Tip:** Použijte absolutní cestu během testování, aby se předešlo chybám „soubor nenalezen“.

### Krok 4: Načtěte soubor PSD
Načtěte PSD do manipulovatelného objektu.

```java
PsdImage im = (PsdImage) Image.load(sourceFile);
```

Nyní `im` představuje celý dokument Photoshopu, včetně všech vrstev.

### Krok 5: Otočte obrázek (Jak otáčet PSD)
Vyberte typ otáčení z `RotateFlipType`. V tomto příkladu otáčíme o 270° a převracíme obě osy.

```java
int flipType = RotateFlipType.Rotate270FlipXY; // Choose the rotation type
im.rotateFlip(flipType); // Rotate the image
```

Klidně experimentujte s dalšími hodnotami, jako je `Rotate90FlipNone` nebo `Rotate180FlipX`. Toto je část tutoriálu **jak otáčet PSD**.

### Krok 6: Uložte otočený obrázek jako PNG (převod PSD na PNG)
Nastavte možnosti PNG tak, aby zachovaly průhlednost, a poté uložte.

```java
PngOptions options = new PngOptions();
options.setColorType(PngColorType.TruecolorWithAlpha); // Preserve transparency
im.save(pngPath, options); // Save the rotated image
```

Výsledné PNG si zachovává průhlednost vrstev, což zajišťuje **preserve PNG transparency** pro další použití.

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
- **Flip PSD image not behaving as expected:** Zkontrolujte konstantu `RotateFlipType`, kterou jste vybrali; některé konstanty kombinují otáčení a převrácení v jednom kroku.  

## Často kladené otázky

**Q: Mohu otáčet konkrétní vrstvu v souboru PSD?**  
A: Ano, můžete použít `Layer.rotateFlip()` na jednotlivé vrstvy po iteraci přes `im.getLayers()`.

**Q: Existuje nějaké omezení výkonu u Aspose.PSD pro Javu?**  
A: Knihovna zvládá většinu souborů efektivně, ale extrémně velké PSD (>500 MB) mohou vyžadovat více paměti.

**Q: Je Aspose.PSD zdarma k použití?**  
A: Aspose nabízí bezplatnou zkušební verzi, ale pro produkci je potřeba placená licence. Podívejte se na [temporary license](https://purchase.aspose.com/temporary-license/) pro testování.

**Q: Kde najdu podrobnou dokumentaci?**  
A: Kompletní dokumentaci najdete na [Aspose.PSD Documentation](https://reference.aspose.com/psd/java/).

**Q: Co když narazím na problémy při používání Aspose.PSD?**  
A: Požádejte o pomoc na [Aspose Support Forum](https://forum.aspose.com/c/psd/34).

**Q: Zachovává převod PSD na PNG efekty vrstev?**  
A: Ano, při uložení s `PngColorType.TruecolorWithAlpha` jsou většina vizuálních efektů rasterizovány do PNG.

**Q: Můžu dávkově zpracovávat více souborů PSD?**  
A: Rozhodně. Zabalte kód do smyčky, která prochází adresář s PSD soubory.

**Q: Lze nastavit úroveň komprese PNG?**  
A: Třída `PngOptions` poskytuje metodu `setCompressionLevel(int)` pro jemné ladění.

**Q: Musím zavřít objekt obrázku?**  
A: `PsdImage` implementuje `Closeable`; zavolejte `im.close()` v bloku `finally` nebo použijte try‑with‑resources.

**Q: Bude mít otočené PNG stejné rozměry jako originál?**  
A: Otáčením o 90° nebo 270° se vymění šířka a výška. PNG bude odrážet novou orientaci.

## Závěr
Využitím Aspose.PSD pro Javu můžete **převést PSD na PNG**, **preserve PNG transparency** a **rotate PSD** vrstvy pomocí několika řádků kódu. Tento přístup eliminuje potřebu Photoshopu, urychluje automatizované workflow a dává vám plnou kontrolu nad výstupem obrázku. Vyzkoušejte to ve svých projektech a uvidíte, kolik času ušetříte!

---

**Poslední aktualizace:** 2026-02-17  
**Testováno s:** Aspose.PSD for Java 24.11  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}