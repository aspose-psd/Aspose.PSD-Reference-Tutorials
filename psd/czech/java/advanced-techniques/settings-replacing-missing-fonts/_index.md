---
date: 2025-12-25
description: Naučte se, jak nahradit písma v souborech PSD pomocí Aspose.PSD pro Javu
  – podrobný návod, který také ukazuje, jak uložit PSD jako PNG a jak řešit chybějící
  písma.
linktitle: Settings for Replacing Missing Fonts
second_title: Aspose.PSD Java API
title: Jak nahradit písma v Aspose.PSD pro Javu
url: /cs/java/advanced-techniques/settings-replacing-missing-fonts/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Jak nahradit písma v Aspose.PSD pro Java

## Úvod

Pokud pracujete se soubory Photoshop (PSD) v Java aplikaci, chybějící písma mohou narušit vizuální rozvržení a způsobit chyby při vykreslování. **Jak nahradit písma** rychle a spolehlivě je nezbytné pro zachování věrnosti designu. V tomto tutoriálu se naučíte, jak pomocí Aspose.PSD pro Java nahradit chybějící písma, převést výsledek do PNG a udržet váš workflow konverze obrázků plynulý. Na konci budete schopni nahradit písma v obrázcích, uložit PSD jako PNG a vyhnout se běžným úskalím, se kterými se vývojáři setkávají.

## Rychlé odpovědi
- **Co znamená „replace fonts“ při zpracování PSD?** Nahrazuje chybějící nebo nedostupné typy písma náhradním fontem, který určíte.  
- **Která knihovna to provádí automaticky?** Aspose.PSD for Java poskytuje `PsdLoadOptions.setDefaultReplacementFont`.  
- **Mohu také po nahrazení převést PSD na PNG?** Ano – použijte `PngOptions` a zavolejte `psdImage.save`.  
- **Potřebuji licenci pro produkční použití?** Platná licence Aspose.PSD je vyžadována pro ne‑evaluační sestavení.  
- **Jaká verze Javy je podporována?** Jakékoli prostředí Java 8+ funguje s aktuálním vydáním Aspose.PSD.

## Co je nahrazení písma v souborech PSD?

Když PSD odkazuje na písmo, které není nainstalováno na hostitelském počítači, vykreslovací engine přejde na generické písmo, což často vede k nesprávně zarovnanému textu. Nahrazení písma vám umožní definovat výchozí písmo (např. Arial), které knihovna použije vždy, když narazí na chybějící typ písma, a zajistí tak konzistentní vizuální výstup.

## Proč nahrazovat chybějící písma pomocí Aspose.PSD?

- **Řešení bez závislostí** – Není potřeba nativní Photoshop ani externí nástroje.  
- **Připraveno pro dávkové zpracování** – Zpracujte desítky souborů ve smyčce se stejným nastavením.  
- **Připraveno pro konverzi obrázků** – Po nahrazení můžete přímo **uložit PSD jako PNG** nebo **převést PSD na PNG** bez dalších kroků.  
- **Cross‑platform** – Funguje na Java runtime Windows, Linux a macOS.

## Požadavky

1. **Aspose.PSD Library** – Stáhněte a nainstalujte knihovnu Aspose.PSD pro Java ze [stránky vydání](https://releases.aspose.com/psd/java/).  
2. **Java Development Environment** – Nainstalovaný a nakonfigurovaný JDK 8 nebo novější.  

Nyní, když máme základy, ponořme se do kódu.

## Import balíčků

Začněte importováním potřebných tříd Aspose.PSD. To vám poskytne přístup k načítání obrázků, možnostem nahrazení písma a funkcím exportu PNG.

```java
import com.aspose.psd.Image;

import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
import com.aspose.psd.imageoptions.PngOptions;
```

## Krok 1: Nastavte adresář dokumentů

Definujte složku, která obsahuje zdrojový PSD a kam bude uložen výsledný PNG.

```java
String dataDir = "Your Document Directory";
```

## Krok 2: Zadejte vstupní a výstupní soubory

Uveďte úplné cesty pro vstupní PSD a výstupní PNG. To činí workflow přehledným a usnadňuje údržbu kódu.

```java
String sourceFile = dataDir + "sample.psd";
String destName = dataDir + "result.png";
```

## Krok 3: Nakonfigurujte nastavení nahrazení písma

Vytvořte instanci `PsdLoadOptions` a řekněte Aspose.PSD, které písmo použít, když narazí na chybějící. V tomto příkladu používáme **Arial**, ale můžete jej nahradit libovolným písmem nainstalovaným ve vašem systému.

```java
PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setDefaultReplacementFont("Arial");
```

## Krok 4: Načtěte PSD obrázek a nahraďte písma

Načtěte PSD pomocí výše definovaných možností. Knihovna automaticky vymění všechna chybějící písma za výchozí, které jste specifikovali.

```java
Image image = Image.load(sourceFile, loadOptions);
PsdImage psdImage = (PsdImage) image;
```

## Krok 5: Uložte upravený obrázek

Nakonfigurujte možnosti exportu PNG – true color s alfa kanálem – pro zachování průhlednosti. Tento krok také demonstruje **image conversion PSD to PNG** po nahrazení písma.

```java
PngOptions options = new PngOptions();
options.setColorType(PngColorType.TruecolorWithAlpha);
psdImage.save(destName, options);
```

### Co se právě stalo?

- PSD byl otevřen s náhradním fontem (Arial).  
- Všechny textové vrstvy, které původně odkazovaly na chybějící písma, jsou nyní vykresleny pomocí Arial.  
- Výsledný obrázek byl uložen jako PNG, což efektivně **uloží PSD jako PNG** při zachování vizuální věrnosti.

## Časté problémy a řešení

| Problém | Příčina | Řešení |
|-------|-------|----------|
| Text stále vypadá špatně | Metriky písma se liší (velikost, tloušťka) | Upravte velikost náhradního písma programově nebo vyberte písmo s podobnými metrikami. |
| PNG je větší, než se očekávalo | Výchozí nastavení PNG používá 32‑bitovou barvu | Přepněte `PngColorType` na `Truecolor`, pokud není potřeba alfa kanál. |
| Výjimka licence | Spuštěno bez platné licence | Aplikujte dočasnou nebo trvalou licenci Aspose.PSD před načtením obrázku. |

## Často kladené otázky

**Q: Je Aspose.PSD kompatibilní se všemi verzemi souborů PSD?**  
A: Aspose.PSD podporuje širokou škálu verzí PSD, od raných vydání Photoshopu až po nejnovější funkce.

**Q: Mohu v Aspose.PSD použít vlastní písma pro nahrazení?**  
A: Ano, stačí předat název vlastního písma metodě `setDefaultReplacementFont`. Ujistěte se, že je písmo přístupné JVM.

**Q: Existují licenční možnosti pro Aspose.PSD?**  
A: Prozkoumejte licenční možnosti [zde](https://purchase.aspose.com/buy), abyste si vybrali nejlepší plán pro vaše potřeby.

**Q: Je k dispozici komunitní fórum pro podporu Aspose.PSD?**  
A: Ano, navštivte [Aspose.PSD fórum](https://forum.aspose.com/c/psd/34) pro komunitní podporu a diskuze.

**Q: Jak získat dočasnou licenci pro Aspose.PSD?**  
A: Získejte dočasnou licenci [zde](https://purchase.aspose.com/temporary-license/) pro testovací a evaluační účely.

---

**Poslední aktualizace:** 2025-12-25  
**Testováno s:** Aspose.PSD 24.11 for Java (nejnovější v době psaní)  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}