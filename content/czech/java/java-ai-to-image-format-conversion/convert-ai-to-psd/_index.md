---
title: Převést AI na PSD v Javě
linktitle: Převést AI na PSD v Javě
second_title: Aspose.PSD Java API
description: Převeďte AI na PSD v Javě pomocí Aspose.PSD s naším jednoduchým průvodcem krok za krokem. Ideální pro vývojáře, kteří potřebují rychlou a bezproblémovou konverzi souborů.
type: docs
weight: 14
url: /cs/java/java-ai-to-image-format-conversion/convert-ai-to-psd/
---
## Zavedení
Chcete převést soubory AI (Adobe Illustrator) na soubory PSD (Adobe Photoshop) pomocí Javy? Tak to jste na správném místě! Dnes prozkoumáme, jak tento úkol splnit pomocí výkonné knihovny Aspose.PSD pro Java. Tato příručka vás provede vším, co potřebujete vědět, od předpokladů až po podrobné pokyny krok za krokem. Pojďme se ponořit a bez problémů transformovat soubory návrhu.
## Předpoklady
Než začneme, je třeba mít připraveno několik věcí:
1. Java Development Kit (JDK): Ujistěte se, že máte v systému nainstalovaný JDK 8 nebo vyšší.
2.  Aspose.PSD for Java: Stáhněte si knihovnu Aspose.PSD for Java z[stránka ke stažení](https://releases.aspose.com/psd/java/).
3. Integrované vývojové prostředí (IDE): IDE jako IntelliJ IDEA nebo Eclipse pro psaní a spouštění vašeho kódu Java.
4. AI File: Soubor Adobe Illustrator, který chcete převést.
5.  Aspose Temporary License (Volitelné): Pro plnou funkčnost bez omezení můžete získat a[dočasná licence](https://purchase.aspose.com/temporary-license/).
## Importujte balíčky
Nejprve nastavíme náš projekt importem potřebných balíčků. Budete muset zahrnout Aspose.PSD pro Javu do cesty třídy vašeho projektu. Jak na to:
```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.ai.AiImage;
import com.aspose.psd.imageoptions.PsdOptions;
```
 Případně si můžete stáhnout soubor JAR z[Aspose.PSD pro stahování Java stránky](https://releases.aspose.com/psd/java/) a přidejte jej do projektu ručně.
Pojďme si tento proces rozdělit na jednoduché, zvládnutelné kroky.
## Krok 1: Nastavení vašeho projektu
Nejprve nastavte svůj projekt v preferovaném IDE.
### Vytvořit nový projekt
1. Otevřete své IDE a vytvořte nový Java projekt.
2. Pojmenujte svůj projekt něčím smysluplným, například „AItoPSDConverter“.
### Přidejte knihovnu Aspose.PSD
1. Pokud jste si stáhli soubor JAR, přidejte jej do cesty sestavení vašeho projektu.
2.  Pokud používáte Maven, ujistěte se, že je závislost správně přidána do vaší`pom.xml`.
## Krok 2: Načtení souboru AI
Nyní, když je váš projekt nastaven, načteme soubor AI, který chcete převést.
```java
String dataDir = "Your Document Directory"; 
String sourceFileName = dataDir + "34992OStroke.ai";       
AiImage image = (AiImage) Image.load(sourceFileName);
```
## Krok 3: Nastavení možností PSD
Dále musíme nastavit možnosti pro náš výstup PSD.
```java
PsdOptions options = new PsdOptions();
```
## Krok 4: Uložení souboru AI jako PSD
S načteným souborem AI a nastavenými možnostmi jej nyní můžeme uložit jako soubor PSD.
```java
String outFileName = dataDir + "34992OStroke.psd";
image.save(outFileName, options);
```
## Závěr
A tady to máte! Úspěšně jste převedli soubor AI na soubor PSD pomocí Aspose.PSD for Java. Tato výkonná knihovna usnadňuje zpracování složitých převodů souborů ve vašich aplikacích Java. Ať už jste zkušený vývojář nebo teprve začínáte, tato příručka by vám měla pomoci snadno integrovat funkci převodu AI na PSD do vašich projektů.
## FAQ
### Co je Aspose.PSD for Java?
Aspose.PSD for Java je robustní knihovna, která umožňuje vývojářům vytvářet, upravovat a převádět soubory Photoshopu (PSD a PSB) v aplikacích Java, aniž by potřebovali Adobe Photoshop.
### Mohu používat Aspose.PSD pro Javu zdarma?
 Aspose.PSD for Java nabízí bezplatnou zkušební verzi, kterou si můžete stáhnout z webu[zkušební stránka zdarma](https://releases.aspose.com/) . Pro plné funkce a[licence](https://purchase.aspose.com/buy) je vyžadováno.
### Jak získám dočasnou licenci pro Aspose.PSD pro Javu?
 Dočasnou licenci můžete získat od[dočasná licenční stránka](https://purchase.aspose.com/temporary-license/).
### Je možné převést soubory PSD zpět na soubory AI?
V současné době Aspose.PSD for Java nepodporuje převod souborů PSD zpět na soubory AI. Zaměřuje se na práci se soubory PSD a PSB.
### Kde najdu další příklady a dokumentaci?
 Kompletní dokumentaci a příklady naleznete na[Stránka dokumentace Aspose.PSD pro Java](https://reference.aspose.com/psd/java/).