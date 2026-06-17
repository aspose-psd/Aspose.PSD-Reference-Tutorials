---
date: 2026-04-08
description: Naučte se, jak exportovat PSD do PNG a vytvořit novou vrstvu PSD pomocí
  Aspose.PSD pro Javu s dočasnou licencí Aspose. Tento krok za krokem tutoriál pokrývá
  manipulaci s obrázkem PSD a nastavení pozice vrstvy.
keywords:
- aspose temporary license
- set layer position
- psd image manipulation
- create new psd layer
linktitle: Přidat novou běžnou vrstvu do PSD
second_title: Aspose.PSD Java API
title: Exportujte PSD do PNG a přidejte novou běžnou vrstvu pomocí Aspose.PSD pro
  Javu – dočasná licence Aspose
url: /cs/java/advanced-image-effects/add-new-regular-layer/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Exportovat PSD do PNG a přidat novou běžnou vrstvu pomocí Aspose.PSD pro Java

## Úvod

V tomto **aspose psd tutorial** objevíte, jak **exportovat PSD do PNG** a zároveň **vytvořit novou běžnou vrstvu** ve stejném souboru, **použitím dočasné licence Aspose** pro vývoj. Ať už potřebujete generovat web‑připravené náhledy, připravovat aktiva pro designový pipeline, nebo jen experimentovat s **psd image manipulation**, Aspose.PSD pro Java vám poskytuje plnou programovou kontrolu. Provedeme vás každým krokem – od načtení zdrojového souboru až po uložení jak aktualizovaného PSD, tak kopie PNG – abyste mohli okamžitě začít manipulovat s vrstvami PSD.

## Rychlé odpovědi
- **Mohu exportovat PSD do PNG jedním voláním?** Ano, po přidání vrstev můžete zavolat `save` s `PngOptions`.
- **Potřebuji licenci pro vývoj?** Dočasná licence funguje pro testování; plná licence je vyžadována pro produkci.
- **Která verze Javy je podporována?** Aspose.PSD funguje s Java 8 a novějšími.
- **Je umístění vrstvy založeno na pixelech?** Ano, nastavujete souřadnice left, top, right, bottom v pixelech pomocí metod **set layer position**.
- **Zachová PNG průhlednost vrstev?** PNG bude obsahovat sloučený výsledek všech viditelných vrstev.

## Proč použít dočasnou licenci Aspose?

Dočasná licence **aspose** vám umožní vyzkoušet kompletní sadu funkcí Aspose.PSD bez jakýchkoli funkčních omezení. Odstraní vodotisk pro hodnocení, odemkne všechna API – včetně možnosti **create new psd layer** objektů – a umožní vám testovat kód v prostředí podobném produkci před zakoupením trvalé licence.

## Požadavky

Before you begin, ensure you have:

- **Java Development Environment** – JDK 8+ a nainstalovaný nástroj pro sestavení (Maven/Gradle).
- **Aspose.PSD for Java** – Stáhněte nejnovější JAR z oficiálního webu [here](https://releases.aspose.com/psd/java/).
- **Ukázkový soubor PSD** – V příkladech použijeme `OneLayer.psd`.

## Import balíčků

Add the required imports to your Java class. These classes provide the core functionality for **psd image manipulation** and layer handling.

```java
import com.aspose.psd.Image;
import com.aspose.psd.Rectangle;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.Layer;
import com.aspose.psd.imageoptions.PngOptions;
import com.aspose.psd.imageoptions.PsdOptions;
```

## Co je „set layer position“ a proč je důležité?

Když přidáte novou vrstvu, musíte definovat, kde se objeví na plátně. Metody `setLeft`, `setTop`, `setRight` a `setBottom` **set layer position** v pixelových souřadnicích. Správné umístění zajišťuje, že vaše grafika bude přesně tam, kde ji očekáváte, což je klíčové pro úkoly jako skládání UI aktiv nebo příprava souborů připravených k tisku.

## Průvodce krok za krokem

### Krok 1: Načíst soubor PSD

Nejprve načtěte existující PSD, který chcete upravit. Tím získáte objekt `PsdImage`, se kterým můžete pracovat.

```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "OneLayer.psd";
PsdImage im = (PsdImage)Image.load(sourceFileName);
```

### Krok 2: Připravit pixelová data a obdélníky

Vytvoříme dva pixelové buffery (`int[]`) a definujeme obdélníkové oblasti, kde budou nové vrstvy namalovány. Toto je základ pro **creating a new psd layer**.

```java
int[] data1 = new int[2500];
int[] data2 = new int[2500];
Rectangle rect1 = new Rectangle(0, 0, 50, 50);
Rectangle rect2 = new Rectangle(0, 0, 100, 25);
```

### Krok 3: Inicializovat data vrstvy

Naplníme pixelové buffery výchozí hodnotou ARGB. Hodnota `-10000000` odpovídá poloprůhlednému tmavému odstínu.

```java
for (int i = 0; i < 2500; i++) {
    data1[i] = -10000000;
    data2[i] = -10000000;
}
```

### Krok 4: Přidat běžné vrstvy (Manipulovat s PSD vrstvami)

Nyní **add regular layers** do PSD obrázku a **set layer position** pomocí vlastností left, top, right a bottom. Toto ukazuje, jak programově **manipulate PSD layers**.

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

### Krok 5: Exportovat PSD do PNG a uložit aktualizovaný PSD

Po umístění vrstev uložte upravený dokument. Nejprve exportujeme výsledek do PNG (krok **export psd to png**), poté uložíme PSD s novými vrstvami.

```java
String exportPath = dataDir + "Updated.psd";
String exportPathPng = dataDir + "Updated.png";

im.save(exportPath, new PsdOptions());          // Save the updated PSD
im.save(exportPathPng, new PngOptions());       // Export PSD to PNG
```

> **Tip:** Pokud potřebujete jen PNG, můžete přeskočit volání `save` pro PSD a přímo zavolat `save` s `PngOptions`.

## Časté problémy a řešení

| Příznak | Pravděpodobná příčina | Oprava |
|---------|-----------------------|--------|
| PNG se zobrazuje prázdné | Vrstvy jsou neviditelné nebo zcela průhledné | Ujistěte se, že nastavujete neprůhledné pixelové hodnoty nebo zavoláte `layer.setVisible(true)`. |
| `ArrayIndexOutOfBoundsException` | Nesoulad mezi velikostí obdélníku a délkou pole pixelů | Ověřte, že `rect.width * rect.height == dataArray.length`. |
| LicenseException at runtime | Nebyla načtena platná licence | Načtěte dočasnou nebo trvalou licenci před voláním jakýchkoli API metod. |

## Často kladené otázky

**Q: Je Aspose.PSD kompatibilní s Java 8?**  
A: Ano, Aspose.PSD podporuje Java 8 a novější verze.

**Q: Mohu na přidané vrstvy aplikovat transformace (rotace, škálování)?**  
A: Rozhodně! Třída `Layer` poskytuje metody jako `rotate`, `scale` a `translate` pro úplnou kontrolu transformací.

**Q: Kde mohu najít další dokumentaci k Aspose.PSD?**  
A: Podrobné API dokumenty jsou k dispozici [here](https://reference.aspose.com/psd/java/).

**Q: Jak získám dočasnou licenci pro Aspose.PSD?**  
A: Navštivte stránku dočasné licence [here](https://purchase.aspose.com/temporary-license/).

**Q: Existují komunitní fóra pro podporu Aspose.PSD?**  
A: Ano, připojte se k diskusím na fórech Aspose [here](https://forum.aspose.com/c/psd/34).

## Závěr

Nyní jste se naučili, jak **exportovat PSD do PNG** a **přidávat nové běžné vrstvy** pomocí Aspose.PSD pro Java, a viděli jste, jak **aspose temporary license** umožňuje vyzkoušet tento postup bez omezení. Tento tutoriál představuje základní schopnosti **psd image manipulation**: načítání souboru, vytváření vrstev, naplňování pixelových dat a export finální kompozice. Klidně experimentujte s různými velikostmi obdélníků, barvami pixelů nebo efekty vrstev, abyste výstup přizpůsobili potřebám vašeho projektu.

---

**Poslední aktualizace:** 2026-04-08  
**Testováno s:** Aspose.PSD 24.11 for Java  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}