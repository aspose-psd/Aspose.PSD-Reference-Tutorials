---
date: 2026-01-01
description: Naučte se, jak vytvářet PSD obrázky v Javě pomocí Aspose.PSD. Tento průvodce
  ukazuje, jak nastavit cestu a v Javě vytvořit Photoshop dokument pomocí kódu krok
  za krokem.
linktitle: Create Image by Setting Path
second_title: Aspose.PSD Java API
title: Jak vytvořit PSD – Vytvořit obrázek nastavením cesty v Aspose.PSD pro Javu
url: /cs/java/image-editing/create-image-by-setting-path/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Jak vytvořit PSD – Vytvořit obrázek nastavením cesty v Aspose.PSD pro Java

## Introduction

Vítejte v tomto krok‑za‑krokem tutoriálu o **jak vytvořit PSD** obrázky pomocí Aspose.PSD pro Java. Provedeme vás nastavením cesty k souboru, konfigurací možností a programovým generováním dokumentu Photoshopu. Na konci pochopíte, jak **java create photoshop document** soubory, které lze dále upravovat nebo integrovat do vašich aplikací.

## Quick Answers
- **Co dělá Aspose.PSD?** Poskytuje čisté Java API pro čtení, úpravu a vytváření souborů Photoshop (PSD) bez nutnosti mít nainstalovaný Photoshop.  
- **Mohu nastavit vlastní výstupní cestu?** Ano – použijte `FileCreateSource` k určení přesného umístění a názvu souboru.  
- **Jaké kompresní metody jsou podporovány?** RLE, ZIP a RAW; tento příklad používá RLE pro bezztrátovou kompresi.  
- **Potřebuji licenci pro vývoj?** Bezplatná zkušební verze funguje pro testování; pro produkci je vyžadována komerční licence.  
- **Jaké verze Javy jsou podporovány?** Aspose.PSD funguje s Java 8 a novějšími.

## What is “how to create PSD”?

Vytvoření souboru PSD znamená generování obrázku kompatibilního s Photoshopem, který zachovává vrstvy, kanály a další specifická data Photoshopu. Aspose.PSD abstrahuje složitý formát souboru, což vám umožňuje soustředit se na vaši obchodní logiku.

## Why use Java to **java create photoshop document**?

- **Cross‑platform** – Java běží kdekoliv, takže vaše generování PSD funguje na Windows, Linuxu i macOS.  
- **Bez závislosti na Photoshopu** – Generujte nebo upravujte soubory PSD bez instalace Adobe Photoshop.  
- **Plná kontrola** – Nastavte kompresi, barevný režim, rozměry a další prostřednictvím čistého objektového modelu.

## Prerequisites

Než se pustíme dál, ujistěte se, že máte:

- Základní znalosti programování v Javě.  
- Nainstalovanou knihovnu Aspose.PSD pro Java. Můžete si ji stáhnout [zde](https://releases.aspose.com/psd/java/).

## Import Packages

Začněte importováním potřebných balíčků do vašeho Java projektu:

```java
import com.aspose.psd.Image;

import com.aspose.psd.fileformats.psd.CompressionMethod;
import com.aspose.psd.imageoptions.PsdOptions;
import com.aspose.psd.sources.FileCreateSource;
```

## Step 1: How to Set Path for Document Directory

Nastavte cestu k adresáři dokumentu, kde bude obrázek vytvořen.

```java
String dataDir = "Your Document Directory";
```

## Step 2: Define Output File Name

Definujte název výstupního souboru, včetně adresáře dokumentu.

```java
String desName = dataDir + "CreatingAnImageBySettingPath_out.psd";
```

## Step 3: Configure PsdOptions

Vytvořte instanci `PsdOptions` a nakonfigurujte její vlastnosti, například kompresní metodu.

```java
PsdOptions psdOptions = new PsdOptions();
psdOptions.setCompressionMethod(CompressionMethod.RLE);
```

## Step 4: Set Source Property

Definujte vlastnost source pro instanci `PsdOptions`, specifikujte výstupní soubor a zda je dočasný.

```java
psdOptions.setSource(new FileCreateSource(desName, false));
```

## Step 5: Create Image

Vytvořte instanci `Image` a zavolejte metodu `create` předáním objektu `PsdOptions` a rozměrů obrázku.

```java
Image image = Image.create(psdOptions, 500, 500);
```

## Step 6: Save the Image

Uložte vytvořený obrázek.

```java
image.save();
```

Opakujte tyto kroky a úspěšně jste vytvořili obrázek pomocí Aspose.PSD pro Java nastavením cesty.

## Common Issues & Tips

- **Neplatný adresář** – Ujistěte se, že `dataDir` končí správným oddělovačem souborů (`/` nebo `\\`).  
- **Chyby oprávnění** – Spusťte aplikaci s právy zápisu do cílové složky.  
- **Licence není nastavena** – Pokud obdržíte výjimku licence, načtěte svou licenci Aspose.PSD před vytvořením obrázku.

## Conclusion

V tomto tutoriálu jsme pokryli **jak vytvořit PSD** soubory pomocí Aspose.PSD pro Java, ukázali **jak nastavit cestu** a představili kompletní postup pro generování dokumentu Photoshopu. Tento přístup umožňuje vývojářům Javy vložit tvorbu PSD přímo do jejich pracovních postupů, ať už pro automatizované reportování, dynamickou grafiku nebo dávkové zpracování.

## FAQ's

### Q1: Je Aspose.PSD kompatibilní s různými Java IDEs?

A1: Ano, Aspose.PSD funguje bez problémů s různými integrovanými vývojovými prostředími (IDE) pro Javu.

### Q2: Mohu používat Aspose.PSD pro komerční projekty?

A2: Ano, můžete používat Aspose.PSD jak pro osobní, tak pro komerční projekty. Podrobnosti o licencování najdete na [stránce nákupu](https://purchase.aspose.com/buy).

### Q3: Jak mohu získat podporu pro Aspose.PSD?

A3: Navštivte [forum Aspose.PSD](https://forum.aspose.com/c/psd/34) pro podporu komunity a diskuze.

### Q4: Je k dispozici bezplatná zkušební verze?

A4: Ano, bezplatnou zkušební verzi můžete získat [zde](https://releases.aspose.com/).

### Q5: Potřebuji dočasnou licenci pro testování?

A5: Dočasnou licenci pro testovací účely můžete získat [zde](https://purchase.aspose.com/temporary-license/).

**Additional Q&A**

**Q: Mohu změnit rozměry obrázku po vytvoření?**  
**A: Ano, můžete změnit velikost obrázku pomocí `image.resize(width, height)` před uložením.**

**Q: Jaké barevné režimy jsou podporovány?**  
**A: Aspose.PSD podporuje režimy RGB, CMYK, Grayscale a Indexed.**

---

**Last Updated:** 2026-01-01  
**Tested With:** Aspose.PSD for Java 24.11  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}