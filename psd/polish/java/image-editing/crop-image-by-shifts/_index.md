---
date: 2026-07-03
description: Dowiedz się, jak przycinać obraz w Javie przy użyciu Aspose.PSD dla Javy.
  Ten krok po kroku poradnik przycinania obrazów obejmuje ładowanie plików PSD, ustawianie
  shift values oraz zapisywanie wyniku.
keywords:
- crop image java
- how to crop image
- load psd file
- java image processing
- crop image left right
linktitle: Przycinanie obrazu według przesunięć
schemas:
- author: Aspose
  dateModified: '2026-07-03'
  description: Learn how to crop image java using Aspose.PSD for Java. This step‑by‑step
    image cropping tutorial covers loading PSD files, setting shift values, and saving
    the result.
  headline: Crop Image Java by Shifts with Aspose.PSD
  type: TechArticle
- description: Learn how to crop image java using Aspose.PSD for Java. This step‑by‑step
    image cropping tutorial covers loading PSD files, setting shift values, and saving
    the result.
  name: Crop Image Java by Shifts with Aspose.PSD
  steps:
  - name: Load the Image
    text: '`Image` is the base class for all image types in Aspose.PSD. `RasterImage`
      represents a raster image and provides cropping capabilities.'
  - name: Cache Image Data
    text: '`cacheData()` loads the image data into memory for faster processing.'
  - name: Define Shift Values
    text: Specify the shift values for all four sides of the image (left, top, right,
      bottom) in pixels.
  - name: Apply Cropping
    text: '`crop(left, right, top, bottom)` trims the image by the specified pixel
      shifts on each side.'
  - name: Save the Results
    text: '`JpegOptions` defines JPEG encoding settings such as quality and color
      profile. Congratulations! You''ve successfully cropped an image using Aspose.PSD
      for Java.'
  type: HowTo
- questions:
  - answer: Yes, Aspose.PSD supports over 30 raster formats, including PSD, JPEG,
      PNG, BMP, TIFF, and GIF, ensuring broad compatibility.
    question: Is Aspose.PSD compatible with all image formats?
  - answer: Absolutely. After each `crop` call you receive a new image object, which
      you can crop again as needed.
    question: Can I apply multiple cropping operations to the same image?
  - answer: Yes, you can find support and engage with the community at [Aspose.PSD
      Forum](https://forum.aspose.com/c/psd/34).
    question: Is there a community forum for Aspose.PSD support?
  - answer: Visit [here](https://purchase.aspose.com/temporary-license/) to obtain
      a temporary license.
    question: How can I obtain a temporary license for Aspose.PSD?
  - answer: Explore the documentation and examples at [Aspose.PSD Java Documentation](https://reference.aspose.com/psd/java/).
    question: Are there sample projects showcasing Aspose.PSD functionalities?
  type: FAQPage
second_title: Aspose.PSD Java API
title: Przycinanie obrazu w Javie według przesunięć z Aspose.PSD
url: /pl/java/image-editing/crop-image-by-shifts/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Przycinanie obrazu w Javie przesunięciami z Aspose.PSD

## Wprowadzenie

W przetwarzaniu obrazów w Javie **crop image java** jest powszechnym wymaganiem przy przygotowywaniu grafiki, miniatur lub zasobów UI. Aspose.PSD for Java upraszcza to zadanie, udostępniając prostą metodę `crop`, działającą na każdym obsługiwanym formacie rastrowym. W tym samouczku nauczysz się, jak wczytać plik PSD, określić wartości przesunięć lewy‑prawy‑górny‑dolny, zastosować przycięcie i zapisać wynik — wszystko bez pisania własnego kodu manipulującego pikselami.

## Szybkie odpowiedzi
- **Jaką bibliotekę używać do przycinania?** Aspose.PSD for Java udostępnia wbudowaną metodę `crop`.  
- **Czy potrzebna jest licencja?** Licencja tymczasowa działa w trybie ewaluacyjnym; pełna licencja jest wymagana w produkcji.  
- **Obsługiwane formaty?** Ponad 30 formatów rastrowych, w tym PSD, JPEG, PNG, BMP i TIFF.  
- **Maksymalny rozmiar pliku?** Obsługuje pliki do 2 GB bez ładowania całego obrazu do pamięci.  
- **Ile linii kodu?** Tylko pięć logicznych kroków — wczytanie, buforowanie, określenie przesunięć, przycięcie i zapis.

## Czym jest przycinanie obrazu w Javie?
`crop image java` odnosi się do operacji przycinania bitmapy w aplikacji Java. Korzystając z Aspose.PSD, operacja jest wykonywana przez metodę `crop`, która przyjmuje wartości przesunięć dla każdej krawędzi obrazu i zwraca nową instancję obrazu.

## Dlaczego używać Aspose.PSD do przycinania obrazów?
Aspose.PSD obsługuje **30+** formatów obrazów i może przetwarzać wielostronicowe pliki PSD przy zużyciu mniej niż 150 MB RAM, dzięki architekturze lazy‑loading. Biblioteka gwarantuje wyniki piksel‑perfekcyjne, zachowując warstwy, maski i profile kolorów — coś, czego nie zapewniają wiele ogólnych bibliotek graficznych.

## Wymagania wstępne

### Java Development Kit (JDK)

Upewnij się, że masz zainstalowaną najnowszą wersję JDK na swoim systemie. Możesz ją pobrać [tutaj](https://www.oracle.com/java/technologies/javase-downloads.html).

### Aspose.PSD for Java Library

Aby rozpocząć, musisz uzyskać bibliotekę Aspose.PSD for Java. Przejdź do [strony pobierania](https://releases.aspose.com/psd/java/) i pobierz najnowszą wersję.

### Integrated Development Environment (IDE)

Wybierz ulubione środowisko IDE Java, takie jak Eclipse lub IntelliJ, aby uzyskać płynne doświadczenie programistyczne.

## Jak przyciąć obraz w Javie?

Wczytaj plik źródłowy, określ przesunięcia pikseli dla każdej krawędzi i wywołaj metodę `crop` — cały przepływ pracy można zapisać w pięciu zwięzłych linijkach kodu. Operacja `crop` tworzy nowy obraz zawierający wyłącznie określony region, pozostawiając oryginalny plik nietknięty.

### Krok 1: Załaduj obraz

`Image` jest klasą bazową dla wszystkich typów obrazów w Aspose.PSD.  
`RasterImage` reprezentuje obraz rastrowy i udostępnia możliwości przycinania.  
```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.imageoptions.JpegOptions;
```

### Krok 2: Buforuj dane obrazu

`cacheData()` ładuje dane obrazu do pamięci, przyspieszając dalsze przetwarzanie.  
```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

// Load an existing image into an instance of RasterImage class
RasterImage rasterImage = (RasterImage)Image.load(sourceFile);
```

### Krok 3: Określ wartości przesunięć

Podaj wartości przesunięć dla wszystkich czterech krawędzi obrazu (lewa, górna, prawa, dolna) w pikselach.  
```java
if (!rasterImage.isCached()) {
  rasterImage.cacheData();
}
```

### Krok 4: Zastosuj przycięcie

`crop(left, right, top, bottom)` przycina obraz o określone przesunięcia pikseli na każdej krawędzi.  
```java
int leftShift = 10;
int rightShift = 10;
int topShift = 10;
int bottomShift = 10;
```

### Krok 5: Zapisz wyniki

`JpegOptions` definiuje ustawienia kodowania JPEG, takie jak jakość i profil kolorów.  
```java
rasterImage.crop(leftShift, rightShift, topShift, bottomShift);
```

Gratulacje! Pomyślnie przycięto obraz przy użyciu Aspose.PSD for Java.

## Typowe problemy i rozwiązania

- **Obraz nie uległ zmianie:** Sprawdź, czy wartości przesunięć są dodatnie i nie przekraczają oryginalnych wymiarów.  
- **OutOfMemoryError przy dużych plikach:** Włącz buforowanie, jak pokazano w Kroku 2; zmusza to Aspose.PSD do użycia pliku tymczasowego zamiast trzymania całego obrazu w RAM.  
- **Przesunięcie kolorów po przycięciu:** Upewnij się, że zachowujesz profil kolorów, wywołując `image.save(..., new JpegOptions { ColorProfile = image.ColorProfile })`, jeśli potrzebna jest dokładna wierność kolorów.

## Najczęściej zadawane pytania

**P: Czy Aspose.PSD jest kompatybilny ze wszystkimi formatami obrazów?**  
O: Tak, Aspose.PSD obsługuje ponad 30 formatów rastrowych, w tym PSD, JPEG, PNG, BMP, TIFF i GIF, zapewniając szeroką kompatybilność.

**P: Czy mogę wykonać wiele operacji przycinania na tym samym obrazie?**  
O: Oczywiście. Po każdym wywołaniu `crop` otrzymujesz nowy obiekt obrazu, który możesz ponownie przyciąć w razie potrzeby.

**P: Czy istnieje forum społecznościowe wsparcia Aspose.PSD?**  
O: Tak, wsparcie i dyskusje społecznościowe znajdziesz na [forum Aspose.PSD](https://forum.aspose.com/c/psd/34).

**P: Jak uzyskać licencję tymczasową dla Aspose.PSD?**  
O: Odwiedź [tę stronę](https://purchase.aspose.com/temporary-license/), aby uzyskać licencję tymczasową.

**P: Czy są dostępne przykładowe projekty demonstrujące funkcje Aspose.PSD?**  
O: Zapoznaj się z dokumentacją i przykładami na [Aspose.PSD Java Documentation](https://reference.aspose.com/psd/java/).

---

**Ostatnia aktualizacja:** 2026-07-03  
**Testowano z:** Aspose.PSD 24.11 for Java  
**Autor:** Aspose  

{{< blocks/products/products-backtop-button >}}

```java
String destName = dataDir + "CroppingByShifts_out.jpg";
rasterImage.save(destName, new JpegOptions());
```

## Powiązane samouczki

- [Przycinanie obrazu prostokątem w Aspose.PSD dla Javy](/psd/java/image-editing/crop-image-by-rectangle/)
- [Przycinanie obrazu w Javie – Rozszerzanie i przycinanie obrazów z Aspose.PSD dla Javy](/psd/java/image-editing/expand-and-crop-images/)
- [Zmiana rozmiaru obrazu w Javie – Użycie wyliczenia Resize Type w Aspose.PSD dla Javy](/psd/java/advanced-image-manipulation/resizing-with-resize-type-enumeration/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}