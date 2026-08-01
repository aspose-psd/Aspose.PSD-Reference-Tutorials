---
date: 2026-08-01
description: Dowiedz się, jak dostosować gamma w przetwarzaniu obrazów w Javie przy
  użyciu Aspose.PSD, konwertować PSD na TIFF oraz naprawić wyblakłe obrazy w zwięzłym
  samouczku.
keywords:
- how to adjust gamma
- fix washed out image
- java image processing
- convert psd to tiff
- server side image processing
lastmod: 2026-08-01
linktitle: Dostosuj gamma obrazu
og_description: Dowiedz się, jak dostosować gamma w przetwarzaniu obrazów w Javie
  przy użyciu Aspose.PSD – szybkiej biblioteki po stronie serwera, która koryguje
  wyblakłe obrazy i konwertuje PSD na TIFF w zaledwie kilku linijkach kodu.
og_image_alt: 'Guide: Adjust gamma in Java images with Aspose.PSD, convert PSD to
  TIFF'
og_title: jak dostosować gamma – przetwarzanie w Javie z Aspose.PSD
schemas:
- author: Aspose
  dateModified: '2026-08-01'
  description: Learn how to adjust gamma in Java image processing with Aspose.PSD,
    convert PSD to TIFF, and fix washed‑out images in a concise tutorial.
  headline: How to Adjust Gamma in Java Image Processing with Aspose.PSD
  type: TechArticle
- description: Learn how to adjust gamma in Java image processing with Aspose.PSD,
    convert PSD to TIFF, and fix washed‑out images in a concise tutorial.
  name: How to Adjust Gamma in Java Image Processing with Aspose.PSD
  steps:
  - name: '**Java Development Environment** – Java 8 or later installed.'
    text: '**Java Development Environment** – Java 8 or later installed.'
  - name: '**Aspose.PSD Library** – Download and add the JAR to your project. See
      the official [documentation](https://reference.aspose.com/psd/java/).'
    text: '**Aspose.PSD Library** – Download and add the JAR to your project. See
      the official [documentation](https://reference.aspose.com/psd/java/).'
  - name: '**Sample Image** – A PSD file you want to process (e.g., `sample.psd`).'
    text: '**Sample Image** – A PSD file you want to process (e.g., `sample.psd`).'
  type: HowTo
- questions:
  - answer: Yes – the `adjustGamma` method accepts separate float values for red,
      green, and blue channels.
    question: Can I apply different gamma values to each colour channel?
  - answer: Absolutely. You can perform resizing, cropping, or colour corrections
      sequentially on the same `RasterImage` instance.
    question: Is it possible to chain multiple image adjustments before saving?
  - answer: Yes, each layer can be accessed and processed individually.
    question: Does Aspose.PSD support multi‑page PSD files?
  - answer: Aspose.PSD supports PNG, JPEG, BMP, and many other formats via their respective
      options classes.
    question: What format can I export to besides TIFF?
  - answer: Start with a moderate gamma (around 2.0) and preview the result; adjust
      downwards if the image looks too bright.
    question: How do I avoid a washed‑out image after gamma correction?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- adjust gamma
- Aspose.PSD
- Java image processing
- PSD to TIFF
- server side processing
title: Jak dostosować gamma w przetwarzaniu obrazów w Javie przy użyciu Aspose.PSD
url: /pl/java/advanced-techniques/adjust-gamma/
weight: 23
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Jak dostosować gamma w przetwarzaniu obrazów Java przy użyciu Aspose.PSD

## Wprowadzenie

## Szybkie odpowiedzi
- **Co robi korekcja gamma?** Przekształca wartości luminancji, aby ciemne obszary były jaśniejsze lub jasne obszary ciemniejsze, zachowując ogólną szczegółowość.  
- **Która biblioteka obsługuje przetwarzanie?** Aspose.PSD for Java udostępnia dedykowaną metodę `adjustGamma` dla obrazów rastrowych.  
- **Czy mogę przekonwertować PSD na TIFF w tym samym procesie?** Tak – po korekcji gamma możesz zapisać obraz bezpośrednio do TIFF używając `TiffOptions`.  
- **Czy potrzebna jest licencja do rozwoju?** Darmowa wersja próbna działa do testów; licencja komercyjna jest wymagana w środowisku produkcyjnym.  
- **Jaką wersję Java obsługuje?** Aspose.PSD obsługuje Java 8 i nowsze.

## Czym jest korekcja gamma w Javie?

Korekcja gamma zmienia nieliniowy związek pomiędzy zakodowanymi wartościami pikseli a wyświetlaną jasnością. Dostosowując krzywą gamma możesz **naprawić wypłowiałe obrazy** lub wzmocnić szczegóły w cieniach bez prześwietlania jasnych partii. Działa poprzez zastosowanie funkcji potęgowej do każdego piksela, co rozjaśnia ciemne tony i kompresuje jasne, dając bardziej naturalny wygląd wizualny.

## Dlaczego używać Aspose.PSD do korekcji gamma?

Aspose.PSD to **biblioteka do przetwarzania obrazów w Javie**, która ukrywa złożoność formatu PSD. Obsługuje przetwarzanie plików do 2 GB, radzi sobie z ponad 50 różnymi formatami obrazów i oferuje prostą metodę `adjustGamma`, co czyni ją idealną do **korekcji gamma w Javie** oraz **konwersji PSD na TIFF**.

## Wymagania wstępne

1. **Środowisko programistyczne Java** – zainstalowana Java 8 lub nowsza.  
2. **Biblioteka Aspose.PSD** – Pobierz i dodaj plik JAR do swojego projektu. Zobacz oficjalną [dokumentację](https://reference.aspose.com/psd/java/).  
3. **Przykładowy obraz** – Plik PSD, który chcesz przetworzyć (np. `sample.psd`).  

## Importowanie pakietów

Zanim rozpoczniesz, zaimportuj niezbędne przestrzenie nazw, które dają dostęp do obsługi rastrowej i opcji formatów plików.

## Krok 1: Załaduj obraz

Klasa `RasterImage` reprezentuje rasteryzowane dane pikseli warstwy PSD w pamięci. Załadowanie obrazu raz i buforowanie go zmniejsza zużycie pamięci przy kolejnych korektach.

## Krok 2: Dostosuj gamma

Załaduj swój PSD za pomocą `new RasterImage("sample.psd")` i wywołaj `rasterImage.adjustGamma(2.0f)` — ta pojedyncza linia stosuje gamma 2.0 we wszystkich kanałach kolorów, rozjaśniając cienie przy zachowaniu jasnych partii. Możesz podać osobne wartości dla czerwonego, zielonego i niebieskiego, jeśli potrzebne są korekty specyficzne dla kanałów.

## Krok 3: Utwórz TiffOptions

`TiffOptions` pozwala kontrolować kompresję, liczbę bitów na próbkę i inne ustawienia specyficzne dla TIFF. Ustawienie 8‑bitowej próbki (`{8,8,8}`) utrzymuje rozmiar pliku TIFF w rozsądnych granicach, zachowując jednocześnie wierność kolorów.

## Krok 4: Zapisz wynikowy obraz

Wywołaj `rasterImage.save("output.tif", tiffOptions)`, aby zapisać przetworzony obraz na dysku. Po zapisaniu możesz przekazać plik TIFF do systemów downstream, takich jak usługi drukowania czy API internetowe.

## Typowe przypadki użycia

- **Zautomatyzowane potoki graficzne** – Dostosuj gamma w locie przed generowaniem miniatur.  
- **Narzędzia do konwersji wsadowej** – Konwertuj duże archiwa PSD na TIFF, jednocześnie normalizując jasność.  
- **Usługi internetowe** – Udostępnij endpoint, który przyjmuje PSD, stosuje korekcję gamma i zwraca TIFF do konsumpcji przez klienta.

## Typowe problemy i rozwiązania

| Issue | Why it Happens | How to Fix |
|-------|----------------|------------|
| **Obraz wygląda wypłowiale** | Wartość gamma jest zbyt wysoka (np. > 2.5) | Obniż współczynnik gamma do wartości pomiędzy 1.8 a 2.2. |
| **`rasterImage.isCached()` zwraca false** | Obraz nie został jeszcze załadowany do pamięci | Wywołaj `rasterImage.cacheData()` przed dostosowaniem gamma. |
| **Rozmiar pliku TIFF jest duży** | Liczba bitów na próbkę ustawiona na 16‑bitową | Użyj 8‑bitowej próbki (`{8,8,8}`) jak pokazano w przykładzie. |

## Najczęściej zadawane pytania

**Q: Czy mogę zastosować różne wartości gamma dla każdego kanału kolorów?**  
A: Tak – metoda `adjustGamma` przyjmuje osobne wartości typu float dla kanałów czerwonego, zielonego i niebieskiego.

**Q: Czy można łączyć wiele korekt obrazu przed zapisem?**  
A: Oczywiście. Możesz kolejno wykonywać zmianę rozmiaru, przycinanie lub korekcje kolorów na tej samej instancji `RasterImage`.

**Q: Czy Aspose.PSD obsługuje wielostronicowe pliki PSD?**  
A: Tak, każda warstwa może być dostępna i przetwarzana indywidualnie.

**Q: Do jakich formatów mogę eksportować oprócz TIFF?**  
A: Aspose.PSD obsługuje PNG, JPEG, BMP i wiele innych formatów poprzez ich odpowiednie klasy opcji.

**Q: Jak uniknąć wypłowiałego obrazu po korekcji gamma?**  
A: Zacznij od umiarkowanej wartości gamma (około 2.0) i podglądaj wynik; obniżaj wartość, jeśli obraz wydaje się zbyt jasny.

## Zakończenie

Gratulacje! Pomyślnie nauczyłeś się **dostosowywać gamma** w **przepływie przetwarzania obrazów w Javie**, przekonwertowałeś PSD na TIFF i uniknąś typowych pułapek, takich jak **wypłowiały obraz**. Ten wzorzec daje precyzyjną kontrolę nad jasnością i kontrastem, co czyni go idealnym dla zautomatyzowanych potoków graficznych, usług internetowych lub aplikacji desktopowych.

---

**Ostatnia aktualizacja:** 2026-08-01  
**Testowano z:** Aspose.PSD 24.11 for Java  
**Autor:** Aspose  

{{< blocks/products/products-backtop-button >}}

## Powiązane tutoriale

- [Tutorial przetwarzania obrazów w Java – Dostosowanie jasności obrazu przy użyciu Aspose.PSD dla Java](/psd/java/advanced-techniques/adjust-brightness/)
- [Jak przekonwertować PSD na TIFF i dostosować kontrast przy użyciu Aspose.PSD dla Java](/psd/java/advanced-techniques/adjust-contrast/)
- [Konwertuj PSD na obraz w Java – Zastosuj warstwy korekcyjne przy użyciu Aspose.PSD](/psd/java/advanced-psd-layer-features-effects/apply-adjustment-layers-psd-files/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.psd.fileformats.tiff.enums.TiffPhotometrics;
import com.aspose.psd.imageoptions.TiffOptions;
```

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

// Load an existing image into an instance of RasterImage class
Image image = Image.load(sourceFile);

// Cast object of Image to RasterImage
RasterImage rasterImage = (RasterImage)image;

// Check if RasterImage is cached for better performance
if (!rasterImage.isCached()) {
    rasterImage.cacheData();
}
```

```java
// Adjust the gamma
rasterImage.adjustGamma(2.2f, 2.2f, 2.2f);
```

```java
// Create an instance of TiffOptions for the resultant image
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
int[] ushort = { 8, 8, 8 };
tiffOptions.setBitsPerSample(ushort);
tiffOptions.setPhotometric(TiffPhotometrics.Rgb);
```

```java
// Save the resultant image to TIFF format
String destName = dataDir + "AdjustGamma_out.tiff";
rasterImage.save(destName, tiffOptions);
```