---
date: 2026-09-03
description: Naučte se, jak v Java grafice nakreslit oblouk pomocí Aspose.PSD pro
  Java. Praktický průvodce krok za krokem s ukázkami kódu pro vytváření oblouků v
  souborech PSD.
keywords:
- java graphics draw arc
- how to draw arcs java
- Aspose.PSD arc drawing
lastmod: 2026-09-03
linktitle: Kreslení oblouků v Java
og_description: Naučte se, jak v Java grafice nakreslit oblouk pomocí Aspose.PSD pro
  Java. Tento tutoriál ukazuje předpoklady, kroky kódu a tipy pro vytváření oblouků
  v souborech PSD.
og_image_alt: Screenshot of a Java program drawing an arc using Aspose.PSD
og_title: Jak v Java grafice nakreslit oblouk – průvodce Aspose.PSD
schemas:
- author: Aspose
  dateModified: '2026-09-03'
  description: Learn how to java graphics draw arc using Aspose.PSD for Java. Step‑by‑step
    guide with code snippets for creating arcs in PSD files.
  headline: How to java graphics draw arc in Java
  type: TechArticle
- description: Learn how to java graphics draw arc using Aspose.PSD for Java. Step‑by‑step
    guide with code snippets for creating arcs in PSD files.
  name: How to java graphics draw arc in Java
  steps:
  - name: set up your Java project
    text: Create a new Java project in your favourite IDE and add the Aspose.PSD JAR
      to the build path. Ensure the JAR is referenced correctly so the compiler can
      locate the library classes.
  - name: import required packages
    text: 'To begin, import the necessary packages from Aspose.PSD for Java: The `Pen`
      class defines the colour, width, and style of the line used to draw the arc.
      These imports expose the `PsdImage`, `Graphics`, `Pen`, and colour classes needed
      for arc drawing.'
  - name: initialise image and graphics objects
    text: 'Create an instance of `PsdImage` and obtain a `Graphics` object to draw
      on: Replace `"Your Document Directory"` with the folder where you want the output
      files saved.'
  - name: define arc parameters
    text: 'Set the geometry and style of the arc—its bounding rectangle, start angle,
      sweep angle, colour, and thickness: Adjust the values to match the visual design
      you need; for example, a 200 px radius arc starting at 45° and sweeping 270°.'
  - name: draw the arc and save the image
    text: 'Invoke `drawArc` on the `Graphics` object and persist the PSD (or export
      to another format): The `drawArc` method of the `Graphics` class renders an
      arc defined by a bounding rectangle, start angle, and sweep angle using the
      specified `Pen`. The snippet draws the arc on the canvas and saves it as a '
  type: HowTo
- questions:
  - answer: Yes, the library can draw rectangles, ellipses, lines, polygons, and custom
      paths using the same `Graphics` API.
    question: Can Aspose.PSD for Java handle other shapes besides arcs?
  - answer: Create a `Pen` with the desired `Color` and width, then pass that `Pen`
      instance to `drawArc`.
    question: How do I change the arc colour and thickness?
  - answer: Absolutely. Aspose.PSD supports PNG, JPEG, TIFF, GIF and many more – just
      change the file extension in the `save` method.
    question: Is it possible to export the PSD to a format other than BMP?
  - answer: Visit the [Aspose.PSD forum](https://forum.aspose.com/c/psd/34) for tutorials,
      code samples, and assistance from other developers.
    question: Where can I find more examples and community support?
  - answer: Yes, it can process files up to 2 GB and render arcs without loading the
      entire document into memory, thanks to its streaming architecture.
    question: Does the library work with large PSD files?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- java graphics
- Aspose.PSD
- arc drawing
- PSD manipulation
title: Jak v Java grafice nakreslit oblouk
url: /cs/java/java-graphics-drawing/drawing-arcs/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Jak v Java grafice kreslit oblouk

## Úvod
V tomto tutoriálu se dozvíte, jak **java graphics draw arc** pomocí knihovny Aspose.PSD pro Java. Programové kreslení oblouků je běžnou potřebou pro vlastní UI komponenty, vizualizace dat a graficky bohaté zprávy. Aspose.PSD pro Java vám poskytuje plnou kontrolu nad soubory PSD (Photoshop Document), což vám umožní vytvářet, upravovat a exportovat obrázky bez nainstalovaného Photoshopu.

## Rychlé odpovědi
- **Která knihovna podporuje kreslení oblouků v Javě?** Aspose.PSD for Java.
- **Potřebuji licenci pro produkční použití?** Ano, pro ne‑zkušební nasazení je vyžadována komerční licence.
- **Do jakých formátů souborů mohu exportovat?** BMP, PNG, JPEG, TIFF, GIF a další.
- **Mohu změnit tloušťku a barvu oblouku?** Ano, pomocí objektu `Pen` předaného metodě `drawArc`.
- **Je API kompatibilní s Java 8 a novějšími?** Plně kompatibilní s Java 8‑21.

## Co je Java graphics draw arc?
`java graphics draw arc` odkazuje na proces vykreslování zakřiveného úseku—oblouku—na grafický povrch pomocí kreslicích API Javy. V kontextu Aspose.PSD se operace provádí na objektu `Graphics`, který představuje vrstvu uvnitř souboru PSD.

## Proč použít Aspose.PSD pro Java pro kreslení oblouků?
Aspose.PSD podporuje **více než 50** formátů obrázků a dokumentů, dokáže zpracovat soubory PSD o **velikosti až 2 GB** a zpracovává dokumenty s mnoha stovkami stránek, aniž by načítal celý soubor do paměti. Tento kvantifikovaný výkon jej činí ideálním pro generování grafiky na serveru, kde jsou důležité rychlost a využití paměti.

## Požadavky
1. **Java Development Environment** – Nainstalujte Javu z [Oracle's website](https://www.oracle.com/java/).  
2. **Aspose.PSD for Java Library** – Stáhněte nejnovější JAR ze [download page](https://releases.aspose.com/psd/java/). Postupujte podle poskytnutých instrukcí a přidejte JAR do classpath vašeho projektu.

## Jak v Java grafice kreslit oblouk?
Načtěte nový `PsdImage`, získejte jeho `Graphics` povrch, nakonfigurujte `Pen` s požadovanou barvou a tloušťkou a zavolejte `drawArc`. Tento stručný sled vytvoří oblouk a uloží výsledek v jedné metodické řetězci. Úpravou ohraničujícího obdélníku a úhlových parametrů můžete řídit velikost, umístění a rozsah oblouku tak, aby vyhovoval vašim návrhovým požadavkům.

### Krok 1: nastavení Java projektu
Vytvořte nový Java projekt ve svém oblíbeném IDE a přidejte Aspose.PSD JAR do cesty sestavení. Ujistěte se, že je JAR správně odkazován, aby kompilátor mohl najít třídy knihovny.

### Krok 2: import požadovaných balíčků
Pro začátek importujte potřebné balíčky z Aspose.PSD pro Java:
Třída `Pen` definuje barvu, šířku a styl čáry používané k vykreslení oblouku.
```java
import com.aspose.psd.Color;
import static com.aspose.psd.ColorAdjustType.Pen;
import com.aspose.psd.Graphics;
import com.aspose.psd.Image;
import com.aspose.psd.Pen;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.BmpOptions;
```  
Tyto importy zpřístupňují třídy `PsdImage`, `Graphics`, `Pen` a barvy potřebné pro kreslení oblouku.

### Krok 3: inicializace objektů obrázku a grafiky
Vytvořte instanci `PsdImage` a získejte objekt `Graphics` pro kreslení:
```java
String dataDir = "Your Document Directory";
// Initialize PsdImage object
PsdImage image = new PsdImage(100, 100);
// Initialize Graphics object and clear surface
Graphics graphics = new Graphics(image);
graphics.clear(Color.getYellow());
```  
Nahraďte `"Your Document Directory"` složkou, kam chcete uložit výstupní soubory.

### Krok 4: definice parametrů oblouku
Nastavte geometrii a styl oblouku — jeho ohraničující obdélník, počáteční úhel, úhel rozsahu, barvu a tloušťku:
```java
int width = 100;
int height = 200;
int startAngle = 45;
int sweepAngle = 270;
```  
Upravte hodnoty tak, aby odpovídaly požadovanému vizuálnímu designu; například oblouk s poloměrem 200 px začínající při 45° a protahující se 270°.

### Krok 5: vykreslení oblouku a uložení obrázku
Zavolejte `drawArc` na objektu `Graphics` a uložte PSD (nebo exportujte do jiného formátu):
Metoda `drawArc` třídy `Graphics` vykresluje oblouk definovaný ohraničujícím obdélníkem, počátečním úhlem a úhlem rozsahu pomocí zadaného `Pen`.
```java
// Draw arc with specified Pen object (black color) and parameters
graphics.drawArc(new Pen(Color.getBlack()), 0, 0, width, height, startAngle, sweepAngle);
// Save the image in BMP format
String outputPath = dataDir + "Arc.bmp";
BmpOptions saveOptions = new BmpOptions();
saveOptions.setBitsPerPixel(32);
image.save(outputPath, saveOptions);
```  
Ukázka vykreslí oblouk na plátně a uloží jej jako BMP soubor. Změňte příponu souboru v `outputPath`, pokud chcete exportovat do PNG, JPEG nebo TIFF.

## Časté problémy a řešení
- **Nesprávné jednotky úhlu** – Aspose.PSD očekává úhly ve stupních, ne v radiánech. Zadání radiánů povede k neočekávaným výsledkům.
- **Příliš velká tloušťka pera** – Velmi silná pera mohou způsobit, že oblouk přesáhne hranice obrázku; zmenšete tloušťku nebo zvětšete plátno.
- **Problémy s cestou k souboru** – Používejte absolutní cesty nebo zajistěte, aby pracovní adresář měl oprávnění k zápisu, aby se předešlo `IOException`.

## Často kladené otázky

**Q: Může Aspose.PSD pro Java zpracovávat jiné tvary kromě oblouků?**  
A: Ano, knihovna může kreslit obdélníky, elipsy, čáry, polygonové tvary a vlastní cesty pomocí stejného `Graphics` API.

**Q: Jak změním barvu a tloušťku oblouku?**  
A: Vytvořte `Pen` s požadovanou `Color` a šířkou a poté předávejte tuto instanci `Pen` metodě `drawArc`.

**Q: Je možné exportovat PSD do formátu jiného než BMP?**  
A: Rozhodně. Aspose.PSD podporuje PNG, JPEG, TIFF, GIF a mnoho dalších — stačí změnit příponu souboru v metodě `save`.

**Q: Kde najdu více příkladů a komunitní podporu?**  
A: Navštivte [Aspose.PSD forum](https://forum.aspose.com/c/psd/34) pro tutoriály, ukázky kódu a pomoc od dalších vývojářů.

**Q: Pracuje knihovna s velkými PSD soubory?**  
A: Ano, dokáže zpracovat soubory až do 2 GB a vykreslovat oblouky bez načítání celého dokumentu do paměti díky své streamovací architektuře.

---

**Poslední aktualizace:** 2026-09-03  
**Testováno s:** Aspose.PSD for Java 24.11  
**Autor:** Aspose

## Související tutoriály

- [Nakreslit a uložit obdélník v PSD pomocí Aspose.PSD pro Java](/psd/java/basic-image-operations/simple-drawing/)
- [Změna velikosti obrázku pomocí Aspose.PSD pro Java – Kreslení tvarů a základní operace s obrázky](/psd/java/basic-image-operations/)
- [Jak změnit barvu tahu v Javě pomocí Aspose.PSD](/psd/java/advanced-image-effects/add-stroke-layer-color/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}