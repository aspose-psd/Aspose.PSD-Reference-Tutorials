---
title: Zastosuj filtry medianowe i wienerowskie za pomocą Aspose.PSD dla Java
linktitle: Zastosuj filtry mediany i Wienera
second_title: Aspose.PSD API Java
description: Poznaj moc przetwarzania obrazów w Javie za pomocą Aspose.PSD. Dowiedz się, jak krok po kroku zastosować filtry medianowe i wienerowskie. Popraw jakość obrazu bez wysiłku.
weight: 12
url: /pl/java/image-processing/apply-median-wiener-filters/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Zastosuj filtry medianowe i wienerowskie za pomocą Aspose.PSD dla Java

## Wstęp

W dziedzinie programowania w języku Java Aspose.PSD wyróżnia się jako potężne narzędzie do manipulacji i przetwarzania obrazów. Jedną z kluczowych funkcjonalności, jakie oferuje, jest zastosowanie filtrów medianowych i wienerowskich, które odgrywają kluczową rolę w poprawie jakości obrazu i redukcji szumów. Ten przewodnik krok po kroku przeprowadzi Cię przez proces stosowania tych filtrów przy użyciu Aspose.PSD dla Java.

## Warunki wstępne

Zanim przejdziesz do samouczka, upewnij się, że spełniasz następujące wymagania wstępne:

1.  Aspose.PSD dla biblioteki Java: Pobierz i zainstaluj bibliotekę z[Tutaj](https://releases.aspose.com/psd/java/).
2. Środowisko programistyczne Java: Upewnij się, że w systemie skonfigurowano środowisko programistyczne Java.

## Importuj pakiety

Rozpocznij od zaimportowania niezbędnych pakietów, aby wykorzystać funkcjonalność Aspose.PSD w projekcie Java:

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.imagefilters.filteroptions.MedianFilterOptions;
import com.aspose.psd.imageoptions.GifOptions;
```

## Stosowanie filtra medianowego

### Krok 1: Załaduj obraz

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

//Załaduj obraz źródłowy
Image image = Image.load(sourceFile);
```

### Krok 2: Rzuć obraz na RasterImage

```java
// Rzuć obraz do RasterImage
RasterImage rasterImage = (RasterImage)image;
if (rasterImage == null) {
    return;
}
```

### Krok 3: Utwórz instancję MedianFilterOptions

```java
// Utwórz instancję klasy MedianFilterOptions i ustaw rozmiar filtra
MedianFilterOptions options = new MedianFilterOptions(4);
```

### Krok 4: Zastosuj filtr mediany

```java
// Zastosuj filtr MedianFilterOptions do obiektu RasterImage
rasterImage.filter(image.getBounds(), options);
```

### Krok 5: Zapisz wynikowy obraz

```java
String destName = dataDir + "median_test_denoise_out.gif";
// Zapisz wynikowy obraz jako GIF
image.save(destName, new GifOptions());
```

Wykonując poniższe kroki, pomyślnie zastosowałeś filtr medianowy do swojego obrazu przy użyciu Aspose.PSD dla Java.

## Wniosek

W tym samouczku zbadaliśmy proces stosowania filtrów medianowych i wienerowskich przy użyciu Aspose.PSD dla Java. Filtry te są niezbędne do poprawy jakości obrazu i redukcji szumów w aplikacjach Java. Wykorzystując moc Aspose.PSD, możesz bez wysiłku włączyć te filtry do procesów przetwarzania obrazu.

## Często zadawane pytania

### P1: Czy mogę zastosować te filtry do obrazów w dowolnym formacie?

Odpowiedź 1: Tak, Aspose.PSD obsługuje szeroką gamę formatów obrazów, dzięki czemu jest wszechstronny w różnych projektach.

### P2: Czy dostępna jest bezpłatna wersja próbna Aspose.PSD dla Java?

 A2: Tak, możesz uzyskać bezpłatną wersję próbną[Tutaj](https://releases.aspose.com/).

### P3: Jak uzyskać wsparcie dla Aspose.PSD dla Java?

 A3: Odwiedź[Forum Aspose.PSD](https://forum.aspose.com/c/psd/34) za wsparcie społeczności.

### P4: Gdzie mogę znaleźć dokumentację Aspose.PSD dla Java?

 Odpowiedź 4: Zapoznaj się z dokumentacją[Tutaj](https://reference.aspose.com/psd/java/).

### P5: Jak mogę kupić Aspose.PSD dla Java?

 A5: Możesz kupić produkt[Tutaj](https://purchase.aspose.com/buy).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
