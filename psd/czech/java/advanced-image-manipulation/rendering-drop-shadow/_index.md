---
date: 2026-04-22
description: Naučte se, jak uložit PSD jako PNG, exportovat PNG s alfa kanálem a přidat
  vrstvu vrženého stínu pomocí Aspose.PSD pro Javu – kompletní, krok za krokem průvodce.
keywords:
- save psd as png
- convert psd to png
- export png with alpha
- batch psd to png
- preserve png transparency
linktitle: Použít stín při vykreslování
second_title: Aspose.PSD Java API
title: Uložte PSD jako PNG a použijte vykreslovací stín v Aspose.PSD pro Javu
url: /cs/java/advanced-image-manipulation/rendering-drop-shadow/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Uložení PSD jako PNG a aplikace vykreslovacího vrženého stínu v Aspose.PSD pro Java

## Úvod

Pokud pracujete s Photoshop soubory v Javě, **uložení PSD jako PNG** je jedním z nejčastějších úkolů, na které narazíte. V mnoha projektech budete potřebovat **uložit psd jako png**, abyste mohli nasadit assety na web nebo do mobilních aplikací, a přitom zachovat průhlednost a vizuální efekty. S Aspose.PSD můžete nejen **převést PSD na PNG**, ale také vylepšit obrázek **přidáním vrstvy vrženého stínu**. V tomto tutoriálu projdeme celý proces – načtení PSD, aplikaci vykreslovacího vrženého stínu a nakonec **uložení PSD jako PNG** souboru – takže můžete tento workflow s jistotou začlenit do svých projektů.

## Rychlé odpovědi
- **Jaká knihovna provádí konverzi PSD na PNG?** Aspose.PSD pro Java.  
- **Jak dlouho trvá implementace vrženého stínu?** Přibližně 10‑15 minut pro základní příklad.  
- **Potřebuji licenci pro spuštění kódu?** Pro hodnocení stačí bezplatná zkušební verze; licence je vyžadována pro produkci.  
- **Mohu aplikovat stín na více vrstev?** Ano – stačí projít požadované vrstvy ve smyčce, což také umožňuje hromadnou konverzi psd na png.  
- **Jaká verze Javy je požadována?** Java 8 nebo vyšší.

## Co znamená „uložit PSD jako PNG“ a proč je to důležité?

**Uložení PSD jako PNG** vytváří široce podporovaný, bezztrátový obrázek, který zachovává průhlednost. To je nezbytné, když potřebujete zobrazit Photoshop assety na webu, v mobilních aplikacích nebo jako součást většího pipeline pro zpracování obrázků. Přidání vrženého stínu současně vám umožní vytvořit vylepšený vizuální efekt bez otevření Photoshopu.

## Proč použít Aspose.PSD pro tento workflow?

* **Plná kontrola z kódu** – Není nutné spouštět Photoshop ani se spoléhat na externí nástroje.  
* **Zachovává efekty vrstev** – Vržené stíny, záře a další efekty jsou vykresleny přesně tak, jak se objevují v originálním souboru.  
* **Export PNG s alfa kanálem** – Výstup PNG si uchovává průhledné pozadí, což zajišťuje **zachování průhlednosti PNG** pro UI nebo webové použití.  
* **Cross‑platform** – Funguje na jakémkoli OS, který podporuje Java 8+.

## Předpoklady

Než se pustíme dál, ujistěte se, že máte:

- **Java vývojové prostředí** – nainstalovaný JDK 8 nebo novější.  
- **Aspose.PSD pro Java** – stáhněte si nejnovější JAR ze [Stránky ke stažení Aspose.PSD](https://releases.aspose.com/psd/java/).  
- **PSD soubor** – Soubor by měl obsahovat alespoň jednu vrstvu, kterou chcete vylepšit vrženým stínem (např. *Shadow.psd*).  

## Import balíčků

Nejprve importujte třídy, které budeme potřebovat. Tím získáme přístup k načítání obrázků, efektům vrstev a možnostem exportu PNG.

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

### Krok 1: Definice adresáře dokumentu  
Určete programu, kde se nachází váš zdrojový PSD.

```java
String dataDir = "Your Document Directory";
```

### Krok 2: Nastavení cest k souborům PSD a PNG  
Zadejte jak vstupní PSD, tak výstupní PNG, který bude obsahovat vykreslený vržený stín.

```java
String sourceFileName = dataDir + "Shadow.psd";
String pngExportPath = dataDir + "Shadowchanged1.png";
```

### Krok 3: Načtení PSD souboru s efekty  
Povolte načítání zdrojů efektů, abychom mohli manipulovat s efektem vrženého stínu.

```java
PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);

PsdImage im = (PsdImage) Image.load(sourceFileName, loadOptions);
```

### Krok 4: Přístup k efektu vrženého stínu  
Získejte první efekt vrženého stínu ze druhé vrstvy (index 1). Zde ověříte nebo upravíte parametry.

```java
DropShadowEffect shadowEffect = (DropShadowEffect) (im.getLayers()[1].getBlendingOptions().getEffects()[0]);
```

### Krok 5: Ověření vlastností efektu stínu  
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

### Krok 6: Uložení jako PNG – krok „uložit PSD jako PNG“  
Exportujte upravený obrázek do PNG, přičemž zachováte alfa kanál, aby se stín správně sloučil.

```java
PngOptions saveOptions = new PngOptions();
saveOptions.setColorType(PngColorType.TruecolorWithAlpha);
im.save(pngExportPath, saveOptions);
```

V tomto okamžiku jste úspěšně **převáděli PSD na PNG**, **exportovali PNG s alfa kanálem** a aplikovali vykreslovací vržený stín v jednom workflow.

## Export PNG s alfa průhledností

Když potřebujete, aby výstupní PNG zachoval průhledné pozadí – zejména pro UI překrytí nebo webovou grafiku – ujistěte se, že používáte `PngColorType.TruecolorWithAlpha`, jak je ukázáno v kroku uložení výše. Tím zajistíte, že vržený stín leží na průhledném plátně místo pevného pozadí, což vám pomůže **zachovat průhlednost PNG**.

## Přidání vrstvy vrženého stínu pomocí Javy

Pokud váš PSD obsahuje více vrstev, které vyžadují stíny, jednoduše opakujte **Krok 4** a **Krok 5** uvnitř smyčky, která iteruje přes `im.getLayers()`. Každá iterace může vytvořit nebo upravit instanci `DropShadowEffect`, což vám dává detailní kontrolu nad neprůhledností, vzdáleností, velikostí a úhlem pro každou vrstvu. Tento přístup také umožňuje **hromadnou konverzi psd na png**, kde každý soubor získá stejnou úpravu stínu.

## Běžné případy použití pro uložení PSD jako PNG

* **Webové asset pipeline** – Převod PSD poskytnutých designéry na web‑ready PNG s vestavěnými stíny.  
* **Zdroje pro mobilní aplikace** – Generování průhledných PNG ikon za běhu, bez ručního exportu.  
* **Hromadné zpracování** – Automatizace konverze stovek PSD souborů v server‑side úloze, přičemž každý PNG si zachová alfa kanál a vizuální efekty.  

## Časté problémy a řešení

| Problém | Pravděpodobná příčina | Řešení |
|-------|--------------|-----|
| **Stín není viditelný** | `Opacity` nastaveno na 0 nebo je vrstva skrytá | Ověřte, že `shadowEffect.getOpacity()` > 0 a že vrstva je viditelná. |
| **PNG vypadá plochý (bez průhlednosti)** | Použit špatný `PngColorType` | Použijte `PngColorType.TruecolorWithAlpha`, jak je ukázáno. |
| **Výjimka při načítání** | Efekty nebyly načteny | Ujistěte se, že je zavoláno `loadOptions.setLoadEffectsResource(true)`. |
| **Špatný index vrstvy** | Struktura PSD se liší | Prozkoumejte `im.getLayers()` a vyberte správný index. |

## Často kladené otázky

**Q: Mohu aplikovat vržené stíny na více vrstev najednou?**  
A: Ano. Projděte `im.getLayers()` a přidejte nebo upravte `DropShadowEffect` pro každou cílovou vrstvu, což také umožňuje hromadnou konverzi psd na png.

**Q: Co řídí parametr „Spread“?**  
A: `Spread` určuje, jak rychle stín přechází z plné neprůhlednosti na průhlednost. Vyšší hodnota vytváří ostřejší okraj.

**Q: Je Aspose.PSD kompatibilní se všemi verzemi Photoshopu?**  
A: Aspose.PSD podporuje PSD soubory od Photoshop 3.0 až po nejnovější verzi, včetně většiny typů vrstev a efektů.

**Q: Jak mohu kód otestovat před zakoupením licence?**  
A: Stáhněte si bezplatnou zkušební verzi ze [Stránky ke stažení Aspose.PSD](https://releases.aspose.com/psd/java/) a spusťte ukázku bez licenčního klíče.

**Q: Kde mohu získat pomoc, pokud narazím na problémy?**  
A: Položte svůj dotaz na [forum Aspose.PSD](https://forum.aspose.com/c/psd/34), kde vám pomohou komunita i inženýři Aspose.

## Závěr

Nyní víte, jak **uložit psd jako png**, **exportovat PNG s alfa kanálem**, **převést PSD na PNG** a **přidat vrstvu vrženého stínu** pomocí Aspose.PSD pro Java. Tato kombinace vám umožní automatizovat přípravu vysoce kvalitních obrázků pro web, mobil nebo desktopové aplikace – a to bez nutnosti otevírat Photoshop.

---

**Poslední aktualizace:** 2026-04-22  
**Testováno s:** Aspose.PSD 24.11 pro Java  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}