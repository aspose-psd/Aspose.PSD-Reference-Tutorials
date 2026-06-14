---
date: 2026-03-15
description: Naučte se, jak komprimovat soubory PNG pomocí Aspose.PSD pro Javu – krok
  za krokem průvodce, jak komprimovat PNG, optimalizovat velikost PNG a efektivně
  převádět PSD na PNG.
linktitle: Compress PNG Files using Aspose.PSD for Java
second_title: Aspose.PSD Java API
title: Jak komprimovat PNG soubory pomocí Aspose.PSD pro Java
url: /cs/java/optimizing-png-files/compress-png-files/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Jak komprimovat soubory PNG pomocí Aspose.PSD pro Java

## Úvod

Když jde o práci s obrázky ve vývoji softwaru, naučit se **jak komprimovat PNG** soubory efektivně může dramaticky zlepšit dobu načítání stránek a snížit spotřebu šířky pásma. Aspose.PSD pro Java je výkonná knihovna, která vám umožní pracovat se soubory Photoshop (PSD) a exportovat je do různých formátů, včetně PNG. Ať už potřebujete **optimalizovat velikost PNG**, převést PSD na PNG pro webovou galerii, nebo jemně doladit **úrovně komprese PNG**, tento tutoriál vás provede kompletním, připraveným příkladem pro produkční nasazení.

## Rychlé odpovědi
- **Co znamená „jak komprimovat PNG“?** Jedná se o snížení velikosti souboru PNG obrázku při zachování vizuální kvality, typicky úpravou parametrů komprese.  
- **Která knihovna je nejlepší pro kompresi PNG v Javě?** Aspose.PSD pro Java nabízí vestavěné možnosti PNG a podporuje celé spektrum úrovní komprese (0‑9).  
- **Potřebuji licenci?** Bezplatná zkušební verze funguje pro hodnocení; pro produkční použití je vyžadována komerční licence.  
- **Mohu automatizovat více úrovní komprese?** Ano — pomocí smyčky přes vlastnost `setCompressionLevel` můžete generovat PNG soubory na každé úrovni.  
- **Je tento přístup vhodný pro velké soubory PSD?** Rozhodně; Aspose.PSD streamuje data efektivně, což je bezpečné i pro vysoce rozlišená aktiva.

## Co je komprese PNG?

PNG používá bezztrátovou kompresi, což znamená, že kvalita obrazu zůstává nedotčena, zatímco se snižuje velikost souboru. Úpravou **úrovně komprese PNG** (0 = žádná komprese, 9 = maximální komprese) řídíte, jak agresivně jsou data sbalená. Vyšší úrovně trvají o něco déle, ale přinášejí menší soubory — ideální pro optimalizaci webu.

## Proč použít Aspose.PSD pro Java k kompresi PNG?

- **Plná podpora PSD** — otevírejte, upravujte a exportujte vrstvy PSD bez ztráty informací.  
- **Granulární kontrola** — nastavte přesné úrovně komprese PNG, typ barvy i bitovou hloubku.  
- **Cross‑platform** — funguje v jakémkoli prostředí kompatibilním s Javou, od desktopových aplikací po cloudové služby.  
- **Výkon** — optimalizovaný nativní kód zajišťuje rychlé zpracování i pro velké obrázky.  

## Předpoklady

Než se ponoříme do kódu, ověřte, že máte následující:

1. **Java JDK** — stáhněte nejnovější JDK z [webových stránek Oracle](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).  
2. **Aspose.PSD pro Java knihovna** — stáhněte nejnovější JAR z oficiální stránky ke stažení [zde](https://releases.aspose.com/psd/java/).  
3. **IDE nebo editor kódu** — IntelliJ IDEA, Eclipse nebo VS Code budou fungovat perfektně.  
4. **Základní znalost Javy** — znalost práce s výjimkami a souborovým I/O urychlí učební křivku.  
5. **Ukázkový soubor PSD** — umístěte soubor PSD (např. `sample.psd`) do složky, na kterou budete odkazovat jako na adresář dokumentu.

Mít tyto položky připravené vám umožní soustředit se na **java image optimization** kroky místo řešení nastavení.

## Import balíčků

Následující importy vám poskytují přístup ke klíčovým třídám Aspose.PSD a možnostem PNG:

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.PngOptions;
```

Tyto třídy vám umožní načíst PSD, nakonfigurovat nastavení PNG a uložit výsledek.

## Krok 1: Nastavte svůj projekt

Vytvořte nový Java projekt (např. `PsdImageCompressor`) a přidejte Aspose.PSD JAR do cesty sestavení. Tím zajistíte, že kompilátor najde výše zmíněné třídy.

## Krok 2: Definujte adresář dokumentu

Dejte programu vědět, kde najde zdrojový soubor PSD a kam má zapisovat komprimované PNG:

```java
String dataDir = "Your Document Directory"; // Replace with actual path
```

Nahraďte `"Your Document Directory"` absolutní nebo relativní cestou, která obsahuje `sample.psd`. Udržování cesty konfigurovatelné usnadňuje **convert PSD to PNG** v různých prostředích.

## Krok 3: Načtěte PSD obrázek

Načtěte soubor PSD do paměti. Tento krok je analogický otevření knihy před čtením:

```java
PsdImage psdImage = (PsdImage)Image.load(dataDir + "sample.psd");
```

Pokud soubor není nalezen, Aspose.PSD vyhodí informativní výjimku — zkontrolujte název souboru a cestu.

## Krok 4: Smyčka přes úrovně komprese

Pro prozkoumání každé možné **png compression level** použijeme jednoduchou `for` smyčku. Tím automaticky vytvoříme devět dalších PNG, každé s jiným nastavením komprese:

```java
for (int i = 0; i <= 9; i++) {
    // Create a new instance of PngOptions
    PngOptions options = new PngOptions();
    options.setCompressionLevel(i); // Set the compression level
```

Smyčka běží od 0 (žádná komprese) do 9 (maximální komprese) a poskytuje jasný obrázek o kompromisu mezi velikostí souboru a časem zpracování.

## Krok 5: Uložte komprimované PNG soubory

Uvnitř smyčky uložte každé PNG pod názvem, který odráží úroveň komprese. To usnadní porovnání:

```java
    psdImage.save(dataDir + i + "_out.png", options);
}
```

Po dokončení smyčky budete mít soubory pojmenované `0_out.png`, `1_out.png`, … `9_out.png` ve vašem adresáři.

## Časté problémy a řešení

| Problém | Proč se vyskytuje | Řešení |
|-------|----------------|-----|
| **FileNotFoundException** | Nesprávná cesta `dataDir` nebo chybějící `sample.psd`. | Ověřte řetězec cesty a ujistěte se, že soubor PSD existuje. |
| **OutOfMemoryError** u velkých PSD | Načítání obrovského PSD bez dostatečné haldy. | Zvyšte haldu JVM (`-Xmx2g`) nebo zpracovávejte obrázek po částech. |
| **Komprimovaný PNG vypadá nezměněně** | Používáte nízkou úroveň komprese (0‑2). | Zvyšte úroveň na 5‑9 pro patrné zmenšení velikosti. |
| **LicenseException** | Spouštíte bez platné licence Aspose.PSD. | Aplikujte zkušební licenci nebo zakupte plnou licenci. |

## Často kladené otázky

**Q: Co je Aspose.PSD pro Java?**  
A: Aspose.PSD pro Java je knihovna, která vývojářům umožňuje programově manipulovat se soubory Photoshop, včetně čtení, úprav a exportu do formátů jako PNG, JPEG a TIFF.

**Q: Můžu komprimovat i jiné formáty obrázků než PNG?**  
A: Tento tutoriál se zaměřuje na PNG, ale Aspose.PSD podporuje PSD, TIFF, JPEG, BMP a další. Stačí změnit třídu výstupních možností na požadovaný formát.

**Q: Potřebuji licenci k použití Aspose.PSD?**  
A: K vyhodnocení můžete použít bezplatnou zkušební verzi, ale pro produkční nasazení je nutná plná licence. Licenci můžete získat [zde](https://purchase.aspose.com/buy).

**Q: Co když při spuštění kódu narazím na chybu?**  
A: Zkontrolujte cesty k souborům, ujistěte se, že jsou všechny importy přítomny, a ověřte, že používáte kompatibilní verzi Aspose.PSD JAR.

**Q: Kde najdu další dokumentaci k Aspose.PSD pro Java?**  
A: Podrobné API reference a další příklady jsou k dispozici na [Aspose.PSD reference](https://reference.aspose.com/psd/java/).

---

**Poslední aktualizace:** 2026-03-15  
**Testováno s:** Aspose.PSD pro Java 24.12 (nejnovější v době psaní)  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}