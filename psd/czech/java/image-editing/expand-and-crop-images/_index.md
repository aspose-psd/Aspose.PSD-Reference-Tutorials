---
date: 2026-01-07
description: Naučte se, jak oříznout obrázek v Javě pomocí Aspose.PSD pro Javu. Podrobný
  návod krok za krokem pro ořezávání obrázků, změnu velikosti a konverzi z PSD do
  JPEG.
linktitle: Expand and Crop Images
second_title: Aspose.PSD Java API
title: 'Ořezávání obrázku v Javě - Rozšíření a ořezávání obrázků pomocí Aspose.PSD
  pro Javu'
url: /cs/java/image-editing/expand-and-crop-images/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Oříznutí obrázku v Javě: Rozšíření a oříznutí obrázků pomocí Aspose.PSD pro Java

## Úvod

V tomto tutoriálu se dozvíte, jak **crop image java** pomocí knihovny Aspose.PSD. Ať už potřebujete rozšířit plátno, oříznout nežádoucí okraje nebo převést soubor PSD na JPEG, níže uvedené kroky vás provedou čistým, opakovatelným procesem. Probereme předpoklady, importy a každý krok kódu s jasnými vysvětleními, abyste techniku mohli použít v reálných projektech.

## Rychlé odpovědi
- **Jaká knihovna provádí crop image java?** Aspose.PSD pro Java.  
- **Potřebuji licenci pro vývoj?** Pro testování stačí bezplatná zkušební verze; pro produkci je vyžadována komerční licence.  
- **Mohu převést PSD na JPEG při ořezávání?** Ano, pomocí `JpegOptions` společně s ořezovým obdélníkem.  
- **Je podporována Java 8?** Aspose.PSD podporuje Java 8 a novější verze.  
- **Jak dlouho trvá implementace?** Obvykle méně než 10 minut pro základní operaci ořezání.

## Co je “crop image java”?

Ořezání obrázku v Javě znamená vybrat obdélníkovou oblast ze zdrojového obrázku a zbytek zahodit. S Aspose.PSD můžete tuto oblast definovat pomocí objektu `Rectangle` a poté výsledek uložit v jiném formátu, například JPEG.

## Proč použít Aspose.PSD pro ořezání obrázků v Javě?

- **Plná podpora PSD** – pracujte přímo s vrstvenými soubory PSD bez předchozí konverze.  
- **Vysoce výkonné zpracování rastru** – efektivní využití paměti i pro velké obrázky.  
- **Vestavěná konverze** – snadno exportujte do JPEG, PNG, BMP atd., přičemž můžete aplikovat ořezání nebo rozšíření plátna.  
- **Cross‑platform** – funguje na jakémkoli systému, který podporuje Javu.

## Předpoklady

Než se pustíme do kódu, ujistěte se, že máte:

1. **Java Development Kit (JDK)** – nainstalovanou Java 8 nebo novější.  
2. **Aspose.PSD pro Java** – stáhněte knihovnu z oficiálního webu **[zde](https://releases.aspose.com/psd/java/)**.  

> **Tip:** Přidejte JAR Aspose.PSD do classpath vašeho projektu nebo do Maven/Gradle závislostí, aby nedošlo k `ClassNotFoundException`.

## Import balíčků

Přidejte požadované importy do svého Java souboru. Tyto třídy vám umožní načíst obrázek, manipulovat s rasterem, definovat obdélník a nastavit možnosti exportu JPEG.

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;
import com.aspose.psd.Rectangle;

import com.aspose.psd.imageoptions.JpegOptions;
```

## Krok 1: Nastavte adresář dokumentů

Určete složku, která obsahuje zdrojový soubor PSD. Nahraďte zástupný text skutečnou cestou na vašem počítači.

```java
String dataDir = "Your Document Directory";
```

## Krok 2: Zadejte vstupní a výstupní cesty

Definujte, odkud se má PSD načíst a kam se má uložit oříznutý JPEG.

```java
String sourceFile = dataDir + "example1.psd";
String destName = dataDir + "jpeg_out.jpg";
```

## Krok 3: Načtěte a cachujte obrázek

Načtěte PSD do objektu `RasterImage`. Cachování zlepšuje výkon pro následné operace, jako je ořezání.

```java
RasterImage rasterImage = (RasterImage)Image.load(sourceFile);
rasterImage.cacheData();
```

## Krok 4: Vytvořte obdélník pro ořezání

Vytvořte `Rectangle`, který popisuje oblast, kterou chcete zachovat. Souřadnice mohou být záporné, aby **rozšířily** plátno před ořezáním – užitečné pro přidání okraje kolem původního obrázku.

```java
Rectangle destRect = new Rectangle(-200, -200, 300, 300);
```

> **Proč použít záporné souřadnice?**  
> Záporné hodnoty X/Y posunou oblast ořezu doleva/dolů, čímž efektivně přidají prázdný prostor (rozšíří plátno) kolem původního obsahu před finálním ořezáním.

## Krok 5: Uložte oříznutý obrázek

Nakonec uložte výsledný obrázek pomocí `JpegOptions`. Tento krok také ukazuje **convert psd jpeg** při aplikaci ořezového obdélníku.

```java
rasterImage.save(destName, new JpegOptions(), destRect);
```

> **Výsledek:** `jpeg_out.jpg` nyní obsahuje obrázek o rozměrech 300 × 300 pixelů, který byl rozšířen o 200 px na každé straně a poté oříznut na definovaný obdélník.

Gratulujeme! Úspěšně jste provedli **java image cropping**, rozšířili plátno a převedli soubor PSD na JPEG – vše během několika stručných řádků kódu.

## Běžné scénáře použití

- **Příprava assetů pro web** – ořízněte a změňte velikost screenshotů nebo návrhů před nahráním.  
- **Generování náhledů** – extrahujte konkrétní oblast z velkého PSD pro ukázky.  
- **Automatizované dávkové zpracování** – projděte složku se soubory PSD a aplikujte stejný ořezový obdélník na každý z nich.

## Řešení problémů a tipy

| Problém | Navrhované řešení |
|---------|-------------------|
| `OutOfMemoryError` při načítání velkých PSD | Zavolejte `rasterImage.cacheData()` brzy a zvažte zvýšení velikosti haldy JVM (`-Xmx`). |
| Ořezaná oblast není ve středu | Ověřte posuny X/Y obdélníku; nezapomeňte, že záporné hodnoty rozšiřují plátno. |
| Výstupní JPEG je rozmazaný | Upravit nastavení kvality v `JpegOptions` (např. `new JpegOptions { Quality = 90 }`). |

## Často kladené otázky

### Q1: Je Aspose.PSD kompatibilní s různými verzemi Javy?

A1: Ano, Aspose.PSD podporuje různé verze Javy, což zajišťuje kompatibilitu s širokou škálou vývojových prostředí.

### Q2: Mohu Aspose.PSD používat v komerčních projektech?

A2: Rozhodně, Aspose.PSD poskytuje komerční licence pro vývojáře, což umožňuje jeho použití jak v osobních, tak v komerčních projektech.

### Q3: Existují omezení podporovaných formátů souborů obrázků?

A3: Aspose.PSD podporuje řadu formátů, včetně PSD, JPEG, PNG a dalších. Kompletní seznam najdete v [dokumentaci](https://reference.aspose.com/psd/java/).

### Q4: Jak získám podporu pro dotazy týkající se Aspose.PSD?

A4: Navštivte [forum Aspose.PSD](https://forum.aspose.com/c/psd/34), kde můžete požádat o pomoc komunitu nebo tým podpory Aspose.

### Q5: Je k dispozici bezplatná zkušební verze?

A5: Ano, můžete si vyzkoušet Aspose.PSD s bezplatnou zkušební verzí. Stáhněte ji [zde](https://releases.aspose.com/).

---

**Poslední aktualizace:** 2026-01-07  
**Testováno s:** Aspose.PSD pro Java 24.12  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}