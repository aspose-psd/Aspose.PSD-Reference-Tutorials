---
date: 2025-12-25
description: Dowiedz się, jak konwertować pliki PSD na PNG przy użyciu Aspose.PSD
  dla Javy z obsługą monitora przerwań, w tym przykład przerwania wątku w Javie oraz
  wskazówki dotyczące zapisywania PSD jako PNG.
linktitle: Support for Interrupt Monitor
second_title: Aspose.PSD Java API
title: Jak przekonwertować PSD na PNG z obsługą monitora przerwań w Aspose.PSD dla
  Javy
url: /pl/java/advanced-techniques/support-interrupt-monitor/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Konwersja PSD do PNG z użyciem Interrupt Monitor w Aspose.PSD dla Javy

## Wprowadzenie

Jeśli potrzebujesz **konwertować PSD do PNG**, zachowując pełną kontrolę nad długotrwałymi konwersjami obrazów, Interrupt Monitor w Aspose.PSD dla Javy jest narzędziem, którego szukasz. W tym samouczku przeprowadzimy Cię przez rzeczywisty **przykład przerwania wątku w Javie**, który pozwala zatrzymać konwersję w trakcie procesu, dając elastyczność w zarządzaniu zasobami, wymuszaniu limitów czasu lub reagowaniu na anulowanie przez użytkownika.

## Szybkie odpowiedzi
- **Co robi Interrupt Monitor?** Umożliwia bezpieczne sygnalizowanie trwającej konwersji obrazu, aby została zatrzymana.  
- **Czy mogę konwertować PSD do PNG przy jego użyciu?** Tak – monitor działa z każdą operacją zapisu, w tym z PNG.  
- **Czy wymagany jest osobny wątek?** Zazwyczaj konwersję uruchamia się w osobnym wątku, aby móc ją przerwać.  
- **Jakiej wersji Aspose.PSD potrzebuję?** Dowolnej nowszej wersji, która zawiera `com.aspose.psd.multithreading.InterruptMonitor`.  
- **Czy potrzebna jest licencja do produkcji?** Tak, do użytku nie‑testowego wymagana jest ważna licencja Aspose.PSD.

## Co to jest „konwersja PSD do PNG” z Interrupt Monitor?

Konwersja dużego dokumentu Photoshop (PSD/PSB) do obrazu PNG może być intensywna pod względem CPU. Dołączając **Interrupt Monitor** do procesu konwersji, zyskujesz możliwość programowego zatrzymania tego procesu – idealne dla usług sieciowych, zadań wsadowych lub aplikacji UI, w których użytkownicy mogą anulować operacje.

## Dlaczego warto używać Interrupt Monitor?

- **Responsywny interfejs:** Zapobiega zamrożeniu aplikacji podczas przetwarzania dużego pliku.  
- **Zarządzanie zasobami:** Zatrzymuje konwersje, które przekraczają limity czasu lub pamięci.  
- **Obsługa błędów:** Elegancko usuwa częściowo wygenerowane pliki wyjściowe po przerwaniu.

## Wymagania wstępne

- Środowisko programistyczne Java (JDK 8 lub nowszy).  
- Biblioteka Aspose.PSD dla Javy – pobierz ją **[tutaj](https://releases.aspose.com/psd/java/)**.  
- Folder zawierający pliki PSD/PSB, z którymi chcesz pracować.

## Importowanie pakietów

Zacznij od zaimportowania niezbędnych klas. Dzięki temu uzyskasz dostęp do opcji obrazu, interrupt monitor oraz narzędzi wątkowych.

```java
import com.aspose.psd.ImageOptionsBase;

import static com.aspose.psd.examples.Utils.Utils.getDateTime;
import com.aspose.psd.imageoptions.PngOptions;
import com.aspose.psd.multithreading.InterruptMonitor;
import com.aspose.psd.system.Threading.ThreadStart;
import java.io.File;
```

## Przewodnik krok po kroku

### Krok 1: Ustaw katalog dokumentów

```java
String dataDir = "Your Document Directory";
```

Zastąp `"Your Document Directory"` absolutną ścieżką, w której znajdują się Twoje pliki PSD.

### Krok 2: Zdefiniuj opcje obrazu i ścieżkę wyjściową

```java
ImageOptionsBase saveOptions = new PngOptions();
String source = dataDir + "big2.psb";
String output = dataDir + "big_out.png";
```

Tutaj **zapisujemy PSD jako PNG** przy użyciu `PngOptions`. Dostosuj nazwy plików w razie potrzeby.

### Krok 3: Zainicjuj Interrupt Monitor i SaveImageWorker

```java
InterruptMonitor monitor = new InterruptMonitor();
SaveImageWorker worker = new SaveImageWorker(source, output, saveOptions, monitor);
```

Instancja `InterruptMonitor` będzie użyta później do zatrzymania konwersji. `SaveImageWorker` łączy monitor z zadaniem konwersji.

### Krok 4: Rozpocznij konwersję obrazu w osobnym wątku

```java
Thread thread = new Thread(worker.ThreadProc());
try {
    thread.start();
    // Add a timeout to allow for potential interruption
    Thread.sleep(3000);
```

Uruchamiamy konwersję w tle, aby główny wątek pozostał responsywny. Wywołanie `Thread.sleep(3000)` symuluje scenariusz limitu czasu.

### Krok 5: Przerwij proces (przykład przerwania wątku w Javie)

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

Wywołanie `monitor.interrupt()` uruchamia logikę **jak przerwać monitor**. Po przerwaniu usuwamy ewentualny częściowo zapisany plik PNG.

## Typowe problemy i rozwiązania

| Problem | Przyczyna | Rozwiązanie |
|---------|-----------|-------------|
| Konwersja nie zatrzymuje się | Monitor nie jest połączony z workerem | Upewnij się, że `SaveImageWorker` otrzymuje tę samą instancję `InterruptMonitor`. |
| Plik wyjściowy pozostaje po przerwaniu | Kod czyszczący nie został wykonany | Sprawdź, czy blok `finally` jest uruchamiany i czy ścieżka pliku jest prawidłowa. |
| `OutOfMemoryError` przy dużych plikach PSB | Nie użyto opcji strumieniowego ładowania | Użyj `PsdImage` z `LoadOptions`, które umożliwiają efektywne pamięciowo ładowanie. |

## Najczęściej zadawane pytania

### P1: czym jest Interrupt Monitor w Aspose.PSD dla Javy?

Odp1: Interrupt Monitor pozwala programistom **zarządzać i przerywać procesy konwersji obrazów**, dając precyzyjną kontrolę nad długotrwałymi zadaniami.

### P2: jak mogę zdobyć bibliotekę Aspose.PSD dla Javy?

Odp2: Bibliotekę Aspose.PSD dla Javy możesz pobrać **[tutaj](https://releases.aspose.com/psd/java/)**.

### P3: czy dostępna jest darmowa wersja próbna Aspose.PSD dla Javy?

Odp3: Tak, darmową wersję próbną Aspose.PSD znajdziesz **[tutaj](https://releases.aspose.com/)**.

### P4: gdzie mogę uzyskać wsparcie dla Aspose.PSD dla Javy?

Odp4: Odwiedź forum wsparcia Aspose.PSD dla Javy **[tutaj](https://forum.aspose.com/c/psd/34)**.

### P5: jak mogę kupić licencję na Aspose.PSD dla Javy?

Odp5: Licencję na Aspose.PSD dla Javy możesz nabyć **[tutaj](https://purchase.aspose.com/buy)**.

---

**Ostatnia aktualizacja:** 2025-12-25  
**Testowano z:** Aspose.PSD 24.11 dla Javy  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}