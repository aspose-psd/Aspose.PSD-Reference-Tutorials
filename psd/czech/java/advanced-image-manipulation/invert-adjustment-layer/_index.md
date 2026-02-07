---
date: 2026-02-07
description: Naučte se, jak používat knihovnu Aspose.PSD pro zpracování obrázků v
  Javě k aplikaci více úpravných vrstev, včetně vrstvy invertování, pro plynulou manipulaci
  s PSD.
linktitle: Invert Adjustment Layer
second_title: Aspose.PSD Java API
title: 'Knihovna Java pro zpracování obrazu: Inverze vrstvy pomocí Aspose.PSD'
url: /cs/java/advanced-image-manipulation/invert-adjustment-layer/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Invert Adjustment Layer v Aspose.PSD pro Java

## Introduction

Pokud hledáte robustní **image processing java library**, Aspose.PSD pro Java je jednou z nejobtížnějších možností na trhu. V tomto tutoriálu vás provedeme, jak přidat **Invert Adjustment Layer** do souboru PSD, techniku, kterou můžete kombinovat s dalšími úpravovými vrstvami pro dosažení sofistikovaných vizuálních efektů. Ať už vytváříte nástroj pro dávkové zpracování nebo editor jedné obrázku, tento průvodce vám poskytne jasnou, krok‑za‑krokem cestu k rychlému dokončení úkolu.

## Quick Answers
- **Co dělá Invert Adjustment Layer?** Obrací všechny hodnoty barev ve vybrané oblasti, čímž vytváří efekt negativního obrazu.  
- **Která knihovna poskytuje tuto funkci?** Aspose.PSD, přední **image processing java library**.  
- **Mohu ji kombinovat s dalšími úpravami?** Ano – můžete **apply multiple adjustment layers** jako Brightness/Contrast, Hue/Saturation a další.  
- **Potřebuji licenci pro vývoj?** K dispozici je bezplatná zkušební verze; licence je vyžadována pro produkční použití.  
- **Jak dlouho trvá implementace?** Obvykle méně než 10 minut pro základní případ použití.

## What is the Invert Adjustment Layer?

Invert Adjustment Layer je nedestruktivní úprava, která převrací RGB hodnoty každého pixelu, na který má vliv. Protože leží navrchu zásobníku vrstev, můžete přepínat její viditelnost nebo měnit pořadí bez trvalé změny původních dat obrázku.

## How to invert layer using Aspose.PSD

Níže uvidíte přesně, **jak invertovat vrstvu** v souboru PSD. Kroky jsou záměrně jednoduché, aby se můžete soustředit na koncept místo boilerplate kódu.

## Why Use Aspose.PSD as Your Image Processing Java Library?

- **Full PSD support** – čtení, úprava a zápis souborů Photoshopu bez nutnosti instalace Photoshopu.  
- **Cross‑platform** – funguje na jakémkoli Java runtime (Java 6+).  
- **Rich adjustment features** – obsahuje vestavěné metody pro mnoho běžných úprav, což usnadňuje **apply multiple adjustment layers** v jednom pracovním postupu.  
- **Performance‑optimized** – efektivně zpracovává velké soubory, což je nezbytné pro dávkové zpracování.

## Prerequisites

Předtím, než začnete, ujistěte se, že máte následující:

1. **Aspose.PSD Library** – stáhněte ji z oficiálního webu [here](https://releases.aspose.com/psd/java/).  
2. **Java Development Environment** – nainstalovaný a nakonfigurovaný JDK 6.0 nebo novější.  

Nyní se ponořme do kódu.

## Import Packages

Začněte importováním potřebných tříd. Tyto importy vám poskytují přístup k základním API pro manipulaci s obrázky a specifické funkčnosti pro PSD.

```java
import com.aspose.psd.Image;

import com.aspose.psd.fileformats.psd.PsdImage;
```

## Step 1: Set Up Document Directory

Definujte složku, která obsahuje váš zdrojový soubor PSD a kam bude výstup uložen.

```java
String dataDir = "Your Document Directory";
```

## Step 2: Load PSD File

Načtěte zdrojový soubor do objektu `PsdImage`. Tento objekt představuje celý dokument PSD v paměti.

```java
String filePath = dataDir + "InvertStripes_before.psd";
String outputPath = dataDir + "InvertStripes_after.psd";

PsdImage im = (PsdImage)Image.load(filePath);
```

## Step 3: Add Invert Adjustment Layer

Zavolejte vestavěnou metodu pro vložení Invert Adjustment Layer na vrchol aktuálního zásobníku vrstev. Později můžete přidat další vrstvy (např. Brightness, Hue), abyste **apply multiple adjustment layers**.

```java
im.addInvertAdjustmentLayer();
```

## Step 4: Save the Output

Uložte upravený PSD na disk. Uložený soubor nyní obsahuje Invert Adjustment Layer a může být otevřen v Photoshopu nebo jakémkoli prohlížeči kompatibilním s PSD.

```java
im.save(outputPath);
```

### What just happened?

- PSD byl načten do paměti.  
- Invert Adjustment Layer byl přidán jako vrchní vrstva.  
- Obrázek byl uložen, zachovávající nedestruktivní úpravu.

Úspěšně jste použili Aspose.PSD, **image processing java library**, k manipulaci se souborem PSD.

## Common Issues & Tips

| Issue | Cause | Solution |
|-------|-------|----------|
| **NullPointerException on `Image.load`** | Nesprávná cesta k souboru nebo chybějící soubor | Ověřte `dataDir` a název souboru; pro testování použijte absolutní cesty |
| **Layer order not as expected** | Přidávání vrstev po existujících mění pořadí | Použijte `im.addInvertAdjustmentLayer()` před přidáním dalších úprav, nebo přeuspořádejte vrstvy pomocí `im.getLayers()` |
| **Performance slowdown on large PSDs** | Načítání velmi velkých souborů do paměti | Zvažte zpracování stránek po částech nebo zvýšení velikosti haldy JVM (`-Xmx2g`) |

## Frequently Asked Questions

**Q: Je Aspose.PSD kompatibilní se všemi verzemi Java?**  
A: Aspose.PSD podporuje Java 6.0 a novější verze.

**Q: Mohu aplikovat více úpravných vrstev v jedné operaci?**  
A: Ano, můžete vrstvit několik úpravných vrstev – jako Invert, Brightness a Hue/Saturation – pro dosažení komplexních efektů.

**Q: Kde najdu další dokumentaci k Aspose.PSD?**  
A: Viz dokumentaci [here](https://reference.aspose.com/psd/java/) pro komplexní průvodce a API reference.

**Q: Je k dispozici bezplatná zkušební verze Aspose.PSD?**  
A: Ano, můžete si prohlédnout bezplatnou zkušební verzi [here](https://releases.aspose.com/).

**Q: Jak mohu získat dočasnou licenci pro Aspose.PSD?**  
A: Dočasnou licenci můžete získat [here](https://purchase.aspose.com/temporary-license/).

---

**Last Updated:** 2026-02-07  
**Tested With:** Aspose.PSD 24.12 for Java  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}