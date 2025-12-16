---
date: 2025-12-15
description: Naucz się konwertować pliki PSD na PNG i obracać warstwy PSD w Javie
  przy użyciu Aspose.PSD. Przewodnik krok po kroku z przykładami kodu.
linktitle: Convert PSD to PNG and Rotate Layers in PSD Files using Java
second_title: Aspose.PSD Java API
title: Konwertuj PSD na PNG i obracaj warstwy w plikach PSD przy użyciu Javy
url: /pl/java/advanced-psd-layer-features-effects/rotate-layers-psd-files/
weight: 21
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Konwertuj PSD do PNG i Obracaj warstwy w plikach PSD przy użyciu Javy

## Wprowadzenie
Jeśli potrzebujesz **konwertować PSD do PNG** jednocześnie obracając warstwy, ten przewodnik jest dla Ciebie. Niezależnie od tego, czy tworzysz narzędzie do przetwarzania wsadowego, czy integrujesz manipulację obrazami w usłudze internetowej, programowe podejście oszczędza czas i eliminuje zależność od Adobe Photoshop. W tym tutorialu pokażemy Ci **jak obracać warstwy PSD** i wyeksportować wynik jako PNG przy użyciu biblioteki Aspose.PSD dla Javy. Zrolujmy rękawy i sprawmy, by Twój przepływ pracy projektowej działał płynnie!

## Szybkie odpowiedzi
- **Jakiej biblioteki mogę użyć?** Aspose.PSD for Java  
- **Czy mogę jednocześnie obracać i konwertować?** Tak – najpierw obróć PSD, a potem zapisz jako PNG  
- **Czy potrzebna jest licencja?** Darmowa wersja próbna działa do testów; licencja płatna jest wymagana w produkcji  
- **Jaką wersję Javy obsługuje?** Java 8 i nowsze  
- **Czy wyjściowy PNG jest przezroczysty?** Tak, gdy ustawisz `PngColorType.TruecolorWithAlpha`

## Co oznacza „konwertować PSD do PNG”
Konwersja dokumentu Photoshop (PSD) do obrazu PNG oznacza wyodrębnienie treści wizualnej — w tym wszystkich warstw, masek i przezroczystości — do powszechnie obsługiwanego formatu rastrowego. PNG zachowuje kanały alfa, co czyni go idealnym dla grafiki internetowej, miniatur i dalszego przetwarzania obrazów.

## Dlaczego używać Aspose.PSD for Java do konwersji PSD do PNG i obracania warstw PSD?
- **Nie wymaga Photoshopa** – działa na dowolnym serwerze lub w środowisku CI  
- **Pełne wsparcie warstw** – zachowuje przezroczystość i efekty warstw  
- **Proste API** – obracaj, odwracaj i zapisuj przy użyciu kilku wywołań metod  
- **Wieloplatformowe** – działa na Windows, Linux i macOS  

## Wymagania wstępne
Zanim przejdziemy do kodu, upewnij się, że masz następujące elementy:

- **Java Development Kit (JDK)** – pobierz ze [strony Oracle](https://www.oracle.com/java/technologies/javase-downloads.html).  
- **Zintegrowane środowisko programistyczne (IDE)** – IntelliJ IDEA, Eclipse lub NetBeans będą odpowiednie.  
- **Biblioteka Aspose.PSD for Java** – pobierz najnowszy plik JAR ze [strony wydań](https://releases.aspose.com/psd/java/).  
- **Podstawowa znajomość Javy** – znajomość klas, obiektów i obsługi wyjątków.  

## Przewodnik krok po kroku

### Krok 1: Skonfiguruj projekt Java
Utwórz nowy projekt Java w swoim IDE i dodaj plik JAR Aspose.PSD do ścieżki kompilacji projektu.

### Krok 2: Zaimportuj wymagane klasy
Dodaj następujące importy na początku pliku źródłowego Java:

```java
import com.aspose.psd.Image;
import com.aspose.psd.RotateFlipType;
import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.PngOptions;
```

Te klasy zapewniają dostęp do ładowania obrazu, rotacji oraz opcji specyficznych dla PNG.

### Krok 3: Zdefiniuj ścieżki plików
Określ, gdzie znajduje się źródłowy plik PSD oraz gdzie mają być zapisywane pliki wyjściowe.

```java
String dataDir = "Your Document Directory"; // Change this to your actual document directory.
String sourceFile = dataDir + "1.psd"; // Source PSD file
String pngPath = dataDir + "RotateFlipTest2617.png"; // Output PNG file path
String psdPath = dataDir + "RotateFlipTest2617.psd"; // Output PSD file path
```

> **Wskazówka:** Używaj ścieżki bezwzględnej podczas testów, aby uniknąć błędów „plik nie znaleziony”.

### Krok 4: Załaduj plik PSD
Załaduj PSD do obiektu, którym można manipulować.

```java
PsdImage im = (PsdImage) Image.load(sourceFile);
```

Teraz `im` reprezentuje cały dokument Photoshop, włącznie ze wszystkimi warstwami.

### Krok 5: Obróć obraz (Jak obrócić PSD)
Wybierz typ rotacji z `RotateFlipType`. W tym przykładzie obracamy o 270° i odwracamy obie osie.

```java
int flipType = RotateFlipType.Rotate270FlipXY; // Choose the rotation type
im.rotateFlip(flipType); // Rotate the image
```

Śmiało eksperymentuj z innymi wartościami, takimi jak `Rotate90FlipNone` lub `Rotate180FlipX`.

### Krok 6: Zapisz obrócony obraz jako PNG (konwertuj PSD do PNG)
Skonfiguruj opcje PNG, aby zachować przezroczystość, a następnie zapisz.

```java
PngOptions options = new PngOptions();
options.setColorType(PngColorType.TruecolorWithAlpha); // Preserve transparency
im.save(pngPath, options); // Save the rotated image
```

Powstały PNG zachowuje przezroczystość warstw, co czyni go gotowym do użycia w sieci.

### Krok 7: Zapisz zmodyfikowany PSD (opcjonalnie)
Jeśli potrzebujesz również nowego PSD z zastosowaną rotacją, zapisz go ponownie.

```java
im.save(psdPath);
```

Masz teraz zarówno podgląd PNG, jak i zaktualizowany plik PSD.

## Typowe problemy i rozwiązania
- **Plik nie znaleziony:** Upewnij się, że `dataDir` kończy się separatorem ścieżki (`/` lub `\`).  
- **OutOfMemoryError przy dużych PSD:** Zwiększ rozmiar sterty JVM (`-Xmx2g`).  
- **Utrata przezroczystości:** Upewnij się, że ustawiono `PngColorType.TruecolorWithAlpha`; w przeciwnym razie PNG zostanie zapisany bez alfa.

## FAQ

### Czy mogę obrócić konkretną warstwę w pliku PSD?
Tak, możesz użyć `Layer.rotateFlip()` na pojedynczych warstwach po iteracji przez `im.getLayers()`.

### Czy istnieją ograniczenia wydajnościowe w Aspose.PSD for Java?
Biblioteka obsługuje większość plików wydajnie, ale bardzo duże pliki PSD (>500 MB) mogą wymagać dodatkowej pamięci.

### Czy Aspose.PSD jest darmowy?
Aspose oferuje darmową wersję próbną, ale do produkcji wymagana jest płatna licencja. Sprawdź [licencję tymczasową](https://purchase.aspose.com/temporary-license/) do testów.

### Gdzie mogę znaleźć szczegółową dokumentację?
Kompleksową dokumentację znajdziesz pod adresem [Aspose.PSD Documentation](https://reference.aspose.com/psd/java/).

### Co zrobić, jeśli napotkam problemy podczas używania Aspose.PSD?
Skontaktuj się po pomoc poprzez [Forum wsparcia Aspose](https://forum.aspose.com/c/psd/34).

## Dodatkowe często zadawane pytania

**Q: Czy konwersja PSD do PNG zachowuje efekty warstw?**  
**A:** Tak, gdy zapisujesz z `PngColorType.TruecolorWithAlpha`, większość efektów wizualnych jest rasteryzowana do PNG.

**Q: Czy mogę przetwarzać wsadowo wiele plików PSD?**  
**A:** Oczywiście. Umieść kod w pętli, która iteruje po katalogu z plikami PSD.

**Q: Czy można ustawić poziom kompresji PNG?**  
**A:** Klasa `PngOptions` udostępnia metodę `setCompressionLevel(int)` do precyzyjnego dostosowania.

**Q: Czy muszę zamknąć obiekt obrazu?**  
**A:** `PsdImage` implementuje `Closeable`; wywołaj `im.close()` w bloku `finally` lub użyj try‑with‑resources.

**Q: Czy obrócony PNG będzie miał te same wymiary co oryginał?**  
**A:** Obrót o 90° lub 270° zamienia szerokość i wysokość. PNG odzwierciedli nową orientację.

## Zakończenie
Korzystając z Aspose.PSD for Java, możesz **konwertować PSD do PNG** i **obracać warstwy PSD** za pomocą kilku linijek kodu. To podejście eliminuje potrzebę używania Photoshopa, przyspiesza zautomatyzowane przepływy pracy i daje pełną kontrolę nad wyjściem obrazu. Wypróbuj to w swoich projektach i zobacz, ile czasu zaoszczędzisz!

---

**Last Updated:** 2025-12-15  
**Tested With:** Aspose.PSD for Java 24.11  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}