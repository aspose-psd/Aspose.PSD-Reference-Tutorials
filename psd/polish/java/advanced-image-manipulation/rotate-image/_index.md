---
date: 2026-02-12
description: Dowiedz się, jak obracać obraz i jak obrócić obraz o 270 stopni przy
  użyciu Aspose.PSD for Java. Ten przewodnik obejmuje obracanie plików PSD, odbijanie
  obrazów oraz konwertowanie PSD na JPEG bez Photoshopa.
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

W tym **tutorialu przetwarzania obrazów w java** odkryjesz **jak obrócić obraz** o 270 stopni szybko i niezawodnie przy użyciu Aspose.PSD dla Javy. Niezależnie od tego, czy tworzysz narzędzie do edycji zdjęć, automatyzujesz konwersje wsadowe, czy po prostu potrzebujesz zmienić orientację warstwy PSD, biblioteka wykonuje zadanie bezproblemowo. Poruszymy także techniki **flip image java** oraz konwersję obróconego PSD do JPEG, abyś uzyskał kompletny przepływ pracy od początku do końca bez Photoshopa.

## Szybkie odpowiedzi
- **Jaką bibliotekę obsługuje obrót?** Aspose.PSD dla Javy  
- **Jaki kąt obrotu jest użyty w przykładzie?** 270 stopni  
- **Czy mogę także odbić obraz?** Tak – użyj opcji `RotateFlipType`, np. `Rotate90FlipX`  
- **Jak zapisać wynik?** W przykładzie zapisujemy jako JPEG przy użyciu `JpegOptions`  
- **Czy potrzebna jest licencja do produkcji?** Do użytku komercyjnego wymagana jest ważna licencja Aspose.PSD  

## Co to znaczy „obrócić obraz o 270 stopni”?
Obrócenie obrazu o 270 stopni oznacza przekształcenie obrazu o trzy czwarte pełnego obrotu w prawo (lub 90 stopni w lewo). W wielu scenariuszach edycji graficznej taka orientacja odpowiada pierwotnemu układowi portretowemu po serii transformacji.

## Dlaczego używać Aspose.PSD do tego zadania?
- **Pełne wsparcie PSD** – działa z warstwami, maskami i obiektami korekcyjnymi.  
- **Brak wymogu natywnego Photoshopa** – działa na dowolnym środowisku Java.  
- **Proste API** – pojedyncze wywołanie metody (`rotateFlip`) obsługuje obrót i odbicie.  
- **Łatwa konwersja formatów** – eksport bezpośrednio do JPEG, PNG lub innych popularnych formatów.

## Jak obrócić obraz przy użyciu Aspose.PSD dla Javy
Poniżej znajdziesz przewodnik krok po kroku, który pokaże, jak wczytać PSD, zastosować obrót o 270°, opcjonalnie odbić obraz i na końcu zapisać wynik jako JPEG.

### Wymagania wstępne

Zanim rozpoczniesz, upewnij się, że masz:

- **Bibliotekę Aspose.PSD dla Javy** zainstalowaną. Możesz ją pobrać i zapoznać się z pełną dokumentacją API [tutaj](https://reference.aspose.com/psd/java/).  
- Środowisko programistyczne Java (JDK 8 lub wyższy).  
- Przykładowy plik PSD, który chcesz obrócić. Zaktualizuj zmienną `sourceFile` w kodzie, podając prawidłową ścieżkę do swojego pliku.

### Importowanie pakietów

Rozpocznij od zaimportowania niezbędnych klas z pakietu Aspose.PSD:

```java
import com.aspose.psd.Image;
import com.aspose.psd.RotateFlipType;

import com.aspose.psd.imageoptions.JpegOptions;
```

### Krok 1: Wczytaj obraz

Utwórz instancję `Image`, wskazującą na Twój plik PSD źródłowy:

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";
Image image = Image.load(sourceFile);
```

### Krok 2: Obróć obraz o 270 stopni

Użyj metody `rotateFlip` z wartością `RotateFlipType.Rotate270FlipNone`, aby uzyskać obrót o 270 stopni bez dodatkowego odbicia:

```java
image.rotateFlip(RotateFlipType.Rotate270FlipNone);
```

> **Pro tip:** Jeśli potrzebujesz także odbić obraz w poziomie lub pionie, wybierz inny `RotateFlipType`, np. `Rotate90FlipX` lub `Rotate180FlipY`. To najczęstszy sposób wykonywania operacji **flip image java**.

### Krok 3: Konwertuj PSD do JPEG i zapisz

Po obróceniu możesz **konwertować PSD do JPEG** (lub innego obsługiwanego formatu) przy użyciu odpowiedniej klasy opcji:

```java
String destName = dataDir + "RotatedImage_out.jpg";
image.save(destName, new JpegOptions());
```

Plik `RotatedImage_out.jpg` zawiera teraz oryginalną zawartość PSD obróconą o 270 stopni i zapisaną jako JPEG.

## Dlaczego to ważne – rzeczywiste przypadki użycia
- **Przetwarzanie wsadowe katalogów produktów** – obróć dziesiątki zasobów PSD do jednolitej orientacji przed publikacją.  
- **Automatyczne generowanie miniatur** – twórz poprawnie skierowane podglądy dla galerii internetowych bez otwierania Photoshopa.  
- **Backendy aplikacji mobilnych** – zmień orientację przesłanych przez użytkowników plików PSD po stronie serwera, używając czystej Javy.

## Typowe problemy i ich rozwiązywanie

| Problem | Rozwiązanie |
|-------|----------|
| **Obraz jest odwrócony do góry nogami** | Upewnij się, że użyłeś `Rotate270FlipNone`. Dla obrotu o 90 stopni w prawo użyj `Rotate90FlipNone`. |
| **Plik wyjściowy jest uszkodzony** | Sprawdź, czy docelowy folder istnieje i masz uprawnienia do zapisu. |
| **Wyjątek licencyjny** | Zainstaluj tymczasową lub stałą licencję Aspose.PSD przed wczytaniem obrazu w środowisku produkcyjnym. |
| **Potrzeba obrotu obrazu bez Photoshopa** | To API wykonuje obrót w całości w kodzie, eliminując zależność od Photoshopa. |
| **Chcę odbić obraz w ramach tej samej operacji** | Użyj innych wartości `RotateFlipType`, np. `Rotate90FlipX` (dotyczy **how to flip image**). |

## Najczęściej zadawane pytania

**P: Czy Aspose.PSD jest kompatybilny z różnymi formatami obrazu?**  
O: Tak, Aspose.PSD obsługuje PSD, JPEG, PNG, BMP, GIF i wiele innych formatów rastrowych.

**P: Czy mogę zastosować własne kąty obrotu, a nie tylko predefiniowane odbicia?**  
O: Oczywiście! Choć `RotateFlipType` zapewnia typowe kąty, możesz łączyć wielokrotne wywołania lub używać macierzy transformacji dla dowolnych kątów.

**P: Jak skonwertować obrócony PSD do innego formatu, np. PNG?**  
O: Zamień `JpegOptions` na `PngOptions` (lub odpowiednią klasę opcji) w metodzie `save`.

**P: Gdzie mogę znaleźć dodatkowe wsparcie lub pomoc?**  
O: Pomoc społeczności znajdziesz na [forum Aspose.PSD](https://forum.aspose.com/c/psd/34).

**P: Czy dostępna jest darmowa wersja próbna?**  
O: Tak, możesz wypróbować Aspose.PSD w ramach [darmowej wersji próbnej](https://releases.aspose.com/).

**P: Jak uzyskać tymczasową licencję?**  
O: Tymczasową licencję możesz otrzymać [tutaj](https://purchase.aspose.com/temporary-license/).

**P: Czy to rozwiązanie działa na serwerach bez interfejsu graficznego?**  
O: Tak, Aspose.PSD dla Javy działa w każdym standardowym środowisku JVM, co czyni go idealnym dla potoków CI/CD lub funkcji w chmurze.

## Podsumowanie

Teraz wiesz, **jak obrócić obraz** o 270 stopni przy użyciu Aspose.PSD dla Javy, **jak odbić obraz** w razie potrzeby oraz jak wyeksportować wynik do JPEG. Ten prosty przepływ pracy może być włączony do większych, opartych na Javie, pipeline’ów przetwarzania obrazów, dając pełną kontrolę nad manipulacją PSD bez konieczności korzystania z Photoshopa.

---

**Ostatnia aktualizacja:** 2026-02-12  
**Testowano z:** Aspose.PSD dla Javy 24.12  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}