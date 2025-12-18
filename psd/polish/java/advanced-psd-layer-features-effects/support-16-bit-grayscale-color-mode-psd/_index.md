---
date: 2025-12-17
description: Dowiedz się, jak konwertować pliki PSD na PNG, ustawiając tryb kolorów
  PSD na 16‑bitowy odcień szarości przy użyciu Aspose.PSD dla Javy. Przewodnik krok
  po kroku z przykładami kodu.
linktitle: Convert PSD to PNG – 16-bit Grayscale – Java
second_title: Aspose.PSD Java API
title: Jak przekonwertować PSD na PNG w trybie 16‑bitowej skali szarości w Javie
url: /pl/java/advanced-psd-layer-features-effects/support-16-bit-grayscale-color-mode-psd/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Konwertowanie PSD do PNG w trybie koloru szarości 16‑bit w Javie

## Wprowadzenie
Kiedy zanurzasz się w świat projektowania graficznego i manipulacji obrazami, zrozumienie, jak **konwertować PSD do PNG** jest jak posiadanie tajnej broni. W szczególności użycie trybu szarości 16‑bit daje Twoim obrazom oszałamiającą głębię i szczegółowość, które naprawdę je wyróżniają. W tym samouczku przejdziemy krok po kroku, jak **ustawić tryb koloru PSD** na 16‑bit szarość, a następnie **wyeksportować PSD jako PNG** przy użyciu Aspose.PSD for Java. Gotowy, aby podnieść swój przepływ pracy z obrazami? Zaczynajmy.

## Szybkie odpowiedzi
- **Co obejmuje „convert PSD to PNG”?** Ładowanie pliku PSD, opcjonalna zmiana jego trybu koloru i zapisanie go jako plik PNG.  
- **Która klasa Aspose obsługuje konwersję?** `PsdImage` do ładowania i `PngOptions` do zapisywania.  
- **Czy potrzebna jest specjalna licencja?** Wersja próbna działa do testów; licencja płatna jest wymagana w produkcji.  
- **Czy mogę zachować głębię 16‑bit w PNG?** Tak, używając `PngColorType.GrayscaleWithAlpha`.  
- **Jakie IDE są obsługiwane?** Dowolne IDE Java – IntelliJ IDEA, Eclipse, VS Code, itp.

## Wymagania wstępne
Zanim zaczniemy, upewnijmy się, że masz wszystko, co potrzebne, aby w pełni wykorzystać ten samouczek. Oto, czego będziesz potrzebować:

1. **Java Development Kit (JDK)** – Upewnij się, że masz zainstalą najnowszą wersję. Możesz ją pobrać z [Oracle's site](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).  
2. **Aspose.PSD for Java Library** – To silnik, który pozwoli nam manipulować plikami PSD. Pobierz go ze [strony pobierania Aspose](https://releases.aspose.com/psd/java/).  
3. **IDE** – IntelliJ IDEA, Eclipse lub Visual Studio Code będą w porządku.  
4. **Podstawowa znajomość Javy** – Znajomość składni Javy ułatwi kolejne kroki.  
5. **Przykładowy plik PSD** – Możesz go utworzyć w Adobe Photoshop lub pobrać darmowy przykład online.

Gotowy? Świetnie! Zaimportujmy niezbędne pakiety i rozpocznijmy kodowanie.

## Importowanie pakietów
Na początek dodaj wymagane importy Aspose.PSD do swojego pliku Java:

```java
import com.aspose.psd.*;
import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.fileformats.psd.ColorModes;
import com.aspose.psd.fileformats.psd.CompressionMethod;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.PngOptions;
import com.aspose.psd.imageoptions.PsdOptions;
import com.aspose.psd.system.Enum;
```

Te importy dają dostęp do funkcji, które będziesz używać do manipulacji plikami PSD, ustawiania trybu koloru i eksportowania wyniku jako PNG.

## Krok 1: Zdefiniuj katalogi
Najpierw skonfiguruj foldery źródłowy i wyjściowy. To informuje program, skąd odczytać oryginalny PSD i gdzie zapisać skonwertowane pliki.

```java
String sourceDir = "Your Source Directory"; // Change to your source directory
String outputDir = "Your Document Directory"; // Change to your output directory
```

Zastąp ciągi znaków zastępczych rzeczywistymi ścieżkami na swoim komputerze.

## Krok 2: Utwórz metodę obsługującą przetwarzanie obrazu
Zamkniemy logikę konwersji w wielokrotnego użytku metodzie. Otrzymuje ona wszystkie parametry, które możesz chcieć dostosować, takie jak tryb koloru, głębia bitowa i kompresja.

```java
class LocalScopeExtension {
    void saveToPsdThenLoadAndSaveToPng(
        String file,
        short colorMode,
        short channelBitsCount,
        short channelsCount,
        short compression,
        int layerNumber) {
```

Ta metoda pozwala **ustawić tryb koloru PSD** i następnie **wyeksportować PSD jako PNG** w jednym przepływie.

## Krok 3: Zdefiniuj ścieżki plików i załaduj PSD
Wewnątrz metody zbuduj pełne ścieżki plików i załaduj oryginalny 16‑bitowy PSD w trybie szarości:

```java
String filePath = sourceDir + file + ".psd";
String postfix = Enum.getName(ColorModes.class, colorMode) + channelBitsCount + "_" +
                 channelsCount + "_" + Enum.getName(CompressionMethod.class, compression);
String exportPath = outputDir + file + postfix + ".psd";
String pngExportPath = outputDir + file + postfix + ".png";
// Load a predefined 16-bit grayscale PSD
PsdImage image = (PsdImage)Image.load(filePath);
```

`postfix` pomaga śledzić ustawienia użyte dla każdego wyeksportowanego pliku.

## Krok 4: Przetwórz warstwę lub cały obraz
Teraz rysujemy albo na konkretnej warstwie, albo na całym obrazie. W tym przykładzie dodajemy subtelną szarą ramkę, aby wynik był bardziej widoczny.

```java
try {
    RasterCachedImage raster = layerNumber >= 0 ? image.getLayers()[layerNumber] : image;
    // Draw a gray inner border around the perimeter of the layer
    Graphics graphics = new Graphics(raster);
    int width = raster.getWidth();
    int height = raster.getHeight();
    Rectangle rect = new Rectangle(
        width / 3,
        height / 3,
        width - (2 * (width / 3)) - 1,
        height - (2 * (height / 3)) - 1);
    graphics.drawRectangle(new Pen(Color.getDarkGray(), 1), rect);
```

Prostokąt jest obliczany dynamicznie, więc pozostaje wyśrodkowany niezależnie od rozmiaru obrazu.

## Krok 5: Zapisz zmodyfikowany plik PSD
Po rysowaniu zapisujemy PSD z dokładnym trybem koloru i głębokością bitową, które określiłeś. To jest sedno **ustawiania trybu koloru PSD** przed konwersją.

```java
    // Save a copy of PSD with specific characteristics
    PsdOptions psdOptions = new PsdOptions();
    psdOptions.setColorMode(colorMode);
    psdOptions.setChannelBitsCount(channelBitsCount);
    psdOptions.setChannelsCount(channelsCount);
    psdOptions.setCompressionMethod(compression);
    image.save(exportPath, psdOptions);
}
```

## Krok 6: Konwertuj PSD do PNG
Na koniec ładujemy nowo zapisany PSD i eksportujemy go jako PNG. Używając `PngColorType.GrayscaleWithAlpha` zachowujemy głębię 16‑bit w pliku PNG.

```java
finally {
    image.dispose();
}
// Load the saved PSD
PsdImage image1 = (PsdImage)Image.load(exportPath);
try {
    // Convert the saved PSD to a grayscale PNG image
    PngOptions pngOptions = new PngOptions();
    pngOptions.setColorType(PngColorType.GrayscaleWithAlpha);
    image1.save(pngExportPath, pngOptions); // here should be no exception
}
finally {
    image1.dispose();
}
```

Teraz pomyślnie **konwertowałeś PSD do PNG**, zachowując wysokiej jakości dane 16‑bitowej skali szarości.

## Typowe problemy i rozwiązania
| Problem | Dlaczego się pojawia | Rozwiązanie |
|---------|----------------------|-------------|
| **Wyjątek „Unsupported color type”** | Próba zapisania PSD z nieobsługiwaną konfiguracją kanałów. | Upewnij się, że `channelBitsCount` odpowiada rzeczywistej głębokości bitowej (16) oraz że `channelsCount` jest prawidłowe dla skali szarości (1). |
| **Plik nie znaleziony** | Nieprawidłowa ścieżka katalogu źródłowego. | Sprawdź dokładnie ciąg `sourceDir` i zweryfikuj, czy plik PSD istnieje. |
| **Wyjściowy PNG jest czarny** | PNG zapisany bez obsługi kanału alfa. | Użyj `PngColorType.GrayscaleWithAlpha` jak pokazano powyżej. |

## Najczęściej zadawane pytania

**Q: Co to jest tryb koloru szarości 16‑bit?**  
A: Dostarcza 65 536 odcieni szarości, zapewniając znacznie więcej szczegółów tonalnych niż standardowy 8‑bitowy (256 odcieni).

**Q: Czy mogę używać Aspose.PSD do obrazów nie‑szarościowych?**  
A: Oczywiście! Aspose.PSD obsługuje RGB, CMYK, Lab i wiele innych trybów koloru.

**Q: Czy istnieje wersja próbna Aspose.PSD?**  
A: Tak, możesz wypróbować darmową wersję próbną Aspose.PSD. Przejdź po prostu na [stronę pobierania Aspose](https://releases.aspose.com/).

**Q: Gdzie mogę znaleźć więcej przykładów użycia Aspose.PSD?**  
A: Możesz sprawdzić [dokumentację](https://reference.aspose.com/psd/java/) po więcej szczegółowych przykładów i samouczków.

**Q: Jak mogę kupić licencję na Aspose.PSD?**  
A: Możesz kupić licencję, odwiedzając [stronę zakupu Aspose](https://purchase.aspose.com/buy).

**Ostatnia aktualizacja:** 2025-12-17  
**Testowano z:** Aspose.PSD for Java 24.12 (najnowsza w momencie pisania)  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}