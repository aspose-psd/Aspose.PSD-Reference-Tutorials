---
date: 2025-12-06
description: Dowiedz się, jak obrócić obraz o 270 stopni przy użyciu Aspose.PSD for
  Java. Ten przewodnik pokazuje, jak obracać pliki PSD, odwracać obrazy i konwertować
  PSD na JPEG.
linktitle: Rotate Image 270 Degrees
second_title: Aspose.PSD Java API
title: Jak obrócić obraz o 270 stopni przy użyciu Aspose.PSD dla Javy
url: /pl/java/advanced-image-manipulation/rotate-image/
weight: 19
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Obróć obraz o 270 stopni przy użyciu Aspose.PSD dla Javy

## Wprowadzenie

W tym **java image processing tutorial** odkryjesz, jak **rotate image 270 degrees** szybko i niezawodnie przy użyciu Aspose.PSD for Java. Niezależnie od tego, czy tworzysz narzędzie do edycji zdjęć, automatyzujesz konwersje wsadowe, czy po prostu potrzebujesz zmienić orientację warstwy PSD, biblioteka sprawia, że zadanie jest bezbolesne. Poruszymy także temat odbijania obrazów oraz konwersji obróconego PSD do JPEG, abyś uzyskał kompletny przepływ pracy od początku do końca.

## Szybkie odpowiedzi
- **Jaką bibliotekę obsługuje rotację?** Aspose.PSD for Java  
- **Jaki kąt rotacji używa przykład?** 270 stopni  
- **Czy mogę także odbić obraz?** Tak – użyj opcji `RotateFlipType` takich jak `Rotate90FlipX`  
- **Jak zapisać wynik?** W przykładzie zapisujemy jako JPEG używając `JpegOptions`  
- **Czy potrzebna jest licencja do produkcji?** Wymagana jest ważna licencja Aspose.PSD do użytku komercyjnego  

## Co oznacza „obrócić obraz o 270 stopni”?
Obrócenie obrazu o 270 stopni oznacza obrócenie zdjęcia o trzy czwarte pełnego obrotu zgodnie z ruchem wskazówek zegara (lub o 90 stopni przeciwnie do ruchu wskazówek zegara). W wielu scenariuszach edycji graficznej taka orientacja odpowiada pierwotnemu układowi portretowemu po serii transformacji.

## Dlaczego używać Aspose.PSD do tego zadania?
- **Pełne wsparcie PSD** – działa z warstwami, maskami i obiektami korekcyjnymi.  
- **Nie wymaga natywnego Photoshopa** – działa na dowolnym środowisku Java.  
- **Proste API** – pojedyncze wywołanie metody (`rotateFlip`) obsługuje rotację i odbicie.  
- **Łatwa konwersja formatów** – eksport bezpośrednio do JPEG, PNG lub innych popularnych formatów.

## Wymagania wstępne

Zanim zaczniesz, upewnij się, że masz:

- **Bibliotekę Aspose.PSD for Java** zainstalowaną. Możesz ją pobrać i zobaczyć pełną dokumentację API [tutaj](https://reference.aspose.com/psd/java/).  
- Środowisko programistyczne Java (JDK 8 lub wyższy).  
- Przykładowy plik PSD, który chcesz obrócić. Zaktualizuj zmienną `sourceFile` w kodzie, podając prawidłową ścieżkę do pliku.

## Importowanie pakietów

Rozpocznij od zaimportowania niezbędnych klas z pakietu Aspose.PSD:

```java
import com.aspose.psd.Image;
import com.aspose.psd.RotateFlipType;

import com.aspose.psd.imageoptions.JpegOptions;
```

## Jak obrócić PSD – Krok 1: Załaduj obraz

Utwórz instancję `Image`, która wskazuje na Twój źródłowy plik PSD:

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";
Image image = Image.load(sourceFile);
```

## Jak obrócić PSD – Krok 2: Obróć obraz o 270 stopni

Użyj metody `rotateFlip` z `RotateFlipType.Rotate270FlipNone`, aby uzyskać rotację o 270 stopni bez żadnego odbicia:

```java
image.rotateFlip(RotateFlipType.Rotate270FlipNone);
```

> **Pro tip:** Jeśli potrzebujesz także odbić obraz poziomo lub pionowo, wybierz inny `RotateFlipType`, taki jak `Rotate90FlipX` lub `Rotate180FlipY`.

## Jak obrócić PSD – Krok 3: Konwertuj PSD do JPEG i zapisz

Po obróceniu możesz **convert PSD to JPEG** (lub innego obsługiwanego formatu) używając odpowiedniej klasy opcji:

```java
String destName = dataDir + "RotatedImage_out.jpg";
image.save(destName, new JpegOptions());
```

Plik `RotatedImage_out.jpg` zawiera teraz oryginalną zawartość PSD obróconą o 270 stopni i zapisaną jako JPEG.

## Typowe problemy i rozwiązania

| Problem | Rozwiązanie |
|-------|----------|
| **Image appears upside‑down** | Sprawdź, czy użyto `Rotate270FlipNone`. Dla rotacji o 90 stopni zgodnie z ruchem wskazówek zegara użyj `Rotate90FlipNone`. |
| **Output file is corrupted** | Upewnij się, że folder docelowy istnieje i masz uprawnienia do zapisu. |
| **License exception** | Zainstaluj tymczasową lub stałą licencję Aspose.PSD przed załadowaniem obrazu w środowisku produkcyjnym. |

## Najczęściej zadawane pytania

**Q: Czy Aspose.PSD jest kompatybilny z różnymi formatami obrazów?**  
A: Tak, Aspose.PSD obsługuje PSD, JPEG, PNG, BMP, GIF i wiele innych formatów rastrowych.

**Q: Czy mogę zastosować własne rotacje, a nie tylko predefiniowane odbicia?**  
A: Oczywiście! Choć `RotateFlipType` zapewnia typowe kąty, możesz łączyć wiele wywołań lub używać macierzy transformacji dla dowolnych kątów.

**Q: Jak skonwertować obrócony PSD do innego formatu, np. PNG?**  
A: Zastąp `JpegOptions` klasą `PngOptions` (lub odpowiednią klasą opcji) w metodzie `save`.

**Q: Gdzie mogę znaleźć dodatkowe wsparcie lub pomoc?**  
A: Pomoc społeczności znajdziesz na [Aspose.PSD Forum](https://forum.aspose.com/c/psd/34).

**Q: Czy dostępna jest darmowa wersja próbna?**  
A: Tak, możesz wypróbować Aspose.PSD korzystając z [free trial](https://releases.aspose.com/).

**Q: Jak uzyskać tymczasową licencję?**  
A: Jeśli potrzebujesz tymczasowej licencji, możesz ją uzyskać [here](https://purchase.aspose.com/temporary-license/).

## Zakończenie

Nauczyłeś się teraz, jak **rotate image 270 degrees** przy użyciu Aspose.PSD for Java, odbijać obrazy w razie potrzeby oraz eksportować wynik do JPEG. Ten prosty przepływ pracy może być zintegrowany z większymi pipeline'ami przetwarzania obrazu opartymi na Javie, dając pełną kontrolę nad manipulacją PSD bez konieczności korzystania z Photoshopa.

---

**Last Updated:** 2025-12-06  
**Tested With:** Aspose.PSD for Java 24.12  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}