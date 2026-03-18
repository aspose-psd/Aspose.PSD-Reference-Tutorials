---
date: 2026-03-18
description: Naučte se, jak převést PSD na PNG a při tom změnit bitovou hloubku PNG
  pomocí Aspose.PSD pro Javu – krok za krokem průvodce s ukázkami kódu.
linktitle: Specify PNG Bit Depth in Aspose.PSD for Java
second_title: Aspose.PSD Java API
title: Jak převést PSD na PNG se specifikovanou bitovou hloubkou pomocí Aspose.PSD
  pro Javu
url: /cs/java/optimizing-png-files/specify-png-bit-depth/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Převod PSD na PNG s určenou bitovou hloubkou pomocí Aspose.PSD pro Java

## Úvod
Pokud potřebujete **převést psd na png** a mít kontrolu nad přesnou bitovou hloubkou PNG, jste na správném místě. V tomto tutoriálu si ukážeme, jak změnit bitovou hloubku PNG při ukládání souboru PSD jako PNG obrázku pomocí Aspose.PSD pro Java. Ať už vytváříte nástroj pro dávkové zpracování, webovou službu nebo desktopovou utilitu, možnost **uložit png s volbami** jako je typ barvy ve stupních šedi a vlastní bitová hloubka vám poskytuje detailní kontrolu nad kvalitou obrazu a velikostí souboru.

## Rychlé odpovědi
- **Mohu změnit bitovou hloubku PNG?** Ano – použijte `PngOptions.setBitDepth()` a zadejte 1, 2, 4, 8 nebo 16 bitů.  
- **Jaké typy barev jsou podporovány?** Stupně šedi, TrueColor, Indexed a další přes `PngColorType`.  
- **Potřebuji licenci pro Aspose.PSD?** Bezplatná zkušební verze funguje pro vývoj; pro produkci je vyžadována komerční licence.  
- **Jaká verze Javy je potřeba?** Java 8+ (knihovna je kompatibilní s novějšími JDK).  
- **Je kód spustitelný tak, jak je?** Ano – stačí nahradit zástupnou cestu vlastní složkou.

## Co je „convert psd to png“ s vlastní bitovou hloubkou?
Převod souboru Photoshop PSD na PNG obrázek je běžná úloha, když potřebujete web‑přátelský formát. Přidání možnosti **upravit kvalitu png** nastavením bitové hloubky vám umožní vyvážit vizuální věrnost a velikost souboru, což je zvláště užitečné pro miniatury, ikony nebo při omezené šířce pásma.

## Proč použít Aspose.PSD pro Java?
Aspose.PSD pro Java poskytuje vysoce úrovňové API, které abstrahuje složitost formátu PSD. Umožňuje vám **vytvořit png ve stupních šedi**, **uložit png s volbami** a pracovat s barevnými profily, aniž byste se museli zabývat nízkoúrovňovou manipulací bajtů. Knihovna je plně spravovaná, multiplatformní a pravidelně aktualizovaná.

## Předpoklady
Než se pustíme do kódu, ujistěte se, že máte následující:

1. **Java Development Kit (JDK)** – stáhněte jej z [webových stránek Oracle](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).  
2. **Aspose.PSD pro Java** – získejte nejnovější JAR z [tohoto odkazu](https://releases.aspose.com/psd/java/).  
3. **Základní znalost Javy** – měli byste být obeznámeni s třídami, metodami a ošetřováním výjimek.  
4. **IDE** jako IntelliJ IDEA nebo Eclipse (volitelné, ale doporučené).  
5. **Ukázkový soubor PSD** – umístěte jej do složky, na kterou budete v kódu odkazovat.

Máte vše? Skvělé – pojďme importovat potřebné balíčky.

## Import balíčků
Nyní, když máme předpoklady pokryté, je čas nastavit prostředí importováním příslušných balíčků v naší Java aplikaci. Otevřete vývojové prostředí a přidejte následující importy na začátek vašeho Java souboru:

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.PngOptions;
```

Tyto příkazy importují třídy, které budeme během tutoriálu používat, což nám umožní načíst PSD soubory a uložit je jako PNG obrázky s určenou bitovou hloubkou.

## Krok 1: Nastavte adresář dokumentů
Než se pustíme do zpracování obrázků, definujme adresář, kde budou naše obrázky uloženy. Je to jako vytvořit složku pro vaše výtvarné potřeby před zahájením projektu.

```java
String dataDir = "Your Document Directory";
```

## Krok 2: Načtěte PSD obrázek
Dále potřebujeme načíst PSD soubor, který chcete převést. Představte si to jako otevření plátna, na kterém budete pracovat.

```java
PsdImage psdImage = (PsdImage)Image.load(dataDir + "sample.psd");
```

Zde využíváme metodu `Image.load()` k načtení našeho ukázkového PSD souboru a přetypování na `PsdImage`, abychom získali přístup k vlastnostem specifickým pro PSD.

## Krok 3: Vytvořte PNG možnosti
Jakmile máme plátno otevřené, potřebujeme sadu možností, jak chceme obrázek uložit. Je to v podstatě výběr barev a štětců před samotným malováním.

```java
PngOptions options = new PngOptions();
```

V tomto kroku inicializujeme instanci `PngOptions`, která nám umožní specifikovat parametry pro výstupní PNG.

## Krok 4: Nastavte požadovaný typ barvy
Nyní rozhodujeme, jaký typ barev chceme v konečném PNG obrázku. Chcete pestrou paletu nebo monochromatický styl? Udělejte si výběr!

```java
options.setColorType(PngColorType.Grayscale);
```

V tomto příkladu nastavujeme typ barvy na stupně šedi. Můžete také zvolit `PngColorType.TrueColor`, pokud chcete plnobarevný obrázek. Toto je část, kde **vytvoříme png ve stupních šedi**.

## Krok 5: Zadejte bitovou hloubku
Dále určete bitovou hloubku. Je to podobné jako říkat tiskárně, jak podrobně má obrázek vytisknout – čím více bitů, tím více detailů!

```java
options.setBitDepth((byte)1);
```

Zde nastavujeme bitovou hloubku na **1 bit**, což je vhodné pro jednoduché stupně šedi. Hodnotu můžete změnit na 2, 4, 8 nebo 16 podle požadované kvality – klasický příklad, jak **změnit bitovou hloubku PNG**.

## Krok 6: Uložte PNG obrázek
Nakonec je čas uložit vaše mistrovské dílo! Tento krok uzavírá náš projekt, když převádíme práci z editovacího plátna na výstupní soubor.

```java
psdImage.save(dataDir + "SpecifyBitDepth_out.png", options);
```

Pomocí metody `save()` třídy `PsdImage` uložíme převedený soubor s aplikovanými možnostmi. Voilà! Náš obrázek je nyní uložen s vlastní bitovou hloubkou.

## Časté problémy a řešení
- **`NullPointerException` při načítání PSD** – ověřte, že `dataDir` ukazuje na správnou složku a že soubor `sample.psd` existuje.  
- **Nesprávná bitová hloubka** – Aspose.PSD podporuje 1, 2, 4, 8 a 16 bitů pro PNG. Použití jiné hodnoty vyvolá `IllegalArgumentException`.  
- **Neshoda typu barvy** – pokud nastavíte bitovou hloubku, která není kompatibilní s vybraným `PngColorType`, knihovna automaticky upraví na nejbližší podporované nastavení.

## Často kladené otázky

**Q: Co je Aspose.PSD pro Java?**  
A: Aspose.PSD pro Java je knihovna pro práci se soubory PSD v Java aplikacích, umožňující manipulaci a konverzi obrázků.

**Q: Jak mohu specifikovat různé bitové hloubky?**  
A: Bitovou hloubku nastavíte pomocí metody `options.setBitDepth((byte)n)`, kde `n` nahradíte požadovanou hodnotou.

**Q: Můžu Aspose.PSD používat zdarma?**  
A: Ano, můžete knihovnu vyzkoušet zdarma pomocí zkušební verze, kterou najdete [zde](https://releases.aspose.com/).

**Q: Kde získám licenci na podporu pro Aspose?**  
A: Pro dočasnou licenci se můžete přihlásit [zde](https://purchase.aspose.com/temporary-license/).

**Q: Jaké typy obrázků mohu převádět?**  
A: Aspose.PSD primárně pracuje se soubory PSD, ale podporuje konverzi do různých formátů jako PNG, JPEG a TIFF.

## Závěr
Nyní jste se naučili, jak **převést psd na png** a zároveň kontrolovat bitovou hloubku PNG pomocí Aspose.PSD pro Java. Úpravou `PngOptions` můžete **upravit kvalitu png**, vytvořit **png ve stupních šedi** a jemně doladit velikost souboru pro jakýkoli scénář. Experimentujte s různými typy barev a bitovými hloubkami, abyste našli ideální rovnováhu pro vaši aplikaci.

---

**Poslední aktualizace:** 2026-03-18  
**Testováno s:** Aspose.PSD pro Java 24.11 (nejnovější v době psaní)  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}