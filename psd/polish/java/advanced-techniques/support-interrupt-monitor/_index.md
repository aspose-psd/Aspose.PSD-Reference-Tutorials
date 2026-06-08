---
date: 2026-06-08
description: Dowiedz się, jak zapisać PSD jako PNG przy użyciu Aspose.PSD for Java
  i w razie potrzeby przerwać konwersję. Efektywnie zarządzaj przepływem pracy z obrazami.
keywords:
- save psd as png
- how to interrupt conversion
- psd to png conversion
- manage image workflow
linktitle: Obsługa Interrupt Monitor
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
title: Jak zapisać PSD jako PNG przy użyciu Interrupt Monitor w Aspose.PSD for Java
url: /pl/java/advanced-techniques/support-interrupt-monitor/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Zapisz PSD jako PNG z Interrupt Monitor w Aspose.PSD dla Javy

## Wprowadzenie

Jeśli potrzebujesz **zapisz PSD jako PNG** zachowując pełną kontrolę nad długotrwałymi konwersjami, Interrupt Monitor w Aspose.PSD dla Javy zapewnia dokładnie to. W tym samouczku przeprowadzimy Cię przez konfigurację monitora, konwersję pliku PSD do PNG oraz bezpieczne przerwanie operacji w razie potrzeby. Zobaczysz także, jak to wpisuje się w typowy przepływ przetwarzania obrazu i dlaczego jest niezbędne w solidnych aplikacjach.

## Szybkie odpowiedzi
- **Czy mogę przerwać konwersję PSD‑do‑PNG?** Tak, użyj `InterruptMonitor`, aby zatrzymać proces na żądanie.  
- **Która metoda zapisuje PSD jako PNG?** Wywołaj `save(outputPath, new PngOptions())`.  
- **Czy potrzebuję licencji do produkcji?** Wymagana jest licencja komercyjna; dostępna jest wersja próbna.  
- **Jaką wersję Java obsługuje się?** Java 8 i nowsze są w pełni obsługiwane.  
- **Czy biblioteka jest bezpieczna wątkowo?** Konwersje mogą działać w oddzielnych wątkach; monitor obsługuje przerwania w sposób bezpieczny.

## Wymagania wstępne

Zanim zagłębisz się w szczegóły użycia Interrupt Monitor, upewnij się, że masz następujące wymagania:

- **Środowisko programistyczne Java:** Skonfiguruj środowisko programistyczne Java na swoim systemie.  
- **Biblioteka Aspose.PSD:** Uzyskaj bibliotekę Aspose.PSD dla Java. Możesz ją pobrać [tutaj](https://releases.aspose.com/psd/java/). Możesz także odwiedzić główną stronę Aspose [tutaj](https://releases.aspose.com/).  
- **Katalog dokumentów:** Miej wyznaczony katalog dla swoich dokumentów PSD.

## Importowanie pakietów

Zacznij od zaimportowania niezbędnych pakietów do swojego projektu Java. Zapewni to dostęp do funkcjonalności Aspose.PSD.

```java
import com.aspose.psd.ImageOptionsBase;

import static com.aspose.psd.examples.Utils.Utils.getDateTime;
import com.aspose.psd.imageoptions.PngOptions;
import com.aspose.psd.multithreading.InterruptMonitor;
import com.aspose.psd.system.Threading.ThreadStart;
import java.io.File;
```

Teraz rozbijmy przykładowy kod na przewodnik krok po kroku, aby włączyć Interrupt Monitor w swoim projekcie Aspose.PSD dla Java.

## Jak zapisać PSD jako PNG przy użyciu Interrupt Monitor?

`PsdImage` reprezentuje dokument PSD załadowany do pamięci.  
`SaveImageWorker` wykonuje konwersję obrazu w osobnym wątku.  

Załaduj swój plik PSD za pomocą `new PsdImage("source.psd")`, podłącz `InterruptMonitor` do `SaveImageWorker` i wywołaj `save("output.png", new PngOptions())`. Monitor obserwuje żądanie anulowania i czysto przerywa konwersję, zwracając kontrolę do aplikacji w ciągu kilku milisekund.

### Krok 1: Ustaw swój katalog dokumentów

```java
String dataDir = "Your Document Directory";
```

Upewnij się, że zamienisz „Your Document Directory” na rzeczywistą ścieżkę, w której przechowywane są Twoje dokumenty PSD.

### Krok 2: Zdefiniuj opcje obrazu i ścieżkę wyjściową

```java
ImageOptionsBase saveOptions = new PngOptions();
String source = dataDir + "big2.psb";
String output = dataDir + "big_out.png";
```

Określ opcje obrazu, źródłowy plik PSD oraz żądaną ścieżkę wyjściową dla skonwertowanego obrazu.

### Krok 3: Zainicjuj Interrupt Monitor i SaveImageWorker

Klasa `InterruptMonitor` obserwuje trwającą konwersję i może ją przerwać, gdy wywołane zostanie `requestInterrupt()`.  

```java
InterruptMonitor monitor = new InterruptMonitor();
SaveImageWorker worker = new SaveImageWorker(source, output, saveOptions, monitor);
```

Utwórz instancje `InterruptMonitor` i `SaveImageWorker`, łącząc monitor z pracownikiem konwersji obrazu.

### Krok 4: Uruchom wątek konwersji obrazu

```java
Thread thread = new Thread(worker.ThreadProc());
try {
    thread.start();
    // Add a timeout to allow for potential interruption
    Thread.sleep(3000);
```

Zainicjuj nowy wątek dla procesu konwersji obrazu i wprowadź okres limitu czasu, aby przewidzieć przerwanie.

### Krok 5: Przerwij proces

Wywołanie `monitor.requestInterrupt()` sygnalizuje monitorowi, aby przerwał trwającą konwersję.  

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

Przerwij proces konwersji obrazu przy użyciu `InterruptMonitor` i poczekaj na zakończenie przerwania. Na koniec posprzątaj, usuwając plik wyjściowy.

## Dlaczego używać Interrupt Monitor przy konwersji PSD‑do‑PNG?

Aspose.PSD obsługuje **ponad 30 formatów wyjściowych**, w tym PNG, JPEG, BMP i TIFF, i może przetwarzać pliki do **500 MB** bez ładowania całego dokumentu do pamięci. Dodając monitor przerwań, zmniejszasz marnotrawstwo CPU i zwiększasz responsywność w potokach przetwarzania wsadowego, szczególnie gdy konwersja przekracza oczekiwane limity czasu.

## Częste problemy i rozwiązania

- **Konwersja zawiesza się bez końca:** Upewnij się, że monitor jest podłączony **przed** wywołaniem `save`.  
- **Plik wyjściowy jest uszkodzony po przerwaniu:** Monitor przerywa czysto; jednak zawsze sprawdzaj, czy plik istnieje przed jego użyciem.  
- **Obawy dotyczące bezpieczeństwa wątkowego:** Uruchamiaj każdą konwersję w osobnym wątku; monitor wpływa tylko na powiązanego pracownika.

## Najczęściej zadawane pytania

**Q1: Czym jest Interrupt Monitor w Aspose.PSD dla Java?**  
A: Interrupt Monitor pozwala programistom wstrzymywać lub anulować długotrwałe konwersje obrazów, zapewniając kontrolę w czasie rzeczywistym nad zużyciem zasobów.

**Q2: Jak mogę uzyskać bibliotekę Aspose.PSD dla Java?**  
A: Możesz pobrać bibliotekę Aspose.PSD dla Java [tutaj](https://releases.aspose.com/psd/java/).

**Q3: Czy dostępna jest darmowa wersja próbna Aspose.PSD dla Java?**  
A: Tak, możesz wypróbować darmową wersję próbną Aspose.PSD [tutaj](https://releases.aspose.com/).

**Q4: Gdzie mogę znaleźć wsparcie dla Aspose.PSD dla Java?**  
A: Odwiedź forum wsparcia Aspose.PSD dla Java [tutaj](https://forum.aspose.com/c/psd/34).

**Q5: Jak mogę kupić licencję na Aspose.PSD dla Java?**  
A: Możesz kupić licencję na Aspose.PSD dla Java [tutaj](https://purchase.aspose.com/buy).

**Q6: Czy mogę konwertować wiele plików PSD do PNG równolegle?**  
A: Tak, uruchom osobny wątek dla każdego pliku i podłącz indywidualny `InterruptMonitor` do każdego pracownika konwersji.

**Q7: Czy biblioteka obsługuje profile kolorów podczas konwersji PSD‑do‑PNG?**  
A: Zdecydowanie; Aspose.PSD zachowuje osadzone profile ICC i automatycznie stosuje je do wyjściowego pliku PNG.

---

**Ostatnia aktualizacja:** 2026-06-08  
**Testowano z:** Aspose.PSD 23.12 for Java  
**Autor:** Aspose  

{{< blocks/products/products-backtop-button >}}

## Powiązane samouczki

- [Zapisz PSD jako PNG i zastosuj cień renderowania w Aspose.PSD dla Javy](/psd/java/advanced-image-manipulation/rendering-drop-shadow/)
- [Eksportuj PSD do PNG i dodaj nową zwykłą warstwę przy użyciu Aspose.PSD dla Javy](/psd/java/advanced-image-effects/add-new-regular-layer/)
- [Obsługa Interrupt Monitor w plikach PSD – Java](/psd/java/psd-layer-management-effects/support-interrupt-monitor-psd-files/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}