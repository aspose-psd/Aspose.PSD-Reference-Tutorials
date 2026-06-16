---
date: 2026-03-07
description: Naučte se, jak vytvořit vodoznak obrázku v souborech PSD pomocí Aspose.PSD
  pro Javu – rychlý průvodce zpracováním PSD obrázků a ochranou vašich grafik.
linktitle: How to Create Image Watermark in PSD Files with Aspose.PSD for Java
second_title: Aspose.PSD Java API
title: Jak vytvořit vodoznak obrázku v souborech PSD pomocí Aspose.PSD pro Javu
url: /cs/java/modifying-converting-psd-images/add-watermark-psd-files/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Přidání vodoznaku do souborů PSD pomocí Aspose.PSD pro Java

## Úvod
Vodoznaky jsou nenápadný, ale účinný způsob, jak chránit vaše obrázky a komunikovat vlastnictví. V tomto tutoriálu se naučíte, jak **create image watermark** v souborech PSD pomocí Aspose.PSD pro Java. Ať už jste fotograf, který představuje své portfolio, nebo designér prezentující své nejnovější práce, přidání vodoznaku může být klíčové pro udržení identity značky. Takže si dejte šálek kávy, pohodlně se usaďte a pojďme na to!

## Rychlé odpovědi
- **Jaký je hlavní cíl?** Vytvořit image watermark v souboru PSD programově.  
- **Která knihovna se používá?** Aspose.PSD for Java.  
- **Jak dlouho trvá implementace?** Přibližně 10‑15 minut pro základní vodoznak.  
- **Jaké jsou hlavní předpoklady?** Java JDK, knihovna Aspose.PSD a zdrojový soubor PSD.  
- **Mohu výsledek exportovat jako PNG?** Ano – použijte metodu `save` s `PngOptions`.

## Co je **create image watermark**?
Vytvoření image watermark znamená programově překrytí semi‑transparentního textu nebo grafiky na soubor obrázku tak, aby informace o vlastnictví byly vloženy přímo do vizuálního obsahu.

## Proč použít Aspose.PSD pro Java pro zpracování psd obrázků?
Aspose.PSD poskytuje bohatou sadu API pro **psd image processing**, umožňující manipulaci s vrstvami, aplikaci efektů a vykreslení finálního obrázku bez potřeby Photoshopu. Podporuje vysoce věrné vykreslování, dávkové operace a funguje na všech hlavních operačních systémech.

## Předpoklady
Než se pustíte do kódu, ujistěte se, že máte následující:

1. **Java Development Kit (JDK)** – jakákoli aktuální verze (8 nebo vyšší).  
2. **Aspose.PSD for Java Library** – stáhněte z [webu Aspose](https://releases.aspose.com/psd/java/).  
3. **IDE** – Eclipse, IntelliJ IDEA nebo jakýkoli editor, který preferujete.  
4. **PSD File** – ukázkový soubor pojmenovaný `layers.psd` umístěný ve vašem pracovním adresáři.  
5. **Basic Java knowledge** – znalost tříd, objektů a souborového I/O.

## Import balíčků
Nyní, když máte vše nastavené, importujme potřebné balíčky. Importy v Javě vám umožňují přinést třídy a funkce z různých knihoven, což činí váš kód efektivnějším. Níže je to, co budete potřebovat:

```java
import com.aspose.psd.Color;
import com.aspose.psd.Font;
import com.aspose.psd.Graphics;
import com.aspose.psd.Image;
import com.aspose.psd.RectangleF;
import com.aspose.psd.StringAlignment;
import com.aspose.psd.StringFormat;
import com.aspose.psd.brushes.SolidBrush;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.PngOptions;
```

## Jak **create image watermark** – Průvodce krok za krokem

### Krok 1: Nastavte svůj adresář
Nejprve musíme nastavit cestu, kde se nachází váš soubor PSD. To je klíčové, protože Java potřebuje vědět, kde najít vaše soubory.

```java
String dataDir = "Your Document Directory";
```

Nahraďte `Your Document Directory` skutečnou složkou, která obsahuje `layers.psd`.

### Krok 2: Načtěte soubor PSD
Dále načteme soubor PSD a přetypujeme jej na `PsdImage`. Tento krok převádí soubor do formátu, který můžeme manipulovat.

```java
PsdImage psdImage = (PsdImage) Image.load(dataDir + "layers.psd");
```

Představte si to jako otevření knihy, abyste na jejích stránkách mohli psát.

### Krok 3: Vytvořte objekt Graphics
Po načtení souboru PSD potřebujeme vytvořit objekt `Graphics`. Ten nám umožní provádět kreslicí operace – v podstatě jako vzít štětec pro vaše plátno.

```java
Graphics graphics = new Graphics(psdImage);
```

### Krok 4: Definujte písmo pro váš vodoznak
Nyní je čas vybrat, jak bude váš vodoznak vypadat. Použijeme Arial s velikostí písma 20. Klidně změňte název písma nebo velikost, aby odpovídaly stylu vaší značky.

```java
Font font = new Font("Arial", 20.0f);
```

### Krok 5: Vytvořte pevný štětec pro vodoznak
Pevný štětec poskytne vašemu vodoznaku barvu a neprůhlednost. Nastavíme alfu na 50 (z 255) pro semi‑transparentní šedou.

```java
SolidBrush brush = new SolidBrush(Color.fromArgb(50, 128, 128, 128));
```

Zde `Color.fromArgb(50, 128, 128, 128)` vytváří šedou barvu s 50 % neprůhledností – ideální pro nenápadný podpis.

### Krok 6: Nastavte zarovnání řetězce pro váš vodoznak
Aby se vodoznak objevil přesně uprostřed obrázku, nakonfigurujeme možnosti zarovnání řetězce.

```java
StringFormat sf = new StringFormat();
sf.setAlignment(StringAlignment.Center);
sf.setLineAlignment(StringAlignment.Center);
```

### Krok 7: Vykreslete vodoznak pomocí **java graphics drawstring**
Nyní přichází ta vzrušující část. S připraveným grafickým kontextem vykreslíme text vodoznaku na obrázek pomocí `java graphics drawstring`.

```java
graphics.drawString("Some watermark text", font, brush, new RectangleF(0, 0, psdImage.getWidth(), psdImage.getHeight()), sf);
```

Nahraďte `"Some watermark text"` skutečným textem, který chcete, aby se objevil v souboru PSD.

### Krok 8: **Save PSD as PNG** – **export psd png**
Jakmile je vodoznak na místě, **save psd png** (tj. exportujeme PSD do PNG), aby výsledek bylo možné zobrazit v libovolném prohlížeči nebo prohlížeči obrázků.

```java
psdImage.save(dataDir + "AddWatermark_output.png", new PngOptions());
```

Spuštěním tohoto řádku se vytvoří nový soubor PNG, který obsahuje váš vodoznak.

## Časté problémy a řešení
- **Vodoznak není vidět?** Ověřte hodnotu alfy v `Color.fromArgb()`; nižší hodnota způsobí, že bude vodoznak průhlednější.  
- **Nesprávné rozměry?** Ujistěte se, že používáte `psdImage.getWidth()` a `psdImage.getHeight()` pro obdélník, aby se text přizpůsobil velikosti obrázku.  
- **Licence výjimky?** Dočasná evaluační licence funguje pro testování, ale pro produkční použití je vyžadována plná licence.

## Často kladené otázky

**Q: Mohu přizpůsobit text vodoznaku?**  
A: Rozhodně! Stačí nahradit řetězec v metodě `drawString` požadovaným textem.

**Q: Co když chci jiné písmo?**  
A: Změňte vytvoření `Font` na libovolné nainstalované písmo, např. `new Font("Times New Roman", 24.0f)`.

**Q: Existuje způsob, jak upravit neprůhlednost?**  
A: Ano – upravte první parametr `Color.fromArgb(alpha, r, g, b)`. Nižší hodnoty `alpha` zvyšují průhlednost.

**Q: Mohu použít jiné formáty obrázků než PNG?**  
A: Samozřejmě. Nahraďte `new PngOptions()` za `new JpegOptions()` nebo `new BmpOptions()`, abyste **save psd png** v jiném formátu.

**Q: Kde mohu najít další pomoc?**  
A: Pro podrobné dotazy navštivte [fóra Aspose](https://forum.aspose.com/c/psd/34) nebo si prohlédněte jejich [dokumentaci](https://reference.aspose.com/psd/java/).

## Závěr
Nyní jste se naučili, jak **create image watermark** v souboru PSD pomocí Aspose.PSD pro Java. Tato technika nejen zabezpečuje váš obsah, ale také posiluje přítomnost vaší značky napříč všemi vizuálními materiály. Experimentujte s různými písmy, barvami a úrovněmi neprůhlednosti, aby odpovídaly vašemu stylu, a pamatujte, že můžete **save psd png** nebo **export psd png** do libovolného formátu, který potřebujete.

---

**Poslední aktualizace:** 2026-03-07  
**Testováno s:** Aspose.PSD for Java 24.11  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}