---
date: 2026-05-19
description: Dowiedz się, jak konwertować PSD do JPEG i obracać obraz o 270 stopni
  przy użyciu Aspose.PSD for Java. Ten przewodnik pokazuje, jak obracać pliki PSD,
  odwracać obrazy i konwertować PSD do JPEG.
keywords:
- convert psd to jpeg
- how to rotate psd
- flip image java
- rotate psd layer
- rotate image without photoshop
linktitle: Obróć obraz o 270 stopni
schemas:
- author: Aspose
  dateModified: '2026-05-19'
  description: Learn how to convert PSD to JPEG and rotate image 270 degrees using
    Aspose.PSD for Java. This guide shows how to rotate PSD files, flip images, and
    convert PSD to JPEG.
  headline: Convert PSD to JPEG & Rotate 270° with Aspose.PSD for Java
  type: TechArticle
- description: Learn how to convert PSD to JPEG and rotate image 270 degrees using
    Aspose.PSD for Java. This guide shows how to rotate PSD files, flip images, and
    convert PSD to JPEG.
  name: Convert PSD to JPEG & Rotate 270° with Aspose.PSD for Java
  steps:
  - name: Load the PSD File
    text: '`Image` is Aspose.PSD''s core class that represents a single PSD document
      in memory. Instantiating it reads only the header information, keeping memory
      usage low.'
  - name: Rotate the Image 270 Degrees
    text: '`rotateFlip` performs the specified rotation and optional flip on the image.
      `RotateFlipType.Rotate270FlipNone` rotates the canvas 270 degrees clockwise
      while leaving the image orientation unchanged. > **Pro tip:** If you also need
      to flip the image horizontally or vertically, choose a different `Ro'
  - name: Convert PSD to JPEG and Save
    text: '`JpegOptions` defines JPEG‑specific parameters such as compression quality.
      The `save` method writes the transformed image to disk in the desired format.
      The file `RotatedImage_out.jpg` now contains the original PSD content rotated
      270 degrees and saved as a JPEG.'
  type: HowTo
- questions:
  - answer: Yes, Aspose.PSD supports PSD, JPEG, PNG, BMP, GIF, TIFF, and many other
      raster formats.
    question: Is Aspose.PSD compatible with different image formats?
  - answer: Absolutely! While `RotateFlipType` provides common angles, you can chain
      multiple calls or use transformation matrices for arbitrary angles.
    question: Can I apply custom rotations, not just predefined flips?
  - answer: Replace `JpegOptions` with `PngOptions` (or the appropriate options class)
      in the `save` method.
    question: How do I convert the rotated PSD to another format, such as PNG?
  - answer: For community help, visit the [Aspose.PSD Forum](https://forum.aspose.com/c/psd/34).
    question: Where can I find additional support or assistance?
  - answer: Yes, you can explore Aspose.PSD with a [free trial](https://releases.aspose.com/).
    question: Is there a free trial available?
  type: FAQPage
second_title: Aspose.PSD Java API
title: Konwertuj PSD do JPEG i obróć o 270° przy użyciu Aspose.PSD for Java
url: /pl/java/advanced-image-manipulation/rotate-image/
weight: 19
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Konwertuj PSD do JPEG i obróć obraz o 270 stopni przy użyciu Aspose.PSD dla Javy

## Wprowadzenie

W tym **tutorialu przetwarzania obrazów w Javie** dowiesz się, jak **konwertować PSD do JPEG** jednocześnie obracając obraz o 270 stopni przy użyciu Aspose.PSD dla Javy. Niezależnie od tego, czy tworzysz potok przetwarzania wsadowego, edytor internetowy, czy narzędzie desktopowe, biblioteka pozwala manipulować warstwami PSD bez Photoshopa. Omówimy także opcjonalne odbicie i pokażemy pełny przepływ od załadowania pliku PSD do zapisania JPEG.

## Szybkie odpowiedzi
- **Jaką bibliotekę obsługuje obrót?** Aspose.PSD for Java  
- **Jaki kąt obrotu jest używany w przykładzie?** 270 degrees  
- **Czy mogę także odbić obraz?** Yes – use `RotateFlipType` options like `Rotate90FlipX`  
- **Jak zapisać wynik?** In the example we save as JPEG using `JpegOptions`  
- **Czy potrzebuję licencji do produkcji?** A valid Aspose.PSD license is required for commercial use  

## Co to jest „obrócenie obrazu o 270 stopni”?

Obracanie obrazu o 270 stopni oznacza obrócenie zdjęcia o trzy czwarte pełnego obrotu zgodnie z ruchem wskazówek zegara (lub o 90 stopni przeciwnie do ruchu wskazówek zegara). Ta orientacja często przywraca pierwotny układ pionowy po wcześniejszych przekształceniach i jest powszechnie używana, gdy obrazy zostały zrobione w trybie poziomym, ale muszą być wyświetlane w pionie. Efektem jest prawidłowo skierowany obraz bez utraty jakości.

## Dlaczego używać Aspose.PSD do tego zadania?

Aspose.PSD obsługuje **ponad 50 formatów wejściowych i wyjściowych** — w tym PSD, JPEG, PNG, BMP, GIF i TIFF — i może przetwarzać pliki do **2 GB** bez ładowania całego dokumentu do pamięci. API działa na dowolnym środowisku Java (JDK 8+), nie wymaga natywnej instalacji Photoshopa i zapewnia pojedyncze wywołanie `rotateFlip`, które obsługuje zarówno obrót, jak i odbicie w jednym kroku.

## Wymagania wstępne

- Bibliotekę **Aspose.PSD for Java** zainstalowaną. Możesz ją pobrać i zobaczyć pełną dokumentację API [tutaj](https://reference.aspose.com/psd/java/).  
- Środowisko programistyczne Java (JDK 8 lub wyższy).  
- Przykładowy plik PSD, który chcesz obrócić. Zaktualizuj zmienną `sourceFile` w kodzie, podając prawidłową ścieżkę do swojego pliku.

## Importowanie pakietów

Klasy `Image`, `RotateFlipType` i `JpegOptions` są wymagane do ładowania, przekształcania i zapisywania pliku.  
`Image` jest podstawową klasą reprezentującą dokument PSD w pamięci.  
`RotateFlipType` wymienia obsługiwane operacje obrotu i odbicia.  
`JpegOptions` konfiguruje ustawienia wyjściowe JPEG, takie jak jakość.  

```java
import com.aspose.psd.Image;
import com.aspose.psd.RotateFlipType;

import com.aspose.psd.imageoptions.JpegOptions;
```

## Jak skonwertować PSD do JPEG po obróceniu?

Załaduj źródłowy PSD, zastosuj obrót o 270 stopni i od razu zapisz jako JPEG. Ten trzyetapowy proces trwa poniżej sekundy dla typowych obrazów 10 MP na nowoczesnym procesorze, co czyni go idealnym do zadań wsadowych o wysokiej przepustowości. Przetwarzając tylko niezbędne dane obrazu, zużycie pamięci pozostaje niskie, a powstały JPEG zachowuje jakość wizualną przy zmniejszeniu rozmiaru pliku.

### Krok 1: Załaduj plik PSD

`Image` jest podstawową klasą Aspose.PSD, która reprezentuje pojedynczy dokument PSD w pamięci. Tworzenie jej instancji odczytuje tylko informacje nagłówka, co utrzymuje niskie zużycie pamięci.

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";
Image image = Image.load(sourceFile);
```

### Krok 2: Obróć obraz o 270 stopni

`rotateFlip` wykonuje określony obrót i opcjonalne odbicie obrazu. `RotateFlipType.Rotate270FlipNone` obraca płótno o 270 stopni zgodnie z ruchem wskazówek zegara, pozostawiając orientację obrazu niezmienioną.

```java
image.rotateFlip(RotateFlipType.Rotate270FlipNone);
```

> **Wskazówka:** Jeśli potrzebujesz także odbić obraz poziomo lub pionowo, wybierz inny `RotateFlipType`, np. `Rotate90FlipX` lub `Rotate180FlipY`.

### Krok 3: Konwertuj PSD do JPEG i zapisz

`JpegOptions` definiuje parametry specyficzne dla JPEG, takie jak jakość kompresji. Metoda `save` zapisuje przekształcony obraz na dysk w żądanym formacie.

```java
String destName = dataDir + "RotatedImage_out.jpg";
image.save(destName, new JpegOptions());
```

Plik `RotatedImage_out.jpg` zawiera teraz oryginalną zawartość PSD obróconą o 270 stopni i zapisaną jako JPEG.

## Typowe problemy i rozwiązania

| Problem | Rozwiązanie |
|-------|----------|
| **Obraz jest odwrócony do góry nogami** | Sprawdź, czy użyto `Rotate270FlipNone`. Dla obrotu o 90 stopni zgodnie z ruchem wskazówek zegara użyj `Rotate90FlipNone`. |
| **Plik wyjściowy jest uszkodzony** | Upewnij się, że folder docelowy istnieje i masz uprawnienia do zapisu. |
| **Wyjątek licencyjny** | Zainstaluj tymczasową lub stałą licencję Aspose.PSD przed załadowaniem obrazu w środowisku produkcyjnym. |

## Najczęściej zadawane pytania

**Q: Czy Aspose.PSD jest kompatybilny z różnymi formatami obrazów?**  
A: Tak, Aspose.PSD obsługuje PSD, JPEG, PNG, BMP, GIF, TIFF i wiele innych formatów rastrowych.

**Q: Czy mogę zastosować własne obroty, a nie tylko predefiniowane odbicia?**  
A: Oczywiście! Chociaż `RotateFlipType` zapewnia typowe kąty, możesz łączyć wiele wywołań lub używać macierzy transformacji dla dowolnych kątów.

**Q: Jak przekonwertować obrócony PSD na inny format, np. PNG?**  
A: Zastąp `JpegOptions` klasą `PngOptions` (lub odpowiednią klasą opcji) w metodzie `save`.

**Q: Gdzie mogę znaleźć dodatkowe wsparcie lub pomoc?**  
A: Aby uzyskać pomoc społeczności, odwiedź [Forum Aspose.PSD](https://forum.aspose.com/c/psd/34).

**Q: Czy dostępna jest darmowa wersja próbna?**  
A: Tak, możesz wypróbować Aspose.PSD korzystając z [darmowej wersji próbnej](https://releases.aspose.com/).

**Q: Jak uzyskać tymczasową licencję?**  
A: Jeśli potrzebujesz tymczasowej licencji, możesz ją uzyskać [tutaj](https://purchase.aspose.com/temporary-license/).

**Ostatnia aktualizacja:** 2026-05-19  
**Testowano z:** Aspose.PSD for Java 24.12  
**Autor:** Aspose  

{{< blocks/products/products-backtop-button >}}

## Powiązane tutoriale

- [Konwertuj PSD do formatów obrazów rastrowych przy użyciu Aspose.PSD dla Javy](/psd/java/advanced-techniques/convert-psd-to-raster-formats/)
- [Konwertuj PSD do PNG i obróć warstwy w plikach PSD przy użyciu Javy](/psd/java/advanced-psd-layer-features-effects/rotate-layers-psd-files/)
- [Jak obrócić obraz w Javie przy użyciu Aspose.PSD](/psd/java/advanced-image-manipulation/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}