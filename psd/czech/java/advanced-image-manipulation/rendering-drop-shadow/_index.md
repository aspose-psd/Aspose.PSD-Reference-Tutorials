---
date: 2026-11-04
description: Zjistěte, jak uložit PSD jako PNG, exportovat PNG s alfa kanálem a přidat
  vrstvu vrženého stínu pomocí Aspose.PSD for Java – kompletní, krok za krokem průvodce.
keywords:
- save psd as png
- convert psd to png
- export png with alpha
- batch psd to png
- java image manipulation
lastmod: 2026-11-04
linktitle: Použít rendering drop shadow
og_description: Uložte PSD jako PNG pomocí Aspose.PSD for Java, exportujte PNG s alfa
  průhledností a přidejte rendering drop shadow — průvodce krok za krokem pro vývojáře
  Java.
og_image_alt: Developer guide showing how to convert PSD to PNG and apply drop shadow
  using Aspose.PSD Java
og_title: Uložte PSD jako PNG a použijte rendering drop shadow v Aspose.PSD for Java
schemas:
- author: Aspose
  dateModified: '2026-11-04'
  description: Learn how to save PSD as PNG, export PNG with alpha, and add a drop
    shadow layer using Aspose.PSD for Java – a complete, step‑by‑step guide.
  headline: Save psd as png and apply rendering drop shadow in Aspose.PSD for Java
  type: TechArticle
- description: Learn how to save PSD as PNG, export PNG with alpha, and add a drop
    shadow layer using Aspose.PSD for Java – a complete, step‑by‑step guide.
  name: Save psd as png and apply rendering drop shadow in Aspose.PSD for Java
  steps:
  - name: define document directory
    text: Define the directory path where your PSD files are stored.
  - name: set psd and png file paths
    text: Specify the full file paths for the source PSD and the target PNG.
  - name: load psd file with effects
    text: '`PsdImage` loads the PSD and gives access to its layers and effects.'
  - name: access drop shadow effect
    text: '`DropShadowEffect` represents a drop‑shadow layer effect that can be read
      or modified.'
  - name: validate shadow effect properties
    text: '`shadowEffect` holds the properties of the drop‑shadow such as opacity,
      distance, and size. > **Pro tip:** Adjust `setSpread()` or `setNoise()` to create
      softer or more textured shadows.'
  - name: save as png – the “save psd as png” step
    text: '`PngOptions` configures PNG export settings, including color type and alpha
      channel handling. At this point you have successfully **converted psd to png**,
      **exported png with alpha**, and applied a rendering drop shadow in a single
      workflow.'
  type: HowTo
- questions:
  - answer: Yes. Loop through `im.getLayers()` and add or modify a `DropShadowEffect`
      for each target layer, which also lets you perform a batch psd to png conversion.
    question: Can I apply drop shadows to multiple layers simultaneously?
  - answer: '`Spread` determines how abruptly the shadow transitions from full opacity
      to transparent. A higher value creates a harder edge.'
    question: What does the ‘Spread’ parameter control?
  - answer: Aspose.PSD supports PSD files from Photoshop 3.0 up to the latest release,
      handling most layer types and effects.
    question: Is Aspose.PSD compatible with all Photoshop versions?
  - answer: Download the free trial from the [Aspose.PSD download page](https://releases.aspose.com/psd/java/)
      and run the sample without a license key.
    question: How can I test the code before purchasing a license?
  - answer: Post your question on the [Aspose.PSD forum](https://forum.aspose.com/c/psd/34)
      where the community and Aspose engineers can assist.
    question: Where can I get help if I run into problems?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- save psd as png
- aspose psd java
- java image manipulation
- png transparency
- rendering drop shadow
title: Uložte PSD jako PNG a použijte rendering drop shadow v Aspose.PSD for Java
url: /cs/java/advanced-image-manipulation/rendering-drop-shadow/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Uložte PSD jako PNG a použijte vykreslovací vržený stín v Aspose.PSD pro Java

## Úvod

Pokud pracujete s Photoshop soubory v Javě, **saving psd as png** je jedním z nejčastějších úkolů, na které narazíte. V mnoha projektech budete potřebovat **save psd as png**, abyste mohli distribuovat aktiva na web nebo mobilní aplikace, přičemž zachováte průhlednost a vizuální efekty. S Aspose.PSD můžete nejen **convert psd to png**, ale také vylepšit obrázek **adding a drop shadow layer**. V tomto tutoriálu projdeme celý proces – načtení PSD, aplikaci vykreslovacího vrženého stínu a nakonec **saving the PSD as a PNG** soubor – abyste mohli tento workflow s jistotou integrovat do svých projektů.

## Rychlé odpovědi
- **Která knihovna zpracovává konverzi PSD na PNG?** Aspose.PSD for Java.  
- **Jak dlouho trvá implementace vrženého stínu?** Přibližně 10‑15 minut pro základní příklad.  
- **Potřebuji licenci pro spuštění kódu?** Bezplatná zkušební verze funguje pro hodnocení; licence je vyžadována pro produkci.  
- **Mohu aplikovat stín na více vrstev?** Ano – stačí projít požadované vrstvy ve smyčce, což vám také umožní provést hromadnou konverzi psd na png.  
- **Která verze Javy je vyžadována?** Java 8 nebo vyšší.

## Co je „save psd as png“ a proč je to důležité?

**Saving a PSD as PNG creates a widely‑supported, lossless image that retains transparency.** Tento formát je nezbytný, když potřebujete zobrazit Photoshop aktiva na webu, v mobilních aplikacích nebo jako součást většího pipeline pro zpracování obrázků. Přidání vrženého stínu zároveň umožňuje vytvořit vylepšený vizuální efekt bez otevření Photoshopu.

## Proč použít Aspose.PSD pro tento workflow?

Vykreslování efektů vrstev během načítání je vestavěné, takže Photoshop nepotřebujete. Aspose.PSD podporuje více než 50 vstupních a výstupních formátů (PSD, PNG, JPEG, TIFF, BMP) a může zpracovávat velké dokumenty, aniž by načítal celý soubor do paměti. Zachovává efekty jako vržené stíny a záře přesně tak, jak se zobrazují, a automaticky exportuje PNG s alfa průhledností.

## Požadavky

- **Java Development Environment** – Nainstalovaný JDK 8 nebo novější.  
- **Aspose.PSD for Java** – Stáhněte nejnovější JAR ze [Aspose.PSD download page](https://releases.aspose.com/psd/java/).  
- **PSD soubor** – Soubor by měl obsahovat alespoň jednu vrstvu, kterou chcete vylepšit vrženým stínem (např. *Shadow.psd*).  

## Import balíčků

Namespace `com.aspose.psd` poskytuje základní třídy pro načítání obrázků, manipulaci s vrstvami a export PNG souborů. `PsdImage` je hlavní třída používaná k načtení a manipulaci s PSD soubory.  

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

### Krok 1: definujte adresář dokumentu
Definujte cestu k adresáři, kde jsou uloženy vaše PSD soubory.  

```java
String dataDir = "Your Document Directory";
```

### Krok 2: nastavte cesty k souborům psd a png
Zadejte úplné cesty k souborům pro zdrojový PSD a cílový PNG.  

```java
String sourceFileName = dataDir + "Shadow.psd";
String pngExportPath = dataDir + "Shadowchanged1.png";
```

### Krok 3: načtěte soubor psd s efekty
`PsdImage` načte PSD a poskytne přístup k jeho vrstvám a efektům.  

```java
PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);

PsdImage im = (PsdImage) Image.load(sourceFileName, loadOptions);
```

### Krok 4: přístup k efektu vrženého stínu
`DropShadowEffect` představuje efekt vrženého stínu vrstvy, který lze číst nebo upravovat.  

```java
DropShadowEffect shadowEffect = (DropShadowEffect) (im.getLayers()[1].getBlendingOptions().getEffects()[0]);
```

### Krok 5: ověřte vlastnosti efektu stínu
`shadowEffect` obsahuje vlastnosti vrženého stínu, jako jsou neprůhlednost, vzdálenost a velikost.  

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

> **Tip:** Upravte `setSpread()` nebo `setNoise()`, abyste vytvořili měkčí nebo texturovanější stíny.

### Krok 6: uložte jako png – krok „save psd as png“
`PngOptions` konfiguruje nastavení exportu PNG, včetně typu barvy a zpracování alfa kanálu.  

```java
PngOptions saveOptions = new PngOptions();
saveOptions.setColorType(PngColorType.TruecolorWithAlpha);
im.save(pngExportPath, saveOptions);
```

V tomto okamžiku jste úspěšně **converted psd to png**, **exported png with alpha**, a aplikovali vykreslovací vržený stín v jednom workflow.

## Export PNG s alfa průhledností

Když potřebujete, aby výstup PNG zachoval průhledné pozadí – zejména pro UI překrytí nebo webovou grafiku – ujistěte se, že používáte `PngColorType.TruecolorWithAlpha`, jak je ukázáno v kroku uložení výše. To zaručuje, že vržený stín leží na průhledném plátně místo pevného pozadí, což vám pomáhá **preserve png transparency**.

## Přidejte vrstvu vrženého stínu pomocí Java

Pokud váš PSD obsahuje více vrstev, které vyžadují stíny, jednoduše opakujte **Step 4** a **Step 5** uvnitř smyčky, která iteruje přes `im.getLayers()`. Každá iterace může vytvořit nebo upravit instanci `DropShadowEffect`, což vám poskytuje detailní kontrolu nad neprůhledností, vzdáleností, velikostí a úhlem pro každou vrstvu. Tento přístup také umožňuje **batch psd to png** konverzi, kde každý soubor získá stejnou úpravu stínu.

## Běžné případy použití pro ukládání psd jako png

* **Webové pipeline pro aktiva** – Převést PSD poskytnuté designérem na web‑připravené PNG s vestavěnými stíny.  
* **Zdroje pro mobilní aplikace** – Generovat průhledné PNG ikony za běhu, vyhnout se ručnímu exportu.  
* **Hromadné zpracování** – Automatizovat konverzi stovek PSD souborů na serveru, zajistit, aby každý PNG zachoval alfa kanál a vizuální efekty.  

## Běžné problémy a řešení

| Problém | Pravděpodobná příčina | Řešení |
|-------|--------------|-----|
| **Stín není viditelný** | `Opacity` nastaveno na 0 nebo je vrstva skrytá | Ověřte, že `shadowEffect.getOpacity()` > 0 a vrstva je viditelná. |
| **PNG vypadá plochý (žádná průhlednost)** | Použit špatný `PngColorType` | Použijte `PngColorType.TruecolorWithAlpha` jak je ukázáno. |
| **Výjimka při načítání** | Efekty nebyly načteny | Ujistěte se, že je zavoláno `loadOptions.setLoadEffectsResource(true)`. |
| **Nesprávný index vrstvy** | Struktura PSD se liší | Prozkoumejte `im.getLayers()` a vyberte správný index. |

## Často kladené otázky

**Q: Mohu aplikovat vržené stíny na více vrstev současně?**  
A: Ano. Projděte `im.getLayers()` ve smyčce a přidejte nebo upravte `DropShadowEffect` pro každou cílovou vrstvu, což vám také umožní provést hromadnou konverzi psd na png.

**Q: Co řídí parametr ‘Spread’?**  
A: `Spread` určuje, jak rychle stín přechází z plné neprůhlednosti na průhlednost. Vyšší hodnota vytváří tvrdší okraj.

**Q: Je Aspose.PSD kompatibilní se všemi verzemi Photoshopu?**  
A: Aspose.PSD podporuje PSD soubory od Photoshop 3.0 až po nejnovější vydání, zpracovává většinu typů vrstev a efektů.

**Q: Jak mohu otestovat kód před zakoupením licence?**  
A: Stáhněte si bezplatnou zkušební verzi ze [Aspose.PSD download page](https://releases.aspose.com/psd/java/) a spusťte ukázku bez licenčního klíče.

**Q: Kde mohu získat pomoc, pokud narazím na problémy?**  
A: Zveřejněte svůj dotaz na [Aspose.PSD forum](https://forum.aspose.com/c/psd/34), kde vám může pomoci komunita a inženýři Aspose.

## Závěr

Nyní víte, jak **save psd as png**, **export png with alpha**, **convert psd to png**, a **apply a drop shadow layer** pomocí Aspose.PSD pro Java. Tato kombinace vám umožní automatizovat přípravu vysoce kvalitních obrázků pro web, mobilní nebo desktopové aplikace – aniž byste kdy otevřeli Photoshop.

---

**Last Updated:** 2026-11-04  
**Tested With:** Aspose.PSD 24.11 for Java  
**Author:** Aspose

## Související tutoriály

- [Převod PSD na PNG s barevným překrytím – Aspose.PSD pro Java](/psd/java/advanced-image-manipulation/rendering-color-effect/)
- [Jak přidat stín v PSD pomocí Java – Pokročilé efekty vrstev](/psd/java/advanced-psd-layer-features-effects/)
- [Jak převést PSD na rastrové formáty obrázků s Aspose.PSD pro Java](/psd/java/advanced-techniques/convert-psd-to-raster-forms/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}