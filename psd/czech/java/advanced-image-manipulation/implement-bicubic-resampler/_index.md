---
date: 2026-04-12
description: Naučte se, jak změnit velikost obrázku v Javě pomocí Bicubic Resampleru
  od Aspose.PSD. Tento návod na škálování obrázků ukazuje krok za krokem, jak dosáhnout
  vynikajících výsledků.
keywords:
- resize image java
- image scaling tutorial
- java image library
linktitle: Implementovat bicubický resampler
second_title: Aspose.PSD Java API
title: Změna velikosti obrázku v Javě – bikubický resampler pro vysoce kvalitní škálování
url: /cs/java/advanced-image-manipulation/implement-bicubic-resampler/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Změna velikosti obrázku Java – Bikubický resampler pro vysoce kvalitní škálování

## Úvod

Pokud potřebujete **resize image java** projekty bez ztráty ostrosti nebo zavádění artefaktů, jste na správném místě. V tomto **image scaling tutorial** vás provedeme používáním Bicubic Resampler od Aspose.PSD — výkonnou funkcí **java image library**, která poskytuje hladké, ostré výsledky pro soubory PSD a mnoho dalších formátů. Na konci tohoto průvodce budete schopni integrovat vysoce kvalitní škálování do jakékoli Java aplikace pomocí jen několika řádků kódu.

## Rychlé odpovědi
- **Co dělá Bicubic Resampler?** Používá sofistikovaný interpolační algoritmus, který zachovává detaily při změně velikosti obrázků.  
- **Které hodnoty ResizeType jsou k dispozici?** `CubicConvolution` a `Bell` jsou dvě možnosti Bicubic poskytované Aspose.PSD.  
- **Potřebuji licenci pro spuštění kódu?** Dočasná licence aspose funguje pro hodnocení; plná licence je vyžadována pro produkci.  
- **Jaká verze Javy je vyžadována?** Jakékoli prostředí Java 8+ je kompatibilní s nejnovější knihovnou Aspose.PSD.  
- **Mohu změnit velikost jiných formátů (PNG, JPEG) pomocí stejného API?** Ano, Aspose.PSD podporuje více typů obrázků, i když příklady se zaměřují na PSD.

## Co je vysoce kvalitní škálování obrázků?

Vysoce kvalitní škálování obrázků označuje změnu velikosti obrázku při zachování ostrých hran, hladkých přechodů a přesné reprodukce barev. Bicubic Resampler toho dosahuje tím, že zohledňuje hodnoty okolních pixelů (použitím cubic convolution nebo Bell algoritmu) při výpočtu každého nového pixelu, což vede k přirozenějšímu vzhledu ve srovnání s metodami nearest‑neighbor nebo bilinear.

## Proč použít Bicubic Resampler pro vysoce kvalitní škálování obrázků?

- **Zachovává detail:** Jemné textury a čáry zůstávají jasné i po výrazných změnách velikosti.  
- **Snižuje artefakty:** Minimalizuje ozvěny a rozmazání, které se často objevují u jednodušších algoritmů.  
- **Snadná integrace:** Jednořádkové volání metody (`image.resize`) vám umožní přepínat mezi algoritmy bez přepisování kódu.  

## Požadavky

Before you start, make sure you have:

- **Aspose.PSD for Java** – stáhněte nejnovější JAR z [Aspose.PSD for Java documentation](https://reference.aspose.com/psd/java/).  
- **Java Development Kit** – nainstalovaný a nakonfigurovaný JDK 8 nebo novější.  
- **Sample PSD file** – testovací obrázek (např. `sample_bicubic.psd`) umístěný v známém adresáři.  

Tyto položky společně tvoří pevný základ **java image library** pro tento tutoriál.

## Import balíčků

Přidejte požadované importy do vaší Java třídy. Tyto importy přinášejí základní třídy Aspose.PSD a výčtový typ `ResizeType`.

```java
import com.aspose.psd.Image;
import com.aspose.psd.ResizeType;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.PsdOptions;
```

## Jak změnit velikost obrázku Java pomocí Bicubic Resampler

### Krok 1: Načíst obrázek

Nejprve načtěte zdrojový soubor PSD, který chcete změnit velikost. Nahraďte `Your Document Directory` skutečnou cestou na vašem počítači.

```java
String dataDir = "Your Document Directory";
String filePath = dataDir + "sample_bicubic.psd";
PsdImage image = (PsdImage)Image.load(filePath);
```

### Krok 2: Změna velikosti pomocí Cubic Convolution (vysoká kvalita)

Nyní použijte algoritmus **Cubic Convolution**, jednu ze dvou možností Bicubic, která poskytuje vysoce kvalitní škálování obrázku. Příklad mění velikost obrázku na 300 × 300 pixelů.

```java
String destNameCubicConvolution = dataDir + "ResamplerCubicConvolutionStripes_after.psd";
image.resize(300, 300, ResizeType.CubicConvolution);
image.save(destNameCubicConvolution, new PsdOptions(image));
```

### Krok 3: Změna velikosti pomocí Bell algoritmu (alternativní vysoká kvalita)

Pokud dáváte přednost algoritmu **Bell**, který nabízí mírně odlišný vyhlazovací efekt, můžete jej použít stejným způsobem. Všimněte si, že znovu načítáme původní obrázek, aby byla srovnání spravedlivá.

```java
String destNameBell = dataDir + "ResamplerBellStripes_after.psd";
PsdImage imageBellStripes = (PsdImage)Image.load(filePath);
imageBellStripes.resize(300, 300, ResizeType.Bell);
imageBellStripes.save(destNameBell, new PsdOptions(imageBellStripes));
```

Klidně experimentujte s jinými rozměry nebo formáty souborů — stačí podle toho upravit parametry.

## Časté úskalí a tipy

- **Nesprávná cesta:** Ujistěte se, že `dataDir` končí souborovým oddělovačem (`/` nebo `\`) vhodným pro váš OS.  
- **Výjimky licence:** Spuštění bez platné licence může do výstupního obrázku přidat vodoznak. Použijte **temporary aspose license** pro testování, poté přepněte na trvalou licenci pro produkci.  
- **Využití paměti:** Velké soubory PSD mohou spotřebovat značné množství paměti; zvažte uvolnění obrázků (`image.dispose()`) po uložení.  

## Často kladené otázky

**Q: Mohu použít Aspose.PSD pro Java s jinými formáty obrázků?**  
A: Ano, knihovna podporuje PSD, PNG, JPEG, TIFF, BMP a mnoho dalších.

**Q: Je pro Aspose.PSD pro Java k dispozici dočasná licence?**  
A: Ano, dočasnou licenci můžete získat [zde](https://purchase.aspose.com/temporary-license/).

**Q: Kde mohu najít podporu pro Aspose.PSD pro Java?**  
A: Navštivte fórum Aspose.PSD [zde](https://forum.aspose.com/c/psd/34) pro dotazy související s podporou.

**Q: Mohu stáhnout knihovnu Aspose.PSD pro Java?**  
A: Ano, knihovnu si můžete stáhnout ze stránky vydání [zde](https://releases.aspose.com/psd/java/).

**Q: Jak mohu zakoupit Aspose.PSD pro Java?**  
A: Aspose.PSD pro Java můžete zakoupit na stránce nákupu [zde](https://purchase.aspose.com/buy).

---

**Poslední aktualizace:** 2026-04-12  
**Testováno s:** Aspose.PSD for Java 24.11 (nejnovější v době psaní)  
**Autor:** Aspose

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}