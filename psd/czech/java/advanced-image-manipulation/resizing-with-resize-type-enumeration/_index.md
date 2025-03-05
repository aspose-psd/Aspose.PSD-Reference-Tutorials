---
title: Změna velikosti pomocí Resize Type Enumeration v Aspose.PSD pro Javu
linktitle: Změna velikosti pomocí výčtu typu Resize
second_title: Aspose.PSD Java API
description: Zvládněte změnu velikosti obrázku v Javě s Aspose.PSD. Podrobný průvodce pomocí výčtu typu změny velikosti.
type: docs
weight: 18
url: /cs/java/advanced-image-manipulation/resizing-with-resize-type-enumeration/
---
## Zavedení

V neustále se vyvíjejícím prostředí vývoje v Javě je efektivní zpracování obrazu klíčovým aspektem, se kterým se vývojáři často potýkají. Aspose.PSD for Java se ukazuje jako výkonné řešení, které poskytuje bezproblémový zážitek pro změnu velikosti obrázků s přidanou výhodou Resize Type Enumeration. V tomto tutoriálu se ponoříme do složitosti změny velikosti obrázků pomocí Aspose.PSD pro Java a rozebereme každý krok, abychom zajistili komplexní pochopení.

## Předpoklady

Než se pustíte do tohoto kurzu, ujistěte se, že máte splněny následující předpoklady:

1. Vývojové prostředí Java: Ujistěte se, že máte na svém počítači nastavené vývojové prostředí Java.

2. Knihovna Aspose.PSD: Stáhněte a nainstalujte knihovnu Aspose.PSD z[webové stránky](https://releases.aspose.com/psd/java/).

3.  Ukázkový soubor PSD: Připravte si ukázkový soubor PSD k experimentování. Můžete použít[sample.psd](Váš adresář dokumentů/sample.psd) pro tento výukový program.

## Importujte balíčky

Chcete-li začít, importujte potřebné balíčky do svého projektu Java:

```java
import com.aspose.psd.Image;
import com.aspose.psd.ResizeType;

import com.aspose.psd.imageoptions.JpegOptions;
```

## Krok 1: Načtěte obrázek

 Začněte načtením existujícího obrázku do instance souboru`RasterImage` třída. Použijte následující fragment kódu:

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

// Načtěte existující obrázek do instance třídy RasterImage
Image image = Image.load(sourceFile);
```

## Krok 2: Změňte velikost obrázku

Nyní změňte velikost načteného obrázku pomocí Resize Type Enumeration. V tomto příkladu používáme metodu Lanczos Resample:

```java
image.resize(300, 300, ResizeType.LanczosResample);
```

## Krok 3: Uložte obrázek se změněnou velikostí

Po změně velikosti uložte obrázek se zadanými rozměry a zvoleným typem změny velikosti. Zde jej uložíme jako soubor JPEG:

```java
String destName = dataDir + "ResizingwithResizeTypeEnumeration_out.jpg";
image.save(destName, new JpegOptions());
```

A tady to máte! Úspěšně jste změnili velikost obrázku pomocí Resize Type Enumeration v Aspose.PSD pro Java.

Závěrem lze říci, že Aspose.PSD for Java poskytuje robustní platformu pro manipulaci s obrázky a Resize Type Enumeration přidává tomuto procesu vrstvu flexibility. Ať už pracujete na malém projektu nebo na rozsáhlé aplikaci, zvládnutí těchto kroků vám umožní bezproblémově zvládnout změnu velikosti obrázku.

## FAQ

### Q1: Je Aspose.PSD for Java vhodný pro malé i velké projekty?

A1: Rozhodně! Aspose.PSD for Java je navržen tak, aby vyhovoval projektům všech velikostí a poskytoval škálovatelnost a efektivitu.

### Q2: Mohu použít jiný typ změny velikosti než Lanczos Resample?

Odpověď 2: Ano, Aspose.PSD pro Java nabízí různé typy změn velikosti, například Nejbližší soused, Bkubický a další. Úplný seznam najdete v dokumentaci.

### Q3: Kde najdu další podporu pro Aspose.PSD pro Java?

 A3: Máte-li jakékoli dotazy nebo pomoc, navštivte stránku[Fórum Aspose.PSD](https://forum.aspose.com/c/psd/34).

### Q4: Je k dispozici bezplatná zkušební verze pro Aspose.PSD pro Java?

 A4: Ano, máte přístup k bezplatné zkušební verzi[zde](https://releases.aspose.com/).

### Q5: Jak mohu získat dočasnou licenci pro Aspose.PSD pro Java?

 A5: Chcete-li získat dočasnou licenci, navštivte[tento odkaz](https://purchase.aspose.com/temporary-license/).