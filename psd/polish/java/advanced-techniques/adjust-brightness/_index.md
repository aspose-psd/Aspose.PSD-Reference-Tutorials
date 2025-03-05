---
title: Dostosuj jasność obrazu za pomocą Aspose.PSD dla Java
linktitle: Dostosuj jasność obrazu
second_title: Aspose.PSD API Java
description: Zwiększ jasność obrazu w Javie za pomocą Aspose.PSD. Przewodnik krok po kroku dotyczący programowej regulacji jasności obrazu.
type: docs
weight: 21
url: /pl/java/advanced-techniques/adjust-brightness/
---
## Wstęp

Ulepszanie obrazów jest powszechnym wymogiem w projektowaniu graficznym i fotografii cyfrowej. Aspose.PSD dla Java zapewnia potężne rozwiązanie do programowego dostosowywania jasności obrazu. W tym samouczku dowiemy się, jak krok po kroku wykorzystać bibliotekę Aspose.PSD for Java do dostosowania jasności obrazu.

## Warunki wstępne

Przed przystąpieniem do samouczka upewnij się, że spełniasz następujące wymagania wstępne:

-  Aspose.PSD dla biblioteki Java: Pobierz i zainstaluj bibliotekę z pliku[Aspose.PSD dla dokumentacji Java](https://reference.aspose.com/psd/java/).

## Importuj pakiety

Aby rozpocząć, zaimportuj niezbędne pakiety do swojego projektu Java. W tym przykładzie użyjemy następujących informacji:

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.psd.fileformats.tiff.enums.TiffPhotometrics;
import com.aspose.psd.imageoptions.TiffOptions;
```

Podzielmy teraz proces dostosowywania jasności obrazu na proste kroki:

## Krok 1: Załaduj obraz

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";
String destName = dataDir + "AdjustBrightness_out.tiff";

// Załaduj istniejący obraz do instancji klasy RasterImage
Image image = Image.load(sourceFile);
// Rzuć obiekt obrazu na RasterImage
RasterImage rasterImage = (RasterImage) image;

// Sprawdź, czy RasterImage jest buforowany i Cache RasterImage, aby uzyskać lepszą wydajność
if (!rasterImage.isCached()) {
    rasterImage.cacheData();
}
```

 Na tym etapie ładujemy obraz docelowy i przesyłamy go do pliku`RasterImage` do dalszego przetwarzania.

## Krok 2: Dostosuj jasność

```java
// Dostosuj jasność
rasterImage.adjustBrightness(-50);
```

 Tutaj używamy`adjustBrightness`metoda modyfikacji jasności obrazu. W tym przykładzie zmniejszamy jasność o 50 jednostek, ale możesz dostosować tę wartość do swoich wymagań.

## Krok 3: Ustaw opcje Tiff

```java
int[] ushort = {8, 8, 8};
// Utwórz instancję TiffOptions dla wynikowego obrazu
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
tiffOptions.setBitsPerSample(ushort);
tiffOptions.setPhotometric(TiffPhotometrics.Rgb);
```

 Skonfiguruj`TiffOptions` do zapisania dostosowanego obrazu. Dostosuj`bitsPerSample` I`photometric` właściwości w zależności od konkretnych potrzeb.

## Krok 4: Zapisz wynikowy obraz

```java
// Zapisz wynikowy obraz
rasterImage.save(destName, tiffOptions);
```

 Na koniec zapisz zmodyfikowany obraz, używając określonego`TiffOptions`.

## Wniosek

Programowe dostosowywanie jasności obrazu jest łatwe dzięki Aspose.PSD dla Java. Ten samouczek zawiera kompleksowy przewodnik dotyczący implementowania tej funkcji w aplikacjach Java.

## Często zadawane pytania

### P1: Czy mogę dostosować jasność w innych formatach obrazu oprócz PSD?

O1: Tak, Aspose.PSD dla Java obsługuje różne formaty obrazów, takie jak JPEG, PNG i TIFF.

### P2: Jak mogę poradzić sobie z błędami podczas procesu dostosowywania obrazu?

Odpowiedź 2: Możesz zaimplementować obsługę błędów za pomocą bloków try-catch, aby zarządzać wyjątkami, które mogą wystąpić.

### P3: Czy istnieje ograniczenie zakresu regulacji jasności?

O3: Zakres regulacji zależy od zawartości i formatu obrazu, ale Aspose.PSD zapewnia elastyczność dostosowywania.

### P4: Czy mogę używać Aspose.PSD dla Java w projektach komercyjnych?

 O4: Tak, Aspose.PSD for Java jest biblioteką komercyjną, z której można uzyskać licencję[Tutaj](https://purchase.aspose.com/buy).

### P5: Czy dostępna jest bezpłatna wersja próbna Aspose.PSD dla Java?

 Odpowiedź 5: Tak, możesz przeglądać bibliotekę w ramach bezpłatnego okresu próbnego[Tutaj](https://releases.aspose.com/).