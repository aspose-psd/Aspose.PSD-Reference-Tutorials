---
date: 2026-08-17
description: Dowiedz się, jak przycinać pliki PSD w języku Java przy użyciu Aspose.PSD
  for Java – szybki i precyzyjny sposób na przycinanie dokumentów Photoshop w aplikacjach
  Java.
keywords:
- crop psd file java
- aspose.psd java
- java image cropping
lastmod: 2026-08-17
linktitle: Przytnij plik PSD
og_description: Przytnij plik PSD w języku Java przy użyciu Aspose.PSD for Java. Ten
  przewodnik pokazuje krok po kroku, jak efektywnie przycinać pliki Photoshop, z wyjaśnieniami
  bez kodu i wskazówkami najlepszych praktyk.
og_image_alt: Guide showing how to crop a PSD file in Java using Aspose.PSD
og_title: Przytnij plik PSD w języku Java przy użyciu Aspose.PSD – szybkie przycinanie
  obrazów
schemas:
- author: Aspose
  dateModified: '2026-08-17'
  description: Learn how to crop psd file java with Aspose.PSD for Java – a fast,
    precise way to trim Photoshop documents in your Java applications.
  headline: Crop psd file java using Aspose.PSD
  type: TechArticle
- description: Learn how to crop psd file java with Aspose.PSD for Java – a fast,
    precise way to trim Photoshop documents in your Java applications.
  name: Crop psd file java using Aspose.PSD
  steps:
  - name: set document directory
    text: Replace “Your Document Directory” with the absolute or relative path that
      contains the PSD you want to process.
  - name: load PSD file
    text: The `RasterImage` class is Aspose.PSD’s entry point for raster‑based operations
      on a PSD file. Loading the file creates an in‑memory representation that you
      can manipulate.
  - name: define crop area
    text: '`Rectangle` defines the X and Y coordinates together with width and height
      of the region to keep. This class is part of the standard Java AWT package and
      is used by Aspose.PSD to specify cropping bounds.'
  - name: save cropped PSD
    text: After applying the crop, you can persist the result back to PSD format.
      The library writes only the cropped pixels, keeping the original color mode
      and bit depth.
  - name: save cropped image as PNG
    text: If you need a web‑friendly version, export the cropped raster to PNG. Aspose.PSD
      provides PNG save options that let you control compression level and interlacing.
  type: HowTo
- questions:
  - answer: Aspose.PSD for Java.
    question: What library handles PSD cropping in Java?
  - answer: Two API calls after loading the image.
    question: How many lines of code are required for a basic crop?
  - answer: Yes, using the built‑in PNG save options.
    question: Can I export the cropped area as PNG?
  - answer: A commercial license is needed beyond the trial period.
    question: Is a license required for production use?
  - answer: Java 8 and later, including Java 11, 17, and 21.
    question: What Java versions are supported?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- crop psd
- aspose.psd
- java image processing
title: Przytnij plik PSD w języku Java przy użyciu Aspose.PSD
url: /pl/java/image-processing/crop-psd-file/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Przycinanie pliku PSD w Javie przy użyciu Aspose.PSD

## Wprowadzenie

Jeśli potrzebujesz programowo przycinać dokumenty Photoshop, **crop psd file java** jest powszechnym zadaniem dla programistów Javy pracujących z pipeline'ami graficznymi, pipeline'ami zasobów lub zautomatyzowanymi przepływami projektowymi. Aspose.PSD for Java udostępnia dedykowane API, które pozwala zdefiniować prostokąt i wyodrębnić potrzebny obszar w kilku linijkach kodu. W tym samouczku dowiesz się, dlaczego biblioteka jest zbudowana pod kątem wysokowydajnego przycinania, jak skonfigurować środowisko oraz jakie są dokładne kroki, aby uzyskać zarówno wyniki w formacie PSD, jak i PNG.

## Szybkie odpowiedzi
- **Jaką bibliotekę obsługuje przycinanie PSD w Javie?** Aspose.PSD for Java.
- **Ile linii kodu jest potrzebnych do podstawowego przycięcia?** Two API calls after loading the image.
- **Czy mogę wyeksportować przycięty obszar jako PNG?** Yes, using the built‑in PNG save options.
- **Czy wymagana jest licencja do użytku produkcyjnego?** A commercial license is needed beyond the trial period.
- **Jakie wersje Javy są wspierane?** Java 8 and later, including Java 11, 17, and 21.

## Czym jest crop psd file java?

Crop psd file java odnosi się do procesu programowego wycinania prostokątnego regionu z dokumentu Photoshop (.psd) przy użyciu kodu Java. Dzięki Aspose.PSD możesz wykonać tę operację bez uruchamiania Photoshopa, co czyni ją idealną dla serwerowych pipeline'ów obrazów.

## Dlaczego warto używać Aspose.PSD dla Javy?

Aspose.PSD obsługuje **30+ formatów wejściowych i wyjściowych** i może przetwarzać pliki PSD do **500 MB** bez ładowania całego dokumentu do pamięci, dzięki architekturze strumieniowej. Biblioteka zachowuje warstwy, maski i profile kolorów, dostarczając przycięty wynik zgodny z natywnym wyjściem Photoshopa. Ta zmierzona wydajność pozwala obsługiwać zadania wsadowe na standardowym sprzęcie przy przewidywalnym zużyciu pamięci.

## Wymagania wstępne

- **Środowisko programistyczne Java** – JDK 8 or newer installed and configured.
- **Aspose.PSD for Java** – download the latest JAR and documentation [Aspose.PSD for Java documentation](https://reference.aspose.com/psd/java/).
- **Przykładowy plik PSD** – place a .psd file inside your project directory so the code can locate it.

## Jak przyciąć plik PSD w Javie?

Załaduj plik źródłowy, zdefiniuj prostokąt, który chcesz zachować, zastosuj przycięcie i na końcu zapisz wynik w żądanych formatach. Cały przepływ pracy wymaga tylko pięciu prostych kroków, z których każdy zilustrowany jest miejscem zastępczym, w którym wstawisz własny kod.

### Krok 1: ustaw katalog dokumentu

Zastąp „Your Document Directory” absolutną lub względną ścieżką, która zawiera PSD, które chcesz przetworzyć.

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;
import com.aspose.psd.Rectangle;

import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.imageoptions.PngOptions;
import com.aspose.psd.imageoptions.PsdOptions;
import com.aspose.psd.xmp.types.complex.colorant.ColorType;
```

### Krok 2: załaduj plik PSD

Klasa `RasterImage` jest punktem wejścia Aspose.PSD dla operacji rastrowych na pliku PSD. Załadowanie pliku tworzy reprezentację w pamięci, którą możesz modyfikować.

```java
String dataDir = "Your Document Directory";
```

### Krok 3: zdefiniuj obszar przycięcia

`Rectangle` definiuje współrzędne X i Y oraz szerokość i wysokość regionu do zachowania. Ta klasa jest częścią standardowego pakietu Java AWT i jest używana przez Aspose.PSD do określania granic przycięcia.

```java
String sourceFileName = dataDir + "1.psd";
RasterImage image = (RasterImage)Image.load(sourceFileName);
```

### Krok 4: zapisz przycięty PSD

Po zastosowaniu przycięcia możesz zapisać wynik ponownie w formacie PSD. Biblioteka zapisuje tylko przycięte piksele, zachowując oryginalny tryb kolorów i głębię bitową.

```java
image.crop(new Rectangle(10, 30, 100, 100));
```

### Krok 5: zapisz przycięty obraz jako PNG

Jeśli potrzebujesz wersji przyjaznej dla sieci, wyeksportuj przycięty raster do PNG. Aspose.PSD udostępnia opcje zapisu PNG, które pozwalają kontrolować poziom kompresji i przeplot.

```java
String exportPathPsd = dataDir + "CropTest.psd";
image.save(exportPathPsd, new PsdOptions());
```

## Typowe problemy i rozwiązania

- **Nieprawidłowe współrzędne prostokąta** – Ensure the X/Y values start at 0 for the top‑left corner; negative values will throw an `ArgumentException`.
- **Wzrost zużycia pamięci przy dużych plikach** – Use the `loadOptions.setLoadOnlyVisibleLayers(true)` option to reduce memory when you do not need hidden layers.
- **Utrata profilu kolorów** – Preserve the original ICC profile by calling `image.getColorProfile()` before cropping and re‑assigning it after the operation.

## Najczęściej zadawane pytania

### Q1: czy mogę używać Aspose.PSD for Java do przycinania obrazów w innych formatach?

A1: Aspose.PSD głównie obsługuje pliki PSD, ale wspiera także BMP, GIF, JPEG, PNG, TIFF i kilka innych formatów rastrowych zarówno jako wejście, jak i wyjście.

### Q2: czy Aspose.PSD for Java jest odpowiedni do przetwarzania obrazów na dużą skalę?

A2: Tak. Architektura strumieniowa biblioteki przetwarza wielostronicowe pliki PSD przy zużyciu pamięci poniżej 100 MB, co czyni ją idealną dla zadań wsadowych.

### Q3: czy istnieją kwestie licencyjne przy używaniu Aspose.PSD for Java?

A3: Wymagana jest licencja komercyjna do wdrożeń produkcyjnych. Szczegóły dostępne są na [stronie zakupu Aspose.PSD for Java](https://purchase.aspose.com/buy).

### Q4: jak mogę uzyskać wsparcie w kwestiach związanych z Aspose.PSD for Java?

A4: Odwiedź [forum Aspose.PSD for Java](https://forum.aspose.com/c/psd/34), aby zadawać pytania, udostępniać fragmenty kodu i otrzymywać pomoc od społeczności oraz inżynierów produktu.

### Q5: czy mogę wypróbować Aspose.PSD for Java przed zakupem?

A5: Tak, w pełni funkcjonalna wersja próbna może być pobrana [Aspose.PSD free trial download](https://releases.aspose.com/).

{{< blocks/products/products-backtop-button >}}

```java
String exportPathPng = dataDir + "CropTest.png";
PngOptions options = new PngOptions();
options.setColorType(PngColorType.TruecolorWithAlpha);
image.save(exportPathPng, options);
```

## Powiązane samouczki

- [Przycinanie obrazu prostokątem w Aspose.PSD for Java](/psd/java/image-editing/crop-image-by-rectangle/)
- [Przycinanie obrazu przesunięciami w Aspose.PSD for Java](/psd/java/image-editing/crop-image-by-shifts/)
- [Jak obrócić obraz w Javie przy użyciu Aspose.PSD](/psd/java/advanced-image-manipulation/rotate-image/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}