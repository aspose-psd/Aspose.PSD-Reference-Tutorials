---
date: 2026-09-28
description: Dowiedz się, jak wyeksportować PSD jako PNG, ustawiając tryb koloru PSD
  na 16‑bit grayscale przy użyciu Aspose.PSD for Java. Step‑by‑step guide with code
  examples.
keywords:
- export psd as png
- how to convert psd to png
- 16-bit grayscale java
lastmod: 2026-09-28
linktitle: Eksportuj PSD jako PNG – 16‑bit Grayscale – Java
og_description: Eksportuj PSD jako PNG w 16‑bit grayscale przy użyciu Aspose.PSD for
  Java. Postępuj zgodnie z tym step‑by‑step tutorial, aby zachować 65,536 odcieni
  szarości.
og_image_alt: Guide showing how to export PSD as PNG with 16-bit grayscale using Aspose.PSD
  Java
og_title: Eksportuj PSD jako PNG w 16‑bit grayscale w Javie – Poradnik Aspose.PSD
schemas:
- author: Aspose
  dateModified: '2026-09-28'
  description: Learn how to export PSD as PNG while setting PSD color mode to 16-bit
    grayscale using Aspose.PSD for Java. Step‑by‑step guide with code examples.
  headline: How to export PSD as PNG with 16‑bit grayscale color mode in Java
  type: TechArticle
- description: Learn how to export PSD as PNG while setting PSD color mode to 16-bit
    grayscale using Aspose.PSD for Java. Step‑by‑step guide with code examples.
  name: How to export PSD as PNG with 16‑bit grayscale color mode in Java
  steps:
  - name: '**Java Development Kit (JDK)** – Install the latest JDK from [Oracle''s
      site](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).'
    text: '**Java Development Kit (JDK)** – Install the latest JDK from [Oracle''s
      site](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).'
  - name: '**Aspose.PSD for Java library** – Download the JAR from the [Aspose download
      page](https://releases.aspose.com/psd/java/).'
    text: '**Aspose.PSD for Java library** – Download the JAR from the [Aspose download
      page](https://releases.aspose.com/psd/java/).'
  - name: '**An IDE** – IntelliJ IDEA, Eclipse, or Visual Studio Code works perfectly.'
    text: '**An IDE** – IntelliJ IDEA, Eclipse, or Visual Studio Code works perfectly.'
  - name: '**Basic Java knowledge** – You should be comfortable creating classes,
      handling exceptions, and working with file paths.'
    text: '**Basic Java knowledge** – You should be comfortable creating classes,
      handling exceptions, and working with file paths.'
  - name: '**A sample PSD file** – Create one in Adobe Photoshop or grab a free sample
      online.'
    text: '**A sample PSD file** – Create one in Adobe Photoshop or grab a free sample
      online.'
  type: HowTo
- questions:
  - answer: It provides 65 536 shades of gray, delivering far more tonal detail than
      the standard 8‑bit (256 shades).
    question: What is 16‑bit grayscale color mode?
  - answer: Absolutely! Aspose.PSD supports RGB, CMYK, Lab, Indexed, and many other
      color modes.
    question: Can I use Aspose.PSD for non‑grayscale images?
  - answer: Yes, you can try a free trial version of Aspose.PSD. Just head to the
      [Aspose download page](https://releases.aspose.com/).
    question: Is there a trial version of Aspose.PSD?
  - answer: Check the official [documentation](https://reference.aspose.com/psd/java/)
      for in‑depth tutorials, API references, and sample projects.
    question: Where can I find more Aspose.PSD examples?
  - answer: You can buy a license by visiting the [Aspose purchase page](https://purchase.aspose.com/buy).
    question: How do I purchase a license for Aspose.PSD?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- convert psd
- Aspose.PSD
- Java image processing
title: Jak wyeksportować PSD jako PNG w trybie 16‑bit grayscale w Javie
url: /pl/java/advanced-psd-layer-features-effects/support-16-bit-grayscale-color-mode-psd/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Eksportuj PSD jako PNG w trybie 16‑bitowej skali szarości w Javie

## Wprowadzenie
Eksportowanie pliku PSD jako PNG przy zachowaniu 16‑bitowego trybu skali szarości zapewnia głębię profesjonalnego zdjęcia oraz uniwersalną kompatybilność PNG. W tym przewodniku dowiesz się, jak **ustawić tryb koloru PSD na 16‑bitową skalę szarości** oraz **wyeksportować PSD jako PNG** przy użyciu Aspose.PSD dla Javy. Samouczek obejmuje wszystko, od wymagań wstępnych po rozwiązywanie problemów, abyś mógł zintegrować ten proces w dowolnym potoku obrazów opartym na Javie.

## Szybkie odpowiedzi
- **Co obejmuje „eksport PSD jako PNG”?** Załaduj plik PSD, opcjonalnie zmień jego tryb koloru i zapisz go jako plik PNG.  
- **Która klasa Aspose obsługuje konwersję?** `PsdImage` ładuje PSD, a `PngOptions` definiuje ustawienia wyjściowe PNG.  
- **Czy potrzebna jest licencja do produkcji?** Tak – wersja próbna działa w testach, ale do użytku komercyjnego wymagana jest płatna licencja.  
- **Czy głębia 16‑bitowa może być zachowana w PNG?** Oczywiście, używając `PngColorType.GrayscaleWithAlpha`.  
- **Jakie IDE są obsługiwane?** Dowolne IDE Java – IntelliJ IDEA, Eclipse, VS Code lub NetBeans.

## Co to jest eksport PSD jako PNG?
Eksport PSD jako PNG to proces konwersji dokumentu Adobe Photoshop (PSD) na plik Portable Network Graphics (PNG) przy zachowaniu danych pikseli i głębi kolorów obrazu. Konwersja ta jest powszechnie używana do udostępniania wysokiej jakości zasobów w skali szarości w sieci bez utraty detali tonalnych.

## Dlaczego eksportować PSD jako PNG w 16‑bitowej skali szarości?
Eksportowanie do PNG przy zachowaniu 16‑bitowej skali szarości zachowuje 65 536 odcieni szarości, co zapewnia znacznie większą bogactwo tonalne niż obrazy 8‑bitowe. Uniwersalne wsparcie PNG zapewnia, że pliki mogą być wyświetlane w przeglądarkach, aplikacjach mobilnych i edytorach desktopowych bez strat, a bezstratna kompresja Aspose.PSD gwarantuje brak wprowadzonych artefaktów.

## Wymagania wstępne
1. **Java Development Kit (JDK)** – Zainstaluj najnowszy JDK ze [strony Oracle](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).  
2. **Biblioteka Aspose.PSD for Java** – Pobierz plik JAR ze [strony pobierania Aspose](https://releases.aspose.com/psd/java/).  
3. **IDE** – IntelliJ IDEA, Eclipse lub Visual Studio Code działają doskonale.  
4. **Podstawowa znajomość Javy** – Powinieneś swobodnie tworzyć klasy, obsługiwać wyjątki i pracować ze ścieżkami plików.  
5. **Przykładowy plik PSD** – Utwórz go w Adobe Photoshop lub pobierz darmowy przykład online.

## Jak wyeksportować PSD jako PNG krok po kroku

## Jak ustawić tryb koloru PSD na 16‑bitową skalę szarości?
PsdImage to klasa Aspose.PSD, która ładuje i reprezentuje plik PSD w pamięci.  
ColorMode to wyliczenie definiujące tryb koloru obrazu PSD.  

Załaduj PSD przy użyciu `PsdImage`, zmień jego tryb koloru za pomocą właściwości `ColorMode`, a następnie zapisz zmodyfikowany plik. Operacja odbywa się w całości w pamięci, eliminując potrzebę plików pośrednich i zapewniając szybką oraz wydajną konwersję.

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

Te importy dają dostęp do funkcjonalności, które będziesz używać do manipulacji plikami PSD, ustawiania trybu koloru i eksportowania wyniku jako PNG.

## Jak określić katalogi źródłowe i wyjściowe?
`File` to klasa java.io reprezentująca ścieżkę do pliku lub katalogu w systemie plików.  

Musisz poinformować program, gdzie odczytać oryginalny PSD i gdzie zapisać skonwertowany PNG. Używanie ścieżek bezwzględnych lub względnych działa, ale zachowaj ich spójność w różnych środowiskach, aby uniknąć błędów rozwiązywania ścieżek.

```java
String sourceDir = "Your Source Directory"; // Change to your source directory
String outputDir = "Your Document Directory"; // Change to your output directory
```

Zastąp ciągi zastępcze rzeczywistymi ścieżkami na swoim komputerze.

## Jak ująć logikę konwersji w metodę wielokrotnego użytku?
`convertPsdToPng` to niestandardowa metoda, która zawiera wszystkie kroki niezbędne do konwersji pliku PSD na PNG z opcjonalnymi ustawieniami.  

Utworzenie dedykowanej metody pozwala ponownie wykorzystać te same kroki konwersji dla wielu plików lub różnych ustawień. Przekazuj parametry takie jak ścieżka źródłowa, folder docelowy oraz opcjonalny poziom kompresji, co sprawia, że przepływ pracy jest elastyczny i łatwy w utrzymaniu.

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

Ta metoda pozwala **ustawić tryb koloru PSD** i następnie **wyeksportować PSD jako PNG** w jednym ciągu.

## Jak załadować PSD i zastosować 16‑bitowy tryb skali szarości?
PsdImage to klasa Aspose.PSD, która ładuje plik PSD do pamięci.  
ColorMode.GRAYSCALE_16 to wartość wyliczenia ustawiająca obraz na 16‑bitową skalę szarości.  
`channelBitsCount` to właściwość określająca liczbę bitów na kanał.  

Wewnątrz metody konwersji zbuduj pełne ścieżki plików, utwórz instancję `PsdImage` i zmień jej `ColorMode` na `ColorMode.GRAYSCALE_16`. Właściwość `channelBitsCount` musi być ustawiona na 16, aby zachować wysoką głębię bitową, zapewniając, że obraz zachowuje wszystkie informacje tonalne.

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

## Jak narysować subtelną ramkę na obrazie (krok opcjonalny)?
`Graphics` to klasa zapewniająca możliwości rysowania na płótnie `PsdImage`.  

Możesz opcjonalnie narysować szary prostokąt wokół obrazu, aby wynik był lepiej widoczny podczas testów. Ten krok pokazuje, jak pracować z warstwami i obiektami graficznymi, a prostokąt jest obliczany dynamicznie, aby pozostawał wyśrodkowany niezależnie od rozmiaru obrazu.

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

## Jak zapisać zmodyfikowany PSD z nowym trybem koloru?
`PsdOptions` to klasa kontrolująca sposób zapisu pliku PSD, w tym ustawienia trybu koloru i głębi bitowej.  

Po rysowaniu (lub pominięciu tego kroku) wywołaj `save` na instancji `PsdImage`, przekazując obiekt `PsdOptions`, który zachowuje konfigurację 16‑bitowej skali szarości. Dzięki temu zapisany PSD zachowuje żądany tryb koloru bez utraty danych.

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

## Jak skonwertować PSD do PNG zachowując głębię 16‑bit?
`PngOptions` to klasa definiująca ustawienia wyjściowe PNG, takie jak typ koloru i poziom kompresji.  
`PngColorType.GrayscaleWithAlpha` to wartość wyliczenia przechowująca 16‑bitowe dane skali szarości z kanałem alfa.  

Załaduj nowo zapisany PSD, skonfiguruj `PngOptions` z `PngColorType.GrayscaleWithAlpha` i wywołaj `save`. To zachowuje 16‑bitowe dane skali szarości w pliku PNG, zapewniając bezstratny, wysokiej jakości obraz odpowiedni do dalszego przetwarzania lub dystrybucji.

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

Teraz pomyślnie **wyeksportowałeś PSD jako PNG**, zachowując wysokiej jakości 16‑bitowe dane skali szarości.

## Typowe problemy i rozwiązania
| Problem | Dlaczego się pojawia | Rozwiązanie |
|---------|----------------------|-------------|
| **Wyjątek „Unsupported color type”** | Próba zapisania PSD z nieobsługiwaną konfiguracją kanałów. | Upewnij się, że `channelBitsCount` odpowiada rzeczywistej głębi bitowej (16) oraz że `channelsCount` jest prawidłowe dla skali szarości (1). |
| **Plik nie znaleziony** | Nieprawidłowa ścieżka katalogu źródłowego. | Sprawdź dokładnie ciąg `sourceDir` i zweryfikuj, czy plik PSD istnieje w podanej lokalizacji. |
| **Wyjściowy PNG jest czarny** | PNG zapisany bez prawidłowego obsłużenia kanału alfa. | Użyj `PngColorType.GrayscaleWithAlpha` jak pokazano powyżej. |
| **Przepełnienie pamięci przy dużych PSD** | Ładowanie całego pliku do pamięci. | Włącz tryb strumieniowy za pomocą `PsdImage.load(inputStream, new LoadOptions())`, aby efektywnie przetwarzać duże pliki. |

## Najczęściej zadawane pytania

**Q: Co to jest 16‑bitowy tryb skali szarości?**  
A: Zapewnia 65 536 odcieni szarości, dostarczając znacznie więcej detali tonalnych niż standardowy 8‑bitowy (256 odcieni).

**Q: Czy mogę używać Aspose.PSD do obrazów nie‑szarościowych?**  
A: Oczywiście! Aspose.PSD obsługuje tryby RGB, CMYK, Lab, Indexed i wiele innych.

**Q: Czy istnieje wersja próbna Aspose.PSD?**  
A: Tak, możesz wypróbować darmową wersję próbną Aspose.PSD. Przejdź po prostu na [stronę pobierania Aspose](https://releases.aspose.com/).

**Q: Gdzie mogę znaleźć więcej przykładów Aspose.PSD?**  
A: Sprawdź oficjalną [dokumentację](https://reference.aspose.com/psd/java/) zawierającą szczegółowe samouczki, odniesienia API i przykładowe projekty.

**Q: Jak mogę zakupić licencję na Aspose.PSD?**  
A: Licencję możesz kupić, odwiedzając [stronę zakupu Aspose](https://purchase.aspose.com/buy).

**Ostatnia aktualizacja:** 2026-09-28  
**Testowano z:** Aspose.PSD for Java 24.12 (najnowsza w momencie pisania)  
**Autor:** Aspose

## Powiązane samouczki

- [Konwertuj PSD na PNG z określoną głębią bitową przy użyciu Aspose.PSD dla Java](/psd/java/optimizing-png-files/specify-png-bit-depth/)
- [Eksportuj PSD do PNG z efektami warstw przy użyciu Aspose.PSD dla Java](/psd/java/psd-image-modification-conversion/apply-layer-effects-psd-files/)
- [Zapisz PSD jako JPEG i obsłuż kolor RGB przy użyciu Aspose.PSD Java](/psd/java/advanced-psd-layer-features-effects/support-rgb-color-psd-files/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}