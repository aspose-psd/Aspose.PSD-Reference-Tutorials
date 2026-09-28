---
date: 2026-09-28
description: Poradnik przetwarzania obrazów w Javie pokazuje, jak regulować jasność
  obrazu przy użyciu Aspose.PSD dla Javy. Postępuj zgodnie z kodem krok po kroku,
  aby wczytać, zmodyfikować i zapisać pliki PSD lub TIFF.
keywords:
- java image processing
- aspose psd java
- java image manipulation
- adjust brightness java
lastmod: 2026-09-28
linktitle: Regulacja jasności obrazu
og_description: Poradnik przetwarzania obrazów w Javie pokazuje, jak regulować jasność
  obrazu przy użyciu Aspose.PSD dla Javy. Postępuj zgodnie z kodem krok po kroku,
  aby wczytać, zmodyfikować i zapisać pliki PSD lub TIFF.
og_image_alt: Guide to adjusting image brightness in Java using Aspose.PSD
og_title: 'Przetwarzanie obrazów w Javie: regulacja jasności przy użyciu Aspose.PSD'
schemas:
- author: Aspose
  dateModified: '2026-09-28'
  description: Java image processing tutorial shows how to adjust brightness of an
    image using Aspose.PSD for Java. Follow step‑by‑step code to load, modify, and
    save PSD or TIFF files.
  headline: 'Java image processing: adjust brightness with Aspose.PSD'
  type: TechArticle
- description: Java image processing tutorial shows how to adjust brightness of an
    image using Aspose.PSD for Java. Follow step‑by‑step code to load, modify, and
    save PSD or TIFF files.
  name: 'Java image processing: adjust brightness with Aspose.PSD'
  steps:
  - name: Load the image
    text: The `RasterImage` class represents a rasterized version of a PSD or TIFF
      file in memory. It provides direct pixel access for color‑correction operations.
      In this step, we load the target image and cast it to a `RasterImage` for further
      processing.
  - name: Adjust brightness
    text: '`adjustBrightness(int value)` changes the lightness of every pixel by the
      specified integer value. Positive numbers brighten the image; negative numbers
      darken it. The method processes the image in‑place, so no additional object
      creation is required. Here, we use the `adjustBrightness` method to mod'
  - name: Set TiffOptions
    text: '`TiffOptions` specifies the encoding parameters for TIFF output, such as
      bits per sample and photometric interpretation. It lets you control how the
      resulting file is encoded. Configure the `TiffOptions` for saving the adjusted
      image. Adjust the `bitsPerSample` and `photometric` properties based on '
  - name: Save the resultant image
    text: Calling `save` writes the processed raster data to a file using the previously
      defined options. The operation is atomic and guarantees that the output file
      is a valid TIFF image. Finally, save the modified image using the specified
      `TiffOptions`.
  type: HowTo
- questions:
  - answer: Yes, Aspose.PSD for Java supports JPEG, PNG, BMP, GIF, and many other
      raster formats in addition to PSD and TIFF.
    question: Can I adjust brightness in other image formats besides PSD?
  - answer: Wrap the processing code in a try‑catch block and catch `IOException`
      or `ImageProcessingException` to manage file‑access and raster‑operation errors.
    question: How can I handle errors during the image adjustment process?
  - answer: The method accepts integer values from –255 to +255; values outside this
      range are clamped to the nearest limit.
    question: Is there a limit to the range of brightness adjustment?
  - answer: Yes, a commercial license is required for production use. Purchase a license
      [here](https://purchase.aspose.com/buy).
    question: Can I use Aspose.PSD for Java in commercial projects?
  - answer: Yes, you can explore the library with a free trial from [here](https://releases.aspose.com/).
    question: Is there a free trial available?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- java image processing
- aspose psd
- java image manipulation
title: 'Przetwarzanie obrazów w Javie: regulacja jasności przy użyciu Aspose.PSD'
url: /pl/java/advanced-techniques/adjust-brightness/
weight: 21
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Regulacja jasności obrazu przy użyciu Aspose.PSD dla Javy

## Wprowadzenie

W tym **java image processing** tutorialu dowiesz się, jak regulować jasność obrazu bezpośrednio z kodu Java. Dostosowywanie jasności jest częstym zadaniem dla grafików, fotografów i każdego, kto buduje potoki przetwarzania obrazów. W tym **java image manipulation** przewodniku przeprowadzimy pełny przepływ pracy — ładowanie pliku PSD/TIFF, zastosowanie przesunięcia jasności i zapis wyniku — przy użyciu biblioteki Aspose.PSD for Java.

## Szybkie odpowiedzi
- **Jaka biblioteka obsługuje jasność?** Aspose.PSD for Java.  
- **Która metoda zmienia jasność?** `RasterImage.adjustBrightness()`.  
- **Czy mogę pracować z plikami PSD i TIFF?** Tak, API obsługuje oba formaty oraz ponad 10 dodatkowych typów obrazów.  
- **Czy potrzebna jest licencja do produkcji?** Licencja komercyjna jest wymagana do użytku nie‑ewaluacyjnego.  
- **Jak długo trwa implementacja?** Zazwyczaj poniżej 10 minut dla podstawowej regulacji.

## Czym jest przetwarzanie obrazu w Javie?

`Java image processing` odnosi się do zestawu technik pozwalających programowo odczytywać, przekształcać i zapisywać dane obrazu przy użyciu Javy. Regulacja jasności jest jedną z podstawowych operacji, które zmieniają ogólną jasność każdego piksela, rozjaśniając ciemne obszary lub przyciemniając jasne.

## Dlaczego używać Aspose.PSD dla Javy?

Aspose.PSD for Java zapewnia kompleksowe, czysto‑Java rozwiązanie, które obsługuje szeroką gamę formatów rastrowych i wektorowych, eliminuje zależności natywne i oferuje wysokowydajne buforowanie dla dużych plików. Rozbudowane API umożliwia programistom wykonywanie złożonych korekt kolorów i edycji warstwowych przy minimalnej ilości kodu, co czyni je idealnym zarówno dla prostych regulacji, jak i zaawansowanych potoków przetwarzania obrazów.

- **Obsługuje ponad 10 formatów rastrowych i wektorowych** – PSD, TIFF, JPEG, PNG, BMP, GIF i inne.  
- **Czysta implementacja Java** – brak natywnych DLL‑ów ani zewnętrznych zależności, więc działa na dowolnej JVM.  
- **Wysokowydajne buforowanie** – dane rastrowe mogą być buforowane, co umożliwia do 2× szybsze powtarzane edycje dużych plików.  
- **Rozbudowane API** – ponad 150 metod do korekcji kolorów, obsługi warstw, masek i kompozycji.

## Wymagania wstępne

Zanim zanurzysz się w tutorial, upewnij się, że masz następujące wymagania wstępne:

- Biblioteka Aspose.PSD for Java: Pobierz i zainstaluj bibliotekę z [dokumentacji Aspose.PSD for Java](https://reference.aspose.com/psd/java/).  
- Java Development Kit (JDK) 8 lub wyższy zainstalowany na twoim komputerze.  
- Środowisko programistyczne (IDE) takie jak IntelliJ IDEA, Eclipse lub VS Code.

## Importowanie pakietów

Aby rozpocząć, zaimportuj niezbędne pakiety do swojego projektu Java. W tym przykładzie użyjemy następujących:

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.psd.fileformats.tiff.enums.TiffPhotometrics;
import com.aspose.psd.imageoptions.TiffOptions;
```

Teraz rozbijmy proces regulacji jasności obrazu na proste kroki:

## Jak regulować jasność przy użyciu Aspose.PSD?

Załaduj obraz źródłowy, zastosuj przesunięcie jasności, skonfiguruj opcje zapisu i zapisz wynik na dysku — wszystko w czterech zwięzłych krokach. Poniższe sekcje zapewniają klarowny przewodnik krok po kroku, który możesz skopiować do własnego projektu. To podejście zapewnia, że każda operacja jest wykonywana wydajnie, a końcowy obraz zachowuje oryginalną jakość, odzwierciedlając pożądaną zmianę jasności.

### Krok 1: Załaduj obraz

Klasa `RasterImage` reprezentuje rasteryzowaną wersję pliku PSD lub TIFF w pamięci. Zapewnia bezpośredni dostęp do pikseli dla operacji korekcji kolorów.

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";
String destName = dataDir + "AdjustBrightness_out.tiff";

// Load an existing image into an instance of RasterImage class
Image image = Image.load(sourceFile);
// Cast object of Image to RasterImage
RasterImage rasterImage = (RasterImage) image;

// Check if RasterImage is cached and Cache RasterImage for better performance
if (!rasterImage.isCached()) {
    rasterImage.cacheData();
}
```

W tym kroku ładujemy docelowy obraz i rzutujemy go na `RasterImage` w celu dalszego przetwarzania.

### Krok 2: Regulacja jasności

`adjustBrightness(int value)` zmienia jasność każdego piksela o podaną wartość całkowitą. Liczby dodatnie rozjaśniają obraz; liczby ujemne go przyciemniają. Metoda przetwarza obraz w miejscu, więc nie jest wymagana dodatkowa kreacja obiektu.

```java
// Adjust the brightness
rasterImage.adjustBrightness(-50);
```

Tutaj używamy metody `adjustBrightness`, aby zmodyfikować jasność obrazu. W tym przykładzie zmniejszamy jasność o 50 jednostek, ale możesz dostosować tę wartość według własnych wymagań.

### Krok 3: Ustawienie TiffOptions

`TiffOptions` określa parametry kodowania wyjściowego TIFF, takie jak liczba bitów na próbkę i interpretacja fotometryczna. Pozwala kontrolować sposób kodowania powstałego pliku.

```java
int[] ushort = {8, 8, 8};
// Create an instance of TiffOptions for the resultant image
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
tiffOptions.setBitsPerSample(ushort);
tiffOptions.setPhotometric(TiffPhotometrics.Rgb);
```

Skonfiguruj `TiffOptions` do zapisu zmodyfikowanego obrazu. Dostosuj właściwości `bitsPerSample` i `photometric` zgodnie ze swoimi potrzebami.

### Krok 4: Zapis zmodyfikowanego obrazu

Wywołanie `save` zapisuje przetworzone dane rastrowe do pliku przy użyciu wcześniej zdefiniowanych opcji. Operacja jest atomowa i zapewnia, że plik wyjściowy jest prawidłowym obrazem TIFF.

```java
// Save the resultant image
rasterImage.save(destName, tiffOptions);
```

Na koniec zapisz zmodyfikowany obraz używając określonych `TiffOptions`.

## Typowe problemy i rozwiązania

| Problem | Przyczyna | Rozwiązanie |
|-------|--------|----------|
| **`ClassCastException` przy rzutowaniu Image** | Plik nie jest obrazem rastrowym (np. wektorowy PSD). | Sprawdź format pliku źródłowego lub użyj `image instanceof RasterImage` przed rzutowaniem. |
| **Zmiana jasności nie ma efektu** | Obraz nie został zbuforowany przed regulacją. | Wywołaj `rasterImage.cacheData()` jak pokazano w Kroku 1. |
| **Zapisany plik wydaje się uszkodzony** | Nieprawidłowa konfiguracja `TiffOptions`. | Upewnij się, że `bitsPerSample` odpowiada głębokości obrazu źródłowego (zwykle 8‑bit na kanał). |

## Najczęściej zadawane pytania

**P: Czy mogę regulować jasność w innych formatach obrazów poza PSD?**  
O: Tak, Aspose.PSD for Java obsługuje JPEG, PNG, BMP, GIF i wiele innych formatów rastrowych oprócz PSD i TIFF.

**P: Jak mogę obsłużyć błędy podczas procesu regulacji obrazu?**  
O: Umieść kod przetwarzania w bloku try‑catch i przechwyć `IOException` lub `ImageProcessingException`, aby zarządzać błędami dostępu do plików i operacji rastrowych.

**P: Czy istnieje limit zakresu regulacji jasności?**  
O: Metoda przyjmuje wartości całkowite od –255 do +255; wartości poza tym zakresem są ograniczane do najbliższej granicy.

**P: Czy mogę używać Aspose.PSD for Java w projektach komercyjnych?**  
O: Tak, wymagana jest licencja komercyjna do użytku produkcyjnego. Kup licencję [tutaj](https://purchase.aspose.com/buy).

**P: Czy dostępna jest darmowa wersja próbna?**  
O: Tak, możesz wypróbować bibliotekę w wersji próbnej [tutaj](https://releases.aspose.com/).

**P: Czy metoda `adjustBrightness` wpływa na widoczność warstw?**  
O: Metoda działa na rasteryzowanym obrazie złożonym, więc ukryte warstwy są pomijane podczas rasteryzacji, zachowując zamierzony efekt wizualny.

**P: Czy mogę łączyć wiele regulacji (np. kontrast, nasycenie) razem?**  
O: Oczywiście. Po regulacji jasności możesz wywołać `adjustContrast`, `adjustSaturation` lub inne metody korekcji kolorów na tym samym obiekcie `RasterImage`.

---

**Last Updated:** 2026-09-28  
**Tested With:** Aspose.PSD for Java 24.12 (latest at time of writing)  
**Author:** Aspose

## Powiązane tutoriale

- [Biblioteka przetwarzania obrazów Java: Odwrócenie warstwy przy użyciu Aspose.PSD](/psd/java/advanced-image-manipulation/invert-adjustment-layer/)
- [Konwersja obrazu do odcieni szarości przy użyciu Aspose.PSD for Java](/psd/java/advanced-techniques/grayscale-image/)
- [Jak obrócić obraz pod określonym kątem przy użyciu Aspose.PSD for Java](/psd/java/advanced-image-manipulation/rotate-image-specific-angle/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}