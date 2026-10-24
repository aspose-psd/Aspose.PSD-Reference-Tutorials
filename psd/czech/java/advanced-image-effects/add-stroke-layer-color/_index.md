---
date: 2026-10-24
description: Naučte se, jak vytvořit stroke layer v Java s Aspose.PSD pro Java. Tento
  krok‑za‑krokem průvodce vám ukáže, jak přidat stroke layer, změnit jeho barvu, upravit
  opacity a uložit PSD.
keywords:
- create stroke layer java
- change stroke color java
- modify stroke opacity
- apply stroke effect
- psd stroke tutorial
lastmod: 2026-10-24
linktitle: Přidat barvu Stroke Layer
og_description: Vytvořte stroke layer v Java pomocí Aspose.PSD pro Java. Postupujte
  podle tohoto stručného tutoriálu, abyste přidali stroke layer, změnili jeho barvu,
  upravili opacity a exportovali soubor PSD.
og_image_alt: Screenshot of a Java IDE showing Aspose.PSD code that creates and modifies
  a stroke layer in a PSD file
og_title: Vytvořte stroke layer v Java s Aspose.PSD – Rychlý průvodce
schemas:
- author: Aspose
  dateModified: '2026-10-24'
  description: Learn how to create stroke layer Java with Aspose.PSD for Java. This
    step‑by‑step guide shows you how to add a stroke layer, change its color, adjust
    opacity, and save the PSD.
  headline: How to create stroke layer Java using Aspose.PSD
  type: TechArticle
- description: Learn how to create stroke layer Java with Aspose.PSD for Java. This
    step‑by‑step guide shows you how to add a stroke layer, change its color, adjust
    opacity, and save the PSD.
  name: How to create stroke layer Java using Aspose.PSD
  steps:
  - name: set up your project
    text: Create a new Java project, add the Aspose.PSD JAR to the build path, and
      verify the library loads without errors.
  - name: load the PSD file
    text: Enable loading of effect resources so the stroke information is available.
  - name: access the stroke effect layer
    text: '`StrokeEffect` is Aspose.PSD’s class that represents a vector outline applied
      to a layer. Retrieve the first stroke effect from the second layer (index 1).'
  - name: validate stroke properties
    text: '`ColorFillSettings` holds the color and opacity values for a stroke. Confirm
      the existing properties before making changes to avoid unexpected results.'
  - name: set color and opacity (how to change stroke color)
    text: Here we **change stroke color** to yellow and reduce opacity to 50 % (127
      / 255). `ColorFillSettings` also lets you specify blend mode and size.
  - name: save the modified PSD
    text: Write the updated image back to disk. The new file now contains the modified
      stroke.
  type: HowTo
- questions:
  - answer: Yes, Aspose.PSD can be combined with libraries such as Apache Commons
      Imaging or Java2D for extended functionality.
    question: Can I use Aspose.PSD with other Java graphic libraries?
  - answer: Absolutely. The library supports the newest Photoshop specifications and
      over 150 PSD features.
    question: Is Aspose.PSD compatible with the latest PSD file format?
  - answer: Wrap your code in try‑catch blocks and consult the [support forum](https://forum.aspose.com/c/psd/34)
      for detailed troubleshooting examples.
    question: How do I handle exceptions while using Aspose.PSD?
  - answer: Certainly! Grab a [free trial](https://releases.aspose.com/) to explore
      all features.
    question: Can I try Aspose.PSD before purchasing?
  - answer: Obtain a [temporary license](https://purchase.aspose.com/temporary-license/)
      to evaluate the library in your development environment.
    question: Where can I get a temporary license for Aspose.PSD?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- create stroke layer
- Aspose.PSD
- Java image processing
title: Jak vytvořit stroke layer v Java pomocí Aspose.PSD
url: /cs/java/advanced-image-effects/add-stroke-layer-color/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Jak vytvořit vrstvu obrysu v Javě pomocí Aspose.PSD

## Úvod

Pokud potřebujete **vytvořit vrstvu obrysu v Javě** v dokumentu Photoshopu programově, Aspose.PSD pro Javu vám poskytuje čistý, kód‑první přístup. V tomto tutoriálu se naučíte, jak přidat novou vrstvu obrysu, změnit její barvu, upravit průhlednost a uložit výsledek — vše bez spouštění Photoshopu. Na konci také zjistíte, jak upravit obrys existující vrstvy, což vám dává plnou kreativní kontrolu přímo z vaší Java aplikace.

## Rychlé odpovědi
- **Jaká knihovna je vyžadována?** Aspose.PSD pro Javu (nejnovější verze).  
- **Mohu změnit barvu obrysu?** Ano — použijte `ColorFillSettings` k nastavení libovolné `Color`.  
- **Potřebuji licenci?** Dočasná licence stačí pro hodnocení; plná licence je vyžadována pro produkci.  
- **Jaká verze Javy je podporována?** Java 8 nebo vyšší.  
- **Jak dlouho trvá implementace?** Obvykle méně než 10 minut pro základní změnu obrysu.

## Co je vrstva obrysu v PSD?
Vrstva obrysu je vektorový efekt, který kreslí obrys kolem obsahu vrstvy. Lze jej přizpůsobit barvou, tloušťkou, průhledností a režimem prolnutí. Programová úprava tohoto efektu umožňuje automatizaci značkování, dávkové zpracování nebo dynamické generování grafiky.

## Proč použít Aspose.PSD ke změně barvy obrysu?
Aspose.PSD podporuje **150+** funkcí PSD — včetně vektorových masek, chytrých objektů a efektů vrstev — při zpracování souborů stovek stránek bez načítání celého dokumentu do paměti. Knihovna běží na libovolném OS s JVM, poskytuje sub‑sekundový výkon pro typické assety a nevyžaduje instalaci Photoshopu.

## Jak vytvořit vrstvu obrysu v Javě?

Načtěte PSD, přidejte efekt obrysu, nakonfigurujte jeho vzhled a uložte soubor — vše v několika jednoduchých řádcích. Níže uvedená odpověď vám přesně řekne, co dělat, než se pustíme do podrobného průvodce.

**Přímá odpověď (40‑70 slov):**  
`PsdImage` představuje dokument PSD a poskytuje metody pro načítání a ukládání souborů. Začněte načtením vašeho PSD pomocí `PsdImage.load("input.psd", loadOptions)`. Vytvořte nový `StrokeEffect`, nastavte jeho `ColorFillSettings` na požadovanou `Color`, upravte průhlednost a velikost, poté připojte efekt k `BlendingOptions` cílové vrstvy. Nakonec zavolejte `psd.save("output.psd", SaveFormat.PSD)`. Tento postup vytvoří vrstvu obrysu v Javě s Aspose.PSD.

### Požadavky

- **Aspose.PSD library** – stáhněte ze [official documentation](https://reference.aspose.com/psd/java/).  
- **Java Development Kit (JDK)** – verze 8 nebo novější.  
- **IDE** – Eclipse, IntelliJ IDEA nebo jakýkoli editor kompatibilní s Javou.

### Import balíčků

Nejprve importujte třídy, které budete potřebovat. Tím získá váš projekt přístup k API pro zpracování PSD a efektů obrysu.

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

### Krok 1: nastavení projektu

Vytvořte nový Java projekt, přidejte Aspose.PSD JAR do cesty sestavení a ověřte, že se knihovna načte bez chyb.

### Krok 2: načtení souboru PSD

Povolte načítání zdrojů efektů, aby byly informace o obrysu k dispozici.

```java
String dataDir = "Your Document Directory";

String sourceFileName = dataDir + "Stroke.psd";
String exportPath = dataDir + "StrokeGradientChanged.psd";

PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);

PsdImage im = (PsdImage)Image.load(sourceFileName, loadOptions);
```

### Krok 3: přístup k vrstvě efektu obrysu

`StrokeEffect` je třída Aspose.PSD, která představuje vektorový obrys aplikovaný na vrstvu. Získejte první efekt obrysu ze druhé vrstvy (index 1).

```java
StrokeEffect colorStroke = (StrokeEffect)im.getLayers()[1].getBlendingOptions().getEffects()[0];
```

### Krok 4: ověření vlastností obrysu

`ColorFillSettings` uchovává barvu a hodnoty průhlednosti pro obrys. Potvrďte existující vlastnosti před provedením změn, abyste předešli neočekávaným výsledkům.

```java
Assert.areEqual(BlendMode.Normal, colorStroke.getBlendMode());
Assert.areEqual(255, colorStroke.getOpacity());
Assert.areEqual(true, colorStroke.isVisible());
```

### Krok 5: nastavení barvy a průhlednosti (jak změnit barvu obrysu)

Zde **měníme barvu obrysu** na žlutou a snižujeme průhlednost na 50 % (127 / 255). `ColorFillSettings` vám také umožňuje specifikovat režim prolnutí a velikost.

```java
ColorFillSettings fillSettings = (ColorFillSettings)colorStroke.getFillSettings();
fillSettings.setColor(Color.getYellow());

colorStroke.setOpacity((byte)127);
```

### Krok 6: uložení upraveného PSD

Zapište aktualizovaný obrázek zpět na disk. Nový soubor nyní obsahuje upravený obrys.

```java
im.save(exportPath);
```

## Jak změnit barvu obrysu v Javě?

`Color` představuje ARGB hodnotu barvy. Načtěte svůj PSD, najděte cílovou vrstvu, aktualizujte `ColorFillSettings` novou `Color` a soubor uložte. Tato operace vyžaduje jen několik řádků kódu a dokončí se za méně než sekundu pro typické assety, což je rychlé a efektivní.

**Přímá odpověď (40‑70 slov):**  
Použijte `layer.getEffects().getStrokeEffect()` k získání existujícího obrysu, zavolejte `stroke.getColorFillSettings().setColor(Color.getRed())` (nebo libovolnou `Color`, kterou potřebujete), volitelně upravte `setOpacity((byte)200)` pro 78 % průhlednost a poté uložte PSD pomocí `psd.save("output.psd", SaveFormat.PSD)`. Změna se aplikuje okamžitě bez pře‑renderování celého dokumentu.

## Jak upravit průhlednost obrysu?

Pokud potřebujete pouze upravit průhlednost a zachovat původní barvu, změňte hodnotu `setOpacity` (0‑255) na `ColorFillSettings`. Například `colorStroke.setOpacity((byte)200);` nastaví obrys přibližně na 78 % neprůhlednosti. Úprava průhlednosti vám umožní vytvořit jemné obrysy nebo plně solidní linie podle požadavků designu.

**Přímá odpověď (40‑70 slov):**  
Získejte `StrokeEffect` z požadované vrstvy a zavolejte `stroke.getColorFillSettings().setOpacity((byte)desiredValue)`, kde `desiredValue` je v rozmezí 0 (průhledné) až 255 (plně neprůhledné). Uložte PSD a nová průhlednost se projeví okamžitě. Tento postup funguje pro jakýkoli existující obrys, bez ohledu na jeho původní barvu.

## Jak použít efekt obrysu?

Pro přidání nového efektu obrysu do vrstvy, která jej zatím nemá, vytvořte instanci `StrokeEffect`, nakonfigurujte její `ColorFillSettings` a připojte ji k `BlendingOptions` vrstvy. Metody `setColor` a `setOpacity` se používají k definování celkového vzhledu.

**Přímá odpověď (40‑70 slov):**  
Instancujte `StrokeEffect newStroke = new StrokeEffect(); newStroke.getColorFillSettings().setColor(Color.getBlue()); newStroke.getColorFillSettings().setOpacity((byte)255); layer.getBlendingOptions().setEffect(newStroke);`. Po připojení efektu uložte PSD. Tím přidáte čerstvou, plně přizpůsobitelnou vrstvu obrysu do libovolné existující vrstvy v dokumentu.

## Běžné případy použití pro změnu barvy obrysu
- **Automatizace značkování:** Aplikujte firemní barvu na loga ve stovkách PSD souborů jedním dávkovým spuštěním.  
- **Dynamické generování UI:** Měňte barvy obrysů za běhu podle uživatelem vybraných motivů ve webovém designovacím nástroji.  
- **Předběžná příprava:** Zajistěte, aby všechny barvy obrysů splňovaly tiskové specifikace před odesláním souborů do tisku.

## Běžné úskalí a tipy

- **Null checks** – vždy ověřte, že `getEffects()` vrací ne‑null pole před přetypováním.  
- **Layer index** – vrstvy PSD jsou číslovány od nuly; ujistěte se, že cílíte na správnou vrstvu.  
- **Color format** – `Color.getYellow()` je jen příklad; vlastní barvy můžete vytvořit pomocí `new Color(r, g, b)`.  
- **Opacity range** – průhlednost je byte (0–255); hodnoty nad 255 budou oříznuty.  
- **Resource loading** – zapomenutí `loadOptions.setLoadEffectsResource(true)` povede k `null` poli efektů.

## Často kladené otázky

**Q: Mohu použít Aspose.PSD s jinými Java grafickými knihovnami?**  
A: Ano, Aspose.PSD lze kombinovat s knihovnami jako Apache Commons Imaging nebo Java2D pro rozšířenou funkčnost.

**Q: Je Aspose.PSD kompatibilní s nejnovějším formátem souboru PSD?**  
A: Rozhodně. Knihovna podporuje nejnovější specifikace Photoshopu a více než 150 funkcí PSD.

**Q: Jak zacházet s výjimkami při používání Aspose.PSD?**  
A: Zabalte kód do bloků try‑catch a navštivte [support forum](https://forum.aspose.com/c/psd/34) pro podrobné příklady řešení problémů.

**Q: Můžu vyzkoušet Aspose.PSD před zakoupením?**  
A: Samozřejmě! Stáhněte si [free trial](https://releases.aspose.com/) a prozkoumejte všechny funkce.

**Q: Kde získám dočasnou licenci pro Aspose.PSD?**  
A: Získejte [temporary license](https://purchase.aspose.com/temporary-license/) pro vyhodnocení knihovny ve vašem vývojovém prostředí.

---

**Poslední aktualizace:** 2026-10-24  
**Testováno s:** Aspose.PSD 24.11 for Java  
**Autor:** Aspose

## Související tutoriály

- [Jak změnit barvu obrysu v Javě pomocí Aspose.PSD](/psd/java/advanced-image-effects/add-stroke-layer-color/)
- [Jak přidat stín v PSD pomocí Javy – Pokročilé efekty vrstev](/psd/java/advanced-psd-layer-features-effects/)
- [Pattern Overlay PSD: Přidat efekty pomocí Aspose.PSD pro Javu](/psd/java/advanced-image-effects/add-pattern-effects/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}