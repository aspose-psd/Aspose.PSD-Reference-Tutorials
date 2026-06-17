---
date: 2026-02-17
description: Dowiedz się, jak konwertować pliki PSD na PNG, zachować przezroczystość
  PNG oraz obracać warstwy PSD w Javie przy użyciu Aspose.PSD. Przewodnik krok po
  kroku z przykładami kodu.
linktitle: Convert PSD to PNG and Rotate Layers in PSD Files using Java
second_title: Aspose.PSD Java API
title: Konwertuj PSD na PNG i obracaj warstwy w plikach PSD przy użyciu Javy
url: /pl/java/advanced-psd-layer-features-effects/rotate-layers-psd-files/
weight: 21
---

 2026-02-17  
**Tested With:** Aspose.PSD for Java 24.11  
**Author:** Aspose  

Keep as is.

Then closing shortcodes.

Now produce final content.

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Konwertowanie PSD do PNG i obracanie warstw w plikach PSD przy użyciu Javy

## Wprowadzenie
Jeśli potrzebujesz **konwertować PSD do PNG** jednocześnie obracając warstwy, ten przewodnik jest dla Ciebie. Niezależnie od tego, czy tworzysz narzędzie do przetwarzania wsadowego, usługę internetową wymagającą manipulacji obrazem w locie, czy po prostu automatyzujesz przepływ pracy projektanta, programowe podejście oszczędza czas i eliminuje zależność od Adobe Photoshop. W tym tutorialu pokażemy **jak obracać warstwy PSD** i eksportować wynik jako PNG przy użyciu biblioteki Aspose.PSD dla Javy. Zaciągnijmy rękawy i sprawmy, by Twój workflow projektowy działał płynnie!

## Szybkie odpowiedzi
- **Jakiej biblioteki mogę użyć?** Aspose.PSD for Java  
- **Czy mogę jednocześnie obrócić i przekonwertować?** Tak – najpierw obracamy PSD, a potem zapisujemy jako PNG  
- **Czy potrzebna jest licencja?** Bezpłatna wersja próbna działa do testów; licencja płatna jest wymagana w produkcji  
- **Jaką wersję Javy obsługuje?** Java 8 i nowsze  
- **Czy wyjściowy PNG jest przezroczysty?** Tak, gdy ustawisz `PngColorType.TruecolorWithAlpha`

## Co oznacza „konwertowanie PSD do PNG”?
Konwersja dokumentu Photoshop (PSD) do obrazu PNG oznacza wyodrębnienie treści wizualnej — w tym wszystkich warstw, masek i przezroczystości — do powszechnie obsługiwanego formatu rastrowego. PNG zachowuje kanały alfa, co czyni go idealnym do grafiki internetowej, miniatur i dalszego przetwarzania obrazów.

## Dlaczego warto używać Aspose.PSD for Java do konwertowania PSD do PNG i obracania warstw PSD?
- **Nie wymaga Photoshopa** – działa na dowolnym serwerze lub w środowisku CI  
- **Pełne wsparcie warstw** – zachowuje przezroczystość i efekty warstw  
- **Proste API** – obracaj, odwracaj i zapisuj przy użyciu kilku wywołań metod  
- **Wieloplatformowość** – działa na Windows, Linux i macOS  
- **Konwersja obrazów w Javie** stała się łatwa dzięki jednej bibliotece  

## Wymagania wstępne
Zanim przejdziesz do kodu, upewnij się, że masz następujące elementy:

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

Te klasy zapewniają dostęp do ładowania obrazu, obracania i opcji specyficznych dla PNG.

### Krok 3: Zdefiniuj ścieżki plików
Określ, gdzie znajduje się źródłowy plik PSD oraz gdzie mają być zapisane pliki wyjściowe.

```java
String dataDir = "Your Document Directory"; // Change this to your actual document directory.
String sourceFile = dataDir + "1.psd"; // Source PSD file
String pngPath = dataDir + "RotateFlipTest2617.png"; // Output PNG file path
String psdPath = dataDir + "RotateFlipTest2617.psd"; // Output PSD file path
```

> **Wskazówka:** Użyj ścieżki bezwzględnej podczas testów, aby uniknąć błędów „plik nie znaleziony”.

### Krok 4: Załaduj plik PSD
Załaduj PSD do obiektu, którym można manipulować.

```java
PsdImage im = (PsdImage) Image.load(sourceFile);
```

Teraz `im` reprezentuje cały dokument Photoshop, włącznie ze wszystkimi warstwami.

### Krok 5: Obróć obraz (Jak obrócić PSD)
Wybierz typ obrotu z `RotateFlipType`. W tym przykładzie obracamy o 270° i odwracamy obie osie.

```java
int flipType = RotateFlipType.Rotate270FlipXY; // Choose the rotation type
im.rotateFlip(flipType); // Rotate the image
```

Śmiało eksperymentuj z innymi wartościami, takimi jak `Rotate90FlipNone` lub `Rotate180FlipX`. To jest część tutorialu **jak obrócić PSD**.

### Krok 6: Zapisz obrócony obraz jako PNG (konwertowanie PSD do PNG)
Skonfiguruj opcje PNG, aby zachować przezroczystość, a następnie zapisz.

```java
PngOptions options = new PngOptions();
options.setColorType(PngColorType.TruecolorWithAlpha); // Preserve transparency
im.save(pngPath, options); // Save the rotated image
```

Wynikowy PNG zachowuje przezroczystość warstw, zapewniając **zachowanie przezroczystości PNG** przy dalszym użyciu.

### Krok 7: Zapisz zmodyfikowany PSD (opcjonalnie)
Jeśli potrzebujesz również nowego pliku PSD z zastosowanym obrotem, zapisz go ponownie.

```java
im.save(psdPath);
```

Masz teraz zarówno podgląd PNG, jak i zaktualizowany plik PSD.

## Częste problemy i rozwiązania
- **Plik nie znaleziony:** Upewnij się, że `dataDir` kończy się separatorem ścieżki (`/` lub `\`).  
- **OutOfMemoryError przy dużych PSD:** Zwiększ rozmiar sterty JVM (`-Xmx2g`).  
- **Utrata przezroczystości:** Upewnij się, że ustawiono `PngColorType.TruecolorWithAlpha`; w przeciwnym razie PNG zostanie zapisany bez kanału alfa.  
- **Odwrócenie obrazu PSD nie działa jak oczekiwano:** Sprawdź ponownie wybraną stałą `RotateFlipType`; niektóre stałe łączą obrót i odwrócenie w jednym kroku.

## Najczęściej zadawane pytania

**P:** Czy mogę obrócić konkretną warstwę w pliku PSD?  
**O:** Tak, możesz użyć `Layer.rotateFlip()` na poszczególnych warstwach po iteracji przez `im.getLayers()`.

**P:** Czy istnieją ograniczenia wydajnościowe w Aspose.PSD for Java?  
**O:** Biblioteka radzi sobie efektywnie z większością plików, ale bardzo duże PSD (>500 MB) mogą wymagać dodatkowej pamięci.

**P:** Czy Aspose.PSD jest darmowy?  
**O:** Aspose oferuje bezpłatną wersję próbną, ale do produkcji wymagana jest płatna licencja. Sprawdź [tymczasową licencję](https://purchase.aspose.com/temporary-license/) do testów.

**P:** Gdzie mogę znaleźć szczegółową dokumentację?  
**O:** Kompleksową dokumentację znajdziesz pod adresem [Aspose.PSD Documentation](https://reference.aspose.com/psd/java/).

**P:** Co zrobić, jeśli napotkam problemy przy używaniu Aspose.PSD?  
**O:** Skontaktuj się po pomoc na [forum wsparcia Aspose](https://forum.aspose.com/c/psd/34).

**P:** Czy konwersja PSD do PNG zachowuje efekty warstw?  
**O:** Tak, przy zapisie z `PngColorType.TruecolorWithAlpha` większość efektów wizualnych jest rasteryzowana do PNG.

**P:** Czy mogę przetwarzać wsadowo wiele plików PSD?  
**O:** Oczywiście. Umieść kod w pętli iterującej po katalogu z plikami PSD.

**P:** Czy można ustawić poziom kompresji PNG?  
**O:** Klasa `PngOptions` udostępnia metodę `setCompressionLevel(int)` do precyzyjnego dostosowania.

**P:** Czy muszę zamknąć obiekt obrazu?  
**O:** `PsdImage` implementuje `Closeable`; wywołaj `im.close()` w bloku `finally` lub użyj try‑with‑resources.

**P:** Czy obrócony PNG będzie miał te same wymiary co oryginał?  
**O:** Obrót o 90° lub 270° zamienia szerokość i wysokość. PNG odzwierciedli nową orientację.

## Podsumowanie
Korzystając z Aspose.PSD for Java, możesz **konwertować PSD do PNG**, **zachować przezroczystość PNG** oraz **obracać warstwy PSD** przy użyciu zaledwie kilku linii kodu. To podejście eliminuje potrzebę Photoshopa, przyspiesza zautomatyzowane przepływy pracy i daje pełną kontrolę nad wynikiem obrazu. Wypróbuj je w swoich projektach i zobacz, ile czasu możesz zaoszczędzić!

---

**Last Updated:** 2026-02-17  
**Tested With:** Aspose.PSD for Java 24.11  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}