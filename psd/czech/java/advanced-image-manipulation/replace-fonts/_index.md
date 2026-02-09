---
date: 2026-02-09
description: Naučte se, jak v Javě použít náhradu fontů Aspose PSD k řešení souborů
  PSD s chybějícími fonty, rychle nahradit chybějící fonty v PSD a exportovat obrázky.
linktitle: Replace Fonts
second_title: Aspose.PSD Java API
title: Aspose PSD substituce fontů v Javě – Nahrazení chybějících fontů
url: /cs/java/advanced-image-manipulation/replace-fonts/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose PSD náhrada fontů v Javě

## Úvod

Pokud potřebujete nahradit chybějící nebo nechtěné typy písma v souboru Photoshop (PSD), **Aspose PSD font substitution** to usnadňuje. V Java aplikacích můžete načíst PSD, říci Aspose, které náhradní písmo použít, a poté výsledek uložit v libovolném formátu. Tento tutoriál vás provede kompletním **aspose psd font substitution** pracovním postupem, od nastavení projektu až po export aktualizovaného obrázku, takže můžete spolehlivě řešit scénáře s chybějícími fonty v PSD bez otevírání Photoshopu.

## Rychlé odpovědi
- **Jaká knihovna provádí náhradu fontů?** Aspose.PSD for Java  
- **Jak dlouho trvá implementace?** Přibližně 5‑10 minut pro základní scénář  
- **Jaké písmo se používá jako výchozí náhrada?** Můžete nastavit libovolné TrueType písmo, např. „Arial“  
- **Mohu uložit do formátů jiných než PNG?** Ano – podporovány jsou PSD, JPEG, BMP a další  
- **Potřebuji licenci pro produkci?** Pro ne‑zkušební použití je vyžadována platná licence Aspose.PSD  

## Co je Aspose PSD Font Substitution?

Aspose PSD font substitution je proces určení náhradního typu písma, který knihovna použije vždy, když narazí na chybějící nebo nepodporované písmo v souboru PSD. Tím se zajistí, že textové vrstvy se vykreslí správně bez ruční úpravy ve Photoshopu a umožní vám **automaticky řešit chybějící fonty v PSD** souborech.

## Proč použít Aspose.PSD pro Javu?

- **Kompletní podpora PSD** – vrstvy, masky, efekty a text jsou všechny přístupné přes API.  
- **Cross‑platform** – funguje na jakémkoli OS, který podporuje Javu.  
- **Žádné externí závislosti** – knihovna provádí náhradu fontů interně, takže nemusíte distribuovat další písma s vaší aplikací.  

## Jak nahradit chybějící fonty v PSD pomocí Aspose PSD

Níže je krok‑za‑krokem průvodce, který ukazuje **jak nahradit chybějící fonty v PSD** souborech pomocí vlastního náhradního písma.

## Požadavky

- **Java Development Kit (JDK)** – nainstalována verze 8 nebo vyšší.  
- **Aspose.PSD for Java** – stáhněte nejnovější JAR ze [release page](https://releases.aspose.com/psd/java/).  
- **IDE** – IntelliJ IDEA, Eclipse nebo jakýkoli editor, který preferujete.  

## Import balíčků

Začněte importováním potřebných tříd. To vám poskytne přístup k načítání obrázků, možnostem načítání a funkcím ukládání.

```java
import com.aspose.psd.Image;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
import com.aspose.psd.imageoptions.PngOptions;
```

## Krok 1: Nastavte adresář dokumentu

Definujte složku, která obsahuje zdrojový soubor PSD. Nahraďte zástupný text skutečnou cestou na vašem počítači.

```java
String dataDir = "Your Document Directory";
```

## Krok 2: Načtěte obrázek s náhradním písmem

Vytvořte instanci `PsdLoadOptions`, určete výchozí náhradní písmo (např. **Arial**) a načtěte PSD. Aspose automaticky použije náhradu, kdykoli narazí na chybějící písmo.

```java
PsdLoadOptions psdLoadOptions = new PsdLoadOptions(); 
psdLoadOptions.setDefaultReplacementFont("Arial");

PsdImage psdImage = (PsdImage)Image.load(dataDir + "Cloud_AzPlat_Banner3A_SB_EN_US_160x600_chinese_font.psd", psdLoadOptions);
```

## Krok 3: Uložte nahrazený obrázek

Po náhradě fontu můžete obrázek exportovat v libovolném podporovaném formátu. Zde jej ukládáme jako PNG, ale můžete také zvolit JPEG, BMP nebo dokonce zapsat zpět do PSD.

```java
PngOptions pngOptions = new PngOptions();
psdImage.save(dataDir + "replaced_font.png", pngOptions);
```

## Časté problémy a řešení

| Problém | Příčina | Řešení |
|---------|---------|--------|
| Text je po nahrazení poškozený | Náhradní písmo neobsahuje požadované glyfy | Zvolte písmo, které podporuje potřebný rozsah Unicode (např. „Arial Unicode MS“). |
| `OutOfMemoryError` u velkých PSD | Načítání velmi vysokého rozlišení souboru bez dostatečné haldy | Zvyšte velikost haldy JVM (`-Xmx2g`) nebo načtěte obrázek v režimu streamování, pokud je k dispozici. |
| Licenční výjimka | Použití zkušební verze v produkci | Aplikujte platnou trvalou nebo dočasnou licenci před načtením obrázku. |

## Často kladené otázky

**Q: Můžu nahradit fonty i v jiných formátech obrázků než PSD?**  
A: Ano. I když je hlavním případem použití PSD, Aspose.PSD také podporuje PNG, JPEG, BMP a TIFF, což umožňuje náhradu fontů tam, kde existují textové vrstvy.

**Q: Je výchozí náhradní písmo povinné?**  
A: Ne. Můžete nastavit libovolné TrueType písmo, které preferujete, nebo nastavení vynechat a nechat Aspose použít svůj interní výchozí font.

**Q: Existují licenční požadavky pro používání Aspose.PSD?**  
A: Pro produkční nasazení je vyžadována komerční licence. Podrobnosti najdete na [purchase page](https://purchase.aspose.com/buy).

**Q: Mohu získat dočasnou licenci pro testování?**  
A: Rozhodně. Aspose nabízí zdarma dočasné licence pro hodnocení – navštivte [temporary license page](https://purchase.aspose.com/temporary-license/).

**Q: Kde mohu najít další podporu nebo diskutovat o problémech souvisejících s Aspose.PSD?**  
A: Komunitní fórum je skvělým místem pro kladení otázek: [Aspose.PSD forum](https://forum.aspose.com/c/psd/34).

**Q: Jak řešit PSD soubory, které obsahují více chybějících fontů?**  
A: Nastavte výchozí náhradní písmo jednou (jak je ukázáno) – bude aplikováno na *všechny* chybějící fonty během načítací operace.

**Q: Je možné nahradit fonty po uložení obrázku?**  
A: Náhrada fontů musí proběhnout během fáze načítání. Pro změnu fontů později načtěte PSD znovu s jiným náhradním písmem a znovu uložte.

## Závěr

Nyní jste viděli kompletní **aspose psd font substitution** workflow v Javě – od importu správných tříd, nastavení náhradního písma, načtení PSD až po export opraveného obrázku. Začleňte tento vzor do vašich pipeline pro zpracování obrázků, abyste zajistili konzistentní typografii ve všech vašich PSD zdrojích a **automaticky řešili chybějící fonty v PSD**.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Poslední aktualizace:** 2026-02-09  
**Testováno s:** Aspose.PSD for Java 24.12 (nejnovější v době psaní)  
**Autor:** Aspose