---
date: 2026-06-18
description: Naučte se, jak změnit barvu stínu v Javě a přizpůsobit efekty stínu pomocí
  Aspose.PSD pro Java. Postupujte podle tohoto tutoriálu krok za krokem o efektech
  stínu.
keywords:
- change shadow color java
- Aspose.PSD shadow effect
- Java PSD manipulation
linktitle: Podpora stínového efektu
schemas:
- author: Aspose
  dateModified: '2026-06-18'
  description: Learn how to change shadow color java and customize shadow effects
    using Asprose.PSD for Java. Follow this step‑by‑step shadow effect tutorial.
  headline: Change Shadow Color Java with Aspose.PSD for Java
  type: TechArticle
- description: Learn how to change shadow color java and customize shadow effects
    using Asprose.PSD for Java. Follow this step‑by‑step shadow effect tutorial.
  name: Change Shadow Color Java with Aspose.PSD for Java
  steps:
  - name: Load the PSD Image
    text: 'First, load the source PSD while enabling the loading of effect resources:'
  - name: Retrieve the Existing Drop Shadow Effect
    text: 'Locate the shadow effect on the desired layer (in this example, the second
      layer):'
  - name: Verify the Default Settings (Optional)
    text: 'Running these assertions helps you understand the original values before
      you modify them:'
  - name: '**Change Shadow Color** and Customize Other Properties'
    text: Now we actually **change shadow color** to green, adjust opacity, distance,
      size, and other attributes. This demonstrates the **customize shadow effect**
      capabilities of Aspose.PSD. The `setOpacity(byte)` method sets the shadow's
      opacity level (0‑255).
  - name: Save the Modified Image
    text: 'Finally, write the updated PSD back to disk using the `save` method of
      `PsdImage`:'
  type: HowTo
- questions:
  - answer: Absolutely! Aspose.PSD for Java is a powerful library designed for professional
      graphic design tasks.
    question: Is Aspose.PSD for Java suitable for professional graphic design projects?
  - answer: Yes, Aspose.PSD for Java is a commercial product. You can purchase it
      [here](https://purchase.aspose.com/buy).
    question: Can I use Aspose.PSD for Java in commercial applications?
  - answer: Yes, you can explore a free trial version [here](https://releases.aspose.com/).
    question: Is there a free trial available?
  - answer: Refer to the comprehensive documentation [here](https://reference.aspose.com/psd/java/).
    question: Where can I find detailed documentation?
  - answer: Join the community forum [here](https://forum.aspose.com/c/psd/34) for
      any support queries.
    question: How can I get support for Aspose.PSD for Java?
  type: FAQPage
second_title: Aspose.PSD Java API
title: Změna barvy stínu v Javě s Aspose.PSD pro Java
url: /cs/java/basic-image-operations/support-shadow-effect/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Změna barvy stínu v Javě s Aspose.PSD pro Java

## Úvod

Přidání hloubky do vašich grafických prací často znamená **změnu barvy stínu**, aby odpovídala náladě designu. S Aspose.PSD pro Java můžete snadno přidávat nebo upravovat efekty drop‑shadow, řídit neprůhlednost a jemně ladit další parametry — vše z Java kódu. V tomto **tutorialu o stínových efektech** si projdeme načtení PSD, čtení existujícího stínu, přizpůsobení jeho barvy, neprůhlednosti, vzdálenosti a nakonec uložení aktualizovaného souboru. Tento průvodce ukazuje přesně, jak **změnit barvu stínu java** reprodukovatelným způsobem.

## Rychlé odpovědi
- **Co znamená „change shadow color“?** Aktualizuje vlastnost barvy DropShadowEffect aplikovaného na vrstvu PSD.  
- **Která knihovna to podporuje?** Aspose.PSD pro Java poskytuje plnou podporu pro stínové efekty.  
- **Potřebuji licenci?** Zkušební verze funguje pro vývoj; pro produkci je vyžadována komerční licence.  
- **Mohu nastavit neprůhlednost stínu?** Ano — použijte `setOpacity(byte)` k definování průhlednosti (0‑255).  
- **Je kód kompatibilní s Java 8+?** Rozhodně, API cílí na Java 8 a novější.

## Co je „change shadow color“ v souborech PSD?

Změna barvy stínu upravuje vizuální odstín drop‑shadow, který se zobrazuje za vrstvou. Toto nastavení umožňuje designérům simulovat různé světelné podmínky, sladit stíny s paletou firemních barev a přidat umělecký nádech do kompozic. Úpravou odstínu můžete učinit stíny teplejší, chladnější nebo je zcela sladit s konkrétním barevným schématem, čímž zvýšíte celkový vizuální dopad.

## Proč použít Aspose.PSD pro Java k přizpůsobení stínových efektů?

Aspose.PSD pro Java zachovává **více než 100 formátů obrázků** a dokáže zpracovávat PSD soubory až do **2 GB** bez načítání celého dokumentu do paměti, což poskytuje enterprise‑grade výkon. Knihovna vám dává plnou kontrolu nad každým atributem stínu — barvou, neprůhledností, vzdáleností, úhlem, rozptylem i šumem — bez nutnosti mít nainstalovaný Photoshop. Běží na Windows, Linux i macOS JVM, což z ní činí nejspolehlivější volbu pro automatizované grafické pipeline.

## Požadavky

- Základní znalost programování v Javě.  
- Aspose.PSD pro Java nainstalováno. Můžete jej stáhnout [zde](https://releases.aspose.com/psd/java/).  

## Import balíčků

Než začnete, importujte potřebné třídy, abyste mohli pracovat s obrázky a stínovými efekty:

Třída `Color` představuje hodnotu barvy používanou v celém API.  
Třída `Image` je základní typ pro všechny objekty obrázků.  
Třída `PsdImage` poskytuje funkce specifické pro soubory PSD.  
Třída `PsdLoadOptions` vám umožňuje specifikovat možnosti načítání souborů PSD, například povolení zdrojů efektů.  
Třída `DropShadowEffect` představuje filtr drop‑shadow aplikovaný na vrstvu PSD a poskytuje přístup ke všem jejím nastavitelným vlastnostem.

```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;


import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.layereffects.DropShadowEffect;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
```

## Průvodce krok za krokem

### Krok 1: Načtení PSD obrázku

Nejprve načtěte zdrojový PSD a povolte načítání zdrojů efektů:

```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "Shadow.psd";
String psdPathAfterChange = dataDir + "ShadowChanged.psd";

PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);

PsdImage im = (PsdImage)Image.load(sourceFileName, loadOptions);
```

### Krok 2: Získání existujícího efektu Drop Shadow

Najděte efekt stínu na požadované vrstvě (v tomto příkladu druhá vrstva):

```java
DropShadowEffect shadowEffect = (DropShadowEffect)(im.getLayers()[1].getBlendingOptions().getEffects()[0]);
```

### Krok 3: Ověření výchozích nastavení (volitelné)

Spuštění těchto asercí vám pomůže pochopit původní hodnoty před jejich úpravou:

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

### Krok 4: **Změna barvy stínu** a přizpůsobení dalších vlastností

Nyní skutečně **změníme barvu stínu** na zelenou, upravíme neprůhlednost, vzdálenost, velikost a další atributy. Toto demonstruje schopnosti **customize shadow effect** v Aspose.PSD. Metoda `setOpacity(byte)` nastavuje úroveň neprůhlednosti stínu (0‑255).

```java
shadowEffect.setColor(Color.getGreen());          // change shadow color
shadowEffect.setOpacity((byte)128);               // set shadow opacity (50% transparent)
shadowEffect.setDistance(11);                     // move shadow farther from the object
shadowEffect.setUseGlobalLight(false);            // use local lighting
shadowEffect.setSize(9);                          // adjust blur radius
shadowEffect.setAngle(45);                        // rotate light source
shadowEffect.setSpread(3);                        // increase spread
shadowEffect.setNoise(50);                        // add texture noise
```

### Krok 5: Uložení upraveného obrázku

Nakonec zapište aktualizovaný PSD zpět na disk pomocí metody `save` třídy `PsdImage`:

```java
im.save(psdPathAfterChange);
```

## Časté problémy a tipy

- **NullPointerException při získávání efektů** – ujistěte se, že je zavoláno `setLoadEffectsResource(true)`; jinak se efekty nenačtou.  
- **Barva se nemění** – ověřte, že upravujete správný index vrstvy (`im.getLayers()[1]` v tomto příkladu).  
- **Opacity vypadá nezměněně** – pamatujte, že opacity je byte (0‑255). Je nutné přetypovat na `(byte)`.

## Závěr

Dodržením těchto kroků můžete **změnit barvu stínu**, **nastavit neprůhlednost stínu** a plně **přizpůsobit parametry stínového efektu** v libovolném PSD souboru pomocí Aspose.PSD pro Java. To vám umožní programově vytvářet bohatší grafiku bez ruční práce ve Photoshopu, ideální pro automatizované designové pipeline a hromadné zpracování.

## Často kladené otázky

**Q: Je Aspose.PSD pro Java vhodný pro profesionální projekty grafického designu?**  
A: Rozhodně! Aspose.PSD pro Java je výkonná knihovna navržená pro profesionální úkoly grafického designu.

**Q: Mohu použít Aspose.PSD pro Java v komerčních aplikacích?**  
A: Ano, Aspose.PSD pro Java je komerční produkt. Můžete jej zakoupit [zde](https://purchase.aspose.com/buy).

**Q: Je k dispozici bezplatná zkušební verze?**  
A: Ano, můžete vyzkoušet bezplatnou verzi [zde](https://releases.aspose.com/).

**Q: Kde najdu podrobnou dokumentaci?**  
A: Odkazujte na komplexní dokumentaci [zde](https://reference.aspose.com/psd/java/).

**Q: Jak získám podporu pro Aspose.PSD pro Java?**  
A: Připojte se k komunitnímu fóru [zde](https://forum.aspose.com/c/psd/34) pro jakékoli dotazy ohledně podpory.

---

**Last Updated:** 2026-06-18  
**Tested With:** Aspose.PSD for Java 24.10  
**Author:** Aspose  

{{< blocks/products/products-backtop-button >}}

## Související tutoriály

- [Java Image Manipulation - Add Effects at Runtime with Aspose.PSD for Java](/psd/java/advanced-techniques/add-effects-runtime/)
- [Save PSD as PNG and Apply Rendering Drop Shadow in Aspose.PSD for Java](/psd/java/advanced-image-manipulation/rendering-drop-shadow/)
- [Blur Image Java with Aspose.PSD – Add Blur Effect](/psd/java/advanced-techniques/blur-image/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}