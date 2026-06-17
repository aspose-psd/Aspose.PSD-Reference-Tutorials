---
date: 2026-02-17
description: Naučte se, jak exportovat PSD do PNG a pracovat s nekomprimovanými obrazovými
  proudy pomocí Aspose.PSD pro Javu.
linktitle: Handle Uncompressed Image Stream Object in PSD - Java
second_title: Aspose.PSD Java API
title: Exportovat PSD do PNG – Vytvořit objekt PSD Graphics – Neukomprimovaný stream
  v Javě
url: /cs/java/advanced-psd-layer-features-effects/handle-uncompressed-image-stream-object-psd/
weight: 26
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Export PSD do PNG – Vytvoření objektu PSD Graphics – Nezkomprimovaný proud v Javě

## Úvod
Vítejte ve světě manipulace s obrázky v Javě! V tomto tutoriálu **vytvoříte objekt PSD graphics**, budete pracovat s nezkomprimovanými proudy obrázků a naučíte se, jak **exportovat PSD do PNG** pomocí Aspose.PSD pro Java. Ať už jste grafický designér, který chce automatizovat své workflow, nebo vývojář, který chce do svých aplikací integrovat výkonné funkce zpracování obrázků, tento průvodce je určen právě pro vás. Provedeme vás všemi kroky od předpokladů až po finální export, abyste měli pevné pochopení celého procesu.

## Rychlé odpovědi
- **Co znamená “vytvořit objekt PSD graphics”?** Jedná se o vytvoření grafického kontextu pro soubor PSD, abyste mohli kreslit nebo upravovat jeho obsah.  
- **Která knihovna zpracovává nezkomprimované proudy?** Aspose.PSD pro Java poskytuje plnou podporu pro surová (nezkomprimovaná) data obrázku.  
- **Mohu po úpravě exportovat PSD do PNG?** Ano — jakmile máte objekt `Graphics`, můžete PSD vykreslit a uložit jako PNG.  
- **Potřebuji licenci pro vývoj?** Pro testování stačí bezplatná zkušební verze; pro produkční nasazení je vyžadována komerční licence.  
- **Je export bezztrátový?** Export do PNG zachovává kvalitu obrazu, přičemž velikost souboru je větší než u JPEG, ale menší než u nezkomprimovaného PSD.  

## Jak exportovat PSD do PNG pomocí Aspose.PSD pro Java
Když potřebujete **exportovat PSD do PNG**, typický postup je:

1. Načtěte soubor PSD (nebo jej vytvořte).  
2. Proveďte libovolné kreslení nebo manipulaci vrstev pomocí objektu `Graphics`.  
3. Uložte výsledný obrázek pomocí `PngOptions` (stejný instance `Graphics` lze znovu použít).  

I když se tento tutoriál zaměřuje na práci s nezkomprimovanými proudy, stejný objekt `Graphics`, který vytvoříte, můžete později v pipeline použít k vykreslení PSD do souboru PNG.

## Požadavky
Než se pustíme do kódu, ujistěte se, že máte vše potřebné k zahájení této cesty. Zde jsou požadavky:

### Java Development Kit (JDK)
Ujistěte se, že máte na svém počítači nainstalovaný JDK. Můžete jej stáhnout z webu Oracle nebo použít OpenJDK.

### Aspose.PSD pro Java
Musíte si stáhnout a nainstalovat knihovnu Aspose.PSD. Tato výkonná knihovna vám umožní snadno manipulovat se soubory PSD. Nejnovější verzi získáte na [této stránce](https://releases.aspose.com/psd/java/).

### Integrated Development Environment (IDE)
Je vhodné použít IDE pro psaní a testování Java kódu. Můžete použít IntelliJ IDEA, Eclipse nebo jakékoli jiné, které vám vyhovuje.

### Základní znalost Javy
Základní povědomí o programování v Javě proces usnadní. Ujistěte se, že ovládáte základy jako třídy, metody a zpracování výjimek.

S vším připraveným si zapřáhněte rukávy a pojďme na to – kódování!

## Import balíčků
Abychom mohli začít, musíme importovat potřebné balíčky pro práci s Aspose.PSD. Níže najdete typické importy, které budete potřebovat pro manipulaci se soubory PSD.

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

## Krok 1: Definujte adresář dokumentů
Než začnete programovat, budete chtít definovat, kde se váš soubor PSD nachází. Tím nastavíte základ pro svůj projekt.

```java
String dataDir = "Your Document Directory";
```

Nahraďte `"Your Document Directory"` skutečnou cestou, kde je umístěn váš soubor PSD (např. `layers.psd`). To vám usnadní práci se soubory bez zbytečných potíží.

## Krok 2: Vytvořte ByteArrayOutputStream
Potřebujete místo, kam uložíte upravený obrázek, než s ním něco uděláte. `ByteArrayOutputStream` vám pomůže snadno zachytit data obrázku.

```java
ByteArrayOutputStream ms = new ByteArrayOutputStream();
```

Tento řádek inicializuje nový objekt `ByteArrayOutputStream` pojmenovaný `ms`. Tento objekt použijete k uložení vašeho nezkomprimovaného obrázku.

## Krok 3: Načtěte soubor PSD
Nyní je čas načíst skutečný soubor PSD. Tady začíná kouzlo!

```java
PsdImage psdImage = (PsdImage) Image.load(dataDir + "layers.psd");
```

Tento řádek načte váš soubor PSD do objektu `PsdImage`. Ujistěte se, že máte správnou cestu; jinak se objeví chyba jako neočekávaný test.

## Krok 4: Nastavte PsdOptions pro uložení
Musíte specifikovat, jak chcete obrázek uložit — nezkomprimovaně, samozřejmě!

```java
PsdOptions saveOptions = new PsdOptions();
saveOptions.setCompressionMethod(CompressionMethod.Raw);
```

Zde vytvoříte objekt `PsdOptions` a nastavíte metodu komprese na `Raw`. Tato metoda zajistí, že obrázek si zachová plnou kvalitu a bude uložen bez jakékoli komprese.

## Krok 5: Uložte obrázek do výstupního proudu
```java
psdImage.save(ms, saveOptions);
```

Tento řádek uloží váš upravený obrázek do `ByteArrayOutputStream`, který jste vytvořili ve Krok 2, pomocí možností definovaných ve Krok 4. Metoda `save` se postará o správné kódování obrázku podle vašich nastavení.

## Krok 6: Resetujte výstupní proud
Po uložení je výstupní proud na konci. Musíte jej resetovat, aby bylo možné číst od začátku.

```java
ms.reset();
```

Metoda `reset` připraví váš `ByteArrayOutputStream` na čtení od začátku znovu. Představte si to jako přetočení pásky před poslechem oblíbené skladby!

## Krok 7: Načtěte nově vytvořený obrázek
```java
PsdImage img = (PsdImage) Image.load(new ByteArrayInputStream(ms.toByteArray()));
```

Zde načteme obrázek zpět z `ByteArrayOutputStream` do nového objektu `PsdImage`. Tady můžete zkontrolovat výsledky své předchozí práce.

## Krok 8: Vytvořte objekt Graphics
Pro další úpravy nebo vykreslení obrázku budete potřebovat vytvořit objekt graphics.

```java
Graphics graphics = new Graphics(psdImage);
```

Tento řádek inicializuje objekt `Graphics` pomocí vašeho `psdImage`. Nyní můžete tento objekt použít k kreslení nebo manipulaci s obrázkem podle potřeby. Je to jako mít štětec v ruce!

## Manipulace s vrstvami PSD pomocí objektu Graphics
Jakmile máte instanci **Graphics**, můžete **manipulovat vrstvami PSD** — například kreslit tvary, přidávat text nebo aplikovat filtry na konkrétní vrstvu. Grafický kontext pracuje přímo s podkladovými pixelovými daty a poskytuje jemnou kontrolu nad vzhledem každé vrstvy.

## Časté problémy a řešení
- **NullPointerException při načítání souboru** — zkontrolujte cestu `dataDir` a ujistěte se, že je název souboru správný.  
- **Komprimovaný výstup i přes nastavení Raw** — ověřte, že je volána `saveOptions.setCompressionMethod(CompressionMethod.Raw);` před metodou `save`.  
- **Objekt Graphics je prázdný** — ujistěte se, že kreslíte na správnou instanci `PsdImage` (použijte tu, kterou jste načetli, ne nově vytvořenou, pokud to není zamýšlené).

## Často kladené otázky
### Co je Aspose.PSD?
Aspose.PSD je .NET knihovna, která umožňuje vývojářům programově vytvářet, upravovat a manipulovat soubory Photoshop PSD a související formáty obrázků.

### Jak si mohu stáhnout Aspose.PSD pro Java?
Můžete jej stáhnout ze [stránky vydání](https://releases.aspose.com/psd/java/).

### Existuje bezplatná zkušební verze Aspose.PSD?
Ano, bezplatnou zkušební verzi získáte [zde](https://releases.aspose.com/).

### Mohu získat podporu pro Aspose.PSD?
Samozřejmě! Pomoc můžete hledat na [fóru podpory Aspose](https://forum.aspose.com/c/psd/34).

### Jak mohu získat dočasnou licenci pro Aspose.PSD?
Stačí navštívit [stránku dočasné licence](https://purchase.aspose.com/temporary-license/) a můžete začít.

## Často kladené otázky

**Q: Mohu použít objekt graphics k úpravě pouze jedné konkrétní vrstvy?**  
**A:** Ano. Po načtení PSD vyberte požadovanou vrstvu pomocí `psdImage.getLayers().get_Item(index)` a předávejte ji konstruktoru `Graphics`.

**Q: Ovlivňuje metoda komprese Raw velikost souboru?**  
**A:** Raw ukládá pixelová data bez komprese, takže velikost souboru bude větší než u komprimovaných PSD, ale kvalita obrazu zůstane nedotčena.

**Q: Je možné exportovat upravený PSD do jiného formátu (např. PNG)?**  
**A:** Rozhodně. Po úpravách použijte vhodnou přetíženou metodu `Image.save` s `PngOptions` – to je standardní způsob, jak **exportovat PSD do PNG**.

**Q: Jaká verze Javy je požadována?**  
**A:** Aspose.PSD pro Java podporuje JDK 8 a novější.

**Q: Jak uvolním prostředky po zpracování?**  
**A:** Zavolejte `psdImage.dispose()` a zavřete všechny proudy, aby se uvolnily nativní zdroje.

---

**Poslední aktualizace:** 2026-02-17  
**Testováno s:** Aspose.PSD pro Java (nejnovější vydání)  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}