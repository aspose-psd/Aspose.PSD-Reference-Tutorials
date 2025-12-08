---
date: 2025-12-06
description: Naučte se, jak otočit obrázek o 270 stupňů pomocí Aspose.PSD pro Javu.
  Tento průvodce ukazuje, jak otáčet soubory PSD, převrátit obrázky a převádět PSD
  na JPEG.
language: cs
linktitle: Rotate Image 270 Degrees
second_title: Aspose.PSD Java API
title: Jak otočit obrázek o 270 stupňů pomocí Aspose.PSD pro Javu
url: /java/advanced-image-manipulation/rotate-image/
weight: 19
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Otočení obrázku o 270 stupňů pomocí Aspose.PSD pro Java

## Úvod

V tomto **java image processing tutorial** objevíte, jak **rotate image 270 degrees** rychle a spolehlivě pomocí Aspose.PSD pro Java. Ať už vytváříte nástroj pro úpravu fotografií, automatizujete hromadné konverze, nebo jen potřebujete přeorientovat vrstvu PSD, knihovna úkol zvládne bez problémů. Dotkneme se také převracení obrázků a konverze otočeného PSD do JPEG, takže získáte kompletní end‑to‑end workflow.

## Rychlé odpovědi
- **Jaká knihovna provádí otáčení?** Aspose.PSD for Java  
- **Jaký úhel otáčení příklad používá?** 270 degrees  
- **Mohu také převrátit obrázek?** Ano – použijte možnosti `RotateFlipType` jako `Rotate90FlipX`  
- **Jak uložit výsledek?** V příkladu ukládáme jako JPEG pomocí `JpegOptions`  
- **Potřebuji licenci pro produkci?** Pro komerční použití je vyžadována platná licence Aspose.PSD  

## Co znamená „otočit obrázek o 270 stupňů“?
Otočení obrázku o 270 stupňů znamená otočit obrázek o tři čtvrtiny úplného kruhu po směru hodinových ručiček (nebo o 90 stupňů proti směru hodinových ručiček). V mnoha scénářích grafické úpravy tato orientace odpovídá původnímu portrétnímu rozložení po sérii transformací.

## Proč použít Aspose.PSD pro tento úkol?
- **Full PSD support** – funguje s vrstvami, maskami a objekty úprav.  
- **No native Photoshop required** – běží na libovolném Java runtime.  
- **Simple API** – jediný volání metody (`rotateFlip`) provádí otáčení i převracení.  
- **Easy format conversion** – export přímo do JPEG, PNG nebo jiných běžných formátů.

## Požadavky

Než začnete, ujistěte se, že máte:

- **Aspose.PSD for Java** knihovnu nainstalovanou. Můžete si ji stáhnout a zobrazit kompletní referenci API [zde](https://reference.aspose.com/psd/java/).  
- Vývojové prostředí Java (JDK 8 nebo vyšší).  
- Vzorkový soubor PSD, který chcete otočit. Aktualizujte proměnnou `sourceFile` v kódu na správnou cestu k vašemu souboru.

## Import balíčků

Začněte importováním potřebných tříd z balíčku Aspose.PSD:

```java
import com.aspose.psd.Image;
import com.aspose.psd.RotateFlipType;

import com.aspose.psd.imageoptions.JpegOptions;
```

## Jak otočit PSD – Krok 1: Načíst obrázek

Vytvořte instanci `Image`, která ukazuje na váš zdrojový soubor PSD:

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";
Image image = Image.load(sourceFile);
```

## Jak otočit PSD – Krok 2: Otočit obrázek o 270 stupňů

Použijte metodu `rotateFlip` s `RotateFlipType.Rotate270FlipNone` pro dosažení otáčení o 270 stupňů bez jakéhokoli převrácení:

```java
image.rotateFlip(RotateFlipType.Rotate270FlipNone);
```

> **Pro tip:** Pokud potřebujete také převrátit obrázek horizontálně nebo vertikálně, zvolte jiný `RotateFlipType`, například `Rotate90FlipX` nebo `Rotate180FlipY`.

## Jak otočit PSD – Krok 3: Převést PSD na JPEG a uložit

Po otočení můžete **convert PSD to JPEG** (nebo jakýkoli jiný podporovaný formát) pomocí příslušné třídy možností:

```java
String destName = dataDir + "RotatedImage_out.jpg";
image.save(destName, new JpegOptions());
```

Soubor `RotatedImage_out.jpg` nyní obsahuje původní obsah PSD otočený o 270 stupňů a uložený jako JPEG.

## Časté problémy a řešení

| Problém | Řešení |
|-------|----------|
| **Obrázek se zobrazuje vzhůru nohama** | Ověřte, že jste použili `Rotate270FlipNone`. Pro otáčení o 90 stupňů po směru hodinových ručiček použijte `Rotate90FlipNone`. |
| **Výstupní soubor je poškozen** | Ujistěte se, že cílová složka existuje a máte oprávnění k zápisu. |
| **Výjimka licence** | Nainstalujte dočasnou nebo trvalou licenci Aspose.PSD před načtením obrázku v produkci. |

## Často kladené otázky

**Q: Je Aspose.PSD kompatibilní s různými formáty obrázků?**  
A: Ano, Aspose.PSD podporuje PSD, JPEG, PNG, BMP, GIF a mnoho dalších rastrových formátů.

**Q: Mohu použít vlastní úhly otáčení, ne jen předdefinované převrácení?**  
A: Rozhodně! Zatímco `RotateFlipType` poskytuje běžné úhly, můžete kombinovat více volání nebo použít transformační matice pro libovolné úhly.

**Q: Jak převést otočený PSD do jiného formátu, například PNG?**  
A: V metodě `save` nahraďte `JpegOptions` třídou `PngOptions` (nebo příslušnou třídou možností).

**Q: Kde najdu další podporu nebo pomoc?**  
A: Pro komunitní pomoc navštivte [Aspose.PSD Forum](https://forum.aspose.com/c/psd/34).

**Q: Je k dispozici bezplatná zkušební verze?**  
A: Ano, můžete si vyzkoušet Aspose.PSD pomocí [free trial](https://releases.aspose.com/).

**Q: Jak získat dočasnou licenci?**  
A: Pokud potřebujete dočasnou licenci, můžete ji získat [zde](https://purchase.aspose.com/temporary-license/).

## Závěr

Nyní jste se naučili, jak **rotate image 270 degrees** pomocí Aspose.PSD pro Java, jak v případě potřeby převracet obrázky a exportovat výsledek do JPEG. Tento jednoduchý workflow lze integrovat do větších Java‑založených pipeline pro zpracování obrázků, což vám poskytuje plnou kontrolu nad manipulací PSD bez nutnosti Photoshopu.

---

**Last Updated:** 2025-12-06  
**Tested With:** Aspose.PSD for Java 24.12  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}