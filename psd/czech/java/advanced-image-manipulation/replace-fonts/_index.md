---
date: 2025-12-05
description: Naučte se, jak provést nahrazení fontů v souborech PSD pomocí Aspose
  v Javě. Tento krok‑za‑krokem návod na manipulaci s obrázky v Javě vám ukáže, jak
  efektivně nahradit fonty v souborech PSD.
linktitle: Replace Fonts
second_title: Aspose.PSD Java API
title: Nahrazení fontů v PSD pomocí Aspose v Javě – Nahraďte fonty v souborech PSD
url: /cs/java/advanced-image-manipulation/replace-fonts/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Nahrazení fontů Aspose PSD v Javě

## Úvod

Pokud potřebujete vyměnit chybějící nebo nechtěné typy písma uvnitř souboru Photoshop (PSD), **Aspose PSD font replacement** to udělá bez problémů. V Java aplikacích můžete načíst PSD, říct Aspose, který náhradní font použít, a poté výsledek uložit v libovolném formátu. Tento tutoriál vás provede kompletním **aspose psd font replacement** pracovním postupem, od nastavení projektu až po export aktualizovaného obrázku.

## Rychlé odpovědi
- **Jaká knihovna provádí nahrazení fontů?** Aspose.PSD for Java  
- **Jak dlouho trvá implementace?** Přibližně 5‑10 minut pro základní scénář  
- **Jaký font se používá jako výchozí náhrada?** Můžete nastavit libovolný TrueType font, např. “Arial”  
- **Mohu uložit do formátů jiných než PNG?** Ano – PSD, JPEG, BMP atd. jsou podporovány  
- **Potřebuji licenci pro produkční použití?** Platná licence Aspose.PSD je vyžadována pro ne‑zkušební použití  

## Co je Aspose PSD Font Replacement?

Aspose PSD font replacement je proces specifikace náhradního typu písma, který knihovna použije vždy, když narazí na chybějící nebo nepodporovaný font v PSD souboru. Tím se zajistí, že textové vrstvy se vykreslí správně bez ruční úpravy ve Photoshopu.

## Proč použít Aspose.PSD pro Java?

- **Kompletní podpora PSD** – vrstvy, masky, efekty i text jsou přístupné přes API.  
- **Cross‑platform** – funguje na libovolném OS, který podporuje Javu.  
- **Žádné externí závislosti** – knihovna provádí náhradu fontů interně, takže nemusíte distribuovat další fonty s aplikací.  

## Požadavky

Než začneme, ujistěte se, že máte:

- **Java Development Kit (JDK)** – verze 8 nebo vyšší nainstalovanou.  
- **Aspose.PSD for Java** – stáhněte nejnovější JAR ze [release page](https://releases.aspose.com/psd/java/).  
- **IDE** – IntelliJ IDEA, Eclipse nebo jakýkoli editor, který preferujete.  

## Import balíčků

Začněte importováním tříd, které budete potřebovat. To vám poskytne přístup k načítání obrázků, možnostem načítání a ukládání.

```java
import com.aspose.psd.Image;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
import com.aspose.psd.imageoptions.PngOptions;
```

## Krok 1: Nastavte adresář dokumentu

Definujte složku, která obsahuje zdrojový PSD soubor. Nahraďte zástupný text skutečnou cestou na vašem počítači.

```java
String dataDir = "Your Document Directory";
```

## Krok 2: Načtěte obrázek s náhradním fontem

Vytvořte instanci `PsdLoadOptions`, specifikujte výchozí náhradní font (např. **Arial**) a načtěte PSD. Aspose automaticky použije tuto náhradu, kdykoli narazí na chybějící font.

```java
PsdLoadOptions psdLoadOptions = new PsdLoadOptions(); 
psdLoadOptions.setDefaultReplacementFont("Arial");

PsdImage psdImage = (PsdImage)Image.load(dataDir + "Cloud_AzPlat_Banner3A_SB_EN_US_160x600_chinese_font.psd", psdLoadOptions);
```

## Krok 3: Uložte obrázek s nahrazeným fontem

Po provedení substituce fontu můžete exportovat obrázek v libovolném podporovaném formátu. Zde jej ukládáme jako PNG, ale můžete také zvolit JPEG, BMP nebo dokonce zpět do PSD.

```java
PngOptions pngOptions = new PngOptions();
psdImage.save(dataDir + "replaced_font.png", pngOptions);
```

## Časté problémy a řešení

| Problém | Příčina | Řešení |
|---------|----------|--------|
| Text se po nahrazení zobrazuje poškozeně | Náhradní font neobsahuje požadované glyfy | Zvolte font, který podporuje potřebný rozsah Unicode (např. “Arial Unicode MS”). |
| `OutOfMemoryError` u velkých PSD | Načítání velmi vysokého rozlišení bez dostatečné paměti | Zvyšte velikost haldy JVM (`-Xmx2g`) nebo načtěte obrázek v režimu streamování, pokud je k dispozici. |
| Výjimka licence | Používání zkušební verze v produkci | Před načtením obrázku aplikujte platnou trvalou nebo dočasnou licenci. |

## Často kladené otázky

**Q: Mohu nahrazovat fonty i v jiných formátech obrázků než PSD?**  
A: Ano. I když je primárním scénářem PSD, Aspose.PSD podporuje také PNG, JPEG, BMP a TIFF, což umožňuje náhradu fontů tam, kde existují textové vrstvy.

**Q: Je výchozí náhradní font povinný?**  
A: Ne. Můžete nastavit libovolný TrueType font, který preferujete, nebo nastavení vynechat a nechat Aspose použít svůj interní výchozí font.

**Q: Existují licenční požadavky pro používání Aspose.PSD?**  
A: Pro produkční nasazení je vyžadována komerční licence. Podrobnosti najdete na [purchase page](https://purchase.aspose.com/buy).

**Q: Můžu získat dočasnou licenci pro testování?**  
A: Rozhodně. Aspose nabízí zdarma dočasné licence pro hodnocení – navštivte [temporary license page](https://purchase.aspose.com/temporary-license/).

**Q: Kde mohu najít další podporu nebo diskutovat o problémech souvisejících s Aspose.PSD?**  
A: Komunitní fórum je skvělým místem pro otázky: [Aspose.PSD forum](https://forum.aspose.com/c/psd/34).

**Q: Jak zacházet se soubory PSD, které obsahují více chybějících fontů?**  
A: Nastavte výchozí náhradní font jednou (jak je ukázáno) – bude aplikován na *všechny* chybějící fonty během operace načítání.

**Q: Je možné nahradit fonty po uložení obrázku?**  
A: Substituce fontu musí proběhnout během fáze načítání. Pro změnu fontů později načtěte PSD znovu s jiným náhradním fontem a znovu uložte.

## Závěr

Nyní jste viděli kompletní **aspose psd font replacement** workflow v Javě — od importu správných tříd, konfigurace náhradního fontu, načtení PSD až po export opraveného obrázku. Začleňte tento vzor do svých pipeline pro zpracování obrázků, aby byla typografie ve všech vašich PSD aktivech konzistentní.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Poslední aktualizace:** 2025-12-05  
**Testováno s:** Aspose.PSD for Java 24.12 (nejnovější v době psaní)  
**Autor:** Aspose  

---