---
date: 2026-01-17
description: Naučte se, jak vytvořit obrázek Bézierovy křivky v Javě pomocí Aspose.PSD.
  Tento krok‑za‑krokem průvodce zahrnuje techniky kreslení Bézierovy křivky v Javě,
  nastavení šířky pera a export výsledku.
linktitle: How to Create Bezier Curve Image in Java
second_title: Aspose.PSD Java API
title: Jak vytvořit obrázek Bézierovy křivky v Javě
url: /cs/java/java-graphics-drawing/drawing-bezier-curves/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Jak vytvořit obrázek Bezierovy křivky v Javě

## Úvod
Pokud potřebujete **vytvořit obrázek Bezierovy křivky** pro desktopovou nebo server‑side aplikaci v Javě, Aspose.PSD for Java vám práci usnadní. V tomto tutoriálu vás provedeme kreslením hladké Bezierovy křivky, úpravou šířky pera a uložením výsledku jako bitmapy. Na konci budete pohodlně ovládat metodu `drawBezier()` a budete připraveni integrovat vektorovou grafiku do jakéhokoli Java projektu.

## Rychlé odpovědi
- **Jaká knihovna je nejlepší pro kreslení křivek v Javě?** Aspose.PSD for Java poskytuje plnohodnotné grafické API.  
- **Jak dlouho trvá vytvoření základního obrázku Bezierovy křivky?** Obvykle méně než 10 minut po nastavení SDK.  
- **Které formáty obrázků jsou podporovány pro export?** BMP, PNG, JPEG, TIFF a další.  
- **Mohu změnit šířku pera křivky?** Ano – konstruktor `Pen` vám umožní zadat libovolnou šířku, kterou potřebujete.  
- **Potřebuji licenci pro produkční použití?** Komerční licence je vyžadována pro nasazení mimo evaluaci.

## Co znamená „vytvořit obrázek Bezierovy křivky“?
Vytvoření obrázku Bezierovy křivky znamená vygenerovat rastrový obrázek, který obsahuje matematicky definovanou křivku. Křivka je určena počátečním bodem, dvěma řídícími body a koncovým bodem, což vám umožní vytvářet hladké, škálovatelné tvary, které vypadají skvěle v jakékoli velikosti.

## Proč použít Aspose.PSD pro Java?
- **Bohaté grafické primitivy** – kreslete čáry, tvary a křivky bez nutnosti manipulace s pixely na nízké úrovni.  
- **Cross‑platform** – funguje na jakémkoli OS, který podporuje Javu.  
- **Podpora vysokého rozlišení** – pracujte s velkými plátny bez nadměrné spotřeby paměti.  
- **Jednoduchý export** – přepínejte mezi BMP, PNG, JPEG, TIFF jedním řádkem kódu.

## Předpoklady
Před zahájením se ujistěte, že máte:

1. **Java Development Kit (JDK)** – libovolná aktuální verze (8 nebo novější).  
2. **Aspose.PSD for Java JAR** – stáhněte jej z [here](https://releases.aspose.com/psd/java/) a přidejte do classpath vašeho projektu.  
3. **IDE** – Eclipse, IntelliJ IDEA nebo jakýkoli editor dle vašeho výběru, nakonfigurovaný s JDK.

## Import balíčků
Než se ponoříte do implementace, importujte potřebné třídy Aspose.PSD:

```java
import com.aspose.psd.Color;
import com.aspose.psd.Graphics;
import com.aspose.psd.Image;
import com.aspose.psd.Pen;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.BmpOptions;
```

## Průvodce krok za krokem

### Krok 1: Vytvořte instanci obrázku
Nejprve musíte vytvořit instanci třídy `PsdImage`, která představuje PSD obrázek v paměti.

```java
String dataDir = "Your Document Directory";
Image image = new PsdImage(100, 100);
```

*Vysvětlení*: `PsdImage` je vytvořena s šířkou a výškou **100 × 100 pixelů** – tyto hodnoty můžete zvýšit pro výstup s vyšším rozlišením.

### Krok 2: Inicializujte grafický kontext
Dále inicializujte instanci třídy `Graphics`, která provádí kreslicí operace na obrázku.

```java
Graphics graphics = new Graphics(image);
```

*Vysvětlení*: Objekt `Graphics` spojuje kreslicí příkazy s `image`, kterou jsme právě vytvořili.

### Krok 3: Vyčistěte grafický povrch
Vyčistěte grafický povrch pomocí konkrétní barvy pozadí, zde `Color.getYellow()`.

```java
graphics.clear(Color.getYellow());
```

*Vysvětlení*: Nastaví jasně žluté pozadí, aby černá Bezierova křivka vynikla.

### Krok 4: Inicializujte pero pro kreslení
Nastavte objekt `Pen` s vlastnostmi jako barva a šířka, aby definoval, jak bude křivka kreslena.

```java
Pen blackPen = new Pen(Color.getBlack(), 3);
```

*Vysvětlení*: Pero je černé a **3 pixely široké** – šířku můžete upravit, aby byla křivka silnější nebo tenčí (`java graphics pen width`).

### Krok 5: Definujte parametry Bezierovy křivky
Určete řídící body a koncové body pro Bezierovu křivku.

```java
float startX = 10, startY = 25;
float controlX1 = 20, controlY1 = 5;
float controlX2 = 55, controlY2 = 10;
float endX = 90, endY = 25;
```

*Vysvětlení*:  
- `startX`, `startY` – počáteční bod křivky.  
- `controlX1`, `controlY1` – první řídící bod.  
- `controlX2`, `controlY2` – druhý řídící bod.  
- `endX`, `endY` – koncový bod.

### Krok 6: Nakreslete Bezierovu křivku
Použijte metodu `drawBezier()` k nakreslení Bezierovy křivky na obrázek pomocí dříve definovaného `Pen` a řídících bodů.

```java
graphics.drawBezier(blackPen, startX, startY, controlX1, controlY1, controlX2, controlY2, endX, endY);
```

*Vysvětlení*: Tento jediný volání vykreslí hladkou **draw bezier curve java** čáru, která sleduje zadané řídící body.

### Krok 7: Uložte obrázek
Uložte nakreslený obrázek do formátu BMP.

```java
String outpath = dataDir + "Bezier.bmp";
BmpOptions saveOptions = new BmpOptions();
image.save(outpath, saveOptions);
```

*Vysvětlení*: Objekt `BmpOptions` říká Aspose.PSD, aby soubor zapsal jako BMP. Pokud potřebujete jiný formát, zaměňte jej za `PngOptions`, `JpegOptions` atd.

## Časté problémy a řešení
- **Křivka vypadá plochá** – Zkontrolujte souřadnice řídících bodů; nesmí být kolineární s počátečním a koncovým bodem.  
- **Obrázek je prázdný** – Ujistěte se, že je před kreslením zavoláno `graphics.clear()` a že barva pera kontrastuje s pozadím.  
- **OutOfMemoryError při velkých plátnech** – Zvyšte velikost haldy JVM (`-Xmx`) nebo pracujte s dlaždicovými obrázky.

## FAQ
### Mohu v jednom obrázku nakreslit více Bezierových křivek?
Ano, můžete kreslit více křivek opakováním procesu v cyklu a měnit řídící body a koncové body podle potřeby.

### Jak mohu změnit barvu Bezierovy křivky?
Upravte vlastnost `color` objektu `Pen` (`Color.getBlack()` v příkladu) před voláním `drawBezier()`.

### Je Aspose.PSD for Java vhodný pro obrázky s vysokým rozlišením?
Ano, Aspose.PSD for Java podporuje obrázky s vysokým rozlišením a efektivní správou paměti.

### Mohu exportovat obrázek do formátů jiných než BMP?
Ano, Aspose.PSD for Java podporuje export do různých formátů, jako jsou PNG, JPEG, TIFF a další.

### Kde najdu více příkladů a dokumentaci?
Navštivte [Aspose.PSD for Java documentation](https://reference.aspose.com/psd/java/) pro komplexní průvodce a ukázkové kódy.

## Závěr
Po absolvování tohoto **bezier curve tutorial java** nyní víte, jak **vytvořit obrázek Bezierovy křivky** pomocí Aspose.PSD for Java. Experimentujte s různými řídícími body, barvami pera a šířkami čar, abyste získali rozmanité umělecké efekty ve svých Java aplikacích.

---

**Poslední aktualizace:** 2026-01-17  
**Testováno s:** Aspose.PSD for Java 24.12 (nejnovější v době psaní)  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}