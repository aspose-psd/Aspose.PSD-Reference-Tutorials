---
title: Zastosuj kompresję Adobe Deflate do TIFF - Java
linktitle: Zastosuj kompresję Adobe Deflate do TIFF - Java
second_title: Aspose.PSD API Java
description: Dowiedz się, jak zastosować kompresję Adobe Deflate do obrazów TIFF przy użyciu Aspose.PSD dla Java. Przewodnik krok po kroku dotyczący wydajnego przetwarzania obrazu.
weight: 12
url: /pl/java/tiff-image-compression-configuration/apply-adobe-deflate-compression-tiff/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Zastosuj kompresję Adobe Deflate do TIFF - Java

## Wstęp

Czy zastanawiałeś się kiedyś, jak efektywnie kompresować obrazy TIFF bez utraty jakości? Jeśli masz do czynienia z dużymi plikami obrazów, prawdopodobnie znasz problemy związane z długim czasem ładowania i problemami z pamięcią. W tym miejscu wchodzi w grę kompresja Adobe Deflate, a dzięki Aspose.PSD dla Java możesz łatwo wdrożyć ją w swoich projektach. Ten samouczek przeprowadzi Cię krok po kroku przez proces stosowania kompresji Adobe Deflate do obrazu TIFF. Gotowy do nurkowania? Zacznijmy!

## Warunki wstępne

Zanim przejdziemy do właściwego kodu, upewnijmy się, że wszystko mamy skonfigurowane. Oto, czego potrzebujesz:

1. Zestaw Java Development Kit (JDK): Upewnij się, że na komputerze jest zainstalowana najnowsza wersja pakietu JDK.
2.  Aspose.PSD dla Java: Pobierz i zintegruj bibliotekę Aspose.PSD dla Java ze swoim projektem. Możesz to dostać od[Tutaj](https://releases.aspose.com/psd/java/).
3. Środowisko programistyczne: IDE, takie jak IntelliJ IDEA, Eclipse lub NetBeans.
4.  Licencja tymczasowa (opcjonalna): Jeśli nie jesteś jeszcze gotowy na zakup, możesz uzyskać licencję[licencja tymczasowa](https://purchase.aspose.com/temporary-license/) aby wypróbować funkcje.

## Importuj pakiety

Zacznijmy od zaimportowania niezbędnych pakietów do Twojego projektu Java. Importy te są kluczowe, ponieważ umożliwiają pracę z biblioteką Aspose.PSD i narzędziami Java.

```java
import com.aspose.psd.Color;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.tiff.TiffRational;
import com.aspose.psd.fileformats.tiff.enums.TiffCompressions;
import com.aspose.psd.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.psd.fileformats.tiff.enums.TiffPhotometrics;
import com.aspose.psd.fileformats.tiff.enums.TiffPlanarConfigs;
import com.aspose.psd.fileformats.tiff.enums.TiffResolutionUnits;
import com.aspose.psd.imageoptions.TiffOptions;
```

Teraz, gdy omówiliśmy podstawy, podzielmy proces na łatwe do wykonania kroki.

## Krok 1: Skonfiguruj opcje TIFF

 Najpierw musisz utworzyć instancję`TiffOptions` i skonfiguruj go według swoich potrzeb. Opcje te określają sposób przetwarzania pliku TIFF, w tym jego rozdzielczość, schemat kolorów i kompresję.

```java
TiffOptions options = new TiffOptions(TiffExpectedFormat.Default);
```

Tutaj tworzymy`TiffOptions` obiekt w formacie domyślnym. Ale to dopiero początek! 

## Krok 2: Skonfiguruj właściwości obrazu

 Następnie musisz ustawić różne właściwości obrazu TIFF, np`BitsPerSample`, `Photometric`, `Resolution` , I`PlanarConfiguration`. Te ustawienia określają sposób przechowywania i wyświetlania danych obrazu.

```java
int[] ushort = { 8, 8, 8 };
options.setBitsPerSample(ushort);
options.setPhotometric(TiffPhotometrics.Rgb);
options.setXresolution(new TiffRational(72));
options.setYresolution(new TiffRational(72));
options.setResolutionUnit(TiffResolutionUnits.Inch);
options.setPlanarConfiguration(TiffPlanarConfigs.Contiguous);
```

Oto, co robi każda właściwość:
- BitsPerSample: Ustawia liczbę bitów na próbkę dla każdego kanału koloru.
- Fotometryczny: Określa model kolorów (w tym przypadku RGB).
- Rozdzielczość: Określa rozdzielczość poziomą i pionową obrazu.
- PlanarConfiguration: określa sposób przechowywania danych pikseli.

## Krok 3: Zastosuj kompresję Adobe Deflate

Teraz nadchodzi magia! Do obrazu TIFF zastosujesz kompresję Adobe Deflate, która pomoże zmniejszyć rozmiar pliku bez utraty jakości obrazu.

```java
options.setCompression(TiffCompressions.AdobeDeflate);
```

Adobe Deflate to bezstratna metoda kompresji, która doskonale sprawdza się w przypadku obrazów, w przypadku których konieczne jest zachowanie wysokiej jakości przy jednoczesnym zmniejszeniu rozmiaru pliku.

## Krok 4: Utwórz i edytuj obraz TIFF

Po ustawieniu opcji nadszedł czas na utworzenie nowego obrazu TIFF i manipulowanie nim. W tym kroku utworzymy prosty obraz o wymiarach 100 x 100 i wypełnimy go czerwonymi pikselami.

```java
PsdImage tiffImage = new PsdImage(100, 100);

for (int j = 0; j < tiffImage.getHeight(); j++) {
    for (int i = 0; i < tiffImage.getWidth(); i++) {
        tiffImage.setPixel(i, j, Color.getRed());
    }
}
```

Tutaj przeglądamy każdy piksel obrazu i ustawiamy jego kolor na czerwony. Oczywiście możesz dostosować tę część, aby tworzyć bardziej złożone obrazy.

## Krok 5: Zapisz skompresowany obraz TIFF

Wreszcie, po skonfigurowaniu i utworzeniu obrazu, ostatnim krokiem jest zapisanie go z zastosowaną kompresją. Upewnij się, że podałeś poprawną ścieżkę katalogu.

```java
String dataDir = "Your Document Directory";
tiffImage.save(dataDir + "TIFFwithAdobeDeflateCompression_output.tif");
```

To wszystko! Pomyślnie zastosowałeś kompresję Adobe Deflate do obrazu TIFF przy użyciu Aspose.PSD dla Java.

## Wniosek

I masz to! Stosowanie kompresji Adobe Deflate do obrazów TIFF jest prostym procesem w Aspose.PSD dla Java. Niezależnie od tego, czy masz do czynienia z dużymi obrazami do swojej witryny internetowej, mediów cyfrowych czy innego projektu, ta metoda gwarantuje, że pliki pozostaną wysokiej jakości, a ich rozmiar będzie łatwiejszy do zarządzania. Siła Aspose.PSD dla Java leży w jego prostocie i wydajności, co czyni go narzędziem obowiązkowym dla programistów pracujących ze złożonymi formatami obrazów.

## Często zadawane pytania

### Co to jest kompresja Adobe Deflate?
Adobe Deflate to bezstratna metoda kompresji używana do zmniejszania rozmiaru obrazów TIFF bez utraty jakości.

### Czy mogę używać innych metod kompresji z Aspose.PSD dla Java?
Tak, Aspose.PSD obsługuje różne metody kompresji, takie jak LZW, CCITT i JPEG.

### Czy biblioteka Aspose.PSD jest bezpłatna?
 Aspose.PSD oferuje bezpłatną wersję próbną, ale do pełnej funkcjonalności wymagana jest licencja. Możesz dostać[licencja tymczasowa](https://purchase.aspose.com/temporary-license/) żeby to wypróbować.

### Jak ustawienie rozdzielczości wpływa na obraz TIFF?
Rozdzielczość określa klarowność obrazu podczas drukowania lub wyświetlania. Wyższe rozdzielczości zapewniają lepszą jakość, ale powodują większe rozmiary plików.

### Czy mogę manipulować innymi formatami obrazów za pomocą Aspose.PSD dla Java?
Absolutnie! Aspose.PSD obsługuje różne formaty, takie jak PSD, PNG, JPEG i inne.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
