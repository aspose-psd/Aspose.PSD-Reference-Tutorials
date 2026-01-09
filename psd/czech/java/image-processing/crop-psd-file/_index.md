---
date: 2026-01-09
description: Naučte se, jak převést PSD na PNG a oříznout soubory PSD v Javě pomocí
  Aspose.PSD. Přesná manipulace s obrázky je snadná.
linktitle: Crop PSD File
second_title: Aspose.PSD Java API
title: Převod PSD na PNG a oříznutí pomocí Aspose.PSD pro Javu
url: /cs/java/image-processing/crop-psd-file/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Převod PSD na PNG a oříznutí souboru PSD pomocí Aspose.PSD pro Java

## Úvod

Pokud potřebujete **převést PSD na PNG** a zároveň oříznout obrázek na přesnou oblast, která vás zajímá, Aspose.PSD pro Java nabízí čistý programový způsob, jak to provést. V tomto tutoriálu projdeme celý proces – od nastavení projektu až po uložení oříznutého PSD a exportu PNG – abyste mohli integrovat přesnou manipulaci s obrázky do jakékoli Java aplikace.

## Rychlé odpovědi
- **Umí Aspose.PSD převést PSD na PNG?** Ano, podporuje přímý převod s plnou věrností vrstev.  
- **Potřebuji licenci pro oříznutí?** Bezplatná zkušební verze funguje pro vývoj; licence je vyžadována pro produkci.  
- **Jaká verze Javy je požadována?** Doporučuje se Java 8 nebo vyšší.  
- **Zachová PNG průhlednost?** Ano, pomocí `PngColorType.TruecolorWithAlpha`.  
- **Je operace rychlá u velkých souborů?** Aspose.PSD je optimalizováno pro výkon u vysokých rozlišení PSD.

## Co je „převod PSD na PNG“ a proč ho oříznout?

Převod Photoshop dokumentu (PSD) na PNG je běžný krok, když potřebujete web‑připravený obrázek nebo lehčí verzi návrhu. Oříznutí vám umožní vyjmout jen tu část plátna, kterou potřebujete, čímž se sníží velikost souboru a zaměří se na relevantní obsah. Kombinace obou akcí v jednom workflow šetří čas a udržuje kód jednoduchý.

## Předpoklady

Než se pustíme dál, ujistěte se, že máte:

- **Vývojové prostředí Java** – nainstalovaný a nakonfigurovaný JDK 8+.  
- **Aspose.PSD pro Java** – stáhněte knihovnu a přidejte ji do svého projektu. Knihovnu a dokumentaci najdete [zde](https://reference.aspose.com/psd/java/).  
- **Ukázkový soubor PSD** – soubor PSD umístěný ve vašem projektovém adresáři, který chcete oříznout a převést.

## Import balíčků

Ve vašem Java projektu začněte importováním potřebných balíčků pro využití funkcí Aspose.PSD. Přidejte následující importy:

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;
import com.aspose.psd.Rectangle;

import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.imageoptions.PngOptions;
import com.aspose.psd.imageoptions.PsdOptions;
import com.aspose.psd.xmp.types.complex.colorant.ColorType;
```

## Krok 1: Nastavení adresáře dokumentu

```java
String dataDir = "Your Document Directory";
```

Nahraďte `"Your Document Directory"` skutečnou cestou, kde se váš soubor PSD nachází.

## Krok 2: Načtení souboru PSD

```java
String sourceFileName = dataDir + "1.psd";
RasterImage image = (RasterImage)Image.load(sourceFileName);
```

Načtěte soubor PSD, který chcete oříznout, do objektu `RasterImage`.

## Krok 3: Definování oblasti ořezu

```java
image.crop(new Rectangle(10, 30, 100, 100));
```

Určete oblast, kterou chcete oříznout, pomocí třídy `Rectangle` a zadejte hodnoty **x**, **y**, **width** a **height**.

## Krok 4: Uložení oříznutého PSD

```java
String exportPathPsd = dataDir + "CropTest.psd";
image.save(exportPathPsd, new PsdOptions());
```

Uložte oříznutý obrázek zpět do formátu PSD pomocí zadané cesty.

## Krok 5: Uložení oříznutého obrázku jako PNG

```java
String exportPathPng = dataDir + "CropTest.png";
PngOptions options = new PngOptions();
options.setColorType(PngColorType.TruecolorWithAlpha);
image.save(exportPathPng, options);
```

Navíc exportujte oříznutý obrázek jako soubor PNG s zachovanou průhledností.

## Proč použít Aspose.PSD pro Java k oříznutí souborů PSD?

- **Plná věrnost PSD** – Všechny vrstvy, masky a efekty zůstávají během převodu nedotčeny.  
- **Není potřeba nativní Photoshop** – Funguje kompletně na serverové straně.  
- **Vysoký výkon** – Optimalizováno pro velké soubory a dávkové zpracování.  
- **Jednoduché API** – Několik řádků kódu stačí k provedení ořezu a převodu.

## Časté problémy a řešení

| Problém | Řešení |
|---------|--------|
| **Soubor nenalezen** | Ověřte, že `dataDir` končí oddělovačem cesty (`/` nebo `\\`). |
| **Ztráta průhledného pozadí** | Ujistěte se, že je nastaveno `PngOptions.setColorType(PngColorType.TruecolorWithAlpha)`. |
| **Nedostatek paměti pro obrovské PSD** | Zpracovávejte obrázek po částech nebo zvýšte haldu JVM (`-Xmx`). |
| **Výjimka licence** | Aplikujte svou Aspose licenci před načtením obrázku (`License license = new License(); license.setLicense("Aspose.PSD.lic");`). |

## Často kladené otázky

**Q: Můžu pomocí Aspose.PSD pro Java ořezávat obrázky i v jiných formátech?**  
A: I když je hlavní zaměření na PSD, knihovna také podporuje PNG, JPEG, BMP a další rastrové formáty.

**Q: Je Aspose.PSD vhodné pro zpracování velkého množství obrázků?**  
A: Ano, je optimalizováno pro výkon a dokáže efektivně zvládnout dávkové operace.

**Q: Jaké jsou licenční podmínky pro produkční použití?**  
A: Ano, podívejte se na [stránku nákupu Aspose.PSD pro Java](https://purchase.aspose.com/buy) pro podrobnosti.

**Q: Kde mohu získat komunitní podporu?**  
A: Navštivte [forum Aspose.PSD pro Java](https://forum.aspose.com/c/psd/34) a získejte pomoc od ostatních vývojářů.

**Q: Můžu knihovnu vyzkoušet před zakoupením?**  
A: Rozhodně – stáhněte si bezplatnou zkušební verzi [zde](https://releases.aspose.com/).

## Závěr

Nyní máte kompletní, end‑to‑end řešení pro **převod PSD na PNG** při ořezu obrázku na přesnou oblast, kterou potřebujete. Vložte tyto úryvky do svých Java projektů a automatizujte manipulaci s obrázky ve stylu Photoshopu bez nutnosti samotného Photoshopu.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Poslední aktualizace:** 2026-01-09  
**Testováno s:** Aspose.PSD 24.11 pro Java  
**Autor:** Aspose  

---