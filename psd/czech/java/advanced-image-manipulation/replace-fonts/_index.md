---
date: 2026-06-23
description: Zjistěte, jak uložit PSD jako PNG, nahradit chybějící písma a exportovat
  obrázky pomocí Aspose.PSD pro Javu – rychle zpracujte PSD soubory s chybějícími
  písmy.
keywords:
- save psd as png
- how to replace fonts
- convert psd to bmp
- export psd to jpeg
- handle missing fonts psd
linktitle: Nahradit písma
schemas:
- author: Aspose
  dateModified: '2026-06-23'
  description: Learn how to save PSD as PNG, replace missing fonts, and export images
    using Aspose.PSD for Java – handle missing fonts PSD files quickly.
  headline: How to Save PSD as PNG and Replace Missing Fonts in Java with Aspose
  type: TechArticle
- questions:
  - answer: Yes. While the primary use‑case is PSD, Aspose.PSD also supports PNG,
      JPEG, BMP, and TIFF, allowing font replacement wherever text layers exist.
    question: Can I replace fonts in other image formats besides PSD?
  - answer: No. You can set any TrueType font you prefer, or omit the setting to let
      Aspose use its internal default.
    question: Is the default replacement font mandatory?
  - answer: A commercial license is required for production deployments. See the [purchase
      page](https://purchase.aspose.com/buy) for details.
    question: Are there licensing requirements for using Aspose.PSD?
  - answer: Absolutely. Aspose offers free temporary licenses for evaluation – visit
      the [temporary license page](https://purchase.aspose.com/temporary-license/).
    question: Can I obtain a temporary license for testing?
  - answer: 'The community forum is a great place to ask questions: [Aspose.PSD forum](https://forum.aspose.com/c/psd/34).'
    question: Where can I find additional support or discuss Aspose.PSD‑related issues?
  type: FAQPage
second_title: Aspose.PSD Java API
title: Jak uložit PSD jako PNG a nahradit chybějící písma v Javě s Aspose
url: /cs/java/advanced-image-manipulation/replace-fonts/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Uložit PSD jako PNG – Nahrazení chybějících fontů v Javě

## Úvod

Pokud potřebujete **uložit PSD jako PNG** a zároveň nahradit chybějící nebo nechtěné typy písma v souboru Photoshop (PSD), nahrazení fontů v Aspose PSD to usnadní. V Java aplikacích můžete načíst PSD, říct Aspose, který náhradní font použít, a poté exportovat opravený obrázek v libovolném formátu. Tento tutoriál vás provede kompletním pracovním postupem – od nastavení projektu po export aktualizovaného PNG – takže můžete spolehlivě **zvládat scénáře s chybějícími fonty v PSD** bez nutnosti otevírat Photoshop.

## Rychlé odpovědi
- **Která knihovna provádí nahrazení fontů?** Aspose.PSD for Java  
- **Jak dlouho trvá implementace?** Přibližně 5‑10 minut pro základní scénář  
- **Jaký font se používá jako výchozí náhrada?** Můžete nastavit libovolný TrueType font, např. „Arial“  
- **Mohu ukládat do jiných formátů než PNG?** Ano – podporovány jsou PSD, JPEG, BMP a další  
- **Potřebuji licenci pro produkci?** Pro ne‑zkušební použití je vyžadována platná licence Aspose.PSD  

## Co je Aspose PSD Font Substitution?

Aspose PSD font substitution je proces specifikace náhradního typu písma, který knihovna použije vždy, když narazí na chybějící nebo nepodporovaný font v souboru PSD. To zajišťuje, že textové vrstvy se vykreslí správně bez ruční úpravy ve Photoshopu a umožňuje vám **zvládat soubory PSD s chybějícími fonty** automaticky.

## Proč použít Aspose.PSD pro Java?

Aspose.PSD for Java poskytuje komplexní, výkonný řešení pro práci se soubory Photoshop přímo z Java kódu, čímž eliminuje potřebu samotného Photoshopu. Podporuje širokou škálu typů vrstev, efektů a velkých souborů a nabízí jednoduchá API pro úkoly jako nahrazení fontů, konverze obrázků a manipulaci s metadaty.

- **Kompletní podpora PSD** – Aspose.PSD podporuje **30+ typů vrstev**, **20+ efektů** a dokáže zpracovat soubory až do **2 GB** bez načítání celého dokumentu do paměti.  
- **Cross‑platform** – funguje na jakémkoli OS, který podporuje Java 8+.  
- **Žádné externí závislosti** – knihovna provádí nahrazení fontů interně, takže nemusíte distribuovat další fonty s vaší aplikací.  

## Jak nahradit chybějící fonty v PSD pomocí Aspose PSD

Pro nahrazení chybějících fontů nejprve načtěte PSD s definovaným náhradním fontem v možnostech načtení, poté vykreslete nebo uložte obrázek. Knihovna automaticky nahradí chybějící typy písma fontem, který určíte, a zajistí, že vizuální výstup bude odpovídat vašim očekáváním bez ruční úpravy.

## Požadavky

Než začneme, ujistěte se, že máte:

- **Java Development Kit (JDK)** – verze 8 nebo vyšší nainstalovaná.  
- **Aspose.PSD for Java** – stáhněte nejnovější JAR ze [stránky vydání](https://releases.aspose.com/psd/java/).  
- **IDE** – IntelliJ IDEA, Eclipse nebo jakýkoli editor, který preferujete.  

## Import balíčků

Třída `PsdImage` představuje dokument Photoshopu v paměti a poskytuje přístup k vrstvám, textu a vykreslovacím možnostem. `PsdLoadOptions` řídí, jak je soubor načten, včetně náhradního fontu, zatímco `SaveOptions` (nebo podtřídy specifické pro formát) definují, jak je obrázek zapisován.

```java
import com.aspose.psd.Image;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
import com.aspose.psd.imageoptions.PngOptions;
```

## Krok 1: Nastavte adresář dokumentu

Zadejte složku, která obsahuje zdrojový soubor PSD. Nahraďte zástupný text skutečnou cestou na vašem počítači.

Objekt `File` jednoduše ukazuje na PSD, který chcete zpracovat; zde není potřeba žádná další konfigurace.  

```java
String dataDir = "Your Document Directory";
```

## Krok 2: Načtěte obrázek s náhradním fontem

Vytvořte instanci `PsdLoadOptions`, nastavte výchozí náhradní font (např. **Arial**) a načtěte PSD. Aspose automaticky použije náhradu, kdykoli narazí na chybějící font.

`PsdLoadOptions` vám umožňuje definovat chování načítání, včetně náhradního fontu, který během importní fáze nahradí jakýkoli chybějící typ písma.  

```java
PsdLoadOptions psdLoadOptions = new PsdLoadOptions(); 
psdLoadOptions.setDefaultReplacementFont("Arial");

PsdImage psdImage = (PsdImage)Image.load(dataDir + "Cloud_AzPlat_Banner3A_SB_EN_US_160x600_chinese_font.psd", psdLoadOptions);
```

## Krok 3: Uložte nahrazený obrázek jako PNG

Po nahrazení fontu můžete obrázek exportovat v libovolném podporovaném formátu. Zde jej ukládáme jako PNG, ale můžete také zvolit JPEG, BMP nebo dokonce znovu uložit jako PSD.

Metoda `save` třídy `PsdImage` přijímá objekt `SaveOptions`; použití `PngOptions` zajišťuje, že výstup bude bezztrátový PNG vhodný pro web nebo další zpracování.  

```java
PngOptions pngOptions = new PngOptions();
psdImage.save(dataDir + "replaced_font.png", pngOptions);
```

## Jak uložit PSD jako PNG po nahrazení fontů?

Načtěte PSD s náhradním fontem a poté zavolejte `psdImage.save("output.png", new PngOptions())`. Tento jednorázový příkaz uloží plně vykreslený PNG, který odráží nahrazený typ písma, a umožní vám vložit obrázek kamkoli bez obav o chybějící fonty. Ujistěte se, že jste před uložením aplikovali náhradní font, a případně upravte nastavení komprese PNG pomocí objektu `PngOptions` pro optimální velikost souboru.

## Časté problémy a řešení

| Problém | Příčina | Řešení |
|-------|-------|-----|
| Text se po nahrazení zobrazuje poškozeně | Náhradní font neobsahuje požadované glyfy | Zvolte font, který podporuje potřebný rozsah Unicode (např. „Arial Unicode MS“). |
| `OutOfMemoryError` u velkých PSD souborů | Načítání velmi vysokého rozlišení souboru bez dostatečné haldy | Zvyšte velikost haldy JVM (`-Xmx2g`) nebo načtěte obrázek ve streamovacím režimu, pokud je k dispozici. |
| Výjimka licence | Použití zkušební verze v produkci | Aplikujte platnou trvalou nebo dočasnou licenci před načtením obrázku. |

## Často kladené otázky

**Q: Mohu nahrazovat fonty i v jiných formátech obrázků než PSD?**  
A: Ano. I když je hlavní scénář PSD, Aspose.PSD také podporuje PNG, JPEG, BMP a TIFF, což umožňuje nahrazení fontů kdekoliv existují textové vrstvy.

**Q: Je výchozí náhradní font povinný?**  
A: Ne. Můžete nastavit libovolný TrueType font podle preference, nebo nastavení vynechat a nechat Aspose použít svůj interní výchozí font.

**Q: Existují licenční požadavky pro používání Aspose.PSD?**  
A: Pro nasazení v produkci je vyžadována komerční licence. Podrobnosti najdete na [stránce nákupu](https://purchase.aspose.com/buy).

**Q: Mohu získat dočasnou licenci pro testování?**  
A: Ano. Aspose nabízí zdarma dočasné licence pro hodnocení – navštivte [stránku dočasné licence](https://purchase.aspose.com/temporary-license/).

**Q: Kde mohu najít další podporu nebo diskutovat o problémech souvisejících s Aspose.PSD?**  
A: Komunitní fórum je skvělé místo pro kladení otázek: [Aspose.PSD fórum](https://forum.aspose.com/c/psd/34).

**Q: Jak zacházet se soubory PSD, které obsahují více chybějících fontů?**  
A: Nastavte výchozí náhradní font jednou (jak je ukázáno) – bude aplikován na *všechny* chybějící fonty během načítací operace.

**Q: Je možné nahradit fonty po uložení obrázku?**  
A: Nahrazení fontů musí proběhnout během fáze načtení. Pro změnu fontů později načtěte PSD znovu s jiným náhradním fontem a znovu uložte.

## Závěr

Viděli jste nyní kompletní **workflow pro uložení PSD jako PNG** v Javě – od importu správných tříd, konfigurace náhradního fontu, načtení PSD až po export opraveného PNG. Začleňte tento vzor do vašich pipeline pro zpracování obrázků, abyste zajistili konzistentní typografii napříč všemi vašimi PSD aktivy a **automaticky zvládali chybějící fonty v PSD**.

**Poslední aktualizace:** 2026-06-23  
**Testováno s:** Aspose.PSD for Java 24.12 (nejnovější v době psaní)  
**Autor:** Aspose

## Související tutoriály

- [Nastavení pro nahrazení chybějících fontů v Aspose.PSD pro Java](/psd/java/advanced-techniques/settings-replacing-missing-fonts/)
- [Uložit PSD jako PNG a použít stínování při vykreslování v Aspose.PSD pro Java](/psd/java/advanced-image-manipulation/rendering-drop-shadow/)
- [Jak převést PSD na PNG a změnit velikost proporcionálně s Aspose.PSD pro Java](/psd/java/advanced-image-manipulation/resize-image-proportionally/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< blocks/products/products-backtop-button >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}