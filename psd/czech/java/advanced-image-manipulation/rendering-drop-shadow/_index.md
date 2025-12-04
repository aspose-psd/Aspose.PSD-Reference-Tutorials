---
date: 2025-12-04
description: Naučte se, jak uložit PSD jako PNG a použít vykreslování vrženého stínu
  pomocí Aspose.PSD pro Java. Tento průvodce popisuje, jak přidat stín, převést PSD
  na PNG a aplikovat vržený stín v Javě.
language: cs
linktitle: Apply Rendering Drop Shadow
second_title: Aspose.PSD Java API
title: Uložte PSD jako PNG a přidejte vržený stín s Aspose.PSD Java
url: /java/advanced-image-manipulation/rendering-drop-shadow/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Uložte PSD jako PNG a přidejte vržený stín pomocí Aspose.PSD Java

## Úvod

Pokud pracujete se soubory Photoshopu v Javě, **uložení PSD jako PNG** a přidání profesionálně vypadajícího vrženého stínu je běžný požadavek. Aspose.PSD tuto úlohu zjednodušuje a umožňuje vám **převést PSD na PNG** a **aplikovat vržený stín v Javě** během několika řádků kódu. V tomto tutoriálu vás provedeme celým procesem, od načtení souboru PSD až po export finálního PNG s vykresleným stínovým efektem.

## Rychlé odpovědi
- **Co znamená „uložit PSD jako PNG“?** Převádí vrstvený soubor Photoshopu na plochý PNG obrázek, přičemž zachovává průhlednost.  
- **Mohu při konverzi přidat vržený stín?** Ano – Aspose.PSD vám umožní upravit efekty vrstev před exportem.  
- **Potřebuji licenci pro spuštění kódu?** Bezplatná zkušební verze stačí pro hodnocení; licence je vyžadována pro produkční nasazení.  
- **Jaká verze Javy je podporována?** Java 8 nebo vyšší.  
- **Je efekt vrženého stínu přizpůsobitelný?** Rozhodně – můžete upravit barvu, neprůhlednost, vzdálenost, velikost, úhel a další parametry.

## Požadavky

Než začneme, ujistěte se, že máte:

- **Java vývojové prostředí** – nainstalovaný JDK 8 nebo novější.  
- **Knihovna Aspose.PSD** – Stáhněte nejnovější JAR z oficiální stránky [here](https://releases.aspose.com/psd/java/).  
- **Soubor PSD** – Soubor, který obsahuje alespoň jednu vrstvu, kterou chcete vylepšit stínem.  

## Jak uložit PSD jako PNG s vrženým stínem v Javě?

Níže je podrobný návod krok za krokem. Každý krok obsahuje stručné vysvětlení a následně přesný kód, který je potřeba zkopírovat.

### Krok 1: Importujte požadované balíčky

Začínáme importem tříd, které poskytují načítání obrázků, manipulaci s efekty a export do PNG.

```java
import com.aspose.psd.Image;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.layereffects.DropShadowEffect;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
import com.aspose.psd.Color;

import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.imageoptions.PngOptions;
```

### Krok 2: Definujte adresář dokumentu

Nastavte složku, kde budou umístěny váš zdrojový PSD a výsledný PNG.

```java
String dataDir = "Your Document Directory";
```

### Krok 3: Nastavte cesty k souborům PSD a PNG

Zadejte úplné cesty k vstupnímu PSD a výstupnímu PNG.

```java
String sourceFileName = dataDir + "Shadow.psd";
String pngExportPath = dataDir + "Shadowchanged1.png";
```

### Krok 4: Načtěte soubor PSD s povolenými efekty

Povolení **loadEffectsResource** zajišťuje, že efekty vrstev (např. stíny) jsou k dispozici pro manipulaci.

```java
PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);

PsdImage im = (PsdImage) Image.load(sourceFileName, loadOptions);
```

### Krok 5: Získejte přístup k efektu vrženého stínu

Zde získáme první efekt aplikovaný na druhou vrstvu (index 1). Zde budeme číst nebo upravovat parametry stínu.

```java
DropShadowEffect shadowEffect = (DropShadowEffect) (im.getLayers()[1].getBlendingOptions().getEffects()[0]);
```

### Krok 6: Ověřte vlastnosti efektu stínu (volitelné, ale užitečné)

Kontrola existujících vlastností vám pomůže rozhodnout, zda je třeba něco změnit. Níže uvedené aserce potvrzují výchozí hodnoty.

```java
Assert.areEqual(Color.getBlack(), shadowEffect.getColor());
Assert.areEqual(255, shadowEffect.getOpacity());
Assert.areEqual(3, shadowEffect.getDistance());
Assert.areEqual(7, shadowEffect.getSize());
Assert.areEqual(true, shadowEffect.getUseGlobalLight());
Assert.areEqual(90, shadowEffect.getAngle());
Assert.areEqual(0, shadowEffect.getSpread());
Assert.areEqual(0, shadowEffect.getNoise());
```

> **Tip:** Pokud chcete **přidat stín** s vlastními nastaveními, upravte vlastnosti na `shadowEffect` před uložením (např. `shadowEffect.setColor(Color.getRed());`).

### Krok 7: Uložte upravený obrázek jako PNG

Nakonec exportujeme PSD (s vykresleným stínem) do souboru PNG. Volba `TruecolorWithAlpha` zachovává průhlednost.

```java
PngOptions saveOptions = new PngOptions();
saveOptions.setColorType(PngColorType.TruecolorWithAlpha);
im.save(pngExportPath, saveOptions);
```

A to je vše – kompletní workflow **convert PSD to PNG**, který také **apply drop shadow java** v jednom kroku.

## Proč použít Aspose.PSD pro tuto úlohu?

- **Není vyžadován nativní Photoshop** – Funguje na jakékoli platformě, která podporuje Javu.  
- **Plná věrnost PSD** – Všechny informace o vrstvách, masky a efekty jsou zachovány.  
- **Detailní kontrola** – Upravte každý parametr vrženého stínu před exportem.  
- **Vysoký výkon** – Optimalizováno pro velké soubory a dávkové zpracování.

## Časté problémy a řešení

| Příznak | Pravděpodobná příčina | Řešení |
|---------|-----------------------|--------|
| `NullPointerException` on `shadowEffect` | Cílová vrstva nemá žádné efekty nebo je špatně zvolen index. | Ověřte index vrstvy (`im.getLayers()[i]`) a ujistěte se, že efekt existuje. |
| Exportovaný PNG je prázdný | Možnosti PNG nejsou nastaveny správně nebo obrázek není uložen. | Použijte `PngColorType.TruecolorWithAlpha` a ověřte, že cesta v `im.save()` je zapisovatelná. |
| Barva stínu není viditelná | Neprůhlednost stínu je nastavena na 0 nebo barva odpovídá pozadí. | Nastavte `shadowEffect.setOpacity(255);` a zvolte kontrastní barvu. |

## Často kladené otázky

**Q: Mohu aplikovat vržené stíny na více vrstev najednou?**  
A: Ano. Projděte smyčkou `im.getLayers()` a upravte `DropShadowEffect` každé vrstvy podle potřeby.

**Q: Co dělá parametr „Spread“?**  
A: Ovládá, jak rychle stín přechází z plně neprůhledného na průhledný. Vyšší spread vytváří ostřejší okraj.

**Q: Je Aspose.PSD kompatibilní se všemi verzemi Photoshopu?**  
A: Podporuje širokou škálu verzí PSD, od starších vydání až po nejnovější soubory Photoshop CC.

**Q: Jak mohu získat pomoc, pokud narazím na problémy?**  
A: Navštivte [Aspose.PSD fórum](https://forum.aspose.com/c/psd/34) pro komunitní podporu a oficiální asistenci.

**Q: Můžu si Aspose.PSD vyzkoušet před zakoupením?**  
A: Rozhodně. Stáhněte si bezplatnou zkušební verzi z [Aspose webu](https://releases.aspose.com/).

---

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

**Last Updated:** 2025-12-04  
**Tested With:** Aspose.PSD 24.12 for Java  
**Author:** Aspose