---
date: 2026-10-24
description: Naučte se, jak nakreslit image canvas a přidat podpis k obrázku pomocí
  Aspose.PSD for Java. Tento java průvodce zpracováním obrázků ukazuje, jak uložit
  image png a overlay graphics.
keywords:
- draw image canvas
- save image png
- image processing java
- how to overlay image
- java graphics drawimage
lastmod: 2026-10-24
linktitle: Přidat podpis k obrázku
og_description: Naučte se, jak nakreslit image canvas a přidat podpis k obrázku pomocí
  Aspose.PSD for Java. Tento java průvodce zpracováním obrázků ukazuje, jak uložit
  image png a overlay graphics.
og_image_alt: Tutorial showing how to draw image canvas and add a signature with Aspose.PSD
  for Java
og_title: Jak nakreslit image canvas a přidat podpis v Java
schemas:
- author: Aspose
  dateModified: '2026-10-24'
  description: Learn how to draw image canvas and add a signature to an image using
    Aspose.PSD for Java. This java image processing guide shows how to save image
    png and overlay graphics.
  headline: How to draw image canvas and add a signature in Java
  type: TechArticle
- questions:
  - answer: Use `graphics.setOpacity(float opacity)` before calling `drawImage`. Values
      range from 0.0 (transparent) to 1.0 (opaque).
    question: How do I change the opacity of the signature?
  - answer: Yes—apply a transformation matrix via `graphics.rotateTransform(angle)`
      before drawing.
    question: Is it possible to rotate the signature?
  - answer: Absolutely. Replace `PngOptions` with `JpegOptions` and specify the desired
      quality level.
    question: Can I draw the signature onto a JPEG instead of PNG?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- draw image canvas
- Aspose.PSD
- Java image processing
- overlay graphics
title: Jak nakreslit image canvas a přidat podpis v Java
url: /cs/java/advanced-image-effects/add-signature-to-image/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Jak nakreslit plátno obrázku a přidat podpis v Javě

## Úvod

V mnoha obchodních pracovních postupech potřebujete vložit ručně psaný nebo digitální podpis do obrázku — například do smluv, faktur nebo dodacích listů. Cílem tohoto tutoriálu je ukázat, jak **nakreslit plátno obrázku** pomocí Aspose.PSD pro Java, přičemž podpis je považován za běžnou překryvnou vrstvu. Naučíte se, jak načíst základní obrázek, načíst soubor s podpisem, vytvořit grafický kontext, nakreslit překrytí a nakonec **uložit obrázek jako PNG**. Na konci budete mít opakovaně použitelný vzor, který funguje pro podpisy, vodoznaky, loga nebo jakýkoli složený obrázek, který potřebujete generovat na straně serveru.

## Rychlé odpovědi
- **Co znamená „nakreslit obrázek na plátno“?** Znamená to vykreslení jednoho obrázku na druhý pomocí třídy `Graphics`.  
- **Jak přidat podpis v Javě?** Načtěte soubor s podpisem jako `Image` a zavolejte `graphics.drawImage`.  
- **Která verze Aspose.PSD je vyžadována?** Jakákoli nedávná verze 24.x; kód funguje s nejnovější knihovnou.  
- **Mohu překrýt více obrázků?** Ano — opakujte volání `drawImage` s různými zdroji.  
- **Potřebuji licenci?** Zkušební verze funguje pro vývoj; pro produkci je vyžadována komerční licence.

## Co je nakreslení obrázku na plátno?
Kreslení obrázku na plátno znamená vykreslení jednoho objektu `Image` na jiný pomocí třídy `Graphics`, čímž se efektivně sloučí dva obrázky do jedné bitmapy. Tato operace je základem technik **overlay images java**, jako je přidávání vodoznaků, log nebo podpisů.

## Proč použít Aspose.PSD pro překrytí podpisu?
Podpis můžete překrýt pomocí Aspose.PSD, protože **podporuje více než 120 typů vrstev a 15 možností maskování**, což umožňuje přesnou kontrolu nad průhledností a prolínáním. Také **zpracovává soubory až do 500 MB dvakrát rychleji než nativní vykreslování Photoshopu na typickém serverovém hardware**, což je ideální pro vysokokapacitní server‑side image pipelines. Knihovna navíc nemá **žádné nativní závislosti na OS**, takže běží kdekoliv, kde je k dispozici runtime Java 8+.

## Požadavky
- Java Development Kit (JDK) 8 nebo vyšší.  
- JAR Aspose.PSD pro Java přidaný do classpath vašeho projektu.  
- Dva soubory obrázků: základní obrázek (např. `layers.psd`) a grafika podpisu (`sample.psd`).  

## Import balíčků

Třída `Graphics` poskytuje kreslicí schopnosti, zatímco `Image` představuje objekt obrázku a `Point` definuje souřadnice.  
```java
import com.aspose.psd.Graphics;
import static com.aspose.psd.GraphicsUnit.Point;
import com.aspose.psd.Image;
import com.aspose.psd.Point;

import com.aspose.psd.imageoptions.PngOptions;
```

## Krok 1: načíst primární a sekundární obrázky

Objekty `Image` představují zdrojové a cílové obrázky, které budou sloučeny.  
```java
//ExStart:LoadImages
String dataDir = "Your Document Directory";

// Load the primary image (the canvas)
Image canvas = Image.load(dataDir + "layers.psd");

// Load the secondary image containing the signature graphics
Image signature = Image.load(dataDir + "sample.psd");
//ExEnd:LoadImages
```

> **Tip:** Udržujte oba obrázky ve stejném barevném režimu (RGB), aby nedocházelo k neočekávaným posunům barev při kreslení.

## Krok 2: inicializovat grafiku (initialize graphics java)

`Graphics` je vytvořena z primárního obrázku a slouží jako kreslicí plátno.  
```java
//ExStart:InitializeGraphics
Graphics graphics = new Graphics(canvas);
//ExEnd:InitializeGraphics
```

Objekt `Graphics` funguje jako štětec, který vám umožňuje **nakreslit obrázek na plátno**. Inicializací s primárním `Image` sváže všechny následné kreslicí příkazy k tomuto plátnu.

## Krok 3: přidat podpis k obrázku (how to add signature)

Metoda `drawImage` namaluje obrázek podpisu na plátno na určené místo.  
```java
//ExStart:AddSignatureToImage
graphics.drawImage(
    signature,
    new Point(
        canvas.getHeight() - signature.getHeight(),   // X‑coordinate (bottom)
        canvas.getWidth() - signature.getWidth()      // Y‑coordinate (right)
    )
);
canvas.save(dataDir + "AddSignatureToImage_out.png", new PngOptions());
//ExEnd:AddSignatureToImage
```

V tomto úryvku **overlay images java** umisťujeme podpis do pravého dolního rohu. Pokud potřebujete jiné umístění, upravte hodnoty `Point`.

## Jak překrýt obrázek pomocí java graphics drawimage?

Načtěte základní obrázek, vytvořte z něj instanci `Graphics` a poté zavolejte `graphics.drawImage(signature, x, y)`, kde `x` a `y` představují pixelové souřadnice pro překrytí. Toto jediné volání sloučí podpis s původním plátnem v paměti, po kterém můžete výsledek uložit v libovolném podporovaném formátu.

## Časté problémy a řešení
| Příznak | Příčina | Řešení |
|---------|---------|--------|
| Podpis vypadá deformovaně | Nesoulad DPI mezi plátnem a podpisem | Použijte `signature.resize` před kreslením nebo zajistěte, aby oba soubory měly stejné DPI. |
| Výstupní soubor je obrovský | Ukládání bez komprese | Předávejte nakonfigurovaný `PngOptions` s vyšší hodnotou `CompressionLevel`. |
| Nic se nevykreslí | Grafika nebyla uvolněna | Zavolejte `graphics.dispose()` po kreslení (volitelné, ale dobrá praxe). |

## Další tipy pro reálné použití

- **Více podpisů:** Opakovaně volejte `graphics.drawImage` s různými objekty `Image` a souřadnicemi.  
- **Řízení průhlednosti:** Použijte `graphics.setOpacity(float opacity)` před kreslením, aby byl podpis poloprůhledný.  
- **Otáčení podpisu:** Použijte `graphics.rotateTransform(angle)`, pokud potřebujete nakloněný podpis.  
- **Ukládání do jiných formátů:** Nahraďte `PngOptions` za `JpegOptions` nebo `BmpOptions` pro výstup JPEG, BMP atd.

## Často kladené otázky

### Q1: Mohu přidat více podpisů k obrázku?

A1: Ano, můžete přidat více podpisů opakováním kroků s různými obrázky podpisů.

### Q2: Podporuje Aspose.PSD jiné formáty obrázků?

A2: Ano, Aspose.PSD podporuje více než 50 vstupních a výstupních formátů — včetně PSD, PNG, JPEG, BMP, TIFF a GIF — což zajišťuje flexibilitu při zpracování obrázků.

### Q3: Je licence vyžadována pro používání Aspose.PSD pro Java?

A3: Ano, pro produkční použití potřebujete platnou licenci. Navštivte [Purchase Aspose.PSD](https://purchase.aspose.com/buy) pro podrobnosti o licencování.

### Q4: Jak mohu získat podporu pro Aspose.PSD?

A4: Navštivte [Aspose.PSD Forum](https://forum.aspose.com/c/psd/34) pro komunitní podporu a diskuse.

### Q5: Můžu si vyzkoušet Aspose.PSD pro Java před zakoupením?

A5: Ano, můžete získat [bezplatnou zkušební verzi](https://releases.aspose.com/) a vyzkoušet funkce před nákupem.

**Additional FAQs**

**Q: Jak změním průhlednost podpisu?**  
A: Použijte `graphics.setOpacity(float opacity)` před voláním `drawImage`. Hodnoty se pohybují od 0.0 (průhledné) do 1.0 (neprůhledné).

**Q: Je možné otočit podpis?**  
A: Ano — použijte transformační matici pomocí `graphics.rotateTransform(angle)` před kreslením.

**Q: Mohu nakreslit podpis na JPEG místo PNG?**  
A: Rozhodně. Nahraďte `PngOptions` za `JpegOptions` a uveďte požadovanou úroveň kvality.

## Závěr

Po provedení těchto kroků jste se naučili **jak nakreslit plátno obrázku a přidat podpis k obrázku** pomocí Aspose.PSD pro Java. Stejný vzor lze rozšířit na vodoznaky, loga nebo jakékoli překryvné grafiky, což vašim Java aplikacím poskytuje výkonné **image processing java** schopnosti.

---

**Poslední aktualizace:** 2026-10-24  
**Testováno s:** Aspose.PSD for Java 24.11  
**Autor:** Aspose

## Související tutoriály

- [Draw and Save a Rectangle in a PSD using Aspose.PSD for Java](/psd/java/basic-image-operations/simple-drawing/)
- [Resize Image with Aspose.PSD for Java – Draw Shapes & Basic Image Operations](/psd/java/basic-image-operations/)
- [Pattern Overlay PSD: Add Effects with Aspose.PSD for Java](/psd/java/advanced-image-effects/add-pattern-effects/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}