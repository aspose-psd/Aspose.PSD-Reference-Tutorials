---
title: Převést AI na PNG v Javě
linktitle: Převést AI na PNG v Javě
second_title: Aspose.PSD Java API
description: Pomocí tohoto průvodce můžete snadno převést AI na PNG v Javě pomocí Aspose.PSD. Naučte se, jak bez námahy načíst, nastavit možnosti a uložit soubory AI jako obrázky PNG.
type: docs
weight: 13
url: /cs/java/java-ai-to-image-format-conversion/convert-ai-to-png/
---
## Zavedení
Chcete převést soubory Adobe Illustrator (.AI) na obrázky PNG pomocí Javy? Jste na správném místě! V tomto tutoriálu vás provedeme procesem krok za krokem pomocí výkonné knihovny Aspose.PSD for Java. Tato příručka vám pomůže pochopit, jak plynule převést soubory AI na vysoce kvalitní soubory PNG pomocí několika řádků kódu. Pojďme se rovnou ponořit!
## Předpoklady
Než začneme, je třeba mít připraveno několik věcí:
1. Java Development Kit (JDK): Ujistěte se, že máte na svém počítači nainstalovaný JDK 8 nebo vyšší.
2.  Aspose.PSD for Java: Potřebujete knihovnu Aspose.PSD for Java. Můžete si jej stáhnout z[Aspose stránku vydání](https://releases.aspose.com/psd/java/) nebo získat a[zkušební verze zdarma](https://releases.aspose.com/).
3. Integrované vývojové prostředí (IDE): Jakékoli Java IDE jako IntelliJ IDEA, Eclipse nebo NetBeans.
4. Základní znalost Javy: Základní znalost programování v Javě bude užitečná.
## Importujte balíčky
Nejprve budete muset importovat potřebné balíčky Aspose.PSD do vašeho projektu Java. Pojďme nastavit vaše prostředí.
```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.ai.AiImage;
import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.imageoptions.PngOptions;
```
Nyní, když máme naše prostředí nastavené, pojďme si proces převodu rozdělit do snadno srozumitelných kroků.
## Krok 1: Načtěte soubor AI
Prvním krokem v procesu převodu je načtení souboru AI do vaší Java aplikace pomocí knihovny Aspose.PSD.
```java
String dataDir = "Your Document Directory"; 
String sourceFileName = dataDir + "34992OStroke.ai";       
AiImage image = (AiImage)Image.load(sourceFileName);
```
## Krok 2: Nastavte možnosti PNG
Dále je třeba nastavit možnosti PNG. To zahrnuje definování typu barvy a jakýchkoli dalších nastavení specifických pro soubory PNG.
```java
PngOptions options = new PngOptions();
options.setColorType(PngColorType.TruecolorWithAlpha);
```
## Krok 3: Uložte obrázek jako PNG
Nakonec uložte načtený soubor AI jako obrázek PNG pomocí zadaných možností.
```java
String outFileName = dataDir + "34992OStroke.png";
image.save(outFileName, options);
```
A je to! Váš soubor AI byl úspěšně převeden na PNG.
## Závěr
Převod souborů AI do PNG v Javě je s Aspose.PSD hračkou. Podle kroků uvedených v této příručce můžete tuto funkci snadno integrovat do svých aplikací Java. Ať už pracujete na grafické aplikaci nebo potřebujete dávkově převádět soubory, Aspose.PSD poskytuje nástroje, které potřebujete k efektivnímu provedení práce.
## FAQ
### Co je Aspose.PSD?
Aspose.PSD je knihovna Java, která umožňuje vývojářům pracovat s PSD (Photoshop) a dalšími formáty souborů Adobe. Podporuje různé operace, jako je editace, konverze a vykreslování.
### Mohu používat Aspose.PSD zdarma?
 Aspose.PSD můžete použít s a[zkušební verze zdarma](https://releases.aspose.com/) , ale pro plnou funkčnost si budete muset zakoupit licenci. Můžete také získat a[dočasná licence](https://purchase.aspose.com/temporary-license/) pro účely hodnocení.
### Jaké formáty souborů podporuje Aspose.PSD?
Aspose.PSD podporuje PSD, PSB, AI a další formáty souborů Adobe. Umožňuje konverzi do různých obrazových formátů, jako jsou PNG, JPEG, BMP a TIFF.
### Je Aspose.PSD kompatibilní se všemi verzemi Javy?
Aspose.PSD je kompatibilní s JDK 8 a vyšší. Ujistěte se, že máte nainstalovanou příslušnou verzi JDK.
### Kde najdu další dokumentaci?
 Podrobnou dokumentaci najdete na[Dokumentační stránka Aspose.PSD](https://reference.aspose.com/psd/java/).