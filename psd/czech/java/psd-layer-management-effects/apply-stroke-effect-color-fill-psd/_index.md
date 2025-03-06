---
title: Použijte efekt tahu s barevnou výplní v PSD - Java
linktitle: Použijte efekt tahu s barevnou výplní v PSD - Java
second_title: Aspose.PSD Java API
description: Naučte se, jak aplikovat efekt tahu s barevnou výplní na vaše soubory PSD pomocí Aspose.PSD for Java. Postupujte podle tohoto podrobného průvodce, abyste své obrázky snadno vylepšili.
weight: 21
url: /cs/java/psd-layer-management-effects/apply-stroke-effect-color-fill-psd/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Použijte efekt tahu s barevnou výplní v PSD - Java

## Zavedení

této příručce vás provedeme procesem aplikace efektu tahu s barevnou výplní na vaše soubory PSD pomocí Aspose.PSD for Java. Ať už jste zkušený vývojář nebo teprve začínáte, tento podrobný návod vám usnadní práci. Pokryjeme vše od nastavení vašeho prostředí až po uložení finálního obrázku s aplikovanými efekty.

## Předpoklady

Než začneme, ujistěte se, že máte vše, co potřebujete, abyste spolu s tímto tutoriálem:

1. Nainstalovaná Java Development Kit (JDK): Ujistěte se, že máte v systému nainstalovanou JDK 8 nebo vyšší.
2.  Aspose.PSD for Java Library: Budete potřebovat knihovnu Aspose.PSD for Java. Můžete si jej stáhnout z[webové stránky](https://releases.aspose.com/psd/java/).
3. Integrované vývojové prostředí (IDE): IDE jako IntelliJ IDEA, Eclipse nebo jakékoli jiné podle vašeho výběru.
4. Ukázkový soubor PSD: Ukázkový soubor PSD, na který můžete použít efekt tahu. Pokud žádný nemáte, můžete si vytvořit jednoduchý soubor PSD ve Photoshopu nebo si jej stáhnout z internetu.
5. Základní znalost Javy: I když je tento tutoriál vhodný pro začátečníky, bude užitečné mít nějaké základní znalosti Javy.

Jakmile splníte tyto předpoklady, jste připraveni začít aplikovat efekt tahu s barevnou výplní na vaše soubory PSD.

## Importujte balíčky

Chcete-li začít pracovat s Aspose.PSD for Java, budete muset do svého projektu Java importovat potřebné balíčky. Můžete to udělat takto:

```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.fillsettings.ColorFillSettings;
import com.aspose.psd.fileformats.psd.layers.layereffects.StrokeEffect;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
import com.aspose.psd.imageoptions.PngOptions;
import com.aspose.psd.imageoptions.PsdOptions;
```

Tyto importy přinášejí všechny potřebné třídy, které budete potřebovat pro práci se soubory PSD, aplikaci efektů a ukládání obrázků v požadovaném formátu.

## Krok 1: Načtěte soubor PSD

 Prvním krokem v našem procesu je načtení souboru PSD, který chcete upravit. Aspose.PSD pro Java to neuvěřitelně zjednodušuje`PsdImage` třída. Můžete to udělat takto:

### 1.1 Nastavte cestu k adresáři

Nejprve definujte cestu k adresáři, kde jsou uloženy vaše soubory PSD:

```java
String dataDir = "Your Document Directory";
```

 Nahradit`"Your Document Directory"` se skutečnou cestou, kde se nachází váš soubor PSD.

### 1.2 Načtěte obrázek PSD

 Nyní načtěte soubor PSD pomocí`PsdLoadOptions` a`PsdImage` třídy:

```java
String sourceFileName = dataDir + "StrokeComplex.psd";

PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);

PsdImage im = (PsdImage) Image.load(sourceFileName, loadOptions);
```

 Tady,`PsdLoadOptions`je nakonfigurován tak, aby načítal zdroje efektů, což zajišťuje, že všechny existující efekty v PSD jsou přístupné.

## Krok 2: Aplikujte efekt tahu s barevnou výplní

Po načtení souboru PSD je dalším krokem použití efektu tahu na vrstvy obrázku. Tady se odehrává ta pravá magie.

Každý soubor PSD může obsahovat více vrstev a na každou z nich budete muset použít efekt. Jak na to:

```java
for (int i = 0; i < im.getLayers().length; i++) {
    StrokeEffect effect = (StrokeEffect) im.getLayers()[i].getBlendingOptions().getEffects()[0];
    ColorFillSettings settings = (ColorFillSettings) effect.getFillSettings();
    settings.setColor(Color.getDeepPink());
}
```

V této smyčce:

- `im.getLayers()`: Načte všechny vrstvy v souboru PSD.
- `StrokeEffect effect`: Extrahuje efekt tahu aplikovaný na vrstvu.
- `ColorFillSettings settings`: Upravuje nastavení výplně pro efekt tahu.
- `settings.setColor(Color.getDeepPink())`: Nastaví barvu tahu na sytě růžovou. Tuto barvu můžete změnit na libovolnou barvu.

## Krok 3: Uložte upravené PSD a exportujte jako PNG

Jakmile použijete efekt tahu, je čas uložit změny a exportovat obrázek.

### 3.1 Uložte soubor PSD

Chcete-li uložit upravený soubor PSD, použijte následující kód:

```java
String exportPath = dataDir + "StrokeComplexRendering.psd";
im.save(exportPath, new PsdOptions());
```

Tím se soubor s aplikovaným efektem tahu uloží do zadané cesty.

### 3.2 Exportovat jako PNG

Chcete-li obrázek zpřístupnit, můžete jej exportovat jako soubor PNG. Zde je postup:

```java
String exportPathPng = dataDir + "StrokeComplexRendering.png";
PngOptions option = new PngOptions();
option.setColorType(PngColorType.TruecolorWithAlpha);

im.save(exportPathPng, option);
```

Tento fragment kódu uloží obrázek jako PNG se skutečnými barvami a průhledností alfa, takže je připraven k použití ve webových aplikacích nebo jiných platformách.

## Závěr

Použití efektu tahu s barevnou výplní na vaše soubory PSD pomocí Aspose.PSD pro Java je nejen jednoduché, ale také neuvěřitelně výkonné. Pomocí několika řádků kódu můžete automatizovat složité úlohy zpracování obrazu, což vám ušetří čas i námahu.

Ať už pracujete na velké dávce obrázků nebo jen potřebujete upravit několik souborů, tato metoda poskytuje flexibilní a efektivní řešení. Nyní, když máte základy, můžete začít experimentovat s různými efekty a přizpůsobeními, aby vaše snímky skutečně vynikly.

Jste připraveni to vyzkoušet? Vezměte si svůj ukázkový soubor PSD a začněte přidávat ty úžasné efekty ještě dnes!

## FAQ

### Mohu použít více efektů na jednu vrstvu pomocí Aspose.PSD pro Java?
Ano, můžete použít více efektů na jednu vrstvu tak, že otevřete možnosti prolnutí vrstvy a přidáte požadované efekty.

### Je možné automatizovat proces pro dávku souborů PSD?
Absolutně! Můžete procházet adresář souborů PSD, aplikovat efekt tahu a automaticky ukládat výsledky.

### Jak mohu vrátit změny provedené v souboru PSD pomocí Aspose.PSD for Java?
Chcete-li vrátit změny, budete muset před uložením jakýchkoli úprav znovu načíst původní soubor PSD. V Aspose.PSD není žádná funkce přímého vrácení zpět.

### Mohu přizpůsobit šířku a polohu tahu?
 Ano, Aspose.PSD pro Java vám umožňuje přizpůsobit šířku tahu, polohu a další vlastnosti prostřednictvím`StrokeEffect` třída.

### Je knihovna Aspose.PSD for Java k použití zdarma?
 Aspose.PSD for Java nabízí bezplatnou zkušební verzi, ale pro plný přístup ke všem funkcím byste si museli zakoupit licenci. Můžete prozkoumat[koupit opce](https://purchase.aspose.com/buy)na jejich webových stránkách.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
