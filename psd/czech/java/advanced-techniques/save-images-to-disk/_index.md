---
date: 2025-12-25
description: Jednoduše uložte PSD jako PNG na disk pomocí Aspose.PSD pro Javu, výkonné
  Java knihovny pro manipulaci se soubory PSD.
linktitle: Save Images to Disk
second_title: Aspose.PSD Java API
title: Uložte PSD jako PNG pomocí Aspose.PSD pro Javu
url: /cs/java/advanced-techniques/save-images-to-disk/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Uložte PSD jako PNG pomocí Aspose.PSD pro Java

## Úvod

Uložení souboru PSD jako PNG obrázku je běžný krok v jakémkoli **java image processing tutorial**. S **Aspose.PSD for Java** můžete **convert PSD to PNG** během několika řádků kódu, což usnadňuje začlenění této funkce do vašich aplikací. V tomto průvodci projdeme celý pracovní postup – od nastavení prostředí po zápis PNG souboru na disk – abyste rychle získali odpověď na otázku **how to save image** data from a PSD.

## Rychlé odpovědi
- **What does “save psd as png” mean?** Znamená to převod souboru Photoshop PSD do přenosného PNG bitmapu.
- **Which library handles the conversion?** Aspose.PSD for Java poskytuje jednoduché API pro tento úkol.
- **Do I need a license?** Bezplatná zkušební verze funguje pro vývoj; pro produkci je vyžadována komerční licence.
- **Can I write other formats?** Ano, knihovna také podporuje JPEG, BMP, TIFF a další.
- **How long does the conversion take?** Obvykle méně než sekunda pro standardně velké PSD soubory.

## Co je “save psd as png”?

Tento výraz odkazuje na extrakci rastrových obrazových dat vložených do dokumentu Photoshop (PSD) a jejich uložení ve formátu PNG, který zachovává průhlednost a nabízí bezztrátovou kompresi. To je zvláště užitečné, když potřebujete web‑připravená aktiva nebo miniatury vytvořené z vrstvených návrhů.

## Proč konvertovat PSD na PNG pomocí Aspose.PSD for Java?

- **Plná věrnost:** Všechny vrstvy, kanály a průhlednost jsou zachovány.
- **Není vyžadován nativní Photoshop:** Funguje na jakékoli platformě s Java runtime.
- **Dávkové zpracování:** Jednoduše iterujte přes více souborů stejným kódem.
- **Výkon:** Optimalizovaný nativní kód zajišťuje rychlou konverzi i pro velké PSD soubory.

## Požadavky

Než se ponoříte do tutoriálu, ujistěte se, že máte následující požadavky připravené:

- Aspose.PSD for Java Library: Stáhněte a nainstalujte knihovnu ze [release page](https://releases.aspose.com/psd/java/).
- Java Development Environment: Ujistěte se, že máte na svém počítači funkční vývojové prostředí Java.

## Import balíčků

Jakmile máte požadavky připravené, je čas importovat potřebné balíčky do vašeho Java projektu. Přidejte následující řádky do svého kódu:

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.PngOptions;
```

### Krok 1: Definujte adresář dokumentů

Nastavte cestu k adresáři dokumentů, kde se nachází váš PSD soubor:

```java
String dataDir = "Your Document Directory";
```

### Krok 2: Zadejte cesty ke zdroji a cíli

Definujte cesty k vašemu zdrojovému PSD souboru a cílovému souboru, kam bude obrázek uložen:

```java
String sourceFile = dataDir + "sample.psd";
String destName = dataDir + "result.png";
```

### Krok 3: Načtěte PSD obrázek

Načtěte PSD obrázek pomocí Aspose.PSD:

```java
Image image = Image.load(sourceFile);
```

### Krok 4: Uložte obrázek s volbami

Přetypujte načtený obrázek na `PsdImage` a uložte jej jako PNG soubor:

```java
PsdImage psdImage = (PsdImage)image;
psdImage.save(destName, new PngOptions());
```

Opakujte tyto kroky pro každý obrázek, který chcete uložit, a zajistěte tak plynulý proces s Aspose.PSD.

## Časté problémy a řešení

| Issue | Reason | Fix |
|-------|--------|-----|
| **Soubor nenalezen** | Nesprávná cesta `dataDir` | Ověřte, že řetězec adresáře končí lomítkem (`/` nebo `\`) a že soubor existuje. |
| **OutOfMemoryError** | Velmi velké PSD soubory | Zvyšte velikost haldy JVM (`-Xmx2g`) nebo zpracovávejte soubor po částech, pokud jsou potřeba jen konkrétní vrstvy. |
| **Prázdný PNG výstup** | Chybí konfigurace `PngOptions` | Použijte výchozí možnosti, jak je ukázáno; přizpůsobte je, pokud potřebujete konkrétní DPI nebo kompresi. |

## Často kladené otázky

### Q1: Mohu používat Aspose.PSD for Java s jinými formáty obrázků?

A1: Ano, Aspose.PSD for Java podporuje různé formáty obrázků, včetně JPEG, BMP, TIFF a dalších.

### Q2: Je k dispozici bezplatná zkušební verze Aspose.PSD for Java?

A2: Ano, můžete vyzkoušet bezplatnou verzi Aspose.PSD for Java na [this link](https://releases.aspose.com/).

### Q3: Kde najdu komplexní dokumentaci k Aspose.PSD for Java?

A3: Odkazujte se na [documentation](https://reference.aspose.com/psd/java/) pro podrobné informace o Aspose.PSD for Java.

### Q4: Jak mohu získat podporu pro Aspose.PSD for Java?

A4: Navštivte [Aspose.PSD forum](https://forum.aspose.com/c/psd/34) pro komunitní podporu a diskuze.

### Q5: Jsou k dispozici dočasné licence pro Aspose.PSD for Java?

A5: Ano, můžete získat dočasnou licenci [here](https://purchase.aspose.com/temporary-license/).

---

**Poslední aktualizace:** 2025-12-25  
**Testováno s:** Aspose.PSD 24.12 for Java  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}