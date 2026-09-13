---
date: 2026-09-13
description: Naučte se, jak nakreslit elipsu a další tvary v Javě s Aspose.PSD. Tento
  podrobný tutoriál o grafice v Javě ukazuje gradientní výplně, výplně polygonů a
  export obrázků.
keywords:
- how to draw ellipse
- draw shapes java
- how to create gradient
- java graphics tutorial
- fill polygon java
lastmod: 2026-09-13
linktitle: Kreslení pomocí grafiky v Javě
og_description: Naučte se, jak nakreslit elipsu v Javě pomocí Aspose.PSD. Tento tutoriál
  o grafice v Javě pokrývá kreslení tvarů, gradientní výplně, výplně polygonů a export
  obrázků.
og_image_alt: Screenshot of Java code drawing an ellipse with Aspose.PSD
og_title: Jak nakreslit elipsu pomocí grafiky v Javě s Aspose.PSD
schemas:
- author: Aspose
  dateModified: '2026-09-13'
  description: Learn how to draw an ellipse and other shapes in Java with Aspose.PSD.
    This step‑by‑step Java graphics tutorial shows gradient fills, polygon fills,
    and image export.
  headline: How to draw ellipse using graphics in Java with Aspose.PSD
  type: TechArticle
- questions:
  - answer: Yes, it supports layer merging, channel adjustments, text rendering, and
      advanced masking in addition to shape drawing.
    question: Can Aspose.PSD handle complex image manipulations?
  - answer: Absolutely; the library is optimized for speed and can process a 10 MP
      image in under 2 seconds on a typical server.
    question: Is Aspose.PSD suitable for high‑performance applications?
  - answer: Visit the [Aspose.PSD Java documentation](https://reference.aspose.com/psd/java/)
      for comprehensive guides and API references.
    question: Where can I find more examples and documentation?
  - answer: Yes, you can export to BMP, PNG, JPEG, TIFF, GIF, and PSD among others.
    question: Does Aspose.PSD support multiple image formats for export?
  - answer: Reach out to the Aspose.PSD community on the [support forum](https://forum.aspose.com/c/psd/34)
      or consider a [temporary license](https://purchase.aspose.com/temporary-license/)
      for priority assistance.
    question: How can I get support or assistance if I encounter issues?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- java graphics
- Aspose.PSD
- drawing shapes java
- gradient fill java
- initialize graphics java
title: Jak nakreslit elipsu pomocí grafiky v Javě s Aspose.PSD
url: /cs/java/java-graphics-drawing/drawing-using-graphics/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Jak nakreslit elipsu pomocí grafiky v Javě s Aspose.PSD

## Úvod
V tomto tutoriálu grafiky v Javě objevíte, **jak nakreslit elipsu** objektů a dalších tvarů programově pomocí Aspose.PSD pro Java. Ať už potřebujete generovat dynamické náhledy, vytvářet vlastní UI prvky nebo automatizovat pracovní postupy designu, zvládnutí kreslení elips a výplní gradientem vám poskytne přesnou vizuální kontrolu. Níže uvedené kroky vás provedou inicializací grafiky, nastavením per a štětců a exportem výsledku do běžných formátů obrázků.

## Rychlé odpovědi
- **Jaká knihovna je vyžadována?** Aspose.PSD pro Java (stáhněte z oficiálního webu).  
- **Na jaký tvar se tutoriál zaměřuje?** Kreslení elipsy a vyplňování polygonu.  
- **Mohu exportovat do jiných formátů než BMP?** Ano – podporovány jsou PNG, JPEG, TIFF a další.  
- **Potřebuji licenci pro vývoj?** Pro testování stačí bezplatná dočasná licence; pro produkci je vyžadována plná licence.  
- **Je API vhodné pro velké obrázky?** Aspose.PSD zpracovává soubory až do 500 MB, aniž by načítalo celý bitmap do paměti.

## Jak nakreslit elipsu v Javě?
Načtěte `PsdImage` s požadovanou šířkou a výškou, vytvořte objekt `Graphics`, nastavte `Pen` a zavolejte `drawEllipse` s ohraničujícím obdélníkem. Celá operace vyžaduje jen několik volání metod a běží pod jednou sekundou pro typické obrázky 800×600 na moderním hardwaru.

## Co je Aspose.PSD pro Java?
Aspose.PSD pro Java je **čistě Java knihovna, která poskytuje 50+ konverzí formátů obrázků a plné možnosti úprav PSD** bez potřeby Adobe Photoshopu. Umí renderovat, upravovat a exportovat soubory s více vrstvami při nízké spotřebě paměti, což ji činí ideální pro generování grafiky na serveru.

## Proč použít Aspose.PSD pro kreslení tvarů?
Aspose.PSD nabízí vysoký výkon, rozsáhlou podporu formátů a přesné vykreslování, což ji činí ideální pro generování grafiky na serveru a kreslení složitých tvarů.

- **Výkon:** Zpracovává obrázky až do 500 MB s využitím haldy méně než 150 MB (≈30 % méně než konkurenční knihovny).  
- **Podpora formátů:** více než 50 vstupních a výstupních formátů, včetně BMP, PNG, JPEG, TIFF a PSD.  
- **Přesnost:** Sub‑pixelové vykreslování zajišťuje ostré elipsy a hladké gradienty na displejích s vysokým DPI.

## Požadavky
- Základní znalost programování v Javě.  
- Nainstalovaný Java Development Kit (JDK).  
- IDE, např. IntelliJ IDEA nebo Eclipse.  
- Knihovna Aspose.PSD pro Java. Můžete si ji stáhnout z [Stáhnout Aspose.PSD pro Java](https://releases.aspose.com/psd/java/).

## Import balíčků
Na začátek importujte potřebné třídy Aspose.PSD a standardní utility Javy. Následující třídy poskytují kreslicí primitivy a manipulaci s barvami:
```java
import com.aspose.psd.Color;
import com.aspose.psd.Graphics;
import com.aspose.psd.Pen;
import com.aspose.psd.Point;
import com.aspose.psd.Rectangle;
import com.aspose.psd.brushes.LinearGradientBrush;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.BmpOptions;
```

## Krok 1: vytvořit objekt obrázku
`PsdImage` představuje v‑paměti rastrové plátno, na které lze kreslit a které lze uložit v různých formátech.
```java
String dataDir = "Your Document Directory";
PsdImage image = new PsdImage(500, 500);
```

## Krok 2: inicializovat grafický objekt
`Graphics` je kreslicí plocha spojená s `PsdImage`, umožňující vektorové operace, jako je kreslení tvarů.
```java
Graphics graphics = new Graphics(image);
```

## Krok 3: vyčistit plochu obrázku
`clear` vyplní celé plátno jednou barvou pozadí.
```java
graphics.clear(Color.getWhite());
```

## Krok 4: vytvořit a nakonfigurovat objekt pera
`Pen` definuje barvu, šířku a styl tahů použité při kreslení obrysů.
```java
Pen pen = new Pen(Color.getBlue());
```

## Krok 5: kreslit tvary
`drawEllipse` vykreslí elipsu, která se vejde do zadaného obdélníku, pomocí aktuálního pera.
```java
graphics.drawEllipse(pen, new Rectangle(10, 10, 150, 100));
```

## Krok 6: použít štětce pro výplň
`LinearGradientBrush` vytvoří gradientní výplň, která přechází mezi dvěma barvami přes definovanou oblast.
```java
LinearGradientBrush linearGradientBrush = new LinearGradientBrush(image.getBounds(), Color.getRed(), Color.getWhite(), 45f);
Point[] points = { new Point(200, 200), new Point(400, 200), new Point(250, 350) };
graphics.fillPolygon(linearGradientBrush, points);
```

## Krok 7: uložit upravený obrázek
`save` zapíše `PsdImage` na disk ve zvoleném formátu, např. BMP nebo PNG.
```java
image.save(dataDir + "DrawingUsingGraphics_output.bmp", new BmpOptions());
```

## Časté problémy a řešení
- **NullPointerException při grafice:** Ujistěte se, že `PsdImage` je plně vytvořený před vytvořením objektu `Graphics`.  
- **Nesprávné barvy:** Použijte `Color.fromArgb` pro zadání přesných ARGB hodnot, pokud výchozí paleta neodpovídá očekáváním.  
- **Zpomalení výkonu u velkých obrázků:** Aktivujte `PsdImageOptions` s `compression = CompressionType.Rle` pro snížení paměťové zátěže.

## Často kladené otázky

**Q: Může Aspose.PSD zvládat komplexní úpravy obrázků?**  
A: Ano, podporuje slučování vrstev, úpravy kanálů, vykreslování textu a pokročilé maskování kromě kreslení tvarů.

**Q: Je Aspose.PSD vhodný pro vysoce výkonné aplikace?**  
A: Rozhodně; knihovna je optimalizována pro rychlost a dokáže zpracovat 10 MP obrázek za méně než 2 sekundy na typickém serveru.

**Q: Kde najdu více příkladů a dokumentaci?**  
A: Navštivte [Dokumentaci Aspose.PSD pro Java](https://reference.aspose.com/psd/java/) pro komplexní průvodce a reference API.

**Q: Podporuje Aspose.PSD export do více formátů obrázků?**  
A: Ano, můžete exportovat do BMP, PNG, JPEG, TIFF, GIF a PSD a dalších.

**Q: Jak získám podporu nebo pomoc, pokud narazím na problémy?**  
A: Kontaktujte komunitu Aspose.PSD na [fóru podpory](https://forum.aspose.com/c/psd/34) nebo zvažte [dočasnou licenci](https://purchase.aspose.com/temporary-license/) pro prioritní asistenci.

---

**Poslední aktualizace:** 2026-09-13  
**Testováno s:** Aspose.PSD pro Java 24.10  
**Autor:** Aspose

## Související tutoriály

- [Změna velikosti obrázku pomocí Aspose.PSD pro Java – Kreslení tvarů a základní operace s obrázky](/psd/java/basic-image-operations/)
- [Kreslení a uložení obdélníku v PSD pomocí Aspose.PSD pro Java](/psd/java/basic-image-operations/simple-drawing/)
- [Přidání podpisu k obrázku – Kreslení obrázku na plátno s Aspose.PSD pro Java](/psd/java/advanced-image-effects/add-signature-to-image/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}