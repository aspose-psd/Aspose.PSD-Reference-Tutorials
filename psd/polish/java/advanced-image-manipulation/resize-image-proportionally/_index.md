---
date: 2026-02-09
description: Dowiedz się, jak konwertować pliki PSD na PNG i proporcjonalnie zmieniać
  rozmiar obrazów w Javie przy użyciu Aspose.PSD. Ten krok po kroku poradnik obejmuje
  buforowanie obrazów, zmianę rozmiaru i zapisywanie jako PNG.
linktitle: Convert PSD to PNG & Resize Proportionally
second_title: Aspose.PSD Java API
title: Jak przekonwertować PSD na PNG i zmienić rozmiar proporcjonalnie przy użyciu
  Aspose.PSD dla Javy
url: /pl/java/advanced-image-manipulation/resize-image-proportionally/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Jak konwertować PSD na PNG i zmieniać rozmiar graficzny przy użyciu Aspose.PSD dla Javy

## Wstęp

Jeśli **konwertować PSD na PNG**, uzyskano dodatkowe połączenie, trafiłeś we właściwe miejsce. W tym **Aspose.PSD Java** tutorialu przeprowadziliśmy Cię przez dowolny **java image Processing tutorial**, który zawiera **jak wybrać rozmiar** proporcjonalnie, buforować obraz dla dowolnej wydajności i w końcu zapisać wynik jako PNG. Po wyłączeniu można wyłączyć dziesięć przepływ pracy z rurociągiem, z których pochodzą systemy oparte na Javie.

## Szybkie odpowiedzi
- **Czy Aspose.PSD może konwertować PSD na PNG?** Tak – po prostu załaduj plik PSD i zapisz go przy użyciu `PngOptions`.
- **Czy biblioteka obsługująca pochodne zmienianie funkcji?** Absolutnie; parametry `resizeWidthProportionally` i `resizeHeightProportionally`.
- **Czy najpierw trzeba buforować obraz?** Buforowanie (`image.cacheData()`) zwiększa wydajność przy dużych plikach PSD.
- **Jaka wersja Javy jest wymagana?** Java8 lub teraz jest w pełni wspierana.
- **Czy wymagana jest licencja do produkcji?** Tak, licencja komercyjna oznacza znak wodny wersji ewaluacyjnej.

## Co to jest „konwertuj plik PSD na PNG” i dlaczego ma to znaczenie?

Konwersja dokumentu Photoshop (PSD) na plik Portable Network Graphics (PNG) pozwala na udostępnianie warstwowych projektów w lekkim, przyjaznym dla sieci. PNG został stworzony przezroczystość i jakość bezstratną, co czyni go idealnym dla zasobów UI, miniaturowych lub uniwersalnych scenariuszy, w których ważna jest wierność obrazu.

## Po co proporcjonalnie zmieniać rozmiar obrazu w Javie?

Zmiana dotyczy **jak zmienić rozmiar obrazu** bez zniekształcania jego integralności zapewnia, że ​​grafika wygląda naturalnie na różnych ekranach. API `Aspose.PSD` udostępnia dedykowane metody do **zmiany rozmiaru obrazu proporcjonalnie**, które automatycznie obliczają pasującą wysokość lub szerokość, oszczędzając Ci wady matematyczne.

## Dlaczego ma to znaczenie dla programistów

- **Zmniejszony rozmiar pliku PSD** – Skalowanie dużych plików PSD przed konwersją, obniżenie pamięci i przyspieszenie transmisji.
- **Spójne renderowanie interfejsu użytkownika** – Proporcjonalne zmienianie zapewnia, że ​​ikony i grafiki udostępniają różne funkcje.
- **Brak zależności od Photoshopa** – Można wykonać te operacje na rozwiązania lub w potoku, czyli CI bez instalacji Photoshopa.

## Warunki wstępne

Zanim przejdziemy do kodu, zastosuj się, że masz:

1. **Java Development Kit (JDK)** – Zainstalowana Javę8 lub nowszą.
2. **Aspose.PSD dla Java** – pobierz ostatni JAR z dodatkowej strony[tutaj](https://releases.aspose.com/psd/java/).
3. Przykładowy plik PSD (`sample.psd`) dotyczy katalogu, do którego można zastosować się w swoim programie.

## Importuj pakiety

Dodaj niezbędny import do swojej klasy Java. Te klasy zapewniają dostęp do zasilania obrazu, buforowania, zmiany zasilania i wyjścia wyjściowego PNG.

```java
import com.aspose.psd.Image;
import com.aspose.psd.imageoptions.PngOptions;
```

## Krok 1: Załaduj obraz PSD

Najpierw załaduj źródłowy plik PSD. Jeśli plik jest duży, buforowanie danych obrazu zmniejsza zużycie pamięci podczas wykonywania kolejnych operacji.

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

Image image = Image.load(sourceFile);

if (!image.isCached()) {
    // Image caching java – improves performance for large files
    image.cacheData();
}
```

## Krok 2: Proporcjonalna zmiana rozmiaru obrazu (Java)

Teraz określ nowe wymiary. W tym przykładzie zmniejszamy obraz do **połowy** rozmiaru oryginalnego, zachowując proporcje. Możesz dostosować docelową szerokość lub wysokość w razie potrzeby.

```java
int newWidth = image.getWidth() / 2;
image.resizeWidthProportionally(newWidth);

int newHeight = image.getHeight() / 2;
image.resizeHeightProportionally(newHeight);
```

> **Wskazówka:** Użyj `resizeWidthProportionally` *lub* `resizeHeightProportionally` — biblioteka automatycznie oblicza drugi wymiar, aby zachować proporcje obrazu.

## Krok 3: Zapisz zmieniony rozmiar obrazu jako PNG

Na koniec wyeksportuj zmieniony rozmiar obrazu do formatu PNG. Ten krok kończy proces **konwersji PSD do PNG**.

```java
String destName = dataDir + "SimpleResizeImageProportionally_out.png";
image.save(destName, new PngOptions());
```

Gdy kod zostanie uruchomiony, plik PNG, który jest opuszczony przez PSD, zostanie powiązany z siecią wizualną i bez zniekształceń.

## Typowe problemy i rozwiązania

| Problem | Przyczyna | Rozwiązanie |
|-------|-------|-----|
| **Błąd OutOfMemory** | Duży PSD niebuforowany | Wywołaj `image.cacheData()` przed uderzeniem |
| **Puste wyjście PNG** | Nieprawidłowa ścieżka pliku | Sprawdź `dataDir` i licencję zapisu |
| **Proporcje wyglądają nieprawidłowo** | Ręczne udostępnienie, jak i wysokość | wykorzystanie metody grafalnej udostępnionej przez Aspose.PSD |

## Wskazówki dotyczące zmniejszania rozmiaru pliku PSD

- **Przystępne działanie** przed wystąpieniem pliku.
- **Zmieniaj rozmiar generalnie** jak opisano powyżej, aby wcześniej zastosować wymiary.
- **Zapisz jako PNG z głębią bitową**, aby udostępnić dane.

## Często zadawane pytania

**P:** Czy Aspose.PSD jest rozwiązaniem ze stosowaniem formatami obrazów?
**O:** Aspose.PSD obsługuje PSD, PNG, JPEG, BMP, GIF i wiele innych. Pełną listę wyników w [dokumentacji](https://reference.aspose.com/psd/java/).

**P:** Czy można zastosować Aspose.PSD w projektach komercyjnych?
**O:** Tak. Kup transport komercyjny w [sklepie Aspose](https://purchase.aspose.com/buy).

**P:** Czy dostępne są tymczasowe licencje do testowania?
**O:** Oczywiście – zamów tymczasową [tutaj](https://purchase.aspose.com/temporary-license/) do celów ewaluacyjnych.

**P:** Gdzie mogę znaleźć wsparcie społeczności?
**O:** Forum [Aspose.PSD](https://forum.aspose.com/c/psd/34) do świetnego miejsca, aby zadawać pytania i dzielić się rozwiązaniami.

**P:** Jak uzyskać dostęp do pełnej referencji API?
**O:** Szczegółowa dokumentacja API jest dostępna [tutaj](https://reference.aspose.com/psd/java/).

## Wniosek

Teraz wiesz, jak **konwertować PSD na PNG**, **zmienić rozmiar obrazu graficznego** i zachować buforowanie przy użyciu Aspose.PSD dla Javy. Włącz te kroki do aplikacji, aby uruchomić szybkie, wysokiej jakości oprogramowanie komputerowe bez konieczności użycia z natywną instalacją Photoshopa. To **aspose psd java** jest niezawodną częścią każdego **java image Processing tutorial** i zawiera różne rozmiary plików PSD pod kontrolą, która jest jednocześnie wierna wizualna.

---

**Aktualizacja Ostatnia:** 2026-02-09
**Testowano z:** Aspose.PSD 24.12 dla Java
**Autor:** Asponuj

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
