---
date: 2026-05-29
description: Naučte se, jak uložit PSD jako PNG s barevným textem pomocí Aspose.PSD
  for Java. Tento průvodce krok za krokem ukazuje, jak efektivně převést PSD na PNG.
keywords:
- save psd as png
- convert psd to png
- Aspose.PSD Java
linktitle: Vykreslete text s různými barvami v textové vrstvě
schemas:
- author: Aspose
  dateModified: '2026-05-29'
  description: Learn how to save PSD as PNG with colored text using Aspose.PSD for
    Java. This step‑by‑step guide shows how to convert PSD to PNG efficiently.
  headline: Save PSD as PNG with Colored Text using Aspose.PSD for Java
  type: TechArticle
- questions:
  - answer: Aspose.PSD is primarily designed for Java, but Aspose provides similar
      libraries for various programming languages.
    question: Can I use Aspose.PSD for Java with other programming languages?
  - answer: Yes, you can obtain a free trial version from [Aspose.PSD](https://releases.aspose.com/).
    question: Is there a trial version available for Aspose.PSD for Java?
  - answer: Visit the [Aspose.PSD forum](https://forum.aspose.com/c/psd/34) for community
      support and discussions.
    question: Where can I find additional support or assistance?
  - answer: You can request a temporary license from [Aspose.PSD](https://purchase.aspose.com/temporary-license/).
    question: How can I obtain a temporary license for Aspose.PSD for Java?
  - answer: Yes, explore the [Aspose.PSD documentation](https://reference.aspose.com/psd/java/)
      for more tutorials and examples.
    question: Are there other tutorials available for Aspose.PSD?
  type: FAQPage
second_title: Aspose.PSD Java API
title: Uložte PSD jako PNG s barevným textem pomocí Aspose.PSD for Java
url: /cs/java/advanced-techniques/render-text-different-colors/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Uložte PSD jako PNG s barevným textem pomocí Aspose.PSD pro Java

Vítejte v našem podrobném průvodci, jak **uložit PSD jako PNG** s různobarevným textem pomocí Aspose.PSD pro Java. Aspose.PSD je výkonná knihovna pro Javu, která umožňuje programově manipulovat se soubory Photoshopu a poskytuje rozsáhlé možnosti práce s formáty PSD a PSB.

V tomto tutoriálu vás provedeme procesem vykreslení textu s různými barvami v textové vrstvě pomocí Aspose.PSD. Na konci tohoto průvodce budete mít jasnou představu, jak tento úkol provést hladce.

## Rychlé odpovědi
- **Jak uložit PSD jako PNG?** Použijte třídu `PsdImage` z Aspose.PSD k načtení PSD a zavolejte `save` s `PngOptions`.
- **Mohu vykreslit více barev v jedné textové vrstvě?** Ano, přiřaďte různé objekty `Color` každému `Portion` textu.
- **Jaká verze Javy je vyžadována?** Java 8 nebo vyšší je podporována.
- **Potřebuji licenci pro produkci?** Komerční licence je vyžadována; k dispozici je bezplatná zkušební verze.
- **Je knihovna paměťově úsporná pro velké soubory?** Dokáže zpracovat soubory až do 2 GB bez úplného načtení do paměti.

## Jak uložit PSD jako PNG s barevným textem?

Načtěte svůj PSD soubor, upravte části textové vrstvy tak, aby měly odlišné barvy, a poté uložte obrázek jako PNG — tento celý postup se provede během několika řádků Java kódu. Aspose.PSD automaticky rasterizuje upravenou vrstvu, zachová průhlednost i věrnost barev, takže výsledné PNG odpovídá původnímu návrhu.

## Co je Aspose.PSD pro Java?

Aspose.PSD pro Java je knihovna, která umožňuje programové vytváření, úpravu a konverzi souborů Photoshop (PSD/PSB). Podporuje **více než 50 formátů obrázků** a dokáže zpracovat dokumenty o stovkách stránek bez načítání celého souboru do paměti, což poskytuje vysoký výkon pro server‑side automatizaci.

## Požadavky

- Základní znalosti programování v Javě.
- Knihovna Aspose.PSD pro Java nainstalovaná. Můžete ji stáhnout z [dokumentace Aspose.PSD pro Java](https://reference.aspose.com/psd/java/).

## Import balíčků

`Image` je základní třída pro načítání a ukládání obrazových souborů. `PsdImage` představuje dokument Photoshopu, zatímco `TextLayer` poskytuje přístup k vlastnostem textové vrstvy. `PngOptions` definuje nastavení pro export do PNG.  
```java
import com.aspose.psd.Image;

import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.TextLayer;
import com.aspose.psd.imageoptions.PngOptions;
```

## Krok 1: Nastavte svůj projekt

Vytvořte nový Java projekt a zahrňte knihovnu Aspose.PSD. Ujistěte se, že máte potřebná oprávnění pro přístup k souborům a jejich úpravu ve vašem projektovém adresáři.

## Krok 2: Definujte vstupní a výstupní adresáře

Určete vstupní a výstupní adresáře, kde se nacházejí vaše PSD soubory a kam se uloží výsledné obrázky. Aktualizujte proměnné `sourceDir` a `outputDir` podle potřeby.  
```java
String sourceDir = "Your Document Directory";
String outputDir = "Your Document Directory";
```

## Krok 3: Načtěte PSD soubor a přistupte k textové vrstvě

`PsdImage` načte PSD soubor do paměti a `TextLayer` umožňuje manipulaci s textovým obsahem v této vrstvě.  
```java
String targetFilePath = sourceDir + "text_ethalon_different_colors.psd";
String resultFilePath = outputDir + "RenderTextWithDifferentColorsInTextLayer_out.png";

PsdImage psdImage = null;
try
{
    psdImage = (PsdImage) Image.load(targetFilePath);
    TextLayer txtLayer = (TextLayer)psdImage.getLayers()[1];
    txtLayer.getTextData().updateLayerData();
```

## Krok 4: Nastavte PNG možnosti a uložte výsledný obrázek

`PngOptions` konfiguruje parametry výstupu PNG, jako je typ barvy a komprese.  
```java
    PngOptions pngOptions = new PngOptions();
    pngOptions.setColorType(PngColorType.TruecolorWithAlpha);
    psdImage.save(resultFilePath, pngOptions);
}
finally
{
    if (psdImage != null) psdImage.dispose();
}
```

## Časté problémy a řešení

- **Výjimka chybějící licence:** Ujistěte se, že jste před voláním jakékoli operace ukládání aplikovali platný licenční soubor.  
- **Barva se nepoužije:** Ověřte, že každému `Portion` v textové vrstvě je správně nastavena vlastnost `Color`.  
- **Vysoká spotřeba paměti u velkých souborů:** Použijte přetíženou metodu `load` třídy `PsdImage` s `loadOptions` pro streamování velkých souborů.

## Často kladené otázky

**Q: Můžu použít Aspose.PSD pro Java s jinými programovacími jazyky?**  
A: Aspose.PSD je primárně navrženo pro Javu, ale Aspose poskytuje podobné knihovny pro různé programovací jazyky.

**Q: Je k dispozici zkušební verze Aspose.PSD pro Java?**  
A: Ano, bezplatnou zkušební verzi můžete získat na [Aspose.PSD](https://releases.aspose.com/).

**Q: Kde najdu další podporu nebo pomoc?**  
A: Navštivte [forum Aspose.PSD](https://forum.aspose.com/c/psd/34) pro komunitní podporu a diskuze.

**Q: Jak získat dočasnou licenci pro Aspose.PSD pro Java?**  
A: Dočasnou licenci můžete požádat na [Aspose.PSD](https://purchase.aspose.com/temporary-license/).

**Q: Existují další tutoriály k Aspose.PSD?**  
A: Ano, prozkoumejte [dokumentaci Aspose.PSD](https://reference.aspose.com/psd/java/) pro další tutoriály a příklady.

**Q: Podporuje knihovna hromadnou konverzi více PSD souborů do PNG?**  
A: Ano, můžete iterovat přes složku s PSD soubory, aplikovat stejnou logiku barevného textu a uložit každý jako PNG pomocí smyčky.

**Q: Je výstupní PNG bezztrátový?**  
A: PNG uložené pomocí Aspose.PSD zachovává plnou bezztrátovou kvalitu, včetně všech informací o barvách a průhlednosti.

---

**Poslední aktualizace:** 2026-05-29  
**Testováno s:** Aspose.PSD 24.12 pro Java  
**Autor:** Aspose

{{< blocks/products/products-backtop-button >}}

## Související tutoriály

- [Export PSD do PNG a přidání nové běžné vrstvy pomocí Aspose.PSD pro Java](/psd/java/advanced-image-effects/add-new-regular-layer/)
- [Uložte PSD jako PNG a aplikujte vykreslení stínu pomocí Aspose.PSD pro Java](/psd/java/advanced-image-manipulation/rendering-drop-shadow/)
- [Převod PSD na PNG s barevným překrytím – Aspose.PSD pro Java](/psd/java/advanced-image-manipulation/rendering-color-effect/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}