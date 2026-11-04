---
date: 2026-11-04
description: Naučte se, jak používat Aspose.PSD pro Java k aplikaci invert adjustment
  layer, dávkovému zpracování PSD obrázků a vytvoření negativních PSD souborů.
keywords:
- how to use aspose
- batch process psd images
- create negative image psd
- image processing java library
- apply multiple adjustment layers
lastmod: 2026-11-04
linktitle: Invert Adjustment Layer
og_description: Jak používat Aspose.PSD pro Java k přidání invert adjustment layer,
  dávkovému zpracování PSD obrázků a vytvoření negativního PSD. Postupujte podle krok‑za‑krokem
  průvodce.
og_image_alt: Screenshot showing Aspose.PSD Java code adding an invert adjustment
  layer
og_title: Jak používat Aspose.PSD k přidání invert adjustment layer v Java
schemas:
- author: Aspose
  dateModified: '2026-11-04'
  description: Learn how to use Aspose.PSD for Java to apply an invert adjustment
    layer, batch process PSD images, and create negative image PSD files.
  headline: How to use Aspose.PSD to add an invert adjustment layer in Java
  type: TechArticle
- questions:
  - answer: Yes, it supports Java 6.0 and later, including Java 8, 11, and 17.
    question: Is Aspose.PSD compatible with all Java versions?
  - answer: Absolutely. After adding the invert layer you can call `addBrightnessAdjustmentLayer()`,
      `addHueSaturationAdjustmentLayer()`, etc., to stack effects.
    question: Can I apply multiple adjustment layers in a single operation?
  - answer: The complete documentation is available [Aspose.PSD Java API reference](https://reference.aspose.com/psd/java/).
    question: Where can I find the full API reference?
  - answer: Yes, you can download a trial version [Aspose.PSD trial download](https://releases.aspose.com/).
    question: Is there a free trial for Aspose.PSD?
  - answer: Request a temporary license [temporary license request page](https://purchase.aspose.com/temporary-license/).
    question: How do I obtain a temporary license for testing?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- aspose psd
- java image processing
- invert adjustment layer
- batch psd processing
title: Jak používat Aspose.PSD k přidání invert adjustment layer v Java
url: /cs/java/advanced-image-manipulation/invert-adjustment-layer/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Jak použít Aspose.PSD k přidání vrstvy úpravy invertování v Javě

## Úvod

Pokud hledáte robustní **image processing java library**, Aspose.PSD pro Javu je jednou z nejvšestrannějších možností na trhu. V tomto tutoriálu uvidíte **jak použít Aspose** k vložení **Invert Adjustment Layer** do souboru PSD, jeho sloučení s dalšími úpravami a dokonce spuštění operace na desítky souborů. Ať už vytváříte nástroj pro dávkové zpracování, serverovou službu pro obrázky nebo editor pro jeden obrázek, níže uvedené kroky vás od zdrojového PSD až po plně editovatelný negativní obrázek během několika minut.

## Rychlé odpovědi
- **Co dělá vrstva úpravy Invert?** Obrací každou RGB hodnotu ve vybrané oblasti, čímž mění obrázek na fotografický negativ.  
- **Která knihovna tuto funkci poskytuje?** Aspose.PSD, přední **image processing java library**.  
- **Mohu ji sloučit s dalšími úpravami?** Ano – můžete **aplikovat více vrstev úprav** jako Jas/Kontrast, Odtón/Nasycení a další.  
- **Potřebuji licenci pro vývoj?** K dispozici je bezplatná zkušební verze; licence je vyžadována pro produkční použití.  
- **Jak dlouho trvá implementace?** Obvykle méně než 10 minut pro základní případ použití.

## Co je vrstva úpravy Invert?

Vrstva úpravy Invert je nedestruktivní úprava, která obrací barevné hodnoty každého pixelu, na který působí. Protože leží navrchu zásobníku vrstev, můžete přepínat její viditelnost nebo ji přeuspořádat, aniž byste trvale změnili původní data obrázku. Toto je nejrychlejší způsob, jak **vytvořit PSD soubory s negativním obrázkem** nebo dosáhnout klasického vzhledu filmového negativu.

## Proč použít Aspose.PSD jako vaši image processing java library?

Aspose.PSD podporuje **více než 200 funkcí PSD**, dokáže číst a zapisovat soubory Photoshopu bez nutnosti Photoshopu a zpracovává dokumenty s stovkami stránek s využitím méně než 500 MB haldy paměti. Běží na jakémkoli Java runtime (Java 6+), což z něj činí ideální nástroj pro **dávkové zpracování psd obrázků** na serverech Windows, Linux nebo macOS.

## Požadavky

Před začátkem se ujistěte, že máte:

1. **Aspose.PSD for Java** – stáhněte nejnovější JAR z oficiální stránky [Aspose.PSD for Java download page](https://releases.aspose.com/psd/java/).  
2. **Java Development Kit** – JDK 6.0 nebo novější nainstalovaný a nakonfigurovaný ve vašem `PATH`.  

Nyní jste připraveni psát kód.

## Import balíčků

Třída `PsdImage` představuje celý Photoshop dokument v paměti, zatímco třídy vrstev úprav sídlí v balíčku `com.aspose.psd.layers.adjustments`.

Třída `PsdImage` je nejvyšší objekt Aspose.PSD, který zapouzdřuje strukturu a pixelová data souboru PSD. Naimportujte jmenné prostory, pak budete moci načíst, upravit a uložit soubory PSD.

## Krok 1: nastavení adresáře dokumentu

Definujte složku, která obsahuje váš zdrojový soubor PSD a kam bude výstup uložen. Použití absolutních cest zabraňuje `NullPointerException`, když se změní pracovní adresář.

## Krok 2: načtení souboru PSD

Načtěte zdrojový soubor do objektu `PsdImage`. Tento objekt uchovává kompletní hierarchii vrstev v paměti, což umožňuje nedestruktivní úpravy.

Třída `PsdImage` poskytuje statickou metodu `load`, která načte hlavičku souboru, ověří formát a vytvoří v‑paměťovou reprezentaci připravenou k manipulaci.

## Krok 3: přidání vrstvy úpravy invert

Zavolejte vestavěnou metodu pro vložení vrstvy Invert Adjustment Layer na vrchol aktuálního zásobníku vrstev. Později můžete přidat další vrstvy (např. Jas, Odtón), abyste **aplikovali více vrstev úprav** v jednom pracovním postupu.

`addInvertAdjustmentLayer()` přidá Invert Adjustment Layer do kolekce vrstev PSD.

## Krok 4: uložení výstupu

Uložte upravený PSD na disk.  

`save()` zapíše soubor PSD, včetně všech vrstev a metadat, na zadanou cestu.

Ukládání používá stejnou metodu `save`, která zapisuje celý dokument, včetně všech vrstev úprav, masek a metadat, do požadovaného formátu.

### Co se právě stalo?

Soubor PSD byl načten do objektu `PsdImage`, byl vytvořen `InvertAdjustmentLayer` a připojen jako nejvyšší vrstva, a dokument byl uložen. Tento postup zachovává původní data obrázku a zároveň přidává nedestruktivní efekt invertování, který lze později přepínat nebo přeuspořádat.

Nyní jste úspěšně použili Aspose.PSD, **image processing java library**, k manipulaci se souborem PSD.

## Jak dávkově zpracovat PSD obrázky s invert úpravou?

Načtěte každý soubor uvnitř smyčky `for`, aplikujte stejné kroky a zavolejte `save` pro každou iteraci. Protože Aspose.PSD zpracovává soubory ve streamovacím režimu, můžete zvládnout **stovky PSD** při zachování využití paměti pod 300 MB opětovným použitím stejné instance `PsdImage`.

## Jak převést PSD na negativní obrázek?

Přidejte vrstvu Invert Adjustment Layer jako nejvyšší položku a uložte dokument – tato operace je ekvivalentní **convert PSD to negative**. Později můžete vrstvu zakázat nebo smazat, abyste se vrátili k původnímu vzhledu bez nutnosti znovu načíst zdrojový soubor.

## Časté problémy a tipy

| Issue | Cause | Solution |
|-------|-------|----------|
| **NullPointerException při `Image.load`** | Nesprávná cesta k souboru nebo chybějící soubor | Ověřte `dataDir` a název souboru; použijte absolutní cesty pro testování |
| **Pořadí vrstev není podle očekávání** | Přidávání vrstev po existujících mění pořadí vrstvení | Vložte vrstvu invert před ostatní úpravy, nebo přeuspořádejte pomocí `psdImage.getLayers().move()` |
| **Zpomalení výkonu u velkých PSD** | Načítání velmi velkých souborů do paměti | Zvyšte JVM haldu (`-Xmx2g`) nebo zpracovávejte soubory po částech pomocí `psdImage.getPages().get(0).getResources().setMemoryOptimized(true)` |

## Často kladené otázky

**Q: Je Aspose.PSD kompatibilní se všemi verzemi Javy?**  
A: Ano, podporuje Java 6.0 a novější, včetně Java 8, 11 a 17.

**Q: Mohu aplikovat více vrstev úprav v jedné operaci?**  
A: Rozhodně. Po přidání vrstvy invert můžete zavolat `addBrightnessAdjustmentLayer()`, `addHueSaturationAdjustmentLayer()` atd., abyste vrstvy sloučili.

**Q: Kde najdu kompletní referenci API?**  
A: Kompletní dokumentace je k dispozici [Aspose.PSD Java API reference](https://reference.aspose.com/psd/java/).

**Q: Existuje bezplatná zkušební verze pro Aspose.PSD?**  
A: Ano, můžete stáhnout zkušební verzi [Aspose.PSD trial download](https://releases.aspose.com/).

**Q: Jak získám dočasnou licenci pro testování?**  
A: Požádejte o dočasnou licenci [temporary license request page](https://purchase.aspose.com/temporary-license/).

**Poslední aktualizace:** 2026-11-04  
**Testováno s:** Aspose.PSD 24.12 for Java  
**Autor:** Aspose  









```java
import com.aspose.psd.Image;

import com.aspose.psd.fileformats.psd.PsdImage;
```

```java
String dataDir = "Your Document Directory";
```

```java
String filePath = dataDir + "InvertStripes_before.psd";
String outputPath = dataDir + "InvertStripes_after.psd";

PsdImage im = (PsdImage)Image.load(filePath);
```

```java
im.addInvertAdjustmentLayer();
```

```java
im.save(outputPath);
```

## Související tutoriály

- [Přidat vrstvu úpravy úrovně do souborů PSD pomocí Aspose.PSD pro Java](/psd/java/modifying-converting-psd-images/add-level-adjustment-layer-psd/)
- [Jak přidat vrstvu úpravy – Channel Mixer v PSD (Java)](/psd/java/modifying-converting-psd-images/add-channel-mixer-adjustment-layer-psd/)
- [Jak upravit PSD – Přidat vrstvu úpravy křivek pomocí Java](/psd/java/modifying-converting-psd-images/add-curves-adjustment-layer-psd/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}