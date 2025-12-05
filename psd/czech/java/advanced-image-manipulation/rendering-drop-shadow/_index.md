---
date: 2025-12-05
description: Naučte se, jak uložit PSD jako PNG, převést PSD na PNG a přidat vrstvu
  s vrženým stínem pomocí Aspose.PSD pro Javu – kompletní, krok za krokem průvodce.
language: cs
linktitle: Apply Rendering Drop Shadow
second_title: Aspose.PSD Java API
title: Uložte PSD jako PNG a aplikujte vykreslovací vržený stín v Aspose.PSD pro Javu
url: /java/advanced-image-manipulation/rendering-drop-shadow/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Uložení PSD jako PNG a aplikace vykreslovacího vrženého stínu v Aspose.PSD pro Java

## Úvod

Pokud pracujete s Photoshop soubory v Javě, **uložení PSD jako PNG** je jedním z nejčastějších úkolů, na které narazíte. S Aspose.PSD můžete nejen **převést PSD na PNG**, ale také vylepšit obrázek **přidáním vrstvy vrženého stínu**. V tomto tutoriálu projdeme celý proces – načtení PSD, aplikaci vykreslovacího vrženého stínu a nakonec **uložení PSD jako PNG** souboru – takže můžete tento workflow s jistotou integrovat do svých projektů.

## Rychlé odpovědi
- **Jaká knihovna provádí konverzi PSD na PNG?** Aspose.PSD for Java.  
- **Jak dlouho trvá implementace vrženého stínu?** Přibližně 10‑15 minut pro základní příklad.  
- **Potřebuji licenci pro spuštění kódu?** Bezplatná zkušební verze funguje pro hodnocení; licence je vyžadována pro produkci.  
- **Mohu aplikovat stín na více vrstev?** Ano – stačí projít požadované vrstvy ve smyčce.  
- **Jaká verze Javy je vyžadována?** Java 8 nebo vyšší.

## Co je „uložení PSD jako PNG“ a proč je to důležité?

Uložení PSD jako PNG vytváří široce podporovaný, bezztrátový obrázek, který zachovává průhlednost. To je nezbytné, když potřebujete zobrazit Photoshop aktiva na webu, v mobilních aplikacích nebo jako součást většího pipeline pro zpracování obrázků. Přidání vrženého stínu zároveň umožňuje vytvořit vylepšený vizuální efekt bez otevření Photoshopu.

## Předpoklady

Než se pustíme dál, ujistěte se, že máte:

- **Vývojové prostředí Java** – nainstalovaný JDK 8 nebo novější.  
- **Aspose.PSD for Java** – stáhněte nejnovější JAR ze [stránky ke stažení Aspose.PSD](https://releases.aspose.com/psd/java/).  
- **Soubor PSD** – soubor by měl obsahovat alespoň jednu vrstvu, kterou chcete vylepšit vrženým stínem (např. *Shadow.psd*).  

## Import balíčků

Nejprve importujte třídy, které budeme potřebovat. To nám poskytne přístup k načítání obrázků, efektům vrstev a možnostem exportu do PNG.

```java
import com.aspose.psd.Image;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.layereffects.DropShadowEffect;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
import com.aspose.psd.Color;

import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.imageoptions.PngOptions;
```

## Průvodce krok za krokem

### Krok 1: Definujte adresář dokumentu  
Řekněte programu, kde se nachází váš zdrojový PSD.

```java
String dataDir = "Your Document Directory";
```

### Krok 2: Nastavte cesty k souborům PSD a PNG  
Zadejte jak vstupní PSD, tak výstupní PNG, který bude obsahovat vykreslený vržený stín.

```java
String sourceFileName = dataDir + "Shadow.psd";
String pngExportPath = dataDir + "Shadowchanged1.png";
```

### Krok 3: Načtěte soubor PSD s efekty  
Povolte načítání zdrojů efektů, abychom mohli manipulovat s efektem vrženého stínu.

```java
PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);

PsdImage im = (PsdImage) Image.load(sourceFileName, loadOptions);
```

### Krok 4: Přístup k efektu vrženého stínu  
Získejte první efekt vrženého stínu ze druhé vrstvy (index 1). Zde ověříme nebo upravíme parametry.

```java
DropShadowEffect shadowEffect = (DropShadowEffect) (im.getLayers()[1].getBlendingOptions().getEffects()[0]);
```

### Krok 5: Ověřte vlastnosti efektu stínu  
Ujistěte se, že vlastnosti efektu odpovídají vašim očekáváním před uložením. Můžete také doladit tyto hodnoty pro dosažení jiného vzhledu.

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

> **Tip:** Upravit `setSpread()` nebo `setNoise()` pro vytvoření měkčích nebo texturovanějších stínů.

### Krok 6: Uložení jako PNG – krok „uložení PSD jako PNG“  
Exportujte upravený obrázek do PNG, přičemž zachováte alfa kanál, aby se stín správně sloučil.

```java
PngOptions saveOptions = new PngOptions();
saveOptions.setColorType(PngColorType.TruecolorWithAlpha);
im.save(pngExportPath, saveOptions);
```

V tomto okamžiku jste úspěšně **převáděli PSD na PNG** a aplikovali vykreslovací vržený stín v jednom workflow.

## Časté problémy a řešení

| Problém | Pravděpodobná příčina | Řešení |
|---------|-----------------------|--------|
| **Stín není viditelný** | `Opacity` nastaveno na 0 nebo vrstva je skrytá | Ověřte, že `shadowEffect.getOpacity()` > 0 a vrstva je viditelná. |
| **PNG vypadá plochý (žádná průhlednost)** | Použit nesprávný `PngColorType` | Použijte `PngColorType.TruecolorWithAlpha` jak je uvedeno. |
| **Výjimka při načítání** | Efekty nebyly načteny | Ujistěte se, že je zavoláno `loadOptions.setLoadEffectsResource(true)`. |
| **Nesprávný index vrstvy** | Struktura PSD se liší | Prozkoumejte `im.getLayers()` a vyberte správný index. |

## Často kladené otázky

**Q: Mohu aplikovat vržené stíny na více vrstev současně?**  
A: Ano. Projděte `im.getLayers()` a přidejte nebo upravte `DropShadowEffect` pro každou cílovou vrstvu.

**Q: Co řídí parametr „Spread“?**  
A: `Spread` určuje, jak rychle stín přechází z plné neprůhlednosti na průhlednost. Vyšší hodnota vytváří ostřejší okraj.

**Q: Je Aspose.PSD kompatibilní se všemi verzemi Photoshopu?**  
A: Aspose.PSD podporuje PSD soubory od Photoshop 3.0 až po nejnovější verzi, přičemž zpracovává většinu typů vrstev a efektů.

**Q: Jak mohu otestovat kód před zakoupením licence?**  
A: Stáhněte bezplatnou zkušební verzi ze [stránky ke stažení Aspose.PSD](https://releases.aspose.com/psd/java/) a spusťte ukázku bez licenčního klíče.

**Q: Kde mohu získat pomoc, pokud narazím na problémy?**  
A: Zveřejněte svůj dotaz na [fóru Aspose.PSD](https://forum.aspose.com/c/psd/34), kde vám může pomoci komunita i inženýři Aspose.

## Závěr

Nyní víte, jak **uložit PSD jako PNG**, **převést PSD na PNG** a **přidat vrstvu vrženého stínu** pomocí Aspose.PSD pro Java. Tato kombinace vám umožní automatizovat přípravu vysoce kvalitních obrázků pro web, mobil nebo desktopové aplikace – a to bez nutnosti otevírat Photoshop.

---

**Poslední aktualizace:** 2025-12-05  
**Testováno s:** Aspose.PSD 24.11 for Java  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}