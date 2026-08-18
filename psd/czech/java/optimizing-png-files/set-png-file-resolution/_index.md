---
date: 2026-03-18
description: Naučte se, jak změnit rozlišení PNG v Javě a nastavit rozlišení obrázku
  v Javě pomocí Aspose.PSD pro Javu. Postupujte podle tohoto krok‑za‑krokem průvodce
  a rychle optimalizujte své obrázky.
linktitle: Change PNG resolution java using Aspose.PSD
second_title: Aspose.PSD Java API
title: Změna rozlišení PNG v Javě pomocí Aspose.PSD
url: /cs/java/optimizing-png-files/set-png-file-resolution/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Změna rozlišení PNG java pomocí Aspose.PSD

## Úvod
Pokud potřebujete **change PNG resolution java** rychle a spolehlivě, jste na správném místě. V tomto tutoriálu projdeme přesně kroky potřebné k úpravě rozlišení PNG souboru pomocí Aspose.PSD pro Java. Ať už vytváříte nástroj pro dávkové zpracování, webovou službu nebo jen vylepšujete několik assetů, stejný přístup funguje všude. Vezměte si své oblíbené IDE a pojďme na to!

## Rychlé odpovědi
- **Jaká knihovna zpracovává rozlišení PNG?** Aspose.PSD for Java  
- **Primární metoda?** `PngOptions.setResolutionSettings`  
- **Typické hodnoty DPI?** 72 × 96 pro web‑ready obrázky  
- **Potřebuji licenci?** Zkušební verze funguje pro testování; licence je vyžadována pro produkci  
- **Podporovaný JDK?** Java 8 nebo vyšší  

## Co je “change PNG resolution java”?
Změna rozlišení PNG v Javě znamená úpravu metadat DPI (dots per inch), která říkají prohlížečům a tiskárnám, jak velký má obrázek být. Pixelová data zůstávají stejná, ale značka rozlišení se aktualizuje, což může ovlivnit velikost tisku a kvalitu.

## Proč použít Aspose.PSD pro tento úkol?
Aspose.PSD poskytuje vysoce‑úrovňové API, které abstrahuje nízko‑úrovňové zpracování PNG, což vám umožní soustředit se na obchodní logiku místo zvláštností formátu souboru. Podporuje stovky funkcí PSD, funguje na jakékoli platformě, která spouští Java, a nevyžaduje žádné nativní knihovny.

## Předpoklady
Předtím, než začnete, ujistěte se, že máte:

1. **Java Development Kit (JDK) 8+** – kód běží na jakémkoli aktuálním JDK.  
2. **Aspose.PSD for Java** – stáhněte jej z [download link](https://releases.aspose.com/psd/java/).  
3. **IDE** – IntelliJ IDEA, Eclipse nebo VS Code s podporou Javy.  
4. **Ukázkový soubor PSD** – převedeme jej na PNG a změníme jeho rozlišení.  
5. **Základní znalost Javy** – pochopíte úryvky kódu bez dalšího vysvětlení.  

## Import balíčků
Nyní, když máme vše připravené, importujte třídy, které budete potřebovat. Tyto importy vám poskytují přístup k načítání obrázků, nastavením rozlišení a možnostem exportu PNG.

```java
import com.aspose.psd.Image;
import com.aspose.psd.ResolutionSetting;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.PngOptions;
```

## Krok 1: Nastavte svůj Java projekt
Vytvořte nový Java projekt (nebo Maven/Gradle modul) a přidejte JAR Aspose.PSD do cesty sestavení. Pokud používáte Maven, přidejte odpovídající závislost z repozitáře Aspose.

## Krok 2: Definujte adresář dokumentů
Řekněte programu, kde najít zdrojový soubor PSD a kam zapsat výstupní PNG.

```java
String dataDir = "Your Document Directory"; // Update with your folder path
```

Nahraďte `"Your Document Directory"` absolutní nebo relativní cestou, která obsahuje `sample.psd`.

## Krok 3: Načtěte PSD obrázek
Použijte třídu `PsdImage` k načtení souboru PSD z disku.

```java
PsdImage psdImage = (PsdImage) Image.load(dataDir + "sample.psd");
```

Ujistěte se, že název souboru odpovídá skutečnému PSD, který chcete zpracovat.

## Krok 4: Vytvořte a nakonfigurujte PNG možnosti
Zde skutečně **change PNG resolution java**. Vytvoříme instanci `PngOptions` a nastavíme horizontální a vertikální hodnoty DPI pomocí `ResolutionSetting`.

```java
PngOptions options = new PngOptions();
options.setResolutionSettings(new ResolutionSetting(72, 96)); // 72 DPI horizontal, 96 DPI vertical
```

Klidně nahraďte `72` a `96` libovolnými hodnotami, které vyhovují vašemu cílovému zařízení. Toto je jádro operace **set image resolution java**.

## Krok 5: Uložte výsledný PNG
Nakonec exportujte PSD jako PNG s novými metadaty rozlišení.

```java
psdImage.save(dataDir + "SettingResolution_output.png", options);
```

Soubor `SettingResolution_output.png` se objeví ve stejném adresáři a bude nyní obsahovat DPI hodnoty, které jste zadali.

## Časté úskalí a tipy
- **Nesprávná cesta** – Zkontrolujte, že `dataDir` končí souborovým oddělovačem (`/` nebo `\`).  
- **Není podporováno DPI** – Většina prohlížečů ignoruje DPI hodnoty nad 300; udržujte je rozumné.  
- **Využití paměti** – Velké PSD mohou spotřebovat značnou RAM; zvažte uvolnění `psdImage` po uložení (`psdImage.dispose()`).  

## Závěr
Právě jste se naučili, jak **change PNG resolution java** pomocí Aspose.PSD. Úpravou `ResolutionSetting` můžete řídit, jak jsou vaše PNG interpretovány tiskárnami a designovými nástroji, aniž byste měnili pixelová data. Prozkoumejte další možnosti, jako je úroveň komprese, barevná hloubka nebo dávkové zpracování, abyste dále automatizovali svůj pracovní postup.

Pro podrobnější průzkum si prohlédněte oficiální [Aspose.PSD Documentation](https://reference.aspose.com/psd/java/).

## Často kladené otázky
### Jaké formáty mohu převést z PSD pomocí Aspose.PSD pro Java?
Můžete převést soubory PSD do formátů jako PNG, JPEG, BMP a TIFF.  
### Potřebuji licenci pro použití Aspose.PSD pro Java?
Ano, i když je k dispozici bezplatná zkušební verze, platná licence je vyžadována pro další používání po vyhodnocení.  
### Můžu změnit rozlišení vícekrát v jednom programu?
Rozhodně! Můžete vytvořit různé instance `PngOptions` pro různá nastavení exportu v rámci jedné aplikace.  
### Co když je můj soubor PSD poškozený?
Aspose.PSD řeší mnoho běžných problémů, ale pokud je soubor silně poškozený, nemusí se načíst. Vždy si uchovávejte zálohu.  
### Je Aspose.PSD vhodný pro vysoce výkonné aplikace?
Ano, je navržen tak, aby efektivně zpracovával velké soubory a je vhodný pro výkonnostně náročné úlohy zpracování obrazu.

## Často kladené otázky
**Q: Jak mohu programově nastavit odlišné DPI pro horizontální a vertikální osu?**  
A: Použijte `new ResolutionSetting(horizontalDpi, verticalDpi)` jak je ukázáno v příkladu PNG možností.  

**Q: Můžu dávkově zpracovat více souborů PSD v jednom běhu?**  
A: Ano—zabalte kroky načítání, konfigurace možností a ukládání do smyčky, která iteruje přes vaši kolekci souborů.  

**Q: Ovlivňuje změna DPI velikost souboru?**  
A: Obvykle ne; DPI jsou metadata. Velikost souboru se změní jen při úpravě komprese nebo rozměrů pixelů.  

**Q: Existuje způsob, jak přečíst aktuální DPI existujícího PNG?**  
A: Načtěte PNG pomocí `Image.load()` a prohlédněte `image.getResolutionSettings()` (k dispozici pro PNG soubory).  

**Q: Které verze JDK jsou oficiálně podporovány?**  
A: Aspose.PSD pro Java podporuje JDK 8 až JDK 21.  

**Poslední aktualizace:** 2026-03-18  
**Testováno s:** Aspose.PSD for Java 24.10  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}