---
date: 2026-01-01
description: Prozkoumejte, jak oříznout obrázek v Javě pomocí Aspose.PSD pro Javu.
  Postupujte podle našeho krok‑za‑krokem návodu, jak načíst soubor PSD, oříznout obdélník
  obrázku a převést PSD na JPEG.
linktitle: Crop Image by Rectangle
second_title: Aspose.PSD Java API
title: 'Oříznutí obrázku v Javě: Oříznutí obrázku obdélníkem pomocí Aspose.PSD'
url: /cs/java/image-editing/crop-image-by-rectangle/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Crop Image Java: Ořezání obrázku obdélníkem pomocí Aspose.PSD

## Úvod

Manipulace s grafikou je běžnou součástí **java image processing** a Aspose.PSD for Java vám poskytuje čisté, výkonné API pro práci se soubory PSD. V tomto tutoriálu se naučíte **jak oříznout obrázek** pomocí obdélníku, načíst soubor PSD a nakonec převést výsledek na JPEG – vše pomocí několika řádků Java kódu.

## Rychlé odpovědi
- **Co znamená „crop image java“?** Odkazuje na oříznutí obrázku na definovaný obdélník pomocí Java kódu.  
- **Která knihovna operaci provádí?** Aspose.PSD for Java poskytuje potřebné třídy.  
- **Potřebuji licenci pro testování?** Je k dispozici bezplatná zkušební verze; licence je vyžadována pro produkční nasazení.  
- **Mohu oříznutý PSD převést na JPEG?** Ano – použijte `JpegOptions` při ukládání.  
- **Jak dlouho trvá implementace?** Obvykle méně než 10 minut pro základní scénář.

## Co je ořezání obrázku obdélníkem v Javě?

Ořezání obrázku obdélníkem znamená výběr konkrétní oblasti (definované X, Y, šířkou a výškou) a zahazování všeho mimo tuto oblast. Tato operace je běžná, když potřebujete zaměřit se na konkrétní část většího PSD dokumentu.

## Proč použít Aspose.PSD pro tento úkol?

- **Žádné externí závislosti** – funguje s čistou Javou.  
- **Podporuje PSD, PNG, JPEG a mnoho dalších formátů** – můžete **převést PSD na JPEG** okamžitě.  
- **Vysoká věrnost renderování** – zachovává informace o vrstvách a barevných profilech během ořezu.  

## Předpoklady

- Nainstalovaný Java Development Kit (JDK).  
- Knihovna Aspose.PSD for Java – stáhněte ji z [webové stránky](https://releases.aspose.com/psd/java/).  

## Import balíčků

Ujistěte se, že ve svém Java projektu zahrnete potřebné balíčky pro využití funkcí Aspose.PSD for Java. Přidejte následující importy na začátek svého Java souboru:

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;
import com.aspose.psd.Rectangle;

import com.aspose.psd.imageoptions.JpegOptions;
```

Nyní rozdělíme proces do několika kroků, abychom vás provedli ořezáním obrázku obdélníkem pomocí Aspose.PSD for Java.

## Krok 1: Nastavte adresář dokumentů

```java
String dataDir = "Your Document Directory";
```

Nahraďte `"Your Document Directory"` skutečnou cestou, kde se nachází váš soubor PSD.

## Krok 2: Zadejte zdrojové a cílové soubory

```java
String sourceFile = dataDir + "sample.psd";
String destName = dataDir + "CroppingByRectangle_out.jpg";
```

Definujte cesty pro váš zdrojový soubor PSD a cílový soubor JPEG.

## Krok 3: Načtěte a cachujte obrázek

```java
RasterImage rasterImage = (RasterImage)Image.load(sourceFile);

if (!rasterImage.isCached()) {
    rasterImage.cacheData();
}
```

Zde **načteme soubor PSD** do instance `RasterImage` a uložíme jeho data do cache pro zlepšení výkonu.

## Krok 4: Vytvořte a definujte ořezový obdélník

```java
Rectangle rectangle = new Rectangle(20, 20, 20, 20);
```

Vytvořte instanci třídy `Rectangle` s požadovanou velikostí pro ořez. Parametry představují **X**, **Y**, **šířku** a **výšku**.

## Krok 5: Ořízněte a uložte obrázek

```java
rasterImage.crop(rectangle);
rasterImage.save(destName, new JpegOptions());
```

Proveďte operaci ořezu pomocí zadaného obdélníku a **převést PSD na JPEG** uložením výsledku s `JpegOptions`.

Opakujte tyto kroky podle potřeby a upravujte parametry podle vašich konkrétních požadavků.

## Časté problémy a tipy

- **Obdélník mimo hranice obrázku** – ujistěte se, že souřadnice obdélníku jsou v rozměrech zdrojového obrázku.  
- **Spotřeba paměti** – po dokončení zavolejte `rasterImage.dispose()` pro uvolnění nativních zdrojů.  
- **Kontrola kvality** – můžete nastavit `JpegOptions.setQuality(int)` pro řízení úrovně komprese výstupního JPEG.

## Závěr

V tomto tutoriálu jsme prošli proces **crop image java** obdélníkem pomocí Aspose.PSD for Java. Dodržením těchto kroků můžete snadno integrovat výkonné možnosti manipulace s obrázky – načtení souboru PSD, ořez specifické oblasti a převod výsledku na JPEG – do jakékoli Java aplikace.

## Často kladené otázky

### Q1: Mohu použít Aspose.PSD for Java s jinými Java frameworky?

A1: Ano, Aspose.PSD for Java lze integrovat s různými Java frameworky, což poskytuje flexibilitu ve vašich vývojových projektech.

### Q2: Je k dispozici bezplatná zkušební verze Aspose.PSD for Java?

A2: Ano, bezplatnou zkušební verzi můžete získat [zde](https://releases.aspose.com/).

### Q3: Kde najdu další podporu nebo pomoc?

A3: Navštivte [Aspose.PSD forum](https://forum.aspose.com/c/psd/34) pro komunitní podporu a diskuse.

### Q4: Jak získám dočasnou licenci pro Aspose.PSD for Java?

A4: Dočasnou licenci můžete získat [zde](https://purchase.aspose.com/temporary-license/).

### Q5: Jaké formáty obrázků jsou podporovány pro ořez v Aspose.PSD for Java?

A5: Aspose.PSD for Java podporuje různé formáty obrázků, včetně PSD, PNG, JPEG a dalších.

---

**Poslední aktualizace:** 2026-01-01  
**Testováno s:** Aspose.PSD for Java 24.12  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}