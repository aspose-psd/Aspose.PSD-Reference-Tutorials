---
title: Převést PSB na JPG v Javě
linktitle: Převést PSB na JPG v Javě
second_title: Aspose.PSD Java API
description: Snadno převeďte PSB na JPG v Javě pomocí Aspose.PSD. Postupujte podle našeho podrobného průvodce pro bezproblémové převody obrázků. Stáhněte si, vyzkoušejte a kupte Aspose.PSD.
type: docs
weight: 10
url: /cs/java/java-psb-to-image-format-conversion/convert-psb-to-jpg-java/
---
## Úvod
Vítejte v našem komplexním průvodci převodem souborů PSB do formátu JPG pomocí Aspose.PSD pro Java! Pokud máte co do činění se soubory PSB – těmi velkými, vrstvenými soubory Photoshopu – a potřebujete je převést do univerzálněji podporovaného formátu JPG, jste na správném místě. V tomto tutoriálu vás provedeme procesem krok za krokem. Na konci budete moci bez problémů převádět soubory PSB na JPG.
## Předpoklady
Než se ponoříme do tutoriálu, pokryjeme předpoklady. Pro začátek budete potřebovat:
-  Java Development Kit (JDK): Ujistěte se, že máte v systému nainstalovaný JDK. Můžete si jej stáhnout z[Web společnosti Oracle](https://www.oracle.com/java/technologies/javase-downloads.html).
-  Aspose.PSD for Java Library: Stáhněte si knihovnu Aspose.PSD for Java z[stránka ke stažení](https://releases.aspose.com/psd/java/).
- Vývojové prostředí: IDE jako IntelliJ IDEA, Eclipse nebo jakýkoli textový editor podle vašeho výběru.
- Soubor PSB: Soubor PSB, který chcete převést.
## Import balíčků
Nejprve naimportujme potřebné balíčky. Tyto importy jsou nezbytné pro práci s knihovnou Aspose.PSD a zpracování převodů obrázků.
```java
import com.aspose.psd.Image;
import com.aspose.psd.examples.Utils.Utils;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
import com.aspose.psd.imageoptions.JpegOptions;
```
## Krok 1: Nastavte svůj projekt
Než začnete kódovat, nastavte svůj projekt Java. Vytvořte nový projekt ve svém IDE a přidejte knihovnu Aspose.PSD for Java do cesty sestavení vašeho projektu. To vám umožní používat třídy a metody poskytované Aspose.PSD.
## Krok 2: Načtěte soubor PSB
 Chcete-li načíst soubor PSB, budete muset zadat cestu k souboru a použít soubor`PsdLoadOptions` pro konfiguraci procesu načítání. Postup je následující:
```java
String dataDir = "Your Document Directory"; // Nahraďte svou cestu k adresáři
String sourceFileName = dataDir + "Simple.psb";
PsdLoadOptions options = new PsdLoadOptions();
PsdImage image = (PsdImage) Image.load(sourceFileName, options);
```
 V tomto kroku nastavujeme adresář, kde se nachází váš soubor PSB, a načítáme soubor do a`PsdImage` pomocí objektu`PsdLoadOptions`.
## Krok 3: Nakonfigurujte možnosti JPG
Nyní, když je váš soubor PSB načten, musíte nastavit možnosti pro převod JPG. To zahrnuje specifikaci kvality výstupu JPG.
```java
JpegOptions jpgOptions = new JpegOptions();
jpgOptions.setQuality(95);
```
 Zde vytváříme a`JpegOptions` objekt a nastavení kvality na 95. Tuto hodnotu můžete upravit, abyste řídili kompresi a kvalitu výstupního obrazu.
## Krok 4: Uložte obrázek jako JPG
S nastavenými možnostmi jste připraveni uložit svůj PSB soubor jako JPG. Zde dochází ke skutečné konverzi.
```java
image.save(dataDir + "Simple_output.jpg", jpgOptions);
```
Tento příkaz uloží načtený obraz PSB jako JPG do určeného adresáře s definovaným nastavením kvality.
## Krok 5: Uložte obrázek jako PSB (volitelné)
Pokud chcete upravený obrázek uložit zpět jako soubor PSB, můžete tak učinit pomocí podobného příkazu:
```java
image.save(dataDir + "Simple_output.psb");
```
Tento krok je volitelný, ale užitečný, pokud potřebujete zachovat vrstvený formát původního souboru PSB spolu s převedeným JPG.
## Závěr
Gratulujeme! Úspěšně jste převedli soubor PSB na JPG pomocí Aspose.PSD for Java. Tento tutoriál vás provede nastavením projektu, načtením souboru PSB, konfigurací možností JPG a uložením převedeného obrázku. Podle těchto kroků můžete snadno zvládnout převody PSB na JPG ve vašich aplikacích Java.
Ať už jste vývojář pracující na aplikaci pro zpracování obrazu nebo jen občas potřebujete převést PSB soubory, Aspose.PSD for Java poskytuje robustní řešení pro vaše potřeby.
## FAQ
### Co je Aspose.PSD for Java?
Aspose.PSD for Java je knihovna, která umožňuje vývojářům manipulovat a převádět soubory PSD a PSB v aplikacích Java. Podporuje různé funkce včetně načítání, úprav a ukládání souborů Photoshopu.
### Mohu vyzkoušet Aspose.PSD pro Javu před nákupem?
 Ano, můžete si stáhnout bezplatnou zkušební verzi Aspose.PSD pro Javu z webu[stránka ke stažení](https://releases.aspose.com/). To vám umožní ohodnotit knihovnu a její funkce před nákupem.
### Jak získám dočasnou licenci pro Aspose.PSD pro Javu?
Dočasnou licenci můžete získat od[dočasná licenční stránka](https://purchase.aspose.com/temporary-license/). To vám umožní využívat všechny funkce knihovny po omezenou dobu.
### Je k dispozici podpora, pokud narazím na problémy?
 Absolutně! K podpoře se můžete dostat přes[Fórum podpory Aspose.PSD](https://forum.aspose.com/c/psd/34). Tým podpory je pohotový a připravený vám pomoci s jakýmikoli problémy nebo dotazy, které můžete mít.
### Mohu upravit kvalitu výstupu JPG?
 Ano, kvalitu výstupu JPG můžete upravit nastavením`Quality` nemovitost v`JpegOptions` objekt. Hodnota se pohybuje od 0 do 100, přičemž vyšší hodnoty znamenají lepší kvalitu a nižší kompresi.