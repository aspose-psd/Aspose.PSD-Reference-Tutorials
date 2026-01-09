---
date: 2026-01-09
description: Naučte se, jak převést PSD na PNG pomocí Bradleyova prahování v Aspose.PSD
  pro Javu. Tento průvodce ukazuje, jak vybrat optimální práh a efektivně binarizovat
  PSD obrázek.
linktitle: Bradley Thresholding
second_title: Aspose.PSD Java API
title: Převést PSD na PNG s Bradleyovým prahováním (Aspose.PSD Java)
url: /cs/java/image-processing/bradley-thresholding/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Převod PSD na PNG s Bradley Thresholding (Aspose.PSD Java)

Vítejte v tomto komplexním průvodci **convert PSD to PNG** pomocí Bradley Thresholding v Aspose.PSD pro Java. V následujících několika minutách uvidíte, proč je tato technika ideální pro vytváření vysoce kontrastních, binarizovaných PNG souborů z Photoshop dokumentů, a získáte praktický krok‑za‑krokem návod.

## Rychlé odpovědi
- **Mohu převést PSD na PNG pomocí Aspose.PSD?** Ano – načtěte PSD, aplikujte `binarizeBradley` a uložte jako PNG.  
- **Co znamená „zvolit optimální práh“?** Jedná se o hodnotu citlivosti (0‑1), která rozhoduje, jak jsou tmavé/světlé pixely klasifikovány.  
- **Potřebuji licenci pro produkční použití?** Komerční licence je vyžadována; bezplatná zkušební verze funguje pro hodnocení.  
- **Jaké formáty obrázků jsou podporovány pro ukládání?** PNG, JPEG, BMP a mnoho dalších prostřednictvím tříd `ImageOptions`.  
- **Je kód kompatibilní s Java 8 a novějšími?** Naprosto – Aspose.PSD Java API podporuje Java 8+.

## Co je Bradley Thresholding?
Bradley Thresholding je adaptivní binarizační algoritmus, který pro každý pixel vypočítá lokální průměr a porovná intenzitu pixelu s tímto průměrem vynásobeným uživatelem definovaným prahem. Výsledkem je čistý černobílý obrázek, který zachovává důležité detaily.

## Proč převádět PSD na PNG s Bradley Thresholding?
- **Zachovat ostré hrany** – Ideální pro OCR, detekci čárových kódů nebo jakýkoli workflow, který potřebuje jasné oddělení popředí a pozadí.  
- **Snížit velikost souboru** – PNG je bezztrátový, ale po binarizaci bývá často menší.  
- **Kompatibilita napříč platformami** – PNG funguje všude, zatímco PSD je specifické pro Photoshop.  

## Předpoklady
Než se pustíme do práce, ujistěte se, že máte:

1. **Vývojové prostředí Java** – nainstalovaný JDK 8 nebo novější.  
2. **Knihovnu Aspose.PSD** – stáhněte nejnovější JAR z [here](https://releases.aspose.com/psd/java/).  
3. **Ukázkový PSD obrázek** – libovolný PSD soubor, který chcete převést; můžete také použít ukázku poskytnutou v příkladech Aspose.

## Import balíčků
Začněte importováním potřebných tříd do vašeho Java projektu:

```java
import com.aspose.psd.Image;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.PngOptions;
```

## Jak převést PSD na PNG pomocí Bradley Thresholding
Níže je kompletní workflow rozdělený do přehledných, číslovaných kroků. Každý krok obsahuje stručné vysvětlení a přesný kód, který stačí zkopírovat‑vložit.

### Krok 1: Načtení PSD obrázku
Nejprve uveďte cestu k vašemu zdrojovému souboru a načtěte jej pomocí Aspose.PSD.

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";
String destName = dataDir + "binarized_out.png";

// Load an image
PsdImage image = (PsdImage)Image.load(sourceFile);
```

### Krok 2: Zvolit optimální práh
Hodnota prahu (rozsah 0 – 1) řídí agresivitu binarizace. Typickým výchozím bodem je **0.15**, ale můžete ji upravit podle potřeby vašeho obrázku.

```java
// Define threshold value
double threshold = 0.15;
```

### Krok 3: Binarizovat PSD obrázek
Nyní aplikujte Bradley algoritmus. Tento krok **binarize PSD image** na základě vybraného prahu.

```java
// Call BinarizeBradley method and pass the threshold value as a parameter
image.binarizeBradley(threshold);
```

### Krok 4: Uložit výstup jako PNG
Nakonec zapište zpracovaný obrázek na disk ve formátu PNG.

```java
// Save the output image
image.save(destName, new PngOptions());
```

Opakujte tyto kroky pro libovolný počet PSD souborů, které potřebujete zpracovat, a dle potřeby upravujte práh, aby byl dosažen nejlepší vizuální výsledek.

## Časté problémy a tipy
- **Práh příliš nízký/vysoký:** Pokud výstup vypadá příliš šumivě nebo vybledle, upravte hodnotu `threshold` postupně (např. 0.10 – 0.20).  
- **Spotřeba paměti:** Velké PSD soubory mohou být náročné na paměť. Zvažte jejich zpracování po jednom nebo zvýšení velikosti haldy JVM (`-Xmx`).  
- **Náhled před uložením:** Použijte `image.save("preview.bmp", new BmpOptions());` k prohlédnutí binarizovaného výsledku před finálním exportem do PNG.

## Často kladené otázky

**Q: Jaký je rozdíl mezi `binarizeBradley` a jinými metodami thresholdingu?**  
A: `binarizeBradley` vypočítává lokální průměr pro každý pixel, což jej činí odolnějším vůči obrázkům s nerovnoměrným osvětlením ve srovnání s globálním thresholdingem.

**Q: Mohu použít Bradley Thresholding na JPEG nebo BMP soubory?**  
A: Ano. Načtěte libovolný podporovaný formát pomocí `Image.load(...)` a poté zavolejte `binarizeBradley` před uložením.

**Q: Existuje způsob, jak si před uložením prohlédnout binarizovaný obrázek?**  
A: Rozhodně. Použijte libovolnou z možností ukládání obrázků v Aspose.PSD (např. BMP) k vytvoření dočasného náhledového souboru.

**Q: Kde mohu najít další podporu a zdroje?**  
A: Navštivte [Aspose.PSD forum](https://forum.aspose.com/c/psd/34) pro komunitní pomoc a prozkoumejte kompletní [dokumentaci](https://reference.aspose.com/psd/java/) pro pokročilé scénáře.

## Závěr
Nyní jste se naučili, jak **convert PSD to PNG** efektivně tím, že **zvolíte optimální práh** a **binarizujete PSD obrázek** pomocí Bradley Thresholding. Tento přístup je ideální pro workflowy, které vyžadují čisté, vysoce kontrastní PNG výstupy z komplexních Photoshop souborů.

---

**Poslední aktualizace:** 2026-01-09  
**Testováno s:** Aspose.PSD Java 23.12 (nejnovější v době psaní)  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}