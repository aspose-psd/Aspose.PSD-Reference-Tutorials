---
title: Přidejte efekty za běhu pomocí Aspose.PSD pro Javu
linktitle: Přidejte efekty za běhu
second_title: Aspose.PSD Java API
description: Prozkoumejte bezproblémovou integraci Aspose.PSD pro Java a dynamicky přidávejte do obrázků podmanivé efekty. Zvyšte svůj vývoj v Javě pomocí tohoto intuitivního tutoriálu.
type: docs
weight: 20
url: /cs/java/advanced-techniques/add-effects-runtime/
---
## Úvod

Ve světě vývoje v Javě je přidávání dynamických efektů do obrázků běžným požadavkem. S Aspose.PSD for Java, výkonnou a všestrannou knihovnou Java, můžete bez námahy přidávat efekty za běhu pro vylepšení obrázků. V tomto tutoriálu vás provedeme procesem přidávání efektů krok za krokem pomocí jasných příkladů a snadno pochopitelných pokynů.

## Předpoklady

Než se pustíte do výukového programu, ujistěte se, že máte splněny následující předpoklady:

1.  Java Development Kit (JDK): Ujistěte se, že máte v systému nainstalovanou Java. Nejnovější JDK si můžete stáhnout z[tady](https://www.oracle.com/java/technologies/javase-downloads.html).

2.  Aspose.PSD for Java Library: Musíte mít knihovnu Aspose.PSD for Java. Pokud jste tak ještě neučinili, stáhněte si jej z[Aspose.PSD Java dokumentace](https://reference.aspose.com/psd/java/).

3. Adresář dokumentů: Nastavte adresář pro své dokumenty a zapamatujte si cestu. V uvedeném příkladu je adresář označován jako`Your Document Directory`.

## Importujte balíčky

Ve svém projektu Java naimportujte potřebné balíčky pro využití funkcí Aspose.PSD for Java.

```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.BlendMode;
import com.aspose.psd.fileformats.psd.layers.layereffects.ColorOverlayEffect;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
```

## Krok 1: Načtěte obrázek PSD

Začněte načtením obrázku PSD, na který chcete použít efekty. Ujistěte se, že jste nastavili správnou cestu k souboru.

```java
String sourceFileName = "Your Document Directory/ThreeRegularLayers.psd";
String exportPath = "Your Document Directory/ThreeRegularLayersChanged.psd";

PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);

PsdImage im = (PsdImage)Image.load(sourceFileName, loadOptions);
```

## Krok 2: Přidejte efekt překrytí barev

V tomto kroku přidáme efekt barevného překrytí do určité vrstvy obrázku PSD.

```java
ColorOverlayEffect effect = im.getLayers()[1].getBlendingOptions().addColorOverlay();
effect.setColor(Color.getGreen());
effect.setOpacity((byte)128);
effect.setBlendMode(BlendMode.Normal);
```

## Krok 3: Uložte upravený obrázek

Nakonec upravený obrázek s aplikovanými efekty uložte do nového souboru.

```java
im.save(exportPath);
```

Gratulujeme! Úspěšně jste přidali efekty za běhu pomocí Aspose.PSD for Java.

## Závěr

Aspose.PSD for Java zjednodušuje proces přidávání dynamických efektů do vašich obrázků a poskytuje vám výkonnou sadu nástrojů pro manipulaci s obrázky. Sledováním tohoto výukového programu jste získali přehled o aplikaci efektů překrytí barev za běhu, čímž zvýšíte vizuální přitažlivost vašich obrázků.

## FAQ

### Q1: Mohu použít více efektů na jednu vrstvu?

Odpověď 1: Ano, můžete použít více efektů na jednu vrstvu pomocí příslušných metod poskytovaných Aspose.PSD pro Java.

### Q2: Je Aspose.PSD kompatibilní s různými formáty obrázků?

Odpověď 2: Ano, Aspose.PSD podporuje širokou škálu obrazových formátů, včetně PSD, BMP, JPEG, PNG a dalších.

### Q3: Jak mohu získat dočasnou licenci pro Aspose.PSD pro Java?

 A3: Můžete získat dočasnou licenci od[tady](https://purchase.aspose.com/temporary-license/).

### Q4: Kde mohu požádat o pomoc s jakýmikoli problémy nebo dotazy souvisejícími s Aspose.PSD?

 A4: Navštivte Aspose.PSD[Fórum podpory](https://forum.aspose.com/c/psd/34) získat pomoc a spojit se s komunitou.

### Q5: Je k dispozici bezplatná zkušební verze pro Aspose.PSD pro Java?

 A5: Ano, můžete prozkoumat bezplatnou zkušební verzi[tady](https://releases.aspose.com/).