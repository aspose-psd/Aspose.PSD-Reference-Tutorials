---
date: 2026-06-08
description: Naučte se, jak uložit PSD jako PNG pomocí Aspose.PSD for Java a přerušit
  konverzi podle potřeby. Efektivně spravujte workflow obrázků.
keywords:
- save psd as png
- how to interrupt conversion
- psd to png conversion
- manage image workflow
linktitle: Podpora pro Interrupt Monitor
schemas:
- author: Aspose
  dateModified: '2026-06-08'
  description: Learn how to save PSD as PNG using Aspose.PSD for Java and interrupt
    conversion when needed. Manage image workflow efficiently.
  headline: How to Save PSD as PNG with Interrupt Monitor in Aspose.PSD for Java
  type: TechArticle
- description: Learn how to save PSD as PNG using Aspose.PSD for Java and interrupt
    conversion when needed. Manage image workflow efficiently.
  name: How to Save PSD as PNG with Interrupt Monitor in Aspose.PSD for Java
  steps:
  - name: Set Your Document Directory
    text: Ensure to replace “Your Document Directory” with the actual path where your
      PSD documents are stored.
  - name: Define Image Options and Output Path
    text: Specify the image options, source PSD file, and the desired output path
      for the converted image.
  - name: Initialize Interrupt Monitor and SaveImageWorker
    text: The `InterruptMonitor` class watches a running conversion and can interrupt
      it when `requestInterrupt()` is called. Create instances of `InterruptMonitor`
      and `SaveImageWorker`, linking the monitor to the image conversion worker.
  - name: Start Image Conversion Thread
    text: Initiate a new thread for the image conversion process and introduce a timeout
      period to anticipate interruption.
  - name: Interrupt the Process
    text: Calling `monitor.requestInterrupt()` signals the monitor to abort the ongoing
      conversion. Interrupt the image conversion process using the `InterruptMonitor`
      and wait for the interruption to complete. Finally, clean up by deleting the
      output file.
  type: HowTo
- questions:
  - answer: Yes, use `InterruptMonitor` to stop the process on demand.
    question: Can I interrupt a PSD‑to‑PNG conversion?
  - answer: Call `save(outputPath, new PngOptions())`.
    question: Which method saves a PSD as PNG?
  - answer: A commercial license is required; a free trial is available.
    question: Do I need a license for production?
  - answer: Java 8 and later are fully supported.
    question: What Java version is supported?
  - answer: Conversions can run in separate threads; the monitor handles interruptions
      safely.
    question: Is the library thread‑safe?
  type: FAQPage
second_title: Aspose.PSD Java API
title: Jak uložit PSD jako PNG s Interrupt Monitor v Aspose.PSD for Java
url: /cs/java/advanced-techniques/support-interrupt-monitor/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Uložit PSD jako PNG s Interrupt Monitor v Aspose.PSD pro Java

## Úvod

Pokud potřebujete **uložit PSD jako PNG** a zároveň mít plnou kontrolu nad dlouhodobými konverzemi, Interrupt Monitor v Aspose.PSD pro Java vám to přesně umožní. V tomto tutoriálu vás provedeme nastavením monitoru, konverzí souboru PSD na PNG a bezpečným přerušením operace podle potřeby. Také uvidíte, jak to zapadá do typického pracovního postupu zpracování obrazu a proč je to nezbytné pro robustní aplikace.

## Rychlé odpovědi
- **Mohu přerušit konverzi PSD‑to‑PNG?** Ano, použijte `InterruptMonitor` k zastavení procesu na požádání.  
- **Která metoda ukládá PSD jako PNG?** Zavolejte `save(outputPath, new PngOptions())`.  
- **Potřebuji licenci pro produkci?** Je vyžadována komerční licence; je k dispozici bezplatná zkušební verze.  
- **Jaká verze Javy je podporována?** Java 8 a novější jsou plně podporovány.  
- **Je knihovna thread‑safe?** Konverze mohou běžet ve zvláštních vláknech; monitor bezpečně zpracovává přerušení.

## Požadavky

Než se ponoříte do detailů používání Interrupt Monitor, ujistěte se, že máte následující požadavky připravené:

- **Java Development Environment:** Nastavte vývojové prostředí Java na vašem systému.  
- **Aspose.PSD Library:** Získejte knihovnu Aspose.PSD pro Java. Můžete ji stáhnout [zde](https://releases.aspose.com/psd/java/). Také můžete navštívit hlavní stránku Aspose [zde](https://releases.aspose.com/).  
- **Document Directory:** Mějte určený adresář pro vaše PSD dokumenty.

## Importovat balíčky

Začněte importováním potřebných balíčků do vašeho Java projektu. Tím zajistíte přístup k funkcím Aspose.PSD.

```java
import com.aspose.psd.ImageOptionsBase;

import static com.aspose.psd.examples.Utils.Utils.getDateTime;
import com.aspose.psd.imageoptions.PngOptions;
import com.aspose.psd.multithreading.InterruptMonitor;
import com.aspose.psd.system.Threading.ThreadStart;
import java.io.File;
```

Nyní rozdělíme ukázkový kód na krok‑za‑krokem průvodce pro začlenění Interrupt Monitor do vašeho projektu Aspose.PSD pro Java.

## Jak uložit PSD jako PNG pomocí Interrupt Monitor?

`PsdImage` představuje PSD dokument načtený do paměti.  
`SaveImageWorker` provádí konverzi obrazu v samostatném vlákně.  

Načtěte svůj PSD soubor pomocí `new PsdImage("source.psd")`, připojte `InterruptMonitor` k `SaveImageWorker` a zavolejte `save("output.png", new PngOptions())`. Monitor sleduje požadavek na zrušení a čistě přeruší konverzi, čímž vrátí kontrolu vaší aplikaci během milisekund.

### Krok 1: Nastavte svůj adresář dokumentů

```java
String dataDir = "Your Document Directory";
```

Ujistěte se, že nahradíte „Your Document Directory“ skutečnou cestou, kde jsou uloženy vaše PSD dokumenty.

### Krok 2: Definujte možnosti obrazu a výstupní cestu

```java
ImageOptionsBase saveOptions = new PngOptions();
String source = dataDir + "big2.psb";
String output = dataDir + "big_out.png";
```

Zadejte možnosti obrazu, zdrojový PSD soubor a požadovanou výstupní cestu pro převedený obrázek.

### Krok 3: Inicializujte Interrupt Monitor a SaveImageWorker

Třída `InterruptMonitor` sleduje probíhající konverzi a může ji přerušit, když je zavolána metoda `requestInterrupt()`.

```java
InterruptMonitor monitor = new InterruptMonitor();
SaveImageWorker worker = new SaveImageWorker(source, output, saveOptions, monitor);
```

Vytvořte instance `InterruptMonitor` a `SaveImageWorker`, propojující monitor s pracovníkem konverze obrazu.

### Krok 4: Spusťte vlákno konverze obrazu

```java
Thread thread = new Thread(worker.ThreadProc());
try {
    thread.start();
    // Add a timeout to allow for potential interruption
    Thread.sleep(3000);
```

Zahajte nové vlákno pro proces konverze obrazu a nastavte časový limit, aby bylo možné předvídat přerušení.

### Krok 5: Přerušte proces

Volání `monitor.requestInterrupt()` signalizuje monitoru, aby přerušil probíhající konverzi.

```java
    // Interrupt the process
    monitor.interrupt();
    System.out.println("Interrupting the save thread #" + thread.getId() + " at " + getDateTime().toString());

    // Wait for interruption...
    thread.join();
} finally {
    // Delete the output file if it exists
    File f = new File(output);
    if (f.exists()) {
        f.delete();
    }
}
```

Přerušte proces konverze obrazu pomocí `InterruptMonitor` a počkejte, až se přerušení dokončí. Nakonec proveďte úklid odstraněním výstupního souboru.

## Proč použít Interrupt Monitor pro konverzi PSD‑to‑PNG?

Aspose.PSD podporuje **více než 30 výstupních formátů**, včetně PNG, JPEG, BMP a TIFF, a může zpracovávat soubory až do **500 MB** bez načítání celého dokumentu do paměti. Přidáním interrupt monitoru snížíte plýtvání CPU a zlepšíte odezvu v dávkových zpracovatelských pipelinech, zejména když konverze překročí očekávané časové limity.

## Časté problémy a řešení

- **Konverze se zablokuje na neurčito:** Ujistěte se, že je monitor připojen **před** voláním `save`.  
- **Výstupní soubor je po přerušení poškozený:** Monitor přeruší čistě; přesto vždy zkontrolujte, zda soubor existuje, než jej použijete.  
- **Obavy o thread‑safety:** Spusťte každou konverzi ve vlastním vlákně; monitor ovlivňuje pouze svého přidruženého pracovníka.

## Často kladené otázky

**Q1: Co je Interrupt Monitor v Aspose.PSD pro Java?**  
A: Interrupt Monitor umožňuje vývojářům pozastavit nebo zrušit dlouhodobé konverze obrázků, poskytuje kontrolu v reálném čase nad využitím zdrojů.

**Q2: Jak mohu získat knihovnu Aspose.PSD pro Java?**  
A: Knihovnu Aspose.PSD pro Java můžete stáhnout [zde](https://releases.aspose.com/psd/java/).

**Q3: Je k dispozici bezplatná zkušební verze Aspose.PSD pro Java?**  
A: Ano, můžete vyzkoušet bezplatnou zkušební verzi Aspose.PSD [zde](https://releases.aspose.com/).

**Q4: Kde mohu najít podporu pro Aspose.PSD pro Java?**  
A: Navštivte fórum podpory Aspose.PSD pro Java [zde](https://forum.aspose.com/c/psd/34).

**Q5: Jak mohu zakoupit licenci pro Aspose.PSD pro Java?**  
A: Licenci pro Aspose.PSD pro Java si můžete zakoupit [zde](https://purchase.aspose.com/buy).

**Q6: Mohu konvertovat více PSD souborů do PNG paralelně?**  
A: Ano, vytvořte samostatné vlákno pro každý soubor a připojte individuální `InterruptMonitor` ke každému pracovníkovi konverze.

**Q7: Zpracovává knihovna barevné profily během konverze PSD‑to‑PNG?**  
A: Rozhodně; Aspose.PSD zachovává vložené ICC profily a automaticky je aplikuje na výstupní PNG.

---

**Poslední aktualizace:** 2026-06-08  
**Testováno s:** Aspose.PSD 23.12 pro Java  
**Autor:** Aspose  

{{< blocks/products/products-backtop-button >}}

## Související tutoriály

- [Uložit PSD jako PNG a použít Rendering Drop Shadow v Aspose.PSD pro Java](/psd/java/advanced-image-manipulation/rendering-drop-shadow/)
- [Exportovat PSD do PNG a přidat novou běžnou vrstvu pomocí Aspose.PSD pro Java](/psd/java/advanced-image-effects/add-new-regular-layer/)
- [Podpora Interrupt Monitor v souborech PSD – Java](/psd/java/psd-layer-management-effects/support-interrupt-monitor-psd-files/)

{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}