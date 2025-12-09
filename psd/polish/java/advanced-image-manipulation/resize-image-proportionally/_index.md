---
date: 2025-12-08
description: Dowiedz się, jak konwertować pliki PSD na PNG i proporcjonalnie zmieniać
  rozmiar obrazów w Javie przy użyciu Aspose.PSD. Ten krok po kroku poradnik obejmuje
  buforowanie obrazów, zmianę rozmiaru oraz zapisywanie jako PNG.
linktitle: Convert PSD to PNG & Resize Proportionally
second_title: Aspose.PSD Java API
title: Jak konwertować PSD na PNG i zmieniać rozmiar proporcjonalnie przy użyciu Aspose.PSD
  dla Javy
url: /pl/java/advanced-image-manipulation/resize-image-proportionally/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Jak przekonwertować PSD na PNG i zmienić rozmiar proporcjonalnie przy użyciu Aspose.PSD dla Javy

## Wprowadzenie

Jeśli potrzebujesz **przekonwertować PSD na PNG** zachowując oryginalne proporcje, trafiłeś we właściwe miejsce. W tym samouczku przeprowadzimy Cię przez kompletny **samouczek Aspose.PSD**, który pokaże, jak **zmienić rozmiar obrazu** proporcjonalnie w Javie, buforować obraz dla optymalnej wydajności i ostatecznie zapisać wynik jako PNG. Po zakończeniu będziesz mógł zintegrować ten przepływ pracy z dowolnym pipeline’em przetwarzania obrazów opartym na Javie.

## Szybkie odpowiedzi
- **Czy Aspose.PSD może konwertować PSD na PNG?** Tak – wystarczy załadować plik PSD i zapisać go przy użyciu `PngOptions`.
- **Czy biblioteka obsługuje proporcjonalne skalowanie?** Absolutnie; użyj `resizeWidthProportionally` i `resizeHeightProportionally`.
- **Czy najpierw muszę buforować obraz?** Buforowanie (`image.cacheData()`) poprawia wydajność przy dużych plikach PSD.
- **Jaka wersja Javy jest wymagana?** Java 8 lub nowsza jest w pełni wspierana.
- **Czy wymagana jest licencja do produkcji?** Tak, licencja komercyjna usuwa znaki wodne wersji ewaluacyjnej.

## Czym jest „konwersja PSD na PNG” i dlaczego ma to znaczenie?

Konwersja dokumentu Photoshop (PSD) na plik portable network graphics (PNG) pozwala udostępniać warstwowe projekty w lekkim, przyjaznym dla sieci formacie. PNG zachowuje przezroczystość i jakość bezstratną, co czyni go idealnym dla zasobów UI, miniatur lub wszelkich scenariuszy, w których liczy się wierność obrazu.

## Dlaczego zmieniać rozmiar obrazu proporcjonalnie w Javie?

Zmiana rozmiaru **jak zmienić rozmiar obrazu** bez zniekształcania proporcji zapewnia naturalny wygląd grafiki na różnych ekranach. API `Aspose.PSD` oferuje dedykowane metody skalowania proporcjonalnego, które automatycznie obliczają pasującą wysokość lub szerokość, oszczędzając Ci ręcznych obliczeń i błędów.

## Wymagania wstępne

Zanim przejdziesz do kodu, upewnij się, że masz:

1. **Java Development Kit (JDK)** – zainstalowaną Javę 8 lub nowszą.
2. **Aspose.PSD for Java** – pobierz najnowszy JAR z oficjalnej strony [here](https://releases.aspose.com/psd/java/).
3. Przykładowy plik PSD (`sample.psd`) umieszczony w katalogu, do którego możesz odwołać się z projektu.

## Importowanie pakietów

Dodaj niezbędne importy do swojej klasy Java. Te klasy dają dostęp do ładowania obrazu, buforowania, zmiany rozmiaru i opcji wyjścia PNG.

```java
import com.aspose.psd.Image;
import com.aspose.psd.imageoptions.PngOptions;
```

## Krok 1: Załaduj obraz PSD

Najpierw załaduj źródłowy plik PSD. Jeśli plik jest duży, buforowanie danych obrazu zmniejsza zużycie pamięci przy kolejnych operacjach.

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

Image image = Image.load(sourceFile);

if (!image.isCached()) {
    // Image caching java – improves performance for large files
    image.cacheData();
}
```

## Krok 2: Zmiana rozmiaru obrazu proporcjonalnie (Java)

Teraz określ nowe wymiary. W tym przykładzie zmniejszamy obraz do **połowy** jego pierwotnego rozmiaru, zachowując proporcje. W razie potrzeby możesz dostosować docelową szerokość lub wysokość.

```java
int newWidth = image.getWidth() / 2;
image.resizeWidthProportionally(newWidth);

int newHeight = image.getHeight() / 2;
image.resizeHeightProportionally(newHeight);
```

> **Pro tip:** Użyj albo `resizeWidthProportionally` *lub* `resizeHeightProportionally` — biblioteka automatycznie oblicza drugą wymiar, aby obraz pozostał proporcjonalny.

## Krok 3: Zapisz zmieniony rozmiar obrazu jako PNG

Na koniec wyeksportuj zmieniony rozmiar obrazu do formatu PNG. Ten krok kończy **konwersję PSD na PNG**.

```java
String destName = dataDir + "SimpleResizeImageProportionally_out.png";
image.save(destName, new PngOptions());
```

Po uruchomieniu kodu znajdziesz plik PNG, który jest o połowę mniejszy od oryginalnego PSD, zachowując tę samą jakość wizualną i bez zniekształceń.

## Typowe problemy i rozwiązania

| Problem | Przyczyna | Rozwiązanie |
|-------|-------|-----|
| **OutOfMemoryError** | Duży PSD nie został buforowany | Wywołaj `image.cacheData()` przed zmianą rozmiaru |
| **Pusty wynik PNG** | Nieprawidłowa ścieżka pliku | Sprawdź `dataDir` i uprawnienia zapisu |
| **Proporcje wyglądają niepoprawnie** | Ręczne ustawienie zarówno szerokości, jak i wysokości | Użyj metod proporcjonalnych dostarczonych przez Aspose.PSD |

## Najczęściej zadawane pytania

**Q: Czy Aspose.PSD jest kompatybilny ze wszystkimi formatami obrazu?**  
A: Aspose.PSD obsługuje PSD, PNG, JPEG, BMP, GIF i wiele innych. Pełną listę znajdziesz w [dokumentacji](https://reference.aspose.com/psd/java/).

**Q: Czy mogę używać Aspose.PSD w projektach komercyjnych?**  
A: Tak. Kup licencję komercyjną w [sklepie Aspose](https://purchase.aspose.com/buy).

**Q: Czy dostępne są licencje tymczasowe do testów?**  
A: Oczywiście – poproś o tymczasową licencję [tutaj](https://purchase.aspose.com/temporary-license/) do celów ewaluacyjnych.

**Q: Gdzie mogę znaleźć wsparcie społeczności?**  
A: Forum [Aspose.PSD](https://forum.aspose.com/c/psd/34) to świetne miejsce na zadawanie pytań i dzielenie się rozwiązaniami.

**Q: Jak uzyskać pełną referencję API?**  
A: Szczegółowa dokumentacja API jest dostępna [tutaj](https://reference.aspose.com/psd/java/).

## Podsumowanie

Teraz wiesz, jak **przekonwertować PSD na PNG**, zmienić rozmiar obrazu proporcjonalnie i efektywnie obsłużyć buforowanie przy użyciu Aspose.PSD dla Javy. Włącz te kroki do własnych aplikacji, aby zapewnić szybkie, wysokiej jakości przetwarzanie obrazów bez konieczności instalacji natywnego Photoshopa.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Last Updated:** 2025-12-08  
**Tested With:** Aspose.PSD 24.12 for Java  
**Author:** Aspose