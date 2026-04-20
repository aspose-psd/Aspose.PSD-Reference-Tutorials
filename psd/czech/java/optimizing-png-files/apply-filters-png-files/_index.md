---
date: 2026-03-15
description: Naučte se filtrovat PNG obrázky pomocí Aspose.PSD pro Javu. Tento krok‑za‑krokem
  průvodce pokrývá optimalizaci PNG v Javě a převod PSD na PNG s typy filtrů.
linktitle: How to Filter PNG Files in Aspose.PSD for Java
second_title: Aspose.PSD Java API
title: Jak filtrovat soubory PNG v Aspose.PSD pro Javu
url: /cs/java/optimizing-png-files/apply-filters-png-files/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Jak filtrovat PNG soubory v Aspose.PSD pro Java

## Úvod
Pokud se zajímáte o **jak filtrovat PNG** obrázky při práci s Javou, jste na správném místě. V tomto tutoriálu si projdeme použití typů PNG filtrů s Aspose.PSD pro Java, knihovnou, která vám také pomůže **převést PSD na PNG** a provést **optimalizaci PNG v Javě**. Na konci budete schopni jemně ladit kompresi, zlepšit vizuální kvalitu a integrovat proces do jakéhokoli Java projektu.

## Rychlé odpovědi
- **Jaká knihovna podporuje PNG filtrování v Javě?** Aspose.PSD for Java.  
- **Který filtr poskytuje nejlepší kompresi pro většinu obrázků?** Paeth filtr (použitý v tomto příkladu).  
- **Potřebuji licenci pro spuštění kódu?** Bezplatná zkušební verze funguje pro hodnocení; licence je vyžadována pro produkci.  
- **Mohu převést PSD na PNG ve stejném pracovním postupu?** Ano – načtěte PSD a uložte jej jako PNG s požadovaným filtrem.  
- **Jaká verze Javy je požadována?** Java 8 nebo novější.

## Co znamená „jak filtrovat png“ v praxi?
Filtrování PNG souboru znamená výběr předzpracovatelského algoritmu, který připraví pixelová data před kompresí. Typ filtru ovlivňuje velikost souboru a to, jak dobře jsou barvy zachovány po uložení PNG. Aspose.PSD vám poskytuje přímou kontrolu nad tímto krokem pomocí metody `PngOptions.setFilterType`.

## Proč používat Aspose.PSD pro Java PNG optimalizaci?
- **Kompletní podpora PSD:** Otevřete, upravujte a exportujte vrstvy PSD bez ztráty věrnosti.  
- **Vestavěný výběr filtrů:** Vyberte si mezi Paeth, Sub, Up, Average nebo None.  
- **Cross‑platform:** Funguje na Windows, Linuxu i macOS s libovolným standardním JDK.  
- **Žádné externí nativní závislosti:** Čistá Java implementace zjednodušuje nasazení.

## Předpoklady
1. **Java Development Kit (JDK) 8+** – ujistěte se, že `java -version` vrací 1.8 nebo vyšší.  
2. **IDE (IntelliJ IDEA, Eclipse nebo VS Code)** – jakékoli prostředí, ve kterém se cítíte pohodlně.  
3. **Knihovna Aspose.PSD pro Java** – stáhněte ji z [zde](https://releases.aspose.com/psd/java/).  
4. **Základní znalost Javy** – znalost tříd, metod a souborového I/O.

## Import balíčků
Nejprve přidejte požadované třídy Aspose.PSD do vašeho Java souboru:

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.png.PngFilterType;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.PngOptions;
```

> **Tip:** Přidejte JAR Aspose.PSD do cesty sestavení vašeho projektu nebo do Maven/Gradle závislostí, aby importy byly vyřešeny bez chyb.

## Krok 1: Nastavte adresář dokumentu
Definujte složku, která obsahuje váš zdrojový PSD a kam bude uložen filtrovaný PNG.

```java
String dataDir = "Your Document Directory"; // Adjust this path
```

Nahraďte `"Your Document Directory"` absolutní nebo relativní cestou na vašem počítači.

## Krok 2: Načtěte PSD obrázek
Otevřete PSD soubor, který chcete zpracovat. Přetypování na `PsdImage` vám poskytne specifické funkce PSD.

```java
PsdImage psdImage = (PsdImage) Image.load(dataDir + "sample.psd");
```

Pokud soubor chybí, `Image.load` vyhodí výjimku – ujistěte se, že cesta je správná.

## Krok 3: Vytvořte PNG možnosti (Java PNG optimalizace)
Nastavte exportní parametry PNG, včetně typu filtru, který přímo odpovídá na **jak filtrovat png**.

```java
PngOptions options = new PngOptions();
options.setFilterType(PngFilterType.Paeth);
```

Můžete experimentovat s dalšími typy filtrů (`Sub`, `Up`, `Average`, `None`), abyste viděli, jak ovlivňují velikost a kvalitu. Tento krok také ilustruje **java png optimalizaci**, protože zvolený filtr ovlivňuje účinnost komprese.

## Krok 4: Uložte PNG obrázek
Nakonec zapište zpracovaný obrázek zpět na disk pomocí definovaných možností.

```java
psdImage.save(dataDir + "ApplyFilterMethod_out.png", options);
```

Výsledný soubor `ApplyFilterMethod_out.png` bude filtrovaný PNG připravený pro webové nebo desktopové použití.

## Časté problémy a řešení
| Příznak | Pravděpodobná příčina | Oprava |
|---------|-----------------------|--------|
| `FileNotFoundException` | Nesprávná cesta `dataDir` | Ověřte, že řetězec adresáře končí oddělovačem (`/` nebo `\\`). |
| Nebyl pozorován žádný efekt filtru | Použití `PngFilterType.None` | Přepněte na `Paeth` nebo jiný typ filtru. |
| Chyba nedostatku paměti u velkých PSD | Načítání obrovského souboru bez streamování | Použijte `PsdImage` s `loadOptions` pro omezení využití paměti. |

## Často kladené otázky

**Q: Co je Aspose.PSD pro Java?**  
A: Aspose.PSD pro Java je robustní API, které umožňuje vývojářům číst, upravovat a převádět PSD soubory, aplikovat filtry a provádět optimalizace obrázků bez potřeby Adobe Photoshopu.

**Q: Jak si stáhnu Aspose.PSD pro Java?**  
A: Můžete si jej stáhnout ze stránky vydání Aspose [zde](https://releases.aspose.com/psd/java/).

**Q: Můžu Aspose.PSD vyzkoušet zdarma?**  
A: Ano, bezplatná zkušební verze je k dispozici [zde](https://releases.aspose.com/).

**Q: Jaké typy filtrů mohu použít na PNG obrázky?**  
A: Aspose.PSD podporuje Paeth, Sub, Up, Average a None. Vyberte ten, který nejlépe vyvažuje velikost a vizuální věrnost.

**Q: Kde mohu najít podporu pro problémy s Aspose.PSD?**  
A: Pomoc a podporu můžete získat návštěvou Aspose fóra [zde](https://forum.aspose.com/c/psd/34).

## Závěr
Nyní víte, **jak filtrovat PNG** soubory pomocí Aspose.PSD pro Java, jak **převést PSD na PNG** a jak provádět **java png optimalizaci** s různými typy filtrů. Experimentujte s různými filtry, integrujte tento pracovní postup do vašeho zpracování obrázků a užívejte si menší, vysoce kvalitní PNG soubory.

---

**Poslední aktualizace:** 2026-03-15  
**Testováno s:** Aspose.PSD for Java 24.10  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}