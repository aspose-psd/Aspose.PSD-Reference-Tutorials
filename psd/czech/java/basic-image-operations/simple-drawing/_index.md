---
date: 2026-06-13
description: Naučte se, jak nakreslit obdélník v souborech PSD pomocí Aspose.PSD pro
  Java. Tento průvodce ukazuje krok za krokem kód, přidávání vrstev, serverové zpracování
  obrázků a kreslení tvarů.
keywords:
- how to draw rectangle
- how to create psd
- java graphics draw rectangle
- server side image processing
- add layer to psd
linktitle: Provést jednoduché kreslení
schemas:
- author: Aspose
  dateModified: '2026-06-13'
  description: Learn how to draw rectangle in PSD files using Aspose.PSD for Java.
    This guide shows step‑by‑step code, adding layers, server‑side image processing
    and shape drawing.
  headline: How to Draw Rectangle in PSD with Aspose.PSD for Java
  type: TechArticle
- questions:
  - answer: Yes, the `Graphics` class also supports drawing ellipses, lines, and custom
      paths via the `drawPath` method.
    question: Can I draw other shapes besides rectangles?
  - answer: Absolutely; you can use `SolidBrush` with an ARGB color to include alpha
      transparency, enabling semi‑transparent overlays.
    question: Does Aspose.PSD support transparency in drawn shapes?
  - answer: Yes, each `Layer` object has a `setOpacity` method that accepts a value
      from 0 to 255, allowing fine‑grained control over layer transparency.
    question: Is it possible to edit the opacity of a layer?
  - answer: Use `PsdImage image = (PsdImage)Image.load("path/to/file.psd");` before
      manipulating layers. The loaded image retains all original layers and masks.
    question: How do I load an existing PSD file instead of creating a new one?
  type: FAQPage
second_title: Aspose.PSD Java API
title: Jak nakreslit obdélník v PSD pomocí Aspose.PSD pro Java
url: /cs/java/basic-image-operations/simple-drawing/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Jak nakreslit obdélník v PSD pomocí Aspose.PSD pro Java

## Úvod

V tomto tutoriálu objevíte **jak nakreslit obdélník** uvnitř souboru Photoshop PSD pomocí čisté Java knihovny Aspose.PSD. Ať už budujete server‑side pipeline pro aktiva, automatizujete tvorbu náhledových obrázků, nebo přidáváte dynamickou grafiku do existujících návrhů, níže uvedené kroky vám poskytnou kompletní, připravené řešení pro produkci. Pokryjeme vytvoření nového PSD dokumentu, přidání vrstvy, vymazání pozadí a nakonec kreslení červených i modrých obdélníků — vše bez spuštění Photoshopu.

## Rychlé odpovědi
- **Jaká je hlavní třída pro vytvoření PSD souboru?** `PsdImage`
- **Která metoda vymaže barvu pozadí vrstvy?** `Graphics.clear(Color)`
- **Jak nakreslíte červený obdélník?** `graphic.drawRectangle(new Pen(Color.getRed()), new Rectangle(...))`
- **Potřebuji licenci pro vývoj?** Bezplatná zkušební verze funguje pro testování; licence je vyžadována pro produkci.
- **Mohu manipulovat s existujícími PSD soubory pomocí stejného API?** Ano, Aspose.PSD podporuje plnou editaci PSD.

## Co znamená kreslení červeného obdélníku v PSD souboru?

Kreslení červeného obdélníku znamená použití objektu `Graphics` k vykreslení obdélníkového tvaru vyplněného nebo obrysmovaného červenou barvou na konkrétní vrstvu PSD obrázku. Tato operace je běžná pro zvýraznění oblastí, vytváření zástupných míst nebo programové přidání jednoduché grafiky.

## Proč používat Aspose.PSD pro Java k manipulaci s PSD soubory?

Aspose.PSD pro Java podporuje **více než 50 vstupních a výstupních formátů**, dokáže zpracovat více než stovky stránek PSD souborů bez načítání celého souboru do paměti a běží na jakékoli platformě, která podporuje Java 8 nebo vyšší. Jeho server‑side engine pro zpracování obrázků eliminuje potřebu Photoshopu, snižuje náklady na licence a umožňuje automatizované pracovní toky, které zvládnou až **10 GB** obrazových dat za hodinu na skromném virtuálním stroji.

## Požadavky

- Java Development Kit (JDK) 8 nebo novější nainstalovaný na vašem počítači.  
- Knihovna Aspose.PSD pro Java. Můžete si ji stáhnout z [Aspose.PSD for Java Documentation](https://reference.aspose.com/psd/java/).

## Import balíčků

`import` příkazy přinášejí požadované třídy do rozsahu, aby bylo možné pracovat s PSD obrázky, vrstvami, barvami a grafikou.

Třída `PsdImage` je nejvyšší objekt Aspose.PSD, který představuje jeden PSD soubor v paměti.  
`Graphics` poskytuje kreslicí primitiva jako čáry, obdélníky a elipsy.  
`Color` a `Pen` vám umožňují určit barvy tahů a tloušťku.  
Třída `Layer` představuje jednotlivou vrstvu obrázku v rámci PSD dokumentu.  
Třída `Rectangle` definuje pozici a velikost obdélníkové oblasti používané pro kreslicí operace.  
Třída `SolidBrush` vyplňuje tvary pevnou barvou.

## Jaký je první krok k vytvoření PSD dokumentu?

Instanciujete `PsdImage` zadáním šířky a výšky plátna v pixelech, což vytvoří prázdnou strukturu PSD souboru. Po nastavení počátečních vrstev nebo pozadí zavoláte metodu `save` s cestou k souboru, aby se dokument zapsal na disk. Tím připravíte obrázek pro následné editační operace.

## Krok 1: Vytvořit nový dokument

Nejprve vytvořte nový PSD dokument s požadovanou velikostí plátna. Tento dokument bude hostit vrstvu, na které budeme kreslit.

```java
import com.aspose.psd.Color;
import com.aspose.psd.Graphics;
import com.aspose.psd.Pen;
import com.aspose.psd.Rectangle;
import com.aspose.psd.brushes.SolidBrush;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.Layer;
```

## Jak přidáte novou prázdnou vrstvu do PSD obrázku?

Nejprve vytvořte novou instanci `Layer` se stejnou šířkou a výškou jako nadřazený `PsdImage`. Poté přidejte tuto vrstvu do kolekce `Layers` obrázku pomocí metody `add`. Jakmile je vrstva součástí obrázku, získejte její objekt `Graphics` pro provádění kreslicích operací; bez tohoto kroku se kresby neobjeví.

## Krok 2: Přidat vrstvu

Dále přidejte novou prázdnou vrstvu, která pokrývá celou šířku a výšku obrázku. Vrstvy jsou nezbytné pro oddělení kreslicích operací.

```java
//ExStart:CreateDocument
String outputDir = "Your Document Directory";
String outPsdFilePath = outputDir + "output.psd";
int width = 100;
int height = 100;

PsdImage image = new PsdImage(width, height);
//ExEnd:CreateDocument
```

## Jaký je účel vymazání barvy pozadí vrstvy?

Volání `Graphics.clear` s konkrétní `Color` vyplní celou vrstvu touto barvou, čímž efektivně resetuje všechna pixelová data. To zajišťuje, že předchozí obsah je odstraněn a vrstva začíná s známým pozadím, což zabraňuje neočekávané průhlednosti nebo míchání barev, když je PSD později otevřen nebo upraven ve Photoshopu.

## Krok 3: Kreslit tvary

Použijeme třídu `Graphics` k manipulaci s pixelovými daty vrstvy. Níže jsou tři příklady, které ilustrují vymazání pozadí a kreslení obdélníků s různými barvami.

### Vymazat barvu vrstvy (nastavit pozadí na žlutou)

```java
//ExStart:AddLayer
Layer layer = new Layer();
layer.setBottom(height);
layer.setRight(width);
image.addLayer(layer);
//ExEnd:AddLayer
```

### Nakreslit červený obdélník (hlavní zaměření)

```java
//ExStart:DrawRectangleYellow
Graphics graphic = new Graphics(layer);
graphic.clear(Color.getYellow());
//ExEnd:DrawRectangleYellow
```

### Nakreslit modrý obdélník (další příklad)

```java
//ExStart:DrawRedRectangle
graphic.drawRectangle(new Pen(Color.getRed()), new Rectangle(30, 10, 40, 80));
//ExEnd:DrawRedRectangle
```

## Jak uložíte upravený PSD soubor na disk?

Použijte metodu `save` na objektu `PsdImage`, předáním úplné cesty k souboru a volitelně specifikací požadovaného formátu obrázku (ve výchozím nastavení PSD). Tím se zapíší všechny vrstvy, masky a kreslicí příkazy do jediného PSD souboru, který splňuje specifikaci Photoshopu, což umožňuje jeho otevření bez varování.

## Krok 4: Uložit změny

Nakonec zapíšete upravený PSD obrázek na disk. Soubor bude obsahovat novou vrstvu a nakreslené tvary.

```java
//ExStart:DrawBlueRectangle
graphic.drawRectangle(new Pen(new SolidBrush(Color.getBlue())), new Rectangle(10, 30, 80, 40));
//ExEnd:DrawBlueRectangle
```

## Časté problémy a řešení

- **Vrstva není po kreslení viditelná:** Ujistěte se, že vrstva je přidána do obrázku **před** vytvořením objektu `Graphics`. Kreslicí plocha musí být připojena k platné vrstvě.
- **Barvy se zobrazují nesprávně:** Ověřte, že používáte `Color.getRed()` (nebo `Color.getBlue()`) místo vytváření vlastního RGB hodnoty, která překračuje rozsah 0‑255.
- **Soubor nebyl uložen:** Potvrďte, že cesta `outputDir` existuje a aplikace má práva k zápisu. V Linuxu může být nutné upravit vlastnictví složky nebo použít `Files.createDirectories`.
- **Pokles výkonu u velkých souborů:** Použijte `setLoadOptions` třídy `PsdImage` k načtení pouze potřebných kanálů, čímž snížíte spotřebu paměti u PSD souborů větších než 200 MB.

## Často kladené otázky

**Q1: Mohu použít Aspose.PSD pro Java k manipulaci s existujícími PSD soubory?**  
A1: Ano, Aspose.PSD pro Java poskytuje rozsáhlou funkčnost pro úpravu a manipulaci s existujícími PSD soubory, včetně přeskupování vrstev, úprav masek a vektorového kreslení.

**Q2: Kde mohu najít podporu pro Aspose.PSD pro Java?**  
A2: Navštívit můžete [Aspose.PSD for Java Forum](https://forum.aspose.com/c/psd/34) pro komunitní pomoc a oficiální odpovědi od Aspose.

**Q3: Je k dispozici bezplatná zkušební verze Aspose.PSD pro Java?**  
A3: Ano, bezplatnou zkušební verzi můžete získat [zde](https://releases.aspose.com/). Zkušební verze obsahuje všechny funkce, ale do uložených souborů přidává vodoznak.

**Q4: Jak mohu zakoupit licenci pro Aspose.PSD pro Java?**  
A4: Licenci můžete zakoupit na [Aspose.PSD Purchase Page](https://purchase.aspose.com/buy). Možnosti licencování zahrnují trvalé, předplatné a licencování pro celé místo.

**Q5: Jsou k dispozici dočasné licence pro Aspose.PSD pro Java?**  
A5: Ano, dočasnou licenci můžete získat [zde](https://purchase.aspose.com/temporary-license/).

## Další často kladené otázky

**Q: Mohu kreslit jiné tvary než obdélníky?**  
A: Ano, třída `Graphics` také podporuje kreslení elips, čar a vlastních cest pomocí metody `drawPath`.

**Q: Podporuje Aspose.PSD průhlednost v kreslených tvarech?**  
A: Rozhodně; můžete použít `SolidBrush` s ARGB barvou pro zahrnutí alfa průhlednosti, což umožňuje poloprůhledné překrytí.

**Q: Je možné upravit neprůhlednost (opacity) vrstvy?**  
A: Ano, každý objekt `Layer` má metodu `setOpacity`, která přijímá hodnotu od 0 do 255, což umožňuje jemné řízení průhlednosti vrstvy.

**Q: Jak načíst existující PSD soubor místo vytvoření nového?**  
A: Použijte `PsdImage image = (PsdImage)Image.load("path/to/file.psd");` před manipulací s vrstvami. Načtený obrázek zachová všechny původní vrstvy a masky.

## Závěr

Nyní jste zvládli **jak nakreslit obdélník** a manipulovat s vrstvami uvnitř PSD souboru pomocí Aspose.PSD pro Java. Vytvořením dokumentu, přidáním vrstvy, vymazáním jejího pozadí a kreslením pomocí API `Graphics` můžete automatizovat nespočet úkolů grafického designu na serverové straně. Experimentujte s různými pery, štětci a efekty vrstev, abyste rozšířili tento základ na plnohodnotné pipeline pro generování obrázků.

```java
//ExStart:SaveChanges
image.save(outPsdFilePath);
//ExEnd:SaveChanges
```

{{< blocks/products/products-backtop-button >}}

## Související tutoriály

- [Jak kreslit tvary v Java – Základní operace s obrázky](/psd/java/basic-image-operations/)
- [Jednoduché změny velikosti s Aspose.PSD – Knihovna pro manipulaci s obrázky v Java](/psd/java/basic-image-operations/simple-resizing/)
- [Oříznout obrázek obdélníkem v Aspose.PSD pro Java](/psd/java/image-editing/crop-image-by-rectangle/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

---

**Poslední aktualizace:** 2026-06-13  
**Testováno s:** Aspose.PSD for Java 24.12 (nejnovější v době psaní)  
**Autor:** Aspose