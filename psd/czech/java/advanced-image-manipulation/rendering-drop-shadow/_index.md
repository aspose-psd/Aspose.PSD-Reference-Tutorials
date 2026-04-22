---
date: 2026-02-07
description: Naučte se, jak uložit PSD jako PNG, exportovat PNG s alfa kanálem a přidat
  vrstvu stínu pomocí Aspose.PSD pro Javu – kompletní průvodce krok po kroku.
linktitle: Apply Rendering Drop Shadow
second_title: Aspose.PSD Java API
title: Uložte PSD jako PNG a aplikujte vykreslovací vržený stín v Aspose.PSD pro Javu
url: /cs/java/advanced-image-manipulation/rendering-drop-shadow/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Uložení PSD jako PNG a aplikace stínování při vykreslování v Aspose.PSD pro Java

## Úvod

Pokud pracujete s Photoshop soubory v Javě, **uložení PSD jako PNG** je jedním z nejčastějších úkolů, na které narazíte. S Aspose.PSD můžete nejen **převést PSD na PNG**, ale také vylepšit obrázek **přidáním vrstvy stínování**. V tomto tutoriálu projdeme celý proces – načtení PSD, aplikaci stínování při vykreslování a nakonec **uložení PSD jako PNG** souboru – takže můžete tento workflow s jistotou začlenit do svých projektů.

## Rychlé odpovědi
- **Která knihovna provádí konverzi PSD na PNG?** Aspose.PSD pro Java.  
- **Jak dlouho trvá implementace stínování?** Přibližně 10‑15 minut pro základní příklad.  
- **Potřebuji licenci pro spuštění kódu?** Bezplatná zkušební verze stačí pro hodnocení; licence je vyžadována pro produkci.  
- **Mohu aplikovat stín na více vrstev?** Ano – stačí projít požadované vrstvy ve smyčce.  
- **Jaká verze Javy je vyžadována?** Java 8 nebo vyšší.

## Co je „uložit PSD jako PNG“ a proč je to důležité?

Uložení PSD jako PNG vytvoří široce podporovaný, bezztrátový obrázek, který zachovává průhlednost. To je nezbytné, když potřebujete zobrazit Photoshop aktiva na webu, v mobilních aplikacích nebo jako součást většího pipeline pro zpracování obrázků. Přidání stínu zároveň umožní vytvořit vylepšený vizuální efekt bez otevření Photoshopu.

## Proč použít Aspose.PSD pro tento workflow?

* **Plná kontrola z kódu** – Není nutné spouštět Photoshop ani spoléhat na externí nástroje.  
* **Zachovává efekty vrstev** – Stíny, záře a další efekty jsou vykresleny přesně tak, jak se objevují v původním souboru.  
* **Export PNG s alfou** – Výstupní PNG si ponechává průhledné pozadí, takže je připravené pro web nebo UI.  
* **Cross‑platform** – Funguje na jakémkoli OS, který podporuje Java 8+.

## Předpoklady

Než se pustíme do práce, ujistěte se, že máte:

- **Vývojové prostředí Javy** – nainstalovaný JDK 8 nebo novější.  
- **Aspose.PSD pro Java** – stáhněte nejnovější JAR ze [stránky ke stažení Aspose.PSD](https://releases.aspose.com/psd/java/).  
- **Soubor PSD** – Soubor by měl obsahovat alespoň jednu vrstvu, kterou chcete vylepšit stínem (např. *Shadow.psd*).  

## Import balíčků

Nejprve importujte třídy, které budeme potřebovat. To nám poskytne přístup k načítání obrázků, efektům vrstev a možnostem exportu PNG.

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
Uveďte programu, kde se nachází váš zdrojový PSD.

```java
String dataDir = "Your Document Directory";
```

### Krok 2: Nastavte cesty k souborům PSD a PNG  
Zadejte jak vstupní PSD, tak výstupní PNG, který bude obsahovat vykreslený stín.

```java
String sourceFileName = dataDir + "Shadow.psd";
String pngExportPath = dataDir + "Shadowchanged1.png";
```

### Krok 3: Načtěte soubor PSD s efekty  
Povolte načítání zdrojů efektů, abychom mohli manipulovat se stínovým efektem.

```java
PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);

PsdImage im = (PsdImage) Image.load(sourceFileName, loadOptions);
```

### Krok 4: Přístup k efektu Drop Shadow  
Získejte první efekt stínu z druhé vrstvy (index 1). Zde ověříte nebo upravíte parametry.

```java
DropShadowEffect shadowEffect = (DropShadowEffect) (im.getLayers()[1].getBlendingOptions().getEffects()[0]);
```

### Krok 5: Ověřte vlastnosti efektu stínu  
Ujistěte se, že vlastnosti efektu odpovídají vašim očekáváním před uložením. Můžete také doladit tyto hodnoty pro jiný vzhled.

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

> **Pro tip:** Upravit `setSpread()` nebo `setNoise()` pro vytvoření měkčích nebo texturovanějších stínů.

### Krok 6: Uložení jako PNG – krok „uložit PSD jako PNG“  
Exportujte upravený obrázek do PNG, zachovávajíc alfa kanál, aby se stín správně sloučil.

```java
PngOptions saveOptions = new PngOptions();
saveOptions.setColorType(PngColorType.TruecolorWithAlpha);
im.save(pngExportPath, saveOptions);
```

V tomto okamžiku jste úspěšně **převáděli PSD na PNG**, **exportovali PNG s alfou** a aplikovali rendering stín v jednom workflow.

## Export PNG s alfa průhledností

Když potřebujete, aby výstupní PNG zachoval průhledné pozadí – zejména pro UI překrytí nebo webovou grafiku – použijte `PngColorType.TruecolorWithAlpha`, jak je ukázáno v kroku uložení výše. Tím zajistíte, že stín bude ležet na průhledném plátně místo na pevném pozadí.

## Přidání vrstvy Drop Shadow pomocí Javy

Pokud váš PSD obsahuje více vrstev, které vyžadují stíny, jednoduše opakujte **Krok 4** a **Krok 5** uvnitř smyčky, která iteruje přes `im.getLayers()`. Každá iterace může vytvořit nebo upravit instanci `DropShadowEffect`, čímž získáte detailní kontrolu nad neprůhledností, vzdáleností, velikostí a úhlem pro každou vrstvu.

## Java Convert Photoshop PNG – běžné scénáře použití

* **Webové asset pipeline** – Převádějte PSD poskytnuté designéry na web‑připravené PNG s vestavěnými stíny.  
* **Zdroje pro mobilní aplikace** – Generujte průhledné PNG ikony za běhu, čímž se vyhnete ručnímu exportu.  
* **Dávkové zpracování** – Automatizujte konverzi stovek PSD souborů v server‑side úloze.

## Časté problémy a řešení

| Problém | Pravděpodobná příčina | Řešení |
|-------|--------------|-----|
| **Stín není viditelný** | `Opacity` nastaveno na 0 nebo vrstva je skrytá | Ověřte, že `shadowEffect.getOpacity()` > 0 a vrstva je viditelná. |
| **PNG vypadá plochý (bez průhlednosti)** | Použita špatná hodnota `PngColorType` | Použijte `PngColorType.TruecolorWithAlpha` jak je ukázáno. |
| **Výjimka při načítání** | Efekty nebyly načteny | Ujistěte se, že je voláno `loadOptions.setLoadEffectsResource(true)`. |
| **Nesprávný index vrstvy** | Struktura PSD se liší | Prozkoumejte `im.getLayers()` a vyberte správný index. |

## Často kladené otázky

**Q: Mohu aplikovat stíny na více vrstev najednou?**  
A: Ano. Projděte `im.getLayers()` a přidejte nebo upravte `DropShadowEffect` pro každou cílovou vrstvu.

**Q: Co řídí parametr „Spread“?**  
A: `Spread` určuje, jak rychle stín přechází z plné neprůhlednosti na průhlednost. Vyšší hodnota vytváří tvrdší okraj.

**Q: Je Aspose.PSD kompatibilní se všemi verzemi Photoshopu?**  
A: Aspose.PSD podporuje PSD soubory od Photoshop 3.0 až po nejnovější verzi, a zvládá většinu typů vrstev a efektů.

**Q: Jak mohu kód otestovat před zakoupením licence?**  
A: Stáhněte si bezplatnou zkušební verzi ze [stránky ke stažení Aspose.PSD](https://releases.aspose.com/psd/java/) a spusťte ukázku bez licenčního klíče.

**Q: Kde mohu získat pomoc, pokud narazím na problémy?**  
A: Položte svůj dotaz na [fóru Aspose.PSD](https://forum.aspose.com/c/psd/34), kde vám pomohou komunita i inženýři Aspose.

## Závěr

Nyní víte, jak **uložit PSD jako PNG**, **exportovat PNG s alfou**, **převádět Photoshop PNG** soubory a **přidat vrstvu stínování** pomocí Aspose.PSD pro Java. Tato kombinace vám umožní automatizovat přípravu vysoce kvalitních obrázků pro web, mobil nebo desktopové aplikace – a to bez nutnosti otevírat Photoshop.

---

**Poslední aktualizace:** 2026-02-07  
**Testováno s:** Aspose.PSD 24.11 pro Java  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}