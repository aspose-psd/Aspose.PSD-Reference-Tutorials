---
date: 2026-04-03
description: Naučte se, jak uložit PSD jako PNG s efektem obrysu a vyplněním barvou
  pomocí Aspose.PSD pro Javu. Tento průvodce krok za krokem ukazuje, jak rychle exportovat
  PSD do PNG.
keywords:
- save psd as png
- export psd to png
- set stroke color
- apply layer effects
- customize stroke width
linktitle: Uložit PSD jako PNG s efektem obrysu – Java
second_title: Aspose.PSD Java API
title: Uložit PSD jako PNG s efektem obrysu – Java
url: /cs/java/psd-layer-management-effects/apply-stroke-effect-color-fill-psd/
weight: 21
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Uložit PSD jako PNG s efektem obrysu a výplní barvou – Java

## Úvod

V tomto průvodci se naučíte, jak **uložit PSD jako PNG** a přitom aplikovat efekt obrysu s výplní barvou pomocí Aspose.PSD pro Java. Ať už jste zkušený vývojář nebo teprve začínáte, tento krok‑za‑krokem tutoriál vám usnadní práci. Probereme vše od nastavení prostředí až po export finálního obrázku, takže rychle **exportujete PSD do PNG** ve svých projektech.

## Rychlé odpovědi
- **Co tento tutoriál dosahuje?** Ukazuje, jak uložit soubor PSD jako PNG po aplikaci přizpůsobitelného efektu obrysu.  
- **Která knihovna je použita?** Aspose.PSD for Java.  
- **Potřebuji licenci?** Bezplatná zkušební verze funguje pro testování; licence je vyžadována pro produkci.  
- **Mohu změnit barvu obrysu?** Ano – můžete nastavit libovolnou barvu pomocí `ColorFillSettings`.  
- **Je možné hromadné zpracování?** Rozhodně – obalte kód smyčkou pro zpracování více souborů PSD.

## Co znamená „uložit PSD jako PNG“?
Uložení PSD jako PNG znamená převod nativního vrstveného souboru Photoshopu do plochého, web‑přátelského formátu obrázku při zachování vizuální věrnosti. To je užitečné, když potřebujete zobrazit obsah PSD na webových stránkách, mobilních aplikacích nebo na jakékoli platformě, která přímo nepodporuje soubory PSD.

## Proč aplikovat efekt obrysu s výplní barvou?
Obrys přidává ostrý kontur kolem obsahu vrstvy, což pomáhá grafice vyniknout na složitých pozadích. Kombinace s vlastní výplní barvou vám umožní značkovat obrázky, zvýraznit UI prvky nebo vytvořit poutavé náhledy bez nutnosti opustit Photoshop.

## Požadavky

1. **Java Development Kit (JDK) 8+** – ujistěte se, že `java` je ve vaší PATH.  
2. **Aspose.PSD for Java** – stáhněte z [webu](https://releases.aspose.com/psd/java/).  
3. **IDE** – IntelliJ IDEA, Eclipse nebo jakýkoli editor, který preferujete.  
4. **Ukázkový PSD** – soubor, který již obsahuje efekt obrysu (nebo jej přidejte ve Photoshopu).  
5. **Základní znalost Javy** – napíšete několik řádků kódu, ale nic pokročilého.

Jakmile budete mít vše připravené, můžeme začít kódovat.

## Import balíčků

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

Tyto importy přinášejí všechny třídy potřebné k načtení PSD, úpravě jeho obrysu a uložení výstupů PSD i PNG.

## Jak uložit PSD jako PNG s efektem obrysu

### Krok 1: Načíst soubor PSD

Nejprve odkažte na složku, která obsahuje váš zdrojový PSD.

```java
String dataDir = "Your Document Directory";
```

Nahraďte `"Your Document Directory"` skutečnou cestou ve vašem počítači.

Nyní načtěte soubor při zachování všech existujících zdrojů efektů:

```java
String sourceFileName = dataDir + "StrokeComplex.psd";

PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);

PsdImage im = (PsdImage) Image.load(sourceFileName, loadOptions);
```

### Krok 2: Nastavit barvu obrysu (a volitelně upravit šířku)

Smyčka níže prochází každou vrstvu, získá první `StrokeEffect` a změní jeho barvu výplně. Můžete také upravit `setWidth` nebo `setPosition` na objektu `StrokeEffect`, pokud potřebujete **upravit šířku obrysu**.

```java
for (int i = 0; i < im.getLayers().length; i++) {
    StrokeEffect effect = (StrokeEffect) im.getLayers()[i].getBlendingOptions().getEffects()[0];
    ColorFillSettings settings = (ColorFillSettings) effect.getFillSettings();
    // Set the stroke color – change to any Color you like
    settings.setColor(Color.getDeepPink());
}
```

> **Tip:** `Color.getDeepPink()` je jen příklad. Použijte `new Color(r, g, b)` pro vlastní RGB hodnoty.

### Krok 3: Uložit upravený PSD (volitelné)

Pokud chcete zachovat verzi PSD s aktualizovaným obrysem, uložte ji takto:

```java
String exportPath = dataDir + "StrokeComplexRendering.psd";
im.save(exportPath, new PsdOptions());
```

### Krok 4: Exportovat obrázek jako PNG (hlavní krok „uložit PSD jako PNG“)

Nakonec převedete upravený PSD na soubor PNG připravený pro web:

```java
String exportPathPng = dataDir + "StrokeComplexRendering.png";
PngOptions option = new PngOptions();
option.setColorType(PngColorType.TruecolorWithAlpha);

im.save(exportPathPng, option);
```

PNG si zachová nastavený růžový obrys a volba `TruecolorWithAlpha` zajistí zachování průhlednosti.

## Časté problémy a řešení

| Problém | Důvod | Řešení |
|---------|-------|--------|
| **`ArrayIndexOutOfBoundsException`** | Vrstva nemá žádné efekty nebo první efekt není `StrokeEffect`. | Ověřte, že vrstva skutečně obsahuje obrys, nebo iterujte přes `getEffects()` a najděte správný typ. |
| **Barva se nemění** | Možná upravujete kopii nastavení místo originálu. | Ujistěte se, že přímo přetypujete na `ColorFillSettings` z `effect.getFillSettings()`. |
| **PNG je prázdný** | PSD byl načten bez rasterizace vrstvy. | Zavolejte `im.save(..., new PngOptions())` po všech úpravách; vyhněte se ukládání původního `im` před změnami. |

## Často kladené otázky

**Q: Mohu aplikovat více efektů na jednu vrstvu pomocí Aspose.PSD for Java?**  
A: Ano, můžete přistupovat k možnostem míchání vrstvy a přidávat tolik efektů, kolik potřebujete, včetně stínů, září a obrysů.

**Q: Je možné automatizovat proces pro dávku souborů PSD?**  
A: Rozhodně. Obalte načítání, aplikaci efektů a ukládání logiku do smyčky `for‑each`, která prochází soubory ve složce.

**Q: Jak mohu vrátit změny provedené v souboru PSD?**  
A: Znovu načtěte původní soubor před uložením jakýchkoli úprav; Aspose.PSD neposkytuje zásobník pro vrácení změn.

**Q: Mohu upravit šířku a umístění obrysu?**  
A: Ano. Použijte `effect.setWidth(float)` a `effect.setPosition(StrokeEffect.Position)` k nastavení tloušťky a umístění (uvnitř, vně nebo uprostřed).

**Q: Je knihovna Aspose.PSD for Java zdarma k použití?**  
A: Bezplatná zkušební verze je k dispozici pro vyhodnocení. Plná funkčnost vyžaduje zakoupenou licenci. Viz [buy options](https://purchase.aspose.com/buy) pro podrobnosti.

**Poslední aktualizace:** 2026-04-03  
**Testováno s:** Aspose.PSD 24.12 for Java  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}