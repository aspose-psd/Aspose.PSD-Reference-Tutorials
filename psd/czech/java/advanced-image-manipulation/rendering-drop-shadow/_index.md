---
title: Použijte Rendering Drop Shadow v Aspose.PSD pro Javu
linktitle: Použít vykreslení vrženého stínu
second_title: Aspose.PSD Java API
description: Prozkoumejte podrobného průvodce aplikací vykreslování vržených stínů v Aspose.PSD pro Java, který bez námahy vylepší vaše dovednosti zpracování obrazu.
weight: 16
url: /cs/java/advanced-image-manipulation/rendering-drop-shadow/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Použijte Rendering Drop Shadow v Aspose.PSD pro Javu

## Zavedení

Pokud se ponoříte do zpracování obrazu pomocí Javy, Aspose.PSD je váš oblíbený nástroj pro bezproblémovou a efektivní manipulaci se soubory PSD. V tomto tutoriálu prozkoumáme proces aplikace vrženého stínu vykreslení pomocí Aspose.PSD pro Java. Připoute se, protože pro vás rozebereme kroky.

## Předpoklady

Než se vydáme na tuto cestu, ujistěte se, že máte splněny následující předpoklady:

- Vývojové prostředí Java: Ujistěte se, že máte na svém počítači nainstalovanou Javu.
- Knihovna Aspose.PSD: Stáhněte a nastavte knihovnu Aspose.PSD. Knihovnu najdete[zde](https://releases.aspose.com/psd/java/).
- Soubor PSD: Připravte soubor PSD obsahující vrstvu, na kterou chcete použít vržený stín.

## Importujte balíčky

Začněme tím, že naimportujeme potřebné balíčky. Tento krok zajistí, že budete mít k dispozici základní nástroje pro hladké provádění kódu.

```java
import com.aspose.psd.Image;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.layereffects.DropShadowEffect;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
import com.aspose.psd.Color;

import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.imageoptions.PngOptions;
```

Nyní si rozeberme každý krok.

## Krok 1: Definujte adresář dokumentů

Začněte zadáním adresáře, kde se nachází váš soubor PSD.

```java
String dataDir = "Your Document Directory";
```

## Krok 2: Nastavte cesty souborů PSD a PNG

Definujte cesty pro váš zdrojový soubor PSD a cílový soubor PNG.

```java
String sourceFileName = dataDir + "Shadow.psd";
String pngExportPath = dataDir + "Shadowchanged1.png";
```

## Krok 3: Načtěte soubor PSD s efekty

Načtěte soubor PSD a povolte načítání zdrojů efektů.

```java
PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);

PsdImage im = (PsdImage) Image.load(sourceFileName, loadOptions);
```

## Krok 4: Přístup k efektu vrženého stínu

Načtěte efekt vrženého stínu ze zadané vrstvy.

```java
DropShadowEffect shadowEffect = (DropShadowEffect) (im.getLayers()[1].getBlendingOptions().getEffects()[0]);
```

## Krok 5: Ověřte vlastnosti stínového efektu

Ujistěte se, že vlastnosti efektu vrženého stínu splňují vaše očekávání.

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

## Krok 6: Uložte jako PNG

Uložte upravený obrázek jako soubor PNG.

```java
PngOptions saveOptions = new PngOptions();
saveOptions.setColorType(PngColorType.TruecolorWithAlpha);
im.save(pngExportPath, saveOptions);
```

A tady to máte – podrobný návod k použití vykreslování vržených stínů v Aspose.PSD pro Java.

## Závěr

Zvládnutí manipulace s obrázky v Javě se s Aspose.PSD stává hračkou. Právě jste odemkli tajemství vykreslování vržených stínů a otevřeli svět kreativních možností.

## FAQ

### Q1: Mohu aplikovat vržené stíny na více vrstev současně?

Odpověď 1: Ano, můžete procházet vrstvami a podle potřeby aplikovat vržené stíny.

### Otázka 2: Jaký je význam parametru „Rozprostření“ ve vržených stínech?

Odpověď 2: Parametr 'Spread' řídí přechod mezi stínovými a nestínovými oblastmi.

### Q3: Je Aspose.PSD kompatibilní se všemi verzemi souborů Photoshopu?

Odpověď 3: Aspose.PSD poskytuje kompatibilitu s širokou škálou verzí souborů PSD a zajišťuje všestrannost.

### Q4: Jak mohu nahlásit problémy nebo požádat o pomoc s Aspose.PSD?

 A4: Přejděte na[Fórum Aspose.PSD](https://forum.aspose.com/c/psd/34) za komplexní podporu.

### Q5: Mohu otestovat Aspose.PSD před nákupem?

 A5: Rozhodně, použijte[zkušební verze zdarma](https://releases.aspose.com/) prozkoumat možnosti, než se zavážete k nákupu.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
