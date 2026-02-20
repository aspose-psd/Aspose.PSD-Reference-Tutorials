---
date: 2026-02-20
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

# Konwertowanie PSD do PNG w trybie koloru 16‑bitowego w skali szarości w Javie

## Wprowadzenie
Kiedy zanurzasz się w świat projektowania graficznego i manipulacji obrazami, znajomość **how to convert PSD to PNG** jest jak posiadanie tajnej broni. Użycie trybu 16‑bitowej skali szarości dodaje niesamowitą głębię i bogactwo tonalne, sprawiając, że Twoje obrazy wyróżniają się. W tym samouczku przeprowadzimy Cię przez **set PSD color mode** na 16‑bitową skalę szarości, a następnie **export PSD as PNG** przy użyciu Aspose.PSD for Java. Gotowy, aby podnieść swój przepływ pracy z obrazami? Zaczynajmy.

## Szybkie odpowiedzi
- **What does “convert PSD to PNG” involve?** Ładowanie pliku PSD, opcjonalna zmiana jego trybu kolorów oraz zapis jako plik PNG.  
- **Which Aspose class handles the conversion?** `PsdImage` do ładowania i `PngOptions` do zapisu.  
- **Do I need a special license?** Wersja próbna działa do testów; płatna licencja jest wymagana w produkcji.  
- **Can I keep the 16‑bit depth in PNG?** Tak, używając `PngColorType.GrayscaleWithAlpha`.  
- **What IDEs are supported?** Dowolne IDE Java – IntelliJ IDEA, Eclipse, VS Code itp.

## Dlaczego konwertować PSD do PNG w 16‑bitowej skali szarości?
* **Zachowaj szczegóły tonalne:** 16‑bitowa skala szarości przechowuje 65 536 odcieni szarości, znacznie więcej niż 256 odcieni obrazu 8‑bitowego.  
* **Szeroka kompatybilność:** PNG jest szeroko wspierany w przeglądarkach, aplikacjach mobilnych i narzędziach desktopowych, jednocześnie zachowując wysokiej jakości dane.  
* **Bezstratny przepływ pracy:** Konwersja przy użyciu Aspose.PSD zapewnia brak niepożądanych artefaktów kompresji, co jest idealne do archiwizacji lub dalszego przetwarzania.

## Wymagania wstępne
Zanim zaczniemy, upewnijmy się, że masz wszystko przygotowane, aby w pełni skorzystać z tego samouczka. Oto, czego będziesz potrzebować:

1. **Java Development Kit (JDK)** – Upewnij się, że masz zainstalowaną najnowszą wersję. Możesz ją pobrać ze [strony Oracle](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).  
2. **Aspose.PSD for Java Library** – To silnik, który pozwoli nam manipulować plikami PSD. Pobierz go ze [strony pobierania Aspose](https://releases.aspose.com/psd/java/).  
3. **IDE** – IntelliJ IDEA, Eclipse lub Visual Studio Code będą w pełni wystarczające.  
4. **Podstawowa znajomość Javy** – Znajomość składni Javy ułatwi wykonywanie kolejnych kroków.  
5. **Przykładowy plik PSD** – Możesz go utworzyć w Adobe Photoshop lub pobrać darmowy przykład z internetu.

Gotowy? Świetnie! Zaimportujmy niezbędne pakiety i rozpocznijmy kodowanie.

## Importowanie pakietów
Aby rozpocząć, dodaj wymagane importy Aspose.PSD do swojego pliku Java:

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

Te importy dają dostęp do funkcjonalności, które będziesz używać do manipulacji plikami PSD, ustawiania trybu kolorów i eksportowania wyniku jako PNG.

## Krok 1: Zdefiniuj katalogi
Najpierw skonfiguruj foldery źródłowy i wyjściowy. To informuje program, gdzie odczytać oryginalny plik PSD i gdzie zapisać przekonwertowane pliki.

```java
String sourceDir = "Your Source Directory"; // Change to your source directory
String outputDir = "Your Document Directory"; // Change to your output directory
```

Zastąp ciągi znaków zastępczych rzeczywistymi ścieżkami na swoim komputerze.

## Krok 2: Utwórz metodę obsługującą przetwarzanie obrazu
Zamkniemy logikę konwersji w wielokrotnego użytku metodzie. Przyjmuje ona wszystkie parametry, które możesz chcieć dostosować, takie jak tryb kolorów, głębia bitowa i kompresja.

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

Ta metoda pozwala Ci **set PSD color mode** i następnie **export PSD as PNG** w jednym przepływie.

## Krok 3: Zdefiniuj ścieżki plików i załaduj PSD
Wewnątrz metody zbuduj pełne ścieżki plików i załaduj oryginalny 16‑bitowy PSD w skali szarości:

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

Prostokąt jest obliczany dynamicznie, aby pozostawał wyśrodkowany niezależnie od rozmiaru obrazu.

## Krok 5: Zapisz zmodyfikowany plik PSD
Po rysowaniu zapisujemy PSD z dokładnym trybem kolorów i głębokością bitową, które określiłeś. To jest sedno **setting PSD color mode** przed konwersją.

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
Na koniec ładujemy nowo zapisany PSD i eksportujemy go jako PNG. Używając `PngColorType.GrayscaleWithAlpha` zachowujemy 16‑bitową głębię w pliku PNG.

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

Teraz pomyślnie **converted PSD to PNG** zachowując wysokiej jakości 16‑bitowe dane w skali szarości.

## Typowe problemy i rozwiązania
| Problem | Dlaczego występuje | Rozwiązanie |
|-------|----------------|-----|
| **“Unsupported color type” exception** | Próba zapisania PSD z nieobsługiwaną konfiguracją kanałów. | Upewnij się, że `channelBitsCount` odpowiada rzeczywistej głębokości bitowej (16) oraz że `channelsCount` jest prawidłowe dla skali szarości (1). |
| **File not found** | Nieprawidłowa ścieżka katalogu źródłowego. | Sprawdź ponownie ciąg `sourceDir` i zweryfikuj, czy plik PSD istnieje. |
| **Output PNG appears black** | PNG zapisany bez obsługi kanału alfa. | Użyj `PngColorType.GrayscaleWithAlpha` jak pokazano powyżej. |

## Najczęściej zadawane pytania

**P: Co to jest tryb koloru 16‑bitowej skali szarości?**  
A: Zapewnia 65 536 odcieni szarości, dostarczając znacznie więcej szczegółów tonalnych niż standardowy 8‑bitowy (256 odcieni).

**P: Czy mogę używać Aspose.PSD do obrazów nie‑szarościowych?**  
A: Oczywiście! Aspose.PSD obsługuje RGB, CMYK, Lab i wiele innych trybów kolorów.

**P: Czy istnieje wersja próbna Aspose.PSD?**  
A: Tak, możesz wypróbować darmową wersję próbną Aspose.PSD. Po prostu przejdź do [strony pobierania Aspose](https://releases.aspose.com/).

**P: Gdzie mogę znaleźć więcej przykładów użycia Aspose.PSD?**  
A: Możesz sprawdzić [dokumentację](https://reference.aspose.com/psd/java/) aby uzyskać bardziej szczegółowe przykłady i samouczki.

**P: Jak mogę kupić licencję na Aspose.PSD?**  
A: Możesz kupić licencję, odwiedzając [stronę zakupu Aspose](https://purchase.aspose.com/buy).

---

**Ostatnia aktualizacja:** 2026-02-20  
**Testowano z:** Aspose.PSD for Java 24.12 (latest at time of writing)  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}