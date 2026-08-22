---
date: 2026-07-17
description: Samouczek przetwarzania obrazów w Javie z użyciem Aspose.PSD, ucz się,
  jak krok po kroku stosować filtry Gaussa i Wienera, aby uzyskać zachwycające wyniki
  wizualne.
keywords:
- java image processing tutorial
- export png java
- gaussian filter java
- wiener filter java
lastmod: 2026-07-17
linktitle: Zastosuj filtry Gaussa i Wienera
og_description: Samouczek przetwarzania obrazów w Javie pokazuje, jak stosować filtry
  Gaussa i Wienera przy użyciu Aspose.PSD dla Javy, w tym eksport do formatu PNG i
  innych formatów.
og_image_alt: 'Developer guide: Apply Gaussian and Wiener filters to images in Java
  using Aspose.PSD'
og_title: Samouczek przetwarzania obrazów w Javie – Zastosowanie filtrów Gaussa i
  Wienera
schemas:
- author: Aspose
  dateModified: '2026-07-17'
  description: Java image processing tutorial using Aspose.PSD learn how to apply
    Gaussian and Wiener filters step‑by‑step for stunning visual results.
  headline: Java Image Processing Tutorial – Apply Gaussian & Wiener Filters
  type: TechArticle
- questions:
  - answer: It smooths an image by averaging neighboring pixels, reducing high‑frequency
      noise.
    question: What does the Gaussian filter do?
  - answer: It performs adaptive smoothing, preserving edges while diminishing noise.
    question: What is the Wiener filter?
  - answer: Aspose.PSD for Java provides built‑in support for both filters.
    question: Which library is used?
  - answer: A trial works for testing, but a commercial license is required for production.
    question: Do I need a license?
  - answer: Yes—Aspose.PSD supports PNG, JPEG, BMP, and many more.
    question: Can I output formats other than GIF?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- java image processing
- Aspose.PSD
- gaussian filter
- wiener filter
- export png java
title: Samouczek przetwarzania obrazów w Javie – Zastosowanie filtrów Gaussa i Wienera
url: /pl/java/image-processing/apply-gaussian-wiener-filters/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Samouczek przetwarzania obrazów w Javie – Zastosowanie filtrów Gaussa i Wienera z Aspose.PSD

## Wprowadzenie

Witamy w naszym **samouczku przetwarzania obrazów w Javie**, który pokazuje, jak zastosować filtry Gaussa i Wienera przy użyciu Aspose.PSD dla Javy. Niezależnie od tego, czy oczyszczasz zaszumione zdjęcia, czy przygotowujesz grafikę do publikacji w sieci, te filtry zapewniają płynne, profesjonalnie wyglądające wyniki. W ciągu kilku minut zobaczysz pełny przepływ pracy — od wczytania pliku PSD po zapis przefiltrowanego wyniku jako GIF.

## Szybkie odpowiedzi
- **Co robi filtr Gaussa?** Wygładza obraz, uśredniając sąsiednie piksele, redukując szum o wysokiej częstotliwości.  
- **Czym jest filtr Wienera?** Wykonuje adaptacyjne wygładzanie, zachowując krawędzie przy jednoczesnym zmniejszaniu szumu.  
- **Jakiej biblioteki użyto?** Aspose.PSD dla Javy zapewnia wbudowane wsparcie dla obu filtrów.  
- **Czy potrzebna jest licencja?** Wersja próbna działa do testów, ale do produkcji wymagana jest licencja komercyjna.  
- **Czy mogę wyeksportować formaty inne niż GIF?** Tak — Aspose.PSD obsługuje PNG, JPEG, BMP i wiele innych.

## Czym jest samouczek przetwarzania obrazów w Javie?

Samouczek przetwarzania obrazów w Javie prowadzi programistów przez niezbędne kroki wczytywania obrazu, stosowania transformacji takich jak filtry czy zmiana rozmiaru oraz ostatecznego zapisu wyniku w wybranym formacie. Dzięki przejrzystym przykładom kodu i wyjaśnieniom pomaga zintegrować możliwości manipulacji obrazami bezpośrednio w aplikacjach Java, zmniejszając potrzebę korzystania z zewnętrznych narzędzi.

## Dlaczego używać filtrów Gaussa i Wienera?

Wczytaj obraz, zastosuj połączony filtr Gaussa‑Wienera i zobacz dramatyczne zmniejszenie ziarnistości przy jednoczesnym zachowaniu ostrości kluczowych krawędzi — idealne do przygotowywania grafik do sieci lub archiwalnych skanów. Część Gaussa usuwa szum o wysokiej częstotliwości, a część Wienera dostosowuje się do lokalnej wariancji, zachowując szczegóły tam, gdzie są najważniejsze.

## Wymagania wstępne

Przed rozpoczęciem upewnij się, że masz:

- Środowisko programistyczne Java (JDK 8 lub nowszy).  
- Bibliotekę Aspose.PSD dla Javy. Możesz ją pobrać **[tutaj](https://releases.aspose.com/psd/java/)**.  
- Podstawową znajomość składni Javy i koncepcji programowania obiektowego.

## Importowanie pakietów

Instrukcje importu wprowadzają klasy Aspose.PSD do zasięgu, abyś mógł pracować z obrazami rastrowymi, opcjami filtrów i formatami wyjściowymi.

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.imagefilters.filteroptions.GaussWienerFilterOptions;
import com.aspose.psd.imageoptions.GifOptions;
```

Te importy dają dostęp do wczytywania obrazów, manipulacji rastrem, opcji filtrów i formatów wyjściowych.

## Krok 1: Wczytaj obraz

Klasa `RasterImage` reprezentuje obraz rastrowy, który może być przetwarzany piksel po pikselu.

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

Image image = Image.load(sourceFile);
RasterImage rasterImage = (RasterImage)image;
```

Wczytujemy plik PSD z określonego katalogu i rzutujemy go na `RasterImage`, aby móc pracować z danymi pikseli.

## Krok 2: Sprawdź RasterImage

Sprawdzenie bezpieczeństwa potwierdza, że wczytany plik jest rastrowy; w przeciwnym razie procedura kończy się łagodnie.

```java
if (rasterImage == null) {
    return;
}
```

## Krok 3: Skonfiguruj opcje filtru

Klasa `GaussWienerFilterOptions` pozwala precyzyjnie dostroić zarówno parametry filtru Gaussa, jak i Wienera w jednym obiekcie.

```java
GaussWienerFilterOptions options = new GaussWienerFilterOptions(12, 3);
options.setGrayscale(true);
```

- Pierwszy argument (`12`) określa rozmiar promienia jądra Gaussa.  
- Drugi argument (`3`) ustawia wartość wygładzania używaną przez algorytm Wienera.  
- `setGrayscale(true)` nakazuje filtrowi pracować w trybie odcieni szarości, co często daje czystsze wyniki przy redukcji szumu.

## Krok 4: Zastosuj filtr i zapisz

Metoda `filter` stosuje skonfigurowaną kombinację filtrów Gaussa‑Wienera do całego obrazu. Na koniec zapisujemy przetworzony obraz jako GIF przy użyciu `GifOptions`. Możesz zamienić `GifOptions` na `PngOptions`, `JpegOptions` itp., aby **eksportować PNG w Javie** lub inne formaty.

```java
rasterImage.filter(image.getBounds(), options);
String destName = dataDir + "gauss_wiener_out.gif";
image.save(destName, new GifOptions());
```

## Typowe problemy i wskazówki

- **Null RasterImage:** Upewnij się, że plik źródłowy jest w formacie PSD lub innym kompatybilnym z rastrem.  
- **Wydajność:** Duże obrazy mogą wymagać więcej czasu; rozważ zmniejszenie promienia lub najpierw przetworzenie skalowanej kopii.  
- **Kolor vs. odcienie szarości:** Jeśli potrzebujesz zachować kolor, ustaw `options.setGrayscale(false)`.

## Najczęściej zadawane pytania

**Q1: Czy mogę zastosować te filtry do obrazów w formatach innych niż PSD?**  
A1: Tak, Aspose.PSD dla Javy obsługuje różne formaty obrazów poza PSD, takie jak PNG, JPEG, BMP i GIF.

**Q2: Czy istnieją ograniczenia w wersji próbnej Aspose.PSD dla Javy?**  
A2: Wersja próbna ogranicza rozmiar wyjścia i dodaje znak wodny. Aby odblokować pełne możliwości, uzyskaj ważną licencję.

**Q3: Jak mogę uzyskać wsparcie dla Aspose.PSD dla Javy?**  
A3: Odwiedź **[forum Aspose.PSD](https://forum.aspose.com/c/psd/34)**, aby uzyskać pomoc społeczności i oficjalne odpowiedzi.

**Q4: Czy dostępna jest tymczasowa licencja do celów testowych?**  
A4: Tak, możesz uzyskać tymczasową licencję **[tutaj](https://purchase.aspose.com/temporary-license/)**.

**Q5: Gdzie mogę znaleźć szczegółową dokumentację Aspose.PSD dla Javy?**  
A5: Zapoznaj się z **[dokumentacją](https://reference.aspose.com/psd/java/)**, aby uzyskać szczegółowe odniesienia API i dodatkowe przykłady.

## Podsumowanie

Ukończyłeś pełny **samouczek przetwarzania obrazów w Javie**, który pokazuje, jak **zastosować filtry Gaussa** i Wienera przy użyciu Aspose.PSD dla Javy. Eksperymentuj z różnymi wartościami promienia i wygładzania, przełączaj tryb odcieni szarości i wypróbuj inne formaty wyjściowe, takie jak PNG, aby zobaczyć, jak filtry wpływają na Twoje obrazy. Szczęśliwego kodowania!

---

**Last Updated:** 2026-07-17  
**Tested With:** Aspose.PSD for Java 23.12 (latest at time of writing)  
**Author:** Aspose

## Powiązane samouczki

- [Filtr krok po kroku – Zastosowanie filtrów ruchu Wienera przy użyciu Aspose.PSD dla Javy](/psd/java/image-processing/apply-motion-wiener-filters/)
- [Filtr krok po kroku – Zastosowanie filtrów medianowych i Wienera (Java)](/psd/java/image-processing/apply-median-wiener-filters/)
- [Jak filtrować pliki PNG w Aspose.PSD dla Javy](/psd/java/optimizing-png-files/apply-filters-png-files/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}