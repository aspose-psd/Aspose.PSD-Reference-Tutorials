---
date: 2026-04-05
description: Naučte se, jak exportovat PSD do PNG a bez námahy zvýšit kontrast obrázku
  pomocí Aspose.PSD pro Javu. Ovládněte vrstvy úpravy úrovní s tímto krok‑za‑krokem
  průvodcem.
keywords:
- export psd to png
- how to adjust levels
- batch process psd files
linktitle: Export PSD do PNG a vykreslení vrstvy úpravy úrovně v Javě
second_title: Aspose.PSD Java API
title: Exportovat PSD do PNG a renderovat vrstvu úpravy úrovně v Javě
url: /cs/java/psd-layer-management-effects/render-level-adjustment-layer-psd/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Export PSD do PNG a vykreslení vrstvy úpravy úrovní v Javě

## Úvod

Už jste někdy otevřeli soubor PSD a všimli si, že barvy vypadají ploché nebo kontrast není správný? Můžete rychle **export PSD to PNG** a zároveň jemně doladit obrázek pomocí vrstvy úpravy úrovní pomocí Aspose.PSD pro Javu. V tomto tutoriálu vás provedeme celým procesem – od načtení PSD, úpravy úrovní až po uložení výsledku jako PNG – takže můžete zvýšit živost a během několika minut připravit webové assety.

## Rychlé odpovědi
- **What does “export PSD to PNG” mean?** Převádí dokument Photoshopu do bezztrátového PNG obrázku při zachování průhlednosti.  
- **Can I adjust levels before exporting?** Ano, Aspose.PSD vám umožňuje programově upravovat vstupní a výstupní úrovně.  
- **Do I need a license?** Bezplatná zkušební verze funguje pro vývoj; pro produkci je vyžadována komerční licence.  
- **Is batch processing possible?** Rozhodně – můžete umístit kód do smyčky pro zpracování více souborů PSD.  
- **Which Java version is required?** Doporučuje se Java 8 nebo novější.

## Co je “export PSD to PNG”?
Exportování PSD do PNG znamená převést vrstvený soubor Photoshopu a zploštit jej do obrázku Portable Network Graphics. PNG podporuje bezztrátovou kompresi a alfa kanál, což ho činí ideálním pro webovou grafiku a UI assety.

## Proč upravit úrovně před exportem?
Úprava úrovní vám umožní řídit stíny, střední tóny a světla, čímž zlepšuje celkový kontrast a barevnou rovnováhu. Tento krok zajišťuje, že finální PNG vypadá vylepšeně bez nutnosti ruční úpravy ve Photoshopu.

## Požadavky

- **Java Development Kit (JDK)** – stáhněte nejnovější verzi z webu Oracle ([https://www.oracle.com/java/technologies/javase-downloads.html](https://www.oracle.com/java/technologies/javase-downloads.html)).  
- **Aspose.PSD for Java Library** – stáhněte ji z oficiální stránky ke stažení ([https://releases.aspose.com/psd/java/](https://releases.aspose.com/psd/java/)). K dispozici je bezplatná zkušební verze ([https://releases.aspose.com/](https://releases.aspose.com/)).

## Import balíčků

Než se ponoříte do kódu, importujte třídy, které nám poskytují přístup k manipulaci s PSD a exportu do PNG:

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.adjustmentlayers.LevelsLayer;
import com.aspose.psd.fileformats.psd.layers.layerresources.LevelChannel;
import com.aspose.psd.imageoptions.PngOptions;
```

## Průvodce krok za krokem

### Krok 1: Definujte cesty k souborům (Jak automatizovat zpracování PSD)

Nastavte jasné, popisné proměnné pro zdrojový PSD, upravený PSD a konečnou destinaci exportu PNG.

```java
String dataDir = "Your Document Directory";

String sourceFileName = dataDir + "LevelsAdjustmentLayer.psd";
String psdPathAfterChange = dataDir + "LevelsAdjustmentLayerChanged.psd";
String pngExportPath = dataDir + "LevelsAdjustmentLayerChanged.png";
```

### Krok 2: Načtěte obrázek PSD

Použijte `Image.load` k načtení souboru PSD do objektu `PsdImage`. Aspose.PSD automaticky detekuje formát.

```java
PsdImage im = (PsdImage)Image.load(sourceFileName);
```

### Krok 3: Procházejte vrstvy (Jak upravit úrovně)

Projděte každou vrstvu, abyste našli vrstvu úpravy úrovní.

```java
for (int i = 0; i < im.getLayers().length; i++) {
   // ... (code to check for Levels Layer will be added here)
}
```

### Krok 4: Identifikujte vrstvu úrovní

Zkontrolujte každou vrstvu pomocí `instanceof LevelsLayer`. Jakmile ji najdete, přetypujte ji, abychom mohli upravit její vlastnosti.

```java
for (int i = 0; i < im.getLayers().length; i++) {
   if (im.getLayers()[i] instanceof LevelsLayer) {
	   LevelsLayer levelsLayer = (LevelsLayer) im.getLayers()[i];
	   // ... (code to adjust levels will be added here)
   }
}
```

### Krok 5: Jemně doladit úrovně (Jak upravit úrovně)

Upravte vstupní i výstupní úrovně pro první kanál (obvykle kompozitní kanál). Tyto hodnoty jsou jen příklady; klidně experimentujte.

```java
for (int i = 0; i < im.getLayers().length; i++) {
   if (im.getLayers()[i] instanceof LevelsLayer) {
	   LevelsLayer levelsLayer = (LevelsLayer) im.getLayers()[i];
	   LevelChannel channel = levelsLayer.getChannel(0);

	   // Adjust Input Levels (0‑255):
	   channel.setInputShadowLevel((short) 10); // Darken shadows slightly
	   channel.setInputMidtoneLevel(2.0f);     // Increase midtones
	   channel.setInputHighlightLevel((short) 230); // Reduce highlights

	   // Adjust Output Levels (0‑255):
	   channel.setOutputShadowLevel((short) 20); // Darken shadows further
	   channel.setOutputHighlightLevel((short) 200); // Brighten highlights
   }
}
```

### Krok 6: Uložte upravený PSD (Jak automatizovat PSD)

Uložte změny zpět do nového souboru PSD.

```java
im.save(psdPathAfterChange);
```

### Krok 7: Exportujte jako PNG (Export PSD to PNG)

Pokud potřebujete verzi PNG, nakonfigurujte `PngOptions` a uložte obrázek.

```java
PngOptions saveOptions = new PngOptions();
saveOptions.setColorType(PngColorType.TruecolorWithAlpha);
im.save(pngExportPath, saveOptions);
```

## Běžné případy použití

- **Web asset preparation:** Převést návrhem poskytnuté PSD mockupy do PNG připravených pro prohlížeče.  
- **Batch processing:** Automatizovat konverzi desítek souborů PSD v CI pipeline.  
- **Dynamic image generation:** Upravit úrovně za běhu na základě vstupu uživatele před exportem.

## Řešení problémů a tipy

- **Null pointer when accessing layers:** Ujistěte se, že PSD skutečně obsahuje vrstvu úpravy úrovní; jinak přidejte kontrolu na null.  
- **Unexpected colors after export:** Ověřte, že typ barvy PNG je nastaven na `TruecolorWithAlpha`, aby se zachovala průhlednost.  
- **Performance with many files:** Znovu použijte stejnou instanci `PsdImage` při zpracování dávky, aby se snížila zátěž paměti.

## Často kladené otázky

**Q: Mohu upravit jednotlivé barevné kanály (RGB) samostatně?**  
A: Ano. Použijte `levelsLayer.getChannel(index)`, kde `index` = 0 (Red), 1 (Green), 2 (Blue) pro úpravu každého kanálu samostatně.

**Q: Jak mohu zpracovat více vrstev úpravy úrovní v jednom PSD?**  
A: Smyčka zpracovává každou vrstvu; každá nalezená `LevelsLayer` bude upravena podle kódu uvnitř bloku `if`.

**Q: Existují i jiné způsoby, jak zlepšit kontrast kromě úrovní?**  
A: Aspose.PSD také nabízí úpravy křivek, jas/kontrast a ekvalizaci histogramu.

**Q: Mohu to automatizovat pro složku souborů PSD?**  
A: Zabalte celý workflow do smyčky `File[] files = new File(dataDir).listFiles((d, name) -> name.endsWith(".psd"));` a zpracovávejte každý soubor postupně.

**Q: Kde mohu najít další dokumentaci a podporu?**  
A: Navštivte oficiální referenci ([https://reference.aspose.com/psd/java/](https://reference.aspose.com/psd/java/)) a komunitní fórum ([https://forum.aspose.com/c/psd/34](https://forum.aspose.com/c/psd/34)).

## Závěr

Ovládnutím workflow **export PSD to PNG** a naučením se **how to adjust levels** programově získáte plnou kontrolu nad kvalitou obrazu, aniž byste opustili své Java prostředí. Ať už připravujete assety pro web, automatizujete design pipeline nebo vytváříte dávkový procesor, Aspose.PSD pro Javu dělá práci jednoduchou a spolehlivou.

---

**Poslední aktualizace:** 2026-04-05  
**Testováno s:** Aspose.PSD 24.11 for Java  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}