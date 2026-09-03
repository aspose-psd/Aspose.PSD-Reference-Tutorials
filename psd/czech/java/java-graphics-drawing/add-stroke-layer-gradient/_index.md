---
date: 2026-09-03
description: Naučte se, jak vytvořit gradientový tah v Java a přizpůsobit gradienty
  tahů v souborech PSD pomocí Aspose.PSD pro Java. Podrobný návod krok za krokem pro
  vývojáře.
keywords:
- create gradient stroke java
- add gradient stroke psd
- Aspose.PSD Java
- PSD gradient stroke
lastmod: 2026-09-03
linktitle: Jak vytvořit vrstvu gradientového tahu v Java
og_description: Vytvořte gradientový tah v Java pomocí Aspose.PSD pro Java během několika
  minut. Tento tutoriál vám ukáže, jak přidat a přizpůsobit gradientové tahy v souborech
  PSD, včetně ukázek kódu a osvědčených postupů.
og_image_alt: Screenshot of a PSD file showing a gradient stroke applied via Aspose.PSD
  Java API
og_title: Vytvoření gradientového tahu v Java – průvodce tutoriálem Aspose.PSD
schemas:
- author: Aspose
  dateModified: '2026-09-03'
  description: Learn how to create gradient stroke java and customize stroke gradients
    in PSD files using Aspose.PSD for Java. Step‑by‑step guide for developers.
  headline: Create gradient stroke java – Aspose.PSD tutorial guide
  type: TechArticle
- description: Learn how to create gradient stroke java and customize stroke gradients
    in PSD files using Aspose.PSD for Java. Step‑by‑step guide for developers.
  name: Create gradient stroke java – Aspose.PSD tutorial guide
  steps:
  - name: '**Java Development Kit (JDK)** – Install the latest JDK from [Oracle''s
      website](https://www.oracle.com/java/technologies/javase-downloads.html).'
    text: '**Java Development Kit (JDK)** – Install the latest JDK from [Oracle''s
      website](https://www.oracle.com/java/technologies/javase-downloads.html).'
  - name: '**Aspose.PSD for Java** – Download the library from the [Aspose.PSD download
      page](https://releases.aspose.com/psd/java/).'
    text: '**Aspose.PSD for Java** – Download the library from the [Aspose.PSD download
      page](https://releases.aspose.com/psd/java/).'
  - name: '**IDE** – IntelliJ IDEA, Eclipse, or NetBeans.'
    text: '**IDE** – IntelliJ IDEA, Eclipse, or NetBeans.'
  - name: '**License** – Obtain a [temporary license](https://purchase.aspose.com/temporary-license/)
      if you don’t have a full commercial license.'
    text: '**License** – Obtain a [temporary license](https://purchase.aspose.com/temporary-license/)
      if you don’t have a full commercial license.'
  type: HowTo
- questions:
  - answer: Aspose.PSD for Java is a pure‑Java library that lets developers create,
      edit, convert, and render Photoshop PSD files without requiring Adobe Photoshop.
    question: What is Aspose.PSD for Java?
  - answer: Yes, a valid license is required for production use. You can obtain a
      [temporary license](https://purchase.aspose.com/temporary-license/) for evaluation.
    question: Do I need a license to use Aspose.PSD for Java?
  - answer: Absolutely. Aspose.PSD provides APIs to build a new PSD document, add
      layers, apply effects, and save the file entirely programmatically.
    question: Can I create PSD files from scratch with this library?
  - answer: Yes, you can apply shadows, glows, bevels, and many other layer effects
      using the same effect‑based API.
    question: Is it possible to apply other effects besides gradient strokes?
  - answer: The official documentation is available in the [Aspose.PSD Java API reference](https://reference.aspose.com/psd/java/).
    question: Where can I find the full reference documentation?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- gradient stroke
- Aspose.PSD
- Java graphics
title: Vytvoření gradientového tahu v Java – průvodce tutoriálem Aspose.PSD
url: /cs/java/java-graphics-drawing/add-stroke-layer-gradient/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Jak vytvořit gradientní tah v Javě s Aspose.PSD

## Úvod
Pokud potřebujete **vytvořit gradientní tah java** efekty bez otevírání Photoshopu, jste na správném místě. V tomto tutoriálu se naučíte, jak použít Aspose.PSD pro Java — čistě‑Java knihovnu, která vám poskytuje plnou programovou kontrolu nad soubory PSD. Provedeme vás načtením PSD, přístupem k efektu tahu vrstvy, konfigurací výplně gradientu a nakonec uložením výsledku. Na konci budete schopni přidat profesionální gradientní obrysy k tvarům nebo textu během několika řádků kódu.

## Rychlé odpovědi
- **Jaký je hlavní cíl?** Vytvořit vrstvu gradientního tahu v souboru PSD pomocí Javy.  
- **Která knihovna poskytuje API?** Aspose.PSD pro Java (podporuje Java 8 +).  
- **Potřebuji licenci pro produkci?** Ano — vyžaduje se platná nebo dočasná licence.  
- **Jak dlouho trvá základní implementace?** Přibližně 10‑15 minut pro jednoduchý tah.  
- **Mohu přizpůsobit typ gradientu?** Samozřejmě — lineární, radiální i úhlové gradienty jsou všechny podporovány.

## Co je vrstva gradientního tahu?
Vrstva gradientního tahu je vektorový obrys, jehož barva plynule přechází mezi dvěma nebo více odstíny. Lze ji použít na tvary, text nebo jakoukoli vektorovou masku uvnitř souboru PSD, čímž designérům poskytuje dynamický vizuální efekt bez rasterizace grafiky.

## Proč použít Aspose.PSD pro Java?
Aspose.PSD pro Java poskytuje **úplnou podporu PSD** pro více než 100 funkcí — včetně vrstev, masek, úpravných vrstev a efektů vrstev — a může zpracovávat soubory až do 2 GB, aniž by načítala celý dokument do paměti. Knihovna běží na jakémkoli operačním systému, který podporuje Javu, nemá žádné nativní závislosti a je měsíčně aktualizována, aby zůstala kompatibilní s nejnovějšími specifikacemi souborů Photoshopu.

## Požadavky
1. **Java Development Kit (JDK)** — Nainstalujte nejnovější JDK z [webu Oracle](https://www.oracle.com/java/technologies/javase-downloads.html).  
2. **Aspose.PSD pro Java** — Stáhněte knihovnu ze [stránky ke stažení Aspose.PSD](https://releases.aspose.com/psd/java/).  
3. **IDE** — IntelliJ IDEA, Eclipse nebo NetBeans.  
4. **Licence** — Získejte [dočasnou licenci](https://purchase.aspose.com/temporary-license/), pokud nemáte plnou komerční licenci.

## Import balíčků
Importní příkazy načtou potřebné třídy do rozsahu.  

```text
```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;
import com.aspose.psd.examples.Utils.Assert;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.BlendMode;
import com.aspose.psd.fileformats.psd.layers.IGradientColorPoint;
import com.aspose.psd.fileformats.psd.layers.fillsettings.FillType;
import com.aspose.psd.fileformats.psd.layers.fillsettings.GradientColorPoint;
import com.aspose.psd.fileformats.psd.layers.fillsettings.GradientFillSettings;
import com.aspose.psd.fileformats.psd.layers.fillsettings.GradientTransparencyPoint;
import com.aspose.psd.fileformats.psd.layers.fillsettings.GradientType;
import com.aspose.psd.fileformats.psd.layers.fillsettings.IGradientTransparencyPoint;
import com.aspose.psd.fileformats.psd.layers.layereffects.StrokeEffect;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
```
```

Nyní rozdělíme proces do jasných kroků.

## Krok 1: Načtení souboru PSD
Načtení zdrojového souboru je první krok; musíte povolit zdroje efektů, aby byly informace o tahu dostupné pro úpravy. **PsdLoadOptions** konfiguruje, jak se PSD soubor načítá, a umožňuje povolit nebo zakázat konkrétní zdroje.  

```text
```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "Stroke.psd";
String exportPath = dataDir + "StrokeGradientChanged.psd";
PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);
PsdImage im = (PsdImage) Image.load(sourceFileName, loadOptions);
```
```

## Krok 2: Přístup k efektu tahu
**StrokeEffect** představuje styl obrysu aplikovaný na vrstvu, včetně šířky, barvy a výplně gradientem.  

```text
```java
StrokeEffect gradientStroke = (StrokeEffect) im.getLayers()[2].getBlendingOptions().getEffects()[0];
```
```

## Krok 3: Ověření vlastností efektu tahu
Než něco změníte, je dobré si přečíst existující vlastnosti. Pomůže vám to pochopit aktuální konfiguraci a vyhnout se neúmyslnému přepsání důležitých nastavení. **GradientFillSettings** obsahuje konfiguraci výplně gradientu pro efekt tahu.  

```text
```java
Assert.areEqual(BlendMode.Normal, gradientStroke.getBlendMode());
Assert.areEqual(255, gradientStroke.getOpacity());
Assert.areEqual(true, gradientStroke.isVisible());
GradientFillSettings fillSettings = (GradientFillSettings) gradientStroke.getFillSettings();
Assert.areEqual(Color.getBlack(), fillSettings.getColor());
Assert.areEqual(FillType.Gradient, fillSettings.getFillType());
Assert.areEqual(true, fillSettings.getAlignWithLayer());
Assert.areEqual(GradientType.Linear, fillSettings.getGradientType());
Assert.isTrue(Math.abs(90 - fillSettings.getAngle()) < 0.001, "Angle is incorrect");
Assert.areEqual(false, fillSettings.getDither());
Assert.isTrue(Math.abs(0 - fillSettings.getHorizontalOffset()) < 0.001, "Horizontal offset is incorrect");
Assert.isTrue(Math.abs(0 - fillSettings.getVerticalOffset()) < 0.001, "Vertical offset is incorrect");
Assert.areEqual(false, fillSettings.getReverse());
```
```

## Krok 4: Úprava nastavení výplně gradientu
`GradientFill` definuje, jak barvy přecházejí podél tahu. Můžete změnit jeho typ (lineární, radiální), úhel a režim míchání, poté přiřadit nové body barvy a průhlednosti.  

```text
```java
fillSettings.setColor(Color.getGreen());
gradientStroke.setOpacity((byte) 127);
gradientStroke.setBlendMode(BlendMode.Color);
fillSettings.setAlignWithLayer(false);
fillSettings.setGradientType(GradientType.Radial);
fillSettings.setAngle(45);
fillSettings.setDither(true);
fillSettings.setHorizontalOffset(15);
fillSettings.setVerticalOffset(11);
fillSettings.setReverse(true);
```
```

## Krok 5: Přidání a úprava barevných a průhlednostních bodů
Gradient se skládá ze série barevných a průhlednostních bodů. **GradientColorPoint** definuje barevný bod v gradientu, určuje jeho barvu a polohu. **GradientTransparencyPoint** definuje průhlednostní bod, určuje jeho průhlednost a polohu. Přidání nebo úprava těchto bodů vám umožní tvarovat vizuální tok tahu.  

```text
```java
// Add new color point
GradientColorPoint colorPoint = fillSettings.addColorPoint();
colorPoint.setColor(Color.getGreen());
colorPoint.setLocation(4096);
colorPoint.setMedianPointLocation(75);
// Change location of previous point
fillSettings.getColorPoints()[1].setLocation(1899);
// Add new transparency point
GradientTransparencyPoint transparencyPoint = fillSettings.addTransparencyPoint();
transparencyPoint.setOpacity(25);
transparencyPoint.setMedianPointLocation(25);
transparencyPoint.setLocation(4096);
// Change location of previous transparency point
fillSettings.getTransparencyPoints()[1].setLocation(2411);
```
```

## Krok 6: Uložení upraveného souboru PSD
Po všech úpravách zapište aktualizovaný dokument zpět na disk. Aspose.PSD automaticky zachová všechny ostatní vrstvy a zdroje.  

```text
```java
im.save(exportPath);
```
```

## Krok 7: Ověření úprav
Znovu načtěte uložený soubor a ověřte, že vlastnosti gradientu tahu odpovídají nastaveným hodnotám. Tento ověřovací krok je nezbytný pro automatizované pipeline. **Assert** poskytuje jednoduché testovací aserce pro ověření podmínek během běhu.  

```text
```java
PsdImage img = (PsdImage) Image.load(exportPath, loadOptions);
StrokeEffect gradientStrokeEffect = (StrokeEffect) img.getLayers()[2].getBlendingOptions().getEffects()[0];
Assert.areEqual(BlendMode.Color, gradientStrokeEffect.getBlendMode());
Assert.areEqual(127, gradientStrokeEffect.getOpacity());
Assert.areEqual(true, gradientStrokeEffect.isVisible());
GradientFillSettings fillSetting = (GradientFillSettings) gradientStrokeEffect.getFillSettings();
Assert.areEqual(Color.getGreen(), fillSetting.getColor());
Assert.areEqual(FillType.Gradient, fillSetting.getFillType());
// Check color points
Assert.areEqual(3, fillSetting.getColorPoints().length);
IGradientColorPoint point = fillSetting.getColorPoints()[0];
Assert.areEqual(50, point.getMedianPointLocation());
Assert.areEqual(Color.getBlack(), point.getColor());
Assert.areEqual(0, point.getLocation());
point = fillSettings.getColorPoints()[1];
Assert.areEqual(50, point.getMedianPointLocation());
Assert.areEqual(Color.getWhite(), point.getColor());
Assert.areEqual(1899, point.getLocation());
point = fillSettings.getColorPoints()[2];
Assert.areEqual(75, point.getMedianPointLocation());
Assert.areEqual(Color.getGreen(), point.getColor());
Assert.areEqual(4096, point.getLocation());
// Check transparency points
Assert.areEqual(3, fillSettings.getTransparencyPoints().length);
IGradientTransparencyPoint transparencyPoint1 = fillSettings.getTransparencyPoints()[0];
Assert.areEqual(50, transparencyPoint1.getMedianPointLocation());
Assert.areEqual(100, transparencyPoint1.getOpacity());
Assert.areEqual(0, transparencyPoint1.getLocation());
transparencyPoint1 = fillSettings.getTransparencyPoints()[1];
Assert.areEqual(50, transparencyPoint1.getMedianPointLocation());
Assert.areEqual(100, transparencyPoint1.getOpacity());
Assert.areEqual(2411, transparencyPoint1.getLocation());
transparencyPoint1 = fillSettings.getTransparencyPoints()[2];
Assert.areEqual(25, transparencyPoint1.getMedianPointLocation());
Assert.areEqual(25, transparencyPoint1.getOpacity());
Assert.areEqual(4096, transparencyPoint1.getLocation());
```
```

## Časté problémy a tipy pro řešení
- **Chyba chybějící licence** — Pokud vidíte výjimku licence, zkontrolujte, že je soubor dočasné licence načten před jakýmkoli voláním API.  
- **Gradient není viditelný** — Ujistěte se, že příznak `strokeEnabled` cílové vrstvy je nastaven na `true`; jinak je efekt během renderování ignorován.  
- **Výkon u velkých souborů** — Pro PSD větší než 500 MB zvažte použití `PsdImage.load(..., LoadOptions)` s `loadResources = false` a povolte jen zdroje, které potřebujete.

## Často kladené otázky

**Q: Co je Aspose.PSD pro Java?**  
A: Aspose.PSD pro Java je čistě‑Java knihovna, která vývojářům umožňuje vytvářet, upravovat, konvertovat a renderovat Photoshop PSD soubory bez nutnosti Adobe Photoshopu.

**Q: Potřebuji licenci k používání Aspose.PSD pro Java?**  
A: Ano, pro produkční použití je vyžadována platná licence. Můžete získat [dočasnou licenci](https://purchase.aspose.com/temporary-license/) pro vyhodnocení.

**Q: Mohu pomocí této knihovny vytvářet PSD soubory od nuly?**  
A: Rozhodně. Aspose.PSD poskytuje API pro vytvoření nového PSD dokumentu, přidání vrstev, aplikaci efektů a uložení souboru kompletně programově.

**Q: Je možné aplikovat jiné efekty kromě gradientních tahů?**  
A: Ano, můžete aplikovat stíny, záře, reliéfy a mnoho dalších efektů vrstev pomocí stejného API založeného na efektech.

**Q: Kde najdu kompletní referenční dokumentaci?**  
A: Oficiální dokumentace je k dispozici v [Aspose.PSD Java API reference](https://reference.aspose.com/psd/java/).

## Závěr
Nyní máte kompletní end‑to‑end řešení, jak **vytvořit gradientní tah java** efekty v PSD souborech pomocí Aspose.PSD. Načtením PSD, přístupem k efektu tahu, konfigurací výplně gradientu a uložením souboru můžete automatizovat složité grafické workflow, které by jinak vyžadovaly ruční práci ve Photoshopu. Experimentujte s různými typy gradientů, režimy míchání a průhlednostními body, abyste dosáhli přesně požadovaného vzhledu pro vaši aplikaci.

---

**Poslední aktualizace:** 2026-09-03  
**Testováno s:** Aspose.PSD for Java 24.11  
**Autor:** Aspose

## Související tutoriály

- [Create Gradient Fill PSD with Java using Aspose.PSD – Add Gradient Fill Layer](/psd/java/psd-image-modification-conversion/add-gradient-fill-layer-psd-files/)
- [How to Create Radial Gradient Effects in Aspose.PSD for Java](/psd/java/advanced-image-effects/add-gradient-effects/)
- [How to Change Stroke Color Java Using Aspose.PSD](/psd/java/advanced-image-effects/add-stroke-layer-color/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}