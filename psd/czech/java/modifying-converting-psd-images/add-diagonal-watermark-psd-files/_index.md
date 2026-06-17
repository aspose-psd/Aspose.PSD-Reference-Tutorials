---
date: 2026-03-04
description: Naučte se, jak v Javě vytvořit grafický objekt a přidat diagonální vodoznak
  do souborů PSD pomocí Aspose.PSD. Tento krok‑za‑krokem průvodce pokrývá použití
  knihovny pro vodoznaky v Javě.
linktitle: Add Diagonal Watermark to PSD Files with Java
second_title: Aspose.PSD Java API
title: Vytvoření grafického objektu v Javě – Diagonální vodoznak pro PSD
url: /cs/java/modifying-converting-psd-images/add-diagonal-watermark-psd-files/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Přidání šikmého vodoznaku do souborů PSD pomocí Javy

## Introduction
V tomto tutoriálu **create graphics object java** a použijete jej k přidání šikmého vodoznaku do souborů PSD. Ať už jste designér chránící své dílo nebo marketér značící obrázky, čistý vodoznak může učinit vaši práci profesionální a zabezpečenou. Provedeme vás každým krokem s jasnými vysvětleními, takže můžete rychle aplikovat techniku ve svých projektech.

## Quick Answers
- **Jakou knihovnu potřebuji?** Aspose.PSD for Java (a robust java image watermark library).  
- **Jaké primární klíčové slovo tento tutoriál pokrývá?** create graphics object java.  
- **Potřebuji licenci?** Bezplatná zkušební verze funguje pro testování; pro produkční nasazení je vyžadována komerční licence.  
- **Mohu změnit text a styl vodoznaku?** Ano – můžete přizpůsobit font, barvu, průhlednost a rotaci.  
- **Jaké výstupní formáty jsou podporovány?** Příklad ukládá jako PNG, ale Aspose.PSD může exportovat do PSD, JPEG, BMP a dalších.

## What is a Graphics Object in Java?
Objekt **Graphics** představuje kreslicí plochu pro obrázek. Vytvořením grafického objektu získáte přístup k metodám, které umožňují vykreslovat text, tvary a další vizuální prvky přímo na bitmapu nebo plátno PSD. Toto je základní koncept za primárním klíčovým slovem **create graphics object java**.

## Why Use Aspose.PSD for Watermarking?
Aspose.PSD je specializovaná **java image watermark library**, která funguje bez Adobe Photoshopu. Poskytuje plnou kontrolu nad vrstvami, vykreslováním textu a transformacemi obrázku, což ji činí ideální pro server‑side zpracování nebo dávkové operace.

## Prerequisites
Než se pustíme do kódu, ujistěte se, že máte následující:

### 1. Java Development Environment
Instalujte nejnovější JDK z [Java website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).

### 2. Aspose.PSD Library
Stáhněte knihovnu ze [Aspose Downloads page](https://releases.aspose.com/psd/java/). Přidejte JAR do projektu pomocí Maven, Gradle nebo ručního zahrnutí do classpath.

### 3. Basic Understanding of Java
Základní znalost Javy – třídy, objekty a souborové I/O vám pomůže plynule sledovat tutoriál.

### 4. IDE Setup
Použijte IntelliJ IDEA, Eclipse nebo NetBeans pro pohodlné programování.

## Import Packages
Pro manipulaci se soubory PSD importujte potřebné třídy Aspose.PSD:

```java
import com.aspose.psd.Color;
import com.aspose.psd.Font;
import com.aspose.psd.Graphics;
import com.aspose.psd.Image;
import com.aspose.psd.Matrix;
import com.aspose.psd.PointF;
import com.aspose.psd.RectangleF;
import com.aspose.psd.StringAlignment;
import com.aspose.psd.StringFormat;
import com.aspose.psd.brushes.SolidBrush;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.PngOptions;
```

Nyní, když máme připravené předpoklady a potřebné balíčky importovány, projdeme kroky pro přidání šikmého vodoznaku do souboru PSD.

## Step 1: Set Up Your Directory
```java
String dataDir = "Your Document Directory";
```
Nahraďte `"Your Document Directory"` cestou ke složce, která obsahuje váš zdrojový soubor PSD.

## Step 2: Load the PSD File
```java
PsdImage psdImage = (PsdImage)Image.load(dataDir + "layers.psd");
```
Metoda `Image.load` načte soubor a přetypuje jej na `PsdImage`, aby bylo možné pracovat s funkcemi specifickými pro PSD.

## Step 3: Create a Graphics Object
```java
Graphics graphics = new Graphics(psdImage);
```
Zde **create graphics object java**—plátno, na kterém nakreslíme vodoznak.

## Step 4: Create a Font for the Watermark
```java
Font font = new Font("Arial", 20.0f);
```
Vyberte libovolný nainstalovaný font; velikost určuje, jak výrazný bude vodoznak.

## Step 5: Create a Brush for the Watermark
```java
SolidBrush brush = new SolidBrush(Color.fromArgb(50, 128, 128, 128));
```
Parametr `alpha` (první parametr) nastavuje průhlednost. Alfa = 50 dává jemný, poloprůhledný vzhled.

## Step 6: Set Up the Transform Matrix
```java
graphics.setTransform(new Matrix());
graphics.getTransform().rotateAt(45, new PointF(psdImage.getWidth() / 2, psdImage.getHeight() / 2));
```
Otočíme kreslicí plochu o 45° kolem středu obrázku, čímž vytvoříme šikmý efekt.

## Step 7: Define String Alignment
```java
StringFormat sf = new StringFormat();
sf.setAlignment(StringAlignment.Center);
```
Zarovnání na střed zajišťuje, že vodoznak bude pěkně uprostřed otočeného obdélníku.

## Step 8: Draw the Watermark
```java
graphics.drawString("Some watermark text", font, brush, new RectangleF(0, psdImage.getHeight() / 2, psdImage.getWidth(), psdImage.getHeight() / 2), sf);
```
Nahraďte `"Some watermark text"` názvem vaší značky nebo upozorněním na autorská práva. Obdélník určuje, kde bude text vykreslen.

## Step 9: Save the Image
```java
psdImage.save(dataDir + "AddDiagnolWatermark_output.png", new PngOptions());
```
Výstup je uložen jako PNG, ale můžete zvolit libovolný formát podporovaný Aspose.PSD.

## Common Use Cases
- **Ochrana značky:** Přidejte poloprůhledné logo, aby se zabránilo neoprávněnému použití.  
- **Dávkové zpracování:** Automatizujte vodoznakování velkých knihoven obrázků na serveru.  
- **Kreativní náhledy:** Ukazujte vodoznakované koncepty klientům, přičemž originální soubory zůstávají nedotčeny.

## Troubleshooting & Tips
- **Průhlednost není vidět?** Zvyšte hodnotu alfa (např. `100`) pro silnější vodoznak.  
- **Vodoznak je mimo střed?** Ověřte, že bod otáčení používá přesné dělení šířky/výšky obrázku.  
- **Obavy o výkon:** Znovu použijte stejný objekt `Graphics` při zpracování více obrázků ve smyčce.

## FAQ's
### What is Aspose.PSD?
Aspose.PSD je Java knihovna pro práci a manipulaci se soubory PSD bez nutnosti Adobe Photoshopu.

### Can I use other fonts for watermarking?
Ano, můžete zvolit libovolný font, který je nainstalován ve vašem systému, pro vodoznakování.

### Is there a way to customize the watermark's transparency?
Určitě! Můžete upravit hodnotu alfa v `SolidBrush`, abyste změnili průhlednost.

### Can I add multiple watermarks?
Ano, můžete volat metodu `drawString` vícekrát s různými parametry a přidat tak více vodoznaků.

### Where can I find more information about Aspose.PSD?
Více informací najdete v dokumentaci [zde](https://reference.aspose.com/psd/java/).

---

**Last Updated:** 2026-03-04  
**Tested With:** Aspose.PSD 24.12 for Java  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}