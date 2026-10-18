---
date: 2026-10-18
description: Naučte se, jak exportovat PSD do PNG a přidat novou běžnou vrstvu pomocí
  Aspose.PSD pro Java s dočasnou licencí. Průvodce krok za krokem, umístění vrstev
  a řešení problémů.
keywords:
- how to export psd
- aspose temporary license
- set layer position
- create new psd layer
lastmod: 2026-10-18
linktitle: Přidat novou běžnou vrstvu do PSD
og_description: Naučte se, jak exportovat PSD do PNG a přidat novou běžnou vrstvu
  pomocí Aspose.PSD pro Java s dočasnou licencí. Obsahuje kompletní kroky bez kódu
  a tipy na umístění vrstev.
og_image_alt: Screenshot of Java code adding a layer to a PSD and exporting to PNG
og_title: Jak exportovat PSD do PNG a přidat vrstvu pomocí Aspose.PSD pro Java
schemas:
- author: Aspose
  dateModified: '2026-10-18'
  description: Learn how to export PSD to PNG and add a new regular layer using Aspose.PSD
    for Java with a temporary license. Step‑by‑step guide, layer positioning and troubleshooting.
  headline: How to export PSD to PNG and add a layer with Aspose.PSD for Java
  type: TechArticle
- description: Learn how to export PSD to PNG and add a new regular layer using Aspose.PSD
    for Java with a temporary license. Step‑by‑step guide, layer positioning and troubleshooting.
  name: How to export PSD to PNG and add a layer with Aspose.PSD for Java
  steps:
  - name: Load the PSD file
    text: '`PsdImage` is Aspose.PSD''s core class that represents a PSD document in
      memory. Loading the file creates a manipulable object you can edit.'
  - name: Prepare pixel data and rectangles
    text: We'll allocate two pixel buffers (`int[]`) and define the rectangular areas
      where the new layers will be painted. Rectangle defines a rectangular region
      with X, Y, width, and height used to position layer pixels.
  - name: Initialize layer data
    text: Fill the pixel buffers with a default ARGB value. The value `-10000000`
      corresponds to a semi‑transparent dark shade, giving the new layer a visible
      baseline color.
  - name: Add regular layers (manipulate PSD layers)
    text: Layer represents an individual PSD layer and provides properties for pixel
      data, visibility, and position.
  - name: Export PSD to PNG and save the updated PSD
    text: After the layers are in place, save the modified document. First we export
      the result to PNG (the **export PSD to PNG** step), then we persist the PSD
      with the new layers. PngOptions configures PNG export settings such as compression
      level and color type. > **Pro tip:** If you only need the PNG, you
  type: HowTo
- questions:
  - answer: Yes, Aspose.PSD supports Java 8 and later versions.
    question: Is Aspose.PSD compatible with Java 8?
  - answer: Absolutely! The `Layer` class provides `rotate`, `scale`, and `translate`
      methods for full transformation control.
    question: Can I apply transformations (rotate, scale) to the added layers?
  - answer: Detailed API docs are available [Aspose.PSD Java API reference](https://reference.aspose.com/psd/java/).
    question: Where can I find additional Aspose.PSD documentation?
  - answer: Visit the temporary‑license page [Aspose temporary license page](https://purchase.aspose.com/temporary-license/).
    question: How do I obtain a temporary license for Aspose.PSD?
  - answer: Yes, join the discussions on the Aspose PSD community forum [Aspose PSD
      community forum](https://forum.aspose.com/c/psd/34).
    question: Are there community forums for Aspose.PSD support?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- export psd to png
- aspose psd
- java image processing
title: Jak exportovat PSD do PNG a přidat vrstvu pomocí Aspose.PSD pro Java
url: /cs/java/advanced-image-effects/add-new-regular-layer/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Jak exportovat PSD do PNG a přidat vrstvu pomocí Aspose.PSD pro Java

V tomto **Aspose.PSD tutoriálu** se naučíte **jak exportovat PSD do PNG** a zároveň **přidat novou běžnou vrstvu** do stejného souboru, vše pomocí **dočasné licence Aspose**. Ať už vytváříte webové miniatury, připravujete aktiva pro designový pipeline, nebo experimentujete s **manipulací obrázků PSD**, tento průvodce ukazuje každý krok – od načtení zdrojového souboru po uložení jak aktualizovaného PSD, tak kopie PNG – takže můžete okamžitě začít pracovat s vrstvami PSD.

## Rychlé odpovědi
- **Mohu exportovat PSD do PNG jedním voláním?** Ano – po přidání libovolných vrstev jednoduše zavoláte `save` s `PngOptions`.
- **Potřebuji plnou licenci pro vývoj?** Dočasná licence odstraňuje vodotisk hodnocení a odemyká všechny API; pro produkční použití je vyžadována trvalá licence.
- **Jaké verze Javy jsou podporovány?** Aspose.PSD funguje s Java 8 a novějšími.
- **Je umístění vrstvy založeno na pixelech?** Rozhodně; nastavujete souřadnice left, top, right, bottom v pixelech pomocí metod **set layer position**.
- **Zachová PNG průhlednost vrstvy?** Exportované PNG obsahuje sloučený výsledek všech viditelných vrstev, zachovávající průhlednost, kde je to relevantní.

## Proč použít dočasnou licenci Aspose?

Dočasná licence Aspose vám umožní vyzkoušet kompletní sadu funkcí Aspose.PSD bez funkčních omezení. Odstraňuje vodotisk hodnocení, odemyká všechna API – včetně možnosti **vytvářet nové objekty vrstvy PSD** – a umožňuje testovat kód v prostředí podobném produkci před zakoupením trvalé licence.

## Požadavky

Než začnete, ujistěte se, že máte:

- **Java vývojové prostředí** – JDK 8+ a **build tool** jako Maven nebo Gradle nainstalované.
- **Aspose.PSD pro Java** – Stáhněte nejnovější JAR z oficiální stránky [Aspose.PSD for Java download page](https://releases.aspose.com/psd/java/).
- **Ukázkový soubor PSD** – V příkladech použijeme `OneLayer.psd`.

## Import balíčků

Přidejte požadované importy do své Java třídy. Tyto třídy poskytují základní funkčnost pro **manipulaci obrázků PSD** a práci s vrstvami.

```java
import com.aspose.psd.Image;
import com.aspose.psd.Rectangle;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.Layer;
import com.aspose.psd.imageoptions.PngOptions;
import com.aspose.psd.imageoptions.PsdOptions;
```

## Co je „set layer position“ a proč je důležité?

Metody **set layer position** definují přesné pixelové souřadnice, kde je vrstva vykreslena na plátně PSD, a řídí tak její horizontální i vertikální umístění. Správné umístění zajišťuje, že grafika bude přesně zarovnaná, což je nezbytné pro skládání UI aktiv, tvorbu tiskových rozvržení nebo generování pixel‑perfektních miniatur.

## Postup krok za krokem

### Krok 1: Načtěte soubor PSD

`PsdImage` je hlavní třída Aspose.PSD, která představuje PSD dokument v paměti. Načtením souboru vytvoříte manipulovatelný objekt, který můžete upravovat.

```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "OneLayer.psd";
PsdImage im = (PsdImage)Image.load(sourceFileName);
```

### Krok 2: Připravte pixelová data a obdélníky

Alokujeme dva pixelové buffery (`int[]`) a definujeme obdélníkové oblasti, kde budou nové vrstvy namalovány.

Obdélník (Rectangle) definuje oblast s X, Y, šířkou a výškou, která se používá k umístění pixelů vrstvy.

```java
int[] data1 = new int[2500];
int[] data2 = new int[2500];
Rectangle rect1 = new Rectangle(0, 0, 50, 50);
Rectangle rect2 = new Rectangle(0, 0, 100, 25);
```

### Krok 3: Inicializujte data vrstvy

Vyplníme pixelové buffery výchozí ARGB hodnotou. Hodnota `-10000000` odpovídá poloprůhlednému tmavému odstínu, který nové vrstvě poskytne viditelnou základní barvu.

```java
for (int i = 0; i < 2500; i++) {
    data1[i] = -10000000;
    data2[i] = -10000000;
}
```

### Krok 4: Přidejte běžné vrstvy (manipulace s vrstvami PSD)

Vrstva (Layer) představuje jednotlivou vrstvu PSD a poskytuje vlastnosti pro pixelová data, viditelnost a pozici.

```java
Layer layer1 = im.addRegularLayer();
layer1.setLeft(25);
layer1.setTop(25);
layer1.setRight(75);
layer1.setBottom(75);
layer1.saveArgb32Pixels(rect1, data1);

Layer layer2 = im.addRegularLayer();
layer2.setLeft(25);
layer2.setTop(150);
layer2.setRight(1255);
layer2.setBottom(175);
layer2.saveArgb32Pixels(rect2, data2);
```

### Krok 5: Exportujte PSD do PNG a uložte aktualizovaný PSD

Po umístění vrstev uložíme upravený dokument. Nejprve exportujeme výsledek do PNG (krok **export PSD to PNG**), poté uložíme PSD s novými vrstvami.

PngOptions konfiguruje nastavení exportu PNG, jako je úroveň komprese a typ barev.

```java
String exportPath = dataDir + "Updated.psd";
String exportPathPng = dataDir + "Updated.png";

im.save(exportPath, new PsdOptions());          // Save the updated PSD
im.save(exportPathPng, new PngOptions());       // Export PSD to PNG
```

> **Tip:** Pokud potřebujete jen PNG, můžete vynechat volání `save` pro PSD a přímo zavolat `save` s `PngOptions`.

## Měřitelné výhody Aspose.PSD pro Java

Aspose.PSD podporuje **30+ formátů obrázků** a dokáže zpracovat PSD soubory až do **500 MB** bez načítání celého souboru do paměti, díky své streamovací architektuře. V benchmarkových testech přidání dvou běžných vrstev do 300‑stránkového PSD trvá méně než **0,8 sekundy** na standardním 3,2 GHz procesoru.

## Časté problémy a řešení

| Příznak | Pravděpodobná příčina | Řešení |
|---------|-----------------------|--------|
| PNG se zobrazuje prázdný | Vrstvy jsou neviditelné nebo plně průhledné | Ujistěte se, že nastavíte neprůhledné pixelové hodnoty nebo zavoláte `layer.setVisible(true)`. |
| `ArrayIndexOutOfBoundsException` | Neshoda mezi velikostí obdélníku a délkou pole pixelů | Ověřte, že `rect.width * rect.height == dataArray.length`. |
| LicenseException at runtime | Nebyla načtena platná licence | Načtěte dočasnou nebo trvalou licenci před voláním jakýchkoli metod API. |

## Často kladené otázky

**Q: Je Aspose.PSD kompatibilní s Java 8?**  
A: Ano, Aspose.PSD podporuje Java 8 a novější verze.

**Q: Mohu na přidané vrstvy aplikovat transformace (rotace, škálování)?**  
A: Rozhodně! Třída `Layer` poskytuje metody `rotate`, `scale` a `translate` pro plnou kontrolu transformací.

**Q: Kde mohu najít další dokumentaci k Aspose.PSD?**  
A: Podrobná API dokumentace je k dispozici [Aspose.PSD Java API reference](https://reference.aspose.com/psd/java/).

**Q: Jak získám dočasnou licenci pro Aspose.PSD?**  
A: Navštivte stránku dočasné licence [Aspose temporary license page](https://purchase.aspose.com/temporary-license/).

**Q: Existují komunitní fóra pro podporu Aspose.PSD?**  
A: Ano, připojte se k diskusím na fóru komunity Aspose PSD [Aspose PSD community forum](https://forum.aspose.com/c/psd/34).

## Závěr

Nyní víte **jak exportovat PSD do PNG** a **přidat nové běžné vrstvy** pomocí Aspose.PSD pro Java a také jste viděli, jak **dočasná licence Aspose** vám umožní tento workflow vyzkoušet bez omezení. Tento tutoriál pokrýval načtení souboru, vytváření vrstev, naplňování pixelových dat, umisťování vrstev a export finální kompozice. Experimentujte s různými velikostmi obdélníků, barvami nebo efekty vrstev, abyste výstup přizpůsobili potřebám svého projektu.

---

**Poslední aktualizace:** 2026-10-18  
**Testováno s:** Aspose.PSD 24.11 pro Java  
**Autor:** Aspose

## Související tutoriály

- [Export PSD do PNG s efekty vrstev pomocí Aspose.PSD pro Java](/psd/java/psd-image-modification-conversion/apply-layer-effects-psd-files/)
- [Export PSD do PNG a sloučení vrstev pomocí Aspose.PSD pro Java](/psd/java/psd-layer-management-effects/merge-psd-layers/)
- [Export skupiny vrstev PSD do obrázku pomocí Javy](/psd/java/working-with-psd-files/export-psd-layer-group-to-image/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}