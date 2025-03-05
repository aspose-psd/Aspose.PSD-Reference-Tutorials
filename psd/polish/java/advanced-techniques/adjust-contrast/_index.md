---
title: Dostosuj kontrast obrazu za pomocą Aspose.PSD dla Java
linktitle: Dostosuj kontrast obrazu
second_title: Aspose.PSD API Java
description: Poznaj świat regulacji kontrastu obrazu w Javie za pomocą Aspose.PSD. Postępuj zgodnie z naszym przewodnikiem krok po kroku, aby uzyskać płynną manipulację obrazem.
type: docs
weight: 22
url: /pl/java/advanced-techniques/adjust-contrast/
---
## Wstęp

dziedzinie przetwarzania obrazów w Javie Aspose.PSD wyróżnia się jako potężne narzędzie. Wśród niezliczonych funkcji częstym wymaganiem jest regulacja kontrastu obrazu. Ten samouczek przeprowadzi Cię przez proces dostosowywania kontrastu obrazu przy użyciu Aspose.PSD dla Java. Niezależnie od tego, czy jesteś doświadczonym programistą, czy dopiero zaczynasz, ten przewodnik pomoże Ci opanować ten istotny aspekt manipulacji obrazami.

## Warunki wstępne

Zanim przejdziesz do samouczka, upewnij się, że spełniasz następujące wymagania wstępne:

- Podstawowa znajomość programowania w języku Java.
-  Zainstalowana biblioteka Aspose.PSD dla Java. Możesz go pobrać[Tutaj](https://releases.aspose.com/psd/java/).

## Importuj pakiety

Aby rozpocząć, musisz zaimportować niezbędne pakiety do swojego projektu Java. Dodaj następujące linie do swojego kodu:

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.psd.fileformats.tiff.enums.TiffPhotometrics;
import com.aspose.psd.imageoptions.TiffOptions;
```

## Krok 1: Załaduj obraz

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

// Załaduj istniejący obraz do instancji klasy RasterImage
Image image = Image.load(sourceFile);
```

 Na tym etapie ładujemy przykładowy obraz („sample.psd”) za pomocą pliku`Image.load` metoda.

## Krok 2: Rzutuj na obraz rastrowy i dane z pamięci podręcznej

```java
// Rzuć obiekt obrazu na RasterImage
RasterImage rasterImage = (RasterImage)image;

// Sprawdź, czy RasterImage jest buforowany i Cache RasterImage, aby uzyskać lepszą wydajność
if (!rasterImage.isCached()) {
    rasterImage.cacheData();
}
```

 Tutaj rzucamy rodzajnik`Image` sprzeciwić się A`RasterImage` do konkretnego przetwarzania. Buforowanie danych obrazu poprawia wydajność.

## Krok 3: Dostosuj kontrast

```java
// Dostosuj kontrast
rasterImage.adjustContrast(50);
```

 The`adjustContrast`Metoda służy do modyfikowania kontrastu obrazu. W tym przykładzie kontrast został zwiększony o 50%.

## Krok 4: Utwórz TiffOptions i zapisz

```java
// Utwórz instancję TiffOptions dla wynikowego obrazu
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
int[] ushort = { 8, 8, 8 };
tiffOptions.setBitsPerSample(ushort);
tiffOptions.setPhotometric(TiffPhotometrics.Rgb);

// Zapisz wynikowy obraz w formacie TIFF
String destName = dataDir + "AdjustContrast_out.tiff";
rasterImage.save(destName, tiffOptions);
```

 Tutaj ustawiliśmy się`TiffOptions` dla obrazu wyjściowego, określając format i inne właściwości. Ostateczny obraz jest następnie zapisywany w pliku TIFF.

## Wniosek

Gratulacje! Pomyślnie dostosowałeś kontrast obrazu za pomocą Aspose.PSD dla Java. W tym samouczku omówiono podstawowe kroki, od importowania pakietów po zapisanie przetworzonego obrazu.

## Często zadawane pytania

### P1: Czy Aspose.PSD jest kompatybilny z różnymi formatami obrazów?

Odpowiedź 1: Tak, Aspose.PSD obsługuje różne formaty obrazów, zapewniając elastyczność w Twoich projektach.

### P2: Jak mogę uzyskać tymczasową licencję na Aspose.PSD?

 Odpowiedź 2: Możesz uzyskać licencję tymczasową[Tutaj](https://purchase.aspose.com/temporary-license/).

### P3: Gdzie mogę znaleźć dokumentację Aspose.PSD?

A3: Dokumentacja jest dostępna[Tutaj](https://reference.aspose.com/psd/java/).

### P4: Jakie opcje wsparcia są dostępne dla Aspose.PSD?

 A4: Aby uzyskać pomoc, odwiedź stronę[Forum Aspose.PSD](https://forum.aspose.com/c/psd/34).

### P5: Czy mogę kupić Aspose.PSD?

 A5: Tak, możesz kupić Aspose.PSD[Tutaj](https://purchase.aspose.com/buy).