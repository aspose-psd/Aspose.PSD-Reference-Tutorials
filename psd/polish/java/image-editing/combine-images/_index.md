---
date: 2025-12-30
description: Dowiedz się, jak w Javie utworzyć plik PSD, łącząc dwa obrazy przy użyciu
  Aspose.PSD. Skorzystaj z naszego przewodnika krok po kroku, aby szybko połączyć
  obrazy w plik PSD.
linktitle: Combine Images
second_title: Aspose.PSD Java API
title: Jak utworzyć plik PSD w Javie – Łączenie obrazów przy użyciu Aspose.PSD
url: /pl/java/image-editing/combine-images/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Utwórz plik PSD w Javie – Łączenie obrazów przy użyciu Aspose.PSD

## Wprowadzenie

Jeśli potrzebujesz **utworzyć plik PSD w Javie** poprzez scalanie kilku obrazów, Aspose.PSD ułatwia to zadanie. W tym samouczku przeprowadzimy Cię przez łączenie dwóch obrazów w jedną płótno PSD, wyjaśnimy, dlaczego to podejście jest przydatne, i dostarczymy gotowy do uruchomienia kod. Po zakończeniu będziesz w stanie **połączyć dwa obrazy w stylu Java** i wygenerować profesjonalnie wyglądający plik warstwowy.

## Szybkie odpowiedzi
- **Jaka biblioteka jest najlepsza do łączenia obrazów w PSD?** Aspose.PSD for Java.
- **Jak długo trwa implementacja?** Około 10‑15 minut dla podstawowego łączenia.
- **Czy potrzebna jest licencja?** Darmowa wersja próbna działa do testów; licencja komercyjna jest wymagana w produkcji.
- **Czy mogę dodać więcej niż dwa obrazy?** Tak – powtórz wywołania `drawImage` dla każdej dodatkowej warstwy.
- **Która wersja Javy jest wspierana?** Java 8 i nowsze.

## Wymagania wstępne

Zanim zaczniemy, upewnij się, że masz następujące elementy:

1. **Biblioteka Aspose.PSD** – pobierz ją z [tutaj](https://releases.aspose.com/psd/java/).  
2. **Java Development Kit (JDK)** – zalecana jest Java 8+.  
3. **Katalog dokumentów** – folder na Twoim komputerze, w którym będą przechowywane obrazy źródłowe oraz wynikowy plik PSD.

## Importowanie pakietów

Rozpocznij od zaimportowania wymaganych klas Aspose.PSD do swojego projektu:

```java
import com.aspose.psd.Color;
import com.aspose.psd.Graphics;
import com.aspose.psd.Image;

import com.aspose.psd.imageoptions.PsdOptions;
import com.aspose.psd.sources.FileCreateSource;
```

## Przewodnik krok po kroku

### Krok 1: Utwórz opcje PSD (przygotowanie pliku)

Najpierw tworzymy instancję `PsdOptions`, która będzie przechowywać ustawienia wyjściowe.

```java
PsdOptions imageOptions = new PsdOptions();
```

### Krok 2: Ustaw FileCreateSource (określenie miejsca zapisu PSD)

Przypisz `FileCreateSource` do opcji, wskazując pożądany plik wynikowy.

```java
imageOptions.setSource(new FileCreateSource(dataDir + "Two_images_result_out.psd", false));
```

### Krok 3: Utwórz instancję Image (inicjalizacja rozmiaru płótna)

Utwórz obiekt `Image` z podanymi opcjami i określ płótno o wymiarach 600 × 600 pikseli.

```java
Image image = Image.create(imageOptions, 600, 600);
```

### Krok 4: Zainicjalizuj Graphics i narysuj pierwszy obraz

Obiekt `Graphics` pozwala nam malować na płótnie. Czyścimy tło na biało i rysujemy pierwszy obraz źródłowy po lewej stronie.

```java
Graphics graphics = new Graphics(image);
graphics.clear(Color.getWhite());
graphics.drawImage(Image.load(dataDir + "example1.psd"), 0, 0, 300, 600);
```

### Krok 5: Narysuj drugi obraz (ukończenie łączenia)

Teraz umieszczamy drugi obraz po prawej stronie tego samego płótna.

```java
graphics.drawImage(Image.load(dataDir + "example2.psd"), 300, 0, 300, 600);
```

### Krok 6: Zapisz wynikowy plik PSD

Na koniec zapisujemy połączone płótno na dysku.

```java
image.save();
```

Gratulacje! Pomyślnie **połączyłeś obrazy w PSD** i utworzyłeś plik PSD w Javie.

## Dlaczego łączyć obrazy przy użyciu Aspose.PSD?

- **Świadomość warstw** – każde wywołanie `drawImage` dodaje osobną warstwę, którą możesz edytować później.  
- **Elastyczność formatów** – obsługuje PSD, PNG, JPEG, BMP i inne.  
- **Brak natywnych zależności** – czysta Java, działa na każdym systemie operacyjnym, na którym działa JDK.  

## Typowe problemy i rozwiązania

| Problem | Przyczyna | Rozwiązanie |
|-------|-------|-----|
| `File not found` błąd podczas ładowania obrazów źródłowych | Nieprawidłowa ścieżka `dataDir` | Sprawdź, czy `dataDir` wskazuje na folder zawierający `example1.psd` i `example2.psd`. |
| Wynikowy PSD jest pusty | `graphics.clear` wywołane po rysowaniu | Upewnij się, że `graphics.clear(Color.getWhite())` jest wykonywane **przed** wywołaniami `drawImage`. |
| Wyjątek licencyjny w czasie wykonywania | Brak lub wygasła licencja Aspose.PSD | Zastosuj ważną licencję używając `License license = new License(); license.setLicense("Aspose.PSD.lic");` przed jakimkolwiek wywołaniem API. |

## Najczęściej zadawane pytania

### P1: Czy Aspose.PSD jest kompatybilny ze wszystkimi formatami obrazów?
O1: Aspose.PSD koncentruje się głównie na formacie plików PSD. Jednak obsługuje różne inne formaty zarówno przy wejściu, jak i wyjściu.

### P2: Czy mogę wykonać dodatkowe modyfikacje połączonego obrazu?
O2: Oczywiście! Po połączeniu obrazów możesz dalej manipulować wynikowym PSD, korzystając z rozbudowanych funkcji Aspose.PSD.

### P3: Czy istnieją wymagania licencyjne dotyczące używania Aspose.PSD?
O3: Tak, wymagana jest ważna licencja do użytku komercyjnego. Uzyskaj ją z [tutaj](https://purchase.aspose.com/buy).

### P4: Czy dostępna jest darmowa wersja próbna Aspose.PSD?
O4: Tak, możesz wypróbować Aspose.PSD w darmowej wersji próbnej [tutaj](https://releases.aspose.com/).

### P5: Gdzie mogę znaleźć wsparcie w kwestiach związanych z Aspose.PSD?
O5: Odwiedź [forum Aspose.PSD](https://forum.aspose.com/c/psd/34), aby uzyskać wsparcie społeczności i dyskusje.

---

**Ostatnia aktualizacja:** 2025-12-30  
**Testowano z:** Aspose.PSD 24.11 for Java  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}