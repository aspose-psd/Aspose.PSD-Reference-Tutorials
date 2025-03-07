---
title: Přidejte diagonální vodoznak do souborů PSD pomocí Java
linktitle: Přidejte diagonální vodoznak do souborů PSD pomocí Java
second_title: Aspose.PSD Java API
description: Naučte se, jak snadno přidat diagonální vodoznak do souborů PSD pomocí Java s Aspose.PSD. Podrobný průvodce, jak své snímky sebevědomě vylepšit.
weight: 12
url: /cs/java/modifying-converting-psd-images/add-diagonal-watermark-psd-files/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Přidejte diagonální vodoznak do souborů PSD pomocí Java

## Zavedení
V dnešním digitálním světě může mít výrazný vizuál zásadní význam. Ať už jste návrhář, který chce chránit svou práci, nebo obchodník, který chce přidat do obrázků značku, použití vodoznaku je zásadní. V tomto tutoriálu prozkoumáme, jak přidat diagonální vodoznak do souborů PSD pomocí Javy s pomocí Aspose.PSD, výkonné knihovny pro manipulaci se soubory PSD.
## Předpoklady
Než se pustíme do šťavnaté části kódování, musíte se ujistit, že máte nastaveno několik věcí:
### 1. Vývojové prostředí Java
 Ujistěte se, že máte na svém počítači nainstalovanou Javu. Nejnovější verzi si můžete stáhnout z[webové stránky Java](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).
### 2. Aspose.PSD Library
 Pro práci se soubory PSD budete potřebovat knihovnu Aspose.PSD. Můžete si jej stáhnout z[Stránka Aspose Downloads](https://releases.aspose.com/psd/java/)V závislosti na struktuře vašeho projektu můžete používat Maven nebo jiný nástroj pro správu závislostí, takže jej můžete začlenit podle svých potřeb.
### 3. Základní porozumění Javě
Dobrá znalost jazyka Java vám pomůže hladce sledovat tento tutoriál. Ujistěte se, že jste spokojeni s třídami, objekty a základní manipulací se soubory v Javě.
### 4. Nastavení IDE
Ke kódování použijte libovolné integrované vývojové prostředí (IDE), jako je IntelliJ IDEA, Eclipse nebo NetBeans. To značně usnadňuje kódování, nemyslíte?
## Importujte balíčky
Chcete-li manipulovat se soubory PSD, budete muset importovat konkrétní balíčky z Aspose.PSD. Zde jsou balíčky, které musíte zahrnout do horní části souboru Java:
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
Nyní, když máme naše předpoklady roztříděné a potřebné balíčky importované, pojďme si projít kroky přidání diagonálního vodoznaku do souboru PSD.
## Krok 1: Nastavte svůj adresář
```java
String dataDir = "Your Document Directory";
```
Nejprve budete muset určit adresář, kde jsou umístěny vaše soubory PSD. Tento adresář bude výchozím bodem pro načtení obrázku. Takže vyměnit`"Your Document Directory"` se skutečnou cestou, kde se nachází váš soubor PSD.
## Krok 2: Načtěte soubor PSD
```java
PsdImage psdImage = (PsdImage)Image.load(dataDir + "layers.psd");
```
 Nyní načteme soubor PSD, se kterým chcete pracovat. The`Image.load` metoda načte soubor a přenese jej do a`PsdImage` objekt. Ujistěte se, že jste uvedli přesný název vašeho souboru PSD, což je v tomto případě`"layers.psd"`.
## Krok 3: Vytvořte grafický objekt
```java
Graphics graphics = new Graphics(psdImage);
```
 V tomto kroku vytvoříme a`Graphics` objekt, který nám umožňuje provádět operace kreslení na načteném obrázku. Berte to jako přípravu plátna, kam můžeme namalovat náš vodoznak.
## Krok 4: Vytvořte písmo pro vodoznak
```java
Font font = new Font("Arial", 20.0f);
```
Zde definujeme styl a velikost písma pro text vodoznaku. V tomto případě jsme zvolili Arial o velikosti 20. Můžete si vybrat libovolné písmo, které máte nainstalované ve vašem systému – trochu to okořeňte!
## Krok 5: Vytvořte štětec pro vodoznak
```java
SolidBrush brush = new SolidBrush(Color.fromArgb(50, 128, 128, 128));
```
 Dále vytvoříme a`SolidBrush` objekt, který obarví náš vodoznak. The`Color.fromArgb`metoda přebírá čtyři parametry: alfa, červená, zelená a modrá. Hodnota alfa řídí průhlednost (0 je plně průhledná a 255 je plně neprůhledná). Nastavili jsme to na 50 pro pěkný poloprůhledný efekt.
## Krok 6: Nastavte transformační matici
```java
graphics.setTransform(new Matrix());
graphics.getTransform().rotateAt(45, new PointF(psdImage.getWidth() / 2, psdImage.getHeight() / 2));
```
 Tady se děje kouzlo! Vytvoříme transformační matici pro otočení vodoznaku. The`rotateAt` funkce má dva parametry: úhel (45 stupňů pro diagonální pohled) a bod, kolem kterého se má otáčet (což je v našem případě střed obrázku).
## Krok 7: Definujte zarovnání řetězců
```java
StringFormat sf = new StringFormat();
sf.setAlignment(StringAlignment.Center);
```
 Musíme zajistit, aby byl náš vodoznak vycentrován. The`StringFormat` class nám s tím pomáhá, zarovnává text dokonale na střed obrázku. Koneckonců, kdo má rád chaotická umístění?
## Krok 8: Nakreslete vodoznak
```java
graphics.drawString("Some watermark text", font, brush, new RectangleF(0, psdImage.getHeight() / 2, psdImage.getWidth(), psdImage.getHeight() / 2), sf);
```
 Nyní je čas skutečně nakreslit vodoznak! Pomocí`drawString`způsob, určíme obsah našeho vodoznaku (neváhejte si text upravit), písmo, štětec, oblast, kam ho chceme nakreslit, a nastavení zarovnání. Váš vodoznak bude použit pomocí parametrů, které jsme nastavili v obdélníku!
## Krok 9: Uložte obrázek
```java
psdImage.save(dataDir + "AddDiagnolWatermark_output.png", new PngOptions());
```
 Nakonec náš upravený obrázek uložíme. Zde jej exportujeme jako soubor PNG. Ujistěte se, že jste výstupnímu souboru dali jedinečný název, aby nepřepsal žádné existující soubory. The`PngOptions` class pomáhá určit formát obrázku.
## Závěr
A právě tak jste úspěšně přidali diagonální vodoznak do svého souboru PSD pomocí Java! Je to přímočarý proces, který však může výrazně zvýšit profesionalitu vašich snímků. Ať už chráníte své umělecké dílo nebo propagujete svou značku, vodoznak je jednoduché, ale účinné řešení.

## FAQ
### Co je Aspose.PSD?
Aspose.PSD je knihovna Java používaná pro práci a manipulaci se soubory PSD bez nutnosti aplikace Adobe Photoshop.
### Mohu pro vodoznak použít jiná písma?
Ano, pro vodoznak si můžete vybrat libovolné písmo, které je nainstalováno ve vašem systému.
### Existuje způsob, jak upravit průhlednost vodoznaku?
Absolutně! Můžete upravit hodnotu alfa v SolidBrush a změnit průhlednost.
### Mohu přidat více vodoznaků?
 Ano, můžete zavolat na`drawString` metoda vícekrát s různými parametry pro přidání více vodoznaků.
### Kde najdu více informací o Aspose.PSD?
 Můžete zkontrolovat dokumentaci[zde](https://reference.aspose.com/psd/java/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
