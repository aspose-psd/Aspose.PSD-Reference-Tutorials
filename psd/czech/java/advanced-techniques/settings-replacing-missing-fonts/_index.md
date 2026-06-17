---
date: 2026-06-13
description: Naučte se, jak nahradit písma v souborech PSD pomocí Aspose.PSD pro Java,
  převést PSD na PNG a efektivně řešit chybějící písma.
keywords:
- how to replace fonts
- convert psd to png
- handle missing fonts psd
linktitle: Nastavení pro nahrazení chybějících písem
schemas:
- author: Aspose
  dateModified: '2026-06-13'
  description: Learn how to replace fonts in PSD files using Aspose.PSD for Java,
    convert PSD to PNG, and handle missing fonts efficiently.
  headline: How to Replace Fonts in PSD Files with Aspose.PSD for Java
  type: TechArticle
- questions:
  - answer: '`PsdImage` is the core class that represents a PSD document in memory.'
    question: What is the primary class for loading PSD files?
  - answer: Use `PsdLoadOptions.setDefaultFontName("Arial")`.
    question: Which option sets a default replacement font?
  - answer: Yes—call `psdImage.save("output.png", new PngOptions())`.
    question: Can I save the result as PNG?
  - answer: A temporary license works for testing; a full license is required for
      production.
    question: Do I need a license for development?
  - answer: Aspose.PSD for Java supports Java 8 and later.
    question: What Java version is supported?
  type: FAQPage
second_title: Aspose.PSD Java API
title: Jak nahradit písma v souborech PSD pomocí Aspose.PSD pro Java
url: /cs/java/advanced-techniques/settings-replacing-missing-fonts/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Jak nahradit písma v souborech PSD pomocí Aspose.PSD pro Java

V moderním vývoji v Javě je **jak nahradit písma** v souboru Photoshop (PSD) běžnou výzvou, která může narušit vizuální rozvržení vašich návrhů. Aspose.PSD pro Java nabízí robustní API, které automatizuje substituci písem, což vám umožní zachovat obrázky přesně tak, jak mají vypadat. Tento průvodce vás provede každým krokem – od nastavení prostředí až po uložení finálního PNG – abyste s jistotou zvládli chybějící písma v souborech PSD.

## Rychlé odpovědi
- **Jaká je hlavní třída pro načítání souborů PSD?** `PsdImage` je hlavní třída, která představuje PSD dokument v paměti.  
- **Která možnost nastavuje výchozí písmo pro náhradu?** Použijte `PsdLoadOptions.setDefaultFontName("Arial")`.  
- **Mohu výsledek uložit jako PNG?** Ano – zavolejte `psdImage.save("output.png", new PngOptions())`.  
- **Potřebuji licenci pro vývoj?** Dočasná licence stačí pro testování; pro produkci je vyžadována plná licence.  
- **Jaká verze Javy je podporována?** Aspose.PSD pro Java podporuje Java 8 a novější.

## Jak nahradit písma v souboru PSD pomocí Aspose.PSD pro Java?

Načtěte zdrojový PSD pomocí `PsdLoadOptions`, kde určíte náhradní písmo, a poté obrázek uložte do požadovaného formátu. API automaticky nahradí chybějící glyfy výchozím písmem, které zadáte, čímž eliminuje chyby vykreslování bez ruční úpravy. Tento jednosměrný přístup funguje u souborů jakékoli velikosti a zachovává vrstvy, masky i efekty.

## Co je `PsdLoadOptions`?

`PsdLoadOptions` je konfigurační objekt, který řídí, jak Aspose.PSD parsuje soubor PSD. Umožňuje nastavit výchozí náhradní písmo, kontrolovat chování načítání vrstev a definovat možnosti pro zpracování chybějících zdrojů. Úpravou jeho vlastností mohou vývojáři zajistit konzistentní vykreslování textu a dalších prvků napříč různými prostředími a vyhnout se chybám za běhu způsobeným nedostupnými písmy.

## Proč nahrazovat chybějící písma v souborech PSD?

Aspose.PSD podporuje **více než 50 vstupních a výstupních formátů** a dokáže zpracovat soubory PSD o stovkách stránek, aniž by načítal celý dokument do paměti. Nahrazení chybějících písem zabraňuje poškozeným textovým vrstvám, snižuje čas manuální korekce až o **80 %** a zaručuje, že exportované PNG zachovají původní věrnost designu.

## Požadavky

1. **Knihovna Aspose.PSD** – Stáhněte a nainstalujte knihovnu Aspose.PSD pro Java z [stránky vydání](https://releases.aspose.com/psd/java/).  
2. **Java Development Environment** – Java 8+ JDK a vaše preferované IDE (Eclipse, IntelliJ IDEA, atd.).  

Nyní, když je vše připraveno, ponořme se do implementace.

## Importovat balíčky

Importujte požadované jmenné prostory, aby kompilátor mohl najít třídy Aspose.PSD.

```java
import com.aspose.psd.Image;

import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
import com.aspose.psd.imageoptions.PngOptions;
```

## Krok 1: Nastavte adresář dokumentu

Definujte složku, která obsahuje zdrojový PSD a kam bude zapsán výstup. Tato cesta je používána načítačem i zapisovačem.

```java
String dataDir = "Your Document Directory";
```

## Krok 2: Zadejte zdrojové a cílové soubory

Uveďte absolutní nebo relativní cesty k původnímu PSD a cílovému PNG. Použití jasných pojmenovacích konvencí pomáhá předejít přepsání souborů.

```java
String sourceFile = dataDir + "sample.psd";
String destName = dataDir + "result.png";
```

## Krok 3: Nakonfigurujte nastavení náhrady písma

Vytvořte instanci `PsdLoadOptions` a nastavte výchozí náhradní písmo na **Arial** (nebo jakékoli písmo nainstalované ve vašem systému). Tím řídíte, které písmo se použije, když originál nelze najít.

```java
PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setDefaultReplacementFont("Arial");
```

## Krok 4: Načtěte PSD obrázek a nahraďte písma

Načtěte PSD pomocí nakonfigurovaných možností. Aspose.PSD automaticky během načítání nahrazuje chybějící písma, takže není potřeba žádný další kód.

```java
Image image = Image.load(sourceFile, loadOptions);
PsdImage psdImage = (PsdImage) image;
```

## Krok 5: Uložte upravený obrázek

Zvolte `PngOptions` pro export obrázku jako true‑color PNG s alfa kanálem. Výsledný soubor zobrazí nahrazená písma správně.

```java
PngOptions options = new PngOptions();
options.setColorType(PngColorType.TruecolorWithAlpha);
psdImage.save(destName, options);
```

## Časté problémy a řešení

| Problém | Příčina | Řešení |
|---------|---------|--------|
| Text se zobrazuje poškozeně | Náhradní písmo postrádá požadované glyfy | Zvolte písmo s širším rozsahem Unicode (např. **Arial Unicode MS**). |
| Chyba souboru nenalezen | Nesprávná cesta v kroku 1 nebo 2 | Ověřte řetězce adresářů a použijte `File.separator` pro multiplatformní kompatibilitu. |
| Výjimka licence | Spuštění bez platné licence | Použijte dočasnou licenci pro testování nebo zakupte plnou licenci pro produkci. |

## Často kladené otázky

### Q1: Je Aspose.PSD kompatibilní se všemi verzemi souborů PSD?

A1: Aspose.PSD podporuje verze PSD od **4.0** až po nejnovější vydání Photoshopu, což zajišťuje širokou kompatibilitu mezi staršími i moderními návrhy.

### Q2: Mohu použít vlastní písma pro náhradu v Aspose.PSD?

A2: Ano, můžete zadat libovolné TrueType nebo OpenType písmo nainstalované na serveru předáním jeho názvu do `setDefaultFontName`. To vám dává plnou kontrolu nad vizuálním výsledkem.

### Q3: Existují licenční možnosti pro Aspose.PSD?

A3: Prozkoumejte licenční možnosti [zde](https://purchase.aspose.com/buy), abyste si vybrali nejlepší plán pro vaši organizaci, včetně vývojářských, site‑ a OEM licencí.

### Q4: Existuje komunitní fórum pro podporu Aspose.PSD?

A4: Ano, navštivte [Aspose.PSD fórum](https://forum.aspose.com/c/psd/34) pro komunitní pomoc, ukázky kódu a tipy na řešení problémů od ostatních vývojářů.

### Q5: Jak získat dočasnou licenci pro Aspose.PSD?

A5: Získejte dočasnou licenci [zde](https://purchase.aspose.com/temporary-license/) pro hodnocení, testování nebo projekty proof‑of‑concept bez jakýchkoli nákladů.

**Poslední aktualizace:** 2026-06-13  
**Testováno s:** Aspose.PSD 24.12 for Java  
**Autor:** Aspose  

{{< blocks/products/products-backtop-button >}}

## Související tutoriály

- [Převést PSD na PNG s barevným překrytím – Aspose.PSD pro Java](/psd/java/advanced-image-manipulation/rendering-color-effect/)
- [Jak převést PSD na PNG a změnit velikost proporcionálně s Aspose.PSD pro Java](/psd/java/advanced-image-manipulation/resize-image-proportionally/)
- [Převést PSD na rastrové formáty obrázků s Aspose.PSD pro Java](/psd/java/advanced-techniques/convert-psd-to-raster-formats/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}