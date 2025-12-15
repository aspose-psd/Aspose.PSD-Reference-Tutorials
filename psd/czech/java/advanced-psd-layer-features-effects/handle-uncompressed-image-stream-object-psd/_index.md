---
date: 2025-12-13
description: Naučte se, jak vytvořit objekt grafiky PSD a manipulovat s vrstvami PSD
  pomocí zpracování nekomprimovaných obrazových toků s Aspose.PSD pro Javu.
linktitle: Handle Uncompressed Image Stream Object in PSD - Java
second_title: Aspose.PSD Java API
title: Vytvořit objekt grafiky PSD – nekomprimovaný stream v Javě
url: /cs/java/advanced-psd-layer-features-effects/handle-uncompressed-image-stream-object-psd/
weight: 26
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Vytvoření objektu PSD Graphics – nekomprimovaný stream v Javě

## Úvod
Vítejte ve světě manipulace s obrázky v Javě! V tomto tutoriálu **vytvoříte objekt PSD graphics** a budete pracovat s nekomprimovanými streamy obrázků pomocí Aspose.PSD pro Java. Ať už jste grafický designér, který chce automatizovat své pracovní postupy, nebo vývojář, který chce integrovat výkonné možnosti zpracování obrázků do svých aplikací, tento průvodce je určen právě pro vás. Provedeme vás všemi kroky od předpokladů až po závěr, abyste získali pevné pochopení, jak začít s Aspose.PSD.

## Rychlé odpovědi
- **Co znamená „vytvořit objekt PSD graphics“?** Jedná se o vytvoření grafického kontextu pro soubor PSD, abyste mohli kreslit nebo upravovat jeho obsah.  
- **Která knihovna zpracovává nekomprimované streamy?** Aspose.PSD pro Java poskytuje plnou podporu pro raw (nekomprimovaná) data obrázku.  
- **Potřebuji licenci pro vývoj?** Bezplatná zkušební verze funguje pro testování; pro produkci je vyžadována komerční licence.  
- **Mohu po vytvoření objektu graphics manipulovat s vrstvami PSD?** Ano – instance Graphics vám umožní kreslit na libovolnou vrstvu.  

## Požadavky
Než se pustíme do kódu, ujistěte se, že máte vše potřebné k zahájení této cesty. Zde jsou požadavky:

### Java Development Kit (JDK)
Ujistěte se, že máte na svém počítači nainstalovaný JDK. Můžete jej stáhnout z webu Oracle nebo použít OpenJDK.

### Aspose.PSD for Java
Musíte si stáhnout a nainstalovat knihovnu Aspose.PSD. Tato výkonná knihovna vám umožní snadno manipulovat se soubory PSD. Nejnovější verzi získáte z [tohoto odkazu](https://releases.aspose.com/psd/java/).

### Integrated Development Environment (IDE)
Je dobré použít IDE pro psaní a testování vašeho Java kódu. Můžete použít IntelliJ IDEA, Eclipse nebo jakýkoli jiný, který vám vyhovuje.

### Basic Understanding of Java
Základní znalost programování v Javě proces usnadní. Ujistěte se, že ovládáte základy jako třídy, metody a zpracování výjimek.

S vším připraveným si svlékněte rukávy a pojďme na to – kódování!

## Import balíčků
Abychom mohli začít, musíme naimportovat potřebné balíčky pro práci s Aspose.PSD. Níže najdete importy, které obvykle potřebujete pro práci se soubory PSD.

```java
import com.aspose.psd.Graphics;
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.CompressionMethod;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.PsdOptions;
import java.io.ByteArrayInputStream;
import java.io.ByteArrayOutputStream;
```

Nyní rozdělíme kód na stravitelné kroky, abyste mohli snadno sledovat postup. Nastavíme, načteme soubor PSD, upravíme jej a uložíme výstup.

## Krok 1: Definujte adresář dokumentu
Než začnete psát kód, budete chtít definovat, kde se váš soubor PSD nachází. Toto je v podstatě nastavení scény pro váš projekt.

```java
String dataDir = "Your Document Directory";
```

Nahraďte `"Your Document Directory"` skutečnou cestou, kde se nachází váš soubor PSD (např. layers.psd). To vám usnadní vyhledávání souborů bez zbytečných komplikací.

## Krok 2: Vytvořte ByteArrayOutputStream
Potřebujete místo, kam uložit upravený obrázek, než s ním něco uděláte. `ByteArrayOutputStream` vám pomůže snadno zachytit data obrázku.

```java
ByteArrayOutputStream ms = new ByteArrayOutputStream();
```

Tento řádek inicializuje nový objekt `ByteArrayOutputStream` pojmenovaný `ms`. Tento objekt použijete k uložení vašeho nekomprimovaného obrázku.

## Krok 3: Načtěte soubor PSD
Nyní je čas načíst skutečný soubor PSD. Tady začíná magie!

```java
PsdImage psdImage = (PsdImage) Image.load(dataDir + "layers.psd");
```

Tento řádek načte váš soubor PSD do objektu `PsdImage`. Ujistěte se, že máte správnou cestu; jinak se objeví chyba jako neočekávaný test.

## Krok 4: Nastavte PsdOptions pro ukládání
Musíte specifikovat, jak chcete obrázek uložit – samozřejmě nekomprimovaně!

```java
PsdOptions saveOptions = new PsdOptions();
saveOptions.setCompressionMethod(CompressionMethod.Raw);
```

Zde vytvoříte objekt `PsdOptions` a nastavíte metodu komprese na `Raw`. Tato metoda zajistí, že obrázek si zachová plnou kvalitu a bude uložen bez jakékoli komprese.

## Krok 5: Uložte obrázek do výstupního proudu
```java
psdImage.save(ms, saveOptions);
```

Tento řádek uloží váš upravený obrázek do `ByteArrayOutputStream`, který jste vytvořili v Kroku 2, pomocí možností definovaných v Kroku 4. Metoda `save` se postará o správné zakódování obrázku podle vašich nastavení.

## Krok 6: Resetujte výstupní proud
Po uložení je váš výstupní proud na konci. Musíte jej resetovat, aby se četl od začátku.

```java
ms.reset();
```

Metoda `reset` připraví váš `ByteArrayOutputStream` k opětovnému čtení od začátku. Představte si to jako přetočení pásky před poslechem vaší oblíbené písně!

## Krok 7: Načtěte nově vytvořený obrázek
```java
PsdImage img = (PsdImage) Image.load(new ByteArrayInputStream(ms.toByteArray()));
```

Zde načteme obrázek zpět z `ByteArrayOutputStream` do nového objektu `PsdImage`. Toto je místo, kde můžete zkontrolovat výsledky své předchozí práce.

## Krok 8: Vytvořte objekt Graphics
Pro další úpravy nebo vykreslení obrázku budete potřebovat vytvořit objekt graphics.

```java
Graphics graphics = new Graphics(psdImage);
```

Tento řádek inicializuje objekt `Graphics` pomocí vašeho `psdImage`. Nyní můžete tento objekt graphics použít k kreslení nebo manipulaci s obrázkem podle potřeby. Je to jako mít štětec v ruce!

## Manipulace s vrstvami PSD pomocí objektu Graphics
Nyní, když máte instanci **Graphics**, můžete **manipulovat vrstvami PSD** – například kreslit tvary, přidávat text nebo aplikovat filtry na konkrétní vrstvu. Kontext graphics pracuje přímo na podkladových pixelových datech, což vám dává detailní kontrolu nad vzhledem každé vrstvy.

## Časté problémy a řešení
- **NullPointerException při načítání souboru** – dvakrát zkontrolujte cestu `dataDir` a ujistěte se, že je název souboru správný.  
- **Komprimovaný výstup i přes použití Raw** – ověřte, že je před voláním `save` zavolána metoda `saveOptions.setCompressionMethod(CompressionMethod.Raw);`.  
- **Objekt Graphics se zdá být prázdný** – ujistěte se, že kreslíte na správnou instanci `PsdImage` (použijte tu, kterou jste načetli, ne nově vytvořenou, pokud to není zamýšlené).

## Často kladené otázky
### Co je Aspose.PSD?
Aspose.PSD je .NET knihovna, která umožňuje vývojářům programově vytvářet, upravovat a manipulovat se soubory Photoshop PSD a souvisejícími formáty obrázků.

### Jak mohu stáhnout Aspose.PSD pro Javu?
Můžete jej stáhnout ze [stránky vydání](https://releases.aspose.com/psd/java/).

### Existuje bezplatná zkušební verze Aspose.PSD?
Ano, bezplatnou zkušební verzi můžete získat [zde](https://releases.aspose.com/).

### Mohu získat podporu pro Aspose.PSD?
Samozřejmě! Pomoc můžete hledat na [fóru podpory Aspose](https://forum.aspose.com/c/psd/34).

### Jak mohu získat dočasnou licenci pro Aspose.PSD?
Stačí navštívit [stránku dočasné licence](https://purchase.aspose.com/temporary-license/) a můžete začít.

## Často kladené otázky
**Q: Mohu použít objekt graphics k úpravě jen jedné konkrétní vrstvy?**  
A: Ano. Po načtení PSD vyberte požadovanou vrstvu pomocí `psdImage.getLayers().get_Item(index)` a předávejte ji konstruktoru `Graphics`.

**Q: Ovlivňuje metoda komprese Raw velikost souboru?**  
A: Raw ukládá pixelová data bez komprese, takže velikost souboru bude větší než u komprimovaných PSD, ale kvalita obrazu zůstane nedotčena.

**Q: Je možné exportovat upravený PSD do jiného formátu (např. PNG)?**  
A: Rozhodně. Po úpravách použijte vhodnou přetížení `Image.save` s `PngOptions`.

**Q: Jaká verze Javy je požadována?**  
A: Aspose.PSD pro Java podporuje JDK 8 a novější.

**Q: Jak uvolním zdroje po zpracování?**  
A: Zavolejte `psdImage.dispose()` a zavřete všechny proudy, aby se uvolnily nativní zdroje.

---  

**Last Updated:** 2025-12-13  
**Testováno s:** Aspose.PSD for Java (latest release)  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}