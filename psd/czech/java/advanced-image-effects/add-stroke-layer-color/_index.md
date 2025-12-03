---
date: 2025-11-30
description: Naučte se, jak přidat obrys a změnit barvu obrysu v souboru PSD pomocí
  Aspose.PSD pro Javu. Postupujte podle tohoto krok‑za‑krokem průvodce a upravte barvu
  a průhlednost vrstvy obrysu.
language: cs
linktitle: Add Stroke Layer Color
second_title: Aspose.PSD Java API
title: Jak přidat barvu obrysu vrstvy v Aspose.PSD pro Javu
url: /java/advanced-image-effects/add-stroke-layer-color/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Jak přidat barvu vrstvy obrysu v Aspose.PSD pro Java

## Úvod

Pokud potřebujete **jak přidat obrys** do dokumentu Photoshopu programově, Aspose.PSD pro Java to usnadňuje. V tomto tutoriálu vás provedeme přidáním barvy vrstvy obrysu, úpravou její průhlednosti a uložením výsledku. Na konci také uvidíte, jak **změnit barvu obrysu** (nebo *změnit barvu obrysu PSD*) pro libovolnou existující vrstvu, což vám poskytne plnou kreativní kontrolu z vašeho Java kódu.

## Rychlé odpovědi
- **Jaká knihovna je vyžadována?** Aspose.PSD pro Java (nejnovější verze).  
- **Mohu změnit barvu obrysu?** Ano – použijte `ColorFillSettings` k nastavení libovolné `Color`.  
- **Potřebuji licenci?** Dočasná licence stačí pro hodnocení; plná licence je vyžadována pro produkci.  
- **Která verze Javy je podporována?** Java 8 nebo vyšší.  
- **Jak dlouho trvá implementace?** Obvykle méně než 10 minut pro základní změnu obrysu.

## Co je vrstva obrysu v PSD?
Vrstva obrysu je vektorový efekt, který kreslí obrys kolem obsahu vrstvy. Lze ji přizpůsobit barvou, tloušťkou, průhledností a režimem prolnutí. Programová úprava tohoto efektu umožňuje automatizované značkování, dávkové zpracování nebo generování dynamické grafiky.

## Proč použít Aspose.PSD ke změně barvy obrysu?
- **Není potřeba Photoshop** – pracujte zcela v Javě.  
- **Plná shoda se specifikací PSD** – jsou podporovány všechny moderní funkce PSD.  
- **Vysoký výkon** – rychle zpracovávejte velké soubory.  
- **Cross‑platform** – běží na jakémkoli OS s JVM.

## Prerequisites

- **Knihovna Aspose.PSD** – stáhněte z [oficiální dokumentace](https://reference.aspose.com/psd/java/).  
- **Java Development Kit (JDK)** – verze 8 nebo novější.  
- **IDE** – Eclipse, IntelliJ IDEA nebo jakýkoli editor kompatibilní s Javou.

## Import balíčků

Nejprve importujte třídy, které budete potřebovat. To vašemu projektu poskytne přístup k API pro práci s PSD a efektem obrysu.

```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;


import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.BlendMode;
import com.aspose.psd.fileformats.psd.layers.fillsettings.ColorFillSettings;
import com.aspose.psd.fileformats.psd.layers.fillsettings.FillType;
import com.aspose.psd.fileformats.psd.layers.layereffects.StrokeEffect;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
```

## Krok 1: Nastavte svůj projekt

Vytvořte nový Java projekt, přidejte JAR Aspose.PSD do cesty sestavení a ověřte, že se knihovna načte bez chyb.

## Krok 2: Načtěte soubor PSD

Povolte načítání zdrojů efektů, aby byly k dispozici informace o obrysu.

```java
String dataDir = "Your Document Directory";

String sourceFileName = dataDir + "Stroke.psd";
String exportPath = dataDir + "StrokeGradientChanged.psd";

PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);

PsdImage im = (PsdImage)Image.load(sourceFileName, loadOptions);
```

## Krok 3: Přístup k vrstvě efektu obrysu

Získejte první efekt obrysu ze druhé vrstvy (index 1).

```java
StrokeEffect colorStroke = (StrokeEffect)im.getLayers()[1].getBlendingOptions().getEffects()[0];
```

## Krok 4: Ověřte vlastnosti obrysu

Potvrďte existující vlastnosti před provedením změn. To pomáhá předejít neočekávaným výsledkům.

```java
Assert.areEqual(BlendMode.Normal, colorStroke.getBlendMode());
Assert.areEqual(255, colorStroke.getOpacity());
Assert.areEqual(true, colorStroke.isVisible());
```

## Krok 5: Nastavte barvu a průhlednost (Jak změnit barvu obrysu)

Zde **měníme barvu obrysu PSD** na žlutou a snižujeme průhlednost na 50 % (127 / 255).

```java
ColorFillSettings fillSettings = (ColorFillSettings)colorStroke.getFillSettings();
fillSettings.setColor(Color.getYellow());

colorStroke.setOpacity((byte)127);
```

## Krok 6: Uložte upravený PSD

Zapište aktualizovaný obrázek zpět na disk. Nový soubor nyní obsahuje upravený obrys.

```java
im.save(exportPath);
```

## Časté úskalí a tipy

- **Kontroly null** – vždy ověřte, že `getEffects()` vrací pole nenulové před přetypováním.  
- **Index vrstvy** – vrstvy PSD jsou číslovány od nuly; ujistěte se, že cílíte na správnou vrstvu.  
- **Formát barvy** – `Color.getYellow()` je jen příklad; můžete vytvořit vlastní barvy pomocí `new Color(r, g, b)`.  
- **Rozsah průhlednosti** – průhlednost je byte (0–255); hodnoty nad 255 budou oříznuty.

## Závěr

Nyní jste se naučili **jak přidat obrys** do souboru PSD a **jak změnit barvu obrysu** pomocí Aspose.PSD pro Java. Experimentujte s různými barvami, režimy prolnutí a průhlednostmi, abyste dosáhli přesně požadovaného vizuálního stylu vašeho projektu.

## Často kladené otázky

**Q: Mohu použít Aspose.PSD s jinými Java grafickými knihovnami?**  
A: Ano, Aspose.PSD lze kombinovat s knihovnami jako Apache Commons Imaging nebo Java2D pro rozšířenou funkčnost.

**Q: Je Aspose.PSD kompatibilní s nejnovějším formátem souboru PSD?**  
A: Rozhodně. Knihovna je pravidelně aktualizována, aby podporovala nejnovější specifikace Photoshopu.

**Q: Jak zacházet s výjimkami při používání Aspose.PSD?**  
A: Podívejte se na [support forum](https://forum.aspose.com/c/psd/34) pro podrobné řešení problémů a ukázkový kód pro zpracování chyb.

**Q: Můžu vyzkoušet Aspose.PSD před zakoupením?**  
A: Samozřejmě! Získejte [free trial](https://releases.aspose.com/) a prozkoumejte všechny funkce.

**Q: Kde mohu získat dočasnou licenci pro Aspose.PSD?**  
A: Získejte [temporary license](https://purchase.aspose.com/temporary-license/) pro vyhodnocení knihovny ve vašem vývojovém prostředí.

---

**Poslední aktualizace:** 2025-11-30  
**Testováno s:** Aspose.PSD 24.11 pro Java  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
