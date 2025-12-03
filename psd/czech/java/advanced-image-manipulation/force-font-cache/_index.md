---
date: 2025-12-01
description: Naučte se, jak uložit soubor PSD, vynutit mezipaměť fontů a zlepšit výkon
  obrázků pomocí Aspose.PSD pro Javu. Krok‑za‑krokem průvodce optimalizací zpracování
  obrázků.
language: cs
linktitle: Force Font Cache
second_title: Aspose.PSD Java API
title: Jak uložit soubor PSD a vynutit mezipaměť písem pomocí Aspose.PSD pro Javu
url: /java/advanced-image-manipulation/force-font-cache/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Jak uložit soubor PSD a vynutit mezipaměť fontů pomocí Aspose.PSD pro Java

## Úvod

Pokud potřebujete rychle **uložit soubor PSD** a zároveň zajistit, že jsou k dispozici správné fonty, jste na správném místě. Mezipaměť fontů může dramaticky **zlepšit výkon obrazu**, zejména při opakovaném zpracování velkých dokumentů Photoshopu. V tomto tutoriálu vás provedeme přesnými kroky, jak vynutit mezipaměť fontů, načíst PSD obrázek a nakonec **uložit soubor PSD** s nově nainstalovanými fonty pomocí Aspose.PSD pro Java.

## Rychlé odpovědi
- **Co dělá vynucení mezipaměti fontů?** Vynutí, aby Aspose.PSD znovu prohledal systémové fonty, takže nově nainstalované fonty jsou okamžitě rozpoznány.  
- **Jak dlouho mám čekat na instalaci fontu?** Vzorový kód pozastaví běh na **2 minuty**, což je obvykle dostatečné pro ruční instalaci.  
- **Mohu to použít s libovolným souborem PSD?** Ano – pokud je soubor přístupný a požadované fonty jsou nainstalovány v systému.  
- **Potřebuji licenci pro spuštění tohoto kódu?** Pro produkční použití je vyžadována dočasná nebo plná licence; pro hodnocení funguje bezplatná zkušební verze.  
- **Které verze Javy jsou podporovány?** Aspose.PSD pro Java funguje s JDK 8 a novějšími.

## Co je „uložit soubor PSD“ a proč je to důležité?

Uložení souboru PSD po úpravě jeho vrstev, textu nebo fontů je posledním krokem, který zachová vaše změny. Když mezipaměť fontů není aktuální, uložený soubor může přejít na výchozí fonty, což vede k vizuálním nesrovnalostem. Vynucením mezipaměti nejprve zajistíte, že operace **uložit soubor PSD** vloží správné typy písma.

## Proč vynutit mezipaměť fontů pomocí Aspose.PSD?

- **Zvýšení výkonu** – Snižuje potřebu opakovaných vyhledávání fontů.  
- **Spolehlivost** – Zaručuje, že uložené soubory PSD se vykreslí přesně podle zamýšleného vzhledu na jakémkoli počítači.  
- **Jednoduchost** – Jediný volání metody (`OpenTypeFontsCache.updateCache()`) provádí těžkou práci.

## Požadavky

Před zahájením se ujistěte, že máte:

- Java Development Kit (JDK) 8 nebo novější nainstalovaný.  
- Knihovnu Aspose.PSD pro Java (stáhněte z oficiálního [download link](https://releases.aspose.com/psd/java/)).  
- Ukázkový soubor PSD (`sample.psd`) umístěný ve složce, na kterou můžete odkazovat ve svém kódu.  

Nyní, když je vše připraveno, pojďme se ponořit do implementace.

## Import balíčků

Nejprve importujte třídy potřebné pro práci s PSD obrázky a mezipamětí fontů. Umístěte tyto příkazy na začátek vaší Java třídy:

```java
import com.aspose.psd.Image;
import com.aspose.psd.OpenTypeFontsCache;

import com.aspose.psd.fileformats.psd.PsdImage;
import java.io.Console;
import java.util.concurrent.TimeUnit;
```

### Krok 1: Načtení PSD obrázku (Jak načíst PSD)

Začneme načtením původního souboru PSD. To nám poskytne základní objekt obrázku, který můžeme později znovu uložit po aktualizaci mezipaměti fontů.

```java
String dataDir = "Your Document Directory";

PsdImage image = (PsdImage)Image.load(dataDir + "sample.psd");
image.save(dataDir + "NoFont.psd");
```

- **Vysvětlení:**  
  - `Image.load` načte soubor do paměti.  
  - `image.save` vytvoří kopii pojmenovanou **NoFont.psd**, která odráží stav **před** tím, než jsou k dispozici nové fonty.  
  - Tento krok je užitečný pro srovnání a zajišťuje, že následná aktualizace mezipaměti skutečně změní výstup.

### Krok 2: Počkat na instalaci fontu (Zlepšení výkonu obrazu)

Nyní dáváme uživateli čas ručně nainstalovat požadovaný font. V reálném scénáři byste tento krok mohli automatizovat, ale pauza demonstruje mechanismus obnovení mezipaměti.

```java
System.out.println("You have 2 minutes to install the font");
Thread.sleep(2 * 60 * 1000);
OpenTypeFontsCache.updateCache();
```

- **Vysvětlení:**  
  - `Thread.sleep` pozastaví provádění na **2 minuty** (2 × 60 × 1000 ms).  
  - `OpenTypeFontsCache.updateCache()` vynutí, aby Aspose.PSD znovu prohledal OpenType fonty systému, čímž jsou nově nainstalované fonty okamžitě k dispozici pro vykreslování.

### Krok 3: Načtení aktualizovaného PSD obrázku (Načíst PSD obrázek) a **uložit soubor PSD**

Po obnovení mezipaměti načteme původní PSD znovu. Tentokrát jsou informace o fontu aktuální a můžeme **uložit soubor PSD** se správným typem písma.

```java
PsdImage image1 = (PsdImage)Image.load(dataDir + "sample.psd");
image1.save(dataDir + "HasFont.psd");
```

- **Vysvětlení:**  
  - Druhé načtení zachytí nově nainstalovaný font.  
  - Uložení do **HasFont.psd** vytvoří soubor, který nyní obsahuje správné vykreslení fontu, což potvrzuje, že aktualizace mezipaměti fungovala.

## Časté problémy a řešení

| Problém | Důvod | Řešení |
|-------|--------|----------|
| Uložený PSD stále zobrazuje výchozí font | Font není nainstalován v umístění, které OS prohledává | Nainstalujte font do systémové složky fontů (např. `C:\Windows\Fonts` ve Windows) a znovu spusťte `updateCache()`. |
| `Thread.sleep` vyvolá `InterruptedException` | Podpis metody neřeší kontrolované výjimky | Přidejte `throws InterruptedException` do vaší `main` metody nebo obalte volání do try‑catch bloku. |
| `OpenTypeFontsCache.updateCache()` nedělá nic | Běží na serveru bez hlavičky (headless) bez konfigurace fontů | Ujistěte se, že server má nainstalované požadované fonty a Java proces má oprávnění je číst. |

## Často kladené otázky

**Q: Je Aspose.PSD kompatibilní se všemi verzemi Javy?**  
A: Aspose.PSD pro Java podporuje JDK 8 a novější, což pokrývá většinu moderních Java aplikací.

**Q: Mohu používat Aspose.PSD pro komerční projekty?**  
A: Ano. Pro produkční použití je vyžadována komerční licence. Můžete ji získat na [purchase page](https://purchase.aspose.com/buy).

**Q: Je k dispozici bezplatná zkušební verze?**  
A: Rozhodně! Stáhněte si trial verzi z [releases page](https://releases.aspose.com/).

**Q: Kde mohu najít komunitní podporu?**  
A: Připojte se k diskusi na [Aspose.PSD forum](https://forum.aspose.com/c/psd/34) pro tipy a řešení problémů.

**Q: Jak mohu získat dočasnou licenci pro testování?**  
A: Navštivte [temporary license page](https://purchase.aspose.com/temporary-license/) a požádejte o krátkodobou licenci.

## Závěr

Nyní jste se naučili, jak **uložit soubor PSD** po vynucení mezipaměti fontů, což zajišťuje, že vaše výstupy PSD se pokaždé vykreslí se správnými typy písma. Tato technika je jednoduchou, ale výkonnou součástí **optimalizace zpracování obrazu** a může být integrována do větších pracovních postupů, které vyžadují spolehlivou, vysoce výkonnou manipulaci s PSD.

---

**Poslední aktualizace:** 2025-12-01  
**Testováno s:** Aspose.PSD pro Java 24.12 (nejnovější v době psaní)  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}